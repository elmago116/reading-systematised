---
title: The Semantic Web 21st International Conference, ESWC 2024
author: ""
year: "2024"
Type: Article
DOI: ""
source: ""
created: 2026-04-24
description: ""
tags:
  - op/acc/pending-review
  - Tech/SemanticWeb/KG/ontology
  - Humanities/culturalHeritage
pdfORepub: "[[The Semantic Web 21st International Conference, ESWC 2024.pdf]]"
---
![[The Semantic Web 21st International Conference, ESWC 2024.pdf]]
## Full text (extracted from `The Semantic Web 21st International Conference, ESWC 2024.pdf`)

*Source:* `2PDF/The Semantic Web 21st International Conference, ESWC 2024.pdf`  
*Extracted:* 2026-04-24

```text
Albert Meroño Peñuela · Anastasia Dimou · 
Raphaël Troncy · Olaf Hartig · 
Maribel Acosta · Mehwish Alam · 
Heiko Paulheim · Pasquale Lisena 
(Eds.)
LNCS 14665 The Semantic Web
21st International Conference, ESWC 2024
Hersonissos, Crete, Greece, May 26–30, 2024
Proceedings, Part II


Lecture Notes in Computer Science 14665
Founding Editors
Gerhard Goos
Juris Hartmanis
Editorial Board Members
Elisa Bertino, Purdue University, West Lafayette, IN, USA
Wen Gao, Peking University, Beijing, China
Bernhard Steffen , TU Dortmund University, Dortmund, Germany
Moti Y ung , Columbia University, New York, NY, USA

The series Lecture Notes in Computer Science (LNCS), including its subseries Lecture
Notes in Artiﬁcial Intelligence (LNAI) and Lecture Notes in Bioinformatics (LNBI),
has established itself as a medium for the publication of new developments in computer
science and information technology research, teaching, and education.
LNCS enjoys close cooperation with the computer science R & D community, the
series counts many renowned academics among its volume editors and paper authors, and
collaborates with prestigious societies. Its mission is to serve this international commu-
nity by providing an invaluable service, mainly focused on the publication of conference
and workshop proceedings and postproceedings. LNCS commenced publication in 1973.

Albert Meroño Peñuela · Anastasia Dimou ·
Raphaël Troncy · Olaf Hartig · Maribel Acosta ·
Mehwish Alam · Heiko Paulheim ·
Pasquale Lisena
Editors
The Semantic Web
21st International Conference, ESWC 2024
Hersonissos, Crete, Greece, May 26–30, 2024
Proceedings, Part II

Editors
Albert Meroño Peñuela
King’s College London
London, UK
Raphaël Troncy
EURECOM
Biot, France
Maribel Acosta
Technical University of Munich
Heilbronn, Germany
Heiko Paulheim
University of Mannheim
Mannheim, Germany
Anastasia Dimou
KU Leuven
Sint-Katelijne-Waver, Belgium
Olaf Hartig
Linköping University
Linköping, Sweden
Mehwish Alam
Polytechnic Institute of Paris
Palaiseau, France
Pasquale Lisena
EURECOM
Biot, France
ISSN 0302-9743 ISSN 1611-3349 (electronic)
Lecture Notes in Computer Science
ISBN 978-3-031-60634-2 ISBN 978-3-031-60635-9 (eBook)
https://doi.org/10.1007/978-3-031-60635-9
© The Editor(s) (if applicable) and The Author(s), under exclusive license
to Springer Nature Switzerland AG 2024
This work is subject to copyright. All rights are solely and exclusively licensed by the Publisher, whether
the whole or part of the material is concerned, speciﬁcally the rights of translation, reprinting, reuse of
illustrations, recitation, broadcasting, reproduction on microﬁlms or in any other physical way, and transmission
or information storage and retrieval, electronic adaptation, computer software, or by similar or dissimilar
methodology now known or hereafter developed.
The use of general descriptive names, registered names, trademarks, service marks, etc. in this publication
does not imply, even in the absence of a speciﬁc statement, that such names are exempt from the relevant
protective laws and regulations and therefore free for general use.
The publisher, the authors and the editors are safe to assume that the advice and information in this book
are believed to be true and accurate at the date of publication. Neither the publisher nor the authors or the
editors give a warranty, expressed or implied, with respect to the material contained herein or for any errors
or omissions that may have been made. The publisher remains neutral with regard to jurisdictional claims in
published maps and institutional afﬁliations.
This Springer imprint is published by the registered company Springer Nature Switzerland AG
The registered company address is: Gewerbestrasse 11, 6330 Cham, Switzerland
If disposing of this product, please recycle the paper.

Preface
This volume contains the main proceedings of the 21st edition of the European Semantic
Web Conference (ESWC 2024). ESWC is a major venue for discussing the latest in
scientiﬁc results and innovations related to the semantic web, knowledge graphs, and
web data. This year we aimed at acknowledging recent developments in AI with a special
tagline, “Fabrics of Knowledge: Knowledge Graphs and Generative AI”. By doing so,
and adapting the program as described below, we intended to open up the conference to
fundamental questions about how we acquire, represent, use, and interact with knowledge
in the advent of Generative AI and large language models.
This year ESWC’s Research track addressed the theoretical, analytical, and empirical
aspects of the Semantic Web, semantic technologies, knowledge graphs and semantics
on the Web in general. The In-use track focused on contributions that reuse and apply
state-of-the-art semantic technologies or resources to real-world settings. The Resource
track welcomed resource contributions that are on the one hand innovative or novel and
on the other hand sharable and reusable (e.g. datasets, knowledge graphs, ontologies,
workﬂows, benchmarks, frameworks), and provide the necessary scaffolding to support
the generation of scientiﬁc work and advance the state of the art.
The main scientiﬁc program of ESWC 2024 contained 32 papers selected out of
138 submissions (62 research, 19 in-use, 57 resource): 13 papers in the Research track,
5 in the In-Use track, and 14 in the Resource track. The overall acceptance rate was
23% (20% research, 26% in-use, 24% resource). Due to last year’s success in innovating
with the ESWC review process, this year we kept the approach of not including a ﬁnal
overall score before the rebuttal phase in the Research and Resource tracks. This enabled
reviewers to focus on their reviews rather than scores, and on asking speciﬁc questions
and to use the answers provided by authors in the rebuttal in their ﬁnal assessment. The
program chairs are grateful to the 40 senior PC members, the 240 PC members, and
the 25 external reviewers for providing their feedback on the scientiﬁc program, and to
all other community members who contributed in reviewing. Each paper received an
average of 3.6 reviews, with both the Research and Resources being dual anonymous,
and In-Use being single anonymous. We adopted ACM’s terminology in all calls to
improve ESWC’s Diversity, Equity, and Inclusion principles in how we communicated
review guidelines.
1
We welcomed invited keynotes from three world renowned speakers, spanning indus-
try and academia and in keeping with our theme of building understanding between the
knowledge graph and generative AI communities: Elena Simperl (King’s College Lon-
don & Open Data Institute), Peter Clark (Allen Institute for Artiﬁcial Intelligence, AI2),
and Katariina Kari (IKEA Systems B.V .).
As part of the conference’s special topic, ESWC 2024 featured a Special Track on
Large Language Models for Knowledge Engineering, providing a venue for scientiﬁc
discussion and community building for early work on this exciting new area of research.
1 See “Words Matter” https://www.acm.org/diversity-inclusion/words-matter.

vi Preface
The track had 52 submissions, demonstrating the importance of research in this direction.
The number of selected papers for presentation and publication for this track is reported
in the Satellite V olume.
ESWC 2024 also had a record-breaking number of workshop and tutorial proposals,
of which 16 workshops and 2 tutorials were accepted. Their large variety of topics
included data management, natural language processing, sustainability, and generative
neuro-symbolic AI, aligning with this year’s conference topic.
The conference also offered other opportunities to discuss the latest research and
innovation work, including a poster and demo session, workshops and tutorials, a PhD
symposium, an EU project networking session, and an industry track. We thank Joe
Raad and Bruno Sartini for organising the Workshop and Tutorials track, which hosted
16 workshops and 2 tutorials covering topics ranging from knowledge graph construc-
tion to deep learning with knowledge graphs. We are also thankful to María Poveda-
Villalón and Andrea Nuzzolese for successfully running the Posters and Demos track.
We are grateful to Marta Sabou and V alentina Presutti for coordinating a very special
PhD Symposium aiming at bridging the ESWC PhD and the International Semantic
Web Summer School (ISWS) alumni, which welcomed 14 PhD students who had the
opportunity to present their work and receive feedback in a constructive environment.
Thanks go to Irene Celino and Artem Revenko for their management of the Industry
Track which welcomed submissions from several large industry players. We also thank
Cassia Trojahn and Sabrina Kirrane for increasing the networking potential of ESWC
by running the Project Networking Session. A special thanks to Tabea Tietz and Stefano
De Giorgis for their amazing job as Web and Publicity chairs, and to Pasquale Lisena
for preparing this volume with Springer and the conference metadata. We thank STI
International for supporting the conference organization, and in particular Umut Serles
and Juliette Opdenplatz for their invaluable support. We thank our sponsors for support-
ing ESWC 2024 and also our sponsorship chairs Nitisha Jain and Jan-Christoph Kalo
for securing them. Finally, we are also grateful to Dieter Fensel, John Domingue, Elena
Simperl, Paul Groth, Catia Pesquita and the ESWC 2023 organising committee for their
invaluable support and advice.
As we reﬂect on both the past and the future, and our role as researchers and
technologists, our thoughts go out to all those impacted by war around the world.
April 2024 Albert Meroño Peñuela
Anastasia Dimou
Raphaël Troncy
Olaf Hartig
Maribel Acosta
Mehwish Alam
Heiko Paulheim
Pasquale Lisena

Organization
General Chair
Albert Meroño Peñuela King’s College London, UK
Research Track Program Chairs
Anastasia Dimou KU Leuven, Belgium
Raphaël Troncy EURECOM, France
Resource Track Program Chairs
Mehwish Alam Télécom Paris, Institut Polytechnique de Paris,
France
Heiko Paulheim University of Mannheim, Germany
In-Use Track Program Chairs
Olaf Hartig Linköpings Universitet, Sweden
Maribel Acosta Ruhr University Bochum, Germany
Special Track on Large Language Models for Knowledge
Engineering
Oscar Corcho Universidad Politécnica de Madrid, Spain
Paul Groth University of Amsterdam, Netherlands
Elena Simperl King’s College London, UK
V alentina Tamma University of Liverpool, UK
Workshops and Tutorials Chairs
Joe Raad University of Paris-Saclay, France
Bruno Sartini Ludwig-Maximilians University of Munich,
Germany

viii Organization
Poster and Demo Chairs
Andrea Nuzzolese ISTC-CNR, Italy
María Poveda-Villalón Universidad Politécnica de Madrid, Spain
PhD Symposium Chairs
Marta Sabou Vienna University of Economics and Business,
Austria
V alentina Presutti University of Bologna, Italy
Industry Track Program Chairs
Irene Celino Cefriel, Italy
Artem Revenko Semantic Web Company GmbH, Austria
Sponsorship
Nitisha Jain King’s College London, UK
Jan-Christoph Kalo University of Amsterdam, Netherlands
Project Networking
Cassia Trojahn IRIT, France
Sabrina Kirrane WU Vienna, Austria
Web and Publicity
Stefano De Giorgis University of Bologna, Italy
Tabea Tietz FIZ Karlsruhe, Germany
Proceedings and Conference Metadata
Pasquale Lisena EURECOM, France

Organization ix
Program Committee
Nora Abdelmageed Friedrich-Schiller-Universität Jena, Germany
Ghadeer Abuoda Aalborg University, Denmark
Maribel Acosta TU Munich, Germany
Shqiponja Ahmetaj TU Wien, Austria
Aljbin Ahmeti Semantic Web Company GmbH and TU Wien,
Austria
Mehwish Alam Télécom Paris, France
Céline Alec Université de Caen-Normandie, France
Vladimir Alexiev Ontotext Corp., Bulgaria
Panos Alexopoulos Textkernel B.V ., Netherlands
Alsayed Algergawy University of Jena, Germany
Reham Alharbi University of Liverpool, UK
Bradley Allen University of Amsterdam, Netherlands
Doerthe Arndt TU Dresden, Germany
Natanael Arndt eccenca GmbH, Germany
Luigi Asprino University of Bologna, Italy
Ghislain Auguste Atemezing ERA, France
Maurizio Atzori University of Cagliari, Italy
Sören Auer TIB Leibniz Information Center Science,
Germany & Technology and University of
Hannover, Germany
Carlos Badenes-Olmedo Universidad Politécnica de Madrid, Spain
Booma Sowkarthiga
Balasubramani
University of Illinois at Chicago, USA
Konstantina Bereta National and Kapodistrian University of Athens,
Greece
Abraham Bernstein University of Zurich, Switzerland
Russa Biswas Hasso Plattner Institute, Germany
Christian Bizer University of Mannheim, Germany
Peter Bloem Vrije Universiteit Amsterdam, Netherlands
Martin Blum University of Trier, Germany
Carlos Bobed University of Zaragoza, Spain
Fernando Bobillo University of Zaragoza, Spain
Pieter Bonte Ghent University, Belgium
Andreas Both DA TEV eG, Germany
Alexandros Bousdekis Institute of Communication and Computer
Systems-National Technical University of
Athens, Greece
Loris Bozzato Fondazione Bruno Kessler, Italy
Janez Brank Jozef Stefan Institute, Slovenia

x Organization
Adrian M. P . Brasoveanu MODUL Technology GmbH, Austria
Olivier Bruneau University of Lorraine, France
Carlos Buil Aranda Universidad Técnica Federico Santa María, Chile
Maxime Buron Inria, France
Davide Buscaldi Université Sorbonne-Paris-Nord, France
Jean-Paul Calbimonte University of Applied Sciences and Arts Western
Switzerland, Switzerland
Pablo Calleja Universidad Politécnica de Madrid, Spain
Antonella Carbonaro University of Bologna, Italy
V alentina Anita Carriero Cefriel, Italy
Sylvie Cazalens LIRIS - INSA de Lyon, France
Irene Celino Cefriel, Italy
Renato Cerqueira IBM Research - Brazil, Brazil
Y oan Chabot Orange Labs, France
Javad Chamanara Technische Informationsbibliothek, Germany
Pierre-Antoine Champin LIRIS, Université Claude Bernard Lyon 1, France
David Chaves-Fraga Universidade de Santiago de Compostela, Spain
Lihu Chen Inria Saclay, France
Gong Cheng Nanjing University, China
Philipp Cimiano Bielefeld University, Germany
Andrea Cimmino Arriaga Universidad Politécnica de Madrid, Spain
Michael Cochez Vrije Universiteit Amsterdam, Netherlands
Diego Collarana Fraunhofer IAIS, Germany
Pieter Colpaert Ghent University, Belgium
Oscar Corcho Universidad Politécnica de Madrid, Spain
Francesco Corcoglioniti Free University of Bozen-Bolzano, Italy
Julien Corman Free University of Bozen-Bolzano, Italy
Marco Cremaschi University of Milano-Bicocca, Italy
Claudia d’Amato University of Bari, Italy
Mathieu D’Aquin LORIA, University of Lorraine, France
Jennifer D’Souza TIB Leibniz Information Centre for Science and
Technology University Library, Germany
Enrico Daga The Open University, UK
Jérôme David Inria, France
Jacopo de Berardinis King’s College London, UK
Victor de Boer Vrije Universiteit Amsterdam, Netherlands
Stefano de Giorgis University of Bologna, Italy
Ben De Meester Ghent University, Belgium
Daniele Dell’Aglio Aalborg University, Denmark
Gianluca Demartini The University of Queensland, Australia
Elena Demidova University of Bonn, Germany
Kathrin Dentler Triply, Netherlands

Organization xi
Danilo Dessì GESIS – Leibniz Institute for the Social Sciences,
Germany
Gayo Diallo University of Bordeaux, France
Stefan Dietze GESIS – Leibniz Institute for the Social Sciences,
Germany
Dimitar Dimitrov GESIS – Leibniz Institute for the Social Sciences,
Germany
Anastasia Dimou KU Leuven, Belgium
Christian Dirschl Wolters Kluwer Germany, Germany
Daniil Dobriy Vienna University of Economics and Business,
Austria
Milan Dojchinovski Czech Technical University in Prague,
Czech Republic
Ivan Donadello Free University of Bozen-Bolzano, Italy
Mauro Dragoni Fondazione Bruno Kessler, Italy
Kai Eckert Mannheim University of Applied Sciences,
Germany
V asilis Efthymiou Harokopio University of Athens, Greece
Shusaku Egami National Institute of Advanced Industrial Science
and Technology, Japan
Fajar J. Ekaputra Vienna University of Economics and Business
(WU), Austria
V adim Ermolayev Ukrainian Catholic University, Ukraine
Paola Espinoza Arias Universidad Politécnica de Madrid, Spain
Lorena Etcheverry Universidad de la República, Uruguay
Pavlos Fafalios Technical University of Crete and FORTH-ICS,
Greece
Alessandro Faraotti IBM, Italy
Catherine Faron Université Côte d’Azur, France
Anna Fensel Wageningen University and Research,
Netherlands
Javier D. Fernández F. Hoffmann-La Roche AG, Switzerland
Mariano Fernández López Universidad San Pablo CEU, Spain
Jesualdo Tomás Fernández-Breis Universidad de Murcia, Spain
Sebastián Ferrada Universidad de Chile, Chile
Agata Filipowska Poznan University of Economics, Poland
Erwin Filtz Siemens AG Österreich, Austria
Giorgos Flouris FORTH-ICS, Greece
Flavius Frasincar Erasmus University Rotterdam, Netherlands
Naoki Fukuta Shizuoka University, Japan
Michael Färber Karlsruhe Institute of Technology, Germany
Mohamed H. Gad-Elrab Bosch Center for Artiﬁcial Intelligence, Germany
Alban Gaignard CNRS, France

xii Organization
Luis Galárraga Inria, France
Fabien Gandon Inria, France
Aldo Gangemi Università di Bologna and ISTC-CNR, Italy
Raúl García-Castro Universidad Politécnica de Madrid, Spain
Andrés García-Silva Expert.ai, Spain
Daniel Garijo Universidad Politécnica de Madrid, Spain
Manas Gaur Wright State University, USA
Y uxia Geng Zhejiang University, China
Genet Asefa Gesese FIZ Karlsruhe – Leibniz-Institut für
Informationsinfrastruktur, Germany
Pouya Ghiasnezhad Omran Australian National University, Australia
Martin Giese University of Oslo, Norway
Jose M. Gimenez-Garcia Universidad de V alladolid, Spain
Francois Goasdoue Université de Rennes 1, France
Jose Manuel Gomez-Perez Expert.ai, Spain
Simon Gottschalk Leibniz Universität Hannover, Germany
Floriana Grasso University of Liverpool, UK
Damien Graux Huawei Research Ltd., UK
Paul Groth University of Amsterdam, Netherlands
Claudio Gutierrez Universidad de Chile, Chile
Peter Haase metaphacts GmbH, Germany
Mohad-Saïd Hacid Université Lyon 1, France
Torsten Hahmann University of Maine, USA
George Hannah University of Liverpool, UK
Andreas Harth Friedrich-Alexander-Universität
Erlangen-Nürnberg and Fraunhofer IIS,
Germany
Olaf Hartig Linköping University, Sweden
Oktie Hassanzadeh IBM, USA
Ivan Heibi University of Bologna, Italy
V eronika Heimsbakk Capgemini, Norway
Nicolas Heist University of Mannheim, Germany
Lars Heling Stardog Union, Germany
Nathalie Hernandez IRIT, France
Daniel Herzig metaphacts GmbH, Germany
Ryohei Hisano ETH Zurich, Switzerland
Pascal Hitzler Kansas State University, USA
Rinke Hoekstra Elsevier, Netherlands
Aidan Hogan Universidad de Chile, Chile
Andreas Hotho University of Wuerzburg, Germany
Wei Hu Nanjing University, China
Thomas Hubauer Siemens AG Corporate Technology, Germany

Organization xiii
Andreea Iana University of Mannheim, Germany
Luis Ibanez-Gonzalez University of Southampton, UK
Ana Iglesias-Molina Universidad Politécnica de Madrid, Spain
Filip Ilievski Vrije Universiteit Amsterdam, Netherlands
Antoine Isaac Europeana & Vrije Universiteit Amsterdam,
Netherlands
Hajira Jabeen GESIS – Leibniz Institute for the Social Sciences,
Germany
Nitisha Jain King’s College London, London, UK
Mustafa Jarrar Birzeit University, Palestine
Ernesto Jimenez-Ruiz City, University of London, UK
Milos Jovanovik Ss. Cyril and Methodius University in Skopje,
North Macedonia
Simon Jupp Elsevier, Netherlands
Jan-Christoph Kalo University of Amsterdam, Netherlands
Eduard Kamburjan University of Oslo, Norway
Maulik R. Kamdar Optum Health, USA
Katariina Kari Inter IKEA Systems B.V ., Finland
Tomi Kauppinen Aalto University, Finland
Mayank Kejriwal University of Southern California, USA
Natthawut Kertkeidkachorn Japan Advanced Institute of Science and
Technology, Japan
Ali Khalili Deloitte, Netherlands
Sabrina Kirrane Vienna University of Economics and Business,
Austria
Tomas Kliegr Prague University of Economics and Business,
Czech Republic
Matthias Klusch DFKI, Germany
Haridimos Kondylakis Institute of Computer Science, FORTH, Greece
George Konstantinidis University of Southampton, UK
Stasinos Konstantopoulos NCSR Demokritos, Greece
Roman Kontchakov Birkbeck, University of London, UK
Manolis Koubarakis National and Kapodistrian University of Athens,
Greece
Kozaki Kouji Osaka Electro-Communication University, Japan
Maria Koutraki Leibniz Universität Hannover, Germany
Anelia Kurteva TU Delft, Netherlands
Tobias Käfer Karlsruhe Institute of Technology, Germany
Birgitta König-Ries Friedrich Schiller University of Jena, German
Jose Emilio Labra Gayo Universidad de Oviedo, Spain
Frederique Laforest INSA Lyon, France
Sarasi Lalithsena IBM Watson, USA

xiv Organization
Andre Lamurias NOV A School of Science and Technology,
Portugal
Davide Lanti Free University of Bozen-Bolzano, Italy
Danh Le Phuoc TU Berlin, Germany
Maxime Lefrançois École des Mines de Saint-Étienne, France
Huanyu Li Linköping University, Sweden
Sven Lieber Royal Library of Belgium (KBR), Belgium
Stephan Linzbach GESIS – Leibniz Institute for the Social Sciences,
Germany
Anna-Soﬁa Lippolis University of Bologna and ISTC-CNR, Italy
Pasquale Lisena EURECOM, France
Wenqiang Liu Xi’an Jiaotong University, China
Giorgia Lodi Istituto di Scienze e Tecnologie della Cognizione
(CNR), Italy
V anessa Lopez IBM, Ireland
Pierre Maillot Inria, France
Maria Maleshkova Helmut-Schmidt-Universität/Universität der
Bundeswehr Hamburg, Germany
Maria V anina Martinez IIIA-CSIC, Spain
Miguel A. Martinez-Prieto University of V alladolid, Spain
Jose L. Martinez-Rodriguez Autonomous University of Tamaulipas, Mexico
Patricia Martín-Chozas Universidad Politécnica de Madrid, Spain
Edgard Marx Leipzig University of Applied Sciences (HTWK),
Germany
Philipp Mayr GESIS – Leibniz Institute for the Social Sciences,
Germany
Jamie McCusker Rensselaer Polytechnic Institute, USA
Lionel Medini CNRS, France
Albert Meroño-Peñuela King’s College London, UK
Franck Michel Université Côte d’Azur, CNRS, I3S, France
Nandana Mihindukulasooriya IBM Research AI, USA
Nada Mimouni CEDRIC lab - CNAM Conservatoire National des
Arts et Métiers Pari, France
Daniel Miranker The University of Texas at Austin, USA
Victor Mireles Semantic Web Company, Austria
Pascal Molli University of Nantes, France
Pierre Monnin Université Côte d’Azur, Inria, CNRS, I3S, Sophia
Antipolis, France
Boris Motik University of Oxford, UK
Enrico Motta The Open University, UK
Diego Moussallem Paderborn University, German
Paul Mulholland The Open University, UK
V arish Mulwad GE Research, India

Organization xv
Raghava Mutharaju IIIT-Delhi, India
María Navas-Loro Universidad Politécnica de Madrid, Spain
Fabian Neuhaus University of Magdeburg, Germany
Vinh Nguyen National Library of Medicine, NIH, USA
Andriy Nikolov AstraZeneca, UK
Nikolay Nikolov SINTEF, Norway
Andrea Nuzzolese ISTC-CNR, Italy
Cliff O’Reilly City London University, UK
Femke Ongenae Ghent University, Belgium
Francesco Osborne The Open University, UK
Ankur Padia UBMC, USA
George Papadakis National Technical University of Athens, Greece
Pierre-Henri Paris Telecom Paris, France
Heiko Paulheim University of Mannheim, German
Terry Payne University of Liverpool, UK
Tassilo Pellegrini University of Applied Sciences St. Pölten, Austria
Maria Angela Pellegrino Università degli Studi di Salerno, Italy
Bernardo Pereira Nunes Australian National University, Australia
Romana Pernisch Vrije Universiteit Amsterdam, Netherlands
Catia Pesquita Universidade de Lisboa, Portugal
Rafael Peñaloza University of Milano-Bicocca, Italy
Guangyuan Piao National University of Ireland, Ireland
Francesco Piccialli University of Naples Federico II, Italy
Lydia Pintscher Wikimedia Deutschland, Germany
Dimitris Plexousakis Institute of Computer Science, FORTH, Greece
Axel Polleres Vienna University of Economics and Business,
Austria
Livio Pompianu University of Cagliari, Italy
María Poveda-Villalón Universidad Politécnica de Madrid, Spain
Nicoleta Preda University of V ersailles
Saint-Quentin-en-Yvelines, France
V alentina Presutti University of Bologna, Italy
Joe Raad University of Paris-Saclay, France
Alexandre Rademaker IBM Research and EMAp/FGV , Brazil
Helen Mair Rawsthorne École des Mines de Saint-Étienne, France
Simon Razniewski Bosch Center for Artiﬁcial Intelligence, Germany
Diego Reforgiato Università degli studi di Cagliari, Italy
Artem Revenko Semantic Web Company GmbH, Austria
Mariano Rico Universidad Politécnica de Madrid, Spain
Célian Ringwald Université Côte d’Azur, Inria, CNRS, I3S, France
Giuseppe Rizzo LINKS Foundation, Italy
Mariano Rodríguez Muro Google, USA

xvi Organization
Sergio José Rodríguez Méndez Australian National University, Australia
Edelweis Rohrer Universidad de la República, Uruguay
Julian Rojas Ghent University, Belgium
Maria Del Mar Roldan-Garcia Universidad de Malaga, Spain
Oscar Romero Universitat Politècnica de Catalunya, Spain
Miguel Romero Orth Universidad Adolfo Ibáñez, Chile
Henry Rosales-Méndez University of Chile, Chile
Catherine Roussey INRAE, France
Sebastian Rudolph TU Dresden, Germany
Anisa Rula University of Brescia, Italy
Alessandro Russo STLab, ISTC-CNR, Italy
Marta Sabou Vienna University of Economics and Business,
Austria
Harald Sack FIZ Karlsruhe, Leibniz Institute for Information
Infrastructure & KIT Karlsruhe, Germany
Afshin Sadeghi Fraunhoder IAIS, Germany
Angelo Antonio Salatino The Open University, UK
Muhammad Saleem AKSW, University Of Leizpig, Germany
Bruno Sartini Ludwig-Maximilians University of Munich,
Germany
Felix Sasaki Cornelsen V erlag GmbH & TH Brandenburg,
Germany
Fatiha Saïs University of Paris-Saclay, France
Ralf Schenkel Trier University, Germany
Stefan Schlobach Vrije Universiteit Amsterdam, Netherlands
Daniel Schwabe PUC-Rio, Brazil
Mario Scrocca Cefriel, Italy
Juan F. Sequeda data.world, USA
Umutcan Serles STI, University of Innsbruck, Austria
Bari¸s Sertkaya Frankfurt University of Applied Sciences,
Germany
Cogan Shimizu Wright State University, USA
Pavel Shvaiko Informatica Trentina, Italy
Lucia Siciliani University of Bari, Italy
Leslie Sikos Edith Cowan University, Australia
Gerardo Simari Universidad Nacional del Sur (UNS) and
CONICET, Argentina
Elena Simperl King’s College London, UK
Hala Skaf-Molli University of Nantes, France
Blerina Spahiu University of Milano-Bicocca, Italy
Marc Spaniol Université de Caen Normandie, France
Kavitha Srinivas IBM, USA

Organization xvii
Steffen Staab UNI Stuttgart, Germany
Bram Steenwinckel Ghent University, Belgium
Kostas Stefanidis Tampere University, Finland
Nadine Steinmetz University of Applied Sciences Erfurt, Germany
Armando Stellato University of Rome Tor V ergata, Italy
Simon Steyskal Siemens AG Österreich, Austria
Lise Stork Vrije Universiteit Amsterdam, Netherlands
Umberto Straccia ISTI-CNR, Italy
Chang Sun Institute of Data Science at Maastricht University,
Netherlands
Zequn Sun Nanjing University, China
Vo j t ˇech Svátek Prague University of Economics and Business,
Czech Republic
Ruben Taelman Ghent University, Belgium
Y ousouf Taghzouti École des Mines de Saint-Étienne, France
V alentina Tamma University of Liverpool, UK
Olivier Teste IRIT, France
Krishnaprasad Thirunarayan Wright State University, USA
Elodie Thiéblin Logilab, France
Ilaria Tiddi Vrije Universiteit Amsterdam, Netherlands
Tabea Tietz FIZ Karlsruhe, Germany
Konstantin Todorov University of Montpellier, France
Ioan Toma STI Innsbruck, Austria
Riccardo Tommasini INSA Lyon, France
Sebastian Tramp eccenca GmbH, Germany
Trung-Kien Tran Bosch Center for Artiﬁcial Intelligence, Germany
Cassia Trojahn IRIT, France
Raphaël Troncy EURECOM, France
Yannis Tzitzikas University of Crete and FORTH-ICS, Greece
Jürgen Umbrich Vienna University of Economy and Business
(WU), Austria
Ricardo Usbeck Leuphana University Lüneburg, Germany
Marieke van Erp KNAW Humanities Cluster, Netherlands
Frank V an Harmelen Vrije Universiteit Amsterdam, Netherlands
Miel V ander Sande Meemoo, Belgium
Guillermo V ega-Gorgojo Universidad de V alladolid, Spain
Ruben V erborgh Ghent University, Belgium
Maria-Esther Vidal TIB, Germany
Serena Villata CNRS, France
Fabio Vitali University of Bologna, Italy
Domagoj Vrgoc Pontiﬁcia Universidad Católica de Chile, Chile
Kewen Wang Grifﬁth University, Australia

xviii Organization
Ruijie Wang University of Zurich, Switzerland
Xander Wilcke Vrije Universiteit Amsterdam, Netherlands
Honghan Wu King’s College London, UK
Zhe Wu eBay, USA
Josiane Xavier Parreira Siemens AG Österreich, Austria
Guohui Xiao University of Bergen, Norway
Nadia Yacoubi Ayadi Université Claude Bernard Lyon 1, France
Fouad Zablith American University of Beirut, Lebanon
Hamada Zahera Paderborn University, Germany
Ondˇrej Zamazal Prague University of Economics and Business,
Czech Republic
Xiaowang Zhang Tianjin University, China
Ziqi Zhang Accessible Intelligence, UK
Yihang Zhao King’s College London, UK
Antoine Zimmermann École des Mines de Saint-Étienne, France
Sara Zuppiroli ISTC-CNR, Italy
Hanna ´Cwiek-Kupczy´nska University of Luxembourg, Luxembourg
K¯arlis ˇCer¯ans University of Latvia, Latvia
Additional Reviewers
Akaichi, Ines
Antakli, Andre
Bruns, Oleksandra
Cardellino, Cristian
Cintra, Paul
Djeddi, Warith Eddine
Fanourakis, Nikolaos
Fischer, Elisabeth
Gaur, Manas
Gautam, Nikita
Gui, Zhou
Martín Chozas, Patricia
Montiel-Ponsoda, Elena
Morales Tirado, Alba Catalina
Nayyeri, Mojtaba
Olivier, Inizan
Omeliyanenko, Janna
Ondraszek, Sarah Rebecca
Patkos, Theodore
Peng, Yiwen
Pons, Gerard
Qu, Y uanwei
Ragazzi, Luca
Raouﬁ, Ensiyeh
Ratta, Marco
Ringwald, Célian
Schlör, Daniel
Schraudner, Daniel
Shao, Chen
van der Weijden, Daniel
Viviurka Do Carmo, Paulo Ricardo
Xiong, Bo
Y umusak, Semih

Organization xix
Sponsors
Platinum Sponsors
VideoLectures.NET is an award-winning free and open access educational video lec-
tures repository. The lectures are given by distinguished scholars and scientists at the
most important and prominent events like conferences, summer schools, workshops and
science promotional events from many ﬁelds of science. The portal is aimed at promoting
science, exchanging ideas and fostering knowledge sharing by providing high quality
didactic contents not only to the scientiﬁc community but also to the general public. All
lectures, accompanying documents, information and links are systematically selected
and classiﬁed through the editorial process taking into account also users’ comments.
Gold Sponsors
Ontotext is a global leader in enterprise knowledge graph technology and semantic
database engines. Ontotext employs big knowledge graphs to enable uniﬁed data access
and cognitive analytics via text mining and integration of data across multiple sources.
Ontotext™ engine and Ontotext Platform power business critical systems in the biggest
banks, media, market intelligence agencies, car and aerospace manufacturers. Ontotext
technology and solutions are spread wide across the value chain of the most knowledge
intensive enterprises in ﬁnancial services, publishing, healthcare, pharma, manufacturing
and public sectors. Leveraging AI and cognitive technologies, Ontotext helps enterprises
get competitive advantage, by connecting the dots of their proprietary knowledge and
putting in the context of global intelligence.

xx Organization
Silver Sponsors
Springer is part of Springer Nature, a leading global research, educational and pro-
fessional publisher, home to an array of respected and trusted brands providing quality
content through a range of innovative products and services. Springer Nature is the
world’s largest academic book publisher, publisher of the world’s most inﬂuential jour-
nals and a pioneer in the ﬁeld of open research. The company numbers almost 13,000
staff in over 50 countries and has a turnover of approximately e1.5 billion. Springer
Nature was formed in 2015 through the merger of Nature Publishing Group, Palgrave
Macmillan, Macmillan Education and Springer Science+Business Media.
Founded over 350 years ago, the University of Innsbruck today is the most important
research and educational institution in western Austria, offering a wide range of pro-
grammes across all disciplines. Located in the heart of the Alps, it offers 28,000 students
and 5,500 employees the best conditions.
Bronze Sponsors
metaphacts is a German software company that empowers customers to drive knowl-
edge democratization and decision intelligence using knowledge graphs. Built entirely
on open standards and technologies, our product metaphactory delivers a low-code, FAIR
Data platform that supports collaborative knowledge modeling and knowledge gener-
ation and enables on-demand citizen access to consumable, contextual and actionable
knowledge. metaphacts serves customers in areas such as life sciences and pharma, engi-
neering and manufacturing, ﬁnance and insurance, retail, cultural heritage, and more.
For more information about metaphacts and its products and solutions please visit www.
metaphacts.com.

Organization xxi
eccenca Corporate Memory is cutting-edge Knowledge Graph technology. It digitally
captures the expertise of knowledge workers so that it can be accessed and processed
by machines. The fusion of human knowledge with large amounts of data, coupled with
the computing power of machines, results in powerful artiﬁcial intelligence that enables
companies to execute existing processes as well as innovation projects of all kinds at
high speed and low cost. And it creates an impressive competitive advantage.
Through eccenca.my you can register and create an eccenca Corporate Memory Com-
munity Edition Sandbox for evaluation. Join pioneers like Bosch, Siemens, AstraZeneca
and many other global market leaders – our world-class team of Linked Data Experts is
ready when you are.

Contents – Part II
Resource
PyGraft: Conﬁgurable Generation of Synthetic Schemas and Knowledge
Graphs at Y our Fingertips . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 3
Nicolas Hubert, Pierre Monnin, Mathieu d’Aquin, Davy Monticolo,
and Armelle Brun
NORIA-O: An Ontology for Anomaly Detection and Incident Management
i nI C TS y s t e m s ....................................................... 2 1
Lionel Tailhardat, Yoan Chabot, and Raphael Troncy
FlexRML: A Flexible and Memory Efﬁcient Knowledge Graph Materializer . . . 40
Michael Freund, Sebastian Schmid, Rene Dorsch, and Andreas Harth
IICONGRAPH: Improved Iconographic and Iconological Statements
in Knowledge Graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 57
Bruno Sartini
VisionKG: Unleashing the Power of Visual Datasets via Knowledge Graph . . . . 75
Jicheng Yuan, Anh Le-Tuan, Manh Nguyen-Duc, Trung-Kien Tran,
Manfred Hauswirth, and Danh Le-Phuoc
OfﬁceGraph: A Knowledge Graph of Ofﬁce Building IoT Measurements . . . . . . 94
Roderick van der Weerdt, Victor de Boer, Ronald Siebes,
Ronnie Groenewold, and Frank van Harmelen
Musical Meetups Knowledge Graph (MMKG): A Collection of Evidence
for Historical Social Network Analysis . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 110
Alba Morales Tirado, Jason Carvalho, Marco Ratta,
Chukwudi Uwasomba, Paul Mulholland, Helen Barlow,
Trevor Herbert, and Enrico Daga
Generate and Update Large HDT RDF Knowledge Graphs on Commodity
H a r d w a r e ............................................................ 1 2 8
Antoine Willerval, Dennis Diefenbach, and Angela Bonifati
SMW Cloud: A Corpus of Domain-Speciﬁc Knowledge Graphs
f r o mS e m a n t i cM e d i a W i k i s ............................................. 1 4 5
Daniil Dobriy, Martin Beno, and Axel Polleres

xxiv Contents – Part II
SousLeSens - A Comprehensive Suite for the Industrial Practice
of Semantic Knowledge Graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 162
Claude Fauconnet, Jean-Charles Leclerc, Arkopaul Sarkar,
and Mohamed Hedi Karray
MLSea: A Semantic Layer for Discoverable Machine Learning . . . . . . . . . . . . . . 178
Ioannis Dasoulas, Duo Yang, and Anastasia Dimou
Enabling Social Demography Research Using Semantic Technologies . . . . . . . . . 199
Lise Stork, Richard L. Zijdeman, Ilaria Tiddi, and Annette ten Teije
SCOOP All the Constraints’ Flavours for Y our Knowledge Graph . . . . . . . . . . . . 217
Xuemin Duan, David Chaves-Fraga, Olivier Derom,
and Anastasia Dimou
FidMark: A Fiducial Marker Ontology for Semantically Describing Visual
M a r k e r s .............................................................. 2 3 5
Maxim Van de Wynckel, Isaac Valadez, and Beat Signer
Author Index ......................................................... 2 5 1

Contents – Part I
Research
Do Similar Entities Have Similar Embeddings? . . . . . . . . . . . . . . . . . . . . . . . . . . . . 3
Nicolas Hubert, Heiko Paulheim, Armelle Brun, and Davy Monticolo
Treat Different Negatives Differently: Enriching Loss Functions
with Domain and Range Constraints for Link Prediction . . . . . . . . . . . . . . . . . . . . 22
Nicolas Hubert, Pierre Monnin, Armelle Brun, and Davy Monticolo
QAGCN: Answering Multi-relation Questions via Single-Step Implicit
Reasoning over Knowledge Graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 41
Ruijie Wang, Luca Rossetto, Michael Cochez, and Abraham Bernstein
Leveraging Pre-trained Language Models for Time Interval Prediction
in Text-Enhanced Temporal Knowledge Graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . 59
Duygu Sezen Islakoglu, Melisachew Wudage Chekol,
and Yannis Velegrakis
A Language Model Based Framework for New Concept Placement
i nO n t o l o g i e s ......................................................... 7 9
Hang Dong, Jiaoyan Chen, Yuan He, Yongsheng Gao, and Ian Horrocks
Low-Dimensional Hyperbolic Knowledge Graph Embedding for Better
Extrapolation to Under-Represented Data . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 100
Zhuoxun Zheng, Baifan Zhou, Hui Yang, Zhipeng Tan, Arild Waaler,
Evgeny Kharlamov, and Ahmet Soylu
SC-Block: Supervised Contrastive Blocking Within Entity Resolution
P i p e l i n e s ............................................................. 1 2 1
Alexander Brinkmann, Roee Shraga, and Christina Bizer
Navigating Ontology Development with Large Language Models . . . . . . . . . . . . . 143
Mohammad Javad Saeedizade and Eva Blomqvist
ESLM: Improving Entity Summarization by Leveraging Language Models . . . . 162
Asep Fajar Firmansyah, Diego Moussallem,
and Axel-Cyrille Ngonga Ngomo

xxvi Contents – Part I
Explanation of Link Predictions on Knowledge Graphs via Levelwise
Filtering and Graph Summarization . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 180
Roberto Barile, Claudia d’Amato, and Nicola Fanizzi
Large Language Models for Scientiﬁc Question Answering: An Extensive
Analysis of the SciQA Benchmark . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 199
Jens Lehmann, Antonello Meloni, Enrico Motta, Francesco Osborne,
Diego Reforgiato Recupero, Angelo Antonio Salatino, and Sahar Vahdati
Efﬁcient Evaluation of Conjunctive Regular Path Queries Using Multi-way
J o i n s ................................................................. 2 1 8
Nikolaos Karalis, Alexander Bigerl, Liss Heidrich,
Mohamed Ahmed Sherif, and Axel-Cyrille Ngonga Ngomo
Can Contrastive Learning Reﬁne Embeddings . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 236
Lihui Liu, Jinha Kim, and Vidit Bansal
In-Use
Automation of Electronic Invoice V alidation Using Knowledge Graph
Technologies . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 253
Johannes Mäkelburg, Christian John, and Maribel Acosta
Towards Cyber Mapping the German Financial System with Knowledge
Graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 270
Markus Schröder, Jacqueline Krüger, Neda Foroutan, Philipp Horn,
Christoph Fricke, Ezgi Delikanli, Heiko Maus, and Andreas Dengel
Integrating Domain Knowledge for Enhanced Concept Model
Explainability in Plant Disease Classiﬁcation . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 289
Jihen Amara, Sheeba Samuel, and Birgitta König-Ries
Generative Expression Constrained Knowledge-Based Decoding for Open
D a t a ................................................................. 3 0 7
Lucas Lageweg and Benno Kruit
OntoEditor: Real-Time Collaboration via Distributed V ersion Control
f o rO n t o l o g yD e v e l o p m e n t .............................................. 3 2 6
Ahmad Hemid, Waleed Shabbir, Abderrahmane Khiat,
Christoph Lange, Christoph Quix, and Stefan Decker
Author Index ......................................................... 3 4 3

Resource

PyGraft: Conﬁgurable Generation
of Synthetic Schemas and Knowledge
Graphs at Your Fingertips
Nicolas Hubert1,2(B) , Pierre Monnin3 , Mathieu d’Aquin2 ,
Davy Monticolo1 , and Armelle Brun2
1 Universit´e de Lorraine, ERPI, Nancy, France
{nicolas.hubert,davy.monticolo}@univ-lorraine.fr
2 Universit´e de Lorraine, CNRS, LORIA, Nancy, France
{mathieu.daquin,armelle.brun}@univ-lorraine.fr
3 Universit´eC ˆote d’Azur, Inria, CNRS, I3S, Sophia-Antipolis, France
pierre.monnin@inria.fr
Abstract. Knowledge graphs (KGs) have emerged as a prominent data
representation and management paradigm. Being usually underpinned
by a schema (e.g., an ontology), KGs capture not only factual informa-
tion but also contextual knowledge. In some tasks, a few KGs established
themselves as standard benchmarks. However, recent works outline that
relying on a limited collection of datasets is not suﬃcient to assess the
generalization capability of an approach. In some data-sensitive ﬁelds
such as education or medicine, access to public datasets is even more
limited. To remedy the aforementioned issues, we release PyGraft, a
Python-based tool that generates highly customized, domain-agnostic
schemas and KGs. The synthesized schemas encompass various RDFS
and OWL constructs, while the synthesized KGs emulate the character-
istics and scale of real-world KGs. Logical consistency of the generated
resources is ultimately ensured by running a description logic (DL) rea-
soner. By providing a way of generating both a schema and KG in a
single pipeline, PyGraft’s aim is to empower the generation of a more
diverse array of KGs for benchmarking novel approaches in areas such
as graph-based machine learning (ML), or more generally KG process-
ing. In graph-based ML in particular, this should foster a more holistic
evaluation of model performance and generalization capability, thereby
going beyond the limited collection of available benchmarks. PyGraft is
available at: https://github.com/nicolas-hbt/pygraft.
Keywords: Knowledge Graph
· Schema · Semantic Web · Synthetic
Data Generator
Resource type: Software
License: MIT License
DOI: https://doi.org/10.5281/zenodo.10243209
URL: https://github.com/nicolas-hbt/pygraft
c⃝ The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
A. Mero˜no Pe˜nuela et al. (Eds.): ESWC 2024, LNCS 14665, pp. 3–20, 2024.
https://doi.org/10.1007/978-3-031-60635-9_1

4N . H u b e r t e t a l .
1 Introduction
Knowledge graphs (KGs) have been increasingly used as a graph-structure repre-
sentation of data. More speciﬁcally, a KG is a collection of triples (s, p, o) where
s (subject) and o (object) are two entities of the graph, andp is a predicate that
qualiﬁes the nature of the relation holding between them [ 16]. KGs are usually
underpinned by a schema ( e.g., an ontology) which deﬁnes the main concepts
and relations of a domain of interest, as well as the rules under which these
concepts and relations are allowed to interact [14].
KGs are being used in a wide array of tasks, in many of which a limited
collection of KGs established themselves as standard benchmarks for evaluating
model performance. However, there are some concerns around the sole usage
of these speciﬁc mainstream KGs for assessing the generalization capability of
newly introduced models. For example, for the particular task of node classiﬁca-
tion, it has been demonstrated that mainstream datasets such as CiteSeer, Cora,
and PubMed feature similar statistical characteristics, especially homophily [24].
Consequently, new models are assessed with respect to a collection of statistically
similar datasets. Therefore, their performance improvement does not always hold
beyond the standard benchmark datasets [24]. Similarly, it has been shown that
many link prediction train sets suﬀer from extremely skewed distributions in
both the degrees of entities and the occurrence of a subset of predicates [28]. In
addition, some of the established link prediction datasets are plagued with data
biases [27] and include many occurrences of inference patterns [8,21,22] that pre-
dictive models are able to incorporate, which may cause overly optimistic evalu-
ation performance [8]. For example, the mainstream FB15k and WN18 datasets
are substantially aﬀected by these biases. Therefore, more diverse datasets are
needed [27]. In this situation, it is of utmost importance to provide a way for
researchers to generate synthetic yet realistic datasets of diﬀerent shapes and
characteristics, so that new models can be evaluated in a wide range of data
settings.
Worse than relying on a limited number of KGs is the lack of publicly avail-
able KGs in some application ﬁelds. Conducting research in domains such as
education, law enforcement, or medicine, is particularly diﬃcult. On the grounds
of data privacy, collecting and sharing real-world knowledge may not be possi-
ble. As such, domain-oriented KGs are barely accessible in these areas. However,
engineers, practitioners, and researchers usually have precise ideas of the char-
acteristics of their problem of interest. In this context, it would be beneﬁcial to
generate a synthetic KG that emulates the characteristics of a real KG [11].
The aforementioned issues led to several attempts at building synthetic gen-
erators of schemas and KGs, even though in most cases these two aspects have
been considered separately. Stochastic-based generators have been proposed to
output domain-agnostic KGs [1,10,25]. However good these methods are at gen-
erating large graphs quickly, their data generation process does not allow to
take an underlying schema into account [ 11]. Therefore, the resulting KGs are
not guaranteed to accurately mimic the characteristics of real-world KGs in a
desired application ﬁeld. In contrast, schema-driven generators are able to syn-
thesize KGs that resemble real-world data. However, most works focused on

PyGraft: Conﬁgurable Generation of Synthetic Schemas and KGs 5
generating synthetic KGs on the basis of an already existing schema [ 23]. Syn-
thesizing both a schema and a KG underpinned by it is a more challenging task
that has been considered but with only limited success so far [23].
In this work, we aim at addressing this issue. In particular, we present
PyGraft, a Python-based tool to generate highly customized, domain-agnostic
schemas and KGs. The contributions of our work are the following:
– To the best of our knowledge, PyGraft is the ﬁrst generator dedicated to
the generation of both schemas and KGs in a unique pipeline, while being
highly tunable based on a broad array of user-speciﬁed parameters. Notably,
the generated resources are domain-agnostic, which makes them usable for
benchmarking purposes regardless of the application ﬁeld.
– The generated schemas and KGs are built with an extended set of RDFS
and OWL constructs and their logical consistency is ensured by the use of a
DL reasoner, which allows for both ﬁne-grained description of resources and
strict compliance with common Semantic Web standards.
– We publicly release our code with a documentation and accompanying exam-
ples for ease of use.
The remainder of the paper is structured as follows. Related work is presented
in Sect.2. In Sect.3, PyGraft is detailed and accompanied with necessary back-
ground knowledge and comparisons with other available generators. In Sect.4,a
thorough performance analysis of PyGraft is presented. A discussion on current
potential use cases, limitations, and future work can be found in Sect.5. Lastly,
Sect.6 sums up the key insights presented in this paper.
2 Related Work
The generation principle governing synthetic graph generators leads to diﬀeren-
tiate between stochastic-based, deep generative ,a n dsemantic-driven generators.
Along the description of these families of generators, Table1 provides details on
current and open-source implementations. These tools are also compared with
PyGraft regarding several criteria.
Stochastic-based generators are usually characterized by their ability to
output large graphs in a short amount of time. Early works are represented by
the famous Erd˝os-R´enyi model [10]. The Erd˝os-R´enyi model generates graphs
by independently assigning edges between pairs of nodes with a ﬁxed probabil-
ity. The Barab´asi-Albert model [ 1] exhibits scale-free degree distributions and
is based on the principle of preferential attachment, where new nodes are more
likely to attach to nodes with higher degrees. The R-MAT model [ 5] generates
large-scale power-law graphs with properties like power-law degree distributions
and community structures. More recently, TrillionG [25] – presented as an exten-
sion of R-MAT – represents nodes and edges as vectors in a high-dimensional
space. TrillionG allows users to generate large graphs up to trillions of edges
while exhibiting lower space and time complexities than previously proposed
generators. In Table 1, stochastic-based generators are represented by igraph
1,
1 https://github.com/igraph/python-igraph/.

6N . H u b e r t e t a l .
NetworkX2, and Snap3. Although they are not speciﬁcally designed for graph
generation, they provide oﬀ-the-shelf implementations for generating random
graphs, such as the Erd˝os-R´enyi and Barab´asi-Albert models. They are domain-
agnostic and scalable, but do not take into account any semantics.
Deep generative graph generators are trained on existing graph datasets
and learn to capture the underlying patterns of the input graphs. Deep genera-
tive graph models are typically based on generative adversarial networks (GANs)
and graph neural networks (GNNs), recurrent neural networks (RNNs), or vari-
ational autoencoders (VAEs). GraphGAN [31] leverages the GAN structure, in
which the generative model receives a vertex and aims at ﬁtting its true connec-
tivity distribution over all other vertices – thereby producing fake samples for the
discriminative model to diﬀerentiate from ground-truth samples. GraphRNN [32]
is a deep autoregressive model that trains on a collection of graphs. It can be
viewed as a hierarchical model adding nodes and edges in a sequential manner.
A representant of the VAE family of generators is NeVAE [29], which is specif-
ically designed for molecular graphs. NeVAE features a decoder which is able
to guarantee a set of valid properties in the generated molecules. In particular,
MolGAN [7]a n dN e V A E[29] are bound to molecular graph generation. There-
fore, they are not domain-agnostic (Table1). The other generators of this family
are, but they do not take a schema as input when generating random graphs,
i.e., they are not schema-driven (Table1).
Semantic-driven generators, in contrast, incorporate schema-based con-
straints or external knowledge to generate graphs that exhibit speciﬁc char-
acteristics or follow certain patterns relevant to the given ﬁeld of application.
In [15], the Lehigh University Benchmark (LUBM) and the Univ-Bench Artiﬁcial
data generator (UBA) are presented. The former is an ontology modelling the
university domain while the latter aims at generating synthetic graphs based on
the LUBM schema as well as user-deﬁned queries and restrictions. Similarly, the
Linked Data Benchmark Council (LDBC) [2] released the Social Network Bench-
mark (SNB), which includes a graph generator for synthesizing social network
data based on realistic distributions. gMark [3] has subsequently been presented
as the ﬁrst generator that satisﬁes the criteria of being domain-independent, scal-
able, schema-driven, and highly conﬁgurable, all at the same time. However, it
still requires already existing schemas as input. In [23], Melo and Paulheim focus
on the synthesis of KGs for the purpose of benchmarking link prediction and type
prediction tasks. The authors claim that there is a need for more diverse bench-
mark datasets for link prediction, with the possibility of having control over
their characteristics ( e.g., the number of entities, relation assertions, number
of types, etc.). Therefore, Melo and Paulheim propose a synthesizing approach
which replicates input real-world graphs while allowing for controlled variations
in graph characteristics. Notably, they highlight the fact that most works, includ-
ing theirs, focus on synthesizing KGs based on an existing schema, which leads
them to formulate the desiderata of generating both a schema and a KG from
scratch as a promising venue for future work – which PyGraft actually does.
2 https://github.com/networkx/networkx/.
3 https://github.com/snap-stanford/snap-python/.

PyGraft: Conﬁgurable Generation of Synthetic Schemas and KGs 7
Subsequently, Feng et al. [11] proposed a schema-driven graph generator based
on the concept of Extended Graph Diﬀerential Dependencies (GDDx). However,
their approach cannot generate domain-agnostic schemas and thus requires an
existing schema as input. The DLCC benchmark proposed in [ 26] features a
synthetic KG generator based on user-speciﬁed graph and schema properties.
Beyond asking for a given number of nodes, relations and degree distribution in
the resulting KG, it allows for specifying a fewRDFS constructs for the generation
of the underpinning schema.
None of the aforementioned semantic-driven generators perform a logical con-
sistency check of the generated graphs (see Table1). Additionally, they can only
produce ﬁnal KGs based on an input schema. Some of them are also domain-
speciﬁc. DLCC [26] is the closest work to ours, and, to the best of our knowl-
edge, this is the ﬁrst and only work that allows to generate both a schema and a
KG while being domain-agnostic. However, it only features 3 schema constructs,
namely rdfs:domain, rdfs:range,a n drdfs:subClassOf. These sole three con-
structs do not pose any constraints on triple generation (hence the consistency
checking is not needed) and do not fully feature all Semantic Web possibilities
that could exist in KGs. This is also why the resources generated with the DLCC
generator do not undergo any logical consistency checks (see Table1).
In the present work, we aim at going a step further and taking numerousRDFS
and OWL constructs into account, as PyGraft features a broad range of schema
constructs (see Tables 2 and 3). Considered together, these constructs lead to
many potential sources of inconsistencies that need to be carefully avoided with
speciﬁc procedures and a ﬁnal consistency check using a DL reasoner. However,
this more challenging setting allows PyGraft to generate KGs that feature a
broader range of Semantic Web possibilities.
3 PyGraft Description
This section starts by formally introducing the notions of schema and knowledge
graph. The schematic overview of PyGraft is presented in Sect. 3.2. PyGraft
schema and KG generation pipelines are presented in Sects.3.3 and 3.4, respec-
tively.
3.1 Preliminaries
On the one hand, a schema – e.g., an ontology – refers to a explicit speciﬁca-
tion of a conceptualization that includes concepts, properties, and restrictions
within a particular domain of knowledge [14]. It helps ensure consistency, clarity,
and interoperability when representing and sharing knowledge. In our work, we
consider schemas to be represented as a collection of concepts C, properties P,
and axioms A, i.e., S = {C,P,A}. Schemas are typically represented using for-
mal languages such as RDFS4 (Resource Description Framework) andOWL5 (Web
Ontology Language).
4 https://www.w3.org/RDFS/.
5 https://www.w3.org/OWL/.

8N . H u b e r t e t a l .
Table 1. Feature comparison of graph generation tools. Dashed line is used when a
feature is not applicable due to the characteristics of the described generation tool.
Domain-agnostic denotes whether a given tool is able to potentially operate with
schemas of diﬀerent application ﬁelds.
Tool Domain-
agnostic
Schema-
driven
Schema
generation
Schema
properties
Graph
properties
Scalable Consistency
check
igrapha ✓ ✗ ✗ – ✓ ✓ –
NetworkXb ✓ ✗ ✗ – ✓ ✓ –
Snapc ✓ ✗ ✗ – ✓ ✓ –
GraphGen [ 13] ✓ ✗ ✗ – ✓ ✓ –
GraphRNN [ 32] ✓ ✗ ✗ – ✓ ✓ –
GraphVAE [30] ✓ ✗ ✗ – ✓ ✗ –
GraphWorld [ 24] ✓ ✗ ✗ – ✓ ✓ –
MolGAN [ 7] ✗ ✗ ✗ – ✓ ✗ –
NeVAE [29] ✗ ✗ ✗ – ✓ ✓ –
UBA-LUBM [ 15] ✗ ✓ ✗ – ✓ ✓ ✗
SNB [ 2] ✗ ✓ ✗ – ✓ ✓ ✗
gMark [ 3] ✓ ✓ ✗ – ✓ ✓ ✗
Melo et al. [23] ✓ ✓ ✗ – ✓ ✓ ✗
GDDx [11] ✓ ✓ ✗ – ✓ ✓ ✗
DLCC [ 26] ✓ ✓ ✓ 3 ✓ ✓ ✗
PyGraph (ours) ✓ ✓ ✓ 13 ✓ ✓ ✓
ahttps://github.com/igraph/python-igraph/
bhttps://github.com/networkx/networkx/
chttps://github.com/snap-stanford/snap-python/
Regarding KGs, distinct deﬁnitions co-exist [4,9]. In this work, we stick to the
inclusive deﬁnition of Hoganet al. [16], i.e., we consider a KG to be a graph where
nodes represent entities and edges represent relations between these entities. The
link between schemas and KGs lies in the fact that schemas are often used to
deﬁne the structure and semantics of a KG. In other words, a schema deﬁnes
the vocabulary and rules that govern entities and relationships in a KG. In this
view, a KG is a data graph that can be potentially enhanced with a schema [16].
3.2 Overview
From a high-level perspective, the entire PyGraft generation pipeline is depicted
in Fig.1. In particular, Class and Relation Generators are ﬁrstly initialized with
user-speciﬁed parameters, and are then used for building the schema incremen-
tally. The logical consistency of the schema is subsequently checked using Her-
miT reasoner [ 12] through the owlready2
6 Python library. If the user is also
interested in generating a KG based on this schema, the KG Generator is ini-
tialized with KG-related parameters, and takes the previously generated schema
as input in order to sequentially build the KG. Ultimately, the logical consistency
of the resulting KG is assessed with HermiT. More details on the schema-level
generation are provided in Sect.3.3, while Sect.3.4 describes the KG generation
procedure.
6 https://github.com/pwin/owlready2/.

PyGraft: Conﬁgurable Generation of Synthetic Schemas and KGs 9
Class Generator
Relation Generator
Schema
Parameters Schema
KG
Parameters KG Generator
KG
Consistency
Checking
Consistency
Checking
Fig. 1. PyGraft general overview.
3.3 Schema Generation
Table 2. User-deﬁned parameters for schema and KG generations.
Parameter Description
Classes num classes Number of classes
max depth Depth of the class hierarchy
avg depth Average class depth
inheritance ratio Proportion of rdfs:subClassOf
avg disjointness Proportion of owl:DisjointWith
Relations num relations Number of relations
prop profiled relations Proportion of rdfs:domain and rdfs:range
relation specificity Average depth of rdfs:domain and rdfs:range
prop asymmetric Proportion of owl:AsymmetricProperty
prop symmetric Proportion of owl:SymmetricProperty
prop irreflexive Proportion of owl:IrreflexiveProperty
prop reflexive Proportion of owl:ReflexiveProperty
prop transitive Proportion of owl:TransitiveProperty
prop functional Proportion of owl:FunctionalProperty
prop inversefunctional Proportion of owl:InverseFunctionalProperty
prop inverseof Proportion of owl:inverseOf
prop subproperties Proportion of rdfs:subPropertyOf
Individuals num entities Number of entities
num triples Number of triples
relation balance Relation distribution across triples
prop untyped Proportion of untyped entities
avg depth specific Average depth of most speciﬁc class
multityping Whether entities are multi-typed
avg multityping Average number of most-speciﬁc classes per entity
The schema generation follows a well-deﬁned series of steps. In particular, the
Class Generator in Fig. 1 is initialized ﬁrst, and generates the class hierarchy

10 N. Hubert et al.
and disjointness axioms as detailed in Algorithm 1. Then, the Relation Genera-
tor is initialized and handles the relation generation following the procedure of
Algorithm 2. In the following, each algorithm is described step by step.
Class Generation. First, classes are generated based on the user-speciﬁed
number of classes num
classes (lines 1–2). Then, the user-speciﬁed max depth
parameter is satisﬁed by taking one class after the other and creating child-
parent connections through the rdfs:subClassOf assertion (lines 3–7). At this
point, the class hierarchy is a purely vertical tree where each node (i.e., class) has
exactly one child, except the leaf node. The class hierarchy is then further ﬁlled
by taking each remaining class sequentially, and connecting it with other classes
so that avg
depth and inheritance ratio are satisﬁed (lines 8–13). It is worth
mentioning that with some probabilityα chosen to be moderately low, a freshly
picked class can be placed randomly (lines 10–11). This does not necessarily go
in the direction of avg
depth and inheritance ratio target parameters, but
it allows adding stochasticity and realism in the characteristics of the generated
class hierarchy. Besides, when a low number of classes are still to be connected,
this randomness is deactivated so that each subsequent class connection is in line
with avg
depth and inheritance ratio fulﬁlment. Finally, class disjointnesses
are added to the schema by picking two classes A and B, ensuring that none of
them is a transitive parent or child of the other, and extending class disjointness
to their respective children, if any (lines 14–16).
When generating classes, anomalies may occur. For instance, choosing values
such that avg
depth > max depth triggers an error. In a few other situations,
the schema is generated but the user requirements might not be completely
fulﬁlled. This can happen because of competing parameter values. For example,
the constraints num
classes =6( root excluded), max depth =3 , avg depth =
1.5, and inheritance ratio =2 .5 cannot be simultaneously satisﬁed (Fig. 2).
In this situation, the schema is generated with a best-eﬀort strategy, seeking to
build a schema with statistics as close as possible to the user requirements.
Relation Generation. Before presenting the procedure for generating rela-
tions and their properties, it is worth mentioning that PyGraft allows relations
to be described by multipleOWL and RDFS constructs. This leads to more realistic
schemas and KGs, at the expense of higher risk of inconsistency: some property
combinations are not logically consistent, e.g., a relation cannot be simulta-
neously qualiﬁed by owl:ReflexiveProperty and owl:IrreflexiveProperty.
Based on the relation properties available in PyGraft (Table 3), all combina-
tions were extracted and for each combination, a new graph was serialized using
rdflib7. This graph contains a unique relation which is qualiﬁed by the given
property combinations8. Based on the simpliﬁed schema, the HermiT reasoner
7 https://github.com/RDFLib/rdﬂib/.
8 An instance triple should also be added. This is because some property combinations
such as owl:SymmetricProperty and owl:AsymmetricProperty are not ﬂagged as
logically inconsistent per se in OWL. However, a relation qualiﬁed by these two prop-
erties is not allowed to connect any instances.

PyGraft: Conﬁgurable Generation of Synthetic Schemas and KGs 11
performs consistency checking. Finally, a dictionary stores all possible property
combinations. Knowing valid and invalid property combinations is necessary for
guiding relation property assignment and minimize logical inconsistency likeli-
hood before actually running the reasoner.
In Algorithm 2, this dictionary of valid property combinations is loaded
(line 3) just after initializing the number of relations speciﬁed by the user
(lines 1–2). Then, each relation in the schema is qualiﬁed with properties based
on a pre-deﬁned order (lines 4–6). For example, owl:ReflexiveProperty and
owl:IrreflexiveProperty are assigned ﬁrst, then owl:SymmetricProperty,
etc. These properties are named attributes as they characterize a relation per
se. Next, the relationship property owl:InverseOf is assigned to relations
(line 7), which poses constraints on relation domain and range assignments
(line 8), which themselves pose constraints on relation pairings through the
rdfs:subPropertyOf assertion (line 9), e.g., domain and range of subproperties
should not be disjoint with domain and range of superproperties.
In Table3 are reported the relation properties that the current PyGraft ver-
sion handles, along with their logical deﬁnition and accompanying examples.
Table 3. Relation properties covered by PyGraft.
Property Deﬁnition Example
owl:AsymmetricProperty ∀x∀y : p(x, y ) ⇒¬ p(y, x ) isParentOf
owl:SymmetricProperty ∀x∀y : p(x, y ) ⇒ p(y, x ) hasSibling
owl:ReflexiveProperty ∀x : p(x, x ) hasSameColorAs
owl:IrreflexiveProperty ∀x : ¬p(x, x ) isYoungerThan
owl:TransitiveProperty ∀x∀y∀z : p(x, y ) ∧ p(y, z ) ⇒ p(x, z ) isCheaperThan
owl:FunctionalProperty ∀x∀y∀z :( p(x, y ) ∧ p(x, z )) ⇒ y = z hasISBN
owl:InverseFunctionalProperty ∀x∀y∀z :( p(x, y ) ∧ p(z, y )) ⇒ x = z isEmailAddressOf
owl:InverseOf ∀x∀y : p(x, y ) ⇐⇒q(y, x ) owns ⇐⇒isOwnedBy
rdfs:subPropertyOf ∀x∀y : p(x, y ) ⇒ q(x, y ) hasMother ⇒ hasParent
3.4 Knowledge Graph Generation
In light of PyGraft overview (Fig.1), this section explores how the KG generator
is initialized with user parameters and used in conjunction with any generated
schema to build the ﬁnal KG. As for schema, we provide a step-by-step insight
into Algorithm 3. Entities and the KG are generated (lines 1–3) and a schema
dedicated to the KG generation is loaded (line 4). Based on prop
untyped,
entities are assigned a class whose depth in the class hierarchy should be in a
close range around avg
depth specific (line 5). Based on avg multityping,
several of them are assigned other classes of the same depth, provided that they
are not disjoint with any of the speciﬁc classes characterizing a given entity (lines
6–7). Then, triples are generated (lines 8–9) in a sequential manner. Namely,
unobserved entities in U have sampling priority, to ensure that the required
number of entities in the resulting KG is met as fully as possible. Ultimately,
checking procedures are performed (line 10) before the KG undergoes logical

12 N. Hubert et al.
root
C1
C2 C5C4 C6
root
C1 C6C4 C5
C2
C3 C3
root
C1
C2 C5C4
C6
C3
avg_depth=1.5
avg_inheritance=1.0
avg_depth=2.0
avg_inheritance=2.5
avg_depth=1.83
avg_inheritance=2.0
Fig. 2. Potential class hierarchies for the constraints:num classes =6 , max depth =3 ,
avg depth =1 .5, and inheritance ratio =2 .5. Left and middle class hierarchies
are built with parameter priority. The right class hierarchy is built with a best-eﬀort
strategy, without speciﬁc parameter privilege.
consistency checking using a semantic reasoner (line 11). If the generated KG is
inconsistent, a message warns the user but the KG is stored nevertheless. The
user can then choose to restart the generation procedure. It is worth mentioning
that the checking procedures (line 10) follow the relevantOWL 2 RL/RDF rules
9.
These rules – in the form of ﬁrst-order implications – are implemented in PyGraft
to ensure consistency pre-checking before the HermiT reasoner is deployed. In
addition, the OntOlogy Pitfall Scanner!
10 was also used for identifying several
checking procedures and for ensuring compliance with common Semantic Web
standards.
4 PyGraft in Action
4.1 Eﬃciency and Scalability Details
In this section, the eﬃciency and scalability of PyGraft are benchmarked across
several schema and graph conﬁgurations. Each schema speciﬁcation reported in
Table4 is paired with each graph speciﬁcation from Table 5. This leads to 27
distinct combinations.
In particular, schemas from S1t o S3 are small-sized, schemas from S4t o
S6 are medium-sized, and schemas from S7t o S9 are of larger sizes (Table 4).
For each schema of a given size, the degree of constraints vary as they contain
diﬀerent levels of OWL and RDFS logical constructs. For example,S1 has less con-
straints than S2, which itself has less constraints than S3. Graph speciﬁcations
G
1, G2,a n dG3 correspond to small-sized, medium-sized and large-sized graphs,
respectively (Table5).
9 https://www.w3.org/TR/owl2-proﬁles/#ref-owl-2-rdf-semantics/.
10 https://oops.linkeddata.es/.

PyGraft: Conﬁgurable Generation of Synthetic Schemas and KGs 13
Algorithm 1. Class Generation
1: Initialize the set of unconnected classes: U = {C1,C 2, ..., Cm}
2: Initialize the set of linked classes: L = ∅
3: C1 ← U.pop(), L.add(C1)
4: C1 rdfs:subClassOf root
5: while max depth is not satisﬁed do ⊿ Fulﬁlling class hierarchy depth
6: Ci ← U.pop(), L.add(Ci)
7: Ci rdfs:subClassOf Ci− 1
8: while U ̸= ∅ do ⊿ Building class hierarchy
9: Ci ← U.pop(), L.add(Ci)
10: if random(0, 1) ≤ α then ⊿ Adding stochasticity
11: Place it randomly
12: else
13: Place it s.t. avg
depth and inheritance ratio are satisﬁed
14: while current disj < disj ratio do ⊿ Adds owl:disjointWith
15: Pick classes A and B s.t. B is neither a parent nor a child of A
16: Make A and B disjoint and extend disjointness to their respective children
Algorithm 2. Relation Generation
1: Initialize the set of unqualiﬁed relations: U = {R1,R 2, ..., Rn}
2: Initialize the set of qualiﬁed relations: Q = ∅
3: Load compatible patterns
4: while U ̸= ∅ and attribute proportions not satisﬁed do ⊿ Adding attributes
5: R
i ← U.pop(), Q.add(Ri)
6: qualify(Ri) based on priority order
7: inverse pairing(Q) ⊿ Adding owl:inverseOf
8: relation profiling(Q) ⊿ Adding rdfs:domain/range
9: subproperty pairing(Q) ⊿ Adding rdfs:subPropertyOf
Algorithm 3. Knowledge Graph Generation
1: Initialize the set of unobserved entities: U = {E1,E 2, ..., Ep}
2: Initialize the set of observed entities: O = ∅
3: Initialize the knowledge graph: KG = ∅
4: Load the underpinning schema S
5: assign class(U) ⊿ Speciﬁc class attribution based on prop untyped
6: if multityping then
7: complete typing(U) ⊿ Adding speciﬁc classes based on avg multityping
8: while U ̸= ∅ and num triples not satisﬁed do
9: KG ← generate triples(U, O,S)
10: checking procedures(KG) ⊿ Removing foreseeable inconsistencies
11: reasoning(KG) ⊿ HermiT reasoner

14 N. Hubert et al.
For these 27 unique conﬁgurations, execution times w.r.t. several dimensions
are computed and shown in Fig. 3. Execution times related to the schema gen-
eration are omitted as they are negligible. Experiments were conducted on a
machine with 2 CPUs Intel Xeon E5-2650 v4, 12 cores/CPU, and 128GB RAM.
It is worth mentioning that the 27 generated KGs were ﬂagged as consistent
at the ﬁrst attempt. The breakdown of time executions diﬀers according to
the schema and graph sizes (see Fig. 3). For small graphs, the ﬁnal consistency
checking is the most time-consuming part. For large graphs, triple generation
time dominates the rest. As graph sizes increase, all execution times grow but
we observe that PyGraft is able to generate consistent KGs quickly, even for
large KGs: with our experimental conﬁguration, the total execution time for
KGs with 10K entities and 100K triples is roughly 1.5 min. In addition, PyGraft
scalability was assessed by asking a KG of 100K entities and 1M triples. On the
same machine, it took 47 min to generate such a KG, which was again consistent
at the ﬁrst attempt.
Table 4. Generated schemas. Column headers from left to right: number of classes,
class hierarchy depth, average class depth, proportion of class disjointness (cd), number
of relations, average depth of relation domains and ranges ( rs), and proportions of
reﬂexive (rf ), irreﬂexive (irr ), asymmetric (asy), symmetric (sy), transitive (tra), and
inverse (inv ) relations.
|C| MAX(D) AVG(D) cd |R| rs ref irr asy sym tra inv
S1 25 3 1.5 0.1 25 1.5 0.1 0.1 0.1 0.1 0.1 0.1
S2 25 3 1.5 0.2 25 1.5 0.2 0.2 0.2 0.2 0.2 0.2
S3 25 3 1.5 0.3 25 1.5 0.3 0.3 0.3 0.3 0.3 0.3
S4 100 4 2.5 0.1 100 2.5 0.1 0.1 0.1 0.1 0.1 0.1
S5 100 4 2.5 0.2 100 2.5 0.2 0.2 0.2 0.2 0.2 0.2
S6 100 4 2.5 0.3 100 2.5 0.3 0.3 0.3 0.3 0.3 0.3
S7 250 5 3.0 0.1 250 3.0 0.1 0.1 0.1 0.1 0.1 0.1
S8 250 5 3.0 0.2 250 3.0 0.2 0.2 0.2 0.2 0.2 0.2
S9 250 5 3.0 0.3 250 3.0 0.3 0.3 0.3 0.3 0.3 0.3
Table 5. Diﬀerent graph speciﬁcations. Column headers from left to right: number of
entities, number of triples, proportion of untyped entities, average depth of the most
speciﬁc class, average number of most-speciﬁc classes per multi-typed entity.
|E| |T | unt asc mul
G1 100 1, 000 0.3 2.0 2.0
G2 1, 000 10, 000 0.3 2.0 2.0
G3 10, 000 100, 000 0.3 2.0 2.0

PyGraft: Conﬁgurable Generation of Synthetic Schemas and KGs 15
Fig. 3. Execution time breakdown for each conﬁguration.
4.2 Usage Illustration
In this section, we brieﬂy provide some usage examples to demonstrate how
easy it is to use PyGraft. Desired characteristics of the output schema and/or
KG can be speciﬁed with the path to a yaml or json conﬁguration ﬁle. In the
example presented in Listing 1.1, after importing PyGraft, we ﬁrst generate a
yaml conﬁguration ﬁle in the current working directory. For the sake of simplicity,
the generated template is left untouched, i.e., we keep the default parameter
values. More advanced usage is provided in the oﬃcial documentation:https://
pygraft.readthedocs.io/en/latest/. Then, we generate both a schema and KG in
a single pipeline. The generated resources are subsequently stored in the current
working directory.
import pygraft
pygraft. create_yaml_template()
pygraft.generate( "template.yml" )
Listing 1.1. Schema and KG generation with PyGraft.
By default, the generated graph is stored as an rdf/xml ﬁle. A snippet of a
KG generated with PyGraft is provided in Listing 1.2.
<?xml version="1.0" encoding="utf-8"? >
<rdf:RDF
xmlns:ns1="http://purl.org/dc/terms/"
xmlns:owl="http://www.w3.org/2002/07/owl#"
xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
xmlns:rdfs="http://www.w3.org/2000/01/rdf-schema#"
xmlns:sc="http://pygraf.t/"
>
<rdf:Description rdf:about="http://pygraf.t/C30">
<rdf:type rdf:resource="http://www.w3.org/2002/07/owl#Class"/>
<rdfs:subClassOf rdf:resource="http://www.w3.org/2002/07/owl#Thing"/>
<owl:disjointWith rdf:resource="http://pygraf.t/C16"/>
</rdf:Description>
<rdf:Description rdf:about="http://pygraf.t/E324">

16 N. Hubert et al.
<rdf:type rdf:resource="http://pygraf.t/C4"/>
<rdf:type rdf:resource="http://pygraf.t/C17"/>
<schema:R15 rdf:resource="http://pygraf.t/E356"/>
<schema:R34 rdf:resource="http://pygraf.t/E44"/>
</rdf:Description>
<rdf:Description rdf:about="http://pygraf.t/R34">
<rdf:type rdf:resource="http://www.w3.org/2002/07/owl#ObjectProperty"/>
<rdf:type rdf:resource="http://www.w3.org/2002/07/owl#TransitiveProperty"/>
<rdfs:domain rdf:resource="http://pygraf.t/C17"/>
<rdfs:range rdf:resource="http://pygraf.t/C17"/>
<owl:inverseOf rdf:resource="http://pygraf.t/R15"/>
</rdf:Description>
Listing 1.2. Excerpt from a generated graph.
5 Discussion
5.1 Potential Uses
As mentioned, PyGraft can be used for generating several schemas and KGs
on the ﬂy, thereby facilitating novel approaches and model benchmarking on a
wider range of datasets with diversiﬁed characteristics. In practice, this can be
easily done with inspecting the conﬁguration ﬁle we provide as template, and
tweaking parameters as one sees ﬁt.
Additionally, PyGraft can be used for generating anonymous data. Let us
assume one is working in a data-sensitive ﬁeld such as medicine or education,
characterized by the paucity of readily available data. Thanks to PyGraft, it
becomes much more accessible to experiment with sensitiveless testbeds, pro-
vided that the user has a rough idea of the scale and characteristics of the
resources they want to mimic.
It is worth noting that a vibrant research community aims at incorporating
schema-based information into the learning process with KGs [ 6,19,20]. Using
information derived from the schema in addition to the facts contained in the KG
aims at building more semantic-aware approaches [17], that are expected to result
in more coherent predictions [18] and better predictive accuracy [6,17]. However,
it is frequently reported that most KGs do not come with publicly available
schemas that would facilitate the development of such schema-aware approaches.
For this reason, PyGraft may also be helpful to generate both synthetic schemas
with dependent KGs to foster the development of schema-driven, neuro-symbolic
approaches, and to run ablation studies on speciﬁc schema constructs in isolation.
5.2 Limitations, Sustainability, Maintenance and Future Work
In this section, we discuss the current limitations of PyGraft and elaborate on
our sustainability and maintenance plan, as well as future work opportunities.
First, it should be noted that PyGraft relies onrdflib for serializing triples.
As part of supplementary experiments, we tried to push PyGraft capabilities
to its limit by generating very large KGs with >10M entities and triples. In

PyGraft: Conﬁgurable Generation of Synthetic Schemas and KGs 17
such cases, the serialization failed. In future work, we will develop independent
serialization procedures so that bigger graphs can be generated.
Secondly, recall that our implemented checking procedures limit the likeli-
hood of any inconsistency before the DL reasoner is ultimately applied on the
generated KG. In case of inconsistencies that would remain undetected by the
checking procedures, our actual use of the HermiT reasoner is able to detect such
inconsistencies, but not to provide any information on the triples that should be
removed so that the KG becomes consistent. In future work, we will implement
such a functionality, so that the consistency of the generated KGs can be ensured
in a single loop without requiring any input from the user’s side.
More generally, we aim at maintaining the PyGraft library, a cornerstone
in our commitment to robust software engineering practices and open-source
community engagement. Our approach is to release new versions in response to
emerging user requirements, ensuring that PyGraft not only meets but antic-
ipates the needs of its users. For instance, a common request is the ability to
generate literals – which we seek to achieve in the near future. Furthermore, we
recently welcomed the suggestion of oﬀering a hub that would gather diﬀerent
KG proﬁles generated by the community. To this aim, we welcome all contribu-
tions on Github (e.g.,, issues, forks, or pull requests) to make PyGraft useful to
researchers of a large array of communities. We are dedicated to incorporating
methodologies for continuous integration and deployment, fostering a test-driven
development environment that guarantees reliability and eﬃciency. We also want
PyGraft to ﬁt within the Semantic Web community and be recognized as a useful
tool for researchers and engineers working on KG-based applications.
In future work, we will showcase the impact of PyGraft in real-world use
cases. Some relevant scenarios include recommender systems and ontology repair-
ment. In particular, for the latter use-case, we envision the creation of voluntarily
imperfect schemas, containing (known) contradictions to resolve. Link prediction
also appears as an appropriate task to evaluate PyGraft’s usefulness.
6 Conclusion
In this work, we presented PyGraft, a Python tool for generating synthetic
schemas and KGs from user requirements. Several OWL and RDFS constructs are
integrated to output realistic KGs that comply with Semantic Web standards.
PyGraft allows researchers and practitioners to generate schemas and KGs on
the ﬂy, provided minimal knowledge about the desired speciﬁcations. Hence,
PyGraft can prove useful for various applications. As it allows for generating
schemas and KGs of controlled characteristics, it can serve as a well-suited tool
for benchmarking novel approaches or models. Being domain-agnostic, PyGraft
can be used to generate synthetic schemas and KGs resembling real ones in data-
sensitive ﬁelds where access or publication of public data is scarce. Due to the
richly described generated KGs in terms of OWL and RDFS constructs, PyGraft
may also facilitate the development of schema-driven, neuro-symbolic models.

18 N. Hubert et al.
References
1. Albert, R., Barab´asi, A.L.: Statistical mechanics of complex networks. Rev. Mod.
Phys. 74, 47–97 (2002). https://doi.org/10.1103/RevModPhys.74.47
2. Angles, R., et al.: The linked data benchmark council: a graph and RDF industry
benchmarking eﬀort. SIGMOD Rec.43(1), 27–31 (2014).https://doi.org/10.1145/
2627692.2627697
3. Bagan, G., Bonifati, A., Ciucanu, R., Fletcher, G.H.L., Lemay, A., Advokaat, N.:
gMark: schema-driven generation of graphs and queries. IEEE Trans. Knowl. Data
Eng. 29(4), 856–869 (2017). https://doi.org/10.1109/TKDE.2016.2633993
4. Bonatti, P.A., Decker, S., Polleres, A., Presutti, V.: Knowledge graphs: new direc-
tions for knowledge representation on the semantic web (Dagstuhl seminar 18371).
Dagstuhl Rep. 8(9), 29–111 (2018). https://doi.org/10.4230/DagRep.8.9.29
5. Chakrabarti, D., Zhan, Y., Faloutsos, C.: R-MAT: a recursive model for graph
mining. In: Proceedings of the Fourth SIAM International Conference on Data
Mining, Lake Buena Vista, Florida, USA, 22–24 April 2004, pp. 442–446. SIAM
(2004). https://doi.org/10.1137/1.9781611972740.43
6. d’Amato, C., Quatraro, N.F., Fanizzi, N.: Injecting background knowledge into
embedding models for predictive tasks on knowledge graphs. In: Verborgh, R.,
et al. (eds.) ESWC 2021. LNCS, vol. 12731, pp. 441–457. Springer, Cham (2021).
https://doi.org/10.1007/978-3-030-77385-4
26
7. De Cao, N., Kipf, T.: MolGAN: an implicit generative model for small molecular
graphs. In: ICML 2018 Workshop on Theoretical Foundations and Applications of
Deep Generative Models (2018)
8. Dettmers, T., Minervini, P., Stenetorp, P., Riedel, S.: Convolutional 2D knowl-
edge graph embeddings. In: Proceedings of the Thirty-Second AAAI Conference
on Artiﬁcial Intelligence, (AAAI-18), the 30th Innovative Applications of Artiﬁcial
Intelligence (IAAI-18), and the 8th AAAI Symposium on Educational Advances
in Artiﬁcial Intelligence (EAAI-18), New Orleans, Louisiana, USA, 2–7 February
2018, pp. 1811–1818. AAAI Press (2018)
9. Ehrlinger, L., W¨oß, W.: Towards a deﬁnition of knowledge graphs. In: Joint Pro-
ceedings of the Posters and Demos Track of the 12th International Conference
on Semantic Systems - SEMANTiCS2016 and the 1st International Workshop on
Semantic Change & Evolving Semantics (SuCCESS’16) co-located with the 12th
International Conference on Semantic Systems (SEMANTiCS 2016), Leipzig, Ger-
many, 12–15 September 2016. CEUR Workshop Proceedings, vol. 1695. CEUR-
WS.org (2016)
10. ERDdS, P., R&wi, A.: On random graphs I. Publ. math. debrecen 6(290-297), 18
(1959)
11. Feng, Z., et al.: A schema-driven synthetic knowledge graph generation approach
with extended graph diﬀerential dependencies (gdd
xs). IEEE Access 9, 5609–5639
(2021). https://doi.org/10.1109/ACCESS.2020.3048186
12. Glimm, B., Horrocks, I., Motik, B., Stoilos, G., Wang, Z.: Hermit: an OWL 2 rea-
soner. J. Autom. Reason. 53(3), 245–269 (2014). https://doi.org/10.1007/s10817-
014-9305-1
13. Goyal, N., Jain, H.V., Ranu, S.: GraphGen: a scalable approach to domain-agnostic
labeled graph generation. In: WWW 2020: The Web Conference 2020, Taipei,
Taiwan, 20–24 April 2020, pp. 1253–1263. ACM/IW3C2 (2020). https://doi.org/
10.1145/3366423.3380201

PyGraft: Conﬁgurable Generation of Synthetic Schemas and KGs 19
14. Gruber, T.R.: Toward principles for the design of ontologies used for knowledge
sharing? Int. J. Hum Comput Stud. 43(5–6), 907–928 (1995). https://doi.org/10.
1006/ijhc.1995.1081
1 5 . G u o ,Y . ,P a n ,Z . ,H e ﬂ i n ,J . :L U B M :ab e n c h m a r kf o rO W Lk n o w l e d g eb a s es y s t e m s .
J. Web Semant. 3(2–3), 158–182 (2005). https://doi.org/10.1016/j.websem.2005.
06.005
16. Hogan, A., et al.: Knowledge Graphs. Synthesis Lectures on Data, Semantics,
and Knowledge, Morgan & Claypool Publishers (2021). https://doi.org/10.2200/
S01125ED1V01Y202109DSK022
17. Hubert, N., Monnin, P., Brun, A., Monticolo, D.: Enhancing knowledge graph
embedding models with semantic-driven loss functions. CoRR abs/2303.00286
(2023). https://doi.org/10.48550/arXiv.2303.00286
18. Hubert, N., Monnin, P., Brun, A., Monticolo, D.: Sem@k: is my knowledge graph
embedding model semantic-aware? CoRR abs/2301.05601 (2023).https://doi.org/
10.48550/arXiv.2301.05601
19. Hubert, N., Paulheim, H., Monnin, P., Brun, A., Monticolo, D.: Schema ﬁrst! learn
versatile knowledge graph embeddings by capturing semantics with machine. CoRR
abs/2306.03659 (2023). https://doi.org/10.48550/arXiv.2306.03659
20. Jain, N., Tran, T.K., Gad-Elrab, M.H., Stepanova, D.: Improving knowledge graph
embeddings with ontological reasoning. In: Hotho, A., et al. (eds.) ISWC 2021.
LNCS, vol. 12922, pp. 410–426. Springer, Cham (2021). https://doi.org/10.1007/
978-3-030-88361-4
24
21. Jin, L., Yao, Z., Chen, M., Chen, H., Zhang, W.: A comprehensive study on knowl-
edge graph embedding over relational patterns based on rule learning (2023)
22. Liu, S., Grau, B.C., Horrocks, I., Kostylev, E.V.: Revisiting inferential benchmarks
for knowledge graph completion. CoRR abs/2306.04814 (2023).https://doi.org/10.
48550/arXiv.2306.04814
23. Melo, A., Paulheim, H.: Synthesizing knowledge graphs for link and type prediction
benchmarking. In: Blomqvist, E., Maynard, D., Gangemi, A., Hoekstra, R., Hitzler,
P., Hartig, O. (eds.) ESWC 2017. LNCS, vol. 10249, pp. 136–151. Springer, Cham
(2017). https://doi.org/10.1007/978-3-319-58068-5
9
24. Palowitch, J., Tsitsulin, A., Mayer, B., Perozzi, B.: GraphWorld: fake graphs bring
real insights for GNNs. In: KDD 2022: The 28th ACM SIGKDD Conference on
Knowledge Discovery and Data Mining, Washington, DC, USA, 14–18 August
2022, pp. 3691–3701. ACM (2022). https://doi.org/10.1145/3534678.3539203
25. Park, H., Kim, M.: Trilliong: a trillion-scale synthetic graph generator using a
recursive vector model. In: Proceedings of the 2017 ACM International Conference
on Management of Data, SIGMOD Conference 2017, Chicago, IL, USA, 14–19 May
2017, pp. 913–928. ACM (2017). https://doi.org/10.1145/3035918.3064014
26. Portisch, J., Paulheim, H.: The DLCC node classiﬁcation benchmark for analyzing
knowledge graph embeddings. In: Sattler, U., et al. (eds.) ISWC 2022. LNCS, vol.
13489, pp. 592–609. Springer, Cham (2022). https://doi.org/10.1007/978-3-031-
19433-7
34
27. Rossi, A., Firmani, D., Merialdo, P., et al.: Knowledge graph embeddings or bias
graph embeddings? A study of bias in link prediction models. In: CEUR Workshop
Proceedings, vol. 3034. CEUR-WS (2021)
28. Rossi, A., Matinata, A.: Knowledge graph embeddings: are relation-learning mod-
els learning relations? In: Proceedings of the Workshops of the EDBT/ICDT 2020
Joint Conference, Copenhagen, Denmark, 30 March 2020. CEUR Workshop Pro-
ceedings, vol. 2578. CEUR-WS.org (2020)

20 N. Hubert et al.
29. Samanta, B., et al.: NEVAE: a deep generative model for molecular graphs. J.
Mach. Learn. Res. 21, 114:1–114:33 (2020)
30. Simonovsky, M., Komodakis, N.: GraphVAE: towards generation of small graphs
using variational autoencoders. In: Kurkova, V., Manolopoulos, Y., Hammer, B.,
Iliadis, L., Maglogiannis, I. (eds.) ICANN 2018. LNCS, vol. 11139, pp. 412–422.
Springer, Cham (2018). https://doi.org/10.1007/978-3-030-01418-6 41
31. Wang, H., et al.: GraphGAN: graph representation learning with generative adver-
sarial nets. In: Proceedings of the Thirty-Second AAAI Conference on Artiﬁcial
Intelligence, (AAAI-18), the 30th innovative Applications of Artiﬁcial Intelligence
(IAAI-18), and the 8th AAAI Symposium on Educational Advances in Artiﬁcial
Intelligence (EAAI-18), New Orleans, Louisiana, USA, 2–7 February 2018, pp.
2508–2515. AAAI Press (2018)
32. You, J., Ying, R., Ren, X., Hamilton, W.L., Leskovec, J.: GraphRNN: generat-
ing realistic graphs with deep auto-regressive models. In: Proceedings of the 35th
International Conference on Machine Learning, ICML 2018, Stockholmsm¨assan,
Stockholm, Sweden, 10–15 July 2018. Proceedings of Machine Learning Research,
vol. 80, pp. 5694–5703. PMLR (2018)

NORIA-O: An Ontology for Anomaly
Detection and Incident Management
in ICT Systems
Lionel Tailhardat1,2(B) , Yoan Chabot3 , and Raphael Troncy2
1 Orange, Paris, France
lionel.tailhardat@orange.com
2 EURECOM, Sophia Antipolis, Biot, France
3 Orange, Belfort, France
Abstract. Large-scale Information and Communications Technology
(ICT) systems give rise to diﬃcult situations such as handling cascading
failures and detecting complex malicious activities occurring on multiple
services and network layers. For network supervision, managing these sit-
uations while ensuring the high-standard quality of service and security
requires a comprehensive view on how communication devices are inter-
connected and are performing. However, the information is spread across
heterogeneous data sources which triggers information integration chal-
lenges. Existing data models enable to represent computing resources and
how they are allocated. However, to date, there is no model to describe
the inter-dependencies between the structural, dynamic, and functional
aspects of a network infrastructure. In this paper, we propose the NORIA
ontology that has been developed together with network and cybersecu-
rity experts in order to describe an infrastructure, its events, diagnosis
and repair actions performed during incident management. A use case
describing a ﬁctitious failure shows how this ontology can model complex
situations and serve as a basis for anomaly detection and root cause anal-
ysis. The ontology is available at https://w3id.org/noria and empowers
the largest telco operator in France.
Keywords: Ontology
· Network Supervision · Incident Management ·
Network Infrastructure · NORIA
1 Introduction
When managing large-scale IT & telco networks (broadband international back-
bones, corporate networks, Internet access networks), one is sooner or later
involved into handling complex incident situations, such as general IT ser-
vice disruption because of cascading failures or cyber-attacks. Incident man-
agement teams rely on decision support tools like Network Monitoring Sys-
tems (NMSs) [25,43] or Security Information and Event Management systems
(SIEMs) [26]. These tools often use an elementary representation of the network
c⃝ The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
A. Mero˜no Pe˜nuela et al. (Eds.): ESWC 2024, LNCS 14665, pp. 21–39, 2024.
https://doi.org/10.1007/978-3-031-60635-9_2

22 L. Tailhardat et al.
infrastructures and services. Basically, an IT network is a set of computers,
routers, and other devices connected and conﬁgured to allow data processing
and sharing. Similarly, an IT service is the usage of this processing and shar-
ing capability for speciﬁc purposes, from the most trivial ones (entertainment,
ticket booking, home automation) to more challenging ones (stock exchange,
road lights, or nuclear plant management). Although obvious at ﬁrst glance,
this level of description is not suﬃcient to scale up for maintaining high-standard
quality of service on large-scale networks. This is due to the heterogeneity of the
Information and Communications Technology (ICT) systems that compose them
and the interdependencies between services and infrastructure: incident diagno-
sis and remediation is a challenging task as supervision teams must deal with
multiple technologies, technical characteristics, monitoring systems, and stake-
holders in siloed organizations. For example, one can consider a service archi-
tecture that combines virtual machines (VMs) distributed across data centers,
which are interconnected through an IPoDWDM
1 network. To achieve eﬃciency,
it is necessary to integrate and correlate data from various sources. This includes
data from VM management tools, Optical Transport Network (OTN) layer man-
agement tools (which may be managed by a third-party operator), information
about scheduled operations, and contact details for local servicing teams.
To tackle these cross-domain data interpretation and incident management
challenges, we argue that a graph-based explicit knowledge representation would
help capturing complex network situations (e.g. discrepancy of routing metrics
with respect to an engineering rule, lack of redundancy in a distributed service)
and reasoning on them (e.g. inventory list to scrutinize further, cause and remedia-
tion procedure search). Our main contribution in this regard is the NORIA Ontol-
ogy (NORIA-O) for representing network infrastructures, incidents and opera-
tions on networks. This ontology re-uses and extends well-known ontologies such
as SEAS [38,39], FOLIO [9], UCO [62], ORG [14], BOT [31] and BBO [ 2]. It
also includes controlled vocabularies for handling data from various ICT systems
and incident situations through a small set of shareable deﬁnitions. NORIA-O
has been developed within the Orange
2 company, a leading international network
infrastructure and service provider. Its long-standing experience on complex net-
work management allows us to back NORIA-O with insightful details from domain
experts and to evaluate the model with real-world data. In addition, NORIA-O
has also been successfully used in a knowledge graph construction pipeline in an
industrial setting [30] and for capturing and classifying incident contexts using
graph embeddings [28]. The ontology, controlled vocabularies and their associated
documentation are available athttps://w3id.org/noria.
The remainder of this paper is organized as follows. In Sect. 2, we review
RDF-based and non-RDF based data models enabling to represent network
infrastructures and incidents. In Sect. 3, we describe the methodology we fol-
low to design NORIA-O, starting from competency questions that capture the
knowledge of experts. In Sect.4, we deep dive into the diﬀerent concepts as well
as into the associated vocabularies. We evaluate the ontology with respect to our
1 Internet Protocol over Dense Wave Division Multiplexing [19].
2 https://www.orange.com/.

NORIA-O: An Ontology for Monitoring ICT Systems 23
requirements and competency questions in Sect. 5. We exemplify how NORIA-
O is used for the supervision of a network infrastructure in Sect. 6. Finally, we
conclude and outline some future work in Sect.7.
2 Related Work
Previous works have demonstrated that the use of semantic modeling is of interest
for network infrastructure monitoring (e.g. INDL [37], CRATELO [1], UCO [62],
ToCo [48], ACCTP [10], DevOpsInfra [42]). Several tools have also been proposed
to facilitate the construction and utilization of knowledge graphs in diﬀerent areas.
These include RMLMapper [3] for data integration, SLOGERT [4] for log pars-
ing and semantization, String2Vocabulary [44] for vocabulary reconciliation, and
KG Explorer [55] and Gephi [36] for visualization purposes. We posit that these
works partly cover the knowledge domains required for describing ICT systems
and related activities (e.g. incident management, cybersecurity risk evaluation).
For example, the combination of the SEAS and PEP [38,39]m o d e l si su s e f u lf o r
describing technological systems, commands and observed values from probing
devices. However, SEAS mostly targets the IoT domain and end-user devices, and
the semantics of PEP relates to computer process. The DevOpsInfra [42] ontol-
ogy describes sets of computing resources and how they are allocated for hosting
services. However, concepts are missing for a ﬁner grain description of the net-
work topology. Moreover, the ontology mostly focuses on the provisioning activ-
ity and is not aligned with other well-known models such as SOSA [27] and the
TMForum Open API
3 for interoperable deﬁnitions of states and operations. The
CRATELO [1] model enables describing and reasoning on cyber-operations. Used
in combination with the PACO [41] model, reasoning on network traﬃc from the
defenders’ and attackers’ perspective is possible. However, concepts for network
topology and operations are missing for contextualizing network traﬃc sessions
within the network topology itself and the day-to-day operations.
In this paper, we aim to ﬁll this gap in developing a comprehensive semantic
model for describing and reasoning on the combination of network infrastructure
characteristics (e.g. device type, links), network activity (e.g. user login, interface
status change, processor overload alert) and operations (e.g. software upgrade,
server reboot, link decommissioning). Based on various selection criteria, such
as the coverage of our target knowledge domain and the enrichment of existing
ontologies, we design NORIA-O so that it builds upon some of these existing
semantic models as described in Sect. 3.
3 Methodology
In this section, we describe the knowledge engineering methodology we used
to develop NORIA-O. First, we capture Competency Questions (CQs) from a
panel of experts familiar with network operation issues and derive archetypes
from these CQs for further analysis (Sect.3.1). Second, we show how we designed
the conceptual model (Sect. 3.2).
3 https://github.com/tmforum-apis.

24 L. Tailhardat et al.
3.1 Competency Questions and Conceptualization
We gathered experts from several entities in the ﬁelds of engineering, operations,
supervision, and incident management on networks and data centers, including
teams from Network Operation Centers (NOCs) and Security Operation Centers
(SOCs). This panel consists of 16 experts who collectively represent 150 oper-
ations team members. To eﬀectively capture the knowledge of the experts, we
followed a user-centered design methodology combined with ontology engineer-
ing methods. From our review of the literature, the Competency Question app-
roach [61] turns out to be the most intuitive and straightforward with respect to
how NOC and SOC teams use and talk about their tools. Indeed, this approach
involves extracting the conceptual model of the knowledge domain by analyzing
user queries expressed in natural language through a set of semantic patterns.
During several iterations of knowledge capture meetings on a shared notebook,
the experts could validate, invalidate, add and modify Competency Questions
(CQs). At the end of this stage, the teams validated 26 CQs presented in Table1.
This includes questions on events, resources (e.g. server, router), applications
(e.g. Domain Name System, Video-on-Demand platform), log and alarms (e.g.
login, CPU overload) and operation plan (e.g. SSL/TLS certiﬁcate renew, IS-IS
interface re-prioritization).
From the set of CQs, we derived a conceptual model of the domain of dis-
course by applying the “Competency Question archetype mapping ” approach [61,
§4.3]. For example, CQ#1 can be mapped to the “Which [CE1] [OPE] [CE2]? ”
archetype (ID: 1), yielding to breaking down the competency question into the
following components: CE 1 = Asset (resource/application/site), OP E =a r e -
ContainedIn, and CE 2 = Incident. We also adhered to the guidelines of the
Linked Open Terms (LOT) methodology [33], which notably include reusing or
aligning with existing vocabularies.
Upon scrutinizing the conceptual model and candidate vocabularies, two
characteristics are observed. Firstly, concepts derived from the Table 1 can be
referred to as “atomic concepts” (e.g. application, alarm, resource), representing
concepts that are not deﬁned by composition but are considered indivisible in
nature. Thus, we can expect to use simple relationships (potentially hierarchical)
between concepts during the modeling and implementation phases. Secondly,
research domains related to ICT systems management (such as event spread-
ing [32], software engineering [16], knowledge management, and automated rea-
soning [7]), exhibit abstract concepts common to these domains and the NORIA-
O ﬁeld, such as physical vs functional and cause vs consequence . Therefore, we
suggest structuring the NORIA-O domain concepts using similar facets to lever-
age the approaches and tools applicable in these research domains, such as ﬁnite
state automatons and Markov decision processes. For instance, combining the
facets allows for a comprehensive analysis of the complexity and observability lev-
els of networks, which we refer to as a hybrid “concrete-conceptual” model [29].
In this model, assets’ states dynamically vary based on behavioral rules and are
interpreted through higher-level composite concepts. Consequently, predicting

NORIA-O: An Ontology for Monitoring ICT Systems 25
the next set of states/concepts becomes a sequential decision under uncertainty
problem. We further deﬁne these facets in the next section.
Table 1. NORIA-O Competency Questions (CQs). In this table, we list the NORIA-O CQs
collected during knowledge capture meetings (Sect. 3.1), along with their corresponding archetype
(Arch. ID, as deﬁned in [ 61, §4.3]) and authoring tests results (Sect. 5, with the number of imple-
mented queries for the evaluation stage). Facets (Sect. 3.2): S = structural, F = functional, D =
dynamic, and P = procedural.
# CQs Facets Arch. ID AT Eval.
1 Which resource/application/site is concerned by a given incident? S, F, D 1 OK (4)
2 What assets are shared by a given asset chain? S, F 6 OK (1)
3 What logs and alarms are coming from a speciﬁed resource? S, D 1 OK (1)
4 Which metrics are coming from a speciﬁed resource? S 1 OK (1)
5 To which event family does this log belong and is this event normal or
abnormal?
D, P 3 OK (1)
6 What events are associated with a given event? D 1 OK (1)
7 Which agent/event/resource caused the event under analysis? S, F, D, P 1 OK (3)
8 What do the various ﬁelds in the log refer to? D 1, 3 OK (1)
9 Is there any pattern in a given set of logs/alarms? D, P 1, 6 AI (1)
10 What interventions were carried out on this resource that could have caused
the incident?
S, D, P 1, 6 OK (2)
11 What was the root cause of the incident? D, P 6 AI (1)
12 Which sequence of events led to the incident? D, P 6 OK (1)
13 On which resource did this sequence of events take place and in which order? S, D 1 OK (1)
14 What past incidents are similar to a given incident? D, P 6 AI (1)
15 What operation plan (automation, operating procedures, etc.) could help us
solve the incident?
D, P 1, 3 AI (1)
16 What corrective actions have been carried out so far for a given incident? D, P 1 OK (1)
17 What is the list of actions taken that led to the resolution of the incident? D, P 1 OK (1)
18 Given all the corrective actions carried out so far for the incident, what
assumptions covered the actions taken?
D, P 1, 4 AI (1)
19 What has been the eﬀect of the corrective actions taken so far for the incident? D, P 1 OK (1)
20 Given all the corrective actions carried out so far for the incident, what
possible actions could we still take?
D, P 6 AI (1)
21 What is the summary of this incident and its resolution? D 1 OK (1)
22 Which agents were involved in the resolution of the incident? D 1 OK (1)
23 What is the ﬁnancial cost of this incident if it occurs? D 2 Ext.
24 How long before this incident is resolved? D 1 AI (1)
25 What are the vulnerabilities and the associated risk levels of this
infrastructure?
S, F, D 1, 2 AI (1)
26 What is the most likely sequence of actions that would cause this
infrastructure to fail?
S, F, P 6 AI (1)
3.2 Domain of Discourse and Modeling Strategy
Facets. Considering dynamic ICT systems with constrained and multi-level func-
tional behavior, we deﬁne the four following facets for structuring the knowledge
domain. An illustration of these facets is provided in Fig.1.
– The structural facet describes the physical and logical elements of the
network. It allows modeling the equipment classes, connections and com-
positions. This facet aims to support calculations on network objects and

26 L. Tailhardat et al.
Fig. 1. ICT system state transition model and relations to the NORIA-O facets. The
representation of a network can be divided into four facets: structural, functional (the blue path
indicates an operational data ﬂow, the red path a faulty ﬂow), dynamic,a n d procedural (logged
events are related to cyber-security attack tactics from the MITRE ATT&CK matrix [ 45]). Ta u
stands for state transition, O(t) for observed state at time t,a n d p for state prediction. (Color
ﬁgure online)
properties (direct or deduced) and calculations on the physical and logical
structures (real or patterns).
– The functional facet describes services provided and diﬀusion areas. This
facet makes it possible to meet the need for functional isomorphism (e.g. replac-
ing one equipment with another performing the same function). It allows mod-
eling the service types, interactions between them, and compositions. This
facet allows calculations on network domains and their properties (direct or
inferred) and calculations on services and streams (e.g. “end-to-end” notion).
– The dynamic facet describes the sequence of events. It allows modeling the
occurrence of an event on a given equipment or service as well as precedence
relationships. This facet aims to support time calculations (absolute, relative,
membership) and causality calculations (ﬁrst order or probabilistic).
– The procedural facet describes how things work and should be interpreted.
Automation principles (e.g. fail-over mechanisms of redundant systems) or
operation principles (e.g. doubt removal procedures) are expected parts of this
facet. Associated application goals are deductive/abductive reasoning over
facts and reﬂection over knowledge for automated learning (discovery/rec-
ommendation) of procedures (e.g. evolutionary search over targeted goals,
composition calculus over sequences of events).
Modeling strategy. Considering the domains of anomaly detection and incident
management, we consider incidents as a central concept for i) computing and
reasoning about anomaly signatures, and ii) linking trouble tickets to anomaly
signatures for root cause analysis tasks. We introduce the noria namespace,
which encompasses the entire set of NORIA-O concepts and relations in a uniﬁed
manner. To align with risk management and business modeling practices (such as

NORIA-O: An Ontology for Monitoring ICT Systems 27
the incident logging and categorization steps in the ITIL’s Incident Management
Process model – IMP [53]), we adopt a top-to-bottom modeling strategy, starting
from the process and extending to objects. Due to the “atomic concepts” char-
acteristic of the knowledge domain (Sect.3.1) and our top-to-bottom approach,
we primarily focus on an axiomatization based on subsumption with RDFS [13],
and with OWL [50] for cases that require additional logical structuring (e.g. class
disjointness, property qualiﬁcation)4.
Model re-use. Following the best practices in ontology development, we aim
to re-use existing data models and vocabularies as a base and extend them to
represent domain-speciﬁc classes and properties. From RDF-based ontologies,
we interconnect and/or extend the following models: BBO [2] for describing
activities from the business process modeling perspective in conformance to the
Business Process Model Notation (BPMN); BOT [31] for describing resource
locations and enabling geographical neighboring analysis for root cause analysis
tasks; DCTERMS for standard management of NORIA-O instances as parts
of a catalog; DevOpsInfra [42] for enabling potential interactions of NORIA-O
with the DevOps perspective; FOAF [12] for describing social organizations;
FOLIO [9] for enabling Root Cause Analysis (RCA) tasks based on the Failure
Mode and Eﬀect Analysis (FMEA) approach; ORG [14] for describing stake-
holders and related organizations; SEAS & PEP [38,39] for describing tech-
nological systems, measures, commands, and results; UCO [62] for enabling
cyber-security risk assessment on instances of NORIA-O; SLOGERT [4]f o r
describing system logs and enabling potential usage of the SLOGERT log inter-
pretation framework.
From non RDF-based data models, we take advantage of the concept hier-
archy and vocabulary deﬁnitions from the TMForum Data Model
5 for
enabling an interoperable deﬁnition of trouble tickets and change requests with
third-party Operations Support Systems (OSSs) and Decision Support Systems
(DSSs), ITU-T [20,21] for standard deﬁnitions of notiﬁcations and ways to
handle them within the telecommunication industry, IETF for precise use of
terminology in the context of a Request for Comments (RFC)6.
We propose implementing alignment with third-party data models and
vocabularies on a class or property basis when relevant, using the dedicated
OWL and RDF constructs such as owl:equivalentClass, rdfs:subClassOf,
or rdfs:isDefinedBy. Similarly, we aim to provide guidelines for directly instan-
tiating these vocabularies in cases where aligning a class or property would be
redundant.
Modeling observations. Considering observables and their state change (e.g. the
operational state of a network interface, the temperature measurements from
4 During implementation, cardinality restrictions were not prioritized as they were
not considered crucial. Instead, we see cardinality restrictions as more beneﬁcial for
post-implementation data quality tasks using SHACL [17].
5 https://github.com/tmforum-apis.
6 https://datatracker.ietf.org/.

28 L. Tailhardat et al.
a sensor), we observe that modeling and logging observations can be done: (a)
as a string, (b) as a concept from a controlled vocabulary, (c) as an instance,
(d) as an instance with time property or time instance (e.g. using reiﬁcation,
or following the sosa:Observation model
7). These four options are relevant for
the NORIA-O application domain. The concern is not about choosing one option
for all situations, but how we can mix them. Hence, we adopt the following
selection criterion: 1) use (a) and (b) for invariant properties, 2) use (c) and
(d) for time-dependent and/or speciﬁc use-case extensions to NORIA-O (i.e.
additional observables are deﬁned in a side vocabulary so the main ontology
remains stable).
Controlled vocabularies. Because of potentially heterogeneous data incoming
from varied ICT systems and incident situations to handle, we take notes of
terms from datasets and other ontologies for building up a controlled vocabu-
lary. This aims at eﬃcient management of anomaly detection patterns, rules and
methods by reducing the lexical range of possible situations to interpret. For this,
we propose a set of domain-speciﬁc vocabularies (e.g. Incident Management Pro-
cess, Application, Notiﬁcation vocabularies) modeled as SKOS concepts within
concept schemes (e.g. the milestones of the Incident Management Process). We
add, whenever available, alternate deﬁnitions of the concepts for reconciliation
of similar object attribute values through a single concept reference (e.g. com-
munication devices may report the same status of network interfaces with varied
t e r m ss u c ha s“active”, “up”o r“ enabled”). We also use the concept scheme
approach for enabling multiple interpretation of a similar concept. For example,
an event may be categorized as an integrityViolation based on the analy-
sis of the event text, which allows us to reason on the event type and infer a
SecurityAlarm thanks to a dual membership of the integrityViolation con-
cept deﬁnition. The implementation of the vocabulary reconciliation task (e.g.
relating the observed network interface administrative status to the adequate
concept reference with help of natural language processing) is out of the scope
of this paper and is left to the NORIA-O user’s choice.
4 NORIA-O: Formalization and Implementation
We have implemented the NORIA-O conceptual model in RDFS/OWL-2.
NORIA-O consists of 59 classes, 107 object properties, and 71 datatype prop-
erties. It is organized with the four facets presented in Sect. 3.2 and illustrated
in Fig.2. Its expressivity is ALCHOI (D) as per Prot´eg´e 5.1. In this section, we
introduce some of the main concepts and properties.
4.1 Resources, Network Interfaces, Network Links and Applications
Within computer science, a resource is some “part contributing to the functioning
of an ICT system. ” Similarly, as per the TMForum Data Model
8, a resource is
7 https://www.w3.org/TR/vocab-ssn/#SOSAObservation.
8 https://github.com/tmforum-apis/Open Api And Data Model.

NORIA-O: An Ontology for Monitoring ICT Systems 29
Fig. 2. Overview of the NORIA-O model. We depict the most important classes and proper-
ties, including related domain of discourse facets and relationships to third-parties models. noria is
the default namespace. The red star indicates where events are characterized within the data model
as incidents or anomalies. Examples are provided for the “literal” and “SKOS scheme” blocks. For
the sake of clarity, some object properties are grouped (see “simpliﬁed object property”) for a light
representation of similar properties (i.e. same rdfs:domain or same rdfs:range). The diagram partly
follows the Graﬀoo speciﬁcation [52].
(Color ﬁgure online)

30 L. Tailhardat et al.
“an abstract entity that describes the common set of attributes shared by all
concrete resources in the inventory ”. Therefore, we deﬁne the Resource class
for describing any physical or logical manageable entity composing the network.
Deﬁning the type of a resource is made possible through object properties such as
resourceType (i.e. controlled-vocabulary concepts such as rack, server, router,
virtual machine, etc.) and resourceProductModel (i.e. entity model instances).
Additional properties allow for identifying the resources based on their logistic
identiﬁer, hostname, installation date, etc.
Locating and reasoning over a physical entity from a geographical standpoint
is available with a chain of bot:containsZone and bot:hasElement proper-
ties, starting from a bot:Site with bot:hasZeroPoint property, down to a
Locus concept for precise Resource location within a Room (i.e. a specializa-
tion of bot:Space). Locating a resource is also available through a dependency
relationship with the seas:subSystemOf object property from the SEAS Syste-
mOntology9. This allows for describing and reasoning with parts from various
levels of organization (e.g. a virtual router instance in a router, a hard drive in
a server, a server in a rack, a rack in a bot:Site, etc.).
Describing the network topology itself is deﬁned with theNetworkInterface
and NetworkLink classes. We align with the SEAS CommunicationOntology
10
model through object properties such as networkInterfaceOf and network-
LinkTerminationResource. It should be noted that this approach is compatible
with advanced networking features such as sub-interfaces, link aggregation, vir-
tual channels, etc. Operational characteristics for interface and links are available
with properties such as networkInterfaceOperationalStatus and network-
InterfaceRoutingPriorityMetric.
The Application concept enables to deﬁne models of purpose (e.g. inter-
net access, network time, alarm monitoring) for sets of resources, and to cat-
egorize these with respect to their nature (i.e. controlled-vocabulary concepts
such as infrastructure, service platform, etc.). An ApplicationModule is a con-
crete instance of a given model (e.g. national federated Internet access, corpo-
rate network time service, monitoring for in-production devices). This grouping
level enables to relate speciﬁc technical skill centers, such as a named IP back-
bone engineering or support team (Sect. 4.4), to a given module for speciﬁc
expertise (e.g. re-engineering, diagnosis and repair). Additional properties allow
for ﬁner grain resources and events management at the module level such as
applicationModuleSlaLevel for prioritizing servicing teams, orapplication-
ModuleHotlineEnabled for triggering night shift support teams.
We also deﬁne theService concept in accordance to the TMForum TMF638
Service Inventory API
11 and the IETF SFC Architecture [ 22] for grouping
instances of ApplicationModule, and thus enabling the data path and appli-
cation composition perspectives of the functional facet (Sect. 3.2). The network
topology related to a given service is inferred from the set of resources, net-
9 https://w3id.org/seas/SystemOntology.
10 https://w3id.org/seas/CommunicationOntology.
11 https://github.com/tmforum-apis.

NORIA-O: An Ontology for Monitoring ICT Systems 31
work interfaces and network links included in each application that is part
of the service. We observe that, although deterministic, the data path granu-
larity calculus for some communication session (e.g. a time-bounded IP/http
query with its response) depends on the speciﬁcity of the resources included
in ApplicationModule instances. For example, the resulting granularity for a
“national IP backbone infrastructure ” application instance will correspond to the
routing domain.
4.2 Logs and Alarms
As per the International Telecommunication Union (ITU), “the log is a reposi-
tory for records ” (ITU-T Rec. X.735) [ 21] and an event log record “ represents
the information stored in the log as a result of receiving notiﬁcations or incom-
ing event reports ” (ITU-T Rec. X.721) [20]. Based on this deﬁnition, we deﬁne
the EventRecord class for storing any event coming from managed objects (e.g.
Resource, Application) such as system logs [49], SNMP Traps [34] and appli-
cation speciﬁc messages (e.g. user applications, operational support systems,
processing platforms). Fundamental properties such as loggingTime, logText,
logOriginatingManagedObject and logOriginatingManagementSystem allow
for keeping track of the event origin and content. Details about the mes-
sage meaning are managed with the dcterms:type property that refers to a
controlled-vocabulary for event type tagging
12 (e.g. state change, processing
error alarm, integrity violation). ThealarmSeverity property provides an indi-
cation of how it is perceived that the capability of the managed object has been
aﬀected, or how serious are the service aﬀecting conditions (including for secu-
rity alarms). Additional properties related to alarm management and interpreta-
tion are available with alignment to the DCTERMS and PEP models, such as:
alarmMitigatedBy and dcterms:relation for aggregating events and build-
ing event signatures; dcterms:conformsTo for root cause analysis and repair
planning; dcterms:mediator for responsibility follow up.
4.3 Trouble Tickets and Change Requests
We deﬁne theTroubleTicket concept accordingly to the TMForum DataModel
where a trouble ticket is “ a record of an issue that is created, tracked, and
managed by a trouble ticket management system ”
13. It is not an event per
se, but a mean to eﬃciently manage targeted resource/service (e.g. trouble-
TicketRelatedResource property) restoration operations through collabora-
tion. Hence, we also consider trouble tickets as a product of the ITIL’s Inci-
dent Management process [53], and relate them to ITIL’s Problem Management
process [54] and the BPMN by alignment to the bbo:DataResource class.
12 Event type tagging can be carried-out at the data integration stage, or through a
posteriori language processing of the “logText” property.
13 http://datamodel.tmforum.org/en/master/Common/TroubleTicket/.

32 L. Tailhardat et al.
Corrective maintenance action details are logged asTroubleTicketNote and
related to the parent TroubleTicket with the dcterms:isPartOf property.
Actions’ accountability is implemented with the dcterms:creator in relation
to the foaf:Agent class (Sect.4.4). Correlating actions to the digital traces (i.e.
EventRecord) they produce at the structural and functional level (e.g. login,
conﬁguration change, upgrade) is available with the dcterms:relation prop-
erty towards a pep:ProcedureExecutionContainer entity.
We provide additional properties for improving the incident diagnosis stage
eﬃciency (e.g. dcterms:hasPart for hierarchical grouping of tickets), and mov-
ing towards root cause analysis based on the notion of Known Error Database
(KEDB) (e.g. troubleTicketCategory and problemCategory for a priori and a
posteriori categorization, respectively) and primary/secondary anomaly (cause/-
eﬀect) with alignment to the FOLIO model. With greater details, a trouble ticket
is a document transitively referencing a set of corrective maintenance actions
that can be abstracted into an issue remediationOperationPlan for solving the
AnomalyPattern at hand. Reaching such abstraction from actions’ digital traces
is enabled by considering the PEP model withTroubleTicket as a specialization
of a pep:ProcedureExecutionContainer, actions aspep:ProcedureExecution
and OperationPlan as pep:Procedure.
Similarly to trouble tickets, we deﬁne the ChangeRequest concept accord-
ing to the TMForum DataModel 14 for tracking scheduled change operations
(as sets of pep:ProcedureExecution carried-out in correspondence to a given
OperationPlan) with structural or functional impact, and computing (potential)
causality for trouble tickets based on the set of correlated resources/applications
and operations start/end time.
4.4 Agents, Teams and Organizations
From the incident management perspective, ﬁnding experts in short time is key
for operational eﬃciency. One common approach is to form teams based on
technical expertise (e.g. routing and international backbone, servers and virtual
machines, forensics and malware retro-engineering) and assign them to manage
speciﬁc equipment or services. External support and engineering services are
also relied upon for specialized cases. To facilitate interoperability with comple-
mentary knowledge bases, we utilize the FOAF and ORG data models for rep-
resenting entities such as agents and users (foaf:Person), organizational units
(org:OrganizationalUnit), and organizations (org:Organization). Relation-
ships with IT entities, such as Resource and Application, are modeled using
properties like elementManagedBy and applicationModuleRelatedParty.
We introduce the CorporateUserIdentifier class as a specialization of
foaf:OnlineAccount and provide a controlled vocabulary for detailed role
descriptions of agents, teams (e.g. Technical Support Group), and organiza-
tions (e.g. Manufacturer). This notably enables applying the cyber security
14 http://datamodel.tmforum.org/en/master/Common/ChangeRequest/.

NORIA-O: An Ontology for Monitoring ICT Systems 33
out-of-policy principle (i.e. what is not deﬁned is not allowed) for tracking non-
legitimate operations (unless facing an insider) by asserting access control groups
as org:OrganizationalUnit and scrutinizing observed or declared user actions
(e.g. eventLogOriginatingAgent, dcterms:creator).
15
5 Evaluation
We have evaluated the NORIA-O implementation according to the ability of the
model to answer the CQs that were collected in Sect.3.1. The CQs have emerged
from an iterative and collaborative process of capturing knowledge from domain
experts. Therefore, we consider that translating these CQs into Authoring Tests
(ATs) [23,61] and obtaining a satisfactory answer to these SPARQL [57] queries
from the knowledge graph constitute a sound evaluation of NORIA-O. This
evaluation aims to check that all the concepts and relations that are important
for the experts’ needs are included in NORIA-O. The set of authoring tests,
available at https://w3id.org/noria/evaluation, has been deﬁned and tested on
two knowledge graph instances structured by NORIA-O. The ﬁrst one describes
a ﬁctitious case of supervision and is publicly available (Sect.6). The second one
has been generated from Orange internal data (10 data sources encompassing
128 features over 15 tables) using an in-house data pipeline [ 30]; the size of
the resulting RDF dataset is approximately 4 million triples for 400K entities,
including streamed events spanning over 111 days.
16
After this evaluation, we distinguish three situations depicted in column
“AT Validation” of Table 1. First, a large number of CQs (16/26) can be
answered using a single or several simple SPARQL queries and the ontology
(“OK” in Table 1). 9/26 CQs (“AI” in Table 1) are partially satisﬁed using
SPARQL queries, to which complementary AI techniques should be added to
fully answer the CQs. For example, to answer CQ#11 “What was the root cause
of the incident? ”, the representation of alarms and logs associated with a given
incident needs to be enhanced with root cause analysis algorithms (e.g. using
semantic reasoners with failure mode descriptions [ 8], or similar incident con-
text search [28]). Another example is CQ#25 “What are the vulnerabilities and
the associated risk levels of this infrastructure? ” that can be answered only by
looking for non-desirable network topology shapes or relations to cybersecu-
rity knowledge derived from network structure and security scanners (e.g. using
the SHACL [17] toolset, or graph-based risk assessment [60] with UCO-labelled
data [62]). Third, 1/26 CQs requires the introduction of new concepts or relations
via an extension of NORIA-O (“Extension” in Table1). The CQ #23 “What is
the ﬁnancial cost of this incident if it occurs? ” involves information about the
cost of an incident (e.g. leveraging the SEAS Failable System ontology [39]a n d
calculating the number of users aﬀected by a service impairment).
15 We assume that companies’ human-resource databases are reliable and accurate
sources of truth.
16 Due to conﬁdentiality, this large dataset is not made public but the ﬁctitious one
has been created with the purpose of being a shareable resource.

34 L. Tailhardat et al.
6 Use Case: Modeling a Complex IT Infrastructure
We illustrate the usage and expressiveness of NORIA-O through a ﬁctitious case
of network infrastructure supervision. The Fig. 3 summarizes this use case by
showing both the network topology and the corresponding entities. The dataset
for this scenario is available at https://w3id.org/noria/dataset. 660 triples are
needed for representing the full scenario with additional resources, organization
and root cause analysis details.
Fig. 3. NORIA-O instantiation example.A fault on an access switch (red star) impacts redun-
dancy for critical application resources. The technician identiﬁes the issue through an inferred alert
(t = t2), traces it back to the faulty equipment, and takes corrective action (t = t3). The process is
documented in a trouble ticket, including the cause and repair action.noria is the default namespace
for classes and properties. “SKOS scheme” block values (e.g. “ equipmentAlarm”, “inferredAlert”,
etc.) are coming from the NORIA-O controlled vocabulary.
(Color ﬁgure online)
Based on this scenario, we observe that NORIA-O enhances anomaly detec-
tion and analysis tasks with the following capabilities. Data integration: it
consolidates data from various sources and provides a standardized interpreta-
tion using the rdf:type and skos:Concept constructs. For example, this allows
entities in the structural and functional facets to combine data from network
discovery tools, VM hypervisors, and the company directory. Events can also be
looked up by their type, regardless of their originating signaling system. Data
querying: it enables facet-wise checking of the network state and conﬁguration
in a rule-based approach using data retrieval. For example, a SPARQL query [57]
can derive the scenario’s inferred alert (a resilience problem) using a k out-of n
graph pattern onResource and Application entities. This would not have been
possible with a single data source or without standardized interpretation of the

NORIA-O: An Ontology for Monitoring ICT Systems 35
data using controlled vocabularies. Situation understanding & classiﬁca-
tion: it enables gaining facet-wise insights about a situation and its ecosystem
using graph traversal. For instance, a SPARQL query can calculate the network
neighborhood for a speciﬁc incident or identify the teams involved in its reso-
lution. Categorizing event patterns and root cause analysis is addressed using
reasoning through complementary ontologies [8,40] or rule engines [35,47]. Addi-
tionally, the context of an incident, represented by the graph structure related
to a TroubleTicket entity, can be captured and categorized using graph embed-
dings [28].
7 Conclusion and Future Work
In this paper, we presented NORIA-O, an ontology for representing network
infrastructures, incidents and maintenance operations, that relies on and extends
well-known semantic models such as BBO, BOT, FOAF, FOLIO, SEAS and
UCO. NORIA-O is available at https://w3id.org/noria under a BSD-4 License,
along with its documentation and a sample dataset. We conducted an evalua-
tion of NORIA-O using the Competency Questions & Authoring Tests method-
ology [61], demonstrating its suitability according to the expert needs. We also
illustrated the usage and expressiveness of the data model using a ﬁctitious case
of network infrastructure supervision. We showcased the complementary use
of graph traversal techniques, reasoning, and incident context capture through
graph embeddings.
Future work will focus on experimenting with NORIA-O for cross-domain
alarm correlation and aggregation. First, event logs from heterogeneous data
sources depicting an identical phenomenon need to be parsed and categorized
in the same way. This can be achieved by incorporating speciﬁc technological
domains, such as OTN or 5G mobile network speciﬁcations, into the NORIA-O
controlled vocabulary. Techniques such as log parsing [ 24,51] and semantiza-
tion [4] can be applied, either before or after the data integration stage. NLP-
related techniques, including named entity recognition [5], topic modeling [18],
and vocabulary reconciliation [44], are crucial in this process. Second, relating
events to anomaly models [28] or attack scenarios [6], requires to ﬁlter-out event
logs and alarms on both trouble tickets’ timespan and impacted resources char-
acteristics. Recent research on dynamic graphs with event streams has shown
promising results in estimating the useful spreading of observables [11,15,56,59].
Finally, we note that network resilience and cybersecurity application
domains will beneﬁt from extensions of a NORIA-O knowledge graph with third-
party data collection tools. For example, network topology anti-patterns and
semantic interpretation of the ICT resources conﬁguration [58] could be related
to the network performance and issues. Similarly, integrating data from vulnera-
bility scanners and cyber threat intelligence tools could enable cybersecurity risk
evaluation and minimization (e.g. combining CVSS [ 46] data from OpenCTI
17
with optimized countermeasure placement techniques [60]).
17 https://www.opencti.io.

36 L. Tailhardat et al.
References
1. Oltramari, A., Cranor, L., Walls, R., McDaniel, P.: Building an ontology of cyber
security. In: 9th Conference on Semantic Technologies for Intelligence, Defense,
and Security (STIDS) (2014)
2. Annane, A., Aussenac-Gilles, N., Kamel, M.: BBO: BPMN 2.0 based ontology
for business process representation. In: 20th European Conference on Knowledge
Management (ECKM) (2019)
3. Dimou, A.: High quality linked data generation from heterogeneous data. Ph.D.
thesis, University of Antwerp (2017)
4. Ekelhart, A., Ekaputra, F.J., Kiesling, E.: The SLOGERT framework for auto-
mated log knowledge graph construction. In: Verborgh, R., et al. (eds.) ESWC
2021. LNCS, vol. 12731, pp. 631–646. Springer, Cham (2021). https://doi.org/10.
1007/978-3-030-77385-4
38
5. Piplai, A., Mittal, S., Joshi, A., Finin, T., Holt, J., Zak, R.: Creating cybersecurity
knowledge graphs from malware after action reports. IEEE Access (2020).https://
doi.org/10.1109/ACCESS.2020.3039234
6. Elitzur, A., Puzis, R., Zilberman, P.: Attack hypothesis generation. In: European
Intelligence and Security Informatics Conference (EISIC) (2019). https://doi.org/
10.1109/EISIC49498.2019.9108886
7. Goertzel, B., Pennachin, C., Geisweiller, N.: Engineering General Intelligence,
Part 1: A Path to Advanced AGI via Embodied Learning and Cognitive Synergy.
Atlantis Press (2014)
8. Steenwinckel, B.: IBCNServices/Folio-Ontology (2019). https://github.com/
IBCNServices/Folio-Ontology
9. Steenwinckel, B., et al.: Towards adaptive anomaly detection and root cause analy-
sis by automated extraction of knowledge from risk analyses. In: 9th International
Semantic Sensor Networks Workshop (SSN) (2018)
10. Brazhuk, A.: Threat modeling of cloud systems with ontological security pattern
catalog. Int. J. Open Inf. Technol. (2021)
11. Xu, C., Nayyeri, M., Alkhoury, F., Yazdi, H.S., Lehmann, J.: Temporal knowledge
graph embedding model based on additive time series decomposition. In: 19th
International Semantic Web Conference (ISWC) (2020)
12. Brickley, D., Miller, L.: Friend of a Friend (FOAF) Vocabulary Speciﬁcation (2004).
http://xmlns.com/foaf/spec/
13. Brickley, D., Guha, R.V.: RDF Schema. W3C Recommendation, W3C (2014)
14. Reynolds, D.: The Organization Ontology. W3C Recommendation, W3C (2014)
15. Maillot-Tchofo, D., Triki, A., Laye, M., Puentes, J.: Clustering of live network
alarms using unsupervised statistical models. In: 49th European Conference on
Optical Communications (ECOC) (2023)
16. Kaur, H., Maini, R.: Identiﬁcation of recurring patterns of code to detect structural
clones. In: 6th International Conference on Advanced Computing (IACC) (2016).
https://doi.org/10.1109/IACC.2016.80
17. Knublauch, H., Kontokostas, D.: Shapes Constraint Language (SHACL). W3C
Recommendation, W3C (2017)
18. Harrando, I., Lisena, P., Troncy, R.: Apples to apples: a systematic evaluation
of topic models. In: Recent Advances in Natural Language Processing (RANLP)
(2021). https://doi.org/10.26615/978-954-452-072-4
055
19. ITU: ITU-T Rec. G.709/Y.1331 (06/20) – Interfaces for the optical transport net-
work. Recommendation, International Telecommunication Union (ITU) (2020)

NORIA-O: An Ontology for Monitoring ICT Systems 37
20. ITU/CCITT: ITU-T Rec. X.721 (02/92) Information Technology – Open Sys-
tems Interconnection – Structure of Management Information: Deﬁnition of Man-
agement Information. Recommendation, International Telecommunication Union
(ITU) (1992)
21. ITU/CCITT: ITU-T Rec. X.735 (09/92) Information Technology – Open Systems
Interconnection – Systems Management: Log Control Function. Recommendation,
International Telecommunication Union (ITU) (1992)
22. Halpern, J., Pignataro, C.: Service function chaining (SFC) architecture. RFC 7665
(2015)
23. Potoniec, J., Wi´sniewski, D., /suppressLawrynowicz, A., Keet, C.M.: Dataset of ontology
competency questions to SPARQL-OWL queries translations. Data in Brief (2020)
24. Zhu, J., et al.: Tools and benchmarks for automated log parsing. In: 41st Inter-
national Conference on Software Engineering: Software Engineering in Practice
(ICSE-SEIP) (2019). https://doi.org/10.1109/ICSE-SEIP.2019.00021
25. Chessman, J.: Magic quadrant for network performance monitoring and diagnos-
tics. Technical report. G00463582, Gartner (2020)
26. Kavanagh, K., Bussa, T., Sadowski, G.: Magic quadrant for security information
and event management. Technical report. G00348811, Gartner (2018)
27. Janowicz, K., Haller, A., Cox, S., Phuoc, D., Lefran¸cois, M.: SOSA: a lightweight
ontology for sensors, observations, samples, and actuators. SSRN Electron. J.
(2018). https://doi.org/10.1016/j.websem.2018.06.003
28. Tailhardat, L., Troncy, R., Chabot, Y.: Leveraging knowledge graphs for classify-
ing incident situations in ICT systems. In: 18th International Conference on Avail-
ability, Reliability and Security (ARES) (2023).https://doi.org/10.1145/3600160.
3604991
29. Tailhardat, L., Chabot, Y., Troncy, R.: NORIA: machine learning, ontology
and reasoning for the identiﬁcation of anomalies (2021). https://genears.github.
io/pubs/IA2-2021-NORIA-POSTER.pdf , position poster, Institut d’Automne en
Intelligence Artiﬁcielle (IA
2), Sorbonne Center for Artiﬁcial Intelligence (SCAI),
Paris, France
30. Tailhardat, L., Chabot, Y., Troncy, R.: Designing NORIA: a knowledge graph-
based platform for anomaly detection and incident management in ICT systems. In:
4th International Workshop on Knowledge Graph Construction (KGCW) (2023)
31. Rasmussen, M.H., Lefran¸cois, M., Schneider, G.F., Pauwels, P.: BOT: the building
topology ontology of the W3C linked building data group. Semant. Web J. (2020).
https://doi.org/10.3233/SW-200385
32. Thapa, M., Espejo-Uribe, J., Pournaras, E.: Measuring network reliability and
repairability against cascading failures. J. Intell. Inf. Syst. (2019)
33. Poveda-Villal´on, M., Fern´ andez-Izquierdo, A., Fern´ andez-L´opez, M., Garc´ ıa-
Castro, R.: LOT: an industrial oriented ontology engineering framework. In: Engi-
neering Applications of Artiﬁcial Intelligence (2022)
34. Fedor, M., Schoﬀstall, M.L., Davin, J.R., Case, J.D.: Simple Network Management
Protocol (SNMP). RFC 1157 (1990)
35. Proctor, M.: Drools: a rule engine for complex event processing. In: Sch¨ urr, A.,
Varr´o, D., Varr´o, G. (eds.) AGTIVE 2011. LNCS, vol. 7233, pp. 2–2. Springer,
Heidelberg (2012). https://doi.org/10.1007/978-3-642-34176-2
2
36. Bastian, M., Heymann, S., Jacomy, M.: Gephi: an open source software for explor-
ing and manipulating networks. In: 3rd International AAAI Conference on Weblogs
and Social Media (ICWSM) (2009). https://doi.org/10.1609/icwsm.v3i1.13937

38 L. Tailhardat et al.
37. Ghijsen, M., et al.: A semantic-web approach for modeling computing infrastruc-
tures. Comput. Electr. Eng. (2013). https://doi.org/10.1016/j.compeleceng.2013.
08.011
38. Lefran¸cois, M.: Planned ETSI SAREF extensions based on the W3C&OGC
SOSA/SSN-compatible SEAS ontology patterns. In: Workshop on Semantic Inter-
operability and Standardization in the IoT (SIS-IoT) (2017)
39. Lefran¸cois, M., Kalaoja, J., Ghariani, T., Zimmermann, A.: SEAS Knowledge
Model. Deliverable 2.2, ITEA2 12004 Smart Energy Aware Systems (2016)
40. Lazzari, N., Poltronieri, A., Presutti, V.: Classifying sequences by combining
context-free grammars and OWL ontologies. In: Pesquita, C., et al. (eds.) ESWC
2023. LNCS, vol. 13870, pp. 156–173. Springer, Cham (2023). https://doi.org/10.
1007/978-3-031-33455-9
10
41. Ben-Asher, N., Oltramari, A., Erbacher, R.F., Gonzalez, C.: Ontology-based adap-
tive systems of cyber defense. In: 10th Conference on Semantic Technology for
Intelligence, Defense, and Security (STIDS) (2015)
42. Corcho, O., et al.: A high-level ontology network for ICT infrastructures. In: Hotho,
A., et al. (eds.) ISWC 2021. LNCS, vol. 12922, pp. 446–462. Springer, Cham (2021).
https://doi.org/10.1007/978-3-030-88361-4
26
43. Prasad, P., Chessman, J.: Market guide for IT infrastructure monitoring tools.
Technical report. G00450400, Gartner (2019)
44. Lisena, P., et al.: Controlled vocabularies for music metadata. In: 19th International
Society for Music Information Retrieval Conference (ISMIR) (2018)
45. Kaloroumakis, P.E., Smith, M.J.: Toward a knowledge graph of cybersecurity coun-
termeasures. Technical report, The MITRE Corporation (2021)
46. Mell, P., Scarfone, K., Romanosky, S.: Common vulnerability scoring system. IEEE
Security Privacy (2006)
47. Bonte, P., Tommasini, R., Valle, E.D., De Turck, F., Ongenae, F.: Streaming
MASSIF: cascading reasoning for eﬃcient processing of IoT data streams. Sen-
sors (2018). https://doi.org/10.3390/s18113832
48. Zhou, Q., Gray, A.J.G., McLaughlin, S.: ToCo: an ontology for representing hybrid
telecommunication networks. In: Hitzler, P., et al. (eds.) ESWC 2019. LNCS, vol.
11503, pp. 507–522. Springer, Cham (2019). https://doi.org/10.1007/978-3-030-
21348-0 33
49. Gerhards, R.: The syslog protocol. RFC 5424 (2009)
50. Bechhofer, S., et al.: Web Ontology Language (OWL). W3C Recommendation,
W3C (2004)
51. He, S., He, P., Chen, Z., Yang, T., Yuxin, S., Lyu, M.R.: A survey on automated
log analysis for reliability engineering. ACM Comput. Surv. (2021). https://doi.
org/10.1145/3460345
52. Peroni, S.: Graﬀoo: Graphical Framework for OWL Ontologies (2013). https://
essepuntato.it/graﬀoo/
53. Kempter, S.: It process maps – incident management (2007). https://wiki.en.it-
processmaps.com/index.php/Incident Management
54. Kempter, S.: It process maps – problem management (2007). https://wiki.en.it-
processmaps.com/index.php/Problem Management
55. Ehrhart, T., Lisena, P., Troncy, R.: KG explorer: a customisable exploration tool
for knowledge graphs. In: 6th International Workshop on the Visualization and
Interaction for Ontologies and Linked Data, co-Located with the 20th International
Semantic Web Conference (ISWC) (2021)
56. Wu, T., Khan, A., Gao, H., Li, C.: Eﬃciently embedding dynamic knowledge
graphs. Knowl.-Based Syst. (2019)

NORIA-O: An Ontology for Monitoring ICT Systems 39
57. W3C SPARQL Working Group: SPARQL Protocol and RDF Query Language 1.1
(SPARQL). W3C Recommendation, W3C (2013)
58. Atoui, W.S.: Toward auto-conﬁguration in software networks. Ph.D. thesis, Institut
Polytechnique de Paris (2020)
59. Li, Y., Ge, T., Chen, C.: Data stream event prediction based on timing knowledge
and state transitions. VDLB Endow. (2020)
60. Naghmouchi, Y., Perrot, N., Kheir, N., Mahjoub, A.R., Wary, J.-P.: A new
risk assessment framework using graph theory for complex ICT systems. In: 8th
ACM CCS International Workshop on Managing Insider Security Threats (2016).
https://doi.org/10.1145/2995959.2995969
61. Ren, Y., Parvizi, A., Mellish, C., Pan, J.Z., van Deemter, K., Stevens, R.: Towards
competency question-driven ontology authoring. In: Presutti, V., d’Amato, C.,
Gandon, F., d’Aquin, M., Staab, S., Tordai, A. (eds.) ESWC 2014. LNCS, vol.
8465, pp. 752–767. Springer, Cham (2014). https://doi.org/10.1007/978-3-319-
07443-6 50
62. Syed, Z., Padia, A., Lisa Mathews, M., Finin, T., Joshi, A.: UCO: a uniﬁed cyber-
security ontology. In: AAAI Workshop on Artiﬁcial Intelligence for Cyber Security
(2016)

FlexRML: A Flexible and Memory
Eﬃcient Knowledge Graph Materializer
Michael Freund1(B) , Sebastian Schmid2 , Rene Dorsch1 ,
and Andreas Harth1,2
1 Fraunhofer Institute for Integrated Circuits IIS, N¨urnberg, Germany
{michael.freund,rene.dorsch,andreas.harth}@iis.fraunhofer.de
2 Friedrich-Alexander-Universit¨at Erlangen-N¨urnberg, N¨urnberg, Germany
Abstract. We present FlexRML, a ﬂexible and memory eﬃcient soft-
ware resource for interpreting and executing RML mappings. As a knowl-
edge graph materializer, FlexRML can operate on a wide range of sys-
tems, from cloud-based environments to edge devices, as well as resource-
constrained IoT devices and real-time microcontrollers. The primary goal
of FlexRML is to balance memory eﬃciency with fast mapping execu-
tion. This is achieved by using C++ for the implementation and a result
size estimation algorithm that approximates the number of N-Quads
generated and, based on the estimate, optimizes bit sizes and data struc-
tures used to save memory in preparation for mapping execution. Our
evaluation shows that FlexRML’s adaptive bit size and data structure
selection results in higher memory eﬃciency compared to conventional
methods. When benchmarked against state-of-the-art RML processors,
FlexRML consistently shows lower peak memory consumption across dif-
ferent datasets while delivering faster or comparable execution times.
Resource type: RML Processor
License: GNU AGPLv3
DOI: https://doi.org/10.5281/zenodo.10256148
URL: https://github.com/wintechis/ﬂex-rml
Keywords: Knowledge Graph Construction
· RML · Internet of
Things
1 Introduction
Knowledge graphs (KGs) [13] have become increasingly popular in both industry
and academia. For instance, KGs are used to enhance Large Language Models
(LLMs) by supplementing them with additional factual information, thereby
countering issues like hallucination [ 20]. In the context of Industry 4.0, KGs
play an important role in enabling semantic interoperability between devices
and services [2]. Additionally, as Internet of Things (IoT) devices generate large
volumes of raw data, the application of Semantic Web technologies, such as RDF
and ontologies, can add context and meaning to the data, which signiﬁcantly
increases its value [29].
c⃝ The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
A. Mero˜no Pe˜nuela et al. (Eds.): ESWC 2024, LNCS 14665, pp. 40–56, 2024.
https://doi.org/10.1007/978-3-031-60635-9_3

FlexRML: A Flexible and Memory Eﬃcient Knowledge Graph Materializer 41
One approach to constructing KGs, i.e., mapping non-RDF data such as
CSV, JSON, or XML to RDF, is to use a generic mapping language such as the
RDF Mapping Language (RML) [ 9]. RML mappings are represented as RDF
graphs and outline the tasks for transforming a non-RDF data source, called
logicalSource, into RDF format. The transformation process is organized by a
construct called triplesMap. Within a triplesMap, the generation of RDF data is
described by two main mappings: the subjectMap and the predicateObjectMap.
The subjectMap is responsible for mapping elements from the logical source to
RDF subjects. In turn, the predicateObjectMap handles the creation of pred-
icates and objects for the RDF data by integrating a predicateMap that maps
to RDF predicates and an objectMap that maps to RDF objects. If objects
are generated using a join, the objectMap also speciﬁes a joinCondition.T h e
RML mappings are used in conjunction with RML processors, which are engines
that interpret the mappings and transform non-RDF input data to output RDF
data in serializations such as N-Quads. Well known RML processors are the
RMLMapper
1, Morph-KGC [3], or the SDM-RDFizer [15].
The current generation of RML processors is implemented using high-level
languages such as Java, JavaScript, and Python. The design choice to use high-
level languages makes them well-suited for operation in unconstrained environ-
ments, such as cloud platforms. However, it also restricts their ability to function
eﬀectively in environments with limited memory, such as single-board computers
or highly constrained microcontrollers. Additionally, these RML processors may
not be optimal for real-time applications that are crucial in Industry 4.0 contexts,
where processing needs to be reliably completed within strict time limits [14].
With the emergence of new and evolving domains such as LLMs and Indus-
try 4.0, there is a growing demand for access to both semantic and factual data.
To meet this demand, there is a need for an RML processor that is not only
fast and memory eﬃcient, but also versatile enough to operate in a variety of
environments, whether constrained, unconstrained, or requiring real-time guar-
antees. The main challenge in developing such a framework is to ensure eﬃcient
management of available processing power and memory.
Our resource, FlexRML, is a ﬂexible and memory eﬃcient RML processor
developed in C++ to ensure adaptability to various environments with diﬀerent
resource constraints. FlexRML uses an algorithm based on Bernoulli sampling
to estimate the result size, speciﬁcally the number of unique RDF N-Quads to
be generated. This feature allows FlexRML to select the most optimal hash
functions for diﬀerent data structures, balancing improved memory eﬃciency
and increased processing time for KG materialization. From an implementation
perspective, FlexRML optimizes at the mapping level using techniques such as
self-join elimination, RML mapping normalization, and, where possible, replaces
join operations with reference conditions. In cases where joins cannot be replaced,
FlexRML uses a hash join algorithm to perform them. To increase memory
eﬃciency, duplicate removal is handled by storing the hash of already generated
RDF data, which carries the risk of hash collisions that can result in missing
1 https://github.com/RMLio/rmlmapper-java.

42 M. Freund et al.
output N-Quads. But the risk can be mitigated by choosing an appropriate bit
size when computing hashes.
The key contributions of our work are as follows:
– Introduction of FlexRML, a memory-eﬃcient RML processor capable of map-
ping data in cloud, edge, and IoT environments.
– Usage of a sampling-based algorithm to estimate N-Quads, enabling optimal
hash function selection for improved memory eﬃciency.
– Comprehensive evaluation of FlexRML’s performance against existing RML
processors across cloud, edge, and IoT platforms, accompanied by the intro-
duction of a dataset speciﬁcally tailored for evaluating IoT devices.
2 Related Work
There are several languages and techniques for building KGs from non-RDF
data, notably SPARQL-Generate [19], SPARQL Anything [6], and D-REPR [28].
However, the dominant method relies on R2RML [7], a W3C recommendation,
and its extension RML, which supports non-relational data sources such as CSV,
JSON, and XML. The adoption of RML is underscored by the number of RML
processors available [3,15,23,25], each with diﬀerent conformance
2 and features,
such as mapping partitions. These implementations in high-level languages are
suitable for cloud environments, but are less optimal for resource-constrained
devices. In contrast, we propose an RML processor designed for a wide range
of devices, from cloud and consumer hardware to single-board computers and
resource-constrained microcontrollers and IoT devices.
Semantic Web technologies such as RDF, RDFS, and OWL are considered
key to semantic interoperability in IoT, as proposed by various authors [12,17].
Many proposed IoT architectures [ 1,18,22] share a common need to map IoT
data to RDF for cloud storage and application use, typically using an edge device
such as a gateway for mapping. However, FlexRML oﬀers a simpler alternative
by enabling direct data mapping on Internet-connected, constrained devices,
enabling direct cloud uploads and bypassing the need for edge RML proces-
sors. Nevertheless, in scenarios where edge-based RML processors are required,
FlexRML’s memory eﬃciency makes it a viable option for edge deployment as
well. The availability of RDF data directly on IoT devices is a prerequisite for
device-level semantic interoperability, which can be used to enable data exchange
in distributed IoT systems.
3 FlexRML: Architecture and Implementation
The FlexRML architecture integrates both high-level design and speciﬁc imple-
mentation details, providing a complete picture of how each component works
within the system.
FlexRML performs two main steps: thePreprocessing Step and the Mapping
Step, as shown in Fig.1.
2 https://rml.io/implementation-report/.

FlexRML: A Flexible and Memory Eﬃcient Knowledge Graph Materializer 43
Fig. 1. The Architecture of FlexRML.
3.1 Preprocessing Step
The Preprocessing Step is designed to optimize input RML mappings for eﬃcient
processing. This involves preparing the correct physical data structures and hash
functions, and extracting necessary processing steps from the RML mappings.
Mapping Optimizer. The Mapping Optimizer is designed to increase the eﬃ-
ciency of input RML mappings. This is achieved through a multi-step process:
First, the component analyzes the input RML mapping and applies strategies
such as self-join elimination [3] or mapping normalization [24]. In addition, the
component evaluates the potential to replace join operations with reference con-
ditions [27]. From a technical point of view, the optimizer uses the Serd
3 C
library for RDF parsing. The component’s functionality includes replacing self-
joins with corresponding objectMaps, expanding constant shortcuts or classes,
and decomposing complex predicateObjectMaps that may consist of multiple
predicateMaps or objectMaps. Where appropriate, the optimizer also replaces
standard joins with reference conditions in the RML mapping to improve mate-
rialization speed.
Result Size Estimator. The Result Size Estimator uses sampling methods
described in Sect. 4 to estimate the number of N-Quads generated by the RML
mapping. Based on the estimated total ˆT , the component determines the appro-
priate bit size for hash functions. The bit size corresponds to the number of
possible unique hash values N and must be chosen according to ˆT . The decision
which hash size to use is based on pre-calculated thresholds derived from the
birthday problem in probability theory (see Eq.1).
P =1 − N !
(N − ˆT )! · N ˆT ≈ 1 − e− ˆT 2
2N (1)
3 https://github.com/drobilla/serd.

44 M. Freund et al.
The thresholds are computed to allow a worst-case maximum hash collision
probability P of 0.05 percent, which has proven suﬃcient in our experiments to
mitigate missing output RDF statements. Therefore, we have set the thresholds
at 2,073 N-Quads for 32-bit hash functions, and 135,835,773 N-Quads for 64-bit
hash functions. For estimates exceeding these thresholds, 128-bit hash functions
are used. FlexRML uses the CityHash algorithm
4 to perform string hashing
operations due to its high hashing speed. The CityHash algorithm is available in
32-bit, 64-bit and 128-bit variants. Using smaller bit sizes for hash computations
not only speeds up the process, but also reduces the amount of memory needed
to store hashes. The goal is to choose the smallest bit size for the hash function
that keeps the risk of hash collisions below the predeﬁned probability thresh-
old. Choosing an optimal bit size is critical, as this will signiﬁcantly reduce the
probability of hash collisions.
Mapping Analyzer. The Mapping Analyzer component processes the normal-
ized input RML mappings and extracts key information. The extracted informa-
tion includes the number of predicateObjectMaps in each triplesMap, the classes
corresponding to the subjectMap, and the details of objectMaps including the
joinCondition. The data extracted by the Mapping Analyzer is organized into
several arrays. These arrays form the basis of the mapping process and serve as
directives to the Mapping Executor.
3.2 Mapping Step
The Mapping Step performs the actual mapping of the logical sources to RDF
using the Mapping Executor, which interprets the extracted information gener-
ated by the Mapping Analyzer, creates N-Quads, and removes duplicates using a
Duplicate Checker and a hash set to track hashes of already generated N-Quads.
The Mapping Step is parallelized in FlexRML using the Producer-Consumer
design pattern. In this setup, each triplesMap is processed in a separate thread by
a Mapping Executor acting as a producer, while the Duplicate Checker operates
as a consumer in a separate thread. This design ensures that all generated N-
Quads are checked before they are written to the output ﬁle, while allowing
FlexRML to use multiple threads to speed up the materialization process.
Mapping Executor. The Mapping Executor component maps input data
sources into N-Quads. The component processes each data element from the
speciﬁed inputs, e.g., from a ﬁle on the local drive or from in-memory data
structures such as the std::string class [ 8], converts the read element into the
internal vector-based data representation, and generates a set of N-Quads for
each element. Note that FlexRML currently supports only CSV data as input,
due to limited support for the C ++ standard library in some microcontroller
environments, which restricts the use of existing parsing libraries. The N-Quad
generation uses the extracted information from the RML mapping gathered by
the Mapping Analyzer. If join operations cannot be substituted with a reference
condition at the mapping level, the Mapping Executor performs a join using a
hash join algorithm, and therefore must create an index on the data beforehand.
4 https://opensource.googleblog.com/2011/04/introducing-cityhash.html.

FlexRML: A Flexible and Memory Eﬃcient Knowledge Graph Materializer 45
Duplicate Checker. Each generated set of N-Quads is passed to the Dupli-
cate Checker. This component uses a hash function with a bit size of either 32,
64, or 128, as speciﬁed by the Result Size Estimator. Each N-Quad is hashed,
and the hash value is then evaluated for uniqueness. The evaluation is done by
attempting to insert the hash into a hash set. If the hash already exists in the set,
indicating a potential duplicate, the corresponding N-Quad is discarded. Other-
wise the N-Quad is considered unique and written to the output ﬁle. Through
this mechanism, the output RDF data is continuously and incrementally built.
As new N-Quads are generated, they undergo the same duplication check. How-
ever, a risk of this method is the possibility of hash collisions where an N-Quad
is mistakenly marked as a duplicate, resulting in its absence in the output. The
risk can be mitigated by choosing an appropriate bit size.
4 Estimation of Generated RDF Elements
Estimating the number of RDF elements, such as N-Quads, that will be gener-
ated before executing an RML mapping is beneﬁcial. For instance, in FlexRML,
the estimate is used to select the appropriate bit size for hash functions. Gen-
erally, the estimation can serve other purposes similar to those in classical rela-
tional database systems, such as query optimization or the selection of eﬃcient
algorithms and access methods [16].
Independent Bernoulli sampling is an established technique for estimating
result sizes [11, p. 348], especially for join operations [ 26]. In general the algo-
rithm consits of following steps:
1. Generate a sample from the original dataset through simple random sampling,
where each record is independently and randomly chosen.
2. Count the elements in the sample that exhibit the desired characteristic. The
proportion of these elements in the sample is an estimate of their proportion
in the entire dataset.
3. Use the identiﬁed proportion to estimate the number of elements with the
desired characteristic in the entire dataset.
The method allows quick estimations by analyzing the distribution and prop-
erties of the data without processing the entire dataset, assuming sample sizes
are large [21]. In KG construction, we sample the logical source data, perform
the RML mapping on the sample, and enumerate the unique results, before
estimating the unique results in the entire dataset.
When performing the estimation, we diﬀerentiate between two categories
of triplesMaps and their corresponding objectMaps: those that require a join
operation and those that do not.
4.1 Estimation of triplesMaps Without Join
To estimate the output size produced by triplesMaps consisting of objectMaps
without join we assess the number of unique N-Quads U that will be generated

46 M. Freund et al.
when mapping each element of the logical data sourceA. Elements in the logical
source can be, for example, rows in CSV ﬁles or JSON objects in JSON arrays.
To estimate U , we generate a Bernoulli sample SA drawn from the original
dataset A. The sampling process is performed with a given probability p.U s i n g
SA, we perform the mapping and enumerate the generated unique N-QuadsU ′.
Given that each element’s inclusion in our sample is deﬁned by p, the expected
count of U ′ is U multiplied by p,o r E[U ′]= U · p. From this, we derive our
estimator ˆU , which represents the estimated total number of unique N-Quads
that will be generated when mapping the entire logical source. To obtain ˆU ,
we scale U ′ by the inverse of the sampling probability, resulting in ˆU = U ′
p .T o
calculate the expected value of ˆU , we consider the scaling of U ′, resulting in
E[ ˆU ]= E[U ′
p ]. Substituting the expression for U ′, we further show that
E[ ˆU ]= E[U ′
p ]= E[U · p
p ]= E[U ] (2)
which demonstrates that ˆU serves as an estimator for U .
To estimate the total number of N-Quads,ˆUtotal, generated by all triplesMaps
with non-join objectMaps, we sum the individual estimates ˆU :
ˆUtotal =
∑ ˆU (3)
4.2 Estimation of triplesMaps with Join
When estimating the number of unique N-Quads J when mapping triplesMaps
consisting of objectMaps with joins, it must be taken into account that there
are two logical sources, A and B, instead of just one. Therefore, the estimation
operation requires the creation of two samples using independent Bernoulli sam-
pling: sample SA from logical source A sampled with probabilitypA, and sample
SB from logical source B sampled with probability pB . The RML mapping is
performed on the two samples, and the unique N-Quads J ′ generated are enu-
merated. To obtain the estimated number of unique N-Quads ˆJ when mapping
the two entire logical sources, we again scale upJ ′ by using the inverse of the two
sampling probabilities pA and pB [26]. The inverse is used because the sampling
probability represents the fraction of the logical source that is included in the
sample. Thus, to estimate the number of unique RDF elements when mapping
the entire content of the logical sources, we use ˆJ =
J ′
pA ·pB
.
To estimate the total number of unique N-Quads generated by triplesMaps
with joins ˆJtotal, we sum the scaled estimates of generated unique N-Quads:
ˆJtotal =
∑ ˆJ (4)
4.3 Estimation of All triplesMaps
The estimate of the total number of unique N-Quads generated from all triples-
Maps, ˆT , is therefore given by
ˆT = ˆUtotal + ˆJtotal (5)

FlexRML: A Flexible and Memory Eﬃcient Knowledge Graph Materializer 47
By adding the unique estimates from predicateObjectMaps without joins to the
unique estimates of predicateObjectMaps with joins, we arrive at an estimation
of the total unique RDF elements generated through an RML mapping.
5 Empirical Evaluation
In the evaluation we aim to answer following three research questions:
– R1: How accurate is the estimation using the Result Size Estimator?
– R2: How does adaptive selection of the appropriate bit size for hash algo-
rithms impact execution time and memory consumption?
– R3: How does FlexRML compare to state-of-the-art KG materializers in
terms of execution time and memory consumption?
All results and scripts to run the benchmark can be found on GitHub5.
Datasets. We evaluated FlexRML using three benchmarks. In a cloud and edge
environment we used the GTFS Madrid benchmark [ 5] with scale factors of
10, 100, and 500, and the SDM Genomic Testbed 6 with dataset sizes of 10K,
100K, and 1M entries and a duplicate rate of 75 percent, with each element
repeated 20 times. To the best of our knowledge, there are no datasets containing
sensor data that are small enough to be mapped on IoT devices, so for this
purpose we introduce a new RML-SENSOR benchmark
7 (SENS). The RML-
SENSOR benchmark simulates data produced by two sensors and includes one
metadata ﬁle. The data can be generated using small scale factors, which allows
for the evaluation of the performance of RML processors on memory-constrained
devices. All datasets used in the evaluation are in CSV format.
The SDM Genomic Testbed provides RML mappings
8 with diﬀerent types of
objectMaps: simple objectMaps without joins (POM), objectMaps with a self-
join (REF), and objectMaps with a join (JOIN), the abbreviations are reused
form [3]. The number of mappings of each type used is indicated by a number
followed by the type, e.g. 1POM means that the mapping consists of one simple
objectMap without join.
Metrics. For R1, we evaluate the Result Size Estimator by comparing the esti-
mated number of generated N-Quads, obtained using various sampling proba-
bilities, against the true value of generated N-Quads and the required execution
time using the built-in chrono module. To address R2 and R3, we assess the
KG materialization performance using two parameters: elapsed wall time and
maximum memory usage. The latter was measured by the maximum resident
set size. These parameters were evaluated on three systems with diﬀerent levels
of constraint. Both parameters, elapsed wall time and maximum resident set
size, were obtained using the time command from the GNU time package
9.E a c h
5 https://github.com/wintechis/ﬂex-rml-evaluation/.
6 https://ﬁgshare.com/articles/dataset/SDM-Genomic-Datasets/14838342/1.
7 https://github.com/wintechis/rml-sensor-benchmark/.
8 https://github.com/SDM-TIB/SDM-RDFizer-Experiments/tree/master/
cikm2020/experiments.
9 https://www.gnu.org/software/time/.

48 M. Freund et al.
experiment was conducted three times, and the average values for elapsed wall
time and peak memory usage are reported. The exact hardware and software
conﬁgurations of each tested device are detailed in Table 1. Better results are
indicated by lower values in the diagram in both metrics.
Table 1. Evaluated Hardware and Systems.
Name Type Processor Memory Operating System
ESP32 IoT Device 2 × 240 MHz 512 KB ESP-IDF FreeRTOS
Pi 4 Edge Node 4 × 1.5 GHz 4G B Raspberry Pi OS
VM Cloud 8 × 2.0 GHz 64 GB Ubuntu 22.04.3 LTS
5.1 Accuracy of Result Size Estimator
To evaluate R1, we performed experiments on the 100k SDM Genomic dataset
using the combination of 4POM and 5JOIN mapping rules (Fig.2), allowing us
to evaluate the accuracy in a complex scenario combining objectMaps with and
without joins. The evaluation is performed on the cloud based virtual machine.
0.20 .40 .60 .8
0
1
2
3
·106
True Value
Sampling Probability
Estimated N-Quads 0.20 .40 .60 .8
0
2
4
·104
Sampling Probability
Time Elapsed [ms]
Fig. 2. Accuracy of estimated N-Quads compared to the true value, indicated by a red
line, at 1,058,181 N-Quads (left) and elapsed time (right) of the Result Size Estimator
on the 100k Genomic dataset using mapping rule 4POM combined with 5JOIN. (Color
ﬁgure online)
Our results show that the estimated N-Quads follow an exponential decay
as a function of the sampling probability and converge to the true value. The
exponential decay is a result of diminishing returns in accuracy gains as the prob-
ability of sampling, and therefore the representativeness of the sample, increases;
initially, small increases in probability yield signiﬁcant improvements in estima-
tion accuracy. However, as the probability and representativeness continue to
increase, the incremental accuracy gains slow down. On the other hand, the
execution time increases linearly with the sampling probability, which is to be

FlexRML: A Flexible and Memory Eﬃcient Knowledge Graph Materializer 49
expected since a doubling of the sampling probability results in twice as much
data in the sample and thus requires roughly twice as much processing time.
In general, a higher sampling probability increases the accuracy of the esti-
mated N-Quads, but at the cost of increased computational time. Conversely,
lower sampling probabilities provide the beneﬁt of faster estimation, but at the
cost of reduced accuracy. Balancing these tradeoﬀs, FlexRML chooses a default
sampling probability of 0.2.
5.2 Performance of Adaptive Hash Function Selection
To address R2, we evaluated FlexRML using an adaptive bit size selection for
the hash algorithm and compared it to FlexRML
128, which represents a naive
approach where a 128-bit hash function is used uniformly for all hash algorithms.
The evaluation is performed on the cloud platform described in Table 1.F o r
the SDM Genomic dataset, the RML mapping for 1POM is used. All mapped
datasets produce the same output using both implementations, i.e. there are no
hash collisions.
Fig. 3. Elapsed time (left) and peak memory usage (right) for FlexRML with Adaptive
Hash Size (Blue) vs. FlexRML with Fixed 128-bit Hash Size (Red). (Color ﬁgure online)
The results show that the execution time of FlexRML 128 is consistently
shorter compared to that of FlexRML (see Fig.3, left diagram). This outcome is
expected, as the algorithms used in the Result Size Estimator require additional
processing time. However, as depicted in the right diagram of Fig. 3,F l e x R M L
shows lower memory consumption when performing the mapping on all datasets,
except in the case of the GTFS500 dataset, where both approaches require a 128-
bit hash function. For instance, when mapping the GTFS100 dataset FlexRML
requires about 1 GB less memory.

50 M. Freund et al.
The evaluation shows that when a 128-bit hash function is unnecessary, the
use of the Result Size Estimator can reduce the peak memory usage. However,
this beneﬁt is accompanied by an increase in processing time.
5.3 Comparison with Existing RML Processors
We perform a comparative analysis of FlexRML on three diﬀerent platforms, as
s h o w ni nT a b l e1: a virtual machine representing a cloud environment, a Rasp-
berry Pi 4 representing an edge node, and an ESP32 microcontroller representing
an embedded real-time IoT device. Note that the ESP32 has 512 KB of RAM,
of which 300 KB are accessible to the heap. The comparison is made against
other state-of-the-art RML processors, speciﬁcally Morph-KGC [ 4] and SDM-
RDFizer [10]. Both RML processors are primarily implemented in Python, but
use libraries written in C/C++ or Rust for performance-critical parts. When com-
paring FlexRML to the two RML processors, we took an outcome-based app-
roach, focusing on comparing results using two metrics: materialization speed
and memory usage, to evaluate KG materializers regardless of their implemen-
tation language. In the following, all ﬁgures have a logarithmic scale.
Fig. 4. Cloud: Elapsed time (top) and peak memory usage (bottom) for the SDM
genomic dataset over data sizes of 10k, 100k, and 1M.

FlexRML: A Flexible and Memory Eﬃcient Knowledge Graph Materializer 51
Cloud Environment. The data on elapsed time and peak memory usage
for the SDM Genomic dataset (Fig. 4), shows FlexRML’s better performance
than Morph-KGC and SDM-RDFizer in processing predicateObjectMaps with-
out join (POMs) or with self-join (REFs), and smaller datasets. However, for
larger datasets, FlexRML is slower than Morph-KGC, and it is slower than both
Morph-KGC and SDM-RDFizer when processing large datasets with JOIN map-
ping rules. Despite this, FlexRML’s overall lower memory consumption across
all datasets is a considerable compensating factor.
Fig. 5. Cloud: Elapsed time (left) and peak memory usage (right) for the GTFS
Madrid benchmark using scale sizes of 10, 100, and 500.
In the GTFS Madrid benchmark (Fig.5), FlexRML shows comparable perfor-
mance to Morph-KGC in terms of processing time, while outperforming SDM-
RDFizer. In addition, FlexRML demonstrates higher memory eﬃciency than
the two other RML processors. The benchmarks show that FlexRML consis-
tently outperforms other leading RML processors in memory eﬃciency across
all datasets on cloud platforms. In situations where mappings consist entirely of
POMs, REFs, or joins that are substitutable by reference conditions, FlexRML
using the Result Size Estimator demonstrates processing speeds that are either
superior to or on par with competing processors.
Edge Environment. The results from the SDM genomic dataset (Fig.6) eval-
uation at the edge are consistent with those observed in the cloud. FlexRML
shows greater memory eﬃciency and faster performance in mapping POMs or
REFs. But for JOIN mappings, FlexRML’s execution time exceeds that of the
other two RML processors. Notably, Morph-KGC was not able to process the
5JOIN operation on the 1M dataset, due to insuﬃcient memory of the edge.
In the case of the GTFS benchmark (Fig. 7), FlexRML again stands out,
showcasing the shortest execution time and the least peak memory usage. This
memory eﬃciency is signiﬁcant in the context of the GTFS100 dataset, where
FlexRML is the only RML processor evaluated that successfully maps the dataset
within the 4 GB RAM limitation of the Pi.

52 M. Freund et al.
Fig. 6. Edge Node : Elapsed time (top) and peak memory usage (bottom) for the
SDM genomic dataset. No bars indicate memory exhaustion and a process crash.
Fig. 7. Edge Node: Elapsed time (left) and peak memory usage (right) for the GTFS
Madrid benchmark. No bars indicate memory exhaustion and a process crash.
Device Environment. FlexRML is the only RML processor capable of running
on real-time microcontrollers due to its implementation in C++,s oo n l yF l e x R M L
can be evaluated. In the device environment, the RML processor can only use in-
memory data structures because the ESP32 microcontroller has no local storage,
therefore both the RML mappings and the data to be mapped were stored in
memory. Peak memory was measured by evaluating the heap memory used.

FlexRML: A Flexible and Memory Eﬃcient Knowledge Graph Materializer 53
Fig. 8. IoT Device: Elapsed time (left) and peak memory usage (right) for the RML-
SENSOR benchmark. Higher scales could not be mapped due to memory limitations.
The results in Fig. 8 show that FlexRML is capable of processing com-
plex RML mappings, including joins, in a simple microcontroller environment.
FlexRML can map up to 550 N-Quads, using the RML-SENSOR benchmark
and a scale factor of 55, with only about 250 KB of memory. Such performance
is considered suﬃcient and has the potential to enable semantic interoperability
at the device level.
6 The Resource FlexRML
FlexRML is designed with several key aspects in mind to maximize usability,
community adoption, and extensibility. These aspects include:
Availability. The FlexRML source code is actively maintained and publicly
available in a GitHub
10 repository. FlexRML is released under the open source
GNU AGPLv3 license. To ensure long-term accessibility and to support repro-
ducibility, all releases of FlexRML are archived on Zenodo. Our future plans
for FlexRML can also be found on the GitHub page. The roadmap outlines our
upcoming features and reﬂects our commitment to continuous improvement and
community engagement.
Novelty.FlexRML introduces a result size estimation technique for constructing
KGs. The result size estimation feature is particularly important for devices
with limited memory. Through this optimization and the implementation in
C++, FlexRML expands the range of devices capable of mapping non-RDF data
to RDF by focusing not only on unconstrained cloud environments, but also
on resource-constrained devices and microcontrollers, a domain not previously
explored by existing RML processors.
Reusability. FlexRML is designed with accessibility and ease of use in mind.
Documentation, usage examples, and conﬁguration ﬁles for various use cases are
available in the GitHub repository, making it easy to use the resource. To further
10 https://github.com/wintechis/ﬂex-rml.

54 M. Freund et al.
enhance user experience, prebuilt executables for multiple platforms are avail-
able. These executables align with the familiar process of installing or running
programs for many users. By oﬀering prebuilt versions, we eliminate the need
to set up a build environment or install a speciﬁc language interpreter, tasks
that require technical expertise. Each release of FlexRML is validated against
the latest RML test cases to ensure full compliance with the RML speciﬁcation.
Versatility.FlexRML uses a modular design that allows future enhancements,
including the ability to handle additional data types such as JSON and XML. To
handle each data encoding, a dedicated reader must be implemented. The reader
is responsible for converting the read data to FlexRML’s internal vector-based
data representation. The FlexRML core can also be adapted to speciﬁc needs,
as we have done with the CLI and ESP32 versions. The CLI version has an
additional C++ ﬁle that handles command line arguments and calls the correct
FlexRML functions based on the parameters, while the ESP32 version does not
need CLI argument processing, but rather uses microcontroller speciﬁc libraries
enabling, for example, serial communication.
7 Conclusion and Future Work
We introduced FlexRML, a ﬂexible and memory-eﬃcient resource for executing
RML mappings to materialize KGs on a variety of devices, spanning diﬀerent
levels of constraints. FlexRML expands the range of devices capable of producing
RDF, including those previously unable to run an RML processor. Our empirical
evaluation shows that using the result size estimation algorithm reduces memory
consumption compared to a naive ﬁxed bit size approach, by allowing the use
of smaller bit sizes in the hash function for duplicate removal without losing
output quads. Additionally we found that FlexRML, using the adaptive bit size
selection and memory advantages of C++, consistently shows lower peak memory
consumption across diﬀerent datasets when benchmarked against leading RML
processors, and oﬀers faster or comparable execution times. Looking ahead, our
future development eﬀorts will focus on implementing support for additional data
formats, with a particular focus on JSON, incorporating compliance with the new
RML speciﬁcation, and reducing the execution time of non-substitutable joins
by implementing join optimizations. In addition, an interesting future research
direction we want to explore is the combination of mapping partitions and result
size estimation to further improve memory eﬃciency.
Acknowledgements. This work was funded by the German Federal Ministry for
Economic Aﬀairs and Climate Action (BMWK) through the Antrieb 4.0 project (Grant
No. 13IK015B).

FlexRML: A Flexible and Memory Eﬃcient Knowledge Graph Materializer 55
References
1. Ahamed, J., Mir, R.N., Chishti, M.A.: RML based ontology development approach
in internet of things for healthcare domain. Int. J. Pervasive Comput. Commun.
17(4), 377–389 (2021)
2. Al-Osta, M., Ahmed, B., Abdelouahed, G.: A lightweight semantic web-based app-
roach for data annotation on IoT gateways. Procedia Comput. Sci. 113, 186–193
(2017)
3. Arenas-Guerrero, J., Chaves-Fraga, D., Toledo, J., P´erez, M.S., Corcho, O.: Morph-
KGC: scalable knowledge graph materialization with mapping partitions. Semant.
Web (Preprint) 1–20 (2022)
4. Arenas-Guerrero, J.: morph-kgc/morph-kgc: 2.6.4 (2023). https://doi.org/10.
5281/zenodo.10171377
5. Chaves-Fraga, D., Priyatna, F., Cimmino, A., Toledo, J., Ruckhaus, E., Corcho,
O.: GTFS-Madrid-Bench: a benchmark for virtual knowledge graph access in the
transport domain. J. Web Semant. 65, 100596 (2020). https://doi.org/10.1016/j.
websem.2020.100596
6. Daga, E., Asprino, L., Mulholland, P., Gangemi, A., et al.: Facade-X: an opinion-
ated approach to SPARQL anything. Stud. Semant. Web53, 58–73 (2021)
7. Das, S., Sundara, S., Cyganiak, R.: R2RML: RDB to RDF Mapping Language
(2012). https://www.w3.org/TR/r2rml/
8. Dasoulas, I., Chaves-Fraga, D., Garijo, D., Dimou, A.: Declarative RDF construc-
tion from in-memory data structures with RML (2023)
9. Dimou, A., Vander Sande, M., Colpaert, P., Verborgh, R., Mannens, E., Van de
Walle, R.: RML: a generic language for integrated RDF mappings of heterogeneous
data. In: 7th Workshop on Linked Data on the Web, vol. 1184 (2014)
10. eiglesias34, Chaves, D., et al.: SDM-TIB/SDM-RDFizer: v4.7.2.7 (2023). https://
doi.org/10.5281/zenodo.10101405
11. Freedman, D., Pisani, R., Purves, R.: Statistics. 4th edn. W. W. Norton & Co
(2007)
12. Ganzha, M., Paprzycki, M., Paw/suppresslowski, W., Szmeja, P., Wasielewska, K.: Towards
semantic interoperability between Internet of Things platforms. In: Integration,
Interconnection, and Interoperability of IoT Systems, pp. 103–127 (2018)
13. Hogan, A., et al.: Knowledge graphs. ACM Comput. Surv. 54(4) (2021). https://
doi.org/10.1145/3447772
14. Hozdi´c, E.: Smart factory for industry 4.0: a review. Int. J. Mod. Manuf. Technol.
7(1), 28–35 (2015)
15. Iglesias, E., Jozashoori, S., Chaves-Fraga, D., Collarana, D., Vidal, M.E.: SDM-
RDFizer: an RML interpreter for the eﬃcient creation of RDF knowledge graphs.
In: Proceedings of the 29th ACM International Conference on Information &
Knowledge Management, pp. 3039–3046 (2020)
16. Ioannidis, Y.E.: Query optimization. ACM Comput. Surv. (CSUR)28(1), 121–123
(1996)
17. Jabbar, S., Ullah, F., Khalid, S., Khan, M., Han, K., et al.: Semantic interoper-
ability in heterogeneous IoT infrastructure for healthcare. Wirel. Commun. Mob.
Comput. 2017 (2017)
18. Lakka, E., et al.: End-to-end semantic interoperability mechanisms for IoT. In: 2019
IEEE 24th International Workshop on Computer Aided Modeling and Design of
Communication Links and Networks (CAMAD), pp. 1–6. IEEE (2019)

56 M. Freund et al.
19. Lefran¸cois, M., Zimmermann, A., Bakerally, N.: A SPARQL extension for generat-
ing RDF from heterogeneous formats. In: Blomqvist, E., Maynard, D., Gangemi,
A., Hoekstra, R., Hitzler, P., Hartig, O. (eds.) ESWC 2017. LNCS, pp. 35–50.
Springer, Cham (2017). https://doi.org/10.1007/978-3-319-58068-5
3
20. Martino, A., Iannelli, M., Truong, C.: Knowledge injection to counter large lan-
guage model (LLM) hallucination. In: Pesquita, C., et al. (eds.) ESWC 2023. LNCS,
vol. 13998, pp. 182–185. Springer, Cham (2023). https://doi.org/10.1007/978-3-
031-43458-7
34
21. Megill, N.D., Pavicic, M.: Estimating Bernoulli trial probability from a small sam-
ple. arXiv preprint arXiv:1105.1486 (2011)
22. Moons, B., Sanders, F., Paelman, T., Hoebeke, J.: Decentralized linked open data
in constrained wireless sensor networks. In: 2020 7th International Conference on
Internet of Things: Systems, Management and Security (IOTSMS), pp. 1–6. IEEE
(2020)
23. Oo, S.M., Haesendonck, G., De Meester, B., Dimou, A.: RMLStreamer-SISO: an
RDF stream generator from streaming heterogeneous data. In: Sattler, U., et al.
(eds.) ISWC 2022. LNCS, vol. 13489, pp. 697–713. Springer, Cham (2022).https://
doi.org/10.1007/978-3-031-19433-7 40
24. Rodriguez-Muro, M., Rezk, M.: Eﬃcient SPARQL-to-SQL with R2RML mappings.
J. Web Semant. 33, 141–169 (2015)
25. S¸im¸sek, U., K¨arle, E., Fensel, D.: RocketRML - a NodeJS implementation of a
use-case speciﬁc RML mapper. arXiv preprint arXiv:1903.04969 (2019)
26. Vengerov, D., Menck, A.C., Zait, M., Chakkappen, S.P.: Join size estimation sub-
ject to ﬁlter conditions. Proc. VLDB Endow. 8(12), 1530–1541 (2015)
27. de Vleeschauwer, E., Min Oo, S., De Meester, B., Colpaert, P.: Reference condi-
tions: relating mapping rules without joining. In: KGCW 2023, the 4th Interna-
tional Workshop on Knowledge Graph Construction (2023)
28. Vu, B., Pujara, J., Knoblock, C.A.: D-REPR: a language for describing and map-
ping diversely-structured data sources to RDF. In: Proceedings of the 10th Inter-
national Conference on Knowledge Capture, pp. 189–196 (2019)
29. Wang, L.: Heterogeneous data and big data analytics. Autom. Control Inf. Sci.
3(1), 8–15 (2017)

IICONGRAPH: Improved Iconographic
and Iconological Statements
in Knowledge Graphs
Bruno Sartini(B)
Ludwig-Maximilians-Universit¨at M¨unchen, Munich, Germany
b.sartini@lmu.de
Abstract. Iconography and iconology are fundamental domains when it
comes to understanding artifacts of cultural heritage (CH). Iconography
deals with the study and interpretation of visual elements depicted in
artifacts and their symbolism, while iconology delves deeper, exploring
the underlying cultural and historical meanings. Despite the advances in
representing CH with Linked Open Data (LOD), recent studies show per-
sistent gaps in the representation of iconographic and iconological state-
ments in current knowledge graphs (KGs). To address them, this paper
presents IICONGRAPH, a KG that was created by reﬁning and extend-
ing the iconographic and iconological statements of ArCo (the Italian
KG of CH) and Wikidata. The development of IICONGRAPH was also
driven by a series of requirements emerging from research case studies
expressed in competency questions (CQs) that were unattainable in the
non-reengineered versions of the KGs. The evaluation results demon-
strate that IICONGRAPH not only outperforms ArCo and Wikidata
through domain-speciﬁc assessments from the literature but also serves
as a robust platform for answering the formulated CQs. IICONGRAPH
is released and documented in accordance with the FAIR principles to
guarantee the resource’s reusability. The algorithms used to create it and
assess the CQs have also been made available to ensure transparency and
reproducibility. While future work focuses on ingesting more data into
the KG, and on implementing it as a backbone of LLM-based question
answering systems, the current version of IICONGRAPH still emerges
as a valuable asset, contributing to the evolving landscape of CH repre-
sentation within KGs, the Semantic Web, and beyond.
Keywords: Knowledge Graph
· Iconography · Iconology ·
Symbolism · Cultural Heritage · Digital Humanities · Knowledge
Graph Generation
Resource type : Knowledge Graph
License: Creative Commons Attribution 4.0 International
DOI: https://doi.org/10.5281/zenodo.10294589
URL: https://w3id.org/iicongraph/
Documentation: https://w3id.org/iicongraph/docs/
c⃝ The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
A. Mero˜no Pe˜nuela et al. (Eds.): ESWC 2024, LNCS 14665, pp. 57–74, 2024.
https://doi.org/10.1007/978-3-031-60635-9_4

58 B. Sartini
1 Introduction
Using Linked Open Data (LOD) in the context of cultural heritage (CH) simpli-
ﬁes the organization, publication, connection, and reuse of knowledge within this
domain, and also provides a structure capable of expressing the complex rela-
tionships that can emerge between CH artifacts [13]. Over the years, numerous
Knowledge Graphs (KGs) have emerged that contain triples on CH, including
those referenced in [1,5–7,12,28]. While some serve a general purpose and deal
with various domains, others have been speciﬁcally crafted to incorporate and
represent information about CH. However, recent studies [4] demonstrate that,
in the artistic domains of iconography and iconology,
1 current KGs show two
main issues: (i) iconographic and iconological statements lack granularity or are
dumped2 in free text descriptions [25], and (ii) cultural symbolism3 is severely
underrepresented.
This paper addresses these gaps by presenting IICONGRAPH, a KG devel-
oped from the iconographic and iconological statements of Wikidata [ 28]a n d
ArCo [6], ﬁrst re-engineered following the ICON ontology [ 23] structure, and
then enriched with LOD on cultural symbolism taken from HyperReal [ 24].
These two KGs were chosen because they showed the greatest potential in the
evaluation work by Baroncini et al. [4], obtaining the highest scores for the cor-
rectness of their iconographic and iconological statements, while showing lim-
its when it comes to the level of granularity of these statements.
4 First, the
same evaluation is conducted on IICONGRAPH to demonstrate its superior
performance compared to the original sources, highlighting its impact through
quantitative assessments. Second, the research potential of IICONGRAPH is
tested by attempting to address domain-speciﬁc competency questions (CQs)
that remained unanswered with the original data from Wikidata and ArCo. The
rest of the paper is divided as follows. Section2 gives a background of the work
by presenting the resources included in IICONGRAPH, the ontology behind it,
and the limitations of the KGs that were chosen as the initial data sources.
Section3 follows by describing the development and release of IICONGRAPH.
In Sect. 4, IICONGRAPH is evaluated using the methodology proposed in [ 4].
The following Sect. 5 describes how the re-engineered KG can now be used to
1 Iconography is the study and interpretation of visual symbols and images, often
within the context of art or visual representation. It involves the identiﬁcation and
analysis of symbols, motifs, and elements within images in an artwork. Iconology
instead involves the interpretation of images in a broader cultural and historical con-
text, exploring the deeper layers of meaning, cultural ideologies, and socio-political
inﬂuences associated with visual representations [17].
2 Considering dumping as the phenomenon in which “important information for which
no appropriate ﬁeld was found, was forced as plain text inside a descriptive ﬁeld,
easy for humans to read but forever lost to any automatic tool” [2].
3 Intended as the set of symbolic meanings that some CH objects (or the elements
depicted in them) convey from speciﬁc cultural perspectives.
4 In the mentioned study, both KGs performed poorly on the “structure” evaluation,
which dealt with the possibility to diﬀerentiate between iconographic, iconological,
and symbolic subjects, among other criteria explained in Sect. 4.

IICONGRAPH 59
answer domain speciﬁc CQs. Section 6 contains a discussion reﬂecting on the
results of the quantitative and research-based evaluations. Then, Sect. 7 men-
tions related work about the generation of artistic KGs. Finally, Sect.8 contains
ﬁnal reﬂections on this work and mentions possible future work.
2 Background, Problem Statement, and Research
Requirements
In this section, the resources used to develop and enrich IICONGRAPH are
described. In the subsections about ArCo and Wikidata, their current issues in
the representation of artistic interpretation domain are highlighted.
2.1 ICON Ontology 2.0
ICON [23] is an ontology that conceptualizes artistic interpretations by formal-
izing the methodology of E. Panofsky [ 17]. According to Panofsky, when per-
forming an artistic interpretation, the interpreter can consider three levels. At
a pre-iconographic level, artistic motifs and their factual or expressional mean-
ings are recognized both as single entities and as groups (or compositions). The
recognition of a tree, of the action of running or the emotion of crying would
be considered pre-iconographical. At an iconographical level, the same motifs
are now recognized as what Panofsky calls images, and these images represent
characters, symbols, personiﬁcations, speciﬁc places, events or objects (such as
Rome, World War II, and Thor’s Hammer). At the same level, the artwork can be
seen as depicting a story or an allegory (Panofsky uses “Invenzione” as a general
term conveying both stories and allegories). At an iconological level, the artworks
are then analyzed in comparison with the cultural context in which they were
created, and they become a vessel to convey more in-depth cultural meanings or
representing cultural values or cultural phenomena. ICON was updated (in ver-
sion 2.0) to include three shortcuts that directly link an artwork to the element
of pre-iconographic, iconographic or iconologic levels that it depicts or represents
[22]. For a more comprehensive overview of ICON, refer to the documentation of
IICONGRAPH
5 or to previous publications on the ontology [22,23]. The classes
and properties of ICON used in this work are displayed in Fig.1.
2.2 HyperReal
HyperReal is a KG that contains more than 40,000 instances of symbolism,
also called simulations. A simulation is a connection between a symbol (like a
cat) and its symbolic meaning (such as divinity) in a particular cultural con-
text (e.g. Egyptian). HyperReal information comes from various sources such
as symbols dictionaries [15], and encyclopedias [16] and is structured according
to the Simulation Ontology framework. Figure 2 shows the graphical rendering
of the cat-divinity simulation. The KG is available through its data dump at
5 https://w3id.org/iicongraph/docs/.

60 B. Sartini
Fig. 1. Graphical Rendering of the ICON ontology classes and properties used in
IICONGRAPH. The shortcuts of ICON 2.0 are red, imported classes are violet. (Color
ﬁgure online)
https://w3id.org/simulation/data. HyperReal data are aligned with the corre-
sponding Wordnet [9] and Babelnet [14] synsets to facilitate the process of align-
ing external data with its symbols and symbolic meanings [ 21]. HyperReal has
been used in the back end of CH-related applications [26], and as a data source for
quantitative comparative cultural studies [27]. In the context of IICONGRAPH,
it is used to enrich the potential symbolism of artworks. For instance, a painting
depicting a cat could be interpreted from an Egyptian point of view as symbol-
izing divinity. This kind of inference is agnostic from the intention of the creator
of the work of art, but contributes to its understanding from a polyvocal and
multicultural perspective.
Fig. 2. Graphical Rendering of the cat-divinity simulation following the Simulation
Ontology schema. The Simulacrum is the speciﬁc term used to represent symbols,
while Reality Counterpart is the term used to represent symbolic meanings.

IICONGRAPH 61
2.3 Wikidata
Wikidata [28] is a user-generated, open, comprehensive knowledge base, launched
in 2012 by the Wikimedia Foundation, with a wide selection of content, available
in various levels of detail and formats. It provides a platform for collaboration,
sharing, integration, and a technology system for creating linked data. In the
Digital Humanities domain, it is often used to annotate and improve project
components, curating metadata to reﬁne the interoperability of authority and
local data sets about CH [ 30]. In the context of this work, the main focus was
on the subset of Wikidata’s statements regarding artworks and their depictions
(the extraction methodology is explained in Sect. 3).
Wikidata Analysis and Problem Statement. When analysing the limita-
tions of Wikidata’s iconographic and iconological statements, the main focus is
on the propertydepicts (wdt:P180) and its qualiﬁers. This property links an art-
work with an element depicted in it. Its qualiﬁers, such as wears (wdt:P3828),
and expression, gesture, or body pose (wdt: P6022), give more context to the
depicted element. On the one hand, Wikidata contains more than 372,000depicts
statements
6 when the subject is a painting (wd:Q3305213), which is a great start-
ing point for digital art history studies. On the other hand, this property is used
for all three levels of interpretations, ﬂattening the expressivity of those state-
ments. When it comes to expressing symbolism, there are some exceptions. For,
instance symbolizes (wdt:P4878) is a qualiﬁer of depicts that links a depicted
element to what it symbolizes. However, the property is rarely used (only 63
statements related to paintings).
7 Therefore, the main issue with Wiki-
data is that when the data are present, the schema is lacking, and
when the schema is present, the data are lacking.
Formulation of Competency Questions for Wikidata. Following the pre-
vious statements, in Wikidata it is not possible to retrieve what the most
symbolic paintings are and how many serendipitous symbolic connections exist
between paintings. Serendipitous connections are deﬁned here as
“all the new connections that emerged between artworks in Wikidata,
caused by the shared symbolic meaningonly. [...]For example, if Painting
A and Painting B both depict a heart, they will share the potential sym-
bolism of love because they share the same symbol, this would not be a
serendipitous connections. Contrarily, if Painting A contains a heart and
painting C contains a red rose, they share the symbolic meaning of love
without sharing the same symbol, which leads to a serendipitous discov-
ery” [21].
6 Query last run in December 2023: https://qlever.cs.uni-freiburg.de/wikidata/
yKhv77.
7 Query last run in December 2023: https://w.wiki/8QyF.

62 B. Sartini
By using the current data in Wikidata, zero serendipitous connections emerge.8
At the same time, it is also currently challenging to distinguish between the pre-
iconographical and the iconographical elements depicted in Wikidata’s paintings,
a task that becomes even more diﬃcult if the objective is distinguishing between
the speciﬁc types of iconographical subjects (characters, places, attributes, etc.)
Given these premises, the following CQs have been formulated and will be
answered in IICONGRAPH.
CQ1. How many serendipitous connections exist among artworks in Wikidata?
CQ2. Which artworks are associated with the most symbolic meanings?
CQ3. How are pre-iconographic and iconographic depictions distributed across
Wikidata’s depicts. statements in paintings?
CQ4. Among iconographical elements, which are the main classes (characters,
places, attributes) that emerge as the most frequent?
Regarding CQ1 and CQ2, I hypothesize that after enriching Wikidata with
HyperReal, the number of serendipitous connections will substantially increase,
and after that it will be possible to rank Wikidata’s painting according to their
symbolic temperature . Addressing CQ3 and CQ4, the hypothesis is that by re-
engineering the statements in Wikidata according to the ICON ontology, it will
be possible to distinguish and measure the distribution of pre-iconographic and
iconographic elements.
2.4 ArCo
ArCo [6] is a KG that describes a wide spectrum of artifacts from the Italian
CH, containing items belonging to the architectural, ethnographic, and artistic
domains. It follows the structure of the ArCo ontology, spread into diﬀerent
modules to address diﬀerent levels of description of CH. In the context of this
work, only a subset of statements related to artworks (which belong to the class
HistoricalOrArtisticProperty) will be considered, with more limitations that will
be explained in the following subsection.
ArCo Analysis and Problem Statement. ArCo was created by applying
Natural Language Processing algorithms to the OCR (Optical Character Recog-
nition) version of printed catalogs. Consequently, even if some of the more techni-
cal information was converted into URIs and single nodes in the KG, a great deal
of free-text information remains, especially about subjective domains like icono-
graphic readings. Therefore, most of the information regarding iconographical
and iconological statements is dumped in a free-text description, not exploiting
the full potential of LOD. On the one hand, this puts ArCo in a worse starting
position compared to Wikidata, which expresses almost all of the information
through URIs and limits the free-text ﬁelds. On the other hand, some of the
8 Query last run in December: https://w.wiki/6BZR.

IICONGRAPH 63
descriptions in ArCo contain detailed interpretations about artworks, even sep-
arating pre-iconographic subjects from iconological meanings conveyed by art-
works. Additionally, the descriptions have a schematic structure with repeating
patterns, especially those related to a series of Italian billboards created in the
20th century. In the current version of ArCo, it is challenging to study the cor-
relations between speciﬁc iconographic and pre-iconographic subjects and the
cultural event/product they promote (iconological level).
Formulation of Competency Questions for ArCo. Given that the starting
point of ArCo is worse compared to Wikidata, only one CQ was formulated,
namely:
CQ5. What are the most common iconological meanings associated with Italian
Billboards from the 20th century?
The hypothesis is that by transforming the free-text description into structured
data following ICON, it will be possible to isolate and then measure the frequency
of iconological meanings.
3 IICONGRAPH Development and Release
This section describes how IICONGRAPH was developed and released. Diﬀerent
strategies were adopted for the development according to the issues mentioned
in Sect. 2 for the two sources. The main distinction between the two sources
is that while Wikidata provides information about the potential relationships
between depicted entities (via the qualiﬁers), requiring a full description using
the ICON ontology, ArCo’s descriptions are very linear; therefore, only the short-
cuts introduced in ICON 2.0 are necessary to describe such information.
9 For
both KGs, the generation of the re-engineered LOD was performed in a Python
environment via the RDFlib package.10
3.1 Wikidata’s Conversion
The general pipeline adopted to convert Wikidata was (i) assigning the depicted
entities to the classes of ICON, (ii) extracting data about paintings, (iii) align-
ing them with HyperReal, and then (iv) re-engineering the statements following
the ICON ontology. To align Wikidata’s depicted entities with ICON classes,
we adopted a methodology involving the annotation of the depicted entity types
and classes expressed in Wikidata through the propertiesinstance of (wdt:P31)
and subclass of (wdt:P279). Given the impracticality of manually annotating
more than 60,000 individual depicted entities, I focused on annotating the top
700 classes and types, ordered by the number of depicted elements assigned to
9 This decision is supported by the work that presents ICON 2.0 [22], in which ArCo’s
descriptions are a use case example for ICON 2.0.
10 https://rdﬂib.readthedocs.io/en/stable/.

64 B. Sartini
them. The top 700 covered more than 85% of the total entities. To ensure objec-
tivity, a no-ambiguity policy guided the single annotator. Each type or class was
analyzed on Wikidata using a SPARQL query to verify that all related entities
could match the designated ICON class; otherwise, the type or class was dis-
carded. The alignment is not made because of a shared or similar label between
the classes of Wikidata and ICON, but rather by choosing the best ICON class
to represent the instances of the Wikidata class. For example, the instances
of the class big city wd:Q1549591 would be modelled, using ICON, with the
icon:Place class. Subsequently, all the depictions of big cities will be described
in ICON using an icon:IconographicalRecognition. At the same time,
other classes of Wikidata which have been aligned to icon:NaturalElement
will make all the elements that belong to classes recognized in ICON via a
icon:PreiconographicalRecognition. Figure 3 illustrates the distribution of
assigned classes and types for pre-iconographical and iconographical elements.
After this alignment, the information about the paintings, their depicted ele-
ments, the types and classes of the depiction, and their qualiﬁers were extracted
via a SPARQL query. A total of almost 150,000 paintings and their related meta-
data were extracted. To align Wikidata’s entities with HyperReal’s symbols for
the enhancement, an alignment done in previous work was reused [26]. The con-
version of Wikidata yielded more than 29,000,000 triples. More than 3,000,000
symbolic interpretations were inferred, due to the alignment to HyperReal, with
an average of around 20 interpretations per painting. For a more detailed descrip-
tion of Wikidata’s conversion, refer to the documentation.
Fig. 3. On the left: manual matching result between Wikidata’s types and classes and
ICON’s classes related to pre-iconographical elements. On the right: manual matching
result between Wikidata’s types and classes and ICON’s classes related to iconograph-
ical elements.
3.2 ArCo’s Conversion
For the conversion of ArCo, only the shortcut version of ICON was necessary,
eliminating the need to assign elements from free-text descriptions to individ-
ual ICON classes. Instead, the depicted elements were categorized into the

IICONGRAPH 65
macrogroups of pre-iconographical, iconographical, and iconological. The pro-
cess involved extracting ArCo’s data using a regex pattern to capture “Icono-
graphic Reading:” (in Italian, “Lettura Iconograﬁca:”) in artwork descriptions
linked via the Dublin Core description property ( dc:description). Following
the extraction of approximately 23,000 artworks and their descriptions (about
1% of ArCo’s total number of artworks), the structure of the descriptions was
analyzed to identify other patterns to facilitate the automatization of the con-
version. It was noticed that standard descriptions are organized into categories
separated by a standard use of punctuation. All descriptions that did not meet
this standard were discarded (around 3,000). All iconological meanings, in the
context of billboards, were determined to be after the category “Product cate-
gory/type of event” (in Italian, “Categoria Merceologica/tipo di evento”), where
the promotional aspect was described. Ambiguous categories (such as “Names”,
which included both the people depicted in the billboards but also the CEOs of
the companies that were getting promoted) were excluded, and a straightforward
approach was employed to distinguish between pre-iconographical and icono-
graphical levels. If an element in the description was written with a capital let-
ter, it was assigned to the iconographic level, otherwise to the pre-iconographical
level. Figure 4 visually shows the rationale behind the assignment and parsing
of descriptions, exempliﬁed by the artwork available at https://w3id.org/arco/
resource/HistoricOrArtisticProperty/0500659063. Before conversion, all descrip-
tions were translated into English using the Google Translate API. Given the
simplicity of the texts, this translation did not generate evident errors. Single
elements were linked to HyperReal through string matching. In summary, the
description from ArCo were translated and then analysed by a simple parser
that separates the categories with the punctuation, and then isolates each single
element of each description category considering it an iconographical element
if written with uppercase or pre-iconographical if lower case. The conversion of
ArCo yielded 767,888 triples, which is signiﬁcantly less than Wikidata because of
the diﬀerence in number of artworks (150,000 against 20,000), and also because
the simpliﬁed version of ICON is much less verbose. A total of 457,747 automatic
interpretations were generated due to the match with HyperReal.
3.3 IICONGRAPH Release
IICONGRAPH was released according to the FAIR principles [ 29]. The w3id
service was used to obtain persistent URIs for the namespace https://w3id.
org/iicongraph/data/, documentation https://w3id.org/iicongraph/docs/ and
analysis related to the research case studies https://w3id.org/iicongraph/
casestudies/. The same information is accessible via the GitHub repository
https://github.com/br0ast/iicongraph/. The preﬁxiig, used in the KG, was reg-
istered in http://preﬁx.cc. The KG is stored in Zenodo, accessible via https://
zenodo.org/doi/10.5281/zenodo.10294588. The metadata about the dataset and

66 B. Sartini
Fig. 4. Visual Example of a standard description in ArCo and the parsing steps applied
to it
the provenance of the data is deﬁned in a separate ﬁle 11 following the DCAT
standard.12 The ICON ontology used as its schema also respects the FAIR prin-
ciples, obtaining a score of 90% on the FOOPS tool [11].
4 Quantitative Evaluation
In this section, IICONGRAPH is quantitatively evaluated following the method-
ology deﬁned by [4]. Three versions of IICONGRAPH will be evaluated, namely
IIC-arco, which contains only the re-engineered statements from ArCo, IIC-
wikidata, which contains only the re-engineered statements from Wikidata, and
IIC-global, containing all the triples. The assessment method considers six cri-
teria, divided into two macro-areas: content and structure. Content considers
the evaluation of the correctness of artistic interpretation statements (CR1),
and the evaluation on the completeness of artworks interpretations (CR2) (i.e.,
whether the interpretation mentions, when needed, pre-iconographical, icono-
graphical, and iconological statements). Then, structure addresses the richness
of the schema describing the artworks (CR3), the entity linking of artworks
with external sources is measured by CR4, CR5 measures how the URIs of the
depicted subjects are linked within the same dataset (in technical terms, the
outdegree of the subjects’ nodes in a graph) and CR6 measures the number of
references to external taxonomies of art and culture. All categories are given a
weight (CR1,2,3 have a weight of 1, CR4,5 have a weight of 0.6 and CR6 has a
weight of 0.8) and the possible scores for each go from 0 to 1. Given the reengi-
neering tasks performed to create IICONGRAPH, this work could only inﬂuence
the criteria CR2, CR3, CR5 as it does not deal with changing wrong interpreta-
tions (CR1), linking artworks between diﬀerent datasets (CR4), or referring to
external taxonomies of art and culture (CR6).
Following the methodology presented in [4], CR2 was calculated by averaging
the scores of two annotators that evaluated the description of 100 artworks. The
annotators had to decide how many interpretation levels they expected for the
artwork. The general guidelines of [ 4] say that artworks depicting a landscape
usually are only interpreted via a pre-iconographical level, most portraits have
11 https://github.com/br0ast/iicongraph/blob/main/data/IICONGRAPH catalogue.
ttl.
12 https://www.w3.org/TR/vocab-dcat-3/.

IICONGRAPH 67
both pre-iconographical and iconographical meanings, and allegorical, religious,
and culturally relevant scenes (depiction of wars, special events for a country
or culture) can usually be described using all levels. After averaging the evalu-
ation, IIC-global obtained 0.92, IIC-arco 0.958 and IIC-wikidata 0.97. CR3 was
calculated through a comparison of the ICON ontology structure with the gold
standard in [4]
13. Given that the schema behind IICONGRAPH is the ICON
ontology, developed to describe all the information mentioned in the gold stan-
dard, the score of all the versions of the KG in this category was set at 1. CR5
was computed via SPARQL queries on the data, ﬁrst counting how many sub-
jects in the data were linked to at least more than 1 artwork, and then dividing
this number by the total number of subject recognized. The scores obtained
are 0.5771 for IIC-arco, 0.4573 for IIC-wikidata and 0.4337 for IIC-global. Since
CR1, CR4, and CR6 were not aﬀected by the changes, IIC-wikidata and IIC-
arco maintain their scores of [4], while IIC-global receives an average of the two
scores. Table1 shows the scores compared to the other datasets analyzed in [4].
In Sect.6 the results are analyzed and discussed. All scripts and queries related
to the quantitative evaluation are available in the documentation at https://
w3id.org/iicongraph/docs/.
Table 1. Overall results of the quantitative evaluation applied to IIC-global, IIC-
wikidata, and IIC-arco compared to the results in the state of the art performed in [4].
UF labeled criteria signal that they were not aﬀected by the changes. Ranking signals
only the overall top 3 for each category.
CR1 UF CR2 CR3 CR4 UF CR5 CR6 UF Content Rank Cont Structure Rank Structure Overall Rank overall
IIC-global 0.9023 0.92 1 0.3508 0.4737 0.1404 0.9111 2 0.5357 2 0.7234 2
IIC-arco 0.8278 0.958 1 0.0026 0.5771 0.1238 0.8929 3 0.4823 3 0.6876 3
IIC-wiki 0.9768 0.97 1 0.699 0.4573 0.157 0.9734 1 0.6065 1 0.7899 1
ArCo 0.8278 0.74 0.3333 0.0026 0.172 0.1238 0.7839 0.1790 0.4815
Wikidata 0.9768 0.74 0.6667 0.699 0.367 0.157 0.8584 0.4773 0.6678
Fondazione Zeri 0.9925 0.5117 0.1111 0.0005 0.266 0.5449 0.7521 0.2356 0.4939
Nomisma 0.9768 0.5 0.2222 0 0.749 0.0001 0.7384 0.2239 0.4811
SARI 0.849 0.3783 0.1111 0.997 0.5 0 0.6136 0.3364 0.475
Europeana 0.4688 0.236 0.1111 0.0073 0.6122 1 0.3524 0.4276 0.39
ND Hungary 0.13 0.5392 0.1111 0 0 0 0.3346 0.037 0.1858
DBpedia 0.655 0.7242 0.2222 0.994 0.41 0 0.6896 0.3549 0.5222
Yago 0.99 0.4825 0.1111 1 0.1675 0 0.7362 0.2705 0.5034
5 Research-Based Evaluation
This section shows how IICONGRAPH can be used to answer the CQs formu-
lated in Sect.2. Regarding CQ1 and CQ2, the methodology consisted of extract-
ing the data on paintings and their symbolic depictions through a SPARQL
query performed on IIC-wikidata. Around 79,000 paintings were associated with
13 In summary, a perfect schema would be able to describe actions, preiconographical
elements, stories, allegories, iconographical subjects, symbols, iconological subjects,
cultural phenomena, and should be able to be used in combination with a taxonomy
or controlled vocabulary of art and culture.

68 B. Sartini
a symbolic meaning shared by more than one symbol. Artwork connections were
computed using Python, with an iterative process comparing each depicted ele-
ment between pairs of paintings. The calculation involved determining how many
symbolic meanings were shared between the depicted elements of the pairs.
At the end of the calculation, 2,481,489,938 serendipitous connections
were exposed . CQ2 was tackled with a SPARQL query, revealing the top
10 most symbolic paintings. “Entrance into the Ark” (wd:Q209050) by
Jan Brueghel The Elder tops the list with almost 1,500 associated simula-
tions; the rest of the top 10 are detailed in Table2. In general, paintings with a
multitude of animals and plants were associated with most symbolic meanings.
Similarly, simple SPARQL queries facilitated the examination of the distribu-
tion of pre-iconographic and iconographic representations in Wikidata (CQ3,
CQ4), revealing that 64.86% of the depicted elements belong to the pre-
iconographical level . Among iconographic elements, Characters are the
most recognized, with almost 100,000 occurrences . The results of this
analysis are presented in Table 3. CQ5 followed a similar approach. Through
a SPARQL query on IIC-arco, the number of paintings associated with each
iconological meaning was determined. The top 10 iconological meanings are pre-
sented in Table 4. In particular, the iconological meaning most referred
to in 20th century billboards is the promotion of tourism . In summary,
post-reengineering and enrichment, all CQs formulated in Sect.2 were eﬀectively
answered. All scripts and queries developed to address these CQs are provided at
https://w3id.org/iicongraph/casestudies to ensure the transparency and repro-
ducibility of the results.
Table 2. Top 10 of the most symbolic paintings in Wikidata, retrieved by a SPARQL
query performed on IICONGRAPH. wd: is the preﬁx for https://www.wikidata.org/
wiki/entity/
Painting ID Painting Label Sim#
wd:Q66107722 Entrance into the Ark 1,488
wd:Q18809786 Entry into Noah’s Ark 998
wd:Q321303 The Garden of Earthly Delights 851
wd:Q27980267 Unknown Title 758
wd:Q2510869 Concert in the Egg 747
wd:Q463392 Paradiesg¨artlein 723
wd:Q20170089 The Ark 723
wd:Q18917077 T h eG a r d e no fE d e na n dt h eC r e a t i o no fE v e721
wd:Q29656879 Earth or The Earthly Paradise 706
wd:Q18573212 The Animals Entering Noah’s Ark 662

IICONGRAPH 69
Table 3. Distribution of Pre-iconographical and Iconographical statements in Wikidata
extracted from IIC-wikidata
Level of interpretation Total Unique Speciﬁc Element Total Unique
Pre-iconographical 224,981 5,131 natural elements 220,463 4,938
actions 4,189 147
expressions 4,667 65
Iconographical 121,893 37,667 characters 98,354 27,847
events 817 399
stories 3,436 3,436
attributes 791 51
places 17,050 5,438
Table 4. Top 10 iconological meanings associated with the most artworks in ArCo
Iconological Meaning Artwork #
iig:promotionOfTourism 4,572
iig:promotionOfExhibitions 3,604
iig:promotionOfTourismPromotionBodies 3,380
iig:promotionOfInformationAndCommunication 2,932
iig:promotionOfFoodIndustry 2,814
iig:promotionOfCulturalEvents 2,219
iig:promotionOfTransport 2,211
iig:promotionOfSport 1,928
iig:promotionOfTrade 1,911
iig:promotionOfAgriculture 1,694
6 Discussion of the Results
After a thorough quantitative evaluation, the performance of IIC-global, along
with its subsets IIC-wikidata and IIC-arco, outperforms the rest of the KGs
examined in [4] in both structure and content scores. The eﬀectiveness of the
re-engineering process is evident in the signiﬁcant improvements observed, par-
ticularly in CR5 (subject intralinking potential) for ArCo, where it experienced
an impressive increase (more than 300%) from 0.172 to 0.5771. This increase
is due to the generation of more subjects expressed in URIs, which increases
the number of connections between artworks that share the same subject (now
defereanceable compared to the previous text-only version).
The best-performing KG overall is IIC-wikidata, similarly to when the stan-
dard version of Wikidata was the top performer before the re-engineering process.
Notably, despite the enhancements, ArCo still falls short in the structure crite-
ria, with an overall structure score of less than 0.5. This limitation is attributed

70 B. Sartini
to issues such as references to external taxonomies and the alignment challenges
between its artworks and those present in other KGs.
When it comes to the evaluation of research-driven CQs, IICONGRAPH
shows great potential for domain-speciﬁc analyses, although these results are
considered preliminary and show some limitations. In fact, the automatic sym-
bolic interpretations of artwork from a polyvocal point of view (given by Hyper-
Real) could be the starting point for more in-depth analysis for art historians,
as they only represent potential, creator-agnostic symbolic meanings. Moreover,
Table 4 displays elements that could be merged after performing entity dis-
ambiguation (i.e., promotion of tourism and promotion of tourism promotion
bodies). Despite this, the results underscore the considerable advancement rep-
resented by IICONGRAPH and its subgraphs. They not only outperform the
state-of-the-art quantitatively but also demonstrate their utility in addressing
CQs that were unattainable in the original versions of the KGs. The improve-
ments in both quantitative metrics and research potential underscore the signif-
icance of the re-engineering eﬀorts and the enriched representations provided by
IICONGRAPH.
7 Related Work
This section provides an overview of the development of artistic KGs or related
resources, highlighting diﬀerences from IICONGRAPH. Artgraph [ 7]i saK G
developed by combining data from DBpedia and Wikiart, including over 250,000
artworks and associated artists. Its objective is to integrate visual embeddings
and graph embeddings from the KG for automated art analysis. However, an
examination of Artgraph’s properties reveals the same issues found in Wikidata
and ArCo, such as the lack of granularity of iconographic and iconological state-
ments due to the absence of interpretative depth. The connection between art-
works and subjects relies on a generic “tag” property. Furthermore, the dataset
does not incorporate symbolic representation. ICONdataset [ 3] is a manually
annotated KG, containing more than 5,500 art historians’ interpretations about
more than 400 artworks. It shares with IICONGRAPH the adoption of the
ICON ontology as its primary schema. While manual annotation, as employed
by ICONdataset, aﬀords complete supervision over the data, ensuring a high
degree of accuracy, the inherent drawback lies in its time-consuming nature,
evident in the relatively low number of artworks and interpretations. In con-
trast, IICONGRAPH adopts a semi-automatic approach, resulting in a signif-
icant disparity in both the quantity of artworks and interpretations between
the two KGs. This distinction emphasizes the scalability and eﬃciency aﬀorded
by a semi-automatic process. Furthermore, IICONGRAPH’s incorporation of the
HyperReal enrichment introduces an additional layer of symbolic data, augment-
ing its comprehensiveness, reach, and potentialities in comparison to manually
annotated counterparts. MythLOD [18] is an LOD catalog that contains inter-
pretations of more than 4,000 mythological works. It was created by converting a
CSV manually populated by domain experts. Its main purpose is to represent in

IICONGRAPH 71
LOD both the methodology and rationale of the interpretations (iconographic,
hermeneutic) and the bibliographic sources which supported the interpretations.
However, when it comes to describing the main objects of the interpretations,
it relies on the standard Dublin Core
14 subject property ( dc:subject), which
is extremely limited compared to the possibilities oﬀered by the ICON ontol-
ogy behind IICONGRAPH. Other datasets, such as [1,8,12,19,20] are not men-
tioned, as they are compared to IICONGRAPH through the evaluation in Sect.4.
8 Conclusion and Future Work
This paper presented the development and evaluation of IICONGRAPH, a KG
created by re-engineering the iconographic and iconological statements of ArCo
and Wikidata. IICONGRAPH, IIC-arco and IIC-wikidata outperformed the
state-of-the-art of artistic KGs in both structure and content scores. Further-
more, the results of the requirements evaluation based on the CQs demonstrate
the suitability of IICONGRAPH to answer domain-speciﬁc artistic inquieres.
Future work is divided into two main areas. First, the expansion of IICON-
GRAPH involves ingestion of additional statements from more artistic KGs.
Second, in the realm of Large Language Models (LLMs), IICONGRAPH emerges
as a valuable resource for developing question answering and chat-based systems
focused on CH, addressing a gap identiﬁed in the literature regarding symbolic
and iconographic knowledge [10]. Additionally, the descriptions in ArCo and the
RDF generated to create IICONGRAPH hold promise as ﬁne-tuning arguments
for an LLM capable of autonomously generating intricate iconographic LOD
from free-text descriptions via prompts. Despite the narrow focus of IICON-
GRAPH in the ﬁeld of iconography and iconology, especially in the context of
linked open data, it can have an impact to attract interest in digital humanities
initiatives that deal with Semantic Web. One key impact of IICONGRAPH is its
potential as a valuable resource for applications dealing with cultural heritage
data. With structured data on over 170,000 artworks, IICONGRAPH provides a
rich source of information for reuse, facilitating nuanced analyses and interpre-
tations. Moreover, the growing ﬁeld of digital art history stands to beneﬁt from
IICONGRAPH’s structured data repository. Museums can leverage this resource
to enrich their digital collections; if some of their artworks are already included
in Wikidata, they can refer also to the IICONGRAPH version, allowing for more
robust and iconographically-centered searches, enhancing the discoverability and
interpretive potential of their artworks. Furthermore, IICONGRAPH serves as
a model for other underrepresented ﬁelds within LOD initiatives. By elevating
the discourse surrounding iconography and iconology, it can set a precedent for
the inclusion and recognition of other specialized domains, such as symbolism
in music or Egyptian iconographic data, fostering innovation and inclusivity
within the broader scholarly ecosystem. In conclusion, IICONGRAPH stands
as a robust and versatile resource that advances the understanding of artistic
interpretation within the domains of art history and digital humanities, and
14 https://www.dublincore.org/speciﬁcations/dublin-core/dcmi-terms/.

72 B. Sartini
also presents signiﬁcant implications for the evolving landscape of LLMs, oﬀer-
ing a promising avenue for further exploration and integration into the broader
context of CH research.
References
1. Auer, S., Bizer, C., Kobilarov, G., Lehmann, J., Cyganiak, R., Ives, Z.: DBpedia:
a nucleus for a web of open data. In: Aberer, K., et al. (eds.) ISWC ASWC 2007.
LNCS, vol. 4825, pp. 722–735. Springer, Heidelberg (2007). https://doi.org/10.
1007/978-3-540-76298-0 52
2. Barabucci, G., Tomasi, F., Vitali, F.: Supporting complexity and conjectures in
cultural heritage descriptions. In: Proceedings of the International Conference Col-
lect and Connect: Archives and Collections in a Digital Age, pp. 104–115. CEUR
Workshop (2021). http://ceur-ws.org/Vol-2810/paper9.pdf
3. Baroncini, S., Daquino, M., Tomasi, F.: Exploring iconographical and iconological
content in semantic data through art historians’ interpretations. In: La memoria
digitale. Forme del testo e organizzazione della conoscenza. Atti del XII convegno
annuale AIUCD, pp. 9–14. Siena (2023)
4. Baroncini, S., Sartini, B., van Erp, M., Tomasi, F., Gangemi, A.: Is dc:subject
enough? A landscape on iconography and iconology statements of knowledge
graphs in the semantic web. J. Documentation 79(7), 115–136 (2023). https://
doi.org/10.1108/JD-09-2022-0207
5. Bruno, E., Pasqual, V., Tomasi, F.: Odi and bacodi: a study on destini incrociati
by italo calvino with semantic web technologies. In: La memoria digitale. Forme
del testo e organizzazione della conoscenza. Atti del XII convegno annuale AIUCD,
p. 35. Siena (2023)
6. Carriero, V.A., et al.: ArCo: the Italian cultural heritage knowledge graph. In:
Ghidini, C., et al. (eds.) ISWC 2019. LNCS, vol. 11779, pp. 36–52. Springer, Cham
(2019). https://doi.org/10.1007/978-3-030-30796-7
3
7. Castellano, G., Digeno, V., Sansaro, G., Vessio, G.: Leveraging knowledge graphs
and deep learning for automatic art analysis. Knowl.-Based Syst. 248, 108859
(2022). https://doi.org/10.1016/j.knosys.2022.108859. https://www.sciencedirect.
com/science/article/pii/S0950705122004105
8. Daquino, M., Mambelli, F., Peroni, S., Tomasi, F., Vitali, F.: Enhancing semantic
expressivity in the cultural heritage domain: exposing the zeri photo archive as
linked open data. J. Comput. Cult. Herit. 10(4) (2017). https://doi.org/10.1145/
3051487
9. Fellbaum, C. (ed.): WordNet: An Electronic Lexical Database. Language, Speech,
and Communication, A Bradford Book, Cambridge (1998)
10. Garcia, N., et al.: A dataset and baselines for visual question answering on art. In:
Bartoli, A., Fusiello, A. (eds.) ECCV 2020. LNCS, vol. 12536, pp. 92–108. Springer,
Cham (2020). https://doi.org/10.1007/978-3-030-66096-3 8
11. Garijo, D., Corcho, O., Poveda-Villal´on, M.: FOOPS!: an ontology pitfall scanner
for the fair principles. In: Proceedings of the ISWC 2021 Posters, Demos and
Industry Tracks: From Novel Ideas to Industrial Practice co-located with 20th
International Semantic Web Conference (ISWC 2021). CEUR-WS, Online (2021).
https://foops.linkeddata.es/assets/iswc
2021 demo.pdf
12. Isaac, A., Haslhofer, B.: Europeana linked open data – data.europeana.eu. Semant.
Web 4(3), 291–297 (2013)

IICONGRAPH 73
13. Lodi, G., et al.: Semantic web for cultural heritage valorisation. In: Hai-Jew, S.
(ed.) Data Analytics in Digital Humanities. MMSA, pp. 3–37. Springer, Cham
(2017). https://doi.org/10.1007/978-3-319-54499-1 1
14. Navigli, R., Ponzetto, S.P.: BabelNet: building a very large multilingual seman-
tic network. In: Proceedings of the 48th Annual Meeting of the Association for
Computational Linguistics, pp. 216–225 (2010)
15. Olderr, S.: Symbolism a Comprehensive Dictionary, 2nd edn. McFarland, London
(2012)
16. Otto, A.F.: Mythological Japan: The Symbolisms of Mythology in Relation to
Japanese Art, with Illustrations Drawn in Japan, by Native Artists - Primar. Bib-
liolife DBA of Bibilio Bazaar II LLC, Charleston, SC, USA (2014). Google-Books-
ID: 0Ki8oAEACAAJ
17. Panofsky, E.: Studies in Iconology: Humanistic Themes in the Art of the Renais-
sance. Westview Press, Boulder (1972)
18. Pasqual, V., Tomasi, F.: Linked open data per la valorizzazione di collezioni cul-
turali: il dataset mythlod. AIB studi 62(1), 149–168 (2022). https://doi.org/10.
2426/aibstudi-13301. https://aibstudi.aib.it/article/view/13301
19. Rebele, T., Suchanek, F., Hoﬀart, J., Biega, J., Kuzey, E., Weikum, G.: YAGO: a
multilingual knowledge base from Wikipedia, Wordnet, and Geonames. In: Groth,
P., et al. (eds.) ISWC 2016. LNCS, vol. 9982, pp. 177–185. Springer, Cham (2016).
https://doi.org/10.1007/978-3-319-46547-0
19
20. Sabah, R., Sabah, Z.: Modeling nomisma ontology and comparing solutions for
uncertainty. Ph.D. thesis, Goethe University Frankfurt (2022)
21. Sartini, B.: Connecting works of art within the semantic web of symbolic
meanings. Ph.D. thesis, Alma Mater Studiorium, University of Bologna (2023).
https://doi.org/10.48676/unibo/amsdottorato/11020. http://amsdottorato.unibo.
it/id/eprint/11020
22. Sartini, B., Baroncini, S.: A comparative study of simple and complex art interpre-
tations in linked open data using icon ontology. In: Proceedings of the International
Workshop on Semantic Web and Ontology Design for Cultural Heritage co-located
with the International Semantic Web Conference 2023 (ISWC 2023). CEUR Work-
shop (2023). https://ceur-ws.org/Vol-3540/paper4.pdf
23. Sartini, B., Baroncini, S., van Erp, M., Tomasi, F., Gangemi, A.: Icon: an ontology
for comprehensive artistic interpretations. J. Comput. Cult. Herit. 16(3) (2023).
https://doi.org/10.1145/3594724
24. Sartini, B., van Erp, M., Gangemi, A.: Marriage is a peach and a chalice: modelling
cultural symbolism on the semantic web. In: Proceedings of the 11th on Knowl-
edge Capture Conference, K-CAP 2021, pp. 201–208. Association for Computing
Machinery, New York (2021).https://doi.org/10.1145/3460210.3493552
25. Sartini, B., Gangemi, A.: Towards the unchaining of symbolism from knowl-
edge graphs: how symbolic relationships can link cultures. In: Book of Extended
Abstracts of the 10th National AIUCD Conference, AIUCD, Pisa, pp. 576–580
(2021)
26. Sartini, B., Nesterov, A., Libbi, C., Brate, R., Shoilee, S.B.A., Daniil, S.: Mul-
tivocal exhibition: a user-centric application to explore symbolic interpretations
of artefacts from diﬀerent cultural perspectives. In: ExICE - Extended Intelli-
gence for Cultural Engagement Conference, Bologna (2023). https://spice-h2020.
eu/conference/papers/posters/ExICE23
paper 7072.pdf
27. Sartini, B., Vogelmann, V., van Erp, M., Gangemi, A.: Comparing symbolism
across Asian cultural contexts. In: Digital Humanities 2022 Conference Abstracts,

74 B. Sartini
pp. 358–361. DH2022 Local Organizing Committee (2022). https://dh2022.dhii.
asia/abstracts/567
28. Vrandeˇci´c, D., Kr¨otzsch, M.: Wikidata: a free collaborative knowledgebase. Com-
mun. ACM 57(10), 78–85 (2014). https://doi.org/10.1145/2629489
29. Wilkinson, M.D., et al.: The fair guiding principles for scientiﬁc data management
and stewardship. Sci. Data 3(1) (2016). https://doi.org/10.1038/sdata.2016.18
30. Zhao, F.: A systematic review of Wikidata in Digital Humanities projects. Digital
Scholarship in the Humanities (2022). https://doi.org/10.1093/llc/fqac083

VisionKG: Unleashing the Power
of Visual Datasets via Knowledge Graph
Jicheng Yuan1(B), Anh Le-Tuan1, Manh Nguyen-Duc1, Trung-Kien Tran2,
Manfred Hauswirth1,3, and Danh Le-Phuoc1,3
1 Open Distributed Systems, Technical University of Berlin, Berlin, Germany
{jicheng.yuan,anh.letuan,duc.manh.nguyen,manfred.hauswirth,
danh.lephuoc}@tu-berlin.de
2 Bosch Center for Artiﬁcial Intelligence, Renningen, Germany
TrungKien.Tran@de.bosch.com
3 Fraunhofer Institute for Open Communication Systems, Berlin, Germany
Abstract. The availability of vast amounts of visual data with diverse
and fruitful features is a key factor for developing, verifying, and bench-
marking advanced computer vision (CV) algorithms and architectures.
Most visual datasets are created and curated for speciﬁc tasks or with
limited data distribution for very speciﬁc ﬁelds of interest, and there is
no uniﬁed approach to manage and access them across diverse sources,
tasks, and taxonomies. This not only creates unnecessary overheads when
building robust visual recognition systems, but also introduces biases into
learning systems and limits the capabilities of data-centric AI. To address
these problems, we propose theVision K nowledge Graph (VisionKG),
a novel resource that interlinks, organizes and manages visual datasets
via knowledge graphs and Semantic Web technologies. It can serve as a
uniﬁed framework facilitating simple access and querying of state-of-the-
art visual datasets, regardless of their heterogeneous formats and tax-
onomies. One of the key diﬀerences between our approach and existing
methods is that VisionKG is not only based on metadata but also utilizes
a uniﬁed data schema and external knowledge bases to integrate, inter-
link, and align visual datasets. It enhances the enrichment of the seman-
tic descriptions and interpretation at both image and instance levels and
oﬀers data retrieval and exploratory services via SPARQL and natural
language empowered by Large Language Models (LLMs). VisionKG cur-
rently contains 617 million RDF triples that describe approximately 61
million entities, which can be accessed at https://vision.semkg.org and
through APIs. With the integration of 37 datasets and four popular com-
puter vision tasks, we demonstrate its usefulness across various scenarios
when working with computer vision pipelines.
Keywords: Computer Vision
· Knowledge Graph · Linked Data ·
Ontology · RDF
Resource Type: Datasets/Knowledge Graph
Repository: https://github.com/cqels/vision
Homepage: https://vision.semkg.org
License: MIT
© The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
A. Mero˜no Pe˜nuela et al. (Eds.): ESWC 2024, LNCS 14665, pp. 75–93, 2024.
https://doi.org/10.1007/978-3-031-60635-9_5

76 J. Yuan et al.
1 Introduction
Computer vision (CV) has made signiﬁcant advances, with visual datasets
emerging as a crucial component in developing robust visual recognition sys-
tems (VRSs). The performance of the underlying deep neural networks (DNNs)
is inﬂuenced not only by advanced architectures but also signiﬁcantly by the
quality of learning data [59]. There exist many open visual datasets, e.g., Ima-
geNet [9], OpenImage [26], and MS-COCO [31], which oﬀer a wide range of visual
characteristics in diﬀerent contexts to support the generalization capabilities of
DNNs.
However, a challenge arises as these datasets often come in varied data for-
mats and the quality of their taxonomies and annotations diﬀers signiﬁcantly.
Furthermore, labels used to deﬁne objects vary in diverse lexical deﬁnitions, from
structured lexical deﬁnitions, such as WordNet [ 32], Freebase [4], to unstruc-
tured plain text. This often leads to semantic inconsistencies across diﬀerent
datasets [ 28]. Additionally, the lack of semantic integration not only causes
unnecessary overhead in developing robust VRSs but also introduces biases in
learning systems, thereby constraining the potential of data-centric AI [45].
Although researchers and practitioners have made eﬀorts to unify visual
datasets [18,27,34], a systematic approach to understanding the features and
unifying semantics underlying visual datasets is yet to be achieved. For instance,
DeepLake [ 18] can access data from multiple sources in a uniﬁed manner,
however, it does not bridge the gap in semantics alignments across datasets.
Conversely, Fiftyone [34] can partially identify inconsistencies in annotations
and analyze data pipeline failures by interlinking metadata manually, while
this labor-intensive solution limits the eﬀectiveness of building computer vision
pipelines. While these works improve the performance of learning systems in
a data-centric manner, training DNNs with high-quality data from multiple
sources in a cost-eﬀective way remains a formidable challenge for researchers
and engineers [50].
To address the aforementioned data inconsistency problems, leveraging the
capabilities of Knowledge Graphs, which oﬀer a ﬂexible and powerful way
to organize and represent data that is comprehensible for both humans and
machines, we built a knowledge graph for visual data, named VisionKG, to sys-
tematically organize and manage data for computer vision. This graph is specif-
ically designed to provide uniﬁed and interoperable semantic representations of
visual data, seamlessly integrated into computer vision pipelines. Furthermore,
VisionKG interlinks taxonomies across diverse datasets and label spaces, pro-
moting a shared semantic understanding and enabling eﬃcient retrieval of images
that meet speciﬁc criteria and user requirements.
Additionally, our approach enables users to better explore and comprehend
relationships between entities using facet-based visualization and exploration
powered by a graph data model. Graph queries, facilitated by graph storage,
can be employed to create declarative training pipelines from merged computer
vision datasets, providing a convenient way to navigate and investigate pat-
terns among interlinked visual datasets such as KITTI [ 15], MS-COCO [ 31],
and Cityscapes [ 7]. Moreover, VisionKG enhances ﬂexibility in terms of data

VisionKG: Unleashing the Power of Visual Datasets via Knowledge Graph 77
representation and organization, ensuring rapid and eﬀortless access to essential
visual data information, thereby supporting developers and users in constructing
computer vision pipelines conveniently and eﬃciently.
Open Visual Datasets
Classification, Detection, Segmentation, Visual Relationship Detection
Heterogeneous
Annotated Rules
Downstream Toolkits & Applications
Pytorch, Tensorflow, MMDetection, Detectron2, TIMM
Unified Data
Schema
Ontology
Visual
Extractor
Diverse Data Formats 
(json, xml, npy, csv…)
Customized
Integrator
Metadata based
Retrieval Results
Linked Data
View
External
Knowledge
Bases
Visual
Knowledge
Graph
User
Requests
LLMs
Knowledge based
Retrieval Results
Traditional Data Routine
VisionKG  Data Routine
Fig. 1. Diﬀerences between VisionKG- and traditional-Data Pipelines
As illustrated in Fig. 1, VisionKG is constructed following the Linked Data
principles [3], adhering to the FAIR [ 51] and open science guidelines [ 5], and
encompasses a large range of data sources. These sources have been deﬁned
and maintained by the research community, as they are widely used and have a
signiﬁcant impact on the development of VRSs. Their popularity ensures that
they will be updated frequently and extended regularly. This makes VisionKG a
valuable resource for researchers and developers who require access to the latest,
high-quality image data with enriched semantics. Our main contributions are
summarized as follows:
– We provide a uniﬁed framework for representing, querying, and analyzing
visual datasets. By aligning diﬀerent taxonomies, we minimize the inconsis-
tencies among diﬀerent datasets.
– Datasets interlinked in VisionKG are made accessible through standardized
SPARQL queries, available via both a web user interface and APIs.
– We demonstrate the advantages of VisionKG through three use cases: com-
posing visual datasets with uniﬁed access and taxonomy through SPARQL
queries, automating training and testing pipelines, and expediting the devel-
opment of robust visual recognition systems.
– Currently, VisionKG comprises 617 million RDF triples that describe approx-
imately 61 million entities from 37 datasets, covering four popular computer
vision tasks.

78 J. Yuan et al.
The remainder of the paper is structured as follows: Sect.2 discusses related
work. Section4 presents the detailed steps to enforce the FAIR principles within
VisionKG that follow the Linked Data publishing practice. Section 3 describes
the infrastructure of the VisionKG framework. In Sect.5, we describe the exam-
ple use cases for VisionKG, e.g., accessing image data with enriched semantics,
thereby enhancing the data pipeline for computer vision through standardized
SPARQL queries. We present our conclusions in Sect.6.
2 Related Work
Limitations in Existing Computer Vision Datasets: Modern CV mod-
els are data-intensive and their eﬀectiveness is signiﬁcantly inﬂuenced by the
quality and diversity of the datasets employed. However, the majority of visual
datasets are typically limited to speciﬁc domains using heterogeneous taxonomies
and exhibit imbalanced class distributions, for example, KITTI [ 15] and MS-
COCO [31] datasets. To address these challenges, model-centric approaches, such
as [48,57], either employ a domain adapter or incorporate auxiliary models to
discern the distribution across diverse datasets. However, these solutions necessi-
tate additional computational resources and even lead to negative transfer. Data-
centric approaches, e.g., MSeg [27], manually unify and interlink datasets, albeit
at the cost of increased labor intensity. Moreover, existing visual content extrac-
tors [39] or data hubs such as Deep Lake [ 18], Hugging Face
1, OpenDataLab2
and MetaVD [53] are well-established data infrastructures for organizing datasets
from distinct web sources. However, these toolchains primarily rely on metadata,
lacking the ability to interlink images and annotations across datasets. In con-
trast, our framework leverages knowledge graphs and diverse external knowledge
bases, and adheres to the FAIR principles [51], enabling VisionKG to interlink
and extend visual datasets and tasks with semantically rich relationships.
Knowledge Graph Technologies in Computer Vision:Knowledge graphs
can augment real-world visual recognition with background knowledge, captur-
ing semantic relationships in images and videos through external knowledge and
facts [8,58]. Approaches such as KG-CNet [ 13] integrate external knowledge
sources like ConceptNet [ 43] to encapsulate the semantic consistency among
objects within images. Similarly, KG-NN [33] enables the conversion of domain-
agnostic knowledge, encapsulated within a knowledge graph, into a vector space
representation and enhances the model’s robustness against domain shift. How-
ever, these methods leverage external knowledge during- or post-learning proce-
dure, whereas our solution utilizes not only external knowledge bases but also
the knowledge inside interlinked datasets to alleviate the data inconsistency and
reduce learning bias. Hence, the enhanced semantics can render fruitful features
for integrated datasets beneﬁting from the interaction between diverse visual
features and external knowledge. Similarly, the approach proposed in [ 14]a n d
1 https://huggingface.co/docs/datasets/index.
2 https://github.com/opendatalab/opendatalab-python-sdk.

VisionKG: Unleashing the Power of Visual Datasets via Knowledge Graph 79
Fig. 2. FAIR for Visual Data Assets
[36] make use of Wikidata [46] to enable and interlink annotations for the Ima-
geNet [25] dataset. Beneﬁting from that external knowledge and facts, the data
quality has been improved, although these approaches are labor-intensive and
primarily target a speciﬁc dataset. The reusability of these approaches with
other extensive visual datasets, such as OpenImages [ 26] and Objects365 [ 42],
and knowledge bases like Freebase, have not been investigated so far. Approaches
proposed by [20,21]u s eW o r d N e t[32] noun hierarchies and bidirectional ontol-
ogy engineering to integrate pre-existing knowledge resources and the selection
of visual objects within images. In contrast, our VisionKG framework utilizes
diverse knowledge bases including WordNet [32], Wikidata [46], and Freebase [4]
to enrich the semantics at both image-level and instance-level. Additionally,
KVQA [41], another knowledge-based visual dataset employing Wikidata, is
restricted mainly to person entities, while our work interlinks various visual
datasets and numerous entities across diverse taxonomies and domains.
3 Uniﬁed Access for Integrated Visual Datasets
This section provides an overview of the VisionKG framework and the details
of the integrated visual datasets, and we demonstrate VisionKG’s capabilities
in providing uniﬁed access to those supported visual datasets with enriched
semantics, ultimately integrating various data sources with diﬀerent formats
and schemas into CV pipelines seamlessly.
3.1 VisionKG Architecture to Facilitate Uniﬁed Access
Figure3 illustrates the pipeline of creating and enriching the uniﬁed knowledge
graph of VisionKG for visual datasets. We start by collecting popular computer
vision datasets from the PaperWithCode platform
3. Next, we extract their anno-
tations and features across datasets using a Visual Extractor .W eu s et h eR D F
3 https://paperswithcode.com/datasets.

80 J. Yuan et al.
Fig. 3. Overview of VisionKG Platform
Mapping Language (RML) [10] to map the extracted data into RDF. RDF data
is generated using a Semantic Annotator implemented using RDFizer [19]. To
enhance interoperability and enrich semantics in VisionKG, we link the data with
multiple knowledge bases, such as WordNet [32] and Wikidata [36]. TheSemantic
Enrichment Reasoner expands the taxonomy by materializing the labels in each
dataset using the ontology hierarchy. For instance, categories like pedestrian
or man isSubClassOf person (Fig.2
2 ). Based on the interlinked datasets and
with the Semantic Enrichment Reasoner, users can access the data in VisionKG
in a uniﬁed way (Fig. 2 3 ). The SPARQL Engine maintains an endpoint for
users to access VisionKG eﬃciently. To simplify access to the data, we also built
a text-to-SPARQL parser into VisionKG’s GUI to translate user requests from
natural language into SPARQL using OpenAI APIs.
Moreover, VisionKG oﬀers a web interface that allows users to explore queried
datasets, such as visualizing their data distribution and their corresponding
annotations (https://vision.semkg.org/statistics.html).
3.2 Linked Datasets and Tasks in VisionKG
As of November 2023, VisionKG integrates the 37 most commonly used visual
datasets, across the tasks for visual relationship detection, image classiﬁcation,
object detection, and instance segmentation. Table1 provides an overview of the
datasets, images, annotations, and triples integrated into VisionKG. In total, it
encompasses over 617 million triples distributed among these visual tasks. To
enhance the eﬀectiveness of our framework for image classiﬁcation, we have inte-
grated both large benchmark datasets, such as ImageNet [9], as well as smaller
commonly used datasets, like CIFAR [ 24]. The diversity of covered datasets
enables users to quickly and conveniently validate the eﬀectiveness of learning
systems, thus avoiding extra laborious work. As shown in Fig.4, ImageNet com-
prises approximately 2.7 million entities across 1.3 million images, dominating

VisionKG: Unleashing the Power of Visual Datasets via Knowledge Graph 81
Fig. 4. Statistics of Triples and Entities in VisionKG for Object Detection and Image
Classiﬁcation Datasets. ImageNet [9], SOP [37], CIFAR [24], CART [16], CUB200 [47],
MSC [31], UAD [ 49], KIT [ 15], CRC [ 22], BDD100K [ 55], OID [ 26], OBJ365 [ 42],
LVS [17], MVD [35], VOC [12], ACDC [40], SHIFT [44]. ∗ presents that synthetic data
generated by VisionKG is included.
the distribution of the classiﬁcation task in VisionKG. Thanks to the inter-
linked datasets and semantic-rich relationships across visual tasks, users can
query images with desired category distributions and contexts to tailor train-
ing pipelines for speciﬁc scenarios. For object detection, Table 1 reveals that
VisionKG includes roughly 576 million triples for 50.8 million box-level anno-
tations primarily derived from large-scale datasets like OpenImages [ 26]a n d
Objects365 [42]. This variety of visual features enables users to create diverse
composite datasets according to speciﬁc requirements, such as the size or the
density of bounding boxes, which can contribute to mitigating biases inherent
in datasets obtained under speciﬁc conditions and scenarios, e.g., to enhance
the model performance in detecting densely distributed small objects, which are
typically challenging to localize and recognize [ 29,30]. For visual relationship
detection, which aims at recognizing object relationships in images, we have
integrated datasets such as Visual Genome [23] and Spatial Scene [54], encom-
passing over 2.1 million triples across 1.2 million annotations for both bounding
boxes and object-level relationships. Additionally, VisionKG includes 22.4 mil-
lion triples for instance segmentation, enabling users to retrieve and reuse masks
of all instance-level objects in downstream scenarios.

82 J. Yuan et al.
Table 1. Statistics across various Visual Tasks in VisionKG.
Visual Tasks Datasets Images Annotations Triples
Visual Relationship 2 119K 1.2M 2.1M
Instance Segmentation 7 300K 3.9M 22.4M
Image Classiﬁcation 9 1.7M 1.7M 16.6M
Object Detection 19 4.3M 50.8M 576.2M
Total 37 6.4M 57.6M 617.3M
Fig. 5. VisionKG Web Interface
3.3 Visual Dataset Explorer Powered by SPARQL
Organizing multiple datasets, often in heterogeneous formats and with diﬀerent
taxonomies, into a single pipeline is a time-consuming task. To streamline this
process, VisionKG oﬀers a GUI for our visual SPARQL frontend, that enables
users to access, explore, and eﬃciently combine data using either the SPARQL
query language or natural language, utilizing the text-to-SPARQL parser in
VisionKG. This empowers users to specify their requirements or criteria using
graph query patterns in an interactive fashion. Figure5 shows the live-interactive
visual datasets explorer in VisionKG: Users can initiate their exploration by
selecting a desired task, such as Detection and Classiﬁcation from a drop-down
menu in Fig.5
1 . Upon task selection, the system will promptly generate a list
of all compatible datasets that support the chosen task, as Fig.5 2 illustrates.
Next, users may choose a dataset, such as MS-COCO [ 31] or KITTI [ 15],
from the list. This will prompt the system to display all available categories
within that dataset in Fig. 5
3 . To ﬁlter or select speciﬁc categories, users can
simply enter a keyword into the text box depicted in Fig. 5 4 . This process is
further facilitated by allowing users to drag and drop a category from Fig.5 3
to the query box in Fig. 5 6 . The system will then auto-generate a SPARQL
query, accompanied by an explainable text in Fig.5 5 , designed to select images
containing the speciﬁed category. It is noteworthy that multiple categories from

VisionKG: Unleashing the Power of Visual Datasets via Knowledge Graph 83
diﬀerent datasets can be selected. Users may modify the query by removing
categories or adjusting the query conditions by selecting available options from
t h eb o x e ss h o w ni nF i g .5
5 or Fig.5 6 . Additionally, users can also adjust the
number of images to be retrieved.
Once the query is ﬁnalized, the user can click the QUERY button, and the
results are displayed in a table format as seen in Fig. 5 7 . Additionally, users
can select the Visualization tab to view the results graphically, as shown in
Fig.5 8 . By clicking on an image, users can access additional information, such
as meta-data or annotations generated by popular DNNs shown in Fig. 5 9 .
Overall, VisionKG oﬀers an intuitive and eﬃcient method for users to explore
and programmatically query images across diverse datasets, thereby accelerating
the data ﬂow in CV pipelines.
4 Enforcing F AIR Principles for Visual Datasets
4.1 Making Visual Data Assets Findable and Accessible
To ensure theﬁndability of visual data assets, VisionKG uses Uniform Resource
Identiﬁers (URIs) to identify resources, including images and their associated
metadata. These URIs provide unique and persistent identiﬁers for each resource,
making it easy to ﬁnd and access speciﬁc images or sets of images. Figure 2
1
illustrates one RDF data snippet linking images and their annotations in MS-
COCO [ 31], KITTI [ 15], and Visual Genome [ 23]. This enables the use of
standardized or popular vocabularies/ontologies, such as schema.org to enrich
metadata associated with the content and context of image data as described
in Sect. 4.2. These metadata can be used to facilitate searching, ﬁltering, and
discovery of visual content based on speciﬁc criteria, such as object category,
weather condition, or image resolution as demonstrated in Sect. 3.3. In partic-
ular, VisionKG links each piece of metadata to a URI for the corresponding
image to ensure that metadata clearly and explicitly describes the image they
refer to, e.g.,containing bounding boxes of aperson,a pedestrian or a man in
Fig.2
1 . This not only enables easy retrieval and exploration of target images
and their related ones based on their metadata but also ensures that more meta-
data can be enriched incrementally by simply adding more RDF triples linked
to the corresponding image. Such desired features are powered by a triple store
for storing, indexing, and querying (cf. Sect.3).
In this context, VisionKG can signiﬁcantly improve theaccessibility of data
and metadata by using standardized communication protocols and supporting
the decoupling of metadata and data. Its publication practice makes it easier
for the targeted user groups to access and reuse relevant data and metadata,
even when the original data is no longer available. For instance, several images
of ImageNet or MS-COCO were downloaded or extracted from web sources and
the metadata will provide alternative sources even if the original sources are no
longer accessible.
To push the accessibility of VisionKG’s data assets even further, users can
access VisionKG through a well-documented web interface and a Python API.

84 J. Yuan et al.
Both allow users to explore diﬀerent aspects of VisionKG, such as the included
tasks, images, and annotations with diverse semantic attributes. Additionally,
many query examples
4,5 enable users to explore the functionalities of VisionKG
in detail and specify queries in SPARQL patterns.
4.2 Ensure Interoperability Across Datasets and Tasks
To make VisionKG interoperable across diﬀerent datasets, computer vision
tasks, and knowledge graph ecosystems, we designed its data schema as an RDFS
ontology as shown in Fig.6. The schema captures the semantics of the properties
of visual data related to computer vision tasks. Our approach makes use of exist-
ing and well-established vocabularies such as schema.org. This ensures interoper-
ability and backward compatibility with other systems using these vocabularies
and reduces the need for customized schema development.
The key concepts in the computer vision datasets include images, annota-
tions, and labels. To deﬁne these concepts, we reuse the schema.org ontol-
ogy by extending its existing classes such as <schema:ImageObject>,a n d
<schema:CreativeWork>. For example, we extend <schema:ImageObject> to
the <cv:Image> class, <schema:Dataset> to the <cv:Dataset> class. By doing
so, we are able to inherit existing properties, such as <schema:hasPart> or
<schema:isPartOf>, to describe the relationships between datasets and images
(Fig.6
a ). Our newly created vocabulary oﬀers the descriptors to capture the
attributes of images that are relevant for training a computer vision (CV) model
(Sect. 3.3), such as the image dimensions, illumination conditions, or weather
patterns as depicted in Fig. 6 b .
The concept Annotation refers to the labeling and outlining of speciﬁc
regions within an image. Each type of annotation is used for a particular com-
puter vision task. For instance, bounding boxes are utilized to train object detec-
tion models. However, annotations are also reusable for various computer vision
tasks. For example, the bounding boxes of object detection annotations can be
cropped to train a classiﬁcation model that does not require bounding boxes.
To enable interoperability of annotations across diﬀerent computer vision tasks,
we developed a taxonomy for them using an RDFS ontology as illustrated in
Fig.6
c . In particular, deﬁning the object detection annotation class as a sub-
class of the classiﬁcation annotation enables the machine to understand that
object detection annotations can be returned when users query annotations for
a classiﬁcation task. The cropping process can be performed during the pre-
processing step of the training pipeline.
Annotations are associated with labels that deﬁne the object or relationship
between two objects (visual relationship). However, labels use heterogeneous
formats, and their semantics are not consistent across datasets. For instance,
as shown in Fig. 2
1 ,t h epedestrian in the KITTI dataset or the man in the
Visual Genome (VG) dataset are annotated asperson in the MS-COCO dataset.
4 https://vision.semkg.org.
5 https://github.com/cqels/vision.

VisionKG: Unleashing the Power of Visual Datasets via Knowledge Graph 85
Fig. 6. VisionKG Data Schema
Furthermore, in the VG dataset, WordNet [32] identiﬁcation is used to describe
the label. Such inconsistencies make it unnecessarily challenging to combine
diﬀerent datasets for training or testing purposes. To tackle this issue, we assign
a speciﬁc label type that indicates how to integrate a dataset with other existing
knowledge graphs to facilitate the semantic interoperability across datasets.
Figure2
2 and Fig.2 3 exemplify how inconsistent labels from three datasets
can be aligned using the RDFS taxonomies from WikiData.
4.3 Enhance Reusability Through a SPARQL Endpoint
To enhance the reusability of visual data assets, VisionKG provides a SPARQL
endpoint6 to enable users to programmatically discover, combine and integrate
visual data assets along with semantic-rich metadata with the vocabularies pro-
vided in Sect.4.2. In particular, users can specify SPARQL queries to automat-
ically retrieve desired data across datasets for various computer vision tasks.
More exemplary queries are provided at http://vision.semkg.org/.
Moreover, we annotated VisionKG with licensing information for more than
ten types7 of licenses associated with datasets listed in Sect.3.2, so that users can
ﬁlter datasets by their licenses to build their own custom datasets. For example,
6 https://vision.semkg.org/sparql.
7 List of dataset licenses in VisionKG: http://vision.semkg.org/licences.html.

86 J. Yuan et al.
a user can issue a single query to retrieve approximately 0.8 million classiﬁcation
training samples for cars with Creative Commons 4.0 license8.
By linking images and annotations with the original sources and related data
curation processes, we captured and shared detailed provenance information for
images and their annotations, thus, VisionKG enables users to understand the
history and context of data and metadata. By providing such detailed prove-
nance information, VisionKG can enable users to better evaluate the quality
and reliability of image and video data and metadata, promoting their reuse.
5 VisionKG: Facilitating Visual Tasks Towards MLOps
Talk about how to use SPARQL to access images, remove the part of MLOps
The term MLOps refers to the application of the DevOps workﬂow [11] specif-
ically for machine learning (ML), where model performance is primarily inﬂu-
enced by the quality of the underlying data [ 1]. This requirement underscores
VisionKG’s signiﬁcant potential to boost the development of MLOps, including
data integration, semantic alignment, and uniﬁed access to data across hetero-
geneous formats and sources. We demonstrate these advantages based on three
use cases. More details and use cases are available in our GitHub repository
9.
5.1 Composing Visual Datasets in a Uniﬁed Taxonomy
Open visual data [9,26], along with their corresponding annotations, often come
in a variety of structures and taxonomies. Considering that eﬃcient data man-
agement with uniﬁed access and expressive query functionalities plays a pivotal
role in MLOps, this necessitates a uniﬁed approach to organizing those visual
corpora. To ensure the eﬃciency and reliability of developed ML models and the
quality and consistency of visual content, as outlined in Sect.4 and 3, VisionKG,
equipped with a SPARQL engine, enables researchers and developers to build
composite datasets in graph queries, regardless of the diversity of sources or
heterogeneity of annotated formats.
Initially, users can perform queries for a subset or speciﬁc categories within
a single dataset, such as images containing car and van from KITTI [ 15]
(Fig.7
1 ). Additionally, beneﬁting from interlinked datasets in a uniﬁed schema,
VisionKG supports users to query images from diverse sources with heteroge-
neous formats, such as images containing car from the MS-COCO [ 31]a n d
sedan from UA-DETRAC [49] datasets, despite their diﬀering annotation for-
mats (Fig. 7
3 ).
Additionally, inconsistent taxonomies and a vast number of categories, e.g.,
1,000 categories in ImageNet-1K [ 9] based on WordNet [32] and 500 classes in
OpenImages [26] using Freebase [ 4], cause a challenge to construct composite
datasets across multiple sources. For instance, in developing a person recog-
nition system, diverse features are required to ensure the robust performance
8 https://creativecommons.org/licenses/by/4.0/.
9 https://github.com/cqels/vision.

VisionKG: Unleashing the Power of Visual Datasets via Knowledge Graph 87
Fig. 7. Retrieving data under various conditions in VisionKG using SPARQL
of learning models. However, there are distinct deﬁnitions for the class person
across diﬀerent sources and taxonomies: It may deﬁned either asperson in MS-
COCO [31]o r pedestrian in KITTI [15], or even man in Visual Genome [ 23]
(Fig.2). Hence, unifying labels from distinct taxonomies is not only a time-
consuming but also a labor-intensive process. To alleviate it, one approach is to
construct a uniﬁed taxonomy for these datasets and mitigate the bias introduced
by speciﬁc domains or similar categories. With VisionKG, we are one step closer
to achieving this. Users can carry out this process with the assistance of exter-
nal knowledge bases, thereby leveraging external knowledge and facts to retrieve
interlinked visual content. Additionally, the uniﬁed data model that leverages
RDF and knowledge graphs, along with the SPARQL endpoint, allows users to
conveniently query speciﬁc parts of the datasets as desired without the extra
eﬀort of parsing and processing the entire large datasets. In this way, VisionKG
enables users to query images containing the desired target categories (such as
person) conveniently (Fig.2 3○) rather than a more complex query (Fig. 2 1○)
that covers all possible cases.
Thanks to the semantic interoperability (Sect.4.2) of interlinked annotations
across diverse label spaces, users can construct datasets from various sources with
relevant deﬁnitions as desired. Along with the enrichment of semantic relation-
ships, VisionKG provides users with composite visual datasets in a cost-eﬃcient
and data-centric manner supporting the data ﬂow in MLOps.
5.2 Automating Training and Testing Pipelines
One of the primary goals of MLOps is to automate the training and testing
pipelines to accelerate the development and deployment of ML models [1]. Auto-
mated workﬂows enable rapid iteration and experimentation, avoiding the time-

88 J. Yuan et al.
consuming process during model development. However, despite the advance-
ments of MLOps, there are some limitations in current MLOps tools, e.g., Kube-
ﬂow [2] and MLﬂow [ 1], such as limited support for complex data types and
multi-modal data, e.g., images, videos, and audios. Besides, integrating these
MLOps tools with existing diverse data infrastructures, such as Deep Lake [18],
can be challenging and requires signiﬁcant eﬀort.
As described in Sect. 3.3, VisionKG boosts automated end-to-end pipelines
for visual tasks. Users can start a training pipeline by writing queries to construct
various composite visual datasets. As demonstrated in Fig. 3, users can query
images and annotations with a few lines of SPARQL code to use RDF-based
descriptions to get desired data, such as images containing box-level annota-
tions of car and person from interlinked datasets in VisionKG. In combination
with popular frameworks, e.g., PyTorch, TensorFlow, or toolboxes, e.g., MMDe-
tection [6], Detectron2 [52], users can further utilize the retrieved data to build
their learning pipelines with minimal Python code without extra eﬀort. Bene-
ﬁting from the interlinked datasets and existing model zoo, users solely need to
deﬁne the model they want to use and the hyperparameters they want to set.
Listing 1.1 demonstrates a simpliﬁed example code to query VisionKG data and
perform training and testing for object detection. More features of automated
pipelines using VisionKG are available in our GitHub repository
10.
1 # Import VisionKG utilities and integrated training pipeline
2 from vision_utils import semkg_api
3 from torch_model_zoo import utils
4 from torch_model_zoo.train_eval import train_eval_pipeline
5
6 def prepare_vkg_pipeline(query_string):
7 # Execute the query
8 rels = semkg_api. query( query_string)
9 params = utils. prepare_for_training( rels)
10 return params
11
12 # SPARQL query to VisionKG for images with specific objects
13 query_string = ''' SPARQL query for object detection '''
14 params = prepare_vkg_pipeline(query_string)
15 params[ 'MODEL ']= ' fasterrcnn_resnet50_fpn '
16 train_eval_pipeline( params)
Listing 1.1. A simpliﬁed example of VisionKG pipeline for MLOps
5.3 Robust Visual Learning over Diverse Data-Sources
The increasing demand for robust visual learning systems has led to the need
for eﬃcient MLOps practices to handle large-scale heterogeneous data, main-
tain data quality, and ensure seamless integration between data ﬂow and model
development. Moreover, a robust learning system should perform consistently
well under varying conditions, such as invariance to viewpoint and scale, stable
performance under instance occlusion, and robustness to illumination changes.
However, many existing visual datasets are speciﬁcally designed and curated for
10 https://github.com/cqels/vision.

VisionKG: Unleashing the Power of Visual Datasets via Knowledge Graph 89
particular tasks, often resulting in a limited distribution of image data applica-
ble only in narrowly deﬁned situations [38]. This not only imposes unnecessary
burdens but also introduces biases within learning systems and constrains the
robustness of VRSs.
As discussed in Sect.5.1, VisionKG enables users to compose datasets across
interlinked data sources and semantic-rich knowledge bases, automating train-
ing and testing pipelines starting from SPARQL queries. This paves the way
to support the construction of robust learning systems exploiting features from
VisionKG. For instance, in developing a robust object detector, besides bound-
ing boxes and annotated categories, other environmental situations should also
be considered and incorporated as prior knowledge to improve the robustness of
trained detectors, such as weather and illumination conditions. Using VisionKG,
as shown in Fig.7
2 , users can employ ﬁne-grained criteria for retrieving images
with annotations, such as querying for “images captured atnight showing cars
in rainy weather conditions”. This extends VisionKG’s functionalities further
for exploring and constructing datasets, allowing users to retrieve useful visual
features and build models that cater to various scenarios robustly, e.g., images
captured during adverse weather conditions or at diﬀerent times of the day. This
functionality can assist users in evaluating the capability of models in domain
transfer, e.g., if a detector trained on KITTI [ 15] is robust enough to detect
cars in snowy weather conditions or handle rare categories and long-tail phe-
nomena [56], e.g., query for a composite dataset containing speciﬁc categories
which are rare in the source dataset to balance the data distribution. These
features reduce the bias arising from unrelated samples and enable users to con-
struct scenario-speciﬁc datasets covering rich semantics in a convenient fashion.
In this way, VisionKG enables users to build robust visual learning systems in a
data-centric manner.
6 Conclusions and Future Works
VisionKG removes data integration, heterogeneity and format inconsistency
problems from datasets intended for vision computing tasks. It enhances the
integrated datasets with a host of semantic annotations from knowledge bases. It
provides a uniﬁed SPARQL query interface to this integrated dataset andoﬀers
powerful exploration tools including a human language interface. All these three
functionalities signiﬁcantly improve access, eﬃciency, and usability to visual
training data based on the power of semantic technologies and demonstrating
how important these technologies are for any kind of data-intensive research
and industrial development. The current version of VisionKG includes 617 mil-
lion RDF triples describing approximately 61 million entities from 37 datasets
and four popular computer vision tasks. VisonKG is easily extensible and will
empower communities to grow around the provided resources. It can serve as
a blueprint for many digital data resources as the functionalities provided are
generic and reusable.

90 J. Yuan et al.
Acknowledgements. This work is supported by the Deutsche Forschungsgemein-
schaft, German Research Foundation under grant number 453130567 (COSMO), by
the Horizon Europe Research and Innovation Actions under grant number 101092908
(SmartEdge), by the Federal Ministry for Education and Research, Germany under
grant number 01IS18037A (BIFOLD) and by the Horizon Europe Research and Inno-
vation programme under grant agreement number 101079214 (AIoTwin).
References
1. Alla, S., Adari, S.K., Alla, S., Adari, S.K.: What is MLOps? Beginning MLOps
with MLFlow: Deploy Models in AWS SageMaker, Google Cloud, and Microsoft
Azure, pp. 79–124 (2021)
2. Bisong, E., Bisong, E.: Kubeﬂow and kubeﬂow pipelines. In: Bisong, E. (ed.) Build-
ing Machine Learning and Deep Learning Models on Google Cloud Platform: A
Comprehensive Guide for Beginners, pp. 671–685. Apress, Berkeley (2019).https://
doi.org/10.1007/978-1-4842-4470-8 46
3. Bizer, C., Heath, T., Berners-Lee, T.: Linked data: the story so far. In: Semantic
Services, Interoperability and Web Applications: Emerging Concepts, pp. 205–227.
IGI global (2011)
4. Bollacker, K., Cook, R., Tufts, P.: Freebase: a shared database of structured general
human knowledge. In: AAAI, vol. 7, pp. 1962–1963 (2007)
5. Budroni, P., Claude-Burgelman, J., Schouppe, M.: Architectures of knowledge: the
European open science cloud. ABI Tech. 39(2), 130–141 (2019)
6. Chen, K., et al.: MMDetection: Open MMLab detection toolbox and benchmark.
arXiv preprint arXiv:1906.07155 (2019)
7. Cordts, M., et al.: The cityscapes dataset. In: CVPR Workshop on the Future of
Datasets in Vision, vol. 2. sn (2015)
8. Cui, P., Liu, S., Zhu, W.: General knowledge embedded image representation learn-
ing. IEEE Trans. Multimed. 20(1), 198–207 (2017)
9. Deng, J., Dong, W., Socher, R., Li, L.J., Li, K., Fei-Fei, L.: ImageNet: a large-scale
hierarchical image database. In: 2009 IEEE Conference on Computer Vision and
Pattern Recognition, pp. 248–255. IEEE (2009)
10. Dimou, A., Vander Sande, M., Colpaert, P., Verborgh, R., Mannens, E., Van de
Walle, R.: RML: a generic language for integrated rdf mappings of heterogeneous
data. Ldow 1184 (2014)
11. Ebert, C., Gallardo, G., Hernantes, J., Serrano, N.: DevOps. IEEE Softw. 33(3),
94–100 (2016)
12. Everingham, M., Van Gool, L., Williams, C.K.I., Winn, J., Zisserman, A.: The
pascal visual object classes (VOC) challenge. Int. J. Comput. Vision 88(2), 303–
338 (2010)
13. Fang, Y., Kuan, K., Lin, J., Tan, C., Chandrasekhar, V.: Object detection meets
knowledge graphs. In: International Joint Conferences on Artiﬁcial Intelligence
(2017)
14. Filipiak, D., Fensel, A., Filipowska, A.: Mapping of ImageNet and Wikidata for
knowledge graphs enabled computer vision. In: Business Information Systems, pp.
151–161 (2021)
15. Geiger, A., Lenz, P., Stiller, C., Urtasun, R.: Vision meets robotics: the KITTI
dataset. Int. J. Robot. Res. 32(11), 1231–1237 (2013)
16. Griﬃn, G., Holub, A., Perona, P.: Caltech-256 object category dataset (2007)

VisionKG: Unleashing the Power of Visual Datasets via Knowledge Graph 91
17. Gupta, A., Dollar, P., Girshick, R.: LVIS: a dataset for large vocabulary instance
segmentation. In: Proceedings of the IEEE/CVF Conference on Computer Vision
and Pattern Recognition, pp. 5356–5364 (2019)
18. Hambardzumyan, S., et al.: Deep lake: a lakehouse for deep learning (2023)
19. Iglesias, E., Jozashoori, S., Chaves-Fraga, D., Collarana, D., Vidal, M.E.: SDM-
RDFizer: an RML interpreter for the eﬃcient creation of rdf knowledge graphs. In:
Proceedings of the 29th ACM International Conference on Information & Knowl-
edge Management, pp. 3039–3046 (2020)
20. Koeva, S.: Multilingual image corpus: annotation protocol. In: Proceedings of the
International Conference on Recent Advances in Natural Language Processing
(RANLP 2021), pp. 701–707 (2021)
21. Koeva, S.: Ontology of visual objects. In: Proceedings of the 5th International
Conference on Computational Linguistics in Bulgaria (CLIB 2022), pp. 120–129.
Department of Computational Linguistics, IBL – BAS, Soﬁa (2022). https://
aclanthology.org/2022.clib-1.14
22. Krause, J., Stark, M., Deng, J., Fei-Fei, L.: 3D object representations for ﬁne-
grained categorization. In: 4th International IEEE Workshop on 3D Representation
and Recognition (3dRR-13), Sydney, Australia (2013)
23. Krishna, R., et al.: Visual genome: connecting language and vision using crowd-
sourced dense image annotations. Int. J. Comput. Vision 123, 32–73 (2017)
24. Krizhevsky, A., Hinton, G., et al.: Learning multiple layers of features from tiny
images (2009)
25. Krizhevsky, A., Sutskever, I., Hinton, G.E.: ImageNet classiﬁcation with deep con-
volutional neural networks. In: NeurIPS (2012)
26. Kuznetsova, A., et al.: The open images dataset v4: uniﬁed image classiﬁcation,
object detection, and visual relationship detection at scale. Int. J. Comput. Vision
128(7), 1956–1981 (2020)
27. Lambert, J., Liu, Z., Sener, O., Hays, J., Koltun, V.: MSeg: a composite dataset
for multi-domain semantic segmentation. In: Proceedings of the IEEE/CVF Con-
ference on Computer Vision and Pattern Recognition, pp. 2879–2888 (2020)
28. Le-Tuan, A., Tran, T.K., Nguyen, D.M., Yuan, J., Hauswirth, M., Le-Phuoc,
D.: VisionKG: towards a uniﬁed vision knowledge graph. In: ISWC (Posters/De-
mos/Industry) (2021)
29. Lin, T.Y., Doll´a r ,P . ,G i r s h i c k ,R . ,H e ,K . ,H a r i h a r a n ,B . ,B e l o n g i e ,S . :F e a t u r e
pyramid networks for object detection. In: Proceedings of the IEEE Conference on
Computer Vision and Pattern Recognition, pp. 2117–2125 (2017)
30. Lin, T.Y., Goyal, P., Girshick, R., He, K., Doll´ar, P.: Focal loss for dense object
detection. In: Proceedings of the IEEE International Conference on Computer
Vision, pp. 2980–2988 (2017)
31. Lin, T.-Y., et al.: Microsoft COCO: common objects in context. In: Fleet, D.,
Pajdla, T., Schiele, B., Tuytelaars, T. (eds.) ECCV 2014. LNCS, vol. 8693, pp.
740–755. Springer, Cham (2014). https://doi.org/10.1007/978-3-319-10602-1
48
32. Miller, G.A.: Wordnet: a lexical database for English. Commun. ACM 38(11),
39–41 (1995)
33. Monka, S., Halilaj, L., Schmid, S., Rettinger, A.: Learning visual models using a
knowledge graph as a trainer. In: Hotho, A., et al. (eds.) ISWC 2021. LNCS, vol.
12922, pp. 357–373. Springer, Cham (2021). https://doi.org/10.1007/978-3-030-
88361-4
21
34. Moore, B.E., Corso, J.J.: Fiftyone. GitHub (2020). https://github.com/voxel51/
ﬁftyone

92 J. Yuan et al.
35. Neuhold, G., Ollmann, T., Rota Bulo, S., Kontschieder, P.: The mapillary vistas
dataset for semantic understanding of street scenes. In: Proceedings of the IEEE
International Conference on Computer Vision, pp. 4990–4999 (2017)
36. Nielsen, F. ˚A.: Linking ImageNet WordNet synsets with Wikidata. In: Companion
Proceedings of the the Web Conference 2018, pp. 1809–1814 (2018)
37. Oh Song, H., Xiang, Y., Jegelka, S., Savarese, S.: Deep metric learning via lifted
structured feature embedding. In: Proceedings of the IEEE Conference on Com-
puter Vision and Pattern Recognition, pp. 4004–4012 (2016)
38. Paullada, A., Raji, I.D., Bender, E.M., Denton, E., Hanna, A.: Data and its (dis)
contents: a survey of dataset development and use in machine learning research.
Patterns 2(11), 100336 (2021)
39. Qin, A., Xiao, M., Wu, Y., Huang, X., Zhang, X.: Mixer: eﬃciently understanding
and retrieving visual content at web-scale. Proc. VLDB Endow.14(12), 2906–2917
(2021)
40. Sakaridis, C., Dai, D., Van Gool, L.: ACDC: the adverse conditions dataset with
correspondences for semantic driving scene understanding. In: Proceedings of the
IEEE/CVF International Conference on Computer Vision, pp. 10765–10775 (2021)
41. Shah, S., Mishra, A., Yadati, N., Talukdar, P.P.: KVQA: knowledge-aware visual
question answering. In: Proceedings of the AAAI Conference on Artiﬁcial Intelli-
gence, vol. 33, pp. 8876–8884 (2019)
42. Shao, S., et al.: Objects365: a large-scale, high-quality dataset for object detection.
In: Proceedings of the IEEE/CVF International Conference on Computer Vision,
pp. 8430–8439 (2019)
43. Speer, R., Chin, J., Havasi, C.: ConceptNet 5.5: an open multilingual graph of
general knowledge. In: AAAI (2017)
44. Sun, T., et al.: SHIFT: a synthetic driving dataset for continuous multi-task domain
adaptation. In: Proceedings of the IEEE/CVF Conference on Computer Vision and
Pattern Recognition, pp. 21371–21382 (2022)
45. Tran, T.K., Le-Tuan, A., Nguyen-Duc, M., Yuan, J., Le-Phuoc, D.: Fantastic data
and how to query them. arXiv preprint arXiv:2201.05026 (2022)
46. Vrandeˇci´c, D., Kr¨otzsch, M.: Wikidata: a free collaborative knowledgebase. Com-
mun. ACM 57(10), 78–85 (2014)
47. Wah, C., Branson, S., Welinder, P., Perona, P., Belongie, S.: The caltech-UCSD
birds-200-2011 dataset (2011)
48. Wang, X., Cai, Z., Gao, D., Vasconcelos, N.: Towards universal object detection
by domain attention. In: Proceedings of the IEEE/CVF Conference on Computer
Vision and Pattern Recognition (CVPR) (2019)
49. Wen, L., et al.: UA-DETRAC: a new benchmark and protocol for multi-object
detection and tracking. Comput. Vis. Image Underst. 193, 102907 (2020)
50. Whang, S.E., Roh, Y., Song, H., Lee, J.G.: Data collection and quality challenges
in deep learning: a data-centric AI perspective. VLDB J. 1–23 (2023)
51. Wilkinson, M.D., et al.: The fair guiding principles for scientiﬁc data management
and stewardship. Sci. Data 3 (2016)
52. Wu, Y., Kirillov, A., Massa, F., Lo, W.Y., Girshick, R.: Detectron2 (2019).https://
github.com/facebookresearch/detectron2
53. Yamamoto, Y., Egami, S., Yoshikawa, Y., Fukuda, K.: Towards semantic data
management of visual computing datasets: increasing usability of MetaVD. In:
Proceedings of the ISWC 2023 Posters, Demos and Industry Tracks (2023)
54. Yang, K., Russakovsky, O., Deng, J.: SpatialSense: an adversarially crowdsourced
benchmark for spatial relation recognition. In: Proceedings of the IEEE/CVF Inter-
national Conference on Computer Vision, pp. 2051–2060 (2019)

VisionKG: Unleashing the Power of Visual Datasets via Knowledge Graph 93
55. Yu, F., et al.: BDD100K: a diverse driving dataset for heterogeneous multitask
learning. In: Proceedings of the IEEE/CVF Conference on Computer Vision and
Pattern Recognition, pp. 2636–2645 (2020)
56. Zhang, Y., Kang, B., Hooi, B., Yan, S., Feng, J.: Deep long-tailed learning: a survey.
IEEE Trans. Pattern Anal. Mach. Intell. (2023)
57. Zhou, X., Koltun, V., Kr¨ahenb¨uhl, P.: Simple multi-dataset detection. In: Proceed-
ings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition,
pp. 7571–7580 (2022)
58. Zhu, C., Chen, F., Ahmed, U., Shen, Z., Savvides, M.: Semantic relation reason-
ing for shot-stable few-shot object detection. In: Proceedings of the IEEE/CVF
Conference on computer vision and Pattern Recognition, pp. 8782–8791 (2021)
59. Zhu, X., Vondrick, C., Fowlkes, C.C., Ramanan, D.: Do we need more training
data? Int. J. Comput. Vision 119(1), 76–92 (2016)

OﬃceGraph: A Knowledge Graph
of Oﬃce Building IoT Measurements
Roderick van der Weerdt1(B) , Victor de Boer1 , Ronald Siebes1 ,
Ronnie Groenewold2, and Frank van Harmelen1
1 Vrije Universiteit Amsterdam,
De Boelelaan 1105, 1081 HV Amsterdam, The Netherlands
{r.p.vander.weerdt,v.de.boer,r.m.siebes,frank.van.harmelen}@vu.nl
2 VolkerWessels iCity, Torenallee 20, 6003, 5617 BC Eindhoven, The Netherlands
RGroenewold@volkerwessels.com
Abstract. In order to support the global energy transition, smart build-
ing management provides opportunities to increase eﬃciency and com-
fort. In practice, real-world smart buildings make use of combinations
of heterogeneous IoT devices, and a need for (knowledge graph-enabled)
interoperability solutions has been established. While ontologies and syn-
thetic datasets are available, a real-world, large scale and diverse knowl-
edge graph has so far not been available. In this paper, we present Oﬃce-
Graph, a knowledge graph expressed in the saref ontology containing
over 14 million sensor measurements from 444 heterogeneous devices,
collected over a period of 11 months, in a seven story oﬃce building.
We describe the procedure of mapping original sensor measurements to
rdf and how links to external linked data are established. We describe
the resulting knowledge graph consisting of 90 Million rdf triples, and
its structural and semantic features. Several use cases are shown of the
knowledge graph: a) through various realistic data analysis use cases
based on competencies identiﬁed by building managers and b) through
an existing machine learning experiment where we replace the original
dataset with OﬃceGraph.
Keywords: Knowledge Graph
· Dataset · IoT · SAREF · Sensors
1 Introduction
Due to the increasing awareness of climate change, in combination with the rising
energy costs, more interest is being shown towards sustainability and eﬃciency of
energy usages. One area where sustainability measures can be especially eﬀective
is in oﬃce building management, where eﬃciency gains for large buildings have
large impact, as compared to dealing with one house at a time [7].
To increase the eﬃciency of oﬃce building management, we can use data
produced in such smart oﬃce buildings. IoT sensors have become prevalent in
oﬃce buildings. Measurements from those sensors can be examined to determine
c⃝ The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
A. Mero˜no Pe˜nuela et al. (Eds.): ESWC 2024, LNCS 14665, pp. 94–109, 2024.
https://doi.org/10.1007/978-3-031-60635-9_6

OﬃceGraph 95
possible sustainability improvements, such as by training a machine learning
system to discover behavioral and systematic patterns of occupation density
during the week, CO
2 levels and heating values [10].
Open datasets facilitate research opportunities and experiments. Unfortu-
nately, large and heterogeneous datasets of sensor data from oﬃce buildings are
rarely available publicly. If they are available, they are either small in size or
only related to one type of measurement (for example only energy consumption
[9] or movement [14]). Some experiments reported in literature are performed on
proprietary datasets, restricting evaluation of systems and comparing research.
As smart oﬃce buildings typically have a multitude of sensor types, realistic
open datasets will contain heterogeneous data since diﬀerent sensors make diﬀer-
ent types of measurements (such as temperature, or occupancy). Additionally, a
successful data model will need to be able to deal with a varied and sometimes
inconsistent use of time intervals. Finally, internal links and links to external data
can increase usefulness of said data. Therefore, making oﬃce building IoT sensor
data available as a knowledge graph addresses these requirements. Ontologies,
such as saref [3] are already available to represent measurements as knowledge
graphs. In summation, the dataset should be a large, heterogenous, and open
knowledge graph.
In this paper, we present OﬃceGraph, a large, real world knowledge graph
containing measurements taken by 444 IoT devices, over 11 months, in a seven
story oﬃce building. The devices are made up of 17 diﬀerent sensor models,
which make measurements of many diﬀerentproperties
1. We ﬁrst discuss relevant
related work, further motivating the resource presented here (Sect. 2). We then
describe the original data and the process of converting it to a knowledge graph
(Sect. 3). The results and ways of accessing the knowledge graph are described
in Sect.4. In Sect.5, we demonstrate the usefulness of OﬃceGraph through two
realistic data analysis use cases provided by building stakeholders. There, we
also deﬁne and execute a machine learning experiment on the knowledge graph.
2 Related Work
This section describes related research by providing examples of what currently
available IoT datasets look like, and what kind of experiments are performed
with such datasets. We compare the datasets on the three requirements deﬁned
in the introduction: size, heterogeneity and openness.
Arz von Straussenburg et al. created a dataset containing (boolean) mea-
surements of detected movement at desks in an oﬃce space, in order to create
a desk sharing space [ 14]. In the experiment the motion sensor measurements
were used to classify a desk as occupied, creating a more accurate desk sharing
platform for the oﬃce occupants. Data was recorded for eleven days. Although
the dataset used is open, the measurements are not heterogeneous (only motion)
1 In order to avoid confusion betweenrdf properties and the property being measured,
we will speciﬁcally refer to the former as rdf properties, and address the latter as
properties.

96 R. van der Weerdt et al.
and it is not large. Motion is also measured in OﬃceGraph, and contact sensors
show which doors are opened. The experiment from Arz von Straussenburg et
al. can be repeated with OﬃceGraph by classifying an oﬃce as occupied when
the door was already opened that day.
Rafsanjani et al. also created a dataset of IoT device data measured in an
oﬃce environment [10], in order to learn the “energy-use behaviors of the occu-
pants”. Occupancy data was used to determine which occupants where using
devices in which rooms, to detect who was using what. Data was recorded over a
six week period, however the data was not made public. Although the data used
in the experiment is heterogeneous, it is not large and not open. OﬃceGraph
includes occupancy data as well, however since it only includes sensor measure-
ments there is no energy consumption for devices that are used by occupants.
Adjustments can be made to the experiment, by changing the energy consump-
tion of devices into the thermostat settings of users, which can yield similar
patterns as the original experiment.
The previous two experiments both required one or two datatypes (movement
or occupancy and energy consumption), but more heterogeneous datasets have
also already been created. Heo et al. created a dataset of 26 diﬀerent devices, with
data recorded for 144 h [5]. They compare various data acquisition scheduling
methods for the devices with the goal of keeping the required data collection
goals but minimizing the traﬃc needed for gather it. By scheduling the data
acquisition fewer data inquiries need to be performed, therefor saving energy. The
dataset has been made available online as downloadable matlab ﬁles. Although
the data used in the experiment is open and heterogenous, it is not large. Since
OﬃceGraph also contains heterogeneous data, it can similarly be used to setup
a testbed with devices. This would also allow for a longer experiment, because
OﬃceGraph contains a longer period of measurements.
OﬃceGraph is an IoT graph with measurements data from the IoT devices,
but there are also diﬀerent kinds of IoT datasets. An example of such a dataset
is created by Ren et al. [ 11]. This traﬃc dataset does not focus on the mea-
surements made by the IoT devices, but instead it focuses on the traﬃc that is
communicated between the devices. The dataset does not contain the measure-
ments made by the devices, but it contains the “packet headers” of the messages
send by 81 devices. Besides recording the measurements being taken by devices
for 112 h, this dataset also contains the results from “34,586 experiments” with
the communications between the devices, linking diﬀerent parameter settings to
diﬀerent behaviors from the devices.
With traﬃc IoT device datasets experiments are performed concerning vari-
ous aspects like privacy and proﬁling based on device behavior [2]. Event though
this traﬃc IoT device dataset is available online, it contains diﬀerent informa-
tion from the IoT devices then what is collected with OﬃceGraph, which puts
the emphasis on the measurements made by the IoT devices. Throughout this
paper when we refer to an IoT dataset or knowledge graph this will be a IoT
measurements dataset or knowledge graph.

OﬃceGraph 97
A larger dataset that is available online is the opsd Household data dataset
[9]. It contains almost ﬁve years of energy consumption information from 68
devices spread out over 11 households in a city in southern Germany. The mea-
surements from the residential households have been used to create a knowl-
edge graph of 36 diﬀerent devices [ 16]. However all the information it contains
about the devices is energy consumption, limiting the applications of the dataset.
Experiments with opsd that investigate the impact of semantic enrichment
on machine learning performance are described in [ 17]. There, two version of
the same knowledge graph are compared, with and without the enrichment.
In Sect. 5.2, we describe how we replicate this same experimental setting with
OﬃceGraph to demonstrate the use of the resource.
3 Converting the Source Data
In order to create the OﬃceGraph we construct a pipeline that maps a collection
of json ﬁles to rdf based on the saref ontology and perform various enrich-
ments. By making changes to the mapping template described in this section
the pipeline is reusable for json data from diﬀerent devices. We did not use
any general knowledge graph creation method, such asrml, because due to the
size of the dataset general knowledge graph creation methods would require a
lot of memory and execution time [ 6]. The Python scripts used to perform the
mapping process can be found on GitHub
2 and were in part based on [17].
3.1 Source Data
The original collection of measurements consists of separate json ﬁles, one ﬁle
for each device, stored in three folders which separate the devices based on
manufacturer: Airwits, Calumino and Samsung. There are 19 diﬀerent models
in total, Airwits and Calumino both have one type of device model, with the
remaining 17 device models being Samsung devices.
All devices are located in a seven story oﬃce building in the Dutch city of
Eindhoven. Over 200 diﬀerent companies make use of the building with an aver-
age of around 250 people working in the oﬃces. The data was initially collected as
part of the InterConnect project
3, which has as its goal to use semantic technolo-
gies to facilitate connections between smart devices. By consistently modeling
the data in the shared saref ontology, any device only needs to map it once,
instead of having to translate it to a bi-lateral format for each receiving device.
3.2 Original Data Structure
Each json ﬁle consists of measurement data originating from one sensor. The
objects in the json ﬁles containing the measurements use a total of 40 diﬀerent
2 https://github.com/RoderickvanderWeerdt/OﬃceGraph
3 https://interconnectproject.eu

98 R. van der Weerdt et al.
Table 1. Three examples of mapping templates used to create the Oﬃcegraph. Bolded
variables represent the data from thejson ﬁle, italicized variables are deﬁned elsewhere
in the mapping and regular font variables are created for this speciﬁc template.
JSON Header Relevant mapping template
“device model description” <device> saref:hasModel <modeltype>
“data room” <device> s4bldg:isContainedIn <data room>
<data room> s4bldg:contains <device>
<data room> rdf:type s4bldg:BuildingSpace.
“data temp c” <device> saref:measuresProperty <property uri >
<device> saref:makesMeasurement <meas uri>
<meas uri> rdf:type saref:Measurement
<meas uri> saref:hasvalue <value>
<meas uri> saref:hasTimestamp <timestamp>
<meas uri> saref:isMeasuredIn om:degreeCelsius
<meas uri> saref:relatesToProperty <property uri >
<property uri > rdf:type saref:Temperature.
headers. Of these, 24 were identiﬁed as containing relevant information for the
OﬃceGraph, by discussing with experts from the domain to determine which
headers contained duplicate information, and by excluding headers that were
always left empty. For each of the 24 headers, mapping rules were created that
produce triples that capture the data, and structure it correctly in the graph.
Three examples of such mapping rules can be seen in Table1.
3.3 Data Model and Mapping Template
Multiple ontology standards exist for smart device information, such as ssn
[1] and WoT Thing Descriptions [15]. OﬃceGraph is expressed in saref [3], a
domain standard ontology speciﬁcally created to model measurements of diﬀer-
ent IoT devices. A comparison and mapping betweensaref and ssn is made in
[8].
The main structure we use from saref can be seen in Fig. 1,f o re a c h
individual device the “device template” creates triples for all consistent infor-
mation about the device, such as the device type and model. For each indi-
vidual measurement the “measurement template” creates triples to describe
the measurement, its value, unit of measurement and timestamp. The device
instance and measurement instances are connected in two ways, directly
through the saref:makesMeasurement property, and indirectly through the
saref:Property instance. The latter describes what has been measured, such
as temperature or humidity.
In addition to thesaref ontology we use two of its extensions.saref4bldg
4,
which provides classes used to describe the relation between devices and rooms,
and between rooms and buildings. The other extension is saref4ener5,w h i c h
4 https://saref.etsi.org/saref4bldg/
5 https://saref.etsi.org/saref4ener/

OﬃceGraph 99
Fig. 1. Visualization of the templates used to create OﬃceGraph.
provides additional classes for information about the device. As suggested in
the saref documentation we use the om1.8 ontology to represent the units of
measure of the measurements [12].
Additionally, the following new instance and six new subclasses of saref
classes, and two new rdf properties are introduced to enable a more detailed
representation of the building data:
new instance of saref:UnitOfMeasure:
– ic:people is used in the measurement of a number of people, such as a
doorcounter which counts the number of passing people.
new subclasses of saref:Property:
– ic:RunningTime is used in the measurement of time that has passed, such as
the time since the last movement was detected.
– ic:Contact is a property related to whether or not a sensor is making contact
(closed window).
– ic:BatteryLevel is a property related to the current percentage of charge
left in the device’s battery level.
– ic:CO2Level is a property related to the current CO2 level measured by the
device.
– ic:DeviceStatus is a property related to current status of the device,
whether it is active or not.
– ic:thermostatHeatingSetpoint is a property related to the current heating
setpoint of a thermostat.
new rdf properties to store diﬀerent information relevant to the device:
– ic:hasParentSerialNumber is a property of a device, to store the Parent
Serial Number, which is related to the edge device it is connected to.

100 R. van der Weerdt et al.
– ic:hasDeviceType is a attribute of the device that represents the devicetype
of the device.
3.4 Enrichment
In addition to OﬃceGraph we also create three enrichments, that can be used
in combination with OﬃceGraph.
Devices in Room. Not all devices recorded the name of the room in which they
were located in the original data. Additional information was retrieved from the
oﬃce building to add triples for most devices in which room they were located,
and in which “service zone” they are located (which is used for maintenance on
the devices). Furthermore, we added for each room and service zone on which
ﬂoor they were located and that each ﬂoor is part of the same building.
Wikidata Days. OﬃceGraph is linked to the Wikidata graph, by matching the
timestamps to the Wikidata concepts of their corresponding dates. This allows
federated queries to be performed, combining information from OﬃceGraph and
Wikidata. For example, we can query the graphs to determine on which day a
measurement is taken.
Graph Learning Enrichment. Previous research has shown that certain semantic
enrichments to a knowledge graph can be beneﬁcial for the machine learning on a
graph process [17]. These same enrichments are made available for OﬃceGraph,
in separate ﬁles. The enrichments are:
– Sequence links, rdf properties that link to the previous and next measure-
ment, taken chronologically.
– Rounded values, URI entities of the measurement values, rounded to function
as a bucket for all similar values.
– Timestamp buckets, This enrichment is slightly diﬀerent compared to the
original semantic enrichment. Where the original was only a URI entity of
the timestamp, this time it also serves as a bucket to collect all measurements
taken within the same hour.
The results of the mapping process will be discussed in the next section.
4 Description of OﬃceGraph
The OﬃceGraph consists of 89,599,577 triples describing 14,930,478 measure-
ments measured by 444 devices. Measurements were taken over a period of 11
months, starting March 1st 2022 and ending January 31st 2023. The resulting
turtle ﬁles have a uncompressed size of 4.5 GB.
The measurements are represented with 11 diﬀerent properties, which are all
shown in Table2. Additionally, the table shows which properties are measured
by which device model and what the distribution of models is for the devices.

OﬃceGraph 101
Table 2. Distribution of the models from the devices, and properties measured by
those device models.
Device property type
Device model
ic:BatteryLevel
ic:CO2Levelic:Contact
ic:DeviceStatusic:RunningTime
ic:thermostatHeating...
saref:Humiditysaref:Motion
saref:Occupancy
saref:Power
saref:TemperatureNumber of devices
Aeon Home Energy Meter 1 1
Fibaro Smoke Sensor 3 3 1 3
Hex Doorcounter Ver 1.0 14 14 14
Qubino Dimmer 1 1
R5 227 227 227 227
SmartPower Outlet 20 13 20
SmartSense Button 3 3 1 3
SmartSense Moisture Sensor 8 8 1 8
SmartSense Motion Sensor 36 36 24 24 36
SmartSense Multi Sensor 93 51 93 62 95
Z-Wave Basic Smoke Alarm 2 2 2
Z-Wave Door/Window Sensor 6 2 6 6
Z-Wave Metering Switch 2 2
Z-Wave Radiator Thermostat 1 1 1
Z-Wave Range Extender 1 1
Z-Wave Switch Secure 4 4
Z-Wave Temp/Light Sensor 2 2 2
Z-Wave Water/Temp/Light Sensor 4 4 2 4
Zigbee Thermostat 14 14 11 11 14
Totals 172 227 53 201 14 11 227 24 14 13 329 444
4.1 Timepoints
The number of timepoints at which measurements were taken diﬀers greatly
between devices, as can be seen in Fig.2. We identiﬁed two causes of this diﬀer-
ence: (1) some devices take measurements every time a change in the measure-
ment is detected (Samsung and Calumino devices). Which also means devices
detecting many changes will generate more measurements than the devices
detecting fewer changes, for example a people counter in a busy hallway will
make more measurements then a door sensor in a one person oﬃce. Other devices
(Airwits devices) will make measurements at a given interval, producing a very
similar amount of timepoints. (2) Some devices were turned oﬀ, or had a low
battery, for a period of time, resulting in fewer overall measurements.

102 R. van der Weerdt et al.
Fig. 2. Boxplots of the number of points in time in which a device has made a mea-
surement. Diﬀerent update settings result in diﬀerent distributions of timepoints. One
Calumino device outlier is not shown for readability, because it made measurements at
600,000 points in time.
4.2 Graph Structure Metrics
The indegree and outdegree of a knowledge graph provide information concerning
the amount of rdf properties of each entities. The outdegree is the number of
rdf properties an entity has, the indegree of an entity is the number of entities
it is an object of. The indegree and outdegree of a graph can have big eﬀects on
algorithms that use graph traversal, such as RDF2Vec [13].
In Fig. 3 we see the indegree and outdegree of OﬃceGraph. To compare it
with other large knowledge graphs we use the in and outdegree as recorded
by Duan et al. [ 4], where the authors describe multiple characteristics about
large knowledge graphs, such as DBpedia or Barton. The average indegree (5.6)
and outdegree (6.0) of OﬃceGraph is similar to the other knowledge graphs, as
is the distribution of the indegree of the entities. However, when we compare
the number of entities with an outdegree higher then 10
4, the other knowledge
graphs only have two entities with such a high outdegree, while OﬃceGraph
has hundreds. These high outdegree entities represent the devices and the high
outdegree is due to the high number of measurements related to the devices.
4.3 Enrichment
Devices in Room. For 340 devices we are able to add additional room informa-
tion, which results in a graph containing 2,426 triples.

OﬃceGraph 103
Fig. 3. The indegree and outdegree of entities in OﬃceGraph, the axis use logarithmic
scale.
Wikidata Days. The Wikidata days enrichment adds 8,088 triples, one triple for
every hour in the OﬃceGraph. We chose to make the links to Wikidata only
for the timebuckets in the graph learning enrichment, since the timestamps in
OﬃceGraph are literals.
Graph Learning Enrichment.When the enrichment is performed with all devices
the graph learning enrichment adds a combined total of 89,581,980 triples. Six
new rdf properties are added for each measurement in the OﬃceGraph, except
for each ﬁrst and last (chronological) measurement of each device, because those
do not have previous or next measurements to link to.
4.4 Accessing the KG
OﬃceGraph is accessible under the Creative Commons Attribution 4.0 Interna-
tional license, in three ways: as rdf ﬁles on GitHub, a snapshot on Zenodo and
through a sparql endpoint.
RDF ﬁles on GitHub. A zipped version of OﬃceGraph is available on GitHub
6.
Instead of one ﬁle containing the entire knowledge graph the zipped folder con-
tains a separate ﬁle for each individual device. Each ﬁle contains all the mea-
surements made by the device. The devices in room enrichment is included in a
separate ﬁle.
Zenodo Snapshot. The same zip ﬁle that is available on Github is also made
available on Zenodo at: https://zenodo.org/records/10245815.
SPARQL Endpoint. A Cliopatria [18] server has been set up at https://data.
interconnect.labs.vu.nl to store the data, and expose it through a sparql end-
point. sparql queries can be used to retrieve information from the graph. The
devices in room enrichment is included in the datastore.
6 https://github.com/RoderickvanderWeerdt/OﬃceGraph

104 R. van der Weerdt et al.
5 Using OﬃceGraph
In this section, we demonstrate the usefulness of OﬃceGraph through two real-
istic use cases: 1) through a data analysis task for building management and 2)
by performing a machine learning experiment with the OﬃceGraph.
5.1 Building Management Data Analytics
The OﬃceGraph can be used to highlight situations where automatization can
be of use. By showing that certain situations occur it can be used as an argument
for why an automatization can be beneﬁcial. Two competency questions were
created in collaboration with the building owners, to assure they are relevant for
the oﬃce building.
Thermostat and Window Status. The ﬁrst question relates to occupant
behavior: “Is the thermostat turned down when the windows are opened in that
same room?”. To answer this question we queried the graph for contact sensors,
thermostat settings and temperature values, from devices that are located in the
same area. The results for one day in one room of these queries are visualized
in Fig. 4a, the temperature (grey lines) is measured by multiple devices, each
diﬀerently colored arrow is a speciﬁc window opening (arrow up) and closing
(arrow down), and the dots are the thermostat temperature settings. We consider
“turning the thermostat down when the windows are opened” to have occurred
when the thermostat is turned to a lower value then the current temperature
within 30 min after a windows has opened. Using the results from the queries,
we can conclude that the answer to the competency question is: no, because
the thermostat is never lowered (within 30 min) in an oﬃce when an window is
opened.
Occupation and Oﬃce Climate.The second question relates to the oﬃce cli-
mate: “Is there a noticeable eﬀect of occupants on the climate of oﬃce rooms?”.
We answer this question by querying the graph for humidity, CO
2 and temper-
ature measurements, over ﬁve days: four weekdays and a Saturday. The results
for one oﬃce are presented in Fig. 4b. The values have been scaled 0–100 to ﬁt
in one ﬁgure. From the ﬁgure we see that in the morning all temperature mea-
surements consistently rise, and lower in the evening, regardless of which day it
is. The humidity is not eﬀected by time of day, nor by which day of the week
it is. However, the CO
2 values only rise in the morning during the workdays,
and stay (relatively) constant during the weekend. Therefor we can answer the
question: yes, the oﬃce climate is aﬀected by occupants, speciﬁcally the CO 2
values.
Jupyter notebooks are available (see footnote 6) that show the code used to
create the ﬁgures and answer the competency questions.

OﬃceGraph 105
Fig. 4. Plots of measurements from OﬃceGraph.
5.2 Machine Learning on OﬃceGraph
In this section we demonstrate how OﬃceGraph can be used for machine learn-
ing experiments. We perform experiments re-using the learning task and learning
approach from [17] on OﬃceGraph. The goal of the original experiment was to
compare the eﬀect of diﬀerent IoT knowledge graph enrichments on the eﬀec-
tiveness of the embedding method (RDF2Vec) and representativeness of the
resulting embeddings.
Experimental Setup. Figure5 depicts the pipeline used in the experiment.
The goal of the experiment is to examine the eﬀect of semantic enrichment on the
quality of embeddings learned from a knowledge graph. In Step 1 of the pipeline
we have two knowledge graphs, one without the enrichment (Basic Graph) and
one with the enrichment (Enriched Graph). The enrichment is described in
Sect.3.4. In Step 2 of the pipeline we train a model to learn embedding rep-
resentations for both knowledge graphs. Step 3 uses the embeddings to train
two classiﬁcation models. By comparing the accuracy of the classiﬁcations we
determine whether the semantic enrichment had a (positive) eﬀect on the quality
of the embeddings.
The classiﬁer in the original experiment predicted whether the outside tem-
perature at a point in time was warm or cold. This label was created by sorting
the timestamps from high to low based on the outside temperature, and labeling
the ﬁrst 50% as warm, and the last 50% as cold. This time the results of the
classiﬁcation model will be based on how well it predicts whether or not a given
point in time is a working day (Monday-Friday) between working hours (9–5).
All code used in this section is made available through GitHub
7.
7 https://github.com/RoderickvanderWeerdt/semantic-enrichment-of-IoT-graphs

106 R. van der Weerdt et al.
Fig. 5. Experimental pipeline. Original image taken from [17].
Pre-processing. Before OﬃceGraph is ready to be used in the pipeline we
perform some pre-processing. Only a subset of OﬃceGraph is used in order to
lower the required compute power to train the embeddings. The subset is created
by selecting only the devices located on the 7th ﬂoor, which leaves us with 13
devices and a knowledge graph with 3.9 million triples.
We use the graph learning enrichment (as described in Sect.3.4) in order to
use the timestamp uris that bucket the timestamps and allow us to use these
uris as entities as input for the pipeline.
We create the entity ﬁle, the document containing the entities in the graph
we want to create an embedding for, and its prediction target (a class or value)
by querying the graph.
Classiﬁcation Task. The classiﬁcation task we use for the experiment predicts
whether a timestamp bucket occurs within working hours. To create the entity
ﬁle we query the graph to retrieve all timestamp buckets, and use a script to
classify each timebucket as occurring within workhours if the day is a weekday,
and the hour is between 9 and 17.
Implementation. Since the goal of the experiment is not to get cutting edge
results, but to perform the experiment to demonstrate the usability of Oﬃce-
Graph we use the same preset hyperparameters that the original experiment
used. Which means that the RDF2Vec embeddings are made with 25 random
walks of length 2. And the classiﬁer is amlp with one hidden layer of 512 ReLU
nodes. The original paper provides additional information [17].
The labels used in the original experiment were made by splitting the dataset
in two even halves of warm and cold outside temperatures, therefor when the
classiﬁer would exclusively predict one of the classes, the accuracy would be
50%. This is used as a baseline to determine whether the classiﬁer is learning
something from the embeddings. For the new experiment the baseline is similarly
always predicting the most prevalent class, which in this case is predicting that
every hour is not a working hour. This results in a baseline accuracy of 76%.
Results. The results of the experiment can be seen in Table3. Both the original
experiment and the new experiment display the same behavior, the basic graphs
score close to the baseline and the enriched graphs score signiﬁcantly above it.

OﬃceGraph 107
Table 3. Results of the experiment with OﬃceGraph, compared with the results of
the original experiment with opsd.
dataset baseline basic graph enriched graph
Classiﬁcation (accuracy)
opsd [17] 50% 49.8% 80.7%
OﬃceGraph 76.1% 73.0% 85.1%
Value Prediction (mae)
opsda 6.3 6.6 6.1
OﬃceGraph 2.03 2.01 1.87
Value Prediction Task. The experiment can also be performed with a dif-
ferent machine learning task, such as value prediction8. For this we replace the
accuracy comparison with a mean absolute error (mae) comparison to evaluate
the resulting prediction from the mlp.
The entity ﬁle for the value prediction task is created by querying the graph
based on the property we want to predict and return all timestamp URIs and
values pairs. In the situation where multiple measurements were taken in the
timespan of one timestamp bucket, we take the average of those measurements.
Implementation. The mlp structure from the classiﬁcation experiment is reused,
but with a mean squared error loss function instead of the cross entropy loss
function. The other change is the evaluation metric.mae is the average diﬀerence
between the prediction and the target value. Therefore, when using accuracy a
higher value represents a more similar prediction, but with mae a lower value
represents a more similar prediction instead.
In the original experiment the outside temperature was predicted, here we
predict the temperature measurements of one speciﬁc device. The outside tem-
perature has a bigger range of measurements, with a minimum temperature of
− 11
◦C, maximum temperature of 28 ◦C and standard deviation of 7.5, com-
pared to a minimum temperature of 15.5 ◦C, maximum temperature of 27 ◦C
and standard deviation of 2.4 with the new experiments. Therefor the results
are expected to diﬀer more then with the classiﬁcation experiments, however,
we still expect the overall behavior, where the model trained with the enriched
outperforms the model trained with the basic graph, to occur.
As a baseline we use the average temperature over the entire dataset as the
predicted value. This was the same baseline used in the original experiment.
Results. Table3 shows the results from the value prediction experiment. As
with the classiﬁcation experiment we see that the experiment with the enriched
graph outperforms the baseline and basic graph. Because the diﬀerence between
8 OPSD results for the value prediction task were not part of the experiments described
in [17], but are presented here to compare results.

108 R. van der Weerdt et al.
the mae results are closer then the classiﬁer results we report the results of a
signiﬁcance test. We performed a t-test which showed that the results from the
enriched graph are signiﬁcantly diﬀerent from the results with the basic graph
(p< 0.002). The results with the baseline are not signiﬁcantly diﬀerent from the
results with the basic graph (p> 0.5).
When we compare the results of the new experiment with the original experi-
ment (which used theopsd dataset) we see that in both cases the enriched graph
provides the most similar predictions. The mae is in all cases much higher for
the original experiment, as was expected, due to the bigger variance and range
of the outside temperature that is predicted in the original experiment.
6 Conclusion
In this paper we presented OﬃceGraph, a knowledge graph containing 11 months
of heterogeneous measurements from 444 IoT devices. We described the mapping
process, how it applies to this dataset, and made the code available to be adapted
and reused for other datasets.
Speciﬁcations of OﬃceGraph are provided in terms of speciﬁc traits: 1) the
properties measured by each device, 2) time points: the amount of times a devices
records a measurement, 3) outdegree: the high outdegree of the device entities,
4) speciﬁc enrichments that can be added to core data of OﬃceGraph.
OﬃceGraph is accessible in three ways: downloadable via Github or Zenodo,
and it can be queried through a sparql endpoint.
In order to demonstrate the usability of OﬃceGraph, we described how it
can be used with python (notebooks), with sparql queries and with machine
learning experiments.
OﬃceGraph is a benchmark set that can be used for future oﬃce data exper-
iments, allowing for more representative experiments for sustainability and eﬃ-
ciency of energy usages.
Acknowledgements. This work is part of the InterConnect project (interconnectpro-
ject.eu/) which has received funding from the European Unions Horizon 2020 research
and innovation program under grant agreement No 857237.
References
1. Compton, M., et al.: The SSN ontology of the W3C semantic sensor network incu-
bator group. J. Web Semant. 17, 25–32 (2012)
2. Dadkhah, S., Mahdikhani, H., Danso, P.K., Zohourian, A., Truong, K.A., Ghor-
bani, A.A.: Towards the development of a realistic multidimensional IoT proﬁling
dataset. In: 2022 19th Annual International Conference on Privacy, Security &
Trust (PST), pp. 1–11 (2022)
3. Daniele, L., den Hartog, F., Roes, J.: Created in close interaction with the industry:
the smart appliances REFerence (SAREF) ontology. In: Cuel, R., Young, R. (eds.)
FOMI 2015. LNBIP, vol. 225, pp. 100–112. Springer, Cham (2015). https://doi.
org/10.1007/978-3-319-21545-7 9

OﬃceGraph 109
4. Duan, S., Kementsietsidis, A., Srinivas, K., Udrea, O.: Apples and oranges: a com-
parison of RDF benchmarks and real RDF datasets. In: Proceedings of the 2011
ACM SIGMOD International Conference on Management of Data, pp. 145–156
(2011)
5. Heo, S., Song, S., Kim, B., Kim, H.: Sharing-aware data acquisition scheduling for
multiple rules in the IoT. In: 2020 IEEE Real-Time and Embedded Technology
and Applications Symposium (RTAS), pp. 43–55. IEEE (2020)
6. Iglesias, E., Jozashoori, S., Vidal, M.E.: Scaling up knowledge graph creation to
large and heterogeneous data sources. J. Web Semant. 75, 100755 (2023)
7. Jafarpur, P., Berardi, U.: Eﬀects of climate changes on building energy demand
and thermal comfort in Canadian oﬃce buildings adopting diﬀerent temperature
setpoints. J. Build. Eng. 42, 102725 (2021)
8. Moreira, J., et al.: Towards IoT platforms’ integration semantic translations
between W3C SSN and ETSI SAREF. In: SEMANTICS Workshops (2017)
9. Open Power System Data: Data Package Household Data. Version 2020-04-15
(2020). https://data.open-power-system-data.org/household
data/2020-04-15/
10. Rafsanjani, H.N., Ghahramani, A.: Towards utilizing internet of things (IoT)
devices for understanding individual occupants’ energy usage of personal and
shared appliances in oﬃce buildings. J. Build. Eng. 27, 100948 (2020)
11. Ren, J., Dubois, D.J., Choﬀnes, D., Mandalari, A.M., Kolcun, R., Haddadi, H.:
Information exposure from consumer IoT devices: a multidimensional, network-
informed measurement approach. In: Proceedings of the Internet Measurement
Conference, pp. 267–279 (2019)
12. Rijgersberg, H., Van Assem, M., Top, J.: Ontology of units of measure and related
concepts. Semant. Web 4(1), 3–13 (2013)
13. Ristoski, P., Rosati, J., Di Noia, T., De Leone, R., Paulheim, H.: RDF2Vec: RDF
graph embeddings and their applications. Semant. Web 10(4), 721–752 (2019)
14. Arz von Straussenburg, A.F., Blazevic, M., Riehle, D.M.: Measuring the actual
oﬃce workspace utilization in a desk sharing environment based on IoT sensors.
In: Gerber, A., Baskerville, R. (eds.) DESRIST 2023. LNCS, vol. 13873, pp. 69–83.
Springer, Cham (2023). https://doi.org/10.1007/978-3-031-32808-4
5
15. W3C: Web of Things (WoT) Thing Description (2020). https://www.w3.org/TR/
2020/REC-wot-thing-description-20200409/
16. van der Weerdt, R., de Boer, V., Daniele, L., Nouwt, B., Siebes, R.: Making hetero-
geneous smart home data interoperable with the SAREF ontology. Int. J. Metadata
Semant. Ontol. 15(4), 280–293 (2021)
17. van der Weerdt, R., de Boer, V., Daniele, L., Siebes, R., van Harmelen, F.: Eval-
uating the eﬀect of semantic enrichment on entity embeddings of IoT knowledge
graphs. In: Proceedings of the 1st International Workshop on Semantic Web on
Constrained Things at ESWC 2023, vol. 3412 (2023)
18. Wielemaker, J., Beek, W., Hildebrand, M., Van Ossenbruggen, J.: ClioPatria: a
SWI-prolog infrastructure for the semantic web. Semant. Web7(5), 529–541 (2016)

Musical Meetups Knowledge Graph
(MMKG): A Collection of Evidence
for Historical Social Network Analysis
Alba Morales Tirado(B) , Jason Carvalho , Marco Ratta ,
Chukwudi Uwasomba , Paul Mulholland , Helen Barlow, Trevor Herbert ,
and Enrico Daga
The Open University, Milton Keynes, UK
{alba.morales-tirado,jason.carvalho,marco.ratta,chukwudi.uwasomba,
paul.mulholland,helen.barlow,trevor.herbert,enrico.daga}@open.ac.uk
Abstract. Knowledge Graphs (KGs) have emerged as a valuable tool
for supporting humanities scholars and cultural heritage organisations. In
this resource paper, we present the Musical Meetups Knowledge Graph
(MMKG), a collection of evidence of historical collaborations between
personalities relevant to the music history domain. We illustrate how
we built the KG with a hybrid methodology that, combining knowl-
edge engineering with natural language processing, including the use of
Large Language Models (LLM), machine learning, and other techniques,
identiﬁes the constituent elements of a historical meetup . MMKG is a
network of historical meetups extracted from ∼33k biographies collected
from Wikipedia focused on European musical culture between 1800 and
1945. We discuss how, by providing a structured representation of social
interactions, MMKG supports digital humanities applications and music
historians’ research, teaching, and learning.
Keywords: Knowledge Graph
· historical encounters · MEETUPS ·
Historical Social Network Analysis
Resource Type: Knowledge Graph
License: CC BY 4.0
DOI: 10.5281/zenodo.7924618
URL: https://github.com/polifonia-project/meetups-knowledge-graph
Endpoint: https://polifonia.kmi.open.ac.uk/meetups/sparql/
1 Introduction
The Semantic Web community has been very active in generating knowledge
from unstructured sources in domains such as scientiﬁc knowledge, social media,
and digital humanities. In this regard, Knowledge Graphs (KGs) have emerged as
© The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
A. Mero˜no Pe˜nuela et al. (Eds.): ESWC 2024, LNCS 14665, pp. 110–127, 2024.
https://doi.org/10.1007/978-3-031-60635-9_7

Musical Meetups Knowledge Graph (MMKG) 111
a valuable tool for supporting humanities scholars and cultural heritage organi-
sations [1,3,5,26]. In the EU project Polifonia1, we study how knowledge graphs
can support scholarship in music history. In this paper, we present the Musi-
cal Meetups Knowledge Graph (MMKG), a collection of evidence of historical
collaborations between personalities relevant to the music history domain. Our
resource aims at representing documentary evidence of social interactions in
the music history domain, to support the needs of humanities scholars. This
includes capturing the evidence text and decorating it with semantic entities,
such as type of events, participants, temporal expressions and spatial instances,
enabling the exploration of complex historical meetups . We build on previous
work focused on conceptualising the domain of interest in the Meetups Ontol-
ogy [21]. Here, we report on the work undertaken to generate a KG extracted
from 33,309 biographies collected from Wikipedia focused on European musical
culture between 1800 and 1945. Our work provides a structured representation of
historical exchanges to enable the discovery of new insights and support music
historians’ research, teaching, and learning. Therefore, in this paper, we con-
tribute 1. Musical Meetups Knowledge Graph (MMKG), a Knowledge Graph
of documentary evidence of musical collaborations from ∼33k biographies from
Wikipedia 2. A KG generation pipeline, combining Natural Language Processing
(NLP), Large Language Models (LLM), Knowledge Engineering, and Knowledge
Graph Construction (KGC) techniques. The rest of the paper is structured as
follows. We discuss the background and motivation for our work in Sect. 2.I n
Sect.3 we illustrate the Meetups Ontology. Section4 describes the hybrid knowl-
edge graph generation pipeline. We evaluate the knowledge graph in Sect. 5 for
its ability to answer key competency questions and via a survey with domain
experts. Next, we discuss feedback on the utility and usability of MMKG from
two types of stakeholders: domain experts of a Music Department and appli-
cation developers of Digital Humanities tools (Sect. 6). We report on relevant
related work in Sect.8, before discussing conclusions and future work (Sect.9).
2 Motivation
Music historians and those involved in the arts and humanities research pro-
cess rely heavily on information and knowledge contained within historical
manuscripts and the biographies of ﬁgures from history. A common method
used for historical investigation is narrative inquiry [23] in which historical evi-
dence is ﬁrst organised into a chronicle including evidence of events in temporal
order. The evidence is then ﬁltered from the chronicle comprising exchanges with
common features of interest, generating, for example, storylines of encounters
of a particular location (e.g. London), purpose (e.g. music making) or partici-
pant (e.g. Elgar). Such storylines can then be used to investigate comparisons
and temporal shifts, for example, why music-making is more common in certain
locations during particular periods.
1 http://polifonia-project.eu.

112 A. Morales Tirado et al.
Fig. 1. Meetups Ontology.
Such forms of inquiry are highly resource-intensive in terms of extracting the
chronicle of social interactions from source documents and organising them into
storylines for further analysis. The development of a knowledge graph comprising
the evidence of historical interactions extracted from source documents that can
then be queried to create storylines (e.g. the music creation events of a composer
or those occurring in a geographic location) would not only enhance the depth of
historical analysis but also facilitate a more thorough and nuanced interpretation
of the dynamic interplay between music and societal evolution.
A knowledge graph would also open up the possibility for Exploratory Data
Analysis (EDA) [25] of storylines to reveal patterns and behaviours that might
evade detection during examinations at a smaller scale. By leveraging these tech-
niques, historians can pinpoint temporal and spatial trends, discern correlations
between genres and historical periods, and unveil unexpected connections, thus
enriching their grasp of the cultural and social contexts surrounding musical
encounters.
3 Meetups Ontology
We use as a guiding framework the Meetups Ontology 2 (See Fig. 1) that mod-
els the elements of a historical meetup. As presented in previous work [21], the
scope of the ontology is the analysis of historical encounters and collaborations
of people in the musical world. These knowledge requirements are formalised as
Competency Questions (listed in the ontology repository), following good prac-
tices in ontology engineering. The ontology considered commonly used vocabu-
laries such as Time Ontology, PROV Ontology, SEM and the Polifonia CORE
Ontology.
2 Meetups Ontology repository: https://github.com/polifonia-project/meetups-onto
logy.

Musical Meetups Knowledge Graph (MMKG) 113
Fig. 2. MMKG construction pipeline.
Here we give a brief description of the main Meetups Ontology classes. A
historical meetup – mtp:Meetup, is derived from evidence within a biography –
mtp:hasEvidenceText. Mentions of at least one or more participants and places
are represented by the mtp:Participant and mtp:Location class, respectively.
Each mention is an entity ( mtp:hasEntity) extracted and linked to DBpedia
or Wikidata (Sect. 4 gives details on the extraction process). To represent the
time when the meetup took place, we use the mtp:TimeExpression class. It
is composed of start time:hasBeginning and end time:hasEnd dates as well
as the text from where it was compiled. Lastly, the purpose of the encounter
is deﬁned by ( mtp:Purpose) and six diﬀerent subclasses speciﬁed by domain
experts. These classes are adjacent but not disjoint and each meetup can be
annotated with more than one purpose, namely: mtp:BusinessCareer, mtp:
PersonalLife, mtp:Coincidence, mtp:Education, mtp:PublicCelebration or
mtp:MusicMaking.
4 Knowledge Graph Generation Pipeline
This section describes the knowledge extraction pipeline developed to build
MMKG (see Fig.2). Our approach focuses on extracting evidence that describes
historical meetups according to Meetups Ontology. We apply knowledge extrac-
tion techniques and methods for text processing to recognise, classify and link
the entities that are part of a historical meetup, particularly: people, places, time
expressions and themes. In what follows, we describe in detail the steps taken
towards the construction of the KG.
4.1 Data Collection and Preparation
The ﬁrst step of the pipeline is dedicated to the collection of data. We rely
on Wikipedia and its database of open-access biographies. To obtain the list of
music personalities, we queried the DBpedia SPARQL endpoint, obtaining all
the entities of typedbo:MusicalArtist. The biographies of 33,309 personalities
were collected
3 in text format4. Next, we prepare the text by removing empty
3 Data was collected on January 2022.
4 Meetups corpus: https://github.com/polifonia-project/meetups corpus collection.

114 A. Morales Tirado et al.
spaces, redundant line breaks and special characters. We organise the text by
assigning indexes to each sentence, grouped by paragraphs and sections. The
output is a corpus of indexed sentences for each biography.
4.2 Entity Recognition
Identiﬁcation of People and Place Entities. People and places correspond
to two of the main elements that characterise a historical meetup; such entities
indicate who was involved and where encounters happened.
Therefore, we use the DBpedia Spotlight
5 tool to automatically anno-
tate mentions of people and places linking them to DBpedia resources.
Once entities are extracted, we select people and places. For places, we ﬁl-
ter the following types: wikidata:Q41176, wikidata:Q486972, dbo:Place,
dbo:Location or wikidata:Q6256. For people, types should be one of
dbo:Person, wikidata:Q215627 or dbo:MusicalArtist. To solve a data qual-
ity issue of DBpedia Spotlight (e.g., errors due to name variation or entity ambi-
guity [22]), we perform an additional evaluation to verify that the entity is an
instance of class wd:Q5 and has a date of birth on Wikidata. We also ﬁlter out
people whose date of birth is posterior to the subjects’ date of death or whose
date of death is before the subject’s dob (meaning that they could not have
actually met them).
The ﬁnal output is a bag of entities containing mentions of person and place,
grouped by sentence and biography.
Identiﬁcation and Normalisation of Temporal Expressions. This task is
divided into two parts:(a) identiﬁcation of temporal expressions and (b)
normalisation.T o (a) extract temporal expressions from text, we use a rule-
base tagger, based on the research by [27] and their implementation of SynTime
6.
The tool is a three-layer system that recognises time expressions using syntac-
tic token types (part-of-speech POS tags) and general heuristic rules. Unlike
SynTime, our implementation exploits the NLTK Toolkit and was developed in
Python. Importantly, the heuristics rules were revised and expanded adapting
them to the Meetups corpus. Furthermore, we classify each expression according
to the type of dates they represent, we use the syntactic token types for this
classiﬁcation: time range (e.g., from 1959 to 1970), time point (e.g., exact date,
23/03/1294), and time reference (e.g., usually incomplete dates (19 April), later
this year). The result is a list of temporal expressions (a short piece of text), for
instance, “2 June 1857” (POS tag “CD NNP CD”) for each sentence.
To allow temporal analysis of meetups with SPARQL, we (b) normalise
temporal expressions into a XSD date time compliant format. We consider time
as ranges, with a start and end time point. We follow the ISO8601
7 format
(YYYY-MM-DD) using two Python libraries (dateutil8 and approx-dates9). On
5 DBpedia-Spotlight: https://www.dbpedia-spotlight.org/.
6 SynTime software: https://github.com/zhongxiaoshi/syntime.
7 ISO8601 International Standard: https://en.wikipedia.org/wiki/ISO 8601.
8 dateutil library: https://dateutil.readthedocs.io/en/stable/index.html.
9 approx-dates library: https://pypi.org/project/approx-dates/.

Musical Meetups Knowledge Graph (MMKG) 115
You are a tool that extracts time references and returns results in ISO8601 date format. I
will provide a sentence and the target text. 1. You should decide if the target text
represents a time reference. 2. If the target text is not a specific time reference
return "NO". 3. If the target text is a specific time reference then estimate the
approximate dates in the context of the sentence. 4. If the information is not enough
to calculate a date then use {}'s biography information. 5. Check the results are in
ISO8601 format. 6. Return the results in JSON format using two keys: start_date and
end_date. Estimate dates after point 4. Don't return fake dates. Sentence {text},
temporal expression {}
↪→
↪→
↪→
↪→
↪→
↪→
↪→
↪→
Listing 1: Prompt to normalise temporal expressions
average 65% of temporal expressions (by biography) are normalised automati-
cally. The left 35% corresponds to expressions such as“the next seven years” or
“of the twentieth century” . To cope with these cases, we make use of the LLM
tool ChatGPT10, providing as input context the temporal expression, the sen-
tence where the expression was identiﬁed, and the subject of the biography (see
Listing 1). We perform dedicated experiments tailoring the prompt to return the
best results regarding quality (accurate to the expression) and coverage (number
of temporal expressions normalised). By including LLMs in the normalisation
process we increase the number of temporal expressions parsed to 82% on aver-
age.
The ﬁnal output is a bag of temporal expressions represented by the textual
evidence, start and end date and additional information such as POS tags and
the way it was normalised (python library or LLM).
Improving Identiﬁcation of Meeting Purpose Using LLM tools. The
main element of a historical meetup is the reason for the encounter, a type of
meetup, which is named as Purpose according to the MEETUPS Ontology. As
detailed in previous work [21] our pipeline included a Machine Learning approach
that follows a semi-supervised classiﬁcation process, annotating each sentence in
the corpus and assigning them one of the meetup types. In [ 21], we identiﬁed
that 74% of predictions were correct, and the 26% left were either Partially
Correct or Incorrect. Therefore, we explored the use of the LLM tool ChatGPT
to increase the accuracy of the automatic classiﬁcation. We followed a zero-shot
learning approach meaning we provided as input the piece of text to analyse, and
the list of classes. We ask the tool to return the two classes that better describe
the meetup type. The prompt (See Listing 2) was designed having three main
elements. First the context of the task (line 1); the expected format output, a
JSON response (line 2); and ﬁnally instructing the tool on the classiﬁcation task
according to the set list of classes (lines 3 to 6).
For each sentence, we gather the two most probable topics of the text. For
instance, the text: ’His father, William Henry Elgar (1821–1906), was raised in
Dover and had been apprenticed to a London music publisher.’ will be classiﬁed
as follows:
10 ChatGPT: https://openai.com/product.

116 A. Morales Tirado et al.
1. “Music making”; the explanation being “The sentence mentions a music pub-
lisher, indicating a connection to music making”; and
2. “Personal life”; the given explanation is “The sentence also provides informa-
tion about the personal life of Elgar’s father”.
1 You are a knowledge classification system that annotates sentences according to their
main topic.↪→
2 Respond in json format using the following keys: thm_type_1, thm_type_2,
thm_explanation_1 and thm_explanation_2.↪→
3 The value for thm_type_1 is the first most probable topic, use only one of the
following keys: ['Music making', 'Business meeting', 'Personal life',
'Coincidence', 'Public celebration', 'Education'].
↪→
↪→
4 The value for thm_type_2 is the second most probable topic, use only one of the
following keys: ['Music making', 'Business meeting', 'Personal life',
'Coincidence', 'Public celebration', 'Education'].
↪→
↪→
5 The value for thm_explanation_1 should be a short explanation for the topic in
thm_type_1. Less than 100 characters.↪→
6 The value for thm_explanation_2 should be a short explanation for the topic in
thm_type_2. Less than 100 characters.↪→
Listing 2: Prompt to classify sentences according to the meetup type (purpose)
We sampled 83 sentences and asked three annotators to verify the accuracy of
the purpose generated. We compared these manual annotations with the results
of the automatic extraction using the Machine Learning (ML) approach, and the
Large Language Model (LLM). Table1 displays the results in terms of Precision.
Using LLM tools leverages the classiﬁcation of text, increasing its precision to
85% (on average).
Table 1. Classiﬁcation results. Comparison ML and LLM Precision @ 1 and 2
# Sentences Machine Learning (ML) prediction LLM prediction
Precision @ 1 Precision @ 2 Precision @ 1 Precision @ 2
Edward Elgar 56 0.34 0.64 0.45 0.73
Yehudi Menuhin 11 0.36 0.45 0.55 0.82
Clara Butt 16 0.69 0.75 0.88 1
83 0.46 0.62 0.62 0.85
The output of this task is a list of sentences grouped by paragraph, each with
two of the most probable meetup types. Since we use LLM tools and the API
to obtain the results. We decided to keep results from the ML approach when it
was not possible to query the tool and obtain an LLM response; this is reﬂected
in the ontology using the mtp:hasSourcePurpose attribute.

Musical Meetups Knowledge Graph (MMKG) 117
4.3 Harmonisation
Coreferences. While the entity identiﬁcation task identiﬁes named entities,
there are also mentions of people and places that are not always automatically
identiﬁed by DBpedia Spotlight, this happens when such mentions are implicit,
in the form of noun phrases or pronouns. For example, people referenced in
the text as he or she. To maximise the identiﬁcation of entities we perform a
Coreference Resolution (CR) task, ﬁnding entities and their coreference mentions
[16] and linking them to DBpedia or Wikipedia resources.
We use the spaCy library coreferee
11. The library receives as input a para-
graph text, then it identiﬁes the entities’ mentions (person or a place) and groups
them into chains of mentions. We use the coreference chains to verify that an
entity is part of the bag of entities in a sentence. New entities are added when
implicit mentions are listed in the chain. The ﬁnal output is a dataset of sen-
tences, each with an extended bag of entities that now includes coreferent men-
tions.
Identiﬁcation of Historical Meetups. At this stage, we have a dataset of sen-
tences, each of them including zero or more entity types (people, place, temporal
expressions and meetup type). However, a historical meetup can be described
in consecutive sentences, having complementary information. In this step, we
harmonise the data by joining adjacent sentences representing the same social
interaction.
To identify historical meetups, we built an algorithm that traverses adja-
cent sentences, incrementally (see Listing 3) and applies a set of heuristics. The
method checks the sentence being evaluated (A) and the previous sentence (B).
The algorithm starts comparing if A has all elements of a meetup: time, place and
person (all sentences have a purpose annotation), and then applies the following
rules:
– If sentence A does not have time but its place is the same as B’s place then
sentence A inherits B’s time (line 6).
– On the contrary, if sentence A does not have a place but its time is the same
as B’s time then sentence A inherits B’s place (line 7).
– If sentence A does not have a person (participants) but its time is the same
as B’s, and A’s place is the same as B’s, then sentence A inherits B’s people
(line 8).
– Finally, if A does not have time and place, but its person is the same as B’s,
then A inherits B’s entities (line 9).
In any case, the algorithm veriﬁes that whenever an entity type is missing, it can
be complemented by the previous sentence given that it complies with having the
same participants, place or time accordingly. If A has all the elements, whether
complemented by B or not, then it is considered a meetup (line 10).
The second part of the algorithm checks whether sentence B complements
sentence A:
11 Coreferee a spaCy library: https://spacy.io/universe/project/coreferee/.

118 A. Morales Tirado et al.
– If all elements of A are the same as B, sentences describe the same evidence
and, consequently, can be considered the same meetup (line 11).
– Other cases include when A and B have the same entity, and B lacks the other
two: 1. Line 13 describes the case of equal A’s and B’s time but B lacking
person and place, 2. line 14 same person, but B having no time or place, and
ﬁnally, 3. line 15 the same place but B having no person or time.
For instance, the evidence “His only formal musical training beyond piano and
violin lessons from local teachers consisted of more advanced violin studies with
Adolf Pollitzer, during brief visits to London in 1877-78.” has all entity types.
People participating (Elgar and Adolf), a location (London) and a date (1877-
18), meeting conditions at line 10. We can mention an example of adding context
thanks to the coreference task. Sentences (B)“Dessay had collaborated frequently
with Michel Legrand in concerts.” and (A) “In May 2009, she dedicated two
concerts of songs written by him in Toulouse.” represent a meetup. Sentence A
satisﬁes conditions in line 11 (having all the elements of a meetup). And in line
13, B lists the same people but no time or place entities. Therefore, sentences A
and B can be joined in a single meetup.
Importantly, when one of the entity types is not present we annotate the
evidence as historical trace. This type of evidence can be useful to complement
social analysis. For example, the sentence “While in France, he visited his fel-
low composer Frederick Delius at his house at Grez-sur-Loing.” describes how
Edward Elgar and Frederick Delius met in France. However, it does not indicate
the date when it took place. This information is still important if we want to
answer questions such as the places he visited or the people he met throughout
his life.
1 A = aSentence() # the current sentence being analysed
2 B = previousSentence() # the previous sentence
3 # place -> all place entities
4 # person -> all people entities
5 # time -> all temporal expressions
6 if !A.time & A.place == B.place -> A.time = B.time
7 if !A.place & A.time == B.time -> A.place = B.place
8 if !A.person & A.time == B.time & A.place == B.place -> A.person = B.person
9 if !A.time & !A.place & A.person == B.person -> A.time = B.time & A.place = B.place
10 if A.time & A.place & A.person -> A = meetup
11 if A.time = B.time & A.place = B.place & A.person = B.person
12 -> meetup = A + B # sentence A and B have the same entities, can be considered a
meetup↪→
13 if A.time = B.time & !B.person & !B.place or
14 A.person = B.person & !B.time & !B.place or
15 A.place = B.place & !B.person & !B.time
16 -> meetup = A + B # A + B have complementary entities and can be considered a
meetup↪→
Listing 3: Historical meetups identiﬁcation
The output is a dataset that contains the text (typically a sentence or a set
of sentences), and the list of entities that account for a meetup. The results

Musical Meetups Knowledge Graph (MMKG) 119
are stored in CSV ﬁles, grouped by biographies. This dataset is ready to be
transformed into the MMKG in the following step.
4.4 Knowledge Graph Construction
The KG was constructed using the CSV ﬁles resulting from the process described
so far and applying the Meetups ontology described in Sect.3. We use SPARQL
Anything [2] and design CONSTRUCT mappings, to create triples from each
biography. MMKG contains data from 33,309 artists’ biographies, 16,748 of
which have at least one historical meetup. The KG describes a total of 45,812
historical meetups. The meetups mention 49,170 people involved in diﬀerent
encounters. So far, the historical meetups gathered around 7,107 places and
51,120 time expressions. The KG is currently published in Turtle and N-quads
RDF format and available in the MMKG GitHub repository.
5 MMKG Evaluation
We evaluate MMKG by implementing queries to answer the competency ques-
tions of the Meetups Ontology and by means of a survey with domain experts.
5.1 Answering CQs
The knowledge requirements, which are the foundation of the Meetups ontology
design, were formalised as a list of Competency Questions (CQs) in [21]. In this
section, we take as guidelines these CQs (Table212) and design a series of SPARQL
queries13 to evaluate that the MMKG data meets the knowledge requirements.
Table 2. List of Competency Questions (CQs).
# Competency Questions Entity focus
1 What places did musician Z visit in his/her career? Place
2 Where did musician X and performer Y meet? where?
3 Why did musician X and performer Y meet? Purpose /
4 What is the nature of the event (a celebration, a festival, a
private event, a performance, accidental)?
Meetup type why?
5 When did musician X and performer Y meet? Temporal
6 Did musician X and performer Y ever meet? when?
7 Who other musicians were working at the same time? Participants
8 What was the composer’s network? who?
12 Due to space constraints, Table 2 displays a summary of the CQs.
13 Queries and results obtained available in the MMKG repository - queries folder
https://github.com/polifonia-project/meetups-knowledge-graph/ .

120 A. Morales Tirado et al.
CQs Focus on Place Dimension. One of the main requirements is about the
places where people met or visited. We take the example of the German pianist
Clara Schumann and build a query (Figs. 3aa n d3b) that retrieves the list of
places she visited during her life (16 places in total). To answer question 2 we
build a query that lists all the places she and Joseph Joachim shared, evidence
shows that they met in Germany and the UK.
(a) Query: Places visited by an artist
 (b) Results: Places visited by an artist
Fig. 3. Illustrative example for CQs focused on place entities
CQs Focus on Purpose. Following the previous example, we can expand the
queries to include the meetup’s purpose and answer questions 3 and 4. Evidence
shows that Clara and Joachim’s meetings mainly related to “Music Making”.
For instance, “In October-November 1857, Schumann and Joachim went on a
recital tour to Dresden and Leipzig” .
CQs Focus on Temporal Expressions. In the previous example, we have
textual evidence that indicates the time Clara and Joachim met in 1857. This
information is available in the MMKG and can be queried in the form of start
and end dates (Figs. 4aa n d4b).
(a ) Query: Date of the meetup
 (b) Results: Date of the meetup
Fig. 4. Illustrative example for CQs focused on temporal expressions
CQs Focus on Person Dimension. We follow the previous example and build
queries that return the list of people Clara met (17 people in total) (Fig. 5a).
Importantly, we can expand this query to include all the artists Clara met (a
total of 50 people), even if the evidence does not provide data on the time or
place they met (a historical trace); results are shown in Fig.5b.

Musical Meetups Knowledge Graph (MMKG) 121
(a)Query: M eetupsa n d participants
 (b) Res ults: Allpeople she met
Fig. 5. Illustrative example for CQs focused on people
Importantly, we produced SPARQL queries to extract statistics about the
top visited places, people met, years of activity and purpose of meetings for each
artist. These queries can be found in the MMKG repository
14
5.2 Feedback Questionnaire from Domain Experts
In a survey with 12 domain experts from the Music Department of our Univer-
sity, we evaluated the value to users of MMKG 15. Participants were either/or
researchers (75%), musicians (33%), educators (33%), and historians (25%), with
a signiﬁcant 91.7% reporting daily engagement with music-related content. All
the respondents agreed on the value of documenting musical history encounters,
considering them either important (50%) or very important (50%). All respon-
dents reported not being aware of any tool/database to store and organise histor-
ical music encounters. We asked about the value of speciﬁc elements of the ontol-
ogy. All respondents rated the importance of documenting the people involved
in musical encounters as “very important” (Fig. 6). The place and time of the
encounter were rated very important and important by 83.33% and 16.67%,
respectively. Responses were varied for the purpose of encounters: 58.34% rated
it as “Very Important”, 33.33% as “Important”, and 8.33% as “Moderately”
important.
Business meetings and music-making have been highly valued throughout
music history, which received over 83% of the rating as “very important” and
“important, respectively”. The survey also revealed that 75% of the respondents
respectively rated personal life and public celebration as “very important” and
“important” purpose for musical encounters. While education and coincidence
were rated the same by 66.67%.
In addition, all participants agree on the utility of exploring the geographical,
temporal, and thematic proximity of subjects, even outside direct evidence of
documented encounters. Finally, the usefulness of knowledge graphs in teaching
music history is largely (75%) acknowledged by experts.
14 Stats queries: https://github.com/polifonia-project/meetups-knowledge-graph/
blob/main/queries/top-entities.sparql.
15 Complete results can be found at this address: https://docs.google.com/document/
d/1PGknESmJm4f -QwSdebTuiHIZ3bMaBrtcs4-9AKLPcc/edit?usp=sharing.

122 A. Morales Tirado et al.
Fig. 6. Dimensions in musical encounters.
6 Using the MMKG
In this section, we discuss the value of the MMKG from the perspective of both
domain experts in their research and exploration and developer communities
leveraging the data to build novel applications and exploration tools.
6.1 Music Historians and Domain Experts
The MMKG, as described in Sect. 2, oﬀers an exploration of historical informa-
tion at a macro-scale using EDA principles, in ways not possible when simply
studying the biographies of individual musical ﬁgures.
This is especially signiﬁcant for the period before globalisation through
broadcasting and recording technologies, when it is often much less obvious
how musical ideas and inﬂuences were disseminated. The MMKG opens the
possibility of identifying points of cultural and musical exchange that have been
unsuspected till now, revealing patterns of travel and contact, and intersections
of musical ﬁgures identiﬁed by place and time. For example, from the biography
of a composer, the researcher might generate a visualisation that reveals meet-
ings with another musician with whom they were not previously known to have
been in contact. This may shed new light on music the composer subsequently
wrote, or on a performer’s subsequent repertoire choices. Similarly, a previously
unknown meeting of a musician with an instrument maker might turn out to be
related to the development of a new or modiﬁed instrument, or the composition
of a new piece for a particular type of instrument. The knowledge graph may
also reveal a cluster of meetings in a particular place, prompting the researcher
to develop new research questions exploring that place as musically or culturally
signiﬁcant.
Traditional humanities research methods are based on linear investigations
in which evidential sources are aligned to research questions and interrogated
within predetermined contexts. In providing a non-linear vision of accumulated
data capable of stimulating new and often unconsidered ideas, MMKG both
complements and expands this process. It oﬀers a diﬀerent set of perspectives
on which to base the evaluation and ordering of data, to shape research questions
and to determine the direction and priorities of a research project.

Musical Meetups Knowledge Graph (MMKG) 123
6.2 Developer Communities
In Sect. 2 we give an overview of some of the principles of Exploratory Data
Analysis, within the context of the MMKG project. These are facilitated by the
use of carefully selected and formatted attributes and annotations that allow
developers to leverage and integrate the data into data-driven visualisations
and applications. These annotations can be used across various mapping and
time-display technologies, libraries, and software. Geolocation data, in partic-
ular, enables seamless integration with mapping libraries, Geographical Infor-
mation System (GIS) software, and advanced geoprocessing routines. Common
JavaScript web mapping libraries such as Leaﬂet
16 or Openlayers17 can be used
to render points or clusters on maps, making use of additional annotations for
nuanced visualisations such as colour-coding by theme. The data is also adapt-
able for integration into GIS software, allowing intricate geoprocessing and geo-
analysis tasks such as creating thematic heatmaps, plotting paths, implementing
advanced clustering algorithms, and executing task-speciﬁc querying and analy-
sis processes. Temporal data oﬀers similar visualisation techniques through the
use of timeline displays, frequency distribution analysis, and visual time-based
search tools. Again, GIS software can also leverage this temporal information to
provide advanced temporospatial geoprocessing.
Beyond academic research, the MMKG oﬀers developers the chance to cre-
ate applications in other domains such as education, archives, and exploration.
MMKG’s data can power interactive learning platforms, browsable archive repos-
itories, immersive museum exhibits and exploration tools. This ﬂexibility caters
to diverse needs, showcasing KG’s potential to transcend disciplinary boundaries.
Accessible through an open SPARQL endpoint, the KG seamlessly integrates
into numerous platforms such as mobile apps and desktop applications. Develop-
ers can integrate straightforward HTTP calls into their application development
and also build intermediary APIs, facilitating eﬃcient data retrieval and reuse
of common SPARQL queries. This accessible approach, often using standardised
formats like JSON, not only streamlines integration but also promotes collabo-
ration within the developer community, encouraging collective utilisation.
7 Resource Availability, Reusability, Sustainability
Our work on this project has been completed whilst adhering to the FAIR 18
principles. We have built the resource in a number of speciﬁc ways to ensure that
the outputs are in compliance with the FAIR Guiding Principles for scientiﬁc
data management and stewardship.
Resource availability for the MMKG is ensured through its presence on
GitHub, providing both source data and documentation. Additionally, a perma-
nent SPARQL endpoint is openly accessible on the web, facilitating ease of use
16 https://leaﬂetjs.com/.
17 https://openlayers.org/.
18 https://www.go-fair.org/fair-principles/.

124 A. Morales Tirado et al.
and integration into various applications. Furthermore, developers can encap-
sulate these results as API calls, promoting sharing and collaboration within
the developer community. These features contribute to the sustainability of the
MMKG, ensuring ongoing accessibility, usability, and collaborative engagement
over time.
8 Related Work
Below we consider related work on musical social relationships, the publishing of
biographical and prosopographical data, event-based KGs and their application.
Within the musical domain, [6] presents an analysis of musical inﬂuence net-
works for sample-based music. In contrast, [15] analyses the MusicBrainz dataset
relationship metadata to uncover how music artists inﬂuence one another.
For biographical/prosopographical data, [ 26] provide a linked data model
to integrate biographical and cultural heritage data while [ 5] presents a KG of
biographical information of German academics from the 16th to 18th century.
[17] performs similar research but with short textual biographies about Finnish
and Swedish academics. [20] extracts information from text about the historical
movements of people, focusing on biographies from the ﬁrst half of the 20th
century and [ 4] presents a relational database of biographies spanning 5,500
years. [11,13,24] and [12] argue towards the adoption of Linked Data practices
for the development of databases, applications and Artiﬁcial Intelligence systems
based on biographies and/or prosopographies.
An Event KG is a graph where the knowledge representation is centred upon
dynamic events happening in time rather than entities and relations. While [10]
provides a general survey of Event KGs, [19] and [18] research related technical
aspects involved in their construction KGs, such as event coreference resolution
and temporal knowledge extraction from texts.
In historiography [7] and [9] present an event KG representing 690 thousand
events enriched by a timeline generation system representing biographies. In [14]
the available archive information of Finland’s involvement in WWII is rendered
as an event KG.
While relevant resources have been published in the domains as mentioned
earlier, there is however evidence (Table 3) of a resource gap when presenting
evidence of historical collaborations between personalities relevant to the music
history domain. MMKG addresses this gap.

Musical Meetups Knowledge Graph (MMKG) 125
Table 3. Knowledge Graph comparison. P - People, L - Location, T - Time, and R -
Reason; e - related to an event only, r - related to a role only.
P T L R Description Size
BiographySampo [ 13] ✓ e ✓ ✗ Finnish Biographies 13.100
biographies
AcademySampo [ 17] ✓ e ✓ ✗ Finnish university
student records
27,500 student
records
Event KG [ 8] ✓ e ✓ ✗ News, focus on events 18,510 news
articles
Early Modern Scholarly
Career KG [ 5]
✓ r ✓ ✗ German biographies
Professional
development
Two sources, #
of biographies
unknown
Meetups Musical KG ✓ ✓ ✓ ✓ Music personalities 33.300
biographies
9 Conclusions and Future Work
In this resource paper, we introduced MMKG, a knowledge graph of documen-
tary evidence of social interaction for supporting research in music history. Our
work shows the potential of hybrid methods for knowledge extraction, combin-
ing knowledge engineering with techniques from traditional NLP and current
LLMs tools. Future work includes studying how to improve the coverage of the
geospatial and temporal annotations of the biographies, for example, tackling
implicit, contextual time references. Further research regarding social iterations
and network inﬂuence (e.g., musical and creative aspects) are natural direc-
tions to expand the use of the KG. A user interface for leveraging the potential
of MMKG is under development in close collaboration with domain experts.
MMKG and the related tools will be applied to teaching and learning content
as well as scholarship of the Music Department of the OU.
Acknowledgements. This work was supported by the EU’s Horizon Europe
research and innovation programme within the Polifonia project (grant agreement N.
101004746).
References
1. Adamou, A., Brown, S., Barlow, H., Allocca, C., d’Aquin, M.: Crowdsourcing
linked data on listening experiences through reuse and enhancement of library
data. Int. J. Digit. Libr. 20(1), 61–79 (2019)
2. Asprino, L., Daga, E., Gangemi, A., Mulholland, P.: Knowledge graph construction
with a fa¸cade: a uniﬁed method to access heterogeneous data sources on the web.
ACM Trans. Internet Technol. 23(1), 1–31 (2023)
3. de Berardinis, J., et al.: The polifonia ontology network: building a semantic back-
bone for musical heritage. In: Payne, T.R., et al. (eds.) ISWC 2023. LNCS, vol.

126 A. Morales Tirado et al.
14266, pp. 302–322. Springer, Cham (2023). https://doi.org/10.1007/978-3-031-
47243-5 17
4. Beyt´ ıa, P., Schobin, J.: Networked pantheon: a relational database of globally
famous people. Available at SSRN 3255401 (2018)
5. Blanke, J., Riechert, T.: Towards an RDF knowledge graph of scholars from early
modern history. In: 2020 IEEE 14th International Conference on Semantic Com-
puting (ICSC), pp. 471–472. IEEE (2020)
6. Bryan, N.J., Wang, G.: Musical inﬂuence network analysis and rank of sample-
based music. In: ISMIR, pp. 329–334 (2011)
7. Gottschalk, S., Demidova, E.: EventKG: a multilingual event-centric temporal
knowledge graph. In: Gangemi, A., et al. (eds.) ESWC 2018. LNCS, vol. 10843, pp.
272–287. Springer, Cham (2018). https://doi.org/10.1007/978-3-319-93417-4
18
8. Gottschalk, S., Demidova, E.: EventKG - the hub of event knowledge on the web
- and biographical timeline generation (2019). http://arxiv.org/abs/1905.08794
9. Gottschalk, S., Demidova, E.: EventKG+BT: generation of interactive biography
timelines from a knowledge graph. In: Harth, A., et al. (eds.) ESWC 2020. LNCS,
vol. 12124, pp. 91–97. Springer, Cham (2020). https://doi.org/10.1007/978-3-030-
62327-2 16
10. Guan, S., et al.: What is event knowledge graph: a survey. IEEE Trans. Knowl.
Data Eng. (2022)
11. Hyv¨ onen, E.: Using the semantic web in digital humanities: shift from data pub-
lishing to data-analysis and serendipitous knowledge discovery. Semant. Web 11,
187–193 (2020)
12. Hyv¨ onen, E., et al.: Linked data–a paradigm change for publishing and using biog-
raphy collections on the semantic web. Biograph. Data Digit. World (2022)
13. Hyv¨ onen, E., et al.: BiographySampo – publishing and enriching biographies on
the semantic web for digital humanities research. In: Hitzler, P., et al. (eds.) ESWC
2019. LNCS, vol. 11503, pp. 574–589. Springer, Cham (2019). https://doi.org/10.
1007/978-3-030-21348-0 37
14. Koho, M., Ikkala, E., Leskinen, P., Tamper, M., Tuominen, J., Hyv¨ onen, E.:
WarSampo knowledge graph: Finland in the second world war as linked open data.
Semant. Web 12(2), 265–278 (2021)
15. Kopel, M.: Analyzing music metadata on artist inﬂuence. In: Nguyen, N.T.,
Trawi´nski, B., Kosala, R. (eds.) ACIIDS 2015. LNCS (LNAI), vol. 9011, pp. 56–65.
Springer, Cham (2015). https://doi.org/10.1007/978-3-319-15702-3 6
16. Lata, K., Singh, P., Dutta, K.: Mention detection in coreference resolution: survey.
Appl. Intell. (2022). https://doi.org/10.1007/s10489-021-02878-2
17. Leskinen, P., Hyv¨ onen, E.: Using the AcademySampo portal and data service
for biographical and prosopographical research in digital humanities. In: ISWC-
Posters-Demos-Industry 2021 International Semantic Web Conference (ISWC)
2021: Posters, Demos, and Industry Tracks. CEUR-WS. org (2021)
18. Liu, Y., Hua, W., Zhou, X.: Temporal knowledge extraction from large-scale text
corpus. World Wide Web 24, 135–156 (2021)
19. Lu, J., Ng, V.: Event coreference resolution: a survey of two decades of research.
In: IJCAI, pp. 5479–5486 (2018)
20. Menini, S., Sprugnoli, R., Moretti, G., Bignotti, E., Tonelli, S., Lepri, B.: RAM-
BLE ON: tracing movements of popular historical ﬁgures. In: Proceedings of the
Software Demonstrations of the 15th Conference of the European Chapter of the
Association for Computational Linguistics, pp. 77–80 (2017)

Musical Meetups Knowledge Graph (MMKG) 127
21. Morales Tirado, A., Carvalho, J., Mulholland, P., Daga, E.: Musical meetups: a
knowledge graph approach for historical social network analysis. In: SEMMES
2023: Semantic Methods for Events and Stories Workshop co-located with 20th
European Semantic Web Conference (ESWC 2023) (2023). https://ceur-ws.org/
Vol-3443/ESWC
2023 SEMMES Meetups-CR.pdf
22. Olieman, A., Azarbonyad, H., Dehghani, M., Kamps, J., Marx, M.: Entity linking
by focusing DBpedia candidate entities. In: Proceedings of the ﬁrst international
workshop on Entity recognition & disambiguation - ERD 2014, pp. 13–24 (2014).
https://doi.org/10.1145/2633211.2634353
23. Polkinghorne, D.E.: Narrative Knowing and the Human Sciences. SUNY Press
(1988)
24. Tamper, M., Leskinen, P., Apajalahti, K., Hyv¨ onen, E.: Using biographical texts
as linked data for prosopographical research and applications. In: Ioannides, M.,
et al. (eds.) EuroMed 2018. LNCS, vol. 11196, pp. 125–137. Springer, Cham (2018).
https://doi.org/10.1007/978-3-030-01762-0
11
25. Tukey, J.W., et al.: Exploratory data analysis, vol. 2. Reading (1977)
26. Tuominen, J.A., Hyv¨ onen, E.A., Leskinen, P.: Bio CRM: a data model for rep-
resenting biographical data for prosopographical research. In: Proceedings of the
Second Conference on Biographical Data in a Digital World 2017 (BD2017). CEUR
Workshop Proceedings (2018)
27. Zhong, X., Sun, A., Cambria, E.: Time expression analysis and recognition using
syntactic token types and general heuristic rules. In: Proceedings of the 55th
Annual Meeting of the Association for Computational Linguistics (2017)

Generate and Update Large HDT RDF
Knowledge Graphs on Commodity
Hardware
Antoine Willerval1,2(B) , Dennis Diefenbach2 , and Angela Bonifati1
1 CNRS, LIRIS UMR 5205, University of Lyon, Lyon, France
angela.bonifati@univ-lyon1.fr
2 The QA Company SAS, Saint-´Etienne, France
{antoine.willerval,dennis.diefenbach}@the-qa-company.com
Abstract. HDT is a popular compressed ﬁle format to store, share and
query large RDF Knowledge Graphs (KGs). While all these operations
are possible in low hardware settings (i.e. a standard laptop), the gener-
ation and updates of HDT ﬁles come with an important hardware cost
especially in terms of memory and disk usage.
In this paper, we present a new tool leveraging HDT, namely k-
HDTDiﬀCat, that allows to a) reduce the memory and disk footprint
for the creation of HDT ﬁles and to b) remove triples from an existing
HDT ﬁle thus allowing updates.
We show that in a system with 8 times less memory, we can achieve
HDT ﬁle generation in almost the same time as existing methods. More-
over, our system allows to remove triples from an HDT ﬁle catering for
updates. This operation is possible without the need to uncompress the
original data (as it was the case in the original HDT ﬁle) and by keeping
low memory consumption.
While HDT was suited for storing, exchanging and querying large
Knowledge Graphs in low hardware settings, we also oﬀer the novel func-
tionality to generate and update HDT ﬁles in these settings. As a side
eﬀect, HDT becomes an ideal indexing structure for large KGs in low
hardware settings making them more accessible to the community.
In particular, we show that we can compress the whole Wikidata
graph, which is the largest knowledge graph currently available, on a
standard laptop with 16 GB of RAM as well as generate Wikidata indexes
that are at most 24 h behind the live Wikidata endpoint.
Keywords: HDT
· HDTq · HDTCat · HDTDiﬀ · LUBM · Wikidata ·
Update
1 Introduction
RDF Knowledge Graphs (KGs) are growing in size, storing and querying them
becomes increasingly challenging. For example, the amount of triples in the Wiki-
data KG increased from 18 billion to 19.2 billion in the last year. Moreover,
c⃝ The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
A. Mero˜no Pe˜nuela et al. (Eds.): ESWC 2024, LNCS 14665, pp. 128–144, 2024.
https://doi.org/10.1007/978-3-031-60635-9_8

Generate and Update Large HDT RDF Graphs 129
serving large graphs can easily become expensive in terms of hardware resources,
making them inaccessible for consumers in low hardware settings, thus impeding
the democratization of the Web.
To overcome this problem, the HDT ﬁle format was created [10]. HDT uses
succinct data structures [ 13] to store RDF graphs. The aim of succinct data
structures is to compress the underlying dataset as much as possible while pre-
serving the query capabilities. In the case of HDT, it is possible to compress
RDF graphs to similar sizes as a GZIP compressed NTriple ﬁle while allowing
to search for triple patterns at a speed that is in the same order of magnitude
of common triple stores. As a concrete example, it is possible to compress the
whole Wikidata KG to an HDT ﬁle of 300 GB and have a triple pattern access
that is equal or faster then the one of the public Wikidata query service.
This explains why HDT is used as the backbone of past projects where scal-
ability becomes a problem. For instance in the LOD laundromat [2] in order to
expose datasets in the LOD cloud, for question-answering engines [3] and as an
indexing structure of Linked Data Fragments [18]. HDT was also used to store
the 28 billion triples dump of the LOD cloud called LOD-a-lot [8].
HDT is used to provide large data, for example in LOD laundromat, providing
an infrastructure to clean and serve all datasets in the LOD cloud and LOD-a-lot
[8], an index of the whole Linked Open Data cloud published as HDT. For the
question answering system WDAqua-core1 [5], a question answering system that
allows to query some of the largest datasets in the LOD cloud, namely: DBpedia,
Wikidata, MusicBrainz and DBlp. But HDT is mostly use for triple stores and
RDF graph querying like Linked Data Fragments [18] to query the Web of data
on Web-scale by moving the query load from servers to clients, qEndpoint [19]a
SPARQL endpoint that uses HDT as an underlying index and OSTRICH [17], a
hybrid archiving approach for RDF (Resource Description Framework) graphs.
It is designed to provide eﬃcient triple pattern queries for diﬀerent versioned
query types while keeping storage requirements reasonable.
The key contribution of the paper is k-HDTDiﬀCat, a new method to combine
and delete triples from one or multiple HDT ﬁles into a new one. Unlike HDTCat
[4], a method to combine two HDT ﬁles into one HDT ﬁle, our method allows to
combine an arbitrary number of HDT ﬁles while keeping a small time overhead
per added HDT ﬁle. It allows to create big HDT ﬁles by splitting the HDT
generation into small HDT ﬁles. The small HDT ﬁles are then merged with k-
HDTDiﬀCat into one HDT ﬁle. Moreover k-HDTDiﬀCat allows also to eliminate
triples from already generated HDT ﬁles.
With provide experiments showing the eﬃciency of our method compared
with previous implementation in systems with few resources.
While storing, exchanging and querying HDT ﬁles is easy in low hardware
settings, this is not the case for the generation and updates. The tool presented
in this paper ﬁlls exactly this gap, i.e. allowing to eﬃciently generate and update
HDT ﬁles in low hardware settings. The paper is organized as follows.
We will ﬁrst explain the HDT internals in Sect. 2, in Sect. 3 we discuss
the related works, in Sect. 4 we present our tool, in Sect. 5 we present our

130 A. Willerval et al.
experimental results and within Sect.6 a presentation of the open source repos-
itory where to ﬁnd our tool with a command line to use it.
2 HDT Internals
Before describing the related works and our contribution, we describe on a high
level the internals of a HDT ﬁle. HDT [ 10,11] is a ﬁle format to compress an
RDF graph while keeping the ability to query over it by triple patterns, it is
composed of 3 components. The header component, the dictionary component
and the triples component.
Fig. 1. The diﬀerent HDT and HDTq
components in the dictionary part.
Fig. 2. The diﬀerent HDT and HDTq
components in the triples part.
H eader. It contains metadata information about the HDT ﬁle like the number
of RDF terms, the raw size, the number of distinct subjects, etc. Due to the
trivial aspect of this component, we won’t consider it in the future sections.
Dictionary (Fig.1). It contains a mapping between the terms in the RDF graph
(i.e. URIs, Literals and Blank Nodes) and numerical IDs.
The default dictionary is called Four Section Dictionary (FSD), previous
HDT Dictionary [10] is composed of four sections: Shared (SH), Subjects (S),
Predicates (P) and Objects (O). The Shared section contains all terms that
appear both as a subject and as an object inside the graph. The subject section
contains terms that appear exclusively in the subject position. Similarly with
the object section, only containing the term appearing at the object position.
The predicate section contains all terms contained in the predicate position. In
each section the terms are sorted lexicographically and compressed using Front-
Coding [21] which is a technique based on diﬀerential compression over the string
preﬁxes.
Other dictionary implementations exist called Multiple Section Dictionaries
(MSD) [16]. These versions are based on the FSD above, but are splitting the
literals in the object section by data-types or language. This saves space by
grouping the literals with the same datatypes and allows quick retrieval of the

Generate and Update Large HDT RDF Graphs 131
literals of a given datatype or language while allowing a fast lookup of a datatype
or language using the literal numerical ID.
T riples (Fig.2). It contains the triples encoded with the above IDs using adja-
cency lists. On a high level these are lists of triples sorted by subject-predicate-
object (i.e. an SPO index). These are stored in a compressed format using two
bitmaps and two sequences. The shared section terms are represented by adding
to non-shared subject/object terms the count of shared terms. If the ID is lower
than the shared terms count, it means the ID is representing the position inside
the shared section. If the ID is greater than the shared terms count, it means
the ID is representing a subject or an object.
Overall one can summarize HDT contains two components, the Dictionary
component and the Triples component that use a global ordering to store and
compress the data.
2.1 HDTq
HDTq [9] is an extension of HDT to allow the storage of named graphs orquads.
In the dictionary, it adds another sorted section to store the named graphs.
(HDTq dictionary part of Fig.1).
In the triples component, this new section of n named graphs is reﬂected
with n bitmaps that have a length corresponding to the number of triples. Each
bitmaps indicates with 1 if the corresponding triple is in the named graph asso-
ciated with the bitmap. These bitmaps are compressed using Roaring bitmaps
[15]. (HDTq triples in Fig.2).
Another version of HDTq exists using one bitmap per triple instead of one
bitmap per named graph. We do not consider this version because it was getting
worse results than the one bitmap per named graph version.
3 Related Work
We ﬁrst describe the current methods to compress an RDF ﬁle into HDT and
then describe general RDF graph indexing methods. There are currently 3 meth-
ods to compress an RDF ﬁle to HDT.rdf2hdt [11], is the original implementation
used to compress an RDF ﬁle to HDT. This implementation is fully in memory.
It basically performs a lexicographic sorting of the terms (URIs, Literals, blank
nodes) for the dictionary and of the IDs in SPO order in the triples. HDT-MR
[12], is an implementation using a MapReduce setup to compress large dataset
into HDT. This algorithm can only be executed on a MapReduce cluster. This
requirement is a hard stop for users having access only to commodity hardware.
HDTCat [4], is an algorithm to merge 2 HDT ﬁles together without the need
to uncompress the data. This method was used to compress large HDT ﬁles
by creating small HDT ﬁles and combine them recursively into one big HDT
ﬁle. There are no methods to delete triples from an existing HDT ﬁle without
uncompressing the dataset.

132 A. Willerval et al.
Besides methods to compress RDF graphs to HDT, the most related works
include triple store indexing strategies. In these cases the RDF graph is stored
into some internal indexing structure that is subsequently used to query it via
SPARQL. Typical indexing structures are:
– B+-trees like Blazegraph
1, Apache Jena2 or RDF4J Native Store3.
– Storing the graph into a SQL database, like Virtuoso [6].
– Custom binary structure, for example inside QLever [ 1] using a read-only
compressed data structure.
Overall these indexing strategies are memory intensive making it diﬃcult to
run them on commodity hardware.
4 Contribution
In this paper, we present k-HDTDiﬀCat, a new tool that allows to merge and
update multiple HDT ﬁles. In combination with an indexing algorithm, it can
be used to compress and update large HDT ﬁles in low hardware settings. More
precisely, we provide the following contributions:
1. Allow to combine multiple HDT ﬁles together at the same time.
2. Allow to subtract triples from HDT ﬁles.
3. Extend these algorithms also for named graphs.
4.1 k-HDTCat
While all functionalities are integrated in the same tool, we ﬁrst describe the
functionality of k-HDTCat, i.e. merging together mutliple HDT ﬁles.
Dictionary Generation. An HDT dictionary is composed of multiple sorted
sections. Inside each section the RDF terms respect multiple properties,
1. An RDF term is unique in its section. (No duplicated term)
2. If an RDF term is used as a subject and as an object, it is inside the shared
section and doesn’t appear inside a subject or an object section.
3. An RDF term is represented by its position or index in the section.
We describe in the following how we merge multiple HDT ﬁles named
HDT
1 ...HD T k with Shared, Subject, Object and Predicate sections named
respectively SH1 ...S H k , S1,...S k , O1,...O k and P1,...P k .
As all sections are sorted, we create iterators over each section type. itSH is
an iterator over all shared sections (SH1,...S H k ) that returns all terms of the
shared sections sorted without duplicates using a merge join. Analogously we
1 https://blazegraph.com.
2 https://jena.apache.org/index.html.
3 https://rdf4j.org/.

Generate and Update Large HDT RDF Graphs 133
create itS for subjects, itO for objects and itP for predicates. By comparing itS
and itO we can compute the terms that need to be moved into the new shared
section SHnew with the already shared terms from itSH . All terms that are not
moved to this section will remain in the Snew , Onew sections respectively. With
that, we respect the properties 1 and 2.
Added to this method, we keep track of the original term index with the origin
HDT IDs and sections, so when we compute the end sectionSnew , Onew , SHnew
and Pnew , we have both the old and new IDs of each term. Using them, we create
4 arrays MSec,HDT , one per HDT ﬁle and section Sec ∈{ S, O, P, SH },HD T ∈
{HDT 1,...HD T k }. We call them “maps” and we ﬁll them using the origin term
location i.e. ID/Section/HDT ﬁle as the index and the new location and if the
term is shared for the value. M
Sec,HDT [OldID ]=( Ne wID,Is Sh a re d ).
With this task done, we have now access to the new sections for the dictionary
with a mapping between the old and the new term’s indexes.
Triples Component Generation. The dictionary being created, we need to
build the triples component, for this part, we extended the HDTCat [4] algorithm
to handle multiple triples by using a merge join. First we read the triple ids
from the HDT ﬁles into multiple stream mapped using MSec,HDT , the arrays
created during the dictionary creation. Before merging them, we need to take into
consideration that a subject or object term can become a shared term leading
to our ids in our streams to be unsorted due to the shared IDs representation
deﬁned in the triples paragraph in Sect.2.
To ﬁx that we split our streams into two diﬀerent streams. A stream with
the triples with shared subjects and a stream with the triples with non-shared
subjects. Once this is done, we use a merge join to create two streams from all
the streams, removing the duplicated terms at the same time.
This solves the unsorted problem for the subject terms, not for the object
terms. To sort again the objects, we can use the fact that our triples are sorted
by subjects and predicates, so if we peek from our stream all the triples with the
same subject and predicate, we can retrieve all the unsorted objects for a given
(subject, predicate) couple. This number of objects is usually small compared to
the triples count, so we can sort them in memory and stream the sorted results.
The result streams being sorted, we can create our triple component.
Large File Indexing Using k-HDTCat. Using this new algorithm version,
we can combine multiple HDT ﬁles into one. Removing the overhead added by
the generation of the HDT ﬁle, but inducing the overhead of reading multiple
HDT ﬁles at once. We made the hypothesis that this added overhead isn’t as big
as the one removed from the original HDTCat. This can be used to index big
HDT ﬁles by ﬁrst chunking the data and indexing smaller HDT ﬁles and then
combining them to create a bigger HDT ﬁle using k-HDTCat. A comparison
with existing methods is available in Sect.5.2 (Fig. 3).

134 A. Willerval et al.
Fig. 3. k-HDTCat Merge streams
 Fig. 4. k-HDTDiﬀCat Merge streams
4.2 k-HDTDiﬀCat
The main drawback of HDTCat is the fact that it is only providing the addition
on datasets, but not the ability to remove triples from datasets. To do it, one is
forced to reindex the dataset without the unwanted triples.
To overcome this missing part, we created k-HDTDiﬀCat, a modiﬁed version
of k-HDTCat to remove triples from one or multiple HDT ﬁles into one HDT
ﬁle. It is built on top of k-HDTCat.
Dictionary Generation. Unlike k-HDTCat, during a diﬀ, an RDF term can
be removed from the dictionary of a HDT ﬁle, leading to 3 cases,
1. The term is still used at least once in the same section, in which case nothing
should be done.
2. The term was a shared term, but now it is only an object or a subject, then
we need to consider its sharedness loss.
3. The term isn’t used anywhere in the dictionary, then we need to completely
remove it.
To mark a triple to be deleted, we are using a bitmap per HDT ﬁle. If the bit
at the index i is set to 1, it means that the triple at the indexi will be removed
from this HDT ﬁle.
To compute the deleted triples, we ﬁrst create one bitmap per section per
HDT ﬁle, a bit set to 1 in a bitmap represents if an term is used inside the
section. We then ﬁll the bitmaps by reading the triples for each HDT ﬁle while
ignoring the ones with the same position as a 1 in the triples bitmap for this
HDT.
With these bitmaps, when we are reading a section, we only have to check
ﬁrst if this term should be read or ignored.
Due to the property 2, we need to check if a shared element is still shared
after the diﬀcat. To do that, as represented in Fig.4, we are merging the shared

Generate and Update Large HDT RDF Graphs 135
Data: itS ,i tO two sorted iterators of respectively subjects and objects terms.
Result: it′
S ,i t′
O
,i t′
SH
, three sorted iterators of the ﬁnal subjects, objects and
shared terms.
it′
S ←∅ it′
O ←∅ it′
SH ←∅
SharedLoop: while itS ̸= ∅ and itO ̸= ∅ do
Ne wSu b je c t ← Next(itS ) N ewObject ← Next(itO )
while Ne wSu b je c t ̸= N ewObject do
if NewSubject < NewObject then
it′
S ← it′
S ∪{ Ne wSu b je c t}
if itS = ∅ then
break SharedLoop
Ne wSu b je c t ← Next(itS )
else
it′
O ← it′
O ∪{ N ewObject }
if itO = ∅ then
break SharedLoop
N ewObject ← Next(itO )
it′
SH ← it′
SH ∪{ Ne wSu b je c t}
while itS ̸= ∅ do
it′
S ← it′
S ∪{ Next(itS )}
while itO ̸= ∅ do
it′
O ← it′
O ∪{ Next(itO )}
Algorithm 1: Split subject/object iterators into subject/object/shared iter-
ators
term iterator itSH with both the subjects itS and the objects itO iterators. As
described in Algorithm 1, by comparing the two iterators in a merged way, k-
HDTDiﬀCat is able to recompute the shared terms with the subjects/objects
when merging the HDT ﬁles by comparing when two elements in the iterators
are equal.
We then run the k-HDTCat method to compute the dictionary without using
it
SH at the end because it was already used at the start.
Triples Generation. Like in the dictionary generation, we are reusing the
k-HDTCat method to compute the triples, we add to the triple reading and
mapping part a check reading the input delete bitmap to see if the read triple is
deleted or not. If it is deleted we ignore the triple, otherwise we continue the k-
HDTCat method. The k-HDTCat method already taking care of the sharedness
“loss” with the same strategy as the sharedness “gain”.
Complexity. The k-HDTDiﬀCat method being close to HDTCat [ 4], it is
reﬂected with a same time and space complexity. In HDTCat, for n, m the
number of triples in the two input HDT ﬁles, the time complexity is O((n +
m) log(n + m)) with at best O(n + m) and the space complexity is O(n + m).
Unlike HDTCat, we don’t have a constant amount of input HDT ﬁles. We denote
the complexities using n, the number of all triples in the input HDT ﬁles and
we add to the deﬁnition m, the number of all RDF terms in the input HDT ﬁle
dictionaries. We will ﬁrst explain the time complexity for the triples generation,
then the time complexity for the dictionary generation and the space complexity.

136 A. Willerval et al.
The input dictionaries being already sorted, computing the union of them is
done using a merge fashion and thus, giving a complexity of O(m).
The triples generation is done by grouping the triples with the same subject-
predicate couple and then sort these groups. The worst case scenario is only one
group giving a time complexity ofO(n log n). In the best scenario, where all the
groups are containing a constant amount of triples, the time complexity isO(n).
By combining both the dictionary and triples generation, the time complexity is
O(m + n log n).
The space complexity is given by the space required to store the new HDT
ﬁle sections, which is O(m) for the dictionary and O(n) for the triples. The
combined space complexity is O(m + n).
4.3 HDTq Integration
To integrate HDTq inside these two methods, we need to consider the new graph
section and the graph bitmaps inside the triples (or quads) section.
The graph section is compressed like all the other sections and isn’t merged
with a shared section, so we can apply our merge join with or without the
section delete bitmaps depending on if we are deleting triples or not using k-
HDTDiﬀCat.
For the quads, in k-HDTDiﬀCat, we are already sorting in memory the
objects ids by grouping them by (subject, predicate) because the memory impact
is low. But we can also notice that the memory impact for grouping the quads
ids by (subject, predicate) is also low so we can extend the triples generation of
k-HDTCat to sort the graphs with the objects.
The main issue comes with the deletion bitmap, HDTq ﬁles not being based
on a triple list, but on a quad list, we now consider our delete bitmap as a 2D
matrix (i, j ) instead of a 1D list (i), the i staying the triple id, but we add the
j to denote the graph id. To construct this matrix, like in HDTq [ 9], we used
Roaring bitmaps [15] to avoid having to have full matrix lines with only few bits
because named graphs are only containing few triples.
5 Experiments
To evaluate HDTDiﬀCat we run four diﬀerent experiments. Their codes are
available on Github
4.
1. This experiment aims to determine the best value of k when compressing a
dataset using k-HDTCat.
2. In this experiment we compare our compression methods with the existing
ones, i.e. rdf2hdt [11], HDT-MR [12] and HDTCat [4].
3. This experiment compares the compression process we propose with other
compression methods, using as an example the Wikidata dataset.
4. This experiment shows how it is possible to use k-HDTDiﬀCat to create an
up to date HDT ﬁle of Wikidata with a max delay of 24 h.
4 https://github.com/ate47/kHDTGenDiskBenchmark.

Generate and Update Large HDT RDF Graphs 137
5.1 Experiment: Experimentally Determine a Good Value of k
in k-HDTCat
This ﬁrst experiment was made using the LUBM benchmark [ 14]. LUBM is a
benchmark for SPARQL that allows to generate synthetically an RDF graph
with diﬀerent sizes. The size is generally indicated by the number of universities
contained in the graph. We use a small LUBM dataset of 1000 universities, giving
us a dataset with 133.5 million RDF triples. We then split this dataset into small
datasets of 1 million triples converted into HDT ﬁles, giving us n = 134 HDT
ﬁles. We then run k-HDTCat in a k-way merge fashion to create one HDT ﬁle
from all the 134 HDT ﬁles by using diﬀerent k. We run our experiments on
a KVM virtual machine with 16GB of RAM with 1TB of SSD with 4 vcpu
Intel(R) Xeon(R) CPU E5-2667 v4 3.20GHz in a University server. The results
are reported in the Table1.
Table 1. Time in function of the k and the number of layers
k layers cats time (s) average (s)
2 8 132 2264 2264
4 4 44 1245 1245
8 3 19 987 971
10 14 955
12 2 12 849 854
20 7 805
28 5 840
36 4 890
44 4 884
134 1 1 1135 1135
We used 4 diﬀerent metrics, the number of k-HDTCat (cats) used obtained
with ⌈ n−1
k−1 ⌉, the number of layers in the k-ways tree, obtained with⌈logk (n)⌉,t h e
time to create the HDT ﬁle for a given k value and the average time for a given
layer count. We notice that the time to merge the HDT ﬁles can be divided by 2
with a good k choice. We can also see that the time is linked with the number of
layers during the k-ways merge, a large number of layers is increasing the time,
the results for k =1 0a n dk = 12 is also showing that the number k-HDTCat
has less impact than the number of layers. We can also see that, after a certain
point the higher the number of HDT ﬁle is, the slower the method is, the HDT
ﬁles being mapped from disk, the higher the number is, the higher the number
of ﬁle pointer is, reducing the speed.
In our future experiments, we will set k = 20, this k being the one with the
best time.

138 A. Willerval et al.
5.2 Experiment: Comparison with Existing HDT Compression
Methods
To compare our approach with existing methods for compressing HDT ﬁle, we
follow the same procedure as in the HDTCat and HDT-MR papers. The idea
is to measure the time to compress diﬀerent sizes of the data generated in the
LUBM benchmark [ 14]. Following existing evaluations we try to generate an
HDT ﬁle for the LUBM dataset with a university count of 1000, 2000, 3000, ...,
8000 (i.e. with a step of 1000 universities), then from 8.000, 12.000, 16.000, ....,
40000 (i.e. with a step of 4.000 universities). This gives us diﬀerent datasets with
sizes from 130 million triples to 5.3 billion triples. For the other approaches we
do no replicate the results but report the results from the previous papers. We
run our experiments on the same machine as the one described in the previous
experiment in Sect.5.1. Each experiment was run 3 times and reported using the
average and standard deviation. The results are reported in Table2. We see that
despite using only a 16 GB RAM machine we are outperforming the original
HDTCat implementation running on both a machine with 16 GB and 128 GB
of RAM. The map reduce setup is still more competitive by 65% but uses a map
reduce cluster with 8 times more memory. Overall we can see that we are able
to compress big datasets on commodity hardware using only one machine.
Table 2. Comparison in seconds (s) between methods to serialize RDF graphs into
HDT using HDTCat [4], HDT-MR [12] and k-HDTCat


Generate and Update Large HDT RDF Graphs 139
5.3 Experiment: Indexing Wikidata
In this section, we want to show how we compare with respect to indexing
strategies of other SPARQL endpoints.
To do this, we want to see how our approach behaves on indexing the whole
Wikidata dump. This is seen as a challenging problem. As reported in [7] there
is only a limited number of successful attempts to index the whole of Wikidata
on existing triple stores since most do not scale to KGs of this size (even with
large hardware conﬁgurations). In the year 2020 the Wikidata dump surpassed
13B triples. Since then only 6 triple stores have been reported to be capable
of indexing the whole dump, namely: Virtuoso [ 6], Stardog
5, Apache Jena 6,
QLever [1] and Blazegraph. We report in Table3 the loading times, the number
of indexed triples, the amount of needed RAM, the ﬁnal index size and the
documentation for indexing Wikidata.
Table 3. Wikidata Index characteristics for diﬀerent endpoints.
System Loading Time #Triples RAM Index size Doc
Apache Jena 9d 21h 13.8 B 64 GB 2TB https://wiki.bitplan.com/index.php/
WikiData Import 2020-08-15 .
Virtuoso “several days” a
(preprocessing)
+1 0 h
11.9 B 378 GB NA https://community.openlinksw.com/t/
loading-wikidata-into-virtuoso-open-
source-or-enterprise-edition/2717 .
Blazegraph ∼5.5d 11.9 B 128 GB 1.1 T https://addshore.com/2019/10/your-own-
wikidata-query-service-with-no-limits/ .
Stardog 9.5 h 16.7 B 256 GB NA https://www.stardog.com/labs/blog/
wikidata-in-stardog/ .
QLever 14.3 h 17 B 128 GB 823 GB https://github.com/ad-freiburg/qlever/
wiki/Using-QLever-for-Wikidata .
qEndpoint 57 h 19.2 B 16 GB 340 GB https://github.com/the-qa-company/
qEndpoint/wiki/Use-qEndpoint-to-index-
a-dataset.
a The precise number of days for the preprocessing is not indicated in the documentation.
Using k-HDTCat we were able to index the Wikidata public dump from
February 2024 with 19.2 billion triples 7. The experiment was run on a 16 GB
desktop computer with a 12 cores AMD Ryzen 5 5600 3.50 GHz CPU and
1 TB of SSD. The experiment was repeated two times, the average time and
standard deviation are used as a metric. The compression time was 52 h. The
compression time is the third best between the reported once. On the other
hand, this compression was achieved on a commodity hardware with 16 GB of
RAM which is from 8 to 23 smaller than other approaches. The ﬁnal index size
of 340 GB is the smallest between the reported ones.
We measured the total time for the diﬀerent generation steps. The k-HDTCat
generation steps are dict for merging and writing the dictionaries, triples for
5 https://www.stardog.com/.
6 https://jena.apache.org.
7 https://dumps.wikimedia.org/wikidatawiki/entities/.

140 A. Willerval et al.
merging and writing the triples andsave to write the end HDT ﬁle. This results
are reported in Table4.
Table 4. Time split per part during WD compression
Method Section Time (s) Time SD Percent. Total (s) Total SD Percent.
HDT ﬁle Generation – 104449 1124 59,68 %
k-HDTCat dict 18964 478 26.87 % 70582 1498 40,32 %
triples 42767 1092 60.6 %
save 8837 73 12.52 %
Total – 175032 378 100 %
SD = Standard deviation
We can see that most of the time is used to compress the small HDT ﬁles.
5.4 Experiment: k-HDTDiﬀCat to Keep Up to Date Datasets
Table 5. Times per part to compute HDTDiﬀ over a Wikidata Truthy HDT ﬁle with
371M changed triples.
Step Diﬀ only time (s) Cat only time (s) DiﬀCat time (s)
Diﬀ bitmap 501 – 462
Dictionary 2121 2155 2206
Triples 4446 3401 4352
Total 7068 5556 7020
A way to keep RDF graphs up to date, is by using buﬀer updates, i.e. adding
and deleting the changes over time in a buﬀer and by applying all of them at the
same time. In this experiment we are using the Wikidata recent changes API 8
to fetch the recent changes from the Wikidata dataset [ 20] and combine them
with an HDT dump of the Wikidata dataset.
For our experiment, we are using a Wikidata truthy dump from 2023-10-28
00:40 (CET) and the recent changes changes from the dump date to the 2023-
11-06 14:00. This accounts for 2, 509, 863 Wikidata entity changes. We create a
bitmap for the HDT triples, when an entity e is changed, we mark as removed
by a 1 in the bitmap all the triples matching the pattern ( e, ?, ?). We put in a
new HDT ﬁle the triples with e as a subject by getting them from Wikidata.
This gives us 371 .278.906 added triples inside what we call the “Delta” HDT
ﬁle.
8 https://www.mediawiki.org/wiki/API:RecentChanges.

Generate and Update Large HDT RDF Graphs 141
Table 6. Times (s) per part to compute k-HDTDiﬀCat over a Wikidata Truthy HDT
ﬁle with 371M changed triples using diﬀerent counts. The added time is compared with
the time to compute a k-HDTDiﬀCat with 2 HDT ﬁles.
Step 1 2 3 4 5 6 7
Diﬀ bitmap 581 553 530 525 550 552 548
Dictionary 2873 3006 3219 3371 3615 3739 3959
Triples 6157 6416 6863 7149 7661 8083 8161
Total 9611 9975 10612 11045 11826 12374 12668
Added time – +4% +10% +14% +23% +28% +32%
Using these datasets, we did four experiments to test the eﬃciency of k-
HDTDiﬀCat, they were done on a 16GB laptop with 200GB of SSD available.
The ﬁrst one was to only apply the HDTDiﬀ part on the Truthy Wikidata
HDT ﬁle with the delete bitmap. This allows to see the speed of only the diﬀ part.
A second test is made by running the HDTCat part on the HDTDiﬀ result with
the delta graph. Giving a time on how fast the HDTCat part is working, it is not
made on the ﬁrst Truthy Wikidata HDT ﬁle to avoid duplicated terms. The third
is to run both algorithms to compare how fast is the couple k-HDTDiﬀCat vs
HDTCat + HDTDiﬀ. The results of these experiments are available in Table5.
In the table, the time to compute each HDT section is mentioned with the total
time to run the method, the diﬀ bitmap building is omited in the cat because
we aren’t running a diﬀ method.
The results of these three experiments are available in Table 5.W ec a ns e e
that HDTDiﬀ is adding an overhead to HDTCat, we believe that it is due to
the bitmap reading to test if an term is in the result HDT ﬁle. Another result is
the time diﬀerence between HDTDiﬀ only + HDTCat only and k-HDTDiﬀCat,
showing that it is pertinent to use k-HDTDiﬀCat instead of HDTDiﬀ and then
HDTCat when building a new HDT ﬁle.
A fourth experiment is done to understand how the increasing count of HDT
ﬁles is aﬀecting our method. To do that, we ﬁrst split our delta HDT ﬁle into 7
pieces and we run the k-HDTDiﬀCat on the truthy HDT ﬁle and i pieces, with
i = {1,... 7}. The results of this experiment are available in Table 6. The diﬀ
being only done on the input HDT ﬁle, the time to compute the diﬀ bitmap is the
same for all the steps. We then notice an increase in time for each added HDT
ﬁle between 4 and 9 percents added to the time to compute two k-HDTDiﬀCat.
6C o d e
k-HDTDiﬀCat and its HDTq support are part of the qEndpoint core repository9.
Af o r ko ft h eJ a v aH D Tl i b r a r y10. It is used in qEndpoint, a SPARQL endpoint
9 https://github.com/the-qa-company/qEndpoint/tree/master/qendpoint-core.
10 https://github.com/rdfhdt/hdt-java.

142 A. Willerval et al.
based on HDT and RDF4J. The code is released under theLesser General Pub-
lic License . The tool is available as a command line interface 11 together with
existing tools like rdf2hdt, hdt2rdf, hdtInfo, hdtVerify. The new tool can be used
as:
hdtDiffCat <input files> -diff <delta file> <output HDT file>
The input ﬁles are the HDT ﬁles to combine, an additional HDT ﬁle can be
added to tell which triples to delete.
It can also be used as a lightweight library without the endpoint for more
speciﬁc operations.
7 Conclusion
HDT is an RDF ﬁle format that allows to store, share and query large RDF
Knowledge Graphs on commodity hardware. In this paper, we presented a new
tool, k-HDTDiﬀCat, a generalization of HDTCat to combine multiple HDT ﬁles
and to remove some of the existing triples.
It is available online as a command line interface or by using our Java library
in the qEndpoint repository
12 under the Lesser General Public License .W eh a v e
shown how this tool can be used to compress HDT ﬁle and how it compares
with respect to existing methods. We have also compared the HDT compression
with the indexing strategies of other performant SPARQL endpoints. Finally, we
have seen how they can be used to maintain an up-to-date Wikidata index. To
conclude, k-HDTDiﬀCat allows generating and update HDT ﬁles on commodity
hardware, something that was not possible before. This is particularly important
since now all operations in the HDT life-cycle can be carried out on commod-
ity hardware. As a consequence HDT becomes an ideal indexing structure for
large KGs in low hardware settings allowing the community to manipulate these
graphs more easily.
References
1. Bast, H., Buchhold, B.: QLever: a query engine for eﬃcient SPARQL+ text search.
In: Proceedings of the 2017 ACM on Conference on Information and Knowledge
Management, pp. 647–656 (2017)
2. Beek, W., Rietveld, L., Bazoobandi, H.R., Wielemaker, J., Schlobach, S.: LOD
laundromat: a uniform way of publishing other people’s dirty data. In: Mika, P.,
et al. (eds.) ISWC 2014. LNCS, vol. 8796, pp. 213–228. Springer, Cham (2014).
https://doi.org/10.1007/978-3-319-11964-9
14
3. Diefenbach, D., Both, A., Singh, K., Maret, P.: Towards a question answering
system over the semantic web. Semant. Web11(3), 421–439 (2020)
11 https://github.com/the-qa-company/qEndpoint/wiki/qEndpoint-CLI-commands.
12 https://github.com/the-qa-company/qEndpoint/tree/master/qendpoint-core.

Generate and Update Large HDT RDF Graphs 143
4. Diefenbach, D., Gim´enez-Garc´ıa, J.M.: HDTCat: let’s make HDT generation scale.
In: Pan, J.Z., et al. (eds.) ISWC 2020. LNCS, vol. 12507, pp. 18–33. Springer, Cham
(2020). https://doi.org/10.1007/978-3-030-62466-8 2
5. Diefenbach, D., Singh, K., Maret, P.: WDAqua-core1: a question answering service
for rdf knowledge bases. In: Companion Proceedings of the The Web Conference
2018, WWW 2018, pp. 1087–1091. International World Wide Web Conferences
Steering Committee, Republic and Canton of Geneva, CHE (2018)https://doi.org/
10.1145/3184558.3191541
6. Erling, O., Mikhailov, I.: RDF support in the virtuoso DBMS. In: Pellegrini, T.,
Auer, S., Tochtermann, K., Schaﬀert, S. (eds.) Networked Knowledge - Networked
Media. Studies in Computational Intelligence, vol. 221, pp. 7–24. Springer, Berlin,
Heidelberg (2009). https://doi.org/10.1007/978-3-642-02184-8
2
7. Fahl, W., Holzheim, T., Westerinen, A., Lange, C., Decker, S.: Getting and hosting
your own copy of Wikidata. In: 3rd Wikidata Workshop @ International Semantic
Web Conference (2022). https://zenodo.org/record/7185889#.Y0WD1y0RoQ0
8. Fern´andez, J.D., Beek, W., Mart´ ınez-Prieto, M.A., Arias, M.: LOD-a-lot: a
queryable dump of the LOD cloud. In: d’Amato, C., et al. (eds.) ISWC 2017,
Part II. LNCS, vol. 10588, pp. 75–83. Springer, Cham (2017). https://doi.org/10.
1007/978-3-319-68204-4 7
9. Fern´andez, J.D., Mart´ınez-Prieto, M.A., Polleres, A., Reindorf, J.: HDTQ: manag-
ing RDF datasets in compressed space. In: Gangemi, A., et al. (eds.) ESWC 2018.
LNCS, vol. 10843, pp. 191–208. Springer, Cham (2018). https://doi.org/10.1007/
978-3-319-93417-4 13
10. Fern´andez, J.D., Mart´ınez-Prieto, M.A., Guti´errez, C., Polleres, A., Arias, M.:
Binary RDF representation for publication and exchange (HDT). J. Web Semant.
19, 22–41 (2013). https://doi.org/10.1016/j.websem.2013.01.002, https://www.
sciencedirect.com/science/article/pii/S1570826813000036
11. Fern´andez Garc´ıa, J.D., et al.: Binary RDF for scalable publishing, exchanging and
consumption in the web of data (2013)
12. Gim´enez-Garc´ıa, J.M., Fern´andez, J.D., Mart´ınez-Prieto, M.A.: HDT-MR: a scal-
able solution for RDF compression with HDT and MapReduce. In: Gandon, F.,
Sabou, M., Sack, H., d’Amato, C., Cudr´e-Mauroux, P., Zimmermann, A. (eds.)
ESWC 2015. LNCS, vol. 9088, pp. 253–268. Springer, Cham (2015). https://doi.
org/10.1007/978-3-319-18818-8
16
13. Gog, S., Beller, T., Moﬀat, A., Petri, M.: From theory to practice: plug and play
with succinct data structures. In: Gudmundsson, J., Katajainen, J. (eds.) SEA
2014. LNCS, vol. 8504, pp. 326–337. Springer, Cham (2014). https://doi.org/10.
1007/978-3-319-07959-2 28
14. Guo, Y., Pan, Z., Heﬂin, J.: LUBM: a benchmark for owl knowledge base systems.
J. Web Semant. 3(2–3), 158–182 (2005)
15. Lemire, D., et al.: Roaring bitmaps: implementation of an optimized software
library. Softw.: Pract. Exp. 48(4), 867–895 (2018)
16. Mart´ınez-Prieto, M.A., Fern´andez, J.D., C´anovas, R.: Compression of rdf dictionar-
ies. In: Proceedings of the 27th Annual ACM Symposium on Applied Computing,
SAC 2012, pp. 340–347. Association for Computing Machinery, New York (2012).
https://doi.org/10.1145/2245276.2245343
17. Taelman, R., Mahieu, T., Vanbrabant, M., Verborgh, R.: Optimizing storage of
RDF archives using bidirectional delta chains. Semant. Web13(4), 705–734 (2022)
18. Verborgh, R., et al.: Triple pattern fragments: a low-cost knowledge graph interface
for the web. J. Web Semant. 37–38, 184–206 (2016). https://doi.org/10.1016/j.
websem.2016.03.003, http://linkeddatafragments.org/publications/jws2016.pdf

144 A. Willerval et al.
19. Willerval, A., Bonifati, A., Diefenbach, D.: qEndpoint: a Wikidata SPARQL end-
point on commodity hardware. In: Companion Proceedings of the ACM Web Con-
ference 2023, pp. 119–122 (2023)
20. Willerval, A., Diefenbach, D., Maret, P.: Easily setting up a local Wikidata
SPARQL endpoint using the qEndpoint (2022)
21. Witten, I.H., et al.: Managing Gigabytes: Compressing and Indexing Documents
and Images. Morgan Kaufmann (1999)

SMW Cloud: A Corpus of
Domain-Speciﬁc Knowledge Graphs from
Semantic MediaWikis
Daniil Dobriy1(B) , Martin Beno1 , and Axel Polleres1,2
1 Vienna University of Economics and Business, Vienna, Austria
{daniil.dobriy,martin.beno,axel.polleres}@wu.ac.at
2 Complexity Science Hub, Vienna, Austria
Abstract. Semantic wikis have become an increasingly popular means
of collaboratively managing Knowledge Graphs. They are powered by
platforms such as Semantic MediaWiki and Wikibase, both of which
enable MediaWiki to store and publish structured data. While there are
many semantic wikis currently in use, there has been little eﬀort to col-
lect and analyse their structured data, nor to make it available for the
research community. This paper seeks to address this gap by systemat-
ically collecting structured data from an extensive corpus of Semantic-
MediaWiki-powered portals and providing an in-depth analysis of the
ontological diversity (and re-use) amongst these wikis using a variety of
ontological metrics. Our paper aims to demonstrate that semantic wikis
are a valuable and extensive part of Linked Open Data (LOD), and
in fact may be considered an own active “sub-cloud” within the LOD
ecosystem, which can provide useful insights into the evolution of small
and medium-sized domain-speciﬁc Knowledge Graphs.
Keywords: Semantic MediaWiki
· Linked Open Data · Ontology ·
Ontology Metrics · Ontology Links
Resource accessibility
The resource is made openly available with the necessary access information
provided below. Section 5.3 provides a sustainability plan, and details further
implemented access modalities for the resource.
Resource Type: Dataset
DOI: 10.5281/zenodo.7920174
License: Creative Commons Attribution 4.0 International1
URL: https://semantic-data.cluster.ai.wu.ac.at/smwcloud/
1 For more information on the Creative Commons Attribution 4.0 International
License, visit https://creativecommons.org/licenses/by/4.0/.
c⃝ The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
A. Mero˜no Pe˜nuela et al. (Eds.): ESWC 2024, LNCS 14665, pp. 145–161, 2024.
https://doi.org/10.1007/978-3-031-60635-9_9

146 D. Dobriy et al.
1 Introduction
With the advent of Large Language Models (LLMs), unconventional approaches
for extracting rich Linked Data from collaborative platforms and knowledge hubs
are gaining attention among researchers, including in the Semantic Web commu-
nity [5]. First introduced in 2005, Semantic MediaWiki2 (SMW) is an extension
for the MediaWiki platform that enables semantic annotations of wiki pages [19],
making it a collaborative Knowledge Graph management platform. It is also a
precursor that majorly inspired Wikidata, and therefore Wikibase (WB), which
uses select code from SMW for common tasks [28]. Yet, SMW has been available
for a longer time and is indeed more broadly used than WB by various projects
to manage their structured data. Indeed, following the approach described in
Sect.2, we could discover 1458 active Semantic MediaWiki instances, compared
to a lower number of 327 Wikibase instances. The two platforms diﬀer inso-
far that SMW stores its data as part of its textual page content and has a
less complicated data model [28]: SMW’s simple subject-predicate-object state-
ment structure known as asemantic facts corresponds straightforwardly to RDF
triples, where subjects are commonly single wiki pages, properties (predicates)
are deﬁned by special syntax in pages or via templates and forms enabled through
additional extensions, and objects can be of diﬀerent datatypes
3 (e.g. numbers,
dates, pages etc.). Therefore, SMW serves as a ﬂexible tool to collaboratively
create and maintain domain-speciﬁc KGs, along with their own vocabularies.
RDF/SPARQL Access. The SMW platform allows to generate full RDF dumps4
of its structured data. Additionally, although semantic facts are stored in a rela-
tional database by default, RDF triples can also be optionally exported/synced
with a triplestore or a SPARQL endpoint via a special extension.5 However, in
practice, SMW instances rarely publish periodical dumps of their data, nor do
they typically make their data available via SPARQL endpoints. 6 This signiﬁ-
cantly decreases the eﬀective semantic interoperability and accessibility of KGs
provided and maintained through SMW. So far, to the best of our knowledge –
an in-depth analysis of the RDF data made available through SMW instances on
the Web is missing .
Linkage and Ontology Re-use. The re-use of external URLs is in principle pos-
sible in semantic facts in SMW, as well as the import of external RDF vocabu-
laries
7 and ontologies8; yet, semantic linkage to other KGs is not directly incen-
2 https://www.semantic-mediawiki.org/.
3 https://www.semantic-mediawiki.org/wiki/Help:Datamodel.
4 https://www.semantic-mediawiki.org/wiki/Help:Maintenance script dumpRDF.php.
5 In principle, this integration also supports adding additional RDF with SPARQL
Updates, cf. https://www.semantic-mediawiki.org/wiki/Help:Using SPARQL and RDF stores,
but herein we focus solely on the RDF data exportable from SMW pages directly.
6 We note that also there is no “best practice” to detect whether an SMW instance
hosts a SPARQL endpoint, as it is not exposed by the SMW API.
7 https://www.semantic-mediawiki.org/wiki/Help:Import vocabulary.
8 https://github.com/TIBHannover/ontology2smw.

SMW Cloud: A Corpus of Domain-Speciﬁc Knowledge Graphs 147
tivised within SMW, or respectively, it is an open question in how far these
features are being used , i.e., in how far the KGs provided by SMW instances
(a) re-use existing ontologies and (b) create links to related RDF from other
authorities.
A commonly cited shortcoming of the Linked Open Data (LOD) infrastruc-
ture is the lack of a single aggregation point [ 8,13]. To this end, our approach,
SMW Cloud, aims at solving this data accessibility issue by aggregating all pub-
licly available SMWs into a single corpus, addressing the above-mentioned gaps
by making the following concrete contributions:
– we systematically track (for now) 1458 Semantic MediaWiki instances, extract
their page RDF data when technically feasible, and aggregate it to a Linked
Data corpus, following a similar approach as the CommonCrawl
9 and Web-
DataCommons [21] projects,
– we make this corpus available as an HDT [12] dump, in an accessible, scalable
and available, easy to (re-)use and cost-eﬀective manner, following the LOD-
a-LOT approach [13] and make calculated metrics for the corpus available in
a SPARQL endpoint.
– we provide an extensive analysis of our corpus in terms of (a) ontology metrics,
following the Neontometrics approach [24] and (b) LOD metrics, following the
LODStats approach [7,8].
As such, we strive to obtain a comprehensive picture of the current state
of Linked Data stored in SMWs, evaluating the quality and internal structure,
thereby tracking the evolution of a signiﬁcant, previously unexplored part of
the LOD ecosystem. Note that we may hypothesise that the domain-speciﬁc,
small and medium-sized KGs, represented by SMW instances, closely reﬂect
Enterprise Knowledge Graphs (EKGs), for which there is no publicly available
corpus. Analysing our corpus, in comparison with the “classic” KGs making up
the LOD Cloud
10, but also in comparison with Wikidata, will therefore gain
insights into the possible diﬀerent parameters to be found in EKGs.
The remainder of this paper is structured as follows: In Sect. 2, we describe
the architecture and our approach to collecting the SMW corpus. Section3 intro-
duces the methods used for further corpus analysis. Corpus statistics and results
of our analyses, including a comparison with similar metrics applied to the “tra-
ditional” LOD Cloud and Wikidata, are summarized in Sect. 4, before we close
with a discussion and outlook to future work in Sect.5.
2 Methods for Collecting the Corpus
Our overall corpus collection approach is illustrated in Fig. 2.I nﬁ r s ts t e p ,w e
discover Semantic MediaWiki instances in a three-fold manner:
9 https://commoncrawl.org.
10 http://lod-cloud.net.

148 D. Dobriy et al.
– We ﬁlter the BuiltWith MediaWiki collection11 for SMW instances.
– We query WikiApiary12 – a“meta-wiki” collecting information about public
MediaWiki instances – for instances that have the SMW extension installed.
– Lastly, we follow the approach utilized by the web platform discovery tool
Crawley13 and use Search Engine APIs (such as the BingAPI, but also by
manual usage of other Search Engines) to discover SMW instances by speciﬁc
text excerpts or HTML elements commonly found on SMW-powered websites:
e.g., “powered by SMW” text snippets).
Following this approach, we collect an extensive list of 1458 SMW instances, for
details on the numbers of instances per source, we refer to Fig.1.
For each found SMW instance, we further retrieve basic statistics directly
available via SMW, such as numbers of pages, numbers of users, creation and
last modiﬁed dates, in order to assess how long the wikis have been operational
and how active they are, and the pagelist. Next, we attempt to crawl RDF by
querying the pagelist, using the MediaWiki API.
14 Frequent problems encoun-
tered in the process of collecting the corpus, such as non-standard behaviours
of MediaWiki and SMW platforms, access restrictions, as well as a number of
parsing errors, limit technical feasibility of collecting RDF from each instance.
Table1 gives an overview of such issues. Apart from the RDF representation
we also crawl the versioning history to identify all changes per page for future
analysis.
15 In the last step, we aggregate16 the RDF by wiki instance to create
our corpus. Apart from creating a single HDT ﬁle per crawled instance con-
taining all RDF triples, we add metadata per wiki KGs using the VoID [2]a n d
DataCube [10] vocabularies to include more complex statistics and metrics dis-
cussed in detail in Sect. 3 below, in the HDT headers.
As an additional item in this metadata aggregation, we collect and classify
wikis per “topics”, similar to the LOD Cloud topics17. Our approach to classify
wikis into “LOD Cloud topics” works by, whenever available, fetching metain-
formation collected by WikiApiary (manually assigned topics) and BuiltWith
(SEO-related keywords), plus the textual information from the respective wiki’s
main page, a random sample of up to 100 page titles and the name of the wiki.
We then feed GPT-4 with this textual information
18 to assign it one of the LOD
Cloud topics – this current naive approach serves mainly for illustration, cf.
Figure4 below.
11 https://trends.builtwith.com/websitelist/MediaWiki.
12 https://wikiapiary.com.
13 http://purl.org/crawley.
14 https://www.mediawiki.org/wiki/API:Query.
15 Cf. Sect. 5, we plan to also extract and analyse the evolution of the RDF KGs per
SMW instances as future work.
16 Given the absence of Blank Nodes within instances, skolemization is unnecessary.
17 https://lod-cloud.net/.
18 Roughly, our GPT prompt is:“Given the text “[WIKINAME+MAINPAGETEXT+
PAGETITLES+METAINFO]”, tell me the best ﬁtting topic among [LODCLOUD-
Topiclist]”.

SMW Cloud: A Corpus of Domain-Speciﬁc Knowledge Graphs 149
Fig. 1. Venn Diagram of Collected SMWs
(1458 in Total) and Their Sources
Table 1. Breakdown of Collection and
Processing Losses
SMWs Description
1458 all active SMW instances
-108 malformed API response
-107 API endpoint unavailable
-55 server-terminated connection
-31 non-standard encoding scheme
1157 instances for which the full pagelist and
page RDF could be collected
-51 XML wrongly declared
-36 malformed XML/mismatched tags
-5 non-compliant IRIs
-36 other processing errors
1029 SMW instances for which HDTs could
be aggregated
Fig. 2. Architecture of the SMW Crawler and Metrics Processor
2.1 Corpus Provision
Our SMW corpus is registered on Zenodo 19 and is available under a perma-
nent URL20 and directly on the open data repository of the institute21 we pro-
vide both separate RDF HDT [ 12] dumps per SMW instance, as well as in a
single HDT ﬁle for the whole corpus. A SPARQL endpoint, serving the VoID
& DataCube metadata in a queryable form, is available at: https://smwcloud-
sparql.cluster.ai.wu.ac.at/. The resource including all calculated metrics are pro-
vided under the Creative Commons Attribution 4.0 International License.22.T h e
canonical citation for the SMW Cloud is:
Dobriy, D., Beno, M., & Polleres, A. (2023). SMW Cloud: A Corpus of
Domain-Speciﬁc Knowledge Graphs from Semantic MediaWikis. Retrieved from
http://purl.org/SMWCloud.
19 10.5281/zenodo.7920175.
20 http://purl.org/SMWCloud.
21 https://semantic-data.cluster.ai.wu.ac.at/smwcloud/.
22 https://creativecommons.org/licenses/by/4.0/.

150 D. Dobriy et al.
Comprehensive documentation for the resource is available at: https://github.
com/semantisch/smwcloud. For illustration, we provide the VoID metadata and
selected DataCube entries available through our endpoint (and as part of the
respective HDT header) for “Wien Geschichte Wiki”, an SMW instance provid-
ing historical information about Vienna [18] in Turtle syntax in Fig.3.
Fig. 3. Metadata for “Wien Geschichte Wiki”
3 Methods for Analysing the Corpus
Due to their topical diversity, data and schemas diﬀer considerably among SMW
instances, but also we hypothesize that the RDF data from SMW instances has
fundamentally diﬀerent characteristics than other Linked Data corpora, such as
the LOD Cloud datasets, or Wikidata. In order to verify these assumptions, a
comprehensive characterization of our corpus requires two things: (1) a funda-
mental understanding of each dataset, and (2) an overview of all available data

SMW Cloud: A Corpus of Domain-Speciﬁc Knowledge Graphs 151
Table 2. Related Work and Implemented Metrics
[3]. Therefore, we perform our analyses both on the single wiki datasets as well
as on the corpus as a whole in terms of commonly used metrics.
In order to establish a foundation for comparative analysis, we review related
LOD analysis studies in Table 2. This allows us to discern and categorize the
prevailing analytical themes. The most common analyses within these studies
are performed on Basic graph metrics , Basic ontology metrics ,a n dQuality.I n
addition to the aforementioned themes, other forthcoming analyses encompass
Vocabulary re-use, Dataset interlinkage and Language usage .
General graph metrics give a comprehensive and comparable characteriza-
tion of the corpus [7]. Additionally, we calculatebasic ontology metrics to assess
the used schemata/ontologies of the individual SMW instances in a compara-
ble manner, and evaluate the corpus on the basis of established quality analysis
frameworks to gain a better understanding of quality characteristics. Explic-
itly including ontology metrics and common ontology quality frameworks in our
analyses through the implementation of the Neontometrics calculation engine
[24], we address the lack of metric validation for real-world data [24], especially
in small KGs : we perceive SMW instances as a publicly available pendant/proxy
for enterprise KGs with their own characteristics.
Table2 brieﬂy summarizes the various metrics and quality frameworks we
have calculated for the SMW corpus: as for calculating the basic graph and ontol-
ogy metrics, we use the Neontometrics OPI (Ontology Programming Interface).

152 D. Dobriy et al.
Afterwards, we apply these metrics to calculate common quality frameworks:
Cohesion Metrics [31], Complexity Metrics [30], Fernandez et al. [14], OQuaRE
[6,25], Gangemi et al. [15], OntoQA [27] and Orme et al. [23]. Please refer Table2
for a summary of their respective dimensions.
4 Results and Corpus Statistics
In this section, we provide a brief overview of the insights into the corpus based
on the collected statistics. We excluded the datasets causing processing errors
as described in Table 1, resulting in 1029 datasets which collectively form the
corpus and the basis for analyses.
4.1 Basic RDF Metrics
Table3 gives a distilled overview of of the corpus dimensions. Notably, the abso-
lute numbers we report for SMW Cloud fall short of the statistics for the num-
ber of statement reported by the instances themselves: totalling 1,012,521,773
statements and 206,997 unique properties, calculated by aggregating statistics
reported by individual SMWs. At the same time, the SMW Cloud dimensions are
comparable to that of LODStats [ 8], which totals 192,230,648 triples. Though
Wikidata has grown considerable in the last 5 years, from 3b triples in 2018
to more than 17b in 2022, exceeding SMW Cloud in size considerably [ 11].
Nevertheless, despite its comparatively smaller size in terms of total number
of statements, the SMW Cloud exhibits a signiﬁcantly broader range of unique
properties, exceeding both Wikidata and LODStats, as well as suggesting limited
vocabulary re-use in SMW Cloud.
For a better overview of the characteristics of individual datasets compris-
ing the corpus, we refer to Table 4. There, we compare their parameters to the
individual LOD Cloud datasets [ 8]. Though LOD Cloud datasets are signiﬁ-
cantly larger on average (2,180,651 triples to 186,813 for SMWs), the majority
of LOD datasets are smaller (median 2,486 vs 12,596 for SMWs) implying more
uniform sizes of the SMWs. Another key characteristic of SMWs is the higher
number of properties and classes per datasets as well as the higher number of
properties per entity, suggesting a more granular and detailed data modeling
approach in SMWs and a user-centric, bottom-up nature of ontology creation.
The lack of class and property depth suggests a ﬂat ontology structure in the
SMW instances. We attribute this to the a) user communities with rich domain
knowledge and limited expertise in ontology management, b) ad-hoc nature of
ontology creation and c) decentralized ontology development in SMWs. Other
characteristics regarding high numbers of labeled subjects and large median
typed and untyped string lengths for Literals further diﬀerentiate user-centric
SMWs from LOD datasets.

SMW Cloud: A Corpus of Domain-Speciﬁc Knowledge Graphs 153
Table 3. SMW Cloud summary statistics
Dataset #Triples #Subjects #Predicates #Objects #Literals
LODStats [ 8] 192,230,648 Not reported 49,916 Not reported 90,261,655
SMW Cloud 236,505,705 24,010,566 52,670 66,052,823 160,108,216
Wikidata 2021 a 17,662,800,665 1,625,057,179 38,867 Not reported Not reported
LOD-a-lot [ 13] 28,362,198,927 3,214,347,198 1,168,932 3,178,409,386 1,302,285,394
a http://gaia.infor.uva.es/hdt/wikidata/wikidata20210305.hdt.gz
Table 4. SMW Cloud and LOD Cloud comparison
SMW Cloud LOD Cloud [ 8]
Metric Mean Min Max Median Mean Min Max Median
Triples p. dataset 186,813 0 31,582,870 12,595.6 2,180,651 2 247,620,294 2,486
Entities 14,828 0 5,036,913 1,281.0 390,325.95 0 63,494,920 106.5
Literals 54,076 0 18,514,040 3,304.0 790,000.57 0 88,315,872 127.0
Blanks 484,540.68 0 202,745,495 0.0
Blanks (subjects) 0.04 0 14 0 399,680.75 0 166,901,812 0.0
Blanks (objects) 0.02 0 6 0 143,005.6 0 50,803,539 0.0
Subclasses 0.14 0 46 0 14.07 0 2,000 0.0
Typed subjects 13,068.83 0 44,374.58 1,047.0 109,790.35 0 25,848,850 22.0
Labeled subjects 2,241.23 0 760,619 267.0 28,652.13 0 11,588,129 0.0
Properties p. entity 6.22 0.88 12.32 4.10 2.86 0 27.27 2.54
String length (typed) 9.32 0 476.05 9.51 9.5 0 1,854.0 0.0
String length (untyped) 72.43 0 369.77 73.12 38.24 0 2,688.0 20.0
Class hierarchy depth 0.009 0 2 0.0 1.63 0 6 0.0
Property hierarchy depth 0 0 0 0.0 1.04 0 5 0.0
Classes 356.52 0 113,270 27.0 20.09 1 1,328 5.0
Properties 155.01 0 45,209 38.0 30.36 1 885 20.0
4.2 Topical Analysis
Semantic MediaWikis capture a variety of highly-specialized domain knowledge,
as visualized in Fig. 4 reusing the LOD Cloud categories: 23 16% wikis special-
ize on publishing/annotating media, 10% are life science wikis, 6% geography-
oriented, 5% government-related, 4.3% language-related. Still, about half of all
wikis (48%) could not be classiﬁed under one of the categories (i.e. summarized
under user generated other ), hinting at the topic diversity and high degree of
specialization of SMWs.
Manual coding of a randomly selected sample of 100 wikis (as partially rep-
resented in Table 5) has shown that the chosen topics represent the wiki well,
overlap and are similar in meaning (87% similarity) with WikiApiary tags and
BuildWith verticals. Therefore, as a result, we characterize each wiki by 3 inde-
pendently created tag/domain collections which promotes discoverability and an
automatically generated description.
We further analyse the distribution of specialized domains in the corpus with
freely annotated tags, see Fig.5. The big components of the hitherto unclassiﬁed
wikis are therefore: gaming with 134 instances in total, technology (115), educa-
tion and community. The 101 unclassiﬁed wikis indeed can hardly be classiﬁed
23 https://lod-cloud.net.

154 D. Dobriy et al.
Fig. 4. Connected SMW Cloud instances with and without semantic-mediawiki.org
Table 5. Examples of SMW domain annotations
SMW LOD Cloud
classiﬁcationa
Free
classiﬁcation
Description Topic
(WikiApiary)
Topic
(BuiltWith)
geschichtewiki
.wien.gv.at
history
(government,
geography)
Vienna,
Austria
The Wien Geschichte Wiki is an
encyclopedia of historical,
geographic, and cultural information
related to the city of Vienna and its
surrounding regions.
city wiki,
history,
vienna
Art And
Entertain-
ment
bacid.eu government public
administra-
tion
BACID Wiki contains information
about decentralized governance,
capacity building, and public
administration initiatives in the
Danube region.
– Business
And
Industrial
korrekt.org publications
(media,
user
generated)
knowledge-
based
systems
Korrekt.org is a wiki focused on the
research and publications of
Professor Markus Kr¨otzsch, covering
topics such as description logic,
semantic wikis, and knowledge-based
systems.
homepage,
semantic
mediawiki
Science
www.
gardenology.
org
life sciences plants,
gardening,
encyclopedia
A comprehensive wiki encyclopedia
covering plants and gardening,
featuring detailed entries and
photographs.
– –
a Classiﬁcations enclosed within parentheses are also produced by the model, serving
as alternatives.
because of the lack of investigated content (see Sect.2). While we see that com-
mon LOD Cloud topics are well suited for classifying about half of SMW Cloud,
other signiﬁcant topics emerge: SMW Cloud has a rich number of technology,
education and community wikis not prominently featured in LOD Cloud.
4.3 Ontological Analysis
A number of metrics has been been proposed for the analysis of KGs and ontolo-
gies. Since a KG comprises both A-Box as well as T-Box statements, we consider

SMW Cloud: A Corpus of Domain-Speciﬁc Knowledge Graphs 155
Fig. 5. Prevalent Topics Across SMW Cloud Instances
both metrics for characterizing KGs and ontologies as suitable for analysing KG
with notable limitations applying to ontology metrics discussed separately.
Reiz et al. [24] proposes an ontology describing common metrics used to char-
acterize Knowledge Graphs and also introduces an open source tool automating
the calculation of a broad variety of metric and quality analyses calculations24.
The website of the tool also includes a Metric Explorer with metric overviews
and descriptions. For SMW Cloud, Table6 summarizes the basic ontology met-
rics for SMWs. We have also calculated all quality analyses based on these basic
ontology metrics suggested by the Neontometrics engine (see Table8).
Ontologically, SMW do contain a large number of class and property
assertion axioms, same individual assertions as well as individual, class and
property annotations. Notably, although SMW technically allows the use of
RDFS and OWL concepts, only a total of 5 SMWs
25 implement class hier-
archies (via rdfs:subClassOf ) and no SMW instance implements property
hierarchies (via rdfs:subPropertyOf) in practice, while 5 SMW instances use
owl:equivalentProperty deﬁnitions, some of which seem redundant. 26 A closer
analysis of the RDF(S) and OWL vocabulary used in 1029 crawled SMW
instances in terms of Description Logics expressivity (testable again through the
Neontometrics tool) is illustrated in Table 7: here, the concrete RDF(S)+OWL
24 http://neontometrics.com/.
25 Speciﬁcally: wiki.spell-plattform.de, wiki.fablab.is, wiki.attraktor.org, spiele.j-crew.de
and dotawiki.de.
26 E.g., a triple dcterms:isPartOf owl:equivalentProperty dcterms:isPartOf in pool.
publicdomainproject.org.

156 D. Dobriy et al.
Table 6. Basic ontology metrics
SMW Cloud
Metric Mean Min Max Median
Class assertion axioms 12,782.75 0 540,701 530.0
Object property assertion axioms 21,735.10 0 1,169,337 635.5
Data property assertion axioms 55,397.72 0 3,144,162 1,793.0
Same individuals axioms 346.05 0 18,512 10.0
General annotation axioms 1,759.55 0 49,391 172.0
Annotation assertion axioms 5,065.86 0 374,185 508.0
Data property annotations 6.92 0 178 6.0
Class annotations 3.25 0 374 2.0
Object property annotations 15.58 0 374 5.0
Individual annotations 5,004.62 0 374,116 439.0
Axioms 95,654.59 0 5,236,436 3,951.5
Logical axioms 90,308.68 0 4,861,744 3,297.5
Classes(See footnote 27) 195.57 0 9,082 22.5
Classes with individuals 188.06 0 9,074 14.5
Object properties 30.83 0 1,500 21.0
Data properties 48.80 0 1,249 32.0
Individuals 12153.97 0 728,482 650.5
constructs being used in each DL expressivity class are analysed, which reveals
that only a small fraction of RDFS’ and OWL’s statements are being used in
SMW instances. Indeed, for instance, neither rdfs:domain and rdfs:range deﬁni-
tions, nor owl:equivalentClass, with one exception, hardly any multi-triple OWL
axioms are being used in SMW instances: under-use of complex OWL constructs,
not even mentioning OWL2, can therefore be also observed on the SMW ecosys-
tem, in a similar and even more pronounced form than already observed more
than 10 years ago for the LOD Cloud [ 16]. Also, due to the sparse use of sub-
classing and sub- or equivalent properties, further analysis does not further focus
on ontology metrics and quality framework metrics, which emphasize schema
depth/inheritance richness [27], see also Footnote
27 in Table6.
In our metric processing, we calculate all Quality Frameworks indicated in
Table2. Although it is not feasible to discuss the evaluation of frameworks in
full, we demonstrate the OQueRe framework in Table8, exampliﬁed by metrics
receiving the best score and the worst score suggesting a more in-depth analysis
as subject of future work capitalizing on the resource established in this work.
27 Due to the observed lack of hierarchical structure, thenumber of classes is equivalent
with the number of root classes , paths to leaf classes , absolute leaf cardinality and
absolute depth , so we do not provide these metrics separately..

SMW Cloud: A Corpus of Domain-Speciﬁc Knowledge Graphs 157
Table 7. Use of the RDF(S)+OWL and DL expressivity of SMW instances
Number of SMW instances: AL
(99)
AL(D)
(165)
ALO(D)
(708)
ALE O(D) –
(50)
ALHO(D)
–
(3)
(1029)
rdf:type 10206194 217002 18593506 1807 69973 29088482
rdfs:isDeﬁnedBy 1829566 35365 2987260 665 3336 4856192
rdfs:label 1829657 35365 2988428 666 3336 4857452
rdfs:seeAlso – – 2 – – 2
rdfs:subClassOf – 51 16 – – 67
rdfs:comment – – 255 – – 255
owl:imports 1430995 26574 2065990 443 3065 3527067
owl:Ontology 1430995 26574 2065990 443 3065 3527067
owl:Class 136758 3934 193832 39 7175 341738
owl:DatatypeProperty 8043 3027 35345 17 216 46648
owl:ObjectProperty 8377 1232 19169 24 82 28884
owl:sameAs 450445 – 358972 76 164 809657
owl:diﬀerentFrom – – 16 – – 16
owl:equivalentProperty – – – – 5 5
owl:intersectionOf – – – 3 – 3
owl:Restriction – – – 3 – 3
owl:onProperty – – – 3 – 3
owl:hasValue – – – 3 – 3
rdf:ﬁrst – – – 6 – 6
rdf:rest – – – 6 – 6
rdf:nil – – – 3 – 3
Table 8. OQueRE Metrics and Scores
Metric Mean Min Max Median Score
Mean number of
annotations per
class
37.96 0.65 710.16 14.29 1 (excellent)
Mean number of
attributes per
class
1.05 0.01 2.67 0.77 1 (excellent)
Weighted
Method Count:
Mean number of
properties per
class [ 6]
345.37 0.70 55439.4 35.19 5 (unsatisfactory)
5 Conclusion and Future Work
This paper presented and characterized the SMW Cloud corpus, an extensive
collection of RDF data collected from Semantic MediaWiki instances. We demon-
strate, with a focused crawling pipeline, that we can identify and collect data
from over 1000 SMW instances, some of which have been in existence and active
use for over 15 years, which demonstrates the considerable interest of relevant
communities and SW technology users of this largely unobserved part of the
Semantic Web.

158 D. Dobriy et al.
To promote interoperability and ease of use, the SMW corpus is made avail-
able as HDT and the corpus’ metadata is queryable via a SPARQL endpoint, in
line with the FAIR data principles [29]. We plan to update the SMW Cloud reg-
ularly and extend it by discovering and crawling RDF from new SMW instances
as they appear.
Following the same approach, we recommend that Semantic MediaWiki
developers 1) enable RDF dump generation by default rather than requiring
administrators to manually make use of a maintenance script to create a dump
(or us to crawl the RDF data per page) 2) when a SPARQL-enpoint is available,
make it discoverable through SMW API and 3) consider adopting HDT as a
compact format for publishing regular dumps as we have demonstrated that it
is highly compact format for SMW data (achieving a Data Compression Ratio
of 17,5 for SMW Cloud compared to NTriples, more eﬃciently that for other
benchmarks evaluated [20]).
In terms of evaluation and benchmarking as a ﬁeld of interest of the Seman-
tic Web Community [4], SMW Cloud provides a novel and distinct dataset with
unique characteristics that introduces variety into the ﬁeld of LOD sources inves-
tigated so far; we have demonstrated these unique characteristics in terms of a
variety of common basic graph and ontology metrics, that illustrate signiﬁcant
diﬀerences of RDF usage within SMW instances and the rest of the LOD Cloud.
We expect the SMW Corpus to enable previously unexplored approaches in LOD
and EKG research.
5.1 Limitations
Statistics calculated by us can not be directly integrated back into individual
SMWs, creating a discoverability problem. To this end, it is planned to introduce
an SMW extension that will 1) schedule regular RDF dump generation, 2) notify
the proposed architecture of the Wiki, and 3) fetch calculated statistics from the
SMW Corpus and integrate them into the Wiki.
5.2 Future Work
As future work we think that the SMW corpus can also provide a basis for longi-
tudinal analysis, link analysis [17], etc. This will enable a better understanding
of dynamics and evolution of vocabularies. It is our goal to create proﬁling tools
and resources enabling users to create an assessment of the data at hand [3].
Finally, as noted in Sect. 1, Wikibases are the second most widely used seman-
tic wiki platform to date. Therefore, crawling eﬀorts and analyses of Wikibase
instances following a similar methodology are a prioritised part of future work.
5.3 Sustainability Plan
To account for the updates in the SMW Cloud, which particularly concerns
the introduction of new SMW instances, but also general changes to already

SMW Cloud: A Corpus of Domain-Speciﬁc Knowledge Graphs 159
accounted SMWs, we plan to release new versions of SMW Cloud at least annu-
aly. The sustainability plan includes further extension of the automatic metric
calculation in the frame of future work and other continuing research as well as
tight collaboration with other researchers and users with regards to its further
development and maintenance, as well as use case documentation.
We are commited to sustainably host and maintain the corpus thought our
institute that already hosts various widely adopted Semantic Web resources for
several years now and promote the sustainability strategy within ongoing com-
munity activities such as the “Distributed Knowledge Graphs” COST Action
28,
which as one of its activities aims at aligning and sustaining community services
and tools.
The Resource is made Accessible in Following Ways:
1. The aggregated SMW Cloud dataset is made available via the institutional
repository.29
2. The SMW Cloud corpus containing individual SMW datasets is also made
available via the institutional repository.30
3. The calculated metrics for the corpus are available via a public SPARQL
endpoint.31
Acknowledgements. The authors would like to express their profound gratitude and
give special acknowledgment to Alexandra Hager for her invaluable, expert and time-
critical support, Thomas Seyﬀertitz for expert advice in the area of research data
management and Gary Brewer, BuiltWith, for providing an extensive MediaWiki col-
lection. This work is part of a project funded by theWU Anniversary Fund of the City
of Vienna .
References
1. Abedjan, Z., Gruetze, T., Jentzsch, A., Naumann, F.: Proﬁling and mining RDF
data with ProLOD++. In: 2014 IEEE 30th International Conference on Data Engi-
neering, pp. 1198–1201. IEEE, Chicago, IL, USA, March 2014.https://doi.org/10.
1109/ICDE.2014.6816740, http://ieeexplore.ieee.org/document/6816740/
2. Alexander, K., Cyganiak, R., Hausenblas, M., Zhao, J.: Describing linked datasets.
In: LDOW (2009)
3. Bohm, C., et al.: Proﬁling linked open data with ProLOD. In: 2010 IEEE 26th
International Conference on Data Engineering Workshops (ICDEW 2010), pp. 175–
178. IEEE, Long Beach, CA, March 2010. https://doi.org/10.1109/ICDEW.2010.
5452762, http://ieeexplore.ieee.org/document/5452762/
4. Boncz, P., Fundulaki, I., Gubichev, A., Larriba-Pey, J., Neumann, T.: The linked
data benchmark council project. Datenbank-Spektrum 13(2), 121–129 (2013)
28 https://cost-dkg.eu/.
29 https://semantic-data.cluster.ai.wu.ac.at/smwcloud/.
30 https://semantic-data.cluster.ai.wu.ac.at/smwcloud/corpus/.
31 https://smwcloud-sparql.cluster.ai.wu.ac.at/.

160 D. Dobriy et al.
5. Burns, A., et al.: A suite of generative tasks for multi-level multimodal webpage
understanding. arXiv preprint arXiv:2305.03668 (2023)
6. Duque-Ramos, A., Fern´ andez-Breis, J.T., Stevens, R., Aussenac-Gilles, N.:
OQuaRE: a SQuaRE-based approach for evaluating the quality of ontologies. J.
Res. Pract. Inf. Technol. 43(2) (2011)
7. Ermilov, I., Demter, J., Martin, M., Lehmann, J., Auer, S.: Lodstats–large scale
dataset analytics for linked open data. Under review in ISWC (2013)
8. Ermilov, I., Lehmann, J., Martin, M., Auer, S.: LODStats: the data web cen-
sus dataset. In: Groth, P., et al. (eds.) ISWC 2016. LNCS, vol. 9982, pp. 38–46.
Springer, Cham (2016). https://doi.org/10.1007/978-3-319-46547-0 5
9. Ermilov, I., Martin, M., Lehmann, J., Auer, S.: Linked open data statistics: collec-
tion and exploitation. In: Klinov, P., Mouromtsev, D. (eds.) KESW 2013. CCIS,
vol. 394, pp. 242–249. Springer, Heidelberg (2013). https://doi.org/10.1007/978-
3-642-41360-5 19
10. Escobar, P., Candela, G., Trujillo, J., Marco-Such, M., Peral, J.: Adding value to
linked open data using a multidimensional model approach based on the RDF data
cube vocabulary. Comput. Stand. Interfaces 68, 103378 (2020)
11. Fahl, W., Holzheim, T., Westerinen, A., Lange, C., Decker, S.: Getting and hosting
your own copy of wikidata. In: Wikidata Workshop @ ISWC 2022 (2022).https://
ceur-ws.org/Vol-3262/paper9.pdf
12. Fern´andez, J.D., Martınez-Prieto, M.A., Guti´errez, C., Polleres, A., Arias, M.:
Binary RDF representation for publication and exchange (HDT). J. Web Semant.
19(2) (2013).https://doi.org/10.1016/j.websem.2013.01.002, http://www.polleres.
net/publications/fern-etal-2013-HDT-JWS.pdf
13. Fern´andez, J.D., Beek, W., Mart´ ınez-Prieto, M.A., Arias, M.: LOD-a-lot. In:
d’Amato, C., et al. (eds.) ISWC 2017. LNCS, vol. 10588, pp. 75–83. Springer,
Cham (2017). https://doi.org/10.1007/978-3-319-68204-4 7
14. Fern´andez, M., Overbeeke, C., Sabou, M., Motta, E.: What makes a good ontology?
A case-study in ﬁne-grained knowledge reuse. In: G´omez-P´erez, A., Yu, Y., Ding,
Y. (eds.) ASWC 2009. LNCS, vol. 5926, pp. 61–75. Springer, Heidelberg (2009).
https://doi.org/10.1007/978-3-642-10871-6 5
15. Gangemi, A., Catenacci, C., Ciaramita, M., Lehmann, J.: Modelling ontology eval-
uation and validation. In: Sure, Y., Domingue, J. (eds.) ESWC 2006. LNCS,
vol. 4011, pp. 140–154. Springer, Heidelberg (2006). https://doi.org/10.1007/
11762256
13
16. Glimm, B., Hogan, A., Kr¨otzsch, M., Polleres, A.: OWL: yet to arrive on the web of
data? In: WWW2012 Workshop on Linked Data on the Web (LDOW2012). Lyon,
France, April 2012. http://www.polleres.net/publications/glim-etal-2012LDOW.
pdf
17. Haller, A., Fern´andez, J.D., Kamdar, M.R., Polleres, A.: What are links in linked
open data? A characterization and evaluation of links between knowledge graphs
on the web. J. Data Inf. Qual. 12(2), 1–34 (2020)
18. Krabina, B.: Building a knowledge graph for the history of Vienna with semantic
MediaWiki. J. Web Semant. 76, 100771 (2023)
19. Kr¨otzsch, M., Vrandeˇci´c, D., V¨olkel, M.: Semantic MediaWiki. In: Cruz, I., et al.
(eds.) ISWC 2006. LNCS, vol. 4273, pp. 935–942. Springer, Heidelberg (2006).
https://doi.org/10.1007/11926078
68
20. Mart´ınez-Prieto, M.A., Arias Gallego, M., Fern´andez, J.D.: Exchange and con-
sumption of huge RDF data. In: Simperl, E., Cimiano, P., Polleres, A., Corcho,
O., Presutti, V. (eds.) ESWC 2012. LNCS, vol. 7295, pp. 437–452. Springer, Hei-
delberg (2012). https://doi.org/10.1007/978-3-642-30284-8 36

SMW Cloud: A Corpus of Domain-Speciﬁc Knowledge Graphs 161
21. Meusel, R., Petrovski, P., Bizer, C.: The webdatacommons microdata, RDFa and
microformat dataset series. In: Mika, P., et al. (eds.) ISWC 2014. LNCS, vol. 8796,
pp. 277–292. Springer, Cham (2014). https://doi.org/10.1007/978-3-319-11964-
9 18
22. Nogales, A., Angel Sicilia-Urban, M., Garc´ıa-Barriocanal, E.: Measuring vocabu-
lary use in the linked data cloud. Online Inf. Rev. 41(2), 252–271 (2017)
23. Orme, A.M., Yao, H., Etzkorn, L.H.: Indicating ontology data quality, stability, and
completeness throughout ontology evolution. J. Softw. Maint. Evol. Res. Pract.
19(1), 49–75 (2007)
24. Reiz, A., Sandkuhl, K.: Neontometrics–a public endpoint for calculating ontology
metrics. In: Proceedings of Poster and Demo Track and Workshop Track of the 18th
International Conference on Semantic Systems co-located with 18th International
Conference on Semantic Systems (SEMANTiCS 2022), vol. 13, pp. 22–15. CEUR-
WS, Vienna (2022)
25. Reiz, A., Sandkuhl, K.: Harmonizing the OQuaRE quality framework:. In: Proceed-
ings of the 24th International Conference on Enterprise Information Systems, pp.
148–158. SCITEPRESS - Science and Technology Publications, Online Stream-
ing (2022). https://doi.org/10.5220/0011077200003179, https://www.scitepress.
org/DigitalLibrary/Link.aspx?doi=10.5220/0011077200003179
26. Rietveld, L., Beek, W., Hoekstra, R., Schlobach, S.: Meta-data for a lot of LOD.
Semant. Web 8(6), 1067–1080 (2017)
27. Tartir, S., Arpinar, I.B.: Ontology evaluation and ranking using ontoqa. In: Inter-
national Conference on Semantic Computing (ICSC 2007), pp. 185–192. IEEE
(2007)
28. Vrandeˇci´c, D., Kr¨otzsch, M.: Wikidata: a free collaborative knowledgebase. Com-
mun. ACM 57(10), 78–85. ACM, New York, NY, USA (2014)
29. Wilkinson, M.D., et al.: The FAIR guiding principles for scientiﬁc data manage-
ment and stewardship. Sci. Data 3(1), 160018 (2016). https://doi.org/10.1038/
sdata.2016.18, https://www.nature.com/articles/sdata201618, number: 1 Pub-
lisher: Nature Publishing Group
30. Yang, Z., Zhang, D., Ye, C.: Ontology analysis on complexity and evolution based
on conceptual model. In: Leser, U., Naumann, F., Eckman, B. (eds.) DILS 2006.
LNCS, vol. 4075, pp. 216–223. Springer, Heidelberg (2006). https://doi.org/10.
1007/11799511
19
31. Yao, H., Orme, A.M., Etzkorn, L.: Cohesion metrics for ontology design and appli-
cation. J. Comput. Sci. 1(1), 107–113 (2005)

SousLeSens - A Comprehensive Suite
for the Industrial Practice of Semantic
Knowledge Graphs
Claude Fauconnet1(B) , Jean-Charles Leclerc2 , Arkopaul Sarkar3 ,
and Mohamed Hedi Karray4
1 SousLeSens, Paris, France
claude.fauconnet@gmail.com
2 TotalEnergies, Paris, France
3 Knowledge Graph Alliance, Brussels, Belgium
4 Universit´e de Technologie de Tarbes, Tarbes, France
Abstract. Over recent decades, the advancement of semantic web tech-
nologies has underscored the increasing importance of tools dedicated
to developing and managing the foundational components of the seman-
tic web stack. Addressing the evolving needs, a variety of tools have
emerged from the research and development projects from academia as
well as commercial software vendors. These tools oﬀer a diverse range
of services tailored to the management of various aspects of semantic
knowledge graphs. Despite this proliferation, feedback from stakeholders
involved in public and privately funded projects has highlighted notable
shortcomings in existing tools. These gaps become evident in two key
areas: ﬁrstly, the user experience struggles to scale up to meet industrial-
level data practices and knowledge engineering methodologies. Secondly,
a lack of interoperability and compatibility among the existing task-
speciﬁc tools leads to elevated costs and eﬀorts. This paper introduces
a novel semantic knowledge management ecosystem embodied in a suite
of tools collectively known as ’SousLeSens’. Unlike its counterparts, SLS
not only provides comprehensive coverage of typical knowledge engineer-
ing tasks while adhering to best practices for ensuring quality but also
boasts a purely visual (no to minimum-code) interface. This feature is
particularly well-suited for handling large-scale, industry-grade semantic
data models. The paper delves into the establishment of requirements
for knowledge engineering tools and services, derived from recent stake-
holder surveys. It proceeds to present the SLS toolkit, elucidating its
architecture and operational protocols. Finally, the paper validates the
toolkit’s capabilities by comparing it with existing tools against prede-
ﬁned requirements and illustrating various use cases.
Keywords: ontology editor
· knowledge graph · SousLeSens ·
protege · semantics
c⃝ The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
A. Mero˜no Pe˜nuela et al. (Eds.): ESWC 2024, LNCS 14665, pp. 162–177, 2024.
https://doi.org/10.1007/978-3-031-60635-9_10

SousLeSens 163
1 Introduction
In the evolving landscape of semantic web engineering tools, there exists a press-
ing need for solutions that can seamlessly navigate the intricacies of constructing
and managing the foundational elements of the semantic web stack. Despite the
emergence of various tools from both academic and commercial spheres, feedback
from stakeholders has consistently highlighted notable shortcomings [ 1]. These
deﬁciencies manifest themselves primarily in the struggle to scale user expe-
riences to meet industrial-level data practices and the lack of interoperability
among existing, task-speciﬁc tools, resulting in increased costs and eﬀorts.
Against this backdrop, this paper introduces ‘SousLeSens’ (SLS), a collabo-
rative semantic knowledge management (KM) ecosystem speciﬁcally designed to
address the identiﬁed gaps in the current tool landscape. Unlike its counterparts,
SLS not only comprehensively covers many typical knowledge engineering tasks,
but also lets users to use a visually driven, minimal-code interface tailored for
handling large-scale, industry-grade semantic data models. The Semantic Label-
ing System (SLS) was developed as part of the TotalEnergies Semantic Frame-
work (TSF) project [7] to address the need for a set of tools that comply with
the best practices in knowledge engineering while also being user-friendly and
easy to learn for professionals in the industry.
In this paper, we ﬁrst identiﬁed the requirements of a comprehensive KM
tool by exploring both the past literature and industrial expectations in Sect.2.
Afterwards, in Sect.3, the methodological principle and technical architecture of
SLS is presented. In Sect. 4, three industrial use cases are presented to demon-
strate the capabilities of SLS. Finally, a comparative analysis of SLS against
other similar products is presented in Sect.5.
2 State-of-the-art
The realm of KM tools is diverse, mirroring the variety of methods, languages,
and formats for knowledge management. The aim of the section is however not
to analyse these tools individually but to identify the requirements for a com-
prehensive KM tool from the past surveys and industrial feedback. SLS gathered
these requirements from two sources: 1) review of the existing KM tools and feed-
back from users of these tools as described in Sect. 2.1 and 2) industrial needs
identiﬁed through various initiatives and projects as described in Sect.2.2.
2.1 Existing Knowledge Engineering Tools
In ontology engineering, while many tools address speciﬁc phases, only a few pro-
vide comprehensive solutions. A recent EU Horizon2020 OntoCommons survey
[11] categorized tools, including competency questions for requirement speciﬁ-
cation, Linked Open Vocabulary (LOV) and IndustryPortal for ontology reuse
and publication, Chowlk and Menthor editor for conceptual modelling, various
reasoners, e.g., Pellet, Hermit, Fact++, and consistency checkers, e.g., OOPS!,

164 C. Fauconnet et al.
all of which has targeted focus in some of the activities along the ontology engi-
neering lifecycle. In contrast, a comprehensive KM tool facilitates many KM
activities, such as ontology implementation, covering drafting, source editing,
evaluation, ontology matching, maintenance, issue management, and usage as
well as managing large data volumes. Past surveys [ 3,8,9,12,13] on ontology
editing tools mention comprehensive tools such as SWOOP, Prot´eg´e, WebODE,
TopBraid Composer, OntoPic Fluent editor, OWLGrEd, OntoEdit, Anzo plat-
form, Cameo modeller, and PoolParty, which comply to the most popular and
de facto standards for knowledge engineering, such as OWL and RDF. It can
also be observed that ontology editing and knowledge graph management are
distinct activities, and the mentioned tools have varied support for both. Graph
database systems such as Neo4J, GraphDB, AllegroGraph, Stardog, and RDFox
often include dedicated data transformation tools along with a triplestore as
their main oﬀering.
The primary aspects of evaluating these tools are their features and usabil-
ity; the former covers the functionalities, architecture, and support to various
activities of ontology engineering and the latter covers various types of user
experience. Past evaluations [ 5,9,11,13] mention many common features that
ontology and knowledge graph editors typically support. These are expressivity,
language, modularisation and reusing, consistency check, reasoning and infer-
ence, merging, mapping, encoding and storage, visualisation, data transforma-
tion, query, and third-party support. As Islam and Sheikh [ 6] noted, there is
no standard approach to evaluate the usability of ontology editors. Still, some
of the usability criteria that can be found in the small number of past surveys
are user experience and visual abstraction, collaboration, multi-lingual support,
performance and scalability, methodological guidance, practicality, help and doc-
umentation, and exception handling. Easy access and deployment of the tool,
along with its openness and extensibility also play a big role in ensuring its
usability. The OntoCommons survey [11] collected 77 responses from the major
knowledge engineering tool developers using online questionnaires that include
a list of common requirements for knowledge engineering tools: collaboration
of multiple stakeholders, visualisation, debugging, validation, quality assurance
and analytics, API support, OWL support, ontology import, user-friendliness,
connected ontologies, tool integration, modularisation, search and reuse ontol-
ogy, ontology correlations, ontology deployment and document generation, and
ontology conceptualisation, understandability of GUI labels. Although the basic
features for a comprehensive ontology editor can be found by surveying the exist-
ing tools, the development of SLS prioritised those features that can fulﬁl the
requirements gathered from community surveys as mentioned above.
2.2 Industrial Feedback
The introduction of a new process and working method requires the support of
new types of tools, as described in the OntoCommons roadmap [1]. The Knowl-
edge Translator report [4] emphasizes the need for easy on-boarding and training
for the transition from a human-centric paper standard to a data-centric and

SousLeSens 165
model-centric approach, exempliﬁed by initiatives such as CFIHOS 1, allowing
the analysis of digital requirements, source coherence and internal knowledge
sharing with external partners.
In 2020 and 2021, TotalEnergies collaborated with stakeholders of the Inter-
national Association of Oil & Gas Producers
2 (IOGP) and the World Economic
Forum (WEF) to formalize the conditions for better data exchanges in the
world’s energy industries. It is evident in the industrial outlook that sharing
reliable information requires addressing the big data challenges (volume, value,
variety, velocity, and veracity) and a common way of structuring and exchanging
knowledge. The IOGP working group identiﬁed not only the fundamentals for
common semantics for data structuring and exchange but also a set of recom-
mendations for a suitable KM tool, including web (HTTP protocol) compliance,
following the motto: ‘Everything is available to everyone and everywhere at any
time’, open code practice, publishing vocabulary deﬁnitions with IRI, obligatory
common schema deﬁnition, compliance to RDF/OWL formalism, and interactive
functional web-applications for query/extraction of information. The industrial
stakeholders of the above-mentioned initiatives realised that existing tools for
supporting these semantic web requirements often have a high learning curve,
necessitating a new kind of tool for easy onboarding and upskilling. In the fol-
lowing sections, we describe how SLS addresses these requirements from the
perspective of its core architectures and various tools dedicated to critical KM
tasks.
3 Speciﬁcation of SLS
Developed within the TSF project, SousLeSens 3 (SLS) is a suite of web tools
designed to facilitate the creation of semantic knowledge graphs using ontolo-
gies. It functions as an adaptable set of tools and a cohesive suite that aims
to demystify the complexities associated with the Semantic Web. By oﬀering
a user-friendly interface, SLS makes it possible for individuals, including those
in industrial sectors, who may not specialize in these technologies, to leverage
Semantic Web capabilities. This accessibility is crucial for meeting industrial
requirements, particularly in managing data and knowledge, developing digital
twins, and supporting decision-making processes.
3.1 Methodological Foundations
The initial requirements for a knowledge graph management tool were chartered
by the TSF project in January 2021, as shown in Fig. 1. The SLS development
team facilitated the creation of initial prototypes that were periodically reviewed
to progressively develop the versatile TSF tool suite. Over time, the support
1 https://www.jip36-cﬁhos.org/cﬁhos-standards/.
2 https://www.iogp.org/.
3 https://sls.kg-alliance.org/.

166 C. Fauconnet et al.
for W3C-recommended formats in a cohesive data management framework pro-
vided a ﬂexible solution to TSF for predeﬁned data interoperability in several
use cases. This allowed the immediate reuse of internal technical references,
expressed in SKOS, by converting them into RDF and OWL formats within
TSF. The code and interface integrated methodological governance, ensuring
conformity to common structuring principles. This orchestration aligned com-
pany activities with semantic knowledge graphs, serving as domain ontologies
for reference data domains.
Fig. 1. Timeline of SousLeSens evolution.
The SLS toolset (purposes of various tools under SLS are summarised in
Fig.2) is designed to facilitate the continuous onboarding and upskilling of inter-
nal members of TotalEnergies by mirroring the exploration process of the seman-
tic web for newcomers. However, the responsive and interactive design principles
of SLS are poised to beneﬁt all users in learning semantic web technologies,
addressing common inquiries throughout the learning curve. For example: 1)
Discovering, Comparing, and Choosing Ontologies : SLS’s visualization
and manipulation of graphs under the tool Lineage simpliﬁes understanding
essential ontology notions, allowing users to explore, mix, and compare diﬀerent
ontologies with visually driven capabilities. 2) Building Ontology :S L Sp r o -
vides a user-friendly interface for creating classes, establishing semantic relation-
ships, and respecting constraints. The tool automates SPARQL queries within
triplestore databases based on the type of ontology being built. 3)Associating
an Ontology with Data : SLS aids in generating mappings between ontology
objects and data model elements, especially for tabular data. The tool allows
users to express, save, and graphically represent mappings for validating their rel-
evance. 4)Building a Semantic Knowledge Graph (SKG) : SLS transforms

SousLeSens 167
data from relational databases or CSV ﬁles into a knowledge graph using pre-
established mappings. The tool is evolving to support the RML standard in its
roadmap. 5) Using SKG : SLS supports two distinct uses of semantic knowledge
graphs, enabling queries through APIs or exploration mode. In exploration mode,
users can interact with graphical representations, simplifying queries based on
ontology concepts. 6) Collaborative Work : SLS’s internet-native architecture
promotes collaborative work by providing secure user management, data source
control, and read-write rights. Metadata addition helps trace modiﬁcations and
qualify their status. 7)Combining Tools: SLS’s layered, modular architecture,
combined with technical standards, allows it to oﬀer integrated services and act
as a client or third-party service provider, facilitating seamless combination with
other tools.
Fig. 2. Overview of SLS mapping diﬀerent usage of its tools (Lineage, KGCreator and
KGQuery) along with the technical stack (at the bottom).
In this context, the technical architecture of SLS was designed based on
the following pillars: 1) Rigorous management of semantics included in upper-
level ontologies, encoding the constraints in reference languages, such as RDF,
RDFS, and OWL; 2) A graphical visual representation, utilizing nodes and
edges as a global metaphor for an RDF graph, captures the expressive richness
of the triples graph while ensuring understandability; ﬁltering and navigation
capabilities within the network elements, coupled with the graph spatialization
engine, aid users in comprehending complexity, coherence, inconsistency, and
multiple relationships by accommodating the limitations of simultaneous infor-
mation apprehension by the human eye. 3) Alternative mode of interaction and
manipulation based on the generalization of a three-step process: translation of
user actions into SPARQL queries, execution of queries on a triplestore internal
to SLS or other in reading as well as in writing modes, and representation of
query results either in graph mode or in table mode.

168 C. Fauconnet et al.
3.2 Software Architecture
The organic design of SLS evolved by gradually aggregating functionalities
around the central core concept of visualizing and manipulating graphs. Tech-
nical solutions, implementing some original codebases, reﬂect this development.
Notably, the client bears the majority of processing, enabling rich interactions
with the graph without frequent server calls-a key for the performance of SLS.
The choice of untyped JavaScript, used on both the client and server sides
(node.js) was based on its agility in seamlessly moving code between them. Type-
Script, a typed form of JavaScript, was not used due to its heavy constraints on
typing, which were deemed impractical for our frequently evolving code needs.
The architecture of SLS is centered on its NodeJs web server which essentially
acts as a ﬂow distributor between its diﬀerent peripheral components through
secure APIs, which gives it the character of an open technical platform as shown
in Fig.3.
Fig. 3. Technical architecture of SLS
In the following, various core components of SLS are described based on the
architecture.
1. Security and access management : Each user of the SLS web interface or
API is authenticated. Several authentication systems are supported but only
one is active within an instance. In addition, requests made to the internal
TripleStore or the search engine are ﬁltered according to the user’s rights.
2. Administration and conﬁguration module : As a collaborative applica-
tion, SLS rigorously manages the access of diﬀerent users to diﬀerent resources
and allows very ﬂexible management of access to resources ranging from pub-
lic sources visible to all to private sources, having restricted write rights for

SousLeSens 169
only a few users. For this purpose, SLS has developed an administrative
management module composed of the objects: Users, having diﬀerent roles
and permissions, Source, identifying diﬀerent KGs, and Proﬁles, maintaining
access rights by mutual association.
3. Storage layer : The RDF graphs manipulated by SLS are stored either in its
internal triplestore (Virtuoso) or in other triple stores referenced and acces-
sible in SLS depending on the conﬁguration.
4. Application server layer : This layer powered by Node.js communicates
via APIs in HTTP(S) mode with the user interface and with external clients
while respecting the access rules applicable to each client. Requesting APIs
triggers various calls, e.g., execution of queries on SPARQL or SQL servers,
speciﬁc internal commands, and access to third-party APIs (python, java,
etc.) depending on the case, always checked in terms of access rights.
5. The web client layer (browser) locally manages most of the actions car-
ried out by the user (business logic) and limits the interactions with the server
layer for reading data or speciﬁc processing. For example, the construction of
SPARQL or SQL queries in response to user actions is done dynamically on
the client side, unlike the practices of many other applications. SLS incorpo-
rates common UI components, such as theSourceSelector, for user-authorized
source selection, the jsTreeWidget, facilitating tree representation and node
control actions, and the NodeInfos dialogue, displaying predicates of a node,
including the ability to add or remove predicates based on user rights and
experimental visualization of axioms. These components streamline various
interactions within the interface across multiple contexts.
6. Visual representation of knowledge graphs stands out in SLS by prior-
itizing graph drawing and manipulation, a central feature that distinguishes
it from similar tools. It utilizes the vis.js
4 JavaScript library, oﬀering a robust
API for graph visualization and interaction. Vis.js provides various spatial-
ization algorithms, optimizing graph representation based on factors like the
number of relationships each node has, with central nodes having more con-
nections. For example, the conﬁguration for the BarnesHut layout algorithm,
which is a quadtree-based gravity model and the fastest non-hierarchical
solver. Graph stabilization is achieved through successive iterations, which
can be manually interrupted by users. Before graph drawing in SLS, SPARQL
queries select triples from the store, transformed into nodes and edges using
vis.js API. As RDF graphs in OWL ontologies or SKGs can be intricate,
diﬀerent triplet ﬁltering strategies, detailed in Sect. 3.3, are implemented for
clear and useful representations. Once represented on the screen it is possible
to interact via the mouse with the nodes and edges of the graph in order either
to obtain information to navigate in the graph or to create new predicates.
7. Plugins: SLS has a system of plugins allowing users to create speciﬁc appli-
cations, including their web app, that can be used like other tools and take
advantage of the entire environment. The open architecture of SLS supports
4 https://github.com/visjs.

170 C. Fauconnet et al.
interaction with external libraries, such as JOWL 5 -a Java web application
with REST APIs developed in 2023. This integration allows the execution of
OWLAPI and SWRL (reasoner and rules) Java methods within SLS. Addi-
tionally, an integrated Python API enables users to choose import/export
formats for triplestores and, soon, to interact with SLS-referenced graphs
from a Jupyter or other Python environment while respecting user access
rights.
8. Deployment: SLS’s technical environment is deployed through diverse
Docker images, including a node.js web server with SLS code and APIs
6,
a Virtuoso triplestore, an ElasticSearch search engine, an SQL server (and
soon Postgres SQL) database, a Python environment, and optional third-
party components and speciﬁc SLS plugins.SLS can be downloaded freely
from its GitHub repository
7 under an MIT license. SLS releases follow a
standard versioning system. Supporting the easy onboarding, a documenta-
tion website8 (currently containing ‘quick start’ and many video tutorials) is
also made available.
3.3 Tools in SLS
Lineage in SLS facilitates the simultaneous representation and manipulation
of graph representations of diﬀerent ontologies. It enables the selection, editing,
evaluation, and comparison of ontologies, allowing users to generate overviews
or details for speciﬁc tasks. Key features include selecting source ontologies,
transforming triples into interactive graph drawings, random navigation on the
whiteboard, creation of classes and individuals, visualization of predicates and
axioms, drag-and-drop relationship creation, advanced SPARQL query genera-
tion, representation of label similarities, label-based graph searches, and object
properties selection and presentation. The UI components of Lineage displaying
an example ontology shown in Fig.4. Lineage being a versatile ontology editor,
it supports constraints on class and properties in a variety of expressivity, from
simple subsumption and transitivity suitable of RDF graph to domain, range,
existential, and universal constraints to support full Description Logic (DL) for-
malism. The graph-drawing complexity is balanced by providing the option to
export information displayed in tabular form (CSV) for users accustomed to
spreadsheets and relational databases. As SLS is integrated into IndustryPortal
[2], users may search for a FAIR ontology from the portal for easy reuse.
KGCreator can be used to simplify the transform complex industrial data into
a semantic knowledge graph by serving as a user-friendly alternative to RML
or R2ML-based tools. Its straightforward structure, depicted in Fig. 5,p r o v e s
5 https://github.com/souslesens/jowl.
6 https://sls.kg-alliance.org/api/v1/.
7 https://github.com/souslesens/souslesensVocables.
8 http://souslesens.org/index.php/tools/.

SousLeSens 171
Fig. 4. Lineage tool displaying an ontology with upper ontologies in its import and
various UI controls for users to manage, view and edit the ontology.
eﬀective for even non-specialist operators. While KGCreator facilitates interop-
erability with standards by easily translating to RML, it oﬀers features such
as access to tabular data schemas, graphical exhibition of the ontology for col-
umn/class associations, detailed mapping for enriched associations, visualization
of mappings’ completeness and consistency, and simulation of generated triplets
for previewing and corrections before storing in the triple store. Additionally,
KGCreator supports functions and transformations for data line processing and
table mapping, ensuring ﬂexibility in adjusting data structures and avoiding
errors. Resource identiﬁers in KGCreator can take various forms, including real
URIs and blank nodes associated with random numbers. Triplet Generation
Engine, a backend processing program, utilizes mappings and associated data to
generate the knowledge graph in the triple store, oﬀering an API for regenerating
the entire sub-graph from previous mapping.
KGQuery allows the use of SKG in exploration mode without having to mas-
ter the SPARQL language and know the complex structure of the graph, the
KGQuery tool oﬀers an interactive query-able abstraction of the KG, which
allows users to automatically generate queries by graphically selecting the
classes, as shown in Fig. 6. KGQuery is also able to apply ﬁlters and per-
form queries on multiple graphs. The visual manipulation of knowledge graphs
through queries relies on correct data typing and predicate construction in
alignment with ontology constraints during graph construction. The queryable
abstraction of the KG is derived from the actual classes and predicates present in
the graph, maintaining ﬁdelity. The graph traversal algorithm, based on short-
est path calculations using adjacency matrices, facilitates automatic SPARQL
query construction, with results presented in tabular form - following the usual
expectations of data users - along with group queries and set operations.

172 C. Fauconnet et al.
Fig. 5. KGCreator interface to create and manage mapping from heterogeneous sources
(e.g., database, CSV) to ontology and generate triples using these mappings.
Fig. 6. Example of automatic SPARQL query generation using the graphical interface
of KGQuery.
4 Validation
In this section, we ﬁrst provide three industrial use cases to demonstrate the
practical use of SLS in semantic modelling and exploitation of data. Furthermore,
we discussed the essential capabilities of SLS in comparison to other tools against
the scope, coverage, and requirements identiﬁed in Sect.2.
4.1 Case Studies
As a fundamental tool, SLS supports many data activities in TSF. The following
sections present three use cases where SLS plays major roles in standardising

SousLeSens 173
industrial data for cross-organisation exchange, supporting business decisions,
and valorising geoscience data by integrating AI tools for oil discovery.
Lineage for Reusing Semantic Standards for Industrial Data. Onto-
Commons Roadmap [1] identiﬁes industrial needs for enhanced data standards,
such as logic-based formats, integration of cross-cutting standards, and multi-
domain stakeholder involvement. The development of the CFIHOS RDL9 proto-
type during the READI JIP10 in Norway (2018-2022), aligned with the Industrial
Domain Ontology11 (IDO) structure, exempliﬁes progress in this area, fostering
major industry adoption under ISO standardization. The lack of interoperability
among standardized ontologies and the demand for clear presentations of CFI-
HOS RDL values emphasize the importance of semantization, providing beneﬁts
like easier accessibility and ﬂexibility for extensions. Lineage proves valuable in
facilitating collaboration in ontology setup and validation phases through its ﬁl-
tering capabilities and visual representations, aiding in the detection of defaults.
TotalEnergies leverages Lineage for digital technical data interoperability and
NLP processing for noise reduction and enhancing machine learning conﬁdence
in used labels, based on application ontologies in the Geosciences and Reservoir
Well domain, which are built following ISO 23726 standard family for ontology
and ISO/IEC 81346 standard for managing digital data. Lineage’s key appli-
cations include versatile source comparisons, collaborative work on a writable
semantic layer, ensuring coherence in the domain knowledge graph, developing
a collaborative CFIHOS vocabulary in IDO through SLS, and facilitating easy
integration of business applications with reference domain ontologies across the
organization.
KGCreator and KGquery for Business Decision Support. KGCreator
and KGQuery play a pivotal role in TotalEnergies’ business decision support,
particularly in addressing challenges during major installation shutdowns, as
showcased in the Dalia asset’s life cycle extension project. In this project, SLS,
equipped with KGCreator and KGQuery, optimized planning sequences by con-
sidering criteria from various Information Systems like SAP, Document Manage-
ment System, and Primavera planning tool. The digital approach transformed
the project by facilitating real-time insights across disciplines and systems, with
a key strength in linking each Work Breakdown Structure item with pertinent
data sources for eﬃcient categorization and ﬁltering. The application of KGCre-
ator and KGQuery within SLS resulted in streamlined decision making, eﬃcient
change management, simpliﬁed project reviews, automated compliance checks,
and impact analysis, bringing tangible beneﬁts such as reduced standby risks,
improved operational eﬃciency, comprehensive documentation, and continuity
preservation.
9 https://www.jip36-cﬁhos.org/cﬁhos-standards/.
10 https://readi-jip.org/.
11 https://www.iso.org/standard/87560.html.

174 C. Fauconnet et al.
SLS for AI-Powered Oil Discovery and Ocean Exploration. TotalEner-
gies’ pilot study integrates SLS and advanced AI tools like NLP, GPT, and LLM
with the well domain ontology (see Sect. 4.1) to revolutionize oil discovery and
ocean exploration. NLP addresses challenges in managing complex informational
portfolios, while GPT enriches the knowledge graph with additional facts. The
experiment focuses on SLS for metadata management, entity reconciliation, and
acculturation support to enhance data value and mitigate challenges in process-
ing data labels and business objects across contexts. The proposed demonstra-
tor, leveraging diverse databases while preserving semantics, aims to rationalize
source databases, enhance data usage, and virtualise data access. For generative
AI projects, SLS provides a reference vocabulary-based semantic guidance and
automated veriﬁcation by reasoning as an essential service to address interoper-
ability challenges and inaccurate data. An SLS python API facilitates easy access
to SLS RDF graphs and third-party AI tool libraries in the Jupiter python envi-
ronment. In conclusion, the modular elements of SLS oﬀer a comprehensive app-
roach to combine generative AI and ontologies for data and industrial engineer-
ing document valorisation. The proposed benchmarking initiative will emphasize
knowledge graphs’ role in enhancing LLMs’ accuracy for question answering on
enterprise SQL databases, as posited by Sequeda et al. [10].
5 Comparative Analysis
SLS aims to be one of the most widely used modern ontology editors that sup-
ports OWL and RDF. It therefore includes tools that span various stages of
ontology engineering, notably Lineage for ontology implementation and KGCre-
ator and KGQuery for ontology maintenance and use. This combination of fea-
tures within a single ecosystem is uncommon among other tool systems, with the
exception of TopBraid and PoolParty. Notably, Prot´eg´e, in its standard oﬀering,
does not include knowledge graph management. Various features of Lineage,
such as the visual whiteboard for conceptual to formal drafting of ontology,
mapping, matching and comparison facility for handling ontology import stack
in a modular fashion, along with in-place guidance to help users build coher-
ent ontologies typical to the other ontology editors, SLS stands out from other
editors, e.g., Protege, TopBraid Composer, WebODE, SWOOP, OntoPic and
Fluent with its unique feature of purely visual, no to minimal code environment
for ontology editing - although many of them provide ad hoc graph visualisa-
tion. This purely visual design becomes a more distinguishable feature of SLS
in terms of KGCreator and KGQuery, considering no comprehensive knowledge
management system contains such a novel interface. Collaboration is a primary
feature of SLS and covers every knowledge engineering activity under its sup-
port. Although collaboration is also provided by some of the other editors, e.g.,
WebProtege, TopBraid, Anzo, SWOOP, and OntoEdit, the user experience for
these editors will be vastly diﬀerent in comparison to SLS’s multi-user simul-
taneous manipulation of visual knowledge graphs. Lastly, in past and ongoing
projects, SLS’s visual abstraction of many complexities of end-to-end knowl-
edge engineering has proven to be particularly suitable for industrial users in

SousLeSens 175
Table 1. Comparison of tools. Columns: A - coverage of KM activities (e - editing
ontology, r - reasoning KG, v - visualizing KG, p - population of data in KG, q - query,
u - use), B - modularisation/import resolution, C - search and reuse ontology, D - Con-
sistency check, E - reasoning/inference, F - rules, G - mapping, H - model repository,
I - conceptualisation, J - data transformation, K - visual query, L - collaboration, M
- methodological guide, N - User-friendliness (no-code environment, ease of learning,
third-party integration)
Tools A B C D E F G H I J K L M N
Prot´eg´e e,r,v Y N Y Y Y N N N N N N Y N
WebProtege e,r,v Y N Y N Y N Y N N N Y Y N
OntoPic p,q,v N N N N N Y N N Y N Y N Y
TopBraid e,r,v,p,q Y Y Y Y Y Y N N Y N Y N N
Fluent e,r,v Y N Y Y Y Y N N N N N Y N
OWLGrEd e,v Y Y N N N N Y Y N N N N N
OntoEdit e,r Y Y Y Y N N N N N N N N N
Anzo p,q,v,u Y Y Y N N Y Y N Y N Y N Y
PoolParty e,v,p,u Y Y N Y N Y Y Y Y N Y N Y
SLS e,r,v,p,q,u Y Y Y Y Y Y Y Y Y Y Y Y Y
co-modelling, co-creating and co-analysing vast amounts of data for common
understanding, system-wide integration and exchange, supporting practical ben-
eﬁts in decision support driven by SLS’s easy integration with other AI-based
tools.
In Table1, we provided a comparative analysis of the SLS against the require-
ments identiﬁed in Sect.2, considering only the default conﬁguration, i.e., with-
out any plug-in for every product. As described in Sect.2, the requirements are
derived from two sources: 1) user surveys on existing tools, and 2) industrial
feedback. The tools presented in Table1 include many other features, which are
sometimes unique to them. These features are not included for them not being
part of baseline requirements. Therefore, the comparison matrix in Table1 is not
an evaluation of the overall eﬃcacy of the tools, as each one of them is built with
its purpose and serves its users with some unique features. Moreover, the com-
parison is conducted by the authors conjointly with some industrial stakeholders
and users, which lacks the critical mass of a typical survey. We want to conduct
a wide survey to compare several existing tools against SLS in the future.
SLS being more focused on ease of use for industrial operators, it does not
yet provide some of the more rigorous language supports that are available in
other tools. e.g., Prot´eg´e. These languages and grammars, including Manchester
Syntax Format for writing complex axioms, SWRL, DataLog, or SPIN rules for
rule-based inference, and SHACL for data validation. The mappings created by
KGCreator is also not exchangeable in standardised formats such as RML and
SSSOM. We plan to include these features in the future versions of SLS.

176 C. Fauconnet et al.
6 Conclusion
This paper introduced SousLeSens (SLS) as a solution that addresses practi-
cal industrial needs and facilitates easy onboarding of industries into semantic
web technologies, especially at a time when traditional data technologies are
no longer suﬃcient to manage present and future data challenges. SLS, born
out of industry necessity, now aspires to foster broad adoption of semantic KM
practices. The future work will focus on key areas for improvement and expan-
sion, including collaboration support, enhanced graphic axiom creation tools,
speciﬁc ontology creation tools, reasoner capabilities for KGcreator mappings
validation, reﬁning the virtual SQL query system in KGquery, and reshaping
the user interface for better ergonomics and a responsive design. Looking ahead,
SLS envisions growing its user community to drive its development roadmap,
along with fostering collaboration between academic and industrial perspectives
through its open-source initiatives. The establishment of a dedicated working
group within the Knowledge Graph Alliance
12 (KGA) will play a pivotal role in
achieving these goals and ensuring the continuous evolution of SLS to meet the
evolving needs of its user base13.
Acknowledgment. This work was funded by the EU H2020 Ontology-driven Data
Documentation for Industry Commons (OntoCommons) under grant agreement no.
958371 and was supported by TotalEnergies and SousLeSens. We would like to thank
Karim Ounnoughi from Akkodis Group, Xavier Garnier and Nicolas Chauvat, from
Logilab, Amine Karoui from UTTOP, and Pierre Jallais from TotalEnergies for their
valuable technical contributions to this work.
References
1. Adamovic, N., et al.: Ontocommons roadmap v1, January 2023. https://doi.org/
10.5281/zenodo.7544509
2. Amdouni, E., Sarkar, A., Jonquet, C., Karray, M.H.: IndustryPortal: a common
repository for FAIR ontologies in industry 4.0. In: The 22nd International Semantic
Web Conference. Athens, Greece (2023)
3. Buraga, S.C., Cojocaru, L., Nichifor, O.C.: Survey on web ontology editing tools.
Trans. Autom. Control Comput. Sci. NN(ZZ), 1–6 (2006)
4. Goldbeck, G., et al.: The Translator in Knowledge Management for Innovation -
A Semantic Vocation of Value to Industry (2023)
5. Gyrard, A., Datta, S.K., Bonnet, C.: A survey and analysis of ontology-based
software tools for semantic interoperability in IoT and WoT landscapes. In: IEEE
World Forum on Internet of Things, WF-IoT 2018 - Proceedings, vol. 2018-Janua,
pp. 86–91 (2018). https://doi.org/10.1109/WF-IoT.2018.8355091
6. Islam, N., Sheikh, G.S.: A review of techniques for ontology editor evaluation. J.
Inf. Commun. Technol. 9(2), 104–114 (2015)
12 https://www.kg-alliance.org/.
13 https://ontocommons.eu.

SousLeSens 177
7. Leclerc, J.C., Tetard, G., Keraron, Y., Fauconnet, C.: Use of ontologies to struc-
ture and manage digital technical data of industrial assets: ﬁrst steps towards an
ecology of knowledge in multi-energies industry. In: CEUR Workshop Proceedings,
vol. 3240 (2022)
8. Rahamatullah Khondoker, M., Mueller, P.: Comparing ontology development tools
based on an online survey. In: WCE 2010 - World Congress on Engineering 2010,
vol. 1, pp. 188–192 (2010)
9. Rastogi, N., Verma, P., Kumar, P.: Analyzing ontology editing tools for eﬀective
semantic information retrieval. Int. J. Eng. Sci. Res. Technol. 6(5), 40–47 (2017).
http://www.ijesrt.com
10. Sequeda, J., Allemang, D.T., Jacob, B.: A Benchmark to Understand the
Role of Knowledge Graphs on Large Language Model’s Accuracy for Question
Answering on Enterprise SQL Databases. ArXiv abs/2311.0 (2023). https://api.
semanticscholar.org/CorpusID:265150432
11. Skjæveland, M.G., Slaughter, L.A., Kindermann, C.: OntoCommons D4.3 - Report
on Landscape Analysis of Ontology Engineering Tools, April 2022.https://doi.org/
10.5281/zenodo.6504670
12. Slimani, T.: Ontology development: a comparing study on tools, languages and
formalisms. Indian J. Sci. Technol. 8(24) (2015). https://doi.org/10.17485/ijst/
2015/v8i1/54249
13. Youn, S., Arora, A.: Survey about Ontology Development Tools for Ontology-based
Knowledge Management. University of ..., pp. 1–26 (2009). http://suanpalm3.
kmutnb.ac.th/teacher/FileDL/supot22255310501.pdf

MLSea: A Semantic Layer for Discoverable
Machine Learning
Ioannis Dasoulas(B) , Duo Yang , and Anastasia Dimou
KU Leuven – Leuven.AI – Flanders Make@KULeuven, Leuven, Belgium
{ioannis.dasoulas,duo.yang,anastasia.dimou}@kuleuven.be
Abstract. With the Machine Learning (ML) ﬁeld rapidly evolving, ML
pipelines continuously grow in numbers, complexity and components.
Online platforms (e.g., OpenML, Kaggle) aim to gather and disseminate
ML experiments. However, available knowledge is fragmented with each
platform representing distinct components of the ML process or inter-
secting components but in diﬀerent ways. To address this problem, we
leverage semantic web technologies to model and integrate ML datasets,
experiments, software and scientiﬁc works into MLSea, a resource con-
sisting of: (i) MLSO, an ontology that models ML datasets, pipelines
and implementations; (ii) MLST, taxonomies with collections of ML
knowledge formulated as controlled vocabularies; and (iii)MLSea-KG,
an RDF graph containing ML datasets, pipelines, implementations and
scientiﬁc works from diverse sources. MLSea paves the way for improving
the search, explainability and reproducibility of ML pipelines.
Keywords: Machine Learning
· Ontologies · Knowledge Graphs ·
Semantic Web · Big Data Management
Resource Type: Ontology, Taxonomies and Knowledge Graph.
MLSea: https://w3id.org/mlsea.
MLSO Ontology: https://w3id.org/mlso.
DOI: 10.5281/zenodo.10286868 | License: CC BY 4.0.
MLSea-KG: https://w3id.org/mlsea-kg.
DOI: 10.5281/zenodo.10287349 | License: CC BY 4.0.
1 Introduction
As the ﬁeld of Machine Learning (ML) continues to evolve, ML pipelines have
grown in complexity, incorporating numerous systems, algorithms, datasets
and hyper-parameters. Therefore, creating ML pipelines necessitates extensive
research and a signiﬁcant number of experiments to assess potential conﬁgura-
tions, leading to expensive testbeds in terms of available resources and time [69].
To facilitate the construction of ML pipelines, several general-purpose (e.g.,
OpenML [ 46,68], Papers with Code [ 50] or Kaggle [ 34]) and type-speciﬁc
(e.g., Hugging Face [27] and TensorFlow [65] which focus on deep learning) plat-
forms and repositories catalogue ML experiments. Yet these platforms not only
c⃝ The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
A. Meroño Peñuela et al. (Eds.): ESWC 2024, LNCS 14665, pp. 178–198, 2024.
https://doi.org/10.1007/978-3-031-60635-9
_11

MLSea: A Semantic Layer for Discoverable Machine Learning 179
exhibit variations in their data representations, access interfaces and search func-
tionalities, but they also cover diverse aspects of ML pipelines. Hence, obtaining
a holistic view of the entire ML pipeline process can be challenging, further hin-
dering the already time-consuming and resource-intensive nature of the task and
heightening the raising concerns about a reproducibility crisis in AI [23,28].
The searchability of ML pipelines can be improved by semantically enhanced
representations that capture the entire spectrum of the ML process and embrace
their diversity. This way, the discovery of ML knowledge can be facilitated by
complementing ML knowledge across platforms. Eﬃcient ML pipelines can then
be achieved by discovering relevant datasets, publications, parameters and design
choices from past experiments, without browsing over multiple platforms.
While past works have tried to model the various aspects of the ML pro-
cess [16,37,49,54], they do not represent all aspects of the ML pipelines. Every
framework is designed to model distinct data sources or aspects of the ML pro-
cess, resulting in a scarcity of datasets and services that combine publicly acces-
sible ML knowledge from a variety of sources.
To tackle these challenges, this work studies the ML pipeline, dataset
attributes and software characteristics available in online repositories (e.g.,
OpenML, Kaggle, Papers with Code), and integrates their ML experiment data
and metadata, resulting in our resource, MLSea, which makes these contribu-
tions:
(i) The Machine Learning Sailor Ontology ( MLSO) that reuses and
extends state-of-the-art ontologies to describe ML workﬂows, conﬁgura-
tions, experimental results, models, datasets, and software implementa-
tions.
(ii) The Machine Learning Sailor Taxonomies ( MLST): 8 Simple Knowl-
edge Organization System (SKOS) [43] taxonomies of ML-related concepts
(e.g., task types, evaluation measures) with a combined total of 4532 SKOS
concepts.
(iii) The Machine Learning Knowledge Graph ( MLSea-KG), a declara-
tively constructed and regularly updated KG with more than 1.44 billion
RDF triples of ML experiments, regarding datasets used in ML experi-
ments, tasks, implementations and related hyper-parameters, experiment
executions, their conﬁguration settings and evaluation results, code note-
books and repositories, algorithms, publications, models, scientists, and
practitioners.
This resource provides a large-scale KG built from diverse sources related to
ML pipelines descriptions, datasets attributes, and software implementations,
accompanied by novel ML concepts taxonomies. MLSea provides a resource for
sharing ML knowledge, potentially supporting the ML community in experi-
ment documentation and reproducibility. This resource can be leveraged by ML
and semantic web researchers and practitioners to discover ML workﬂows and
metadata from a large source of ML experiments, conduct analyses and draw
conclusions over ML experiments and their results, support ML recommendation
systems, and complement Automated ML (AutoML) software systems.

180 I. Dasoulas et al.
In the next sections, we discuss motivating examples leading to the develop-
ment of this resource (Sect. 2), related work (Sect. 3), the MLSO and MLST
(Sect.4), the construction process and use cases of MLSea-KG (Sect.5), the
potential impact of our resource (Sect. 6), and future work (Sect.7).
2 Motivating Examples
Currently, the acquisition and discovery of multifaceted ML information require
users to browse diﬀerent ML repositories and platforms, where data are frag-
mented and disconnected from each other. We provide two motivating examples:
Example 1. Find a dataset & its relevant code notebooks & scientiﬁc papers.
A user may search for the image dataset “CIFAR-10”
1 in OpenML [46], view its
statistics and ML tasks deﬁned on it. Yet, conducting a sole search on OpenML
would not uncover the ML code notebooks on Kaggle [34] for this dataset2 which
can assist the users in programming their own ML projects. More, the user would
not ﬁnd scientiﬁc papers that introduced or referenced this dataset, as the ones
i n c l u d e di nP a p e r sw i t hC o d e3, accompanied with code repositories. Such papers
would enable the users to understand the scientiﬁc questions that can be tested
with the dataset and the details of the ML pipeline. To gather information on
various aspects of the ML process related to a speciﬁc dataset, multiple searches
across diﬀerent online repositories are needed.
Example 2. Find a pipeline & its scientiﬁc papers, algorithms & parameters. A
user may search for implementations of the “Bagging” ensemble learning method
in Papers with Code
4 and discover related scientiﬁc papers along with algorithms
they may leverage. However, there also exist implementations in OpenML using
this method that additionally provide hyper-parameters they are using, their
descriptions and values
5. The hyper-parameters can help users understand the
conﬁgurations they would have to make and their diﬀerent options when imple-
menting this kind of pipeline.
3 Related Work
Semantic web technologies are regularly used to support data mining and ML
systems in diﬀerent stages of their pipeline [ 6,56]. ML systems leverage large
knowledge graphs (KGs) to enhance their performance [8] and provide explana-
tions regarding the models’ decisions [31], taking advantage of the semantics and
relationships captured within the KGs. In addition, semantic web technologies
1 https://www.openml.org/d/40927.
2 https://www.kaggle.com/datasets/pankrzysiu/cifar10-python/code.
3 https://www.cs.toronto.edu/~kriz/learning-features-2009-TR.pdf .
4 https://paperswithcode.com/paper/bagging-provides-assumption-free-stability .
5 https://www.openml.org/f/2058.

MLSea: A Semantic Layer for Discoverable Machine Learning 181
are regularly deployed to model ML pipelines, their diﬀerent stages and compo-
nents [16,37,48,54], in an eﬀort to describe and document the ML lifecycle and
the rich metadata that are associated with it.
Knowledge Graphs. Researchers have used semantic representations to bet-
ter track, describe, and encode ML pipelines. In Bosch [72], formally encoded
ML knowledge and solutions are translated to executable scripts, for external
systems to leverage. SemML [73] enables the reuse and generalisation of ML
pipelines for condition monitoring relying on ontology templates for ML task
negotiation and data and feature annotation. Venkataramanan et al. [69]
propose a knowledge-infused recommender system that utilizes metadata of exe-
cuted ML pipelines from open repositories to recommend pipelines based on the
users’ queries. AssistML [70] collects and pre-processes metadata of existing
ML solutions, to recommend alternatives for ML implementations. Regarding
the tracking of ML publications, Linked Papers with Code [18]i saK G
that provides information about ML publications from Papers with Code [ 50]
with related metadata such as their datasets, tasks, and evaluations. Similarly,
SWeMLS-KG [14] is a KG that contains workﬂows and machine-actionable
metadata of 470 papers regarding systems that combine semantic web resources
and ML components. To track ML datasets,KGLac [25] captures metadata and
semantics of datasets to construct a KG that interconnects relevant datasets.
Despite the progress in encoding ML knowledge, there is an absence of large
and openly available resources with ML knowledge from multiple sources and
stages of the ML pipeline due to the complexity and diversity of the various ML
repositories. While domain-speciﬁc KGs are commonly used in other areas, e.g.,
scientiﬁc work organization [4], publication tracking [19], and healthcare [39,57],
the ML ﬁeld lacks large resources describing and inter-connecting ML workﬂows.
Ontologies. Several ontologies have been curated to model ML systems, exper-
iments, and pipelines. EXPO [63], one of the earlier attempts to model scien-
tiﬁc experiments, formalizes the generic concepts of experiment design, method-
ology, and results representation and Exposé [67] focuses on describing ML
experiments and components. OntoDM [48] provides generic representations
and descriptions of the data mining domain and DMOP [37] describes data
mining tasks, data, algorithms, hypotheses, and workﬂows, in an eﬀort to sup-
port decision-making during the data mining process. MEX Vocabulary [16]
and PROV-ML [64
] describe ML experiments, with a strong focus on data
provenance between stages of the ML lifecycle. Task Ontologies [72]m o d e l
executable KGs of ML pipelines, describing pipelines as series of data, methods,
and tasks. ML-Schema [54] is a collaborative eﬀort from the W3C Machine
Learning Schema Community Group6, developed to align existing ML ontolo-
gies and serve as the foundation for more speciﬁc ontologies and applications.
These ontologies provide a solid foundation for describing the fundamental
components within the ML domain. However, they are not integrated with other
domain-speciﬁc ontologies. For instance, they are not aligned with ontologies
about dataset and data catalogs description (e.g., DCAT Vocabulary [40], daQ
6 https://www.w3.org/community/ml-schema/.

182 I. Dasoulas et al.
Ontology [11]), software systems and characteristics (e.g., SWO [41], SDO [22]),
and scientiﬁc works (e.g., FaBiO [ 51]). More, there are no taxonomies cover-
ing pivotal ML concepts, such as algorithms, task types, ﬁelds, evaluation mea-
sures, and dataset characteristics. Whenever such taxonomies do exist within the
ontologies (e.g., MEX Vocabulary [16]), they are limited in scope, and embedded
within the ontologies as class taxonomies. This lack of modularity makes exist-
ing ML taxonomies hard to manage and integrate with other works, while future
updates and additions may require extensive changes to the ontology structure.
ML Platforms. Kaggle [34] is a data science competition platform and online
community of data scientists and ML practitioners. It contains numerous ML
datasets, along with statistical analyses and code used to conduct ML experi-
ments with them. Papers with Code is a community-driven platform which
encompasses ML-related research papers together with their code, datasets,
methods, and evaluation tables. OpenML [46,68] is an open platform for shar-
ing datasets, algorithms, and experiments. It contains datasets along with ML
tasks and pipelines in which they were employed. Additionally, it provides sta-
tistical metadata for the dataset characteristics and pipeline performance, and
experiment conﬁgurations. Hugging Face [27]a n dTensorFlow [65]a r ep o p -
ular platforms for collaboration in ML applications, focusing on the sharing of
ML datasets and development of ML models.
4 The MLS Ontology and Taxonomies
The Machine Learning Sailor Ontology (MLSO) and the Machine
Learning Sailor Taxonomies (MLST) provide a ﬂexible schema to represent
ML pipelines, datasets, implementations, and experiments. They are developed
based on an in-depth analysis of ML experiment-related data from prominent
online repositories, such as OpenML [46], Kaggle [34], and Papers with Code [50].
MLSO extends and enriches existing ontologies, such as ML-Schema [54], DCAT
[40], SDO [ 22], and FaBiO [ 51] to model the ML pipeline. MLST consist of
SKOS [43] controlled taxonomies to organize ML concepts. MLSO and MLST
are available at https://github.com/dtai-kg/mlso/ and published at https://
w3id.org/mlso/. A summary of their namespaces is available at Table1.
Table 1. MLS Modules
Module Description Namespace
MLSO Machine Learning Sailor Ontology http://w3id.org/mlso/
MLSO-DC Dataset Characteristic Taxonomy http://w3id.org/mlso/vocab/dataset_characteristic/
MLSO-FC Feature Characteristic Taxonomy http://w3id.org/mlso/vocab/feature_characteristic/
MLSO-EM Evaluation Measure Taxonomy http://w3id.org/mlso/vocab/evaluation_measure/
MLSO-EP Estimation Procedure Taxonomy http://w3id.org/mlso/vocab/estimation_procedure/
MLSO-LM Learning Method Taxonomy http://w3id.org/mlso/vocab/learning_method/
MLSO-ALGO Algorithm Taxonomy http://w3id.org/mlso/vocab/ml_algorithm/
MLSO-F Machine Learning Field Taxonomy http://w3id.org/mlso/vocab/ml_ﬁeld/
MLSO-TT Task Type Taxonomy http://w3id.org/mlso/vocab/ml_task_type/

MLSea: A Semantic Layer for Discoverable Machine Learning 183
4.1 MLS Development Methodology and Maintenance
The development of MLSO and MLST follows the Linked Open Terms (LOT)
methodology [52]. The four major stages of LOT are: Requirements Speci-
ﬁcation, Implementation, Publication and Maintenance. We deﬁned the
ontology requirements based on the scope of the ontology, i.e. the discovery of
ML knowledge from diverse platforms. The ontology was conceptualized using
the draw.io [13] diagram generation tool and implemented in OWL2 [42]u s i n g
Protegé [45]. To evaluate the ontology, SPARQL [24] queries
7 and the OOPS!
validator [53] are used and its documentation is generated with Widoco [21].
Availability and Maintenance. For at least a ten-year period, KU Leuven
will maintain the ontology and taxonomies with new requirements, error correc-
tions, and gathering of recommendations, using the GitHub issue tracker of the
ontology repository8, where everyone can contribute and raise issues. We antic-
ipate that this collaborative approach will foster the creation of a community
around the ontology, that will take part in the ontology’s further growth and
development. Since we plan to add new knowledge and data from more plat-
forms to our system, such as Hugging Face [ 27], the ontology will need to be
carefully revised as newer versions will be published.
Fig. 1. MLSO and MLST Overview (Color ﬁgure online)
4.2 MLSO: The Machine Learning Sailor Ontology
The ontology’s elements are grouped into four components: the Dataset com-
ponents representing ML datasets along with their statistical and generic meta-
data; the ML Pipeline components representing the fundamental concepts of
7 https://github.com/dtai-kg/MLSea-KGC/tree/main/sparql_examples.
8 https://github.com/dtai-kg/MLSO.

184 I. Dasoulas et al.
the ML pipeline, such as the ML task and experiment; the Software compo-
nents, representing software characteristics of the described implementations;
and the Scientiﬁc Work components , representing ML peer-reviewed pub-
lications. The primary focus of the ontology lies in interconnecting these com-
ponents to create a cohesive framework for modeling ML processes, extending
already established standards. MLSO’s core elements are shown in Fig.1.
Dataset Components (yellow in Fig. 1) represent the concepts inherent to
datasets utilized in ML processes. They describe the structural composition of
datasets, along with other traits such as generic and statistical metadata. These
concepts include: datasets, catalogs, data services, dataset distributions, formats,
modalities, characteristics, dataset features, and feature characteristics.
To articulate the generic traits of dataset entities, such as their language,
creators, and licences, we reuse the following general-purpose ontologies: the
Data Catalog (DCAT), Friend Of A Friend (FOAF) [ 7], Provenance Ontology
(PROV-O) [38], and Dublin Core (DC) [71]. While these ontologies capture the
generic aspects of datasets, they do not provide statistical metadata crucial for
ML processes or for deﬁning ML tasks relevant to the datasets. To address this
limitation we align DCAT and ML-Schema, and use ML-Schema to describe data
qualities of datasets and dataset features, as well as ML tasks based on datasets.
Moreover, for the description of dataset formats, we reuse the extensive data
formats collection found in the EDAM Ontology [32].
While OpenML provides a means to represent data qualities
9, the existing
representation is limited to a list of literals published on OpenML. To bridge
this gap, we introduce 2 SKOS taxonomies: the Dataset Characteristic Tax-
onomy and the Feature Characteristic Taxonomy (Sect.4.3). These taxonomies
classify dataset and feature characteristics, respectively, providing a standard-
ized approach to express the qualities of datasets and their features.
We introduce new properties to connect datasets (mlso:hasVariant), datasets
with their features ( mlso:hasDefaultTargetFeature and mlso:hasIdFeature)a n d
their modality (mlso:hasModality), and data qualities with the introduced data
quality types (mlso:hasDataCharacteristicType). We also introduce new proper-
ties to connect datasets and ML implementations that leverage them and models
trained on these datasets (mlso:hasRelatedImplementation, mlso:trainedOn).
Last, the reused ontologies do not include a way to connect datasets with
peer-reviewed publications that reference them or software that leverages them.
Therefore, we added new properties to link datasets with relevant publications
(mlso:hasScientiﬁcReference ) and software using them (mlso:hasRelatedSoftware),
such as code notebooks or large-scale software applications. We also include other
dataset attributes, e.g., their data loader locations (mlso:hasDataLoaderLocation),
as well as the cache format of their platform version (mlso:hasCacheFormat).
ML Pipeline Components (blue in Fig.1) serve as a comprehensive represen-
tation of the fundamental concepts integral to the ML pipeline. They focus on
describing the characteristics of ML experiments, their hyper-parameters, set-
9 https://www.openml.org/search?type=measure.

MLSea: A Semantic Layer for Discoverable Machine Learning 185
tings, and evaluation results. The concepts include: ML tasks, runs, implemen-
tations, implementation characteristics, algorithms, hyper-parameters, hyper-
parameter settings, experiments, models, model evaluations, model character-
istics, evaluation measures, evaluation speciﬁcations, and evaluation procedures.
We reuse and extend ML-Schema to represent the fundamental concepts of
ML pipelines, such as the tasks they address, their implementations and execu-
tions, and their inputs and outputs. While ML-Schema captures the fundamental
concepts of the ML process, it does not include the details and characteristics
of software used in these processes. To address this, we align ML-Schema and
SDO, an ontology for describing software components, including their metadata
and their inputs, outputs and variables. SDO enriches the representations of ML
pipelines with their software characteristics and requirements.
ML-Schema oﬀers descriptions of estimation procedures, evaluation mea-
sures, algorithms, and tasks. However, these are represented as literals with-
out systematic classiﬁcation or categorization. To more eﬃciently classify and
document these concepts, we introduce 4 SKOS taxonomies; the Estimation Pro-
cedure, Evaluation Measure, Task Type, and Algorithm Taxonomies (Sect.4.3),
allowing for the classiﬁcation of estimation procedures, evaluation measures,
algorithms, and tasks, enriching the ontology with a categorized representation.
More, we introduce 2 new taxonomies: the Machine Learning Field Taxonomy
to classify ML ﬁelds of research that tasks belong to and the Learning Method
Taxonomy to categorize learning methods used in ML pipelines (Sect.4.3).
To explicitly assign types and categories to ML-Schema classes, we intro-
duce new properties linking ML tasks to ML task categories (mlso:hasTaskType)
and ML ﬁelds they relate to (mlso:relatedToField). We link ML algorithms with
algorithm types (mlso:hasAlgorithmType) and types of ML learning method they
may include ( mlso:hasLearningMethodType). We also link evaluation measures
and estimation procedures with their types ( mlso:hasEvaluationProcedureType)
and evaluation types (mlso:hasEvaluationMeasureType. Last, we introduce a new
property (mlso:hasScientiﬁcReference ) to link ML models or pipelines and the
scientiﬁc works related to them or referencing them.
Software Components (orange in Fig. 1) encapsulate fundamental software
concepts related to the execution of ML experiments, the settings and the
requirements they have. These concepts include: software, software conﬁguration,
and software source code. We reuse SDO to describe the software characteris-
tics and requirements of software used in ML pipelines. MLSO leverages these
already established descriptions to augment the linkage between ML experiments
and their software components. We introduce new properties to interconnect
software components with scientiﬁc works (mlso:hasScientiﬁcReference ), datasets
(mlso:hasRelatedSoftware), and with ML ﬁelds of research (mlso:relatedToField).
Scientiﬁc Work Components (pink in Fig.1) represent peer-reviewed publi-
cations related to developments in the ﬁeld of ML. We reuse the FaBiO and
FOAF vocabularies to describe publications, authors. MLSO extends FaBiO
to connect ML publications with datasets they leverage or reference, ML
experiments they conduct, models they create and publish, and the soft-

186 I. Dasoulas et al.
ware they use. We introduce new properties to enrich the ML research
works descriptions, connecting them with datasets and software they leverage
(mlso:hasScientiﬁcReference , mlso:hasRelatedSoftware), and ML ﬁelds of research
(mlso:relatedToField).
4.3 MLST: Machine Learning Sailor Taxonomies
MLSO is complemented by MLST, a series of SKOS taxonomies, formulated as
RDF vocabularies, to provide a ﬂexible and standardized framework for man-
aging large controlled collections of ML knowledge. These taxonomies serve as
comprehensive thesauri, oﬀering a structured overview of essential ML concepts.
The taxonomies were developed by systematically studying and integrating
data from three primary sources. Firstly, data were gathered from online ML
repositories that provide organised data collections, such as the OpenML data
qualities collection
10 and the Papers with Code ML methods collection 11. Sec-
ondly, information was sourced from smaller pre-existing collections formalized
as vocabularies, such as the MEX vocabulary [ 16]. Lastly, categorizations were
extracted from peer-reviewed publications that systematically consolidate ML
knowledge, predominantly from ML surveys and scholarly works.
MLST include the following 8 ML-focused taxonomies:
(i) Dataset Characteristic Taxonomy , a collection of qualities used to
characterize datasets (e.g., entropy, number of classes). It is based on
the OpenML data qualities collection(see footnote 10) and contains 127
dataset characteristics.
(ii) Feature Characteristics Taxonomy , a collection of qualities to
describe dataset features (e.g., data-type, maximum value). It is based
on the OpenML data qualities collection(see footnote 10) and contains 55
feature characteristics.
(iii) Evaluation Measure Taxonomy, a collection of measures for the evalu-
ation of ML experiments. It is based on the OpenML evaluation measures
collection
12 and contains 86 evaluation measures (e.g., accuracy, recall).
(iv) The Estimation Procedure Taxonomy , a collection of data-splitting
techniques to evaluate ML models based on the OpenML evaluation pro-
cedures collection13 containing 5 estimation procedures (e.g., cross valida-
tion, holdout).
(v) The Learning Method Taxonomy , a collection of methods of learning
and training in ML, based on the learning approach and the type of data
they input and output. The taxonomy reuses MEX vocabulary learning
method classes, learning methods found in Papers with Code ML tasks
and literature review [59]. It contains 33 learning methods (e.g., supervised
learning, transfer learning).
10 https://www.openml.org/search?type=measure&measure_type=data_quality.
11 https://paperswithcode.com/methods.
12 www.openml.org/search?type=measure&measure_type=evaluation_measure.
13 www.openml.org/search?type=measure&measure_type=estimation_procedure.

MLSea: A Semantic Layer for Discoverable Machine Learning 187
Fig. 2. MLSea-KG Construction Process Overview
(vi) The Algorithm Taxonomy, a collection of 2321 algorithms used in dif-
ferent stages of the ML process (e.g., Adam, Dropout). The taxonomy
re-uses MEX vocabulary algorithm classes, the Paper with Code methods
collection(see footnote 11), and ML surveys that organize ML algorithms
from diverse ML ﬁelds [1,3,5,9,17,20,36,44,55,58,60–62,66].
(vii) The Machine Learning Field Taxonomy , a collection of areas of study
in the ML domain. It is based on MEX vocabulary ML context classes
and literature review [ 33] and contains 30 ﬁelds (e.g., computer vision,
bioinformatics).
(viii) The Task Type Taxonomy , a collection of 1875 ML task types, deﬁned
based on the problem they try to solve (e.g., object detection, colorization).
The taxonomy is based on MEX vocabulary ML context classes and task
types found in OpenML tasks and Papers with Code datasets, methods,
and publications.
The modular design and availability of the taxonomies aim to empower the
ML community, allowing researchers and practitioners to propose new entries,
suggest modiﬁcations, and redeﬁne the hierarchy of terms via GitHub issues.
This collaborative approach aims to sustain a resource that evolves in line with
the dynamic landscape of ML, ensuring the taxonomies remain up-to-date.
5 MLSea-KG: Construction, Publication and Usage
We applied ourMLSO ontology to createMLSea-KG, a KG for discovering ML
data containing more than 1.44 billion triples (Fig.2). We discuss the population
and update methodology we follow for declaratively constructing and preserving
MLSea-KG which is available at http://w3id.org/mlsea-kg. In this section, we
showcase MLSea-KG’s key statistics, availability and usage examples.

188 I. Dasoulas et al.
5.1 Knowledge Graph Construction Process
The KG construction process starts with the data collection step ( Step 1 ,
Fig.2) for each of the examined publicly available platforms. We collectedKag-
gle’s[34] data as CSV ﬁles via the Meta Kaggle dataset [35], a public repos-
itory containing metadata about Kaggle datasets, kernels, users, and competi-
tions, updated on a daily basis. For OpenML [46], we iteratively collected all
OpenML datasets, tasks, ﬂows, runs, and their related metadata, in the form
of Pandas [47] dataframes, through the OpenML Python API service14.F o r
Papers with Code [50], we collected the platform’s data, as JSON ﬁles, via
the platform’s public dump ﬁles15 that contain metadata regarding papers, code
repositories, methods, and datasets of the platform. To prepare the collected
data, pre-processing modules ﬁlter out problematic data, such as faulty OpenML
URLs, new-line characters in literals, and non-escaped backslashes, as well as ML
pipeline-unrelated data, such as Kaggle forum messages, as we do not include
platform-speciﬁc data to the MLSea-KG that are not directly related to ML.
The RDF graph is constructed by applying the MLSO and MLST to the
retrieved data. We leverage the RDF Mapping Language (RML) [12,30]t om a p
the heterogeneous data (Pandas DataFrames from OpenML, CSV ﬁles from Kag-
gle and JSON ﬁles from Papers with Code) to RDF triples. To deﬁne the RML
mapping rules, we leverage the human-friendly serialization YARRRML [26]a n d
the Yatter [29] tool which converts YARRRML mapping rules to RML rules.
To eﬃciently process large data sources, such as the Meta Kaggle and the
Papers with Code metadata datasets, with RML processors we extract a batch
of the complete initial dataset each time (Step 2 , Fig.2). We employ platform-
speciﬁc custom sampling strategies to ensure that pertinent data are consistently
grouped together within each batch. For example, when constructing an RDF
graph from a batch of Kaggle datasets metadata, we also extract related Kaggle
code notebooks metadata for code notebooks based on the datasets of the batch,
and as a result contain useful information for the datasets’ RDF graph.
We leverage Morph-KGC [2] and its extension for in-memory RDF gener-
ation [10] to declaratively generate the RDF triples for each extracted batch
(Step 3 , Fig. 2). The generated RDF batches are compressed into .gz archives,
to facilitate data management and reduce the total storage. Each RDF batch is
then imported into our Virtuoso triple store [15], hosted on an Ubuntu 22.04.3
LTS server with Intel(R) Xeon(R) CPU E5-2650 v2 and 128 GB RAM (Step 4 ,
Fig.2). The 3 RDF graphs, 1 for each platform, comprise the MLSea-KG.
14 https://www.openml.org/apis.
15 https://paperswithcode.com/about.

MLSea: A Semantic Layer for Discoverable Machine Learning 189
Table 2. MLSea-KG core entities, number of instances & triples per dataset & type.
Entity Type Instance Count Triples Count
OpenML Kaggle PwC Total OpenML Kaggle PwC Total
Datasets 5.4K 277.4K 11.1K 295.9K 49.7M 4.2M 163.2K 54.1M
Tasks 47.2K – 2.1K 49.3K 642.3K – 8.5K 650.8K
Pipelines 16.7K – 26.9K 43.6K 1.3M – 1.2M 2.6M
Algorithms – – 2.1K 2.1K – – – 19.4K
Runs 10.1M – 26.9K 10.1M 1.36B – 524.7K 1.36B
Models – – 26.9K 26.9K – – 214.6K 214.6K
Notebooks – 940.4K – 940.4K – 9.3M - 9.3M
Repositories – – 146.2K 14.2K – – 955.2K 955.2K
Publications 308 – 407.4K 407.4K 1.2K – 6.8M 6.8M
Agents 1.4K 360.1K 433.5K 407K 4.3K 1.0M 1.3M 2.3M
Total 10.1M 1.5M 1.0M 12.6M 1.41B 14.5M 11.1M 1.44B
Continuous Integration. MLSea-KG is updated using an automatic proce-
dure. The updated Meta Kaggle dataset and the Papers with Code dump ﬁles are
downloaded and compared with their previous versions to identify new entries,
while the latest data of the OpenML are downloaded through its API. Then, the
same KG construction process is followed to update MLSea-KG.
Statistics of MLSea-KG. As of November 2023, MLSea-KG consists of 5.4K
datasets, 47.2K ML tasks, 16.7 ﬂows (descriptions of ML pipelines), 10.1M runs
(executions, settings, and evaluations of ML experiments), 308 publications, and
1.4K agents (scientists and practitioners) from OpenML; 277K datasets, 940K
ML code notebooks and 360.1K agents from Kaggle; 11.1K datasets, 2.1K ML
tasks, 2.1K algorithms, 407K ML publications, 146K ML code repositories, 26.9K
ML models, accompanied by experiment metadata and related evaluations, and
433K researchers from Papers with Code, all complemented with rich metadata.
A total count of the instances of MLSea-KG, along with the total number of
triples by instance, is exhibited in Table 2. Along with all metadata, the total
triples count of MLSea-KG exceeds 1.44 billion, with the majority of the RDF
triples originating from OpenML, which contains a plethora of ML-related meta-
data, from detailed characteristics for each dataset to numerous ML experiment
conﬁguration settings and results. Kaggle and Papers with Code focus more on
generic metadata and can be, thus, represented with less RDF triples.
Availability and Maintenance. Our resource’s landing page ( http://w3id.
org/mlsea) provides pointers to the public SPARQL endpoint of MLSea-KG
(http://w3id.org/mlsea-kg), the Zenodo repository for the RDF snapshots of
MLSea-KG, and the GitHub repository with the RML mapping rules for KG
construction and the source code employed for metadata collection and sam-
pling, and KG construction. The webpage summarizes how MLSea-KG was con-

190 I. Dasoulas et al.
structed leveraging MLSO and MLST. For at least a ten-year period, KU Leu-
ven will maintain MLSea-KG, applying the continuous integration process on a
monthly basis to incorporate the latest updates from all ML repositories. The
KG population scripts and RML mapping rules will also be regularly updated.
5.2 Use Case Examples
The MLSea-KG allows users to search for ML datasets, tasks, implementations,
models, experiments, software, and scientiﬁc works. They can view the charac-
teristics of these components and navigate through their intricate relationships.
The search over the data of the diﬀerent platforms is facilitated as a user can
ﬁnd all relevant information with a single query. In this section, we look back
at the motivating examples (Sect. 2) and demonstrate how the users can take
advantage of MLSea to address the same use cases.
Example 1. Find a dataset & its relevant code notebooks & scientiﬁc papers.
In this example, a user searches for a dataset, its code notebooks, and scientiﬁc
papers over the 3 platforms simultaneously, as it was described in Sect.2.
As opposed to this manual task, a user can retrieve the same information
by leveraging MLSea. The SPARQL query of this search overMLSea-KG for the
“CIFAR-10” is shown in Listing 5.1 and an excerpt of the results is shown in
Table3. The complete set of results is returned within 12 secs.
Listing 5.1. Query for CIFAR-10 dataset locations, tasks, code and publications.
PREFIX mlso : <http://w3id.org/ mlso />
PREFIX mls : <http://www.w3.org/ns/ mls #>
#... dcterms , rdfs , dcat , prov , schema and skos are omitted
SELECT ?datasetTitle , ?datasetLocation , ( GROUP_CONCAT ( DISTINCT COALESCE
(?omlTask , ? pwcTask); separator =’,\n’) AS ?task), ( GROUP_CONCAT ( DISTINCT
COALESCE (?codeNotebook , ?codeRepo); separator =’,\n’) AS ?code),
( GROUP_CONCAT ( DISTINCT ?publication; separator =’,\n’) AS ?introducedIn)
WHERE {
?dataset a mls :Dataset;
dcat :landingPage ?datasetLocation; dcterms :title ? datasetTitle.
OPTIONAL {?dataset dcterms :description ? label}
OPTIONAL {?dataset rdfs :label ?label}
FILTER ( CONTAINS (?label, "CIFAR -10")|| CONTAINS ( LCASE (?label), " cifar -10"))
OPTIONAL {?dataset mlso :hasRelatedSoftware ? softwareID.
?softwareID schema :codeRepository ?codeNotebook.}
OPTIONAL {?taskId mls :definedOn ?dataset; prov :atLocation ?omlTask.}
OPTIONAL {?dataset mlso :hasTaskType ?taskType.
?taskType skos :prefLabel ?pwcTask.}
OPTIONAL {?dataset mlso :hasScientificReference ? publicationID.
?publicationID dcterms :source ? publication.}
OPTIONAL {?dataset mlso :hasScientificReference ? publicationID.
?publicationID mlso :hasRelatedSoftware ? softwareID.
?softwareID schema :codeRepository ? codeRepo.}
} GROUP BY ?datasetTitle ?datasetLocation

MLSea: A Semantic Layer for Discoverable Machine Learning 191
Table 3. Query results for CIFAR-10 dataset locations, tasks, code & publications.
dataset
Title
dataset
Location
task code introducedIn
CIFAR-FS paperswithcode.com/dataset/cifar-fs Few-Shot Image
Classiﬁcation, ...
github.com/bertinetto/r2d2 arxiv.org/pdf/1805.08136v3
CIFAR-10 kaggle.com/datasets/ayush1220/cifar10 – kaggle.com/code/alphapii/knn-cvpr –
CIFAR_10
small
api.openml.org/data/v1/download/16797612/
CIFAR_10_small.arff
openml.org/t/294086 – –
Listing 5.2. Query for Bagging implementations, publications & hyper-parameters.
PREFIX mls : <http://www.w3.org/ns/ mls #>
#... dcterms , rdfs , dcat , prov , schema and skos are omitted
SELECT ( STR ( COALESCE (?label, ? title)) AS ?implementation),
( GROUP_CONCAT ( DISTINCT ?publication; separator =‘,\n’) AS ?publications),
( GROUP_CONCAT ( DISTINCT ?algorithm; separator =‘,\n’) AS ?algorithms),
( GROUP_CONCAT ( DISTINCT ?hyperP; separator =‘,\n’) AS ?hyperParameters)
WHERE {
{?implemId a mls :Implementation; rdfs :label ?label.
FILTER ( CONTAINS ( LCASE (?label), ‘‘bagging ’ ’))}
UNION {?implemId a mls :Implementation; dcterms :description ? desc;
dcterms :title ?title. FILTER ( CONTAINS ( LCASE (?desc), "bagging"))}
OPTIONAL {?pubId mlso :hasRelatedImplementation ?implemId;
rdf:type mlso :ScientificWork; dcterms :source ? publication.}
OPTIONAL {?implemId mls :implements ? algoId. ?algoId rdfs :label ? algorithm.}
OPTIONAL {?implemId mls :hasHyperParameter ? hyperPID.
?hyperPID dcterms :description ?hyperP_desc; dcterms :title ? hyperP_title.
BIND ( CONCAT ( STR (?hyperP_title ),‘‘: ’’, str (?hyperP_desc)) as ?hyperP)}
} GROUP BY ?label ?title
Example 2. Find a pipeline & its papers, algorithms & parameters. In this exam-
ple, a user manually searches for a pipeline over the 3 platforms to ﬁnd scientiﬁc
papers, algorithms, and hyper-parameters, as described in Sect. 2.
As opposed to this manual task, a user can retrieve the same information by
leveraging MLSea. The SPARQL query of this search over MLSea-KG is shown
in Listing 5.2, where publications, algorithms, and hyper-parameters about the
popular “Bagging” ensemble method are retrieved. An excerpt of the query
results is shown in Table4; the complete results are returned within 6 secs.
6 Impact of the Resource
This resource can be of interest and have impact for the ML and the Semantic
Web community oﬀering abundant prospects for future research and adoption.
Practitioners can immediately use it for ML artifacts search, such as dataset
Table 4. Query results for Bagging implementations, publications & hyper-parameters.
implementation publications algorithms hyperParameters
Internal node bagging arxiv.org/pdf/1805.00215v5.pdf Dropout –
weka.Bagging_REPTree(22) – – L: Maximum tree depth, ...
BagBERT arxiv.org/pdf/2111.05808v1.pdf Adam, BERT, ... –

192 I. Dasoulas et al.
and model search, while researchers can leverage it for analyzing ML metadata,
discover ML insights and trends, and develop ML recommendation systems.
Searchability. MLSea’s immediate impact lies on the ML knowledge discov-
ery opportunities it facilitates with the MLSea-KG and the MLST that organize
ML knowledge. Researchers and practitioners can now navigate the prominent
repositories (OpenML, Kaggle, and Papers with Code), by formulating precise
SPARQL queries and immediately get integrated answers. They can retrieve
ML datasets and view their statistical and feature characteristics, ML pipelines,
their inputs, hyper-parameter settings and results, ML tasks and related imple-
mentations that attempt to solve them, ML peer-reviewed publications, code
notebooks, and ML models, precisely tailored to their needs.
This semantic layer has the potential to accelerate the progress of ML projects
by facilitating more eﬃcient searches through previous works and enabling their
reuse. For example, users can reuse or augment datasets, identify optimal hyper-
parameter settings for a speciﬁc task or leverage pre-trained models, via transfer
learning. Likewise, the integration of the taxonomies (MLST)w i t ht h eMLSea-KG
can enhance the search capabilities overMLSea-KG. For instance, users can query
MLSea-KG for a task with a speciﬁc type from the ML Task Type taxonomy.
MLSea does not only facilitate individual platform searches, but also enables
combined searches over platforms. The diverse data that the resource provides
oﬀer new capabilities for fostering a more comprehensive understanding of ML
experiments, by connecting fragmented information. For instance, discovering a
dataset from Papers with Code and subsequently locating relevant code note-
books in Kaggle enhances cross-platform connectivity, promoting a deeper and
more complete understanding of the available ML resources.
Reproducibility.Utilizing MLSea to model and store ML pipelines signiﬁcantly
enhances documentation and has the potential to increase the repeatability,
reproducibility, traceability, and explainability of ML pipelines. It promotes a
standardized approach to sharing experiments, enhancing knowledge exchange
among practitioners and interoperability amongst ML online repositories. Simul-
taneously, MLST function as a dynamic thesaurus, oﬀering a structured reposi-
tory for organizing ML knowledge in a modular way.
Data Analysis. By leveraging MLSea-KG, new data analysis and insights
opportunities emerge. Through innovative techniques, such as graph embed-
dings, users can derive signiﬁcant insights, such as hidden patterns and trends,
from connections prevalent in the graph. Users can investigate relationships
between dataset characteristics, the impact of diﬀerent hyper-parameter set-
tings on model performance, or discover correlations between speciﬁc algorithms
and successful experiments. These potential explorations can lead to a better
understanding of best practices, optimizations, and success factors within ML
projects.
Recommendations. MLSea provides an extensive data source for ML recom-
mendation systems to be based on by harnessing past successful experiments
and user requirements to recommend suitable datasets, pre-trained models,

MLSea: A Semantic Layer for Discoverable Machine Learning 193
hyper-parameter settings, and algorithms. These recommendation systems could
complement AutoML systems in providing solutions to ML practitioners. For
instance, a recommendation system could analyze experiment outcomes, and
propose related datasets, eﬀective models or algorithms for a given context.
7 Conclusions and Future Work
This work leverages semantic web technologies to meticulously model diverse
ML information and encompass a large corpus of ML datasets, experiments,
software and scientiﬁc publications. The introduced MLSO and MLST extend
and combine past ontologies and W3C recommendations to provide a versatile
schema that describes diﬀerent facets of the ML process.
We applied this schema to 3 prominent ML platforms (OpenML, Kaggle, and
Papers with Code), using their metadata related to ML processes to generate
RDF graphs, ultimately creating MLSea-KG, a large-scale KG for ML, boasting
over 1.44 billion RDF triples. We discuss MLSea-KG’s construction and update,
its characteristics, use cases, and potential impact for the ML community, high-
lighting its usefulness for practitioners and researchers on a variety of levels.
In the future, we plan to continue updating the resources, integrating the
latest data of the examined platforms. We also plan to extend our resources,
by modeling and incorporating metadata from additional ML repositories, thus
encompassing an even broader picture of the ML landscape. Furthermore, we aim
to enhance speciﬁcity in representing deep learning components and experiments,
fostering a more detailed layer of deep learning semantic descriptions. Finally,
we intend to explore further potential of our resource, examining its use as a
source for data analysis, insights discovery, and ML recommendation systems.
Acknowledgements. This research was partially supported by Flanders Make (REX-
PEK project), the strategic research centre for the manufacturing industry and the
Flanders innovation and entrepreneurship (VLAIO – KG3D project).
References
1. AlMahamid, F., Grolinger, K.: Reinforcement learning algorithms: an overview and
classiﬁcation. In: 2021 IEEE Canadian Conference on Electrical and Computer
Engineering (CCECE), pp. 1–7 (2021). https://doi.org/10.1109/CCECE53047.
2021.9569056
2. Arenas-Guerrero, J., Chaves-Fraga, D., Toledo, J., Pérez, M.S., Corcho, O.: Morph-
KGC: scalable knowledge graph materialization with mapping partitions. Semant.
Web (2022). https://doi.org/10.3233/SW-223135
3. Arulkumaran, K., Deisenroth, M.P., Brundage, M., Bharath, A.A.: Deep reinforce-
ment learning: a brief survey. IEEE Signal Process. Mag. 34(6), 26–38 (2017).
https://doi.org/10.1109/MSP.2017.2743240
4. Auer, S., Kovtun, V., Prinz, M., Kasprzik, A., Stocker, M., Vidal, M.E.: Towards
a knowledge graph for science. In: Proceedings of the 8
th International Conference
on Web Intelligence, Mining and Semantics, pp. 1–6 (2018). https://doi.org/10.
1145/3227609.3227689

194 I. Dasoulas et al.
5. Bielza, C., Larrañaga, P.: Discrete Bayesian network classiﬁers: a survey. ACM
Comput. Surv. 47(1) (2014). https://doi.org/10.1145/2576868
6. Breit, A., et al.: Combining machine learning and semantic web: a systematic map-
ping study. ACM Comput. Surv.55(14s) (2023). https://doi.org/10.1145/3586163
7. Brickley, D., Miller, L.: FOAF Vocabulary Speciﬁcation 0.99 (2014).http://xmlns.
com/foaf/spec/
8. Castellano, G., Digeno, V., Sansaro, G., Vessio, G.: Leveraging knowledge graphs
and deep learning for automatic art analysis. Knowl.-Based Syst. 248, 108859
(2022). https://doi.org/10.1016/j.knosys.2022.108859
9. Charbuty, B., Abdulazeez, A.: Classiﬁcation based on decision tree algorithm for
machine learning. J. Appl. Sci. Technol. Trends 2(01), 20–28 (2021). https://doi.
org/10.38094/jastt20165
10. Dasoulas, I., Chaves-Fraga, D., Garijo, D., Dimou, A.: Declarative RDF construc-
tion from in-memory data structures with RML. In: Proceedings of the 4th Interna-
tional Workshop on Knowledge Graph Construction co-located with 20th Extended
Semantic Web Conference ESWC 2023, vol. 1613, p. 0073 (2023)
11. Debattista, J., Lange, C., Auer, S.: daQ, an ontology for dataset quality informa-
tion. In: LDOW (2014)
12. Dimou, A., Vander Sande, M., Colpaert, P., Verborgh, R., Mannens, E., Van de
Walle, R.: RML: a generic language for integrated RDF mappings of heterogeneous
data. In: Bizer, C., Heath, T., Auer, S., Berners-Lee, T. (eds.) Proceedings of the 7
th
Workshop on Linked Data on the Web. CEUR Workshop Proceedings, vol. 1184.
CEUR (2014)
13. Draw.io: Security-ﬁrst diagramming for teams.https://www.drawio.com. Accessed
28 Nov 2023
14. Ekaputra, F.J., et al.: Describing and organizing semantic web and machine learn-
ing systems in the SWeMLS-KG. In: Pesquita, C., et al. (eds.) The Semantic Web.
ESWC 2023. LNCS, vol. 13870, pp. 372–389. Springer, Cham (2023). https://doi.
org/10.1007/978-3-031-33455-9_22
15. Erling, O., Mikhailov, I.: Virtuoso: RDF support in a native RDBMS. In: de Vir-
gilio, R., Giunchiglia, F., Tanca, L. (eds.) Semantic Web Information Management,
pp. 501–519. Springer, Berlin, Heidelberg (2009). https://doi.org/10.1007/978-3-
642-04329-1_21
16. Esteves, D., et al.: MEX vocabulary: a lightweight interchange format for machine
learning experiments. In: Proceedings of the 11
th International Conference on
Semantic Systems, pp. 169–176. SEMANTICS ’15, Association for Computing
Machinery, New York, NY, USA (2015).https://doi.org/10.1145/2814864.2814883
17. Fahad, A., et al.: A survey of clustering algorithms for big data: taxonomy and
empirical analysis. IEEE Trans. Emerg. Top. Comput. 2(3), 267–279 (2014).
https://doi.org/10.1109/TETC.2014.2330519
18. Färber, M., Lamprecht, D.: Linked papers with code: the latest in machine learning
as an RDF knowledge graph. In: ISWC 2023 Posters and Demos: 22nd International
Semantic Web Conference, 6–10 November 2023, Athens, Greece (2023). https://
doi.org/10.48550/arXiv.2310.20475
19. Färber, M., Lamprecht, D., Krause, J., Aung, L., Haase, P.: SemOpenAlex: the
scientiﬁc landscape in 26 billion RDF triples. In: Payne, T.R., et al. (eds.) The
Semantic Web – ISWC 2023. ISWC 2023. LNCS, vol. 14266, pp. 94–112. Springer,
Cham (2023). https://doi.org/10.1007/978-3-031-47243-5_6 , https://doi.org/10.
48550/arXiv.2308.03671

MLSea: A Semantic Layer for Discoverable Machine Learning 195
20. Fürnkranz, J., Kliegr, T.: A brief overview of rule learning. In: Bassiliades, N., Got-
tlob, G., Sadri, F., Paschke, A., Roman, D. (eds.) RuleML 2015. LNCS, vol. 9202,
pp. 54–69. Springer, Cham (2015). https://doi.org/10.1007/978-3-319-21542-6_4
21. Garijo, D.: WIDOCO: a wizard for documenting ontologies. In: d’Amato, C., et al.
(eds.) ISWC 2017. LNCS, vol. 10588, pp. 94–102. Springer, Cham (2017).https://
doi.org/10.1007/978-3-319-68204-4_9
22. Garijo, D., Osorio, M., Khider, D., Ratnakar, V., Gil, Y.: OKG-Soft: an open knowl-
edge graph with machine readable scientiﬁc software metadata. In: 15 th Interna-
tional Conference on eScience (eScience), pp. 349–358 (2019). https://doi.org/10.
1109/eScience.2019.00046
23. Gundersen, O.E., Shamsaliei, S., Isdahl, R.J.: Do machine learning platforms
provide out-of-the-box reproducibility? Futur. Gener. Comput. Syst. 126, 34–47
(2022). https://doi.org/10.1016/j.future.2021.06.014
24. Harris, S., Seaborne, A.: SPARQL 1.1 Query Language. Recommendation, World
Wide Web Consortium (W3C), March 2013. https://www.w3.org/TR/sparql11-
query/
25. Helal, A., Helali, M., Ammar, K., Mansour, E.: A demonstration of KGLac: a data
discovery and enrichment platform for data science. Proc. VLDB Endow. 14(12),
2675–2678 (2021). https://doi.org/10.14778/3476311.3476317
26. Heyvaert, P., De Meester, B., Dimou, A., Verborgh, R.: Declarative rules for linked
data generation at your ﬁngertips! In: The Semantic Web: ESWC 2018 Satellite
Events: ESWC 2018 Satellite Events, Heraklion, Crete, Greece, 3–7 June 2018,
Revised Selected Papers 15 (2018)
27. Hugging Face: Hugging Face – The AI community building the future. https://
huggingface.co. Accessed 28 Nov 2023
28. Hutson, M.: Artiﬁcial intelligence faces reproducibility crisis (2018). https://doi.
org/10.1126/science.359.6377.725
29. Iglesias-Molina, A., Chaves-Fraga, D., Dasoulas, I., Dimou, A.: Human-
Friendly RDF graph construction: which one do you chose? In: Garrigós, I.,
Murillo Rodríguez, J.M., Wimmer, M. (eds.) Web Engineering. ICWE 2023. LNCS,
vol. 13893, pp. 262–277. Springer, Cham (2023). https://doi.org/10.1007/978-3-
031-34444-2_19
30. Iglesias-Molina, A., et al.: The RML ontology: a community-driven modular
redesign after a decade of experience in mapping heterogeneous data to RDF.
In: Payne, T.R., et al. (eds.) The Semantic Web – ISWC 2023. ISWC 2023. LNCS,
vol. 14266, pp. 152–175. Springer, Cham (2023). https://doi.org/10.1007/978-3-
031-47243-5_9
31. Ismaeil, Y., Stepanova, D., Tran, T.K., Saranrittichai, P., Domokos, C., Blockeel,
H.: Towards neural network interpretability using commonsense knowledge graphs.
In: Sattler, U., et al. (eds.) The Semantic Web – ISWC 2022. ISWC 2022. LNCS,
vol. 13489, pp. 74–90. Springer, Cham (2022).https://doi.org/10.1007/978-3-031-
19433-7_5
32. Ison, J., et al.: EDAM: an ontology of bioinformatics operations, types of data and
identiﬁers, topics and formats. Bioinformatics 29(10), 1325–1332 (2013). https://
doi.org/10.1093/bioinformatics/btt113
33. Jordan, M.I., Mitchell, T.M.: Machine learning: trends, perspectives, and
prospects. Science 349(6245), 255–260 (2015). https://doi.org/10.1126/science.
aaa8415
34. Kaggle: Kaggle: Your Machine Learning and Data Science Community. https://
www.kaggle.com. Accessed 28 Nov 2023

196 I. Dasoulas et al.
35. Kaggle: Meta Kaggle - Kaggle’s public data on competitions, users, submis-
sion scores, and kernels. https://www.kaggle.com/datasets/kaggle/meta-kaggle.
Accessed 28 Nov 2023
36. Kaur, J., Madan, N.: Association rule mining: a survey. Int. J. Hybrid Inf. Technol.
8(7), 239–242 (2015)
37. Keet, C.M., et al.: The data mining optimization ontology. J. Web Semant. 32,
43–53 (2015). https://doi.org/10.1016/j.websem.2015.01.001
38. Lebo, T., et al.: PROV-O: The PROV Ontology. Recommendation, World Wide
Web Consortium (W3C), April 2013. https://www.w3.org/TR/prov-o/
39. Li, L., et al.: Real-world data medical knowledge graph: construction and appli-
cations. Artif. Intell. Med. 103, 101817 (2020). https://doi.org/10.1016/j.artmed.
2020.101817
40. Maali, F., Erickson, J.: Data Catalog Vocabulary (DCAT). Recommendation,
World Wide Web Consortium (W3C), January 2014. https://www.w3.org/TR/
vocab-dcat/
41. Malone, J., et al.: The software ontology (SWO): a resource for reproducibility in
biomedical data analysis, curation and digital preservation. J. Biomed. Semant.
5(1), 1–13 (2014). https://doi.org/10.1186/2041-1480-5-25
42. McGuinness, D.L., Van Harmelen, F., et al.: Owl web ontology language overview.
W3C Recommendation (2004)
43. Miles, A., Bechhofer, S.: SKOS Simple Knowledge Organization System Reference.
Recommendation, World Wide Web Consortium (W3C), August 2009. https://
www.w3.org/TR/skos-reference/
44. Moradi, R., Berangi, R., Minaei, B.: A survey of regularization strategies for deep
models. Artif. Intell. Rev. 53, 3947–3986 (2020). https://doi.org/10.1007/s10462-
019-09784-7
45. Musen, M.A.: The Protégé project: a look back and a look forward. AI Matters
1(4), 4–12 (2015). https://doi.org/10.1145/2757001.2757003
46. OpenML: OpenML: a worldwide machine learning lab. https://www.openml.org
47. pandas: Pandas - A fast, powerful, ﬂexible and easy to use open source data analysis
and manipulation tool, built on top of the Python programming language.https://
pandas.pydata.org. Accessed 28 Nov 2023
48. Panov, P., Džeroski, S., Soldatova, L.: OntoDM: an ontology of data mining. In:
2008 IEEE International Conference on Data Mining Workshops, pp. 752–760.
IEEE (2008). https://doi.org/10.1109/ICDMW.2008.62
49. Panov, P., Soldatova, L., Džeroski, S.: OntoDM-KDD: ontology for representing
the knowledge discovery process. In: Fürnkranz, J., Hüllermeier, E., Higuchi, T.
(eds.) DS 2013. LNCS (LNAI), vol. 8140, pp. 126–140. Springer, Heidelberg (2013).
https://doi.org/10.1007/978-3-642-40897-7_9
50. Papers with Code: Papers With Code: The latest in Machine Learning. https://
paperswithcode.com. Accessed 28 Nov 2023
51. Peroni, S., Shotton, D.: FaBiO and CiTO: ontologies for describing bibliographic
resources and citations. J. Web Semant.17, 33–43 (2012).https://doi.org/10.1016/
j.websem.2012.08.001
52. Poveda-Villalón, M., Fernández-Izquierdo, A., Fernández-López, M., García-
Castro, R.: LOT: an industrial oriented ontology engineering framework. Eng.
Appl. Artif. Intell. 111, 104755 (2022). https://doi.org/10.1016/j.engappai.2022.
104755
53. Poveda-Villalón, M., Gómez-Pérez, A., Suárez-Figueroa, M.C.: OOPS! (OntOlogy
Pitfall Scanner!): an on-line tool for ontology evaluation. Int. J. Semant. Web Inf.
Syst. (IJSWIS) 10(2), 7–34 (2014). https://doi.org/10.4018/ijswis.2014040102

MLSea: A Semantic Layer for Discoverable Machine Learning 197
54. Publio, G.C., et al.: ML-Schema: Exposing the Semantics of Machine Learning
with Schemas and Ontologies. arXiv preprint arXiv:1807.05351 (2018). https://
doi.org/10.48550/arXiv.1807.05351
55. Ravishankar, N., Vijayakumar, M.: Reinforcement learning algorithms: survey and
classiﬁcation. Indian J. Sci. Technol.10(1), 1–8 (2017). https://doi.org/10.17485/
ijst/2017/v10i1/109385
56. Ristoski, P., Paulheim, H.: Semantic web in data mining and knowledge discovery:
a comprehensive survey. J. Web Semant.36, 1–22 (2016).https://doi.org/10.1016/
j.websem.2016.01.001
57. Rotmensch, M., Halpern, Y., Tlimat, A., Horng, S., Sontag, D.: Learning a health
knowledge graph from electronic medical records. Sci. Rep. 7(1), 5994 (2017).
https://doi.org/10.1038/s41598-017-05778-z
58. Ruder, S.: An overview of gradient descent optimization algorithms (2017).https://
doi.org/10.48550/arXiv.1609.04747
59. Sah, S.: Machine learning: a review of learning types. Int. Res. J. Mod. Eng. Tech-
nol. Sci. (2020). https://doi.org/10.20944/preprints202007.0230.v1
60. Saxena, A., et al.: A review of clustering techniques and developments. Neurocom-
puting 267, 664–681 (2017). https://doi.org/10.1016/j.neucom.2017.06.053
61. Sharma, H., Kumar, S., et al.: A survey on decision tree algorithms of classiﬁcation
i nd a t am i n i n g .I n t .J .S c i .R e s .( I J S R )5(4), 2094–2097 (2016)
62. Shrestha, A., Mahmood, A.: Review of deep learning algorithms and architec-
tures. IEEE Access 7, 53040–53065 (2019). https://doi.org/10.1109/ACCESS.
2019.2912200
63. Soldatova, L.N., King, R.D.: An ontology of scientiﬁc experiments. J. R. Soc. Inter-
face 3(11), 795–803 (2006). https://doi.org/10.1098/rsif.2006.0134
64. Souza, R., et al.: Provenance data in the machine learning lifecycle in compu-
tational science and engineering. In: 2019 IEEE/ACM Workﬂows in Support of
Large-Scale Science (WORKS), pp. 1–10. IEEE (2019). https://doi.org/10.1109/
WORKS49585.2019.00006
65. TensorFlow: An end-to-end open source machine learning platform for everyone.
https://www.tensorﬂow.org. Accessed 28 Nov 2023
66. Tian, Y., Zhang, Y.: A comprehensive survey on regularization strategies in
machine learning. Inf. Fusion80, 146–166 (2022). https://doi.org/10.1016/j.inﬀus.
2021.11.005
67. Vanschoren, J., Blockeel, H., Pfahringer, B., Holmes, G.: Experiment databases: a
new way to share, organize and learn from experiments. Mach. Learn.87, 127–158
(2012). https://doi.org/10.1007/s10994-011-5277-0
68. Vanschoren, J., Van Rijn, J.N., Bischl, B., Torgo, L.: OpenML: networked science
in machine learning. ACM SIGKDD Explor. Newsl. 15(2), 49–60 (2014). https://
doi.org/10.1145/2641190.2641198
69. Venkataramanan, R., Tripathy, A., Foltin, M., Yip, H.Y., Justine, A., Sheth,
A.: Knowledge graph empowered machine learning pipelines for improved eﬃ-
ciency, reusability, and explainability. IEEE Internet Comput.27(1), 81–88 (2023).
https://doi.org/10.1109/MIC.2022.3228087
70. Villanueva Zacarias, A.G., Reimann, P., Weber, C., Mitschang, B.: AssistML: an
approach to manage, recommend and reuse ML solutions. Int. J. Data Sci. Anal.
1–25 (2023). https://doi.org/10.1007/s41060-023-00417-5
71. Weibel, S.L., Koch, T.: DCMI metadata terms. Technical report, Dublin Core
Metadata Initiative (2012). http://dublincore.org/documents/dcmi-terms/

198 I. Dasoulas et al.
72. Zheng, Z., et al.: Executable knowledge graphs for machine learning: a Bosch case
of welding monitoring. In: Sattler, U., et al. (eds.) The Semantic Web – ISWC 2022.
ISWC 2022. LNCS, vol. 13489, pp. 791–809. Springer, Cham (2022). https://doi.
org/10.1007/978-3-031-19433-7_45
73. Zhou, B., et al.: SemML: facilitating development of ML models for condition
monitoring with semantics. J. Web Semant. 71, 100664 (2021). https://doi.org/
10.1016/j.websem.2021.100664

Enabling Social Demography Research
Using Semantic Technologies
Lise Stork1(B) , Richard L. Zijdeman2 , Ilaria Tiddi1 ,
and Annette ten Teije1
1 Vrije Universiteit Amsterdam, Amsterdam, The Netherlands
l.stork@uva.nl
2 International Institute of Social History, Amsterdam, The Netherlands
Abstract. A shift in scientiﬁc publishing from paper-based to
knowledge-based practices promotes reproducibility, machine actionabil-
ity and knowledge discovery. This is important for disciplines like social
demography, where study indicators are often social constructs such as
race or education, hypothesis tests are challenging to compare due to
their limited temporal and spatial coverage, and research output is pre-
sented in natural language, which can be ambiguous and imprecise. In
this work, we present the MIRA resource, to aid researchers in their
research workﬂow, and publish FAIR ﬁndings. MIRA consists of: (1) an
ontology for social demography research, (2) a method for automated
ontology population by prompting Large Language Models, and (3) a
knowledge graph populated in terms of the ontology by annotating a set
of research papers on health inequality. The resource allows researchers
to formally represent their social demography research hypotheses, dis-
covering research biases and novel research questions.
Keywords: Scientiﬁc Knowledge Graphs
· Social Demography ·
Hypothesis Representation · Health Inequality · Information Extraction
Resource type: Ontology, Knowledge Graph
License: CC BY 4.0 International
DOI: https://doi.org/10.5281/zenodo.10286846
URL: http://w3id.org/mira, http://w3id.org/mira/ontology/
1 Introduction
Research on social demography focuses on the statistical study of human popula-
tions, with the aim of understanding and predicting social, cultural and economic
trends across populations. Since the ﬁrst known census taken by the Babylonian
Empire in 3500 BCE [25], demographers have involved themselves with the task
of explaining aggregate statistics of a population [ 14]. Speciﬁcally, the research
cycle of a social historian consists of analysing observational data about society
to form novel hypotheses and theories about societal mechanisms (see left side of
Fig.1). However, such studies tend to be restricted to speciﬁc time periods and
c⃝ The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
A. Mero˜no Pe˜nuela et al. (Eds.): ESWC 2024, LNCS 14665, pp. 199–216, 2024.
https://doi.org/10.1007/978-3-031-60635-9_12

200 L. Stork et al.
regions, making comparison of hypothesis tests across the vast array of research
papers diﬃcult. Moreover, demographers test research hypotheses in which vari-
ables are often social constructs such as intelligence, ownership, or nationality.
Unclarity and ambiguity reporting research ﬁndings in natural language com-
plicates their precise understanding. Due to these complexities, demographers
often describe rather than explain demographic phenomena [14], whereas causal
explanations could help shape better policies for the future. Below we describe
a common motivating scenario.
Example 1. A social historian aims to analyse a population census from the
Netherlands between 1850–1922—consisting of certiﬁcates (births and mar-
riages), occupational and survival data
1—to better understand mechanisms of
social inequality. For this, the historian has to carefully survey the literature for
known theories and the datasets and statistics that support them.What was the
evidence for a speciﬁc hypothesis? How did they measure social stratiﬁcation?
What were the outcomes? Which societal factors, that are (not) in my dataset,
can moderate the eﬀect between my study variables? The historian may ﬁnd it
challenging to discover relevant papers or interpret research ﬁndings precisely.
To address such challenges, the paradigm of scientiﬁc publishing is seeing a
shift from document-oriented publishing to knowledge-based publishing [ 1,20],
with the aim of making the infrastructure for scientiﬁc publication of research
output more FAIR (Findable, Accessible, Interoperable, and Reusable). Seman-
tic technologies have been successfully employed in various domains to accommo-
date such a shift. Notable examples are the Open Science Knowledge Graph [1,
31], the Uniﬁed Medical Language System (UMLS) [ 2], or Biomedical knowl-
edge graphs such as [17], but many other examples exist [4,7,8,10,21,22,32,33].
These sources promote reusability of research ﬁndings, as well as the machine-
aided design of novel research questions. Moreover, by adopting formal represen-
tations of knowledge, such resources promote transparency and explainability.
In social demography, work has been done formally describing observational
data, such as census data hosted as linked data at the International Institute of
Social History (IISH)
2 [24]. To the best of our knowledge, no studies formalise
knowledge such as hypotheses and ﬁndings on social demography–and very few
from social sciences in general [ 22,32], whereas these are important in each of
the steps of the scientiﬁc workﬂow of a social historian (see Fig.1). The research
process, hypotheses and ﬁndings are mostly written up in scientiﬁc documents
in natural language, which can be ambiguous and imprecise. Such ﬁelds can
thus beneﬁt from adopting the FAIR data principles, to reduce unclarity and
ambiguity in the research workﬂow of a social demographer.
In summary, there is a need for the improvement of the digital infrastruc-
ture underlying scientiﬁc publication in social demography and social history
research, to stimulate a deep understanding, and reuse of existing hypotheses,
methods and ﬁndings. To address this need, this work provides:
1 for example: https://datasets.iisg.amsterdam/dataverse/HSNDB-HSN.
2 https://iisg.amsterdam/en.

Enabling Social Demography Research Using Semantic Technologies 201
1. The MIRA ontology, which includes a set of classes, properties and axioms for
capturing research ﬁndings (observations, comparisons and explanations)o n
social demography, as well as SHACL shapes following data quality criteria
of [5], for data validation.
2. A Knowledge Graph Construction (KGC) method, based on: (i) prompting
a Large Language Model to annotate paper abstracts using the ontology, (ii)
mapping concepts to terms from NCBO BioPortal ontologies and GeoNames,
and (iii) reﬁning the ﬁnal graph by a set of SHACL constraints, developed
according to data quality criteria.
3. The MIRA-KG, a knowledge graph of machine-annotated paper abstracts on
social health inequality in terms of the MIRA ontology. Annotations are linked
to Linked Open Data. The resource is published on the druid datalegend
database infrastructure
3, maintained by the international institute of social
history (IISH) and Triply4.
In general, this work (i) supports the shift towards knowledge-based scientiﬁc
publishing by contributing a novel method for KGC construction that can easily
be adapted to accommodate other application domains, and (ii) contributes to
a more FAIR infrastructure for social demography research.
data
(observations)
knowledge engineers
knowledge
extraction
data transformation
semantic technologies
knowledge
(declarative,
procedural)
1. analyse data
2. define semantic
 model
3. make data linkable
1. analyse data
2. define semantic
 model
3. extract knowledge
4. link knowledge
1.  assign license
2. define metadata
3. deploy resource
1.  assign license
2. define metadata
3. deploy resource
Intelligent
applications
data
(observations)
knowledge
(declarative,
procedural)
comparatory question
explanatory question
?
research workflow
descriptive question
a
b
c
demographers
knowledge
elicitation
1. define requirement
 stories
2. create competency
questions
Fig. 1.The social demography research workﬂow. Blue boxes contain components of
FAIR data management (e.g. for social history), which would enable social historians
to make their research more FAIR. (Color ﬁgure online)
2 Related Work
Ontologies and Vocabularies for Scientiﬁc Knowledge. Below we discuss exam-
ples of ontologies developed for various types of scientiﬁc knowledge:
3 https://druid.datalegend.net/.
4 https://triply.cc/.

202 L. Stork et al.
Upper-level science ontologies. Examples of upper-level ontologies for sci-
entiﬁc research are the Modern Science (ModSci) ontology [ 10], an upper
ontology for modern science branches and related entities, and the Semantic-
science Integrated Ontology (SIO) [9], a simple integrated ontology for rich
description of scientiﬁc concepts and processes.
Hypothesis representations. Work has been done on formalising research
hypotheses, and notable examples are the SuperPattern ontology [ 4], which
allows researchers to write up the main claims of scientiﬁc articles as state-
ments in formal logic; the nanopublication model [15], which aims at publish-
ing “core scientiﬁc statements with associated context”, or the DISK Hypoth-
esis Evolution ontology [12], which captures the evolution of hypotheses over
time. Many other representations exist, of which [ 12] provides an extensive
comparative overview. An example of a domain-speciﬁc scientiﬁc ontology is
the PICO ontology (for Population, Intervention, Comparator, Outcome) for
synthesis and querying of clinical trial experiments [23].
Data representations. The RDF Data Cube vocabulary
5 allows researchers
to publish their multi-dimensional data, and an example of a domain-speciﬁc
model for publishing datasets is the Data Scopes model [3,18], which captures
how datasets are processed in social history research.
Publication metadata. Lastly, vocabularies have been created to capture pub-
lication metadata. The most notable ones are the bibliographic ontology
(BIBO)6, the PRISM vocabulary7, and the Dublin Core8.
In this work, we formalise research hypotheses and link them to data repre-
sentations and publication metadata. We do so for the domain of social demog-
raphy, which has not been done before, and make use of some of the ontologies
and vocabularies enumerated above.
Scientiﬁc Knowledge Graphs. Knowledge Graphs that capture scientiﬁc knowl-
edge have been created from unstructured texts such as research papers, in
various domains like Computer Science and Artiﬁcial Intelligence [ 6–8], social
science [29], biomedicine [17], plant sciences [21], social and behavioural sciences
[22], or scientiﬁc articles in general [1,30,31]. Resources such as these support a
variety of tasks that aid researchers in the development of their research ques-
tions and methods. Our work is most related to the work of [ 29] and [22], but
instead proposes a semantic model of social demography hypotheses and ﬁnd-
ings, and a knowledge graph construction (KGC) method that does not rely on
the knowledge-intensive task of expert semantic annotation and links extracted
knowledge to other linked open data (LOD).
5 https://www.w3.org/TR/vocab-data-cube/.
6 https://www.dublincore.org/speciﬁcations/bibo/bibo/bibo.rdf.xml.
7 https://www.w3.org/submissions/2020/SUBM-prism-20200910/psv-over.html.
8 https://www.dublincore.org/.

Enabling Social Demography Research Using Semantic Technologies 203
3 Knowledge Graph Construction
This section describes the knowledge graph construction pipeline (see Fig. 2 for
the entire pipeline). Ontology creation is discussed in Sect. 3.1, the resulting
ontology in Sect. 3.2, ontology population in Sect. 3.3, and the resulting KG in
Sect.3.4.
Fig. 2. The knowledge graph constructionpipeline. Coloured artifacts are novel
contributions; non-coloured artifacts represent external repositories. (Color ﬁgure
online)
3.1 Ontology Creation
Below, we describe ontology creation process (see 1⃝ of Fig. 2). We follow the
eXtreme Design (XD) method for ontology development [ 27], a collaborative,
incremental, iterative method for pattern-based ontology design. We followed the
main steps of the XD methodology: (i) project scoping, (ii) creation of require-
ment stories, (iii) a module development loop.
1. Project initiation and scoping. A ﬁrst interview was set up with a domain
expert on social history and humanities research from the International Institute
of Social History (IISH)
9. The outcome of the interview was used to deﬁne
the task context, get a better understanding of the challenges, and write out a
ﬁrst list of ontology requirements (inspired by how a hypotheses is represented
in DISK [ 12,13]): Article metadata (RQ1), Hypothesis classiﬁcation (RQ2),
Hypothesis statement (RQ3), Hypothesis context (RQ4), Hypothesis qualiﬁer
(RQ5), and Hypothesis evidence (RQ6). For RQ2–6, we collected requirement
stories.
2. Requirement stories. Within this project, requirement stories were col-
lected based on insights retrieved during the project scoping phase about hypoth-
esis types and their elements. We show one requirement story below (Example2),
which shows an explanatory question (asking whether economic developments
can explain diﬀerences in socioeconomic inequality).
9 https://iisg.amsterdam/en.

204 L. Stork et al.
Example 2. “Is the inﬂuence of ascription on education larger than the inﬂu-
ence of achievement, and is the eﬀect moderated by economic developments?”
After a ﬁrst elicitation round, academic papers were used as requirement sto-
ries. An example annotation, based on the paper “Industrialization and inequal-
ity revisited: Mortality diﬀerentials and vulnerability to economic stress in Stock-
holm, 1878–1926”[ 26] is used as an example in the visual schematic of the ﬁnal
ontology (indicated by ■ ), see Figs. 3, 4 and 5.
3. Module development loop. Ontological requirements were elicited by
generalising terms from requirement stories and deriving competency questions
(CQs), resulting in a categorisation of main entity types and relations derived
from the requirement stories, see Table1.
Table 1. Question Type (QT), Question Level (QL), Observation Type (OT), and
Trend Type (TT) categorisations, based on requirement stories.
QT QL OT TT
Descriptive
Describing phenomena,
e.g. temperature is
rising over time
Micro
Individuals
Human
populations
Longitudinal
Observations over
time
Temporal trend
Comparison of
time intervals
Comparative
Comparisons between sam-
ple
means, trends, or eﬀects,
e.g. did temperature rise
more after
industrialisation?
Meso
Social groups,
Organisations
Intergenerational
Observations over
generations
Spatial trend
Comparison of
regions
Explanatory
Deﬁning a potential cause
of the outcome of a
comparison, e.g. did
human emission cause
t h er i s eo ft e m p e r a t u r e ?
Macro
Geographical
regions
Intersectional
Observations from
a single point
in time
Socioeconomic
trend
Comparison of
distribution
across
social classes
Moreover, contextual statements (CSs), and reasoning requirements (RRs)
were derived. CSs informed the creation of SHACL constraints for validation,
and RRs informed the creation of OWL
10 axioms. A collaborative environment in
the form of a Wiki was set up to gather the CQs, CSs, RRs and other outcomes.
A dump of the Wiki is published on Zenodo together with the dataset.
Ontology Reuse. For representing article metadata (RQ1), we use BIBO, PRISM
and Dublin Core. To classify hypotheses (RQ2), we use the classiﬁcation (QT)
from Table1. Moreover, to write up hypothesis statements (RQ3) and their con-
text (RQ4, based on (QL) from Table1) we utilise the structure and properties
of the SuperPattern Ontology [4]. However, we represent instances of the Super-
Pattern as individuals instead of classes. As in social demography, evidence often
10 https://www.w3.org/TR/owl-syntax/.

Enabling Social Demography Research Using Semantic Technologies 205
comes from speciﬁc time periods and regions, future work will explore the use of
class axioms to collect all evidence belonging to a claim. We additionally reuse
classes and properties from the Semanticscience Integrated Ontology (SIO) [33]
(e.g. trend line sio:SIO
000527 or human population sio:SIO 001062). For
qualiﬁers (RQ5), we reuse qualiﬁer categories from [16], as results can be trans-
lated to eﬀect sizes. Lastly, to link hypotheses to their evidence ( RQ6), we
reuse the RDF Data Cube Vocabulary11, furthering reproducibility and machine
actionability.
Design Pattern (ODP) Reuse. Scientiﬁc hypotheses and claims often consist of
complex relations between variables, relations, and ﬁndings, and as such there
are various ways of modeling them. One typical way is to reify the relation-
holding context as a node with binary relations for the subject, object and
property, and a fourth binary relation indicating the context [ 11]. A downside
of such a representation is that the Web Ontology Language (OWL)
12 does
not support reiﬁcation. Some Ontology Design Patterns such as the Content
Slices ODP
13 address the issue, but such modeling hampers easy integration
with paper metadata. Therefore, we choose for reiﬁcation with the idea that
the reiﬁed hypotheses can later be transformed to binary relations, should OWL
reasoning be required.
  LEGEND
    time: http://www.w3.org/2006/time#
    sio: http://semanticscience.org/resource/
    bibo: http://purl.org/ontology/bibo/           
    sp: https://w3id.org/linkflows/superpattern/latest/
    sem: http://semanticweb.cs.vu.nl/2009/11/sem/
    qb: http://purl.org/linked-data/cube#
    mira: https://w3id.org/mira/
    rdfs: http://www.w3.org/2000/01/rdf-schema#
    skos: http://www.w3.org/2004/02/skos/core#
    prov: http://www.w3.org/ns/prov#
    xsd: http://www.w3.org/2001/XMLSchema#
owl:Class Extracted
Class
RDF Data
Cube Vocab
running example (sub)class info
Academic
Article
has attribute
(SIO:SIO_000008)
Observational
Study
ID: SIO:IO_000976
ID: bibo:AcademicArticle
Comparison
ID: mira:Comparison
ID: mira:Explanation,
    mira:MainEffect
Main Effect
ID: mira:InteractionEffect
    
is evidence for
(SIO:SIO_000773)
Dataset
ID: mira:Context,
   qb:DataSet
has attribute
(SIO:SIO_000008)
has attribute
(SIO:SIO_000008)
Observational
Study 
has attribute
(SIO:SIO_000008)has attribute
(SIO:SIO_000008)
is evidence for
(SIO:SIO_000773)
Interaction
Effect
is evidence for
(SIO:SIO_000773)
Fig. 3.Main classes of the MIRA ontology. A ⋆ points to the IRI of the class(es) or
superclass. Elements retrieved from paper abstracts during the ontology population
process (see Sect. 3.3) are indicated in blue. Commonly, paper abstracts from social
demography do not contain statistical data and precise ﬁndings. (Color ﬁgure online)
3.2 The MIRA Ontology
The main concepts, relations and their domains and ranges of the MIRA Ontol-
ogy are created in light of our requirements and categorisations (Table 1)14.
T h e s ea r es h o w ni nF i g .3. Figure4 unfolds the comparison branch of the MIRA
11 http://www.w3.org/TR/vocab-data-cube/.
12 https://www.w3.org/TR/owl-ref/.
13 http://ontologydesignpatterns.org/wiki/Submissions:Context Slices.
14 Some categorisations (such as OT and CT) are omitted as these can be derived by
querying dataset information (the qb:sliceStructure of a qb:Slice).

206 L. Stork et al.
qb:slice
qb:slice
mira:hasContext
Dimension Property
mira:hasRelation
mira:hasEffectSize
mira:hasSubject
Measure
Type
ID: mira:MeasureType
subclasses:
ratio: SIO_001018 hazard ratio: 
IOBC:201006058769910455 
Comparison ID: mira:Comparison_:b 
 
mira:hasObject
mira:hasProbability
measure type
Information
Content Entity
Comparison Slice_:b 
 
ID: qb:Slice
qb:dataset
qb:dataset
Information
Content Entity 
ratio: SIO:SIO_001018
(_:b rdf:type  SIO:SIO_001018) Measure
Property
is about
(SIO:SIO_000332)
ID: qb:Slice
is about
(SIO:SIO_000332)
Slice Key_:b 
 
qb:sliceStructure
qb:sliceStructure
ex:mortalityRate 
rdf:type qb:MeasureProperty
qb:dimension
Dataset,
Sample
_:b 
 ID: qb:DataSet
SIO:SIO_001050
Probability
Value
_:b has value "0.002"
ID: SIO:SIO_000765
Relational
property
sp:hasLargerValueThan
Effect size
ID: SIO:SIO_000015
subclasses: 
trend line SIO:IO_000527
centrality measure SIO:SIO_001108
ratio SIO:SIO_001018
Slice_:b 
 
ID: qb:Slice
ID: qb:ComponentProperty
subclasses: 
qb:AttributeProperty
qb:DimensionProperty
qb:MeasureProperty
_:b rdfs:value "2.41"
ID: mira:EffectSize
ID: mira:RelationalProperty
ex:socialClass 
rdf:type qb:DimensionProperty
Fig. 4. The Comparison class and its links to the RDF Data Cube Vocabulary.
Comparisons compare information content entities such as trend lines, centrality mea-
sures, and ratios, which are based on slices over multidimensional data cubes. Example
instances and literals are based on the article“Industrialization and inequality revisited:
Mortality diﬀerentials and vulnerability to economic stress in Stockholm, 1878–1926”,
and indicated with ■ [26] (Color ﬁgure online)
mira:hasContext
mira:hasRelation
mira:hasSubject
Main Effect
ID: mira:Explanation,
    mira:MainEffect
mira:hasObject
Explanation
(main effect)
ID: qb:ComponentSpecification
Context/Population
human population: SIO:SIO_001062
(_:b rdf:type SIO:SIO_001062)
Dimension
Property
Relational
property
mira:correlatesWith
Interaction
Effect
_:b 
 
ID: mira:Explanation,
    mira:InteractionEffect
ex:mortalityRate 
rdf:type qb:MeasureProperty
Measure
Property
Dimension
Property
mira:hasObject
rdfs:subClassOf
ID: qb:ComponentProperty,
subclasses: 
qb:AttributeProperty
qb:DimensionProperty
qb:MeasureProperty
Data Structure
Definition
qb:structure
qb:dimension
qb:measure
qb:dimension
Component
Specification
_:b 
 
qb:component
Dataset,
Sample
_:b 
 
ID: mira:RelationalProperty
ID: mira:EffectSize
mira:hasEffectSize
is represented by
(SIO:SIO_000205)
Effect Size
mira:LargeMediumPositiveES
ID: mira:Context
ex:main1
has attribute
(SIO:SIO_000008)
ID: qb:DataStructureDefinition
sem:hasPlace
time:hasTime
Temporal Entity
Geographic
Location
ID: SIO:SIO_000414
ID: time:TemporalEntity
_:b rdfs:label "Stockholm"@en 
 
ID: qb:DataSet
SIO:SIO_001050
qb:dimension
mira:hasMediator
ex:socialClass 
rdf:type qb:DimensionProperty _:b 
 
Fig. 5. The Explanation (Main Eﬀect) class and its links to the RDF Data
Cube Vocabulary. Explanations describe measured eﬀects of dimensions in the dataset
(such as ex:socialClass, instance of qb:DimensionProperty) on measurements in the
dataset (instances of qb:MeasureProperty such as ex:mortalityRate). These prop-
erties can then be linked to concepts from ontologies using qb:concept (for exam-
ple ex:mortalityRate qb:concept STATO:STATO 0000414). The mira:correlatesWith
property is used as a subproperty of mira:RelationalProperty.N oc a u s a ll i n ki sy e t
stated, since more evidence from various regions and periods is required to state a
causal relationship. Interaction Eﬀectsare subclasses of main eﬀects. They are mod-
eled in the same way, with the following exceptions: the range of mira:hasObject is
an instance of mira:MainEffect; the range of mira:hasProperty is mira:moderates.
(Color ﬁgure online)
ontology. Descriptive statistics (such as ratios) can be compared, and are linked
to their respective data cube slices. Figure5 unfolds the explanation (main eﬀect
and interaction eﬀect) branch of the MIRA ontology.

Enabling Social Demography Research Using Semantic Technologies 207
From the CSs and RRs enumerated during the ontology design process, we
developed a set of OWL axioms and SHACL constraints for validation, which
describe the semantic requirements of the hypotheses. An example of an OWL
statement and axiom are: is evidence for is an owl:transitiveProperty,a n d
mira:InteractionEffect owl:subClassOf mira:Explanation respectively.
Examples of SHACL constraints are the use ofsh:minCount and sh:maxCount to
ensure that each paper has at least one study, each study has at least one expla-
nation, each explanation has as exactly one context, subject, object, relation and
qualiﬁer.
3.3 Ontology Population
Below, we describe the ontology population process from scientiﬁc papers (See2⃝
of Fig.2). Our method is related to other KGC methods such as [6], but explores
prompt-based triple extraction as a single extraction step allows for fewer errors
to be propagated to subsequent steps. Future work will compare such a method
with other established KGC methods. As a use case, we focus on articles related
to health inequality.
1. Retrieve papers. Papers included were retrieved from Semantic Scholar
using the Semantic Scholar API, and selected by the following steps:
– retrieving papers between 2020–2023, based on the keywords: ∈{ social,
inequality, disparities, mortality, population, socioeconomic, demographic,
study}, and the ﬁelds of study ∈{ Economics, History, Sociology }. These
keywords were terms encountered in the titles of the ﬁve papers used as
requirement stories;
– ﬁltering papers based on:
i citation count: removing articles with lower impact, with ≤ 10 citations;
ii journal: removing articles published in non peer-reviewed journals;
iii abstract length: including articles with abstract length l = μ − σ>l>
μ+σ (within plus-or-minus 1 standard deviation) as we found that it was
easier to extract hypotheses from texts that were not too long nor too
short due to conciseness and lack of information, respectively;
iv doi: whether or not articles included a Digital Object Identiﬁer (DOI).
2. Extract Knowledge. In social demography, the abstract of a paper com-
monly includes the explanatory question and the time period and location of
the population sample. We thus annotate paper abstracts with these parts of
the ontology (see the blue classes in Figs. 3, 4 and 5). In order to extract the
relevant entities, relations and attributes in terms of the ontology, we prompt
GPT-4 (OpenAI, 2023), see Table2. Large Language Models can learn multiple
tasks without any explicit supervision [19,28] and can therefore take on the task
normally performed through human annotators via crowdsourcing, without any
training. Retrieved annotations were extracted directly as triples of the form
< subject, predicate, object >using the Resource Description Framework
15.
15 https://www.w3.org/RDF/.

208 L. Stork et al.
Table 2. Prompt used to retrieve structured abstract annotations using GPT-4. Each
prompt consisted of the paper abstract, the ontology (domains and ranges), and some
instructions for formatting of individuals.
Prompt template
< abstract >
Describe the claim of the abstract above only using RDF (the turtle syntax),
and using the following ontology:
< property >< domain >< range >
< instructionnumber >< instruction >< example >
Only return proper RDF, no free text comments
Instruction example Answer
Instruction : use rdfs:label to describe all
blank nodes, also the geographic region. [ ] :hasSubject [rdfs:label “residential
Use short descriptions, pieces of text patterns and nutrition”@en]
verbatim from the abstract,
and add language tags to all labels.
Example:
[] :hasSubject [rdfs:label “social class”@en].
Instruction : for instances of the class
gn:Feature, ﬁnd the URI for the [] gn:locatedIn
place name in GeoNames <http://sws.geonames.org/2673730/>
(uri = https://www.geonames.org/<code>)
Example:[ ]g n : l o c a t e d I n<uri>
3. Process Knowledge. After extracting a set of triples (a subgraph) from
a paper abstract, we: (i) reshape the subgraph, as we prompted GPT-4 to
return annotations in a somewhat simpler structure to avoid structural errors,
(iii) add paper metadata by transforming paper metadata retrieved from
SemanticScholar (abstract, DOI, citations, publication date, authors) to RDF,
(ii) link study variables in the subgraph to Linked Open Data from BioPor-
tal and GeoNames, (iii) validate the subgraph using the SHACL shapes, and
(iv) integrate the subgraph with the MIRA-KG, andpostprocess the merged
graph by removing redundant entities.
Speciﬁcally, in the link step, instances of qb:ComponentProperty are linked
to concepts from BioPortal
16 using qb:concept. Prior to linking, a manual map-
ping study was performed (output can be found in the Zenodo repository) to
see which BioPortal ontologies contained most of the useful study variables.
Selected ontologies were HHEAR
17,S I O18, IOBC19 and MESH20). Subsequently,
16 https://bioportal.bioontology.org/.
17 https://bioportal.bioontology.org/ontologies/HHEAR/.
18 https://www.ebi.ac.uk/ols/ontologies/sio.
19 https://purl.bioontology.org/ontology/IOBC.
20 https://purl.bioontology.org/ontology/MESH.

Enabling Social Demography Research Using Semantic Technologies 209
we retrieve location metadata from GeoNames 21 through FactForge22,a st h e
knowledge extraction step already retrieves GeoNames IRIs. Location coordi-
nates, for instance, can aid researchers in discovering regional biases, or tempo-
ral trends. For the validate step, SHACL shapes are used to check for schema
and ontological correctness. One of the SHACL shapes, for instance, checks for
syntactic validity of dates, by ensuringsh:datatype xsd:date , and by checking
for ontological correctness (begin before end-date, see SHACL shapes). For the
integrate and postprocess steps, the subgraph is merged with the MIRA-KG.
After processing all paper subgraphs, we remove duplicate BioPortal concepts
and their labels via owl:sameAs smushing using RDFpro
23.
The time it took to process a single paper abstract was 1 min and 11 s (Mac-
Book M1 Chip, 8 cores, 8 gb RAM). A fully annotated paper abstract as machine-
readable data can be found in the Github repository.
3.4 The MIRA-KG
Table3 shows statistics of the ﬁnal knowledge graph, formalising 398 paper
abstracts. We remove paper metadata functional properties from this view
(for example dcterms:created), as these counts are equal to the instance
count for bibo:AcademicArticle. We present the average degree with and
Table 3.Statistics of the MIRA-KG: Class instance count, property count, number of
nodes and edges, and average degree.
Classes Instances Properties Count
time:Instant 948 bibo:cites 13496
qb:DimensionProperty 701 qb:concept 4041
skos:Concept 587 rdfs:label 3133
mira:Explanation 582 dcterms:contributor 1176
SIO:SIO 000414 (geographic region) 524 SIO:SIO 000008 (has attribute) 1065
SIO:SIO 001050 (sample) 477 time:inXSDDate 946
time:TemporalEntity 474 mira:hasSubject 607
qb:MeasureProperty 477 mira:hasContext 607
SIO:SIO 000976 (observational study) 469 SIO:SIO 000205 (is represented by) 607
SIO:SIO 001062 (human population) 408 mira:hasObject 602
bibo:AcademicArticle 398 mira:hasEffectSize 589
gn:Feature 114 mira:hasRelation 583
mira:InteractionEffect 105 sem:hasPlace 479
SIO:SIO 000012 (organisation) 12 time:hasTime 477
gn:locatedIn 454
wgs84 pos:long 172Dataset statistics
Number of Nodes 24281 wgs84 pos:lat 172
Number of Edges 32359 gn:name 114
Av. Degree 1.59 mira:hasMediator 77
Av. Degree (no types) 1.33 SIO:SIO 000061 (located in) 2
21 https://www.geonames.org/.
22 http://factforge.net.
23 https://github.com/dkmfbk/rdfpro.

210 L. Stork et al.
without types, as these are naturally densely connected hubs. More interest-
ing are the densely connected papers via citations or BioPortal concepts and
locations with high in-degrees. Nodes with the highest in-degree that were
not classes of the MIRA ontology were: economics/economy ( MESH:D004467,
IOBC:200906008393315870, 222), mortality rate (MESH:D009026, 188), hygiene
(MESH:D006920, 91), the United States ( geonames:6252001, 90) health
(MESH:D006262, 90), age (MESH:D006262, 83) and income (MESH:D007182, 47).
4 Evaluation
In this section, we ﬁrst evaluate the ontology (Sect. 4.1), and then the whole
knowledge graph via a use case and data quality measures (Sect.4.1).
4.1 Ontology Evaluation
Here, we show one of the competency questions as a SPARQL query (for brevity
we omit preﬁxes, but these can be found in Fig. 3): The CQ retrieves a claim
with a speciﬁc dependent variable and a potential mediator.
Fig. 6. CQ1: Have associations been found between a socioeconomic variable and
COVID-19, and which explanations can be found for the inequality?
Figure6b shows the output of the query for the CQ (ﬁrst ﬁve rows). It
indicates that residential segregation, economics and ethnicity were all correlated
with COVID-19 mortality. The association between COVID-19 and occupation
was speciﬁcally mediated by the ability to work from home (ability, home). The
rest of the competency questions can be found as SPARQL queries in the Github
repository. They could all be answered using SPARQL queries over the MIRA
ontology, although some limitations were discovered during ontology creation,
see Sect. 4.2 below.

Enabling Social Demography Research Using Semantic Technologies 211
Limitations. The sessions with the expert showed that within papers there are
various reformulations of the same hypothesis, which are at times not semanti-
cally the same. Such variations cannot be covered entirely without overly com-
plicating the ontology, and cannot always be fully understood without access to
the data and experiments. Moreover, eﬀect sizes are often not clearly reported
in the paper abstracts, hampering the quality of the extracted eﬀectsizes.
4.2 Knowledge Graph Evaluation
In this section, we evaluate the use of the MIRA-KG via a use case, and its
quality via a set of data quality criteria.
Use Case: Geographic Biases of Hypotheses and Findings. A researcher
is studying the eﬀect of income on mortality rates. They aim at discover-
ing whether there is a geographic study bias for the research question, and
whether the strength of the association diﬀers among geographic regions. The
researcher queries the MIRA-KG for all studies researching the inﬂuence of
income (MESH:D007182) on mortality (MESH:D00902).
Fig. 7. Use case:A social historian queries the MIRA-KG for metadata of all studies
researching the inﬂuence of income (MESH:D007182 ) on mortality (MESH:D00902 )
The output of the SPARQL query (ﬁrst four rows shown in Fig.7b) is visu-
alised on a world map (see Fig.8), and shows a bias of research studies towards
American samples for the speciﬁc correlation. Moreover, by aggregating the
results, the historian notices that four studies that are based on American pop-
ulation samples measure a negative correlation, and four a positive.

212 L. Stork et al.
Fig. 8.Density plot for the use case query, showing a bias towards studies based on
American population samples.
Data Quality Evaluation. We use the RDF data quality criteria as deﬁned
by [5] to, on the one hand, validate the MIRA-KG as well as the KGC pipeline,
and, on the other hand, reﬁne the graph. We summarise the most important
ones for our case below.
Accuracy. Accuracy in terms of Linked Data deals with syntactic and
semantic validity, as well as duplicate entries . Syntactic validity: the
DatatypeConstraintComponent catches data type violations, such as the use of
rdf:XMLLiteral where xsd:date should have been used. Furthermore, Table3
shows all retrieved GeoNames identiﬁers were correct identiﬁers, as meta-
data was retrieved for all of them from FactForge. Semantic validity: The
LessThanConstraintComponent measures logical temporal violations (begin
date before end date).Duplicate entries: from Table4 we see that with eight vio-
lations, these were annotated with high logical accuracy (98.3%). Lastly, dupli-
cate BioPortal entities were handled during the postprocessing step of the KGC
pipeline, as described in Sect. 3.3.
Table 4. Left: SHACL constraint violations for the MIRA-KG.Right: LLM retrieval
errors for 20 research articles.
Constraint violation Count LLM retrieval error (20 articles) Count
sh:LessThanConstraintComponent 8 Study variables 3
sh:DatatypeConstraintComponent 23 Location 2
sh:ClassConstraintComponent 38 Context 1
sh:MinCountConstraintComponent 122 Time period 7
sh:MaxCountConstraintComponent 4 Effect size 1
sh:XoneConstraintComponent 27
Trustworthiness. This dimension is deﬁned as the degree to which the infor-
mation is accepted to be correct, true, real and credible. As the MIRA-KG
was created automatically using GPT-4, we analyse the ﬁrst twenty hypotheses
(annotations can be found on Zenodo). Errors with respect to the retrieval are

Enabling Social Demography Research Using Semantic Technologies 213
shown in Table4. Study variables: in case study variables were incorrect, GPT-4
used related terms (such as time instead of age as independent variable). Time
period: most common errors were incorrectly retrieved dates. However it should
be mentioned that, in most cases, dates were incorrectly extracted when no dates
were mentioned in the abstract.
Even though errors appear, most terms appear to be retrieved correctly,
even for quite complicated hypotheses such as: In the context of a human popu-
lation, “Social inequality”, mediated through “Health-services structure”, is cor-
related with “COVID-19 mortality” with a largeMediumPositiveES. “Govern-
mental response to COVID-19” moderates this correlation. Evidence comes from
“S˜ao Paulo residents”, from “S˜ao Paulo” between the years “2020-03-01” and
“2020-09-30”.
Consistency. Semantic consistency is the extent to which a collection uses the
same values for conveying the same meanings throughout. SHACL constraints
were applied to enforce schema-correctness (such as a hypothesis has at least one
independent variable). Constraint violations can be found in Table4 (sh:Class,
sh:MinCount, sh:MaxCount and sh:Xone-ConstraintComponent). By looking
at the exact violations, we see that common errors were errors in structure, such
as a context which was linked to a study instead of an explanation, resulting
in violations of both the Class as well as the MinCount constraint components.
The graph was queried to retrieve and dissolve these common errors to further
consummate the entire graph.
Limitations. Due to the limitations mentioned in Sect.4.1 (underspeciﬁcation,
ambiguity, and unclarity), it is challenging to extract hypotheses from scientiﬁc
papers in a precise manner. The ontology will, however, allow researchers to
publish their ﬁndings in a machine-readable manner alongside paper publication.
Second, representing complex concepts, such as ‘the ability to work from home’,
is non-trivial, as these are not always deﬁned in ontologies or vocabularies and
can be described in many diﬀerent ways. For querying, linking such a variable
to the concepts ‘ability’ as well as ‘home’ would suﬃce, but if precise reasoning
is required, other solutions need to be considered (e.g. OWL axioms).
5 Conclusions
Studies in (historical) social sciences, such as social demography, tend to be
restricted to speciﬁc time periods and regions, making comparison of hypothesis
tests across the vast array of research papers diﬃcult. To assist social histori-
ans and demographers in the scientiﬁc process, this study describes MIRA, a
method knowledge graph construction, and a resource consisting of a ontology
and knowledge graph to capture hypotheses and ﬁndings in social demography.
This study shows that the MIRA ontology allows researchers to formulate
their key questions, and research results in a structured and semantically sound
way. Moreover, using over 400 abstracts from the ﬁeld of social demography,

214 L. Stork et al.
our knowledge graph construction pipeline demonstrates that the knowledge-
intensive task of semantic annotation can be (semi-)automated when employing
a Large Language Model, even without any training, validating data quality
after automated annotation.
Future work will focus on dealing with variations in natural language, and
on expanding the MIRA-KG by application of the MIRA ontology on a larger
set of studies in order for the ﬁeld to reorganize itself, for instance by motivating
researchers to publish their ﬁndings in a machine-readable manner.
Acknowledgements. This work was funded by the European MUHAI project (Hori-
zon 2020 research and innovation program) under grant agreement number 951846. We
thank Tobias Kuhn, Frank van Harmelen, and In`es Blin for the insightful discussions
that contributed to this work.
References
1. Auer, S., Kovtun, V., Prinz, M., Kasprzik, A., Stocker, M., Vidal, M.E.: Towards
a knowledge graph for science. In: Proceedings of the 8th International Conference
on Web Intelligence, Mining and Semantics, pp. 1–6 (2018)
2. Bodenreider, O.: The uniﬁed medical language system (UMLS): integrating
biomedical terminology. Nucleic Acids Res. 32(suppl 1), D267–D270 (2004)
3. de Boer, V., Bonestroo, I., Koolen, M., Hoekstra, R.: A linked data model for data
scopes. In: Garoufallou, E., Ovalle-Perandones, M.A. (eds.) MTSR 2020. CCIS,
vol. 1355, pp. 345–351. Springer, Cham (2021).https://doi.org/10.1007/978-3-030-
71903-6
32
4. Bucur, C.I., Kuhn, T., Ceolin, D., Van Ossenbruggen, J.: Expressing high-level
scientiﬁc claims with formal semantics. In: K-CAP 2021 - Proceedings of the
11th Knowledge Capture Conference, pp. 233–240 (2021).https://doi.org/10.1145/
3460210.3493561
5. Candela, G., Escobar, P., Carrasco, R.C., Marco-Such, M.: Evaluating the quality
of linked open data in digital libraries. J. Inf. Sci. 48(1), 21–43 (2022)
6. Dess´ı, D., Osborne, F., Recupero, D.R., Buscaldi, D., Motta, E.: SCICERO: a
deep learning and NLP approach for generating scientiﬁc knowledge graphs in the
computer science domain. Knowl.-Based Syst. 258, 109945 (2022). https://doi.
org/10.1016/j.knosys.2022.109945
7. Dess´ı, D., Osborne, F., Reforgiato Recupero, D., Buscaldi, D., Motta, E.: CS-KG:
a large-scale knowledge graph of research entities and claims in computer science.
In: Sattler, U., et al. (eds.) ISWC 2022. LNCS, vol. 13489, pp. 678–696. Springer,
Cham (2022). https://doi.org/10.1007/978-3-031-19433-7
39
8. Dess`ı, D., Osborne, F., Reforgiato Recupero, D., Buscaldi, D., Motta, E., Sack,
H.: AI-KG: an automatically generated knowledge graph of artiﬁcial intelligence.
In: Pan, J.Z., et al. (eds.) ISWC 2020, Part II. LNCS, vol. 12507, pp. 127–143.
Springer, Cham (2020). https://doi.org/10.1007/978-3-030-62466-8 9
9. Dumontier, M., et al.: The Semanticscience Integrated Ontology (SIO) for biomed-
ical research and knowledge discovery. J. Biomed. Semant.5, 1–11 (2014)
10. Fathalla, S., Lange, C., Auer, S.: An upper ontology for modern science branches
and related entities. In: Pesquita, C., et al. (eds.) ESWC 2023. LNCS, vol. 13870,
pp. 436–453. Springer, Cham (2023). https://doi.org/10.1007/978-3-031-33455-
9 26

Enabling Social Demography Research Using Semantic Technologies 215
11. Gangemi, A., Presutti, V.: A multi-dimensional comparison of ontology design
patterns for representing n-ary relations. In: van Emde Boas, P., Groen, F.C.A.,
Italiano, G.F., Nawrocki, J., Sack, H. (eds.) SOFSEM 2013. LNCS, vol. 7741, pp.
86–105. Springer, Cham (2013). https://doi.org/10.1007/978-3-642-35843-2
8
12. Garijo, D., Gil, Y., Ratnakar, V.: The DISK hypothesis ontology: capturing
hypothesis evolution for automated discovery. In: K-CAP Workshops, pp. 40–46
(2017)
13. Gil, Y., et al.: Towards continuous scientiﬁc data analysis and hypothesis evolution.
In: Proceedings of the AAAI Conference on Artiﬁcial Intelligence, vol. 31 (2017)
14. Graham, E.: Theory and explanation in demography: the case of low fertility in
Europe. Popul. Stud. 75(sup1), 133–155 (2021)
15. Groth, P., Gibson, A., Velterop, J.: The anatomy of a nanopublication. Inf. Serv.
Use 30(1–2), 51–56 (2010)
16. de Haan, R., Tiddi, I., Beek, W.: Discovering research hypotheses in social science
using knowledge graph embeddings. In: Verborgh, R., et al. (eds.) ESWC 2021.
LNCS, vol. 12731, pp. 477–494. Springer, Cham (2021). https://doi.org/10.1007/
978-3-030-77385-4
28
17. Himmelstein, D.S., et al.: Systematic integration of biomedical knowledge priori-
tizes drugs for repurposing. Elife 6, e26726 (2017)
18. Hoekstra, R., Koolen, M.: Data scopes for digital history research. Hist. Methods:
A J. Quant. Interdisc. Hist. 52(2), 79–94 (2019)
19. Kojima, T., Gu, S.S., Reid, M., Matsuo, Y., Iwasawa, Y.: Large language models
are zero-shot reasoners. In: Advances in Neural Information Processing Systems,
vol. 35, pp. 22199–22213 (2022)
20. Kuhn, T., et al.: Decentralized provenance-aware publishing with nanopublications.
PeerJ Comput. Sci. 2, e78 (2016)
21. Larmande, P., Todorov, K.: AgroLD: a knowledge graph for the plant sciences.
In: Hotho, A., et al. (eds.) ISWC 2021. LNCS, vol. 12922, pp. 496–510. Springer,
Cham (2021). https://doi.org/10.1007/978-3-030-88361-4
29
22. Magnusson, I.H., Friedman, S.E.: Extracting ﬁne-grained knowledge graphs of sci-
entiﬁc claims: dataset and transformer-based results. In: EMNLP 2021 - 2021 Con-
ference on Empirical Methods in Natural Language Processing, Proceedings, pp.
4651–4658 (2021). https://doi.org/10.18653/v1/2021.emnlp-main.381
23. Mavergames, C., Oliver, S., Becker, L.: Systematic reviews as an interface to the
web of (trial) data: using PICO as an ontology for knowledge synthesis in evidence-
based healthcare research. SePublica 994, 22–6 (2013)
24. Mero˜no-Pe˜nuela, A., Ashkpour, A., Gu´eret, C., Schlobach, S.: CEDAR: the Dutch
historical censuses as linked open data. Semant. Web 8(2), 297–310 (2017)
25. Missiakoulis, S.: Cecrops, King of Athens: the ﬁrst (?) recorded population census
in history. Int. Stat. Rev. 78(3), 413–418 (2010)
26. Molitoris, J., Dribe, M.: Industrialization and inequality revisited: mortality dif-
ferentials and vulnerability to economic stress in Stockholm, 1878–1926. Eur. Rev.
Econ. Hist. 20(2), 176–197 (2016)
27. Presutti, V., Daga, E., Gangemi, A., Blomqvist, E.: Extreme design with content
ontology design patterns. In: Proceedings of the Workshop on Ontology Patterns,
pp. 83–97 (2009)
28. Radford, A., Wu, J., Child, R., Luan, D., Amodei, D., Sutskever, I., et al.: Language
models are unsupervised multitask learners. OpenAI Blog 1(8), 9 (2019)
29. Spadaro, G., et al.: The Cooperation Databank: machine-readable science acceler-
ates research synthesis. Perspect. Psychol. Sci. 17(5), 1472–1489 (2022)

216 L. Stork et al.
30. Stocker, M., et al.: SKG4EOSC-scholarly knowledge graphs for EOSC: establishing
a backbone of knowledge graphs for fair scholarly information in EOSC. Res. Ideas
Outcomes 8, e83789 (2022)
31. Stocker, M., et al.: FAIR scientiﬁc information with the open research knowledge
graph. FAIR Connect 1(1), 19–21 (2023)
32. Tiddi, I., Balliet, D., ten Teije, A.: Fostering scientiﬁc meta-analyses with knowl-
edge graphs: a case-study. In: Harth, A., et al. (eds.) ESWC 2020. LNCS, vol.
12123, pp. 287–303. Springer, Cham (2020). https://doi.org/10.1007/978-3-030-
49461-2 17
33. Viet, S.M., et al.: Human Health Exposure Analysis Resource (HHEAR): a model
for incorporating the exposome into health studies. Int. J. Hyg. Environ. Health
235, 113768 (2021)

SCOOP All the Constraints’ Flavours
for Your Knowledge Graph
Xuemin Duan1(B) , David Chaves-Fraga2,1 , Olivier Derom1,
and Anastasia Dimou1
1 KU Leuven – Flanders Make@KULeuven – Leuven.AI, Leuven, Belgium
{xuemin.duan,anastasia.dimou}@kuleuven.be
2 Grupo de Sistemas Intelixentes, Universidade de Santiago de Compostela,
Santiago de Compostela, Spain
david.chaves@usc.es
Abstract. Creating SHACL shapes for the validation of RDF graphs
is a non-trivial endeavor. Automated shape extraction systems typically
derive SHACL shapes from RDF graphs, and thus, their eﬀectiveness
is inherently inﬂuenced by the size and complexity of the RDF graph.
However, these systems often overlook the constraints imposed by indi-
vidual artifacts, although RDF graphs are often constructed by apply-
ing ontology terms to heterogeneous data. Only a few systems extract
SHACL shapes from either the data schema or the ontology, leading, in
either case, to limited or incomplete constraints. We propose SCOOP,
a framework that exploits all artifacts associated with the construction
of an RDF graph, i.e. data schemas, ontologies, and mapping rules, and
integrates the SHACL shapes extracted from each artifact into a uniﬁed
shapes graph. We applied our approach to real-world use cases and exper-
imental results showed that SCOOP outperforms systems that extract
SHACL shapes from RDF graphs, generating more than double the types
of constraints than those systems, and eﬀectively identifying missing and
erroneous RDF triples during the validation process.
Resource type : Software Framework — License: Apache-2.0
DOI: https://doi.org/10.5281/zenodo.10280346
URL: https://github.com/dtai-kg/SCOOP
Keywords: SHACL
· Shape integration · Knowledge graph validation
1 Introduction
Creating SHACL shapes for the validation of RDF graphs is a non-trivial
endeavor. Shapes Constraint Language (SHACL) [27], the W3C recommendation
for validating RDF graphs, has gained increasing popularity, which has further
prompted a growing number of endeavors in automating shape extraction. How-
ever, a notable proportion of users in industry and academia still favor creating
shapes manually [13,32], indicating the practical limitations of existing works.
Currently, automated shape extraction broadly falls into two categories:
RDF-based and non-RDF-based systems. The cost and performance of systems
c⃝ The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
A. Mero˜no Pe˜nuela et al. (Eds.): ESWC 2024, LNCS 14665, pp. 217–234, 2024.
https://doi.org/10.1007/978-3-031-60635-9_13

218 X. Duan et al.
extracting shapes from RDF graphs [16–18,28,33,38] are inherently contingent
upon the scale and intricacy of the RDF graph, frequently leading to a limited
subset of constraints [31], e.g., not covering value range (e.g.,sh:minExclusive)o r
string-based constraints (e.g., sh:minLength). Besides, these systems also over-
look the constraints imposed by an RDF graph’s individual artifacts.
Non-RDF systems can be further delineated into extraction systems mining
shapes from either ontologies, mappings, or raw data schemas, i.e. the artifacts
from which RDF graphs are constructed. However, extracting shapes only from
ontologies [5,23] often results in redundant shapes, as the shapes frequently
encompass a broader spectrum of classes and properties than those in the target
RDF graph. Extracting shapes from raw data schemas , e.g., SQL schema [39],
XML Schema Deﬁnitions (XSD) [12,21] or JSON Schema [6], always results in
the misalignment between the extracted shapes and the classes and properties
within the target RDF graph [12]. Extracting shapes from mappings [9] covers
only a limited set of constraints [ 9]. This singular input source often results
in limited or incomplete constraints. To date, no research has been undertaken
to integrate shapes from multiple relevant sources into a uniﬁed shapes graph,
alleviating the drawbacks of individual systems and bolstering overall robustness.
We present SCOOP, a framework that exploits all artifacts associated with
the construction of an RDF graph: data SChemas, OntOlogies, and maPpings.
SCOOP integrates the SHACL shapes extracted from each artifact into a uni-
ﬁed shapes graph. To achieve this, SCOOP comprises three modules: (i) post-
adjustment to align schema-driven shapes with the target RDF graph; (ii)equiv-
alences identiﬁcation to align shapes from diverse sources, and (iii) integration
and inconsistencies resolution to prevent unsatisﬁable shapes. We implement
SCOOP as an open-source system
1 which incorporates RML2SHACL [ 8,9],
Astrea [4,5], and XSD2SHACL [ 11,12] to integrate shapes from mappings in
RML [10,25], ontologies in OWL [2], and raw data schemas in XSD [15].
We compare SCOOP with state-of-the-art systems in a real-world use case.
The performance experiments show that SCOOP has a signiﬁcantly lower max-
imum memory usage compared to the RDF-based system. Addtionally, its run-
ning time is independent of the data size and faster than the RDF-based system
when the RDF graph exceeds 3.30 GB in size. The coverage experiments reveal
that SCOOP excels in generating accurate shapes to target classes and prop-
erties, outperforming state-of-the-art systems, and generates more than twice
the types of constraints compared to RDF-based systems. SCOOP is an exten-
sible framework that can seamlessly integrate more sources as additional shape
extraction systems emerge, e.g., other raw data schemas or mapping languages.
The remaining paper is organized as follows: Sect. 2 describes related works
and preliminaries; Sect. 3 discusses the challenges during shape integration;
Sect.4 describes our methodology and implementation to address these chal-
lenges. Section 5 provides the evaluation of SCOOP in real-world use cases.
Section6 concludes this paper and outlines possible future directions.
1 https://github.com/dtai-kg/SCOOP.

SCOOP All the Constraints’ Flavours for Your Knowledge Graph 219
2 Preliminaries and Related Work
In this section, we introduce RDF validation (SHACL) and RDF construction
(RML), and then outline related work regarding shape extraction.
2.1 Preliminaries
This subsection summarizes the concepts required to understand the paper.
KG Validation with SHACL. To validate nodes in the RDF graph, the
Shapes Constraint Language (SHACL) was recommended by W3C [ 27]. The
shapes graph refers to a collection of shapes containing constraints expressed in
RDF format, while thedata graph pertains to the target RDF graph undergoing
validation. A node shape typically speciﬁes constraints on the focus node, where
the focus node represents the node in the RDF graph being validated (e.g., all
instances of :Student, Fig.2). The focus node can be directly designated by tar-
get declaration (e.g., :NS sh:targetClass :Student ), indirectly speciﬁed through
reference relationships (e.g., :NS sh:node :NS2 ), or explicitly fed to the SHACL
processor with nodes to be validated. In cases where RDF graphs are to be
validated automatically without explicit extra speciﬁcation, shapes lacking tar-
get declarations become invalid as they do not trigger validation. A property
shape primarily serves to deﬁne the property value reached from the focus node
through a property path (e.g., :PS sh:path :grade ). Therefore, reference relation-
ships between shapes (e.g., :NS sh:property :PS ) are crucial, as they delineate
how the SHACL processor traverses from the focus node to the property value.
KG Construction with RML. To map heterogeneous data to RDF graphs,
the RDF Mapping language was proposed in [ 10,25] generalizing R2RML [ 7],
the W3C recommendation to construct RDF graphs from relational databases.
The triples map describes how to map a data source, comprised by a logical
source, a subject map, and multiple predicate-object maps. The logical source
deﬁnes information about the mapped data source, including data location (e.g.,
“student.xml” in Fig. 2), reference formulation (e.g., ql:XPath in Fig. 2), and an
optional iterator (e.g., “/student” in Fig. 2). The subject map deﬁnes how the
subjects of triples are generated (e.g., “http://example.com/{@id}” in Fig. 2),
and the predicate-object map deﬁnes how the corresponding predicate (e.g.,
:grade in Fig.2) and object (e.g., “/grade” in Fig.2) are generated. Thereference
is used to directly specify the original data source, while the template is used to
build strings with the data source, which can be a single-component template
or a multi-component template (e.g., “http://example.com/{@id} {grade}”).
2.2 Related Work
Prior research on SHACL shape extraction primarily focuses on deriving shapes
graphs from RDF graphs ; but also ontologies, raw data schemas ,a n dmapping
rules. However, no system integrates multiple shapes into a uniﬁed shape.
RDF Graphs-Driven. Numerous eﬀorts were proposed to extract shapes and
constraints from RDF graphs but the computational burden is contingent upon

220 X. Duan et al.
the scale of the RDF graphs and the covered constraints are limited [ 31].
QSE [33] mines shapes from large RDF graphs and avoids spurious shapes
by calculating the support and conﬁdence scores of extracted shapes; SHAC-
TOR [34] provides a graphical user interface based on QSE. SHACLGEN [1]
implements a query-based system, which loads the whole RDF graph in memory
restricting its capacity to handle large RDF graphs. SheXer [17,18] mines and
ﬁlters feature for constraints according to the frequency of occurrence, but the
implementation lacks support for N-Quads. ABSTAT [38] employs a summa-
rization model to mine shapes by summarizing triple patterns extracted from
the semantic proﬁle of RDF graphs. ShapeInduction [28] proposes an RDF
graph proﬁling approach using machine learning techniques by transforming the
regression problem into a classiﬁcation problem.SHACLearner [22] utilizes the
inverse open path (IOP) to infer potential constraints in shape fragments for a
given target. Last, ShapeDesigner [3] extracts shapes using a query language.
Ontology-Driven. Deriving SHACL shapes from ontologies is independent of
data scale, yet limited to constraints exclusively deﬁned by the ontology, and
frequently derives redundant shapes as the RDF graph may only involve a subset
of the ontology.Astrea [5] derives SHACL shapes from ontologies by executing
a set of pre-deﬁned SPARQL queries to retrieve ontology elements and derive
corresponding shapes and constraints. SHACLGEN also supports extracting
shapes from ontologies and Harshvardhan et al. [23,29] reuse the Ontology
Design Pattern (ODP) axioms to extract equivalent SHACL shapes.
Schema-Driven. Extracting SHACL shapes fromraw data schemas eliminates
the dependencies on the RDF graph scale, akin to ontology-driven systems. How-
ever, the extracted shapes resort to a default namespace, causing a misalign-
ment with their targeted RDF graphs. For XML, XSD2SHACL [12] mines
SHACL shapes based on a set of correspondences between XSD and SHACL,
while XMLSchema2ShEx [21] mines ShEx shapes, but partially covers XSD.
Mapping-Driven. Deriving shapes frommapping rules [9] captures the implied
constraints within the mapping rules, but it is limited to the constraints that can
be described by the mapping language. RML2SHACL [9] is the only system
that derives SHACL shapes from RML mapping rules [ 10] based on a set of
proposed correspondences. Its coverage is limited to constraints of a more basic
nature, as RML does not oﬀer the same scope of support for rich constraints
found in SHACL, such as value range constraints (e.g., sh:minExclusive).
As opposed to the aforementioned, SCOOP integrates SHACL shapes
extracted from the raw data schema, the ontology, and the mapping rules, taking
advantage of all aspects that contributed to the construction of an RDF graph.
3 Shape Integration Challenges
Integrating SHACL shapes from mapping rules, ontologies, and raw data
schemas is not straightforward, as challenges may arise during the integration
process.

SCOOP All the Constraints’ Flavours for Your Knowledge Graph 221
(C1) Misalignments. Misalignment arises inevitably during the integra-
tion of shapes extracted from raw data schemas and those extracted from ontol-
ogy or mappings. The shapes derived from mappings and ontologies are swiftly
applicable for validation purposes, as they inherently align with the deﬁned
classes and properties within the RDF graph (e.g.,sh:targetClass of stu:Student).
However, the shapes from raw data schemas cannot be directly aligned with
the SHACL shapes extracted from the mappings and ontologies. Due to the
absence of classes and properties information speciﬁc to the target RDF graphs,
the extracted shapes resort to default namespaces pre-deﬁned by the extraction
systems. As shown in Fig.2,t h eXSD-driven shapes opt for ex:student as target
class (instead of stu:Student as in the target RDF graph). Moreover, constraints
extracted from the raw data schema may be superseded or become invalid during
the RDF construction. For instance, theid originally deﬁned as a string in XSD-
driven shapes may be used to create an IRI according to the mappings.
(C2) Inequivalences. The basis of the shape integration lies in the con-
solidation of constraints encapsulated within equivalent shapes, i.e. shapes vali-
dating the same node, which cannot be solely ascertained through uniform tar-
get declarations or property paths due to the ﬂexibility of SHACL syntax. For
instance, a node shape speciﬁed with sh:targetClass :Student is deemed equiva-
lent to a shape that deﬁnes the same target declaration. However, it may also
be considered equivalent to another node shape referenced by a shape sharing
the same target declaration (e.g., sh:targetClass :Student ) through sh:node,e v e n
if the latter node shape lacks the same target declaration.
(C3) Inconsistencies. Integrating shapes from diﬀerent sources may lead
to constraint inconsistencies, potentially rendering the unsatisﬁable shape, i.e.,
a shape that can never be conformed. Two distinct types of inconsistencies are
identiﬁed: one type adheres to SHACL syntax without violation, while the other
type poses a risk to the well-formedness of the resulting shape. As an illustrative
scenario, consider the construction of an RDF graph from two distinct raw data
sources, each is adhering to dissimilar grading systems. One source speciﬁes a
passing grade range spanning from 8 to 20 points and the student id should
be IRI, while the other designates that from 60 to 100 and the id should be
a string. Direct integration of constraints of sh:nodeKind sh:IRI and sh:datatype
:string will lead to inconsistency, i.e. it does not violate syntax but will cause the
shape to never be satisﬁed. The simultaneous presence of two distinct passing
grade constraints sh:minInclusive and two sh:maxInclusive can be categorized as
an inconsistency, which arises from the restriction that a shape incorporates at
most one sh:minInclusive constraint and one sh:maxInclusive constraint.
4 SCOOP
We propose SCOOP, an open-source framework1 designed to integrate existing
shape extraction systems targeting diverse sources into a uniﬁed and compre-
hensive shapes graph. The current version of SCOOP supports SHACL core [27].
The integration workﬂow (Fig.1) can be delineated into three principal mod-
ules: (1) post-adjustment of shapes extracted from raw data schema to ensure

222 X. Duan et al.
Fig. 1. The workﬂow of SCOOP.
alignment with the target RDF graph (Fig.1– 1 ), overcoming (C1); (2)equiva-
lences identiﬁcation among extracted shapes from diverse sources to identify
equivalent shapes (Fig. 1– 2 ), overcoming (C2); (3) integration and incon-
sistencies resolution for identifying inconsistent constraints within equivalent
shapes (Fig. 1– 3 ) to make integration decisions based-on three conﬁgurations,
SCOOP-All, SCOOP-Prior, and SCOOP-Prior-R, overcoming (C3). The mod-
ules are explained in detail in Subsect. 4.1, 4.2,a n d4.3 respectively.
4.1 Post-adjustment
We mitigate the misalignment between preliminary shapes extracted from raw
data schemas and target RDF graphs by leveraging the RML mappings during
post-adjustment. Given that the most mature systems to extract shapes from
the raw data schema are focused on XML, we demonstrate our methodology for
XML Schema but the same should hold for other schemas as well.
The post-adjustment (Fig. 2) is structured into three steps: (a) SHACL
parsing to compute the implicit XPath within each shape (e.g.,/student/grade)
(Fig.2– A ); (b) RML parsing to extract the XPath alongside the correspond-
ing classes and properties (e.g., the property stu:grade is related to objects con-
structed with the values of the elements matching the /student/grade XPath
expression) (Fig. 2– B ); (c) shape adjustment based on the outcomes of the
parsing process (e.g., adjust ex:grade to stu:grade) (Fig. 2– C ).
SHACL Parsing. We compute the XPath for each XSD-driven shape
based on shape identiﬁers and the referencing relationships among shapes
by utilizing a depth-ﬁrst search (DFS) algorithm. The identiﬁer for
shapes (e.g., http://example.com/PropertyShape/studentType/grade) generated
by XSD2SHACL is the concatenation of the names of element declarations (e.g.,
grade), attribute declarations (e.g.,id), and global complex type deﬁnitions (e.g.,
studentType) within the XSD. It encapsulates the path from the global declara-
tion or deﬁnition (e.g.,studentType) to the corresponding XSD component (e.g.,
grade). Nevertheless, the identiﬁer cannot be swiftly extracted as an XPath due
to the potential truncation of the XPath (e.g., /student/studentType and /stu-
dentType/grade) in the identiﬁer. Thus, the entire shapes graph needs to be
traversed to compute the complete XPath (e.g., student/grade).
We convert the shapes into a reversed directional acyclic graph of iden-
tiﬁers and employ a DFS algorithm to traverse it, then compute the com-
plete XPath for each shape by considering all relevant shapes. We initiate

SCOOP All the Constraints’ Flavours for Your Knowledge Graph 223
Fig. 2. An example of post-adjustment. RML in YARRRML serialisation.
the process by reversing the relationships of identiﬁers referenced through
sh:property and sh:node to construct a graph. Shapes that reference other
shapes but are not referenced by any shape are transformed into leaf nodes
(e.g., http://example.com/NodeShape/student). Then we traverse the graph using
DFS to calculate the paths leading to all potential leaf nodes commencing
from each node. We can distinguish the segments within identiﬁers that are
not elements or attributes names (e.g., studentType), as complex type deﬁ-
nitions do not require the target declarations creation in XSD2SHACL (e.g.,
http://example.com/NodeShape/student/studentType). Ultimately, we obtain an
XPath for each shape by concatenating the path fragments found within each
path list (e.g., /student and /grade), while eliminating any fragments corre-
sponding to complex type deﬁnitions (e.g., studentType). An example outcome
of SHACL parsing can be found in Fig.2.
RML Parsing. We parse the RML mappings to extract the XPath (e.g., stu-
dent/grade) corresponding to the associated classes or properties (e.g.,stu:grade)
as Fig.2 shows. For each triples map (e.g.,:StudentMapping), we identify all rel-
evant classes (e.g., stu:Student) and associate them with the XPath extracted
from a template (e.g., id from http://example.com/@id) or reference in the sub-
ject map and concatenate it with the iterator (e.g., /student). Similarly, for
each predicate-object map, we correlate the property (e.g., stu:grade) deﬁned
by the predicate map with the XPath (e.g.,/student/grade) extracted also from
the object map, as described previously. Simultaneously, in cases of multiple
components templates (e.g., http://example.com/{@id}
{name}) where multiple
XPaths are implicated and multiple shapes are involved, we manage them as a
list (e.g., [/student/@id, /student/name]) for future adjustment.
Adjustment. We adjust the classes, properties, and constraints within the pre-
liminary shapes to align with the target RDF graph based on parsing outcomes

224 X. Duan et al.
Table 1. Focus node and property value extraction for equivalences identiﬁcation.
Extraction Resultant mapping
?S a sh:NodeShape
?S sh:targetClass | sh:targetNode |
sh:targetSubjectsOf | sh:targetObjectsOf
?node
focusNode[S]=node
?S sh:node* ?S2 focusNode[S2]+=focusNode[S]
?S a sh:PropertyShape
?S sh:targetClass | sh:targetNode |
sh:targetSubjectsOf | sh:targetObjectsOf ?fn
?S sh:path ?node
propertyValue[S]=(?fn,?node)
if focusNode[S]:
?S sh:property ?PS ?PS sh:path ?node
propertyValue[PS]=(focusNode[S],?node)
from both RML and SHACL, and showcase the example in Fig.2. For each class
and property (e.g., stu:grade) associated with the XPath (e.g., /student/grade)
within the RML parsing results, we look for the corresponding shape identi-
ﬁer (e.g., http://example.com/PropertyShape/studentType/grade) that shares the
same XPath in the SHACL parsing results. If found, we update the target dec-
laration (i.e. sh:targetClass) or property path (i.e. sh:path) with the class or
property (e.g., stu:grade) deﬁned in RML. Ultimately, we eliminate shapes that
remain unadjusted and are not referenced by the adjusted shapes.
In addition to aligning classes and properties, we speciﬁcally create a new
shape for templates with multiple references to the raw data schema (e.g.,
http://example.com/{id}
{name}). As that template involves multiple shapes
derived from the raw data schema, one for each XPath expression in the tem-
plate, the constraints originally present in individual shapes may no longer be
valid. For instance if, on the one hand, we have string-based constraints (e.g.,
sh:pattern) and, on the other hand, the sh:datatype is an integer, not both con-
straints may be retained. After parsing the RML mappings, the XPath list is
retrieved.
Moreover, in the presence of cardinality constraints (e.g.,sh:minCount 2 and
sh:minCount 3 ) across all pertinent shapes, these constraints are multiplied to cal-
culate the cardinality constraint (e.g.,sh:minCount 6 ) for the merged shape. Sim-
ilarly, if length constraints are present in all relevant shapes (e.g., sh:minLength
3 for id and sh:minLength 1 for name in the template above), the cumulative sum
(e.g., sh:minLength 24 ), considering the length of the string outside the compo-
nent in the template (e.g., length of 20 for http://example.com/
), is added.
4.2 Equivalences Identiﬁcation
To determine the constraints within shapes that should be integrated, we identify
the equivalent shapes, i.e. the shapes designated for validating either the same
focus node or the identical property value reached via the same focus node.

SCOOP All the Constraints’ Flavours for Your Knowledge Graph 225
Fig. 3. An example process of theequivalences identiﬁcation module. Identiﬁers of
the same color refer to equivalent shapes.
We traverse the shapes from diverse sources that are intended for integration,
sequentially evaluating the following four scenarios, as delineated in Table 1,
to ascertain equivalency: (i) the present focus nodes of the node shape that
deﬁnes the target declaration; (ii) the cumulative focus nodes of shapes refer-
enced through sh:node by other shapes that possess focus nodes; (iii) the directly
deﬁned property path with focus nodes; and (v) the property path of the prop-
erty shape referenced by the node shape with focus nodes through sh:property.
Utilizing these outcomes, shapes sharing identical focus nodes or property values,
derived from disparate sources, are recognized as equivalent shapes.
Figure3 presents an example of equivalences identiﬁcation, emphasizing the
necessity of considering four scenarios. The ﬁrst scenario’s equivalences calcu-
lation facilitates the determination of the focus nodes directly deﬁned by node
shapes (e.g.,<student> sh:targetClass stu:Student). The second scenario’s equiva-
lence calculation prevents the oversight of focus nodes indirectly deﬁned through
sh:node reference relationships (e.g., <student> sh:node <studentType>). The
third scenario assists in identifying the focus node and property value pair
that is directly deﬁned within the same property shape (e.g., <studentPS>
sh:targetClass stu:Student , sh:path stu:grade ). The fourth scenario aids in deter-
mining the property value reached through thesh:property reference relationship
from the focus node (e.g., <studentShape> sh:property <gradeShape>).
4.3 Integration and Inconsistencies Resolution
To provide a variety of integration possibilities, we devised three approaches:
SCOOP-All, SCOOP-Prior, and SCOOP-Prior-R. All aims to integrate all con-
straints from all equivalent shapes, Prior aims to integrate constraints from
lower-priority shapes that are not inconsistent with higher-priority equivalent

226 X. Duan et al.
Table 2. The inconsistent combination of constraints slated for addition and the cor-
responding constraints within the presently integrated shape.
Constraints to be added Inconsistent constraints
sh:datatype sh:nodeKind isnot sh:Literal
sh:nodeKind is (sh:IRIOrLiteral or sh:datatype or sh:languageIn or
sh:IRI or sh:BlankNodeOrLiteral or sh:minExclusive or sh:minInclusive or
sh:BlankNode or sh:BlankNodeOrIRI) sh:maxExclusive or sh:maxInclusive
sh:minCount > sh:maxCount
sh:maxCount < sh:minCount
sh:minExclusive sh:nodeKind isnot sh:Literal or
≥ sh:maxExclusive or ≥ sh:maxInclusive
sh:minInclusive sh:nodeKind isnot sh:Literal or
≥ sh:maxExclusive or > sh:maxInclusive
sh:maxExclusive sh:nodeKind isnot sh:Literal or
≤ sh:minExclusive or ≤ sh:minInclusive
sh:maxInclusive sh:nodeKind isnot sh:Literal or
≤ sh:minExclusive or < sh:minInclusive
sh:minLength sh:nodeKind isnot sh:Literal or > sh:maxLength
sh:maxLength sh:nodeKind isnot sh:Literal or < sh:minLength
shapes based on deﬁned source priority, andR is designed to ﬁlter out redundant
shapes from the ontology based on higher-priority shapes. We also introduce the
inconsistencies resolutions for All and Prior to harmonize all constraints within
equivalent shapes to be integrated, mitigating inconsistencies in the ﬁnal shape.
SCOOP and Resolution. For all algorithms, we initialize an empty graphS to
store the ﬁnal uniﬁed shapes. We consider the current shapes as the shape to be
added and the current constraintc as the constraint to be added. The constraints
deﬁned for shapes equivalent tos in S are denoted as C(s). For SCOOP-All, we
sequentially add s translated from diﬀerent sources. If an equivalent shape does
not exist inS, we directly adds to S. Otherwise, we perform constraint checks on
C(s)a n dc (explained in detail below). In cases where no inconsistencies are found,
we add c directly to C(s). Conversely, we reconstruct and integrate inconsistent
constraints using sh:or. For SCOOP-Prior, we traverse and adds into S based on
the user-deﬁned priorities of diﬀerent sources. Similarly, if an equivalent shape
does not exist inS, we directly adds to S, otherwise, we conduct an inconsisten-
cies check. However, in cases of ﬁnding an inconsistency, we refrain from addingc.
Unlike SCOOP-Prior, SCOOP-Prior-R refrains from addings that is translated
from ontology toS if there is no equivalent shape inS.
Inconsistencies Check. We perform two types of constraint checks: (i) inter-
nal checks based on the SHACL speciﬁcation [26], determining whether adding
c violates the constraint’s cardinality restriction (e.g., a shape cannot have two
sh:minLength), and (ii) external checks based on Table 2, verifying if there are
inconsistencies between C(s)a n dc (e.g., C(s) contains sh:nodeKind sh:IRI while
c deﬁnes sh:datatype xsd:string ). Speciﬁcally, we categorized the core constraints

SCOOP All the Constraints’ Flavours for Your Knowledge Graph 227
into those constraints permitting at most one appearance in a shape and those
allowing multiple occurrences. We consider it an inconsistency if there is a con-
straint in C(s) same as c that allows only one occurrence. All cases are outlined
in Table2.
4.4 Implementation
Algorithm 1: SCOOP implementation.
1 Function SCOOP(rml fi l e s = ∅, owl fi l e s = ∅, xsd fi l e s = ∅,
priority =[ ” rml”, ”owl”, ”xsd”], mode =[ ” All”, ”Pr i o r”, ”Pr i o r R”]):
2 shapes inorder, S ←∅ , Graph()
3 for source in priority do
4 if source is rml and rml fi l e s then
5 shapes ← RML2SHACL(rml fi l e s)
6 else if source is owl and owl fi l e s then
7 shapes ← OWL2SHACL(owl fi l e s)
8 else if source is xsd and xsd fi l e s then
9 xsd shapes ← XSD2SHACL(xsd fi l e s)
10 if rml fi l e s then
11 xsd shapes ← Post adjustment(shapes, rml fi l e s)
12 shapes inorder.add(shapes)
13 S ← shapes inorder[0]
14 for shape next in shapes inorder[1:] do
15 parseResults current ← Equivalences identiﬁcation (S)
16 parseResults next ← Equivalences identiﬁcation (shape next)
17 for parseResult in parseResults next do
18 if parseResult can be found in parseResults current then
19 S ← Inconsistencies resolution integration(S, shape next,
parseResult, parseResults current) // Check for inconsistencies
that may caused by constraints to be added and resolve them
20
21 else if mode is not Pr i o r R then
22 S ← addConstraints(shape next, parseResult) // Direct add the
corresponding shape with constraints since there is no equivalent
shape that may raise inconsistencies found in the current shape
23
24 return S
SCOOP integrates RML2SHACL [ 8], Astrea [ 4], and XSD2SHACL [ 11]t o
extract shapes from the mappings, ontology, and XSD respectively, implements
the post-adjustment, equivalences identiﬁcation, and integration and inconsis-
tencies resolution modules in the workﬂow (Fig. 1) as outlined in Algorithm
1, and provides conﬁguration options with SCOOP-All, SCOOP-Prior, and
SCOOP-Prior-R. SCOOP accepts ﬁles from diverse sources as input, with default
user-deﬁned priority that accords precedence to mappings over ontology and over
XSD, ultimately yielding a uniﬁed shapes graph. Besides, the SCOOP frame-
work can be expanded to incorporate shapes from supplementary sources, such
as CSVW and JSON Schema. The code and usage instructions for SCOOP are
available online on the GitHub repository:https://github.com/dtai-kg/SCOOP.

228 X. Duan et al.
5 Evaluation
We performed a comprehensive analysis, encompassing both performance and
coverage aspects, to evaluate the eﬀectiveness of SCOOP in addressing real-
world use cases and compared it with current state-of-the-art systems.
Systems. We selected a state-of-the-art system from each of the RDF graphs ,
ontologies, mappings,a n d raw data schemas -based systems for extracting
SHACL shapes to serve as a point of comparison. For theRDF graphs -based sys-
tem, we considered the available systems, including SHACLGEN [1], SheXer [19],
and QSE [ 30], ultimately opting for QSE. This selection was inﬂuenced by
QSE’s broader coverage of constraints compared to other systems [ 31]. For
the ontologies-based system, our considerations encompass Astrea [ 4] and the
OWL2SHACL conversion rules [20]. We ﬁnally selected Astrea due to the avail-
ability of detailed information on its implementation and performance [5], which
is absent for OWL2SHACL. For the systems based on mapping rules and raw
data schemas , we opted for RML2SHACL [8] and XSD2SHACL [11].
Datasets. To demonstrate our framework’s potential, we leverage the real-world
u s ec a s eR I N F[35], the railway infrastructure register published by each country,
containing the infrastructure parameters applied to the railway system. RINF
includes raw XML data from 30 countries, 28 RML ﬁles2, an ERA ontology from
version 3.0.0 [14], and an XSD from version 1.5 [36]. We arrange the XML data
from 30 countries in ascending order of size and progressively construct RDF
graphs using the RML mapping rules and the RMLMapper [24]. The minimum
RDF graph (0.003 GB) comprises solely the smallest XML dataset, while the
largest RDF graph (8.52 GB) incorporates data from all countries. The con-
structed RDF graphs serve as input for QSE.
Experimental Setup. We conduct all experiments on a Rocky 8.8 Linux based
system with Intel(R) Xeon(R) Gold 6140 CPUs running at 2.30 GHz, conﬁg-
ured with 128 GB RAM and 32 cores. We experimented with SCOOP v1.0.0 in
its diﬀerent conﬁgurations (i.e. SCOOP-All, SCOOP-Prior, and SCOOP-Prior-
R) under diﬀerent input combinations. We executed the RML2SHACL v1.0.0,
Astrea v1.2.1, and XSD2SHACL v1.0.0 systems as per the instructions outlined
in their repositories. Regarding QSE ( pvldb release), we ran QSE-Exact with
conﬁdence ≥25% and support ≥100%, and QSE-Approx with conﬁdence≥25%,
support ≥100%, sampling percentage of 50%, and reservoir size of 5000.
Performance Analysis. We evaluated the running time and maximum memory
usage of diﬀerent systems (average of 5 runs) in the RINF use case across diverse
data sizes. Figure 4 illustrates the running time and maximum memory usage
of diﬀerent systems, with both ﬁgures including only one QSE-Exact and one
SCOOP-Prior-R due to negligible diﬀerences between the various approaches.
Figure4b shows QSE and SCOOP exclusively, as the results for other systems
align closely with those of SCOOP.
2 The mapping rules will be publicly available soon by ERA (era.europa.eu/).

SCOOP All the Constraints’ Flavours for Your Knowledge Graph 229
Fig. 4. (a) Running time and (b) Maximum memory usage comparison across various
systems on the RINF use case.
Our experiments demonstrate that the memory usage of the QSE increases
approximately linearly with the size of the RDF graph, and the maximum mem-
ory usage of QSE is higher than SCOOP in all experiments. The running time of
QSE is higher than all non-RDF-based systems without post-adjustment when
the RDF graph’s size exceeds 0.10GB; is higher than XSD2SHACL with post-
adjustment when the graph size exceeds 2.73GB; and is higher than SCOOP
when the RDF graph’s size exceeds 3.30GB. The running time of SCOOP is pri-
marily inﬂuenced by the post-adjustment phase, while the triggering and integra-
tion of shapes incur relatively less time. SCOOP’s memory usage is independent
of the RDF graph’s size. SCOOP uses lower memory usage than QSE through-
out all experiments, and surpasses QSE in terms of running time when the RDF
graph’s size exceeds 3.30 GB, ensuring scalability for larger RDF graphs.
Coverage Analysis. We conducted a statistical analysis of the extracted shapes
concerning targeting suﬃcient classes and properties and generating rich con-
straints. We extracted the involved 21 classes and 223 properties of the largest
RDF graph (8.52 GB), which includes all raw data as the ground truth. We also
chose the shapes produced by QSE on this RDF graph for comparison.
We compared the classes deﬁned by the sh:targetClass and the properties
deﬁned by thesh:path referenced by shapes containing target declarations in the
extracted shapes with the ground truth to calculate precision (P), recall (R), and
F1 score. We also assessed the richness of constraints within shapes. Following
the SHACL speciﬁcation [27], we categorized SHACL core constraints into eight
categories: Value Type (VT), Value Range (VR), String-based (SR), Property
Pair (PP), Logical (LG), Shape-based (SA), Other (OT) which also includes
sh:name and sh:description, and analyze the coverage for each category. Table 3
show that SCOOP-Prior-R performs comparably to XSD2SHACL with our post-
adjustment module, and surpasses all other systems in deﬁning suﬃcient classes
and properties. SCOOP-All generates the richest constraints, and all SCOOP
systems surpass QSE by generating more than twice the types of constraints.

230 X. Duan et al.
Table 3. The precision (P), recall (R), and F1 score on the extracted classes and
properties, and the coverage of constraints: Value Type (VT), Cardinality Constraint
(CD), Value Range (VR), String-based (SR), Property Pair (PP), Logical (LG), Shape-
based (SA), Other (OT). PA refers to the post-adjustment.
Systems Classes Properties Core Constraints
P R F1 P R F1 VT CD VR SR PP LG SA OT Total
QSE-Exact 1.0 1.0 1.0 1.0 0.44 0.61 2100001 2 7
QSE-Approx 1.0 1.0 1.0 1.0 0.44 0.61 2100001 2 7
RML2SHACL 1.0 1.0 1.0 1.0 0.26 0.41 20010020 5
Astrea 0.45 1.0 0.62 0.44 0.94 0.60 3 101 12 4 2 14
XSD2SHACL+PA 1.0 1.0 1.0 0.98 1.0 0.99 2 2 020021 9
SCOOP
All
rml+owl 0.45 1.0 0.62 0.45 0.98 0.62 3 101 1252 15
rml+xsd 1.0 1.0 1.0 0.98 1.0 0.99 2 2 0 3 0121 1 1
rml+owl+xsd 0.45 1.0 0.62 0.45 1.0 0.62 32 0 31252 1 8
SCOOP
Prior
rml+owl 0.45 1.0 0.62 0.45 0.98 0.62 3 101 1 1 52 14
rml+xsd 1.0 1.0 1.0 0.98 1.0 0.99 2 2 0 3 0021 1 0
rml+owl+xsd 0.45 1.0 0.62 0.45 1.0 0.62 32 0 31 1 52 17
SCOOP
Prior-R
rml+owl 1.0 1.0 1.0 1.0 0.26 0.41 3 101 00 52 12
rml+xsd 1.0 1.0 1.0 0.98 1.0 0.99 2 2 0 3 0021 1 0
rml+owl+xsd 1.0 1.0 1.0 0.98 1.0 0.99 32 0 3 00 52 15
Coverage Analysis in Classes. Examining the outcomes for the targeted classes,
QSE and systems involving RML demonstrate the capability of perfectly target-
ing classes. The exceptional performance of QSE in class extraction is foresee-
able, given its input is the target RDF graph. Among the non-RDF-systems,
RML2SHACL beneﬁts from RML, aligning perfectly with the target RDF
graph’s classes. Our implemented post-adjustment helps XSD2SHACL to cap-
ture information from RML, thereby achieving full scores across all metrics.
However, Astrea exhibits lower precision, a common issue in systems extracting
shapes from ontologies, because ontologies cover the entire domain but the target
RDF graph may only involve a subset, resulting in many unnecessary shapes.
In the case of the SCOOP-All and SCOOP-Prior, the inclusion of the entire
ontology negatively impacts the precision where SCOOP-Prior-R is speciﬁcally
designed to mitigate the issue of redundant shapes generated by ontologies. The
results demonstrate that SCOOP-Prior-R achieves full scores across all metrics
for all input combinations, indicating its stronger robustness.
Coverage Analysis in Properties. In terms of targeted properties, SCOOP
exhibits superior overall performance compared to other systems. The low recall
scores of QSE indicate that they omit many properties during the shape extrac-
tion process. We attribute this to their novel extraction method based on support
and conﬁdence score, which, in an attempt to ﬁlter out spurious shapes, also ﬁl-
ter out some properties present in the RDF graph. The low recall values observed
in RML2SHACL can be attributed to instances where certain property shapes
lack references from target declarations. This is attributed to implicit class def-

SCOOP All the Constraints’ Flavours for Your Knowledge Graph 231
initions in our RML use case, where multiple triples maps are involved, with
only one explicitly deﬁning the class, while the others imply its existence using
the same subject map. However, RML2SHACL fails to capture this implicit def-
inition, resulting in the oversight of certain reference relationships. In contrast,
our post-adjustment module combined with XSD2SHACL performs well and
does not encounter this issue because we considered implicit class deﬁnitions
when parsing RML, and the precision of 0.98 suggests that the generated RDF
graph may not have produced some expected triples due to missing raw data.
In addition, Astrea’s lower precision score in property extraction is ascribed to
the ontology’s broader coverage of properties. The performance of all SCOOP
approaches with RML and XSD as inputs overcomes all other systems.
Coverage Analysis in Constraints. The analysis of core constraints conﬁrms the
outstanding performance of SCOOP in terms of constraint richness. The shapes
extracted by SCOOP-All encompass a total of 18 distinct constraints, slightly
surpassing SCOOP-Prior, SCOOP-Prior-R, and Astrea, marginally higher than
XSD2SHACL, and markedly superior to both QSE and RML2SHACL. Further-
more, with regard to the SCOOP-All, we conducted a ﬁne-grained analysis of
the contributions of diﬀerent sources to the ﬁnal constraints. Among the 18 ﬁnal
constraints, 5 originate from RML, 14 from the ontology, and 9 from XSD. In
particular, the ontology covers property pair constraints (e.g., sh:equals)a n d
logical constraints (e.g., sh:not) not covered by other sources.
Practical Implications on Validation. We assessed the eﬀectiveness of
SCOOP to extract valid SHACL shapes by validating an RDF graph using
those shapes. We used the pySHACL validator [ 37] to validate the smallest
RDF graph (0.003 GB, 1620 triples) constructed from RINF. Due to violations
of SHACL syntax in shapes generated by QSE, e.g., multiple occurrences of
sh:in, and Astrea, e.g., missing sh:path, we could not directly use their shapes
for validation.
The validation results indicated that the target RDF graph conformed to all
shapes generated by RML2SHACL but violated shapes generated by other sys-
tems. Speciﬁcally, the shapes extracted by XSD2SHACL revealed 738 missing
triples and 540 error triples (e.g., sh:maxLength, sh:datatype,a n dsh:nodeKind).
We analyzed the additional violations found by XSD2SHACL, attributing them
to lingering issues from mismatched versions of XSD and RML. SCOOP-Prior
and SCOOP-R, incorporating the mapping rules, ontology, and XSD, discovered
738 missing triples and 972 error triples (involving sh:class and sh:maxLength).
We attribute this to the introduction of constraints from the ontology, distin-
guishing it from XSD2SHACL. SCOOP-All, including all sources, also identi-
ﬁed 738 missing triples but labeled 864 error triples (involving only sh:class),
slightly fewer than SCOOP-Prior. This was reasonable as SCOOP-All’s strategy
of adding sh:or introduces more lenient constraints to the RDF graph. In sum-
mary, this experiment demonstrates that our SCOOP framework strictly adheres
to SHACL syntax, and provides users with eﬀective RDF validation results.

232 X. Duan et al.
6 Conclusion
In this paper, we propose SCOOP, an open-source framework designed to inte-
grate existing shape extraction systems targeting diverse sources into a uniﬁed
and comprehensive shapes graph. SCOOP consists of three modules and devises
three integration approaches to provide diverse choices. The implementation of
SCOOP includes the incorporation of RML2SHACL, Astrea, and XSD2SHACL.
SCOOP exhibits signiﬁcantly lower memory usage compared to RDF-based sys-
tems, performs faster when the RDF graph exceeds 3.30 GB in size, and outper-
forms state-of-the-art systems in extracting eﬀective node and property shapes
and generating richer constraints.
SCOOP is an extensible framework that goes beyond current sources and sys-
tems, including ontologies, mapping rules, and raw data schemas. The method-
ology is transferable to any SHACL shapes extraction work, therefore, seamless
integration with other systems can be easily achieved. In the future, we will
extend SCOOP to a broader range of sources, e.g., CSVW, JSONSchema, etc.
SCOOP enables users to extract SHACL shapes eﬀortlessly, without even
having to construct the RDF graphs using hardware with limited resources. It
is expected that this framework will have a high impact on the Semantic Web
community as most RDF graphs nowadays are constructed from various data.
Acknowledgement. Xuemin Duan and Anastasia Dimou are partially supported by
Flanders Make, the research centre for the manufacturing industry, and the Flanders
innovation and entrepreneurship (VLAIO) through the KG3D project. David Chaves-
Fraga is funded by the Galician Ministry of Education, University and Professional
Training and the European Regional Development Fund (ERDF/FEDER program)
through grants ED431C2018/29 and ED431G2019/04. The resources and services used
in this work were provided by the VSC (Flemish Supercomputer Center), funded by
the Research Foundation - Flanders (FWO) and the Flemish Government.
References
1. Arndt, N.: SHACLGEN. https://github.com/AKSW/shaclgen. Accessed 20 Sept
2023
2. Bock, C., et al.: OWL 2 Web Ontology Language – Structural Speciﬁcation and
Functional-Style Syntax, 2nd edn. Recommendation, World Wide Web Consortium
(W3C) (2012). http://www.w3.org/TR/owl2-syntax/
3. Boneva, I., Dusart, J., Fern´andez Alvarez, D., Gayo, J.E.L.: Shape designer for
ShEx and SHACL constraints. In: Proceedings of the ISWC 2019 Satellite Tracks
(Poster & Demonstrations, Industry, and Outrageous Ideas), vol. 2456, pp. 269–
272. CEUR (2019)
4. Cimmino, A.: Astrea. https://github.com/oeg-upm/astrea. Accessed 20 Sept 2023
5. Cimmino, A., Fern´andez-Izquierdo, A., Garc´ıa-Castro, R.: Astrea: automatic gen-
eration of SHACL shapes from ontologies. In: Harth, A., et al. (eds.) ESWC 2020.
LNCS, vol. 12123, pp. 497–513. Springer, Cham (2020). https://doi.org/10.1007/
978-3-030-49461-2
29

SCOOP All the Constraints’ Flavours for Your Knowledge Graph 233
6. Comelli, T.: JS2SHACL - JSON schema to SHACL conversor. https://github.
com/ThiagoCComelli/JS2SHACL-JSON-Schema-to-SHACL-conversor. Accessed
20 Sept 2023
7. Das, S., Sundara, S., Cyganiak, R.: R2RML: RDB to RDF mapping language.
Working group recommendation, World Wide Web Consortium (W3C) (2012).
http://www.w3.org/TR/r2rml/
8. Delva, T.: RML2SHACL. https://github.com/RMLio/RML2SHACL. Accessed 20
Sept 2023
9. Delva, T., Smedt, B.D., Min Oo, S., Assche, D.V., Lieber, S., Dimou, A.:
RML2SHACL: RDF generation taking shape. In: Proceedings of the 11th on
Knowledge Capture Conference, pp. 153–160. ACM (2021). https://doi.org/10.
1145/3460210.3493562
10. Dimou, A., Vander Sande, M., Colpaert, P., Verborgh, R., Mannens, E., Van de
Walle, R.: RML: a generic language for integrated RDF mappings of heterogeneous
data. In: Proceedings of the 7th Workshop on Linked Data on the Web, vol. 1184.
CEUR Workshop Proceedings (2014)
11. Duan, X.: XSD2SHACL (2023). https://doi.org/10.5281/zenodo.8318452.
Accessed 20 Sept 2023
12. Duan, X., Chaves-Fraga, D., Dimou, A.: XSD2SHACL: capturing RDF constraints
from XML schema. In: Proceedings of the 12th Knowledge Capture Conference
2023, K-CAP 2023, pp. 214–222. Association for Computing Machinery (2023).
https://doi.org/10.1145/3587259.3627565
13. Ekaputra, F.J., et al.: Describing and organizing semantic web and machine learn-
ing systems in the SWeMLS-KG. In: Pesquita, C., et al. (eds.) ESWC 2023. LNCS,
vol. 13870, pp. 372–389. Springer, Cham (2023). https://doi.org/10.1007/978-3-
031-33455-9
22
14. European Union Agency for Railways: ERA vocabulary. https://data-interop.era.
europa.eu/era-vocabulary/. Accessed 20 Sept 2023
15. Fallside, D., Walmsley, P.: XML Schema Part 0: Primer Second Edition. Recom-
mendation, W3C (2004). https://www.w3.org/TR/xmlschema-0/
16. Felin, R., Faron, C., Tettamanzi, A.G.B.: A framework to include and exploit
probabilistic information in SHACL validation reports. In: Pesquita, C., et al. (eds.)
ESWC 2023. LNCS, vol. 13870, pp. 91–104. Springer, Cham (2023). https://doi.
org/10.1007/978-3-031-33455-9
6
17. Fern´andez-´Alvarez, D., Garc´ıa-Gonz´alez, H., Frey, J., Hellmann, S., Gayo, J.E.L.:
Inference of latent shape expressions associated to DBpedia ontology. In: Pro-
ceedings of the ISWC 2018 Posters & Demonstrations, Industry and Blue Sky
Ideas Tracks Co-Located with 17th International Semantic Web Conference (ISWC
2018), vol. 2180. CEUR Workshop Proceedings (2018)
18. Fernandez- ´Alvarez, D., Labra-Gayo, J.E., Gayo-Avello, D.: Automatic extraction
of shapes using sheXer. Knowl.-Based Syst. 238, 107975 (2022). https://doi.org/
10.1016/j.knosys.2021.107975
19. Fern´andez-´Alvarez, D.: sheXer. https://github.com/DaniFdezAlvarez/shexer.
Accessed 10 Nov 2023
20. Francart, T.: OWL2SHACL. https://github.com/sparna-git/owl2shacl. Accessed
10 Nov 2023
21. Garcia-Gonzalez, H., Labra-Gayo, J.E.: XMLSchema2ShEx: converting XML val-
idation to RDF validation. Semant. Web11(2), 235–253 (2020)
22. Ghiasnezhad Omran, P., Taylor, K., Rodr´ ıguez M´endez, S., Haller, A., et al.:
Towards SHACL learning from knowledge graphs. In: Proceedings of the ISWC

234 X. Duan et al.
2020 Demos and Industry Tracks: From Novel Ideas to Industrial Practice Co-
Located with 19th International Semantic Web Conference (ISWC 2020), vol. 2721,
pp. 94–99. CEUR Workshop Proceedings (2020)
23. Pandit, H.J., O’Sullivan, D., Lewis, D.: Using ontology design patterns to deﬁne
SHACL shapes. In: 9th Workshop on Ontology Design and Patterns (WOP 2018),
vol. 2195, pp. 67–71. CEUR-WS, Monterey (2018)
24. Heyvaert, P., Meester, B.D., et al.: RMLMapper-Java. https://github.com/
RMLio/rmlmapper-java. Accessed 20 Sept 2023
25. Iglesias-Molina, A., et al.: The RML ontology: a community-driven modular
redesign after a decade of experience in mapping heterogeneous data to RDF.
In: Payne, T.R., et al. (eds.) ISWC 2023, Part II. LNCS, vol. 14266, pp. 152–175.
Springer, Cham (2023). https://doi.org/10.1007/978-3-031-47243-5
9
26. Knublauch, H., Kontokostas, D.: SHACL-SHACL. http://www.w3.org/ns/shacl-
shacl#. Accessed 01 Dec 2023
27. Knublauch, H., Kontokostas, D.: Shapes constraint language (SHACL). Recom-
mendation, W3C (2017). https://www.w3.org/TR/shacl/
28. Mihindukulasooriya, N., Rashid, M.R.A., Rizzo, G., Garcia-Castro, R., Corcho,
O., Torchiano, M.: RDF shape induction using knowledge base proﬁling. In: Pro-
ceedings of the 33rd ACM/SIGAPP Symposium on Applied Computing (2017)
29. Pandit, H.J., O’Sullivan, D., Lewis, D.: Using ontology design patterns to deﬁne
SHACL shapes. In: Proceedings of the 9th Workshop on Ontology Design and Pat-
terns (WOP 2018) Co-Located with 17th International Semantic Web Conference
(ISWC 2018), vol. 2195, pp. 67–71. CEUR (2018)
30. Rabbani, K.: Quality shapes extraction (QSE). https://github.com/dkw-aau/qse.
Accessed 20 Sept 2023
31. Rabbani, K., Lissandrini, M., Hose, K.: Extraction of validating shapes from very
large knowledge graphs [extended version]
32. Rabbani, K., Lissandrini, M., Hose, K.: SHACL and ShEx in the wild: a community
survey on validating shapes generation and adoption. In: Companion Proceedings
of the Web Conference 2022, WWW 2022, pp. 260–263. Association for Computing
Machinery (2022). https://doi.org/10.1145/3487553.3524253
33. Rabbani, K., Lissandrini, M., Hose, K.: Extraction of validating shapes from very
large knowledge graphs. Proc. VLDB Endow. 16(5), 1023–1032 (2023)
34. Rabbani, K., Lissandrini, M., Hose, K.: SHACTOR: improving the quality of large-
scale knowledge graphs with validating shapes. In: Proceedings of the 2023 Inter-
national Conference on Management of Data (SIGMOD-Companion 2023), pp.
151–154. Association for Computing Machinery (2023). https://doi.org/10.1145/
3555041.3589723
35. The RINF: RINF: Railway infrastructure register. https://www.rinf-ch.ch/.
Accessed 01 Dec 2023
36. The RINF: RINF XML Schema v1.5. https://www.era.europa.eu/domains/
registers/rinf
en. Accessed 01 Dec 2023
37. Sommer, A., Car, N.: pySHACL (2022). https://doi.org/10.5281/zenodo.4750840.
https://github.com/RDFLib/pySHACL
38. Spahiu, B., Maurino, A., Palmonari, M.: Towards improving the quality of knowl-
edge graphs with data-driven ontology patterns and SHACL. In: Workshop on
Ontology Design Patterns (WOP) at ISWC (Best Workshop Papers). CEUR Work-
shop Proceedings, vol. 2195, pp. 52–66. CEUR (2018)
39. Thapa, R.B., Giese, M.: A source-to-target constraint rewriting for direct mapping.
In: Hotho, A., et al. (eds.) ISWC 2021. LNCS, vol. 12922, pp. 21–38. Springer,
Cham (2021). https://doi.org/10.1007/978-3-030-88361-4
2

FidMark: A Fiducial Marker Ontology
for Semantically Describing Visual
Markers
Maxim Van de Wynckel(B) , Isaac Valadez , and Beat Signer
Web & Information Systems Engineering Lab, Vrije Universiteit Brussel,
Pleinlaan 2, 1050 Brussels, Belgium
{mvdewync,jvaladez,bsigner}@vub.be
Abstract. Fiducial markers are visual objects that can be placed in the
ﬁeld of view of an imaging sensor to determine its position and orienta-
tion, and subsequently the scale and position of other objects within the
same ﬁeld of view. They are used in a wide variety of applications rang-
ing from medical applications to augmented reality (AR) solutions where
they are applied to determine the location of an AR headset. Despite the
wide range of diﬀerent marker types with their advantages for speciﬁc
use cases, there exists no standard to decide which marker to best use
in which situation. This leads to proprietary AR solutions that rely on a
predeﬁned set of marker and pose detection algorithms, preventing inter-
operability between AR applications. We propose the FidMark ﬁducial
marker ontology, classifying and describing the diﬀerent markers avail-
able for computer vision and augmented reality along with their spatial
position and orientation. Our proposed ontology also describes the pro-
cedures required to perform pose estimation, and marker detection to
allow the description of algorithms used to perform these procedures.
With FidMark we aim to enable future AR solutions to semantically
describe markers within an environment so that third-party applications
can utilise this information.
Keywords: ﬁducial marker
· ontology · augmented reality · pose
estimation
Resource type Ontology
License CC BY-SA 4.0
URL https://purl.org/ﬁdmark/
Documentation https://ﬁdmark.openhps.org/1.0/en/
Demonstrator https://ﬁdmark.openhps.org/application/
Repository https://github.com/OpenHPS/FidMark/
DOI 10.5281/zenodo.10730905
1 Introduction
In computer vision applications, or more speciﬁcally augmented reality (AR)
solutions, superimposing virtual objects in real-world scenes poses a challenge
c⃝ The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
A. Mero˜no Pe˜nuela et al. (Eds.): ESWC 2024, LNCS 14665, pp. 235–250, 2024.
https://doi.org/10.1007/978-3-031-60635-9_14

236 M. Van de Wynckel et al.
due to the lack of an accurate absolute position of the camera in the physi-
cal world. Various methods can be employed, such as creating virtual anchors
based on visual features [7], anchoring these virtual objects to an absolute loca-
tion based on GPS or indoor positioning systems [33] or using predeﬁned visual
landmarks that can be used as a spatial reference [ 26]. These landmarks, often
referred to as ﬁducial markers, are used to determine the position and orien-
tation (i.e. a pose) of an image sensor detecting these markers within its ﬁeld
of view [ 25]. While markers can be used to track the position of a camera or
AR device, they can also help to position and scale virtual objects relative to
these markers.
Applications using ﬁducial markers to determine a pose need to be able to
detect and map the markers to their known position and orientation, which often
requires a proprietary local or cloud-based database to retrieve this contextual
information. In addition, the vast variety of available marker types [20,23], each
with their own set of properties that are required to detect and identify these
markers, make it diﬃcult to generically deﬁne the contextual information of a
marker.
Looking at existing ontologies and vocabularies, the Digital Imaging and
Communications in Medicine (DICOM) ontology [19] describes ﬁducial markers
and identiﬁers used within the medical ﬁeld for use cases such as providing a
visual landmark when performing radiology. Despite of being a domain-speciﬁc
ontology, DICOM deﬁnes some generic concepts that are also found in ﬁducial
markers for other applications. In the Machine-to-Machine Measurement (M3)
Lite ontology, a description for the concept of a m3lite:TagDevice and tag
device types such as a QR code or barcode are provided [12]. However, similar to
the Schema.org vocabulary [11] also providing concepts for a generic barcode, it
does not provide concepts for identifying diﬀerent types of markers or individual
markers for a speciﬁc type of marker.
When focusing on AR applications, ﬁducial markers are used for position and
orientation tracking using both outside-in [35] and inside-out tracking [10]. With
inside-out tracking, markers are placed within the physical environment and
tracked by an AR device’s image sensor. On the other hand, in outside-in track-
ing, markers are placed on a moving object such as a person, with ﬁxed image
sensors in the physical environment tracking these markers. Diﬀerent marker
types and variations exist that perform better depending on the environmental
conditions such as scanning distance, scanning angle, light conditions or motion
blur [5]. This makes it impossible to rely on a single type of ﬁducial marker when
used for AR applications.
In order to support the interoperability of computer vision and augmented
reality applications using ﬁducial markers, we propose the FidMark ontology
that can semantically describe these individual markers as well as provide an
annotated description on various marker types. Our ontology can describe the
main properties of markers and their pose within a deﬁned reference space.
Being able to describe ﬁducial markers and their position within a physical space
allows multiple actors to understand the semantics of a visible marker and even

FidMark: A Fiducial Marker Ontology 237
allows them to detect these markers. This enables future interoperability between
augmented and mixed reality applications by describing a common reference
frame relative to a marker.
We start by presenting our design approach and several design goals for our
FidMark ontology in Sect. 2. The design of the FidMark ontology with some
examples is introduced in Sect. 3. Finally, a validation of the FidMark ontology
and discussion of a demonstrator application in Sect. 4 is followed by some
conclusions and plans for future work.
2 Approach and Methodology
Our design approach for the requirements of our ontology is based on the Linked
Open Terms (LOT) methodology [ 31]. Due to the already existing ontologies
for describing ﬁducial markers in medical sciences [ 19], we decided to focus on
ﬁducial markers used within the domain of computer vision (CV), primarily for
markers which can be used for pose estimation [27] that obtains both a position
and orientation. We started by analysing the diﬀerent existing types of markers
for applications within the domain of computer vision [20,23]. Next, using this set
of diﬀerent markers with their use cases for diﬀerent scenarios and environmental
conditions, we have listed a set of use cases, design goals and required data for
each type of marker.
Based on the marker analysis and their data properties, we determined the
common attributes and properties of each marker. Two of the main common
properties of each marker are the inclusion of an identiﬁer and its ability to be
used to determine a pose. Depending on the type of encoding and error correc-
tion, these markers use a dictionary that contains a set of possible identiﬁers
that can be encoded within the marker. Computer vision applications that want
to detect these markers should know which dictionary is used to perform the
correct identiﬁcation.
For the terminologies used for these data properties, we relied on common
terms used within academic research as well as the standardisation of ﬁducials
and their intrinsic properties for various domains [14–17]. We also investigated
frameworks and libraries that scan for markers and the variable names that were
used for expressing the data [1,4].
2.1 Design Goals
In the following, we list the main design goals (DG1–DG7) we aim to achieve
with our ontology. These goals will be used to scope our ontology to the required
functionality and serve as a basis for the implementation and validation of the
FidMark ontology.
DG1 Enable the retrieval of a list of supported markers : This design goal should
enable applications to retrieve individual markers that are detectable by
the hardware and software.

238 M. Van de Wynckel et al.
DG2 Enable the retrieval of markers using the identiﬁable information : This
design goal should enable applications to retrieve marker information
based on visually detectable and identiﬁable information such as the
marker identiﬁer or encoded data.
DG3 Enable the description of a marker with a non-standard symbology :I n
order to enable scalability for the ontology and marker types, variations
on the symbology should be possible.
DG4 Enable pose estimation of markers based on their description without ambi-
guity: Two actors, each with their own marker detection implementation
should be able to use all the available information to provide equal pose
estimation for the same semantically described marker.
DG5 Enable the positioning of virtual objects relative to a marker : It should be
possible to superimpose virtual objects around a marker, without having
to to know where the marker is located in the physical space.
DG6 A marker should be used as an engineering reference frame or image coor-
dinate reference system [15,16]: The marker should be used as a landmark
when performing visual positioning. This entails that the marker should
enable absolute pose estimation for an image sensor.
DG7 Facilitate the integration of computer vision markers in frameworks :H a v -
ing a semantic description of a marker is required to decide what algo-
rithms to use to detect and identify the marker. However, to further facili-
tate the detection, information should be available to decide what marker
types to use and how to integrate them into a computer vision framework
without having to perform a manual mapping. This in turn also relies on
design goal DG4 that requires the detection of markers without ambiguity,
as it also means that the description of a ﬁducial marker should not be
framework dependent.
Each design goal poses its challenges. While we can determine multiple com-
mon properties for each marker type in our ontology design as shown later in
Sect.3.1, ensuring that markers can be described without ambiguity such as dif-
ferent marker origins (e.g. using the centre of the marker as the origin of its
position) also requires a more detailed description of the necessary detection
processes.
3 Ontology Design
As outlined in our approach, the proposed FidMark ontology is primarily
designed to describe ﬁducial markers used in augmented reality (AR). However,
one of our design goals is to ensure that our ontology can easily be extended and
aligned to also describe ﬁducial markers for other domains.
In order that markers can be used for pose estimation, we have built our
ontology on top of the generic Positioning System Ontology (POSO) [ 40] that
can already describe visual landmarks with their spatial location and orientation.
POSO allows us to add both absolute positions and relative positions to spatial

FidMark: A Fiducial Marker Ontology 239
objects, enabling the positioning of (virtual) objects relative to a marker. We
expanded POSO to support diﬀerent types and classiﬁcations of ﬁducial markers,
their identiﬁers, image descriptors and calibration data. In addition, we also
added two procedures to diﬀerentiate between markerless [28] and marker-based
pose estimation via the poso:PositioningTechnique concept.
Fig. 1. FidMark main classes
The main classes of our FidMark ontology are illustrated in Fig.1. We make
a clear classiﬁcation of active and passive markers [ 29] as this represents the
major diﬀerence between diﬀerent types of markers. We further subclassed pas-
sive markers into barcodes that can encode information such as an identiﬁer. In
addition to these main classes, we currently provide over 30 diﬀerent types of
markers as subclasses of the ﬁducial marker class
1, such as reacTIVision [21]o r
CCTag [5].
With our ontology we aim to describe diﬀerent markers, their setup and
their position relative to a certain reference space. The basic architecture and a
use case for our ontology is demonstrated in Fig. 2. We describe markers, their
identiﬁer, position and orientation using the combination of FidMark and POSO.
FidMark handles the description of the markers while POSO is used to describe
the markers’ absolute and relative position as visual landmarks. AR-capable
devices with access to this description can synchronise their reference frame due
to the common description. Any virtual object placed relative to these markers
can again use the generality of POSO to indicate its relative position.
In our ontology, each type of ﬁducial marker is annotated with additional
metadata describing the markers’ visual and functional properties such as their
shape, colour and encoding method. When available in OpenCV [ 4], we also
provide the dictionary names of markers as they are available in OpenCV to
facilitate the development as outlined in design goal DG7.
1 For more information about the ontology proﬁle and ontology statistics, please check
the online documentation.

240 M. Van de Wynckel et al.
Fig. 2. Basic usage of FidMark together with the POSO ontology
To demonstrate the generality of FidMark for applications outside the domain
of augmented reality, we provide thefidmark-dicom alignment ontology to align
ﬁducial markers and POSO with the Digital Imaging and Communications in
Medicine (DICOM) ontology [19] in our supplemental material.
3.1 Properties and Terminologies
Fiducial markers have a set of properties that are subproperties of properties on
sosa:FeatureOfInterest from the Sensors, Observations, Systems and Actu-
ators (SOSA) ontology [ 18]. They deﬁne how the marker should be detected,
decoded and mapped to its location within the physical space. With ﬁducial
markers being used to determine the relative translation, scale or orientation of
visual objects within the ﬁeld of view. The object and data properties we added
to our ontology are also chosen to enable this description.
We provide the :hasOrigin predicate and :MarkerOrigin property to indi-
cate the position origin on the marker itself. This origin determines the 2D or
3D location on the ﬁducial marker. An origin description is required to deter-
mine the accurate translation when performing relative positioning from virtual
objects relative to the marker.
– dictionary: A set of marker identiﬁers that are available using a speciﬁed
encoding scheme. A dictionary is also referred to as a marker symbology or
marker family [17]. This encoding scheme can be generalised to both binary
encoding in barcodes as well as the encoding with active markers such as
infrared markers [37].

FidMark: A Fiducial Marker Ontology 241
Fig. 3. Relative positioning of virtual objects and markers
– origin: The origin of the marker is an important design requirement in
order to determine the relative orientation and translation to the marker.
Our :hasOrigin predicate and :MarkerOrigin property are based on the
OpenCV pattern. In Fig. 3, we illustrate how a virtual object is positioned
relative to the :MarkerOrigin. The marker itself can be positioned relative
to a known coordinate reference system or relative to other objects such as a
room or building.
– dimensions: The known dimensions of a marker can be used to determine
its scale. Our ontology supports the speciﬁcation of both, a marker’s width
and height to support rectangular markers such as AprilTag [30].
– hamming distance : The minimum hamming distance between two codes,
represented by the minimum number of bits that must be changed in one
tag’s code to reach another tag’s code.
– image descriptor : The marker image descriptor links to an image URI or
a Base64 representation of the image. Alternatively, the image descriptor
can be described as a processed descriptor for natural feature tracking [3]a s
illustrated in Fig.4.
– identiﬁer: A numeric identiﬁer that can uniquely identify a marker from a
(pre-)deﬁned dictionary. The identiﬁer is (part of) the encoded data.
– data: Other than an identiﬁer, some marker types allow the encoding of other
types of binary data. An example of such a marker is a QR code, which can
be used for both, pose estimation as well as the encoding of binary data.
– codes & marker bits : Frameworks with no prior knowledge of the concept
of a dictionary or how it is computed require a list of all available codes that
can be encoded with the available :markerBits and error correction.
Fig. 4. Image descriptor usage for markers
For a complete list of properties, please refer to the online documentation
in our supplemental material also providing marker-speciﬁc object and data
properties2.
2 https://openhps.github.io/FidMark/1.0/en/.

242 M. Van de Wynckel et al.
3.2 Procedures
The SOSA and POSO ontology both useproceduresto indicate a process of com-
puting data in a certain way. In Fig.1, we already listed procedures for marker
detection and pose estimation. However, in order to reduce the chance of ambi-
guity in pose estimation [36], we also extended POSO to add the most common
Perspective-n-Point (PnP) pose computation algorithms used in existing AR and
Computer Vision frameworks [6,8,22,24].
Fig. 5. Pose computation procedures in the FidMark ontology
The use of the PnP pose computation algorithms and the:PoseOutput asso-
ciated with these procedures is illustrated in Fig. 5. Similar to the examples in
the SOSA ontology, this output can be linked to a SHACL [ 13] shape to vali-
date the output of an algorithmic procedure, which in this case would include a
position and orientation.
3.3 Usage
In the following, we illustrate how FidMark can be used to describe markers in
various scenarios. In Listing 1, we provide an example of an ArUco marker [ 9]
described using our ontology. FidMark comes with a set of predeﬁned dictionar-
ies which in this example uses the original ArUco dictionary with a minimum
hamming code distance of 0 and a maximum of 1024 identiﬁers. In addition to
the marker information, the position and orientation are described. Computer
vision applications can utilise this information to detect the marker and deter-
mine its position within 3D space. To avoid ambiguity, the origin of the origin of
any object’s position is positioned relative to the centre of the marker using the
fidmark:hasOrigin predicate. The position of the marker is described using a
well-known text (WKT) representation of a geo-referenced position [2].
Using the POSO ontology, we can utilise the fidmark:FiducialMarker
visual landmark as a reference frame to position other objects. In Listing 2,
we demonstrate how a simple virtual object is positioned relative on top of
the AruCo marker from Listing 1 by indicating that it is positioned relative to

FidMark: A Fiducial Marker Ontology 243
1 :marker-1 a fidmark:ArUco ;
2 fidmark:hasDictionary fidmark:DICT_ARUCO_ORIGINAL ;
3 fidmark:markerIdentifier 94 ;
4 fidmark:hasHeight [ a qudt:QuantityValue ;
5 qudt:unit unit:MilliM ; qudt:numericValue "100"^^xsd:float ];
6 fidmark:hasWidth [ a qudt:QuantityValue ;
7 qudt:unit unit:MilliM ; qudt:numericValue "100"^^xsd:float ];
8 fidmark:hasOrigin fidmark:OriginCenter ;
9 poso:hasPosition [ a geo:Point, poso:AbsolutePosition ;
10 ogc:asWKT "POINT Z(...)" ^^ogc:wktLiteral ];
11 poso:hasOrientation [ a poso:QuaternionOrientation
12 poso:xAxisValue [ ... ] ; poso:yAxisValue [. . .];
13 poso:zAxisValue [ ... ] ; poso:scalar [. . .]].
ahttp://purl.org/ﬁdmark/
bhttp://purl.org/poso/
chttp://qudt.org/schema/qudt/
dhttp://qudt.org/vocab/unit/
ehttp://www.opengis.net/ont/geosparql#
Listing 1. Example ArUco marker using the fidmarka, posob, qudtc, unitd
and ogce preﬁxes
1 :object a sosa:FeatureOfInterest ;
2 rdfs:label "A virtual cube" @en ;
3 poso:hasPosition [ a poso:RelativePosition ;
4 poso:isRelativeTo :marker-1 ;
5 poso:xAxisValue [ ... ] ; poso:yAxisValue [. . .];
6 poso:yAxisValue [. . .]];
7 poso:hasPosition [ a poso:EulerOrientation ;
8 poso:isRelativeTo :marker-1 ;
9 poso:pitch [. . .]; poso:roll [. . .]; poso:yaw [. . .]];
10 omg:hasGeometry [ a omg:Geometry ;
11 fog:asGltf "https://.../Cube.gltf"^^xsd::anyURI ].
ahttp://www.w3.org/ns/sosa/
bhttps://w3id.org/omg#
chttps://w3id.org/fog#
Listing 2. Example relative positioning using thesosaa, omga and fogc preﬁxes
this object. As a demonstrator, we utilise the Ontology for Managing Geom-
etry (OMG) and File Ontology for Geometry formats (FOG) to describe the
3D geometry model that will be superimposed [38].
By enabling relative positioning with the marker, we satisfy design goal DG6
which requires the marker to be used as an engineering or image frame of refer-
ence. A marker can also be described without a position and orientation in the
physical world, in which case it only acts as an engineering frame of reference
for other objects positioned relative to the marker.

244 M. Van de Wynckel et al.
Some tags rely on the training of image data, preventing the possibility of
only describing a marker using a dictionary and a simple identiﬁer. To enable the
description of ﬁducial markers that do not encode information or identiﬁers, we
provide a :hasImageDescriptor predicate and :ImageDescriptor class. The
image descriptor can be expressed as a raw image or pattern such as natural
feature tracking (NFT) [3].
Tracked Markers. While previous examples used the description of markers
relative to the markers with a ﬁxed position, ﬁducial markers are also used
for outside-in tracking [ 35] where stationary image sensors track the position
of moving markers. The POSO ontology can be used to observe changes in the
position of tracked markers and Listing3 illustrates a marker with an observable
absolute position.
1 :marker-1 a fidmark:ArUco ;
2 poso:hasPosition :marker-1-position ;
3 poso:hasOrientation :marker-1-orientation .
4
5 :marker-1-position a poso:AbsolutePosition ;
6 rdfs:label "Position of Marker 1" @en .
7 :marker-1-orientation a poso:Orientation ;
8 rdfs:label "Orientation of Marker 1" @en .
9
10 :position-1701946800 a sosa:Observation ;
11 sosa:hasFeatureOfInterest :marker-1 ;
12 sosa:observedProperty :marker-1-position ;
13 sosa:resultTime "2023-12-07T11:00:00+01:00"^^xsd:dateTimeStamp ;
14 sosa:hasResult [
15 ...
16 ].
Listing 3. Marker with multiple tracked poses
4 Ontology Validation and Demonstrator
Our FidMark ontology has been validated using the OntOlogy Pitfall Scan-
ner [32] and a set of SPARQL queries that answer the design goals DG1–DG7
listed earlier in our methodology. In addition, we created a demonstrator web
application that can serialise and deserialise markers and virtual objects posi-
tioned relative to these markers. The web application will then use the deseri-
alised information to superimpose virtual objects on top of markers detected with
js-aruco2
3. Our application4 superimposing a 3D object ten centimetres above
3 https://github.com/damianofalcioni/js-aruco2.
4 https://openhps.github.io/FidMark/application/.

FidMark: A Fiducial Marker Ontology 245
an ArUco marker with identiﬁer 10 in a speciﬁc dictionary as shown in Fig. 6.
This demonstrator was created using the OpenHPS framework [ 39] for aiding
with the positioning and serialisation.
:marker-1 a fidmark:ArUco ;
fidmark:markerIdentifier 10 ;
fidmark:hasOrigin fidmark:CenterOrigin ;
fidmark:hasDictionary fidmark:DICT_MIP_36h12 ;
fidmark:hasWidth [ a qudt:QuantityValue ;
qudt:unit unit:MilliM ;
qudt:numericValue "200"^^xsd:double ];
fidmark:hasHeight [ a qudt:QuantityValue ;
qudt:unit unit:MilliM ;
qudt:numericValue "200"^^xsd:double ].
:earth a sosa:FeatureOfInterest ;
poso:hasPosition [ a poso:RelativePosition ;
poso:isRelativeTo example:marker-1 ;
poso:xAxisValue [. . .];
poso:yAxisValue [. . .];
poso:zAxisValue [ a qudt:QuantityValue ;
qudt:unit unit:CentiM ;
qudt:numericValue "10"^^xsd:double ]] ;
omg:hasGeometry [ a omg:Geometry;
fog:asGltf ".../earth.gltf"^^xsd:anyURI ].
Fig. 6. Demonstrator web application showing two markers with diﬀerent dic-
tionaries and two virtual objects positioned relative to these markers
Every SPARQL query is based on the design goals listed in Sect.2.1.W eh a v e
used the Pellet reasoner [ 34] on top of our ontology and an example dataset 5
which was created to test the queries. Fiducial markers have multiple subclasses
that we query for all square ﬁducial markers in Listing 4 (lines 1–4) using the
:shape annotation property on every subclass of :FiducialMarker. Similarly,
other annotation properties such as the colours used within the marker can be
used to determine the appropriate marker type for the available hardware.
Use cases where the ontology is applied to discover the appropriate marker
type can also make use of the available dictionaries or marker families for markers
that support identiﬁcation. To demonstrate a scenario where we want to search
for an ArUco dictionary that supports at least 150 markers, we can perform a
similar query as shown in Listing4 (lines 6–11). Each known dictionary will have
listed its dictionary size, bit size and possible error correction methods.
5 https://github.com/OpenHPS/FidMark/blob/main/examples/virtual objects.ttl.

246 M. Van de Wynckel et al.
1 SELECT ?markerType WHERE {
2 ?markerType rdfs:subClassOf* fidmark:FiducialMarker .
3 ?markerType fidmark:shape "Square"@en .
4 }
5
6 SELECT ?dictionary ?size WHERE {
7 ?dictionary a fidmark:MarkerDictionary .
8 ?dictionary fidmark:supportedMarker fidmark:TopoTag .
9 ?dictionary fidmark:dictionarySize ?size .
10 FILTER(?size >= 150 )
11 }
Listing 4. SPARQL query to retrieve all square markers and another SPARQL
query to retrieve all predeﬁned TopoTag dictionaries that support more than
150 unique tags
On lines 1–7 of Listing5 we illustrate a query to obtain a pose from an ArUco
marker with identiﬁer 19. Optionally, a dictionary can be provided when multi-
ple ArUco markers are available with diﬀerent dictionaries. When an AR appli-
cation detects a marker, it should retrieve all the information including the
virtual objects placed relative to this detected marker. An example query is pro-
vided in Listing 5 on lines 9–16 where we query for all virtual objects with a
poso:RelativePosition that is positioned relative to the QR code using the
poso:isRelativeTo predicate.
1 SELECT ?position ?orientation WHERE {
2 ?markerType rdfs:subClassOf* fidmark:ArUco .
3 ?marker a ?markerType .
4 ?marker fidmark:identifier 19 .
5 ?marker poso:hasPosition ?position .
6 ?marker poso:hasOrientation ?orientation .
7 }
8
9 SELECT ?object WHERE {
10 ?object a sosa:FeatureOfInterest .
11 ?object omg:hasGeometry ?geometry .
12 ?object poso:hasPosition ?position .
13 ?position poso:isRelativeTo ?marker .
14 ?marker a fidmark:QRCode .
15 ?marker fidmark:markerData "001122334455"^^xsd:hexBinary .
16 }
Listing 5. SPARQL query to retrieve marker pose based on type and identiﬁer
and a SPARQL query used in the web application to retrieve all virtual objects
placed relative to a detected marker

FidMark: A Fiducial Marker Ontology 247
5 Conclusion and Future Work
In the presented work, we proposed the FidMark ontology for describing visual
ﬁducial landmarks. FidMark can be used to semantically describe and publish
the type and position of ﬁducial markers in the physical world. Augmented
reality (AR) applications can use this description to detect, identify and position
themselves or other virtual objects that are placed relative to the markers.
Our ontology is built upon the generic Positioning System Ontology (POSO)
supporting the generic description of the absolute and relative position and ori-
entation of markers and objects placed relative to these markers. Despite focus-
ing on computer vision ﬁducial markers, we also provide an alignment with the
DICOM ontology for ﬁducial markers in healthcare applications.
Based on seven design goals (DG1–DG7), we validated our ontology using
a set of example SPARQL queries on top of our ontology and a generated test
dataset. We also created an open-source demonstrator AR application that is
available online and shows virtual objects relative to markers described with the
FidMark ontology. This AR application demonstrates how the FidMark ontol-
ogy can help to build interoperable AR applications that can use a commonly
described reference frame.
Future work will primarily focus on expanding the annotation of marker
types and dictionaries. While our ontology currently includes the most prominent
AR ﬁducial markers according to recent surveys, we plan to expand FidMark
with additional ﬁducial marker types based on other academic research that
was not covered in the survey papers used for our initial release. Using these
new marker types we will also expand the available procedures to detect and
perform pose estimation for diﬀerent types of markers, based on the diﬀerent
visual features oﬀered by the markers. Finally, we will also develop additional
FidMark use cases and examples to facilitate the synchronisation of reference
spaces between multiple AR devices.
Acknowledgements. The research of Isaac Valadez has been funded by a Baekeland
mandate of Flanders Innovation & Entrepreneurship (VLAIO, HBC.2020.2881).
References
1. Barone Rodrigues, A., Dias, D.R.C., Martins, V.F., Bressan, P.A., de Paiva
Guimar˜aes, M.: WebAR: a web-augmented reality-based authoring tool with expe-
rience API support for educational applications. In: Antona, M., Stephanidis,
C. (eds.) UAHCI 2017. LNCS, vol. 10278, pp. 118–128. Springer, Cham (2017).
https://doi.org/10.1007/978-3-319-58703-5 9
2. Battle, R., Kolas, D.: GeoSPARQL: enabling a geospatial semantic web. Semant.
Web J. 3(4) (2011)
3. Bermudez, F.F., Diaz, C.S., Ward, S., Radkowski, R., Garrett, T., Oliver, J.: Com-
parison of natural feature descriptors for rigid-object tracking for real-time aug-
mented reality. In: Proceedings of the 34th Computers and Information in Engi-
neering Conference, Buﬀalo, USA (2014). https://doi.org/10.1115/DETC2014-
35319

248 M. Van de Wynckel et al.
4. Bradski, G.: The OpenCV library. Dr. Dobb’s J. Softw. Tools Prof. Programmer
25(11) (2000)
5. Calvet, L., Gurdjos, P., Griwodz, C., Gasparini, S.: Detection and accurate local-
ization of circular ﬁducials under highly challenging conditions. In: Proceedings of
the IEEE Conference on Computer Vision and Pattern Recognition (CVPR 2016)
(2016). https://openaccess.thecvf.com/content cvpr 2016/html/Calvet Detection
and Accurate CVPR 2016 paper.html
6. Collins, T., Bartoli, A.: Inﬁnitesimal plane-based pose estimation. Int. J. Comput.
Vis. 109(3) (2014). https://doi.org/10.1007/s11263-014-0725-5
7. D´ıaz, A., Caicedo, S., Caicedo, E.: Augmented reality without ﬁducial markers. In:
Proceedings of the 20th Symposium on Signal Processing, Images and Computer
Vision (STSIVA 2015) (2015). https://doi.org/10.1109/STSIVA.2015.7330431
8. Gao, X.S., Hou, X.R., Tang, J., Cheng, H.F.: Complete solution classiﬁcation
for the perspective-three-point problem. IEEE Trans. Pattern Anal. Mach. Intell.
25(8) (2003). https://doi.org/10.1109/TPAMI.2003.1217599
9. Garrido-Jurado, S., Mu˜noz-Salinas, R., Madrid-Cuevas, F.J., Mar´ın-Jim´enez, M.J.:
Automatic generation and detection of highly reliable ﬁducial markers under occlu-
sion. Pattern Recogn. 47(6) (2014). https://doi.org/10.1016/j.patcog.2014.01.005
10. Gsaxner, C., Li, J., Pepe, A., Schmalstieg, D., Egger, J.: Inside-out instrument
tracking for surgical navigation in augmented reality. In: Proceedings of the 27th
ACM Symposium on Virtual Reality Software and Technology (VRST 2021)
(2021). https://doi.org/10.1145/3489849.3489863
11. Guha, R.V., Brickley, D., Macbeth, S.: Schema.org: evolution of structured data
on the web. Commun. ACM 59(2) (2016). https://doi.org/10.1145/2844544
12. Gyrard, A., Datta, S.K., Bonnet, C., Boudaoud, K.: Cross-domain internet of
things application development: M3 framework and evaluation. In: Proceedings of
the 3rd International Conference on Future Internet of Things and Cloud (FiCloud
2015) (2015). https://doi.org/10.1109/FiCloud.2015.10
13. Hogan, A.: Shape constraints and expressions. In: Hogan, A. (ed.) The Web of
Data, pp. 449–513. Springer, Cham (2020). https://doi.org/10.1007/978-3-030-
51580-5
7
14. ISO Central Secretary: Photography – Archiving Systems: Vocabulary. Standard
ISO 19262:2015, International Organization for Standardization (2015). https://
www.iso.org/standard/64219.html
15. ISO Central Secretary: Geographic information – Imagery Sensor Models for
Geopositioning. Standard ISO 19130-1:2018, International Organization for Stan-
dardization (2018). https://www.iso.org/standard/66847.html
16. ISO Central Secretary: Geographic Information – Referencing by Coordinates.
Standard ISO 19111:2019, International Organization for Standardization (2019).
https://www.iso.org/standard/74039.html
17. ISO Central Secretary: Information technology – Automatic Identiﬁcation and
Data Capture Techniques. Standard ISO 18004:2015, International Organization
for Standardization (2021). https://www.iso.org/standard/62021.html
18. Janowicz, K., Haller, A., Cox, S.J., Le Phuoc, D., Lefran¸ cois, M.: SOSA: a
lightweight ontology for sensors, observations, samples, and actuators. J. Web
Semant. 56 (2019). https://doi.org/10.1016/j.websem.2018.06.003
19. Kahn, C.E., Jr., Langlotz, C.P., Channin, D.S., Rubin, D.L.: Informatics in radiol-
ogy: an information model of the DICOM standard. Radiographics 31(1) (2011).
https://doi.org/10.1148/rg.311105085

FidMark: A Fiducial Marker Ontology 249
20. Kalaitzakis, M., Cain, B., Carroll, S., Ambrosi, A., Whitehead, C., Vitzilaios, N.:
Fiducial markers for pose estimation: overview, applications and experimental com-
parison of the ARTag, AprilTag, ArUco and STag Markers. J. Intell. Robot. Syst.
101 (2021). https://doi.org/10.1007/s10846-020-01307-9
21. Kaltenbrunner, M., Bencina, R.: reacTIVision: a computer-vision framework for
table-based tangible interaction. In: Proceedings of the 1st International Confer-
ence on Tangible and Embedded interaction (TEI 2007), Baton Rouge, USA (2007).
https://doi.org/10.1145/1226969.1226983
22. Ke, T., Roumeliotis, S.I.: An eﬃcient algebraic solution to the perspective-three-
point problem. In: Proceedings of the IEEE Conference on Computer Vision and
Pattern Recognition (CVPR 2017) (2017)
23. Koˇst’´ak, M., Slab`y, A.: Designing a simple ﬁducial marker for localization in spa-
tial scenes using neural networks. Sensors21(16) (2021). https://doi.org/10.3390/
s21165407
24. Lepetit, V., Moreno-Noguer, F., Fua, P.: EPnP: an accurate O(n) solution to the
PnP problem. Int. J. Comput. Vis. 81 (2009). https://doi.org/10.1007/s11263-
008-0152-6
25. Marchand, E., Uchiyama, H., Spindler, F.: Pose estimation for augmented reality:
a hands-on survey. IEEE Trans. Vis. Comput. Graph. 22(12), 2633–2651 (2015).
https://doi.org/10.1109/TVCG.2015.2513408
26. Mr´az, E., Rodina, J., Babinec, A.: Using ﬁducial markers to improve localization
of a drone. In: Proceedings of the 23rd International Symposium on Measurement
and Control in Robotics (ISMCR 2020), Budapest, Hungary (2020). https://doi.
org/10.1109/ISMCR51255.2020.9263754
27. Murphy-Chutorian, E., Trivedi, M.M.: Head pose estimation in computer vision:
a survey. IEEE Trans. Pattern Anal. Mach. Intell. 31(4) (2008). https://doi.org/
10.1109/TPAMI.2008.106
28. N¨oll, T., Pagani, A., Stricker, D.: Markerless camera pose estimation: an overview.
In: Proceedings of the Workshop on Visualization of Large and Unstructured Data
Sets (VLUDS 2010), Dagstuhl, Germany (2010).https://doi.org/10.4230/OASIcs.
VLUDS.2010.45
29. Odmins, J., Slics, K., Fenuks, R., Linina, E., Osmanis, K., Osmanis, I.: Comparison
of passive and active ﬁducials for optical tracking. Latvian J. Phys. Tech. Sci.59(5)
(2022). https://doi.org/10.2478/lpts-2022-0040
30. Olson, E.: AprilTag: a robust and ﬂexible visual ﬁducial system. In: Proceedings
of the IEEE International Conference on Robotics and Automation (ICRA 2011),
Shanghai, China (2011). https://doi.org/10.1109/ICRA.2011.5979561
31. Poveda-Villal´on, M., Fern´ andez-Izquierdo, A., Fern´ andez-L´opez, M., Garc´ ıa-
Castro, R.: LOT: an industrial oriented ontology engineering framework. Eng.
Appl. Artif. Intell. 111 (2022). https://doi.org/10.1016/j.engappai.2022.104755
32. Poveda-Villal´on, M., G´omez-P´erez, A., Su´arez-Figueroa, M.C.: OOPS! (OntOlogy
Pitfall Scanner!): an on-line tool for ontology evaluation. Int. J. Semant. Web Inf.
Syst. (IJSWIS) 10(2) (2014). https://doi.org/10.4018/ijswis.2014040102
33. Roberts, G.W., et al.: The use of augmented reality, GPS and INS for subsurface
data visualization. In: Proceedings of the 22nd International FIG Congress (2002)
34. Sirin, E., Parsia, B., Grau, B.C., Kalyanpur, A., Katz, Y.: Pellet: a practical OWL-
DL reasoner. J. Web Semant.5(2) (2007). https://doi.org/10.1016/j.websem.2007.
03.004
35. Song, K.T., Chang, Y.C.: Design and implementation of a pose estimation sys-
tem based on visual ﬁducial features and multiple cameras. In: Proceedings of

250 M. Van de Wynckel et al.
the International Automatic Control Conference (CACS 2018), Taoyuan, Taiwan
(2018). https://doi.org/10.1109/CACS.2018.8606773
36. Ulrich, J., Alsayed, A., Arvin, F., Krajn´ık, T.: Towards fast ﬁducial marker with full
6 DOF pose estimation. In: Proceedings of the 37th ACM/SIGAPP Symposium on
Applied Computing (SAC 2022), Virtual Event (2022). https://doi.org/10.1145/
3477314.3507043
37. Urtans, E., Nikitenko, A.: Active infrared markers for augmented and virtual
reality. Eng. Rural Dev. 9, 10 (2016). https://api.semanticscholar.org/CorpusID:
29944026
38. Wagner, A., Bonduel, M., Pauwels, P., Uwe, R.: Relating geometry descriptions to
its derivatives on the web. In: Proceedings of the European Conference on Com-
puting in Construction, Chania, Greece (2019).https://doi.org/10.35490/ec3.2019.
146
39. Van de Wynckel, M., Signer, B.: OpenHPS: an open source hybrid positioning
system. Technical report. WISE-2020-01, Vrije Universiteit Brussel (2020).https://
doi.org/10.48550/ARXIV.2101.05198
40. Van de Wynckel, M., Signer, B.: POSO: a generic positioning system ontology.
In: Sattler, U., et al. (eds.) ISWC 2022. LNCS, vol. 13489, pp. 231–247. Springer,
Cham (2022). https://doi.org/10.1007/978-3-031-19433-7
14

Author Index
A
Acosta, Maribel I-253
Amara, Jihen I-289
B
Bansal, Vidit I-236
Barile, Roberto I-180
Barlow, Helen II-110
Beno, Martin II-145
Bernstein, Abraham I-41
Bigerl, Alexander I-218
Bizer, Christina I-121
Blomqvist, Eva I-143
Bonifati, Angela II-128
Brinkmann, Alexander I-121
Brun, Armelle I-3, I-22, II-3
C
Carvalho, Jason II-110
Chabot, Y oan II-21
Chaves-Fraga, David II-217
Chekol, Melisachew Wudage I-59
Chen, Jiaoyan I-79
Cochez, Michael I-41
D
d’Amato, Claudia I-180
d’Aquin, Mathieu II-3
Daga, Enrico II-110
Dasoulas, Ioannis II-178
de Boer, Victor II-94
Decker, Stefan I-326
Delikanli, Ezgi I-270
Dengel, Andreas I-270
Derom, Olivier II-217
Diefenbach, Dennis II-128
Dimou, Anastasia II-178, II-217
Dobriy, Daniil II-145
Dong, Hang I-79
Dorsch, Rene II-40
Duan, Xuemin II-217
F
Fanizzi, Nicola I-180
Fauconnet, Claude II-162
Firmansyah, Asep Fajar I-162
Foroutan, Neda I-270
Freund, Michael II-40
Fricke, Christoph I-270
G
Gao, Y ongsheng I-79
Groenewold, Ronnie II-94
H
Harth, Andreas II-40
Hauswirth, Manfred II-75
He, Y uan I-79
Heidrich, Liss I-218
Hemid, Ahmad I-326
Herbert, Trevor II-110
Horn, Philipp I-270
Horrocks, Ian I-79
Hubert, Nicolas I-3, I-22, II-3
I
Islakoglu, Duygu Sezen I-59
J
John, Christian I-253
K
Karalis, Nikolaos I-218
Karray, Mohamed Hedi II-162
Kharlamov, Evgeny I-100
Khiat, Abderrahmane I-326
Kim, Jinha I-236
König-Ries, Birgitta I-289
Krüger, Jacqueline I-270
Kruit, Benno I-307
© The Editor(s) (if applicable) and The Author(s), under exclusive license
to Springer Nature Switzerland AG 2024
A. Meroño Peñuela et al. (Eds.): ESWC 2024, LNCS 14665, pp. 251–252, 2024.
https://doi.org/10.1007/978-3-031-60635-9

252 Author Index
L
Lageweg, Lucas I-307
Lange, Christoph I-326
Leclerc, Jean-Charles II-162
Lehmann, Jens I-199
Le-Phuoc, Danh II-75
Le-Tuan, Anh II-75
Liu, Lihui I-236
M
Mäkelburg, Johannes I-253
Maus, Heiko I-270
Meloni, Antonello I-199
Monnin, Pierre I-22, II-3
Monticolo, Davy I-3, I-22, II-3
Morales Tirado, Alba II-110
Motta, Enrico I-199
Moussallem, Diego I-162
Mulholland, Paul II-110
N
Ngomo, Axel-Cyrille Ngonga I-162
Ngonga Ngomo, Axel-Cyrille I-218
Nguyen-Duc, Manh II-75
O
Osborne, Francesco I-199
P
Paulheim, Heiko I-3
Polleres, Axel II-145
Q
Quix, Christoph I-326
R
Ratta, Marco II-110
Recupero, Diego Reforgiato I-199
Rossetto, Luca I-41
S
Saeedizade, Mohammad Javad I-143
Salatino, Angelo Antonio I-199
Samuel, Sheeba I-289
Sarkar, Arkopaul II-162
Sartini, Bruno II-57
Schmid, Sebastian II-40
Schröder, Markus I-270
Shabbir, Waleed I-326
Sherif, Mohamed Ahmed I-218
Shraga, Roee I-121
Siebes, Ronald II-94
Signer, Beat II-235
Soylu, Ahmet I-100
Stork, Lise II-199
T
Tailhardat, Lionel II-21
Tan, Zhipeng I-100
ten Teije, Annette II-199
Tiddi, Ilaria II-199
Tran, Trung-Kien II-75
Troncy, Raphael II-21
U
Uwasomba, Chukwudi II-110
V
V ahdati, Sahar I-199
V aladez, Isaac II-235
V an de Wynckel, Maxim II-235
van der Weerdt, Roderick II-94
van Harmelen, Frank II-94
V elegrakis, Yannis I-59
W
Waaler, Arild I-100
Wang, Ruijie I-41
Willerval, Antoine II-128
Y
Yang, Duo II-178
Yang, Hui I-100
Y uan, Jicheng II-75
Z
Zheng, Zhuoxun I-100
Zhou, Baifan I-100
Zijdeman, Richard L. II-199
```
