---
title: "Geo-Tracked Rights Explainers: Combatting Misinfodemics and Advancing Open Rights"
author:
  - Patrick Keyzer
source: https://ceur-ws.org/Vol-3531/SPaper_13.pdf
venue: AIGEL 2022
type: Proceedings Article
created: 2025-02-17
tags:
  - themes/bias
  - tech/Ai
  - themes/ethics
pdfORepub: "[[Geo-Tracked Rights Explainers - Combatting Misinfodemics and Open Rights.pdf]]"
modified: 2026-09-08
---

# Notes

## Full text (extracted from `2PDF/Geo-Tracked Rights Explainers - Combatting Misinfodemics and Open Rights.pdf`)

*Extracted:* 2026-09-17

```text
Geo-Tracked Rights Explainers: Combatting
Misinfodemics and Advancing “Open Rights”
Patrick Keyzer1
1Australian Catholic University, 115 Victoria Parade, Fitzroy, Melbourne, 3065, Australia
Abstract
This paper has three objectives: First, to describe circumstances where legal misinformation can have
potentially deadly consequences. Second, to propose a remedy, an app that would use geographical
positioning technology to pinpoint the location of a person in real time, and then provide them with
answers to fundamental questions relating to constitutional law and human rights that might protect
them from harm. Finally, this paper will explain how this device could go a very considerable way to
improving access to justice by opening rights. Constitutional and human rights are meaningless if you
have no knowledge of them and no tools to access them. An app that provides geo-tracked explanations
of rights could be a highly beneficial educational tool, improving the quality of civic engagement, and
advancing the objective of open rights.
Keywords
Misinformation, “misinfodemic”, GIS, constitutional law, human rights, civic engagement, open rights.
1.
At some point during the incredible time warp that was the COVID-19 pandemic that everyone
who is reading this thankfully survived, I was amused to read an article in The Guardian entitled
“Protestors claim to ‘seize’ Edinburgh Castle citing Magna Carta”. It told the story of a group of
about twenty Scottish demonstrators who were fed up with pandemic restrictions and decided
to enter the grounds of the Castle without paying for a ticket. In a video posted to Facebook Live
(where else?) which no doubt later served as useful evidence for law enforcement authorities,
one demonstrator indicated that the purpose of taking the Castle was to “restore the rule of
law”. Another said the action was intended to draw attention to the treason and tyranny of the
government. The demonstrators also said the protest was supported by the Magna Carta. The
author of the article wryly noted that Magna Carta was signed by King John in 1215 and has
never applied in Scotland because it predates the Act of Union.
The right to peaceful protest is sacrosanct [1], and a gathering of protesters can be amusing.
Some of the funniest memes come from protester placards. But a mass demonstration during
a pandemic is not a good idea. Reading the article got me thinking about the lawlessness of
some Australians during the COVID-19 pandemic, the risk of further spread of COVID-19 and
Proceedings of Artificial Intelligence Governance Ethics and Law (AIGEL), Reviewed, Selected Papers. November 02 -
December 19, 2022, Barcelona, Spain
Envelope-Open patrick.keyzer@acu.edu.au (P. Keyzer)
Orcid 0000-0003-0807-8366 (P. Keyzer)
© 2022 Copyright for this paper by its authors. Use permitted under Creative Commons License Attribution 4.0 International (CC BY 4.0).
CEUR
Workshop
Proceedings
http://ceur-ws.org
ISSN 1613-0073
CEUR Workshop Proceedings (CEUR-WS.org)
161


Patrick Keyzer CEUR Workshop Proceedings 161–170
extension of the harsh lockdown measures we experienced, and the misinformation that drove
on the self-styled “freedom fighters”.
Notwithstanding the valiant efforts of public health experts during the pandemic, including,
remarkably, resisting death threats on themselves and their families [2], [3], misinformation (or
“fake news”; [4]) about COVID-19, particularly across social media, was rampant [5]. The twice-
impeached and disgraced former President Donald Trump was, unsurprisingly, the principal
culprit in the mis-“infodemic” [6] that drove people away from wearing masks [7] and towards
quackery like hydroxychloroquine [8] and even injecting bleach (see, for example, the analysis
of Chejfec-Ciociano, [9] considering how Mexicans responded to this misinformation).
Steffens, Dunn, Wiley and Leask [10] explored how Australian organisations promoting
vaccination face significant challenges combatting misinformation and anti-science sentiment
on social media. They have had to develop sophisticated strategies to respond to ignorance.
Their strategies included “communicating with openness in an evidence-informed way; creating
safe spaces to encourage audience dialogue” and “countering misinformation with care”.
I think I might be too impatient to greet some varieties of ignorance with care. It seems
remarkablethatthereevenisananti-sciencemovement. However,itisnowverywellunderstood
that social media is rife with anti-science misinformation, and during the pandemic, we lived
through what can be called a misinfodemic. The danger posed by social media is not merely the
ignorance of people challenged by the Dunning Kruger Effect (“in which poor performers in
many social and intellectual domains seem largely unaware of just how deficient their expertise
is”; [11]), but the subversive technologies that have been utilised by horrible people to spread
misinformation.
Software allows criminal propagandists to generate automated content and share it via coun-
terfeitaccounts(“bots”)toamplifymisinformation[12], [13]). Someplatforms, suchasTelegram,
provide encryption capability that makes it impossible to divine the source of the misinfor-
mation [14]. In their significant study, Bradshaw and Howard [15] note that computational
propaganda has extended beyond social media automation via bots to encompass paid online
commentary teams trafficking misinformation, and even the use of paid advertisements and
search engine optimization to cause what I call misinfodemics. These methods have resisted
attempts by social media platforms to engage in detection and intervention [16].
An increasing number of scholars are studying this phenomenon, alerting us to the dangers
of dissemination of misinformation via these means and how this can undermine scientific
communication [17]. Although Australian scholars have been aware of the risks and done
important work to combat misinformation [18], the anti-lockdown movement and demonstra-
tions in Australia (particularly in Melbourne) that were fuelled by the misinformation were
much more than a public nuisance caused by a few dim protesters attempting a takeover of
Edinburgh Castle – they were dangerous COVID-19 super-spreader events [19]. The Victorian
Health Minister said that these “potential superspreader events make us very concerned, not
just for the ill-advised protesters, but think about Victoria Police members who’ve had to put
themselves in harm’s way to protect the rest of us” (quoted in the Sydney Morning Herald, 24
September 2021). (To like effect, Lange and Monscheuer [20] analysed bus traffic from anti
COVID-19 restriction demonstrations in Germany and found significant increases in the spread
of that disease after demonstrations in that country).
Worse still, the rhizomic effect of anti-vax misinformation (a brilliant concept, the notion
162

Patrick Keyzer CEUR Workshop Proceedings 161–170
that misinformation spreads like mushrooms, which I draw from Christopher Goff’s excellent
PhD thesis, “The Historical Trajectory of Terrorism and Legal Challenges in the Post-Modern
Era”, awarded in 2022, [21]) was further spread by extremist groups with putatively libertarian
but often dangerous objectives, such as Freie Bürger Kassel [22] – their various Facebook and
Telegram pages are “awash with anti-vaccine and Covid-19 conspiracy theories, as well as
other conspiratorial content such as QAnon and Islamophobia”), Australians vs The Agenda
(“Our mission is to create a mass-scale awakening of Australian citizens — a fully empowered,
conscious and cooperative collective of individuals. We want to help you free your mind from
what the Government and the media is trying to make you do” - an anti-vax protest movement
with an active website, YouTube channel, and TikTok presence that peddles misinformation and
sells t-shirts), Reignite (Democracy Australia) (over 70,000 followers on Instagram, indicating
that it is an “advocacy group aimed at maintaining individual and collective liberty” that has
sought to distance itself from right-wing anti-Semitic groups but has a website and social
media presence peddling anti-vax misinformation), Australian Vaccination-risks Network (the
“AVN” “was started in 1994 by a group of parents and health professionals who were concerned
about the lack of scientifically-based information on the ‘other side’ of the vaccination issue”;
their website contains a significant amount of anti-vax misinformation) and Informed Medical
Opinions (they now seem to have learned that they don’t have legislated human rights, but
now advocate “a Bill of Rights or Federal Human Rights Act which recognises the rights of
all people to work, open their business, go to school/childcare, enter a venue, visit family and
travel without interference from bureaucrats”, i.e., when people are unvaccinated).
Misinfodemics are not restricted to vaccine information [23] as anyone following the rise
(and, at the time of writing [hopefully] the imminent demise) of Donald Trump would well
understand. Even the public information made available by these groups – to say nothing of
the information available on encrypted services – is rife with legal misinformation. Examples
include:
1. Assertions that parents have a right not to vaccinate their children.
2. Assertions that independent schools should not be regulated.
3. Rejection of the rules and mandates developed by the:
a) Goods Administration (TGA),
b) the Gene Technology Regulator,
c) the Australian Health Practitioners Regulation Authority (AHPRA), the Health Care
Complaints Commission (HCCC) and
d) “any other organisation whose decisions impacted the health and freedoms of our
citizens”.
4. Assertions that human rights can be invoked as a barrier to police enforcement activities
(more on this later).
2.
Nathan Buckley, a lawyer then practising in NSW (and later suspended and offering himself as a
candidate for right-wing political party “One Nation”), encouraged Victorian residents who had
163

Patrick Keyzer CEUR Workshop Proceedings 161–170
been ticketed for failing to comply with mask mandates to elect to contest their tickets in court,
arguing they would thereby overwhelm the system. Making a name for himself as a virulent
anti-vax campaigner, Buckley then secured crowdfunding for a series of cases challenging anti-
vaccine mandates. One such case was Kassam v Hazzard; Henry v Hazzard [2021] NSWSC 1320
(15 October 2021) [24]. In that case, a number of people who declined to be vaccinated against
COVID-19 challenged the legality of New South Wales public health orders that designated
certain areas (aged care facilities and childcare facilities, amongst others) and required workers
in those places to be vaccinated against COVID-19. Challenges were made on the basis that
thesevitiatedtherightsofthesepeopletodeclinetobevaccinated. TheSupremeCourtheldthat
the public health orders that might affect freedom of movement and capacity to work did not
violate the right to bodily integrity and did not vitiate consent to vaccination. Arguments were
also made that the public health orders violated the Commonwealth Constitution’s prohibition
against legislation that included any “civil conscription” in the provision of medical services.
These arguments were doomed to fail as the civil conscription prohibition only applies to
Commonwealthlegislation, whichispatentlyobviouswhentheconstitutionalprovision(section
51(xxiiiA) of the Constitution) is read. As the Supreme Court observed, “the preclusion on
authorising civil conscription only qualifies a (Commonwealth) law for the “provision” of
“medical or dental services” (British Medical Authority v The Commonwealth (1949) 79 CLR
201; [1949] HCA 44 at 254 per Rich J, at 261 per Dixon J, at 282 per McTiernan J, at 286 per
Williams J, contra per Latham CJ at 253 and Webb J not deciding at 292 [25]; Alexandra Private
Geriatric Hospital Pty Ltd v Commonwealth [1987] HCA 6; (1987) 162 CLR 271 at 279) [26].
Australian Vaccination-Risks Network Incorporated took their cause several steps further
than merely promoting misinformation, gathering funds from donors to progress a test case
against the Secretary of the Department of Health, aimed at challenging the registration of the
COVID-19 vaccine and particularly aimed at preventing its use on children. The Federal Court
held they had no standing as they failed to identify an interest greater than that of an ordinary
member of the public to argue that the decisions to allow vaccines were improperly made
(Australian Vaccination-Risks Network v Secretary, Department of Health [2022] FCA 320 [27],
applying the High Court authority, Australian Conservation Foundation v The Commonwealth
(1980) 146 CLR 493, [28]). Their appeal was unanimously rejected (Australian Vaccination-Risks
NetworkIncorporatedvSecretary, DepartmentofHealth[2022]FCAFC135(8August2022)[29].
Costs were awarded against the Australian Vaccination-Risks Network Incorporated. These
would likely be very significant and could easily be more than$1𝑀 [30].
It is a terrible thing even for misguided people to have to spend so much energy and time
and money to find out they are wrong in this way. Litigation in countries where “costs follow
the event” can be high stakes. Would it be possible to develop an easy way for people to
find out whether the Magna Carta or international human rights principles actually apply,
before they engage in potentially dangerous activity? This lawyer, safely ensconced in his
home, attended on by masked and gloved delivery drivers providing my daily needs at some
risk to themselves, started to wonder why so many people in Australia seem to have such a
fundamental misunderstanding of Australian law, and a lack of knowledge that put them and
others in harm’s way.
Other than briskly gliding past debates on social media I got a sense of the strength of the
anti-vaccine lobby in Australia when I participated in a webinar in 2021 for New Chambers, a
164

Patrick Keyzer CEUR Workshop Proceedings 161–170
barrister’s chambers in Sydney, New South Wales (NSW). Together with eminent epidemiologist
Professor Mary-Louise McClaws, and barristers Arthur Moses SC and Henry Cooper, I fielded
questions from over 500 people, mainly on the principles of constitutional law that supported
the COVID regulations. Prominent amongst the scores of questions asked were questions from
quite a number of people (most marking themselves as “Anonymous” in the Zoom chat) who
wanted to know how or whether the Government could assert any legal power to vaccinate
them. After all, they reasoned, it’s my body, so how can anyone force me to do something like
this?
Well, I said, you are not being forced to be vaccinated, but your freedom of movement and
opportunities to enter workplaces where vaccinated people are working might be restricted
until the pandemic is past. But isn’t that effectively the same thing as being forced? Well, no,
because rights within society need to be balanced. Your right to freedom of speech doesn’t give
you the right to defame or bully others. Rights can and do compete, and it is the job of our
parliaments, through laws, to regulate competing rights. On this occasion, a State Parliament
has decided to make orders under public health legislation to restrict the access of unvaccinated
people to vaccinated workplaces. This is reasonable, and constitutionally valid.
Hold on, isn’t the State Parliament subject to international human rights law or the Com-
monwealth Constitution. Yes, but not in the way that you might want.
First, subject to the Commonwealth Constitution and valid Federal laws, State Parliaments
can enact legislation on any topic whatsoever (Union Steamship Co Ltd v King (1988) 166 CLR
1). Unsurprisingly, this pronouncement was met with astonishment and disbelief. I doubled
down by telling participants that a State Parliament could pass a valid law stating that “all
blue-eyed babies shall be murdered” (this was the famous example of a brutal law designed to
test the theory of parliamentary sovereignty). (More astonishment). Now this would be a brutal
law, but a valid law. Is a law requiring people to be vaccinated before entering the workplace of
people who want to be safe a brutal law?
Some of the people on the Zoom chat then sought to assert their “common law rights”, and
sometimes, as “free people”, faintly or even stoutly echoing the rhetoric of the sovereign citizen
movements that are active online and in social media [31]. I then explained (the elementary
principle) that while there is a common law right not to accept a medical procedure (including
a vaccine), and the Commonwealth could not enact a valid law that forced any person to take a
vaccine (section 51(xxiiiA) of the Constitution gives the Commonwealth power to pass laws
with respect to “medical … services, but not so as to authorize any form of civil conscription”) no
such restriction applied to the States. So, a State parliament can enact valid legislation requiring
you to have a vaccine. Commonwealth law trumps State law trumps the common law … but
in the absence of a Commonwealth law, the State law operated. In addition, a State law can
operate in any field left vacant by the Commonwealth.
Three decades of providing pro bono legal advice for interesting people prepared me well for
what often happens next. Querulous people tend not to want to hear the advice you are giving
them if it is inconsistent with their beliefs. You don’t have to look very far to see examples of
this phenomenon, and writ large. A lot of people in the United States think that Donald Trump
is still the President. Once you give querulous people the sort of explanation I gave above, they
assume the law is like an elaborate game of euchre, and they want to pull out a bower to trump
you (and preferably the right one). They will then reach for the most important sounding law
165

Patrick Keyzer CEUR Workshop Proceedings 161–170
they can find, to topple your explanation that they do not care to hear. Magna Carta sounds
pretty weighty, and it is very old, so it must prevail! Or maybe it could be the International
Covenant on Civil and Political Rights. Surely, the Covenant protects against the gross violation
of human rights that being required to take a vaccine represents. Article 7 reads:
No one shall be subjected to torture or to cruel, inhuman or degrading treatment or punish-
ment. In particular, no one shall be subjected without his free consent to medical or scientific
experimentation.
What’s more, Australia is a signatory! Surely the ICCPR prevails!
Alas, no. Learning that the Commonwealth Constitution doesn’t automatically trump any
State law is tough medicine but finding out that the International Covenanton Civil and Political
Rights does not apply in Australia because it has not been implemented into domestic law is
usually enough to provoke a reaction. Surely Australia has to implement a treaty it signs?
No. Surely the U.N. compels countries to implement treaties they’ve signed? No. So there’s
nothing I can do? You could make a complaint to the United Nations, but the Australia doesn’t
implement the decisions of the UN Human Rights Committee (that’s right, even though they
signed the First Optional Protocol to the International Covenant on Civil and Political Rights)
[32].
3.
All of the legal questions raised by the anti-vax crowd could be easily answered. They weren’t
the answers that they wanted to hear, but they could have saved themselves an enormous
amount of time, money and wasted effort. Putting the litigation to one side, there would have
been hundreds or even many thousands of people who declined to be vaccinated (due to medical
misinformation) and then took on their employers or governments (due to legal misinformation)
and wrecked their own lives in the process. Then there are all of the knock-on effects as these
legally misinformed people bullied service workers in shops, on public transport and the like,
making their lives miserable, again, based on their misinformed opinions.
Wouldn’t it have been splendid if all these querulous people could have opened their smart-
phone, opened an app that geo-tracked their location, and allowed them to find out whether
Magna Carta applied before they conducted their demonstration? Wouldn’t it be great if the
information in that app was sufficiently detailed to give people some basic, uncontroversial
information about their rights, or in Australia, their lack of them? You could assist with compli-
ance, shrink reliance on law enforcement and educate the citizenry at the same time. There is
great potential for better understanding of the legal system, better quality civic engagement,
and, of increasing importance, the debunking of misinformation.
Recently the “New Tactics Conversation” for the Center for Victims of Torture explored the
concept of geo-mapping for human rights. Their conversation focused on “the role of spatial
mapping tools in working to further human rights goals”:
With the rise of technology, mapping tools become not only more available to practitioners
thatmaypreviouslyhaveshiedawayfromusingtechnology,butmapsalsooffernewpossibilities
for advocacy, promoting transparency around human rights issues, tracking impact of human
rights efforts, and engaging the community in local issues. Geo-mapping is a rapidly developing
166

Patrick Keyzer CEUR Workshop Proceedings 161–170
tool in the human rights community, and this dialogue acted as a platform for practitioners to
share ideas, advice, and resources regarding its use.
Geographers have drawn attention to the potential of GIS to create a critical cartography of
human rights. In a study of mass atrocity in northern Uganda, Madden and Ross complemented
use of geographic information systems with quantified data that complemented testimonials
and other qualitative data from the field. Cartographic functions, geo-visualization, and spatial
analyses available in GIS were used to extract information from high-resolution remote sensing
images documenting internally displaced persons (IDP) camps and quantifying evidence of
crimes against humanity [33].
Ithasinfactlongbeenrecognisedthatgeographicinformationsystemsareasocialtechnology.
As such, can and should be deployed to enable better understanding of social conditions [34].
It is a short step to take to combine geographic positioning systems with legal information
to improve understanding of the applicability of legal human rights norms everywhere in the
world (just as David Harvey mapped capitalism [35]). Combining GPS and legal information –
so long as equal access is provided – would also be a highly useful tool to pinpoint places where
reform and improvement is needed [36].
4.
In 1978, Mauro Cappeletti and Bryant Garth observed [37]:
The words “access to justice” are admittedly not easily defined, but they do serve to focus on
two basic purposes of the legal system – the system by which people may vindicate their rights
and/or resolve their disputes under the general auspices of the state. First, the system must be
accessible to all; second, it must lead to results that are individually and socially just. … a basic
premise of social justice, as sought by our modern societies, presupposes access.
Focusing on the first aspect of this definition of access to justice – accessibility – knowing
what the law is is plainly a vital first step in seeking its application, its reform, or even its
rejection. Everyone is entitled to know the law and a device such as the one proposed here
would have an enormous equalising effect, giving everyone access to the knowledge that is
brokered through often expensive and impenetrable legal and justice systems. In Australia,
legal information is made available freely by the Australasian Legal Information Institute, so
much of the hard work has already been done.
The underlying premise of human dignity is that we all share in it [38]. Even people who
are afflicted by the Dunning-Kruger Effect. I feel sorry for the people who, acting upon
misinformation, challenged vaccine rules and public health orders, failing to appreciate basic
principles of constitutional law and human rights in the process. We can hardly blame people
for acting upon misinformation when we have not used every technological tool at our disposal
to improve their understanding of the law. It’s time for an app! We need an app for that!
Quite apart from anything else, giving people access to a geographically positioned system
of constitutional and human rights information would be enormously beneficial to the teaching
of civics (in Australia). The futile forays into the justice system outlined above could be
averted, people might be less likely to put themselves into legal (or health) jeopardy, and they
might focus their energy on entering politics or engaging in peaceful and less hazardous or
167

Patrick Keyzer CEUR Workshop Proceedings 161–170
harmful activity to advance their objectives. A better-informed populace that understands how
significant democracy is in driving the development of constitutional and human rights norms
might propel the development of even more perfect unions, even more legitimate systems, and
wider, safer spaces for the powerless to contend with the powerful [39]. We could develop
more inclusive conversations, building a larger sense of what Kim Scheppele has called “the
constitutive we” which can sometimes exclude the “they”. We could all learn from this work
[40].
Finally,anapplikethiscouldopen(verb)rights(noun)andachieveopenrights(nounqualified
by an adjective). This should be an objective with all human rights.
Acknowledgments
I acknowledge that this paper was written on Wurundjeri Land of the Kulin Nation in Naarm
(Melbourne)andIacknowledgethatthelandofthetraditionalownerswasnevercededandIpay
tribute to elders past, present and emerging. Thanks to Assumpció Malgosa, Pompeu Casanovas,
Carles Sierra, Esther Zapater, and Susana Navas for their respective roles in convening the
AIGEL Scientific Workshop together with the Institute of Law and Technology (IDT-UAB) and
IIIA-CSIC.
References
[1] International Covenant on Civil and Political Rights, Article 21; see also Office of the High
Commissioner of Human Rights, General Comment No 37 on Article 21).
[2] Michelle M. Mello, Jeremy A. Greene and Joshua M. Sharfstein, 2020. “Attacks on Public
Health Officials During COVID-19”, JAMA, 324(8), 741-2.
[3] Bianca Nogrady, 13 August 2021. “’I hope you die’: how the COVID pandemic unleashed
attacks on scientists”, Nature.
[4] David M.J. Lazer, Matthew A. Baum, Yochai Benkler, Adam J.Berinsky, Kelly M.Greenhill,
FilippoMenczer, MiriamJ.Metzger, BrendanNyhan, GordonPennycokk, DavidRothschild,
Michael Schudson, Steven A. Sloman, Cass R. Sunstein, Emily A. Thorson, Duncan J. Watts
and Jonathan L. Zittrain, 2018. “The science of fake news: Addressing fake news requires
a multidisciplinary effort”, Science, 359: 6380, 1094-7.
[5] Samia Tasnim, Md Mahbub Hossain and Hoimonty Mazumder, 2020. “Impact of Rumors
and Misinformation on COVID-19 in Social Media”, Journal of Preventive Medicine and
Public Health, 53:3, 171-4.
[6] Sarah Evanega, Mark Lynas, Jordan Adams and Karinne Smolenyak, 2020. “Coronavirus
misinformation: quantifying sources and themes in the COVID-19 ‘infodemic’”, The
Cornell Alliance for Science.
[7] John W. Ayers, Brian Chu, Zechariah Zhu, Eric C. Leas, Davey M. Smith, Mark Dredze and
David A. Broniatowski, 2021. JAMA Internal Medicine, 181(9): 1251-1253.
168

Patrick Keyzer CEUR Workshop Proceedings 161–170
[8] Tim K Mackey, Vidya Purushothaman, Michael Haupt, Matthew C Nali and Jiawei Li,
2021. “Application of unsupervised machine learning to identify and characterize hydroxy-
chloroquine misinformation on Twitter”, 3:2, E72-E75. DOI: https://doi.org/10.1016/S2589-
7500(20)30318-6.
[9] Jonathan Matias Chejfec-Ciociano, Juan Pablo Martinez-Herrera, Alexa Darianna Parra-
Guerra, Ricardo Chejfec, Francisco José Barbosa-Camacho, Juan Carlos Ibarrola-Peña,
GabinoCervantes-Guevara, GuillermoAlonsoCervantes-Cardona, CltildeFuentes-Orozco,
Enrique Cervantes-Pérez, Benjamin Garcia-Reyna and Alejandro González-Ojeda, 2022.
“MisinformationAboutandInterestinChlorineDioxideDuringtheCOVID-19Pandemicin
Mexico Identified Using Google Trends Data: Infodemiology Study”, JMIR Infodemiology,
2(1): e29894. DOI: 10.2196/29894.
[10] Maryke S. Steffens, Adam G. Dunn, Kerrie E. Wiley and Julie Leask, 2019. “How organi-
sations promoting vaccination respond to misinformation on social media: a qualitative
investigation”, BMC Public Health 19, Article number 1348.
[11] David Dunning, 2011. “Chapter five – The Dunning-Kruger Effect: On Being Ignorant of
One’s Own Ignorance”, Advances in Experimental Social Psychology, 44, 247-296.
[12] Broniatowski DA, Jamison AM, Qi S, et al.. 2018. “Weaponized health communica-
tion: Twitter bots and Russian trolls amplify the vaccine debate”. Am J Public Health,
108(10):1378-1384. doi: 10.2105/AJPH.2018.304567.
[13] Allem JP and Ferrara E., 2018. “Could social bots pose a threat to public health?” Am J
Public Health. 108(8):1005-1006. doi: 10.2105/AJPH.2018.304512.
[14] SamanthaBradshawandPhilipN.Howard, 2019#. ChallengingTruthandTrust: AGlobal
Inventory of Organized Social Media Manipulation, Computational Propaganda Research
Project, Oxford Internet Institute.
[15] SamanthaBradshawandPhilipN.Howard, 2019#. ChallengingTruthandTrust: AGlobal
Inventory of Organized Social Media Manipulation, Computational Propaganda Research
Project, Oxford Internet Institute.
[16] David M.J. Lazer, Matthew A. Baum, Yochai Benkler, Adam J.Berinsky, Kelly M.Greenhill,
FilippoMenczer, MiriamJ.Metzger, BrendanNyhan, GordonPennycokk, DavidRothschild,
Michael Schudson, Steven A. Sloman, Cass R. Sunstein, Emily A. Thorson, Duncan J. Watts
and Jonathan L. Zittrain, 2018. “The science of fake news: Addressing fake news requires
a multidisciplinary effort”, Science, 359: 6380, 1094-7.
[17] Saitz R, Schwitzer G. 2020. “Communicating science in the time of a pandemic”. JAMA.
324(5):443-444. doi: 10.1001/jama.2020.12535.
[18] Lisa Parker, Jennifer A. Byrne, Micah Goldwater and Nick Enfield, 2021. “Misinformation:
an empirical study with scientists and communicators during the COVID-19 pandemic”,
BMJ Open Science, 5(1): e100188. DOI: 10.1136/bmjos-2021-100188
[19] Emily Cosenza and Cortney Gould, 4 December 2021. “Three in hospital, 39 with Covid
after contracting the virus at anti-vax rallies in Melbourne”, News.com.au.
[20] Martin Lange and Ole Monscheuer, 2022. Spreading the disease: Protects in times of
pandemics. Health Economics 31:12, 2664-2679.
[21] Christopher Goff, 2022. “The Historical Trajectory of Terrorism and Legal Challenges in
the Post-Modern Era”. PhD Thesis, Bond University.
169

Patrick Keyzer CEUR Workshop Proceedings 161–170
[22] Christopher Knaus and Michael McGowan, 27 July 2021, “Who’s behind Australia’s
anti-lockdown protests? The German conspiracy group driving marches”, The Guardian.
[23] Victor Suarez-Lledo and Javier Alvarez-Galvez, 2021. “Prevalence of Health Misinfor-
mation on Social Media: A Systematic Review”, Journal of Medical Internet Research,
23:1.
[24] Kassam v Hazzard; Henry v Hazzard [2021] NSWSC 1320
[25] British Medical Authority v The Commonwealth (1949) 79 CLR 201; [1949] HCA 44.
[26] Alexandra Private Geriatric Hospital Pty Ltd v Commonwealth [1987] HCA 6; (1987) 162
CLR 271
[27] Australian Vaccination-Risks Network v Secretary, Department of Health [2022] FCA 320
[28] Australian Conservation Foundation v The Commonwealth (1980) 146 CLR 493
[29] Australian Vaccination-Risks Network Incorporated v Secretary, Department of Health
[2022] FCAFC 135
[30] Patrick Keyzer, 2010. “A Battle and a Gamble: The Spectre of an Adverse Costs Order in
Constitutional Litigation”, Bond Law Review, 22(3), 82
[31] Christine M. Sarteschi, 2020. Sovereign Citizens: A Psychological and Criminological
Analysis, Springer
[32] Darren O’Donovan and Patrick Keyzer, 2015. “Visions of a Distant Millennium? The ef-
fectiveness of the UN Human Rights Petition System”, in Patrick Keyzer, Vesselin Popovski
and Charles Sampford, eds., Access to International Justice, Routledge, 2015
[33] Marguerite Madden and Amy Ross, 2009. Genocide and GIScience: Integrating Personal
Narratives and Geographic Information Science to Study Human Rights. The Professional
Geographer 508-526.
[34] Eric Sheppard, “GIS and Society: Towards a Research Agenda”, Cartography and Geo-
graphic Information Systems, 22:1, 5-16.
[35] David Harvey, 1990. “Between space and time: Reflections on the geographical imagina-
tion”. Association of American Geographers, Annals 80: 418-35.
[36] Harlan J. Onsrud and Robert I. Reis, 1995. Law and Information Policy for Spatial
Databases: A Research Agenda, Jurimetrics, 35:4, 377-393.
[37] Mauro Cappelletti and Bryant Garth, 1978. “Access to Justice: The Newest Wave in the
Worldwide Movement to Make Rights Effective”, Buffalo Law Review, 27(2) 181-192.
[38] Charles Taylor, 1994. “The Politics of Recognition”, in Amy Gutmann, ed., Multicultural-
ism, Princeton: Princeton University Press, 25-73, 38
[39] Patrick Keyzer, 2010. Open Constitutional Courts, Federation Press.
[40] Kim Scheppele, 1989. “Telling Stories”, Michigan Law Review, 87: 2073-2098, 2078
170
```
