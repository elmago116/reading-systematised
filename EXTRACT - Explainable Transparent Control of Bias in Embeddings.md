---
title: "EXTRACT: Explainable Transparent Control of Bias in Embeddings"
author:
  - Zhijin Guo
  - Zhaozhen Xu
  - Martha Lewis
  - Nello Cristianini
source: https://ceur-ws.org/Vol-3523/paper6.pdf
venue: AEQUITAS 2023
type: Proceedings Article
created: 2025-02-17
tags:
  - themes/bias
  - themes/ethics
  - tech/Ai/embeddings
pdfORepub: "[[EXTRACT - Explainable Transparent Control of Bias in Embeddings.pdf]]"
modified: 2026-09-08
---

# Notes

## Full text (extracted from `2PDF/EXTRACT - Explainable Transparent Control of Bias in Embeddings.pdf`)

*Extracted:* 2026-09-17

```text
EXTRACT: Explainable Transparent Control of Bias
in Embeddings
Zhijin Guo1, Zhaozhen Xu1, Martha Lewis1 and Nello Cristianini2
1University of Bristol, Beacon House, Queens Road, Bristol, BS8 1QU, UK.
2University of Bath, Claverton Down, Bath BA2 7AY, UK
Abstract
Knowledge Graphs are a widely used method to represent relations between entities in various AI
applications, and Graph Embedding has rapidly become a standard technique to represent Knowledge
Graphs in such a way as to facilitate inferences and decisions. As this representation is obtained from
behavioural data, and is not in a form readable by humans, there is a concern that it might incorporate
unintended information that could lead to biases. We propose EXTRACT: a suite ofExplainable and
Transparent methods toConTrol bias in knowledge graph embeddings, so as to assess and decrease
the implicit presence of protected information. Our method uses Canonical Correlation Analysis (CCA)
to investigate the presence, extent and origins of information leaks during training, then decomposes
embeddings into a sum of their private attributes by solving a linear system. Our experiments, performed
on the MovieLens-1M dataset, show that a range of personal attributes can be inferred from a user’s
viewing behaviour and preferences, including gender, age and occupation. Further experiments, per-
formed on the KG20C citation dataset, show that the information about the conference in which a paper
was published can be inferred from the citation network of that article. We propose four transparent
methods to maintain the capability of the embedding to make the intended predictions without retaining
unwanted information. A trade-off between these two goals is observed.
Keywords
Fairness, Knowledge graph embedding, Learning representations, Recommender system
1. Introduction
Knowledge graphs are structures that encode entities and the relationships between them, and
are useful representations of real world phenomena. Knowledge graphs can be employed in an
array of applications, including linguistic representation learning [1], question answering [2],
multihop reasoning [3], or recommender systems [4].
This study emphasizeslink prediction , an inherent task in Knowledge Graph Embedding,
that can simplify crucial issues like recommending user actions or answering entity-specific
queries. Using user gender as an exemplar of private information, we scrutinize its influence on
representations and its ethical implications within AI systems.
Aequitas 2023: Workshop on Fairness and Bias in AI | co-located with ECAI 2023, Kraków, Poland
Envelope-Open zhijin.guo@bristol.ac.uk (Z. Guo);zhaozhen.xu@bristol.ac.uk (Z. Xu);martha.lewis@bristol.ac.uk (M. Lewis);
nc993@bath.ac.uk (N. Cristianini)
GLOBE https://research-information.bris.ac.uk/en/persons/martha-lewis (M. Lewis);
https://researchportal.bath.ac.uk/en/persons/nello-cristianini (N. Cristianini)
© 2023 Copyright for this paper by its authors. Use permitted under Creative Commons License Attribution 4.0 International (CC BY 4.0).
CEUR
Workshop
Proceedings
http://ceur-ws.org
ISSN 1613-0073
CEUR Workshop Proceedings (CEUR-WS.org)


Recent studies showed that personal information can be inferred from user behaviour. A
study of Facebook users showed that certain private traits (including gender and race) could
be reconstructed on the basis of their public “likes” [5]; and a study of word embeddings
showed that these representations contained information related to gender and race, that might
potentially affect the decisions of algorithms that make use of those representations [6]. We
investigate this problem with specific application to detecting and removing bias in knowledge
graphs.
We address issues, similar to prior word embedding research, concerning vector representa-
tions derived from word co-occurrence [7], recasting this process as a particular facet of the
graphembeddingproblem. Thenotable“compositionality”featureinwordembeddingssignified
the potential for analogical reasoning and the risk of undesirable encodings, such as gender
biases [8]. It was observed that these distributions also contain additional information including
associations and biases that reflect customs and practices. For example, the embeddings of
color names were not gender neutral [9], nor were those of job titles or academic disciplines.
Engineering disciplines and leadership jobs tended to be represented in a “more male” way than
artistic disciplines or service jobs [9, 6].
Related Work Thepresenceofgenderinformationinwordembeddingswasalreadyreported
in Bolukbasi et al.[10], in an article aptly entitled “Man is to Computer Programmer as Woman
is to Homemaker?”, as well as in Mikolov et al.[8]. An interesting possibility is the presence of
similar biases in Knowledge Graph embedding, which would lead both to opportunities and
challenges, and which would require attention. Our research significantly extends the field by
introducingdetectionmethodsundertheEXTRACTframework. Ina“fairclassification”context,
Madras et al.[11] aimed to predict a label𝑦 from data𝑥, while ensuring fairness regarding a
binary sensitive attribute𝑎. Our detection methods are tailored to identify specific dimensions
in user embeddings that are associated with private or sensitive attributes. Notably, our linear
decompositionsystemrevealsthatuserbehaviourcanbeapproximatedasasumofdemographic
vectors, uncovering another layer of embedded bias.
When it comes to bias removal, a range of strategies exists. Regularization methods focusing
on fairness have been explored [12]. The LFR framework [13] aimed to encode non-sensitive
attributes while minimizing sensitive ones. Its extension, ALFR, has been adopted in recom-
mendation systems [14]. Works like Zhu et al.[15] employ adversarial learning for equal score
distribution, Bose and Hamilton[16] and Wu et al.[17] extended ALFR’s scope by imposing
compositional fairness. Notably, Fisher et al.[18] used adversarial loss for model neutrality.
Our contributions in debiasing offer transparency and interpretability. We employ linear trans-
formations to identify bias direction and leverage first-moment loss to minimize distributional
disparities during training.
Our Contributions We introduce EXTRACT: Explainable and Transparent ConTrol of bias
in embeddings, a two-step process to detect and mitigate bias in Knowledge Graph Embeddings,
implemented on the MovieLens 1M and KG20C citation datasets. Our detection methods
include logistic classifiers (detect-LC), canonical correlation analysis (detect-CCA), and a linear
decomposition (detect-LD). Bias removal leverages linear projection methods (remove-LP and

remove-LP-multi) and two retraining methods, remove-FM and remove-FM-multi.
The proposed methods are effective and interpretable, with our novel application of detect-
CCA and detect-LD. Specifically, detect-CCA constitutes a novel use of CCA, marking its
debut in bias detection. Additionally, detect-LD contributes a unique decomposition of node
embedding space into interpretable dimensions, signifying attribute presence or absence - a
method not previously implemented. Our methods, remove-LP and remove-LP-multi, can be
directly applied to pre-existing embeddings, saving computational resources by eliminating the
need for retraining from scratch. Despite slight performance decreases, our methods parallel
state-of-the-art results, maintaining conciseness, interpretability, and explainability.
2. Mathematical Preliminaries
Knowledge Graph-Based Recommendation Algorithms In a knowledge graph 𝐺 =
(𝑉 , ℱ , 𝐴), vertices𝑉 signify real-world entities, each endowed with a set𝐴 of attributes. Rela-
tionships between these vertices are captured in a setℱ consisting offacts. Each fact𝑓 ∈ ℱ is
articulated as a triple(ℎ, 𝑟, 𝑡) , where𝑟 belongs to a set of relationsℛ that serve as direct edges
from headℎ to tail𝑡. For instance, considering a set of users and movies as vertices, user ratings
form the edges.
A knowledge graph embedding translates vertices into vectors maintaining graph topology,
represented as(h, R, t) ∈ ℝ 𝑛. The score function𝑆(h, R, t) governs the linking between nodes.
Rating Prediction In alignment with Berg et al.[19], we establish a function𝑃 that, given
a triple of embeddings(h, R, t), calculates the probability of the relation against all potential
alternatives.
𝑃 (h, R, t) = SoftArgmax(𝑆(𝑓 )) = 𝑒𝑆(𝑓 )
𝑒𝑆(𝑓 ) + ∑𝑟′≠𝑟∈R 𝑒𝑆(𝑓 ′) (1)
In the above formula,𝑓 = (ℎ, 𝑟, 𝑡) denotes a true triple, and𝑓 ′ = (ℎ, 𝑟 ′, 𝑡) denotes a corrupted
triple, that is a randomly generated one. We use as a proxy for a negative example (a pair of
nodes that are not connected).
Assigningnumericalvaluestorelations 𝑟, thepredictedrelationisthenjusttheexpectedvalue
prediction = ∑𝑟∈R 𝑟𝑃 (h, R, t) In our application of viewers and movies, the set of relations
R could be the possible ratings that a user can give a movie. The predicted rating is then
the expected value of the ratings, given the probability distribution produced by the scoring
function. 𝑆(𝑓 ) refers to the scoring function in Yang et al. [20].
To learn a graph embedding, we follow the setting of Bose and Hamilton [16] as follows,
𝐿 = − ∑
𝑓 ∈F
log 𝑒𝑆(𝑓 )
𝑒𝑆(𝑓 ) + ∑𝑓 ′∈F′ 𝑒𝑆(𝑓 ′) (2)
This loss function maximises the probabilities of true triples(𝑓 ) and minimises the probability
of triples with corrupted triples(𝑓 ′).

Entity prediction Unlike predicting movie ratings which is the relation in MovieLens 1M,
we use a margin based loss [21] to predict the tail entities (which could be paper, affilation and
domain) as follows. In this loss function,𝑓 represents for a true triple while𝑓 ′ represents for a
corrupted triple,
𝐿 = ∑
𝑓 ∈ℱ
∑
𝑓 ′∈ℱ ′
[𝛾 + 𝑆 (𝑓 ′) − 𝑆(𝑓 )]+ (3)
Here, []+ means keeping the positive part of the loss function and we want𝑆(𝑓 ) > 𝑆(𝑓 ′).
Evaluation Metrics We use 4 metrics to evaluate our performance on the link prediction
task. These are root mean square error (RMSE,√
1
𝑛 ∑𝑛
𝑖=1 ( ̂ 𝑦𝑖 − 𝑦𝑖)2, where ̂ 𝑦𝑖 is our predicted
relation and𝑦𝑖 is the true relation), Hits@K - the probability that our target value is in the top
𝐾 predictions, mean rank (MR) - the average ranking of each prediction, and mean reciprocal
rank (MRR) to evaluate our performance on the link prediction task. These are standard metrics
in the knowledge graph embedding community.
3. Explainable Bias Detection
The general problem is as follows. Given a knowledge graph𝐺 = (𝑉 , ℱ , 𝐴), suppose that one
attribute 𝑎 ∈ 𝐴 is private: we do not wish users of the embedded graph to be able to predict the
value of𝑎 for a given vertex𝑣 ∈ 𝑉 . We show here that it is possible to predict the value of some
private attributes even when that attribute is not used in the embedding algorithm.
We give three methods: a logistic classifier based method (detect-LC), Canonical Correla-
tion Analysis (detect-CCA), and a linear decomposition method (detect-LD) to detect private
information in the vertices𝑉.
detect-LC: Logistic Classifier Consider a knowledge graph denoted by𝐺 = (𝑉 , ℱ , 𝐴) .
We’ve represented this graph in a𝑑-dimensional space,ℝ𝑑, based solely on the information
from 𝑉 and 𝑅. Suppose a subset of vertices𝑈 ⊆ 𝑉 is labelled with the presence or absence of
attributes 𝑎𝑖. For example, in a database of users and movies, we might have a subset𝑈 of users,
with each node labelled as over 18 or under 18. We train a logistic classifier to predict the value
of 𝑎𝑖 for each vertex𝑢 ∈ 𝑈 . See Figure1 for an illustration. In the case of our movie rating
example, private attributes could be gender, age, and occupation.
Figure 1: Schematic of detect-LC
 Figure 2: Schematic of detect-CCA

Figure 3: Schematic of detect-LD: Our Linear Decomposition System
Figure 4: First Moment Loss
detect-CCA: Canonical Correlation Analysis Canonical Correlation Analysis (CCA) is
used to measure the correlation information between two multivariate random variables [22].
Just like the univariate correlation coefficient, it is estimated on the basis of two aligned samples
of observations.
As above, we assume that a subset𝑈 ⊆ 𝑉 of vertices is labelled with the presence or absence
of attributes𝑎𝑖. Supposing we have𝑛 attributes, we can then form a Boolean-valued matrixA of
dimension |𝑈 | × 𝑛, where each row corresponds to a vertex in𝑈, and each column corresponds
to an attribute. In this matrix, each𝑢 ∈ 𝑈 is therefore represented by a vector of ones and zeros
corresponding to presence or absence of each attribute. Suppose we have a|𝑈 | × 𝑑 matrix of
vertex embeddingsU that we have learnt via our knowledge graph embedding. We compute
the CCA betweenA and U. We learn vectorsw𝐴 and w𝑈, such that the correlation between
the projectedA and projectedU are maximised, that is𝜌 = max(w𝐴,w𝑈) corr (Aw𝐴, Uw𝑈). Note
there are𝑘 correlations corresponding to𝑘 components.
In the example of viewers and movies, we use this method to compare two descriptions of
users, illustrated in Figure2. One matrix is based on demographic information, represented
by Boolean vectors. The other matrix is based on their behaviour, computed by their movie
ratings only.
detect-LD: Linear Decomposition Again assuming we have a matrix of entity embeddings
U with Boolean matrixA encoding the attribute information, we investigate the possibility
that the entity embeddings can be decomposed into a linear combination of embeddings corre-
sponding to attributes. Specifically, we investigate whether we can learn a matrixX by solving
AX = U.
We investigate here the possibility that entity embeddings in knowledge graphs can be
decomposed into linear combinations of embeddings corresponding to attributes. We use
methods from Xu et al. [23] to see if an entity embeddingu can be decomposed.
In our example of viewers and movies, we define a set of users as𝑈 and the Boolean encoding
matrix of the attributes asA. We aim to solve a linear systemAX = U, so that the user
embedding can be decomposed into three components (gender, age, occupation) as follows,
u = ∑𝑖 𝑎𝑖x𝑖, whereu is a user embedding,𝑖 ranges over all possible values of each private
attribute,x𝑖 is an embedding corresponding to the𝑖th attribute value, and𝑎𝑖 ∈ {0, 1} indicates the
presence or absence of that attribute value. Figure3 shows a running example of decomposing
user into gender and age (18-30 and 31-60). Figure3 shows the schematic of detect-LD.

Hypothesis Testing with Random Permutations We test whether our methods are able
to detect private information by comparing with randomly shuffled data. Our null hypothesis is
that the embedding of a vertex𝑢 and its attributes𝑎 are independent. To test whether this is the
case, we employ a non-parametric statistical test, whereby we directly estimate the𝑝-value as
theprobabilitythatwecouldobtaina“good” 1 valueoftheteststatisticunderthenullhypothesis.
If the probability of obtaining the observed value of the test statistic is less that 1%, we reject
the null hypothesis. Specifically, we will randomly shuffle the pairing of vertices and attributes
100 times, and compute the same test statistic. If the test statistic of the paired data is better
than that of the randomly shuffled data across all 100 random permutations, we conclude that
the correctly paired data performs better to a 1% significance level. The test statistic for the
logistic classifier is the accuracy of predicted labels, for CCA is the correlation𝜌, and for the
linear SystemAX = U we look at the L2 norm loss of the linear system, cosine similarity and
retrieval accuracy, a metric defined in [23].
4. Transparent Control of Bias
As well as detecting bias in a knowledge graph, we also wish to remove it. In the following, we
give two methods for removing bias based on a linear transformation method (remove-LP) as
well as an extension of this (remove-LP-multi), and two (remove-FM and remove-FM-multi)
based on penalising differences between the distribution of items with different protected
characteristics. The difference in distribution is approximated by comparing only the first
moments, though the method can be extended to further moments.
(remove-LP): Linear Transformation Werefertopreviousworkonwordembeddingdebias
[24] on eliminating sensitive attributes for user embedding. Suppose we have a knowledge
graph (𝑉 , ℱ , 𝐴) and an embedding of that graph, and we are interested in the attributes of
a subset𝑈 ⊆ 𝑉 of the vertices. Suppose we have private attribute𝑎 that we wish to protect,
which takes two values𝑚 and 𝑛. Let 𝑈𝑚 represnt a set of entity embeddings with attribute
𝑚, and𝑈𝑛 is a set of entity embeddings with attribute𝑛. If we identify a hyperplane that best
separates these two sets of points, then̂b can be defined as the normalised vector orthogonal to
the hyperplane pointing from𝑚 to 𝑛. Given a vertex embeddingu, we can project𝑢 onto the
hyperplane orthogonal to ̂b via u⟂ = u − (u ⋅ ̂b𝑇) ⋅ ̂b.
(remove-LP-multi): Linear Shifting for 2 or more classes For more than two classes, we
propose a new linear-shifting method. Again suppose we have a graph(𝑉 , ℱ , 𝐴), an embedding
of this graph, and a subset𝑈 ⊆ 𝑉 vertices with particular attributes. Suppose that we are able to
detect information about an attribute𝑎 that we wish to keep private, and𝑎 can take one of𝑛
values. We take the set of entity embeddings𝑈 = { u𝑖}, each having a value𝑎𝑗 of the attribute𝑎.
For instance, in our running example of movie rating,𝑈 may be users,𝑎 may be occupation,
and the values𝑎𝑗 could be{academic, artist, clerical, college student, ...}. Now, the set𝑈 of
embeddings is partitioned into𝑛 sets {𝑈1, ..., 𝑈𝑛} according to the value of𝑎. We calculate the
1either high or low, depending on the statistic

centroid 𝜇𝑗 of each of the sets𝑈𝑗, and then calculate the centroid𝜇 of all the centroids𝜇𝑗. Finally,
we shift each vectoru𝑗𝑘 ∈ 𝑈𝑗 by 𝜇 − 𝜇𝑗, so that now, all the sets𝑈𝑗 have the same centroid.
(remove-FM): First-Moment Loss Ideally, two sets of items that differ only along protected
dimensions should have the same distribution in the embedding space. Therefore we aim to
reduce the difference between distributions of items which differ in that way by penalising the
distance between first-moments of their empirical distribution (i.e. between their empirical
means) during the training process.
Againsupposewehaveagraph 𝐺 = (𝑉 , ℱ , 𝐴), asubsetofverticesofinterest 𝑈, anembedding
of this graph, and that we are able to detect information about an attribute𝑎 that we wish
to keep private. Consider two subsets of vertex embeddings𝑈𝑚 = { u𝑚𝑖} and 𝑈𝑛 = { u𝑛𝑗} with
private attribute𝑎 taking values𝑚 and 𝑛. For the first-moment loss we consider each of𝑈𝑚 and
𝑈𝑚 as multivariate distributions of the two classes𝑚 and 𝑛. We aim to remove the difference in
the first moments of the two classes by centering the mean coordinates of the two classes. An
illustration of this can be shown in Figure4. We follow Zemel et al.[13] and implement this
method on our knowledge graph. In order to do this we minimize the following loss function:
L = Loss + 𝜎 ‖ 𝑔𝑚
𝑁𝑚
∑
𝑖
u𝑚𝑖 + 𝑔𝑛
𝑁𝑛
∑
𝑗
u𝑛𝑗‖ (4)
where 𝑔𝑖 ∈ {−1, 1}, whilst𝑔𝑚 = 1, 𝑔𝑛 = −1. 𝑁𝑚, 𝑁𝑛 stand for the counts of vertices with attribute
taking values𝑚 and𝑛. 𝜎 is a weight parameter that gives more weight to the regularization, Loss
refers to Equations2, 3 for predicting relations/entities. Consider the example of knowledge
graph of viewers and movies, we aim to neutralize gender information in the first moment of
the two multivariate distributions by standardizing the mean coordinates across genders.
(remove-FM-multi): First-Moment loss for 2 or more classes For more than two classes,
we adapt the “mean-match” [25] process. We impose a constraint, limiting the norm of the
embeddings to 1. Our rationale for this is rooted in the belief that this constraint might preserve
or even boost the predictive capability of the model. We aim to test this conjecture and, if
corroborated, demonstrate its implications for the robustness of the predictive model. We
propose a new loss function in5,
L = 𝜃 ∗ Loss + ∑
𝑖
1
𝑁𝑐𝑖
(‖u𝑐𝑖 − 𝜇𝑐𝑖 ‖2 − 1)
2
+ ∑
𝑖𝑗
1
𝑁𝑐𝑖,𝑗
(𝜇𝑐𝑖 − 𝜇𝑐𝑗 )
2
(5)
where 𝑐𝑖,𝑗 ∈ {Class 1, Class2, Class3 ...}, 𝑁𝑐𝑖 is the count of vertices of class𝑖, 𝑁𝑐𝑖,𝑗 is the count of
combinations of different classes.𝜇𝑐𝑖 is the center point of class𝑖, 𝜃 is the weight parameter that
gives more weight to the Loss (the original loss in Equation2, 3) for predicting relations/entities.
5. Experimental Study
5.1. Datasets and Training Details
MovieLens ThisexperimentwasconductedontheMovieLens1Mdataset[ 26]whichconsists
of a large set of movies and users, and a set of movie ratings for each individual user. It is widely

used to create and test recommender systems.
Users and movies each have attributes. For example, users have demographic information
such as gender, age, or occupation. Whilst this information is typically used to improve the
accuracy of recommendations, we use it to test whether the embedding of a user correlates
to private attributes, such as gender or age. Crucially,we compute our graph embedding
based only on ratings, leaving out user attributes . Experiments for training knowledge
graph embeddings are implemented with the OpenKE [21] toolkit.
We use a 90:10 train:test split to train user and movie embeddings with triples
(𝑢𝑠𝑒𝑟, 𝑟𝑎𝑡𝑖𝑛𝑔, 𝑚𝑜𝑣 𝑖𝑒) . Initial embeddings are randomly assigned and optimized to minimize
loss as per equation(2). We sample 10 corrupted entities and 4 corrupted relations for each true
relation. The learning rate is 0.01 and epochs are set at 300. Link prediction on the 10% test set
yields an RMSE score of 0.88 (table2).
Citation Network The KG20C knowledge graph is constructed from 20 top AI conferences
[27]. The entities consist of 5407 papers, 8060 authors, 692 affiliations, 1920 domains, and 20
conferences. We train entity embeddings for papers, authors, affiliations, and domains, and
relation embeddings of the following four types: “Author in affiliation”, “Author write paper”,
“Paper cite paper” and “Paper in domain”.
We view the venue, i.e. conference, as information that we wish to detect and potentially
remove. As an application, suppose we are building a search engine and wish to avoid the “echo
chamber” of groups of authors citing each other’s work. Detecting conference information
could help to return a more diverse set of search results.
Embeddings for entities and relation types were randomly initialized and trained to minimize
the loss as per equation3, using a 0.05 learning rate over 300 epochs and a margin,𝛾, set to
6. Link prediction task metrics (Hits@10: 0.29, Hits@1: 0.075, MRR: 0.15, and MR: 1369.93)
attest to our embeddings’ quality. The bias-removal strength,𝜎, incrementally set to 50, 100,
and 150, increased the loss function’s bias-removal component. With 1/3 of triples sharing the
same head and relation but different tails, individual triples were tested to maintain accuracy.
To ensure the reproducibility of our results, we have made the code available athttps://github.
com/ZhijinGuo/EXTRACT.
5.2. MovieLens Bias Detection
We now apply our three methods for bias detection to investigate the extent to which private
information can be detected in user embeddings trained without that information.
detect-LC on MovieLens We use a logistic classifier to predict gender, age, and occupation
from the embeddings. We sub-sample the data to have balanced datasets with respect to gender,
age, and occupation.
Using an 80:20 training-to-test split across all datasets, we trained logistic classifiers for each
attribute, implemented via the scikit-learn toolkit [28]. Preliminary results highlight the model’s
ability to predict private traits, with 73% accuracy in predicting gender, approximately 72%
and 68% in predicting younger and older users respectively, and 59% accuracy for occupation
prediction. These binary classification results outperform the 0.50 baseline.

detect-CCA on MovieLens We collect attribute information for all 6040 users and represent
their personal attributes with Boolean indicator vectorsa𝑖 which encode the value of each
attribute (gender, age, and occupation). See figure2 for a schematic of these vectors.
We apply CCA to calculate the correlation between users and their attributes. We apply
the non-parametric statistical test described in section3. Specifically, our null hypothesis is
that users’ movie preferences are not correlated with their attributes. We calculate Pearson’s
correlation coefficient (PCC) between projectedAw𝐴 and projectedUw𝑈. We go on to calculate
the PCC between 100 randomly generated pairings of user and attribute embeddings, and find
that the PCC between true pairs of attribute and user embeddings is higher each time. We
therefore reject the null hypothesis at a 1% significance level. The correlation coefficients
between real pairs and random pairs is reported in figure5a.
(a) Pearson’s correlation coefficient (PCC) for true
user-attributepairingsand100permutedpairings.
PCC is calculated between projectedA and pro-
jected U. 𝑥 axes stands for the𝑘th components,
𝑦 axes gives the value. The PCC value for real
pairings is larger than for any permuted pairings.
(b) (t-SNE) visualisation [29] for paper embedding,
colour-coded by conference. Notice that even
though we do not use conference information in
learning these embeddings, information about
the conferences is clearly present in the embed-
dings.
Figure 5: Explainable Detection of Bias
detect-LD on MovieLens We investigate the ability of a user embedding to be reconstructed
as a linear sum of attribute embeddings. We find that a user embedding can be reconstructed as
a linear combination of its attributes by solving the linear system described in section3 with
pseudo-inverse method. In order to interpret the user embedding with user attributes such
as gender, age and occupation, we first group the user by age and gender firstly and compute
the mean embedding of 14 group of users. We afterwards group the user by gender, age and
occupation and compute the mean embedding of 241 group of users. Two test statistics are used
to test our linear system with significance threshold𝛼 = 0.01 .
As with the CCA setting, we permuted the pairing of users 100 times. Table1 shows the
observed p-value for three different statistics, which is the probability of seeing that value of
statistic under the null hypothesis. We first decompose the user embedding into gender and
age. Our results show the linear system is able to decompose the user embedding with a loss of
0.47, which is lower than every loss for a random permutation (1.11-2.11). The cosine similarity

Table 1
p-value for hypothesis test. Note that * indicates better than random baseline to significance level 𝛼 =
0.01. In our case, we are estimating directly the p-value, as the probability of an event, that we could
have a high (low) value of the test-statistic by chance under the null-hypothesis
L2 Norm Cosine Similarity Retrieval Acc. p-value
Gender, Age Real Pair 0.47* 99.8% 0.79* <0.01
Gender, Age Permuted 1.11-2.11* 96.5%-99.0% 0.00-0.14* <0.01
Gender, Age, Occ Real Pair 17.87* 97.1% 0.23* <0.01
Gender, Age, Occ Permuted 18.90-19.56* 96.2%-96.8% 0.00-0.08* <0.01
is 99.8%, higher than any permuted pairs. The identity retrieval accuracy is 0.79 which is higher
than any random permuted pairs (0.0-0.14). Therefore, the null hypothesis is rejected. This
shows that a user embedding can be reconstructed as a linear combination of gender and age.
When decomposing the embedding into gender, age and occupation, the L2 norm is 17.87
which is lower than every loss for a random permutation (18.90-19.56). The cosine similarity is
97.1%, higher than any permuted pairs. As for identity retrieval accuracy, although the value is
only 0.23 which is not a good result, it is still higher than any random permuted pairs (0.00-0.08).
Therefore, the null hypothesis is rejected.
5.3. Citation Network Bias Detection
We consider a dataset of scientific papers, whose entities are the papers, their authors, the
conference in which those papers were presented, and the scientific domain they belong to. For
the sake of example, we will treat as sensitive the information about the specific conferences in
which a given paper was presented (we could pretend that this information should not be used
as part of career assessment, and therefore should be hidden for this reason).
We embed scientific papers using their relations with the sets of authors and domains, and
then we will test if that embedding could contain enough information for a logistic classifier to
learn how to predict the specific conference. Note that this is a very strict requirement - that in
no way can any information relevant to this task be contained in the embedding of the paper.
Similar to the movie recommender system, we treat the conference information in this citation
network as a sensitive attribute.
Utilizing 5407 papers with respective author, citation, domain, and author affiliation relations,
we generate embeddings for each and label them with one of the 20 conferences, which are
then split into training and test sets. Our logistic classifier (detect-LC) yields a 55% accuracy in
conference venue prediction, surpassing the 13% baseline (5b). Despite not being trained on
conference data, the embeddings can still distinguish different conferences.
5.4. Transparent Control of Bias
We apply the techniques introduced in section4 to remove information about age and gender
from MovieLens-1M, and information about conference from the KG20C citation network.

(a) Gender - rating trade-off
 (b) Age - rating trade-off
Figure 6: Bias - rating prediction trade-off, model becomes gender neutral with slightly losing prediction
power
remove-LP for MovieLens We investigate the ability to remove the gender and age bias
detectedintheknowledgegraphuserembeddingwhilstmaintainingtheabilityoftheembedding
to predict behaviour. We apply remove-LP (section4) to remove gender and age information
from the data splits described in section5.2. We run the bias removal process for 10 iterations.
Results are reported in table2.
As depicted in figures6a and 6b, there is a trade-off between predictive power and bias. An
increase in iterations leads to a drop in gender classification accuracy from 73% to 54%, nearing
baseline accuracy, with a slight increase in RMSE from 0.88 to 0.93. A similar pattern is observed
in age bias removal, with accuracy for under/over 50s decreasing from 0.72 to 0.62, and RMSE
rising from 0.88 to 1.01.
remove-FM for MovieLens Weuseremove-FM(section 4)toremovebiasduringthetraining
of the embeddings. We again use embeddings and splits described in section5.2, and investigate
how well predictive power is retained as bias information is removed. Figures are reported
in table2. We see that as we increase the parameter𝜎, the accuracy of the gender classifier
decreases, although not monotonically. The RMSE increases slightly from 0.88 to 0.96.
remove-LP-multi for KG20C Regarding the KG20C dataset, we employ linear shifting
for classes greater than or equal to two to eliminate bias post-training, adjusting the paper
embedding to ensure that paper sets labelled with different conferences converge at a common
center. Results, detailed in Table3, indicate that the model, while becoming conference neutral,
experiences a minor decrease in predictive power (Hits@10 reduces from 0.29 to 0.21).
remove-FM for KG20C Weapplythemethodsdescribedinthemulti-classversionofremove-
FM(section 4). Theembeddingsaredebiasedduringtraining. Aparameter 𝜃 weightsthestrength
of the prediction power. We set𝜃 to 1 and 20, to increase the influence of the prediction part
of the loss function. As shown in Table3, a larger𝜃 slightly improves Hits@10 but decreases
Hits@1 and MR. Additionally, the retained conference information increases accuracy from
0.14 to 0.26, though Hits@10 drops 0.14, signifying a trade-off between prediction power and
unwanted information removal.

Table 2
Performance Comparison for Gender and Age Bias Removal, Mean accuracies for the gender and age
logistic classifiers are reflected in the respective gender and age rows. Random refers to untrained
random embedding, KG refers to the non-debiased embedding, while 50, 100, 150 represent for the value
of 𝜎, underline numbers denote mean accuracy of logistic classifier for embedding without debiasing.
We compare our results with the best results from the literature, ICML_2019 [ 16], and FairGo [ 17].
Random KG remove-LP remove-FM50/100/150 ICML_2019 FairGo
RMSE 1.26 0.88 0.93 1.01 0.96 0.96 0.96 0.92 0.92
Gender 0.50 0.73 0.54 - 0.66 0.62 0.58 0.53 0.50
Age 0.50 0.72 - 0.62 - - - - -
Table 3
Performance Comparison for Conference Bias Removal, The mean accuracies for conference logistic
classifiers are reflected in the respective conference column. Random refers to untrained random
embedding, KG refers to the embedding without debiasing, underline numbers denote mean accuracy
of logistic classifier for embedding without debiasing. 1, 20 represent for the value of 𝜃.
Hits@1 Hits@10 MRR MR Conference
Random 0.00 0.00 0.00 4106.62 0.15
KG 0.075 0.29 0.15 1369.93 0.55
remove-LP-multi 0.053 0.21 0.11 2044.66 0.10
remove-FM-multi1 0.05 0.15 0.09 971.57 0.14
remove-FM-multi20 0.04 0.17 0.09 1466.61 0.26
6. Discussion and Conclusions
In this work, we introduced EXTRACT, a comprehensive framework that combined three
methods for detecting and four methods for removing biases in knowledge graph embeddings.
Using datasets like MovieLens 1M and KG20C, EXTRACT efficiently identified leaks of sensitive
attributes and unintended conference affiliations. This two-step process ensured that specific
dimensions of user embeddings, correlating to private or sensitive attributes, were identified and
appropriately treated. Our findings showed that the correlations between the private attributes
and the user representations were significantly higher than random, validating the efficacy of
EXTRACT in capturing statistical patterns that reflect private attribute information.
Furthermore, our linear decomposition system, an integral part of the EXTRACT framework,
revealed that user-behaviour-embedding can be approximated by a sum of user-demographic
vectors. This validated the framework’s ability to decompose user embeddings into a weighted
sum of attribute embeddings, thereby allowing for the targeted removal or control of bias.
Our four approaches to debiasing were more transparent and explainable than more complex
methods. Remove-LP method was most successful at debiasing, whilst retaining relatively good
performance than the link prediction task. Overall, EXTRACT served as a unified, two-step
approach that advanced the field towards ethical and transparent knowledge graph embeddings.

References
[1] R. L. Logan IV, N. F. Liu, M. E. Peters, M. Gardner, S. Singh, Barack’s wife hillary: Using
knowledge-graphs for fact-aware language modeling, arXiv preprint arXiv:1906.07241
(2019).
[2] Z. Dai, L. Li, W. Xu, Cfo: Conditional focused neural question answering with large-scale
knowledge bases, arXiv preprint arXiv:1606.01994 (2016).
[3] L. Bauer, Y. Wang, M. Bansal, Commonsense for generative multi-hop question answering
tasks, arXiv preprint arXiv:1809.06309 (2018).
[4] S. Ji, S. Pan, E. Cambria, P. Marttinen, S. Y. Philip, A survey on knowledge graphs:
Representation, acquisition, and applications, IEEE transactions on neural networks and
learning systems 33 (2021) 494–514.
[5] M. Kosinski, D. Stillwell, T. Graepel, Private traits and attributes are predictable from
digital records of human behavior, Proceedings of the national academy of sciences 110
(2013) 5802–5805.
[6] A. Caliskan, J. J. Bryson, A. Narayanan, Semantics derived automatically from language
corpora contain human-like biases, Science 356 (2017) 183–186.
[7] J. Pennington, R. Socher, C. D. Manning, Glove: Global vectors for word representation, in:
Proceedings of the 2014 conference on empirical methods in natural language processing
(EMNLP), 2014, pp. 1532–1543.
[8] T. Mikolov, I. Sutskever, K. Chen, G. S. Corrado, J. Dean, Distributed representations of
words and phrases and their compositionality, Advances in neural information processing
systems 26 (2013).
[9] D. Jonauskaite, A. Sutton, N. Cristianini, C. Mohr, English colour terms carry gender and
valence biases: A corpus study using word embeddings, PloS one 16 (2021) e0251559.
[10] T. Bolukbasi, K.-W. Chang, J. Y. Zou, V. Saligrama, A. T. Kalai, Man is to computer
programmer as woman is to homemaker? debiasing word embeddings, Advances in
neural information processing systems 29 (2016).
[11] D. Madras, E. Creager, T. Pitassi, R. Zemel, Learning adversarially fair and transferable
representations, in: International Conference on Machine Learning, PMLR, 2018, pp.
3384–3393.
[12] J. Chen, H. Dong, X. Wang, F. Feng, M. Wang, X. He, Bias and debias in recommender
system: A survey and future directions, ACM Transactions on Information Systems 41
(2023) 1–39.
[13] R. Zemel, Y. Wu, K. Swersky, T. Pitassi, C. Dwork, Learning fair representations, in:
International conference on machine learning, PMLR, 2013, pp. 325–333.
[14] H. Edwards, A. Storkey, Censoring representations with an adversary, arXiv preprint
arXiv:1511.05897 (2015).
[15] Z. Zhu, J. Wang, J. Caverlee, Measuring and mitigating item under-recommendation bias
in personalized ranking systems, in: Proceedings of the 43rd international ACM SIGIR
conference on research and development in information retrieval, 2020, pp. 449–458.
[16] A. Bose, W. Hamilton, Compositional fairness constraints for graph embeddings, in:
International Conference on Machine Learning, PMLR, 2019, pp. 715–724.
[17] L. Wu, L. Chen, P. Shao, R. Hong, X. Wang, M. Wang, Learning fair representations for

recommendation: A graph-based perspective, in: Proceedings of the Web Conference
2021, 2021, pp. 2198–2208.
[18] J. Fisher, A. Mittal, D. Palfrey, C. Christodoulopoulos, Debiasing knowledge graph em-
beddings, in: Proceedings of the 2020 Conference on Empirical Methods in Natural
Language Processing (EMNLP), Association for Computational Linguistics, Online, 2020,
pp. 7332–7345. URL:https://aclanthology.org/2020.emnlp-main.595. doi:1 0 . 1 8 6 5 3 / v 1 / 2 0 2 0 .
e m n l p - m a i n . 5 9 5.
[19] R. v. d. Berg, T. N. Kipf, M. Welling, Graph convolutional matrix completion, arXiv preprint
arXiv:1706.02263 (2017).
[20] B. Yang, W.-t. Yih, X. He, J. Gao, L. Deng, Embedding entities and relations for learning
and inference in knowledge bases, arXiv preprint arXiv:1412.6575 (2014).
[21] X. Han, S. Cao, X. Lv, Y. Lin, Z. Liu, M. Sun, J. Li, OpenKE: An open toolkit for knowledge
embedding, in: Proceedings of the 2018 Conference on Empirical Methods in Natural
Language Processing: System Demonstrations, Association for Computational Linguistics,
Brussels, Belgium, 2018, pp. 139–144. URL:https://aclanthology.org/D18-2024. doi:1 0 .
1 8 6 5 3 / v 1 / D 1 8 - 2 0 2 4.
[22] J. Shawe-Taylor, N. Cristianini, et al., Kernel methods for pattern analysis, Cambridge
university press, 2004.
[23] Z. Xu, Z. Guo, N. Cristianini, On compositionality in data embedding, in: Advances in
Intelligent Data Analysis XXI: 21st International Symposium, IDA 2023, Springer, 2023.
[24] A. Sutton, T. Lansdall-Welfare, N. Cristianini, Biased embeddings from wild data: Mea-
suring, understanding and removing, in: International Symposium on Intelligent Data
Analysis, Springer, 2018, pp. 328–339.
[25] T. Kamishima, S. Akaho, H. Asoh, J. Sakuma, Enhancement of the neutrality in recommen-
dation., in: Decisions@ RecSys, 2012, pp. 8–14.
[26] F.M.Harper, J.A.Konstan, Themovielensdatasets: Historyandcontext, Acmtransactions
on interactive intelligent systems (tiis) 5 (2015) 1–19.
[27] H. N. Tran, A. Takasu, Exploring scholarly data by semantic query on knowledge graph
embeddingspace, in: DigitalLibrariesforOpenKnowledge: 23rdInternationalConference
on Theory and Practice of Digital Libraries, TPDL 2019, Oslo, Norway, September 9-12,
2019, Proceedings 23, Springer, 2019, pp. 154–162.
[28] F. Pedregosa, G. Varoquaux, A. Gramfort, V. Michel, B. Thirion, O. Grisel, M. Blondel,
P. Prettenhofer, R. Weiss, V. Dubourg, J. Vanderplas, A. Passos, D. Cournapeau, M. Brucher,
M. Perrot, E. Duchesnay, Scikit-learn: Machine learning in Python, Journal of Machine
Learning Research 12 (2011) 2825–2830.
[29] L. Van der Maaten, G. Hinton, Visualizing data using t-sne., Journal of machine learning
research 9 (2008).
```
