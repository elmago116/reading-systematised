---
title: Brick by Brick- A Human-Centered Approach to Effective Dashboard Design for Smart Building and Energy Management
author:
  - Givannah Noor
year: "2025"
Type: Master thesis
DOI: ""
source: ""
created: 2026-04-24
description: ""
tags:
  - op/acc/pending-review
  - design/UCD/participation
  - themes/arquitecture_urban
  - design/UX
  - design/UCD/UX
  - op/doc/similar
pdfORepub: "[[Brick by Brick- A Human-Centered Approach to Effective Dashboard Design for Smart Building and Energy Management.pdf]]"
---
[[Brick by Brick- A Human-Centered Approach to Effective Dashboard Design for Smart Building and Energy Management.pdf]]
## Full text (extracted from `Brick by Brick- A Human-Centered Approach to Effective Dashboard Design for Smart Building and Energy Management.pdf`)

*Source:* `2PDF/Brick by Brick- A Human-Centered Approach to Effective Dashboard Design for Smart Building and Energy Management.pdf`  
*Extracted:* 2026-04-24

```text
Master Thesis
Brick by Brick: A Human-Centered Approach to Effective
Dashboard Design for Smart Building and Energy Management
by
Givannah Noor
(gnr240)
First supervisor: dr. Victor de Boer
Daily supervisor: dr. Victor de Boer
Second reader: dr. Ronald Siebes
January 17, 2025
Submitted in partial fulfillment of the requirements for
the VU degree of Master of Science in Information Sciences

DECLARATION OF AUTHORSHIP
I, Givannah, declare that this thesis titled, Brick-by-Brick: A Human-Centered Approach to Effective Dashboard Design for Energy
and Smart Building Managent . I confirm that:
• This work was done wholly or mainly while in candidature for a research degree at this University.
• Where any part of this thesis has previously been submitted for a degree or any other qualification at this University or any other
institution, this has been clearly stated.
• Where I have consulted the published work of others, this is always clearly attributed.
• Where I have quoted from the work of others, the source is always given. With the exception of such quotations, this thesis is entirely
my own work.
• I have acknowledged all main sources of help.
• Where the thesis is based on work done by myself jointly with others, I have made clear exactly what was done by others and what I
have contributed myself.
Signed:
Date:
2

Brick by Brick: A Human-Centered Approach to Effective
Dashboard Design for Smart Building and Energy Management
Givannah Noor
Vrije Universiteit Amsterdam
Amsterdam, The Netherlands
g.l.m.noor@student.vu.nl
ABSTRACT
Dashboards play a crucial role in data-driven decision-making and
monitoring across various industries, including non-profits, and
service organizations. Despite the prevalence of dashboards, there
is a lack of research on effective and applicable dashboard design,
particularly for smart building and energy management. Every or-
ganization or project brings unique visual design challenges that
often do not fit ready-made dashboarding tools. At Arnhems Buiten,
a HEDGE-IoT pilot site, a specialized dashboard is being developed
to help monitor various Internet of Things devices. This research
adopts a human-centered approach to effective dashboard design.
Using this approach, I have conducted four stakeholder interviews
with a project manager, building owner, property manager, and
director to identify pain points, key needs, and objectives. Insights
from user interviews guided the development of an initial con-
cept that was further refined into a high-fidelity prototype. This
prototype was then evaluated with two stakeholders using the
think-aloud technique. Three tasks were conducted to assess design
choices, user satisfaction, and usability. The findings demonstrate
that effective dashboard design extends beyond user interface pat-
terns and user experience principles, highlighting the importance
of storytelling and designing for predictive analytics. These re-
sults offer valuable implications for designing dashboards for smart
building and energy management needs and for improving the
visualization of predictive analytics.
1 INTRODUCTION
As technology becomes more advanced and accessible it is expected
that smart building systems will increase and transform the way
humans interact and live with their living spaces [13]. Smart homes
and buildings integrate advanced technologies such as artificial
intelligence (AI) and the Internet of Things (IoT) to create more
efficient and convenient living environments. HEDGE-IoT is an
innovative European project aimed at digitizing energy ecosystems
through the adoption of IoT solutions. The project framework will
be developed and demonstrated through six different pilots in six
different countries [1]. One pilot is located at Arnhems Buiten, an
Electricity Campus in the Netherlands fostering new initiatives.
At the site, a specialized dashboard is being developed to enable
administrators to monitor IoT devices, such as energy and smart
meters. HEDGE-IoT seeks to create a system to manage different en-
ergy nodes, providing real-data analysis through a dashboard, and
improving grid stability. Ultimately, this initiative aims to reduce
costs and promote sustainable energy practices.
Visual dashboards serve a critical role across various industries,
including non-profits, and service organizations. Dashboards are
defined in literature as visual displays of information designed to
achieve one or more objectives, often presented on a single screen
[2]. Dashboards are thus used as a way to facilitate understanding
of rapidly changing conditions, particularly those requiring timely
responses [22]. Optimal visual interfaces can provide substantial
value to users and create a significant impact on businesses, thus
making dashboards an compelling area of study [3].
However, dashboards bring together many challenges, such as
coordinated views, in-depth reading, and data tracking [22]. The
main challenge designers face when it comes to dashboard design is
that every dashboard has a unique visual design that often does not
fit ready-made dashboarding tools. Every organization or project
has a unique collection of metrics with unique visual presentation
challenges [3]. Specifically, the Arnhems Buiten pilot presents sev-
eral unique collections of metrics, due to the diverse types of data
it handles, such as heterogeneous, geographical, and numerical
data. The primary issue with IoT data is heterogeneity, as differ-
ent devices speak different languages, leading to interoperability
problems. In general, ready-made dashboarding tools fail to un-
derstand the complexity of user needs and goals, as well as visual
and analytical literacy [22]. This research aims to address unique
design challenges, along with user needs, to create a user-friendly,
effective, and applicable dashboard for the HEDGE-IoT pilot.
To drive the research, the following main research question was
formulated:
How can an effective user dashboard be designed to support smart
building and energy management?
To help answer the main research question, the following sub-
questions were formulated:
(1) What are the primary goals and needs of key stakeholders
using a dashboard for smart building and energy manage-
ment?
(2) What design principles can be applied to align the dashboard
design with stakeholder goals?
There is a lack of research on effective and applicable dash-
board design specifically tailored to smart buildings. The existing
literature and research on dashboard design focuses on dashboard
design for business management, visual analytics, education, or
health management. This research aims to address this gap by fo-
cusing on effective dashboard design for smart building and energy
management. In general, effective design is crucial for dashboards
to communicate key information to users and ensure easy access
to data [3]. Due to the increasing prominence of smart buildings
in efforts to create a more sustainable future, it is essential to un-
derstand how to design dashboards that facilitate effective building
management.
1

Dashboard designers must consider different factors such as
user literacy, contextually appropriate representations, and visual
language [22]. Design decisions should also align with specific orga-
nizational goals and user needs. Ready-made dashboard tools often
do not address these complex factors. Effective dashboards require
a gradual, iterative development process. This paper explores the
iterative gradual approach needed to design a dashboard for smart
building and energy management. Ultimately, the findings of this
research aim to enhance the user experience (UX) for the users,
provide valuable insights, improve performance monitoring, and
help users address malfunctions proactively.
2 RELATED WORK
2.1 UX Design
This research adopts a human-centered approach, drawing exten-
sively on the UX literature. In the book Interaction Design: Beyond
Human-Computer Interaction , Sharp et al. [24] explore the process
of interaction design, including interfaces, data analysis, proto-
typing, and evaluation. This work provides state-of-the-art UX
methods and techniques, offering valuable insights and a struc-
tured approach. This research uses Sharp et al. (2019) as a guideline
for the UX process. Elsewhere, Nunnally and Farkas [ 18] focus
on the process of planning, preparing, and facilitating research in
their book titled ‘UX Research: Practical Techniques for Designing
Better Products’ . This book particularly focuses on the UX research
aspect of the design process, offering practical guidance and meth-
ods for user-centered research. This research incorporates their
method of conducting a landscape analysis prior to user research
to understand the market. Furthermore, Portigal [ 21] provides a
framework for user interviews, emphasizing the importance of ef-
fective questioning and optimizing the interview process. These
insights provide a clear framework to follow for the user research
phase.
2.2 Dashboard Design
As mentioned prior, existing literature and research on dashboard
design focuses on application domains such as business, visual ana-
lytics, education, and public health. Although these domains differ
from the focus of this research, the existing literature provides valu-
able insights applicable to this research. Martins et al. conducted a
literature review arguing that functionality is the most important
element for dashboards. Furthermore, the study states that visual
elements are complex problems that require logical methods to
ensure an efficient solution [15]. Similarly, Pappas and Whitman
[19] conducted research on business data dashboards. In their study,
they conclude that to have an effective design, designers must let
their design be guided by the user’s goals, the context of use, and
the constraints of the underlying data. In addition, the research
offers insights for strategic, operational, and analytical business
dashboards. Although these studies focus on dashboards related
to business management, they still offer valuable design insights
for research on dashboard design for smart buildings and energy
management.
There are many high-level guidelines on dashboard design, in-
cluding advice on visual perception, the use of interaction, and help
to reduce information overload, such as the research conducted
by Janes et al. [12]. The journal article explains how to choose the
right data and the right visualization technique, as well as how a
dashboard can be perceived as useful and successful. Elsewhere,
Bach et al. [
2] performed an online dashboard design workshop
to help scrutinize and refine dashboard design patterns such as
content design, composition design, and color design. At the end
of the paper, a design framework is presented consisting of four
parts: knowledge, trade-offs, design process, and tool support. In
summary, Bach et al. [2] presents design patterns and principles
that can be applied to dashboard design for smart building and
energy management.
In 2015, Cahyadi and Prananto [ 4] explored key elements or
aspects that influence a dashboard design to analyze the dashboard
design process in the journal article ‘Reflecting design thinking: a
case study of the process of designing dashboards’. They argued that
a dashboard can be broken down into the following components:
data, technologies, users, graphs, metrics, organization, and features.
Knowing these components is crucial to making design decisions.
Furthermore, their study determined that interdisciplinary and
cross-functional group communication plays an important role
in the dashboard design process. Ultimately, this paper presents
valuable findings for the design process.
Although the existing literature focuses on different application
domains, Curry et al. did research on IoT-enabled UX for smart
water and energy management with a specific focus on generating
user awareness about their energy consumption [ 6]. Curry et al.
delivered several smart water and energy management systems
enabled by IoT at a number of pilot sites, providing useful infor-
mation on the enhanced user experience. They found that it is
important to understand the needs of your users and bring them
into the loop of the smart environment. In addition, their findings
highlighted the importance of minimizing cognitive overload with
clear and focused visualizations and careful use of targeted alerts
and notifications. The research conducted by Curry et al. serves as
a strong foundation for further research on dashboard design for
smart building and energy management.
3 DESIGN METHODS
This section outlines the methods and outcomes used in this re-
search. Section 3.1 highlights the internal research conducted to
better understand the Arnhems Buiten pilot site and the energy
management market. Section 3.2 details the user research phase.
Section 3.3 outlines the conceptualization and synthesis of the inter-
nal and user research, along with the ideation process for a possible
solution. Figure 1 provides an overview of the process, inputs, and
outputs of this section for clarity. The results of this section are
further discussed in Section 4, presented in the form of a prototype.
3.1 Internal Research
This section summarizes the internal research conducted before the
user research phase. The internal research consists of an informal
interview with the creator of the initial dashboard demo, a review
of the HEDGE-IoT system specifications, and a landscape analysis.
In addition to describing these methods, this section discusses the
results of the internal research. This provides information on cur-
rent design choices and specifications for the dashboard, as well
2

Figure 1: Overview design methods process
as a better understanding of the energy management dashboard
market and its competitors.
3.1.1 Intial Dashboard Demo Evaluation. The initial dashboard de-
sign demo, shown in Figure 2, served as a preview for prospective
users and stakeholders during the first general assembly at Arn-
hems Buiten. A non-structured interview with the demo’s creator
provided further insights into the design process. The demo was
created in Grafana, a ready-made dashboarding tool, thus mostly de-
fault settings and features were used. Few, if any, design principles
were applied, with the primary focus being achieving a functional
and readable layout. Overall, user involvement was absent in the
demo’s development and design principles were not considered.
Figure 2: Screenshot of initial Grafana dashboard demo made
by Mateusz Kędzia [14]
3.1.2 Analysis of Dashboard Specifications.Following the initial
interview with the creator of the demo, I analyzed the specifica-
tions document provided by HEDGE-IoT. The analysis clarified the
scope, objectives, and key performance indicators (KPIs) for the
dashboard. According to the pilot document, the main objectives are
to provide actionable insights and enable real-time data collection.
The dashboard should be designed to be a reliable communication
channel for real-time data transmissions that are tailored to the
needs of grid operators and stakeholders. The user interface (UI)
must provide real-time monitoring, predictive analytics, historical
data analysis, and optimization recommendations. Similarly, the
UI should be visualised through data charts to indicate consump-
tion and production levels. The overarching goal of the dashboard
is to reduce energy costs, improve grid stability through timely
notifications, and promote sustainable energy practices.
3.1.3 Landscape Analysis. Prior to conducting user research, I per-
formed a landscape analysis. This section defines landscape analysis,
outlines its limitations, and summarizes the most important find-
ings. In UX design literature, landscape analysis refers to a form
of insight-driven research that allows designers and researchers
to gain a crucial understanding of the market they are designing
for. Ultimately, the goal is for designers to use low-level analysis to
identify existing products or services that reflect a portion of the
functionality of the new product and better understand the possible
gaps or opportunities for a new product [18].
The documentation of four energy management platforms was
analyzed: Blockbax, Metrikus, OpenRemote, and BluWaveAI. This
resulted in a detailed strength and weakness analysis for each plat-
form as seen in Appendix A. A common feature among the plat-
forms is the use of off-the-shelf visualisation with minimal coding
required. The platforms also support communication with external
devices and services, such as APIs and protocol agents. In addition,
the platforms offered desktop and mobile app versions. Notably,
only Blockbax and BlueWave AI offered predictive analytics, which
presented an area for further opportunities. Additionally, platforms
were found to offer limited customization or excessive flexibility,
which could lead to decision fatigue for users.
However, landscape analysis has inherent limitations. Due to the
fact that the analysis was conducted independently, it reflects my
own priorities and relies on publicly available information disclosed
by companies. Despite limitations, landscape analysis is essential to
build an understanding of the market and inform future qualitative
research.
3.2 User Research
To acquire a deep and multifaceted understanding of stakeholder
goals, pain points, and mental models, user research was conducted
in the form of semi-structured interviews. User research allows for
a better understanding of the experience and emotions of stakehold-
ers [21]. In addition, user interviews are a helpful way to structure
the design process and provide relevant solutions that resonate
with users [10].
3.2.1 Participants. Four participants were interviewed, each of
whom held a managerial or executive role. Their roles are as follows:
project manager, property manager, building owner, and director. As
key stakeholders in the Arnhems Buiten and HEDGE-IoT project,
3

all participants are potential users of the dashboard to varying
degrees.
3.2.2 Materials. For this research, I conducted semi-structured
interviews as a method of discovery. Before interviewing, an ethics
review self-check was completed using the protocol provided by the
Ethics Review Committee of the Faculty of Science (BETHCIE) at
Vrije Universiteit Amsterdam. The self-check ensures that no ethical
concerns are raised with the conducted research. The results of the
self-check confirmed that the research did not raise ethical concerns
and no further action was required. A set of 24 pre-determined ques-
tions, detailed in Appendix B, was prepared to guide the interviews.
The questions were inspired by UX research books, including Inter-
viewing users: how to uncover compelling insights and UX research:
Practical techniques for designing better products . Examples of the
questions asked include the following:
(1) What tools or systems do you currently use to access, man-
age, and collect information?
(2) What problem are you aiming to solve with the dashboard?
(3) What are your three main goals for the dashboard?
Semi-structured interviews provide the liberty for participants
to elaborate on their responses and introduce new topics. A semi-
structured approach ensures more structure and consistency than
non-structured interviews while maintaining flexibility between
interview sessions [
10]. To be able to assess the usability of the
interview guide I conducted a test interview. The main goal was
to obtain an indication of the duration of the interview, identify
redundant questions, and ensure the logical order of the questions.
The initial interview guide was designed with property managers
in mind, as they represented the main stakeholders of the dash-
board. However, after the first interview, the questions were refined.
For example, questions about users’ daily routines were deemed
less relevant for stakeholders who would not use the dashboard
frequently and were removed. Similarly, questions related to pain
points with the current system were excluded, due to the fact that
Arnhems Buiten currently has an outdated energy management
system. The revised questions mainly focused on improving the
demo dashboard. Finally, the platform ATLAS.ti was used to help
organize and code the qualitative data acquired from the interviews.
3.2.3 Procedure. The interviews began with an introduction that
provided participants with an explanation of the purpose of the
study and a detailed description of their role in contributing to the
study. Participants were also informed about how their data will
be collected, processed, and used. Additionally, their rights were
explained, and consent to record the audio was obtained. The inter-
view guide consisted of three sections. The sections are as follows:
participant background, current systems in use at Arnhems Buiten,
and hypothetical questions for the desired dashboard. At the end of
each session, participants were thanked for their contributions and
informed about a follow-up user evaluation session. After the partic-
ipants left, additional notes were recorded to capture observations
that could not be documented during the interview.
3.2.4 Data Analysis. After completing all four interviews, the au-
dio recordings were transcribed to produce written copies. The
transcriptions were reviewed multiple times to create familiarity
with the data. To code the data, ATLAS.ti was utilized. Coding
involves identifying themes across interview data to get a clear
understanding of the patterns that come across the interviews. The
ultimate goal with coding is data management and reduction [25].
Coding approaches can be either inductive or deductive. This re-
search utilized inductive coding, also referred to as open coding.
Inductive coding begins with the identification of general themes
and ideas. Thus, the development and elaboration of the codes arise
from the material being examined. Next, focused coding, also re-
ferred to as axial coding, was performed. Focused coding involves
narrowing down, identifying relationships, and merging different
themes and categories discovered during open coding [25].
3.3 Conceptualization
This section discusses key outcomes and insights from the internal
research discussed in Section 3.1 and the user interviews discussed
in Section 3.2. It begins by defining the problem scope, followed by
an exploration of potential solutions.
3.3.1 Problem Scope. After coding the interview data and identify-
ing key themes, the problem scope was identified. It is essential to
understand the problem’s scope and the underlying issues rather
than immediately moving to solutions and conclusions. One promi-
nent theme identified is the user goals for the dashboard. Since
Arnhems Buiten did not have a dashboard in place, it was crucial
to understand the users’ specific needs and expectations for a mon-
itoring dashboard. The interview data revealed that users desired
two distinct dashboards: one tailored for the administrators and
management at Arnhems Buiten, and another for tenants and other
users. The user goals were summarized and presented in Table 1.
To better illustrate participants’ needs for two distinct dash-
boards, two user personas were created. User personas are a critical
component to help orientate UX design and development. Personas
help ensure that user needs are considered in the design process,
thus aiding design decisions without inappropriate generalization.
Furthermore, they also offer an easy way to communicate about
users to stakeholders [
16]. The first persona, outlined in Table 2
represents the property manager. The persona was created to rep-
resent the administrative perspective and the overlapping goals
of the other stakeholders, including the project manager, the di-
rector, and the building owner. The second persona, outlined in
Table 3 represents the goals and needs of the other users, notably
the tenants.
After the personas were crafted, user stories were created to
help identify the best possible way to implement a solution. User
stories are defined as short statements expressing user needs and
what they hope to achieve [ 9]. User stories are often structured
in the following format: “As a [persona/user], I want to [goal or
action], so I can [outcome or reason]”. Two examples of user stories
formulated for this research include:
(1) As a property manager at Arnhems Buiten, I want to check
the energy meters often, so I can make sure we are paying
the correct amount of money to the energy providers
(2) As a tenant at Arnhems Buiten, I want real time analysis of
energy consumption, so I am aware of my own energy usage
and consumption
A total of 31 user stories were created, the full list is detailed in
Appendix C. Each user story is assigned a unique identifier (e.g.,
4

Table 1: Summary of the user goals expressed in the interviews
Project Manager Building Owner Property Manager Director Other Users
Insights into energy
consumption, production,
and electricity usage
Energy usage awareness
for individuals who have
difficulty understanding
complex diagrams
Insights into energy
consumption, production,
and electricity usage
Insights into energy
consumption and
production, and
electricity usage
Awareness of energy
usage
Real-time data analysis
with notifications
Predictive metrics for
energy optimization
Historical data analysis Share energy
consumption and
production statistics with
lessees or other users
Reducing energy costs
Energy usage awareness
for individuals who have
difficulty understanding
complex diagrams
Real-time data analysis
with notifications
Real-time data analysis
with notifications
Predictive metrics for
energy optimization
Enabling lessees to
monitor energy
consumption
independently
Analyze the impact of
new systems and
possibilities
Table 2: Property Manager User Persona
Name Thomas Bakker
Occupation Property Manager
Age 38
Psychographics
• Quick Thinking
• Detail Oriented
• Financial Literacy
• Values Structure
• Efficient
• Hospitality Driven
End Goals Use a monitoring dashboard
for historical data analysis, real
time data analysis with notifi-
cations of faults and/or anom-
alies, and insights into energy
consumption and production.
US-1, Us-2) to ensure clear differentiation. The user stories were
derived from the user interviews and personas, making them a
summarization of the data acquired in the interviews. The user
stories were essential to be able to assess priority. The 31 user
stories were placed in an impact-effort matrix, shown in Figure 3.
The matrix is based on the perceived impact expressed by the users
in the interviews and my own assessment of the effort needed to
design and implement certain requirements. The matrix was used
to categorize the requirements for the MoSCoW table, outlined in
Table 4. MoSCoW prioritization technique is an abbreviation that
stands for: must-have, should-have, could-have, and will not have.
Each requirement in the MoSCoW can be linked to a user story
through its unique identifier (e.g., US-1, US-17).
Table 3: Tenant User Persona
Name Daniel de Graaf
Occupation Daycare Worker/Tenant at Arn-
hems Buiten
Age 26
Psychographics
• Sustainability Advocate
• Enjoys Teaching
• Child-Friendly
• Non-Technical
• Curious
End Goals To use the monitor dashboard
to keep track of the energy us-
age and to help reduce energy
costs.
It is important to note that the impact-effort matrix and MoSCoW
prioritization were applied within the scope of this thesis. They
focus on the design of the artifact proposed in Sections 4 and 6,
and not the final HEDGE-IoT system. In particular, the ‘could-have’
column requires an additional explanation. Requirements in this col-
umn, such as a ‘fast dashboard system’ and ‘easily adding additional
datasets’, are more technical requirements. However, since the scope
of this thesis is focused on the UI design of dashboards, technical
requirements will not be focused on. Due to time constraints, the
property manager persona, representing the administrative side,
was prioritized. This decision was made because users fitting the
property manager persona were interviewed, while users fitting
the tenant persona were not directly interviewed. Additionally, the
tenants and other users are a diverse group of users with different
5

backgrounds and technical knowledge, thus requiring a different
design approach. However, this creates room for future research.
3.3.2 Solution Scope. Once the scope of the problem was defined,
the next step involved ideation to determine the solution scope.
This section focused on brainstorming and developing possible solu-
tions. To commence the ideation process, “How Might We” (HMW)
questions were formulated to frame the problem for ideation and
help generate creative ideas. The main goal with HMW questions
is to ensure that the right problems are addressed during ideation.
Examples of the formulated HMW questions include the following:
• How might we let administrators easily access the building
energy meter data?
• How might we help administrators understand the data bet-
ter?
• How might we provide administrators and users with all the
needed information?
The HMW questions were derived from the ‘must-have’ require-
ments from the MoSCoW prioritization, in Table 4. Once the HMW
questions were formulated, the Crazy 8 method for ideation was
used. Crazy 8 is a widely used ideation technique in UX design that
involves sketching eight solutions in eight minutes. This approach
encourages the rapid generation of ideas. From the eight sketched
ideas, three concepts were chosen:
(1) A dashboard system with a map as the focal point providing
an overview with zoom-in functionality
(2) A companion app for regular updates and notifications
(3) A multisensory dashboard ensuring no events are overlooked
From the three concepts, the first concept was chosen for further
development. The first concept was chosen since it addressed the
‘must-have’ and ‘could-have’ requirements outlined in the MoSCoW
prioritization. The selected concept was refined further through
sketches that focused on details such as the information archi-
tecture. A complete overview of the ideation process, including
Figure 3: Impact-effort matrix
HMW questions, Crazy 8 sketches, and subsequent refinements, is
provided in Appendix D.
4 PROTOTYPE
Based on the outcomes of the internal research, user research, and
conceptualization done in Section 3, a low-fidelity (Lo-Fi) concep-
tual design and high-fidelity (Hi-Fi) prototype were developed. This
section discusses the two designs and the relevant underlying de-
sign choices.
4.1 Lo-Fi Wireframes
An overview of th wireframes and the key design choices involved
is provided in this section. Wireframes are a set of documents that
show structure, content, and controls. Wireframes are also a way
to capture initial concept designs. Wireframes can be captured at
varying levels of abstraction and may only show a part of the system
or a complete overview [24]. For this research, the wireframes offer
a partial overview of the system. Pages such as a sign-in/login page
to grant authorization to the dashboard were not designed and
included in the wireframes.
For the dashboard, a multi-page structure was chosen, since the
requirements from the users are too much to fit in a traditional
single-page dashboard layout. The overarching design decision
made for the dashboard, specifically the overview page, comes
from Schneiderman’s Visual Information-Seeking mantra [26]. It
provides a framework for designing information visualization ap-
plications. In the mantra the basic visual design guidelines are
summarized as follows: overview first, zoom and filter, then details-
on-demand. To adhere to the Visual Information-Seeking Mantra
the visualisation structure drill-down story was used. Segel and
Heer [23] describe drill-down story as presenting a general theme to
users and then allowing users to choose among particular instances
of the theme to reveal more details. This visualization structure
was used for the overview page, shown in Figure 4a. A partial map
provides an overview of all buildings in Arnhems Buiten, allowing
users to click on each building for more details. Partial maps are
commonly used in enterprise and analysis systems due to their bal-
ance between map visualisation and content. The drill-down story
visualization structure allows users to dictate what information and
details they can see and when [23]. The zoom-in page, shown in
Figure 4b, is implemented as a pop-up modal. This approach allows
for screen space to be saved on the overview page. On the pop-up
modal users can view details regarding energy usage and produc-
tion. The chosen design is a grouped layout, where the widgets
are organized using Gestalt Principles of proximity and closure [2].
These principles effectively describe visual perception behavior [7].
Additional wireframes created for this research, but not discussed
in this section, can be found in Appendix E.
4.2 Hi-Fi Prototype
This section provides an overview of the Hi-Fi prototype and the
key design choices involved. A Hi-Fi prototype closely resembles
the final product and offers more functionality than wireframes
or other forms of Lo-Fi prototypes [24]. The Hi-Fi prototype is an
offline prototype made in Figma, a software for interface design.
6

Table 4: MoSCoW Prioritization
Must-Have Should-Have Could-Have Will Not Have
All needed data in one easily
accessible platform
(US-1/10/14/16)
Added context to understand
why there is a peak (US-5)
Invoices easily accessible in the
dashboard (US-2)
Knowing how many people are
in the building (US-15)
Notifications for any
anomalies/faults or if the grid
capacity will be exceeded
(US-3/4)
Advice and analysis (US-8) Fast dashboard system (US-17) Cartoon figurine to explain what
is going on with the data (US-25)
Forecasted prices and costs
(US-6/9)
Map indicating all building and
energy nodes (US-11)
See difference in usage after new
installation (US-12/21)
Correlate business cases upfront
(US-20)
Historical data to compare
energy usage (US-13)
Energy behavior awareness
(US-22/26/27)
Real time data analysis to
pinpoint the usage of a specific
tenant (US-7)
Mobile app (US-31)
Simple and appealing user
interface (US-24)
Easily adding additional datasets
(US-18)
Multi-view dashboard for
different users (US-23/14)
Notifications for tenants if usage
is above or approaching average
usage (US-28/29)
(a) Overview page
 (b) Zoom-in page
Figure 4: Dashboard wireframes designed in Figma
Due to users requesting a simple and appealing user interface,
the goal was to create an analytical and infographic dashboard.
Analytical dashboards typically use complete visualizations to show
larger and more complex data sets, while infographic dashboards
include graphical elements and other non-data ink to complement
data representations [2]. The decorative graphical elements used
in the dashboard enhance the dashboard’s appeal and usability.
On the overview page of the Hi-Fi prototype, shown in Figure 5a,
semantic colors are used to convey good-bad semantics [ 2]. For
example, red indicates a critical issue in a building, orange signals
a warning, and blue suggests energy saving tips. On the map, the
focal point pattern indicates important pieces of information to
the users quickly, such as specific buildings on the campus. For
real-time data, focal points often use animation, such as a pulsating
dot. The animation helps to convey that the location is updated
frequently [8]. Throughout the dashboard, simple visualizations,
such as bar and line charts, are used because they provide more
clarity and are easier to read [2].
The insights page, shown in Figure 5b, provides additional con-
text and forecasted analytics. Insights from user interviews revealed
a strong interest in incorporating predictive analytics into the dash-
board. However, with an increased emphasis on predictive data, it
is crucial that users understand which data is predictive and should
not be taken as absolute truth and which data is fully accurate.
To differentiate between actual data and predictive data, a distinct
color border was applied to the widget. Color is described as a
pre-attentive property along with form, movement, and spatial po-
sitioning. A pre-attentive visual property is one which processes in
spatial memory without conscious action. In short, pre-attentive
properties are easier to process for the eye and brain [
11]. These
7

design choices collectively create an interface that balances func-
tionality with user-friendly design.
4.2.1 Accessibility. Although not explicitly required, designing
with accessibility in mind ensures that the content is usable by a
broad range of individuals, including those with disabilities. The
Web Accessibility Guidelines (WCAG 2.0) were consulted during
the design process. According to WCAG 2.0 level AA, normal text
requires a contrast ratio of at least 4.5:1, while large text and user
interface elements require a ratio of at least 3:1 [ 5]. Level AAA
recommends higher contrast ratios of 7:1 for normal text and 4:5:1
for large text. In this dashboard, the level AA requirements of
WCAG 2.0 were followed for crucial information. All touch points
were designed to be at least 24x24 pixels, and text sizes were 12
pixels or larger to ensure readability. Additionally, the Stark plugin
in Figma was used to simulate various types of color blindness,
including protanopia, achromatopsia, deuteranopia, and tritanopia.
This ensures that all elements on the dashboard remain readable,
enhancing overall accessibility.
5 USER EVALUATION
5.1 Approach
The Hi-Fi prototype discussed in Section 4.2 was evaluated by two
users. These participants were among those interviewed during the
user research phase outlined in Section 3.2. Although testing the
prototype with only two participants is a limitation, their status as
power users provided valuable insights. Power users are individuals
categorized by their competence and strong motivation to maximize
the functionality of a computer system [
20]. The evaluation focused
on three key design choices:
(1) Differentiating predictive data from actual data on the in-
sights page
(2) Assessing the effectiveness of pulsating focal points and
zoom-in functionality on the map
(3) Evaluating the frequency of error notifications
To structure the evaluation, specific UX success metrics were de-
fined to measure the design’s effectiveness. These metrics included
user satisfaction, task success, and usability.
The evaluation sessions were conducted online via Microsoft
Teams. Participants were initially asked to provide general feed-
back on the interface. To assess the effectiveness of the UX success
metrics, participants were asked to complete three tasks related to
the three key design choices mentioned prior. Participants shared
their screens during the session, allowing their interactions to be
observed. Participants were also instructed to simulate using the
dashboard as they would in their professional roles. Example of
tasks included identifying which building has a critical event, de-
termining the predicted energy usage for the following day, and
reviewing the costs for Arnhems Buiten in June.
Throughout the tasks, participants used the think-aloud tech-
nique, which involves verbalizing their thoughts and actions to
provide insight into their perceptions and challenges [24]. The user
evaluation guide, including detailed descriptions of the tasks, is
provided in Appendix F. Both evaluation sessions were recorded
and transcribed. A manual analysis of the transcriptions was per-
formed to extract the most important topics. A summary of the
most important results is discussed in the subsequent section.
5.2 Results
This section presents an overview of the results of the evaluation
session, focusing on important findings related to the design choices
and UX metrics tested. Overall, participants thought the dashboard
was easy to understand and expressed interest in using it frequently.
Regarding design choices, participants indicated that they were able
to distinguish between predictive and actual data. However, both
participants noted that if all focal points on the map pulsated, it
would diminish their effectiveness and become distracting. When
it comes to the frequency of notifications, both participants were
satisfied. In terms of task completion, the participants successfully
completed two out of the three. The task the participants struggled
with was to change the overview page to a different date. The
participants also provided feedback on some words used in the
dashboard. For example, participants found the distinction between
‘problem’ and ‘warning’ unclear. Moreover, the summary of the
total euros spent lacked clarity, particularly whether the amount
was for the month, quarter, or year. Feedback obtained during the
user evaluation session informed the next iteration of the Hi-Fi
prototype, which will be discussed in the following section.
6 FINAL PROTOTYPE
This section will detail each page of the final prototype and any
notable changes made after the user evaluation discussed in Section
5. As mentioned prior, the final prototype is an offline prototype
made in Figma, available through this link. The final prototype is
depicted in Figure 6. Larger images of screenshots of the prototype
can also be found in Appendix G. The final prototype provides
a clear and central system for real-time energy data analysis. It
streamlines management and ensures transparency and efficiency
in a simple and appealing user interface. The overview page, shown
in Figure 6a, includes a map that shows an overview of the entire
campus and the current state of energy usage and production. It
also presents key statistics, such as the percentage of grid capacity
used and the percentage of energy saved. On the overview page,
users can also set an energy saving goal for the entire campus or
specific buildings. The dashboard will then provide tailored tips
to help achieve the goals. When the grid capacity exceeds 75%, a
warning pop-up modal appears. If it exceeds 90%, users will receive
an issue pop-up modal. Users can click on individual buildings
on the map to access detailed information, including hourly and
cumulative energy usage, as illustrated in Figure 6b.
The insights page, shown in Figure 6c, provides additional con-
text of the energy usage and production, integrating weather in-
formation for a complete overview. Users can also view forecasted
prices and costs to plan adequately for the following day. The dash-
board offers advice for the next day, as well as alternative insights.
These scenarios allow users to explore how energy usage and pro-
duction could change under specific conditions, such as charging
only during off-peak hours.
8

(a) Overview page
 (b) Insights page
(c) History page
Figure 5: Screenshots of Hi-Fi dashboard prototype made in Figma
The historical data page, illustrated in Figure 6d, allows users
to analyze past energy data. It allows for comparisons of energy
usage, production, costs, and savings on a monthly or yearly basis.
The final prototype satisfies all the ‘must-have’ and ‘should-have’
requirements as specified in the MoSCoW prioritization in Table 4.
The requirements listed in the categories ‘could-have’ or ‘will not
have’ were not included in the final design.
6.1 Changes From First Iteration
Following the user evaluation, several changes were made to the
initial dashboard design, shown in Figure 5, and discussed in Sec-
tion 4. First, users expressed a preference for fewer pulsating focal
points on the map. Consequently, only buildings with a critical
event requiring immediate action feature a pulsating focal point to
grab the user’s attention. Second, the date displayed at the top of
the overview page and the insight page has a different color and
a heavier font weight to make it more noticeable. Simultaneously,
other elements, such as tables with eye-catching colors, were ad-
justed to a more neutral tone. Third, the costs section was removed
from the top of the overview and insights page. Users found the
cost section unclear, since it did not specify the time frame. An
overview of the accumulated costs is still available on the historical
data page, however, only when it is clear if it is about monthly or
yearly costs. Additionally, the terms ‘used’ and ‘produced’ at the
top of the overview and insights page were changed to ‘used today’
and ‘produced today’ to improve clarity. Fourth, the word ‘prob-
lem’ was changed to ‘issue’ to emphasize that immediate action is
required. Finally, decorative embellishments were removed from
the insights page to reduce the cognitive load for the users. These
modifications improve the overall design, usability, and UX of the
dashboard based on feedback from user evaluation sessions.
7 DISCUSSION
This section outlines the limitations of the research, generalizability
of the findings to related projects, and opportunities for future
research.
7.1 Limitations
As mentioned in Section 3.3.1, a user persona was developed to
represent the tenants at Arnhems Buiten, however, due to time
constraints, no direct interviews were conducted with the tenants
themselves. Instead, the user persona was informed by the user
interviews conducted with administrators in Section 3.2. This limits
the accuracy and applicability of the tenant representation in this
thesis.
9

(a) Overview page
 (b) Zoom-in page
(c) Insights page
 (d) History page
Figure 6: Screenshots of final Hi-Fi dashboard prototype made in Figma
Additionally, in Section 3.1.3, a landscape analysis was used to
gain a crucial understanding of the energy management market.
However, landscape analysis has inherent limitations, since it was
conducted independently and is based on publicly disclosed infor-
mation.
Finally, as mentioned in Section 5 the design evaluation also faced
constraints. Due to time limitations, the design was tested with two
power users and underwent two iterations. A human-computer
interaction researcher, Jakob Nielsen, recommends evaluating de-
signs with three to five users across three iterations to derive the
best usability insights. Nielsen argues that a second study provides
deeper insight into usability and fundamental structures. Multiple
user evaluation sessions help to reassure re-designs and ensure that
no new usability issues have arisen during the re-design process
[17]. The inability to conduct additional evaluation sessions and
iterations represents a limitation of this study.
7.2 Contributions and Future Research
This research highlights the importance of incorporating narrative
storytelling principles into dashboard design, extending beyond
conventional UX principles and UI patterns. Segel and Heer em-
phasize that narratives are rooted in a clear starting point, often
represented by an establishing shot or overview, as seen in films and
visual media [23]. In the dashboard, the overview page serves as the
clear starting point, providing a comprehensive view of Arnhems
Buiten. In narrative storytelling, continuity is of the utmost impor-
tance. Visual media achieves continuity through techniques such
as object matching, which maintain viewer orientation. Similarly,
consistent design elements across the dashboard offer continuity
and allow users to remain oriented within the narrative conveyed
by the dashboard. Ultimately, this research has determined the im-
portance of narrative storytelling techniques for dashboard design
to communicate complex content to users. This approach can be
applied to various dashboards across different fields which require
contextual understanding to be able to connect data points and
interpret information appropriately. Examples include dashboards
in healthcare, financial analytics, transportation and logistics, ur-
ban planning, and sports analytics. Future research could further
explore the narrative techniques that are often used in visual media
and apply them to dashboard design.
Moreover, this research explores the differentiation of predictive
and actual data using pre-attentive processing with color. As pre-
dictive analytics become more prevalent in dashboards due to the
advancements of AI, effective differentiation methods are crucial.
Ultimately, the goal with dashboard design is to orient the user
10

early and draw attention to key elements. While this study eval-
uates the effectiveness of a single differentiation method, future
research could examine other methods to differentiate between
predictive and actual data. Furthermore, future research on en-
ergy management dashboards could focus on tenant engagement,
particularly how design can influence sustainable behavior and
encourage energy consciousness among users.
8 CONCLUSION
This section concludes the paper and addresses the research ques-
tions proposed in Section 1, the introduction. This study presents
an effective dashboard design through a human-centered approach,
incorporating user interviews and evaluations. User interviews
provide valuable insight into user needs, goals, and pain points.
User evaluations were conducted to test the effectiveness of the
proposed design. The main research question guiding this study is:
“How can an effective user dashboard be designed to support smart
building and energy management?”
To address the main research question, two sub-questions were
formulated. The first sub-question is: “What are the primary goals
and needs of key stakeholders using a dashboard for smart building
and energy management?” This question aims to gain a complete
understanding of user goals and needs. Section 3, specifically Sec-
tion 3.3.1, provides an answer to this sub-question using data from
user interviews and internal research. The findings are summarized
through a user goals table, personas, and user stories.
In summary, users wanted a dashboard that functions as a clear,
centralized system that offers real-time energy analysis to ensure
transparency and efficiency. This functionality is crucial for users to
better monitor energy consumption and production, reduce costs,
and adopt more sustainable practices.
The second sub-question is: “What design principles can be
applied to align the dashboard design with stakeholder goals?”
This question aims to identify which design principles contribute
to effective dashboard design. The answer to this sub-question
was presented through the proposed design artifact in Section 4
and Section 6. The findings indicate that both established design
principles, such as Schneiderman’s Information-Seeking mantra
[
26] and drill-down story [23], along with storytelling principles
commonly used in visual media, enhance the effectiveness of the
dashboard. Examples of narrative design principles include estab-
lishing or overview shots, continuity techniques, and highlight-
ing important elements to guide users. This research particularly
implemented a partial map along with summarized statistics to
provide an overview of Arnhems Buiten. Additionally, color was
used to highlight predictive data, allowing users to differentiate
between predictive analytics and actual data. As AI and predictive
analytics are increasingly used in dashboards, it becomes crucial
to further explore methods for effectively presenting predictive
data to users. In summary, dashboards often handle complex and
organization specific data, making ready-made dashboarding tools
often insufficient. Designing an effective dashboard for energy and
smart building management designers requires aligning the design
with user goals and needs while going beyond design principles.
Narrative storytelling techniques, as used in visual media, offer
valuable strategies to establish context, maintain continuity, and
highlight important elements. These principles are beneficial when
managing complex data. Thus, effective dashboard design requires
an incremental human-centered approach, brick by brick.
REFERENCES
[1] [n.d.]. About - HEDGE-IoT. https://hedgeiot.eu/about/
[2] Benjamin Bach, Euan Freeman, Alfie Abdul-Rahman, Cagatay Turkay, Saiful
Khan, Yulei Fan, and Min Chen. 2022. Dashboard Design Patterns. IEEE
Transactions on Visualization and Computer Graphics (2022), 1–11. https:
//doi.org/10.1109/TVCG.2022.3209448
[3] Richard Brath and Michael Peters. 2004. Dashboard Design: Why Design is
Important. DM Review Online (Oct. 2004).
[4] Amelia Cahyadi and Adi Prananto. 2015. Reflecting design thinking: a case
study of the process of designing dashboards. Journal of Systems and Information
Technology 17, 3 (Aug. 2015), 286–306. https://doi.org/10.1108/JSIT-03-2015-0018
[5] Ben Caldwell, Michael Cooper, Loretta Guarino Reid, and Gregg Vanderheidn.
2008. Web Content Accessibility Guidelines (WCAG) 2.0. https://www.w3.org/
TR/WCAG20/
[6] Edward Curry, Souleiman Hasan, Christos Kouroupetroglou, Willem Fabritius,
Umair Ul Hassan, and Wassim Derguech. 2018. Internet of Things Enhanced User
Experience for Smart Water and Energy Management. IEEE Internet Computing
22, 1 (Jan. 2018), 18–28. https://doi.org/10.1109/MIC.2018.011581514
[7] Stephen Few. 2016. Data Visualization for Human Perception. InThe Encyclopedia
of Human-Computer Interaction (2 ed.). 28.
[8] Michael Gaigg. 2023. Designing map interfaces: patterns for building effective map
apps (first edition ed.). Esri Press, Redlands.
[9] Interaction Design Foundation. [n.d.]. What Are User Stories? https://www.
interaction-design.org/literature/topics/user-stories
[10] Interaction Design Foundation. 2016. What are User Interviews? https://www.
interaction-design.org/literature/topics/user-interviews
[11] Interaction Design Foundation. 2018. Preattentive Visual Properties and
How to Use Them in Information Visualization. https://www.interaction-
design.org/literature/article/preattentive-visual-properties-and-how-to-use-
them-in-information-visualization
[12] Andrea Janes, Alberto Sillitti, and Giancarlo Succi. 2013. Effective Dashboard
Design. (Jan. 2013).
[13] Team Kaarwan. 2024. Innovative UX Design for Smart Homes and Build-
ings. https://www.kaarwan.com/blog/ui-ux-design/user-experience-for-smart-
homes?id=459
[14] Mateusz Kędzia. 2023. Explainable AI Development Enviroment and Tutorial for
Heterogeneous IoT Data Processing . Bachelor’s Thesis. Vrije Univrsiteit Amster-
dam.
[15] Nuno Martins, Susana Martins, and Daniel Brandão. 2022. Design Principles in the
Development of Dashboards for Business Management. In Perspectives on Design
II, Daniel Raposo, João Neves, and José Silva (Eds.). Vol. 16. Springer International
Publishing, Cham, 353–365. https://doi.org/10.1007/978-3-030-79879-6_26 Series
Title: Springer Series in Design and Innovation.
[16] Tara Matthews, Tejinder Judge, and Steve Whittaker. 2012. How do designers and
user experience professionals actually perceive and use personas?. InProceedings
of the SIGCHI Conference on Human Factors in Computing Systems . ACM, Austin
Texas USA, 1219–1228. https://doi.org/10.1145/2207676.2208573
[17] Jakob Nielsen. 2000. Why You Only Need to Test with 5 Users. https://www.
nngroup.com/articles/why-you-only-need-to-test-with-5-users/
[18] Brad Nunnally and David Farkas. 2016. UX Research: Practical Techniques for
Designing Better Products (first ed.). https://www.oreilly.com/library/view/ux-
research/9781491951286/index.html ISBN: 9781491951293.
[19] Lisa Pappas and Lisa Whitman. 2011. Riding the Technology Wave: Effec-
tive Dashboard Data Visualization. In Human Interface and the Management
of Information. Interacting with Information , Michael J. Smith and Gavriel Sal-
vendy (Eds.). Vol. 6771. Springer Berlin Heidelberg, Berlin, Heidelberg, 249–258.
https://doi.org/10.1007/978-3-642-21793-7_29 Series Title: Lecture Notes in Com-
puter Science.
[20] SAP Help Portal. [n.d.]. Power User’s Guide. https://help.sap.
com/docs/SAP_NETWEAVER_702/fe13d28d6c551014bdb0efcab31d7096/
1e013f420e09b26be10000000a155106.html?locale=en-US&version=7.02.22
[21] Steve Portigal. 2013. Interviewing users: how to uncover compelling insights . Rosen-
feld Media, New York.
[22] Alper Sarikaya, Michael Correll, Lyn Bartram, Melanie Tory, and Danyel Fisher.
2019. What Do We Talk About When We Talk About Dashboards? IEEE
Transactions on Visualization and Computer Graphics 25, 1 (Jan. 2019), 682–692.
https://doi.org/10.1109/TVCG.2018.2864903
[23] E Segel and J Heer. 2010. Narrative Visualization: Telling Stories with Data. IEEE
Transactions on Visualization and Computer Graphics 16, 6 (Nov. 2010), 1139–1148.
https://doi.org/10.1109/TVCG.2010.179
[24] Helen Sharp, Jennifer Preece, and Yvonne Rogers. 2019. Interaction Design (5 ed.).
John Wiley & Sons, Inc.
11

[25] Valerie Sheppard. 2020. Analysis of Qualitative Interview Data. (April
2020). https://pressbooks.bccampus.ca/jibcresearchmethods/chapter/10-5-
analysis-of-qualitative-interview-data/ Book Title: Research Methods for the
Social Sciences: An Introduction.
[26] Ben Shneiderman. 1996. The Eyes Have It: A Task by Data Type Taxonomy for
Information Visualizations. (1996). #op/acc/revisar 
12

APPENDIX
An online version of the appendix is also available through this link.
A LANDSCAPE ANALYSIS
Blockbax
Link to Blockbax documentation here.
Table 5: Strengths and Weaknesses of Blockbax
Strengths Weaknesses
• Able to add map layers such as floor plans and technical drawings
• Wide range of off-the-shelf visualizations
• Event explorer allows finding the root cause of an event
• Immediate notification via email, app, and web
• Customizable dashboards accessible by role
• Low code functionality
• Ability to forecast and calculate metrics
• Price: 1695 EUR per month for the Core plan, 3295 EUR for the
Advanced plan
• Requires JavaScript knowledge for custom payload integration
• Limited to built-in off-the-shelf visualizations
• Excessive customization may lead to information overload or de-
cision fatigue
Metrikus
Link to Metrikus documentation here.
Table 6: Strengths and Weaknesses of Metrikus
Strengths Weaknesses
• Focus on speeding up data integration process
• Available as a public API as well as an app
• Helps reduce resource consumption by monitoring key environ-
mental, social and governance criteria (ESG) metrics
• Helps reduce costs and increase productivity
• Main focus currently lies with industries such as commercial real
estate, healthcare, and data centers
• Lack of forecast metrics and opportunities
• Lack of own/no user customization, all of it is done by Metrikus
OpenRemote
Link to OpenRemote documentation here.
Table 7: Strengths and Weaknesses of the OpenRemote
Strengths Weaknesses
• Dashboards available in app as well as on desktop
• Multi-tenant roles (Multi-tenancy access)
• No code needed
• Able to style the interface to match your brand
• Allows for communication with external devices and services with
manager APIs, protocol agents, and gateways and access
• Possible learning curve with their flow and groovy rules, as well
as with their when-then rules for adding automation and alarms
•
Too much interface customization could cause information over-
load/decision fatigue if companies try to fit everything on their
dashboard
• Lack of predictive/forecast metrics
13

BluWaveAI
Link to BluWaveAI documentation here.
Table 8: Strengths and Weaknesses of BluWaveAI
Strengths Weaknesses
• Load Predictor offers advanced capabilities for accurate load fore-
casting, including intra-day and day-ahead predictions, taking
into account multiple weather sources, holidays, and other rele-
vant data.
• Wind predictor and solar predictor
• The flexibility of the Smart Grid Optimizer allows it to adapt and
control a wide range of devices within the smart grid ecosystem,
facilitating efficient energy management, grid stability, and cost
optimization.
• Interoperability
• Lack of own customization that users can do themselves; cus-
tomization is done by the expert team.
• No direct mention of including maps and geospatial data in the
dashboard.
• No mention of a notification system.
• No mention of whether the dashboard is available in multiple
formats such as API, app, etc.
14

B INTERVIEW GUIDE
Introduction
Hello, my name is Givannah Noor and I am an Information Science Master’s student at the Vrije Universiteit Amsterdam. Today, I would like
to discuss your role as a building manager or relevant stakeholder to gather further insights for designing a dashboard for the Arnhems
Buiten case, building upon Matteusz’s work.
Participant Background/Overview
(1) Can you tell me a bit about yourself? What is your role? What do you do?
(2) Have you seen the Grafana dashboard made by Matteusz?
a. If yes: What do you think of it? What do you like and what do you dislike about the Grafana dashboard?
b. If no: (Show a screenshot of the dashboard) What do you think of it? What do you like and what do you dislike about the Grafana
dashboard?
(3) How are you accustomed to viewing data? What type of data visualizations are you/they familiar with?
(4) Do you have prior experience with monitor dashboards or data visualizations?
Main Body: Exploring Specific Topics
Building Manager Tasks
(1) Tell me about your day-to-day schedule or workday. Describe the day-to-day schedule of building managers.
(2) Describe the problems or tasks you are trying to achieve/solve as a building manager.
a. If a task/problem is mentioned: How did you obtain the needed information?
(3) How much time do you typically spend on your tasks as a building manager?
(4) How do you keep track of maintenance schedules, safety checks, or equipment performances?
(5) How often do you need to collect or review building-related data?
(6) What is the hardest part of your job?
a. What are you doing to make it easier?
Current Situation: Usage of System
(1) What tools/systems do you currently use to access, manage, and collect information?
a. Do you already have a dashboard system?
(2) How do you check the tools/system?
a. Is it on a computer, mobile device, tablet, etc.?
b. If no system exists: How would you like to check the tools/system?
(3) Are you the only person using the system/tool, or are other stakeholders involved?
a. If no system exists: Would you be the only person using the system?
(4) What type of information do you gather or monitor most frequently?
(5) What metrics are important for you to see?
(6) What context does each metric require to make it meaningful?
Projection/Dream/Hypothetical Questions
(1) What problem are you looking to solve with the dashboard?
(2) How can a user dashboard improve your experience? How can it make your job easier?
(3) Do you work with or expect to work with a lot of temporal or geospatial information?
(4) What is the time scale for decision-making you work with or expect to work with?
a. Is there a lot of time pressure? Do decisions need to be made really fast?
(5) How do you want to view the data?
a. Pie charts, scatter plots, heat maps, etc.?
(6) If you could build your ideal dashboard experience, what would it look like?
Wrap Up
(1) Did I miss anything? Is there anything else you want to tell me?
(2) Is there anything you want to ask me?
Thank you so much for making time for this interview. Your contribution is very valuable and much appreciated.
15

C USER STORIES
As a [persona], I want to [goal or action], so I can [outcome or reason]
US-1. As a property manager at Arnhems Buiten, I want to check the energy meters often, so I can make sure we are paying the correct
amount of money to the energy providers.
US-2. As a property manager at Arnhems Buiten, I want the data overview and invoices in one platform, so I can easily make sure we are
paying the correct amount of money to the energy providers.
US-3. As a property manager at Arnhems Buiten, I want to be notified of any anomalies or faults immediately, so I can help prevent power
outages and voltage fluctuations.
US-4. As a property manager at Arnhems Buiten, I want to be notified if we are going to exceed the grid capacity, so I can prevent paying
for a penalty.
US-5. As a property manager at Arnhems Buiten, I want an overview of all available data, so I can understand why there is a peak above the
average usage.
US-6. As a property manager at Arnhems Buiten, I would like to see an overview of the energy prices per hour of today and the following
day, so I can help shift peak moments of energy usage to a time where the prices are lower to save on energy costs.
US-7. As a property manager at Arnhems Buiten, I want real-time data of the energy consumption, so I can pinpoint the usage and
consumption of a specific tenant so the whole park does not pay for just a specific tenant.
US-8. As a property manager at Arnhems Buiten, I would like advice and analysis of what the system is going to do, so I can advise tenants
to act accordingly.
US-9. As a property manager at Arnhems Buiten, I want to have the forecasted costs and energy prices for the following day, so I can advise
tenants to act accordingly.
US-10. As a property manager at Arnhems Buiten, I want to see all the needed data on one platform, so I do not have to log in to multiple
different systems or platforms.
US-11. As a property manager at Arnhems Buiten, I want to look at the map, so I can easily tell where all the buildings and energy nodes are
on the property.
US-12. As a property manager at Arnhems Buiten, I want to see the value of the use of electric and gas, so I can see the differences in usage
after a new installation has been installed.
US-13. As a property manager at Arnhems Buiten, I want to see historical data, so I can compare the current usage with the usage of the past.
US-14. As a property manager at Arnhems Buiten, I want my tenants to be able to check their own electricity usage, so I can have more time
to focus on other tasks than sending out updates to the tenants.
US-15. As a property manager at Arnhems Buiten, I want to know how many people are in the building every day, so I can help reduce
energy costs based on the amount of people in the building.
US-16. As a property manager at Arnhems Buiten, I want to have all the necessary data in one platform, so I can check the data more often.
US-17. As a property manager at Arnhems Buiten, I want the dashboard system to be fast, so I do not have to wait to see something change
when interacting with the dashboard.
US-18. As a property manager at Arnhems Buiten, I want to easily be able to add additional datasets, so I can customize the information I
need from the dashboard.
US-19. As a property manager at Arnhems Buiten, I want different views for the administration and the tenants, so I can see the relevant
information for me depending on my role.
US-20. As a property manager at Arnhems Buiten, I want help with correlating business cases upfront, so I can make the right business
investments.
US-21. As a property manager at Arnhems Buiten, I want to see the impact of new installations, so I can decide if action is needed.
US-22. As a tenant at Arnhems Buiten, I want to be able to see what Arnhems Buiten is doing on the energy/sustainability front, so I can be
aware of how I can contribute as well.
US-23. As a tenant at Arnhems Buiten, I want real-time analysis of energy consumption, so I am aware of my own energy usage and
consumption.
US-24. As a tenant at Arnhems Buiten, I want a simple and appealing view of the energy data, so I can easily understand what is going on.
US-25.
As a tenant at Arnhems Buiten, I want a dashboard with a cartoon figurine to explain to me what is going on with the data, so it is
more fun and easy for me to understand.
US-26. As a tenant at Arnhems Buiten, I want a quick one-perspective overview of the data, so I can better understand if we are doing good
or not.
US-27. As a tenant at Arnhems Buiten, I want a quick one-perspective overview of the data, so I can better understand what I can do to help
lower the energy usage and consumption.
US-28. As a tenant at Arnhems Buiten, I want to know if my energy usage is above my usual average consumption, so I can know that I must
pay more.
US-29. As a tenant at Arnhems Buiten, I want to know if my energy usage is approaching above my average consumption, so I can act
accordingly to save on energy costs.
16

US-30. As a tenant at Arnhems Buiten, I want an overview of my energy usage in a dashboard, so I can frequently check my energy usage
independent of the property managers’ monthly overviews.
US-31. As a tenant at Arnhems Buiten, I want a user-friendly app, so I can check my energy consumption wherever I am.
17

D IDEATION PROCESS
HMW Questions
(1) How might we let administrators easily access the building energy meter data?
(2) How might we increase energy behavior awareness for tenants and administrators?
(3) How might we use historical data to increase energy optimization?
(4) How might we help administrators understand the data better?
(5) How might we make complex data easier to understand?
(6) How might we provide administrators and users with all the needed information?
Figure 7: HMW questions and associations
18

Crazy8
Figure 8: Crazy8 ideation method
19

Sketches chosen concept
Figure 9: Initial sketches
Figure 10: Sketches and information architecture
20

E WIREFRAMES
Figure 11: Overview page wireframe
 Figure 12: Zoom-in page wirframe
Figure 13: Insights page wireframe
 Figure 14: History page wireframe
21

F USER EVALUATION GUIDE
The prototype can be accessed through this link.
IMPORTANT INFORMATION TO DISCLOSE
• Ask for permission to record audio.
• Participation is completely voluntary.
• The data will only be used for this study.
• The prototype was made with some dummy data, so do not pay too much attention to whether the data makes sense or not.
• We will start with you looking at the prototype and providing general feedback. Then, we will move on to three scenarios/tasks, and
close with a short satisfaction/usability survey.
• I might interrupt to ask some questions.
• Please use the think-aloud technique and tell me everything you are thinking while doing it.
TASKS
Scenario: Overview Page
• You log in for the first time on the dashboard today.
• You did not check the dashboard yesterday since you had a day off. You are curious to see which building had a critical event the day
before.
• Question: Which building has critical events on November 18?
– Answer: B31
• You also want to know which building is doing alright and requires no further attention today on November 19.
• Question: Which building is it? How much energy has that building saved of the energy-saving goal for that building?
– Answer: B42 and 30% of the goal was saved (150 kWh).
Scenario: Insights Page
• You are aware that today (Nov 19) you used a bit more energy than you would have hoped.
• You are curious to see how much energy you are predicted to use tomorrow.
• Question: How much energy is Arnhems Buiten predicted to use on Wednesday, November 20?
– Answer: 1850 kWh
Scenario: History Page
• It is the end of the year, and you receive a bill from the energy provider. On the bill, it states your costs for June were 7,000 EUR.
• You want to double-check on the dashboard if that is true.
• Question: According to the dashboard, what was the total cost in June?
– Answer: 6,230 EUR
22

G SCREENSHOTS OF FINAL HI-FI PROTOTYPE
Figure 15: Overview page
Figure 16: Zoom-in page
23

Figure 17: Insights page
Figure 18: History page
24
```
