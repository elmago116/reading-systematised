---
title: "Perpetuating misogyny with generative AI: How model personalization normalizes gendered harm"
author: Laura A. Wagner, Eva Cetinić
year: "2026"
Type: Article
DOI: 10.1177/20539517261467361
source: https://doi.org/10.1177/20539517261467361
created: 2026-08-06
description: Open-source text-to-image (TTI) pipelines have become dominant in the landscape of AI-generated visual content, driven by technological advances that enable users to personalize models through adapters tailored to specific tasks. While personalization methods such as LoRA (low-rank adaptation) offer
tags:
  - themes/gender
  - tech/Ai/LLM
  - tech/Ai
  - tech/Ai/personalization
  - themes/ethics/normalization
pdfORepub: "[[Perpetuating misogyny with generative AI - How model personalization normalizes gendered harm.pdf]]"
---
[[Perpetuating misogyny with generative AI - How model personalization normalizes gendered harm.pdf]]

> **Abstract:** Open-source text-to-image (TTI) pipelines have become dominant in the landscape of AI-generated visual content, driven by technological advances that enable users to personalize models through adapters tailored to specific tasks. While personalization methods such as LoRA (low-rank adaptation) offer unprecedented creative opportunities, they also facilitate harmful practices, including the generation of non-consensual deepfakes and the amplification of misogynistic or hypersexualized content. This study presents an exploratory sociotechnical analysis of CivitAI, the most active platform for sharing and developing open-source TTI models. Drawing on a dataset of more than 40 million user-generated images and over 230,000 models, we find a disproportionate rise in not-safe-for-work (NSFW) content and a significant number of models intended to mimic real individuals. We also observe a strong influence of internet subcultures on the tools and practices shaping model personalizations and res
## Full text (extracted from `Perpetuating misogyny with generative AI - How model personalization normalizes gendered harm.pdf`)

*Source:* `2PDF/Perpetuating misogyny with generative AI - How model personalization normalizes gendered harm.pdf`  
*Extracted:* 2026-08-06

```text
Perpetuating misogyny with generative
AI: How model personalization
normalizes gendered harm
Laura Wagner1 and Eva Cetinić 1
Abstract
Open-source text-to-image (TTI) pipelines have become dominant in the landscape of AI-generated visual content, driven
by technological advances that enable users to personalize models through adapters tailored to speciﬁc tasks. While per-
sonalization methods such as LoRA (low-rank adaptation) offer unprecedented creative opportunities, they also facilitate
harmful practices, including the generation of non-consensual deepfakes and the ampliﬁcation of misogynistic or hyper-
sexualized content. This study presents an exploratory sociotechnical analysis of CivitAI, the most active platform for
sharing and developing open-source TTI models. Drawing on a dataset of more than 40 million user-generated images
and over 230,000 models, weﬁnd a disproportionate rise in not-safe-for-work (NSFW) content and a signiﬁcant number
of models intended to mimic real individuals. We also observe a strong inﬂuence of internet subcultures on the tools and
practices shaping model personalizations and resulting visual media. In response to theseﬁndings, we contextualize the
emergence of exploitative visual media through feminist and constructivist perspectives on technology, emphasizing how
design choices and community dynamics shape platform outcomes. Building on this analysis, we propose interventions
aimed at mitigating downstream harm, including improved content moderation, rethinking tool design, and establishing
clearer platform policies to promote accountability and consent.
Content warning:This paper contains references to pornography, gender-based digital violence and verbal vulgarity
that might be disturbing, distressing, and/or offensive.
Keywords
Artiﬁcial intelligence, Generative AI, text-to-image models, Open-Source AI, platformization, model personalization,
deepfakes, community-driven development, visual culture, gender bias, NSFW content, CivitAI, digital feminism
Received: 21 May 2025; accepted: 21 June 2026
Introduction
The evolution of open-source text-to-image (TTI) technol-
ogy has shifted from being a niche area for early adopters
to becoming a vast ecosystem driven by increasing invest-
ment and commercialization. The technology continues to
advance rapidly, with recent innovations allowing users to
personalize models through model adapters, tailoring
them for speciﬁc tasks and creative pursuits such as mim-
icking a speciﬁc art style or reproducing the physiognomy
of a particular individual.
While model personalizations open up unprecedented op-
portunities for artists and researchers, they also raise signiﬁ-
cant ethical and legal concerns, particularly the potential for
misuse such as non-consensual deepfakes and disinforma-
tion. Platforms like CivitAI (2024), a pioneering and
established hub for developing and sharing open-source
TTI models, have played a central role in the expansion of
AI-generated content and speciﬁcally TTI models. What
sets model-sharing hubs apart from other platforms is their
function: the content shared on these hubs is not an end prod-
uct but a tool for generating limitless derivative content. In
our study we focus on the analysis of CivitAI, a community-
driven platform for sharing, customizing and discovering
1Department of Art History, University of Zurich, Zurich, Switzerland
Corresponding author:
Eva Cetinić , Department of Art History, University of Zurich, Zurich
8006, Switzerland.
Email: eva.cetinic@uzh.ch
Creative Commons Non Commercial CC BY-NC: This article is distributed under the terms of the Creative Commons Attribution-
NonCommercial 4.0 License (https://creativecommons.org/licenses/by-nc/4.0/) which permits non-commercial use, reproduction and
distribution of the work without further permission provided the original work is attributed as speciﬁed on the SAGE and Open Access page (https://us.
sagepub.com/en-us/nam/open-access-at-sage).
Original research article
Big Data & Society
July–September: 1–18
© The Author(s) 2026
Article reuse guidelines:
sagepub.com/journals-permissions
DOI: 10.1177/20539517261467361
journals.sagepub.com/home/bds


personalized models. CivitAI differs from other model-
sharing platforms by focusing speciﬁcally on creative image
generation, with built-in community features that actively
promote model personalization and derivative visual work,
rather than serving as a general-purpose repository.
The models shared on this platform are usually trained
on smaller, more specialized datasets than general-purpose
models, and enable users to create vast amounts of content
that mimics the characteristics of that training data, which
can then be widely shared across social media and other on-
line platforms. This dynamic harbors a high potential for the
rapid propagation of generated content, the impact of which
can extend far beyond the communities creating these mod-
els. Given that such models can produce entirely fabricated,
photorealistic, and convincing imagery within seconds, this
capacity is particularly concerning, as it enables and ampli-
ﬁes forms of technology-facilitated gender-based violence
(TFGBV) (UN Women, 2024).
We aim to highlight how CivitAI, as a representative ex-
ample of community-oriented model-sharing platforms, may
contribute to these concerning developments by fostering en-
vironments that, through certain design choices and commu-
nity norms, can become more tolerant of abusive practices
while simultaneously growing less welcoming for some
user groups. Drawing on a deﬁnition of misogyny as a set
of hostile mechanisms designed to reinforce patriarchal power
structures (Manne, 2017), our objective is to investigate how
these dynamics manifest themselves on open-source model-
sharing platforms, as exempliﬁed by CivitAI. Speciﬁcally,
we document patterns of over-sexualization, objectiﬁcation,
and erosion of consent in TTI models and imagery, with wo-
men emerging as a primary target of these dynamics.
1
Our study examines the underlying mechanisms contrib-
uting to the escalation of not-safe-for-work (NSFW) content
and the perpetuation of misogynistic tropes within CivitAI.
The prevalence of NSFW content is illustrated in Figure 1,
which shows a uniformly random sample of images from
our initial data collection in March 2024, when weﬁrst in-
itiated this study. These images are categorized by the plat-
form moderation system according to different levels of
NSFW and reﬂect the distribution of content that initially
motivated our analysis. We perform a detailed analysis of
user-generated content, model adapters, and textual training
data to uncover how community-driven, tool-driven, and
model-infused biases may have intensiﬁed within the plat-
form’s ecosystem over two years from January 2023 to
December 2024. Our analysis reveals patterns consistent
with a self-reinforcing dynamic in which certain types of
content become increasingly normalized. We discuss how
these patterns align with theoretical frameworks suggesting
such normalization may foster environments more permis-
sive of harmful and exploitative material.
Besides documenting problematic aspects of open-
source TTI systems, we discuss potential areas for interven-
tion, such as improving tools used for training models and
model adapters, vetting model metadata, and developing
and enforcing ethical frameworks. Without such interven-
tions, the persistence of problematic patterns may under-
mine the legitimacy and long-term sustainability of
open-source innovation, potentially inviting more restrict-
ive external regulation or eroding public trust in these tech-
nologies. By identifying these patterns, our study aims to
contribute to a more inclusive and responsible open-source
TTI ecosystem and to support more equitable representation
in AI-generated content.
Investigating model personalization and
model-sharing platforms: A case study of
CivitAI
In early 2021, OpenAI introduced the TTI system DALL·E
(OpenAI, 2021) and publicly released its CLIP component
(Radford et al., 2021), a model trained on large-scale im-
age–text pairs that enabled semantic alignment between lan-
guage and images and became foundational for later TTI
generation systems. The open-source community aimed to
recreate similar TTI functionality through shared experi-
mentation, with early pipelines circulating via social media
and Discord channels and developing within collaborative
communities focused primarily on creative and artistic ap-
plications (Oppenlaender, 2022).
Figure 1. Random sample of images from CivitAI (March 2024) with different NSFW levels as assigned by the platform.
2 Big Data & Society 13(3)

The release of Stable Diffusion in 2022 (Rombach et al.,
2022) marked a milestone as theﬁrst open-source TTI foun-
dation model. Its popularity due to high-quality image gener-
ation capabilities indicated a shift from community-driven
innovation toward investor-funded commercial activity. At
the same time, increased scrutiny emerged over copyright vio-
lations, attribution issues, and social biases stemming from
training on uncurated web-scraped data. Systematic research
efforts emerged to quantify and evaluate gender, racial, and
cultural biases in generated images. In particular, several stud-
ies have documented gender biases in occupational represen-
tation that mirror and reinforce real-world inequalities (Sim
et al., 2025; Wang et al., 2024; Wu et al., 2024, 2025).
Beyond occupational roles, these models have been shown
to perpetuate broader patterns of stereotyping across multiple
demographic categories (Naik and Nushi, 2023; Schneider
and Hagendorff, 2025; Suﬁan et al., 2025). Researchers
have also identiﬁed racial biases in the representation of
skin tones and ethnic features (AlDahoul et al., 2025;
Ghosh and Caliskan, 2023), as well as cultural biases that priv-
ilege Western perspectives and aesthetics (Kannen et al.,
2024; Liu et al., 2024b; Shi et al., 2025; Zhang et al., 2024).
Many of these issues emerge from limitations in founda-
tional datasets, which not only reﬂect biases but have also
been shown to contain various forms of problematic con-
tent. For example, the LAION datasets, which are founda-
tional to many TTI models despite being “not
recommended” for commercial use (Buschek and Thorp,
2025), initially contained harmful content (Birhane et al.,
2023, 2021), including child sexual abuse material (Thiel
et al., 2023). In response, LAION temporarily removed,
cleaned, and re-released the datasets, highlighting that foun-
dational dataset curation is an ongoing process.
While such interventions address foundation model
training data, model personalizations are created through
ﬁne-tuning with small, user-curated datasets which are
mostly undisclosed. As a result, improvements to founda-
tional datasets have limited impact on the potential harms
emerging within personalization workﬂows. Recent devel-
opments in model personalization techniques such as
LoRA (low-rank adaptation) (Hu et al., 2022), originally
developed for language models and later adapted for TTI,
and textual inversion (Gal et al., 2023), offer reﬁned control
over generated content without retraining entire models.
Applications with graphical user interfaces, such as
Stable-Diffusion-WebUI (automatic1111, 2022) and
ComfyUI (comfyanonymous, 2023), lowered the barrier
to entry for TTI, allowing users to personalize models easily
and without advanced technical skills. However, model per-
sonalization introduced new risks, particularly through the
tailored generation of deepfake imagery, exacerbating
digital sexual violence disproportionately affecting women
(Viola and Voto, 2023).
Despite the growing prominence of model personaliza-
tion techniques and sharing platforms, research into their
implications remains limited. Early investigative journalism
documented the prevalence of NSFW content and sexually
exploitative AI-generated imagery, including non-
consensual deepfakes (Maiberg, 2023, 2024). Subsequent
studies conﬁrmed the widespread presence of abusive gen-
erative practices on CivitAI, including thousands of non-
consensual deepfake models (Hawkins et al., 2025; Wei
et al., 2024). Research on user prompting patterns on
CivitAI highlights a high prevalence of NSFW material
(Palmini et al., 2024). Platform governance research high-
lights moderation failures, including weak responses to ar-
tists’ consent concerns (Gorwa and Veale, 2024) and
shortcomings in open-source licensing frameworks (Cui
and Araujo, 2024).
Our exploratory analysis of CivitAI aims to quantify and
contextualize these systemic challenges as they manifest on
this platform. Understanding the layered structure through
which content is produced and shaped, including generative
models and the surrounding sociotechnical ecosystem, of-
fers valuable insight into this case and supports a more hol-
istic perspective on model-sharing platforms.
Figure 2 provides a schematic overview of the CivitAI plat-
form, illustrating the layers of content generation and circula-
tion. We focused our analysis on CivitAI as it represents the
most established model-sharing platform exclusively dedi-
cated to TTI personalizations, distinguished by its rapid
growth and integration of social community-building features.
Data collection and categorization
To illustrate the evolving dynamics of this model-sharing
platform, we collected and analyzed image metadata, model
metadata, and training process metadata from content pub-
lished on CivitAI over a 2-year period (late November 2022
to December 2024), using the CivitAI REST API (CivitAI,
2023). The dataset covers 40,630,560 images (Wagner and
Cetinic, 2025a) and 231,252 models (Wagner and Cetinic,
2025b) as of 19
th January 2025. The model metadata in-
cludes 9,948 standalone models, commonly referred to as
“checkpoints,” capable of generating images independ-
ently, and 221,304 adapters (e.g., LoRA, Textual
Inversion) that require a checkpoint to function. We ana-
lyzed three primary data categories:image metadata, model
metadata, andtraining process metadata.
Image metadata consists ofcontent-organization meta-
data and generation metadata. Content-organization meta-
data includes identi ﬁers (CivitAI ID, perceptual hash),
creator usernames, timestamps, engagement metrics (likes)
and NSFW categories. CivitAI assigns images to one ofﬁve
NSFW levels. For this, a tiered content classiﬁcation system
known as “browsing levels” is used, loosely based on
Motion Picture Association ﬁlm ratings (Motion Picture
Association, 2023), ranging from level 1 (PG, safe for all
ages) to level 8 (X, restricted to adults 18+), with an add-
itional level 16 (XXX) introduced for the most extreme
Wagner and Cetinić 3

content. Generation metadata includes the settings, models,
and adapters used to produce each image (identiﬁed by
CivitAI IDs or model hashes). For an example structure
see Figure S1 in the Supplemental material.
Model-related metadata includes unique CivitAI IDs,
version-speciﬁc IDs, download counts, timestamps, en-
gagement metrics and a POI (person of interest)ﬂag indicat-
ing deepfake models. Metadata from model creation
pipelines, including base model details and framework-
speciﬁc hashes, facilitates identiﬁcation. A detailed struc-
ture is shown in Figure S2 in the Supplemental material.
Finally, we extracted metadata written during training of
a model, which were used to identify the auto-tagging sys-
tem responsible for annotating the training data for model
personalizations. This metadata was extracted from the
downloaded model adapter ﬁles (in the
*.safetensors format, as described by by321 (2022).
A detailed overview of the data structure can be found in
our Supplemental material, Figure S3.
Image-level analysis: Trends and representations
To deepen our understanding of the visual material beyond ini-
tial impressions of the user-facing layer of the CivitAI plat-
form, we examined all images and their metadata shared
between January 2023 and December 2024. Weﬁrst quanti-
ﬁed temporal trends in the distribution of NSFW classiﬁcation
levels assigned by the CivitAI platform, as extracted from im-
age metadata. We then analyzed the images themselves with
regard to the demographic characteristics of depicted subjects,
employing a classiﬁer trained to infer age and gender to reveal
broader trends in the generation of humanﬁgures.
Quantifying NSFW trends. We examine how the compos-
ition of the CivitAI image corpus has changed over time
with respect to associated NSFW levels. A previous study
described by Palmini et al. (2024) revealed a disproportion-
ate increase in NSFW imagery compared to SFW on
CivitAI with the NSFW ratio, deﬁned as the proportion of
all imagesﬂagged as NSFW and assigned any browsing le-
vel other than 1 (which is SFW), increased from 56% in
October 2023 to 73% in April 2024. Additionally, Wei
et al. (2024) demonstrated that NSFW images receive
more social engagement on CivitAI than SFW images.
Our current study extends the dataset to include model
metadata and covers a full two-year period, from January
2023 to December 2024. With this extended dataset, we
conﬁrm a continuation of the trend, with the NSFW ratio in-
creasing from 41% in January 2023 to 80% by the end of
December 2024. This trend is visualized in Figure 3, which
presents a stacked bar diagram showing the color-coded
proportions of over 40 million images according to their as-
signed NSFW browsing level, posted to CivitAI between
January 2023 and December 2024. A more detailed account
of monthly trends in image generation and NSFW classiﬁ-
cation is provided in Table S1 in the Supplemental material.
Demographic patterns in generated images. To analyze and
quantify the demographic distribution of human subjects
depicted in generated images shared via CivitAI, we em-
ployed the MiVOLO (Multi-Input VOLO) model intro-
duced by Kuprashevich and Tolstykh (2023). This is a
transformer-based system designed to predict age and gen-
der from images, even when faces are partially or fully oc-
cluded, while excluding images without human subjects.
The results are shown in Figure 4, which shows the distri-
bution of estimated gender and age and the corresponding
NSFW browsing levels.
The gender and age estimation was performed on a
sampled subset of the original 40-million-image dataset.
Figure 2. Schematic overview of the CivitAI platform, showing layered relationships between the curated front-end images, the
underlying generative models, and the broader sociotechnical ecosystem. This includes tools, data sources, and cultural inﬂuences, that
shape model development.
4 Big Data & Society 13(3)

The subset consists of 40,636 images, representing approxi-
mately 0.1% of the full dataset. It was created through sam-
pling to ensure a temporally balanced and distributionally
representative sample. Using the MiVOLO classiﬁer, we
identiﬁed 29,073 human subjects in the 40,636 images, dis-
carding images with no human subjects or a low conﬁdence
level for gender classiﬁcation.
The results of gender classi ﬁcation indicate a stark
over-representation of female subjects, with an average
female-to-male ratio of 6.24 to 1 across the dataset.
NSFW co-occurrence rates were also notably higher for
female subjects, with 85.44%of images depicting women
having a browsing level other than 1, compared to male
subjects, where the NSFW incidence was 73.66%. The
average age for female subjects was 23.67 years, with a
standard deviation of 5.1, while male subjects had a
higher average age of 31.16 years with a standard devi-
ation of 9.09 years. This indicates a narrower age range
and a strong emphasis on sexualized portrayals of
younger women, in contrast to a broader age distribution
and more varied depictions of male individuals. A more
detailed overview of these results, including a monthly
breakdown of estimated gender and age distributions in
sampled images, proportions across NSFW browsing le-
vels, female-to-male ratios, and mean age statistics for
each group is given in Table S3 in the Supplemental
material.
Several limitations should be noted in this analysis:
CivitAI assigns browsing levels using Amazon
Rekognition, unspeciﬁed open-source NSFW classiﬁers,
and manual reviews. NSFW classiﬁers disproportionately
misclassify images of female subjects as explicit compared
to male subjects (Leu et al., 2024), potentially skewing
NSFW label distributions towards higher-sensitivity cat-
egories for females. Additionally, MiVOLO’s binary gen-
der classiﬁcation relies on visually inferred traits, ignoring
non-binary and gender-diverse identities, and may produce
uneven error rates, especially for darker-skinned indivi-
duals (Buolamwini and Gebru, 2018). Age estimation
models also introduce biases; for instance, digital ageism
can distort the representation of older adults, particularly
older women (Chu et al., 2022). While the classiﬁer ex-
cludes images without recognized human subjects and
we employed conservative thresholds to reject borderline
cases, AI-generated images often exhibit hybrid character-
istics that blend cartoonish and photorealistic elements. In
some cases, images with stylized or cartoonish features
m a yh a v eb e e nc l a s s iﬁed as depicting human subjects, po-
tentially introducing some distortion in the reported demo-
graphic distributions.
Figure 3. Monthly distribution of generated images categorized by the NSFW browsing level assigned by CivitAI.
Wagner and Cetinić 5

Model-level analysis: Themes and biases
While generated images often attract the most attention, it is
important to recognize that platforms like CivitAI primarily
function as model-sharing hubs. Of the 232,164 assets pub-
lished on CivitAI between November 2022 and January
2025, only 4.28% were standalone checkpoint models,
while 94.04% weremodel adapters, which require a com-
patible checkpoint to generate images. A breakdown of as-
set types appears in Figure S5 in the Supplemental material.
To examine the thematic focus of these models, we began
with an analysis of user-generated promotional tags. We
then evaluated gender bias reproduction by running infer-
ence tests on the 10 most popular checkpoint models.
Next, we examined thirty popular model adapters, such as
LoRA models, assessing their function in augmenting the
visual repertoire of base models. Within this group, we
identiﬁed a speciﬁc subset, referred to asdeepfake adapters,
which were designed to replicate particular individuals and
made up about 15% of all adapters.
Thematic overview of models shared on CivitAI.To understand
dominant thematic orientations, we collected promotional
tags added by model creators on CivitAI. These tags categor-
ize and describe thematic, esthetic, and functional attributes
of models and adapters during the publishing process. We
analyzed their frequency and co-occurrence across the plat-
form. Figure 5 (interactive version available
2 ) presents a co-
occurrence network of the 300 most common tags. Each
node represents a tag, with size indicating frequency.
Edges indicate co-occurrence, with thicker, darker lines re-
presenting stronger connections. To aid visual interpretation,
the size of nodes was normalized, and the top three most fre-
quent nodes display their absolute occurrence counts.
The most active cluster revolved around“character,” oc-
curring in 50.39% of models. This is followed by the tag
“anime,” appearing in 32.18% of models, indicating that an-
ime aesthetics is a prevalent theme on the platform.
Additionally, tags denoting female gender were highly
prevalent. The tag“woman” appeared in 29.2% of models,
“girls” in 15.7%, and“female” in 11.2%. While these tags
often co-occur in individual models, their high prevalence
indicates a pronounced emphasis on women and girls as de-
picted subjects across all models exchanged on the plat-
form. 20.97% of all models tagged “woman” were also
tagged “sexy,” while this term co-occurred in only 1.34%
of adapters tagged“man.”
Bias in model checkpoints.To visualize what embedded dis-
crimination in popular diffusion models means in terms of
Figure 4. Inferred age and gender predictions using MiVOLO on a 0.1% sample of temporally representative images from the 40
million image dataset.
6 Big Data & Society 13(3)

visual output, we performed an experiment on the top ten
most popular checkpoints ranked by download count.
Checkpoints are saved versions of a pretrained model, con-
taining all necessary parameters to perform inference tasks
without additional training and serving as the foundational
assets for image synthesis, whereas adapters such as LoRA
function as extensions merged into checkpoints to tweak
their generative capabilities. To assess gender bias in popu-
lar checkpoint models shared on CivitAI, we performed a
simple inference experiment based on comparing outputs
of two different neutral text prompts. We selected the ten
most popular checkpoint models according to download
count available on the platform as of January 19
th, 2025.
For instance, Realistic Vision, the most downloaded asset
at the time, had been downloaded over 1.5 million times, il-
lustrating the scale of model adoption and its potential im-
pact on generated content. We prompted each checkpoint
model separately with the single-word prompts“woman”
and “man”. Prompt embeddings were generated using the
standard CLIP text encoder expected by each checkpoint.
All images were generated using consistent parameters:
CFG scale 6.5, Euler sampler (Qi et al., 2024), and 15 infer-
ence steps. To ensure comparability across outputs, we
initialized the generation process with the same random
noise seed for each model. The selected checkpoints and
their inference results are visualized in Figure 6. For com-
parison, we also included results from Stable Diffusion
1.5 and Stable Diffusion XL 1.0, since most of the selected
checkpoints (aside from Pony Diffusion), are derivatives of
these models. The generated outputs across all models re-
vealed a stark difference in gender representation: women
were predominantly depicted nude, while men were fre-
quently portrayed in professional attire.
While the baseline models, Stable Diffusion 1.5 and
Stable Diffusion XL, still exhibit noticeable gender biases,
these biases are even more pronounced in the model deriva-
tives popular on CivitAI. It must be noted that our selection
of checkpoint models was based on platform popularity me-
trics without restricting for model generality or application
domain. As a result, the sample includes both general-
purpose models and specialized models (e.g.
anime-stylized, NSFW-oriented). This choice reﬂects the
actual diversity of models encountered by end-users on
CivitAI and allows us to capture platform-wide trends in
gender representation. However, it also introduces speciﬁc
variations that may intensify gender biases. Taken together,
Figure 5. Co-occurrence network of the 300 most frequent promotional tags across all assets shared on CivitAI with the top three
nodes indicating total occurrence rates and opacity and thickness intensity of co-occurrence rates.
Wagner and Cetinić 7

Figure 6. Top 10 most popular standalone models (type: checkpoint) as of 19th January 2025, prompted with the neutral terms
woman and man using identical parameters. Initial noise seeds were iterated to ensure a representative, uncurated sample.
Photorealistic and semi-realistic nudity was pixelized.
Figure 7. Top 30 most popular model adapters on CivitAI, including the number of downloads, adapter type, associated base model,
and user-assigned promotional tags. Textual Inversion was abbreviated with“TI.”
8 Big Data & Society 13(3)

these ﬁndings point toward embedded discrimination
within the platform’s model ecosystem, where user prefer-
ences, modelﬁne-tuning practices, and training data biases
converge to systematically reproduce and amplify narrow
and hypersexualized portrayals of women.
Most popular model adapters. The core aim of model per-
sonalization is to enable users to generate synthetic imagery
with a degree of speciﬁcity and control that general-purpose
models cannot achieve through prompting alone. This raises
an important question: what kinds of“personalized visual
worlds” are being created and shared in practice most com-
monly? To explore this, we examine the most popular model
adapters on CivitAI. As shown in Figure 7, we identiﬁed the
30 most downloaded adapters on January 19
th, along with
their promotional tags, the compatible base architecture
(base model), and download counts. A brief examination
of the promotional tags of the most popular models conﬁrms
the thematic orientation identiﬁed in our broader tag ana-
lysis, with frequent references to tags such as“anime,”“ fe-
male,” and “sexy,” suggesting a strong emphasis on
gendered and sexualized representations. Indeed, a closer
look at the 30 most downloaded adapters reveals a strong
presence of adapters implying pornographic themes. Many
of the promotional tags accompanying these models specif-
ically emphasize female subjects or body parts, with three
models focused solely on the depiction of vaginas.
Disconcertingly, one of the most popular adapters,Nudify
XL: Better Bodies, directly references the practice of non-
consensual “nudiﬁcation,” where photos of dressed indivi-
duals are manipulated to appear naked. Surprisingly, even
models focused on stylistic variation often include tags
like “female.” While CivitAI does not disclose how tags in-
ﬂuence visibility, it is likely that popular tags improve disco-
verability. This can create a feedback loop: widely used
terms like “female,”“ girl,” or “sexy” not only reﬂect user
interest but also shape platform norms, as creators adopt
them to boost exposure.
Deepfake adapters and targeted subjects. One of the most
ethically concerning applications of model personalization
is the creation of model adapters intended to replicate real
individuals. To better understand the scope and impact of
this phenomenon, we focused on analyzing the subset of
such adapters, investigating their prevalence, common use
cases, and the demographic characteristics of the indivi-
duals they target. According to a report by Ajder et al.
(2019), 96% of all deepfake content online was porno-
graphic, a trend that intensiﬁed by 2023 when a report by
Home Security Heroes found that 98% of deepfake videos
were pornographic and 99% of the victims were women
(Birrer and Just, 2025; Home Security Heroes, 2023).
Although CivitAI prohibits users from publicly sharing ex-
plicit content involving real people, it has no control over
how models are used once downloaded or what is shared
on external platforms. This creates a signiﬁcant blind spot
in the enforcement of ethical guidelines, as deepfake mod-
els can still be deployed in harmful ways beyond the plat-
form’s visibility. Given this regulatory gap and the
continuing risk of abuse, we sought to understand who is
being targeted by these models. To gain more insight into
the individuals currently targeted by the practice of non-
consensual deepfakes created from models shared on
CivitAI, we annotated our dataset of deepfake adapters
using large language models, similarly to the approach pio-
neered by Wei et al. (2024). This allowed us to identify the
most commonly associated professions and countries linked
to those individuals.
In our dataset of models and adapters, we found 15.27%,
33,804 model adapters were tagged“person of interest” as dis-
cussed in Section 2.3.4, which means that these were tailored
to replicate identiﬁable individuals. The individual’sn a m ei s
rarely included in the model tags and is typically indicated
in the model name. Toﬁ
nd more data on the individuals tar-
geted by deepfake models, we standardized modelﬁlenames
by converting obfuscated text into regular characters and re-
moving version numbers, emojis, and model-adapter-related
terms such as “LoRA” or “SD1.5.” We then used the
en_core_web_trfmodel (Explosion, 2021) from spaCy
3 (Montani and Honnibal, 2021) for named entity recognition
(NER) to extract cleaned names from the processedﬁlenames.
Subsequently, we queried three large language models to an-
notate each entry: Mistral-Small-Instruct−2409 (Mistral AI,
2024), Gemma−3−27b-it (Gemini Team et al., 2024), and
Qwen2.5−32B-Instruct (Yang et al., 2024). The prompt
was constructed from the NER-identiﬁed name and contextual
hints derived from the model’s promotional tags, such as“ja-
panese” or “supermodel,” instructing the LLM’s to provide
the full name of the targeted person, the country name they
are most associated with, their associated gender and up to
three different professions. To ensure conservative predic-
tions, the models were instructed to return“unknown” when-
ever uncertain and were conﬁgured with a temperature of 0.1
and top_p of 1.0 at inference.
We applied a multi-stageﬁlter. First, we kept annota-
tions only when at least two of the three models agreed
on the individual’s name and country, allowing for minor
variations such as name order. Second, we kept only entries
where all three models agreed on gender. We removed rows
that were uncertain, referred toﬁctional characters, or were
trained on multiple individuals, such as an adapter titled
“bond girls.” Finally, we merged all models linked to the
same person so each individual appeared only once. The re-
sulting dataset is shown in two bar charts in Figure 8 by pro-
fession and gender on the left and by profession and
associated country on the right.
Our results indicate that actors emerged as the most com-
mon profession for both genders. Among women, adult per-
formers were the second most frequent category, whereas
public ﬁgures ranked second among men.
Wagner and Cetinić 9

The majority of targeted individuals were associated
with countries in the Global North, speciﬁcally the United
States, the United Kingdom, and Japan. Cultural factors ap-
pear to inﬂuence who is targeted. For example, Japan
showed a notably high presence of voice actors compared
to other countries, likely reﬂecting the country’s strong an-
ime and gaming industries. Sports professionals were also
frequently identiﬁed, a pattern that may be attributed to
the increased media exposure surrounding international
events such as the 2024 Olympics.
This analysis offers insight into the cultural and profes-
sional context of deepfake victims but remains constrained
by methodological limits. Language models may misclas-
sify individuals by overlooking multiple roles and reducing
complex professional identities to a small set of predeﬁned
options. In addition, the experiment is inherently limited to
recognizing individuals with a public record excluding pri-
vate individuals, who can equally be targeted by deepfakes.
Even with these limitations, the results provide a structured
entry point for examining the social dynamics behind deep-
fake creation.
The creation of deepfake explicit images is an abuse that
highlights the risks of model personalization. Yet beyond
these malicious uses lies a systemic problem: the spread
of misogynistic and ethically troubling content through
model training and dissemination. These issues often arise
not from intent, but from seemingly neutral processes like
image-text pairing.
System-level analysis: Conﬁgurations and training
practices
Even when personalization workﬂows do not explicitly aim
to sexualize or objectify individuals, the training mechan-
isms themselves can introduce and reinforce such
representations.
Training LoRA adapters requires image–caption pairs.
Because manually writing captions is time-consuming,
auto-tagging models, which create text descriptions for
sets of images, are widely used. Although many TTI models
exist, only a few captioning models are commonly adopted.
One widely used system is CLIP Interrogator, which
generates captions by comparing image features with a
structured vocabulary through the CLIP model (Radford
et al., 2021). Its vocabulary is organized into categories
such as artists, mediums and art movements (pharmapsy-
chotic, 2022). It includes a few violence-related terms but
no explicit sexual terms.
The other major approach relies on Danbooru-based tag-
gers. Danbooru (2024) is an anime-focused imageboard
with a tag set that contains many sexually explicit terms
and comparatively few labels for domains such as nature
Figure 8. Bar charts depicting the distribution of identiﬁed 8,243 individuals targeted by deepfake models available on CivitAI,
categorized by LLM-predicted profession and gender (left), and associated country (right).
10 Big Data & Society 13(3)

or art history (Britt, 2019). Several tagging models have
been trained on this dataset, including DeepDanbooru
(Kim, 2024). Danbooru-based models are integrated into
popular LoRA training tools such as kohya-ss (bmaltais,
2025) and Stable Diffusion WebUI. In ComfyUI, users
can install extensions such as WD−14 Tagger (smiling-
wolf, 2022). Danbooru-based auto-captioning models typ-
ically produce short tag sequences such as 1girl, red
dress, white background, while CLIP Interrogator generates
full-sentence descriptions. These distinct patterns allow us
to determine which model was used. To categorize training
keywords and identify sensitive content, we created a struc-
tured taxonomy of Danbooru tags based on the public tag
groups on the site. The resulting hierarchy of 35,559 terms
appears in Figure S4 in the Supplemental material.
To examine auto-tagging practices on CivitAI, we ana-
lyzed the 40,000 most downloaded models. For about
11,000 models, we could identify the tagging system by
comparing metadata to the characteristic vocabularies and
structures of CLIP Interrogator and Danbooru-based mod-
els. If fewer than ﬁve matches were found or captions
were missing, the system was marked as unknown.
Only 14% of adapters matched CLIP Interrogator pat-
terns, while more than 70% matched Danbooru-based vo-
cabulary. Among those models representing real
individuals, 42.6% included Danbooru-derived tags.
Figure 9 illustrates the overall landscape, showing how
many of the 40,000 models are adapters, how many contain
extractable training text, and within that group, how many
include explicit or abusive tags.
Among models with extractable captions, about half
contained at least one tag mapped to the Danbooru sex
category. Roughly 5.6% included the keywords“loli” and
“shota,” which typically refer to sexualized depictions of
minors, and 2.1% included“rape.” These ﬁndings indicate
that captioning tools and training conﬁgurations have a sig-
niﬁcant inﬂuence on TTI personalization. They also show
how auto-tagging models embed norms from niche online
communities, normalizing sexualized depictions of minors
and reinforcing misogynistic tropes.
Sociotechnical implications and pathways
for intervention
The following discussion is organized around four principal
thematic domains identiﬁed through our analysis: content
degradation and platform decay driven by
engagement-oriented incentives; the ampliﬁcation of gen-
dered biases and misogyny in generative outputs; the prolif-
eration of non-consensual deepfakes enabled by accessible
tools; and potential avenues for intervention through tech-
nical, regulatory, and community-based approaches.
Commercialization and content degradation
What began as a promising creative breakthrough in TTI
generation and model personalization has, on platforms
like CivitAI, devolved into a pipeline for the large-scale
production of sensational, biased, and abusive content.
The open-source nature of TTI technologies, proclaimed
as a democratizing force in generative AI, has also enabled
the propagation of models that perpetuate hypersexualized
imagery and non-consensual deepfakes. This shift reﬂects
a broader structural trend described by the phenomenon
Figure 9. Subdivision of the 40,000 most downloaded CivitAI assets by type, presence of extractable training data, and occurrence of
problematic tags.
Wagner and Cetinić 11

of enshittiﬁcation, as coined by Doctorow (2025), also
known as platform decay. It describes the process by which
a platform originally offering value to its customers grows
increasingly exploitative under the imperative to recoup ini-
tial investments. While Doctorow’s framework centers on
venture-capital-driven commercialization, model-sharing
platforms like CivitAI present a distinct variant of these dy-
namics. The platform actively incentivizes sensational con-
tent through its reward economy: users can credit creators
with the platform ’s virtual currency ”Buzz” (CivitAI,
2025) and vote to feature models in online generators,
with creators receiving incentives for inclusion. This gami-
ﬁed system createsﬁnancial and reputational incentives that
favor engagement-maximizing content, which combined
with insufﬁcient moderation and network effects, drives tra-
jectories toward harmful content concentration. While some
of these aspects of Doctorow’s framework do apply, some
users may actively seek pornographic content, suggesting
the platform could be serving its intended audience that
wouldn’t deem the developments as degradation.
However, the platform’s mechanisms can be described as
exploitative in tolerating non-consensual deepfake content,
hosting models trained on pornographic content of dubious
origin and incentivizing the unauthorized usage of digital
artists’ work for model training (Gorwa and Veale, 2024).
Several indicators suggest a self-reinforcing feedback loop
accelerating these dynamics, including a dramatic increase
in NSFW imagery from 41% to 80% in two years, as well
as the community’s normalization of deepfakes, misogynis-
tic tropes, and other exploitative content as documented in
this study.
Platform toxicity often extends beyond internal dynam-
ics into broader social contexts (Trott et al., 2022). Social
media entities are explicitly marketed as platforms rather
than publishers, a distinction that suggests they are not
bound by the ethical responsibilities typically expected of
traditional publishers (Applebaum, 2024). For model-
sharing platforms, the consequences of this distinction
may be especially problematic, as the output of models
and model adapters, by design, can serve as means to gen-
erate and perpetuate content across the internet.
Open-source technologies frequently transition from col-
laborative, community-driven origins into proﬁt-oriented
ecosystems (Widder et al., 2023), a pattern TTI models
now follow. While these platforms exist within, and are
shaped by, broader cultural contexts that include pre-
existing patterns of discrimination and misogyny in online
spaces, the design choices and incentive structures of
model-sharing hubs can amplify these issues. As such, these
models and their distribution mechanisms bear partial re-
sponsibility for downstream harms, particularly when
biased, hypersexualized, or non-consensual content is
widely replicated and disseminated without meaningful
oversight or accountability. Beyond immediate harms to af-
fected individuals and communities, these issues risk
undermining trust in open-source AI development more
broadly, potentially inviting restrictive regulatory responses
that could stiﬂe innovation and limit the collaborative ethos
that has historically driven open-source progress. These dy-
namics have already begun to trigger external intervention,
as illustrated by the recent decision to restrict access to
CivitAI in the UK (Blocked.org.uk, 2025), underscoring
how unchecked platform practices can prompt regulatory
responses that impact the open-source TTI ecosystem.
Perpetual misogyny
According to Manne (2017), misogyny is not merely the
hatred of women or the ideological framing of women
and girls as inferior, which constitutes sexism. Rather, it
is performative: a hostile set of mechanisms and actions de-
signed to reinforce patriarchal power structures. The over-
sexualization and objectiﬁcation observed in our analysis
exemplify such mechanisms, as they perpetuate harmful
stereotypes and contribute to a culture that marginalizes wo-
men and may deter their participation on the platform.
Drawing on Mulvey ’s notion of the “male gaze ”
(Mulvey, 1989) and Berger ’s critique of Western art
(Berger, 1972), a recent article (King, 2024), elaborates
on how AI-generated imagery echoes the historical object-
iﬁcation, commodiﬁcation and hyper-sexualization of fe-
male bodies. Such visual compartmentalization of the
female body aligns with documented differences in cogni-
tive processing associated with objecti ﬁcation (Gervais
et al., 2012).
Our analysis of the most popular model adapters, indi-
cates the persistence of this trend in the context of genera-
tive AI personalization, where women are frequently
depicted through fragmented, sexualized representations
that emphasize speciﬁc body parts. The reduction of women
to isolated body parts through objectiﬁcation extends into
fantasies of replacement, where the human subject is erased
and substituted with artiﬁcial representations devoid of au-
tonomy or consent.
Erscoi et al. (2023) discuss how the concept of
Pygmalion Displacement, derived from the myth of the
Cypriot king who preferred the marble statue Galatea
over real women, remains a consistent trope in scienceﬁc-
tion as well as in recent technological advancements. The
sexual fantasy of the woman automaton, a machine created
for male sexual gratiﬁcation and/or menial tasks, continues
to shape representations of artiﬁcial femininity. Our study
indicates that in the context of generative AI, this fantasy
is not only perpetuated but also operationalized through
the personalization of models that allow users to generate
synthetic femaleﬁgures tailored to idealized and often hy-
persexualized speciﬁcations. While we lack comprehensive
demographic data on platform users and acknowledge that
individuals of any gender may generate objectifying con-
tent, the patterns we observe align with historically male-
12 Big Data & Society 13(3)

dominated fantasy tropes. These representations emerge
from a complex interplay of platform-driven incentive
structures and model-inherent biases, each reinforcing the
other. The underlying technology is trained on billions of
images, among them hundreds of thousands of women’s
bodies with partly questionable origin (Birhane et al.,
2021), and subsequently ﬁne-tuned with data often used
without the consent of the individuals represented. While
our analysis focuses on model outputs and platform dynam-
ics rather than user prompting behavior, the resulting con-
tent reﬂects a feedback loop where biased training data,
platform recommendation algorithms, and user engagement
patterns mutually amplify objectifying representations.
The proliferation of deepfakes
As problematic as objectiﬁcation and Pygmalion fantasies
may be, they differ fundamentally from the disruptive im-
pact that ultra-realistic deepfakes can exert on an indivi-
dual’s life. The consequences of sharing pornographic
deepfakes can, depending on the circumstances or cultural
context of the victim, range from a minor nuisance to sui-
cide (Gavrilovic Nilsson et al., 2019) or homicide, speciﬁc-
ally femicide (Ng, 2025). While this is tragic on an
individual level, the now readily available technology
may have detrimental effects on society as a whole. The
ability to manipulate someone’s likeness, face, and/or voice
is not only a severe violation of that individual’s dignity, it
undermines the foundational principles of liberal democra-
cies, including autonomy, consent, trust-based exchange
and the right to self-ownership. While platforms such as
CivitAI are not responsible for the mere existence of such
technologies, they actively normalize and even incentivize
their creation. In the case of CivitAI, this occurs through
a “celebrity-creator leaderboard.” This term is itself a mis-
nomer, as it extends to individuals without a signiﬁcant
public visual record, such as YouTubers, Instagrammers,
many of whom might not have theﬁnancial means to re-
move widespread AI-generated non-consensual pornog-
raphy from the internet. As we discussed in Section 2.4,
our survey of 221,304 CivitAI assets found that 15.27%
(33,804 model adapters) wereﬂagged as person of interest,
meaning they are tailored to replicate the likeness of real in-
dividuals. Since the initial version of this paper was written,
CivitAI has implemented a complete ban on deepfake con-
tent involving real individuals, following an update to its
platform policies (Maiberg, 2025a). Notably, the public an-
nouncement framed the decision primarily in terms of regu-
latory compliance rather than the recognition of underlying
ethical concerns. However, this policy change does not
retroactively eliminate models that were created, down-
loaded, and disseminated before the ban. Model adapters re-
leased prior to the policy change may still remain stored
locally on users’ machines, be shared through private chan-
nels, or be redistributed across alternative platforms beyond
CivitAI’s control. Recent investigations suggest that ap-
proximately 5,000 deepfake models were migrated to
Hugging Face following the CivitAI ban (Maiberg,
2025b). While Hugging Face maintains an Acceptable
Use Policy that prohibits content enabling harassment, sex-
ual exploitation, or the creation of non-consensual sexual
material involving real individuals (Hugging Face, 2025),
enforcement necessarily relies on reporting mechanisms
and moderation at scale. In practice, this allows such mod-
els to persist in obscured or fragmented forms, illustrating
how policy enforcement varies across platforms and how
harmful artifacts can migrate rather than disappear.
This redistribution underscores the complexity of the
model-sharing ecosystem. Even after formal prohibition
on CivitAI, the affordances of open model distribution en-
able pre-existing deepfake models to persist, migrate to
other platforms, and continue generating harmful content.
The persistence of these models underscores the path-
dependent effects of early platform governance choices,
as artifacts released into open ecosystems cannot be fully re-
called even when platforms later implement more restrictive
policies.
Pathways to harm mitigation
In line with constructivist perspectives on technology
(Hayles, 2025), we argue that technological development,
including generative AI, is not determined but contingent,
and as such, subject to complex sociotechnical dynamics.
All technology is shaped by the value systems from which
it emerges, stakeholder decisions, and underlying power
structures (O’Connor and Liu, 2024). In a recent article,
(Morton, 2025) builds on Bruno Latour’s Actor-Network
Theory (Latour, 1986) to conceptualizeinscription as the
encoding of designers’ and users’ values into technology,
extending the concept to TTI models, to show how datasets,
design choices, and platform practices become embedded in
these models and shape both their outputs and the visual
norms they reproduce. While Morton primarily focuses on
foundational TTI models, extending this framework to
TTI personalization introduces additional layers of inscrip-
tion into an already complex system. Besides the initial
biases inscribed into problematic foundational datasets, in
the model personalization process the tools employed in da-
taset creation, such as auto-tagging systems, also function
as inscriptions, along with users’ preferred topics andﬁne-
tuning choices, and the platform settings where models are
eventually shared, such as the prioritization of sensational
content. Each layer may reinforce values and biases intro-
duced at earlier stages, producing cumulative effects that
diffuse responsibility and make resulting harms difﬁcult
to identify, isolate, and address through single-point tech-
nical or policy interventions. In this sense, model-sharing
platforms not only extend technical limitations but also ex-
pose deeper societal pathologies, confronting us with visual
Wagner and Cetinić 13

symptoms of racism, ageism, misogyny, and dehumaniza-
tion, which may prompt critical reﬂection on the structural
conditions that sustain these harms. At the same time, rec-
ognizing these outputs as symptoms of deeper systemic is-
sues does not lessen the need for concrete safeguards at the
platform level to mitigate immediate harms.
Effective safety interventions require rigorous evaluation
using diverse datasets that capture the full spectrum of po-
tential harms (Bavalatti et al., 2025), as well as innovative
responses from platform operators that can repurpose exist-
ing technical infrastructure toward protective ends.
Notably, the same tools that contribute to bias inscription
can be adapted for harm prevention. For instance, Haidra
(2024), a decentralized compute provider, developed a
safety mechanism that makes use of DeepDanbooru ’s
knowledge of problematic concepts to block abusive image
generations on their hardware (tazlin, 2023). This demon-
strates how the auto-tagging system discussed in Section
2.4 can be repurposed as a detection mechanism for content
moderation.
Despite such innovative solutions, some issues require
more immediate and explicit policy interventions, espe-
cially the growing threat of deepfakes. For example, al-
though the model-sharing platform Hugging Face restricts
the sharing of models mimicking real individuals’ like-
nesses unless explicit consent is provided (Hugging Face,
2025), recent reporting suggests that deepfake models can
nonetheless be found on the platform. It also remains un-
clear to what extent these policies are proactively enforced,
or whether moderation primarily relies on user reporting.
Even when model-sharing platforms implement policies,
signiﬁcant harm may already have spread beyond their con-
trol. Individuals affected by digital violence require both
retroactive and preventative support. StopNCII (2024) of-
fers preventative tools that allow individuals to hash non-
consensual intimate imagery (NCII) so partnering online
content and social media platforms can then use these
hashes to detect and block such content. Amiinporn
(2025) by the NGO digital dignity, supports victims by
helping detect and remove existing non-consensual content
on sites that provide database access. Additionally,
FaceSafe (2025), represents a proactive approach aimed at
preventing deepfakes and identity theft. Once launched,
this subscription-based service will allow individuals to re-
gistinmer a vector derived from extracted facial features in
order to be notiﬁed if their likeness appears on any partici-
pating platform.
In addition, these issues are being tackled on the techno-
logical level through the development of various protective
techniques designed to prevent misuse or reproduction of
sensitive content. Image perturbation methods such as
Glaze (Shan et al., 2025), Nightshade (Shan et al., 2024),
Mist (Liang and Wu, 2023), and MetaCloak (Liu et al.,
2024a) aim to protect images from unauthorized use in
model training. However, as Zhao et al. (2024) note, these
protective methods exist in a constant arms race with model
development, as newer architectures andﬁne-tuning techni-
ques continuously evolve to overcome existing defenses.
While such methods could be integrated into social media
platforms as optional uploadﬁlters, their effectiveness ul-
timately depends on the willingness of platforms to priori-
tize user protection over engagement, a commitment that
is currently lacking (Li et al., 2024).
Conclusion
Patterns of structural discrimination inadvertently intro-
duced into large-scale foundation TTI models are likely to
become overshadowed by the biased models and adapters
deliberately infused into the digital ecosystem through
open-source model-sharing platforms and their users. As
shown in this study, on model-sharing platforms like
CivitAI biases, particularly those reinforcing hypersexuali-
zation and gendered objectiﬁcation, are ampliﬁed and nor-
malized. The rapid rise of NSFW content, the
over-representation of young female subjects, and the pri-
oritization of sensational content re ﬂect an exploitative
and potentially harmful dynamic. Additionally, structural
discrimination embedded in today’s open-source TTI tools
and models has the potential to cause signiﬁcant down-
stream harm as they might become widely adopted and
even integrated into future consumer applications. Even
more alarming is the normalization and incentivization of
deepfake model adapters, which fundamentally violate indi-
vidual dignity, autonomy, and the core democratic princi-
ples of self-ownership and consent. While these general
remarks emerge from our study, which focuses on a single
platform, we acknowledge that platform-speci ﬁc design
choices and community norms may limit the generalizabil-
ity of these observations. Although our study represents one
of theﬁrst attempts to analyze model personalization prac-
tices in detail, it is limited by its focus on a single platform.
Consequently, our observations should be interpreted as in-
dicative of emerging dynamics rather than as universal
claims about all model-sharing ecosystems. Additionally,
our analysis does not cover all relevant aspects, and the
technological landscape is evolving rapidly. Future research
could examine prompting behavior in more detail and ex-
tend this framework of analysis to emerging text-to-video
models, where the risks of ultra-realistic non-consensual
deepfakes and other problematic content may intensify.
Even though our observations are necessarily partial and
platform-speciﬁc, they nonetheless indicate broader struc-
tural dynamics whose continuation or redirection depends
on how online communities, platform operators, law-
makers, and society, choose to intervene. Model-sharing
and social media platforms both have the capacity to imple-
ment safeguards that can limit the spread of abusive prac-
tices such as deepfake creation and abusive imagery.
Strengthening responsible moderation, supporting ethical
14 Big Data & Society 13(3)

model development, introducing technical safeguards, and
collaborating with NGOs focused on preventing digital vio-
lence, are necessary steps to adjust the current trajectory.
Rather than reacting after harm has occurred, all stake-
holders have the opportunity to innovate proactively and
to collectively shape the future direction of model sharing
and personalization ecosystems.
Acknowledgments
The authors thank Amanda Wasielewski, Tristan Weddigen,
Maria-Teresa de Rosa Palmini, Tania de León Yong for their help-
ful comments and suggestions. They are also thankful to Jonas
Schnabel and Yannick Schuchmann of digital dignity e.V. for their
valuable insights and comments. They are particularly grateful to
Lasse Scherfﬁg and Thomas Hawranke for their guidance in shap-
ing the initial proposal for this study.
ORCID iDs
Laura Wagner https://orcid.org/0009-0003-4244-6342
Eva Cetinić https://orcid.org/0000-0002-5330-1259
Ethical approval and informed consent statements
This study did not involve human participants or identiﬁable per-
sonal data, and therefore did not require ethical approval or in-
formed consent.
Author contributions
Laura Wagner was responsible for developing the main idea, con-
ceptualizing the study, conducting the exploratory analysis, visu-
alizing the results, and writing the manuscript. Eva Cetinic
contributed to the methodological design, assisted with data inter-
pretation, and provided critical revisions to the manuscript. Both
authors reviewed and approved theﬁnal version.
Funding
The authors disclosed receipt of the followingﬁnancial support for
the research, authorship, and/or publication of this article: This
work was supported by Swiss National Science Foundation
(Ambizione Grant 216104).
Declaration of conﬂicting interests
The authors declare no potential conﬂicts of interest with respect to
the research, authorship, and/or publication of this article.
Code availability
The code to reproduce the results in this paper is available at
Wagner and Cetinic (2025c). The image metadata dataset
(40,630,560 images) and model metadata dataset (231,252 mod-
els) are available upon request at Wagner and Cetinic (2025a)
and Wagner and Cetinic (2025b), respectively.
Supplemental material
Supplemental material for this article is available online.
Notes
1. We use the termswomen and girls to denote individuals who
are perceived or depicted as female, because the harms exam-
ined here are disproportionately directed at such bodies. We
recognize gender diversity and use this terminology for analyt-
ical speciﬁcity rather than to exclude other identities.
2. An interactive version of this graph is available here: https://
pm-paper-b68c5e.pages.uzh.ch/ﬁgure_5.html
References
Ajder H, Patrini G, Cavalli F, et al. (2019)The state of deepfakes:
Landscape, threats, and impact . Deeptrace. Available at:
https://regmedia.co.uk/2019/10/08/deepfake_report.pdf (ac-
cessed: 2 May 2025).
AlDahoul N, Rahwan T and Zaki Y (2025) AI-generated faces in-
ﬂuence gender stereotypes and racial homogenization.
Scientiﬁc Reports15(1): 14449.
Amiinporn (2025) Amiinporn. Available at: https://amiinporn.io/
(accessed: 20 April 2025).
Applebaum A (2024) Don’t Fight the Information War,
Undermine It. Chapter Epilogue. Random House.
Automatic1111 (2022)Stable diffusion web UI. GitHub. Available
at: https://github.com/AUTOMATIC1111/stable-diffusion-
webui (accessed: 6 September 2024).
Bavalatti T, Ahmed O, Potdar D, et al. (2025) A systematic review
of open datasets used in text-to-image (T2I) gen AI model
safety. IEEE access 13: 32661 –32680. DOI: 10.1109/
ACCESS.2025.3539933
Berger J (1972)Ways of Seeing. London, England: Penguin Books
Limited.
Birhane A, Prabhu V, Han S, et al. (2023) Into the LAIONs den:
Investigating hate in multimodal datasets. In:Proceedings of
the 37th conference on neural information processing systems
(NeurIPS 2023), datasets and benchmarks track . DOI:
10.52202/075280-0930.
Birhane A, Prabhu VU and Kahembwe E (2021) Multimodal da-
tasets: Misogyny, pornography, and malignant stereotypes.
DOI: 10.48550/arXiv.2110.01963.
Birrer A and Just N (2025) What we know and don’t know about
deepfakes: An investigation into the state of the research and
regulatory landscape. New Media & Society 27(12): 6819–
6838. DOI: 10.1177/14614448241253138.
Blockedorguk (2025) Online safety act — Shutdowns and site
blocks (entry: civitai.com— Access restricted for UK visitors).
CivitAI entry lists UK access restriction and dates. Available
at: https://www.blocked.org.uk/osa-blocks (Reported: 24 July
2025; Shut down: 25 July 2025) (accessed: 21 December).
Bmaltais (2025) bmaltais/kohya_ss. GitHub. Available at: https://
github.com/bmaltais/kohya_ss (accessed: 14 January 2025).
Britt BC (2019) Content curation, evaluation, and reﬁnement on a
nonlinearly directed imageboard: Lessons from danbooru.
Social Media+ Society 5(4): 2056305119880020.
Buolamwini J and Gebru T (2018) Gender shades: Intersectional ac-
curacy disparities in commercial gender classi ﬁcation. In:
Wagner and Cetinić 15

Friedler SA and Wilson C (eds.)Proceedings of the 1st confer-
ence on fairness, accountability and transparency, Proceedings
of Machine Learning Research, Vol. 81, pp.77–91. PMLR.
Buschek C and Thorp J (2025) Models all the way down. Knowing
Machines. Available at: https://knowingmachines.org/models-
all-the-way (accessed: 1 January 2025).
by321 (2022) by321/safetensors_util. GitHub. Available at: https://
github.com/by321/safetensors_util (accessed: 26 July 2024).
Chu C, Nyrup R, Leslie K, et al. (2022) Digital ageism: Challenges
and opportunities in artiﬁcial intelligence for older adults.The
Gerontologist 62. DOI: 10.1093/geront/gnab167
CivitAI (2023) REST API reference. GitHub. Available at: https://
github.com/civitai/civitai/wiki/REST-API-Reference (ac-
cessed: 14 January 2025).
CivitAI (2024) Civitai. Available at: https://civitai.com/ (accessed:
11 November 2024).
CivitAI (2025) Civitai’s guide to on-site currency: Buzz. Available
at: https://education.civitai.com/civitais-guide-to-on-site-
currency-buzz- (accessed: 8 November 2025).
Comfyanonymous (2023) comfyanonymous/ComfyUI. GitHub.
Available at: https://github.com/comfyanonymous/ComfyUI
(accessed: 6 September 2024).
Cui J and Araujo DA (2024) Rethinking use-restricted open-
source licenses for regulating abuse of generative models.
Big Data & Society11(1). DOI: 10.1177/20539517241229699
Danbooru (2024) Danbooru. Available at: https://danbooru.
donmai.us/ (accessed: 11 November 2024).
Doctorow C (2025)Platform decay: The enshittiﬁcation of every-
thing. Die ZeitAvailable at: https://www.zeit.de/digital/internet/
2025-04/platform-decay-enshittiﬁcation-cory-doctorow-facebook-
internet/seite-2 (accessed 27 April 2025).
Erscoi L, Kleinherenbrink A and Guest O (2023) Pygmalion dis-
placement: When humanising AI dehumanises women.
SocArXiv. DOI: 10.31235/osf.io/jqxb6.
Explosion (2021) en_core_web_trf: Spacy’s transformer-based
english nlp pipeline. SpaCy. Available at: https://spacy.io/
models/en#en_core_web_trf (accessed 2 May 2025).
FaceSafe (2025) Facesafe. Available at: https://facesafe.io/ (ac-
cessed 20 April 2025).
Gal R, Alaluf Y, Atzmon Y, et al. (2023) An image is worth one
word: Personalizing text-to-image generation using textual in-
version. In: Proceedings of the 11th international conference
on learning representations (ICLR 2023). Kigali, Rwanda.
DOI: 10.48550/arXiv.2208.01618.
Gavrilovic Nilsson M, Tzani-Pepelasis C, Ioannou M, et al. (2019)
Understanding the link between sextortion and suicide.
International Journal of Cyber Criminology13(1): 55–69.
Gervais SJ, Vescio TK, Förster J, et al. (2012) Seeing women as
objects: The sexual body part recognition bias. European
Journal of Social Psychology42(6): 743–753.
Ghosh S and Caliskan A (2023)’person’ == light-skinned, western
man, and sexualization of women of color: Stereotypes in stable
diffusion. In: Findings of the Association for Computational
Linguistics: EMNLP 2023, December 6–10, 2023. pp.6971–
6985. DOI: 10.18653/v1/2023.ﬁndings-emnlp.465.
Gorwa R and Veale M (2024) Moderating model marketplaces:
Platform governance puzzles for AI intermediaries. Law,
Innovation and Technology16(2): 341
–391.
Haidra (2024) Haidra. Available at: https://haidra.net/ (accessed:
11 November 2024).
Hawkins W, Mittelstadt B and Russell C (2025) Deepfakes on de-
mand: The rise of accessible non-consensual deepfake image
generators. In: Proceedings of the 2025 ACM conference on
fairness, accountability, and transparency (FAccT), pp.1602–
1614. ACM. DOI: 10.1145/3715275.3732107.
Hayles NK (2025) Bacteria to AI: Human Futures With Our
Nonhuman Symbionts. London, UK: University of Chicago
Press.
Home Security Heroes (2023)2023 state of deepfakes: Realities,
threats, and impact. Home Security Heroes. Available at:
https://www.homesecurityheroes.com/state-of-deepfakes/ (ac-
cessed 30 April 2025).
Hu EJ, Shen Y, Wallis P, et al. (2022) LoRA: Low-rank adaptation
of large language models. DOI: 10.48550/arXiv.2106.09685.
Hugging Face (2025) Content policy— Hugging Face. Hugging
Face. Available at: https://huggingface.co/content-guidelines
(accessed: 13 January 2025).
Kannen N, Ahmad A, Andreetto M, et al. (2024) Beyond aesthet-
ics: Cultural competence in text-to-image models. In:Advances
in neural information processing systems , Vol. 37. DOI:
10.48550/arXiv.2407.06863.
Kim K (2024)KichangKim/DeepDanbooru. GitHub. Available at:
https://github.com/KichangKim/DeepDanbooru (accessed 26
July 2024).
King D (2024)The algorithmic gaze: Representations of women in
AI art. Le random. Available at: https://www.lerandom.art/
editorial/the-algorithmic-gaze-representations-of-women-in-
ai-art (accessed 10 January 2025).
Kuprashevich M and Tolstykh I (2023) Mivolo: Multi-input trans-
former for age and gender estimation. In:Analysis of Images,
Social Networks and Texts , Lecture Notes in Computer
Science, Vol. 14447, pp.212 –226. Springer Nature
Switzerland. DOI: 10.1007/978-3-031-54534-4_15.
Latour B (1986) Visualization and cognition: Thinking with eyes
and hands.Knowledge and Society6: 1–40.
Leu W, Nakashima Y and Garcia N (2024) Auditing image-based
NSFW classiﬁers for contentﬁltering. In:The 2024 ACM con-
ference on fairness, accountability, and transparency ,
pp.1163–1173. ACM. DOI: 10.1145/3630106.3658963.
Li Q, Zhang S, Kasper AT, et al. (2024) Reporting non-consensual
intimate media: An audit study of deepfakes. DOI: 10.48550/
arXiv.2409.12138.
Liang C and Wu X (2023) Mist: Towards improved adversarial ex-
amples for diffusion models. DOI: 10.48550/arXiv.2305.12683.
Liu Y, Fan C, Dai Y, et al. (2024a) Metacloak: Preventing un-
authorized subject-driven text-to-image diffusion-based syn-
thesis via meta-learning. In:Proceedings of the 2024 IEEE/
CVF conference on computer vision and pattern recognition
(CVPR), pp.24219 –24228. IEEE. DOI: 10.1109/
CVPR52733.2024.02286.
16 Big Data & Society 13(3)

Liu Z, Schaldenbrand P, Okogwu BC, et al. (2024b) SCoFT:
Self-contrastive ﬁne-tuning for equitable image generation.
In: Proceedings of the IEEE/CVF conference on computer vi-
sion and pattern recognition (CVPR) , pp.10822 –10832.
IEEE. DOI: 10.1109/CVPR52733.2024.01029.
Maiberg E (2023)Inside the AI porn marketplace where every-
thing and everyone is for sale . 404 Media. Available at:
https://www.404media.co/insi de-the-ai-porn-marketplace-
where-everything-and- everyone-is-for-sale/ (accessed: 2
January 2025).
Maiberg E (2024)a16z funded AI platform generated images that
“could be categorized as child pornography,” leaked docu-
ments show. 404 Media. Available at: https://www.404media.
co/a16z-funded-ai-platform-generated-images-that-could-be-
categorized-as-child-pornography-leaked-documents-show/
(accessed: 29 January 2024).
Maiberg E (2025a)Civitai ban of real people content deals major
blow to the nonconsensual ai porn ecosystem. 404 Media re-
porting on CivitAI’s ban on real-person-likeness AI models.
Available at: https://www.404media.co/civitai-ban-of-real-
people-content-deals-major-blow-to-the-nonconsensual-ai-
porn-ecosystem/ (accessed: 21 December 2025).
Maiberg E (2025b)Hugging face is hosting 5,000 nonconsensual
ai models of real people. 404 Media article documenting re-
upload of deepfake models from CivitAI to Hugging Face.
Available at: https://www.404media.co/hugging-face-is-
hosting-5-000-nonconsensual-ai-models-of-real-people/ (ac-
cessed: 21 December 2025).
Manne K (2017) Ameliorating Misogyny. Chapter 2. Oxford
University Press.
Mistral AI (2024) Mistral-small-instruct-2409. Hugging Face.
Available at: https://huggingface.co/mistralai/Mistral-Small-
Instruct-2409 (accessed 10 December 2024).
Montani I and Honnibal M (2021)spacy 3: Industrial-strength
natural language processing in Python. SpaCy. Available at:
https://spacy.io (accessed: 2 May 2025).
Morton JL (2025) On inscription and bias: Data, actor network
theory, and the social problems of text-to-image ai models.
AI and Ethics5: 775–790.
Motion Picture Association (2023)Film ratings. Motion Picture
Association. Available at: https://www.motionpictures.org/
ﬁlm-ratings/ (accessed: 14 January 2025).
Mulvey L (1989)Visual Pleasure and Narrative Cinema. Chapter
3. London: Palgrave Macmillan UK.
Naik R and Nushi B (2023) Social biases through the
text-to-image generation lens. In: Proceedings of the 2023
AAAI/ACM conference on AI, Ethics, and Society (AIES) ,
pp.786–808. ACM. DOI: 10.1145/3600211.3604711.
Ng K (2025)Pakistan: US teen shot dead by father over TikTok
videos. BBC News. Available at: https://www.bbc.com/news/
articles/cy8pvw3xxxeo (accessed: 27 April 2025).
O’Connor S and Liu H (2024) Gender bias perpetuation and miti-
gation in AI technologies: Challenges and opportunities.AI &
Society 39: 2045–2057.
OpenAI (2021) Dall.e: Creating images from text . OpenAI.
Available at: https://openai.com/index/dall-e/ (accessed: 14
July 2024).
Oppenlaender J (2022) The creativity of text-to-image generation. In:
Proceedings of the 25th international academic mindtrek confer-
ence.p p . 1 9 2–202. DOI: 10.1145/3569219.3569352.
Palmini MTDR, Wagner L and Cetinic E (2024) Civiverse: A dataset
for analyzing user engagement with open-source text-to-image
models. arXiv DOI: 10.48550/arXiv.2408.15261.
Pharmapsychotic (2022) pharmapsychotic/clip-interrogator.
GitHub. Available at: https://github.com/pharmapsychotic/
clip-interrogator (accessed: 28 January 2025).
Qi Z, Bai L, Xiong H, et al. (2024) Not all noises are created
equally: Diffusion noise selection and optimization. DOI:
10.48550/arXiv.2407.14041.
Radford A, Kim JW, Hallacy C, et al. (2021) Learning transferable
visual models from natural language supervision. In:
Proceedings of the 38th international conference on machine
learning, Proceedings of Machine Learning Research, Vol.
139, pp.8748–8763. PMLR.
Rombach R, Blattmann A, Lorenz D, et al. (2022) High-resolution
image synthesis with latent diffusion models. In:Proceedings
of the IEEE/CVF conference on Computer Vision and
Pattern Recognition (CVPR) . pp.10684 –10695. DOI:
10.1109/CVPR52688.2022.01042.
Schneider M and Hagendorff T (2025) Investigating toxicity and
bias in stable diffusion text-to-image models. Scientiﬁc
Reports 15(1): 31401.
Shan S, Cryan J, Wenger E, et al. (2025) Glaze: Protecting artists
from style mimicry by text-to-image models. DOI: 10.48550/
arXiv.2302.04222.
Shan S, Ding W, Passananti J, et al. (2024) Nightshade:
Prompt-speciﬁc poisoning attacks on text-to-image generative
models. DOI: 10.48550/arXiv.2310.13828.
Shi C, Li S, Guo S, et al. (2025) Where culture fades: Revealing
the cultural gap in text-to-image generation. DOI: 10.48550/
arXiv.2511.17282.
Sim M, Brigham NG, Kohno T, et al. (2025) Biased AI outputs can im-
pact humans’ implicit bias: A case study of the impact of gender-
biased text-to-image generators.Proceedings of the AAAI/ACM
Conference on AI, Ethics, and Society8(3): 2375–2386.
Smilingwolf (2022) SmilingWolf/wd-v1-4-vit-tagger at main .
Hugging Face. Available at: https://huggingface.co/
SmilingWolf/wd-v1-4-vit-tagger (accessed: 29 July 2024).
StopNCII (2024) Stopncii. Available at: https://stopncii.org/ (ac-
cessed: 10 November 2024).
Suﬁan A, Distante C, Leo M, et al. (2025) T2ibias: Uncovering so-
cietal bias encoded in the latent space of text-to-image genera-
tive models. DOI: 10.48550/arXiv.2511.10089.
tazlin (2023)Haidra-org/horde-safety. Haidra. Available at: https://
github.com/Haidra-Org/horde-safety (accessed: 28 April 2025).
Team Gemini Anil R, S Borgeaud, et al. (2024) Gemini: A family
of highly capable multimodal models. DOI: 10.48550/
arXiv.2312.11805.
Wagner and Cetinić 17

Thiel D, Stroebel M and Portnoff R (2023)Identifying and elimin-
ating CSAM in generative ML training data and models .
Technical Report kh752sm9123. Stanford Internet
Observatory and Thorn. Available at: https://purl.stanford.
edu/kh752sm9123 (accessed: 6 September 2024).
Trott V, Beckett J and Paech V (2022) Operationalising‘toxicity’
in the manosphere: Automation, platform governance and com-
munity health.Convergence 28(6): 1754–1769.
UN Women (2024) THE DARK SIDE OF DIGITALIZATION:
Technology-facilitated violence against women in Eastern
Europe and Central Asia. UN Women. Available at: https://
eca.unwomen.org/sites/default/ﬁles/2024-01/research-tf-vaw_
full-report_24-january2.pdf (accessed: 2 January 2025).
Viola M and Voto C (2023) Designed to abuse? Deepfakes and the
non-consensual diffusion of intimate images.Synthese201(1): 30.
Wagner L and Cetinic E (2025a) latentcanon/civ-40m. DOI:
10.57967/hf/9053. Hugging Face. (accessed: 5 June 2025).
Wagner L and Cetinic E (2025b) latentcanon/civ-models. DOI:
10.57967/hf/9049. Hugging Face. (accessed: 5 June 2025).
Wagner L and Cetinic E (2025c) latentcanon/code. DOI:
10.57967/hf/9052. Hugging Face. (accessed: 5 June 2025).
Wang W, Bai H, Huang J, et al. (2024) New job, new gender?
Measuring the social bias in image generation models. In:
Proceedings of the 32nd ACM international conference on
multimedia, MM 2024, Melbourne, VIC, Australia, 28
October–1 November 2024 , pp.3781 –3789. ACM. DOI:
10.1145/3664647.3681433.
Wei Y, Zhu Y, Hui P, et al. (2024) Exploring the use of abusive
generative ai models on civitai. In:Proceedings of the 32nd
ACM international conference on multimedia (MM 2024) ,
pp.6949–6958. ACM. DOI: 10.1145/3664647.3681052.
Widder DG, West S and Whittaker M (2023) Open (for business):
Big tech, concentrated power, and the political economy of
OpenAI. SSRN Electronic Journal. DOI: 10.2139/ssrn.4543807.
Wu Y, Nakashima Y and Garcia N (2024) Stable diffusion exposed:
Gender bias from prompt to image. In:Proceedings of the Seventh
AAAI/ACM conference on AI, Ethics, and Society (AIES) ,
pp.1648–1659. AAAI Press. DOI: 10.1609/aies.v7i1.31754.
Wu Y, Nakashima Y and Garcia N (2025) Revealing gender bias
from prompt to image in stable diffusion.Electronics11(3): 379.
Yang A, Yang B, Hui B, et al. et al (2024) Qwen2 technical report.
DOI: 10.48550/arXiv.2407.10671.
Zhang L, Liao X, Yang Z, et al. (2024) Partiality and misconception:
Investigating cultural representativeness in text-to-image models.
In: Proceedings of the CHI conference on human factors in com-
puting systems, CHI 2024, Honolulu, HI, USA, 11–16 May 2024,
pp.620:1–620:25. ACM. DOI: 10.1145/3613904.3642877.
Zhao Z, Duan J, Xu K, et al. (2024) Can protective perturbation
safeguard personal data from being exploited by stable diffu-
sion? DOI: 10.48550/arXiv.2312.00084.
18 Big Data & Society 13(3)
```
