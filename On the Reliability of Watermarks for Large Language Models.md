---
title: On the Reliability of Watermarks for Large Language Models
author: John Kirchenbauer, Jonas Geiping, et al.
year: "2023"
Type: Article
DOI: ""
source: https://proceedings.mlr.press/v202/kirchenbauer23a.html
created: 2026-06-18
description: ""
tags:
  - op/acc/pending-review
  - tech/Ai/LLM
pdfORepub: "[[On the Reliability of Watermarks for LLMs Kirchenbauer 2023.pdf]]"
---
[[On the Reliability of Watermarks for LLMs Kirchenbauer 2023.pdf]]

## Full text (extracted from `On the Reliability of Watermarks for LLMs Kirchenbauer 2023.pdf`)

*Source:* `2PDF/On the Reliability of Watermarks for LLMs Kirchenbauer 2023.pdf`  
*Extracted:* 2026-06-18

```text
A Watermark for Large Language Models
John Kirchenbauer * 1 Jonas Geiping * 1 Yuxin Wen1 Jonathan Katz 1 Ian Miers 1 Tom Goldstein1
Abstract
Potential harms of large language models can be
mitigated by watermarking model output, i.e., em-
bedding signals into generated text that are invisi-
ble to humans but algorithmically detectable from
a short span of tokens. We propose a watermark-
ing framework for proprietary language models.
The watermark can be embedded with negligible
impact on text quality, and can be detected using
an efficient open-source algorithm without access
to the language model API or parameters. The
watermark works by selecting a randomized set
of “green” tokens before a word is generated, and
then softly promoting use of green tokens during
sampling. We propose a statistical test for de-
tecting the watermark with interpretable p-values,
and derive an information-theoretic framework
for analyzing the sensitivity of the watermark. We
test the watermark using a multi-billion parameter
model from the Open Pretrained Transformer
(OPT) family, and discuss robustness and security.
1. Introduction
Large language models (LLMs), such as the recently de-
veloped ChatGPT, can write documents, create executable
code, and answer questions, often with human-like capa-
bilities (Schulman et al., 2022). As these systems become
more pervasive, there is increasing risk that they may be
used for malicious purposes (Bergman et al., 2022; Mirsky
et al., 2023). These include social engineering and election
manipulation campaigns that exploit automated bots on so-
cial media platforms, creation of fake news and web content,
and use of AI systems for cheating on academic writing and
coding assignments. Furthermore, the proliferation of syn-
thetic data on the web complicates future dataset creation
efforts, as synthetic data is often inferior to human content
and must be detected and excluded before model training
Code is available at https://www.github.com/
jwkirchenbauer/lm-watermarking. *Equal contribu-
tion 1University of Maryland. Correspondence to: John Kirchen-
bauer <jkirchen@umd.edu>.
Proceedings of the 40 th International Conference on Machine
Learning, Honolulu, Hawaii, USA. PMLR 202, 2023. Copyright
2023 by the author(s).
…The watermark detection algorithm 
can be made public, enabling third 
parties (e.g., social media 
platforms) to run it themselves, or 
it can be kept private and run behind 
an API.  We seek a watermark with the 
following properties:
Prompt
No watermark
With watermark
- minimal marginal probability for a 
detection attempt. 
- Good speech frequency and energy 
rate reduction. 
- messages indiscernible to humans. 
- easy for humans to verify.
Extremely efficient on average term 
lengths and word frequencies on 
synthetic, microamount text (as little 
as 25 words) 
Very small and low-resource key/hash 
(e.g., 140 bits per key is sufficient 
for 99.999999999% of the Synthetic 
Internet
p-value 
Z-score
Num tokens
56
36
.31
7.4
.38
6e-14
Figure 1.Outputs of a language model, both with and without
the application of a watermark. The watermarked text, if written
by a human, is expected to contain 9 “green” tokens, yet it con-
tains 28. The probability of this happening by random chance is
≈ 6×10−14, leaving us extremely certain that this text is machine
generated. Words are marked with their respective colors. The
model is OPT-6.7B using multinomial sampling. Watermark
parameters are γ, δ= (0.25, 2). The prompt is the whole blue
paragraph marked below.
(Radford et al., 2022). For many reasons, the ability to de-
tect and audit the usage of machine-generated text becomes
a key principle of harm reduction for large language mod-
els (Bender et al., 2021; Crothers et al., 2022; Grinbaum &
Adomaitis, 2022).
In this work, we study watermarking of language
model output. A watermark is a hidden pattern in
text that is imperceptible to humans, while making
the text algorithmically identifiable as synthetic. We
propose an efficient watermark that makes synthetic
text detectable from short spans of tokens (as few as
25 tokens), while false-positives (where human text
is marked as machine-generated) are statistically im-
probable. The watermark detection algorithm can be
1
A Watermark for Large Language Models
made public, enabling third parties (e.g., social media
platforms) to run it themselves, or it can be kept private
and run behind an API. We seek a watermark with the
following properties:
• The watermark can be algorithmically detected with-
out any knowledge of the model parameters or access
to the language model API. This property allows the
detection algorithm to be open sourced even when the
model is not. This also makes detection cheap and fast
because the LLM does not need to be loaded or run.
• Watermarked text can be generated using a standard
language model without re-training.
• The watermark is detectable from only a contiguous
portion of the generated text. This way, the watermark
remains detectable when only a slice of the generation
is used to create a larger document.
• The watermark cannot be removed without modifying
a significant fraction of the generated tokens.
• We can compute a rigorous statistical measure of con-
fidence that the watermark has been detected.
1.1. Notation & Language model basics
Language models have a “vocabulary” V containing words
or word fragments known as “tokens.” Typical vocab-
ularies contain |V| = 50 , 000 tokens or more (Radford
et al., 2019; Liu et al., 2019). Consider a sequence of
T tokens {s(t)} ∈ VT . Entries with negative indices,
s(−Np), ··· , s(−1), represent a “prompt” of length Np and
s(0), ··· , s(T) are tokens generated by an AI system in re-
sponse to the prompt.
A language model (LM) for next word prediction, is a func-
tion f, often parameterized by a neural network, that accepts
as input a sequence of known tokens s(−Np), ··· , s(t−1),
which contains a prompt and the first t − 1 tokens already
produced by the language model, and then outputs a vector
of |V | logits, one for each word in the vocabulary. These
logits are then passed through a softmax operator to convert
them into a discrete probability distribution over the vocab-
ulary. The next token at position t is then sampled from this
distribution using either standard multinomial sampling, or
greedy sampling (greedy decoding) of the single most likely
next token. Additionally, a procedure such as beam search
can be employed to consider multiple possible sequences
before selecting the one with the overall highest score.
1.2. A caveat: The difficulty of watermarking
low-entropy sequences
Consider the following two sequences of tokens, with
prompts in red:
The quick brown fox jumps over the lazy dog
for(i=0;i<n;i++) sum+=array[i]
Were they produced by a human or by a language model?
Determining this is fundamentally hard because these se-
quences have low entropy; the first few tokens strongly
determine the following tokens.
Low entropy text creates two problems for watermarking.
First, both humans and machines provide similar if not
identical completions for low entropy prompts, making it
impossible to discern between them. Second, it is difficult
to watermark low entropy text, as any changes to the choice
of tokens may result in high perplexity, unexpected tokens
that degrade the quality of the text. Later, we rigorously de-
fine sentence entropy, and analyze its impact on watermark
detection.
2. A simple proof of concept
We start out by describing a simple “hard” red list watermark
in Algorithm 1 that is easy to analyze, easy to detect and
hard to remove. The simplicity of this approach comes at the
cost of poor generation quality on low entropy sequences.
We will discuss more sophisticated strategies later.
Algorithm 1 Text Generation with Hard Red List
Input: prompt, s(−Np) ··· s(−1)
for t = 0, 1, ··· do
1. Apply the language model to prior tokens
s(−Np) ··· s(t−1) to get a probability vector p(t)
over the vocabulary.
2. Compute a hash of token s(t−1), and use it to
seed a random number generator.
3. Using this seed, randomly partition the vocab-
ulary into a “green list” G and a “red list” R of
equal size.
4. Sample s(t) from G , never generating any token
in the red list.
end for
The method works by generating a pseudo-random red list
of tokens that are barred from appearing as s(t). The red list
generator is seeded with the prior token s(t−1), enabling the
red list to be reproduced later without access to the entire
generated sequence.
Detecting the watermark. While producing watermarked
text requires access to the language model, detecting the
watermark does not. A third party with knowledge of the
hash function and random number generator can re-produce
the red list for each token and count how many times the red
list rule is violated. We can detect the watermark by testing
2
A Watermark for Large Language Models
the following null hypothesis,
H0: The text sequence is generated with
no knowledge of the red list rule. (1)
Because the red list is chosen at random, a natural writer is
expected to violate the red list rule with half of their tokens,
while the watermarked model produces no violations. The
probability that a natural source produces T tokens without
violating the red list rule is only 1/2T , which is vanishingly
small even for short text fragments with a dozen words. This
enables detection of the watermark (rejection of H0) for,
e.g., a synthetic tweet.
A more robust detection approach uses a one proportion
z-test to evaluate the null hypothesis. If the null hypothesis
is true, then the number of green list tokens, denoted |s|G,
has expected value T/2 and variance T/4. The z-statistic
for this test is
z = 2(|s|G − T/2)/
√
T . (2)
We reject the null hypothesis and detect the watermark if z
is above a chosen threshold. Suppose we choose to reject
the null hypothesis if z >4. In this case, the probability of
a false positive is 3 × 10−5, which is the one-sided p-value
corresponding to z >4. At the same time, we will detect
any watermarked sequence with 16 or more tokens (the
minimum value of T that produces z = 4 when |s|G=T).
How hard is it to remove the watermark? The use of
the one proportion z-test makes removal of the watermark
difficult. Consider the case of a watermarked sequence
of length T = 1000. Suppose an adversary modifies 200
tokens in the sequence to add red list words and scrub the
watermark. A modified token at position t can violate the
red list rule at position t. Furthermore, the value of st
determines the red list for token st+1, and a maximally
adversarial choice of st will put st+1 in violation of the red
list rule as well. For this reason, 200 token flips can create
at most 400 violations of the red list rule. Unfortunately
for the attacker, this maximally adversarial sequence with
600 remaining green list tokens still produces a z-statistic of
2(600−1000/2)/
√
1000 ≈ 6.3, and a p-value of ≈ 10−10,
leaving the watermark readily detectable with extremely
high confidence. In general, removing the watermark of a
long sequence requires modifying roughly one quarter of
the tokens or more.
Note the analysis above assumes the attacker has complete
knowledge of the watermark, and each selected token is
maximally adversarial (which likely has a negative impact
on quality). Without knowledge of the watermark algorithm,
each flipped token has only a 50% chance of being in the
red list, as does the adjacent token. In this case, the attacker
above only creates 200 red list words (in expectation) by
modifying 200 tokens. Methods for keeping the watermark
algorithm secret but available via API are discussed in
Section 5.
Drawbacks of the hard red list rule. The hard red list rule
handles low entropy sequences in a simple way; it prevents
the language model from producing them. For example,
the token “Barack” is almost deterministically followed
by “Obama” in many text datasets, yet “Obama” may be
disallowed by the red list.
A better behavior is to use a “soft” watermarking rule that
is only active for high-entropy text that can be impercep-
tibly watermarked. As long as low-entropy sequences are
wrapped inside a passage with enough total entropy, the
passage will still easily trigger a watermark detector, solv-
ing the problem described in Section 1.2. Further, one can
combine the watermark with a beam search decoder that
“irons-in” the watermark. By searching the hypothesis space
of likely token sequences, candidates sequences with a high
density of green list tokens are found, resulting in a high
strength watermark with minimal perplexity cost.
3. A more sophisticated watermark
We now discuss the “soft” watermark that promotes the
use of the green list for high entropy tokens when many
good choices are available, while having little impact on the
choice of low-entropy tokens that are nearly deterministic.
To derive this watermark, we examine what happens in the
language model just before it produces a probability vector.
The last layer of the language model outputs a vector of
logits l(t). These logits get converted into a probability
vector p(t) using the softmax operator
p(t)
k = exp(l(t)
k )/
X
i
exp(l(t)
i ).
Rather than strictly prohibiting the red list tokens, Algorithm
2 adds a constant δ to the logits of the green list tokens.
The soft red list rule adaptively enforces the watermark in
situations where doing so will have little impact on quality,
while almost ignoring the watermark rule in the low entropy
case where there is a clear and unique choice of the “best”
word. A highly likely word with p(t)
k ≈ 1 has a much larger
logit than other candidates, and this will remain the largest
regardless of whether it is in the red list. But when the
entropy is high, there are many comparably large logits
to choose from, and the δ rule has a large impact on the
sampling distribution, strongly biasing the output towards
the green list.
3
A Watermark for Large Language Models
Algorithm 2 Text Generation with Soft Red List
Input: prompt, s(−Np) ··· s(−1)
green list size, γ ∈ (0, 1)
hardness parameter, δ >0
for t = 0, 1, ··· do
1. Apply the language model to prior tokens
s(−Np) ··· s(t−1) to get a logit vector l(t) over
the vocabulary.
2. Compute a hash of token s(t−1), and use it to
seed a random number generator.
3. Using this random number generator, randomly
partition the vocabulary into a “green list” G of
size γ|V |, and a “red list” R of size (1 − γ)|V |.
4. Add δ to each green list logit. Apply the soft-
max operator to these modified logits to get a
probability distribution over the vocabulary.
ˆp(t)
k =



exp(l(t)
k +δ)
P
i∈R exp(l(t)
i )+P
i∈G exp(l(t)
i +δ) , k ∈ G
exp(l(t)
k )
P
i∈R exp(l(t)
i )+P
i∈G exp(l(t)
i +δ) , k ∈ R.
5. Sample the next token, s(t), using the water-
marked distribution ˆp(t).
end for
3.1. Detecting the soft watermark
The process for detecting the soft watermark is identical to
that for the hard watermark. We assume the null hypothesis
(1) and compute a z-statistic using Equation (2). We reject
the null hypothesis and detect the watermark if z is greater
than a threshold. For arbitrary γ we have
z = (|s|G − γT )/
p
T γ(1 − γ). (3)
Consider again the case in which we detect the watermark
for z >4. Just like in the case of the hard watermark, we
get false positives with rate 3 × 10−5. In the case of the
hard watermark, we could detect any watermarked sequence
of length 16 tokens or more, regardless of the properties
of the text. However, in the case of the soft watermark our
ability to detect synthetic text depends on the entropy of
the sequence. High entropy sequences are detected with
relatively few tokens, while low entropy sequences require
more tokens for detection. Below, we rigorously analyze
the detection sensitivity of the soft watermark, and its
dependence on entropy.
4. Analysis of the soft watermark
In this section, we examine the expected number of green list
tokens used by a watermarked language model and analyze
the dependence of this quantity on the entropy of a generated
text fragment. Our analysis assumes the red list is sampled
uniformly at random. This is a deviation from the method
used in practice, which generates red lists using a pseudo-
random number generator seeded with previous tokens. The
consequences of pseudo-random sampling are explored in
Section 5. We analyze the case in which text is generated
by multinomial random sampling. In our experiments, we
consider two more sampling schemes, greedy decoding and
beam search.
We need a definition of entropy that is appropriate for our
analysis. The strength of our watermark is weak when the
distribution over tokens has a large “spike” concentrated
on one or several tokens. We define the following type of
entropy to quantify this phenomenon.
Definition 4.1. Given a discrete probability vector p and a
scalar z, we define the spike entropy of p with modulus z as
S(p, z) =
X
k
pk
1 + zpk
.
Like the classical Shannon entropy, the spike entropy is
a measure of how spread out a distribution is; The spike
entropy assumes its minimal value of 1
1+z when the en-
tire mass of p is concentrated at a single location, and its
maximal value of N
N+z when the mass of p is uniformly
distributed. For large z, the value of pk
1+zpk
≈ 1/z when
pk > 1/z and ≈ 0 for pk < 1/z. For this reason, one can
interpret the spike entropy as a softened measure of the
number of entries in p greater than 1/z.
The following theorem predicts the number of green list
tokens that appear in a sequence with the watermark.
Theorem 4.2. Consider watermarked text sequences of T
tokens. Each sequence is produced by sequentially sam-
pling a raw probability vector p(t) from the language model,
sampling a random green list of size γN , and boosting the
green list logits by δ using Equation 4 before sampling each
token. Define α = exp(δ), and let |s|G denote the number
of green list tokens in sequence s.
If a randomly generated watermarked sequence has average
spike entropy at least S⋆, i.e.,
1
T
X
t
S

p(t), (1 − γ)(α − 1)
1 + (α − 1)γ

≥ S⋆,
then the number of green list tokens in the sequence has
expected value at least
E|s|G ≥ γαT
1 + (α − 1)γ S⋆,
Furthermore, the number of green list tokens has variance
at most
Var |s|G ≤ T γαS⋆
1 + (α − 1)γ

1 − γαS⋆
1 + (α − 1)γ

.
4
A Watermark for Large Language Models
If we have chosen γ ≥ .5, then we can use the strictly looser
but simpler bound
Var |s|G ≤ T γ(1 − γ).
Remark. It may seem like there are a lot of messy constants
floating around in this bound. However, when we choose
γ = 1
2 and δ = ln(2) ≈ 0.7, this bound simplifies to
E|s|G ≥ 2
3T S⋆, Var |s|G ≤ 2
3T S⋆

1 − 2
3S⋆

where S⋆ is a bound on spike entropy with modulus 1/3. If
we study the “hard” red list rules by choosing γ = 1
2 and
letting δ → ∞, we have
E|s|G ≥ T S⋆, Var |s|G ≤ T S⋆ (1 − S⋆)
where S⋆ is a bound on spike entropy with modulus 1.
4.1. Sensitivity of the watermark test
The sensitivity of the soft watermark can be computed using
standard type-II error analysis. For illustrative purposes,
we estimate the type-II (false negative) error rate of a soft
watermark with γ = .5 and δ = 2. We assume 200 tokens
are generated using OPT-1.3B (Zhang et al., 2022) using
prompts from the C4 dataset’s RealNewsLike subset (Raffel
et al., 2019). We also assume a detection threshold of z = 4
(which occurs at ∼ 128.2/100 tokens) which gives us a
type-I error (false positive) rate of 3 × 10−5.
Theoretical bound. Our generations have an average spike
entropy per sample of S = 0.807 over ∼ 500 generations.
Theorem 4.2 says that the expected number of green list
tokens per generation is at least 142.2. Indeed, the empiri-
cal average is 159.5. For sequences with entropy equal to
the mean (S = 0.807) we get σ ≤ 6.41 tokens, and 98.6%
sensitivity (1.4% type-II error rate), using a standard Gaus-
sian approximation for the green list count. Note, this is a
lower bound on the sensitivity for this particular entropy.
If we use the true empirical mean of 159.5 rather than the
theoretical bound, we get a 5.3 × 10−7 type-II error rate, a
realistic approximation but not a rigorous lower bound.
Empirical sensitivity. Empirically, 98.4% of generations
are detected at the z = 4 (128 token) threshold when multi-
nomial sampling is used. When 4-way beam search over a
greedy decoding is used, we get 99.6% empirical sensitivity.
Unlike the theoretical bounds, these are computed over all
generations, which have the same length but vary in their
individual entropies. Here, the primary source of type-II
errors is low entropy sequences, as calculations above show
that we expect a very low error rate when the entropy lies
near the mean. To validate this, we examine the subset of
375/500 generations that have spike entropy above the 25th
percentile, of which we detect 100% of generations at the
z = 4 threshold.
What do failure cases look like? We display typical suc-
cess and failure cases for the watermark in Table 1. We
observe that low-entropy (undetectable) sequences typically
involve data memorization; the model regurgitates a copy
(or near copy) of human-written text which is therefore not
detectable as machine-written. A detailed exploration of
model accuracy is presented in Section 6 with more genera-
tion examples provided in Appendix A.3.
4.2. Impact on quality of generated text
When the distribution produced by the language model is
uniform (maximal entropy), the randomness of the green list
results in tokens being uniformly sampled, and the perplex-
ity remains untouched. Conversely, in the case of minimal
entropy, where all probability mass is concentrated on a
single token, the soft watermark rule has no effect and there
is once again no impact on perplexity. However, the wa-
termark rule does impact perplexity for tokens of moderate
entropy. We provide a bound on this perplexity change in
the supplementary material.
5. Private Watermarking
The watermark algorithms above are designed to be pub-
lic. A watermark can also be operated in private mode, in
which the algorithm uses a random key that is kept secret and
hosted behind a secure API. If the attacker has no knowledge
of the key used to produce the red list, it becomes more diffi-
cult for the attacker to remove the watermark as the attacker
does not know which tokens are in the red list. However,
testing for the presence of the watermark now requires using
the same secure API and, if this API is public, access needs
to be monitored to prevent an adversary from making too
many queries using minor variants of the same sequence.
A range of more complex mechanisms are possible with
different efficiency and security tradeoffs, and we discuss a
few of these in the supplementary material.
6. Experiments
In this section we explore the behavior of the watermark us-
ing the OPT-1.3B model (Zhang et al., 2022). We measure
watermark strength using the rate of type-I errors (human
text falsely flagged as watermarked) and type-II errors (wa-
termarked text not detected). We provide basic implementa-
tion details in Appendix A.1.
Datasets and Prompts. To simulate a variety of realistic
language modeling scenarios we slice and dice a random
selection of texts from the news-like subset of the C4 dataset
(Raffel et al., 2019). For each random string, we trim a fixed
5
A Watermark for Large Language Models
Table 1.Selected outputs from non-watermarked (NW) and watermarked (W) multinomial sampling using γ = 0.5 and δ = 2.0. The
example in the first row has high entropy and correspondingly high z-scores, without any perceptible degradation in output quality. The
lower row is a failure case where the watermark is too weak to be detected – it has low entropy and corresponding low z-scores.
prompt real completion no watermark (NW) watermarked (W) S (W)
z
(NW)
PPL
(W)
PPL
...tled out of court and publicly
reconciled.\nIn the ’80s the band’s
popularity waned in the United
States but remained strong abroad.
Robin released three solo albums,
with limited success. The Bee Gees
returned with some moderate hits
in the late 1990s and were inducted
into the Rock and Roll Hall of
Fame in 1997. With his brothers,
Mr. Gibb won six Grammys.\nIn
addition to his wife and his brother
[...continues]
continued to tour, and Barry became
a television producer.\nBut in the
early ’90s, the Bee Gees’ popularity
remained high. They scored a
hit with “Don’t Stop Believing”
in 1990, and in 1992 the Bee
Ge[...continues]
’ 1990 album, “Spirits of the
Century,” was a mixed critical and
commercial success.\nWhen the
brothers were nominated for a
Grammy Award in 1990, Mr. Gibb’s
“You Should Be Dancing” and
“Massachusetts,[...continues]
0.68 12.73 3.15 1.93
...cond season at Hall Bros
Oval.\nThe defender also ad-
mitted his surprise at Young’s run to
the finals but credited the injection
of youth into the side.\n“We were
really in a building phase last year
and
we copped a few floggings with
all those juniors blokes coming
in,” Galvin said.\n“Now, we’ve
kept that core group together
for two years and I think we’ve
come along quicker than we
anticipated.\nROCK[...continues]
we copped a few floggings with
all those juniors blokes coming
in,” Galvin said.\n“Now, we’ve
kept that core group together
for two years and I think we’ve
come along quicker than we
anticipated.\n“Tha[...continues]
we copped a few floggings with
all those juniors blokes coming
in,” Galvin said.\n“Now, we’ve
kept that core group together
for two years and I think we’ve
come along quicker than we
anticipated.\n“Tha[...continues]
0.58 -1.13 1.05 1.04
345678910111213
Oracle Model PPL (better → )
0
5
10
15
20
25
30
35
40z-score (better → )
δ = 10.0
δ = 5.0
δ = 2.0
δ = 1.0
δ = 0.0
0.9
0.75
0.5
0.25
0.1
γ
1.01.21.41.61.82.0
Oracle Model PPL (better → )
0
2
4
6
8
10
12
14
16z-score (better → )
δ = 10.0
δ = 5.0
δ = 2.0
δ = 1.0
δ = 0.5
δ = 0.1
δ = 0.0
1
4
8
Num Beams
Figure 2.The tradeoff between average z-score and language model perplexity for T = 200± 5 tokens. (left) Multinomial sampling.
(right) Greedy and beam search with 4 and 8 beams for γ = .5. Beam search promotes higher green list usage and thus larger z-scores
with smaller impact to model quality (perplexity, PPL).
length of tokens from the end and treat them as a “baseline”
completion. The remaining tokens are a prompt. A larger
oracle language model (OPT-2.7B) is used to compute per-
plexity (PPL) for the generated completions and for the
human baseline.
Watermark Strength vs Text Quality. One can achieve
a very strong watermark for short sequences by choosing
a small green list size γ and a large green list bias δ. How-
ever, creating a stronger watermark may distort generated
text. Figure 2 (left) shows the tradeoff between watermark
strength (z-score) and text quality (perplexity) for various
combinations of watermarking parameters. We compute
results using 500 ± 10 sequences of length T = 200 ± 5
tokens for each parameter choice. Interestingly, we see that
a small green list, γ = .1 is pareto-optimal.
In addition to these quantitative results, we show exam-
ples of real prompts and watermarked outputs in Table 1 to
provide a qualitative sense for the behavior of the test statis-
tic and quality measurement on different kinds of prompts.
Additional examples are compiled in Appendix A.3.
Ironing in the Watermark with Beam Search. Figure 2
(right) shows the tradeoff between watermark strength and
accuracy when beam search is used. Beam search has a
synergistic interaction with the soft watermarking rule. Par-
ticularly when 8 beams are used, the points in Figure 2 form
an almost vertical line, showing very little perplexity cost to
achieve strong watermarking.
Watermark Strength vs Number of Tokens.Theory pre-
dicts that the type I and type II error rates of the watermark
should decay to zero as the sequence length T increases.
Figure 3 shows the strength of the watermark, measured
using the average z-score over samples, as T sweeps from 2
to 200. Curves are shown for various values of δ and γ. The
left two charts use multinomial sampling, while the right
chart uses 8-way beam search and γ = .25. Once again, we
see the power of the beam search in achieving high green
list ratios; even for the moderate bias of δ = 2, an average
z-score greater than 5 is achieved for as few as 35 tokens.
Performance and Sensitivity for Multinomial Sampling.
To show the sensitivity of the resulting hypothesis test based
6
A Watermark for Large Language Models
0 25 50 75 100 125 150 175
T
0
5
10
15
20
25
30z-score
δ : 5.0, γ: 0.1
δ : 5.0, γ: 0.25
δ : 5.0, γ: 0.5
δ : 5.0, γ: 0.75
δ : 5.0, γ: 0.9
(a)
0 25 50 75 100 125 150 175
T
0
5
10
15
20z-score
δ : 10.0, γ: 0.25
δ : 5.0, γ: 0.25
δ : 2.0, γ: 0.25
δ : 1.0, γ: 0.25
δ : 0.5, γ: 0.25 (b)
0 25 50 75 100 125 150 175 200
T
0
5
10
15
20
25z-score
δ : 10.0, γ: 0.25
δ : 5.0, γ: 0.25
δ : 2.0, γ: 0.25
δ : 1.0, γ: 0.25
δ : 0.5, γ: 0.25 (c)
Figure 3.The average z-score as a function of T the token length of the generated text. (a) The dependence of the z-score on the green
list size parameter γ, under multinomial sampling. (b) The effect of δ on z-score, under multinomial sampling. (c) The impact of the
green list size parameter γ on the z-score, but with greedy decoding using 8-way beam search.
0.0 0.2 0.4 0.6 0.8 1.0
False Positive Rate
0.0
0.2
0.4
0.6
0.8
1.0
True Positive Rate
(a)
0.0 0.2 0.4 0.6 0.8 1.0
False Positive Rate
0.0
0.2
0.4
0.6
0.8
1.0
True Positive Rate (b)
10−2 10−1 100
False Positive Rate
0.5
0.6
0.7
0.8
0.9
1.0
True Positive Rate
δ : 10.0, γ: 0.5, AUC:1.000, PPL:11.6
δ : 10.0, γ: 0.25, AUC:1.000, PPL:12.4
δ : 5.0, γ: 0.5, AUC:1.000, PPL:9.1
δ : 5.0, γ: 0.25, AUC:1.000, PPL:10.7
δ : 2.0, γ: 0.5, AUC:0.998, PPL:6.2
δ : 2.0, γ: 0.25, AUC:0.998, PPL:6.6
δ : 1.0, γ: 0.5, AUC:0.985, PPL:5.4
δ : 1.0, γ: 0.25, AUC:0.989, PPL:5.5
δ = 0, PPL: 5.1 (c)
10−2 10−1 100
False Positive Rate
0.5
0.6
0.7
0.8
0.9
1.0
True Positive Rate
δ : 10.0, γ: 0.5, AUC:1.000, PPL:1.2
δ : 10.0, γ: 0.25, AUC:1.000, PPL:1.2
δ : 5.0, γ: 0.5, AUC:1.000, PPL:1.2
δ : 5.0, γ: 0.25, AUC:1.000, PPL:1.3
δ : 2.0, γ: 0.5, AUC:0.999, PPL:1.2
δ : 2.0, γ: 0.25, AUC:1.000, PPL:1.3
δ : 1.0, γ: 0.5, AUC:0.987, PPL:1.2
δ : 1.0, γ: 0.25, AUC:0.977, PPL:1.2
δ = 0, PPL: 1.2 (d)
Figure 4.ROC curves with AUC values for watermark detection. Several choices of watermark parameterδ are shown for (a) multi-
nomial sampling and (b) greedy decoding with 8-way beam search. (c,d) The same charts with semilog axes. Higher δ values achieve
stronger performance, but additionally we see that for a given δ, the beam search allows the watermark to capture slightly more AUC
than the corresponding parameters under the multinomial sampling scheme.
on the observed z-scores, we provide a table of error rate for
various watermarking parameters in Table 2. We also sweep
a range of thresholds in ROC charts in Figure 4. We further
report detection performance and error rates for various
cutoffs in Appendix C, and provide a comparison between
empirical z-scores and theoretical predictions. Note that
no type-I (false positive) errors were observed for any run
shown in the error tables (see the columns of 0.0’s).
7. Attacking the watermark
Like any software tool, care must be taken when implement-
ing a watermark and watermark detector so that security is
maintained. Otherwise, an adversarial user may modify text
to add red list tokens, and thus avoid detection. In many
cases, simple attacks can be avoided by properly normaliz-
ing text before hashes are computed. In Appendix B.1, we
discuss a range of attacks that we are currently aware of,
and methods to mitigate them. In the next section, we im-
plement and evaluate an example of a representative attack
using a second, smaller language model.
7.1. Degradation Under Attack: Span Replacement
Using a LM
We study a realistic black-box attack by attempting to re-
move the presence of the watermark by replacing spans in
the original output text using another language model. We
treat the watermark algorithm as if it is private, mocking
seclusion behind an API. The attacker does not have access
to the locations of green list tokens and instead tries to mod-
ify the text through token replacement at random indices
until a certain word replacement budget, ε, is reached. The
budget constraint maintains a level semantic similarity be-
tween the original watermarked text and the attacked text,
otherwise the “utility” of the original text for its intended
task may be lost. Also, each span replacement in the attack
is performed via inference using a multi-million parameter
language model. While this is roughly a third the size of the
target model, it means that the attack incurs an associated
cost per step implying that a base level of efficiency with
respect to model calls would be desired in practice.
In our experiment, we adopt T5-Large (Raffel et al., 2020)
as the replacement model and iteratively select and replace
tokens until the attacker either reaches the budget, or no
7
A Watermark for Large Language Models
Table 2.Empirical error rates for watermark detection using
multinomial sampling and beam search. Each row is averaged
over ∼ 500(−4/+7) generated sequences of length T = 200±5.
A maximum of one type-I (false positive) error was observed for
any given run. All soft watermarks at δ = 2.0 incur at most
1.6% (8/500) type-II error at z = 4. No type-II errors occurred
for the hardest watermarks with δ = 5.0 and γ = 0.25. A more
extensive set of error rates is provided in Table 8.
z=4.0
sampling δ γ FPR TNR TPR FNR
m-nom. 1.0 0.50 0.0 1.0 0.767 0.233
m-nom. 1.0 0.25 0.0 1.0 0.729 0.271
m-nom. 2.0 0.50 0.0 1.0 0.984 0.016
m-nom. 2.0 0.25 0.0 1.0 0.994 0.006
m-nom. 5.0 0.50 0.0 1.0 0.996 0.004
m-nom. 5.0 0.25 0.0 1.0 1.000 0.000
8-beams 1.0 0.25 0.0 1.0 0.819 0.181
8-beams 2.0 0.25 0.0 1.0 0.994 0.006
8-beams 5.0 0.25 0.0 1.0 1.000 0.000
more suitable replacement candidates are returned.
Details of the T5 Span Attack. We tokenize the water-
marked text using the T5 tokenizer. Then, while fewer
than εT successful replacements have been performed or a
maximal iteration count is reached:
1. Randomly replace one word from the tokenization with
a <mask>.
2. Pass the region of text surrounding the mask token
to T5 to obtain a list of k = 20 candidate replace-
ment token sequences via a 50-way beam search, with
associated scores corresponding to their likelihood.
3. Each candidate is decoded into a string. If one of the
k candidates returned by the model is not equal to the
original string corresponding to the masked span, then
the attack succeeds, and the span is replaced with the
new text.
After attacking a set of500 sequences of length T = 200±5
token sequences this way, we compute updatedz-scores and
tabulate error rates (Table 9 in the Appendix). We also
generate ROC plots for a range of ε budgets. While this
attack is effective at increasing the number of red list tokens
in the text, as shown in Figure 5, we only measure a decrease
in watermark strength of 0.01 AUC when ε = 0.1. While
the watermark removal is more successful at a larger budget
of 0.3, the average PPL of attacked sequences increases by
3× in addition to requiring more model calls.
8. Related Work
The idea of watermarking has a long history. Watermarking
of digital text has been considered challenging, due to its dis-
crete nature (Katzenbeisser & Petitcolas, 2000). Watermark-
0.0 0.2 0.4 0.6 0.8 1.0
False Positive Rate
0.0
0.2
0.4
0.6
0.8
1.0
True Positive Rate
unattacked, AUC:0.998, PPL:6.3
ϵ= 0.1, AUC:0.988, PPL:13.1
ϵ= 0.3, AUC:0.954, PPL:21.2
ϵ= 0.5, AUC:0.838, PPL:28.4
ϵ= 0.7, AUC:0.696, PPL:33.9
Figure 5.ROC curves for watermark detection under attack via
the T5 Span Attack detailed in Section 7.1, with various replace-
ment budgets ε. The initial, unattacked watermark is a γ = 0.5,
δ = 2.0 soft watermark generated using multinomial sampling.
The attack achieves a high level of watermark degradation, but
only at ε = 0.3, which costs the attacker an average of ∼ 15
points of perplexity compared the PPL of the original water-
marked text.
ing is considered easier for continuous data, where a variety
of effective strategies are known (Petitcolas et al., 1999;
Zhu et al., 2018; Lu et al., 2021; Boenisch, 2021). Note that
watermarking is a special case of steganography, the task
of embedding arbitrary hidden information into data.
Watermarking Natural Language. Early approaches to
watermarking natural text in digital form (Atallah et al.,
2001; 2003; Venugopal et al., 2011) pose similar desiderata
as in Section 1, except for classical models.
Rule-based watermarks were further developed in a series of
works (Chiang et al., 2004; Topkara et al., 2006a;b; Meral
et al., 2009) with variants also embedding watermarks based
on synonym tables instead of only parse trees. Early de-
velopments were summarized in Jalil & Mirza (2009), but
strong watermarks significantly degraded the text quality
due to the limited flexibility of language models of the time.
While approaches via hierarchical language models in Wil-
son et al. (2014) still required human interactions, the emer-
gence of modern neural language models (Vaswani et al.,
2017; Devlin et al., 2019) also allowed for improved wa-
termarking/steganography (Fang et al., 2017; Ziegler et al.,
2019; Dai & Cai, 2019; He et al., 2022). Fang et al. (2017)
propose such a neural steganography approach where, to
encode a message of w bits, the message is first separated
into blocks of length b. Then, the vocabulary V of a lan-
guage model is partitioned at random into disjoint sets of
size |V |/2b. A generative LM can then encode the message
8
A Watermark for Large Language Models
by generating only a token from the “allowed” set at each
position. However, this hard rule reduces the quality of gen-
erated text, boxing the LM into a small selection of tokens
for each step.
In a somewhat similar approach to our proposal, Kaptchuk
et al. (2021) constructs a framework that adapts traditional
public-key cryptographic steganography specifically for
“natural” comunication channels like text using generative
models. However, their method, Meteor, relies on a synchro-
nized model framework where the sender and receiver agree
on a shared generative model used to embed and decode the
hidden bits of information being sent.
Another approach (Ueoka et al., 2021) uses mask-infilling
via BERT to edit already-generated text for steganography.
Finally, Abdelnabi & Fritz (2021) design an end-to-end
system where both encoding and decoding are handled by
text-to-text language models that are trained adversarially
for this purpose, and Gu et al. (2022) implants a series
of backdoor triggers through a finetuning process to cause
biased responses to specific inputs, a behavior detectable at
verification time.
Recently, Aaronson (2022) announced that he is also study-
ing cryptographic approaches to watermarking in collabo-
ration with OpenAI. Their preliminary method is based on
biasing of the LM output, as opposed to complete determina-
tion as in Fang et al. (2017). While details are not currently
available, the description suggests that hashing of n-gram
sequences is involved. We hope to extend our comparison
to this work when more information becomes available.
In contrast to other currently published works, we want
to focus on strategies that are simultaneously minimally
restrictive to a language model, leverage the LMs own un-
derstanding of natural text, require no usage of the LM to
decode the watermark, and can be theoretically analyzed
and validated.
Post-hoc Detection. An alternative to watermarking is
post-hoc analysis of machine-generated text, for example
using language model features or finetuning existing large
language models to behave as detectors (Zellers et al.,
2019; Tan et al., 2020), see an overview in Jawahar et al.
(2020). Implementation details, such as sampling strategies,
can be reverse-engineered from text (Tay et al., 2020).
However, detection approaches are slowly losing ground
as LM capabilities increase; Gambini et al. (2022) note that
detection strategies for GPT-2 struggle with GPT-3. Further,
known detectors are vulnerable to adversarial attacks that
degrade their functionality (Wolff & Wolff, 2022).
While efforts to provide strong detectors continue, as in Tian
(2023a), ultimately language model progress may make de-
tection infeasible. All post-hoc detection methods require
the LM to be significantly biased away from human text in
some measurable way, such as low variation in perplexity
across sentences (Tian, 2023b). Even for current LLMs,
this margin might be small. Detection schemes that op-
erate within this small margin are susceptible to labeling
human text as false-positive, a concern that is especially
pressing for non-native speakers and people who use com-
puter writing assistance tools. Such populations might be
especially at risk for false-positives, which could lead to
academic problems if these detectors are used in schools
(Butoi, 2023).
9. Conclusion
There is one more important property of the proposed
method: The z-statistic used for detection depends only
on the green list size parameter γ and the hash function.
There is no dependence on δ or any other factor related to
how the green list is enforced. For this reason, one can
deploy the watermark using context-specific δ or green list
enforcement rules for different kinds of text (e.g., prose
vs code) while using the same downstream detector. One
can also change a proprietary implementation of the water-
marked sampling algorithm without any need to change the
detector. Finally, the watermarking method could be turned
on only in certain contexts, for example when a specific user
seems to exhibit suspicious behavior.
There are still a number of open questions regarding water-
marking. For example, what is the best way to test for the
watermark in a streaming context, or in a context where a
short span of watermarked text lives inside a longer non-
watermarked span? We hope our present results are enough
to convince readers that watermarks could be a practical
tool for combating malicious uses of generative models, and
we leave these additional questions for future research.
10. Acknowledgements
This work was made possible by the ONR MURI program,
DARPA GARD (HR00112020007), the Office of Naval Re-
search (N000142112557), and the AFOSR MURI program.
Commercial support was provided by Capital One Bank, the
Amazon Research Award program, and Open Philanthropy.
Further support was provided by the National Science Foun-
dation (IIS-2212182), and by the NSF TRAILS Institute
(2229885).
References
Aaronson, S. My AI Safety Lecture for UT Effec-
tive Altruism, November 2022. URL https://
scottaaronson.blog/?p=6823.
Abdelnabi, S. and Fritz, M. Adversarial Watermark-
ing Transformer: Towards Tracing Text Provenance
9
A Watermark for Large Language Models
with Data Hiding. In 2021 IEEE Symposium on Secu-
rity and Privacy (SP) , pp. 121–140, May 2021. doi:
10.1109/SP40001.2021.00083.
Atallah, M. J., Raskin, V ., Crogan, M., Hempelmann, C.,
Kerschbaum, F., Mohamed, D., and Naik, S. Natural
Language Watermarking: Design, Analysis, and a Proof-
of-Concept Implementation. In Moskowitz, I. S. (ed.),
Information Hiding, Lecture Notes in Computer Science,
pp. 185–200, Berlin, Heidelberg, 2001. Springer. ISBN
978-3-540-45496-0. doi: 10.1007/3-540-45496-9 14.
Atallah, M. J., Raskin, V ., Hempelmann, C. F., Karahan,
M., Sion, R., Topkara, U., and Triezenberg, K. E. Nat-
ural Language Watermarking and Tamperproofing. In
Petitcolas, F. A. P. (ed.), Information Hiding, Lecture
Notes in Computer Science, pp. 196–212, Berlin, Hei-
delberg, 2003. Springer. ISBN 978-3-540-36415-3. doi:
10.1007/3-540-36415-3 13.
Bai, Y ., Kadavath, S., Kundu, S., Askell, A., Kernion, J.,
Jones, A., Chen, A., Goldie, A., Mirhoseini, A., McK-
innon, C., Chen, C., Olsson, C., Olah, C., Hernandez,
D., Drain, D., Ganguli, D., Li, D., Tran-Johnson, E.,
Perez, E., Kerr, J., Mueller, J., Ladish, J., Landau, J.,
Ndousse, K., Lukosiute, K., Lovitt, L., Sellitto, M.,
Elhage, N., Schiefer, N., Mercado, N., DasSarma, N.,
Lasenby, R., Larson, R., Ringer, S., Johnston, S., Kravec,
S., Showk, S. E., Fort, S., Lanham, T., Telleen-Lawton,
T., Conerly, T., Henighan, T., Hume, T., Bowman, S. R.,
Hatfield-Dodds, Z., Mann, B., Amodei, D., Joseph, N.,
McCandlish, S., Brown, T., and Kaplan, J. Consti-
tutional AI: Harmlessness from AI Feedback, Decem-
ber 2022. URL https://www.anthropic.com/
constitutional.pdf.
Bender, E. M., Gebru, T., McMillan-Major, A., and
Shmitchell, S. On the Dangers of Stochastic Parrots:
Can Language Models Be Too Big? In Proceed-
ings of the 2021 ACM Conference on Fairness, Ac-
countability, and Transparency , FAccT ’21, pp. 610–
623, New York, NY , USA, March 2021. Association
for Computing Machinery. ISBN 978-1-4503-8309-7.
doi: 10.1145/3442188.3445922. URL https://doi.
org/10.1145/3442188.3445922.
Bergman, A. S., Abercrombie, G., Spruit, S., Hovy, D.,
Dinan, E., Boureau, Y .-L., and Rieser, V . Guiding the
Release of Safer E2E Conversational AI through Value
Sensitive Design. In Proceedings of the 23rd Annual
Meeting of the Special Interest Group on Discourse and
Dialogue, pp. 39–52, Edinburgh, UK, September 2022.
Association for Computational Linguistics. URLhttps:
//aclanthology.org/2022.sigdial-1.4.
Boenisch, F. A Systematic Review on Model Water-
marking for Neural Networks. Frontiers in Big Data ,
4, 2021. ISSN 2624-909X. doi: 10.3389/fdata.2021.
729663. URL https://www.frontiersin.org/
articles/10.3389/fdata.2021.729663.
Boucher, N., Shumailov, I., Anderson, R., and Papernot, N.
Bad Characters: Imperceptible NLP Attacks. In 2022
IEEE Symposium on Security and Privacy (SP), pp. 1987–
2004, May 2022. doi: 10.1109/SP46214.2022.9833641.
Butoi, V . Things like GPTZero are scary. I’m sure
the creator didn’t have the intention, but the fact
that it’s marketed as ”a solution to detecting AI writ-
ten responses” even though there’s no evidence to
show it works consistently and is nevertheless being
EMPLOYED by schools, is crazy., January 2023.
URL https://twitter.com/VictorButoi/
status/1614779846210752512.
Chiang, Y .-L., Chang, L.-P., Hsieh, W.-T., and Chen, W.-
C. Natural Language Watermarking Using Semantic
Substitution for Chinese Text. In Kalker, T., Cox, I., and
Ro, Y . M. (eds.),Digital Watermarking, Lecture Notes
in Computer Science, pp. 129–140, Berlin, Heidelberg,
2004. Springer. ISBN 978-3-540-24624-4. doi: 10.1007/
978-3-540-24624-4 10.
Christiano, P., Leike, J., Brown, T. B., Martic, M., Legg,
S., and Amodei, D. Deep reinforcement learning from
human preferences. arxiv:1706.03741[cs, stat] , July
2017. doi: 10.48550/arXiv.1706.03741. URL http:
//arxiv.org/abs/1706.03741.
Crothers, E., Japkowicz, N., and Viktor, H. Machine
Generated Text: A Comprehensive Survey of Threat
Models and Detection Methods. arxiv:2210.07321[cs],
November 2022. doi: 10.48550/arXiv.2210.07321. URL
http://arxiv.org/abs/2210.07321.
Dai, F. and Cai, Z. Towards Near-imperceptible Stegano-
graphic Text. In Proceedings of the 57th Annual Meet-
ing of the Association for Computational Linguistics, pp.
4303–4308, Florence, Italy, July 2019. Association for
Computational Linguistics. doi: 10.18653/v1/P19-1422.
URL https://aclanthology.org/P19-1422.
Devlin, J., Chang, M.-W., Lee, K., and Toutanova, K. BERT:
Pre-training of Deep Bidirectional Transformers for Lan-
guage Understanding. arXiv:1810.04805 [cs], May 2019.
URL http://arxiv.org/abs/1810.04805.
Fang, T., Jaggi, M., and Argyraki, K. Generating Stegano-
graphic Text with LSTMs. In Proceedings of ACL
2017, Student Research Workshop, pp. 100–106, Vancou-
ver, Canada, July 2017. Association for Computational
Linguistics. URL https://aclanthology.org/
P17-3017.
10
A Watermark for Large Language Models
Folt´ynek, T., Meuschke, N., and Gipp, B. Academic
Plagiarism Detection: A Systematic Literature Review.
ACM Computing Surveys, 52(6):112:1–112:42, October
2019. ISSN 0360-0300. doi: 10.1145/3345317. URL
https://doi.org/10.1145/3345317.
Gabrilovich, E. and Gontmakher, A. The homograph at-
tack. Communications of the ACM , 45(2):128, Febru-
ary 2002. ISSN 0001-0782, 1557-7317. doi: 10.1145/
503124.503156. URL https://dl.acm.org/doi/
10.1145/503124.503156.
Gambini, M., Fagni, T., Falchi, F., and Tesconi, M. On push-
ing DeepFake Tweet Detection capabilities to the limits.
In 14th ACM Web Science Conference 2022, WebSci ’22,
pp. 154–163, New York, NY , USA, June 2022. Asso-
ciation for Computing Machinery. ISBN 978-1-4503-
9191-7. doi: 10.1145/3501247.3531560. URL https:
//doi.org/10.1145/3501247.3531560.
Goodside, R. There are adversarial attacks for that pro-
posal as well — in particular, generating with emojis after
words and then removing them before submitting defeats
it., January 2023. URL https://twitter.com/
goodside/status/1610682909647671306.
Grinbaum, A. and Adomaitis, L. The Ethical
Need for Watermarks in Machine-Generated Language.
arxiv:2209.03118[cs], September 2022. doi: 10.48550/
arXiv.2209.03118. URL http://arxiv.org/abs/
2209.03118.
Gu, C., Huang, C., Zheng, X., Chang, K.-W., and Hsieh,
C.-J. Watermarking pre-trained language models with
backdooring. arXiv preprint arXiv:2210.07543, 2022.
He, X., Xu, Q., Zeng, Y ., Lyu, L., Wu, F., Li, J., and
Jia, R. CATER: Intellectual Property Protection on
Text Generation APIs via Conditional Watermarks. In
Advances in Neural Information Processing Systems ,
October 2022. URL https://openreview.net/
forum?id=L7P3IvsoUXY.
Helfrich, J. N. and Neff, R. Dual canonicalization: An
answer to the homograph attack. In 2012 eCrime
Researchers Summit , pp. 1–10, October 2012. doi:
10.1109/eCrime.2012.6489517.
Jalil, Z. and Mirza, A. M. A Review of Digital Water-
marking Techniques for Text Documents. In 2009 In-
ternational Conference on Information and Multime-
dia Techno
```
