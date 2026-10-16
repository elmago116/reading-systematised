---
title: "Online Dispute Resolution: Ethics and Governance"
author:
  - John Zeleznikow
source: https://ceur-ws.org/Vol-3531/SPaper_12.pdf
venue: AIGEL 2022
type: Proceedings Article
created: 2025-02-17
tags:
  - themes/bias
  - tech/Ai
  - themes/ethics
pdfORepub: "[[Online Dispute Resolution - Ethics and Governance.pdf]]"
modified: 2026-09-08
---

# Notes

## Full text (extracted from `2PDF/Online Dispute Resolution - Ethics and Governance.pdf`)

*Extracted:* 2026-09-17

```text
Online Dispute Resolution: Ethics and Governance
John Zelenikow1,2
1Research Unit of Excellence Digital Society: Security and Protection of Rights, University of Granada, Spain
2Law and Technology Group, Law School, La Trobe University, Australia
Abstract
In this article we survey the history of Intelligent Online Dispute Resolution Systems. This leads to the
development of a six-step module for building systems that can be used by non-professionals. The use of
Machine Learning to build such systems, and underlying ethics and governance problems are discussed.
Keywords
Online Dispute Resolution, Artificial Intelligence, Machine Learning, Ethics, Governance
1. Introduction
Use only styles embedded in the document. For paragraph, use Normal. Paragraph text.
Paragraph text. Paragraph text. Paragraph text. Paragraph text. Paragraph text. Paragraph text.
Paragraph text.
The pioneers of ODR, saw it as a futuristic idea that could cope with ecommerce disputes [1].
Despite a number of research papers being produced, very few practical systems were widely
used prior to 2010. Only recently have legal communities recognised the benefits of ODR for
helping resolve far more than ecommerce disputes.
Amongst the reasons for using both ADR and ODR are:
1. The time taken to reach judgements in trials;
2. The cost of resorting to traditional legal recourse – especially litigation;
3. ADR and ODR focus upon providing users with the outcomes they desire rather than
seeking judicially far outcomes; and
4. ODR can be particularly efficient for low-cost high volume transactional disputesAn
example of bulleted list is as following.
The 1970s were the decade where ADR gained traction, The Pound Conference of April 9-11
1976 was organised by then US Supreme Court Chief Justice Warren Burger to investigate
developing alternative forms of justice. Chief amongst the ideas presented were Frank Sander’s
notion of the Multidoor Courthouse [2]. Resulting from Pound Conference was the Harvard
Program on Negotiation and the publication of Fisher and Ury’s ‘Getting to Yes’ book [3] and
Howard Raiffa’s ‘the Art and Science of Negotiation’ [4].
Proceedings of Artificial Intelligence Governance Ethics and Law (AIGEL), Reviewed, Selected Papers. November 02 -
December 19, 2022, Barcelona, Spain
Envelope-Open john.zeleznikow@vu.edu.au (J. Zelenikow)
Orcid 0000-0002-8786-2644 (J. Zelenikow)
© 2022 Copyright for this paper by its authors. Use permitted under Creative Commons License Attribution 4.0 International (CC BY 4.0).
CEUR
Workshop
Proceedings
http://ceur-ws.org
ISSN 1613-0073
CEUR Workshop Proceedings (CEUR-WS.org)
150


John Zelenikow CEUR Workshop Proceedings 150–160
The 1980s saw the development of what was the considered a number of futuristic expert
systems which could model legalistic decision making. Such systems included TAXMAN
(McCarty 1976) [5]. The British Nationality Act as a Logic Program [6] and the Latent Damage
Adviser [7].
It was not until the early 1990s that we saw and extensive development of the World Wide
Web. Initial proposals for the development of ODR followed soon thereafter. Initially ODR
developer focussed upon the resolution of E-Commerce disputes. They argued that disputes
which originated online could be resolved digitally and that Ecommerce users would not face
difficulties using Information Technology. Thus, in the decade following 2000, we saw the
development of ODR for E-Commerce.
The 2010s have been the first decade in which we have seen the development of practical
widely usable systems. Examples include Rechtwijzer (Netherlands) and British Columbia Civil
Resolution Tribunal. The use of ODR has now moved far beyond Ecommerce. It is finally
being used for non-financial disputes. Examples include the work of Ethan Katsh and Orna
Rabinovich-Einy [8] and the access to justice work being performed at Kent Law School.
2. The Importance of User Centric Computing for ODR
Over the past thirty years there has been a growing trend for disputants to engage in legal
conflict without professional support [9]. Disputants who represent themselves rather than
use lawyers are known as Self-Represented Litigants (SRLs). Many SRLs use ODR for debt,
employment, and family relationships conflicts without seeking professional help. Zeleznikow
argues that ODR can help SRLs [10].
However, if non-professional SRLs hope to use ODR, then associated software must be user
friendly. Human-centered design focuses on users’ experiences to develop solutions that are
both experimental and iterative.
Margaret Hagan identifies seven key recommendations for courts and Self-Help Centers to
improve efficiency and usability [11]:
1. Courts must coordinate Navigable Pathways which help people understand the whole
sequence of events that will face them during their legal processes and more effectively
assist them through that process.
2. People need more robust and user-friendly tools to navigate through the courts.
3. Peopleneedwarmandefficientwelcomeexperiencestoencouragethemtofollowthrough
with the procedures.
4. Paperwork should be redesigned to be more visually clear, prioritized, and manageable.
5. Pre-court appearances - the development of more online court tools that can help people
prep for their court visits and get their tasks done correctly.
6. Better work-stations and materials in courts to prepare litigants for their appearances.
7. The court system needs to develop a culture of usability, testing, and feedback.
Richard Susskind discusses two tiers of online courts [12]:
151

John Zelenikow CEUR Workshop Proceedings 150–160
• The first tier uses rule-based and case-based systems —such as Rechtwijzer and the
British Columbia Civil Resolution Tribunal, and compliance systems (such as Robodebt
and driving regulations). Such systems are now routinely used and whilst they use the
first generation of AI, they are often not viewed as AI
• In the second tier, Susskind imagines a machine learning system helping parties
by predicting the likely outcome of their case were it to come before a human
judge –oneexampleisourSplit-Upsystem(seelater)whichadvisesuponthedistribution
of marital property following divorce in Australia, by providing appropriate BATNAs.
Roberge and Fraser [13] argue that an optimal ODR platform, from a commercial standpoint,
will provide guides and flowcharts, an adaptive question and answer interface, transparent
ethical commitments, outcome predictions, an expedited procedure leading to an enforceable
outcome, a proportional cost model, a mediation process, and a range of communications.
3. Machine Learning and Legal Data
Paragraph text. Rajkomar et al. argue that a central challenge in building a machine-learning
modelisassemblingarepresentative, diversedataset[14]. Legaldataisnotaspreciseasmedical
data, and often needs to be transformed so that it can be gainfully used.
Stevens classified data into nominal, ordinal, interval, and ratio types [15]. There is much
more and cleaner medical data than there is for legal data. Further most legal data is nominal
(free-text data) whilst most medical data is of the ratio type. Thus, the use of Machine Learning
in law will never model its use in medicine.
Familylawisperhapsthelegaldomainmostappropriatefortheuseofinformationtechnology
because it has more data than other domains and most clients cannot afford expensive, time-
consuming litigation.
Branting’s Protection Order Advisor (2000) had its genesis in the decision by the Idaho
Supreme Court Technology Committee to fund a demonstration project to evaluate the appli-
cability of AI to judicial administration [16]. Several different domains for a demonstration
project were considered, including sentencing, pre-trial release, child support, and protection
order applications.
The Technology Committee selected protection order application assistance because the
inability to offer advice to pro se protection order applicants was distressing to staff in Idaho
courts. It relieved court staff of the painful choice between providing unauthorized legal advice
and ignoring the needs of domestic violence.
We now discuss a variety of systems that use AI to support ODR. From these systems we
hope to develop a methodology for developing ODR systems. “AI” used by current legal tech
companies tends to be rule-based or case-based reasoning, with an aim toward eventually
including machine learning.
The British Columbia Civil Resolution Tribunal (CRT) [17] has as its goal being:
1. Timely
2. Flexible
152

John Zelenikow CEUR Workshop Proceedings 150–160
3. Accessible
4. Affordable
5. Efficient
It diagnoses the dispute presented to it and provides legal information and tools such as
customized letter templates. If the initial provision of advice through the rule-based Solution
Explorer (essentially advice about BATNAs and Bargaining in the Shadow of the Law) does not
resolve the conflict, applicants can use the CRT to support dispute resolution.
Once the user has submitted the appropriate application forms and the application has been
accepted, the disputants can enter a secure and confidential negotiation platform, where the
disputants can attempt, without external help, to resolve the dispute. If this action fails, a
facilitator or mediator can be employed to help resolve the conflict. When desirable, agreements
can be turned into enforceable orders. If mediation, negotiation or facilitation does not resolve
the dispute, an independent member of the Civil Resolution Tribunal will make a ruling about
the case.
Currently, the British Columbia Civil Resolution Tribunal deals with the following five
categories of cases:
Table 1
Type of dispute Maximum Vale ($C)
Housing 5,000
Motor Injuries 50,000
Owners corporation (also called condominiums or strata titles) Any amount
Small Claims 5,000
Cooperative associations and societies Any amount
In the future, it is planned that the Civil Resolution Tribunal will be extended to further
domains. For these five domains, potential litigants are restricted to only using the Civil
Resolution Tribunal. Paper-based solutions are unavailable. This can potentially lead to major
problems for the digitally disadvantaged. To deal with this dilemma, potential litigants can
receive assistance in accessing the internet.
We believe that the major reason for the significant success of the Civil Resolution Tribunal,
is that British Columbia government has decreed that the British Columbia Civil Resolution is
the only forum in which residents can attempt to resolve those disputes listed above.
TheDutchplatformRechtwijzer(nowcalledJUSTICE42)wasdesignedforseparatingcouples
[18]. Thedevelopersviewedtheaimofthesystemas‘toempowercitizenstosolvetheirproblems
by themselves or together with his or her partner. If necessary, it refers people to the assistance
of experts.’
Couples pay €100 for access to the Rechtwijzer system. The system commences by asking
each partner for personal information such as their age, education and income, as well as their
priorities in the dispute such as whether they want the children to live with only one parent or
part time with each and other relevant preferences. The Rechtwijzer platform has 1. a diagnosis
phase; 2. an intake phase for the initiating party; and then 3. an intake phase for the responding
party.
153

John Zelenikow CEUR Workshop Proceedings 150–160
Following the completion of the intake process, the parties are encouraged to commence
working on agreements on those issues that occur in every separation. These may include a.
future communication channels; b. issues related to child welfare; c property issues (including
housing, money and debts); and d. child support and spousal maintenance.
The prevalent dispute resolution model in Rechtwijzer is integrative negotiation—focussing
upon the childrens’ and parents’ interests rather than haggling about rights. Nevertheless,
the ex-partners are informed of relevant processes—such as those for dividing property, child
support and standard arrangements for visiting rights. This allows the disputants to agree based
on informed consent, and essentially allows the parties to Bargain in the Shadow of the Law.
Final Agreements are reviewed by an independent lawyer. In the situation where the so-
lutions proposed by the Rechtwijzer system are not accepted by the couple, the disputants
are encouraged to request a mediator (this step costs an additional €360), or ask for a binding
decision to be made by an adjudicator. Until the step where adjudication is requested, the use
of the Rechtwijzer system is voluntary and non-binding.
The initial goal of the Rechtwijzer developers was to have the system as self-financing,
primarily through user contributions. Sadly, this has not occurred, primarily for commercial
reasons unrelated to the quality of the system.
Domestic and Family Violence apps should be used as part of a triaging system to ensure
timely action to protect potential victims. ODR systems also have capacity to incorporate
triaging to determine which problems require urgent action.
For example, systems should build in “tripwires” based on answers to questions or evidence
gathered through GPS (e.g., stalking) to dispatch assistance. Triaging is also required in other
legal domains. Examples might include when urgent action is required in the case of child
abduction or with regard to the granting of bail. It is important for triaging to be available to
initiate and expedite action in high-risk cases, leading to a reduced risk to the community. The
significance of timely, relevant advice is vital.
4. Some Family Dispute Resolution Tools
CoParenter helps separating, divorced, and never-married parents make and manage co-
parenting responsibilities, create court-ready parenting and holiday plans, resolve disputes,
and make more informed, child-centric decisions that save them time and money and keep
them out of court.1 Integrated ODR facilitates online negotiation and mediation and adds a
means for collaboration among various parties over a long period of time. The platform allows
co-parents to communicate, track scheduling, and manage responsibilities A large part of the
app’s features centre on communication: secure, time-stamped messaging; records of child
exchanges; on-demand mediation to make decisions about cost splitting; and a synced calendar.
CoParenter is a “rule-based” system set up to take parents step-by-step through the process
of creating a plan, asking them yes or no questions about what they want to do next, their
children’s names, and other relevant information.
Split-Up uses a predictive algorithm that can be used to determine a party’s BATNA going
into a negotiation for a discussion [19]. The system was developed using 103 commonplace (or
1https://coparenter.com (last visited January 29, 2023).
154

John Zelenikow CEUR Workshop Proceedings 150–160
unreported) family court cases to develop a predictive analytic for how future assets would be
divided between couples in the event of a divorce. Couples input shared costs, labor performed,
division of household duties, future job prospects, and more, which the algorithm uses to predict
division of assets. Despite using Machine Learning, the development of Split-Up involved much
conceptual modelling. 25 years later, the theoretical principles behind AI software have not
changed. But computer software and hardware are much less expensive, and data can be much
more easily stored. Portable and the Legal Services Commission of South Australia designed
and developed Amica , which emulates Split-Up.
In the 25 years since Stranieri et al developed their pioneering ML legal system Split-Up [19],
the solutions they developed to relevant problems are similar to today’s issues:
• What data do we choose?—In Split-Up we chose unreported commonplace cases from the
Melbourne Registry of the Family Court of Australia. In 1995, neural networks were slow,
expensive in computing cost and took much hard disc space – today we can use many
more cases, if we can find them.
• How do we check for biases in the data?—in RBR and CBR, due to transparency, bias is
evident. In ML cases in the training set can lead to bias - In Split-Up we eliminated cases
that lead to no results or results that are unfair. This requires human intervention—we
also argue that when using ML to build legal decision support systems we need hybrid
(together with RBR and/or CBR) systems rather than pure ML systems.
• How do we clean and transform the data?—In Split-Up we converted 103 free text judge-
ment into a database. PhD students (not lawyers) conducted the conversions. We rejected
cases that stopped our neural networks from learning. Family Court of Australia judges
later told us that the cases we rejected were indeed by a rogue judge whose decisions
were often in contradiction with those of other judges.
• How do we provide explanation?—in ML (except for decision trees which essentially
learn rules) decisions are made from black boxes with no readily available explanations -
In Split-Up we rationalised an explanation of the answer – once we were confident of
the answer, we used Toulmin’s (1958) theory of argumentation to provide explanations,
modelling the way FCA judges did so [20]—much legal theory says judges make a decision
which they justify instead of rationally working their way up a tree of arguments i.e.
top-down rather than bottom-up reasoning.
• How do we evaluate the outcomes? – When using a Machine Learning black box, we
want to feel fairly confident that the results are valid—In Split-Up we used the evaluation
theory of Reich and Barai [21].
Our Family Wizard offers tools to parents for scheduling, tracking, reimbursement requests/-
payments, communication, and creating logs of the communication. It emphasises effective
communication and allows parents to create third party accounts for others they want to be
able to join in, such as their therapists. Parents can use Our Family Wizard to create a shared
calendar, securely message on the app, check-in at various locations, and easily share payment
obligations. The app offers case management, the ability to view client activity, and access to
easily downloadable client records.
Family Winner is a family law support system that uses a variety of AI and game theory
techniques as developed by John Nash [22] to help structure the mediation process and give
155

John Zelenikow CEUR Workshop Proceedings 150–160
parties an idea of possible trade-offs . The system can also be used in other types of disputes,
calculating results strongly resembling eventual outcomes.
Thesystemisaskediftheissuescanberesolvedinthemap’scurrentformandwillallocatethe
issue as desired by the parties if so. If not, the user is asked to break down the least contentious
issue until they find sub-issues on which agreement can be attained. The system then will
then mathematically calculate which issue to give to each party, maximizing values and thus
satisfaction to clients.
Agreement Technologies are computer systems in which autonomous software agents nego-
tiate with one another with the aim of reaching mutually acceptable agreements. They provide
for an interaction mechanism that allows for agreements to be established and executed. More
sophisticated agreement technologies may use AI to pre-populate documents and provide stan-
dardized contracts based on party needs. The software can review parties’ previous documents
and learn to identify essential aspects in light of data observed. AI can also be used to flag
potentially problematic terms, recognizing changes that should be made based on context.
Examples include Lawyaw, Onit and LinklSquares [23].
5. How we envisage the ideal ODR System
We have examined ODR tools that somehow incorporate data analytics, algorithms, and/or AI.
Our examination leads us to believe that a truly helpful and holistic ODR program aimed to
assist SRLs and others should have the capacity to provide the following processes – as part of
a modular system.
It is modular in that all of the following modules are not necessary for every case. Still
having the modules accessible will allow individuals to better navigate the legal system and
find solutions to their legal problems. The ideal combination is a jigsaw puzzle combines:
1. CaseManagement: TheODRsystemshouldallowuserstoinitiatethedisputebyproviding
templatestoenterinformationabouttheissues. Itshouldthenqueryusersforappropriate
data. Users should be able to initiate the conflict, continuously access the data, and be
aware of timelines they need to meet, what documents are required at specific times, and
the progress of the case.
2. Triaging: The ODR system should indicate which cases require immediate action and
which cases provide less risks to litigants and can afford to be delayed. Non-professionals
also may have difficulty in choosing the appropriate forum for their dispute. Thus, the
ODR system should suggest immediate interventions where necessary and otherwise
direct parties where their cases should be addressed and/or heard. Triaging systems
are vital for initiating and expediting action in high-risk cases, leading to reduced risk
to both the applicants and the community. The significance of timely, relevant advice
is especially vital in cases of bail applications, child abduction, and domestic violence.
Triaging systems are needed to protect the interests of at-risk individuals.
3. Advisory Tools: The ODR system should provide processes for reality testing. Relevant
toolscouldincludearticles,BATNAadvisorysystemsmaterialsprovidingusefulparenting
156

John Zelenikow CEUR Workshop Proceedings 150–160
advice, calculators (such as those to advise upon tax and child support obligations), copies
of legislation, reports of cases, and videos of desirable and undesirable behavior. Advisory
Tools assist the disputants to enter the mediation/negotiation with the likely and best
(the two are often different) outcomes. With our focus upon user-centric computing we
need to consider how we can design advisory tools that SRLs (or indeed any disputants
without professional advisors) can gainfully use. Are the legal concepts behind the use of
these tools too difficult for amateurs to understand? How do we construct suitable user
interfaces for such disputants?
4. Communication Tools: All current ODR systems provide communication tools to support
some combination of arbitration, conciliation, facilitation, mediation, and negotiation.
ODR tools also naturally provide for shuttle mediation This can be very effective where
toxic relationships make it difficult for parties to reach agreement while in the same room,
even if it is virtual. Such a system could provide a trace of the parties conduct during the
dispute (e.g. Our Family Wizard).
5. Decision Support Tools: If the disputants still cannot resolve their conflict after receiving
advice from advisory systems and substantial communications between the parties, then
systems should incorporate computer programs that utilize AI and/or algorithms building
on game theory to facilitate trade-offs. While professionals can provide significant advice
regarding trade-offs, ODR systems should incorporate suitable decision support tools
using advanced analytics. Properly developed and monitored advisory systems can
provide each disputant, separately, with advice about appropriate options and the likely
outcomes of their disputes. Such decision support tools have capacity to assist disputants
during the mediation or negotiation in conducting the best possible trade-offs to obtain
those issues that they most desire.
6. Drafting Tools: Once the parties to a dispute reach an in-principle settlement, it is impor-
tant to provide computer software that assists in drafting acceptable agreements. Having
technologies available to memorialize an agreement saves everyone time and stress. In-
deed, it is problematic when parties back away from a concluded agreement under a guise
of falsely claimed lack of memory. Thus, ODR systems should incorporate agreement
technologies. Preparing agreements (such as parenting plans) that are acceptable to all
parties is a complex task that is especially problematic for parties without expert (human
or digital) support.
We are merely proposing further development of free or low-cost access to these 6 modules,
understanding that not all individuals or cases need all six modules. The aspiration is that
individuals, especially those that cannot afford access to attorneys, will have these modules
available so that they can “mix and match” to pave the way for access to justice in their given
situations.
157

John Zelenikow CEUR Workshop Proceedings 150–160
6. Ethics and Governance in ODR
Ebner and Zeleznikow (2016) viewed the governance of ODR as the ‘wild west’ [24]. Neither of
its constituent components, ADR or IT have strong governance models. They discuss:
• No-governance models;
• Self-governance models;
• Internal governance models; and
• External governance models.
Each has its pros and cons.
The European Ethical Charter on the use of AI in judicial systems and their environment,
approved on 3-4 December 2018 by the European Commission for the Efficiency of Justice
(CEPEJ) of the Council of Europe, describes the risks of the use of AI in this field. One regulation
says that the outcomes of the proceedings involving ODR should be transparent. Another
stresses the security of data. Others talk about quality and fairness.
All of these requirements are seemingly desirable. But many of them are contradictory,
especially when applied to Artificial Intelligence. And the techniques to be used vary depending
upon which forms of AI are used.
Rule-based reasoning and case-based reasoning are first generation forms of AI. Whilst they
may not be what most non-professionals today think of AI, they are very useful for building
systems for compliance and rules as code. The rules (or decision trees) and case retrieval are
transparent and act as explanation.
European principles require transparency—the manner in which transparency is ensured
depends on the form of Artificial Intelligence being used. For RBR it is the rules. For CBR it
is the cases in the case-base and the retrieval algorithm. In ML the algorithms are essentially
‘statistical black boxes. They report answers (or connections) without adequately explaining
how theses answers are derived. Of major concern for transparency are:
1. How do these algorithms opérate – unlike for rule-based systems, we do not see the code?
2. How is the data chosen for the algorithms to learn?
3. Is the data in any way massaged so that the algorithms can appropriately derive conclu-
sions from the data?
Security and Transparency are often opposing principles– If we make documents private, they
will be more secure. Making data and knowledge freely available and transparent may leave
it insecure and open to abuse. Quality of the data depends upon how the data is collected,
transformedandanalysed. Qualityoftheoutcomes(essentiallydistributivejustice)derivedfrom
‘clean and appropriate data’ depends upon the appropriate design and use of rules and cases.
Quality of the processes (procedural justice) relies upon the appropriate design of algorithms
by the developers.
158

John Zelenikow CEUR Workshop Proceedings 150–160
The most vexing question is whether systems are fair. Procedural fairness of rule-based
systemsisreasonablyeasytoevaluate: havethedesignersappropriatelymodelledthelegislation.
For CBR and ML the question is whether the cases and training set have been appropriately
chosen and transformed. Judging distributive fairness is more complex and requires domain
experts to evaluate a series of different outcomes.
7. Conclusions
There has not been enough attention paid to dispute system design, especially where the
stakeholders do not have the incentive and power to provide the best system to address concerns
with Access to Justice. System design must be human, user-centric, and provide access to
remedies for SRLs. All six typographies described should be available, even if offered in a
modular way so that no company needs to shoulder the burden of providing all six processes in
one system.
Such development must abide by ethical guidelines, including vigilance regarding the use
of AI and algorithms to ensure that SRLs are not left with “second class” justice. It is time to
reimagine Access to Justice through the innovative use of technology, not simply to advance
efficiency and corporate savings, but to empower SRLs in an often one-sided legal market.
This Word template was created by Aleksandr Ometov, TAU, Finland. The template is made
available under a Creative Commons License Attribution-ShareAlike 4.0 International (CC
BY-SA 4.0).
References
[1] M. E. Katsh. ”Dispute resolution in cyberspace”. Connecticut Law Review 28 (1996): 953.
[2] F. E. A. Sander. ”The multi-door courthouse.” Barrister 3 (1976): 18.
[3] R. Fisher and W. Ury, Getting to Yes, PenguinGroup, New York, 1981.
[4] H. Raiffa, The art and science of negotiation. Harvard University Press, Cambridge
(Massachusetts), 1982.
[5] L. McCarty. “Reflections on TAXMAN: An experiment in artificial intelligence and legal
reasoning”. Harvard Law Review 90 (1976): 305-373.
[6] M. J. Sergot, F. Sadri, R. A. Kowalski, F. Kriwaczek, P. Hammond, and H. T. Cory. “The
British Nationality Act as a logic program”. Communications of the ACM 29.5 (1986):
370-386.
[7] R. Susskind, Expert systems in law, Oxford University Press, Oxford, 1987.
[8] M.E.KatshandO.Rabinovich-Einy,Digitaljustice: technologyandtheinternetofdisputes,
Oxford University Press, Oxford, 2017.
[9] M. Galanter. “The vanishing trial: An examination of trials and related matters in federal
and state courts”. Journal of Empirical Legal Studies 1.3 (2004): 459-570.
[10] T. Sourdin and J. Zeleznikow. “Courts, Mediation and COVID-1”9. Australian Business
Law Review 48.2 (2020): 138-158.
159

John Zelenikow CEUR Workshop Proceedings 150–160
[11] M. Hagan. “A human-centered design approach to access to justice: generating new
prototypesandhypothesesforinterventionstomakecourtsuser-friendly”. IndianaJournal
of Law & Social Equality 6 (2018): 199.
[12] R. Susskind, Online Courts and the Future of Justice. Oxford University Press, Oxford,
2019.
[13] J. F. Roberge and V. Fraser. ”Access to commercial justice: A roadmap for online dispute
resolution (ODR) design for small and medium-sized businesses (SMEs) disputes.” Ohio
State Journal on Dispute Resolution 35 (2019): 1.
[14] A. Rajkomar, J. Dean and I. Kohane. “Machine Learning in Medicine”. New England
Journal of Medicine 380 (2019): 1347–1358.
[15] S. S. Stevens. “On the theory of scales of measurement”. Science 103.2684 (1946): 677-680.
[16] L. K. Branting. “An advisory system for pro se protection order applicants”. International
Review of Law, Computers and Technology 14.3 (2000): 357-369.
[17] S. Salter and D. Thompson. “Public-centered civil justice redesign: a case study of
the British Columbia civil resolution tribunal”. McGill Journal of Dispute Resolution 3
(2016):113-136.
[18] L. Kistemaker. “Rechtwijzer and Uitelkaar. NL. Dutch experiences with ODR for divorce”.
Family Court Review 59.2. (2021): 232-243.
[19] A. Stranieri, J. Zeleznikow, M. Gawler and B. Lewis. “A Hybrid rule-neural approach for
the automation of legal reasoning in the discretionary domain of family law in Australia”.
Artificial Intelligence and Law 7 (1999): 153.
[20] S. Toulmin, The Uses of Arguments, Cambridge University Press, Cambridge, 1958.
[21] Y. Reich and S. V. Barai. “Evaluating machine learning models for engineering problems”.
Artificial Intelligence in Engineering 13.3 (1999): 257-272.
[22] J. Nash. “Two-Person Cooperative Games”. Econometrica: Journal of the Econometric
Society 128 (1953): 128-140.
[23] A. Schmitz and J. Zeleznikow. “Intelligent Legal Tech to Empower Self-Represented
Litigants”. Columbia Science and Technology Law Review 23 (2021): 142-190.
[24] N.EbnerandJ.Zeleznikow. “Nosheriffintown: governanceforonlinedisputeresolution”.
Negotiation Journal 32.4 (2016): 297-323.
160
```
