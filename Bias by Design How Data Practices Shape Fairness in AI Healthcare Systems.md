---
title: Bias by Design? How Data Practices Shape Fairness in AI Healthcare Systems
author: Anna Arias-Duart, Maria Eugenia Cardello, Atia Cortés
year: "2025"
Type: Preprint
DOI: 10.48550/arXiv.2510.20332
source: https://arxiv.org/abs/2510.20332
created: 2026-05-05
description: Artificial intelligence (AI) holds great promise for transforming healthcare. However, despite significant advances, the integration of AI solutions into real-world clinical practice remains limited. A major barrier is the quality and fairness of training data, which is often compromised by biased data collection practices. This paper draws on insights from the AI4HealthyAging project, part of Spa
tags:
  - op/acc/pending-review
  - themes/ethics
pdfORepub: "[[Bias by Design How Data Practices Shape Fairness in AI Healthcare Systems.pdf]]"
---
[[Bias by Design How Data Practices Shape Fairness in AI Healthcare Systems.pdf]]

> **Abstract:** Artificial intelligence (AI) holds great promise for transforming healthcare. However, despite significant advances, the integration of AI solutions into real-world clinical practice remains limited. A major barrier is the quality and fairness of training data, which is often compromised by biased data collection practices. This paper draws on insights from the AI4HealthyAging project, part of Spa

## Full text (extracted from `Bias by Design How Data Practices Shape Fairness in AI Healthcare Systems.pdf`)

*Source:* `2PDF/Bias by Design How Data Practices Shape Fairness in AI Healthcare Systems.pdf`  
*Extracted:* 2026-05-05

```text
BIAS BYDESIGN? HOWDATAPRACTICESSHAPEFAIRNESS IN
AI HEALTHCARESYSTEMS
Anna Arias-Duart
Orcid ID: 0000-0002-8819-6735
Barcelona Supercomputing Center (BSC)
anna.ariasduart@bsc.es
Maria Eugenia Cardello
Orcid ID: 0009-0004-6467-4511
Barcelona Supercomputing Center (BSC)
maria.cardello@bsc.es
Atia Cortés
Orcid ID: 0000-0002-4394-439X
Barcelona Supercomputing Center (BSC)
atia.cortes@bsc.es
October 24, 2025
ABSTRACT
Artificial intelligence (AI) holds great promise for transforming healthcare. However, despite
significant advances, the integration of AI solutions into real-world clinical practice remains limited.
A major barrier is the quality and fairness of training data, which is often compromised by biased
data collection practices. This paper draws on insights from the AI4HealthyAging project, part of
Spain’s national R&D initiative, where our task was to detect biases during clinical data collection.
We identify several types of bias across multiple use cases, including historical, representation,
and measurement biases. These biases manifest in variables such as sex, gender, age, habitat,
socioeconomic status, equipment, and labeling. We conclude with practical recommendations for
improving the fairness and robustness of clinical problem design and data collection. We hope that
our findings and experience contribute to guiding future projects in the development of fairer AI
systems in healthcare.
KeywordsArtificial intelligence·biases·healthcare·data collection·
1 Introduction
The application of artificial intelligence (AI) in healthcare has grown rapidly in recent years, offering new possibilities
for medical tasks such as diagnosis and clinical decision-making [1, 2, 3]. Among the most transformative developments
are the adoption of machine learning (ML), deep learning (DL) with the recent emergence of generative AI marking a
significant new frontier. However, only a small fraction of these AI solutions are ultimately integrated into real-world
healthcare systems [4]. This limited adoption can be attributed to different factors, including a mismatch with practical
clinical needs or non-compliance with the European Union’s AI Act [5], which emphasizes transparency, safety, and
accountability in AI systems.
As a result, many hospitals are increasingly investing in the development of smaller, in-house models tailored to their
specific clinical needs. However, training such models remains a significant challenge. Medical data is highly sensitive
and typically subject to strict GDPR regulations [ 6], which limit access and use. Moreover, it is particularly hard
to collect data, in terms of the time required to pass through the evaluation of protocols by ethical committees, the
constraints of inclusion / exclusion criteria and the difficulty to find enough population aiming to participate into the
study. Even so, the amount of collected data will often not be enough to train AI models. It does not get better with
publicly available datasets, which often lack essential metadata, undermining both the generalizability and clinical
relevance of trained models [7].
arXiv:2510.20332v1  [cs.AI]  23 Oct 2025
APREPRINT- OCTOBER24, 2025
Consequently, the successful implementation of in-house AI solutions often depends not on model architecture or
performance metrics, but on a more fundamental, and frequently overlooked, factor:how data collection for model
training is defined and planned. The success, reliability, and safety of AI systems in healthcare are deeply rooted in
the quality, structure, and contextual appropriateness of the data on which they are built.
This paper draws on lessons learned from AI4HealthyAging, a national AI research project under Spain’s 2021 “R&D
Missions in Artificial Intelligence” Program, focused on developing AI solutions for age-related diseases. The project
addressed a range of clinical use cases, including cardiovascular conditions, sarcopenia, sleep disorders, Parkinson’s
disease, mental health, colorectal and prostate cancer, and hearing loss. Our work centered on identifying bias in
data through stakeholder interviews and limited metadata analysis. Based on these insights, we present a set of
recommendations to guide data planning and collection in clinical AI projects, aiming to improve fairness, quality, and
reliability.
Before presenting the specific biases identified in our study, we begin in Section 2 by examining how bias is defined in
the existing literature. Section 3 explores how bias has been categorized in previous work. In Section 4, we present the
biases we identified, already categorized. Finally, Section 5 offers a set of recommendations, measures that could have
mitigated the biases observed and which we hope will support future clinical data collection efforts in AI development.
2 Bias definition
Despite its widespread use, the term bias lacks a standardized definition in the AI field. Different subfields and
applications interpret and operationalize bias in different ways depending on their specific context [8, 9, 10, 11, 12].
However, definitions across the literature tend to converge around three core elements: the source of the bias (e.g.,
algorithms, systems, or errors), how the bias manifests (e.g.,through discrimination, unequal impacts, or prediction
errors), and the entities affected by the bias (e.g.,individuals, patients, or underrepresented groups). Table 1 presents
a selection of definitions from the literature, spanning general AI to healthcare-specific contexts, organized and
color-coded according to these three analytical dimensions.
These definitions of bias imply a normative judgment: that the outcomes it produces are undesirable, unjust, or
detrimental to certain individuals or groups. This aligns closely with the concept of health equity, which is defined as the
absence of systematic disparities in health (or in the major social determinants of health) between groups with different
levels of underlying social advantage/disadvantage—that is, wealth, power, or prestige[13]. Understanding bias in AI
as a normative issue highlights that biased outcomes are more than technical errors; they can reinforce social inequities,
particularly in healthcare. Addressing bias is needed to achieving health equity by preventing unfair disparities.
Table 1: Different definitions of bias and algorithmic bias in AI, ranging from general to healthcare-specific contexts.
Highlights indicate the source of bias (green), how it manifests (purple), and the affected groups or outcomes (yellow).
Context Term Definition
General Algorithmic
bias
It occurs when the outputs of an algorithm benefit or disadvantage certain individuals or
groups more than others without a justified reason for such unequal impacts [8].
General Bias It refers to systematic and unfair favoritism or prejudice in AI systems, which can lead to
discriminatory outcomes [9].
Health Algorithmic
bias
The instances when the application of an algorithm compounds existing inequities in socioe-
conomic status, race, ethnic background, religion, gender, disability or sexual orientation to
amplify them and adversely impact inequities in health systems [11].
Health Bias It refers to systematic errors leading to a distance between prediction and truth, to the
potential detriment of all or some patients [10].
3 Bias categorization
Many studies in the literature have proposed different categorizations of the sources of bias in AI systems [10, 14, 15, 16,
17, 18, 19, 20, 21, 22]. While terminology may vary across articles, most reflect a general consensus around three stages
in the AI development pipeline where biases can originate: data, model development, and system implementation. Some
works also propose additional stages that are also crucial to identify possible biases:(i)an initial stage to formulate of
the research problem, where the purpose, requirements and impact need to be evaluated [10, 19, 20, 21, 22], and(ii)a
2
APREPRINT- OCTOBER24, 2025
final phase of monitoring after deployment, which should be maintained as long as the AI system is in use [ 19, 21].
Table 2 illustrates this alignment by mapping the terminology used in nine different papers to these five stages.
Table 2: Comparison of sources of bias with the AI/ML system life cycle.
Design Data Modeling Deployment - [10]
- Data Generation Model Building Implementation - [14]
- Data Algorithm User Interaction - [15]
- Training Data /
Publication
Model
Development &
Evaluation
Model
Implementation - [16]
- Pre-processing In-processing Post-processing - [17]
Conception &
Design Development Validation Access Monitoring [19]
Formulating
Research
Problem
Data Collection &
Pre-processing
Model
Development &
Validation
Model
Implementation - [20]
Conception Data Collection &
Pre-processing In-processing Post-processing Post-deployment
Surveillance [21]
Problem scope Data used Model building
Decisions
supported by
analytical tool
- [22]
Although there is a broad agreement on the stages at which biases are introduced, the types of biases identified within
these stages vary in both nomenclature and granularity across sources. Some categories are broad, such asselection bias
[17], while others are more fine-grained, likevalidity of the research question[ 10]. Certain labels serve as umbrella
terms, for examplerepresentation bias[ 14], under which more specific biases fall. For instance,demographic bias
[10] can be considered a subcategory of representation bias. Furthermore, there is often overlap between categories, as
certain biases span multiple dimensions. For example,institutional bias[ 10] can be understood as a combination of
historical bias[ 14], which reflects systemic inequalities, andaggregation bias[ 10], where institutional practices rely
on generalized data that may overlook the specific needs of marginalized groups.
4 Bias in Practice
In this section, we highlight several biases identified in our work that may affect the performance and generalizability of
AI models. These biases arise from the first two steps detailed in the previous section: data design and data collection.
To make these issues more tangible, we present concrete examples illustrating how such biases can be inadvertently
introduced into training data, potentially compromising model fairness and validity.
For clarity, we categorize these biases according to the three sources of harm in data generation proposed by Suresh and
Guttag [14]: historical bias, representation bias, and measurement bias (see Table 3). As noted earlier, these categories
are not mutually exclusive. For example, we classify gender bias as historical bias due to its roots in societal norms
and systemic inequalities. However, it could also be considered a form of measurement bias if gender is inferred using
subjective scoring methods, as the methodology itself can introduce additional bias.
Sex bias.In the Parkinson’s study, the distribution of participants by age group and sex was generally balanced,
except in the 40–49 and 80–89 age groups. The notably lower representation of females in the 80–89 group may be
due to higher female mortality rates, which make recruiting females in this age range more difficult. These sex-based
differences in participant distribution reflect important biological and disease-related factors. For example, research by
Cerri et al. [23] shows that males have about twice the risk of developing Parkinson’s disease compared to females,
yet females tend to experience faster disease progression and higher mortality. Such sex differences in disease risk,
progression, and survival underscore the importance of carefully considering sex as a key variable to avoid bias in data
collection and analysis, ensuring predictive models accurately capture these nuances.
3
APREPRINT- OCTOBER24, 2025
Table 3: Identified biases categorized according to the classification proposed by Suresh and Guttag [14]. Each bias
listed is clickable and links to a detailed explanation in the text.
Problem Design and Data Collection
Historical Biases Representation Biases Measurement Biases
Sex Age Equipment
Gender Habitat Labeling
Socioeconomic
Gender bias.Although gender information was not directly available in the data we analyzed, a Gender Score could
be derived as in [24]. Gender bias is particularly important to consider in healthcare contexts. For instance, Samulowitz
et al. [25] demonstrated that gender norms influence pain treatment: women with pain received less effective relief,
fewer opioid prescriptions, more antidepressants, and more mental health referrals compared to men. Neglecting gender
data and its proper analysis can exacerbate existing inequalities and lead to biased health outcomes.
Age bias.Because the project focuses on age-related conditions, the control group, composed of participants without
the disease, tent to be younger on average, while the disease groups include older individuals. This difference arises
because these diseases primarily affect older adults, making it easier to recruit younger healthy controls but harder to
find older participants without the condition.
Another example of age bias is found in the Parkinson’s study, where the majority of subjects were between 60 and 79
years old. This aligns well with the known prevalence of Parkinson’s, which affects approximately 3% of people at
age 65 and up to 5% of those over 85 [26]. Additionally, the median age increased with disease severity, 64 years for
severity 1, 71.5 years for severity 2, and 75 years for severity 3, with no participants younger than 60 in the most severe
category. This further reflects the strong association between age and disease progression. However, such uneven age
distributions can introduce age bias in AI models trained on this data. Hence, models may learn to associate age-related
features with disease presence or severity rather than true disease-specific markers.
Habitat bias.This bias arises when geographic or environmental context affects participant representation. In this
project, most participants came from urban areas, largely because the hospitals conducting the studies were located
in urban settings. Travel distance and accessibility can be significant barriers for individuals living in rural areas,
making it less likely for them to participate or remain involved in long-term studies. Even in urban areas, usually
hospitals concentrate patients from some specific regions of the city that are determined by socio-economic factors or
environmental exposure that have an impact on their quality of life [27], which leads to the following type of bias.
Socioeconomic bias.It occurs when participants’ social and economic factors, such as income, education, occupation,
or access to healthcare, influence who is included in a study. For example, in one of the studies, data was collected
from a private hospital. Because private hospitals typically serve patients with higher income levels or better insurance
coverage, this creates a socioeconomic bias by primarily including individuals from wealthier backgrounds.
In the hearing loss study, control group participants tended to have higher education levels than other groups. Education
often correlates with quieter work environments, while lower education may correspond to noisier jobs (e.g., factory
work). Ignoring these factors could lead to misleading conclusions about hearing loss causes.
Equipment bias.It occurs when variations in the devices used for data collection, such as different models, calibration
settings, or software, affect measurement consistency. This can lead to results that are not comparable across participants
or sites. For example, in the hearing loss study, most participants had cochlear implants from the same manufacturer.
As a result, findings on quality of life and cognitive improvement may not generalize to users of other implant types,
potentially biasing the model toward the characteristics of one specific device.
Labeling bias.This bias occurs when data labels, such as diagnoses or classifications, are influenced by human
judgment or local context. This can occur when different people use inconsistent criteria, or even when the same
team labels all data but follows specific institutional practices. For example, labels from one hospital with its unique
diagnostic style may not generalize well elsewhere, reducing model accuracy and fairness in real-world settings.
4
APREPRINT- OCTOBER24, 2025
An example of labeling bias was found in the hearing loss study, specifically in the classification of participants’
occupations. Initially, the dataset used standardized occupational categories1 that did not include a significant group of
society: homemakers. After adding this category, it was revealed that 35% of women fell into this group, with no male
representation. This initial omission and subsequent reclassification demonstrate how labeling categories influenced by
human decisions can misrepresent certain groups.
Intersectional bias.It occurs when two or more demographic variables interact in a way that affects the fairness or
validity of a model. In the Alzheimer’s study, a potential intersectional bias involving age and sex was observed across
three diagnostic groups: control, mild cognitive impairment (MCI), and Alzheimer’s. On average, female were younger
than male across all groups: the age difference is two years in both the control and Alzheimer’s groups, and four years
in the MCI group. If the interaction between age and sex is not properly controlled, models may misattribute these
normative age-related sex differences to disease-specific changes, compromising the validity and fairness of diagnostic
predictions.
5 Recommendations
In this section, we present recommendations for mitigating bias in medical data collection. We organize them using the
same three categories as before: historical, representation, and measurement biases. These categories are not strictly
separated, some recommendations may address multiple types of bias.
Historical bias.
• Involve a diverse,interdisciplinary groupin planning the experiment. Collection design may be influenced
by the implicit biases of those responsible for data collection. As research has consistently shown, healthcare
providers often exhibit biases toward historically excluded groups [28, 29, 30], and these biases are likely to
persist in the absence of curricula specifically focused on minority health [31]. Furthermore, stakeholders hold
divergent views on the nature, significance, and mitigation of bias in healthcare AI [32]. As such, assembling a
diverse and interdisciplinary team is important to incorporate multiple perspectives, minimize bias, and ensure
that data collection strategies are equitable and inclusive.
• Ensure that data is collected in anaggregated or disaggregatedmanner when appropriate. As Cirillo et
al. [33] explain, bias can be desirable or undesirable. Including sex and gender, for example, may improve
prediction accuracy in cardiovascular diseases [ 34], but may also reinforce harmful assumptions, such as
higher reported depression rates among women [35]. It is therefore essential to review existing literature and
carefully plan what metadata to collect and use, to avoid unintended harm.
Representation bias.
• Define clear and balancedinclusion and exclusion criteria. Criteria should be specific but not overly
restrictive, to maintain sample diversity and enable the formation of appropriate control groups. In this project,
the study population was older, which made it challenging to find age-matched control groups for those with
the comorbidity. As a result, the control groups had lower mean values, potentially introducing spurious
correlations and biasing the results.
• Analyse the need to include anintersectional benchmarkto better represent the targeted population [ 36].
This will help refining the evaluation metrics and understand the health condition.
• Ensure thesample sizeis feasible and sustainable. This involves assessing recruitment and retention potential
within time and resources constraints. Engage experts with experience in similar studies to identify potential
challenges, such as high dropout rates or participant burden. For instance, in this study, some protocols had to
be shortened, as their extended duration was too demanding for participants.
Equipment bias.
• Evaluate thedata labelingprocess. Review how data has been labeled to ensure that categories are clear
and consistent. Well-defined labeling reduces ambiguity, improves data quality becoming an essential step to
align with FAIR principles [37]. Depending on the type of data, labeling should be approached differently, for
example, socioeconomic variables may benefit from input by an interdisciplinary team, while clinical related
data should not be labeled by a single professional alone, in order to minimize personal bias.
1https://www.ine.es/dyngs/INEbase/operacion.htm?c=Estadistica_C&cid=1254736177033&menu=enlaces&
idp=1254735976614
5
APREPRINT- OCTOBER24, 2025
• Considerequipmentand deployment context. It is important to account for the equipment used during data
collection and where the model will ultimately be deployed. If both data collection and deployment occur
within the same hospital using the same equipment, consistency is maintained. However, if a model is trained
on data from one type of equipment and then applied to data form another, equipment-related bias may arise.
This can compromise the model’s performance and limit its generalizability.
6 Conclusions
To successfully incoporate AI systems into healthcare, clinical AI projects must address bias not only as a technical
issue but also as a matter of governance. Our work highlights how different forms of bias can emerge during data
collection, illustrated with real cases from our project. We provide a list of recommendations to avoid these biases
and emphasize the importance of interdisciplinary collaboration, balanced cohort design, and thoughtful inclusion of
metadata. We hope that these lessons learned from our experience will inform and support future healthcare AI projets
in building more equitable and effective systems that are both legally compliant and socially responsible.
Acknowledgments
We would like to thank all the collaborators involved in the project who participated in the interviews, and Amparo
Callejón-Leblic for her insightful feedback. This research has been funded by the Artificial Intelligence for Healthy
Aging (AI4HA, MIA.2021.M02.0007.E03) project from the Programa Misiones de I+D en Inteligencia Artificial
2021 and by the European Union-NextGenerationEU, Ministry of Universities and Recovery, Transformation and
Resilience Plan, through a call from Universitat Politècnica de Catalunya and Barcelona Supercomputing Center (Grant
Ref. 2021UPC-MS-67461/2021BSC-MS-67461). Anna Arias Duart acknowledges her AI4S fellowship within the
“Generación D” initiative by Red.es, Ministerio para la Transformación Digital y de la Función Pública, for talent
attraction (C005/24-ED CV1), funded by NextGenerationEU through PRTR. Additional funding from the European
Union through the Marie Skłodowska-Curie project AHEAD (grant agreement No 101183031). We would also like to
thank Nardine Osman and Mark d’Inverno for Figure 2 in their work [38], which inspired our Table 1.
Declaration on Generative AI
During the preparation of this work, the authors used ChatGPT (GPT-4) and DeepSeek Chat for grammar and spelling
checks. After using these tools, the authors reviewed and edited the content as needed and take full responsibility for
the publication’s content.
References
[1] Malek Elhaddad and Sara Hamam. AI-driven clinical decision support systems: an ongoing pursuit of potential.
Cureus, 16(4), 2024.
[2] Stefan Busnatu, Adelina Gabriela Niculescu, Alexandra Bolocan, George ED Petrescu, Dan Nicolae P˘aduraru,
Iulian N˘astas˘a, Mircea Lupus, oru, Marius Geant˘a, Octavian Andronic, Alexandru Mihai Grumezescu, et al. Clinical
applications of artificial intelligence—an updated overview.Journal of clinical medicine, 11(8):2265, 2022.
[3] Gokul Krishnan, Shiana Singh, Monika Pathania, Siddharth Gosavi, Shuchi Abhishek, Ashwin Parchani, and
Minakshi Dhar. Artificial intelligence in clinical medicine: catalyzing a sustainable global healthcare paradigm.
Frontiers in artificial intelligence, 6:1227091, 2023.
[4] Julia Gong, RM Currano, David Sirkin, Serena Yeung, and F Christopher Holsinger. Nice: Four human-centered
ai principles for bridging the ai-to-clinic translational gap. InACM CHI 2021, page 7. 2021.
[5] Council of Europe (EU). Regulation (eu) 2024/1689 (artificial intelligence act), 2024.
[6] European Parliament and Council of the European Union. Regulation (EU) 2016/679 of the European Parliament
and of the Council, 2016.
[7] Roxana Daneshjou, Mary P Smith, Mary D Sun, Veronica Rotemberg, and James Zou. Lack of transparency
and potential bias in artificial intelligence data sets and algorithms: a scoping review.JAMA dermatology,
157(11):1362–1369, 2021.
[8] Nima Kordzadeh and Maryam Ghasemaghaei. Algorithmic bias: review, synthesis, and future research directions.
European Journal of Information Systems, 31(3):388–409, 2022.
6
APREPRINT- OCTOBER24, 2025
[9] Matthew G Hanna, Liron Pantanowitz, Brian Jackson, Octavia Palmer, Shyam Visweswaran, Joshua Pantanowitz,
Mustafa Deebajah, and Hooman H Rashidi. Ethical and bias considerations in artificial intelligence/machine
learning.Modern Pathology, 38(3):100686, 2025.
[10] Burak Koçak, Andrea Ponsiglione, Arnaldo Stanzione, Christian Bluethgen, João Santinha, Lorenzo Ugga, Merel
Huisman, Michail E Klontzas, Roberto Cannella, and Renato Cuocolo. Bias in artificial intelligence for medical
imaging: fundamentals, detection, avoidance, mitigation, challenges, ethics, and prospects.Diagnostic and
interventional radiology, 31(2):75, 2025.
[11] Trishan Panch, Heather Mattie, and Rifat Atun. Artificial intelligence and algorithmic bias: implications for health
systems.Journal of global health, 9(2):020318, 2019.
[12] Alexandra Olteanu, Carlos Castillo, Fernando Diaz, and Emre Kıcıman. Social data: Biases, methodological
pitfalls, and ethical boundaries.Frontiers in big data, 2:13, 2019.
[13] Paula Braveman and Sofia Gruskin. Defining equity in health.Journal of Epidemiology & Community Health,
57(4):254–258, 2003.
[14] Harini Suresh and John Guttag. A framework for understanding sources of harm throughout the machine learning
life cycle. InProceedings of the 1st ACM Conference on Equity and Access in Algorithms, Mechanisms, and
Optimization, pages 1–9, 2021.
[15] Ninareh Mehrabi, Fred Morstatter, Nripsuta Saxena, Kristina Lerman, and Aram Galstyan. A survey on bias and
fairness in machine learning.ACM computing surveys (CSUR), 54(6):1–35, 2021.
[16] James L Cross, Michael A Choma, and John A Onofrey. Bias in medical ai: Implications for clinical decision-
making.PLOS Digital Health, 3(11):e0000651, 2024.
[17] Sribala Vidyadhari Chinta, Zichong Wang, Xingyu Zhang, Thang Doan Viet, Ayesha Kashif, Monique Antoinette
Smith, and Wenbin Zhang. Ai-driven healthcare: A survey on ensuring fairness and mitigating bias.arXiv preprint
arXiv:2407.19655, 2024.
[18] Reva Schwartz, Reva Schwartz, Apostol Vassilev, Kristen Greene, Lori Perine, Andrew Burt, and Patrick Hall.
Towards a standard for identifying and managing bias in artificial intelligence, volume 3. US Department of
Commerce, National Institute of Standards and Technology . . . , 2022.
[19] Michael D Abràmoff, Michelle E Tarver, Nilsa Loyo-Berrios, Sylvia Trujillo, Danton Char, Ziad Obermeyer,
Malvina B Eydelman, Foundational Principles of Ophthalmic Imaging, DC Algorithmic Interpretation Working
Group of the Collaborative Community for Ophthalmic Imaging Foundation, Washington, and William H Maisel.
Considerations for addressing bias in artificial intelligence for health equity.NPJ digital medicine, 6(1):170, 2023.
[20] Lama H Nazer, Razan Zatarah, Shai Waldrip, Janny Xue Chen Ke, Mira Moukheiber, Ashish K Khanna, Rachel S
Hicklen, Lama Moukheiber, Dana Moukheiber, Haobo Ma, et al. Bias in artificial intelligence algorithms and
recommendations for mitigation.PLOS digital health, 2(6):e0000278, 2023.
[21] Fereshteh Hasanzadeh, Colin B Josephson, Gabriella Waters, Demilade Adedinsewo, Zahra Azizi, and James A
White. Bias recognition and mitigation strategies in artificial intelligence healthcare applications.NPJ Digital
Medicine, 8(1):154, 2025.
[22] R. Agarwal, M. Bjarnadottir, L. Rhue, M. Dugas, K. Crowley, J. Clark, and G. Gao. Addressing algorithmic
bias and the perpetuation of health inequities: An ai bias aware framework.Health Policy and Technology,
12(1):100702, 2023.
[23] S Cerri, L Mus, and F Blandini. Parkinson’s disease in women and men: what’s the difference? j parkinsons dis 9
(3): 501–515, 2019.
[24] Jing Yuan, Shuping Sang, Jessica Pham, and Wei-Jia Kong. Gender modifies the association of cognition with
age-related hearing impairment in the health and retirement study.Frontiers in Public Health, 9:751828, 2021.
[25] Anke Samulowitz, Ida Gremyr, Erik Eriksson, and Gunnel Hensing. “brave men” and “emotional women”: A
theory-guided literature review on gender bias in health care and gendered norms towards patients with chronic
pain.Pain research and management, 2018(1):6358624, 2018.
[26] David T Dexter and Peter Jenner. Parkinson disease: from pathology to molecular disease mechanisms.Free
Radical Biology and Medicine, 62:132–144, 2013.
[27] Cláudia Jardim Santos, Inês Paciência, and Ana Isabel Ribeiro. Neighbourhood socioeconomic processes and
dynamics and healthy ageing: A scoping review.International Journal of Environmental Research and Public
Health, 19(11), 2022.
[28] Chloë FitzGerald and Samia Hurst. Implicit bias in healthcare professionals: a systematic review.BMC medical
ethics, 18:1–18, 2017.
7
APREPRINT- OCTOBER24, 2025
[29] Ivy W Maina, Tanisha D Belton, Sara Ginzberg, Ajit Singh, and Tiffani J Johnson. A decade of studying
implicit racial/ethnic bias in healthcare providers using the implicit association test.Social science & medicine,
199:219–229, 2018.
[30] Janice A Sabin, Rachel G Riskind, and Brian A Nosek. Health care providers’ implicit and explicit attitudes
toward lesbian women and gay men.American journal of public health, 105(9):1831–1841, 2015.
[31] Sean M Phelan, Sara Emily Burke, Brooke A Cunningham, Sylvia P Perry, Rachel R Hardeman, John F Dovidio,
Jeph Herrin, Liselotte N Dyrbye, Richard O White, Mark W Yeazel, et al. The effects of racism in medical
education on students’ decisions to practice in underserved or minority communities.Academic Medicine,
94(8):1178–1189, 2019.
[32] Yves Saint James Aquino, Stacy M Carter, Nehmat Houssami, Annette Braunack-Mayer, Khin Than Win, Chris
Degeling, Lei Wang, and Wendy A Rogers. Practical, epistemic and normative implications of algorithmic bias in
healthcare artificial intelligence: a qualitative study of multidisciplinary expert perspectives.Journal of Medical
Ethics, 51(6):420–428, 2025.
[33] Davide Cirillo, Silvina Catuara-Solarz, Czuee Morey, Emre Guney, Laia Subirats, Simona Mellino, Annalisa
Gigante, Alfonso Valencia, María José Rementeria, Antonella Santuccione Chadha, et al. Sex and gender
differences and biases in artificial intelligence for biomedicine and healthcare.NPJ digital medicine, 3(1):81,
2020.
[34] Sanket S Dhruva, Lisa A Bero, and Rita F Redberg. Gender bias in studies for food and drug administration
premarket approval of cardiovascular devices.Circulation: Cardiovascular Quality and Outcomes, 4(2):165–171,
2011.
[35] Lisa A Martin, Harold W Neighbors, and Derek M Griffith. The experience of symptoms of depression in men vs
women: analysis of the national comorbidity survey replication.JAMA psychiatry, 70(10), 2013.
[36] Joy Buolamwini and Timnit Gebru. Gender shades: Intersectional accuracy disparities in commercial gender
classification. In Sorelle A. Friedler and Christo Wilson, editors,Proceedings of the 1st Conference on Fairness,
Accountability and Transparency, volume 81 ofProceedings of Machine Learning Research, pages 77–91. PMLR,
23–24 Feb 2018.
[37] Mark Wilkinson, Michel Dumontier, IJsbrand Jan Aalbersberg, Gaby Appleton, Myles Axton, Arie Baak, Niklas
Blomberg, Jan-Willem Boiten, Luiz Olavo Bonino da Silva Santos, Philip Bourne, Jildau Bouwman, Anthony
Brookes, Tim Clark, Merce Crosas, Ingrid Dillo, Olivier Dumon, Scott Edmunds, Chris Evelo, Richard Finkers,
and Barend Mons. The fair guiding principles for scientific data management and stewardship.Scientific Data, 3,
03 2016.
[38] Nardine Osman and Mark d’Inverno. Modelling human values for ai reasoning.arXiv preprint arXiv:2402.06359,
2024.
8
```
