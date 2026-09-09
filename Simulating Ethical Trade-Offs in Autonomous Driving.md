---
title: Simulating Ethical Trade-Offs in Autonomous Driving
author: John Mocettini, Atia Cortés, Luis Oliva-Felipe, Sergio Álvarez-Napagao
year: "2025"
Type: Proceedings Article
DOI: 10.1109/iv64158.2025.11097552
source: https://doi.org/10.1109/iv64158.2025.11097552
created: 2026-05-05
description: ""
tags:
  - op/acc/pending-review
pdfORepub: "[[Simulating Ethical Trade-Offs in Autonomous Driving.pdf]]"
---
[[Simulating Ethical Trade-Offs in Autonomous Driving.pdf]]
## Full text (extracted from `Simulating Ethical Trade-Offs in Autonomous Driving.pdf`)

*Source:* `2PDF/Simulating Ethical Trade-Offs in Autonomous Driving.pdf`  
*Extracted:* 2026-05-05

```text
Simulating Ethical Trade-offs in Autonomous Driving
John Mocettini1, Atia Cort ´es*2, Luis Oliva-Felipe 2 and Sergio ´Alvarez-Napagao1,2
Abstract— As autonomous vehicle (A V) technology advances,
ethical questions surrounding its implementation and inte-
gration become increasingly apparent. This work explores
the potential of leveraging CARLA, an open-source driving
simulator for A Vs in urban environments, to simulate ethical
dilemmas that could occur in real-world self-driving car scenar-
ios. A scenario depicting a more likely, less emotionally loaded
ethical dilemma was desired in response to A V ethics’ seeming
overfocus on the Trolley Problem. Additionally, the framing of
the chosen dilemma as a trade-off became a central concept and
contribution of the work. Brief reviews of the existing A V ethics
literature and key technologies are provided, and similar works
described. Then, a scenario involving an ambulance exiting a
congested highway is defined and implemented with the specific
ethical trade-off of privacy vs. efficiency in mind. Vehicle-to-
vehicle (V2V) communication levels are used as markers of
privacy, while the elapsed simulation time for the ambulance to
reach its goal measures efficiency. Thus, the privacy-efficiency
trade-off is evaluated at different levels of privacy sacrifice,
where privacy can be discussed qualitatively and efficiency
quantitatively. Experimental results determine that the simula-
tion grows more efficient as privacy sacrifice increases, though
partly due to biases in devised agent behaviors. The use of a
trade-off for analysis in combination with simulation software is
emphasized as the most significant contribution and encouraged
for future A V ethics work.
I. INTRODUCTION
Autonomous Vehicle (A V) technology has great potential
to improve the efficiency and safety of how humans transport
themselves on a daily basis. In 2015, the National Highway
Traffic Safety Administration in the US found 94% of crashes
had driver-related failure as the critical reason for the acci-
dent [1]. In addition to this, the World Health Organization
identified road traffic injuries as the leading cause of death
for children and young adults aged 5-29 years and reports the
annual global death toll among all age ranges to have reached
1.35 million in 2018 [2]. Thus, there is much support for
A V advancement and an expectation for rapid improvement
alongside other revolutionary AI techniques such as the use
of Large Language Models (LLMs). In addition to saving
lives by removing human error from driving, A V proponents
argue the development and public adoption of self-driving
cars will free up commute time [3], improve traffic flow
efficiency [4], and even reduce harmful emissions on the
environment [5]. However promising, the integration of such
systems into society will not be easy.
Aside from the technical challenge of developing effec-
tive driving systems, A Vs face obstacles on their path to
widespread use such as ethical dilemmas, legislation, and
1Universitat Polit`ecnica de Catalunya, Barcelona, Spain
2Barcelona Supercomputing Center, Barcelona Spain. Atia Cort ´es is
corresponding author atia.cortes@bsc.es
public acceptance. Simulation technology is one popular
method to aid in preparing for these obstacles. It has be-
come a prevalent technique for testing A V systems, with
game engines such as Unreal Engine or Unity3D allowing
the creation of high-fidelity environments for testing, while
maintaining low cost compared to real-world vehicle tests
which may be expensive or dangerous. Recently, some
academic work has been done to leverage simulation in A V
ethics discussions (see §III).
Upon reviewing the existing literature on the crossover
between A V ethical dilemma discussion and concretely im-
plemented simulations to analyze dilemmas, there appears
to be a gap in the research. Far less attention has been
paid to simulating ethical problems that will be encountered
regularly should A Vs become ubiquitous in society, in favor
of more emotional ones such as the Trolley Problem. The
aim of this paper is to study the relation of privacy with
other requirements such as efficiency and safety. While not as
emotionally charged as life-and-death scenarios, these kind
of situations will certainly affect A V users extensively.
The concept of an ethical trade-off is key for analy-
sis, and the present study emphasizes its importance in
evaluating A V systems when performance metrics can be
weighed against ethical concerns. By framing an ethical
dilemma as a trade-off, engineers, policymakers, and the
general public can inform decisions regarding A V design,
legislation, and use, respectively. The former represents a
situation where a decision must be made between two or
more competing ethical principles, where choosing one often
entails sacrificing the other. The latter describes the balancing
act between two competing but not necessarily mutually
exclusive ethical concerns. Being less about an all-or-nothing
choice, it suggests different system configurations can reflect
degrees of compromise.
Privacy is of growing concern in many applications of AI,
and can sometimes be undervalued because it is intangible,
or difficult to quantify. Additionally, different end-users may
prioritize or value their privacy at varying levels. In the
field of A Vs, there is a clear concern over data privacy
on the technical side of vehicle systems, especially as the
possibility of inter-vehicle communication looms (see II).
Due to the prominent role of vehicles in humans’ daily
lives, sacrificing privacy can take shape in other ways, such
as ceding control of the vehicle to a computer (e.g. fully
autonomous) – or another human or computer pilot. Being
something all users will be affected by, and all A V designers
or policymakers should be aware of, privacy was selected
as one side of the trade-off to simulate. On the other side,
a comparatively measurable and understandable concept of
2025 IEEE Intelligent Vehicles Symposium (IV)
June 22-25, 2025. Cluj-Napoca, Romania
979-8-3315-3803-3/25/$31.00 ©2025 IEEE 2490
2025 IEEE Intelligent Vehicles Symposium (IV) | 979-8-3315-3803-3/25/$31.00 ©2025 IEEE | DOI: 10.1109/IV64158.2025.11097552
Authorized licensed use limited to: Universitat de Barcelona. Downloaded on May 05,2026 at 07:59:11 UTC from IEEE Xplore.  Restrictions apply. 

efficiency was chosen. In other words, how fast a vehicle or
driver can reach its goal destination. With this trade-off in
mind, a scenario can be formulated to showcase it, and a
simulation implemented to analyze it. This experiment will
be done using CARLA, an open-source autonomous driving
simulator.
The remainder of this work will take the following struc-
ture. In §II key background information is presented on A V
ethics, a specific ethical concern relating to technology likely
to be prevalent in the field, and the simulation technology
used in this work. §III introduces the most relevant academic
works and how they relate to the present study. The methods
for designing the scenario and the variable levels of agent
behavior are detailed in §IV, along with the details of the
implemented simulation. The results of the simulation are
presented and analyzed in §VI. Finally, conclusions about
the study are drawn, and directions for future research are
outlined in §VII.
II. BACKGROUND
A. The Trolley Problem
The Trolley Problem is a moral thought experiment de-
veloped by Philippa Foot in 1967 [6] and has since been
expanded by others such as Thomson in 1985 [7]. The
problem consists of a decision maker choosing to sacrifice
the few or the many, where prioritizing the most saved
lives requires taking action, and the decision of inaction
results in more innocent lives lost. This thought experiment
raises questions about utilitarianism and action versus in-
action, among others. Its vehicle-centric nature lends itself
to discussions in A V ethics, as A Vs will undoubtedly face
situations where innocent lives are lost, perhaps in cases
where a programmed machine is the decision-maker rather
than a human.
The most famous study related to this topic is the Moral
Machine experiment, conducted by MIT in 2016 [8]. Sub-
jects who participated in an online survey were presented
with a series of Trolley-like dilemmas where a choice
is required for the hypothetical vehicle to either continue
straight or swerve into the adjacent lane, with no option
to brake in either case. The study garnered much attention
and received millions of responses, where statistical analysis
revealed trends such as cross-gender preference for sparing
females or Western countries prioritizing sparing younger
characters.
Many recent scientific works in A V ethics are based on
Trolley-like scenarios, and so many discussions are published
arguing whether or not this problem is useful to focus on.
Undoubtedly, this type of problem has heightened societal
awareness on the implications of A V decision making. They
also raise important questions over design decisions, public
opinion, and liability. On the other hand, [9] claims Trolley
Problems represent an ”engineering and policy distraction”,
”cannot be reliably detected by any real-world perception
system”, and that social experiments such as the Moral
Machine ”do not accurately reflect anyone’s opinion”, citing
the framing of the survey as flawed with its all-or-nothing
approach.
B. V2V and Privacy
One of the most promising techniques for improving A Vs’
driving and safety capabilities is Vehicle-to-Vehicle (V2V)
communication. Enabling A Vs to communicate with each
other and with other roadway infrastructure will allow traffic,
hazard, or emergency information to be detected even the
notified vehicle is out of range or obstructed from the source.
Additionally, risky vehicle maneuvers can be coordinated
between agents, improving safety and efficiency.
This method would require data transmission between ve-
hicles and other IoT devices. As such, data privacy becomes
of utmost concern in the application of V2V methods in A Vs.
Much sensitive information will power highly-functioning
A V systems and needs to be handled properly and safely to
foster trust and eventual widespread adoption. In fact, the EU
Commission recognizes vehicle broadcast data as personal
data, subjecting data to privacy legislation like the European
Union’s General Data Protection Regulation (GDPR), thus
requiring users to knowingly consent to allow the transfer
and use of such data [10]. While there is, therefore, some
precedent for protecting this data, the context of A Vs presents
new challenges. For instance, A Vs often employ cameras or
sensors to detect their environment, and the data can often
contain the faces of other drivers or pedestrians who, in most
cases, would be unable to consent to their personal data being
used knowingly.
This privacy issue raised by A Vs has worrying impli-
cations, and will not be easy to overcome. Aside from
personal liberty and legislative concerns, in [11], a survey
was conducted on city residents to gauge public feeling over
different aspects of A Vs. It found that participants found
privacy scenarios to invoke the most discomfort, with 85%
of respondents being uncomfortable with image capture and
77% uncomfortable that data were being aggregated and
analyzed. In addition, it found that more than half of the
participants would spend more than five minutes to opt out of
data collection online, if that were an option. Other worrying
incidents regarding remote control of car functionality have
been reported, such as prior owners having continued access
to their old car’s system [12]. Causes of discomfort like this
can be seen as massive challenges to the eventual adoption
of A V systems, as widespread public acceptance will be
crucial for their successful adoption. With sensitive personal
data bound to be transmitted, such as in communicative A V
carpool systems, users will need to trust the service provides
some level of anonymity [13].
III. RELATED WORKS
The most similar existing work to the present study is
[14], which also focuses on quantifying different ethical
outcomes in vehicle decision making through simulation.
The paper analyzes a simulation of a Trolley-type scenario,
where the action taken is determined by one of four ethical
frameworks: utilitarianism, ethical egoism, moral machine,
2491
Authorized licensed use limited to: Universitat de Barcelona. Downloaded on May 05,2026 at 07:59:11 UTC from IEEE Xplore.  Restrictions apply. 

or virtue ethics. Probabilities are used to define the outcome
of each action, using real-world statistics like fatality rates for
different age ranges. Information about neighboring vehicles
such as number of passengers and their ages is shared,
forming a type of V2V communication that advises each
ethical framework in making a decision.
The stated purpose of this work was not to argue for or
against certain ethical frameworks, but rather to show how
programming different ethical frameworks into the decision-
maker of an A V has profound effects on the outcomes. In the
simulation, self-sacrificing decisions resulted in the fewest
total fatalities. Notably, different simulation parameters could
result in a framework always choosing the same action. In
one example, self-sacrifice was always chosen if the likeli-
hood of the decision maker’s vehicle rolling was low enough,
raising an interesting question about whether utilitarianism
could disincentivize vehicle safety by car manufacturers.
Although the Trolley-type scenario could be criticized for its
realism and applicability to A V development, Mordue et al.
[14] demonstrate the complex outcomes and ethical questions
that programming ethics into A Vs gives rise to.
In [15], Himmelreich discusses Trolley Problems and their
applicability, while also comparing them to the ethical prob-
lems faced in mundane situations that are more aligned with
the present study’s focus. He notes that even the most routine
of driving situations are extremely complex – something the
focus on analyzing Trolley Problems fails to capture. The
current work selects a specific mundane driving scenario to
analyze as an ethical trade-off.
TrolleyMod [16] similarly uses the CARLA simulator,
but again focuses on Trolley-like moral dilemmas, focusing
on immersing the participant in the scenario, similar to the
CARLA simulation using VR done in [17].
IV. METHODS
A. Scenario Design
To effectively confront the trade-off, a scenario had to be
devised to portray it. The scenario designed for this study
takes place on a highway, where an ambulance attempts to
navigate through traffic to reach the next exit. A straight
portion of a four lane highway in a CARLA provided map
was chosen in order to give multiple opportunities for lane-
change interactions between vehicles.
By including an emergency vehicle, this imposes a sense
of urgency as well as a figure of authority on the scenario.
In real life, it is common that normal drivers recognize the
importance of these vehicles, and are primed to react and
yield to them if necessary. A general desire for facilitating
the speedy movement of these vehicles can normally be
assumed. This contributes to the core idea of the ethical
trade-off, that the efficiency and safety of the ambulance
should be maximized, and that other normal vehicles may
be more willing to give up privacy in order to achieve this
than they would in interactions with non-emergency vehicles.
Some key features of the highway scenario include: Road
Options, having multiple lanes to facilitate lane-change
maneuvers; Traffic Density, varying the amount of vehicles
in the same stretch of road to observe agent behaviors in
different levels of congestion; and Ambulance Objective ,
where the ambulance’s goal is to successfully take the next
exit as soon as possible, reflecting the sense of urgency a
real ambulance would have.
This scenario was designed so that the ethical dilemma
posed by privacy concerns could be explored, with the
particular goal in mind of the ambulance quickly reaching
the exit.
B. Agent Behaviors
The behaviors of agents in this highway scenario are
critical for simulating privacy sacrifices. Different levels of
communication between the ambulance and other vehicles
represent varying degrees of privacy given up. The imple-
mented agent behaviors are used to emulate these varying
levels of communication. Behaviors are implemented in
code using CARLA’s Traffic Manager together with custom
classes used in Scenario Runner.
Three levels of behavior/communication were defined:
• Level 1 (L1): No Communication: Vehicles drive
autonomously and do not communicate with the am-
bulance. This level depicts a total protection of privacy.
• Level 2 (L2): Message Passing with Option to Reject
Slow Down: The ambulance sends a request for a
blocking vehicle to yield to it by slowing down. The
blocker can decide whether to accept or reject this
request. A sub-level of depth is added by introducing
the concept of benevolent and selfish vehicles:
– Benevolent vehicles will tend to prioritize the
ambulance’s goal, accepting slow down requests
the majority of the time
– Selfish vehicles will behave in the opposite fashion,
rejecting slow down requests more often
This level represents a middle ground, where vehicles
adopt a system of message passing, but they maintain
autonomy over their decisions and actions.
• Level 3 (L3): Full Control: Blocking vehicles allow
the ambulance to dictate their actions. When the ambu-
lance faces a blocker, it forces the blocking vehicle to
slow down. This represents the most substantial privacy
sacrifice as autonomy is completely given up for the
greater good, implying intense levels of data access and
control in a real life system.
With the inclusion of benevolent and selfish agents in L2,
it was broken into three different scenario configurations to
evaluate different proportions of the two agent types. These
sub-levels are L2A, L2B, and L2C, arbitrarily decided to be
made up of 20%, 50%, and 80% benevolent vehicles, respec-
tively, where the complement of each benevolent percentage
is the proportion of selfish vehicles. This expansion was
made to investigate whether, within L2, if some threshold
of benevolent agents existed where increasing the proportion
had diminishing returns.
Each level of privacy sacrifice is thus modeled by changing
the behaviors of agents. As communication and control grow
2492
Authorized licensed use limited to: Universitat de Barcelona. Downloaded on May 05,2026 at 07:59:11 UTC from IEEE Xplore.  Restrictions apply. 

stronger, more privacy is given up in an effort to fulfill the
ambulance’s goal.
C. ODD Specified Model
The Overview, Design Concepts, Details protocol [18] is
used to convey the realized simulation, while also promoting
transparency and reproducibility. The model, submodels (in-
cluding agent behavior diagrams), associated code, and video
demonstrations are publicly available from the project’s
GitHub repository1.
Fig. 1. Basic Simulation Architecture Showing ScenarioRunner and
CARLA’s Relationship
V. EXPERIMENTAL DESIGN
Three levels of traffic density were applied to the five
configurations, for a total of fifteen combinations to evaluate.
All trials were run on CARLA and ScenarioRunner version
0.9.15 using a Windows 10 computer with 32GB of RAM,
an Intel i7-8700k processor, and an Nvidia RTX 2080 GPU
with 8GB of dedicated RAM. An overview of the simulation
architecture can be seen in Fig. 1.
For each combination of communication level and traffic
density, 100 trials were executed, and their results saved. For
L1 and L3, these recorded values were Trial Number, Total
Vehicles, Ambulance Arrival Time , Ambulance Arrival Suc-
cess, Total Collisions, Ambulance Collisions , and Blocking
Vehicles Encountered. For L2, the additional fields of Benev-
olent Vehicle Count, Selfish Vehicle Count, Blocking Vehicles
Who Accepted Slowdown Requests , and Blocking Vehicles
Who Rejected Slowdown Requests were also recorded.
Vehicles start locations were randomly selected from a
pool of pre-determined spawn points. Each vehicle’s start
speed was randomly chosen between a pre-defined range,
with the exception of the ambulance start speed being
constant. All constants including simulation frame rate, min-
imum and maximum vehicle speeds, ambulance speed, and
1GitHub URL: https://github.com/jmoss7/
ThesisHighwaySimulation
slowdown speeds are kept consistent across configurations.
Notably, the Ambulance Arrival Time metric is explained
by measuring the time from simulation trial start until the
ambulance arrives at a pre-determined spot in the goal
exit lane that is consistent across all trials. Additionally,
benevolent vehicles were assigned a distinct 3D model to be
visually distinguishable from their selfish counterparts (see
Fig. 2).
Fig. 2. An Aerial View of the Start of an L2B Simulation Trial (White
Ambulance, Red Benevolent Vehicles, and Blue Selfish Vehicles)
VI. RESULTS & ANALYSIS
A. Communication’s Effect on Efficiency
As the levels of communication between the ambulance
and other actors rise, the time it takes the ambulance to exit
the highway successfully falls. Fig. 3 shows the resultant
average ambulance arrival time across 100 trials for each of
the three levels of traffic density. Across all three, a clear
downward trend is observed in exit time as communication
level rises, with some slight discrepancies between the vari-
ants of L2.
In weighing the trade-off of data privacy versus navigation
efficiency, this result lends itself to the argument that giving
up more data may be worth its cost. L3 involves allowing
total remote control over blocking vehicles, and results in
the fastest average ambulance arrival times. This optimal
result in terms of efficiency must be weighed against how
severe the privacy implications of allowing total control are.
L2, enabling communication consisting of requests from the
ambulance for the blocking vehicle to slow down that can be
accepted or rejected introduces a middle ground, where the
other vehicles maintain their autonomy while being willing
to broadcast and receive messages. This level performs a
bit worse than L3 in average ambulance exit time, while
outperforming L1. In L1, neither party implements any sort
of messaging or allowance of control, relying solely on the
ambulances ability to navigate the traffic. This configuration
performed the worst by far.
One flaw that becomes apparent in evaluating efficiency is
the inevitability of fewer ambulance decelerations occurring
as the communication level increases, due to the behavior
design. In L3, the ambulance never decelerates. In other
formulations of the scenario, such as with a shorter stretch
2493
Authorized licensed use limited to: Universitat de Barcelona. Downloaded on May 05,2026 at 07:59:11 UTC from IEEE Xplore.  Restrictions apply. 

Fig. 3. Average Ambulance Arrival Time vs Communication Level for all Configurations
of highway, this behavior implementation could have led
to worse statistics, like failing to merge all the way to
the right in order to take the exit. However, in the present
implementation, this lack of slowing combined with forcing
blocking vehicles to yield results in a nearly absolute win in
terms of ambulance efficiency.
This analysis identifies quite a major flaw in the exper-
imental design, simply due to the way the different levels
of behavior were designed. Too much of the primary perfor-
mance metric of required exit time relied on the ambulance’s
slowing down, or lack thereof. That being said, this oversight
in failing to isolate the variable of behavior/communication
level does not render the experiment nor its analysis useless.
In fact, this outcome highlights the fact that analyzing an
ethical trade-off centered on a topic like privacy will be
very challenging in the real world, and the systems being
compared will not always be equal, or competitive with each
other on certain metrics. The purpose remains to consider
the sacrifice of privacy in light of efficiency improvements,
which this work maintains is possible via simulation.
B. L2 Benevolence
The L2 version of the simulation emulates how in a
real-world road environment, only certain percentages of
actors may decide to implement certain driving technologies.
Although for the purposes of implementing the scenario even
Fig. 4. L2 Configurations’ Avg. Ambulance Arrival Times vs Traffic
Density
selfish actors communicate with the ambulance by message,
it can be imagined that they represent A V owners who opt-
out of privacy sacrificing measures that promote public safety
or efficiency. This begs the question of whether these actors
have a detrimental effect on the roadway, or efficiency in the
simulation, or if some ratio of benevolent to selfish actors
is most effective or worth the trade-off involved. The three
proportions of 20%, 50%, and 80% benevolent actors were
chosen to investigate such a question.
Based on the prior discussion on how L3 dominates the
efficiency metric due to its lack of slowdowns, it is curious
that configuration L2C outperformed L3 with a traffic density
of 16 (Fig. 3). On top of that, it is very interesting that
this variant of L2 is only the best L2 performer in terms of
ambulance exit time in the highest traffic density case, yet
L2B is the best L2 version under both of the other traffic
conditions (Fig. 4). In no cases does the 20% benevolent
L2A configuration outperform the other two. Perhaps this
indicates that in situations of higher congestion, the ambu-
lance slowing down more rarely allows it to escape clogs
in the road, and move to the front of the pack more easily.
With the way the simulation is implemented, getting stuck
behind a slower vehicle could be a major cause of longer
exit times. In the two lower traffic density cases, maybe the
landscape with 50% of vehicles being benevolent ended up
with easier traffic patterns for the ambulance to navigate.
This L2B configuration performed substantially better than
the 80% benevolent case at the lowest traffic density, yet
these results were flipped for the highest.
The concept of benevolence influencing A V decisions is
also interesting in that it mimics cooperation or its absence
in society. In terms of privacy, a high level of cooperation
(e.g. L2C) may require a large sacrifice in order to function
properly. In future real-world A V systems, governments may
attempt to incentivize cooperative behavior, which could
come at a cost to user privacy and/or autonomy. Using the
simulation results as an example, perhaps situations of lower
traffic congestion may not require high levels of cooperation,
but a higher proportion of benevolent vehicles may have a no-
ticeable effect in high traffic scenarios. Reminiscent of game
theory concepts like the prisoner’s dilemma, drivers would
have to make decisions weighing their potential outcomes by
2494
Authorized licensed use limited to: Universitat de Barcelona. Downloaded on May 05,2026 at 07:59:11 UTC from IEEE Xplore.  Restrictions apply. 

being selfish or cooperative while also being influenced by
external factors such as governmental or societal pressure.
Here, the data given up is merely acceptance or rejection
message passing, but this can be seen as a proxy for real life
situations where more sensitive data is at stake, including
position, destination, or personal information. Considering
this trade-off in the context of specific situations is vital to
determining whether or not sacrificing privacy for efficiency
is worth it in that particular instance.
C. Analyzing the Trade-off
In this analysis, the trade-off between privacy and ef-
ficiency is evaluated by comparing the numeric efficiency
data to the implied privacy concessions at each configuration
level. Even here, it is not clear whether or not the sacrifice
is ever worth it -– that decision would be left up to the
government, company, or individual operating the vehicle
and putting their privacy at risk. However, this study argues
that more similar work ought to be done to provide evidence
for that decision, to attach real data to this “worth”. In the
real world, the modeling of privacy sacrifices will be much
less obvious, and unless private businesses are incentivized
to make the risks clear, consumers may not recognize the
trade-off.
At the highest level of communication, L3, there is a
complete relinquishing of control, where the emergency
vehicle manages other vehicles without the need for real-time
acceptance. While highly efficient, this is a huge sacrifice
of autonomy, as the blocking vehicle’s decisions are totally
overridden for the sake of the ambulance’s movement. It
may be argued through different ethical frameworks such
as utilitarianism (maximizing net output good) or virtue
ethics through the lens of compassion (assuming helping
the ambulance will speed up its ability to help an injured
person, who should be prioritized). These approaches could
be used as the basis for arguing for this privacy sacrifice due
to the improved efficiency of ambulance arrival. This idea is
reminiscent of the prior discussion on moral dilemmas such
as the Trolley Problem and Moral Machine experiment. On
the other hand, by thinking specifically about the amount
of privacy given up to achieve this outcome, the present
topic diverts slightly from these thought experiments, where
real data and submodels can be analyzed and compared in
terms of a trade-off. If the users elect to adopt systems
like L3, informed consent should be obtained, so that users
understand the pros and cons of adhering to them. Relating
back to GDPR, clear communication about how and when
control or data is seized, as well as an evidence-supported
case for why, empowers users to decide what level of privacy
they want, and what data they hand over.
The L2 configurations include more nuanced options that
reflect different balances in the privacy vs efficiency trade-
off. Each sub-level presents varying degrees of cooperation,
with vehicle owners giving a binary choice in real time on
whether to engage in communication, still maintaining full
control over the vehicle’s actions. This idea can be extended
to existing data-sharing protocols, such as users being given
options to accept or decline different settings of internet
cookies requested by a web page. The measured results in
the experiment suggest that, while slightly suboptimal in
terms of efficiency, this “middle ground” is still comparable
to L3, even outperforming it in one case. This suggests
that an A V landscape where flexible options are provided
to users could achieve a good balance between ensuring
privacy and optimizing efficiency. However, the possibility
of more customization and freedom producing worse results
such as those shown by L2A is also apparent, so reaching
an optimal balance may require careful consideration, while
risking negative consequences.
Ultimately, this simulation drills down on the idea of eval-
uating an ethical dilemma by examining an example ethical
trade-off. Simulation experiments such as this one enable
researchers, companies, and policymakers to gather data and
argue for or against certain technologies, weighing each side
of the trade-off. Testing different variables and combina-
tions of parameters or submodels allows the investigation
of hypotheses, while giving rise to unforeseen behaviors
or consequences, resulting in a better understanding of the
tested systems, and how they should be altered or properly
described to stakeholders.
VII. CONCLUSION
A. Contributions
This study has explored a simulated A V ethical dilemma
with a focus on analysis through the lens of a trade-off.
The issue of privacy will be at the forefront of ethical
design of A V systems, and this work presents one privacy
trade-off that can be considered in the evaluation of such
systems. Although simulated, these trade-offs reflect real
world concerns about how personal data and autonomy may
be sacrificed for efficiency or safety, and whether these
benefits are worth the cost.
The focus on privacy in particular is an important con-
tribution of this study, being a subject that is highlighted
for requiring deeper analysis in the A V landscape [19] and
often overlooked by automakers [20]. Using the CARLA
simulator, a concrete experiment was established to simu-
late the sacrifice of privacy with differing communication
levels, reflected in agent behaviors. The outcome of the
simulation was analyzed as a trade-off, attempting to quantify
the balance between privacy and efficiency. Transparency
and reproducibility were emphasized by incorporating the
ODD protocol. Additionally, this work advocates for more
research in the simulation of ethical topics in A Vs, using the
impressive simulation technologies available at a low cost to
advance the field in an ethical manner, and to raise important
questions before they arise due to real driving scenarios.
B. Improvements and Future Work
Additional work to improve the simulation could include
implementing different agent behaviors, enabling more effec-
tive analysis of the privacy efficiency trade-off. Measuring
other data such as collisions could allow the evaluation of
other ethical trade-offs, like safety. Since the simulation is
2495
Authorized licensed use limited to: Universitat de Barcelona. Downloaded on May 05,2026 at 07:59:11 UTC from IEEE Xplore.  Restrictions apply. 

rule-based with stochastic elements, another expansion of
this work would be to develop agent learning behaviors
(e.g. using reinforcement learning). This would also leverage
some CARLA features like cameras and sensors that the
present study does not make use of. In fact, difficulties were
faced in using CARLA’s Traffic Manager, which limited the
kind of trade-off simulations we could analyze. Improving it
or avoiding its use moving forward is recommended.
There are a few avenues for future research stemming
from this study. One of the difficulties in clearly evaluating
the privacy-efficiency trade-off was the lack of a numeric
representation for privacy. This could allow for better clarity
in what is being sacrificed, and therefore a better evaluation
of whether the sacrifice is worth it, depending on the stake-
holders’ perspectives on that regard. Future work to develop
more a more explicit privacy scale or framework would aid
in this regard. Additionally, future work to develop more sce-
narios or edge-cases of the present scenario, possibly testing
distinct dilemmas or trade-offs, would benefit the A V ethics
and simulation research field. Also, considering explicit value
preferences on the considered trade-offs could lead to more
realistic agents’ behaviors; this could support policy-makers
to identify potential challenges. Finally, further investigation
of the impact privacy will have on A V trust and adoption is
recommended to expedite the positive effects A Vs will have
on society. One example of this is through surveys to gauge
public opinion, such as the AI4CCAM online participatory
space 2.
This work intended to present a trade-off, and analyze it
via scenario design and simulation implementation, but not
to claim one side of the trade-off ought to be prioritized.
Making that argument could be another interesting topic for
further academic research.
ACKNOWLEDGMENT
This work is partially funded by the European Commis-
sion through the AI4CCAM project (Trustworthy AI for
Connected, Cooperative Automated Mobility) under grant
agreement No 101076911. Views and opinions expressed
are however those of authors only and do not necessarily
reflect those of the European Union or CINEA. Neither
the European Union nor the granting authority can be held
responsible for them. Additionally, this work is supported
by the AI4S fellowships awarded to Luis Oliva-Felipe as
part of the “Generaci ´on D” initiative, Red.es 3, Ministerio
para la Transformaci ´on Digital y de la Funci ´on P ´ublica,
for talent attraction (C005/24-ED CV1). Funded by the
European Union NextGenerationEU funds, through PRTR.
REFERENCES
[1] U. D. of Transportation National Highway Traffic Safety Ad-
ministration, “Traffic safety facts: Critical reasons for crashes
investigated in the national motor vehicle crash causation survey,”
Feb. 2015. [Online]. Available: https://crashstats.nhtsa.dot.gov/Api/
Public/ViewPublication/812115
2https://ai4ccam-participate.hpai.cloud/
3https://www.red.es/es
[2] World Health Organization, Global status report on road safety 2018 .
Gen`eve, Switzerland: World Health Organization, Jan. 2019.
[3] T. J. Crayton and B. M. Meier, “Autonomous vehicles: Developing
a public health research agenda to frame the future of transportation
policy,” Journal of Transport & Health , vol. 6, pp. 245–252, 2017.
[4] B. van Arem, C. J. G. van Driel, and R. Visser, “The impact of
cooperative adaptive cruise control on traffic-flow characteristics,”
IEEE Transactions on Intelligent Transportation Systems, vol. 7, no. 4,
pp. 429–436, 2006.
[5] G. Meyer and S. Beiker, Eds., Road Vehicle Automation, 2014th ed.,
ser. Lecture Notes in Mobility. Cham, Switzerland: Springer Inter-
national Publishing, June 2014.
[6] P. Foot, “The problem of abortion and the doctrine of double effect,”
Oxford, vol. 5, pp. 5–15, 1967.
[7] J. J. Thomson, “Killing, letting die, and the trolley problem,” The
Monist, vol. 59, no. 2, pp. 204–217, 1976.
[8] E. Awad, S. Dsouza, R. Kim, J. Schulz, J. Henrich, A. Shariff, J.-F.
Bonnefon, and I. Rahwan, “The moral machine experiment,” Nature,
vol. 563, no. 7729, pp. 59–64, Nov. 2018.
[9] J. D. Freitas, S. E. Anthony, A. Censi, and G. A. Alvarez, “Doubting
driverless dilemmas,” Perspectives on Psychological Science , vol. 15,
no. 5, pp. 1284–1288, 2020, pMID: 32735472. [Online]. Available:
https://doi.org/10.1177/1745691620922201
[10] European Parliament and Council of the European Union. Regulation
(EU) 2016/679 of the European Parliament and of the Council.
[Online]. Available: https://data.europa.eu/eli/reg/2016/679/oj
[11] C. Bloom, J. Tan, J. Ramjohn, and L. Bauer, “Self-driving cars
and data collection: Privacy perceptions of networked autonomous
vehicles,” in Symposium On Usable Privacy and Security , 2017.
[Online]. Available: https://api.semanticscholar.org/CorpusID:446594
[12] E. D. P. Supervisor, TechDispatch – Connected cars. Issue
3, 2019 . Publications Office of the European Union, 2019.
[Online]. Available: https://www.edps.europa.eu/data-protection/
our-work/publications/techdispatch/techdispatch-3-connected-cars en
[13] M. Hataba, A. Sherif, M. Mahmoud, M. Abdallah, and W. Alasmary,
“Security and privacy issues in autonomous vehicles: A layer-based
survey,” IEEE Open Journal of the Communications Society , vol. 3,
pp. 811–829, 2022.
[14] G. Mordue, A. Yeung, and F. Wu, “The looming challenges of
regulating high level autonomous vehicles,” Transportation Research
Part A: Policy and Practice , vol. 132, pp. 174–187, 2020.
[Online]. Available: https://www.sciencedirect.com/science/article/pii/
S096585641930480X
[15] J. Himmelreich, “Never mind the trolley: The ethics of autonomous
vehicles in mundane situations,” Ethical Theory and Moral
Practice, vol. 21, pp. 669 – 684, 2018. [Online]. Available:
https://api.semanticscholar.org/CorpusID:150184601
[16] V . Behzadan, J. Minton, and A. Munir, “Trolleymod v1.0: An
open-source simulation and data-collection platform for ethical
decision making in autonomous vehicles,” 2018. [Online]. Available:
https://arxiv.org/abs/1811.05594
[17] S. M. Serrano, D. F. Llorca, I. G. Daza, and M. ´Angel Sotelo,
“Insertion of real agents behaviors in carla autonomous driving
simulator,” 2022. [Online]. Available: https://arxiv.org/abs/2206.00337
[18] V . Grimm, S. F. Railsback, C. E. Vincenot, U. Berger, C. Gallagher,
D. L. DeAngelis, B. Edmonds, J. Ge, J. Giske, J. Groeneveld,
A. S. Johnston, A. Milles, J. Nabe-Nielsen, J. G. Polhill,
V . Radchuk, M.-S. Rohw ¨ader, R. A. Stillman, J. C. Thiele, and
D. Ayll ´on, “The odd protocol for describing agent-based and
other simulation models: A second update to improve clarity,
replication, and structural realism,” Journal of Artificial Societies and
Social Simulation , vol. 23, no. 2, p. 7, 2020. [Online]. Available:
http://jasss.soc.surrey.ac.uk/23/2/7.html
[19] I. Krontiris, K. Grammenou, K. Terzidou, M. Zacharopoulou,
M. Tsikintikou, F. Baladima, C. Sakellari, and K. Kaouras,
“Autonomous vehicles: Data protection and ethical considerations,”
in Proceedings of the 4th ACM Computer Science in Cars
Symposium, ser. CSCS ’20. New York, NY , USA: Association for
Computing Machinery, 2020. [Online]. Available: https://doi.org/10.
1145/3385958.3430481
[20] M. K. Andreia Martinho, Nils Herber and C. Chorus, “Ethical
issues in focus by the autonomous vehicles industry,” Transport
Reviews, vol. 41, no. 5, pp. 556–577, 2021. [Online]. Available:
https://doi.org/10.1080/01441647.2020.1862355
2496
Authorized licensed use limited to: Universitat de Barcelona. Downloaded on May 05,2026 at 07:59:11 UTC from IEEE Xplore.  Restrictions apply. 
```
