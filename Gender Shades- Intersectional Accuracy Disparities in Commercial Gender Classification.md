---
title: Gender Shades- Intersectional Accuracy Disparities in Commercial Gender Classification
year: "2023"
Type: Article
DOI: ""
source: https://proceedings.mlr.press/v81/buolamwini18a.html?mod=article_inline&ref=akusion-ci-shi-dai-bizinesumedeia
created: 2026-04-24
description: "Gender Shades: Intersectional Accuracy Disparities in Commercial Gender ClassificationJoy Buolamwini, Timnit GebruRecent studies demonstrate that machin..."
tags:
  - op/acc/pending-review
  - themes/gender
  - themes/bias/algorithmic
  - Tech/AI
  - themes/intersectionality
pdfORepub: "[[Gender Shades- Intersectional Accuracy Disparities in Commercial Gender Classification.pdf]]"
author:
  - Joy Buolamwini
  - Timnit Gebru
published: 2018-01-21
---

![[Gender Shades- Intersectional Accuracy Disparities in Commercial Gender Classification.pdf]]
## Full text (extracted from `Gender Shades- Intersectional Accuracy Disparities in Commercial Gender Classification.pdf`)

*Source:* `2PDF/Gender Shades- Intersectional Accuracy Disparities in Commercial Gender Classification.pdf`  
*Extracted:* 2026-04-24

```text
Proceedings of Machine Learning Research 81:1–15, 2018 Conference on Fairness, Accountability, and Transparency
Gender Shades: Intersectional Accuracy Disparities in
Commercial Gender Classiﬁcation∗
Joy Buolamwini joyab@mit.edu
MIT Media Lab 75 Amherst St. Cambridge, MA 02139
Timnit Gebru timnit.gebru@microsoft.com
Microsoft Research 641 Avenue of the Americas, New York, NY 10011
Editors: Sorelle A. Friedler and Christo Wilson
Abstract
Recent studies demonstrate that machine
learning algorithms can discriminate based
on classes like race and gender. In this
work, we present an approach to evaluate
bias present in automated facial analysis al-
gorithms and datasets with respect to phe-
notypic subgroups. Using the dermatolo-
gist approved Fitzpatrick Skin Type clas-
siﬁcation system, we characterize the gen-
der and skin type distribution of two facial
analysis benchmarks, IJB-A and Adience.
We ﬁnd that these datasets are overwhelm-
ingly composed of lighter-skinned subjects
(79.6% for IJB-A and 86 .2% for Adience)
and introduce a new facial analysis dataset
which is balanced by gender and skin type.
We evaluate 3 commercial gender clas-
siﬁcation systems using our dataset and
show that darker-skinned females are the
most misclassiﬁed group (with error rates
of up to 34 .7%). The maximum error rate
for lighter-skinned males is 0 .8%. The
substantial disparities in the accuracy of
classifying darker females, lighter females,
darker males, and lighter males in gender
classiﬁcation systems require urgent atten-
tion if commercial companies are to build
genuinely fair, transparent and accountable
facial analysis algorithms.
Keywords: Computer Vision, Algorith-
mic Audit, Gender Classiﬁcation
1. Introduction
Artiﬁcial Intelligence (AI) is rapidly inﬁltrating
every aspect of society. From helping determine
∗ Download our gender and skin type balanced PPB
dataset atgendershades.org
who is hired, ﬁred, granted a loan, or how long
an individual spends in prison, decisions that
have traditionally been performed by humans are
rapidly made by algorithms (O’Neil, 2017; Citron
and Pasquale, 2014). Even AI-based technologies
that are not speciﬁcally trained to perform high-
stakes tasks (such as determining how long some-
one spends in prison) can be used in a pipeline
that performs such tasks. For example, while
face recognition software by itself should not be
trained to determine the fate of an individual in
the criminal justice system, it is very likely that
such software is used to identify suspects. Thus,
an error in the output of a face recognition algo-
rithm used as input for other tasks can have se-
rious consequences. For example, someone could
be wrongfully accused of a crime based on erro-
neous but conﬁdent misidentiﬁcation of the per-
petrator from security video footage analysis.
Many AI systems, e.g. face recognition tools,
rely on machine learning algorithms that are
trained with labeled data. It has recently
been shown that algorithms trained with biased
data have resulted in algorithmic discrimination
(Bolukbasi et al., 2016; Caliskan et al., 2017).
Bolukbasi et al. even showed that the popular
word embedding space, Word2Vec, encodes soci-
etal gender biases. The authors used Word2Vec
to train an analogy generator that ﬁlls in miss-
ing words in analogies. The analogy man is to
computer programmer as woman is to “X” was
completed with “homemaker”, conforming to the
stereotype that programming is associated with
men and homemaking with women. The biases
in Word2Vec are thus likely to be propagated
throughout any system that uses this embedding.
c⃝ 2018 J. Buolamwini & T. Gebru.

Gender Shades
Although many works have studied how to
create fairer algorithms, and benchmarked dis-
crimination in various contexts (Kilbertus et al.,
2017; Hardt et al., 2016b,a), only a handful of
works have done this analysis for computer vi-
sion. However, computer vision systems with
inferior performance across demographics can
have serious implications. Esteva et al. showed
that simple convolutional neural networks can be
trained to detect melanoma from images, with ac-
curacies as high as experts (Esteva et al., 2017).
However, without a dataset that has labels for
various skin characteristics such as color, thick-
ness, and the amount of hair, one cannot measure
the accuracy of such automated skin cancer de-
tection systems for individuals with diﬀerent skin
types. Similar to the well documented detrimen-
tal eﬀects of biased clinical trials (Popejoy and
Fullerton, 2016; Melloni et al., 2010), biased sam-
ples in AI for health care can result in treatments
that do not work well for many segments of the
population.
In other contexts, a demographic group that
is underrepresented in benchmark datasets can
nonetheless be subjected to frequent targeting.
The use of automated face recognition by law
enforcement provides such an example. At least
117 million Americans are included in law en-
forcement face recognition networks. A year-
long research investigation across 100 police de-
partments revealed that African-American indi-
viduals are more likely to be stopped by law
enforcement and be subjected to face recogni-
tion searches than individuals of other ethnici-
ties (Garvie et al., 2016). False positives and un-
warranted searches pose a threat to civil liberties.
Some face recognition systems have been shown
to misidentify people of color, women, and young
people at high rates (Klare et al., 2012). Moni-
toring phenotypic and demographic accuracy of
these systems as well as their use is necessary to
protect citizens’ rights and keep vendors and law
enforcement accountable to the public.
We take a step in this direction by making two
contributions. First, our work advances gender
classiﬁcation benchmarking by introducing a new
face dataset composed of 1270 unique individu-
als that is more phenotypically balanced on the
basis of skin type than existing benchmarks. To
our knowledge this is the ﬁrst gender classiﬁca-
tion benchmark labeled by the Fitzpatrick (TB,
1988) six-point skin type scale, allowing us to
benchmark the performance of gender classiﬁca-
tion algorithms by skin type. Second, this work
introduces the ﬁrst intersectional demographic
and phenotypic evaluation of face-based gender
classiﬁcation accuracy. Instead of evaluating ac-
curacy by gender or skin type alone, accuracy
is also examined on 4 intersectional subgroups:
darker females, darker males, lighter females, and
lighter males. The 3 evaluated commercial gen-
der classiﬁers have the lowest accuracy on darker
females. Since computer vision technology is be-
ing utilized in high-stakes sectors such as health-
care and law enforcement, more work needs to
be done in benchmarking vision algorithms for
various demographic and phenotypic groups.
2. Related Work
Automated Facial Analysis. Automated fa-
cial image analysis describes a range of face per-
ception tasks including, but not limited to, face
detection (Zafeiriou et al., 2015; Mathias et al.,
2014; Bai and Ghanem, 2017), face classiﬁca-
tion (Reid et al., 2013; Levi and Hassner, 2015a;
Rothe et al., 2016) and face recognition (Parkhi
et al., 2015; Wen et al., 2016; Ranjan et al., 2017).
Face recognition software is now built into most
smart phones and companies such as Google,
IBM, Microsoft and Face++ have released com-
mercial software that perform automated facial
analysis (IBM; Microsoft; Face++; Google).
A number of works have gone further than
solely performing tasks like face detection, recog-
nition and classiﬁcation that are easy for humans
to perform. For example, companies such as Af-
fectiva (Aﬀectiva) and researchers in academia
attempt to identify emotions from images of peo-
ple’s faces (Dehghan et al., 2017; Srinivasan et al.,
2016; Fabian Benitez-Quiroz et al., 2016). Some
works have also used automated facial analysis
to understand and help those with autism (Leo
et al., 2015; Palestra et al., 2016). Controversial
papers such as (Kosinski and Wang, 2017) claim
to determine the sexuality of Caucasian males
whose proﬁle pictures are on Facebook or dating
sites. And others such as (Wu and Zhang, 2016)
and Israeli based company Faception (Faception)
have developed software that purports to deter-
mine an individual’s characteristics (e.g. propen-
sity towards crime, IQ, terrorism) solely from
2

Gender Shades
their faces. The clients of such software include
governments. An article by (Aguera Y Arcas et
al., 2017) details the dangers and errors propa-
gated by some of these aforementioned works.
Face detection and classiﬁcation algorithms
are also used by US-based law enforcement for
surveillance and crime prevention purposes. In
“The Perpetual Lineup”, Garvie and colleagues
provide an in-depth analysis of the unregulated
police use of face recognition and call for rigorous
standards of automated facial analysis, racial ac-
curacy testing, and regularly informing the pub-
lic about the use of such technology (Garvie
et al., 2016). Past research has also shown that
the accuracies of face recognition systems used
by US-based law enforcement are systematically
lower for people labeled female, Black, or be-
tween the ages of 18—30 than for other demo-
graphic cohorts (Klare et al., 2012). The latest
gender classiﬁcation report from the National In-
stitute for Standards and Technology (NIST) also
shows that algorithms NIST evaluated performed
worse for female-labeled faces than male-labeled
faces (Ngan et al., 2015).
The lack of datasets that are labeled by eth-
nicity limits the generalizability of research ex-
ploring the impact of ethnicity on gender classi-
ﬁcation accuracy. While the NIST gender report
explored the impact of ethnicity on gender classi-
ﬁcation through the use of an ethnic proxy (coun-
try of origin), none of the 10 locations used in
the study were in Africa or the Caribbean where
there are signiﬁcant Black populations. On the
other hand, Farinella and Dugelay claimed that
ethnicity has no eﬀect on gender classiﬁcation,
but they used a binary ethnic categorization
scheme: Caucasian and non-Caucasian (Farinella
and Dugelay, 2012). To address the underrepre-
sentation of people of African-descent in previ-
ous studies, our work explores gender classiﬁca-
tion on African faces to further scholarship on
the impact of phenotype on gender classiﬁcation.
Benchmarks. Most large-scale attempts to
collect visual face datasets rely on face de-
tection algorithms to ﬁrst detect faces (Huang
et al., 2007; Kemelmacher-Shlizerman et al.,
2016). Megaface, which to date is the largest
publicly available set of facial images, was com-
posed utilizing Head Hunter (Mathias et al.,
2014) to select one million images from the Yahoo
Flicker 100M image dataset (Thomee et al., 2015;
Kemelmacher-Shlizerman et al., 2016). Any sys-
tematic error found in face detectors will in-
evitably aﬀect the composition of the bench-
mark. Some datasets collected in this manner
have already been documented to contain signif-
icant demographic bias. For example, LFW, a
dataset composed of celebrity faces which has
served as a gold standard benchmark for face
recognition, was estimated to be 77.5% male and
83.5% White (Han and Jain, 2014). Although
(Taigman et al., 2014)’s face recognition system
recently reported 97 .35% accuracy on the LFW
dataset, its performance is not broken down by
race or gender. Given these skews in the LFW
dataset, it is not clear that the high reported ac-
curacy is applicable to people who are not well
represented in the LFW benchmark. In response
to these limitations, Intelligence Advanced Re-
search Projects Activity (IARPA) released the
IJB-A dataset as the most geographically diverse
set of collected faces (Klare et al., 2015). In
order to limit bias, no face detector was used
to select images containing faces. In compari-
son to face recognition, less work has been done
to benchmark performance on gender classiﬁca-
tion. In 2015, the Adience gender and age classi-
ﬁcation benchmark was released (Levi and Has-
sner, 2015b). As of 2017, The National Insti-
tute of Standards and Technology is starting an-
other challenge to spur improvement in face gen-
der classiﬁcation by expanding on the 2014-15
study.
3. Intersectional Benchmark
An evaluation of gender classiﬁcation perfor-
mance currently requires reducing the construct
of gender into deﬁned classes. In this work we use
the sex labels of “male” and “female” to deﬁne
gender classes since the evaluated benchmarks
and classiﬁcation systems use these binary labels.
An intersectional evaluation further requires a
dataset representing the deﬁned genders with a
range of phenotypes that enable subgroup accu-
racy analysis. To assess the suitability of exist-
ing datasets for intersectional benchmarking, we
provided skin type annotations for unique sub-
jects within two selected datasets, and compared
the distribution of darker females, darker males,
lighter females, and lighter males. Due to phe-
notypic imbalances in existing benchmarks, we
3

Gender Shades
Figure 1: Example images and average faces from the new Pilot Parliaments Benchmark (PPB). As
the examples show, the images are constrained with relatively little variation in pose. The
subjects are composed of male and female parliamentarians from 6 countries. On average,
Senegalese subjects are the darkest skinned while those from Finland and Iceland are the
lightest skinned.
created a new dataset with more balanced skin
type and gender representations.
3.1. Rationale for Phenotypic Labeling
Though demographic labels for protected classes
like race and ethnicity have been used for per-
forming algorithmic audits (Friedler et al., 2016;
Angwin et al., 2016) and assessing dataset diver-
sity (Han and Jain, 2014), phenotypic labels are
seldom used for these purposes. While race la-
bels are suitable for assessing potential algorith-
mic discrimination in some forms of data (e.g.
those used to predict criminal recidivism rates),
they face two key limitations when used on visual
images. First, subjects’ phenotypic features can
vary widely within a racial or ethnic category.
For example, the skin types of individuals iden-
tifying as Black in the US can represent many
hues. Thus, facial analysis benchmarks consist-
ing of lighter-skinned Black individuals would not
adequately represent darker-skinned ones. Sec-
ond, racial and ethnic categories are not consis-
tent across geographies: even within countries
these categories change over time.
Since race and ethnic labels are unstable, we
decided to use skin type as a more visually pre-
cise label to measure dataset diversity. Skin type
is one phenotypic attribute that can be used to
more objectively characterize datasets along with
eye and nose shapes. Furthermore, skin type was
chosen as a phenotypic factor of interest because
default camera settings are calibrated to expose
lighter-skinned individuals (Roth, 2009). Poorly
exposed images that result from sensor optimiza-
tions for lighter-skinned subjects or poor illumi-
nation can prove challenging for automated facial
analysis. By labeling faces with skin type, we
can increase our understanding of performance
on this important phenotypic attribute.
3.2. Existing Benchmark Selection
Rationale
IJB-A is a US government benchmark released
by the National Institute of Standards and Tech-
4

Gender Shades
LightestDarkest
180o 120o 60o 0o 60o 120o 180o
60o
0o
30o
60o
30o
Figure 2: The global distribution of skin color. Most Africans have darker skin while those from
Nordic countries are lighter-skinned. Image from (Encyclopedia Britannica) c⃝Copyright
2012 Encyclopedia Britannica.
nology (NIST) in 2015. We chose to evaluate this
dataset given the government’s involvement and
the explicit development of the benchmark to be
geographically diverse (as mentioned in Sec. 2).
At the time of assessment in April and May of
2017, the dataset consisted of 500 unique sub-
jects who are public ﬁgures. One image of each
unique subject was manually labeled with one of
six Fitzpatrick skin types (TB, 1988).
Adience is a gender classiﬁcation benchmark
released in 2014 and was selected due to its re-
cency and unconstrained nature. The Adience
benchmark contains 2, 284 unique individual sub-
jects. 2 , 194 of those subjects had reference im-
ages that were discernible enough to be labeled
by skin type and gender. Like the IJB-A dataset,
only one image of each subject was labeled for
skin type.
3.3. Creation of Pilot Parliaments
Benchmark
Preliminary analysis of the IJB-A and Adi-
ence benchmarks revealed overrepresentation of
lighter males, underrepresentation of darker fe-
males, and underrepresentation of darker indi-
viduals in general. We developed the Pilot Par-
liaments Benchmark (PPB) to achieve better in-
tersectional representation on the basis of gender
and skin type. PPB consists of 1270 individuals
from three African countries (Rwanda, Senegal,
South Africa) and three European countries (Ice-
land, Finland, Sweden) selected for gender parity
in the national parliaments.
Property PPB IJB-A Adience
Release Year 2017 2015 2014
#Subjects 1270 500 2284
Avg. IPD 63 pixels - -
BBox Size 141 (avg) ≥36 -
IM Width 160-590 - 816
IM Height 213-886 - 816
Table 1: Various image characteristics of the Pi-
lot Parliaments Benchmark compared
with prior datasets. #Subjects denotes
the number of unique subjects, the aver-
age bounding box size is given in pixels,
and IM stands for image.
Figure 1 shows example images from PPB as
well as average faces of males and females in
each country represented in the datasets. We
decided to use images of parliamentarians since
they are public ﬁgures with known identities and
photos available under non-restrictive licenses
posted on government websites. To add skin
5

Gender Shades
type diversity to the dataset, we chose parlia-
mentarians from African and European coun-
tries. Fig. 2 shows an approximated distribu-
tion of average skin types around the world. As
seen in the map, African countries typically have
darker-skinned individuals whereas Nordic coun-
tries tend to have lighter-skinned citizens. Col-
onization and migration patterns nonetheless in-
ﬂuence the phenotypic distribution of skin type
and not all Africans are darker-skinned. Simi-
larly, not all citizens of Nordic countries can be
classiﬁed as lighter-skinned.
The speciﬁc African and European countries
were selected based on their ranking for gen-
der parity as assessed by the Inter Parliamen-
tary Union (Inter Parliamentary Union Rank-
ing). Of all the countries in the world, Rwanda
has the highest proportion of women in parlia-
ment. Nordic countries were also well represented
in the top 10 nations. Given the gender parity
and prevalence of lighter skin in the region, Ice-
land, Finland, and Sweden were chosen. To bal-
ance for darker skin, the next two highest-ranking
African nations, Senegal and South Africa, were
also added.
Table 1 compares image characteristics of PPB
with IJB-A and Adience. PPB is highly con-
strained since it is composed of oﬃcial proﬁle
photos of parliamentarians. These proﬁle photos
are taken under conditions with cooperative sub-
jects where pose is relatively ﬁxed, illumination is
constant, and expressions are neutral or smiling.
Conversely, the images in the IJB-A and Adi-
ence benchmarks are unconstrained and subject
pose, illumination, and expression by construc-
tion have more variation.
3.4. Intersectional Labeling Methodology
Skin Type Labels. We chose the Fitzpatrick
six-point labeling system to determine skin type
labels given its scientiﬁc origins. Dermatologists
use this scale as the gold standard for skin classi-
ﬁcation and determining risk for skin cancer (TB,
1988).
The six-point Fitzpatrick classiﬁcation system
which labels skin as Type I to Type VI is skewed
towards lighter skin and has three categories that
can be applied to people perceived as White (Fig-
ure 2). Yet when it comes to fully representing
the sepia spectrum that characterizes the rest of
PPB
IJB-A
Adience
0% 25% 50% 75% 100%
30.323.325.021.3
4.4 16.0 20.2 59.4
7.46.4 44.6 41.6 %Darker Female
%Darker Male
%Lighter Female
%Ligher Male
Figure 3: The percentage of darker female,
lighter female, darker male, and lighter
male subjects in PPB, IJB-A and Adi-
ence. Only 4.4% of subjects in Adience
are darker-skinned and female in com-
parison to 21.3% in PPB.
the world, the categorizations are fairly coarse.
Nonetheless, the scale provides a scientiﬁcally
based starting point for auditing algorithms and
datasets by skin type.
Gender Labels. All evaluated companies
provided a “gender classiﬁcation” feature that
uses the binary sex labels of female and male.
This reductionist view of gender does not ade-
quately capture the complexities of gender or ad-
dress transgender identities. The companies pro-
vide no documentation to clarify if their gender
classiﬁcation systems which provide sex labels are
classifying gender identity or biological sex. To
label the PPB data, we use female and male la-
bels to indicate subjects perceived as women or
men respectively.
Labeling Process. For existing benchmarks,
one author labeled each image with one of six
Fitzpatrick skin types and provided gender an-
notations for the IJB-A dataset. The Adience
benchmark was already annotated for gender.
These preliminary skin type annotations on ex-
isting datasets were used to determine if a new
benchmark was needed.
More annotation resources were used to label
PPB. For the new parliamentarian benchmark,
3 annotators including the authors provided gen-
der and Fitzpatrick labels. A board-certiﬁed sur-
gical dermatologist provided the deﬁnitive labels
for the Fitzpatrick skin type. Gender labels were
determined based on the name of the parliamen-
tarian, gendered title, preﬁxes such as Mr or Ms,
and the appearance of the photo.
6

Gender Shades
Set n F M Darker Lighter DF DM LF LM
All Subjects 1270 44.6% 55.4% 46.4% 53.6% 21.3% 25.0% 23.3% 30.3%
Africa 661 43.9% 56.1% 86.2% 13.8% 39.8% 46.4% 4.1% 9.7%
South Africa 437 41.4% 58.6% 79.2% 20.8% 35.2% 43.9% 6.2% 14.6%
Senegal 149 43.0% 57.0% 100.0% 0.0% 43.0% 57.0% 0.0% 0.0%
Rwanda 75 60.0% 40.0% 100.0% 0.0% 60.0% 40.0% 0.0% 0.0%
Europe 609 45.5% 54.5% 3.1% 96.9% 1.3% 1.8% 44.2% 52.7%
Sweden 349 46.7% 53.3% 4.9% 95.1% 2.0% 2.9% 44.7% 50.4%
Finland 197 42.6% 57.4% 1.0% 99.0% 0.5% 0.5% 42.1% 56.9%
Iceland 63 47.6% 52.4% 0.0% 100.0% 0.0% 0.0% 47.6% 52.4%
Table 2: Pilot Parliaments Benchmark decomposition by the total number of female subjects de-
noted as F, total number of male subjects (M), total number of darker and lighter subjects,
as well as female darker/lighter (DF/LF) and male darker/lighter subjects (DM/LM). The
group compositions are shown for all unique subjects, Africa, Europe and the countries in
our dataset located in each of these continents.
Dataset Lighter (I,II,III) Darker (IV, V, VI) Total
PPB 53.6% 681 46.4% 589 1270
IJB-A 79.6% 398 20.4% 102 500
Adience 86.2% 1892 13.8% 302 2194
Table 3: The distributions of lighter and darker-skinned subjects (according to the Fitzpatrick clas-
siﬁcation system) in PPB, IJB-A, and Adience datasets. Adience has the most skewed
distribution with 86.2% of the subjects consisting of lighter-skinned individuals whereas
PPB is more evenly distributed between lighter (53.6%) and darker (46.4%) subjects.
3.5. Fitzpatrick Skin Type Comparison
For the purposes of our analysis, lighter subjects
will refer to faces with a Fitzpatrick skin type
of I,II, or III. Darker subjects will refer to faces
labeled with a Fitzpatrick skin type of IV,V, or
VI. We intentionally choose countries with ma-
jority populations at opposite ends of the skin
type scale to make the lighter/darker dichotomy
more distinct. The skin types are aggregated to
account for potential oﬀ-by-one errors since the
skin type is estimated using images instead of em-
ploying a standard spectrophotometer and Fitz-
patrick questionnaire.
Table 2 presents the gender, skin type, and in-
tersectional gender by skin type composition of
PPB. And Figure 3 compares the percentage of
images from darker female, darker male, lighter
female and lighter male subjects from Adience,
IJB-A, and PBB. PPB provides the most bal-
anced representation of all four groups whereas
IJB-A has the least balanced distribution.
Darker females are the least represented in
IJB-A (4.4%) and darker males are the least rep-
resented in Adience (6.4%). Lighter males are the
most represented unique subjects in all datasets.
IJB-A is composed of 59.4% unique lighter males
whereas this percentage is reduced to 41 .6% in
Adience and 30 .3% in PPB. As seen in Table 3,
Adience has the most skewed distribution by skin
type.
While all the datasets have more lighter-
skinned unique individuals, PPB is around half
light at 53.6% whereas the proportion of lighter-
skinned unique subjects in IJB-A and Adience
7

Gender Shades
is 79.6% and 86 .2% respectively. PPB provides
substantially more darker-skinned unique sub-
jects than IJB-A and Adience. Even though Adi-
ence has 2194 labeled unique subjects, which is
nearly twice that of the 1270 subjects in PPB,
it has 302 darker subjects, nearly half the 589
darker subjects in PPB. Overall, PPB has a more
balanced representation of lighter and darker
subjects as compared to the IJB-A and Adience
datasets.
4. Commercial Gender
Classiﬁcation Audit
We evaluated 3 commercial gender classiﬁers.
Overall, male subjects were more accurately clas-
siﬁed than female subjects replicating previous
ﬁndings (Ngan et al., 2015), and lighter subjects
were more accurately classiﬁed than darker in-
dividuals. An intersectional breakdown reveals
that all classiﬁers performed worst on darker fe-
male subjects.
4.1. Key Findings on Evaluated
Classiﬁers
• All classiﬁers perform better on male faces
than female faces (8 .1% − 20.6% diﬀerence
in error rate)
• All classiﬁers perform better on lighter faces
than darker faces (11 .8% − 19.2% diﬀerence
in error rate)
• All classiﬁers perform worst on darker female
faces (20.8% − 34.7% error rate)
• Microsoft and IBM classiﬁers perform best
on lighter male faces (error rates of 0.0% and
0.3% respectively)
• Face++ classiﬁers perform best on darker
male faces (0.7% error rate)
• The maximum diﬀerence in error rate be-
tween the best and worst classiﬁed groups is
34.4%
4.2. Commercial Gender Classiﬁer
Selection: Microsoft, IBM, Face++
We focus on gender classiﬁers sold in API bun-
dles made available by Microsoft, IBM, and
Face++ (Microsoft; IBM; Face++). Microsoft’s
Cognitive Services Face API and IBM’s Wat-
son Visual Recognition API were chosen since
both companies have made large investments in
artiﬁcial intelligence, capture signiﬁcant market
shares in the machine learning services domain,
and provide public demonstrations of their fa-
cial analysis technology. At the time of evalua-
tion, Google did not provide a publicly available
gender classiﬁer. Previous studies have shown
that face recognition systems developed in West-
ern nations and those developed in Asian nations
tend to perform better on their respective popu-
lations (Phillips et al., 2011). Face++, a com-
puter vision company headquartered in China
with facial analysis technology previously inte-
grated with some Lenovo computers, was thus
chosen to see if this observation holds for gender
classiﬁcation. Like Microsoft and IBM, Face++
also provided a publicly available demonstration
of their gender classiﬁcation capabilities at the
time of evaluation(April and May 2017).
All of the companies oﬀered gender classiﬁca-
tion as a component of a set of proprietary facial
analysis API services (Microsoft; IBM; Face++).
The description of classiﬁcation methodology
lacked detail and there was no mention of what
training data was used. At the time of evaluation,
Microsoft’s Face Detect service was described as
using advanced statistical algorithms that “may
not always be 100% precise” (Microsoft API Ref-
erence). IBM Watson Visual Recognition and
Face++ services were said to use deep learning-
based algorithms (IBM API Reference; Face++
Terms of Service). None of the commercial gen-
der classiﬁers chosen for this analysis reported
performance metrics on existing gender estima-
tion benchmarks in their provided documenta-
tion. The Face++ terms of use explicitly dis-
claim any warranties of accuracy. Only IBM
provided conﬁdence scores (between 0 and 1) for
face-based gender classiﬁcation labels. But it did
not report how any metrics like true positive rates
(TPR) or false positive rates (FPR) were bal-
anced.
4.3. Evaluation Methodology
In following the gender classiﬁcation evaluation
precedent established by the National Institute
for Standards and Technology (NIST), we assess
8

Gender Shades
Classiﬁer Metric All F M Darker Lighter DF DM LF LM
MSFT
TPR(%) 93.7 89.3 97.4 87.1 99.3 79.2 94.0 98.3 100
Error Rate(%) 6.3 10.7 2.6 12.9 0.7 20.8 6.0 1.7 0.0
PPV (%) 93.7 96.5 91.7 87.1 99.3 92.1 83.7 100 98.7
FPR (%) 6.3 2.6 10.7 12.9 0.7 6.0 20.8 0.0 1.7
Face++
TPR(%) 90.0 78.7 99.3 83.5 95.3 65.5 99.3 90.2 99.2
Error Rate(%) 10.0 21.3 0.7 16.5 4.7 34.5 0.7 9.8 0.8
PPV (%) 90.0 98.9 85.1 83.5 95.3 98.8 76.6 98.9 92.9
FPR (%) 10.0 0.7 21.3 16.5 4.7 0.7 34.5 0.8 9.8
IBM
TPR(%) 87.9 79.7 94.4 77.6 96.8 65.3 88.0 92.9 99.7
Error Rate(%) 12.1 20.3 5.6 22.4 3.2 34.7 12.0 7.1 0.3
PPV (%) 87.9 92.1 85.2 77.6 96.8 82.3 74.8 99.6 94.8
FPR (%) 12.1 5.6 20.3 22.4 3.2 12.0 34.7 0.3 7.1
Table 4: Gender classiﬁcation performance as measured by the positive predictive value (PPV), error
rate (1-TPR), true positive rate (TPR), and false positive rate (FPR) of the 3 evaluated
commercial classiﬁers on the PPB dataset. All classiﬁers have the highest error rates for
darker-skinned females (ranging from 20.8% for Microsoft to 34.7% for IBM).
Classiﬁer Metric DF DM LF LM
MSFT
TPR(%) 76.2 100 100 100
Error Rate(%) 23.8 0.0 0.0 0.0
PPV(%) 100 84.2 100 100
FPR(%) 0.0 23.8 0.0 0.0
Face++
TPR(%) 64.0 99.5 92.6 100
Error Rate(%) 36.0 0.5 7.4 0.0
PPV(%) 99.0 77.8 100 96.9
FPR(%) 0.5 36.0 0.0 7.4
IBM
TPR(%) 66.9 94.3 100 98.4
Error Rate(%) 33.1 5.7 0.0 1.6
PPV(%) 90.4 78.0 96.4 100
FPR(%) 5.7 33.1 1.6 0.0
Table 5: Gender classiﬁcation performance as measured by the positive predictive value (PPV), error
rate (1-TPR), true positive rate (TPR), and false positive rate (FPR) of the 3 evaluated
commercial classiﬁers on the South African subset of the PPB dataset. Results for South
Africa follow the overall trend with the highest error rates seen on darker-skinned females.
the overall classiﬁcation accuracy, male classiﬁca-
tion accuracy, and female classiﬁcation accuracy
as measured by the true positive rate (TPR). Ex-
tending beyond the NIST methodology we also
evaluate the positive predictive value, false posi-
tive rate, and error rate (1-TPR) of the following
groups: all subjects, male subjects, female sub-
jects, lighter subjects, darker subjects, darker fe-
males, darker males, lighter females, and lighter
males. See Table 2 in supplementary materials
for results disaggregated by gender and each Fitz-
patrick Skin Type.
9

Gender Shades
4.4. Audit Results
Male and Female Error Rates
To conduct a demographic performance analy-
sis, the diﬀerences in male and female error rates
for each gender classiﬁer are compared ﬁrst in
aggregate (Table 4) and then for South Africa
(Table 5). The NIST Evaluation of Automated
Gender Classiﬁcation Algorithms report revealed
that gender classiﬁcation performance on female
faces was 1.8% to 12.5% lower than performance
on male faces for the nine evaluated algorithms
(Ngan et al., 2015). The gender misclassiﬁca-
tion rates on the Pilot Parliaments Benchmark
replicate this trend across all classiﬁers. The dif-
ferences between female and male classiﬁcation
error rates range from 8 .1% to 20 .6%. The rel-
atively high positive predictive value for females
indicate that when a face is predicted to be fe-
male the estimation is more likely to be correct
than when a face is predicted to be male. For the
Microsoft and IBM classiﬁers, the false positive
rates (FPR) for males are triple or more than
the FPR for females. The FPR for males is more
than 30 times that of females with the Face++
classiﬁer.
Darker and Lighter Error Rates
To conduct a phenotypic performance analysis,
the diﬀerences in darker and lighter skin type er-
ror rates for each gender classiﬁer are compared
ﬁrst in aggregate (Table 4) and then for South
Africa (Table 5). All classiﬁers perform better
on lighter subjects than darker subjects in PPB.
Microsoft achieves the best result with error rates
of 12.9% on darker subjects and 0 .7% on lighter
individuals. On darker subjects, IBM achieves
the worst classiﬁcation accuracy with an error
rate of 22.4%. This rate is nearly 7 times higher
than the IBM error rate on lighter faces.
Intersectional Error Rates
To conduct an intersectional demographic and
phenotypic analysis, the error rates for four inter-
sectional groups (darker females, darker males,
lighter females and lighter males) are compared
in aggregate and then for South Africa.
Across the board, darker females account for
the largest proportion of misclassiﬁed subjects.
Even though darker females make up 21 .3% of
the PPB benchmark, they constitute between
61.0% to 72.4% of the classiﬁcation error. Lighter
males who make up 30.3% of the benchmark con-
tribute only 0.0% to 2.4% of the total errors from
these classiﬁers (See Table 1 in supplementary
materials).
We present a deeper look at images from South
Africa to see if diﬀerences in algorithmic per-
formance are mainly due to image quality from
each parliament. In PPB, the European parlia-
mentary images tend to be of higher resolution
with less pose variation when compared to images
from African parliaments. The South African
parliament, however, has comparable image res-
olution and has the largest skin type spread of
all the parliaments. Lighter subjects makeup
20.8% (n=91) of the images, and darker subjects
make up the remaining 79 .2% ( n=346) of im-
ages. Table 5 shows that all algorithms perform
worse on female and darker subjects when com-
pared to their counterpart male and lighter sub-
jects. The Microsoft gender classiﬁer performs
the best, with zero errors on classifying all males
and lighter females.
On the South African subset of the PPB bench-
mark, all the error for Microsoft arises from mis-
classifying images of darker females. Table 5
also shows that all classiﬁers perform worse on
darker females. Face++ is ﬂawless on lighter
males. IBM performs best on lighter females
with 0 .0% error rate. Examining classiﬁcation
performance on the South African subset of PPB
reveals trends that closely match the algorith-
mic performance on the entire dataset. Thus,
we conclude that variation in performance due
to the image characteristics of each country does
not fully account for the diﬀerences in misclassiﬁ-
cation rates between intersectional subgroups. In
other words, the presence of more darker individ-
uals is a better explanation for error rates than a
deviation in how images of parliamentarians are
composed and produced. However, darker skin
alone may not be fully responsible for misclassi-
ﬁcation. Instead, darker skin may be highly cor-
related with facial geometries or gender display
norms that were less represented in the training
data of the evaluated classiﬁers.
10

Gender Shades
●●●●
●
●●●●
●
●●●●●
●
●●●●●●
●
●
●
●
●
●
●
●
●●●● ●●
●
●
●
●●●●
●
●
●
●●●●●●●
●
●●●●●●●●●●●●●●●●
●
●
●●
●
●●●●●●●●
●●
●●●●●●
●
●
●
●
●●●
●
●●●●
●
●●●
●
●●●
●●
●
●
●
●
●
●●●●
●
●
●●
●
●●
●
●●
●
●●
●
●
●
●●
●
●
●●
●
●
●
●
●
●
●
●
●
●
●●●●
●●●●●●●●●●
●
●
●
●
●●●●●●●●●●●
●●●●●●●●●
●
●●●●●●●
●
●●●●●●●●●●●●●●
●
●●●●●●●●●●
●
●●●●●●●●●●●●●●
●●
●
●
●
●●
0.00
0.25
0.50
0.75
1.00
Darker Female Darker Male Lighter Female Lighter Male
Group
Confidence Scores
Gender
Female
Male
Figure 4: Gender classiﬁcation conﬁdence scores
from IBM (IBM). Scores are near 1 for
lighter male and female subjects while
they range from ∼ 0.75 − 1 for darker
females.
4.5. Analysis of Results
The overall gender classiﬁcation accuracy results
show the obfuscating nature of single perfor-
mance metrics. Taken at face value, gender clas-
siﬁcation accuracies ranging from 87.9% to 93.7%
on the PPB dataset, suggest that these classi-
ﬁers can be used for all populations represented
by the benchmark. A company might justify the
market readiness of a classiﬁer by presenting per-
formance results in aggregate. Yet a gender and
phenotypic breakdown of the results shows that
performance diﬀers substantially for distinct sub-
groups. Classiﬁcation is 8 .1% − 20.6% worse on
female than male subjects and 11 .8% − 19.2%
worse on darker than lighter subjects.
Though helpful in seeing systematic error, gen-
der and skin type analysis by themselves do not
present the whole story. Is misclassiﬁcation dis-
tributed evenly amongst all females? Are there
other factors at play? Likewise, is the misclassi-
ﬁcation of darker skin uniform across gender?
The intersectional error analysis that targets
gender classiﬁcation performance on darker fe-
male, lighter female, darker male, and lighter
male subgroups provides more answers. Darker
females have the highest error rates for all gender
classiﬁers ranging from 20 .8% − 34.7%. For Mi-
crosoft and IBM classiﬁers lighter males are the
best classiﬁed group with 0 .0% and 0 .3% error
rates respectively. Face++ classiﬁes darker males
best with an error rate of 0.7%. When examining
the gap in lighter and darker skin classiﬁcation,
we see that even though darker females are most
impacted, darker males are still more misclassi-
ﬁed than lighter males for IBM and Microsoft.
The most improvement is needed on darker fe-
males speciﬁcally. More broadly, the error gaps
between male and female classiﬁcation along with
lighter and darker classiﬁcation should be closed.
4.6. Accuracy Metrics
Microsoft and Face++ APIs solely output single
labels indicating whether the face was classiﬁed
as female or male. IBM’s API outputs an ad-
ditional number which indicates the conﬁdence
with which the classiﬁcation was made. Fig-
ure 4 plots the distribution of conﬁdence values
for each of the subgroups we evaluate (i.e. darker
females, darker males, lighter females and lighter
males). Numbers near 0 indicate low conﬁdence
whereas those close to 1 denote high conﬁdence
in classifying gender. As shown in the box plots,
the API is most conﬁdent in classifying lighter
males and least conﬁdent in classifying darker fe-
males.
While conﬁdence values give users more in-
formation, commercial classiﬁers should provide
additional metrics. All 3 evaluated APIs only
provide gender classiﬁcations, they do not out-
put probabilities associated with the likelihood
of being a particular gender. This indicates that
companies are choosing a threshold which deter-
mines the classiﬁcation: if the prediction proba-
bility is greater than this threshold, the image is
determined to be that of a male (or female) sub-
ject, and viceversa if the probability is less than
this number. This does not give users the abil-
ity to analyze true positive (TPR) and false posi-
tive (FPR) rates for various subgroups if diﬀerent
thresholds were to be chosen. The commercial
classiﬁers have picked thresholds that result in
speciﬁc TPR and FPR rates for each subgroup.
And the FPR for some groups can be much higher
than those for others. By having APIs that fail
to provide the ability to adjust these thresholds,
they are limiting users’ ability to pick their own
TPR/FPR trade-oﬀ.
4.7. Data Quality and Sensors
It is well established that pose, illumination, and
expression (PIE) can impact the accuracy of au-
tomated facial analysis. Techniques to create ro-
bust systems that are invariant to pose, illumi-
nation, expression, occlusions, and background
have received substantial attention in computer
vision research (Kakadiaris et al., 2017; Ganguly
11

Gender Shades
et al., 2015; Ahmad Radzi et al., 2014). Illumi-
nation is of particular importance when doing an
evaluation based on skin type. Default camera
settings are often optimized to expose lighter skin
better than darker skin (Roth, 2009). Underex-
posed or overexposed images that present signif-
icant information loss can make accurate classi-
ﬁcation challenging.
With full awareness of the challenges that arise
due to pose and illumination, we intentionally
chose an optimistic sample of constrained images
that were taken from the parliamentarian web-
sites. Each country had its peculiarities. Images
from Rwanda and Senegal had more pose and
illumination variation than images from other
countries (Figure 1). The Swedish parliamen-
tarians all had photos that were taken with a
shadow on the face. The South African images
had the most consistent pose and illumination.
The South African subset was also composed of
a substantial number of lighter and darker sub-
jects. Given the diversity of the subset, the
high image resolution, and the consistency of
illumination and pose, our ﬁnding that classi-
ﬁcation accuracy varied by gender, skin type,
and the intersection of gender with skin type do
not appear to be confounded by the quality of
sensor readings. The disparities presented with
such a constrained dataset do suggest that error
rates would be higher on more challenging uncon-
strained datasets. Future work should explore
gender classiﬁcation on an inclusive benchmark
composed of unconstrained images.
5. Conclusion
We measured the accuracy of 3 commercial gen-
der classiﬁcation algorithms on the new Pilot
Parliaments Benchmark which is balanced by
gender and skin type. We annotated the dataset
with the Fitzpatrick skin classiﬁcation system
and tested gender classiﬁcation performance on 4
subgroups: darker females, darker males, lighter
females and lighter males. We found that all clas-
siﬁers performed best for lighter individuals and
males overall. The classiﬁers performed worst
for darker females. Further work is needed to
see if the substantial error rate gaps on the ba-
sis of gender, skin type and intersectional sub-
group revealed in this study of gender classiﬁca-
tion persist in other human-based computer vi-
sion tasks. Future work should explore intersec-
tional error analysis of facial detection, identiﬁ-
cation and veriﬁcation. Intersectional phenotypic
and demographic error analysis can help inform
methods to improve dataset composition, feature
selection, and neural network architectures.
Because algorithmic fairness is based on diﬀer-
ent contextual assumptions and optimizations for
accuracy, this work aimed to show why we need
rigorous reporting on the performance metrics on
which algorithmic fairness debates center. The
work focuses on increasing phenotypic and demo-
graphic representation in face datasets and algo-
rithmic evaluation. Inclusive benchmark datasets
and subgroup accuracy reports will be necessary
to increase transparency and accountability in
artiﬁcial intelligence. For human-centered com-
puter vision, we deﬁne transparency as providing
information on the demographic and phenotypic
composition of training and benchmark datasets.
We deﬁne accountability as reporting algorith-
mic performance on demographic and pheno-
typic subgroups and actively working to close
performance gaps where they arise. Algorith-
mic transparency and accountability reach be-
yond technical reports and should include mech-
anisms for consent and redress which we do not
focus on here. Nonetheless, the ﬁndings from this
work concerning benchmark representation and
intersectional auditing provide empirical support
for increased demographic and phenotypic trans-
parency and accountability in artiﬁcial intelli-
gence.
Acknowledgments
We thank board-certiﬁed surgical dermatologist
Dr. Helen Raynham for providing the oﬃcial
Fitzpatrick annotations for the Pilot Parliaments
Benchmark.
References
Face++ API. http://old .faceplusplus.com/
demo-detect/. Accessed: 2017-10-06.
Face, Google APIs for Android, Google De-
velopers. https://developers .google.com/
android/reference/com/google/android/
gms/vision/face/Face . Accessed: 2017-10-
06.
12

Gender Shades
Watson Visual Recognition. https :
/ / www.ibm.com / watson / services / visual -
recognition/. Accessed: 2017-10-06.
Microsoft Face API. https : / /
www.microsoft.com / cognitive - services /
en-us/faceapi. Accessed: 2017-10-06.
Aﬀectiva Emotion Recognition Software and
Analysis. https://www.affectiva.com/. Ac-
cessed: 2017-10-06.
Physiognomys New Clothes. https : / /
medium.com / @blaisea / physiognomys - new -
clothes-f2d4b59fdd6a. Accessed: 2017-10-
06.
Face++ Terms of Use. a. Accessed: 2018-12-13.
Faception, Facial Personality Analytics. https:
//www.faception.com/, b. Accessed: 2017-10-
06.
Visual Recognition API Reference. Accessed:
2018-12-13.
How to Detect Faces in Image. Accessed: 2018-
12-13.
Proportion of seats held by women in national
parliaments. https://data .worldbank.org/
indicator/SG .GEN.PARL.ZS?year high desc=
true. Accessed: 2017-10-06.
Syafeeza Ahmad Radzi, Khalil-Hani Mohamad,
Shan Sung Liew, and Rabia Bakhteri. Con-
volutional neural network for face recognition
with pose and illumination variation. Interna-
tional Journal of Engineering and Technology
(IJET), 6(1):44–57, 2014.
Julia Angwin, Jeﬀ Larson, Surya Mattu, and
Lauren Kirchner. Machine bias: Theres soft-
ware used across the country to predict future
criminals. and its biased against blacks. ProP-
ublica, May, 23, 2016.
Yancheng Bai and Bernard Ghanem. Multi-scale
fully convolutional network for face detection
in the wild. In Computer Vision and Pattern
Recognition Workshops (CVPRW), 2017 IEEE
Conference on, pages 2078–2087. IEEE, 2017.
Tolga Bolukbasi, Kai-Wei Chang, James Y Zou,
Venkatesh Saligrama, and Adam T Kalai. Man
is to computer programmer as woman is to
homemaker? debiasing word embeddings. In
D. D. Lee, M. Sugiyama, U. V. Luxburg,
I. Guyon, and R. Garnett, editors, Advances
in Neural Information Processing Systems 29 ,
pages 4349–4357. Curran Associates, Inc.,
2016. URL http://papers .nips.cc/paper/
6228 - man - is - to - computer - programmer -
as - woman - is - to - homemaker - debiasing -
word-embeddings.pdf.
Encyclopedia Britannica. Skin distribution map.
https://media1.britannica.com/eb-media/
59 / 61759 - 004 - 9A507F1C.gif, 2012. Ac-
cessed: 2017-12-17.
Aylin Caliskan, Joanna J Bryson, and Arvind
Narayanan. Semantics derived automatically
from language corpora contain human-like bi-
ases. Science, 356(6334):183–186, 2017.
Danielle Keats Citron and Frank A Pasquale.
The scored society: due process for automated
predictions. 2014.
Afshin Dehghan, Enrique G Ortiz, Guang Shu,
and Syed Zain Masood. Dager: Deep age,
gender and emotion recognition using con-
volutional neural network. arXiv preprint
arXiv:1702.04280, 2017.
Andre Esteva, Brett Kuprel, Roberto A Novoa,
Justin Ko, Susan M Swetter, Helen M Blau,
and Sebastian Thrun. Dermatologist-level clas-
siﬁcation of skin cancer with deep neural net-
works. Nature, 542(7639):115–118, 2017.
C Fabian Benitez-Quiroz, Ramprakash Srini-
vasan, and Aleix M Martinez. Emotionet: An
accurate, real-time algorithm for the automatic
annotation of a million facial expressions in the
wild. In Proceedings of the IEEE Conference
on Computer Vision and Pattern Recognition ,
pages 5562–5570, 2016.
Giovanna Farinella and Jean-Luc Dugelay. De-
mographic classiﬁcation: Do gender and eth-
nicity aﬀect each other? In Informatics, Elec-
tronics & Vision (ICIEV), 2012 International
Conference on, pages 383–390. IEEE, 2012.
Sorelle A Friedler, Carlos Scheidegger, and
Suresh Venkatasubramanian. On the (im)
possibility of fairness. arXiv preprint
arXiv:1609.07236, 2016.
13

Gender Shades
Suranjan Ganguly, Debotosh Bhattacharjee, and
Mita Nasipuri. Illumination, pose and occlu-
sion invariant face recognition from range im-
ages using erﬁ model. International Journal of
System Dynamics Applications (IJSDA) , 4(2):
1–20, 2015.
Clare Garvie, Alvaro Bedoya, and Jonathan
Frankle. The Perpetual Line-Up: Unregulated
Police Face Recognition in America . George-
town Law, Center on Privacy & Technology,
2016.
Hu Han and Anil K Jain. Age, gender and
race estimation from unconstrained face im-
ages. Dept. Comput. Sci. Eng., Michigan State
Univ., East Lansing, MI, USA, MSU Tech.
Rep.(MSU-CSE-14-5), 2014.
Moritz Hardt, Eric Price, Nati Srebro, et al.
Equality of opportunity in supervised learning.
In Advances in Neural Information Processing
Systems, pages 3315–3323, 2016a.
Moritz Hardt, Eric Price, Nati Srebro, et al.
Equality of opportunity in supervised learning.
In Advances in Neural Information Processing
Systems, pages 3315–3323, 2016b.
Gary B Huang, Manu Ramesh, Tamara Berg,
and Erik Learned-Miller. Labeled faces in the
wild: A database for studying face recogni-
tion in unconstrained environments. Technical
report, Technical Report 07-49, University of
Massachusetts, Amherst, 2007.
Ioannis A Kakadiaris, George Toderici, Georgios
Evangelopoulos, Georgios Passalis, Dat Chu,
Xi Zhao, Shishir K Shah, and Theoharis Theo-
haris. 3d-2d face recognition with pose and
illumination normalization. Computer Vision
and Image Understanding , 154:137–151, 2017.
Ira Kemelmacher-Shlizerman, Steven M Seitz,
Daniel Miller, and Evan Brossard. The
megaface benchmark: 1 million faces for recog-
nition at scale. In Proceedings of the IEEE
Conference on Computer Vision and Pattern
Recognition, pages 4873–4882, 2016.
Niki Kilbertus, Mateo Rojas-Carulla, Giambat-
tista Parascandolo, Moritz Hardt, Dominik
Janzing, and Bernhard Sch¨ olkopf. Avoiding
discrimination through causal reasoning. arXiv
preprint arXiv:1706.02744, 2017.
Brendan F Klare, Mark J Burge, Joshua C
Klontz, Richard W Vorder Bruegge, and
Anil K Jain. Face recognition performance:
Role of demographic information.IEEE Trans-
actions on Information Forensics and Security,
7(6):1789–1801, 2012.
Brendan F Klare, Ben Klein, Emma Taborsky,
Austin Blanton, Jordan Cheney, Kristen Allen,
Patrick Grother, Alan Mah, and Anil K Jain.
Pushing the frontiers of unconstrained face de-
tection and recognition: Iarpa janus bench-
mark a. In Proceedings of the IEEE Conference
on Computer Vision and Pattern Recognition ,
pages 1931–1939, 2015.
Michal Kosinski and Yilun Wang. Deep neural
networks are more accurate than humans at
detecting sexual orientation from facial images.
2017.
Marco Leo, Marco Del Coco, Pierluigi Carcagni,
Cosimo Distante, Massimo Bernava, Giovanni
Pioggia, and Giuseppe Palestra. Automatic
emotion recognition in robot-children interac-
tion for asd treatment. In Proceedings of the
IEEE International Conference on Computer
Vision Workshops, pages 145–153, 2015.
Gil Levi and Tal Hassner. Age and gender classiﬁ-
cation using convolutional neural networks. In
Proceedings of the IEEE Conference on Com-
puter Vision and Pattern Recognition Work-
shops, pages 34–42, 2015a.
Gil Levi and Tal Hassner. Age and gender classiﬁ-
cation using convolutional neural networks. In
Proceedings of the IEEE Conference on Com-
puter Vision and Pattern Recognition Work-
shops, pages 34–42, 2015b.
Markus Mathias, Rodrigo Benenson, Marco Ped-
ersoli, and Luc Van Gool. Face detection with-
out bells and whistles. In European Conference
on Computer Vision , pages 720–735. Springer,
2014.
Chiara Melloni, Jeﬀrey S Berger, Tracy Y Wang,
Funda Gunes, Amanda Stebbins, Karen S
Pieper, Rowena J Dolor, Pamela S Douglas,
Daniel B Mark, and L Kristin Newby. Repre-
sentation of women in randomized clinical tri-
als of cardiovascular disease prevention. Circu-
14

Gender Shades
lation: Cardiovascular Quality and Outcomes ,
3(2):135–142, 2010.
Mei Ngan, Mei Ngan, and Patrick Grother. Face
recognition vendor test (FRVT) performance of
automated gender classiﬁcation algorithms. US
Department of Commerce, National Institute
of Standards and Technology, 2015.
Cathy O’Neil. Weapons of math destruction:
How big data increases inequality and threat-
ens democracy. Broadway Books, 2017.
Giuseppe Palestra, Giovanna Varni, Mohamed
Chetouani, and Floriana Esposito. A multi-
modal and multilevel system for robotics treat-
ment of autism in children. In Proceedings of
the International Workshop on Social Learn-
ing and Multimodal Interaction for Designing
Artiﬁcial Agents, page 3. ACM, 2016.
Omkar M Parkhi, Andrea Vedaldi, Andrew Zis-
serman, et al. Deep face recognition. In
BMVC, volume 1, page 6, 2015.
P Jonathon Phillips, Fang Jiang, Abhijit
Narvekar, Julianne Ayyad, and Alice J
O’Toole. An other-race eﬀect for face recogni-
tion algorithms. ACM Transactions on Applied
Perception (TAP), 8(2):14, 2011.
Alice B Popejoy and Stephanie M Fullerton. Ge-
nomics is failing on diversity. Nature, 538
(7624):161, 2016.
Rajeev Ranjan, Swami Sankaranarayanan, Car-
los D Castillo, and Rama Chellappa. An all-in-
one convolutional neural network for face anal-
ysis. In Automatic Face & Gesture Recogni-
tion (FG 2017), 2017 12th IEEE International
Conference on, pages 17–24. IEEE, 2017.
Daniel Reid, Sina Samangooei, Cunjian Chen,
Mark Nixon, and Arun Ross. Soft biometrics
for surveillance: an overview. Machine learn-
ing: theory and applications. Elsevier , pages
327–352, 2013.
Lorna Roth. Looking at shirley, the ultimate
norm: Colour balance, image technologies, and
cognitive equity.Canadian Journal of Commu-
nication, 34(1):111, 2009.
Rasmus Rothe, Radu Timofte, and Luc
Van Gool. Deep expectation of real and ap-
parent age from a single image without facial
landmarks. International Journal of Computer
Vision, pages 1–14, 2016.
Ramprakash Srinivasan, Julie D Golomb, and
Aleix M Martinez. A neural basis of facial ac-
tion recognition in humans. Journal of Neuro-
science, 36(16):4434–4442, 2016.
Yaniv Taigman, Ming Yang, Marc’Aurelio Ran-
zato, and Lior Wolf. Deepface: Closing the
gap to human-level performance in face veri-
ﬁcation. In Proceedings of the IEEE confer-
ence on computer vision and pattern recogni-
tion, pages 1701–1708, 2014.
Fitzpatrick TB. The validity and practicality of
sun-reactive skin types i through vi. Archives
of Dermatology , 124(6):869–871, 1988. doi:
10.1001 / archderm .1988.01670060015008.
URL +http : / / dx.doi.org / 10.1001 /
archderm.1988.01670060015008.
Bart Thomee, David A Shamma, Gerald Fried-
land, Benjamin Elizalde, Karl Ni, Douglas
Poland, Damian Borth, and Li-Jia Li. The
new data and new challenges in multimedia re-
search. arXiv preprint arXiv:1503.01817, 1(8),
2015.
Yandong Wen, Kaipeng Zhang, Zhifeng Li, and
Yu Qiao. A discriminative feature learning ap-
proach for deep face recognition. In European
Conference on Computer Vision , pages 499–
515. Springer, 2016.
Xiaolin Wu and Xi Zhang. Automated infer-
ence on criminality using face images. arXiv
preprint arXiv:1611.04135, 2016.
Stefanos Zafeiriou, Cha Zhang, and Zhengyou
Zhang. A survey on face detection in the wild:
past, present and future. Computer Vision and
Image Understanding, 138:1–24, 2015.
15
```

## Merged notes from duplicate

_Source file:_ `Gender Shades_ Intersectional Accuracy Disparities in Commercial Gender Classification.md`

[[Gender Shades Intersectional Accuracy Disparities in Commercial Gender Classification.pdf]]

Joy Buolamwini, Timnit Gebru

*Proceedings of the 1st Conference on Fairness, Accountability and Transparency*, PMLR 81:77-91, 2018.

#### Abstract

Recent studies demonstrate that machine learning algorithms can discriminate based on classes like race and gender. In this work, we present an approach to evaluate bias present in automated facial analysis algorithms and datasets with respect to phenotypic subgroups. Using the dermatologist approved Fitzpatrick Skin Type classification system, we characterize the gender and skin type distribution of two facial analysis benchmarks, IJB-A and Adience. We find that these datasets are overwhelmingly composed of lighter-skinned subjects (79.6% for IJB-A and 86.2% for Adience) and introduce a new facial analysis dataset which is balanced by gender and skin type. We evaluate 3 commercial gender classification systems using our dataset and show that darker-skinned females are the most misclassified group (with error rates of up to 34.7%). The maximum error rate for lighter-skinned males is 0.8%. The substantial disparities in the accuracy of classifying darker females, lighter females, darker males, and lighter males in gender classification systems require urgent attention if commercial companies are to build genuinely fair, transparent and accountable facial analysis algorithms.

#### Cite this Paper

---

BibTeX

`  @InProceedings{pmlr-v81-buolamwini18a,   title = 	 {Gender Shades: Intersectional Accuracy Disparities in Commercial Gender Classification},   author = 	 {Buolamwini, Joy and Gebru, Timnit},   booktitle = 	 {Proceedings of the 1st Conference on Fairness, Accountability and Transparency},   pages = 	 {77--91},   year = 	 {2018},   editor = 	 {Friedler, Sorelle A. and Wilson, Christo},   volume = 	 {81},   series = 	 {Proceedings of Machine Learning Research},   month = 	 {23--24 Feb},   publisher =    {PMLR},   pdf = 	 {http://proceedings.mlr.press/v81/buolamwini18a/buolamwini18a.pdf},   url = 	 {https://proceedings.mlr.press/v81/buolamwini18a.html},   abstract = 	 {Recent studies demonstrate that machine learning algorithms can discriminate based on classes like race and gender. In this work, we present an approach to evaluate bias present in automated facial analysis algorithms and datasets with respect to phenotypic subgroups. Using the dermatologist  approved Fitzpatrick Skin Type classification system, we characterize the gender and skin type distribution of two facial analysis benchmarks, IJB-A and Adience. We find that these datasets are overwhelmingly composed of lighter-skinned subjects (79.6% for IJB-A and 86.2% for Adience) and introduce a new facial analysis dataset which is balanced by gender and skin type. We evaluate 3 commercial gender classification systems using our dataset and show that darker-skinned females are the most misclassified group (with error rates of up to 34.7%). The maximum error rate for lighter-skinned males is 0.8%. The substantial disparities in the accuracy of classifying darker females, lighter females, darker males, and lighter males in gender classification systems require urgent attention if commercial companies are to build genuinely fair, transparent and accountable facial analysis algorithms.} }  `

Endnote

`%0 Conference Paper %T Gender Shades: Intersectional Accuracy Disparities in Commercial Gender Classification %A Joy Buolamwini %A Timnit Gebru %B Proceedings of the 1st Conference on Fairness, Accountability and Transparency %C Proceedings of Machine Learning Research %D 2018 %E Sorelle A. Friedler %E Christo Wilson	 %F pmlr-v81-buolamwini18a %I PMLR %P 77--91 %U https://proceedings.mlr.press/v81/buolamwini18a.html %V 81 %X Recent studies demonstrate that machine learning algorithms can discriminate based on classes like race and gender. In this work, we present an approach to evaluate bias present in automated facial analysis algorithms and datasets with respect to phenotypic subgroups. Using the dermatologist  approved Fitzpatrick Skin Type classification system, we characterize the gender and skin type distribution of two facial analysis benchmarks, IJB-A and Adience. We find that these datasets are overwhelmingly composed of lighter-skinned subjects (79.6% for IJB-A and 86.2% for Adience) and introduce a new facial analysis dataset which is balanced by gender and skin type. We evaluate 3 commercial gender classification systems using our dataset and show that darker-skinned females are the most misclassified group (with error rates of up to 34.7%). The maximum error rate for lighter-skinned males is 0.8%. The substantial disparities in the accuracy of classifying darker females, lighter females, darker males, and lighter males in gender classification systems require urgent attention if commercial companies are to build genuinely fair, transparent and accountable facial analysis algorithms. `

APA

`  Buolamwini, J. & Gebru, T.. (2018). Gender Shades: Intersectional Accuracy Disparities in Commercial Gender Classification. *Proceedings of the 1st Conference on Fairness, Accountability and Transparency*, in *Proceedings of Machine Learning Research* 81:77-91 Available from https://proceedings.mlr.press/v81/buolamwini18a.html.   `

---

#### Related Material

- [Download PDF](http://proceedings.mlr.press/v81/buolamwini18a/buolamwini18a.pdf)
- [Supplementary PDF](http://proceedings.mlr.press/v81/buolamwini18a/buolamwini18a-supp.pdf)