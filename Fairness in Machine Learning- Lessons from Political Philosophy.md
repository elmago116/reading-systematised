---
title: Fairness in Machine Learning- Lessons from Political Philosophy
year: "2017"
Type: Article
DOI: ""
source: https://proceedings.mlr.press/v81/binns18a.html
created: 2026-04-24
description: "Fairness in Machine Learning: Lessons from Political PhilosophyReuben BinnsWhat does it mean for a machine learning model to be ‘fair’, in terms which can be..."
tags:
  - op/acc/pending-review
  - themes/ethics
  - themes/bias/algorithmic
  - Tech/AI
  - Humanities
  - humanities/EJ
  - themes/bias/algorithmic/bias-auditing-tools
  - themes/bias
pdfORepub: "[[Fairness in Machine Learning- Lessons from Political Philosophy.pdf]]"
author: "[[PMLR]]"
published: 2018-01-21
---

![[Fairness in Machine Learning- Lessons from Political Philosophy.pdf]]
## Full text (extracted from `Fairness in Machine Learning- Lessons from Political Philosophy.pdf`)

*Source:* `2PDF/Fairness in Machine Learning- Lessons from Political Philosophy.pdf`  
*Extracted:* 2026-04-24

```text
Proceedings of Machine Learning Research 81:1–11, 2018 Conference on Fairness, Accountability, and Transparency
Fairness in Machine Learning: Lessons from Political
Philosophy
Reuben Binns reuben.binns@cs.ox.ac.uk
Department of Computer Science, University of Oxford, United Kingdom
Editors: Sorelle A. Friedler and Christo Wilson
Abstract
What does it mean for a machine learning
model to be ‘fair’, in terms which can be
operationalised? Should fairness consist of
ensuring everyone has an equal probabil-
ity of obtaining some beneﬁt, or should we
aim instead to minimise the harms to the
least advantaged? Can the relevant ideal
be determined by reference to some alter-
native state of aﬀairs in which a particu-
lar social pattern of discrimination does not
exist? Various deﬁnitions proposed in re-
cent literature make diﬀerent assumptions
about what terms like discrimination and
fairness mean and how they can be deﬁned
in mathematical terms. Questions of dis-
crimination, egalitarianism and justice are
of signiﬁcant interest to moral and polit-
ical philosophers, who have expended sig-
niﬁcant eﬀorts in formalising and defending
these central concepts. It is therefore un-
surprising that attempts to formalise ‘fair-
ness’ in machine learning contain echoes of
these old philosophical debates. This paper
draws on existing work in moral and politi-
cal philosophy in order to elucidate emerg-
ing debates about fair machine learning.
Keywords: fairness, discrimination,
machine learning, algorithmic decision-
making, egalitarianism
1. Introduction
Machine learning allows us to predict and clas-
sify phenomena, by training models using labeled
data from the real world. When consequential de-
cisions are made about individuals on the basis of
the outputs of such models, concerns about dis-
crimination and fairness inevitably arise. What
if the model’s outputs result in decisions that are
systematically biased against people with certain
protected characteristics like race, gender or reli-
gion? If there are underlying patterns of discrim-
ination in the real world, such biases will likely be
picked up in the learning process. This could re-
sult in certain groups being unfairly denied loans,
insurance, or employment opportunities. Cog-
nisant of this problem, a burgeoning research
paradigm of ‘discrimination-aware data mining’
and ‘fair machine learning’ has emerged, which
attempts to detect and mitigate unfairness Ha-
jian and Domingo-Ferrer (2013); Kamiran et al.
(2013); Barocas and Selbst (2016).
One question which immediately arises in such
an endeavour is the need for formalisation. What
does it mean for a machine learning model to
be ‘fair’ or ‘non-discriminatory’, in terms which
can be operationalised? Various measures have
been proposed. A common theme is compar-
ing diﬀerences in treatment between protected
and non-protected groups, but there are multiple
ways to measure such diﬀerences. The most basic
would be ‘disparate impact’ or ‘statistical / de-
mographic parity’, which consider the overall per-
centage of positive/ negative classiﬁcation rates
between groups. However, this is blunt, since it
fails to account for discrimination which is ex-
plainable in terms of legitimate grounds Dwork
et al. (2012). For instance, attempting to enforce
equal impact between men and women in recidi-
vism prediction systems, if men have higher re-
oﬀending rates, could result in women remaining
in prison longer despite being less likely to re-
oﬀend.
A range of more nuanced measures have been
proposed, including; ‘accuracy equity’, which
considers the overall accuracy of a predictive
model for each group Angwin et al. (2016); ‘con-
ditional accuracy equity’, which considers the ac-
curacy of a predictive model for each group, con-
ditional on their predicted class Dieterich et al.
(2016); ‘equality of opportunity’, which considers
c⃝ 2018 R. Binns.

Fairness in Machine Learning: Lessons from Political Philosophy
whether each group is equally likely to be pre-
dicted a desirable outcome given the actual base
rates for that group Hardt et al. (2016); and ‘dis-
parate mistreatment’, a corollary which considers
diﬀerences in false positive rates between groups
Zafar et al. (2017). Another deﬁnition involves
imagining counterfactual scenarios wherein mem-
bers of protected groups are instead members of
the non-protected group Kusner et al. (2017). To
the extent that outcomes would diﬀer, the system
is unfair; i.e. a woman classiﬁed by a fair system
should get the same classiﬁcation she would have
done in a counterfactual scenario in which she
had been born a man.
Ideally, a system might be expected to meet all
of these intuitively plausible measures of fairness.
But, somewhat problematically, certain measures
turn out to be mathematically impossible to sat-
isfy simultaneously except in rare and contrived
circumstances Kleinberg et al. (2016), and there-
fore hard choices between fairness metrics must
be made before the technical work of detecting
and mitigating unfairness can proceed. A fur-
ther underlying tension is that fairness may also
imply that similar people should be treated sim-
ilarly, but this is often in tension with the ideal
of parity between groups, when base rates for
the target variable are diﬀerent between those
groups Dwork et al. (2012). Fair machine learn-
ing therefore faces an upfront set of conceptual
ethical challenges; which measures of fairness are
most appropriate in a given context? Which vari-
ables are legitimate grounds for diﬀerential treat-
ment, and why? Are all instances of disparity
between groups objectionable? Should fairness
consist of ensuring everyone has an equal prob-
ability of obtaining some beneﬁt, or should we
aim instead to minimise the harms to the least
advantaged? In making such tradeoﬀs, should
the decision-maker consider only the harms and
beneﬁts imposed within the decision-making con-
text, or also those faced by decision-subjects in
other contexts? What relevance might past, fu-
ture or inter-generational injustices have?
Such questions of discrimination and fairness
have long been of signiﬁcant interest to moral
and political philosophers, who have expended
signiﬁcant eﬀorts in formalising, diﬀerentiating
and debating many of the central concepts in-
volved. It is therefore unsurprising that attempts
to formalise fairness in machine learning contain
echoes of these old philosophical debates. Indeed,
some seminal work in the FAT-ML community
explicitly refers to political philosophy as inspi-
ration, albeit in a limited and somewhat ad-hoc
way.1 A more comprehensive overview could pro-
vide a wealth of argumentation which may use-
fully apply to the questions arising in the pur-
suit of more ethical algorithmic decision-making.
This article aims to provide an overview of some
of the relevant philosophical literature on dis-
crimination, fairness and egalitarianism in order
to clarify and situate the emerging debate within
the discrimination-aware and fair machine learn-
ing literature. Throughout, I aim to address the
conceptual distinctions drawn between terms fre-
quently used in the fair ML literature–including
‘discrimination’ and ‘fairness’–and the use of re-
lated terms in the philosophical literature. The
purpose of this is not merely to consider similar-
ities and diﬀerences between the two discourses,
but to map the terrain of the philosophical de-
bate and locate those points which provide help-
ful clariﬁcation for future research on algorith-
mic fairness, or otherwise raise relevant problems
which have yet to be considered in that research.
I begin by discussing philosophical accounts
of what discrimination is and what makes it
wrong, if and when it is wrong. I show how on
certain accounts of what makes discrimination
wrong, the proposed conditions are unlikely to
obtain in algorithmic decision-making contexts.
If correct, these accounts do not necessarily im-
ply that algorithmic decision-making is always
morally benign–only that its potential wrongness
is not to be found in the notion of discrimination
as it is traditionally understood. This leads us
to consider other grounds on which algorithmic
decision-making might be problematic, which are
primarily captured by a variety of considerations
connected to the ideals of egalitarianism–the no-
tion that human beings are in some fundamen-
tal sense equal and that eﬀorts should be made
to avoid and correct certain forms of inequality.
This discussion suggests that ‘fairness’ as used
in the fair machine learning community is best
understood as a placeholder term for a variety
of normative egalitarian considerations. Notably,
1. Notable examples include references to the work of
authors such as H. Peyton Young, John Rawles, and
John Roemer in Dwork et al. (2012); Joseph et al.
(2016).
2

Fairness in Machine Learning: Lessons from Political Philosophy
while egalitarianism is a widely held principle, ex-
actly what it requires is the subject of much de-
bate. I provide an overview of some of this debate
and ﬁnish with implications for the incorporation
of ‘fairness’ into algorithmic decision-making sys-
tems.
2. What is discrimination, and
what makes it wrong?
Early work which explored how to embed fair-
ness constraints in machine learning used the
term ‘discrimination-aware’ rather than ‘fair’.
While this terminological diﬀerence may seem
relatively insigniﬁcant amongst computer scien-
tists, it points to a potentially important distinc-
tion which has been the preoccupation of much
philosophical writing on the topic. For philoso-
phers, the division of moral phenomena into con-
ceptually coherent categories is both intrinsically
satisfying, and, hopefully, brings helpful clariﬁ-
cation to otherwise perplexing issues. Getting a
closer conceptual grip over what discrimination
consists in, what (if anything) makes it distinc-
tively wrong, and how it relates to other moral
concepts such as fairness, should therefore help
clarify whether and when algorithmic systems
can be wrongfully discriminatory and what ought
to be done about them. It may turn out that so-
called ‘algorithmic discrimination’ diﬀers in im-
portant ways to classical forms of discrimination,
such that diﬀerent counter-measures are appro-
priate.
2.1. Mental state accounts
Paradigm cases of discrimination include diﬀer-
ential treatment on the basis of membership of
a salient social group–e.g. gender or ‘race’–by
those with decision-making power to distribute
harms or beneﬁts. Examples include employers
who prefer to hire a male job applicant over an
equally qualiﬁed female applicant, or parole of-
ﬁcers who impose stricter conditions on parolees
of a particular minority in comparison to a priv-
ileged majority. Focusing on these paradigm
cases, a range of accounts of what makes discrim-
ination wrong place emphasis on the intentions,
beliefs and values of the decision-maker. For
such mental state accounts, defended by among
others Richard Arneson, Thomas Scanlon, and
Annabelle Lever, the existence of systematic ani-
mosity or preferences for or against certain salient
social groups on the part of the decision-maker
is what makes discrimination wrong Arneson
(1989); Lever (2016); Scanlon (2009). Such con-
cerns might be couched in terms of the defective
moral character of the decision maker–that they
show bad intent or animosity, for example-or in
terms of the harmful eﬀect of such intentions on
the discriminated-against individual, such as hu-
miliation as a result of lack of respect.
On such accounts, the decision-maker’s intent
is key to discrimination. A decision-maker with
no such intent, who nonetheless accidentally and
unwittingly created such disparities, would ar-
guably not be guilty of wrongful discrimination
(even if the situation is morally problematic on
other grounds). Such cases–often called indirect
or institutional discrimination in the UK, or in
the U.S., disparate impact–might still count as
discriminatory on a mental state account of dis-
crimination if the failure of decision-makers to
anticipate such disparities, or to redress them
when they become apparent, is suﬃciently simi-
larly morally objectionable to the failure to treat
people equally in the ﬁrst instance. However, if
such conditions do not obtain, then indirect dis-
crimination, while it may be wrong, may not use-
fully be described as an instance of discrimination
at all Eidelson (2015).
This line of thinking suggests a potential chal-
lenge to the notion of algorithmic discrimina-
tion. If the possession of certain mental states by
decision-makers is a necessary condition of a de-
cision being discriminatory, one might argue that
algorithmic decision-making systems can never
be discriminatory as such, because such systems
are incapable of possessing the relevant mental
states. This is not the place for discussion of the
possibility of machine consciousness, but assum-
ing that it is not (yet) a reality, it seems that AI
and autonomous decision-making systems cannot
be the bearers of states such as contempt, ani-
mosity, or disrespect that would be required for
a decision to qualify as discriminatory on such
accounts.
That said, proponents of mental state ac-
counts might similarly argue that algorithmic
decision-making systems might involve discrim-
ination, without imputing the algorithm with
mental states. First, they might argue that hu-
3

Fairness in Machine Learning: Lessons from Political Philosophy
man decision-makers, and data scientists respon-
sible for building decision models, might some-
times be condemned if they possess bad inten-
tions which result in them intentionally embed-
ding biases in their system, or if they negligently
ignore or overlook unintended disparities result-
ing from it. Second, as social epistemologists
have argued, we can sometimes still morally eval-
uate decisions which do not stem from one in-
dividual but are the result of multiple individ-
ual judgements aggregated in variously complex
ways Gilbert (2004); Pettit (2007). Drawing
from work on judgement aggregation problems
in economics and social choice theory, they ar-
gue that when suitably arranged in institutional
decision-making scenarios, groups of people can
be held morally responsible for their collective
judgements. Machine learning models trained on
data consisting of previous human judgements
might therefore be critiqued on similar grounds if
those individual judgements were themselves the
result of similarly discriminatory intent on the
part of those individuals.
However, aside from such special cases, it
seems that mental state accounts of discrim-
ination do not naturally transfer to the con-
text of algorithmic decision-making. If these ac-
counts are correct, we might therefore conclude
that algorithmic decision-making, while poten-
tially morally problematic, should not be charac-
terised as an example of wrongful discrimination.
Alternatively, other accounts of why discrimina-
tion is (sometimes) wrongful which are not based
on mental states of the decision-maker, might be
better able to accommodate discrimination of an
algorithmic variety.
2.2. Failing to treat people as individuals
One such account, which has received signiﬁ-
cant attention in recent writing on discrimina-
tion, locates the wrongness of discrimination–in
both its direct and indirect varieties–in the ex-
tent to which it relies on inferences about in-
dividuals based on generalisations about groups
of which they are a member Lippert-Rasmussen
(2014). This objection is frequently raised in re-
sponse to what is often called statistical discrim-
ination Phelps (1972). Statistical discrimina-
tion is the use of statistical generalisations about
groups to infer attributes or future behaviours of
members of those groups. For instance, an em-
ployer might read evidence purporting to show
that smokers are generally less hard-working than
non-smokers, and reject a job application from
a smoker and give the job a less qualiﬁed non-
smoker who is anticipated to be more productive.
As economists have argued on the basis of
models, such generalisations about groups can be
an eﬃcient means for ﬁrms to reduce risk when
more direct evidence about an individual is lack-
ing Phelps (1972). Despite the potential eﬃ-
ciency beneﬁts of generalisation, it is widely re-
garded as wrong in at least some cases. While
intuitions about the wrongfulness of statistical
discrimination are widely shared, it has proven
surprisingly diﬃcult to articulate coherent objec-
tions to the practice, particularly when we go
beyond simple cases in which the inference is
simply unsupported by rigorous statistical anal-
ysis, to those where membership of a group re-
ally does correlate with an outcome of interest to
the decision-maker. Since algorithmic decision-
making could be regarded as a form of gener-
alisation on steroids, any account of discrimina-
tion which is grounded in the wrongness of gen-
eralisation would be particularly pertinent to our
present concerns.
On one popular account, statistical discrimi-
nation is wrong, even if the generalisations in-
volved have some truth, because it fails to treat
the decision-subject as an individual. Subject-
ing travellers from Muslim-majority countries to
harsher border checks on the basis of generalisa-
tions (whether true or false) about the prepon-
derance of terrorism amongst such groups fails
to consider each individual traveler on their own
merit. Similarly, rejecting a job applicant who
smokes because of evidence that smokers are on
average (let us assume, for the sake of argument)
less productive, unfairly punishes them as a re-
sult of the behaviour of other members of that
group. Such examples have led some to ground
objections to statistical discrimination in its fail-
ure to treat people as individuals. If this is cor-
rect, it presents a strong challenge to the very ex-
istence of algorithmic decision-making systems;
since they fail to treat people as individuals by
design. Given any two individuals with the same
attributes, a deterministic model will give the
same output, and would therefore, on this ac-
count, be quintessentially discriminatory.
4

Fairness in Machine Learning: Lessons from Political Philosophy
However, others have argued that the fail-
ure to treat people as individuals cannot plau-
sibly be the essence of wrongful discrimina-
tion Schauer (2009); Dworkin (1981); Lippert-
Rasmussen (2014). One concern is that this cri-
terion is too broad because it encompasses gen-
eralisation against any kind of group, not just
those categories enshrined in human rights law
such as gender, ‘race’, religion, etc. While such
categories readily trigger concerns about wrong-
ful discrimination, other categories like ‘smoker’
do not obviously invoke discrimination concerns.
This suggests that it is only generalisations about
certain groups that matter vis--vis discrimina-
tion. Others object that the very notion of ‘treat-
ing someone as an individual’ is misconceived;
they argue that, on closer inspection, even deci-
sions which appear to consider the individual are
in fact a disguised form of generalisation Schauer
(2009). Suppose that rather than using ‘smoker
/ non-smoker’ as a predictor of productivity, the
employer requires applicants to undergo some
test which more accurately predicts productivity;
even in this case, as Schauer argues, the employer
must rely upon generalizations from test scores to
on-the-job behavior. Test scores might be a more
accurate predictor than ‘smoker / non-smoker’,
but they are still fundamentally a form of gen-
eralization ( Schauer (2009), p68). Unless the
test is perfect, some people who perform badly
on it would nevertheless turn out to be relatively
productive on-the-job.
If this line of critique is correct, then it can-
not be the case that treating people diﬀerently
on the basis of generalisations about a category
they ﬁt into is necessarily discriminatory in any
wrongful sense. What appear to be criticisms
of generalization in general(!), may in fact boil
down to criticisms of insuﬃciently precise means
of generalization. If the border security sys-
tem (or the recruitment process) could identify
more accurate predictor variables, which resulted
in fewer burdens on innocent tourists (or hard-
working smokers), then the charge of discrimi-
nation might lose some force. Of course, more
accurate predictions are likely to be more costly,
and as such tradeoﬀs must be made between the
harms and beneﬁts of generalization; but either
way, this view suggests that anti-discrimination
does not necessarily require treating people as in-
dividuals. Rather, statistical discrimination may
be more or less morally permissible depending on
who and how many people are wrongly judged
on the basis of membership of whatever statis-
tical groups they may be part of, compared to
the costs involved in improving the accuracy of
the generalisation. If correct, this should be a
welcome conclusion for proponents of algorith-
mic systems, since they are essentially based on
generalisations in some form or other.
So far I have presented arguments which sug-
gest that there are diﬃculties with accounting for
algorithmic discrimination in terms of the wrong-
ness of mental states or of generalisations. Some
of these diﬃculties are internal to the philosoph-
ical accounts of discrimination, and others stem
from the dis-analogy between human and algo-
rithmic decision-makers. If the wrongness of (al-
gorithmic) discrimination does not consist in the
morally suspect intentions of decision-makers, or
in failing to treat people as individuals, then what
might it consist in? A more general set of egal-
itarian norms might provide a better footing for
a theory of algorithmic fairness. 2
3. Egalitarianism
Broadly speaking, egalitarianism is the idea that
people should be treated equally, and (some-
times) that certain valuable things should be
equally distributed. It might seem entirely ob-
vious that what makes discrimination wrongful
is something to do with egalitarianism. How-
ever, this connection has, perhaps surprisingly,
been resisted by many of the previously men-
tioned theorists of discrimination, with one even
claiming that any ‘connection between anti-
discrimination laws and equality it is at best neg-
ligible, and in any event is insuﬃcient to count as
a justiﬁcation’ Holmes (2005). Meanwhile, oth-
ers argue the opposite: that only a direct appeal
to egalitarian norms can satisfactorily account
for everything that is wrong about discrimina-
tion Segall (2012). For our current purposes,
this debate can be safely sidestepped. This is
not because it is uninteresting or unimportant
2. However, even if philosophical accounts of discrimina-
tion do not easily apply to algorithmic decisions, call-
ing an algorithmic system discriminatory, (or speciﬁ-
cally sexist, racist, etc.) might still be justiﬁed by its
rhetorical power, or as useful shorthand in everyday
discourse.
5

Fairness in Machine Learning: Lessons from Political Philosophy
as a philosophical project. Rather, our purpose
here is to examine how egalitarian norms might
provide an account of why and when algorithmic
systems can be considered unfair; whether or not
such unfairness should rightfully be considered a
form of discrimination, per se, is not our concern.
This section therefore provides a brief overview
of some major debates within egalitarianism and
draws out their signiﬁcance for fair machine
learning.
3.1. The currency of egalitarianism and
spheres of justice
Invariably in machine learning contexts where
fairness issues arise, a system is mapping indi-
viduals to diﬀerent outcome classes which are as-
sumed to have negative and positive eﬀects; such
as being approved / denied a ﬁnancial loan, high
or low insurance prices, or a greater or fewer num-
ber of years spent under incarceration. We as-
sume that these outcome classes are means or
barriers to some fundamentally valuable object
or set of objects which ought to be to some ex-
tent equally distributed. But what exactly is
the ‘currency’ of egalitarianism that lies behind
the valuation of these outcome classes? Egalitar-
ians have articulated various competing views,
including welfare, understood in terms of plea-
sure or preference-satisfaction Cohen (1989); re-
sources such as income and assets Rawls (2009);
Dworkin (1981); or capabilities, understood as
both the ability and resources necessary to do
certain things Sen (1992). Others propose that
inequalities in welfare, resources, or capabilities
may be acceptable, so long as citizens have equal
political and democratic status Anderson (1999).
The question of what egalitarianism is con-
cerned with (the ‘equality of what?’ debate as
it is sometimes referred to), is relevant to our as-
sumptions about the impact of diﬀerent algorith-
mic decision outcomes. In many cases – like the
automated allocation of loans, or the setting of
insurance premiums – the decision outcomes pri-
marily aﬀect distribution of resources. In others
– like algorithmic blocking or banning of users
from an online discussion – the decisions may
be more directly related to distribution of wel-
fare or capabilities. The importance of each cur-
rency of egalitarianism may plausibly diﬀer be-
tween contexts, thus aﬀecting how we account for
the potentially diﬀerential impacts of algorithmic
decision-making systems.
This debate also trades heavily on the intu-
ition that diﬀerent people may value the same
outcome or set of harms and beneﬁts diﬀerently;
yet most existing work on fair machine learning
assumes a uniform valuation of decision outcomes
across diﬀerent populations. In some cases it may
be safe to assume that diﬀerent sub-groups are
equally likely to regard a particular outcome class
– e.g. being denied a loan, or being hired for a job
- as bad or good. But in other cases, especially in
personalisation and recommender systems where
there are multiple outcome classes with no ob-
vious universally agreed-on rank order, this as-
sumption may be ﬂawed.
A connected debate concerns whether we
should apply a single egalitarian calculus across
diﬀerent social contexts, or whether there are in-
ternal ‘spheres of justice’ in which diﬀerent in-
commensurable logics of fairness might apply,
and between which redistributions might not be
appropriate Walzer (2008). For instance, with
regard to civil and democratic rights like voting
in elections, the aim of egalitarianism might be
absolute equal distribution of the good, rather
than merely equality of opportunity to compete
for it. This idea would explain the intuition that
voter registration tests are wrong, while tests for
jobs are not. Requiring some form of test prior
to voting may ensure equality of opportunity in
the sense that everyone has an equal opportunity
to take the test; but since talent and eﬀorts are
not equally distributed, some people may fail the
test, and there would not be equality of outcome.
But an essential element of democracy, one might
argue, is that voting rights shouldn’t depend on
talent or eﬀort. However, when it comes to com-
petition for social positions and economic goods,
we may be concerned with ensuring equality of
opportunity but less concerned about equality of
outcome. We may consider it fair, other things
being equal, that the most qualiﬁed applicant ob-
tains the role, and that the most industrious and
/ or talented individuals deserve more economic
beneﬁts than others (even if we believe that cur-
rent systems do not actually ensure a level play-
ing ﬁeld, and some level of income redistribution
is also morally required).
Diﬀerent contexts being subject to diﬀerent
spheres of justice would have a direct bearing on
6

Fairness in Machine Learning: Lessons from Political Philosophy
the appropriateness of certain fairness-correcting
methods in those contexts. Equality of oppor-
tunity may be an appropriate metric to apply
to models that will be deployed in the sphere of
‘economic justice’; e.g. selection of candidates for
job interviews or calculation of insurance. But in
contexts which fall under the sphere of civil jus-
tice, we may want to impose more blunt metrics
like equality of outcome (or ‘parity of impact’).
This might be the case for airport security checks,
where it is important to a sense of social solidar-
ity that no group is over-examined as a result of
a predictive system, even if there really are diﬀer-
ences in base rates (Hellman 2008). We therefore
can’t assume that fairness metrics which are ap-
propriate in one context will be appropriate in
another.
3.2. Luck and desert
A second major strand of debate in egalitarian
thinking considers the role of notions like choice
Huseby (2016) and desert Temkin (1986) in de-
termining which inequalities are acceptable? In
which circumstances, and to what extent, should
people be held responsible for the unequal status
they ﬁnd themselves in? So-called ‘luck egali-
tarians’ aim to answer this question by propos-
ing that the ideal solution should allow those in-
equalities resulting from people’s free choices and
informed risk-taking, but disregard those which
are the result of brute luck Arneson (1989). As
free-willed individuals, we are capable of mak-
ing choices and bearing their consequences, which
may sometimes make us better or worse oﬀ than
others. The choices we make may deserve cer-
tain rewards and punishments. However, where
inequalities are the result of circumstances out-
side an individual’s control (e.g. being born with
a debilitating health condition, or being born into
a culture in which one’s skin colour results in sys-
temically worse treatment), egalitarians argue for
their correction. However, deﬁning a principle
which can demarcate between those inequalities
which are and are not chosen or deserved is a
tricky prospect, one which has vexed egalitarians
for centuries.
The luck egalitarian aim of pursuing redistri-
bution only where inequalities are due to pure
luck, and leaving in place inequalities which are
the result of personal choices and informed gam-
bles, raises interesting questions for which vari-
ables should be included in fair ML models.
High-proﬁle controversies around the creation of
criminal recidivism risk scoring in the US, no-
tably the COMPAS system, have focused pri-
marily on the diﬀerential impacts on African
American and Caucasian subjects Angwin et al.
(2016). But one of the potentially objectionable
features of the COMPAS scoring system was not
the use of ‘race’ as a variable (which it did not),
but rather its use of variables which are not the
result of individuals’ choices, such as being part
of a family, social circle, or neighbourhood with
higher rates of crime. These may be objection-
able in part because they correlate with ‘race’ in
the U.S., but they are also objectionable more
generally to the extent that they are not the re-
sult of personal choices. As such, any inequalities
that arise from them should not, on the luck egal-
itarian view, be tolerated.
Furthermore, as critics of luck egalitarianism
have argued, sometimes even inequalities which
are the result of choice still ought to be compen-
sated. For instance, as Elizabeth Anderson has
argued, standard luck egalitarianism leads to the
vulnerability of dependent caretakers, because it
would not compensate those who are responsible
for choosing to care for dependents rather than
working a wage-earning job full time Anderson
(1999). This is what Thayson and Albertson call
a ‘costly rescue’ Thaysen and Albertsen (2017);
on their view, luck egalitarianism should only be
sensitive to responsibility for creating advantages
and disadvantages – not to responsibility for dis-
tributing them. Thus, individuals who voluntar-
ily place themselves in unequal positions might
sometimes deserve compensation if their choice
served some important social purpose. To re-
turn to the COMPAS case, even if certain vari-
ables like one’s social circle or neighbourhood
were the result of individual choice (which is per-
haps more likely to be the case for the economi-
cally advantaged), such choices may nevertheless
deserve protection from negative consequences.
This might apply in cases like those outlined by
Anderson, Thayson and Albertson above; for in-
stance, one might choose to remain a resident in
a high crime neighbourhood in order to make a
positive diﬀerence to the community.
7

Fairness in Machine Learning: Lessons from Political Philosophy
3.3. Deontic justice
In applying egalitarian political philosophy to
the analysis of particular instances of inequal-
ity, these abstract principles need to be supple-
mented with empirical claims about how and why
certain circumstances obtain. This reﬂects the
sense in which egalitarianism can be, in Derek
Parﬁt’s terms, deontic; that is, not concerned
with an unequal state of aﬀairs per se, but rather
with the way in which that state of aﬀairs was
produced Parﬁt (1997). Where analytic phi-
losophy ends, sociology, history, economics, and
other nascent disciplines are needed, to under-
stand the speciﬁc ways in which some groups
come to be unfairly disadvantaged Fang and
Moro (2010); Hooks (1992). Only then can we
meaningfully evaluate whether and to what ex-
tent a given disparity is unfair. But consider-
ation of historical and sociological contexts can
also inform philosophical accounts and raise new
questions. One example is in the attribution of
responsibility; who should be held responsible
for the initial creation of inequalities, and who
should be held responsible for correcting them?
Can historical injustices perpetrated by an insti-
tution in the past ground present-day claims for
redistribution? Is a particular instance of un-
equal treatment of a particular group worse if it
takes place in a wider context of inequality for
that group, compared to a general pattern of be-
nign or advantageous treatment?
Abstracting away from particular cases and
considering broader historical and social trends
may better enable us to account for what makes
certain forms of unequal treatment particularly
concerning. In discussing what makes racial pro-
ﬁling worse than other forms of proﬁling, even if
it is based on statistical facts, Kasper Lippert-
Rasmussen argues ( Lippert-Rasmussen (2014),
p. 300):
‘Statistical facts are often facts about
how we choose to act. Since we can
morally evaluate how we choose to act,
we cannot simply take statistical facts
for granted when justifying policies:
we need to ask the prior question of
whether it can be justiﬁed that we make
these statistical facts obtain’
On this view, the particular wrongness of racial
proﬁling can only be understood by appealing
to the social processes which cause the statisti-
cal regularities to obtain in the ﬁrst place. In
Lippert-Rasmussen’s example, the reason racial
proﬁling for crime in the U.S. ‘works’ (if it does
at all), may be due to things that the white ma-
jority do or fail to do which might reduce or elim-
inate the reliability of such statistical inferences.
Similarly, such ‘deontic’, historical and socio-
logical considerations can provide critical back-
ground information which is likely to be cru-
cially relevant in determinations of fairness in
particular algorithmic decision-making contexts.
Historical causes of inequalities and broader ex-
isting social structures cannot be ignored when
deploying models in such contexts. At a ba-
sic level, this means that feature selection–both
for protected characteristics and other variables–
should be informed by such information, but it
also might determine which disparities take pri-
ority in fairness analysis and mitigation if more
than one exists. More broadly, deontic consider-
ations may help situate and illuminate the moral
tensions that arise between diﬀerent and incom-
patible fairness metrics. Returning to the debate
about the COMPAS criminal recidivism scoring
system, where unequal base rates mean that ac-
curacy equity is mathematically impossible to
achieve alongside equalised false positive rates,
a deontic egalitarian perspective suggests focus-
ing attention on the historic reasons for such un-
equal base rates. While this may not in itself di-
rectly resolve the question of which fairness met-
ric ought to apply, it does suggest that part of
the answer should involve consideration of the
historic and contemporary factors responsible for
the broader social situation from which the in-
compatibility dilemma arises.
3.4. Distributive versus representative
harms
Finally, it is important to note that some aspects
of egalitarian fairness may not be distributive in
a direct way, in the sense that they concern the
distribution of beneﬁts and harms to speciﬁc peo-
ple from speciﬁc decisions. Rather, they may be
about the fair representation of diﬀerent iden-
tities, cultures, ethnicities, languages, or other
social categories. For instance, states with mul-
tiple oﬃcial languages may have a duty to ensure
equal representation of each language, a duty
8

Fairness in Machine Learning: Lessons from Political Philosophy
which need not derive from any speciﬁc claims
about the unequal beneﬁts and harms to indi-
vidual members of each linguistic group Taylor
(1994). Similar arguments might be made about
cultural representation in oﬃcial documents, or
even within the editorial policies of institutions
in receipt of public money. Even private institu-
tions might well voluntarily impose such duties
upon themselves. There is a debate about the
extent to which equal cultural recognition and
distributive egalitarianism are truly distinct no-
tions; some argue that ‘recognition and distribu-
tion are two irreducible elements of a satisfactory
theory of justice’, while others that ‘any dispute
regarding redistribution of wealth or resources is
reducible to a claim over the social valorisation
of speciﬁc group or individual traits’ Fraser and
Honneth (2003).
Such notions of representational fairness cap-
ture many of the most high-proﬁle controver-
sial examples of algorithmic bias. For instance,
much-reported work on gender and other biases
in the language corpora used to produce word
embeddings is an example of representational
fairness Bolukbasi et al. (2016); Caliskan-Islam
et al. (2016). In such cases, the problem is not
necessarily one of speciﬁc harms to speciﬁc mem-
bers of a social group, but rather one of the way
in which certain groups are represented in dig-
ital cultural artefacts, such as natural language
classiﬁers or search engine results. This may re-
quire diﬀerent ways of approaching fairness and
bias since the notions of diﬀerential group im-
pacts and treating like people alike do not apply;
instead, the goal might be to ensure equal rep-
resentation of groups in a ranking Zehlike et al.
(2017), or to give due weight to diﬀerent nor-
mative / ideological outlooks in a classiﬁer which
automates the enforcement of norms Binns et al.
(2017).
4. Conclusion
Current approaches to fair machine learning are
typically focused on interventions at the data
preparation, model-learning or post-processing
stages. This is understandable given the typi-
cal remit of data scientists who are intended to
carry out these processes. However, there is a
danger that this results in an approach which fo-
cuses on a narrow, static set of prescribed pro-
tected classes, derived from law and devoid of
context, without considering why those classes
are protected and how they relate to the partic-
ular justice aspects of the application in ques-
tion. Philosophical accounts of discrimination
and fairness prompt reﬂection on these more fun-
damental questions, and suggest avenues for fur-
ther consideration of what might be relevant and
why.
This raises a series of practical challenges
which may limit how eﬀective and systematic fair
ML approaches can be in practice. Attempting
to translate and elucidate the diﬀerences between
such egalitarian theories in the context of partic-
ular machine learning tasks will likely be tricky.
In simple cases, it may be that feature vectors
used to train models include personal charac-
teristics which can intuitively be classed as ei-
ther chosen or unchosen (and therefore legiti-
mate or illegitimate grounds for diﬀerential treat-
ment according to e.g. luck egalitarianism). But
more often, a contextually appropriate approach
to fairness which truly captures the essence of
the relevant philosophical points may hinge on
factors which are not typically present in the
data available in situ. Such missing data may
include the protected characteristics of aﬀected
individuals Veale and Binns (2017), but also in-
formation relevant to an assessment of an indi-
vidual’s responsibility, culpability or desert–such
as their socio-economic circumstances, life expe-
rience, personal development, and the relation-
ships between them. Attempts to draw such con-
clusions from training data and lists of legally
protected categories alone, are unlikely to do jus-
tice to the way that questions of justice arise in
idiosyncratic lives and diﬀering social contexts.
Acknowledgments
The author was supported by funding from the
UK Engineering and Physical Sciences Research
Council (EPSRC) under SOCIAM: The Theory
and Practice of Social Machines , grant number
EP/J017728/2, and PETRAS: Cyber Security
of the Internet of Things , under grant number
EP/N02334X/1.
9

Fairness in Machine Learning: Lessons from Political Philosophy
References
Elizabeth S Anderson. What is the point of
equality? Ethics, 109(2):287–337, 1999.
Julia Angwin, Jeﬀ Larson, Surya Mattu, and
Lauren Kirchner. Machine bias. Pro Publica,
2016.
Richard J Arneson. Equality and equal opportu-
nity for welfare. Philosophical studies , 56(1):
77–93, 1989.
Solon Barocas and Andrew D Selbst. Big data’s
disparate impact. Cal. L. Rev. , 104:671, 2016.
Reuben Binns, Michael Veale, Max Van Kleek,
and Nigel Shadbolt. Like trainer, like bot? in-
heritance of bias in algorithmic content mod-
eration. In International Conference on Social
Informatics, pages 405–415. Springer, 2017.
Tolga Bolukbasi, Kai-Wei Chang, James Y Zou,
Venkatesh Saligrama, and Adam T Kalai. Man
is to computer programmer as woman is to
homemaker? debiasing word embeddings. In
Advances in Neural Information Processing
Systems, pages 4349–4357, 2016.
Aylin Caliskan-Islam, Joanna J Bryson, and
Arvind Narayanan. Semantics derived au-
tomatically from language corpora necessar-
ily contain human biases. arXiv preprint
arXiv:1608.07187, 2016.
Gerald A Cohen. On the currency of egalitarian
justice. Ethics, 99(4):906–944, 1989.
William Dieterich, Christina Mendoza, and Tim
Brennan. Compas risk scales: Demonstrating
accuracy equity and predictive parity. North-
point Inc, 2016.
Cynthia Dwork, Moritz Hardt, Toniann Pitassi,
Omer Reingold, and Richard Zemel. Fairness
through awareness. In Proceedings of the 3rd
Innovations in Theoretical Computer Science
Conference, pages 214–226. ACM, 2012.
Ronald Dworkin. What is equality? part 1:
Equality of welfare. Philosophy & public af-
fairs, pages 185–246, 1981.
Benjamin Eidelson. Discrimination and Disre-
spect. Oxford University Press, 2015.
Hanming Fang and Andrea Moro. Theories of
statistical discrimination and aﬃrmative ac-
tion: A survey. Technical report, National Bu-
reau of Economic Research, 2010.
Nancy Fraser and Axel Honneth. Redistribu-
tion or recognition?: a political-philosophical
exchange. Verso, 2003.
Margaret Gilbert. Collective epistemology. Epis-
teme, 1(2):95–107, 2004.
Sara Hajian and Josep Domingo-Ferrer. A
methodology for direct and indirect discrimi-
nation prevention in data mining. IEEE trans-
actions on knowledge and data engineering , 25
(7):1445–1459, 2013.
Moritz Hardt, Eric Price, Nati Srebro, et al.
Equality of opportunity in supervised learning.
In Advances in Neural Information Processing
Systems, pages 3315–3323, 2016.
Elisa Holmes. Anti-discrimination rights without
equality. The Modern Law Review , 68(2):175–
194, 2005.
Bell Hooks. Yearning: Race, gender, and cultural
politics. 1992.
Robert Huseby. Can luck egalitarianism justify
the fact that some are worse oﬀ than others?
Journal of Applied Philosophy , 33(3):259–269,
2016.
Matthew Joseph, Michael Kearns, Jamie Mor-
genstern, Seth Neel, and Aaron Roth. Rawl-
sian fairness for machine learning. arXiv
preprint arXiv:1610.09559, 2016.
Faisal Kamiran, Toon Calders, and Mykola Pech-
enizkiy. Techniques for discrimination-free pre-
dictive models. In Discrimination and Pri-
vacy in the Information Society , pages 223–
239. Springer, 2013.
Jon Kleinberg, Sendhil Mullainathan, and Man-
ish Raghavan. Inherent trade-oﬀs in the fair
determination of risk scores. arXiv preprint
arXiv:1609.05807, 2016.
Matt J Kusner, Joshua R Loftus, Chris Russell,
and Ricardo Silva. Counterfactual fairness.
arXiv preprint arXiv:1703.06856 , 2017.
10

Fairness in Machine Learning: Lessons from Political Philosophy
Annabelle Lever. Racial proﬁling and the polit-
ical philosophy of race. The Oxford Handbook
of Philosophy and Race , page 425, 2016.
Kasper Lippert-Rasmussen. Born free and
equal?: a philosophical inquiry into the nature
of discrimination . Oxford University Press,
2014.
Derek Parﬁt. Equality and priority. Ratio, 10(3):
202–221, 1997.
Philip Pettit. Responsibility incorporated.
Ethics, 117(2):171–201, 2007.
Edmund S Phelps. The statistical theory of
racism and sexism. The american economic
review, 62(4):659–661, 1972.
John Rawls. A theory of justice. Harvard univer-
sity press, 2009.
Thomas M Scanlon. Moral dimensions. Harvard
University Press, 2009.
Frederick F Schauer. Proﬁles, probabilities, and
stereotypes. Harvard University Press, 2009.
Shlomi Segall. What’s so bad about discrimina-
tion? Utilitas, 24(1):82–100, 2012.
Amartya Sen. Inequality reexamined. Clarendon
Press, 1992.
Charles Taylor. Multiculturalism. Princeton Uni-
versity Press, 1994.
Larry S Temkin. Inequality. Philosophy & Public
Aﬀairs, pages 99–121, 1986.
Jens Damgaard Thaysen and Andreas Albert-
sen. When bad things happen to good people:
luck egalitarianism and costly rescues.Politics,
Philosophy & Economics , 16(1):93–112, 2017.
Michael Veale and Reuben Binns. Fairer machine
learning in the real world: Mitigating discrim-
ination without collecting sensitive data. Big
Data & Society , 4(2):2053951717743530, 2017.
Michael Walzer. Spheres of justice: A defense of
pluralism and equality. Basic books, 2008.
Muhammad Bilal Zafar, Isabel Valera, Manuel
Gomez Rodriguez, and Krishna P Gummadi.
Fairness beyond disparate treatment & dis-
parate impact: Learning classiﬁcation without
disparate mistreatment. In Proceedings of the
26th International Conference on World Wide
Web, pages 1171–1180. International World
Wide Web Conferences Steering Committee,
2017.
Meike Zehlike, Francesco Bonchi, Carlos Castillo,
Sara Hajian, Mohamed Megahed, and Ricardo
Baeza-Yates. Fa* ir: A fair top-k ranking algo-
rithm. arXiv preprint arXiv:1706.06368, 2017.
11
```

## Merged notes from duplicate

_Source file:_ `Fairness in Machine Learning_ Lessons from Political Philosophy.md`

[[Fairness in Machine Learning- Lessons from Political Philosophy.pdf]]

Reuben Binns

*Proceedings of the 1st Conference on Fairness, Accountability and Transparency*, PMLR 81:149-159, 2018.

#### Abstract

What does it mean for a machine learning model to be ‘fair’, in terms which can be operationalised? Should fairness consist of ensuring everyone has an equal probability of obtaining some benefit, or should we aim instead to minimise the harms to the least advantaged? Can the relevant ideal be determined by reference to some alternative state of affairs in which a particular social pattern of discrimination does not exist? Various definitions proposed in recent literature make different assumptions about what terms like discrimination and fairness mean and how they can be defined in mathematical terms. Questions of discrimination, egalitarianism and justice are of significant interest to moral and political philosophers, who have expended significant efforts in formalising and defending these central concepts. It is therefore unsurprising that attempts to formalise ‘fairness’ in machine learning contain echoes of these old philosophical debates. This paper draws on existing work in moral and political philosophy in order to elucidate emerging debates about fair machine learning.

#### Cite this Paper

---

BibTeX

`  @InProceedings{pmlr-v81-binns18a,   title = 	 {Fairness in Machine Learning: Lessons from Political Philosophy},   author = 	 {Binns, Reuben},   booktitle = 	 {Proceedings of the 1st Conference on Fairness, Accountability and Transparency},   pages = 	 {149--159},   year = 	 {2018},   editor = 	 {Friedler, Sorelle A. and Wilson, Christo},   volume = 	 {81},   series = 	 {Proceedings of Machine Learning Research},   month = 	 {23--24 Feb},   publisher =    {PMLR},   pdf = 	 {http://proceedings.mlr.press/v81/binns18a/binns18a.pdf},   url = 	 {https://proceedings.mlr.press/v81/binns18a.html},   abstract = 	 {What does it mean for a machine learning model to be ‘fair’, in terms which can be operationalised? Should fairness consist of ensuring everyone has an equal probability of obtaining some benefit, or should we aim instead to minimise the harms to the least advantaged? Can the relevant ideal be determined by reference to some alternative state of affairs in which a particular social pattern of discrimination does not exist? Various definitions proposed in recent literature make different assumptions about what terms like discrimination and fairness mean and how they can be defined in mathematical terms. Questions of discrimination, egalitarianism and justice are of significant interest to moral and political philosophers, who have expended significant efforts in formalising and defending these central concepts. It is therefore unsurprising that attempts to formalise ‘fairness’ in machine learning contain echoes of these old philosophical debates. This paper draws on existing work in moral and political philosophy in order to elucidate emerging debates about fair machine learning.} }  `

Endnote

`%0 Conference Paper %T Fairness in Machine Learning: Lessons from Political Philosophy %A Reuben Binns %B Proceedings of the 1st Conference on Fairness, Accountability and Transparency %C Proceedings of Machine Learning Research %D 2018 %E Sorelle A. Friedler %E Christo Wilson	 %F pmlr-v81-binns18a %I PMLR %P 149--159 %U https://proceedings.mlr.press/v81/binns18a.html %V 81 %X What does it mean for a machine learning model to be ‘fair’, in terms which can be operationalised? Should fairness consist of ensuring everyone has an equal probability of obtaining some benefit, or should we aim instead to minimise the harms to the least advantaged? Can the relevant ideal be determined by reference to some alternative state of affairs in which a particular social pattern of discrimination does not exist? Various definitions proposed in recent literature make different assumptions about what terms like discrimination and fairness mean and how they can be defined in mathematical terms. Questions of discrimination, egalitarianism and justice are of significant interest to moral and political philosophers, who have expended significant efforts in formalising and defending these central concepts. It is therefore unsurprising that attempts to formalise ‘fairness’ in machine learning contain echoes of these old philosophical debates. This paper draws on existing work in moral and political philosophy in order to elucidate emerging debates about fair machine learning. `

APA

`  Binns, R.. (2018). Fairness in Machine Learning: Lessons from Political Philosophy. *Proceedings of the 1st Conference on Fairness, Accountability and Transparency*, in *Proceedings of Machine Learning Research* 81:149-159 Available from https://proceedings.mlr.press/v81/binns18a.html.   `

---

#### Related Material

- [Download PDF](http://proceedings.mlr.press/v81/binns18a/binns18a.pdf)