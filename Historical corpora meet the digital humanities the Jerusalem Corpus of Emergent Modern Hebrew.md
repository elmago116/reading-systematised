---
title: "Historical corpora meet the digital humanities: the Jerusalem Corpus of Emergent Modern Hebrew"
author: Aynat Rubinstein
year: "2019"
Type: Article
DOI: 10.1007/s10579-019-09458-4
source: https://doi.org/10.1007/s10579-019-09458-4
created: 2026-07-31
description: ""
tags:
  - Humanities/digitalHumanities
  - tech/AI
  - Humanities/culturalHeritage
  - op/acc/leer
  - HerStory/historical_corpora
  - Humanities/language
pdfORepub: "[[Historical corpora meet the digital humanities the Jerusalem Corpus of Emergent Modern Hebrew.pdf]]"
---
[[Historical corpora meet the digital humanities the Jerusalem Corpus of Emergent Modern Hebrew.pdf]]
## Full text (extracted from `Historical corpora meet the digital humanities the Jerusalem Corpus of Emergent Modern Hebrew.pdf`)

*Source:* `2PDF/Historical corpora meet the digital humanities the Jerusalem Corpus of Emergent Modern Hebrew.pdf`  
*Extracted:* 2026-07-31

```text
ORIGINAL PAPER
Historical corpora meet the digital humanities: the
Jerusalem Corpus of Emergent Modern Hebrew
Aynat Rubinstein 1
© Springer Nature B.V. 2019
Abstract The paper describes the creation of the ﬁrst open access multi-genre
historical corpus of Emergent Modern Hebrew, made possible by implementation of
digital humanities methods in the process of corpus curation, encoding, and dis-
semination. Corpus contents originate in the Ben-Yehuda Project , an open access
repository of Hebrew literature online, and in digital images curated from the
collections of the National Library of Israel, a selection of which have been tran-
scribed through a dedicated crowdsourcing task that feeds back into the library’s
online catalog. Texts in the corpus are encoded following best practices in the
digital humanities, including markup of metadata that enables time-sensitive
research, linguistic and other, of the corpus. Evaluation of morphological analysis
based on Modern Hebrew language models is shown to distinguish between genres
in the historical variety, highlighting the importance of ephemeral materials for
linguistic research and for potential collaboration with libraries and cultural insti-
tutions in the process of corpus creation. We demonstrate the use of the corpus in
diachronic linguistic research and suggest ways in which the association it provides
between digital images and texts can be used to support automatic language pro-
cessing and to enhance resources in the digital humanities.
Keywords Historical corpora · Language change · Ephemera · Digital humanities ·
Citizen science · Crowdsourcing · Hebrew
& Aynat Rubinstein
aynat.rubinstein@mail.huji.ac.il
1 Hebrew University of Jerusalem, Jerusalem, Israel
123
Lang Resources & Evaluation
https://doi.org/10.1007/s10579-019-09458-4

1 Introduction
The re-emergence of Hebrew as a language of everyday exchange with native
speakers around the turn of the twentieth century is an unprecedented case of
successful language revival (Harshav 1993). A century later, it is still the case that
little is known about the linguistic unfolding of this emergence process. There have
been numerous studies of the “initial state”, namely what was inherited from
classical and pre-modern varieties of Hebrew. There is also a rich body of literature
describing all aspects of the grammar of Modern Hebrew (MH), the variety of the
language spoken in our time.
1 But what was the process of change leading from the
initial state to the present state? Descriptions of the step by step evolution of
Hebrew in the early stages of its emergence, what I will call here Emergent Modern
Hebrew (EMH), are very few. This is due in large part to the lack of open language
resources for studying EMH. Corpora documenting the spoken language in the
critical stages of its revernacularization are scarce (Reshef 2013), and as discussed
below, those that are based on more literary styles only partially support diachronic
linguistic research.
Recently, due to a growing interest in understanding the structural changes in
EMH and the inﬂuence of language contact on its emergence (see Doron 2015 and
the collection of papers in Doron 2016), the development of corpora has become
imperative. Linguists from a range of theoretical, philological, and computational
backgrounds have been seeking open corpora representing the casual everyday use
of the non-extant EMH variety. Morphological and syntactic annotations as well as
metadata (temporal, geographical, sociolinguistic, and other) are being sought in
order to support in-depth study of the structural properties of EMH and its evolution
into MH. This paper describes the ﬁrst effort responding to this call.
We present the Jerusalem Corpus of Emergent Modern Hebrew (JEMH), a new
open digital corpus of EMH which is the ﬁrst freely available multi-genre corpus of
EMH that combines metadata and linguistic annotations on a large scale. Its creation
was made possible by pooling together existing tools and resources in the Digital
Humanities (DH): digitized collections of documents, crowdsourcing platforms, and
library catalogs. The corpus creation process we will describe thus serves as an
example of how interdisciplinary and inter-institutional collaboration can lead to the
relatively rapid development of high-quality language resources for non-extant
languages, which by deﬁnition are under-documented and usually under-studied as a
result.
Historical corpora cannot usually be assembled by collecting running text from
the Web. Their creation starts with scanning and transcribing, i.e., digitizing, a
collection of documents. Digitization is among the specializations of archives,
libraries, heritage institutions and museums, non-proﬁt initiatives such as Project
Gutenberg,
2 and commercial projects such as Google Books (Piotrowski 2012: 25–
1 A survey of this rich literature is beyond the scope of this paper. Entries in the Encyclopedia of Hebrew
Language and Linguistics (EHLL ; Khan, ed., 2013 ) provide a useful starting point for reviews of all topics
related to the Hebrew language. See in particular Reshef ( 2013) and references cited therein.
2 http://www.gutenberg.org/.
123
A. Rubinstein

28). In creating JEMH, we relied on content housed in the digital collections of the
National Library of Israel (NLI) and a snapshot of the Ben-Yehuda Project , the
Israeli initiative inspired by Project Gutenberg.
Since access to digitized content is a prerequisite for historical corpus creation,
the researcher interested in the content is usually seen as a client of the institution
responsible for digitization. Our project recommends a more collaborative
relationship. The linguist receives documents and metadata and produces annotated
texts that can be used to enrich the original repository. Part of this collaboration
involves the realization that corpora should be encoded according to best practices
in DH. All documents in JEMH thus comply with the guidelines of the Text
Encoding Initiative (TEI) and are available for download in this format (see
Sect. 3.1 for details). A major beneﬁt of this approach is the ability to make use of
existing tools for displaying, querying, and disseminating the corpus, and the
prospects it holds for developing computational tools for automatic processing of
the historical language variety. We discuss these in detail in the paper.
The discussion will proceed as follows. Section 2 contains a brief survey of
existing corpora of EMH and their drawbacks, motivating the creation of a new
corpus of this historical variety. Section 3 presents the newly developed corpus,
JEMH, in the context of like-minded diachronic corpora in other languages. It
provides an overview of the corpus and describes the methods used for rapid
collaborative corpus creation, including results of applying a Modern Hebrew
Natural Language Processing (NLP) toolkit to the historical language. Section 4
shows JEMH in use. Initial linguistic insights gleaned from the corpus are presented
in Sect. 4.1. Section 4.2 provides an overview of a collaborative DH project in
which the corpus is being used to improve automatic text recognition of early
twentieth century Hebrew and to enrich existing DH resources containing materials
from this time. Finally, Sect. 5 concludes and discusses directions for future work.
2 Existing corpora of Emergent Modern Hebrew and their limitations
Five large-scale initiatives have produced sizeable electronic corpora of EMH in its
formative years (see Table 1):
1. The Historical Dictionary Project of the Academy of the Hebrew Language
(Ma’agarim)
2. The Ben-Yehuda Project (BYP)
3. Historical Jewish Press (JPress) and historical children’s newspapers
4. The Bar Ilan Responsa Project (The Global Jewish Database)
5. The Hebrew section of the Google Books Ngrams corpus
These corpora, especially the ﬁrst three, have provided the empirical foundation for
much recent research on linguistic aspects of the emergence of MH. The size and
scope of these ﬁve corpora set them apart from other initiatives that collect Hebrew
123
Historical corpora meet the digital humanities: the…

Table 1 Existing corpora of EMH. The summary is focused on the years 1850–1970. Corpus size is based on tokenized versions of the texts (where prepositions afﬁ xed to
words and punctuation marks contribute to the counts), except for cases in which this information is unavailable. Square brackets indicate estimate s (see Appendix A for
information on how estimates were obtained). Sources: website of the Historical Dictionary Project (accessed July 28, 2016); Ben-Yehuda Project (Hackathon version
2014); Historical Jewish Press (version of August 2016; Sinai Rusinek and Eyal Miller, p.c.); Bar Ilan Responsa Project (version 2.1); Google Ngrams Hebrew 2012
unigrams (version of July 1, 2012)
Corpus and size Genre Digitization method Metadata Accessibility for research
Historical Dictionary Project
4,241,440 words
1851–1933
Literature, Reference,
Opinion journalism
Expert transcription and
annotation
Date, Genre, Author, Title Proprietary web interface
Ben-Yehuda Project
22,465,379 tokenized units
1830–1970
Literature, Poetry, Diaries,
Opinion journalism
Volunteer transcription Genre, Author, Title Full open access
Historical Jewish Press
[1,292,143,230 tokenized units]
1856–1970
Journalism OCR Date, Title Proprietary web interface
Google Ngrams
2,712,430,325 tokenized units
1850–1970
(Literary and Scientiﬁc
writing?)
OCR Date Ngrams (unigrams to 5-g)
Responsa Project
[42,599,545 words]
[1850–1950]
Religious literature, Responsa
books
Expert transcription Genre, Title Paid access, proprietary software
123
A. Rubinstein

texts from the relevant time period, but which are comparably very small and
domain speciﬁc (e.g., Jewish religious literature in the Wikitext collection).3
The most detailed, and in many respects the best historical corpus of EMH to date
is the one created by the Academy of the Hebrew Language as part of its Historical
Dictionary Project. It is the only corpus of EMH that has been both transcribed
manually and analyzed morphologically by experts. Texts have been assigned
trustworthy bibliographical metadata and annotated for key linguistic features by
researchers with expertise in Hebrew linguistics, literature, and Judaic Studies.
Starting in 2014, the database constructed at the Academy is accessible through a
dedicated web interface (Ma’agarim).
4 While this website is a big leap forward in
opening the Historical Dictionary to the public, there is still much to be desired in
terms of its utility for research. Crucially, the website’s sophisticated search
capabilities are not matched by tools that streamline the workﬂow of a corpus study.
The works themselves are not made available (as running text), making it difﬁcult to
acquire measures of relative frequency, dispersion, and other basic quantitative
characteristics of the collection. Ad hoc annotations are only partly supported. It is
not possible, for example, to create a subcorpus of texts based on the results of a
search query. Finally, given that snapshots of the corpus are not provided, studies
based on Ma’agarim cannot be independently evaluated or replicated. In terms of
content, the corpus contains texts that belong mainly to literary genres and
represents written language of a formal register.
The Ben-Yehuda Project is the largest digital repository of manually transcribed
EMH texts.
5 It draws inspiration from the late Michael S. Hart’s Project Gutenberg,
and similarly aims to create an open access repository of literature online, in this
case Hebrew literature. The corpus represents the joint efforts of volunteers, who
select, type, and proofread the texts. The size of this corpus, the quality of the
transcription, and the fact that it is fully open access are its main strengths.
6 Its
major drawback is the lack of date metadata for the texts. The corpus contains
literary works from a range of historical periods, including a small collection of
earlier texts, mainly poetry, from the 10th to 18th centuries, and a few texts from the
end of the twentieth century (non-EMH materials account for only 3% of the entire
BYP). Absence of timestamps currently preclude the use of this corpus for
diachronic linguistic investigation. In addition, linguistic phenomena can be studied
only to the extent that they can be matched using full text search, since the texts are
not annotated with linguistic features. Like Ma’agarim, the corpus of the BYP is
literary (including mainly poetry, prose, and essays, and to a lesser extent also
letters, memoirs, and reference works). This means that it represents the language of
a select few, speciﬁcally, a small group of educated individuals, mainly men. A
secondary drawback of the corpus is that it contains translations and texts in
3 https://he.wikisource.org/.
4 https://maagarim.hebrew-academy.org.il.
5 http://benyehuda.org/.
6 Dumps of the Project are archived periodically as of 2018, at https://github.com/projectbenyehuda.
123
Historical corpora meet the digital humanities: the…

languages other than Hebrew. These should arguably be set aside in studies that
focus on “native” EMH.
The two largest corpora from the EMH period are those by JPress and Google
Books.7,8 Both of them have been digitized using Optical Character Recognition
(OCR) technology and, accordingly, are problematic in terms of content. In
addition, they are searchable only through proprietary interfaces with pre-set
functionality. Nonetheless, JPress has proven valuable for corpus studies that take a
qualitative approach based on a small set of documents or on sampled documents
attesting a particular linguistic phenomenon.
9 It is unique in providing access to
decades of writing in Hebrew in a single genre, namely journalistic writing. 10
Google Books has also put together a massive corpus of Hebrew reaching back to
publications from the mid-nineteenth century (Michel et al. 2011; Lin et al. 2012).
However, little is known about the sources that were scanned and digitized. Taken
together, this unclarity about text selection, mediocre quality of the OCR, and the
fact that the corpus is only available for search in the format of context-less ngrams
limit its utility for linguistic research.
We turn ﬁnally to the Bar Ilan Responsa Project.
11 This corpus provides a
window into the unique genre of religious correspondence in Hebrew (known as
responsa) and Chasidic literature of the early EMH period. The responsa collection
in particular includes an unbroken chain of Hebrew correspondence from medieval
times to the twentieth century, and is thus an invaluable resource for studying the
transmission of Hebrew over the many generations in which it was not a spoken
language with native speakers. It is a large, high-quality corpus, produced through
meticulous transcription and editing. It has been successfully used in Hebrew NLP,
in tasks such as text classiﬁcation (HaCohen-Kerner et al. 2010; Mughaz et al. 2017)
and thesaurus creation (Zohar et al. 2013; Liebeskind et al. 2016). Despite years of
development, however, and despite the fact that the authors of the texts are
generally known, the corpus is distributed without date and author metadata.
Without dates, it is difﬁcult to conduct diachronic investigation of the language of
the corpus. Another notable drawback is that access to the texts is possible only
through a commercial search software.
To summarize, existing electronic corpora of EMH are lacking as a basis for
diachronic linguistic investigations due to some combination of the following
factors: (1) mediocre quality of electronic texts that were obtained through the
application of OCR technology, (2) little metadata, crucially lacking the texts’
creation date, (3) limited user access to the texts and accompanying linguistic
7 http://www.jpress.org.il.
8 http://storage.googleapis.com/books/ngrams/books/datasetsv2.html.
9 See Ariel ( 2015), Bar-Ziv Levy and Agranovsky ( 2015), and Reshef ( 2016).
10 A small section is devoted speciﬁcally to children’s newspapers. A beneﬁt of the automatic text
recognition with OCR is that the corpus is very large compared to other historical corpora of newspapers
before the twentieth century (e.g., the 1.6 million-word Zurich English Newspaper Corpus (ZEN), 1661–
1791; Lehmann et al. 2006).
11 https://www.responsa.co.il/home.en-US.aspx.
123
A. Rubinstein

annotations, and (4) homogeneity in terms of genre and author, with a focus on
literary and journalistic writing belonging to a formal register.
It should also be noted that the corpora just surveyed have been produced by
different organizations and are maintained independently, making it challenging to
consolidate materials and ﬁll in gaps in the data. This is not to say that uniformity
cannot be achieved in principle, but it would require dedicated efforts at the national
level and considerable investment of time and money. Our project takes a shoestring
approach and identiﬁes ways in which existing resources, linguistic and other, can
be pooled together rapidly in order to create a high-quality historical corpus of
EMH.
Finally, it is important to realize that in order to support theoretical linguistic
research on the revival of Hebrew, it is not enough to have a large corpus of
meticulously transcribed authentic texts. The corpus should also contain information
that can further our understanding of linguistic aspects of this unique case of
language revival. Competing hypotheses range from creolization/re-lexiﬁcation
under heavy inﬂuence from non-Semitic contact languages, to smooth transmission
of the classical Hebrew grammar that was based on intimate knowledge of the
writers with the classical Hebrew sources.
12 An ideal corpus of EMH must therefore
provide extensive author metadata, including biographical and sociolinguistic
information. What were the authors’ native languages? What other languages did
they speak? When were they ﬁrst exposed to classical Hebrew and what level of
familiarity did they have with the classical Hebrew sources? At what age did they
become part of a Hebrew speaking community, if at all? What kind of community
was it, and what was their social standing in this community? Questions of this kind
are crucial for understanding how MH came to be the language it is, and they can
only be answered with the aid of an appropriately rich corpus. While JEMH does
not currently contain all the relevant information, it can technically be extended to
include it. More importantly, it provides food for thought on how a DH informed
approach might help in collecting and assembling the necessary information from
existing sources.
3 JEMH: Jerusalem Corpus of Emergent Modern Hebrew
We created JEMH in response to the need for an open access multi-genre corpus of
EMH that will provide basic metadata and morphological analysis. Diversiﬁcation
of genres was an important secondary goal of the project, following Reshef
(2009, 2012) and Reshef and Helman ( 2009). In addition to literary and journalistic
texts and other more formal genres, we incorporated texts that are representative of
less formal, more colloquial writing of a larger circle of authors. We describe our
methodology for genre and author diversiﬁcation, metadata enhancement, and
morphological annotation in what follows.
12 For a recent overview and critical evaluation of the leading hypotheses in this area, the reader is
referred to Doron ( 2015).
123
Historical corpora meet the digital humanities: the…

3.1 Overview of the corpus
JEMH currently consists of three subcorpora as described in Table 2. The largest
part is the BYP corpus with dates, a snapshot of the Ben-Yehuda Project from 2014
to which we have been adding date metadata.
13 Two additional subcorpora represent
more colloquial EMH, captured in ephemeral documents of the time: street ads and
municipal posters. The ﬁrst has been transcribed manually via crowdsourcing (as
described in Sect. 3.2.1 below), and the second is the result of manual transcription
by research assistants to the project. All ephemeral documents have been digitized
and cataloged in the Time Travel collection of the National Library of Israel.
14 The
Municipal Posters subcorpus, in particular, includes materials from three munic-
ipalities: Haifa, Netanya, and Petah ˙ Tikvah.
JEMH is made available in two formats: as a collection of TEI-XML ﬁles and as a
pre-compiled corpus for import into a search and visualization platform for linguistic
corpora (ANNIS3; Krause and Zeldes 2016). These two formats provide comple-
mentary views on the content of the corpus. The ﬁrst allows for a faithful typographical
representation of the texts and makes it accessible to the broader DH community. The
second is designed for linguistic research and encompasses features, notably
morphological annotations, which are mainly of interest for the linguist.
15
All materials have been marked up using version P5 of the TEI Guidelines. 16 For
the content in the BYP, markup is minimal and consists only of metadata. The
Ephemera subcorpora are more extensively marked up. The text’s digital
Table 2 JEMH components
Subcorpus Genre Digitization
method
Metadata Document
count
Size
(tokenized
units)
Street Ads
1862–1941
Ephemera Crowdsourcing Date, Location,
Author, Title
93 14,993
Municipal Posters
1920–1960
Ephemera Student
transcription
Date, Location,
Author, Title
580 83,556
Dated BYP
1830–1970
Literature, Poetry,
Diaries,
Opinion
journalism
Volunteer
transcription
Date, Author, Title 1144 5,315,617
Estimated Date,
Author, Title
4339 17,149,762
Total 22,563,928
13 We are grateful to Asaf Bartov for providing this snapshot of the corpus at the Ben-Yehuda Hackathon
(THATCamp Haifa, University of Haifa; February 2014).
14 See http://web.nli.org.il/sites/NLI/English/digitallibrary/time_journey/. The Time Travel project is a
collaborative project of NLI and the University of California Los Angeles and is sponsored by the
Arcadia Fund.
15 https://github.com/JEMHcorpus.
16 http://www.tei-c.org/Guidelines/P5/.
123
A. Rubinstein

representation in TEI-XML includes information about the document’s internal
structure (opener, closer, signatures, paragraphs), visual features of the text (e.g.,
highlights, deletions and additions in the original), transcription comments (e.g., the
transcriber’s degree of certainty concerning unclear content), and named entities
(person, place, date). Normalization was carried out on dates, such that Hebrew
dates given according to the Jewish calendar have been normalized where possible
to include their Gregorian equivalent. This normalization was carried out both in the
metadata and in the text body of all documents in the new subcorpora. An example
is shown in Fig. 1. The Hebrew date, given in the text as Adar II 5679 , has been
normalized in the TEI-XML to March, 1919.
Sophisticated queries that combine metadata, textual content, and linguistic
annotations are made possible via ANNIS3. The following section discusses the
available markup and annotation in the corpus. Sample queries are described in
Sect. 4, showcasing JEMH in two linguistic case studies.
3.2 Rapid collaborative creation of historical corpora
In Sect. 2, we identiﬁed three main desiderata for an open access historical corpus of
EMH: genre and author diversiﬁcation, date metadata, and linguistic annotation. If
done by traditional annotation, these tasks are highly costly. They are time
consuming and require expert knowledge, not just in linguistics, but in literature,
history, and more. Manually annotated Hebrew corpora have indeed grown very
slowly: more than forty-ﬁve years have been devoted to the consolidation of the
Modern Literature subcorpus of the Historical Dictionary Project, an ongoing
projected launched in 1969 at the Academy of the Hebrew Language.
17 The Ben-
Yehuda Project has produced a sizeable body of digital texts its 20 years of
existence, an extraordinary achievement given that it is entirely a volunteer-based
initiative, but its focus so far has been on textual content and not on markup or
annotation. Therefore, out of the box, it does not lend itself to studying linguistic
change.
In creating JEMH, we aimed to develop methods for speeding up the process of
corpus creation without giving up on the usefulness of the resulting resource for
linguistic research. For genre and author diversiﬁcation we included ephemeral
documents representing the everyday language use of ordinary speakers, imple-
menting a crowdsourcing transcription task to turn the scanned images into machine
readable texts. Metadata enhancement was carried out based on author information
extracted from a large library catalog. Finally, for linguistic annotation we applied
NLP tools for MH to analyze the EMH texts. We evaluate their accuracy on our
corpus and identify aspects of EMH that are challenging for them. Each of these
methods is described in detail in the following subsections.
17 http://hebrew-academy.org.il/%d7%94%d7%9e%d7%99%d7%9c%d7%95%d7%9f/%d7%a1%d7%
a4%d7%a8%d7%95%d7%aa-%d7%94%d7%a2%d7%aa-%d7%94%d7%97%d7%93%d7%a9%d7%94/.
The Modern Literature subcorpus focuses on texts from the mid-eighteenth century up to the estab-
lishment of the State of Israel in 1948.
123
Historical corpora meet the digital humanities: the…

3.2.1 Genre and author diversi ﬁcation: ephemera
Materials in the JEMH Street Ads and Municipal Posters subcorpora are both part of
the Ephemera Collection of the National Library of Israel, a collection of streets
signs, commercial ads, tickets, greeting cards, show announcements, and other
printed matter documenting ﬂeeting moments in time.
18 These materials are highly
valuable for linguistic research, as will be shown here for EMH, but they are rarely
represented in linguistic corpora.
19
Ephemeral documents are unique and valuable for linguistic research because of
their diversity. They represent the writing of multiple individuals, in different
locations, coming from varied sociological and linguistic backgrounds. Individual
linguistic abilities of the authors also have a chance of surfacing in the data. Since
the ﬁrst generation of speakers learned Hebrew as a second language, as adults, it is
to be expected that they reached different levels of competence in the language
based on their individual propensities for language learning.
20 Importantly, authors
of ephemeral documents are typically not trained writers. This allows certain
linguistic features to be captured in their writing that would otherwise have been
removed or standardized by a professional editor. Documents in our corpus retain
both typographical errors and inconsistencies, as well as linguistic features that
would be considered “mistakes” by prescriptive standards and may reﬂect actual,
non-standardized language use.
Two examples of linguistic peculiarities that are fossilized in the ephemeral
materials are given in (1). Both are cases of agreement mismatches that are special
to EMH and considered non-standard in MH as well as in classical varieties of the
language. (1a) shows a mismatch in verbal inﬂection, i.e., a 1st person verb form in
the conditional antecedent with a non-matching 3rd person impersonal form in the
consequent. (1b), from the ad in Fig. 1, is a case of deﬁniteness mismatch in a noun
phrase. Generally, a noun and its modifying adjective agree in deﬁniteness in
Hebrew: either both are marked with the deﬁniteness preﬁx ha- or both are left
unmarked. What we see in (1b) is a phrase in which only the modifying adjective
carries deﬁniteness marking.
21
18 Currently, the collection includes over 139,000 freely browsable items as well as 13,483 items that can
only be viewed on location at the library.
19 One exception is the work of Grosse et al. ( 1987) on the evolution of Ruhrdeutsch (cited in Anderwald
and Szmrecsanyi 2009, p. 1134). In the study of the emergence of Modern Hebrew, Reshef ( 2009: 144–
148, 2012) and Reshef and Helman ( 2009) stress the importance of municipal correspondence and posters
to the study of language development. These materials have not been included in an openly accessible
corpus, however. Another notable resource that contains, in part, historical ephemeral documents in
classical and medieval Hebrew is the Cairo Genizah (available in digital format at http://www.
jewishmanuscripts.org/). See Morag 1998 for an early assessment of the role of this corpus in the
linguistic study of Hebrew.
20 For relevant discussion, see Harshav ( 1993), Reshef ( 2013), and Doron ( 2015).
21 A possible source for this non-standard use may be found in Mishnaic Hebrew, which is known to
show precisely this kind of exception to deﬁniteness agreement (Azar 1995: 246). Rubin ( 2013) notes that
the nouns involved are usually generic or collective (e.g., ‘water’, ‘camel’), like ‘sesame’ in (2b).
However, note that the phrase in (2b) is preceded by the “correctly” inﬂected noun phrase ha-min ha-
muvḥar ‘the select brand’ (lit.
DEF-kind DEF-select), which also features a generic noun. The juxtaposition
123
A. Rubinstein

(1) a. ve-im ken nuxal yictarxu ri šayon
and-if yes can. FUT.1PL need.FUT.3MPL license
meʔet ha -memšala
from the-government
‘… and if we can, we will need a government license…’
(Petah˙ Tikvah, Final Announcement, November 1921)
b. mi-sumsmin ha -meqomi
from-sesame DEF-local
‘from local sesame’
(Jaffa, ad, March 1919)
The immediacy in which ephemeral texts are produced and their short-lived
nature also sets them apart from writing in diaries and private correspondence,
which are other less formal genres that do enjoy some level of representation in
existing historical corpora (e.g., the Middle English and Early Modern English
sections of the Helsinki Corpus , the Corpus of Early English Correspondence , and
ARCHER— A Representative Corpus of Historical English Registers ).
22 Ya´ n˜ez-
Bouza ( 2015), who points out interesting differences within the diurnial genre
between diaries and travelogues, notes that in the latter “The frequent presence of an
addressee, whether someone speciﬁc or ‘the reader’ in general, is bound to result in
a more carefully monitored use of language” and that “Some authors are known to
have revised their original notes in preparation for publication” (p. 468). Diaries and
private letters, in contrast, are often regarded as more reﬂective of the spoken
vernacular (Rissanen 2008: 60; Culpeper and Kyto ¨ 2010: 17; Ya´ n˜ez-Bouza 2015:
467).
Ephemeral materials are written texts with certain key features of spoken
language. We ﬁnd in them traces of pronunciation conventions that are usually
absent from edited written corpora.
23 In the ad in Fig. 1, for example, we see the
word ecleynu ‘with us’ spelled with the letter y. This is an orthographic variant of a
word whose standard spelling is eclenu, without a y. The orthographic variant in the
text arguably represents the writer’s pronunciation of this word, i.e., a diphthong ey
replacing the vowel e in the speech of EMH Ashkenazi speakers whose native
Footnote 21 continued
of standard and non-standard forms is well-attested in materials from this period (see, e.g., Reshef 2016,
pp. 195, 199).
22 See Claridge ( 2008), Xiao ( 2008), Piotrowski ( 2012) and Ya ´ n˜ez-Bouza ( 2015) for an overview of
these and other resources. Basic information about English language corpora can be gleaned from the
Corpus Resource Database (CoRD; http://www.helsinki.ﬁ/varieng/CoRD/index.html). Piotrowski ( 2012)
provides an overview of historical corpora in languages other than English, including Arabic, Chinese,
Dutch, French, German, Nordic languages, Latin and Ancient Greek, and Portuguese (see his chapter 8).
23 On the limitations of studying historical phonology from corpora, see Curzan ( 2009: 1097).
123
Historical corpora meet the digital humanities: the…

language was Yiddish (Neuman 2013). That the author or authors of this text
belongs to this community of speakers gains support from the Ashkenazi family
names in the signature. Since spoken corpora are difﬁcult to produce and are
practically non-existent in the context of historical linguistics before the twentieth
century—there are simply no recordings and no living speakers who can be
recorded—ephemeral material may provide an alternative source of data about
grammatical features that are typically gathered orally (e.g., in interviews,
experiments, surveys, or ethnographic observation).
24
Not only are ephemeral documents revealing in terms of their language, they are
also interesting in terms of content. They offer a glimpse into daily life in an era long
gone and deal with a wide range of historical, cultural, and idiosyncratic topics that are
curious from today’s point of view. Genre and author diversiﬁcation is thus important
not only for studying grammar, but for a wide range of research in the humanities and
in the social sciences. There are street ads in our corpus describing life during times of
political turmoil, linguistic attitudes (e.g., toward the revival of Hebrew), fundraisers,
community events, job ads, news about consumer products and sales, and more. The
corpus is also geographically diverse. Municipal posters come from both urban and
agricultural communities (Haifa and Petah˙ Tikvah, respectively), from urban centers
of different sizes (Haifa and Netanya, respectively), geographically separated
communities (Haifa in the north versus the more centrally located Netanya and Petah ˙Tikvah), new versus more established communities (Netanya, having been established
in the 1930s, is the youngest of the three municipalities, and Haifa and Petah ˙ Tikvah
have a longer history), communities that were ethnically and religiously diverse to
differing degrees, and so on.
Ephemeral documents are interesting to read and are typically short. In JEMH,
they average 127.3 word tokens per document (excluding punctuation), compared
with an average of 3443.1 word tokens per document in the literary texts of the
Fig. 1 Document from the Street Ads subcorpus announcing the sale of sesame oil for Passover in Jaffa
in 1919. ( Source: National Library of Israel, “Time Travel” Ephemera Collection.) Corresponding TEI-
XML markup for the closer of the document is shown on the right. Markup includes structural features,
annotation of locations, and date normalization
24 See Schilling ( 2013) on sociolinguistic ﬁeldwork and Anderwald and Szmrecsanyi ( 2009) for an
overview of corpus-based dialectology.
123
A. Rubinstein

BYP. The fact that the textual snippets are not dauntingly long combined with their
engaging content makes them ideal targets for transcription by non-experts.
Alongside its language, the textual content of a document holds clues about its
topic, its date and place of creation, its author, and other information that would allow
the document to be found in a catalog search. Unlocking this content is thus a shared
goal of the researcher and the library. During the development of JEMH, the National
Library of Israel expressed interest in acquiring transcriptions of its ephemeral
materials in order to include them in its searchable catalog. Subsequently, the library
offered its crowdsourcing platform for this purpose.
25 The platform is web-based,
attractive, and sophisticated. It allows anyone with web access to contribute
information about digital images from the library’s ephemera collection, through a
variety of tasks (e.g., classiﬁcation, identiﬁcation of entities, date estimation) and
topics (photographs, languages, theatre, political campaigning, and more). The
information contributed by the virtual volunteers is processed by NLI staff and
incorporated into its online catalog. Therefore, it ﬁts squarely with Saxton et al.’s
(2013) characterization of crowdsourcing as “a sourcing model in which organizations
use predominantly advanced internet technologies to harness the efforts of a virtual
crowd to perform speciﬁc organizational tasks” (p. 3).
26
A transcription task was designed and integrated into the library’s crowdsourcing
platform.27 We organized a special event at the library—advertised under the title of
Ads Awakening —to launch the new task in May 2015. It consisted of two
introductory lectures (on the linguistic revival of Hebrew and on crowdsourcing)
followed by a 2-h transcription marathon in which the attendees transcribed ads
from the collection using NLI’s crowdsourcing platform. About 20 participants
completed the transcription of about 100 ads during these 2 h. A round of editing
and post processing then produced the Street Ads subcorpus included in the release
version of JEMH and described in Table 2. The transcriptions were simultaneously
made accessible in NLI’s online catalog and are now fully accessible to the public.
Participants were not compensated ﬁnancially for their work. Nevertheless, the
event attracted a highly motivated crowd.
28 One reason was the “small core of
devoted members” who participated, a proﬁle identiﬁed in the literature as
especially productive and creative in crowdsourcing initiatives (Garcia Martinez
and Walton 2014: 205 and references cited there). Another reason may be the
compensation scheme we adopted. Participants were invited to report on interesting
linguistic phenomena as they were transcribing, with a promise of prizes and public
acclaim for those who reported the most examples. The competition added aspects
of gamiﬁcation and citizen science to the transcription task and elevated it from a
25 Osey he-Ḥayil: (literally: ‘Achievers of Success’) http://nlics.org, powered by PyBossa ( http://pybossa.
com/).
26 The term crowdsourcing is due to Howe ( 2006, 2008).
27 We thank Maayan Almagor, NLI’s former Community Manager, and Sinai Rusinek from Digital
Humanities Israel for their collaboration on this project.
28 Volunteers were recruited through announcements distributed among students and faculty at the
Hebrew University of Jerusalem (including research assistants who were involved in transcription of
other materials in the corpus), through announcements in local forums of digital humanities, and through
the library’s social media outlets.
123
Historical corpora meet the digital humanities: the…

somewhat tedious task of reading and typing to an activity in which participants
engaged in scientiﬁc discovery.
We deﬁned linguistic phenomena of interest as features of language (at any level
of representation: pronunciation, sentence structure, lexical meaning, and so forth)
that appeared archaic and that did not, according to the participants’ judgment,
characterize present day Hebrew. Examples of the reported phenomena are shown in
Table 3. These phenomena are known from the literature on EMH and do not
constitute new linguistic discoveries,
29 but the fact that they were identiﬁed by our
volunteers is evidence that they paid close attention to detail while performing the
transcription task. It is also reassuring in terms of the nature of documents in our
corpus: these documents reﬂect key features of the language of their time.
In summary, our task ﬁts the Collaborative Science Project Model of
crowdsourcing (Saxton et al. 2013), not only because the role of participants in
the task is similar to that of a research assistant, i.e., deciphering text and producing
machine readable content, but also due to the research oriented competition that was
integrated into the task. The competition was not directly related to the output
generated and therefore went beyond the standard model of incentive-building in
crowdsourcing in which participants accumulate points for each task completed or
for the quality of their work.
30 Although the transcriptions generated were not
monitored or evaluated for quality in real time, we succeeded in drawing a crowd of
intrinsically motivated volunteers with a keen interest in reading the texts and
exposing the language in them, with all its peculiarities. The amount of editing and
corrections that was necessary in the post-processing phase was minimal.
As a result of our collaboration with the library, we now enjoy a diversiﬁed
corpus in terms of genre and have access to a platform for ongoing text collection.
31
Table 3 Examples of EMH phenomena reported in the transcription marathon
Phenomenon Component Example
Obsolete lexicalizations Lexicon EMH: mistaderet ‘getting organized’
(MH: mitʔargenet) qvuca ‘a group is
getting organized’
Biblical verb forms Morphology, Semantics EMH: še-tehi ‘that there will be’ (MH:
še-tihye)
Obsolete verbal
template nitpa`el
Morphology, Semantics EMH: nitparsem ‘was published’ (MH:
hitparsem)
Matres lectionis omitted Orthography EMH spelling: LSˇLT ‘to prevail’ (MH
spelling: LSˇLOT)
29 See, among others, Bendavid ( 1971), Reshef ( 2009), Shatil ( 2007), and Wigderson ( 2015).
30 On ways to increase motivation of participants in crowdsourcing see, e.g., Kaufmann et al. ( 2011),
Zheng et al. ( 2011), Zhao and Zhu ( 2014), and Morschheuser et al. ( 2016).
31 http://nlics.org/, transcription of ads for children’s’ plays (accessed November 7, 2017).
123
A. Rubinstein

3.2.2 Metadata enhancement
Metadata annotations in JEMH focused on date and place of creation, information
that is necessary to facilitate corpus studies of historical language change and
dialectal variation.
A large portion of our corpus is based on the texts of the Ben-Yehuda Project. Apart
from the unique literary and cultural value of this corpus, it has recently been piloted in
a number of DH tasks, including automatic identiﬁcation of literary allusions and
stylometric clustering by genre and author.
32 These tasks are all able to leverage the
corpus as a large undifferentiated bag of words, but for time sensitive research, in
linguistics and more generally, dates are invaluable. Language metadata is necessary
in order to set aside texts whose language is not Hebrew, or which are translations not
written originally in Hebrew.
33 Some of this metadata can be gleaned from the BYP
website by a human reader, but is currently not accessible for automatic processing or
search due to the unstructured format of the website: a collection of HTML pages with
basic search functionality provided by Google Search.
We set out to provide date and language metadata for all texts in this collection.
In some cases, the work itself or an author’s bibliographic contents page in the Ben-
Yehuda Project mentions the text’s creation date (Fig. 2). In such cases, the date
need only be inserted, potentially after some normalization, into the appropriate
metadata ﬁeld in the JEMH TEI-XML ﬁle. The dates circled in Fig. 2b, for example,
are Hebrew dates mentioning years and months in the Jewish calendar. They need,
ﬁrst, to be converted into the equivalent Gregorian date ranges, and then marked up
as date metadata using the correct TEI syntax. When the Ben-Yehuda Project does
not provide date information for a given text, some non-trivial bibliographical and
literary detective work is needed to track down its creation date.
We have so far added date metadata manually to 21% of the documents in the
BYP snapshot corpus. For the rest, we provide date estimations . Estimations are
based on the author’s life span, a piece of information obtained from the NLI
catalog. Texts in the Ben-Yehuda Project are all organized by author, and putting
these two resources together it is possible to estimate dates for all texts in the
collection by associating each undated text with the decade corresponding to the
midpoint of its author’s life span.
34 As an example, consider the writings of Bar-
Tuvia (pseudonym of Shraga Feybush Frenkel), who lived between the years 1875
and 1933. In our snapshot of the Ben-Yehuda Project there are 45 texts by this
author and only 43 of these are dated. More than half were written in the 1920s (the
text shown in Fig. 2a is one example), 8 are dated to the 1910s, and 9 to the ﬁrst
decade of the twentieth century. The two undated texts are mapped by the life span
32 Experiments run by participants of the Ben-Yehuda Hackathon (THATCamp at the University of
Haifa, February 2014).
33 Some works in Russian, Yiddish, German, English, and Italian, for example, are included in the Ben-
Yehuda Project.
34 The heuristic of estimating creation dates based on author lifespan is mentioned in other historical
corpora, e.g., the Corpus of Modern Yiddish (CMY; http://web-corpora.net/YNC/search/index.php).
There are various implementations of this heuristic that one could employ; we leave experimentation with
their accuracy for future research.
123
Historical corpora meet the digital humanities: the…

heuristic to the earliest of these three decades. Although this is not the author’s most
proliﬁc period according to the data we have, it is nevertheless a time in which he
was actively engaged in writing. Users can choose to search only the manually dated
texts of the BYP (a collection containing about 5.3 million tokenized units) or
include those for which we have only date estimations (for a total of over 22.4
million tokenized units).
Turning to place metadata, documents in the Street Ads collection and in the
Municipal Posters collection have been manually annotated for publication place,
enabling the researcher to address questions about variation among geographically
deﬁned dialects. As noted in the previous section, the posters come from three
distinct locations that differ from one another in terms of settlement type, population
proﬁle, geography, and history. Street ads come mainly from three central urban
centers (Tel Aviv and Jaffa, Jerusalem, Haifa). Diversity of locations in the
ephemera subcorpora is shown in Table 4.
The imbalance in the geographical source of street ads is not intentional and
should be rectiﬁed as the ephemera subcorpus grows. In the future, we would also
like to provide place metadata for all documents in JEMH, including the literary
works in the BYP. We plan to do so based on Linked Open Data containing
biographical information about the authors and bibliographical information about
particular works.
3.2.3 Morphological annotation
A third major goal we had in designing JEMH was to provide linguistic annotation of
the EMH data. Linguistic annotation is a prerequisite for studies that aim for a certain
level of linguistic generalization. In the domain of morphology, or word structure,
(a) http://benyehuda.org/frenkel/maase_bishney.html (b) http://benyehuda.org/schein/
Fig. 2 Dates in the Ben-Yehuda Project (circled). Some entries include a date as part of the running text
(a). In certain other cases, an author’s table of works contains this information implicitly ( b). Source:
http://benyehuda.org/; accessed September 6, 2016
123
A. Rubinstein

searches based on lemmas or morphological features can reveal generalizations that
are difﬁcult to establish based on searches targeting individual words. In the current
release of the corpus, we provide morphological annotations of lemma, grammatical
category (part of speech), inﬂection (e.g., tense, person, number, gender; as relevant
for different grammatical categories), other afﬁxes (e.g., adpositions, conjunctions, the
deﬁnite article), and verbal template (known as binyan).
35
In the absence of dedicated NLP tools for EMH, we followed common practice in
historical NLP and experimented with applying new tools on the old data
(Piotrowski 2012: 85, 91ff.): our historical texts were tokenized, morphologically
analyzed, and morphologically disambiguated automatically based on language
models trained on MH. In particular, texts are tokenized using the MILA Hebrew
Tokenization Tool (Itai and Wintner 2008), analyzed morphologically by the MILA
Hebrew Morphological Analysis Tool (Itai and Wintner 2008), and disambiguated
morphologically using a state of the art Hebrew Morphological Disambiguator
(Adler 2007; Adler and Elhadad 2006) with good initial conditions (Goldberg et al.
2008). The disambiguator applies a Hidden Markov Model (HMM) word-based
model to determine the most likely analysis for a given sequence of words, taking
into account all possible analyses for the individual words in the sequence.
Although these tools were developed for MH based on language models of MH,
they provide a ﬁrst-pass annotation of the historical texts that is reasonable and
comparable to what has been reported in the literature for historical European
languages. Claridge ( 2008) provides ballpark ﬁgures for part of speech tagging in
English, stating a drop from 96–97% accuracy on modern texts to ﬁgures in the
range from 80% to mid-90% accuracy on Early Modern English texts (p. 254). Pre-
processing the texts, e.g., by modernizing the spelling, results in a signiﬁcant
increase in accuracy (see Piotrowski 2012, 91ff. for a summary). Ro ¨ gnvaldsson and
Helgado´ ttir ( 2011) apply a part of speech tagger for modern Icelandic to an Old
Norse corpus. Even without adjustments, the drop in accuracy is smaller than in
English, from 90.4% to 88.0%. With some manual correction and retraining, the Old
Norse tagger outperforms the modern tagger. In Czech, Hana et al. ( 2011) advocate
a combined approach: they train a tagger for Old Czech after both modernizing the
old corpus and aging the modern corpus, achieving 91.5% accuracy on part of
Table 4 Geographical distribution of ephemera in JEMH. Only 73 out of the 93 street ads in the corpus
had an identiﬁable publication place
Street Ads Municipal posters
Tel Aviv and Jaffa 54 (74%) Haifa 239 (41.2%)
Jerusalem 12 (16.4%) Netanya 180 (31%)
Haifa 3 (4.1) % Petah ˙ Tikvah 161 (27.8%)
Other 4 (5.5%)
Total 73 (100%) 580 (100%)
35 Verbal templates are characteristic of Hebrew’s Semitic non-concatenative morphology. Future
releases of the corpus will include annotation of roots alongside templates for verbs.
123
Historical corpora meet the digital humanities: the…

speech tagging and 70.6% on a tagset of 11 features (comparable in size to the
Hebrew tagset). Accuracy for lemmatization is not provided. 36
The accuracy of morphological disambiguation on a gold set of JEMH
documents is shown in Table 5. The gold set contains 4219 tokenized units from
documents chosen at random from the three subcorpora (about 3200 tokenized units
in total from the BYP subcorpus and about 1000 divided evenly between Street Ads
and Municipal Posters).
We see, ﬁrst, a clear difference in accuracy according to genre: the ephemeral
corpora are overall more accurately annotated by the modern tools than the literary
texts of the BYP. The difference is dramatic when multiple features, including
tense, number, and gender, are taken into account. Second, the accuracy of part of
speech and lemma annotations in all subcorpora, including the BYP, is in the 91–
96% range. Even the BYP corpus, whose language appears according to these
metrics to be most dissimilar from the MH language model, is annotated reasonably
well for lemmas and parts of speech in this sample. For comparison, Goldberg et al.
(2008) report reaching an accuracy of 92.4% for part of speech tagging (and word
segmentation), and 89.4% for full morphological analysis.
37 We observe a slight
drop in accuracy for part of speech annotations of BYP texts, concomitant with a
substantial difﬁculty to assign correct inﬂectional features to the EMH texts.
Morphological disambiguation is a notoriously difﬁcult task in a morphologically
rich language like Hebrew, which, moreover, is written with a script that only
partially encodes vocalizations in most contemporary genres.
38 A number of
additional challenges are posed for the modern tools speciﬁcally by the inherent
characteristics of the historical texts, which, as is typical (Claridge 2008), document
a less-standardized and distinct language variety. Three central challenges for
automatic annotation of EMH are exempliﬁed below. The ﬁrst is a lexical-syntactic
challenge of obsolete lexicalizations. The verb in (2) is obsolete in the nif`al verbal
template with the meaning of ‘to skin’; it incorrectly receives the analysis it would
have in MH, as a verb in the pi`el template meaning ‘to simplify’. The analyzer in
this case predicts an incorrect lemma and a host of incorrect inﬂectional features
(tense, person, number, and gender) that go along with the modern analysis.
(2) dag-im še-nifšat me -hem ha -ʕor
ﬁsh-
MPL that-skinned from-them the-skin
‘ﬁsh that were skinned’
(Haifa, poster, December 1944)
36 See Piotrowski ( 2012) for a more complete survey of NLP tools for historical corpora in additional
languages.
37 Adler ( 2007) reports an accuracy of 93.36% for part of speech tagging (and segmentation), and
90.05% for full morphological analysis. Full analysis in his system consisted of more features than those
tested here. Presumably, this is the case also for Goldberg et al.’s ( 2008) system.
38 See Adler ( 2007: 2) for an example of a seven-way ambiguity in the morphological analysis of the
four-character word BCLM.
123
A. Rubinstein

Mistakes of this kind are found not only in verbs. They are common in nouns
denoting objects that are nowadays rarely in use (e.g., ALMNK ‘almanac’ which the
tagger incorrectly decomposes into ALMN-K ‘your widower’) or in nouns that have
been replaced by native vocabulary (e.g., ʔKSMPLRIM ‘exemplars’ which in present
day Hebrew would be replaced by a different lexical item).
A related problem concerns words that follow the grammar of classical Hebrew,
in structures that were not inherited by MH. Not surprisingly, the MH language
model can go awry in these cases. Certain verb forms characteristic of Biblical
Hebrew, for instance, are not recognized as such and annotated incorrectly (e.g., as
proper names). Examples involving Mishnaic Hebrew morphology are also attested
in the data.
The third and most devastating challenge for the tagger is omission of matres
lectionis. Written EMH, in sharp contrast to written MH, is characterized by a
propensity to not indicate vocalizations using the small set of consonants known as
‘mothers of reading’. Mistakes arise when modern writing conventions do not allow
the reduced spelling for the word in question but recognize a different analysis of
the non-vocalized string. In the following example, [o] indicates a vowel that is
necessarily expressed in the MH spelling of ‘address’, but is missing from the EMH
text. The MH disambiguator mistakenly chooses the analysis k[a]t[e]v[e]t ‘reporter
(F)’ instead, even though it is not a good ﬁt within the broader context of the
sentence.
(3) ve-nodiʕae t h a -kt[o]v[e]t
and-tell.
FUT.1PL ACC the-address
‘and we will disclose the address’
(Petah˙ Tikvah, poster, February 1926)
These points of confusion suggest future directions of research for automatic
processing of EMH. Overall the MH tools achieve accuracy that is comparable to
what has been reported in the historical NLP literature. The presence of Biblical
Table 5 Accuracy of morphological analysis on gold set obtained by correcting the output of Goldberg
et al.’s ( 2008) morphological disambiguator. Morphological features evaluated: POS, lemma, tense,
number, gender
POS only (%) L EMMA only (%) All features %
Ephemera:
Street Ads
96.0 94.0 81.6
Ephemera:
Municipal posters
95.9 92.7 84.2
Literature:
BYP
91.6 90.7 64.1
Overall accuracy 92.7 91.3 68.7
123
Historical corpora meet the digital humanities: the…

Hebrew and later varieties in the EMH texts, both in the lexical inventory and in the
morphology, motivates building a hybrid language model that incorporates lexical
and morphological features of classical Hebrew varieties.
3.3 Comparison with diachronic corpora in other languages
JEMH is a collection of texts in one language (Hebrew) that spans several decades
and supports the study of language evolution. This makes it a diachronic (or
historical) corpus by deﬁnition.
39 It strives for diversity in genre and author by
including ephemeral materials alongside literary texts, and is designed to be useful
for DH projects that are not necessarily linguistic in nature. This second goal is
achieved by encoding texts and metadata in TEI-XML and allowing open access to
the corpus. In this section, I describe a few corpora in other languages that have also
been developed with some of these goals in mind.
40
Noteworthy among existing diachronic corpora is the Lampeter Corpus of Early
Modern English Trac ts (LC; Schmied 1994). The corpus includes texts in British
English from 1640 to 1740, focusing on tracts and pamphlets dealing with a wide
range of subject matters. The LC is encoded in TEI compliant SGML and is freely
available for download in this format.
41 Like JEMH, the LC is the result of
collaboration between linguists and library staff, and it was conceived as a resource
that would propel research in (English) historical linguistics while simultaneously
documenting a key period in English history (a decade that began with the English
Civil War and led into the beginning of the Industrial Revolution). The corpus is
balanced in terms of text topics and it contains a wealth of valuable metadata for
each text, including information about its author, publication date and place, and
more. For the Hebrew researcher, JEMH provides in addition morphological
annotations. It is not similarly balanced by pre-selection of materials, but is more
open ended, in that it allows for constant corpus growth through crowdsourcing.
Documenting another historical variety of English, the Helsinki Corpus of Older
Scots (HCOS; Meurman-Solin 1995) is a multi-genre balanced diachronic corpus of
Older Scots from 1450 to 1700. HCOS aims speciﬁcally to expose non-literary
genres that may reﬂect spoken, informal language of both women and men. These
include travelogues, diaries, pamphlets, and diaries. The corpus is not large (it
contains about 0.5 million words for the years 1570–1700, compared with, e.g., 1.1
million words in the LC for just ten decades), but is rich in metadata. It is freely
available for research under a non-commercial share-alike license.
42
Outside of English, the Base de Français Médiéval (BFM) is a multi-genre
collection of French texts from the Middle Ages (9th–15th centuries). The corpus is
encoded in TEI-XML and is available for download upon request. In addition to rich
metadata, a large portion of the corpus has been automatically annotated with
39 In contrast, a corpus of historical texts from just 1 year, e.g., the Brown Corpus (with texts collected in
1961), is not a diachronic corpus according to this deﬁnition (Claridge 2008: 243).
40 See footnote 22 above for pointers to comprehensive surveys of existing diachronic corpora.
41 https://www.tu-chemnitz.de/phil/english/sections/linguist/real/independent/lampeter/lamphome.htm.
42 http://purl.ox.ac.uk/ota/2081.
123
A. Rubinstein

morphosyntactic features. For the diachronic study of German, the DWDS-
Kernkorpus corpus provides a balanced multi-genre corpus of twentieth century
German (1900–1999) encoded in TEI-XML and annotated automatically with
lemmas and parts of speech (Geyken 2007).43 The corpus is not available for
download due to issues of copyright. The Modern Chinese Language Corpus
(MCLC) is noteworthy in speciﬁcally sampling ephemeral materials. It is a balanced
multi-genre corpus which spans almost one century of written Chinese, from 1919
to 2002 (although the majority of the texts are from 1977 and on).
Finally, among the Semitic languages, large historical corpora of Arabic are
under active development. Several of these are based on the content of Al-Maktaba
Al-Shamela (“The complete library”), a website providing online access to Arabic
texts from the 7th century to the modern era.
44 Belinkov et al. ( 2016), for example,
report on ongoing work to clean up the corpus, detect text reuse, and automatically
add dates and morphosyntactic annotations. Due to their religious content, the texts
are primarily from a formal register and are relatively limited in terms of genre.
Ahmed ( 2018) reports on the construction of a historical corpus of medieval Judeo-
Arabic (10th–12th centuries) aimed to support the study of language contact
between Hebrew and Judeo-Arabic in the Middle Ages. The corpus contains three
religious works by three authors; it is encoded in TEI-XML and is annotated with
linguistic features relating to code switching, borrowing, and quotation.
4 Using JEMH
4.1 Using JEMH in linguistics: language change in EMH
All morphological and metadata annotations are bundled with the text into an
ANNIS3 corpus, allowing the user access to the rich functionality offered by
ANNIS (Krause et al. 2016). The platform is free and open source and importantly
supports the right-to-left layout of Hebrew. It offers convenient keyword in context
(KWIC) views, sophisticated querying options (including an easy to use user
interface for building and executing queries), basic frequency analyses, and the
ability to export search results in various formats and share them with others via
designated links.
45
Queries that combine metadata restrictions and linguistic features are easy to
formulate. Some do not require JEMH; they can also be investigated using existing
resources (notably, Ma’agarim, which indeed contains higher quality annotation of
morphological features). But JEMH offers more than this. Due to its open access
nature, it is possible to aggregate results from all texts and all annotations in ways
that are tailored to answering speciﬁc research questions. I demonstrate with two
test cases, in morphology and in semantics.
43 https://www.dwds.de/.
44 http://shamela.ws.
45 See the ANNIS user guide for details: http://corpus-tools.org/annis/documentation.html.
123
Historical corpora meet the digital humanities: the…

Suppose we are interested in the morphological question of how verbal templates
in Hebrew evolved over time. Current literature has pointed to the changing
productivity of the templates, but has generally been concerned with changes as they
are observed in MH in recent decades (see, e.g., Bolozky 2009). Researchers seem
to agree that the templates known as “heavy” or “intensive”, i.e., hitpa`el, pi`el (and
its passive counterpart pu`al), have risen in productivity, while the unmarked default
template, pa` al , is on the decline.
46 We would like to know whether these changes
were abrupt or gradual, whether they followed the same pace or not, and perhaps
whether they were correlated with other structural changes in the language. In the
tool suite provided with ANNIS, we have direct access to summary statistics about
the frequency of the templates in each decade in the corpus ANNIS (see Zipser and
Romary 2010 on the Pepper conversion tool). We can use this data to observe
gradual changes in template productivity (Fig. 3): a gradual decline in the pa`al
template, and a gradual rise in the hitpa`el template. Smaller rises are observed in
pi`el and in its passive counterpart pu`al, and in nif`al. We see that productivity
changed gradually and that it was initiated in EMH.
The raw counts underlying the percentages in Fig. 3 can be used to test the
statistical signiﬁcance of these apparent changes.
47 For example, the decline in
pa’al, from 133 instances out of 220 verb tokens in the 1840s, to 6485 out of 13,112
in the 1970s, is statistically signiﬁcant according to Fisher’s exact test ( p value =
0.0014). The rise in hitpa`el is also signiﬁcant according to this test, while the rise in
pi`el is not signiﬁcant but approaches signiﬁcance. In contrast, the rises in nif`al and
pu`al turn out not to be statistically signiﬁcant. 48 Among existing resources, only
Ma’agarim allows access to data of this kind, and even then not directly.
Questions that require access to the broader context of a word or phrase in
addition to its linguistic features can only be done in JEMH. This is typically the
case when the phenomenon of interest is syntactic, semantic, or discourse oriented
in nature. Consider the modal use of the existential element yeš (and its negative
counterpart eyn) when followed by an inﬁnitive. Similarly to English have and
existential/possessive constructions in other languages, the MH existential gives rise
to a meaning of obligation as a modal (as in yeš laʕamod ‘
EX to.stand’ meaning ‘one
must stand’; Boneh 2013). Perhaps surprisingly, the construction did not always
have this meaning (Ben-H˙ayyim 1953, 1992; Shehadeh 1991). A corpus study based
on JEMH has shown that the construction developed its obligation meaning
throughout the EMH period, concomitant to losing the dative phrase that was
characteristic of modality in previous stages of the language (Rubinstein,
46 A variety of reasons have been given in the literature to explain the decline in productivity of pa`al,
which still remains the most common template in the language: the template is already associated with
many roots, it cannot accommodate quadri-literal roots due to its morphophonology, it is not associated
with a uniform semantics, and more. See Bolozky ( 2009: 360) and reference cited there for further
discussion.
47 I thank an anonymous reviewer for suggesting this avenue for research. Changes in the productivity of
MH verbal templates have so far been described based on a range of quantitative studies, but without
systematically reporting the statistical signiﬁcance of the ﬁndings (see, e.g., Bolozky 2009).
48 Raw counts are as follows (for the 1840s and the 1970s): 6 and 966 in hitpa`el, 28 and 2299 in pi`el,1
and 228 in pu`al, 13 and 1170 in nif`al.
123
A. Rubinstein

forthcoming). To obtain these results, one must collect a subcorpus of relevant
instances of the construction and save them in their broad contextual context for
further annotation and analysis. This functionality is supported by JEMH but by
none of the existing EMH corpora.
JEMH’s BYP subcorpus has also recently been used to trace the development of
the grammatical feature of superﬂuous negation in MH (a phenomenon distinct from
Negative Concord; see Rubinstein et al. 2015) as well as the evolution of discourse
markers in the language (Tsirkin-Sadan 2015).
4.2 Using JEMH in the digital humanities
The relevance of corpora such as JEMH to the digital humanities and vice versa
begins in corpus creation.
49 More and more textual collections are created as
projects in the digital and public humanities frameworks, driven by varied interests
in history, literature, art, and all facets of human culture. The TEI guidelines were
developed to enable markup and analysis of phenomena of interest to a variety of
subdisciplines in the humanities. Even if linguistic issues were not of interest during
corpus creation, corpora created using this methodology enable the study of
language within various genres and contexts; they make possible research on topics
such as the language of headlines, features of turn taking in correspondence, and
ways of establishing reference to multiple addressees in dramatic corpora. The
linguist’s enhancement of texts, in turn, provides material for further DH work. For
instance, annotation of named entities facilitates gazetteer and prosopography
building, as well as use of Linked Open Data on the corpus.
Fig. 3 Changes in the productivity of the verbal templates over time in JEMH’s BYP subcorpus
49 I thank Sinai Rusinek for discussion of these issues.
123
Historical corpora meet the digital humanities: the…

Large sections of JEMH were curated through two DH events: the ﬁrst was the
Haifa THATcamp for which the BYP corpus was downloaded and preprocessed, and
in which one of the working groups prototyped a corpus query tool.
50 The second was
the transcription marathon we organized in collaboration with the National Library,
which brought to light the special language of the ephemeral documents.
JEMH pairs digital images with machine-readable text and metadata. In terms of
textual content, each TEI-XML contains running text obtained via manual
transcription. The ephermeral materials also contain annotation of entities
(speciﬁcally, locations), also obtained via manual annotation as described above.
The corpus can thus serve as training data for applications that aim to carry out these
tasks automatically.
Two current collaborations explore these directions of DH engagement with
JEMH. A process of aligning visual images of the ephemera with their textual
content, enabled by the XML encoding of JEMH, is currently underway using the
READ (Recognition and Enrichment of Archival Documents) Transkribus
platform.
51 The output of this process will serve as training data for a neural
network OCR, which will subsequently be used on previously undigitized posters
and ads to augment JEMH. Following this work, JEMH will be used by students of
the Digital Humanities BSc program at Haifa University in their assignments to
recognize place and person names in the corpus, using the Pelagios Recogito
platform and the KIMA historical gazetteer (Rusinek 2016). This work will enhance
the gazetteer with new forms of place names and support studying the geographical
aspect of texts in JEMH.
5 Conclusion
In this paper I have advocated a collaborative resource-light approach to creating
historical language resources. I have argued that it is worthwhile to invest time in
encoding the corpus using best practices in DH, although they are still largely
foreign to the linguistics and computational linguistics community. The TEI-XML
format allows for cross-disciplinary collaboration and broad dissemination of new
primary sources for research and analysis. The linguist beneﬁts from a corpus
marked up with metadata, in a format that is easily converted into input for state of
the art open source search and query systems (ANNIS, in particular, recognizes a
subset of TEI directly and other features are supported by its generic XML
importer), in addition to friendly visual rendering of the texts (e.g., using
TEIBoilerplate or EVT, or export into PDF or RTF). More importantly, the
association between digital image and transcribed text that is encapsulated in the
TEI-XML can serve as training data for systems in the NLP pipeline for historical
texts. A pilot using the JEMH ephemera subcorpora as training data for a character
recognition system is currently underway. The recognizer could be deployed by
50 Search-Yehuda working group (the group included the author, Livnat Herzig Sheinfux, Nadav Bin
Nun, Nurit Melnik, Shira Wigderson, Sinai Rusinek, Tal Baumel, Toma Tasovac, and Tsvi Sadan).
51 https://read.transkribus.eu/.
123
A. Rubinstein

libraries, archives, and researchers, for large-scale acquisition of textual corpora of
historical materials. JEMH would be the seed of this expanding resource.
Future linguistically-oriented work will add new collections of documents to the
corpus and expand the set of morphological features available for search (notably,
including the roots of verbs in addition to templates). A layer of syntactic
dependencies obtained from MH parsers will be added to JEMH, as well as
visualizations of the entities annotated in the corpus.
These efforts all serve the main purpose of building the corpus: to provide the
linguistics community with a new tool for researching the step by step consolidation
of EMH into a stable linguistic system, its relation to previous stages of Hebrew,
and the effects of contact with foreign languages on its evolving grammar.
Acknowledgements I wish to thank the three anonymous reviewers of this manuscript for their helpful
comments. For invaluable discussion and feedback during all stages of the project, I am grateful to Sinai
Rusinek. Thanks also to Meni Adler, Maayan Almagor, Yael Netzer, Avigail Tsirkin-Sadan, and Amir
Zeldes. This research was supported by the Mandel Scholion Interdisciplinary Research Center in the
Humanities and Jewish Studies at the Hebrew University of Jerusalem. I thank researchers at the Center
for their support, especially Yael Reshef for enabling me to train research assistants of the “Emergence of
Modern Hebrew” research group in the TEI format. Programming support by Itay Zandbank of The
Research Software Company ( https://www.chelem.co.il) is also gratefully acknowledged.
Appendix A: Corpus size estimates
Historical Jewish Press (JPress)
The JPress corpus is not freely available for search. In order to provide an
estimation of the size of the corpus, I relied on the number of scanned newspaper
pages from the years 1856–1970, as reported by the JPress team for the version of
the corpus from August 2016 (Sinai Rusinek and Eyal Miller, p.c.). An estimation of
token counts was done manually, by counting the number of tokens (base words,
prepositions, and punctuation marks) in one column of one randomly chosen
newspaper page in the corpus ( Ha-zman, volume 78, April 20, 1914; page 2).
● Tokens in column: 777
● Tokens in page [estimate]: 4662 (six columns)
● Total pages (1856–1970): 277,165
● Total tokens (1856–1970) [estimate]: 1,292,143,230
Bar Ilan Responsa project
The corpus is searchable through a proprietary interface, in which it is possible to
see word counts for individual texts and subcorpora. However, since works in the
corpus are distributed without date metadata, it is not possible to search for those
that are from a particular time period. To achieve an estimate of the size of the
corpus for the period of interest to us, we located relevant subcorpora and estimated
123
Historical corpora meet the digital humanities: the…

word counts for each of them. The following calculations are based on version 2.1
of the Bar Ilan Responsa Project.
References
Adler, M. (2007). Hebrew morphological disambiguation: An unsupervised stochastic word -based
approach. Ph.D. thesis, Ben-Gurion University of the Negev.
Adler, M., & Elhadad, M. (2006). An unsupervised morpheme-based HMM for Hebrew morphological
disambiguation. In Proceeding of COLING -ACL-06, Sydney, Australia.
Ahmed, M. A. (2018). XML annotation of Hebrew elements in Judeo-Arabic texts. Journal of Jewish
Languages, 6, 221–242.
Anderwald, L., & Szmrecsanyi, B. (2009). Corpus linguistics and dialectology. In M. Kyto ¨ &A .L u¨ deling
(Eds.), Corpus linguistics: An international handbook (Vol. 2, pp. 1126–1140). Berlin: De Gruyter.
Ariel, Ch. (2015). The expression of material constitution in Revival Hebrew. Journal of Jewish
Languages 3(1–2), 231–244 (Reprinted in E. Doron (Ed.), Language contact and the development
of Modern Hebrew , Studies in Semitic Languages and Linguistics, Brill (vol. 84)) .
Azar, M. (1995). The syntax of Mishnaic Hebrew . Jerusalem, Haifa: The Academy of the Hebrew
Language and University of Haifa Press. (in Hebrew) .
Bar-Ziv Levy, M. & Agranovsky. V. (2015). The evolution of the structure of free relative clauses in
Modern Hebrew: Internal development and contact language inﬂuence. Journal of Jewish
Languages 3 (1–2): 259–270. ( Reprinted in Doron, E. (Ed.), Language contact and the
development of Modern Hebrew , Studies in Semitic Languages and Linguistics, Brill (vol. 84 )).
Belinkov, Y., Magidow, A., Romanov, M., Shmidman, A. & Koppel, M. (2016). Shamela: A large-scale
historical Arabic corpus. In Proceedings of the Workshop on Language Technology Resources and
Tools for Digital Humanities (LT4DH at Coling) 2016 (pp. 45–53).
Bendavid, A. (1971). Biblical Hebrew and Mishnaic Hebrew . Tel Aviv: Dvir. (in Hebrew) .
Ben-H˙ayyim, Z. (1953). On the use of the phrase yes ˇ l-. Lĕšonénu La ‘am 4. ( in Hebrew ).
Ben-H˙ayyim, Z. (1992). The struggle for a language . Jerusalem: The Academy of the Hebrew Language.
(in Hebrew) .
Bolozky, S. (2009). Frequency and productivity in the verb system of Israeli Hebrew. Lĕšonénu, 71, 345–
367. (in Hebrew) .
Boneh, N. (2013). Mood and modality: Modern Hebrew. In G. Khan (Ed.), Encyclopedia of Hebrew
Language and Linguistics (Vol. 2, pp. 693–703). Leiden: Brill.
Claridge, C. (2008). Historical corpora. In M. Kyto ¨ &A .L u ¨ deling (Eds.), Corpus linguistics: An
international handbook (Vol. 1, pp. 242–259). Berlin: De Gruyter.
Culpeper, J., & Kyto ¨ , M. (2010). Early Modern English dialogues: Spoken interaction as writing .
Cambridge: Cambridge University Press.
Curzan, A. (2009). Historical corpus linguistics and evidence of language change. In M. Kyto ¨ &A .
Lu¨ deling (Eds.), Corpus linguistics: An international handbook (Vol. 2, pp. 1091–1109). Berlin: De
Gruyter.
Subcorpus Word count estimate (in version 2.1)
Responsa Literature 17th
to 19th centuries
7,026,451
(estimating the second half of the 19th c.: sixth of 42,158,711)
Responsa literature
twentieth century
24,465,243
(estimating the ﬁrst half of the 20th c.: half of 48,930,486)
Sifrei Chasidut 11,107,851
Total 42,599,545
123
A. Rubinstein

Doron, E. (2015). Introduction: Language contact and the development of Modern Hebrew. Journal of
Jewish Languages 3 (1–2): 5–26. ( Reprinted in E. Doron (ed.), Language contact and the
development of Modern Hebrew , Studies in Semitic Languages and Linguistics, Brill (vol. 84 )).
Doron, E. (2016). Language contact and the development of Modern Hebrew, Studies in Semitic
Languages and Linguistics (Vol. 84). Leiden: Brill.
Garcia Martinez, M., & Walton, B. (2014). The wisdom of crowds: The potential of online communities
as a tool for data analysis. Technovation, 34, 203–214.
Geyken, A. (2007). The DWDS corpus: A reference corpus for the German language of the 20th century.
In C. Fellbaum (Ed.), Collocations and idioms: Linguistic, lexicographic, and computational aspects
(pp. 23–41). London: Continuum Press.
Goldberg, Y., Adler, M. & Elhadad, M. (2008). EM can ﬁnd pretty good HMM POS-taggers (when given
a good start). In Proceedings of ACL -08: HLT (pp. 746–754).
Grosse, S., Grimberg, M., Ho ¨ lscher, T., Karweick, J., & Kuntz, H. (1987). Sprachwandel und
Sprachwachstum im Ruhrgebiet des 19. Jahrhunderts unter dem Einﬂuss der Industrialisierung.
Zeitschrift für Dialektologie und Linguistik, 54 (2), 202–221. (In German) .
HaCohen-Kerner, Y., Beck, H., Yehudai, E., & Mughaz, D. (2010). Stylistic feature sets as classiﬁers of
documents according to their historical period and ethnic origin. Applied Arti ﬁcial Intelligence, 24
(9), 847–862.
Hana, J., Feldman, A. & Aharodnik, K. (2011). A low-budget tagger for Old Czech. In Proceedings of the
5th ACL -HLT Workshop on Language Technology for Cultural Heritage, Social Sciences, and
Humanities (pp. 10–18).
Harshav, B. (1993). Language in time of revolution . Berkeley: University of California Press.
Howe, J. (2006). The rise of crowdsourcing . Wired 14(6). http://www.wired.com/2006/06/crowds/.
Accessed 11 Aug 2017.
Howe, J. (2008). Crowdsourcing: Why the power of crowd is driving the future of business . New York
City: Crown Business.
Itai, A., & Wintner, S. (2008). Language resources for Hebrew. Language Resources and Evaluation, 42
(1), 75–98.
Kaufmann, N., Schulze, T. & Veit, D. (2011). More than fun and money. Worker Motivation in
Crowdsourcing-A Study on Mechanical Turk. In Proceedings of the 17th Americas Conference on
Information Systems -AMCIS, 2011 (pp. 1–11).
Krause, T. & Zeldes, A. (2016). ANNIS3: A new architecture for generic corpus query and visualization.
Digital Scholarship in the Humanities 2016, 31 (1), 118–139.
Lehmann, H. M., auf dem Keller., C., & Ruef, B. (2006). ZEN Corpus 1.0. In R. Facchinetti & M.
Rissanen (Eds.), Corpus-based Studies of Diachronic English (pp. 135–155). New York: Peter Lang.
Liebeskind, C., Dagan, I., & Schler, J. (2016). Semiautomatic construction of cross-period thesaurus.
Journal on Computing and Cultural Heritage, 9 (4), 22.
Lin, Y., Michel, J. B., Aiden, E. L., Orwant, J., Brockman, W. & Petrov, S. (2012). Syntactic annotations
for the Google Books Ngram Corpus. In Proceedings of the ACL 2012 System Demonstrations, ACL
‘12 (pp. 169–174).
Meurman-Solin, A. (1995). A new tool: The Helsinki Corpus of Older Scots (1450–1700). ICAME
Journal, 19, 49–62.
Michel, J. B., Shen, Y. K., Aiden, A. P., Veres, A., Gray, M. K., Brockman, W., et al. (2011). Quantitative
analysis of culture using millions of digitized books. Science, 331, 176–182.
Morag, S. (1998). The contribution of the Geniza to the study of the Hebrew language. Jewish Studies, 38,
239–251. (in Hebrew) .
Morschheuser, B., Hamari, J. & Koivisto, J. (2016). Gamiﬁcation in crowdsourcing: A review. In Bui, T.
X. and Sprague Jr, R. H., (Eds.), In Proceedings of the 49th Hawaii International Conference on
System Sciences (pp. 4375–4384).
Mughaz, D., HaCohen-Kerner, Y., & Gabbay, D. (2017). Mining and using key-words and key-phrases to
identify the era of an anonymous text. In N. Nguyen, R. Kowalczyk, A. Pinto, & J. Cardoso (Eds.),
Transactions on computational collective intelligence XXVI. Lecture notes in computer science (Vol.
10190). Cham: Springer.
Neuman, Y. (2013). The diphthong [e ʸ] in Israeli Hebrew: Its origin and the factors conditioning its
distribution. In R. Ben-Shahar & N. Ben-Ari (Eds.), Hebrew— A Living Language, volume VI . Tel-
Aviv: The Porter Institute for Poetics & Semiotics Tel-Aviv University, HaKibbutz HaMeuchad. (in
Hebrew).
123
Historical corpora meet the digital humanities: the…

Piotrowski, M. (2012). Natural language processing for historical texts . San Rafael: Morgan & Claypool.
Reshef, Y. (2009). Continuity vs. change in the emergence of Standard Modern Hebrew: The verbal
system in the early Mandate period. In H. Cohen (Ed.), Modern Hebrew: Two hundred and ﬁfty years
(pp. 143–176). Jerusalem: The Academy of the Hebrew Language. (in Hebrew) .
Reshef, Y. (2012). Early Spoken Hebrew. In S. Izre’el (Ed.), The speech machine as a language teacher
Hebrew Spoken Here: Hebrew voices from Nazi Germany: A testimony on spoken Hebrew and Jewish
life in Palestine during the British Mandate (pp. 163–187). Tel Aviv: The Haim Rubin Tel Aviv
University Press. (in Hebrew) .
Reshef, Y. (2013). Revival of Hebrew: Grammatical structure and lexicon. In G. Khan (Ed.),
Encyclopedia of Hebrew Language and Linguistics (Vol. 3, pp. 397–405). Leiden: Brill.
Reshef, Y. (2016). Written Hebrew of the revival generation as a distinct phase in the evolution of
Modern Hebrew. Journal of Semitic Studies, 61 (1), 187–213.
Reshef, Y., & Helman, A. (2009). Instructing or recruiting? Language and style in 1920s and 1930s Tel
Aviv municipal posters. Jewish Studies Quarterly, 16, 306–332.
Rissanen, M. (2008). Corpus linguistic and historical linguistics. In M. Kyto ¨ &A .L u ¨ deling (Eds.),
Corpus linguistics: An international handbook (Vol. 1, pp. 53–68). Berlin: De Gruyter.
Ro¨ gnvaldsson, E., & Helgado ´ ttir, S. (2011). Morphological tagging of Old Norse texts and its use in
studying syntactic variation ad change. In C. Sporleder, A. van den Bosch, & K. Zervanou (Eds.),
Language Technology for Cultural Heritage: Selected papers from the LaTeCH workshop series (pp.
63–76). Berlin: Springer.
Rubin, A. D. (2013). Deﬁnite Article: Pre-Modern Hebrew. In G. Khan (Ed.), Encyclopedia of Hebrew
Language and Linguistics (Vol. 1, pp. 678–682). Leiden: Brill.
Rubinstein, A. (forthcoming). Existential possessive modality in the emergence of Modern Hebrew. In E.
Doron, M. Rappaport Hovav, Y. Reshef, M. Taube (Eds.), Linguistic contact, continuity, and change
in the genesis of Modern Hebrew. Amsterdam: John Benjamins ( to appear ).
Rubinstein, A., Sichel, I. & Tsirkin-Sadan, A. (2015). Superﬂuous negation in Modern Hebrew and its
origins. Journal of Jewish Languages 3 (1–2): 165–182. ( Reprinted in Doron, E. (Ed.), Language
contact and the development of Modern Hebrew , Studies in Semitic Languages and Linguistics,
Brill (vol. 84) ).
Rusinek, S. (2016). Kima: Towards an open digital historical Hebrew gazetteer. http://commons.pelagios.
org/2016/07/kima-towards-an-open-digital-historical-hebrew-gazetteer/. Accessed 11 Aug 2017.
Saxton, G. D., Oh, O., & Kishore, R. (2013). Rules of crowdsourcing: Models, issues, and systems of
control. Information Systems Management, 30 (1), 2–20. https://doi.org/10.1080/
10580530.2013.739883.
Schilling, N. (2013). Sociolinguistic ﬁeldwork. Cambridge: Cambridge University Press.
Schmied, J. (1994). The Lampeter Corpus of Early Modern English Tracts. In Kyto ¨ , M., Rissanen, M. and
Wright S. (Eds.), Corpora across the centuries: Proceedings of the First International Colloquium on
English Diachronic Corpora, Rodopi (pp. 81–89).
Shatil, N. (2007). The synchronic status of nitpa’el. Divrei ha- ḥug ha-yisr ’eli lavalshanut, 16, 105–127.
(in Hebrew) .
Shehadeh, H. (1991). Gilguley ha-bituy ‘yesh (lo) lilmod’/‘haya (lo) lilmod’. In M. H. Goshen-Gottstein,
S. Morag, & S. Kogut (Eds.), Studies on Hebrew and other Semitic languages presented to Professor
Chaim Rabin on the occassion of his seventy- ﬁfth birthday (pp. 415–442). Jerusalem: Academon
Press. (in Hebrew) .
Tsirkin-Sadan, A. (2015). Inheritance and Slavic contact in the polysemy of bixlal. Journal of Jewish
Languages 3 (1–2): 218–230. ( Reprinted in Doron, E. (Ed .), Language contact and the
development of Modern Hebrew , Studies in Semitic Languages and Linguistics, Brill (vol. 84) ).
Wigderson, S. (2015). The sudden disappearance of Nitpael and the rise of Hitpael in Modern Hebrew,
and the role of Yiddish in the process. Journal of Jewish Languages, 3 (1–2): 199–206. ( Reprinted
in Doron, E. (Ed.), Language contact and the development of Modern Hebrew , Studies in Semitic
Languages and Linguistics, Brill (vol. 84) ).
Xiao, R. (2008). Well-known and inﬂuential corpora. In M. Kyto ¨ &A .L u ¨ deling (Eds.), Corpus
linguistics: An international handbook (Vol. 1, pp. 383–457). Berlin: De Gruyter.
Ya´ n˜ez-Bouza, N. (2015). ‘Have you ever written a diary or journal?’ Diurnial prose and register variation.
Neuphilologische Mitteilungen, 116 (2), 449–474.
Zhao, Y. & Zhu, Q. (2014). Effects of extrinsic and intrinsic motivation on participation in crowdsourcing
contest. Online Information Review, 38 (7), 896–917.
123
A. Rubinstein

Zheng, H., Li, D., & Hou, W. (2011). Task design, motivation, and participation in crowdsourcing
contests. International Journal of Electronic Commerce, 15 (4), 57–88.
Zipser, F. & Romary, L. (2010). A model oriented approach to the mapping of annotation formats using
standards. In Proceedings of the Workshop on Language Resource and Language Technology
Standards, LREC 2010 . Malta. URL: http://hal.archives-ouvertes.fr/inria-00527799/en/.
Zohar, H., Liebeskind, C., Schler, J., & Dagan, I. (2013). Automatic thesaurus construction for cross
generation corpus. Journal on Computing and Cultural Heritage, 6 (1), 4.
Publisher's Note Springer Nature remains neutral with regard to jurisdictional claims in published
maps and institutional afﬁliations.
Historical corpora meet the digital humanities: the…
123
```
