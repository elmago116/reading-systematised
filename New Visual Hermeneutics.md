---
title: 02 KathSchaalDumm 27..51
author: ""
year: "2015"
Type: Book
DOI: ""
source: ""
created: 2026-04-24
description: ""
tags:
  - op/acc/pending-review
  - Humanities/hermeneutics
  - design/visualization
pdfORepub: "[[New Visual Hermeneutics.pdf]]"
---
[[New Visual Hermeneutics.pdf]]
## Full text (extracted from `New Visual Hermeneutics.pdf`)

*Source:* `2PDF/New Visual Hermeneutics.pdf`  
*Extracted:* 2026-04-24

```text
Roxana Kath, Gary S. Schaal, Sebastian Dumm
New Visual Hermeneutics
Abstract: In digital humanities, research insights are often achieved by the
interpretation of visualizations of data, but the interpretation of visualization is
not self-evident.
In this paper we present a new methodology to attain interpretations of
visualizations which may be accepted intersubjectively. New Visual Hermeneu-
tics is an integrated research framework with special attention to the episte-
mology of visualizations. Adapting Don Ihde’s experimental phenomenology it
addresses the research process as a whole, focusing on the impact of all research
decisions which result in the final visualization(s) in four distinct steps: 1. data
sampling, 2. algorithmic analysis of the sampled data, 3. choosing visualization
of the algorithmic analysis, 4. hermeneutic interpretation of the chosen visuali-
zation.
DOI 10.1515/zgl-2015-0002
1 Forschungskontext und Erkenntnisinteresse
2 Der Stand der Forschung: Theorizing oder Doing?
3 New Visual Hermeneutics
3.1 Analyseschritt 1: Acquisition/Repository/Semantic Enrichment
3.2 Analyseschritt 2: Text ‐Mining & Information Retrieval
3.3 Analyseschritt 3: Visualisierung der Daten
3.4 Analyseschritt 4: die hermeneutische Analyse einer Visualisierung im Kontext einer
empirischen Phänomenologie
4 Schluss
Literatur
Dr. Roxana Kath: Universität Leipzig, Historisches Seminar, Beethovenstr. 15, D-04107 Leipzig,
E-Mail: roxana.kath@me.com
Prof. Dr. Gary S. Schaal: Helmut-Schmidt-Universität, Institut für Politikwissenschaft, Holsten-
hofweg 85, D-22043 Hamburg, E-Mail: gschaal@hsu-hh.de
Sebastian Dumm: Helmut-Schmidt-Universität, Institut für Politikwissenschaft, Holstenhofweg 85,
D-22043 Hamburg, E-Mail: sebastian.dumm@hsu-hh.de
ZGL 2015; 43(1): 27–51

1 Forschungskontext und Erkenntnisinteresse1
Visualisierungen sind für die automatisierte Textanalyse, ob in der Linguistik oder
in den Digital Humanities von herausragender Bedeutung,2 denn aufgrund der
Größe der analysierten Korpora (Big Data) sind zumeist nur noch abstrakte visuelle
Repräsentationen (text-)statistischer Analysen möglich, die sich jedoch einer direk-
ten und unmittelbaren visuellen Interpretation entziehen.
3 Eine explorative Ana-
lyse von Visualisierungen wie sie beispielsweise bei der Analyse von Kookurrenz-
mustern (Kollokationsgraphen) oder bei der Analyse von Komposita (Decision
Trees) zum Einsatz kommt wird im Hinblick auf ihren epistemologischen Mehrwert
bislang selten reflektiert. Wir stellen mit diesem Aufsatz den Entwurf einerNew
Visual Hermeneuticsvor, um den Prozess, mit deminsights4 aus großen unstruktu-
rierten Datenkorpora durchexplorative Analysen vonVisualisierungen erzielt wer-
den, methodologisch zu fundieren. Wir argumentieren dabei aus der Perspektive
der Digital Humanities (DH), die sich darin einig sehen, dass die die visuelle
Analyse der Königsweg für die Generierung von„insight[s]“ ist (vgl. Seifert et al.
2014, 190) und fundieren unseren Ansatz epistemisch in der empirischen Phäno-
menologie von Ihde (1998; 2012). Unsere Überlegungen sind aber für alle Bereiche,
in denen große Textkorpora mit maschinellen Methoden untersucht werden, von
Relevanz; er ist auch geeignet, das in der Einleitung von den Herausgebern
skizzierte Desiderat einer Methodik der Visualisierung zu beheben.
Viele KollegInnen innerhalb der amerikanischen Digital Humanities (DH)5
vertreten die Position, dass „the emphasis on creating and the process and
creation itself being the theory seems fitting for the digital humanities“ (Taka-
hashi 2012), während die deutschsprachige DH-Community einer grundlagen-
1 Herzlichen Dank an Alexander Stulpe und Kelly Lancaster für kritische Kommentare zu einer
ersten Version dieses Beitrages.
2 Vgl. für viele Seifert et al. (2014, 190):„Visualization is an effective enabler for exploratory
analysis, making it a powerful tool for gaining insight into unexplored data sets.“
3 „The rationale is that data is too large for purely visual methods, requiring the use of data
processing and mining; yet, the desired tasks are too exploratory for purely analytical methods,
requiring the involvement of human analysts, using visualization as a medium for human
interaction with the data.“ (Endert et al. 2014, 2).
4 Mit ‚insights‘wird relevantes neues Wissen bezeichnet.
5 Wir möchten uns an dieser Stelle nicht an der Debatte über das Für und Wider derDigital
Humanities als eigener Disziplin beteiligen (vgl. hierzu u. a. Rehbein/Schubert 2013; Schubert
2013). Vielmehr verstehen wir die DH als eine epistemische Community, die sich durch die
Anwendung neuer algorithmenbasierter Analysemethoden auszeichnet.
28 Roxana Kath, Gary S. Schaal, Sebastian Dumm

theoretischen Fundierung derDH grosso modo positiver gegenübersteht (vgl. mit
weiteren Nachweisen Rieder/Röhle 2012).6
Die DH greifen gleichermaßen auf Theorien, Methoden und Ansätze der
Natur- und Sozialwissenschaften sowie auf jene der Geisteswissenschaften, im
Bereich der Textanalyse insbesondere auf die Computer- und Korpuslinguistik als
Grundlagenwissenschaften zurück. Hieraus resultiert für dieDH nicht nur die
Notwendigkeit, eine interdisziplinäre Perspektive einzunehmen, sondern auch
eine besondere Sensibilität für Kompatibilitäten und Inkompatibilitäten sowie für
die epistemischen Friktionen zu entwickeln, die daraus entstehen.7 Würden die
DH diese epistemische Sensibilität (weiter) entwickeln, wären sie nicht nur in der
Lage, den vermeintlichen Graben zwischen Natur-, Sozial- und Geisteswissen-
schaften zu überwinden, sondern auch genuin neues Wissen zu generieren.8 Wir
vertreten daher die These, dass dieDH dringend einer eigenen epistemischen
Fundierung und einer eigenen Methodologie bedürfen, da von beidem die weitere
Entwicklung der wissenschaftlichen Akzeptanz und der Auswirkungen derDH
nachhaltig bestimmt werden. Eine Debatte über die epistemischen und metho-
dischen Grundlagen befindet sich jedoch noch in ihren Anfängen. Der vorlie-
gende Aufsatz möchte hierzu einen Beitrag leisten, indem er die Grundzüge einer
New Visual Hermeneuticsskizziert, einer expliziten Methodik für die explorative
6 Die systematischen Gründe für diesen interessanten Unterschied können an dieser Stelle leider
nicht näher ausgeführt werden. Eine wichtige Rolle spielt jedoch die institutionelle Struktur der
Universität und der wissenschaftlichen Forschungsförderung. In den USA ist es v. a. der akade-
mische Mittelbau, derDH betreibt und im Gegensatz zu denfull professorseine doppelte Kompe-
tenz (EDV- und fachspezifische Kenntnisse) besitzt. Die programmatische Forderung nachhack
statt yack (also Praxis statt Theorie) kann vor diesem Hintergrund auch als Verteidigung der
eigenen Forschungsfelder gegen die Übernahme durch etablierte Professoren im Machtfeld der
Universität gedeutet werden. Anders ist die Situation in der Bundesrepublik. Hier wurde durch
massive Förderung gerade durch das BMBF die Entwicklung einer Strukturvon obenunterstützt.
7 So Lauer (2013, 101): „Die rechnende Geisteswissenschaft muss vor diesem Hintergrund
geradezu als ein Oxymoron erscheinen.‚Digital Humanities‘ ist da ein handlicheres Label für
nicht ohne Weiteres zu integrierende Erweiterungen des Methodeninventars, die über qualitativ-
interpretierende Verfahren hinausgehen. Die Unschärfe der Bezeichnung ist dabei den episte-
mischen Passungsschwierigkeiten von Methodik und Disziplin geschuldet.“
8 So Rieder/Röhle (2012, 72):„Digital humanities – an endeavour at the forefront of crossing
boundaries and research traditions– would seem to bridge the gap between the‚two cultures‘
[… ], between the quantitative orientation of the natural sciences and critical cultural discourses
in the humanities. Computational methods would provide the means to generate new kinds of
knowledge in a productive and unconventional way.“
New Visual Hermeneutics 29

Analyse von Visualisierungen.9 Die Implikationen der hier skizziertenNew Visual
Hermeneutics für hypothesentestende Erkenntnisinteressen werden dabei nur am
Rande Gegenstand unserer Ausführungen sein.
Ihde hat sein Konzept einer experimentellen Phänomenologie im Rahmen der
klassischen Phänomenologie entwickelt, aber (noch) nicht mit Blick auf die
Erfordernisse der Interpretation komplexer, digital generierter Visualisierungen.
Die Arbeiten von Rosenberger (2009; 2011a; 2011b) stellen prototypische Anwen-
dungen von Ihde im Bereich der Visual Analytics dar. Rosenberger reflektiert
jedoch ausschließlich auf die phänomenologischen Implikationen bei der Bild-
interpretation in den Naturwissenschaften. Unser Ziel ist es daher, einen inte-
grativen Ansatz zur epistemisch-methodischen Fundierung einer Analyse von
Visualisierungen in den DH vorzulegen, die auch für Visualisierungen in der
Sprachwissenschaft fruchtbar gemacht werden kann. Wir schlagen hierfür den
eingangs bereits genannten Begriff‚New Visual Hermeneutics‘vor.
Die New Visual Hermeneutics zur Erzeugung relevanten neuen Wissens
zeichnen sich durch eine holistische Perspektive aus, die die epistemischen
Interdependenzen unterschiedlicher Phasen der„visualization pipeline“ (Ren-
sink 2014, 153)konstitutiv berücksichtigt. Eine zentrale Einsicht dieses Ansatzes
lautet ‚Code ist Theorie‘, eine andere, dass für eine phänomenologisch fundierte
Perspektive die Validität hermeneutischer Interpretationen von Visualisierun-
gen von dem Verstehenaller Operationen auf den unterschiedlichen Stufen der
„visualization pipeline“ basiert.10
9 Unser Begriff reflektiert in einer Analogie zum New Criticism und New Historicism die
klassische Hermeneutik. Darüber hinaus verweist er auf Kernsätze der beiden Literaturtheorien,
die in denDH eine wichtige Rolle spielen. DieDH betonen zwar in Anlehnung an Franco Moretti
(2009; 2013) das„distant reading“, allerdings in geisteswissenschaftlicher Perspektive häufig in
Kombination mit dem„close reading“ des New Criticism. Mit demNew Historicismteilen sie die
durch Metadaten vermittelte „Geschichtlichkeit der Texte“ und in der Aufhebung der Grenze
zwischen Text und Bild die„Textualität von Geschichte“ (vgl. Montrose 1995, 67; Baßler 1995; zur
„Zirkulation sozialer Energie“ in und zwischen den verschiedenen Medien vgl. Greenblatt 1993).
10 Der vorliegende Aufsatz skizziert die theoretischen und methodischen Grundlagen der New
Visual Hermeneutics. Es ist uns bewusst, dass die Überzeugungskraft unseres Vorschlages nicht
nur auf der theoretisch-konzeptionellen, sondern auch auf der Ebene der praktischen Anwen-
dung verortet ist. Es würde jedoch sowohl die Zielsetzung dieses Aufsatzes als auch seinen
Umfang sprengen, wenn wir der theoretischen Explikation eine empirische Anwendung zur Seite
stellen würden. Eine erste, noch tentative, eher empirisch-praktisch orientierte Anwendung
unserer grundlegenden Überlegungen findet sich Kath (2014).
30 Roxana Kath, Gary S. Schaal, Sebastian Dumm

2 Der Stand der Forschung:Theorizing oder Doing?
Die DH sind in eine neue Phase eingetreten (vgl. Schnapp et al. 2009; Presner
2010; Berry 2011; Drucker 2012), die für ihre weitere Entwicklung sowohl im Sinne
ihrer Innovationsfähigkeit als auch mit Blick auf ihre Akzeptanz jenseits der
eigenen epistemischen Gemeinschaft prägend sein wird. Diese neue Phase ist
gekennzeichnet durch die Notwendigkeit, zentrale Weichenstellungen hinsicht-
lich der epistemischen, (wissenschafts-)theoretischen und methodischen Grund-
lagen vorzunehmen.
Mit dem Konzept descomputational turn(Berry 2011) soll der grundlegende,
aktuell stattfindende Medienwandel (vgl. Hepp 2011) bezeichnet werden. Er
begründet die Erwartung, dass dieDH und ihre Tools eine zunehmend größere
Rolle spielen werden, und zwar sowohl in den Geisteswissenschaften als auch
den Sozialwissenschaften. Zwei zusammenhängende Phänomene verlangsamen
aus unserer Perspektive die volle Entfaltung des oben skizzierten erkenntnis-
generierenden Potentials derDH jedoch:
–
Berry (2011, 1) argumentiert, dass die dem Forschungsprozess zugrundeliegen-
den Epistemologien und Ontologien durch dencomputational turngrundlegend
verändert werden. Diese veränderten epistemischen Grundlagen derDH bedür-
fen noch einer grundlagentheoretischen und methodischen Reflexion.
– Es existiert noch keinebest practice, die den Forschungsprozess in denDH
strukturierend anleiten kann. Daher werden kumulativer Erkenntnisgewinn
und eine zielgerichtete Entwicklung derDH deutlich erschwert.
Denn erst die Explikation der epistemischen, (wissenschafts-)theoretischen und
methodischen Grundlagen entlang konkreter Forschungsprozesse in den DH
kann zur Ausbildung einer gehaltvollen best practice führen. Gerade daran
mangelt es jedoch (Cecire 2011, 45):„Digital humanities is undertheorized“. Auf
einer deskriptiven Ebene ist diese Diagnose innerhalb derepistemic community
weithin akzeptiert, auf normativer Ebene jedoch stark umstritten. Die Gegen-
position lautet:doing researchstatt theorizing.11
11 Dabei wurde die Bedeutung von epistemischen Fragen für die Entwicklung der DH bereits
2004 in Schreibman et al. adressiert, die Beiträge wurden jedoch weder systematisch theoretisch
aufgegriffen, noch in der Forschungspraxis berücksichtigt (vgl. Berry 2011, 4; 2011; Ramsay/
Rockwell 2012). Trotz einiger Statements zur Bedeutung von Theorie für die DH (Cecire 2011a;
2011 b) steht im Kern des Selbstverständnisses der DH community aktuell die Position, dass die
DH sich im doing bewähren (also hack) und nicht in der theoretischen Reflexion des theorizing
(also yack, umgangssprachlich‚Herumgeplappere‘) (vgl. affirmativ Takahashi 2012).
New Visual Hermeneutics 31

Aus der Untertheoretisierung ergeben sich jedoch gravierende Herausforderun-
gen, deren Adressierung für die Weiterentwicklung derDH von zentraler Bedeu-
tung ist: Programme und Algorithmen sind erkenntnistheoretisch nicht neutral,
da jeder komplexere Algorithmus Theorie ist, allerdings in einer nichtsemanti-
schen Form (vgl. Becker 2012). Wenn Algorithmen Theorie sind, dann müssen
Standards der theoretischen Güte von Algorithmen entwickelt werden, d. h. der
digitalen Modellierung von Theorie.
In den DH nehmen Visualisierungen von Daten im Prozess der Erkenntnis-
gewinnung eine zentrale Stellung ein. Doch auch hier muss man sich weitaus
stärker als bisher geschehen der epistemischen Implikationen und Konsequenzen
von Visualisierungen bewusst sein, denn„visualization tools work like herme-
neutical theories“ (Ramsay/Rockwell 2012, 79). Wenn Visualisierung selbst eine
Interpretation der Daten ist, wird für deren Verständnis eine neue Form der
Hermeneutik benötigt, gleichsam eine Hermeneutik zweiter Ordnung, die den
Prozess der Generierung von Visualisierungen konstitutiv berücksichtigt. Eine
solche Methodik bezeichnen wir alsNew Visual Hermeneutics.
Die Tools derDH basieren auf statistischen Methoden. Doch existieren nur
wenige belastbare und allgemein akzeptierte statistische Standards und Tests,
anhand derer ihre Güte und Angemessenheit bewertet werden kann (vgl. Kople-
nig 2014; vgl. jedoch auch Moisl 2013 und Baroni/Evert 2008). Dies gilt beispiels-
weise auch für die sozial- und kulturwissenschaftlich interessierte Sprachwissen-
schaft, in der die Validität und Reliabilität von korpuslinguistischen Methoden
noch zu wenig diskutiert wird.
Die von uns vorgeschlagene neue visuelle Hermeneutik versucht in ihren
Grundkategorien die hier nur skizzierten Herausforderungen zu berücksichtigen.
Sie soll im nächsten Schritt in ihren Grundzügen entfaltet werden.
3 New Visual Hermeneutics
Die neue visuelle Hermeneutikist ein methodischer Ansatz für die Generierung
von Wissen mittels explorativer Analysen aus großen,unstrukturierten Text-
daten mit Hilfe einer Information Visualization.12 Unser Ansatz ist somit im
12 „One core difference between Information Visualization and Visual Analytics lies in the
support of analytical workflows and the generation and validation of hypothesis.“ (Seifert et al.
2014, 197) Eine„allgemeine Visualisierungswissenschaft fehlt bis heute; damit auch ein über-
geordneter und etablierter Theorierahmen.“ (Burkhard 2006, 202)
32 Roxana Kath, Gary S. Schaal, Sebastian Dumm

größeren Forschungsfeld derVisual Analytics13 verortet (vgl. Keim et al. 2010).
Aus dem explorativen Charakter einer Visualisierungsanalyse folgt zumeist,
dass „the questions are ill-defined or unknown apriori and training data is not
available“ (Endert 2014, 2), so dass sich relevantes neues Wissen erst aus einer
hermeneutischen Interpretation ergibt.14 In diesem Sinne besteht einkonstituti-
ver Zusammenhang von Phänomenologie und Hermeneutik in derneuen visuel-
len Hermeneutik. Der besondere Fokus der neuen visuellen Hermeneutik liegt
erstens auf einerintegrativen Betrachtung des gesamten Prozesses der Visua-
lisierung (vgl. Abb. 1 und insb. Abb. 2 für eine graphische Darstellung der
Phasen). Besondere Aufmerksamkeit liegt hierbei auf densystematischen Kon-
sequenzen bestimmter methodisch-konzeptioneller Entscheidungen in den Pha-
sen des Datasampling (1), der algorithmenbasierten Analyse der Daten (2) sowie
der konkreten Visualisierung (3) für die Interpretation dieser Visualisierungen
(4).15 Zweitens zeichnet sich dieneue visuelle Hermeneutikdurch einen beson-
deren hermeneutischen Ansatz aus, die experimentelle Phänomenologie von
Don Ihde (1998; 2012). Diese ist nicht auf Phase 4 begrenzt, sondern liegt als
Epistemik dem gesamten Ansatz zugrunde.
Ihde (2012) prägte den Begriff der‚visual hermeneutics‘, der hier jedoch in
einer konzeptionell stark erweiterten Form genutzt wird. Der hier vorgeschlagene
Ansatz der neuen visuellen Hermeneutik bezieht sich nicht nur auf die Ausdeu-
tung des Gegebenen, sondern berücksichtigt auchkonstitutiv den Prozess des
Geworden-Seins, der Generierung der Visualisierung, indem er die Feedback-
schleifen zwischen den unterschiedlichen Stufen der Analysen auf ihre episte-
mischen Implikationen hin reflektiert.16
13 „Visual Analytics is an interdisciplinary field based on information visualization, knowledge
discovery and cognitive and perceptual sciences, which deals with designing and applying
interactive visual user interfaces to facilitate analytical reasoning.“ (Seifert et al. 2014, 190)
14 Weiter Endert (2014, 2):„Stasko points out that while text analytics and visualizations are
helpful in structuring the information, eventually the analyst must ,read and understand the
actual text documents‘to gain semantic insight and report a finding (Stasko et al. 2008). [… ] This
approach must be situated within an understanding of human cognitive reasoning processes.“
15
Die Notwendigkeit einer integrierten Perspektive wird von Landesberger et al. (2014, 655)
angesprochen: „Tracking of an analytical process is based on the underlying interaction taxonomy.
At present, however, only separate taxonomies for interaction techniques exist in the three Visual
Analytics fields [… ]. None of them covers the whole Visual Analytics area, so the interwoven
character of the Visual Analytics process cannot be captured. Their application in complex Visual
Analytics systems is therefore limited.“ Vgl. aber Grotz et al. (2008), Heer et al. (2012) und Card et
al. (1999) für eine dynamische Betrachtung der Relationen der drei distinkten Phasen.
16 Endert et al. (2014, Fig. 1) erkennen ebenfalls die Notwendigkeit eines integrativen Ansatzes,
sprechen jedoch im Rekurs auf Paroli/Card (2005) von der„sense-making loop for analysts“.
New Visual Hermeneutics 33

Die neue visuelle Hermeneutikdifferenziert zwischen den vier distinkten, aber in
konstitutiver Verbindung stehenden Arbeitsschritten.
Damit greifen wir auf eine Differenzierung zurück, die– zumindest in ihrer
Grundstruktur – innerhalb der Visual Analytics inzwischen allgemein akzeptiert
ist. Seifert et al. (2014, 191) sprechen z. B. von der„Processing Pipeline for Visual
Analysis of Text“, Rensink (2014, 153) von der „visualization pipeline“ und
Landesberger et al. (2014, 655) von„interaction types in visual analytics“.
Landesberger et al. (2014) konzeptualisieren diese Pipeline mit drei Phasen:
Abbildung 1:Interaction Types in Visual Analytics nach Landesberger et al. (2014, 655)
Die drei Phasen von Landesberger et al. (2014) entsprechen auch unserer Model-
lierung (1, 3, 4), jedoch ergänzen wir die Phase der algorithmenbasierten Analyse
(2), da dieser eigene theoretisch-methodische Vorannahmen zugrunde liegen und
bezeichnen den gesamten Prozess inklusive seiner Feedbackschleifen alsneue
visuelle Hermeneutik:
34
Roxana Kath, Gary S. Schaal, Sebastian Dumm

Abbildung 2:New Visual Hermeneutics (eigene Abbildung)
3.1 Analyseschritt 1: Acquisition/Repository/
Semantic Enrichment
Ein Algorithmus ist aber bekanntlich nur so viel wert wie die Daten, mit denen er gefüttert
wird. Also müssen auch diese transparent gemacht werden, und zwar in leicht verständli-
cher, lesbarer Form. (Noller 2012)
Der erste Analyseschritt der New Visual Hermeneutics gilt den sogenannten
„Rohdaten“,17 denn im Prozess der Datenakquise und Datenauswahl, Aufberei-
tung und Langzeitspeicherung werden bereits wichtige Entscheidungen getrof-
fen, die die späteren Auswertungen wesentlich beeinflussen. Allerdings haben
Geistes- und SozialwissenschaftlerInnen aus verschiedenen Gründen häufig kei-
17 Eine wichtige epistemische Frage wirft Bollier (2010, 13) auf:„Als große Masse von Rohinfor-
mationen sind Datenmengen nie selbsterklärend. Und die verschiedenen Methoden zur Inter-
pretation der Daten können Gegenstand aller möglichen philosophischen Debatten sein. Können
Daten eine‚objektive Wahrheit‘repräsentieren? Oder wird jede Interpretation notwendigerweise
durch subjektive Filter oder die Art und Weise, wie die Daten‚gesäubert‘wurden, verzerrt?“
New Visual Hermeneutics 35

nen direkten Einfluss auf diese Entscheidungen. Einige der Gründe und mögliche
Konsequenzen sollen hier im Folgenden kurz skizziert werden.18
– Datenschutz- und Urheberrechtsbestimmungen beeinflussen den Zugang zu
Daten und die Art ihrer Auswertung. Beispielsweise können private Anbieter
(Oligopole oder Monopole) über Gebühren und Nutzungsrechte den Zugang
zu Datenbeständen regulieren. Die Frage der Verwendung von Visualisierun-
gen, die aus geschützten Daten hervorgehen, z. B. die Reproduktion zum
Zwecke des wissenschaftlichen Beleges in einer Publikation, ist bisher lizenz-
rechtlich kaum geregelt.
–
Alternativ übernehmen kommerzielle Anbieter wie z. B.Google Booksoder
die Open Book Alliance(Amazon, Microsoft und Yahoo) die Digitalisierung
großer Textbestände, deren Qualitätskriterien den Wissenschaftlern entzo-
gen sind (s. u.).
– Die Langzeitarchivierung von Daten ist in der Regel Aufgabe ‚klassischer‘
Forschungsinfrastrukturen wie Bibliotheken, Archive und Sammlungen sowie
digitaler Fachinformationsdienste bzw. -zentren (z. B. das Göttinger Digitalisie-
rungszentrum [GDZ]
19 oder das Zentrum für Elektronisches Publizieren [ZEP]20
der Bayerischen Staatsbibliothek München).
Auch die Qualität der Textcodierung hat Einfluss auf die Analyse, denn letztlich
arbeiten die Suchalgorithmen auf der Ebene von Zeichenketten. Inwiefern die Anno-
tierung mit linguistischen Kategorien bereits ein Interpretationsakt ist, zeigt der
Beitrag von Heike Zinsmeister in diesem Band. Den Einfluss von Fehlern in der
Textcodierung auf die Suchergebnisse und deren Interpretation hat Sullivan (2010)
am Beispiel desGoogle Ngram Viewerund den Schwächen von OCR (optical character
recognition) bei älteren Drucken eindrucksvoll vorgeführt (vgl. Schubert 2013, 181/
Anm. 29). Analog stehen altertumswissenschaftliche Projekte derDH häufig vor
Herausforderungen, die sich aus den besonderen Schwierigkeiten der Kodierung
altsprachlicher Texte und/oder deren OCR ergeben.21 Die Entscheidung darüber,
18 Vgl. hierzu auch die Empfehlungen des Wissenschaftsrates zu Forschungsinfrastrukturen in
den Geistes- und Sozialwissenschaften v. 28.1.2011, 50 u. 51; 55– 58; 64 u. 65; http://www.
wissenschaftsrat.de/download/archiv/10465-11.pdf
19 http://gdz.sub.uni-goettingen.de/gdz/
20 https://www.bsb-muenchen.de/Zentrum-fuer-Elektronisches-Publizieren-ZEP.2349.0.html
21 Die historisch arbeitenden Altertumswissenschaften (Alte Geschichte, Klassische Philologie,
Epigraphik, Papyrologie) greifen heute alle auf digitalisierte Textkorpora zurück, die in un-
terschiedlichsten Formen (digitalisierte Bibliotheken im Internet, auf CD-ROM) und Formaten
(z. B. verschiedene ASCII– basierte Beta-Code-Varianten und UNICODE-basierte UTF-Formate)
vorliegen, weswegen diese Projekte auch untereinander kaum oder gar nicht vernetzt sind.
36 Roxana Kath, Gary S. Schaal, Sebastian Dumm

diakritische Zeichen in einem digitalisierten Text abzubilden oder wegzulassen, hat
immensen Einfluss auf das spätere wissenschaftliche Ergebnis. Häufig müssen
jedoch aus Performanzgründen der Datenbank Kompromisse über die Auszeich-
nungstiefe gefunden werden. Dasselbe gilt auf der Ebene der Metadaten, wobei die
Qualität der Annotationen hier eher eine Frage der zur Verfügung stehenden fach-
wissenschaftlichen Ressourcen und weniger eine technische Frage ist.
Die Visualisierungen in denDH basieren häufig auf den dahinterliegenden
Metadaten (z. B. das im Rahmen von eAQUA entwickelteMental Maps Tool).22
Dabei gilt es zu bedenken, dass vor allem in den historischen Disziplinen bereits
die Inhalte der Metadaten (auch Namen und Orte zu Autoren o. Ä.) Ergebnisse
wissenschaftlicher Interpretation sind. Die Informationen werden in der Regel
aus Lexika, Fachpublikationen oder Originalquellen entnommen, allerdings blei-
ben dabei viele Unsicherheiten (z. B. bei Pseudo-Autoren, Autorenkollektiven
oder Scholien) und Leerstellen. Autoren, von denen keine Lebensdaten und Orte
überliefert sind, können in georeferenzierten Visualisierungen eigentlich nicht
abgebildet werden und würden im Suchergebnis nicht berücksichtigt.
23 Aufgrund
ihrer Abstraktion erzeugen die Visualisierungen hier folglich z. T. historisch
falsche Ansichten. Das Projekt„eXChange: Exploring Concept Change and Trans-
fer in Antiquity“24 versucht, dieses Problem durch eine dynamischere Metadaten-
auswahl zu lösen, die es ForscherInnen erlaubt, eigene Hypothesen (z. B. den
Einfluss einer alternativen Datierung eines oder mehrerer Werke) zu testen.
Eine Alternative und Ergänzung zur interaktiven Gestaltung der Datengrund-
lage ist die Standardisierung.25
Der Wissenschaftsrat begreift den Prozess der Standardisierung und Interoperabilität digi-
taler Angebote als eineconditio sine qua nonfür die Herausbildung einer europäischen
Forschungsinfrastruktur in den Geisteswissenschaften. Standardsetzung ist hierbei nicht als
einmaliger Akt, sondern als ein permanenter Prozess der Qualitätssicherung und Prüfung
der Standards zu begreifen.
26
22 http://www.eaqua.net/sti/; vgl. hierzu Kath (2011).
23 Bei der Entwicklung von Mental Maps wurde dieses Problem dadurch kompensiert, dass
diese Autoren in„Atlantis“ bzw. „Utopia“ lokalisiert werden.
24 http://www.exchange-projekt.de
25 Beispiele für Standardisierungen sind u. a. ISO-Standards für die persistente Referenzierbar-
keit von Sprachressourcen (ISO/DIS 24619),Persistent identifier(PI) bzw.digital object identifier
(DOI) zur eindeutigen Identifizierung und Zitierbarkeit digital hinterlegter Daten, Standards zur
Auszeichnung von Texten wie TEI P5 und Metadatenstandards wie der Dublin Core Metadaten-
standard (DCMI); vgl. hierzu die Empfehlungen des Wissenschaftsrates zu Forschungsinfrastruk-
turen in den Geistes- und Sozialwissenschaften v. 28.1.2011, 58; 62; 65.
26 Ebd. 66.
New Visual Hermeneutics 37

Für die Sozialwissenschaften gelten ähnliche Überlegungen hinsichtlich der
Selektivität der ‚Rohdaten‘, die analysiert werden. Immer häufiger werden in
den Sozialwissenschaften Analysen von Twitternachrichten durchgeführt. 27
Boyd/Crawford (2013) haben mit Nachdruck darauf hingewiesen, dass es für die
analysierenden WissenschaftlerIn nicht transparent ist, aufwelche gesendeten
Daten sie Zugriff hat, d. h., wie repräsentativ die analysierten Daten für die
Grundgesamtheit aller Twittermeldungen sind.
28 Zeitungen stellen in den Sozial-
wissenschaften eine weitere wichtige Datenquelle dar. Doch auch hier stellen sich
kritische Fragen hinsichtlich der Auswahl der Rohdaten: Von einigen Zeitungen
existieren regulär unterschiedliche Druckausgaben (z. B. regionale und nationale
Ausgaben); von einzelnen Ausgaben können im Druck unterschiedliche inhalt-
liche Varianten aufgrund aktueller Ereignisse existieren. Einige Zeitungen stellen
Auszüge ihrer Printausgabe ins Netz und aktualisieren diese Beiträge im Laufe
des Tages. Welche dieser Rohdatenvarianten sollen für die Analyse herangezogen
werden? Welche sind für die ForscherInnen überhaupt zugänglich? In welchen
Fällen ist ihr überhaupt bewusst, dass unterschiedliche Varianten existieren?
Diese Fragen sind nicht neu, sie gewinnen jedoch durch die Möglichkeit der
permanenten Aktualisierung von Zeitungsnachrichten im Internet an Relevanz.
Unsere exemplarischen Überlegungen verdeutlichen, dass die Frage nach der
Qualität der Rohdaten gleichermaßen für Geistes- und SozialwissenschaftlerIn-
nen – wenn auch mit unterschiedlichen Schwerpunkten– hochrelevant ist. Sie
verdeutlichen jedoch auch, dass die Frage nach der Repräsentativität von Daten,
nach dem Verhältnis von Sample und Grundgesamtheit, auch in Zeiten von Big
Data nicht irrelevant geworden ist, sondern in neuer Form wieder erscheint.
3.2 Analyseschritt 2: Text-Mining & Information Retrieval
Als knowledge discovery (KD) wird der Prozess„of automatically processing large
amounts of data to identify patterns and extract useful new knowledge“ (Seifert
et al. 2014, 189) bezeichnet. In dem hier interessierenden Fall steht dieKD auf Basis
von unstrukturierten Daten im Fokus. DaText Mining und Information Retrieval
eigene Disziplinen mit eigenen theoretisch-methodischen Grundlagen sind,29 soll
27 Vergleiche hier beispielsweise das Projekt„Analyse von Diskursen in Social Media“ http://
www.social-media-analytics.org/de/
28 So existieren unterschiedliche Niveaus von Zugangsrechten für Twitterdaten. Die Kriterien,
nach denen die bereitgestellten Daten gefiltert werden, sind jedoch nicht vollständig transparent.
29 Vgl. zur Einführung u. a. Heyer et al. (2006); Mehler (2004); Gorunescu (2011).
38 Roxana Kath, Gary S. Schaal, Sebastian Dumm

im Folgenden nur kursorisch angerissen werden, welche Verfahrensschritte aus
epistemischer Perspektive im Rahmen unsererNew Visual Hermeneuticsdetaillier-
terer Betrachtung bedürften.
Rieder und Röhle (2012, 75) argumentieren mit Blick auf die Methoden des
Information Retrieval: „In creating truly digital methods we mechanise parts of
the heuristic process, and we specify and materialise methodological considera-
tions in technical form.“
Dieser Einschätzung folgen wir und reformulieren sie auf einer noch abs-
trakteren Ebene: Codeist Theorie und dies in doppelter Perspektive. Einerseits
sind die eingesetzten Verfahren und Algorithmen (im Folgenden: Code) selbst
Erscheinungsformen theoretischer Überlegungen und in diesem Sinne muss der
Code konstruktvalide sein, d. h. er muss in seiner Anwendung das empirisch
messen, was er theoretisch messen soll.
30 Dieses Erfordernis betrifft v. a. einen
innovativen Code (Analysemethoden). Notwendig wird damit ein qualitäts-
sicherndes Verfahren der Validierung des Codes auf der Ebene der Programmie-
rung und auf der Ebene des zu messenden Konzepts. Andererseits sollte– selbst
unter Maßgabe der explorativen Nutzung derDH – die Anwendung des Codes
theoretischen Kriterien unterliegen. So macht es z. B. bei der Analyse von Tages-
zeitungen theoretisch-konzeptionell einen großen Unterschied, ob die Referenz-
einheit der Satz, der Absatz oder der Artikel ist. Die Begründung der ausgewähl-
ten Referenzeinheit sollte der Anwendung des Codes vorgängig sein. Auch sollten
z. B. die datentechnischen Voraussetzungen und dietheoretischen Implikation
der Anwendung unterschiedlicher mathematischer Verfahren der Dimensions-
reduktion vor deren Anwendung bekannt sein.
Erst in dieser doppelten Perspektive werden die Implikationen der These
‚Code ist Theorie‘ in ihren Umrissen deutlich: Code ist ein Erscheinungsmedium
von Theorie– genau wie Sprache– und muss daher ähnlichen Validitätsprüfun-
gen unterzogen werden wie sprachlich vermittelte Theorien. Zugleich muss die
Anwendung von Theorie selbst theoretisch begründet werden, um keine rein
datengetriebene Forschung zu sein.
Vor einem eher gesellschaftlich-politischen Hintergrund hat Stefan Noller in
der Frankfurter Allgemeinen Zeitung (2012) eine Algorithmenethik gefordert, die
sich v. a. durch Transparenz auszeichnen müsse:
Algorithmen müssen transparent gemacht werden, sowohl in ihrem Einsatz als auch in ihrer
Wirkweise. Das wäre auf den ersten Blick am einfachsten durch eine Publikationspflicht des
Algorithmus im Quellcode zu bewerkstelligen. (Noller 2012; vgl. hierzu auch Schubert 2013, 186)
30 Vgl. weiterführend zu Konstruktvalidität Campbell/Fiske (1959); Wirth/Matthes (2008).
New Visual Hermeneutics 39

Noller selbst weist allerdings darauf hin, dass der Quellcode allein u. U. nicht für
jede NutzerIn verständlich sein wird. Dies gilt auch für die mit den mathematisch-
technischen Vorentscheidungen der InformatikerInnen konfrontierten Geistes-
und SozialwissenschaftlerInnen. Die darauf antwortende Forderung nach einer
umfassenden wechselseitigen Kompetenz, die einen neuen Typus Wissenschaft-
lerIn – den Digital Humanist– hervorbringen würde, erscheint aus verschiedenen
Gründen dennoch unrealistisch. Abgesehen von den fachinternen und -externen
Widerständen, die das hervorrufen würde, und der Tatsache, dass es dennoch
immer WissenschaftlerInnen geben wird, die einfach weiter dem explorativen
Versprechen der DH folgen werden, ist es u. E. unmöglich, eine umfassende
Einsicht in alle technischen und nicht technischen Vorentscheidungen zu errei-
chen. Was wir jedoch anregen möchten, ist ein kritisches Bewusstsein für das
Geworden-Sein der Datenbestände und deren Auswertungsergebnissen.
3.3 Analyseschritt 3: Visualisierung der Daten
The inherent possibilities of computational visualization for exploration, investigation,
experimentation and, ultimately, representations are unlimited.
Dies schrieb DiSalvo (1998, 83) bereits 1998. Auch Seifert et al. (2014, 190) betonen
im Kontext derDH, dass der Visualisierung eine besondere Bedeutung zukommt,
da sie „an enabler for exploratory analysis“ ist, „making it a powerful tool for
gaining insight into unexplored data sets“ (ebd.). Die Visualisierung darf jedoch
nicht erkenntnistheoretisch naiv betrachtet werden, denn es existiert keine‚neu-
trale‘ Form der Visualisierung. Dies betonen auch Rieder/Röhle (2012, 69):„This
does not mean that questions of visual arrangement are epistemologically inno-
cent, quite the contrary.“ Die Visualisierung selbst ist eine Interpretation von
Daten. Da jede Visualisierung auf theoretischen und methodischen Grundannah-
men beruht, müssen sie den interpretierenden WissenschaftlerInnen transparent
sein. Die erste Anforderung an eine angemessene Form der Visualisierung besteht
daher darin, dass den interpretierenden WissenschaftlerInnen die der Visualisie-
rung vorgängigen prozessualen Schritte in ihren Konsequenzen für die konkrete
Visualisierung bewusst sein müssen. Die Kontingenz einer Visualisierung muss
genauso transparent sein wie die Pfadabhängigkeiten im Prozess ihrer Erstellung.
31
Die Wertschätzung des Explorativen in den DH verschleiert partiell die
Tatsache, dass bei vielen Visualisierungen häufig Unklarheit darüber besteht,
welche gewählten Parameter angemessene, d. h.bedeutungstragende Visualisie-
31 Vgl. hierzu Drucker (2011).
40 Roxana Kath, Gary S. Schaal, Sebastian Dumm

rungen generieren (vgl. Keim et al. 2010, 102). Nicht ohne Grund hat sich in vielen
Projekten der DH die Praxis einer Methodentriangulation mitstreet-level-episte-
mology etabliert, die die Angemessenheit von Visualisierungen anhand von Daten
validiert, die den ForscherInnen bekannt sind. Diese Validierung scheitert jedoch
dann, wenn das analysierte Corpus in seiner Detailstruktur den ForscherInnen–
beispielsweise aufgrund seiner schieren Größe – nicht mehr bekannt ist und
wenn mit Hilfe von Visualisierungen Aussagen auf der Makroebene der Daten
getroffen werden sollen.32 Spätestens dann werden Benchmarks benötigt, um die
Angemessenheit einer Visualisierung zu bestimmen, denn der Erkenntnisgewinn
variiert in Abhängigkeit von der Visualisierung der Daten.
Diese Überlegungen führen zur zweiten epistemischen Herausforderung,
die Rensink (2014, 148) in Form von drei Fragen adressiert:„What is the best
way to measure how a given visualization works? How could we find the
perceptual and cognitive factors that limit its performance? Could we determine
if its design is optimal?“
Viele der Benchmarks innerhalb derInformation Visualization(vgl. Keim et al.
2010) sind eher technischer Natur und orientieren sich an der usability von
Visualisierungsumgebungen. Diese technizistischen Benchmarks erscheinen im
wissenschaftlichen Kontext des Erkenntnisinteresses in denDH jedoch unange-
messen. Liu et al. (2013, 543) argumentieren,„what is important is the ability to
discover high-value insights that somehow are ,hidden‘in the unimaginably vast
amount of low-value digital data that is scattered and unstructured“. Diesen
Überlegungen können wir uns anschließen, denn gerade wenn Visualisierungen
in explorativer Perspektivegenutzt werden, sollte die Visualisierung möglichst so
gestaltet sein, dass neue Einsichten angeregt werden. Diese Offenheit der Auf-
gabe – Rensink (2014, 154) spricht abwertend davon„just find something interes-
ting“– ist es, die eine Visualisierung nahelegt, dielatentes Wissen, dass in den
Daten vorhanden ist, durch eineadäquate Form ihrer graphischen Repräsenta-
tion für die BetrachterInnen sichtbar werden lässt. Daraus folgt ein wichtiges
Qualitätskriterium von Visualisierungen: die Ermöglichung von bedeutungsvol-
len wissenschaftlichen Einsichten und Erkenntnissen. Und nicht jede Form der
Visualisierung ist dafür gleich gut geeignet.
In diesem Kontext möchten wir jedoch keine Benchmarkliste entwickeln, um
die Qualität von Visualisierungen objektiv bewerten zu können. Das Gegenteil ist
vielmehr der Fall, da die explorative Nutzung von Visualisierungen bestimmte
Konventionen und Erwartungen, die an Visualisierungen gemeinhin gestellt wer-
32 Hier kollidieren zwei prototypische Verständnisse miteinander: Visual Analytics als‚Such-
maschine‘für close readingund Visual Analytics als‚Generator von Makroaussagen‘.
New Visual Hermeneutics 41

den, unterläuft. Wie im Abschnitt 3.4 detailliert ausgeführt wird, plädieren wir für
eine experimentelle Phänomenologie, welche die Polylatenz von Visualisierungen
betont. Ihde (2012, 47) spricht in diesem Kontext von„multistable configurations“,
d. h. von pluralen Deutungen ein und derselben Visualisierung, die jedochglei-
chermaßen valide sind. Gerade wenn Visualisierungen also in explorativer Per-
spektive genutzt werden sollen, folgt daraus, dass die Frage von Rensink (2014,
148) „is there a best way to visually display a given dataset for a given task, and if
so, can we find it?“, für die DH nicht angemessen ist, da sie im Kontext eines
Wissenschaftsverständnisses artikuliert ist, das dort Eindeutigkeit erwartet und
anstrebt, wo Polylatenz, multiple Bedeutungen und interpretative Offenheit er-
wünscht und notwendig sind. Aus unserer epistemischen Grundposition folgt
auch, dass Eineindeutigkeit von Visualisierungen und ihre identische Reproduzier-
barkeit über die Zeit als normative Ideale kritisch reflektiert werden müssen.
33 Es ist
wahr, dass dieDH, um die Intersubjektivität von Interpretation von Visualisierun-
gen zu sichern, stabile Formen von Visualisierungen benötigt. Identische Formen
von Visualisierungen legen jedoch auch pfadabhängige Interpretationen nahe, die
ihre epistemische Autorität aus der identischen Reproduzierbarkeit von Visuali-
sierungen ziehen. Wenn jedoch– wie im Abschnitt 3.4 näher ausgeführt wird–
Visualisierungen in denDH häufig multistable configurationssind, können Iteratio-
nen in der Visualisierung zu produktiven Irritationen führen, die die Polylatenz von
Visualisierungen immer wieder ins Bewusstsein rücken.
Jenseits dieser eher epistemisch motivierten Überlegungen zu Visualisierun-
gen existieren objektive Qualitätsfaktoren von Visualisierungen. So ist es von
zentraler Bedeutung das der Forscher weiß, welche Dimensionen einer konkreten
Visualisierung bedeutungstragend und welche kontingenter Natur sind: trägt die
Verortung im Raum Bedeutung, die Dicke der Verbindungen zwischen Begriffen,
die Farbe von Zeichen?
Relevant ist jedoch auch, welche Strukturen einer Visualisierung typischer-
weise als bedeutungstragend identifiziert wurden, unabhängig davon, ob die
konkrete Visualisierung dies impliziert. Diese Fragen sind auch an anderer Stelle
intensiv diskutiert worden (vgl. grundlegend Ware 2000 und aktuell Tversky
2014) und werden hier nicht weiter vertieft. Wichtig aus der Perspektive der
neuen visuellen Hermeneutik ist, dass die epistemischen Grundlagen der Inter-
pretation von Grafiken auch bedeutsame Implikationen für ihre Erstellung
besitzen. Relevant ist darüber hinaus die Einsicht in die Polyvalenz von Visuali-
33 Einen herzlichen Dank an Christiane Cromm, die uns erst auf diese Perspektive aufmerksam
gemacht hat.
42 Roxana Kath, Gary S. Schaal, Sebastian Dumm

sierungen, die Forderung nach kontrollierter Variabilität von Visualisierungen
sowie die Option ihrer Nicht-Eineindeutigkeit.
3.4 Analyseschritt 4: die hermeneutische Analyse einer
Visualisierung im Kontext einer empirischen
Phänomenologie
Bereits in der Einleitung haben wir die Prämisse dargelegt, dass dieDH eine
stärkere methodische, theoretische und epistemische Fundierung benötigen.34
Die Notwendigkeit, aber auch die Gewinne einer solchen Fundierung finden sich
besonders im vierten Analyseschritt, der konkreten Interpretation einer Visuali-
sierung. Wir plädieren in demAnsatz einer neuen visuellen Hermeneutikdafür,
zwei erkenntnistheoretische Ansätze miteinander zu verbinden. Es handelt sich
einerseits um dieHermeneutik, andererseits um die (empirische)Phänomenolo-
gie.
35 Die Angemessenheit der beiden Ansätze folgt direkt aus den inhärenten
Erfordernissen einer explorativen Nutzung von Visualisierungen in denDH.36
Als Hermeneutik bezeichnet man mit Dilthey (1957, 318)„den Vorgang, in
welchem wir aus Zeichen, die von außen sinnlich gegeben sind, ein Inneres
erkennen: Verstehen“. Damit ist das Ziel der Hermeneutik die Rekonstruktion
des in sprachlichen und anderen kulturellen Objektivationen zum Ausdruck
kommenden Sinns. Ausgangspunkt der Phänomenologie ist hingegen die trans-
zendentalphilosophische Frage nach den universellen Strukturen des Bewusst-
seins und seiner Operationsweise. Husserl (1993, 177) bezeichnete die Phä-
nomenologie entsprechend als eine „Hermeneutik des Bewusstseinslebens“.
Phänomenologisch kann mit Husserl (1976) argumentiert werden, dass Be-
wusstsein immer Bewusstsein von etwas ist. Das heißt zugleich, dass das
Bewusstsein die Dinge nur als seine eigenen Erlebnisinhalte in den Blick
bekommt. Die Frage, ob sie‚an sich‘ existieren, bleibt erkenntnistheoretisch
ausgeklammert. Sie liegen als Phänomene vor, als Bewusstseinsakte und -in-
halte, in ihrer Bedeutungfür uns.
34 Es versteht sich von selbst, dass hier nur eine Skizze vorgelegt werden kann, die plausibili-
sieren soll, warum Hermeneutik und (empirische) Phänomenologie eine angemessene episte-
mische und theoretische Fundierung für dieVisual Analyticsin denDH darstellen.
35 Im Folgenden fokussieren wir auf die Phänomenologie, da sie im Kontext unserer Überlegun-
gen grundlegender ist.
36 Vgl. für die Verbindung von Hermeneutik, Phänomenologie und Visualisierungen Ihde (1998;
2012); Verbeek (2007); Hasse (2008); Rosenberger (2009); Engström/Selinger (i. E.).
New Visual Hermeneutics 43

Sind die beiden Ansätze kompatibel? Kurt (2008, 369) diskutiert diese Frage und
kommt zu dem Ergebnis:„Hermeneutik und Phänomenologie sind Philosophien
der Subjektivität und Perspektivität. Sie fordern eine Denkhaltung, die die lebens-
weltlich fundierte Subjektivität, Perspektivität und Intentionalität des Bewusst-
seins-von-etwas beziehungsweise des Zeichensetzens und Zeichendeutens me-
thodisch kontrolliert mitreflektiert.“ Die Fluchtpunkte dieser Perspektivierungen
und der damit verbundenen anti-objektivistischen Art des Denkens variieren zwar
mit der jeweiligen Fokussierung auf Sinn bzw. Bewusstsein systematisch. Trotz-
dem – oder gerade durch ihre komplementären Perspektivierungen– ergänzen
sich die beiden Ansätze mit Blick auf die neue visuelle Hermeneutik ideal.
Denn Hermeneutik und Phänomenologie antworten (implizit) auf ein Prob-
lem der Analyse von Visualisierungen, das bereits Goethe (1948, 52) in einem
Brief an Friedrich von Müller beschreibt:„Man erblickt nur, was man schon
weiß und versteht.“ Goethes Aussage besitzt auch heute noch Gültigkeit und
wirft die eminent wichtige Frage auf, wie neues Wissen im Kontext von unklar
definierten Problemen generiert werden kann, wenn Sehen ein konstruktiver
Prozess ist undimmer bedeutet, „mit seinen Gedanken, Gefühlen, Erinnerun-
gen, Phantasien und Interessen [Dinge; d. A.] hinzufügen, wegnehmen, pro-
jizieren, übersehen, verschieben, vergrößern, verkleinern, zentrieren und selek-
tieren“ (Kurt 2008, 371) zu können.
Für die Generierung von relevantem neuen Wissens ist besonders das von
Husserl (1973, 139) beschriebene Prinzip derAppräsentation, d. h. das„als mit-
gegenwärtig-bewusst-machen“ von Bedeutung.37 Wir sehen mehrere Taschen-
bücher in den Farben des Regenbogens und denken‚Suhrkamp‘, wir sehen die
Vorderseite eines Hauses und denken‚Haus‘– und nicht‚Potemkinsches Dorf‘– ,
d. h. wir sehenetwas (einen Teil) und erkennen esals etwas im Rahmen eines
größeren Kontextes, der der konkreten Wahrnehmung des Teiles jedochvorgän-
gig ist. Der Prozess der subjektiven Konstruktion des Gesehenen basiert damit
37 Husserls Konzept der Appräsentation lässt sich generell mit der Unterscheidung zwischen
Perzeption und Apperzeption in den Kognitionswissenschaften analogisieren, auf den bereits
Leibniz (1996) und Wundt (2007 [1874]) hingewiesen haben: Wir erhalten immer einen Teilabschnitt
der ‚Gesamtinformation‘und versuchen den Rest kognitiv zu vervollständigen, d. h., es bleibt nicht
bei der Wahrnehmung als solche, sondern der bewussten Apperzeption. Die Gestalttheorie mit ihrer
Fokussierung auf die Phänomenologie (Metzger 1975, 22 betont explizit:„Gestaltpsychologie ist
Phänomenologie“) stellt eine ähnlich wertvolle Addition zu Husserls Überlegungen und der Ver-
knüpfung von Phänomenologie und Hermeneutik in unserem Ansatz dar: Wahrnehmung und
Deutung finden nicht willkürlich statt, sondern folgen bestimmtenMustern und wie wir dement-
sprechende Informationen kognitiv verarbeiten. Ziel ist eine Verknüpfung der Teile oder Strukturen
zu einer Ordnung bzw. Rekonstruktion/Extrapolation einer Gesamtfassung.
44 Roxana Kath, Gary S. Schaal, Sebastian Dumm

u. a. auf subjektiven, vorgängigen Erfahrungen und Kenntnissen, aber auch auf
kulturellen und gesellschaftlich vermittelten Codes.38
Die einschlägigen Befangenheiten und Vorurteile bei der Verarbeitung visuel-
ler Information werden in derDH-Literatur diskutiert. So analysiert Hundhausen
(2013, 116) „cognitive, social, and cultural perspectives“ bei der Evaluierung von
„Visualization Environments“. Wo liegt vor diesem Hintergrund der Mehrwert ihrer
epistemischen Adressierung in Form der (empirischen) Phänomenologie?
Grundlegend kann auf phänomenologischer Basis argumentiert werden, dass
„die Bild-Hermeneutik [… ] erst dann beginnen [kann; d. A.], wenn die Routinen
des alltagsweltlichen Bildverstehens außer Kraft gesetzt werden“ (Kurt 2008,
374). Dieses Zurücktreten hinter unsere alltäglichen Sehroutinen wird in der
Phänomenologie generell alsEpoché bezeichnet. Unterschiedliche Niveaus des
systematischen und theoretisch angeleiteten Zurücktretens werden„phenomeno-
logical reductions“ (Ihde 2012, 17) genannt. Don Ihde benennt hierfür drei„opera-
tional rules“:
1. „Attend to the phenomena of experience as they appear. [… ] Describe, don’t
explain“ (ebd., 18).
2. „Focus [… ] upon describable experience as it shows itself“ (ebd., 19).
3. „Horizontalize or equalize all immediate phenomena. [… ] Do not assume an
initial hierarchy of ,realities‘“(ebd., 19).
Es ist hier nicht der Ort, um auf die weiteren prozeduralen Schritte der empiri-
schen Phänomenologie von Ihde einzugehen, vielmehr soll direkt das Telos
seiner Perspektivierung in den Fokus gerückt werden. Aus der Vielzahl von
Konsequenzen, die aus dem Einnehmen einer phänomenologischen Perspektive
folgen, sollen im Folgenden einige exemplarisch herausgegriffen werden.
Die Phänomenologie legt es nahe, sich im Modus der mentalen Offenheit
einer Visualisierung zu nähern und damit das Neue zu sehen und nicht das
Bekannte (oder: Erwartete) wiederzuerkennen.
Der radikale Verzicht auf Erklärungen reduziert die Wahrscheinlichkeit,
Visualisierungen kausal überzustrapazieren. Kahneman (2012) argumentiert,
dass Menschen SinnsucherInnen sind und daher eher Struktur und Kausalität
erkennen als Zufall und Kontingenz. Dieses Phänomen wird bei der Interpreta-
tion von Visualisierungen besonders virulent. Schmidt (2012) greift dieses
Problem auf und weist darauf hin, dass Visualisierungen von Textkorpora, die
38 Dies gilt insbesondere für die naturwissenschaftlichen Disziplinen, wobei sich die Forscher-
Innen die von Fleck (1980) thematisierte„gerichtete Wahrnehmung“ auf für Laien unverständliche
Visualisierungen erwerben, die„unmittelbar wahrzunehmende Gestalt[en]“ hervorbringen.
New Visual Hermeneutics 45

die ForscherInnen nicht gut kennen, selten einen Plausibilitätscheck besitzen
und „interpretive leaps are extraordinarily easy to make with texts “. Der
bewusste Versuch, Deskription und Explanation systematisch zu trennen, redu-
ziert die Wahrscheinlichkeit von falschen„interpretive leaps“.
Auch der aktive Versuch,Appräsentationen zu vermeiden, führt dazu, nicht
das Bekannte wiederzuerkennen, sondern das Neue zu sehen.
Besonders relevant für die neue visuelle Hermeneutik ist Ihdes (2012, 48)
Konzept der „multistabilities“ oder „multistable configurations“. Um seine Be-
deutung richtig einschätzen zu können, ist es notwendig, sich zu vergegen-
wärtigen, dass eine positivistische Wissenschaftslogik die Tendenz besitzt, nach
Eineindeutigkeiten (Erklärungen, Beschreibungen) zu suchen. Auch Ihde (1998)
kann experimentell zeigen, dass ohne phänomenologische Anleitung dominant
nach der einen, richtigen Interpretation einer Visualisierung gesucht wird.
Husserl (1985, 421) argumentiert jedoch:„Die Wirklichkeiten müssen behandelt
werden als Möglichkeiten unter anderen Möglichkeiten.“ Ihde (2012, 50) spricht
davon, dass eine„phenomenological attitude“ existiert, die sich durch„poly-
morphic-mindedness“ auszeichnet, die „deliberately seeks a particular kind of
richness within phenomena“. Adressiert ist damit das Phänomen, dass ein und
dieselbe Visualisierung mehrere Wahrnehmungen (in der korrespondierenden
Terminologie: ‚noema‘) gleichzeitig besitzen kann, zwischen denen der Wahr-
nehmende intentional wechseln kann. Diese Gleichzeitigkeit wird von Ihde folg-
lich als „multistable configurations“ bezeichnet. Den epistemischen Blick für
diese Möglichkeit von Polylatenz zu öffnen, ist ein Ziel der Phänomenologie–
und der Kern der Aussage des sehr kurzen Zitates von Husserl weiter oben.39
Doch wie kann die Polylatenz, die„multistable configuration“, an andere
kommuniziert werden, die diese Aussagen in einer Visualisierung noch nicht
erkannt haben? Ihde (ebd., 61) identifiziert hierfür zwei Strategien: diehermeneu-
tische und die transzendente Strategie. Die hermeneutische Strategie basiert
darauf, dass „story devices” and „naming” zum Erzählen von Geschichten und
Einbetten der Visualisierung in (narrativ) bekannte Kontexte genutzt werden, so
dass sich ihre Bedeutung aus der Erzählung ergibt. Die transzendente Strategie
fokussiert hingegen auf den Prozess der individuellen Wahrnehmung. Hier
könnte zum Beispiel eine Anleitung gegeben werden, wie der Blick auf einer
Visualisierung zu wandern hat, in welcher Reihenfolge der Blick welche Objekte
in den Fokus nehmen soll etc. Beide Strategien besitzen inhärente Vor- und
39 Oder, in den Worten von Kurt (2008, 375):„Je zahlreicher und gegensätzlicher die Seharten,
desto besser für den Interpretationsprozess, denn auf diese Weise werden Hypothesen entwi-
ckelt, die in späteren Phasen der Auslegung überprüft werden können.“
46 Roxana Kath, Gary S. Schaal, Sebastian Dumm

Nachteile, die sich– da sie in denDH zur Anwendung kommen– mit großem
Gewinn auf Basis der experimentellen Phänomenologie diskutieren lassen.
Wir sind nun in der Lage, eine genauere Antwort auf die Frage zu liefern,
warum eine epistemische Fundierung in der Hermeneutik und der Phänomeno-
logie für die Phase 4 der neuen visuellen Hermeneutik angemessen ist: Die
phänomenologische Fundierung überwindet die„passivity of ordinary viewing
[… ] [leading to; d. A.] a growing sense of control over what is seen. In the
process, a new type of familiarity is constructed, the familiarity of polymorphy“
(ebd., 76).40 Die experimentelle Phänomenologie dient als ein „interpretive
framework[… ] that enable[s] different image readings“ (Rosenberger 2011, 7).
Gewinnbringend ist der phänomenologische Ansatz jedoch auch mit Blick auf
die vorherigen Phasen der neuen visuellen Hermeneutik. Die Überlegung lautet,
dass die Frage, welche Visualisierung gewählt wird, ähnlichen Phänomenen der
systematischen Verzerrung unterliegt, wie die nicht phänomenologisch inspirierte
Interpretation von Grafiken. Wenn, wie gezeigt wurde, das Wiedererkennen und
die Suche nach Kausalität wiederkehrende Motive bei der Interpretation von
Visualisierungen sind, so steht zu erwarten, dass diese Motive auch prospektiv die
Wahl der Visualisierung anleiten können. Dieser Zusammenhang ist bislang noch
nicht empirisch analysiert worden, aber die empirische Phänomenologie von Ihde
liefert die theoretischen und die konzeptionellen Grundlagen einer solchen Studie.
Für die Phasen des Datensamplings und der algorithmenbasierten Analyse lassen
sich ähnliche Überlegungen anstellen, welche die Vorteile einerneuen visuellen
Hermeneutik und deren Sensibilität für den Prozess des Geworden-Seins, ver-
anschaulichen. Diese tentative Überlegung verdeutlicht zudem, dass eine episte-
mische Fundierung derDH eine holistische und innovativere Forschungsperspek-
tive ermöglicht als eine auf die einzelnen Phasen fokussierte Methodik.
4 Schluss
Der Beitrag entwickelte die Grundzüge einerneuen visuellen Hermeneutik als
Forschungsansatz, der den besonderen epistemischen Herausforderungen der
DH und damit auch den Herausforderungen, denen sich eine sozial- und kultur-
40 Vgl. auch die Arbeiten von Rosenberger (2011) für empirische Anwendungen von Ihde auf
komplexe Probleme der Interpretation von Visualisierungen. Die Beispiele von Rosenberger
unterscheiden sich jedoch von den Visualisierungen, an die im Rahmen dieses Beitrages gedacht
wird, weil Rosenberger keine Visualisierungen von Daten analysiert, sondern polymorphe
Deutungen von‚realen‘Bildern wie Aufnahmen von Mikroskopen etc.
New Visual Hermeneutics 47

analytisch interessierte Korpuslinguistik gegenüber sieht, Rechnung trägt. Es
konnte gezeigt werden, dass das Erkenntnispotential derDH und damit ver-
bunden ihre Akzeptanz sich durch eine eigene epistemische und methodische
Fundierung signifikant verbessert. Dieneue visuelle Hermeneutik nimmt eine
holistische Perspektive auf die vier Phasen des Forschungsprozesses ein und
verdeutlicht, wie interdependent die sonst distinkt betrachteten Phasen des
Forschungsprozesses sind. Dies impliziert, dass die epistemische Qualität der
Arbeit in denDH und damit auch in der Korpuslinguistik zentral davon abhängt,
dass die ForscherInnen die methodischen, theoretischen und epistemischen
Implikationen in allen Phasen des Forschungsprozesses kennen.
Literatur
Baroni, Marco/Evert, Stefan (2008): Statistical methods for corpus exploitation. In: Anke Lüdeling/
Merja Kytö (Hg.): Corpus Linguistics. An International Handbook. Berlin: de Gruyter, 777–803.
Baßler, Moritz (1995): Einleitung. In: Moritz Baßler (Hg.): New Historicism. Literaturgeschichte
als Poetik der Kultur. Frankfurt am Main: Fischer, 7–28.
Becker, Matthias (2012): Der Algorithmus, bei dem man mit muss? Über die Kehrseite der digitalen
Automatisierung, Feature. Deutschlandfunk 2. März 2012, (http://www.deutschlandfunk.de/
der-algorithmus-bei-dem-man-mit-muss.1170.de.html?dram:article_id=184103).
Berry, David M. (2011): The Computational Turn: Thinking about the Digital Humanities. In: www.
culturemachine.net 12, 1–22, 14.05.2013.
Berry, David M. (2012): Introduction: Understanding the Digital Humanities. In: David M. Berry
(Hg.): Understanding Digital Humanities. London: Palgrave Macmillan.
Bollier, David (2010): The promise and peril of big data. In: http://www.aspeninstitute.org/sites/
default/files/content/docs/pubs/1he_Promise_and_Peril_of_Big_Data.pdf, 16.4.2014
Boyd, Danah/Crawford, Kate (2013): Big Data als kulturelles, technologisches und wissenschaft-
liches Phänomen. Sechs Provokationen. In: Heinrich Geiselberger/Tobias Moorstedt (Hg.):
Big Data. Das neue Versprechen der Allwissenheit. Berlin: Suhrkamp, 187–218.
Burkhard, Remo (2006): Knowledge Visualization: Die nächste Herausforderung für Semantic
Web Forschende? In: Tassilo Pellegrini/Andreas Blumauer (Hg.): Semantic Web. Berlin,
Heidelberg: Springer, 201–212.
Campbell, Donald T./Fiske, Donald W. (1959): Convergent and discriminant validation by the
multitrait-multimethod matrix. In: Psychological Bulletin 56, 81–105. DOI: 10.1037/h0046016.
Card, Stuart K./Mackinlay Jock D./Shneiderman, Ben (1999): Readings in Information Visualiza-
tion: Using Vision to Think. San Francisco: Morgan Kaufmann Publishers.
Cecire, Natalia (2011a): Introduction: Theory and the Virtues of Digital Humanities. In: Journal of
Digital Humanities 1, 45–53.
Cecire, Natalia (2011b): When Digital Humanities was in Vogue. In: Journal of Digital Humanities 1,
54–59.
Crease, R. P. (1993): The play of nature: Experimentation as performance. Bloomington: Indiana
University Press.
Dilthey, Wilhelm (1957): Die geistige Welt. Einleitung in die Philosophie des Lebens. Gesammelte
Schriften V. Band. Stuttgart: Teubner.
48 Roxana Kath, Gary S. Schaal, Sebastian Dumm

Dilthey, Wilhelm (1958): Der Aufbau der geschichtlichen Welt in den Geisteswissenschaften.
Gesammelte Schriften Band VII. Stuttgart: Teubner.
Drucker, Johanna (2012): Humanistic Theory and Digital Scholarship. In: Matthew K. Gold (Hg.):
Debates in the Digital Humanities. Minneapolis, London: University of Minnesota Press.
Drucker, Johanna (2011): Humanities Approaches to Graphical Display. In: Digital Humanities
Quaterly 5, http://digitalhumanities.org/dhq/vol/5/1/000091/000091.html, 17.04.2014.
Endert, Alex/Hossain, M. Shahriar/Ramakrishnan, Naren/North, Chris/Fiaux, Patrick/Andrews,
Christopher (2014): The human is the loop: new directions for visual analytics. In: Journal of
Intelligent Information Systems 42, 1–25.
Engström, T./Selinger, E. (Hg.): Rethinking theories and practices of imaging. State College:
Penn State University Press, i. E.
Fleck, Ludwik (1980): Entstehung und Entwicklung einer wissenschaftlichen Tatsache. Frankfurt
am Main: Suhrkamp.
Goethe, Johann-Wolfgang von (1948): Brief an F. v. Müller vom 24.4.1819. In: Gedenkausgabe der
Werke, Briefe und Gespräche, Bd. 23, Zürich: Artemis-Verlag, 52.
Gorunescu, Florin (2011): Data Mining. Concepts, Models and Techniques. Berlin, Heidelberg:
Springer.
Gotz, D., Zhou, M. (2008): Characterizing users’ visual analytic activity for insight provenance.
In: Proceedings of IEEE Symposium on Visual Analytics Science and Technology, 123–130
Greenblatt, Stephen (1993): Einleitung. Die Zirkulation sozialer Energie. In: Stephen Greenblatt:
Verhandlungen mit Shakespeare. Innenansichten der englischen Renaissance. Frankfurt
am Main: Fischer, 9–33.
Haber, Peter (2011): Digital Past. Geschichtswissenschaften im digitalen Zeitalter. München:
Oldenbourg Wissenschaftsverlag.
Hasse, Cathrine (2008): Postphenomenology: Learning cultural perception in science. In: Human
Studies 31, 43–61.
Heelan, Patrick (1983): Space perception and the philosophy of science. Berkeley: University of
California Press.
Heer, Jeffrey/Shneiderman, Ben (2012): Interactive dynamics for visual analysis. In: Queue 10, 30.
Hepp, Andreas (2011): Medienkultur. Die Kultur mediatisierter Welten. Wiesbaden: VS Verlag.
Heyer, Gerhard/Quasthoff, Uwe/Wittig, Thomas (2006): Text Mining: Wissensrohstoff Text–
Konzepte, Algorithmen, Ergebnisse. Bochum: w3l-Verlag.
Husserl, Edmund (1973): Cartesianische Meditationen und Pariser Vorträge, hg. v. S. Strasser,
Husserliana Band 1. Den Haag: Martinus Nijhoff.
Husserl, Edmund (1976): Die Krisis der europäischen Wissenschaften und die transzendentale
Phäno-menologie. Eine Einleitung in die phänomenologische Philosophie, hg. v. W. Biemel,
Husserliana Bd. 6. Den Haag: Martinus Nijhoff.
Husserl, Edmund (1980): Phantasie, Bildbewusstsein, Erinnerung. Zur Phänomenologie der
anschaulichen Vergegenwärtigungen. Husserliana Bd. 23. Den Haag, Boston, London:
Martin Nijhoff.
Husserl, Edmund (1985): Erfahrung und Urteil. Untersuchungen zur Genealogie der Logik,
redigiert und hg. v. L. Landgrebe. Hamburg: Felix Meiner Verlag.
Husserl, Edmund (1993): Aufsätze und Vorträge (1922–1937), Husserliana Bd. 27. Dordrecht,
Boston, London: Kluwer Academic Publishers.
Ihde, Don (1998): Expanding Hermeneutics. Visualism in Science. Evanston (IL.): Northwestern
University Press.
Ihde, Don (2012): Experimental Phenomenology. Multistables. New York: Sunny Press.
New Visual Hermeneutics 49

Kahneman, Daniel (2012): Schnelles Denken, langsames Denken. München: Siedler.
Kath, Roxana (2011): Das Mental Maps-Interface: Erforschung von Konzepten in Raum und Zeit.
In: Charlotte Schubert (Hg.): Neue Methoden der geisteswissenschaftlichen Forschung. Eine
Einführung in das Portal eAQUA II (Working Papers Contested Order No. 3). Leipzig, 64–86.
Kath, Roxana (2014): Aesthetics are (ir)relevant: Für eine Neue Visuelle Hermeneutik in den
Geisteswissenschaften. In: Zeitschrift für Politische Theorie 5, 97–120.
Keim, Daniel/Kohlhammer, Jörn/Ellis, Geoffrey/Mansmann, Florian (Hg.) (2010): Mastering the
information age. Solving problems with visual analytics. In: http://www.diglib.eg.org,
14.05.2014.
Koplenig, Alexander (2014): Prinzipielle Probleme der Anwendung statistischer Signifikanztests
in der Korpuslinguistik. Vortrag, gehalten auf der 1. Jahrestagung der Digital Humanities im
deutschsprachigen Raum (DHd 2014). In: https://www.conftool.pro/dhd2014/index.php?
page=browseSessions&path=adminSessions&form_session=1, 09.05.2014.
Kurt, Ronald (2008): Vom Sinn des Sehens: Phänomenologie und Hermeneutik als Methoden
visueller Erkenntnis. In: Jochen Dreher/Michaela Padenhauer(Hg.): Phänomenologie und
Soziologie. Wiesbaden: VS Verlag für Sozialwissenschaften, 369–378.
Landesberger, Tatiane von/Fiebig, Sebastian/Bremm, Sebastian/Kuijper, Arjan/Fellner, Dieter
W. (2014): Interaction Taxonomy for Tracking of User Actions in Visual Analytics Applica-
tions. In: Weidong Huang (Hg.): Handbook of Human Centric Visualization. New York:
Springer, 653–670.
Lauer, Gerhard (2013): Die digitale Vermessung der Kultur. Geisteswissenschaften als Digital
Humanities. In: Heinrich Geiselberger/Tobias Moorstedt (Hg.): Big Data. Das neue Verspre-
chen der Allwissenheit. Suhrkamp: Berlin, 99–116.
Leibniz, Gottfried Wilhelm (1996): Neue Abhandlungen über den menschlichen Verstand. Ham-
burg: Felix Meiner Verlag.
Liu, Qing/Vorvoreanu, Mihaela/Madhavan, Krishna P. C./McKenna, Ann F. (2013): Designing
Discovery Experience for Big Data Interaction: A Case of Web-Based Knowledge Mining and
Interactive Visualization Platform. In: Design, User Experience, and Usability. Web, Mobile,
and Product Design. Berlin, Heidelberg: Springer, 543–552.
Lückerath, Carl August (1968): Prolegomena zur elektronischen Datenverarbeitung im Bereich
der Geschichtswissenschaft. In: Historische Zeitschrift 207, 265–296.
Mehler, Alexander (2004): Textmining. In: Henning Lobin (Hg): Texttechnologie. Perspektiven
und Anwendungen. Tübingen: Stauffenburg, 329–352.
Metzger, Wolfgang (1975): Gesetze des Sehens. Frankfurt am Main: Kramer.
Moisl, Hermann L. (2013): Statistical Corpus Exploitation. Oxford Handbooks online. In: http://
www.oxfordhandbooks.com/view/10.1093/oxfordhb/9780199571932.001.0001/oxfordhb-
9780199571932-e-013, 09.04.2014.
Montrose, Louis (1995): Die Renaissance behaupten. Die Poetik und Politik der Kultur. In: Moritz
Baßler (Hg.): New Historicism. Literaturgeschichte als Poetik der Kultur. Frankfurt am Main:
Fischer, 60–93.
Moretti, Franco (2009): Kurven, Karten, Stammbäume. Abstrakte Modelle für die Literatur-
geschichte. Frankfurt am Main: Suhrkamp.
Moretti, Franco (2013): Distant Reading. London, New York: Verso.
Noller, Stefan (2012): Plädoyer für eine Algorithmen-Ethik. Relevanz ist alles. In: Frankfurter
Allgemeine Zeitung vom 24.10.2012, http://www.faz.net/aktuell/feuilleton/debatten/plae-
doyer-fuer-eine-algorithmen-ethik-relevanz-ist-alles-11934495.html, 14.04.2014
50 Roxana Kath, Gary S. Schaal, Sebastian Dumm

Pirolli, Peter/Card, Stuart (2005): The sensemaking process and leverage points for analyst
technology as identified through cognitive task analysis. In: ICIA’05.
Ramsay, Stephen/Rockwell, George (2012): Developing Things: Notes toward an Epistemology of
Building in the Digital Humanities. In: Matthew K. Gold (Hg.): Debates in Digital Humanities.
Minneapolis: University of Minnesota Press, 75–84.
Rehbein, Malte/Schubert, Charlotte (2013): Sind die Digital Humanities eine eigene Disziplin? In:
duzMagazin12, 13.
Rensink, Ronald A. (2014): On the Prospects for a Science of Visualization. In: Weidong Huang
(Hg.): Handbook of Human Centric Visualization. New York: Springer, 147–178.
Rieder, Bernhard/Röhle, Theo (2012): Digital Methods, Five Challenges. In: David M. Berry (Hg.):
Understanding Digital Humanities. London: Palgrave Macmillan, 67–84.
Rosenberger, Robert (2009): Quick-freezing philosophy: An analysis of imaging technologies in
neurobiology. In: Jan-Kyrre Berg Olsen/Evan Selinger/Søren Riis (Hg.): New waves in phi-
losophy of technology. New York: Palgrave Macmillan, 65–82.
Rosenberger, Robert (2011): A Case Study in the Applied Philosophy of Imaging: The Synaptic
Vesicle Debate. In: Science, Technology & Human Values 36, 6–32.
Schmidt, Benjamin (2012): When You Have a Mallet, Everything Looks like a Nail. In: http://sap-
pingattention.blogspot.de/2012/11/when-you-have-mallet-everything-looks.html, 12.01.2014.
Schnapp, Jeffrey/Presner, Todd/Lunenfeld, Peter et al. (2009): Digital Humanities Manifesto 2.0.
In: http://www.humanitiesblast.com/manifesto/Manifesto_V2.pdf, 31.05.2013.
Schreibman, Susan/Siemen, Ray/Unsworth, John (2004): The Digital Humanities and Humanities
Computing: An Introduction. In: Dies. (Hg.): A Companion to Digital Humanities. Oxford. In:
http://www.digitalhumanities.org/companion/, 14.05.2013.
Schubert, Charlotte (2013): Zauberlehrling und Meister: Digital Humanities zwischen Informatik und
Geisteswissenschaften? In: Jörn Kobes/Kai Ruffing/Wolfgang Spickermann (Hg.): 20 Jahre
Arbeitsgemeinschaft Geschichte und EDV. Gutenberg: Computus Druck Satz & Verlag, 167–186.
Seifert, Christin/Sabol, Vedran/Kienreich, Wolfgang/Lex, Eisabeth/Granitzer, Michael (2014):
Visual Analysis and Knowledge Discovery for Text. In: Aris Gkoulalas-Divanis/Abderrahim
Labbi (Hg.): Large-Scale Data Analytics. New York: Springer, 189–218.
Sullivan, Danny (2010): When OCR Goes Bad: Google’s Ngram Viewer & The F-Word. In:
http://searchengineland.com/when-ocr-goes-bad-googles-ngram-viewer-the-f-word-59181,
14.04.2012.
Takahashi, Jade (2012): Is Theory the Doing? In: http://dh201.humanities.ucla.edu/?p=398,
14.5.2012.
Tversky, Barbara 2014: Visualizing Thought. In: Weidong Huang (Hg.): Handbook of Human
Centric Visualization. New York: Springer, 3–40.
Verbeek, Peter-Paul (2007): Beyond the human eye: Technological mediation and posthuman
visions. In: Petran Kockelkoren (Hg.): Mediated vision. Rotterdam: Veenman Publishers and
ArtEZ Press, 43–53.
Ware, Colin (2000): Information visualization: Perception for Design. San Francisco: Morgan
Kaufmann.
Wirth, Werner/Matthes, Jörg (2008): Zur Quantifizierung von Konstruktvalidität: Problemaufriss
und Entwicklung eines Validitätsindex. In: Jörg Matthes/Werner Wirth/Gregor Daschmann/
Andreas Fahr (Hg.): Die Brücke zwischen Theorie und Empirie. Operationalisierung, Mes-
sung und Validierung in der Kommunikationswissenschaft. Köln: von Halem, 14–27.
Wundt, Wilhelm (2007 [1874]): Grundzüge der physiologischen Psychologie. Saarbrücken:
VDM Verlag.
New Visual Hermeneutics 51
```
