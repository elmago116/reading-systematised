---
title: "One schema to rule them all: How Schema.org models the world of search"
author: Andrew Iliadis, Amelia Acker, Wesley Stevens, Sezgi Başak Kavakli
year: "2023"
Type: Article
DOI: 10.1002/asi.24744
source: https://doi.org/10.1002/asi.24744
created: 2026-04-24
description: "AbstractSeveral industry‐specific metadata initiatives have historically facilitated structured data modeling for the web in domains such as commerce, publishing, social media, and so forth. The metadata vocabularies produced by these initiatives allow developers to “wrap” information on the web to "
tags:
  - op/acc/pending-review
  - Tech/SemanticWeb
  - tech/metadata
  - LIS
pdfORepub: "[[One schema to rule them all How Schema.org models the world of search.pdf]]"
---

[[One schema to rule them all How Schema.org models the world of search.pdf]]

> **Abstract:** AbstractSeveral industry‐specific metadata initiatives have historically facilitated structured data modeling for the web in domains such as commerce, publishing, social media, and so forth. The metadata vocabularies produced by these initiatives allow developers to “wrap” information on the web to provide machine‐readable signals for search engines, advertisers, and user‐facing content on apps and websites, thus assisting with surfacing facts about people, places, and products. A universal iteration of such a project called Schema.org started in 2011, resulting from a partnership between Google, Microsoft, Yahoo, and Yandex to collaborate on a single structured data model across domains. Yet, few studies have explored the metadata vocabulary terms in this significant web resource. What terms are included, upon what subject domains do they focus, and how does Schema.org represent knowledge in its conceptual model? This article presents findings from our extraction and analysis of the documented release history and complete hierarchy on Schema.org's developer pages. We provide a semantic network visualization of Schema.org, including an analysis of its modularity and domains, and discuss its global significance concerning fact‐checking and COVID‐19. We end by theorizing Schema.org as a gatekeeper of data on the web that authors vocabulary that everyday web users encounter in their searches.
## Full text (extracted from `One schema to rule them all How Schema.org models the world of search.pdf`)

*Source:* `2PDF/One schema to rule them all How Schema.org models the world of search.pdf`  
*Extracted:* 2026-04-24

```text
RESEARCH ARTICLE
One schema to rule them all: How Schema.org models
the world of search
Andrew Iliadis1 | Amelia Acker 2 | Wesley Stevens 3 | Sezgi Bas¸ak Kavakli4
1Klein College of Media and
Communication, Department of Media
Studies and Production, Temple
University, Philadelphia,
Pennsylvania, USA
2School of Information, University of
Texas at Austin, Austin, Texas, USA
3College of Information and
Communications, School of Journalism
and Mass Communications, University of
South Carolina, Columbia, South
Carolina, USA
4Klein College of Media and
Communication, Media and
Communication Doctoral Program, Temple
University, Philadelphia, Pennsylvania, USA
Correspondence
Andrew Iliadis, Klein College of Media
and Communication, Department of
Media Studies and Production, Temple
University, 2020 N. 13th Street, Room 225,
Philadelphia, PA 19122, USA.
Email:
andrew.iliadis@temple.edu
Funding information
Temple University
Abstract
Several industry-specific metadata initiatives have historically facilitated struc-
tured data modeling for the web in domains such as commerce, publishing,
social media, and so forth. The metadata vocabularies produced by these initia-
tives allow developers to“wrap” information on the web to provide machine-
readable signals for search engines, advertisers, and user-facing content on
apps and websites, thus assisting with surfacing facts about people, places, and
products. A universal iteration of such a project calledSchema.org started in
2011, resulting from a partnership between Google, Microsoft, Yahoo, and
Yandex to collaborate on a single structured data model across domains. Yet,
few studies have explored the metadata vocabulary terms in this significant
web resource. What terms are included, upon what subject domains do they
focus, and how doesSchema.org represent knowledge in its conceptual model?
This article presents findings from our extraction and analysis of the documen-
ted release history and complete hierarchy onSchema.org's developer pages.
We provide a semantic network visualization of Schema.org, including an
analysis of its modularity and domains, and discuss its global significance con-
cerning fact-checking and COVID-19. We end by theorizingSchema.org as a
gatekeeper of data on the web that authors vocabulary that everyday web users
encounter in their searches.
1 | INTRODUCTION
Metadata are central to web and internet processes in
that they help organize and structure data (Greenberg,
2005; Iliadis et al., 2021; Mayernik & Acker, 2018;
Pomerantz, 2015). One can merely think about how
search engines or online retailers structure information
in results, including menus and knowledge panels. Sev-
eral industry-specific metadata initiatives have histori-
cally facilitated structured data modeling for the web in
domains such as commerce, publishing, social media,
and so forth (Guns,
2013). The standardized metadata
vocabularies produced by these initiatives allow web
developers to “wrap” information on the web to provide
machine-readable signals for advertisers and user-facing
content on apps and websites. Thus, metadata assist with
information search and surfacing specific facts about peo-
ple, places, and products (Acker,
2021). Where such
efforts were once fragmented across industries, today,
this landscape is changing with globally coordinated
efforts to create a universal structured data model across
fields. The implications of such a model have
Received: 26 May 2022 Revised: 29 January 2023 Accepted: 31 January 2023
DOI: 10.1002/asi.24744
This is an open access article under the terms of theCreative Commons Attribution-NonCommercialLicense, which permits use, distribution and reproduction in any
medium, provided the original work is properly cited and is not used for commercial purposes.
© 2023 The Authors.Journal of the Association for Information Science and Technologypublished by Wiley Periodicals LLC on behalf of Association for Information Sci-
ence and Technology.
460 J Assoc Inf Sci Technol.2025;76:460–523.wileyonlinelibrary.com/journal/asi


far-reaching consequences concerning the monopoliza-
tion, centralization, and exploitation of data resources.1
One such project,Schema.org, started in 2011 and is
the result of a partnership between Google, Microsoft,
Yahoo, and Yandex— organizations that are traditionally
commercial competitors but decided to collaborate on a
single structured data model for the web to benefit their
search products (Guha et al., 2016). Today, millions of
websites and applications use theSchema.org structured
data model to assist with information search and
retrieval, including news organizations involved in verify-
ing misinformation and fact-checking with structured
data (Adair,
2020). The schema also feeds data to virtual
assistant products such as Alexa and Google Assistant
which pull structured data from the web to answer
queries (Kollar et al.,
2018). Such practices show the ben-
efits of using a single structured data model for the inter-
operability of web data across sites and applications. Yet,
scholars have not adequately attended to the conceptual
model of
Schema.org's metadata vocabulary and its
domain coverage (i.e., what topics it includes) relative to
its central role in structuring experiences of the web. In
its positioning as a global web schema,
Schema.org acts
as a conceptual model of the world for search engines.
As such, this partnership between internet companies engen-
ders values, goals, and aspirations that have far-reaching
consequences beyond searching for pizza delivery or the
latest news headline.
One way to interpret
Schema.org is to accept the defi-
nition provided on its website. TheSchema.org website
states that the project was made“to make it easier for
webmasters to provide us with data so that we may better
direct users to their sites.” Schema.org is a self-described
“collaborative, community activity with a mission to cre-
ate, maintain, and promote schemas for structured data
on the internet, on web pages, in email messages, and
beyond.” The website makes several other distinctions,
including that the metadata“hierarchy presented on this
site is not intended to be a “global ontology” of the
world… it is still the case thatschema.org is not intended
as a universal ontology.” The website also states that
“applications from Google, Microsoft, Pinterest, Yandex
and others already use these vocabularies to power rich,
extensible experiences” (
schema.org). Figure1 shows the
FIGURE 1 Beginning of theSchema.org metadata vocabulary (schema.org)
ILIADIS ET AL. 461
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


beginning of the Schema.org metadata vocabulary in
plain English. Figure2 represents a metadata vocabulary
item using JavaScript Object Notation for Linked Data
(JSON-LD) syntax.
As infrastructures for facilitating information interoper-
ability, projects such asSchema.org are a less visible aspect
of the web when compared to platforms like Facebook,
TikTok, and Google, but information science scholars have
long emphasized the necessary and often invisible power
of classification standards in information infrastructures
(Bowker et al.,
2010;B o w k e r&S t a r ,1999;S t a r ,1999).
Recent advancements in structured data modeling, knowl-
edge graphs, and the reach of the internet allow companies
to leverage metadata vocabularies and crawl the machine-
readable data on the web as if it were a single database of
facts and assertions. Such processes allegedly help these
companies represent “knowledge” in their products, like
the knowledge panels in search engine results and the
maps and menus of service applications (Noy, Gao et al.,
2019). Structured data thus increasingly provide underlying
semantics and context-control related to content for devel-
opers while also“intuitively” helping users find what they
are looking for on apps and websites without relying on
specific keywords in their searches. For developers, such
structured data modeling allows for a faster, dynamic dis-
play of information for users. For users, this data modeling
allows for dynamic webbing across platforms like Insta-
gram, Amazon, and Netflix, tracking and anticipating their
next search or action. Structured data are at once both hid-
den and increasingly an expectation of responsive personal-
ization design of platforms (Acker & Donovan,
2019).
Projects like Schema.org are a kind of compre-
hensive “crosswalk” intended to avoid the convoluted
intersecting of multiple schemas, which can overburden
web administrators and create confusion and can even
resolve the multiple schemas problem by harmonizing
web information through a central structured data pro-
ject. Yet, as a global structured data model,
Schema.org is
a gatekeeper of structured data on the web. The schema
authorizes the metadata vocabulary that web administra-
tors and everyday web users encounter in their platforms
and applications. Up to now, relatively few critical stud-
ies have explored the development and release of the
metadata vocabulary terms in this significant web
resource. What terms are included, upon what subject
domains do they focus, and how does
Schema.org repre-
sent knowledge in its conceptual model? This article pre-
sents results from our extraction and analysis of the
metadata vocabulary's release history and complete hier-
archy located on
Schema.org's developer pages. We pro-
vide a semantic network visualization of Schema.org,
including an analysis of its modularity and domains, and
discuss its global significance concerning fact-checking
and coronavirus (COVID-19). We end by theorizing
Schema.org as a gatekeeper of data on the web that
authors vocabulary that everyday web users encounter in
their searches.
2 | DEFINING SCHEMA.ORG
Some terminological clarification is needed to understand
Schema.org's role across the web, given that the term
refers to several things at once.Schema.org is each of the
following: (1) a universal metadata vocabulary, (2) an
administrative body with people who work for large
internet companies, volunteers, and a governance struc-
ture, and (3) a website with code examples, release his-
tory, and term hierarchy. A final (4) category might be
how
Schema.org is applied and operationalized by web
FIGURE 2 Example of a metadata
vocabulary item represented in JSON-
LD (schema.org)
462 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


administrators and developers“in the wild.” This process
is often orthogonal to its creators’ originally intended
aims and purposes. Designs such as the conceptual model
offered bySchema.org's metadata vocabulary are not con-
sistently implemented in the ways that producers antici-
pate. In what follows, our concern is not with the
implementation of
Schema.org across the web in the
“real world” (definition 4) but instead with the metadata
vocabulary itself (definition 1). We set aside questions of
its organization and governance (definition 2) and web-
site (definition 3) for our discussion and conclusion. We
acknowledge that there is frequently a disconnect
between design and deployment (Iliadis & Pedersen,
2018; Liao & Iliadis, 2021), especially in the world of
metadata where people design models and tools that fail
to reach a critical mass of adopters or differ in their
implementation (Maron & Feinberg,
2018). Such discon-
nects have been theorized as instances of technological
de-scription where there are different conceptualizations
between creators and potential users (Akrich,
1992). We
thus reserve some of our broader and speculative claims
concerning
Schema.org's role in gatekeeping for our dis-
cussion and conclusion, and suggest additional studies
that can be carried out either quantitatively with usage
data or qualitatively with user studies. Indeed, studies
focusing on
Schema.org's use, adoption, and validation
are beginning to appear (Meusel et al.,2015; Paulheim,
2015; Şims¸ek et al.,2018). The present work strictly con-
cerns the metadata vocabulary that Schema.org offers,
and merely theorizes the project's more prominent
position on the web as a type of gatekeeper.
3 | LITERATURE REVIEW
3.1 | Schema.org's role in semantic
platformization
Metadata vocabularies like the kind offered bySchema.
org are part of a long history of implementing machine-
readable semantics on the internet to enable greater data
integration across platforms. Recent studies into the
social significance of data integration tools like applica-
tion programming interfaces (APIs) have shown that
such technologies facilitate platformization (Berry et al.,
2015; Bucher, 2013). Platformization has been said to
entail the “extension of social media platforms into
the rest of the web and their drive to make external web
data ‘platform ready’” (Helmond,
2015). Concurrently,
research into digital information infrastructures (such as
the structured data offered bySchema.org) has developed
adjacent to these platform-oriented approaches (Bowker
et al., 2010; Edwards et al.,2009) with a subset focusing
on online knowledge infrastructures for sharing things
like research data (Edwards et al., 2013; Karasti et al.,
2016) and ensuring their long-term preservation (Acker,
2019; Acker & Kriesberg, 2020). More recently, there
have been calls to combine these infrastructure and
platform-based frameworks to examine information
exchange mechanisms on the web through digital tools
for knowledge sharing (Plantin et al.,
2016).
Our paper builds and extends the critical work on
these platform and infrastructure studies in what has
been referred to as“knowledge as programmable object”
(Plantin et al., 2016) by explicitly focusing on recent
advancements in structured data modeling across web
platforms. As Bucher (2012, 2013) and Helmond (2015)
show data portability in the context of web platforms
requires a certain level of semantic annotation. This
semantic interoperability is perhaps one of several defin-
ing features of the web, or what has been referred to by
computer scientists as the “semantic web” (Antoniou
et al.,
2012; Szeredi et al.,2014). Since its inception as a
global project reaching back to the beginnings of the web
in the early 1990s, semantic web practitioners have privi-
leged the status of metadata for providing fine-grained
levels of contextual expressivity needed for machine-
readable web data. Now web semantics are commonplace
in products like knowledge panels, virtual assistants like
Siri and Alexa that rely on Wikidata, and other sources
that engage markup in platformized versions of knowl-
edge representation.
Schema.org thus contributes to the
increasing semantic platformization of the web by
enabling data integration through applications of its
metadata vocabulary.
3.2 | The semantic web
The semantic web is a longstanding internet project
focused on an interconnected group of technologies, stan-
dards, and methods for improving data interoperability
across the web (Calaresu & Shiri,
2015). Schema.org is a
modern outgrowth of the semantic web project, which
was originally initiated by web inventor Sir Tim Berners-
Lee through his World Wide Web Consortium (W3C)
standards body. W3C produces web standards such as the
Resource Description Framework (RDF) (a structured
data model standard).
2 The Schema.org website plainly
states that the data model used therein is“derived from
RDF Schema” which Berners-Lee's W3C previously pub-
lished. Schema.org founders and leadership also have or
had close ties to W3C. These people include Dan Brick-
ley, who runs the daily operations forSchema.org and is
on the steering group as Google's representative (Brickley
previously developed RDF and semantic web technology
ILIADIS ET AL. 463
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


at W3C). Ramanathan Guha, also from Google, initiated
Schema.org and is one of its founders (Guha previously
co-edited the RDF Schema specification with Brickley).
The website further states that “since April 2015, the
W3C Schema.org Community Group is the main forum
for collaboration” and that current Chief Operating Offi-
cer of W3C Ralph Swick (along with Vint Cerf)“helped
establish the relations between Schema.org and the
W3C.” Though Schema.org has close ties to the W3C it is
not an official part of the W3C nor is it considered one of
their standards, indicating on their website thatSchema.
org is not“a standards body like the W3C.”
Previous studies have discussed the semantic web
before the rise ofSchema.org, focusing either on histori-
cal and philosophical conceptions of the semantic web,
on notable standards bodies like the W3C, or public and
institutional use of semantic web technologies such as in
libraries, governments, and laboratories. Few studies
(McCarthy,
2017; Patel-Schneider, 2014) have attempted
to examine Schema.org from critical or sociological per-
spectives, and those that do have not commented on the
metadata vocabulary of
Schema.org, nor have they pro-
vided any substantial empirical evidence ofSchema.org's
domain coverage and conceptual model in this era of
semantic platformization.
3.3 | Critical histories of the
semantic web
Several studies have critically examined the social history
of the semantic web and its ideal of a universal standard
semantics for the internet. Guns (2013) charts its linguis-
tic and intellectual history and argues that as features
present in early web standards, linking and metadata
connect the semantic web to early artificial intelligence
work involving semantic networks. Adding to this his-
tory, Hallo et al. (
2016) describes the concept of“linked
data” (primarily understood as the second“wave” of the
semantic web) and examine libraries' attempts to gather
and share data on the semantic web to highlight pro-
cesses for data integration. Following Guns' theoretical
concerns, Hallo et al. discuss the linguistic and concep-
tual ontologies that underscore linked data and consider
the more significant societal and practical implications of
global shifts in data storage and accessibility.
Other information researchers map the fascinating con-
ceptual “prehistory” of knowledge representation technolo-
gies on the web that have shaped and given rise to the
semantic web's ontological and individualized underpin-
nings. Wang (
2019) maps a conceptual history of domain
analysis and knowledge organization on the semantic web,
tracing notable scholars in semantics research. Machado
et al. (2018) provide a historical concept of the semantic
web, beginning in the late 1990s, through an examination
of the publications of Berners–Lee. The review draws
concrete definitions of linked data and related terms, offer-
ing an operationalization of web semantics within the con-
text of data and intelligent, automated information systems.
Similarly, Swanson (
2020) charts the rise of informa-
tion systems and their role as new social and economic
infrastructures which govern daily life for individuals
and institutions alike. Reflecting on historical develop-
ments in finance, retail automation, and digital com-
merce over the last several decades, Swanson provides a
foundation and context to understand the semantic web
and its embeddedness in the everyday lives of web users.
Halford et al. (
2013) also critically examine semantic web
tools and technologies and how these both complicate
and structure current iterations of knowledge production
on the web. Each of the above studies offers portions of
semantic web history, underscoring a critical dimension
to web semantics that we further take up in this article.
3.4 | Conceptualizing digital objects
Other studies have attempted to provide a formal defini-
tion for semantic “digital objects” in the context of the
semantic web, often interrogating data models such as the
triples represented in RDF's modeling of subjects, predi-
cates, and objects. Conceptualizing “digital objects” as
semantic data, Hui (
2016) examines how modern-day
semantic systems have a social and philosophical lineage.
Campbell (
2009) takes Foucault's historicization of medi-
cal classification techniques and practices and applies
them to semantic web technologies. The triadic relation-
ship that emerges is posited as helpful in theorizing the
semantic web's taxonomic, descriptive, and analytic
dimensions, further addressing semantic search systems in
creating technological rationality. Greenberg (
2005)l i k e -
wise explores how metadata has been operationalized and
offers a reconceptualization of metadata schemes and how
the human component involved in shaping digital objects
poses critical considerations related to how these technol-
ogies permeate and govern aspects of social life.
The work of Kallinikos (
2010) examines digital tech-
nologies and the semantics of information objects and
how “information is a subset of culture” (p. 4) including
“the meaning of information tokens” (p. 10). Kallinikos
et al. (2010, 2013) discern “digital objects” on the web
and their function by further exploring how search
engines ultimately shape the way a digital object is
located, authenticated, and understood, arguing that
these processes are embedded in a fundamentally social
context and that, as such, semantic entities that make
464 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


these processes possible must take some measure of
responsibility for them. McCarthy (2017) offers one of the
first sociological analyses of Schema.org and the digital
objects which structure the modern semantic web, and,
subsequently, how knowledge is represented through
semantic triples such as those identified in the RDF data
model. McCarthy thus examines the “instability” that
accompanies the semantic web, which largely remains
invisible through search engines, algorithms, and other
associated tools.
3.5 | Political economies of semantic
infrastructures
DeNardis (2009, 2014)a n dR u s s e l l(2011, 2014)d e t a i lt h e
governance of internet infrastructure by examining the
r o l e st h a ti n s t i t u t i o n ss u c ha sW 3 Cp l a yw h e r ei n f o r m a t i o n
is controlled, manipulated, and eventually commodified by
platform companies. At a lower level of abstraction,
Edwards et al. (
2011) offer a reconceptualization of meta-
data not as an outcome of fixed product search mecha-
nisms but as a fluid and temporal process of collaboration,
arguing that the very nature of metadata renders it a signi-
fier of the unfinished and in-progress. Researchers have
foregrounded these explicitly political issues related to net-
worked semantics on the web. Waller's (
2016) and Poirier's
(2017, 2019) ethnographic studies examine how infrastruc-
tures on the semantic web (e.g., taxonomies, schemas, and
ontologies) are built and reveal the power dynamics
embedded in their creation and use. Beghtol (2005)o f f e r sa
specific set of global actionable solutions for making more
ethical decisions when creating and maintaining knowl-
edge representations in information systems, arguing for
more thoughtful treatments ofinstitutionally backed sys-
tems. Douglas et al. (
2018)e x p l o r et h ee x t e n tt ow h i c h
linked data provides meaningful solutions for decolonizing
archival work, arguing that linked data can better represent
more complex connections that can be used to include
marginalized perspectives in archives.
In line with these ethical and political insights, Ford
and Graham (
2016a, 2016b) examine linked data and how
platforms (e.g., Wikipedia and Google, respectively) utilize
linked data to depoliticize cultural constructions of place
while dismissing alternative voices through digital tools. Sri-
nivasan (
2013) argues that research and cultural under-
standings of ontologies are primarily understood through a
Eurocentric perspective, asserting this needs to be de-
centered for a more culturallydiverse set of codes for new
media. Others have examined the political contexts where
ontologies are used in military, security, and surveillance
contexts (Iliadis,
2018; Iliadis,2019; Iliadis & Acker,2022)
and in their service operations.
Schema.orgpresents itself as a community collaboration
between nonprofits, standards organizations, and corpo-
rate partners in the service of web administrators and
users who will benefit from the structured data model.
Yet, as a seemingly general-use structured data model,
Schema.org distances itself from the label of being a
global or universal ontology.Schema.org thus represents
a unique opportunity to study the emergence of a world-
wide metadata vocabulary that can play a significant
moderating role concerning how web data are shared
and displayed on major web applications and platforms.
As
Schema.org grows and becomes a critical infrastruc-
ture in structured data modeling across the web, the
terms and vocabularies expressed through its ontology
also represent what the organization considers worthy
of knowledge representation. With these conceptual
models in mind, we ask the following two research ques-
tions concerning how
Schema.org grows its metadata
vocabulary:
RQ1: Since the beginning ofSchema.org's release his-
tory, what kinds of terms have been included in
the Schema.org metadata vocabulary?
RQ2: What do the terms in Schema.org's metadata
vocabulary tell us about Schema.org's domain
coverage (i.e., the topic areas of focus)?
4 | METHODS
We wanted to learn more about the terms inSchema.
org's metadata vocabulary and the conceptual model that
emerges from it; to answer our research questions, we
obtained digital materials from the Schema.org website
and developer pages. First, we scraped the documented
release history of the
Schema.org updates and manually
created a summary of the kinds of vocabulary topics
included for discussion in each release.3 We then pro-
cessed the text of the complete release history using
Wordlist Maker to extract unique terms from the corpus.4
We removed non-schema-related words and isolated
all the schema terms contained in the release history
(n = 970). The full text of theSchema.org release history,
documented updates, and an alphabetical list of schema
terms are available in Tables
A1 and A2.
Once we obtained the release history and distilled the
schema terms, we also wanted to represent the complete
metadata vocabulary hierarchy in a data visualization to
observe what domain clusters appear (i.e., which terms/
topics are more central in the metadata vocabulary). To
visualize
Schema.org's ontology in a semantic network,
we downloaded two CSV files (Types and Properties) con-
taining the Schema.org ontology from the Schema.org
ILIADIS ET AL. 465
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


developers page and processed them using Gephi
(Bastian et al., 2009).5 Using Gephi's interaction tech-
niques, we explored the Schema.org ontology and cus-
tomized the visualization by expanding the hierarchy
to display the nodes (representing vocabulary terms)
and edges (representing subTypeOf relationships).
After importing the CSV material to Gephi, the For-
ceAtlas2 layout algorithm was employed to expand the
network for an improved visualization (Jacomy et al.,
2014). The nodes were resized according to their
degree ranking (min 100 to max 1,500). The network's
modularity was calculated using Gephi's statistics tools
to observe communities (i.e., clusters of topics) in the
metadata vocabulary (Gephi uses the Louvain method
for detecting communities in networks described in
Blondel et al. [
2008]). All data we collected can be
accessed via the Schema.org links in the footnotes
provided in this section (ours was collected as of
05/11/22). The data thus represent
Schema.org's meta-
data vocabulary in a “snapshot” or moment in its
growth rather than chronologically over time or by
future projections.
5 | ANALYSIS AND FINDINGS
As of this writing, theSchema.org release history contains
14 significant updates and 53 total updates ranging from
release 0.91 (released April 21, 2012) to release 14.0
(released March 17, 2022).
Schema.org's vocabulary cur-
rently consists of 797 Types, 1,453 Properties, 14 Datatypes,
86 Enumerations, and 462 Enumeration members. The
semantic network contains 1,387 nodes and 1,344 edges in
a directed graph, which we represent in Figure
3. The net-
work's modularity is 0.925, showing that the network is
highly clustered in nature, with communities numbering
73 and an average degree of 0.969. Figure
4 shows the size
distribution of nodes among each modularity class. A sum-
mary of the types of terms included for discussion in each
o ft h er e l e a s e si si nT a b l e
1. The average weighted degree is
0.969 (average total of the weights of edges linked to a
node) with a diameter of 5 (the maximum distance between
nodes in the graph), an average path length of 2.319 (aver-
age number of steps from one random node to another),
and a density of 0.001 (how many links between nodes exist
compared to how many links between nodes are possible).
FIGURE 3 Schema.org semantic network visualization
466 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


The 970 unique terms extracted from the release his-
tory range across various fields, and some topics appear
to be added out of necessity based on current events.
There are terms related to content moderation (an evolv-
ing concern given the proliferation of material on social
media sites that goes against their terms of service, as
explained in Gillespie [
2018] and Roberts [2019]), fact-
checking and misinformation (another area of increasing
importance given the recent increase in media manipula-
tion and disinformation campaigns online, as explained
in Marwick and Lewis [
2017] and Benkler et al. [2018]),
educational activities, and identifying media artifacts,
among many others. Other than the topics that appear to
be of increasing global concern, there does not seem to
be consistent logic concerning the types and kinds of
metadata terms discussed and included in the
Schema.
org model. Indeed, possible community extensions to
Schema.org vocabulary are proposed and temporarily
hosted on a pending ad hoc basis before they are
included in the Schema.org core, as explained on the
website.
These schema terms range from simple entities and
relationships in which “regular” everyday web users
might be interested (such as locating information about
employment or education) to more complex instances
where specialists and experts would likely be the benefi-
ciaries of the terms. The range of complexity represented
in the unique terms contained in the
Schema.org release
history indicates Schema.org's coverage and possible
application areas, spanning several domains and indus-
tries. For example, designating actions on the web are
described, such as acquiring license pages and applica-
tions, providing feedback policies, or giving opinions, all
of which can be used by web administrators to surface
such actions in search results. More specialized terms
related to fact-checking and misinformation labeling are
provided through “review of claim ” and “review of
media” terms which news organizations can use to mark
up their news stories and surface warnings in the news
feed. Educational programs, credentials, occupations,
events, and requirements terms are included for facilita-
tors to boost these data points in their profiles for poten-
tial students searching for information.
While the unique terms in the
Schema.org release his-
tory point to areas that have recently been under develop-
ment, Schema.org's current core vocabulary shows what
might be considered the earliest and seemingly most
important domains for the project. For example, our
semantic network offers that the high-level representa-
tions in the
Schema.org hierarchy include top-level
domains for vocabulary items relating to the categories of
Person, Organization, Place, CreativeWork, Intangible,
Action, MedicalEntity, and Event. The core categories
illustrate the datafication of life within several areas,
from tech industries to creative work. These top-level
domains are relatively abstract and less specific than the
lower-level vocabulary items, clearly indicating that from
the beginning,
Schema.org was intended to organize its
structured data as knowledge across a wide variety of
domains.
Details in our semantic network show several features
of the Schema.org core hierarchy, including which hier-
archy terms are subclasses of higher-level domain terms
and which terms belong to specific clusters of related
terms. For example, the CreativeWork category in the
network has a high degree of centrality and connects to
FIGURE 4 Schema.org modularity
size distribution
ILIADIS ET AL. 467
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


media texts, production, and consumption entities. Here,
creative works are understood as units or types of labor,
illustrating a schema's role in shaping normative stan-
dards of cultural production and consumption (Craig &
Cunningham,
2019; Napoli & Caplan, 2017). Similarly,
the Place categorization privileges locations related to
culture, tourism, and commerce (i.e., where people are
likely to spend money and leisure time).
TABLE 1 Topics covered in theSchema.org releases
Release version (date) Topics addressed in vocabulary
14:14 (2022) Search and rescue; adult oriented goods and services; online businesses; funding
13:13 (2021) Biology and life science, biochemistry, molecular entities, and chemicals; merchant return
policies, return shipping, damaged products, labels, policies; job applications and postings;
fact-checking and misinformation including reviews of media and claims; casual opinion
claims unrelated to news or factual records; positive and negative reviews; countries of
processing and assembly
12:12 (2021) Ineligible regions; durations of media episodes; structured sizes and measurement;
backorders and item availability; health aspects relating to vaccines, health access,
allergies, safety, pregnancy; occupational experience and requirements
11:11.0, 11.01 (2020) Offline and online events; animated stories; prices, invoices, down payments, cleaning fees,
billing start/end dates; seeking and actions related to video content; math actions and
solutions; learning and educational resources; copyright and credit notices
10:10.0 (2020) Educational questions, learning resources, and courses; floorplans and layout images; energy
efficiency, consumption
9:9.0 (2020) Learning resources, creative works, and quizzes; product groups and variations; boat
reservations and boat trips
8:8.0 (2020) Non-profit status, organizations, and types; delivery times, shipping destinations, rates and
details; citizenship, legal, and visa requirements for job postings
7:7.0, 7.01, 7.02, 7.03, 7.04 (2020) School districts; special announcements and locations; hospital reporting; hackathons; start
and end times for schedules; COVID-19
6:6.0 (2020) Media collections such as images, videos, or media galleries; 3D modeling; financial aid and
educational occupational programs; job posting features such as security clearance or
physical abilities
5:5.0 (2019) Health aspects; features within web sites, including pages, sites, and site elements; property
information related to accommodations and real estate listings such as bathrooms, floor
level, and lease length
4:4.0 (2019) Real estate information, purchase offers and losing information; podcast information related
to series, seasons, episodes; sport teams information, including gender of athlete; job
opening, employment, and unemployment information
3:3.0, 3.1, 3.2, 3.3, 3.4, 3.5, 3.6, 3.7, 3.8,
3.9 (2016–2019)
Life sciences; lodging and rental information, amenities, check in times; social media posts;
recipe information like cook time and preparation time; health warnings for breastfeeding,
prescriptions, and health conditions; course information, enrollment, prerequisites; how to
directions for structured steps of instructions; claim type and claim review features to
support fact checks; legislation; tourism, tourist attractions
2:2.0, 2.1, 2.2 (2015) Automotive/car properties, engine specifications, fuel/safety features; exercise courses,
exercise related diets, health and fitness actions; payment features such as due dates,
actions, receipts; geographic place names for different locations (home, work, gym),
including radiuses and midpoints between locations
1:1.1, 1.2, 1.3, 1.4, 1.5, 1.6, 1.7, 1.8, 1.91,
1.92, 1.93 (2013–2015)
Audiences, publishers, technical publishing; citations to scholarly sources, creative works,
medical articles; actions, potential and in the past; civic services, government services;
television and radio content, video games series, episodes, role names; not-for-profit offers,
sales, and item conditions for used goods; reservations for meals, hotels, airlines, or trips;
question and answer features for questions, answers, facts; work performance, music
events, live event announcements; visual arts, editions, forms, materials, surface
0:0.91, 0.95, 0.96, 0.97, 0.98, 0.99 (2012) Family members; software applications, mobile applications, web applications; medical and
health care entities; time and temporality features, timezones
468 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


The Intangible category hierarchizes purchasing
behaviors and commodities, a common theme among all
the second-level entities (beyond the top-level entity
Thing). Moreover, some items appear far less tangible
than others (e.g., the difference between making a
reservation, purchasing a ticket, or enumeration). This
category includes sub-level items such as Brand,
MerchantReturnPolicy, and MediaSubscription. What is
notable here is not necessarily how well these items fit
within the assigned category but the extent to which each
class is defined by purchasing behaviors, cultural com-
modities, and creative labor. The privileging of creative
work and focus on cultural labor made possible through
the metadata vocabulary provided illustrates the complex
webs of meaning-making within these spheres and the
role that
Schema.org plays in legitimizing and making
those meanings accessible to the people who use them.
We note here that developers themselves use their labor
to mark up their content with the vocabulary and thus
are also involved in work by giving their labeling labor to
search companies. Scholars have researched such uneven
labor practices in the context of data workers. Irani
(
2013) has examined unfair labor practices in the context
of microworkers involved with Amazon's Mechanical
Turk crowdsourcing website, and Posada (
2022) has simi-
larly examined unjust labor in the context of data
annotators.
Several other interesting entities appear in the
Schema.org hierarchy, including ClaimReview, which
enables developers to markup news stories with fact-
checks, so they appear as such in search results, and
terms related to COVID-19, including CovidTestingFaci-
lity, SpecialAnnouncement, and eventAttendanceMode.
5.1 | Fact-checks and misinformation
Since 2016, Schema.org appears to have released vocabu-
lary to combat conspiracy theories and misinformation on
the internet. One term, ClaimReview, enables developers to
m a r k u pn e w ss t o r i e sw i t hf a c t - c h e c k st oa p p e a ra ss u c hi n
search results. A detail of the cluster to which ClaimReview
belongs in our semantic network is represented in Figure
5.
Google announced the display of this feature on October
13, 2016. The use of this tool grew in connection to the fake
news debates surrounding the 2016 US presidential election
(Bing introduced support for fact-checks using ClaimRe-
view on September 14, 2017). ClaimReview positions
Schema.org and Google as critical arbiters of what is credi-
ble, leveraging the perception of their widespread legiti-
macy as a source of information.
Alexios Mantzarlis, the former News and Information
Credibility Lead at Google News Lab, writes that“fact-
checking initiatives around the world mark up their work
with ClaimReview, which allows fact-checkers to signal—
and anyone online to automatically detect— that a web-
page contains a fact check” (Mantzarlis,
2019). Google's
Fact Check Explorer is a search feature to discover fact-
checks, including those that use the ClaimReview
markup. Academic researchers are also interested in
ClaimReview and are involved in spreading literacy about
the feature. The Duke Reporters’ Lab runs the ClaimRe-
view Project initiative that shares information about the
fact-check function (Lim,
2019). A similar project, Full
Fact, is a registered charity and consists of“a team of inde-
pendent fact-checkers and campaigners who find, expose
and counter the harm” (see
fullfact.org). Facebook and
Google fund Full Fact; the charity works for these
FIGURE 5 Detail of
ClaimReview cluster inSchema.
org semantic network
ILIADIS ET AL. 469
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


companies, including Facebook's Third-Party Fact Check-
ing Program and Google's work on COVID-19 fact-
checking.
A recent Full Fact guest blog post at
Schema.org
about ClaimReview discusses the link to fact-checking
(Dudfield & Dodds, 2021). The post is titled“Enriching
ClaimReview for Fact Checkers ” and is written by
Andrew Dudfield (Head of Automated Fact Checking at
Full Fact) and Leigh Dodds (an open data expert). The
post states that ClaimReview is one of the “hidden
jewels” of the schema hierarchy because of the way it
enrolls human fact-checkers. The authors also note that
the Full Fact organization has been“exploring ways to
revise and extend the claim review metadata to provide
more detail that might enable further reuse and labeling
of content, and further insights into the fact checking
process.” These areas include consolidating the recom-
mendations and examples for implementing the feature
Google and Bing have included in their structured data
markup documentation pages. Others describe expanding
ClaimReview to include further term identifiers and link-
ing, enriching the markup to include claims, information
about errors and corrections, and citing evidence.
5.2 | COVID-19 and data commons
Schema.org's vocabulary about COVID-19 is another exam-
ple of a rapidly growing topic, thanks to recent current
world events. In the first 2 months of the pandemic,
Schema.org fast-tracked the approval of terms in the
schema hierarchy to assist with information search and
retrieval related to the pandemic. The first such release
occurred with version 7.0 on March 17, 2020 and included
the fast-track release of terms such as CovidTestingFacility,
SpecialAnnouncement, and eventAttendanceMode.
Material marked up with these terms can appear on Goo-
gle's Fact Check page for Coronavirus, in Google and Bing
knowledge panels, and is available for retrieval by apps and
platforms. These schema features populate some of the rich
search results that users can see, allowing them to look up
information and possibly take action concerning COVID-
19.
Schema.org is also helping a National Science
Foundation-funded study for a semantic integration plat-
form to fight COVID-19 (Zverina,
2020). A detail of the
cluster to which CovidTestingFacility belongs in our
semantic network is represented in Figure6.
Another initiative tied to Schema.org relevant to
accessing structured COVID-19 data is Data Commons,
“an open knowledge database of statistical data started in
collaboration with the U.S. Census, Bureau of Labor Sta-
tistics, World Bank, and many others” (Raghavan,
2020).
This project assists with finding statistics and presenting
them in the knowledge panels when searchers look for
something like“Covid-19 cases in Philadelphia.” Its web-
site is“an open knowledge repository that combines data
from public datasets using mapped common entities. It
includes tools to easily explore and analyze data across
different datasets without data cleaning or joining. ”
Schema.org is one way these data can map to these famil-
iar entities in emissions, health, water, energy, education,
employment, income, and other areas. Specifically, the
website states that “
DataCommons.org builds upon on
the vocabularies defined by Schema.org.” Google offi-
cially announced that it was making Data Commons
available directly in Google Search and knowledge panels
as a new layer of their Knowledge Graph as of 2020.
Since Google announced Dataset Search in 2020, it has
indexed almost 25 million datasets; it is “a dataset-
discovery tool that provides search capabilities over
potentially all datasets published on the Web” and draws
heavily on
Schema.org (Noy, Burgess et al.,2019).
FIGURE 6 Detail of
CovidTestingFacility cluster inSchema.
org semantic network
470 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


6 | DISCUSSION: A GLOBAL
ONTOLOGY FOR WHOM?
As seen in our semantic network,Schema.org contains
several clusters that address emerging topics of key inter-
national importance, including fact-checks and COVID-
19. Yet, other terms and clusters concern commerce-
related topics, such as shopping, vacationing, and cul-
tural work. However, the domain coverage is not limited
to these terms and is very broad, which suggests that
Schema.org is indeed a global ontology, or at least aspires
to be. Which leads us to ask the following question: a
global ontology for whom?
On the one hand,
Schema.org might not be as
“global” in its data interoperability as its creators envi-
sioned. For example, ClaimReview might exacerbate
problems related to misinformation or provide a false
sense of credibility. Things can be labeled “credible”
without regard to the validity of the claim; thus, it would
be possible for bad actors to fact-check a claim simply by
using the metadata vocabulary. Another thing to consider
is that many medical terms seem applicable to privatized
US healthcare systems, indicating a type of platform
nationalism (Jin,
2015). On the other hand,Schema.org
does seem to be approximating something like a global
ontology. In answer to our research questions, we find
that the terms included since the beginning of the
Schema.org ontology span a wide variety of domains and
that Schema.org is not a domain-specific ontology.
Instead, it aims to crosswalk several domains specific to
human actions and published structured data. The top-
level domains are reserved for abstract entities under
which more specific domain information can be located.
The ontology terms, along with the information in the
release history and on
Schema.org's website, tell us that
Schema.org does aspire to become a global ontology (if it
is not already). For example, smaller domain-specific
structured data initiatives have been“absorbed” since the
rise ofSchema.org, as their vocabularies became adopted
and instantiated in Schema.org and thus were made
redundant. Existing projects developing Schema.org
extensions to connect their work will likely be eclipsed
and outdated.
Some benefits come with using structured data like
Schema.org. Certain features are directed at using struc-
tured data for social good, including vocabulary items
relating to providing information about the COVID-19
pandemic. Yet,
Schema.org is a double bind for web
developers who are encouraged to use Schema.org to
increase the findability of their content while simulta-
neously being victims to how search engines present the
information. Google's knowledge panels which show
structured data are a way of keeping traffic on their
search engine. Such practices illustrate the company's
attempt to monopolize information as a semantic middle
layer that discourages users from visiting primary
sources. Knowledge panels that encourage implicit reli-
ance on auto-populated facts (instead of visiting“exter-
nal” sites) are a significant part of the internet for users
today. For example, one study showed that“62 percent of
mobile searches in June 2019 were no-click ” and
that “people ages 13 to 21” are “twice as likely as respon-
dents over 50 to consider their search complete” once
they have seen a“knowledge panel” (Kelley,
2019).
Indeed, Schema.org's structured data model has made
searching for facts and known sources easier and faster
for people using search engines (in the English language).
But the model also has embedded sociocultural biases
towards privatized and for-profit contexts. Search engines
benefit from closed platforms, cookies and user tracking,
data collection from searchers, and targeted advertising
in results. The result of retrieving sources and facts in a
privatized space presents a kind of capitalist realism
(Fisher,
2009) where every search and click has potential
value to platforms, data brokers, and corporations under-
written by advertising mechanics. This reality can be laid
bare if one examines the political economy ofSchema.org
and the influences of its schema governance, particularly
how new terms and features are added (and retired) from
the structured data model. Most terms in
Schema.org are
directed at financially oriented topics relating to logistics,
purchasing, traveling, and so forth. Fewer terms focus on
areas that might benefit socioeconomically underprivi-
leged groups. For example, as far as we can tell currently,
there is no clear information relating to pro bono legal or
immigration services (though there are terms for general
legal services), shelter information for humans (rather
than pets), food drives (instead of fast food which is
included), retirement homes (there is information about
hotels). There are many other areas where the hierarchy
is aimed at those already privileged (tourism, shopping,
etc.). One of the larger subclasses is for different types of
stores (including outlets, liquor, and pawn).
Schema.org's governance, according to our review of
its website and email list, is primarily controlled by Goo-
gle, which might explain the focus on commodities,
services, and purchasing (Andrews, 2020a, 2020b).
According to the project's website, it is also unclear the
extent to which Microsoft, Yahoo, and Yandex still have
personnel affiliated with the project.Schema.org could be
more transparent and forthcoming with its governance
structure and describe who benefits from its structured
data. Given that
Schema.org seemingly appears like a
Google-run property (due to the decreasing participation
of other platform companies), what, then, can web devel-
opers and administrators do so that they are not merely
ILIADIS ET AL. 471
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


giving their labor to a giant platform company that will
essentially “take” information from their pages to repre-
sent in semantic search results? One option might be to
initiate similar or adjacent projects focusing on justice
and equity, such as multiple languages or social services.
As we argued above, developers must use the schema
for their content to appear in search results or risk becom-
ing less visible. Yet, the very nature of the schema means
that content from their sites can be displayed in Google's
rich search results, including knowledge panels. These
practices result in fewer people visiting their sites once
people receive the information they need, which is already
extracted and presented by Google. In this way,
Schema.
org may contribute to Google searches being dominated
by Google information and keeping people on its product,
thus substantiating claims of Google's knowledge monop-
oly. Mager (
2012) describes how capitalist society shapes
search engines through the politics of privatization, and
we view such practices occuring with Google's influence
over the governance of
Schema.org. By engineering soft-
ware that analyses structured metadata that it controls
and uses to provide ontological descriptions of the world,
companies like Google have designed technological infra-
structure that privileges capitalistic conceptualizations of
work, labor, news, life, and technology that favor its plat-
forms, while limiting or ignoring alternatives. Through its
ability to surface information sources in retrieval,
Schema.
org acts as a regulator and gatekeeper controlled by search
engines such as Google. Researchers might also set for
themselves the task of locating examples of limitations.
For example, researchers may surface semantic errors in
information retrieval on products like Google's knowledge
panels and Alexa's answers which rely on the markup that
Schema.org provides or may conduct studies to see what
content areas are omitted. As we have argued elsewhere,
researchers concerned with the power of metadata might
also examine the implications of standards engineering in
private, closed spaces and how that may influence what
internet users can see, access, find, and know (Acker,
2019;A c k e r ,2021;I l i a d i s&A c k e r ,2021).
Lastly, Schema.org connects to projects like Wikipedia
given its ability to present information alongside Wikipe-
dia infoboxes in search results like knowledge panels and
virtual assistant responses (Minhaj & Urs,2021). Google
has specified its preference forSchema.org markup and
has recommended a preference for JSON-LD over other
serializations (such as Microdata and RDFa). The emer-
gence of
Schema.org as the de facto metadata vocabulary
on the web and JSON-LD as the preferred serialization
offer opportunities for researchers to study these new
advancements in the industry. For example, how and why
were these models and serializations chosen, how have
practitioners implemented them across the web, and what
opportunities are there for studying their impact in cur-
rent search and knowledge discovery paradigms?
7 | CONCLUSION
Semantic infrastructures such asSchema.org assert what is
possible, standard, and appropriate in web search while
consolidating the datafication of information in ways that
benefit companies and corporations. The
Schema.org part-
nership represents a critical juncture where tech companies
have evolved to govern how representations of labor, infor-
mation, cultural commodities, and media products as pro-
grammable knowledge are understood and accessed on the
web through search. In doingso, platform companies have
created a hierarchy of what they think people want to
know while underscoring these processes with their mar-
keting and cultural logic. Google's close relationship to
Schema.org and its use of structured data in search results
also has implications for growing Google's monopoly in the
information ecosystem. Further information studies/science
research into structured data will make the organizational
role of platform companies more transparent, specifically in
knowledge management and new media. We encourage
scholars to take up a renewed interest in critical search
engine studies (Haider & Sundin,
2019;R i e d e r ,2022)t os e e
how new gatekeepers and sociocultural biases are created
in the semantic “knowledge” that is constructed and
imparted to users by large platform companies.
ORCID
Andrew Iliadis https://orcid.org/0000-0002-8345-6251
Amelia Acker https://orcid.org/0000-0001-5332-0487
ENDNOTES
1 In this article, we use the terms “metadata vocabulary” and
“structured data” somewhat interchangeably for the sake of read-
ability, with the key distinction that we view all metadata vocabu-
laries as a form of structured data but not all structured data as a
form of metadata.
2 There is not enough room in this article to explain the compli-
cated history of the semantic web project; interested readers may
see Allemang et al.,
2020; Berners-Lee et al.,2001; Calaresu et al.,
2015; Guns, 2013; Hitzler, 2021; McCarthy, 2017; Szeredi
et al.,2014.
3 https://schema.org/docs/releases.html.
4 https://design215.com/toolbox/wordlist.php.
5 https://schema.org/docs/developers.html.
REFERENCES
Acker, A. (2019). A death in the timeline: Memory and metadata in
social platforms. Journal of Critical Library and Information
Studies, 2(2), 1–27. https://doi.org/10.24242/jclis.v2i2.66
472 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


Acker, A. (2021).“Metadata” in N. Thylstrup. In D. Agostinho, C.
D'Ignazio, A. Ring, & K. Veel (Eds.), Uncertain Archives
(pp. 239–244). MIT Press.
Acker, A., & Donovan, J. (2019). Data craft: A theory/methods
package for critical internet studies.Information, Communica-
tion & Society , 22(11), 1590 –1609. https://doi.org/10.1080/
1369118X.2019.1645194
Acker, A., & Kriesberg, A. (2020). Social media data archives in an
API-driven world. Archival Science, 20(2), 105–123. https://doi.
org/10.1007/s10502-019-09325-9
Adair, B. (2020, December).The future of fact-checking is all about
structured data . NiemanLab. Retrieved from https://www.
niemanlab.org/2020/12/the-future-of-fact-checking-is-all-about-
structured-data/
Akrich, M. (1992). The de-scription of technical objects. In W. Bij-
ker & J. Law (Eds.),Shaping technology-building society: Studies
in sociotechnical change(pp. 205–224). MIT Press.
Allemang, D., Hendler, J., & Gandon, F. (2020).Semantic web for
the working ontologist: Effective modeling for linked data, RDFS,
and OWL. ACM Books.https://doi.org/10.1145/3382097
Andrews, M. (2020a, August 9).Time to end Google's domination of
schema.org. Story Needle Retrieved from https://storyneedle.
com/time-to-end-googles-domination-of-schema-org/
Andrews, M. (2020b, August 23). Who benefits from schema.org?
Story Needle Retrieved from https://storyneedle.com/who-
benefits-from-schema-org/
Antoniou, G., Groth, P., van Harmelen, F., & Hoekstra, R. (2012).A
semantic web primer. MIT Press.
Bastian, M., Heymann, S., & Jacomy, M. (2009). Gephi: An open
source software for exploring and manipulating networks.Pro-
ceedings of the International AAAI Conference on Web and Social
Media, 3(1), 361–362.
https://doi.org/10.1609/icwsm.v3i1.13937
Beghtol, C. (2005). Ethical decision-making for knowledge repre-
sentation and organization systems for global use.Journal of
the American Society for Information Science and Technology,
56(9), 903–912. https://doi.org/10.1002/asi.20184
Benkler, Y., Faris, R., & Roberts, H. (2018).Network propaganda:
Manipulation, disinformation, and radicalization in American
politics. Oxford University Press.
Berners-Lee, T., Hendler, J., & Lassila, O. (2001, 17 May). The
semantic web. Scientific American. 284,3 4–43. Retrieved from
https://www.scientificamerican.com/article/the-semantic-web/
Berry, D. M., Borra, E., Helmond, A., Plantin, J.-C., Walker
Rettberg, J., & Walker, J. (2015). The data sprint approach:
Exploring the field of digital humanities through Amazon's
application programming interface. Digital Humanities Quar-
terly, 9(4). Retrieved fromhttp://eprints.lse.ac.uk/65438/
Blondel, V. D., Guillaume, J. L., Lambiotte, R., & Lefebvre, E.
(2008). Fast unfolding of communities in large networks.Jour-
nal of Statistical Mechanics: Theory and Experiment , 2008.
https://doi.org/10.1088/1742-5468/2008/10/P10008
B o w k e r ,G .C . ,B a k e r ,K . ,M i l l e r a n d ,F . ,&R i b e s ,D .( 2 0 1 0 ) .T o w a r d
information infrastructure studies: Ways of knowing in a networked
environment. In J. Hunsinger, L. Klastrup, & M. Allen (Eds.),Inter-
national handbook of internet research(pp. 97–117). Springer.
Bowker, G. C., & Star, S. L. (1999).Sorting things out: Classification
and its consequences. MIT Press.
Bucher, T. (2012). A technicity of attention: How software“makes
sense”. Culture Machine, 13,1 –23. Retrieved from
http://svr91.
edns1.com//C24culturem/index.php/cm/article/view/506/521
Bucher, T. (2013). Objects of intense feeling: The case of the twitter
API. Computational Culture (a Journal of Software Studies), 3,
1–17. Retrieved from http://computationalculture.net/article/
objects-of-intense-feeling-the-case-of-the-twitter-api
Calaresu, M., & Shiri, A. (2015). Understanding semantic web: A
conceptual model. Library Review, 64(1/2), 82–100. https://doi.
org/10.1108/LR-09-2014-0097
Campbell, D. G. (2009). The birth of the new web: A Foucauldian
reading of the Semantic web. Cataloging and Classification
Quarterly, 43(3–4), 9–20. https://doi.org/10.1300/J104v43n03_01
Craig, D., & Cunningham, S. (2019).Social media entertainment: The
new intersection. Of Hollywood and Silicon Valley.N Y UP r e s s .
DeNardis, L. (2009). Protocol politics: The globalization of internet
governance. MIT Press.
DeNardis, L. (2014). The global war for internet governance. MIT
Press.
Douglas, J., Bak, G., McLellan, E., van Hooland, S., & Frogner, R.
(2018). Decolonizing archival description: Can linked data
help? Proceedings of the Association for Information Science and
Technology, 55(1), 669 –672. Portico.
https://doi.org/10.1002/
pra2.2018.14505501077
Dudfield, A., & Dodds, L. (2021). Enriching ClaimReview for fact
checkers. Schema.org Blog. Retrieved fromhttp://blog.schema.
org/2021/12/enriching-claim-reviews-sharing.html
Edwards, P. N., Bowker, G. C., Jackson, S. J., & Williams, R. (2009).
Introduction: An agenda for infrastructure studies.Journal of
the Association for Information Systems, 10(5), 364–374. https://
doi.org/10.17705/1jais.00200
Edwards, P. N., Jackson, S. J., Chalmers, M. K., Bowker, G. C.,
Borgman, C. L., Ribes, D., Burton, M., & Calvert, S. (2013).
Knowledge infrastructures: Intellectual frameworks and research
challenges, (May), pp. 25–28. Retrieved from
http://hdl.handle.
net/2027.42/97552
Edwards, P. N., Mayernik, M. S., Batcheller, A. L., Bowker, G. C., &
Borgman, C. L. (2011). Science friction: Data, metadata, and
collaboration. Social Studies of Science, 41(5), 667–690.
https://
doi.org/10.1177/0306312711413314
Fisher, M. (2009).Capitalist Realism: Is There No Alternative?Zero
Books.
Ford, H., & Graham, M. (2016a). Provenance, power and place:
Linked data and opaque digital geographies.Environment and
Planning D: Society and Space, 34(6), 957–970. https://doi.org/
10.1177/0263775816668857
Ford, H., & Graham, M. (2016b). Semantic cities: Coded geopolitics
and the rise of the semantic web. In R. Kitchin & S.-Y. Perng
(Eds.), Code and the City(pp. 200–214). Routledge.
Gillespie, T. (2018). Custodians of the internet: Platforms, content
moderation, and the hidden decisions that shape social media.
Yale University Press.
Greenberg, J. (2005). Understanding metadata and metadata
schemes. Cataloging and Classification Quarterly, 40(3–4), 17–36.
https://doi.org/10.1300/J104v40n03_02
Guha, R., Brickley, D., & Macbeth, S. (2016). Schema.org: Evolution
of structured data on the web.Communications of the ACM,
59(2), 44–51. https://doi.org/10.1145/2844544
Guns, R. (2013). Tracing the origins of the semantic web.Journal of
the American Society for Information Science and Technology,
64(10), 2173–2181. https://doi.org/10.1002/asi.22907
Haider, J., & Sundin, O. (2019).Invisible search and online search
engines: The ubiquity of search in everyday life. Routledge.
ILIADIS ET AL. 473
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


Halford, S., Pope, C., & Weal, M. (2013). Digital futures? Sociologi-
cal challenges and. Opportunities in the emergent semantic
web. Sociology, 47(1), 173–189.
https://doi.org/10.1177/00380
38512453798
Hallo, M., Luj/C19an-Mora, S., Maté, A., & Trujillo, J. (2016). Current
state of linked data. in digital libraries.Journal of Information
Science, 42(2), 117–127. https://doi.org/10.1177/016555151559
4729
Helmond, A. (2015). The platformization of the web: Making web
data platform ready. Social Media + Society, 1(2). https://doi.
org/10.1177/2056305115603080
Hitzler, P. (2021). A review of the semantic web field.Communica-
tions of the ACM, 64(2), 76–83. https://doi.org/10.1145/3397512
Hui, Y. (2016).On the existence of digital objects. University of Min-
nesota Press.
Iliadis, A. (2018). Algorithms, ontology, and social progress.Global
Media and Communication, 14(2), 219–230. https://doi.org/10.
1177/1742766518776688
Iliadis, A. (2019). The tower of babel problem: Making data make
sense with Basic Formal Ontology.Online Information Review,
43(6), 1021–1045. https://doi.org/10.1108/OIR-07-2018-0210
Iliadis, A., & Acker, A. (2022). The seer and the seen: Surveying
Palantir's surveillance platform.The Information Society, 38(5),
334–363. https://doi.org/10.1080/01972243.2022.2100851
Iliadis, A., Liao, T., Pedersen, I., & Han, J. (2021). Learning about
metadata and machines: Teaching students using a novel struc-
tured database activity.Journal of Communication Pedagogy, 4,
152–165. https://doi.org/10.31446/JCP.2021.1.14
Iliadis, A., & Pedersen, I. (2018). The fabric of digital life: Uncover-
ing sociotechnical tradeoffs in embodied computing through
metadata. Journal of Information, Communication and Ethics in
Society, 16(3), 1–18.
https://doi.org/10.1108/JICES-03-2018-0022
Irani, L. (2013). The cultural work of microwork. New Media &
Society, 17(5), 720 –739. https://doi.org/10.1177/146144481
3511926
Jacomy, M., Venturini, T., Heymann, S., & Bastian, M. (2014).
ForceAtlas2, a continuous graph layout algorithm for handy
network visualization designed for the Gephi software. PLoS
One, 9(6), 1–12.
https://doi.org/10.1371/journal.pone.0098679
Jin, D. Y. (2015).Digital platforms, imperialism and political culture.
Routledge.
Kallinikos, J. (2010). Governing through technology: Information
artefacts and social practice. Palgrave.
Kallinikos, J., Aaltonen, A., & Marton, A. (2010). A theory of digital
objects. First Monday, 15(6). https://doi.org/10.5210/fm.v15i6.
3033
Kallinikos, J., Aaltonen, A., & Marton, A. (2013). The ambivalent
ontology of digital artifacts. MIS Quarterly, 37(2), 357–370.
Retrieved fromhttp://www.jstor.org/stable/43825913
Karasti, H., Millerand, F., Hine, C. M., & Bowker, G. (2016). Knowl-
edge infrastructures: Part IV. Science and Technology Studies,
29(4), 1–9. https://doi.org/10.23987/sts.60220
Kelley, L. (2019).The Google feature magnifying disinformation. The
Atlantic. September 23. Retrieved fromhttps://www.theatlantic.
com/technology/archive/2019/09/googles-knowledge-panels-are-
magnifying-disinformation/598474/
Kollar, T., Berry, D., Stuart, L. M., Owczarzak, K., Chung, T.,
Mathias, L., Kayser, M., Snow, B., & Matsoukas, S. (2018). The
Alexa meaning representation language.Proceedings of the 2018
Conference of the North American Chapter of the Association for
Computational Linguistics: Human Language Technologies, 3,
177–184. https://doi.org/10.18653/v1/N18-3022
Liao, T., & Iliadis, A. (2021). A future so close: Mapping 10 years of
promises and futures across the augmented reality development
cycle. New Media & Society, 23(2), 258–283.
https://doi.org/10.
1177/1461444820924623
Lim, S. (2019, April 18).A better ClaimReview to grow a global fact-
check database. Duke Reporters' Lab. Retrieved fromhttps://
reporterslab.org/a-better-claimreview-to-grow-a-global-fact-che
ck-database/
Machado, L. M. O., Souza, R. R., & da Graça Simões, M. (2018).
Semantic web or web of data? A diachronic study (1999 to 2017)
of the publications of Tim Berners-Lee.Journal of the Associa-
tion for Information Science and Technology, 70(7), 701–714.
https://doi.org/10.1002/asi.24111
Mager, A. (2012). Algorithmic ideology: How capitalist society
shapes search engines.Information, Communication & Society,
15(5), 769–787. https://doi.org/10.1080/1369118X.2012.676056
Mantzarlis, A. (2019, Decemeber 19).How we highlight fact checks
in search and Google news. Google Blog. Retrieved fromhttps://
blog.google/outreach-initiatives/google-news-initiative/how-we-
highlight-fact-checks-search-and-google-news/
Maron, D., & Feinberg, M. (2018). What does it mean to adopt a
metadata standard? A case study of Omeka and the Dublin
Core. Journal of Documentation, 74(4), 674–691.
Marwick, A., & Lewis, R. (2017).Media manipulation and disinfor-
mation online . Data and Society. Retrieved from https://
datasociety.net/library/media-manipulation-and-disinfo-online
Mayernik, M. S., & Acker, A. (2018). Tracing the traces: The critical
role of metadata within networked communications.Journal of
the Association for Information Science and Technology, 69(1),
177–180. https://doi.org/10.1002/asi.23927
McCarthy, M. T. (2017). The semantic web and its entanglements.
Science, Technology And Society, 22(1), 21–37. https://doi.org/
10.1177/0971721816682796
Meusel, R., Bizer, C., & Paulheim, H. (2015, July). A web-scale
study of the adoption and evolution of the schema. Org vocabu-
lary over time.Proceedings of the Fifth International Conference
on Web Intelligence, Mining and Semantics,1 . https://doi.org/
10.1145/2797115.2797124
Minhaj, M., & Urs, S. (2021, November 23). Wikipedia Infoboxes:
The big data source for knowledge bases behind Alexa and Siri
virtual assistants. Information Matters, 1(11). Retrieved from
https://r7q.22f.myftpupload.com/2021/11/wikipedia-infoboxes-
the-big-data-source-for-knowledge-bases-behind-alexa-and-siri-
virtual-assistants/
Napoli, P., & Caplan, R. (2017). Why media companies insist they're
not media companies, why they're wrong, and why it matters.
First Monday, 22(5).
https://doi.org/10.5210/fm.v22i5.7051
Noy, N., Burgess, M., & Brickley, D. (2019). Google dataset search:
Building a search engine for datasets in an open web ecosys-
tem. In L. Liu & R. White (Eds.),Proceedings of the 2019 world
wide web conference (WWW '19), May 13 –17, 2019, San
Francisco, CA. ACM.https://doi.org/10.1145/3308558.3313685
Noy, N., Gao, Y., Jain, A., Narayanan, A., Patterson, A., & Taylor, J.
(2019). Industry-scale knowledge graphs: Lessons and chal-
lenges. Communications of the ACM, 62(8), 36–43. https://doi.
org/10.1145/3331166
474 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


Patel-Schneider, P. F. (2014). Analyzing Schema.org. In P. Mika,
et al. (Eds.), The semantic web— ISWC 2014. Lecture Notes in
Computer Science(Vol. 8796). Springer.https://doi.org/10.1007/
978-3-319-11964-9_17
Paulheim, H. (2015, May). What the adoption of schema. Org tells
about linked open data. InUsewod-profiles@ eswc (pp. 85–90).
Retrieved from http://ceur-ws.org/Vol-1362/PROFILES2015_
paper6.pdf
Plantin, J. C., Lagoze, C., Edwards, P. N., & Sandvig, C. (2016).
Infrastructure studies meet platform studies in the age of Goo-
gle and Facebook. New Media & Society , 20(1), 293 –310.
https://doi.org/10.1177/1461444816661553
Poirier, L. (2017). A turn for the scruffy: An ethnographic study of
semantic web architecture. InProceedings of the 2017 ACM on
Web Science Conference(pp. 359–367). ACM.https://doi.org/10.
1145/3091478.3091505
Poirier, L. (2019). Classification as catachresis: Double binds of
representing difference with semiotic infrastructure.Canadian
Journal of Communication, 44(3), 361–371. https://doi.org/10.
22230/cjc.2019v44n3a3455
Pomerantz, J. (2015).Metadata. MIT Press.
Posada, J. (2022). Embedded reproduction in platform data work.
Information, Communication & Society, 25(6), 816–834. https://
doi.org/10.1080/1369118X.2022.2049849
Raghavan, P. (2020, October 15).How AI is powering a more helpful
Google. Google Blog. Retrieved from https://blog.google/
products/search/search-on/
Rieder, B. (2022). Towards a political economy of technical systems:
The case of Google.Big Data & Society, 9(2), 1–5. https://doi.
org/10.1177/20539517221135162
Roberts, S. T. (2019).Behind the screen: Content moderation in the
shadows of social media. Yale University Press.
Russell, A. L. (2011). Constructing legitimacy: The W3C's patent
policy. In L. DeNardis (Ed.),Opening standards: The global poli-
tics of interoperability(pp. 159–176). MIT Press.
Russell, A. L. (2014).Open standards and the digital age: History,
ideology, and networks. Cambridge University Press.
Şims¸ek, U., Kärle, E., Holzknecht, O., & Fensel, D. (2018). Domain
specific semantic validation of Schema.org annotations.
In A. Petrenko & A. Voronkov (Eds.),Perspectives of system infor-
matics. PSI 2017. Lecture Notes in Computer Science(Vol. 10742).
Springer. https://doi.org/10.1007/978-3-319-74313-4_31
Srinivasan, R. (2013). Re-thinking the cultural codes of new media:
The question concerning ontology.New Media & Society, 15(2),
203–223. https://doi.org/10.1177/1461444812450686
Star, S. L. (1999). The ethnography of infrastructure. American
Behavioral Scientist , 43(3), 377 –391. https://doi.org/10.1177/
00027649921955326
Swanson, E. B. (2020). How infor mation systems came to rule
the world: Reflections. On the information systems field.The
Information Society , 36(2). https://doi.org/10.1080/01972243.
2019.1709931
Szeredi, P., Luk/C19acsy, G., & Benk}o, T. (2014). The semantic web
explained: The Technology and mathematics behind web 3.0.
Cambridge University Press.
Waller, V. (2016). Making knowledge machine-processable: Some
implications of general semantic search.Behaviour & Informa-
tion Technology, 35(10), 784–795. https://doi.org/10.1080/01449
29X.2016.1183710
Wang, S. (2019). The intellectual landscape of the domain of
culture and ethics in knowledge organization: An analysis of
influential authors and works. Cataloging and Classification
Quarterly, 57(4), 227 –243.
https://doi.org/10.1080/01639374.
2019.1614710
Zverina, J. (2020, June 1).Fighting COVID-19 with knowledge graphs.
UC San Diego News Center Retrieved from https://ucsdnews.
ucsd.edu/pressrelease/fighting-covid-19-with-knowledge-graphs
How to cite this article:Iliadis, A., Acker, A.,
Stevens, W., & Kavakli, S. B. (2025). One schema to
rule them all: How Schema.org models the world
of search.Journal of the Association for Information
Science and Technology, 76(2), 460–523. https://doi.
org/10.1002/asi.24744
ILIADIS ET AL. 475
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


APPENDIX
TABLE A1 Full Schema.org release history as of May 11, 2022
Release Overview Description
14.0 (March 17, 2022) Version 14.0 — this release includes improvements
proposed via the pending section, including
additions around audience restrictions for
eCommerce.
Vocabulary
Changes in Core section:
 Issue #3026: Fixed incorrect longitude value for
empire state building in example eg-0005.
 Issue #3059: Added gameEdition for VideoGame
by analogy with bookEdition.
Changes in pending section:
 Issue #3052: Added a new subtype of organization
to distinguish organizations that are search and
rescue organizations: SearchRescueOrganization.
 Issue #3053: Updated keywords property to clarify
that comma-separated usage only applies to
textual keywords. Also updated to expect this
property in several other high-level types.
 Issue #3057: Added DigitalPlatformEnumeration
as a convenience enumeration for use with
actionPlatform.
 Issue #3056: Added funding as a convenient
inverse of fundedItem, with the associated types
for both properties alligned. Added more examples
around Grant.
 Issue #3058: Added a new subtype of
ConsumeAction called PlayGameAction.
 Issue #2989: Added enumeration
AdultOrientedEnumeration for use as value for
new property hasAdultConsideration. Added
hasAdultConsideration for use on offer and
product. Also added isFamilyFriendly for use on
offer and product in addition to CreativeWork.
 Issue #3001: Added new property
returnPolicyCountry for use on
MerchantReturnPolicy.
 Issue #2915: Added new property iso6523Code for
use on organization.
 Issue #3028: Added OnlineBusiness as a subtype
of organization and OnlineStore as a subtype of
OnlineBusiness.
 Issue #3025: Added CategoryCode as an expected
value for category.
 Issue #2927: Added provider to action type.
Site improvements
PR #2990: Update supporting python version and
libraries— RDFLib 6.1, python 3.10.
13.0 (July 7, 2021) Version 13.0 — see planning pages. This release
includes improvements proposed via the pending
section, in particular a number of terms proposed
by the bioschemas project, alongside other
additions around e-commerce returns policy
markup, job postings, and MediaReview markup.
Vocabulary
Changes in Core section:
Changes in pending section:
 Issue #2892: Clarifications around blog,
BlogPosting and LiveBlogPosting, including better
cross-referencing, and acknowledgment of related
terminology (“weblog,” and “blog” in the sense of
posting). For clarity, the example showing
476 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
LiveBlogPosting is no longer tagged to show up as
an example of blog too.
 Issue #2862: Additions proposed by the the
bioschemas community. Adds several types for
basic life science concepts. A type taxon, with
properties: childTaxon parentTaxon taxonRank
hasDefinedTerm. A general type BioChemEntity:
associatedDisease, bioChemInteraction,
bioChemSimilarity, hasBioChemEntityPart,
hasRepresentation, isEncodedByBioChemEntity,
encodesBioChemEntity, isPartOfBioChemEntity,
taxonomicRange, biologicalRole,
hasMolecularFunction,
isInvolvedInBiologicalProcess,
isLocatedInSubcellularLocation. The following
types are subtypes of this convenience type. A type
MolecularEntity, with properties inChI, inChIKey,
iupacName, molecularFormula, molecularWeight,
monoisotopicMolecularWeight, smiles. A type
ChemicalSubstance with properties
chemicalComposition, chemicalRole,
potentialUse. A type Gene with additional
property hasBioPolymerSequence. A type protein
with additional property hasBioPolymerSequence.
 Issue #2880: Additions to merchant return
policies. Implemented in #2381. Adds
ReturnLabelSourceEnumeration,
ReturnMethodEnumeration and several
enumerated values for these. Also adds several
new enumerated values to existing
ReturnFeesEnumeration. Adds properties
returnMethod, itemDefectReturnFees,
customerRemorseReturnFees,
returnShippingFeesAmount,
itemDefectReturnShippingFeesAmount,
customerRemorseReturnShippingFeesAmount,
returnLabelSource, itemDefectReturnLabelSource,
customerRemorseReturnLabelSource,
restockingFee, returnPolicyCountry. A dds new
type MerchantReturnPolicySeasonalOverride and
new property returnPolicySeasonalOverride. Adds
existing additionalProperty and itemCondition to
MerchantReturnPolicy and
hasMerchantReturnPolicy to offer
 Issue #2907: Added directApply property to
indicate on a JobPosting whether direct
applications are supported.
 Issue #2844: Additional detail for MediaReview
description. To cross-reference (via link or
embedded description) between ClaimReview and
MediaReview, two new properties:
associatedClaimReview, associatedMediaReview.
These are defined as specializations of a common
superproperty: associatedReview. To describe
exact, specific,“frozen” snapshots of a potentially
changing MediaObject, three new types:
(Continues)
ILIADIS ET AL. 477
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
ImageObjectSnapshot, AudioObjectSnapshot,
VideoObjectSnapshot. A new property, sha256,
can be used to identify the specific file by a hash of
its contents. To group together multiple elements
for reference by itemReviewed, a new type:
MediaReviewItem. Its property,
mediaItemAppearance, can use the“snapshot”
types to bundle several different appearances of
the same basic media item. For the case of an
image with embedded text, a new property:
embeddedTextCaption (a subproperty of caption).
To characterize the original context of a
potentially decontextualized media item, a
property originalMediaContextDescription,
alongside originalMediaLink,
embeddedTextCaption, interpretedAsClaim,
claimInterpreter, and archivedAt to provide
additional supporting information useful for fact
checking and misinformation-related workflows.
 Issue #2912: Add a statement type, parallel to
claim, for simple statements such as“fun or
interesting” facts, to distinguish them from more
formal (e.g., fact-checkable) claims.
 Issue #2882: Added organization as an expected
value for buyer.
 Issue #2895: Add actor to PodcastSeries.
 Issue #991: Adding countryOfLastProcessing and
countryOfAssembly, to improve compatability
with GS1.
 Issue #2911: Added startOffset, which was
accidentally omitted from the SeekToAction
definitions previously.
 Issue #2825 (also #2823): Added location,
startTime and endTime to InteractionCounter.
 Issue #2832: Added positiveNotes and
negativeNotes properties for review, providing a
simple dedicated syntax to support pro/con lists
summarizing reviews.
Site improvements
 Issue #2790: Schema markup validator:
validator.
schema.org is available for review. See
documentation for details.
 Issue #2891: Published draftSchema.org feeds
specification for implementor discussion and
feedback.
 Issue #2842: Fixed many examples after review
and update of ruby CI tests.
12.0 (March 8, 2021) Version 12.0 — see planning pages. This release
consists primarily of additions to the pending
section of
schema.org, alongside some bugfixes and
improvements to core terms.
Vocabulary
Changes in Core section:
 Issue #1417: Fixed typo in isLiveBroadcast.
 Issue #2786: Updated JSON-LD example in
mainEntityOfPage.
 Issue #2803: Add ineligibleRegion as expected on
the MediaObject type.
 Issue #2821: Add duration as expected on the
episode type.
478 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
 Issue #2840: Clarified definition of
schemaVersion.
 Issue #2803: (implemented in PR #2804): Added
property ineligibleRegion to MediaObject type.
 See also pending for cases where new terms
required minor adjustments to core vocabulary.
Changes in pending section:
 Issue #2844: Updates to MediaReview reflecting
community work towards clarifying a list of codes
for MediaManipulationRatingEnumeration.
 Issue #2810: Fixed bug: marginOfError should
have values of type QuantitativeValue.
 Issue #2811: Additions to support structured sizes
and measurements. Implemented in #2819. Adds
SizeSystemEnumeration,
WearableSizeSystemEnumeration,
SizeGroupEnumeration,
WearableSizeGroupEnumeration,
MeasurementTypeEnumeration,
WearableMeasurementTypeEnumeration,
BodyMeasurementTypeEnumeration,
SizeSpecification and several initial enumerated
values for these. Also add sizeGroup, sizeSystem,
hasMeasurement, suggestedMeasurement,
suggestedAge. Updated sizeproperty to include the
new SizeSpecification type as a potential value.
Additional expected values for valueReference:
MeasurementTypeEnumeration, text and
DefinedTerm.
 Issue #2651: Add BackOrder as an enumeration
member of ItemAvailability.
 Issue #2799: Additional enumerated aspects for
HealthAspectEnumeration, and clarified
HowOrWhereHealthAspect for the case of
vaccines. Additions: GettingAccessHealthAspect,
AllergiesHealthAspect, SafetyHealthAspect,
EffectivenessHealthAspect,
PregnancyHealthAspect, IngredientsHealthAspect,
HowItWorksHealthAspect.
 Issue #2681: Added vocabulary around JobPosting
and occupation so that we can explicitly indicate
when degree-level qualification is not required.
Added a boolean experienceInPlaceOfEducation
property for JobPosting. Also added a new
OccupationalExperienceRequirements type as an
additional possible value for the existing
experienceRequirements property. Added a
number-valued property monthsOfExperience for
use on OccupationalExperienceRequirements.
Site improvements
 PR #2706: Replaced TravisCI with GitHub actions
for continuous integration testing of changes to
the schemaorg repository.
 Issue #2822: Updated punctuation used in
breadcrumb path displayed at the top of property
(Continues)
ILIADIS ET AL. 479
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
pages to reflect that a property is not a subtype of
the property type.
 PR #2789: Identified and corrected 80+ broken
links within site. Created a localized link checking
script (brokenlinkcheck.Py) for future testing
possibilities.
 PR #2800: Reorganized directory structure of
repository and development environment to
separate out software and test elements (into a
software subdirectory) from vocabulary definition
elements.
 PR #2814: Completed process of moving
Schema.
org to https. This step included the move to https
of vocabulary term definitions and consequent
change to https of the canonical URI displayed
under the term pages [more… ] tag. The web site
will continue to respond to both http and https
URLs. Download files will continue to support
both protocols.
 PR #2815: Fixed links in release page that return a
404 response.
11.01 (December 8,
2020)
Version 11.01— see planning pages. This interim
release consists primarily of bug fixes and site
improvements.
Site improvements
 Fix invalid link to home page on attic home page.
 Reinstated home pages for auto, bib, health-lifesci
and meta sections.
 Fix invalid links to section home pages on
schemas page.
 Update wording on pages for terms that are
superseded, pending or retired.
 Reinstated link to section home page for non-core
terms.
11.0 (November 30,
2020)
Version 11.0— see planning pages. This release
consists primarily of additions to the pending
section of
schema.org, alongside some bugfixes and
improvements to core terms.
Vocabulary
Changes in Core section:
 Issue #2733: Fixed typo in description of
ReceiveAction.
 Issue #2746: Fixed invalid JSON-LD in example
# eg-0449 on VideoGame.
 Removed redundant property definitions for
upvoteCount & downvoteCount.
 Issue #2776: Fix invalid term links identified in
examples files.
Changes in pending section:
 Issue #1842 implemented in PR #2744: Added
examples for online and mixed online & offline
events. Attached to event, eventAttendanceMode,
and VirtualLocation descriptions.
 PR #2737: Removed subproperty relationship
between hasCategoryCode and hasPart.
 Issue #2482 implemented in PR #2736: Added
examples for sameAs, titleEIDR, and editEIDR
properties.
480 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
 Issue #2646 implemented in PR #2719: Added
new AmpStory type— “A creative work with a
visual storytelling format intended to be viewed
online, particularly on mobile devices.” This is
intended in particular, for works designed for
AMP story readers. A more general supertype
could be added if there is implementation interest.
 Issue #2712 implemented in PR #2716: Added
new PriceTypeEnumeration enumeration type
with values InvoicePrice, ListPrice, MSRP,
MinimumAdvertisedPrice, SRP, SalePrice. Added
to range of priceType property on the
UnitPriceSpecification and
CompoundPriceSpecification types.
 Issue #2689 implemented in PR #2715 & PR
#2758: Added new
PriceComponentTypeEnumeration enumeration
type with values installment, subscription,
Downpayment, ActivationFee, CleaningFee,
DistanceFee. Added to range of new
priceComponentType property on type
UnitPriceSpecification. Added new billingStart
and billingDuration properties on type
UnitPriceSpecification.
 Issue #2766: Added new HyperToc,
HyperTocEntry types, tocEntry, tocContinuation
and utterances properties to support navigation
and annotation within MediaObject content.
 Issue #2722 implemented in PR #2732: Added
SeekToAction type to be used as a value for the
potentialAction property on a VideoObject type.
 Issue #2740 implemented in PR #2752: Added
SolveMathAction, for sites than can analyze a
mathematical expression, potentially solving or
simplifying it. Also added a related type,
MathSolver.
 Issue 1401 implemented in PR #2745: Adjusted
definition of competencyRequired so that it can be
used to described the skills, knowledge, ability
required in order to understand a learning
resource.
 Issue #2764 implemented in #2765: Added
DefinedTerm to learningResourceType and
educationalUse.
 Issue 2,659: Added copyrightNotice and
creditText, to help improve interoperability
between
schema.org and IPTC metadata.
 Added missing supertype (intangible) to
EnergyConsumptionDetails.
Site improvements
 PR #2706: Improvements to underlying site build
architecture including separation of vocabulary
definition and display logic; move to python 3;
and simplified local build and test processes. Full
type hierarchy page is now more usable and
accessible (collapsible navigation). Copy example
(Continues)
ILIADIS ET AL. 481
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
to clipboard button added to examples on term
definition pages.
 PR #2760: Added structured representation of
JSON-LD examples tab to examples display on
term definition pages.
 PR #2726: Removed previous RDFa term
description from within html of term definition
pages, replace with equivalent JSON-LD script
element.
 Issue #2747 implemented in PR #2748: Fixed
invalid comment syntax in the JSON-LD element
of 47 examples.
10.0 (September 7,
2020)
Version 10.0— see planning pages. This release
consists primarily of additions to the pending
section of
schema.org, alongside some bugfixes and
improvements to core terms.
Vocabulary
Changes in Core section:
 Issue #737: Improve support for controlled
taxonomies (e.g., SKOS) by supporting URLs into
taxonomies for the keywords field: Added URL
and DefinedTerm as expected values.
 Issue #2647: SkiResort should be a subclass of
resort (in addition to the existing
SportsActivityLocation supertype).
 Issue #2664: a parentItem of a comment should be
a comment, not a question.
 Issue #2662: The supertype of question should be
comment, by analogy with answer.
 Issue #881: Changed description to reviewBody in
a review example.
Changes in pending section:
 Issue #2663: Add a property eduQuestionType for
questions that act as practice problems.
 Issue #2678: Indicated that learningResourceType
is expected on LearningResource.
 Issue #2483: Add hasCourse property to
EducationalOccupationalProgram to specify which
courses are components of a program.
 Issue #2690: Add a layoutImage property to
FloorPlan to clearly indicate an image that depicts
the floorplan.
 Issue #2670: Add vocabulary to express the energy
efficiency of products. Adds a
hasEnergyConsumptionDetails property for use on
product to indicate an EnergyConsumptionDetails
item which in turn has a
hasEnergyEfficiencyCategory property whose
values are drawn from enumerations. An
enumeration class EnergyEfficiencyEnumeration
with two initial subtypes, for
EUEnergyEfficiencyEnumeration and
EnergyStarEnergyEfficiencyEnumeration. The
elements in the EU scheme are ordered, allowing
energyEfficiencyScaleMax and
energyEfficiencyScaleMin properties to specify the
482 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
portion of the scale applicable to the relevant
product category.
Site improvements
 Issue #2663: Updated all examples to use
https://
schema.org instead ofhttp://schema.org.
 Style guide: Added a style guide for schema
authoring to the site, giving conventions for term
naming and capitalization.
9.0 (July 21, 2020) Version 9.0 see planning pages. This release consists
primarily of additions to the pending section of
schema.org, alongside minimal edits to core terms
to integrate the new vocabulary into the larger
system.
Vocabulary
Changes in Core section:
 Issue #2604: Improvements around enumerations.
Some code improvements to present subtyped
enumerations more usefully, and addition of a
StatusEnumeration type to group numerous
enumerations from various kinds of status-related
situations.
 Issue #2512: Fixed definition of LockerDelivery
and ParcelService to correctly define them as
enumeration members of DeliveryMethod.
 Issue #2268: Defined expected type of several
properties in ExercisePlan to be QuantitativeValue
instead of the incorrect value of QualitativeValue.
Changes in health-lifesci section:
 Issue #2268: Defined expected type of several
properties in ExercisePlan to be QuantitativeValue
instead of the incorrect value of QualitativeValue.
Changes in pending section:
 Issue #1401: Add a type LearningResource to
indicate CreativeWorks that have a particular and
explicit orientation towards learning, education,
skill acquisition and other educational purposes.
 Issue #2611: Add a quiz type, as a kind of
LearningResource, defined as a“test of
knowledge, skills and abilities.”
 Issue #2587: Add two properties size and pattern
for type product to support common product
variant dimensions.
 Issue #1797: Add a ProductGroup type to allow
modeling of a group of products (variants) that
vary along explicitly defined dimensions. Add
properties variesBy and hasVariant for type
ProductGroup to explicitly define the variant-
identifying properties and the list of variants
belonging to the group. Adds existing property
isVariantOf to type product to indicate the
ProductGroup it is a variant of. Adds property
productGroupID as explicit identifier for type
ProductGroup. Also adds inverse property
inProductGroupWithID for type product to
identify the product group it is a variant of.
 Issue #2605: Clarify the definition of collection to
make clear that it covers a broad range of kind of
“collection.” Add a ProductCollection type to
allow modeling of a collection of products that are
commonly bundled together. Extend the existing
property includesObject for use with the type
ProductCollection to indicate the (type and
(Continues)
ILIADIS ET AL. 483
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
number of) products that are member of the
collection.
 Issue #2620: Added several new examples.
 Issue #2599: Add byMonthWeek to schedule type.
 Issue #1755: Add BoatReservation, BoatTrip (and
arrivalBoatTerminal, departureBoatTerminal
properties), BoatTerminal types.
Site improvements
 Issue #2304: (implemented in PR #2654):
Rationalization of dump files. Machine readable
vocabulary definition files, available from the
developers area, have been rationalized to include
definitions from the core plus all sections of the
vocabulary. Now download file names have been
used to reflect this change. Also introduced two
versions of each file, one containing http URIs the
other https URIs.
8.0 (May 1, 2020) Version 8.0 see planning pages. This release consists
of additions to the pending section of
schema.org.
Vocabulary
Changes in Core section:
 N/A
Changes in pending section:
 Issue #2543: Add a nonprofitStatus property to
indicate non-profit organizations, alongside an
initial enumeration of non-profit organization
types, NonprofitType.
 Issue #2506: Add vocabulary to help online
vendors publish information about their shipping-
related policies, associatted with an offer using the
shippingDetails property. Adds
OfferShippingDetails and supporting properties
(including deliveryTime, doesNotShip,
shippingDestination, shippingLabel, shippingRate,
shippingSettingsLink, transitTimeLabel). Also
added supporting types ShippingDeliveryTime,
DefinedRegion, PostalCodeRangeSpecification,
OfferShippingDetails, ShippingRateSettings.
 Issue #2427: Simplifies education-related markup
for describing what a learning resource teaches or
assesses, and its educationalLevel. Allows these
properties to be used for EducationEvents.
 Issue #2384: Add property to JobPosting for legal
requirements relating to eligibility to work such as
citizenship, visa or other documentation.
 Issue #2469: Add two properties to represent
EIDR identifiers: titleEIDR and editEIDR.
7.04 (April 16, 2020) Version 7.04. See planning pages. This was a minor
release, with improvements relating to the COVID-
19 response effort.
Vocabulary
Changes in Core section:
 Issue #2540: EducationalOrganization has an
additional supertype of CivicStructure, clarifying
that it can be used with announcementLocation.
Changes in pending section:
 Issue #2534: Improved vocabulary for describing
government benefits in the context of a
SpecialAnnouncement. A new
governmentBenefitsInfo property can now
reference a GovernmentService. The existing
484 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
serviceType property can now optionally use
enumerated values from
GovernmentBenefitsType. This enumerates
several kinds of government benefits. While the
list is general purpose, our priority is to support
the COVID-19 response. We anticipate adding
more structure here in future to better capture
per-country systems and new kinds of benefit. As
part of this work we also introduce a jurisdiction
property as a superproperty of
legislationJurisdiction.
 Issue #2536: Fixed a bug in the amended
definition for category.
 Issue #2626: Add a hackathon type.
 Issue #2493: Add startTime/endTime to schedule.
7.03 (April 2, 2020) Version 7.03. See planning pages. This was a minor
release, with improvements relating to the COVID-
19 response effort.
Vocabulary
Changes in pending section:
 Issue #2521: Adds a document and schema
definitions capturing a 1:1 representation of a
CDC CSV format for hospital reporting.
 Issue #2519: Clarifies that webFeed can be
expected on the SpecialAnnouncement type.
 Issue #2518: Updated pending draft of 3DModel to
place it under MediaObject rather than clutter
CreativeWork.
7.02 (March 31, 2020) Version 7.02. See planning pages. This was a minor
release, with improvements relating to the COVID-
19 response effort.
Vocabulary
Changes in pending section:
 Issue #2514: Added an announcementLocation
property, clarifying how a SpecialAnnouncement
can reference both regions and specific places.
7.01 (March 22, 2020) Version 7.01. See planning pages. This was a minor
release, with improvements relating to the COVID-
19 response effort.
Vocabulary
Core changes
 N/A
Changes in pending section:
 Issue #2500: Added a SchoolDistrict type.
 Issue #2497: Added datePosted to
SpecialAnnouncement type.
Site improvements
 Issue #2495: Added an example for the geographic
region of a SpecialAnnouncement.
7.0 (March 17, 2020) Version 7.0. See planning pages. Vocabulary
Core changes
 Issue #2448: Removed several largely un-used
medical health properties whose names were
inappropriately general:Action, background,
cause, cost, function, indication, origin, outcome,
overview, phase, population, purpose, source,
subtype. Note that we do not remove terms
casually, but in the current case the usability
consequences of keeping them in the system
outweighed the benefits of retaining them, even if
flagged as archived/superseded.
 Issue #1842: Introduced a VirtualLocation type, to
support description of events whose location is
online. Added eventAttendanceMode to clarify the
(Continues)
ILIADIS ET AL. 485
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
current attendance mode of an event (online,
offline, or a mix). Also added a new enumeration
value for eventStatus for event:
EventMovedOnline.
Changes in pending section:
 Issue #2490: Added (fast track) a
SpecialAnnouncement type with several
properties and supporting documentation, as a
contribution to the global response to the COVID-
19 coronavirus pandemic. We expect to iterate on
this design after implementator and publisher
feedback.
 Issue #2460: Added properties to
EducationalOccupationalProgram to support cases
where it is not clear the distinction between
classroom-based and work-based programs.
 Issue #2373: Added petsAllowed for use with
ApartmentComplex, and petsAllowed,
amenityFeature and floorSize to FloorPlan.
Created new properties for numberOfBedrooms
and a new tourBookingPage.
 Issue #2450: Addeddraft type MediaReview, and
associated MediaManipulationRatingEnumeration
with two example values AuthenticContent and
MissingContext. Note that this is editorial work in
progress and not a complete design. See also
NiemanLab background article on this work.
 Issue #2454: Added usageInfo, and
acquireLicensePage to CreativeWork.
Site improvements
 Reinstated 301 redirect to https for http requests.
 Issue #2412: Implemented in sdopythonapp
submodule issue #6: Enhancements to CORS
support, providing appropriate responses to HTTP
OPTIONS request.
6.0 (January 21, 2020) Version 6.0. See planning pages. Vocabulary
Core changes
Other changes in Core section:
 Issue #637: Made itemOffered and offers fully
inverseOf each other.
 Issue #2397: Reworded datePosted to avoid tying
this property to overly-specific usecase (i.e., it
originally assumed usage only with JobPosting).
 Issue #2433: Shortened definition of PreOrder
from ItemAvailability enumeration.
 Issue #2375: Added note to descriptions for offer
and AggregateOffer indicating default
businessFunction.
 Issue #2309: (implemented in PR #2380):
Extended rangeIncludes of datePublished to
include DateTime.
 Issue #2420: Added MusicRecording as an
expected value of audio.
 Issue #2421: Added person and organization to
the domain for interactionStatistic.
486 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
 Issue #2139: Added MediaGallery as a super-type
of ImageGallery and VideoGallery, to allow for a
mixed-media collection page type.
 Issue #2382: Added BroadcastService to the
domain for inLanguage.
 Issue #1951: Added SportsEvent to the domain for
sport.
Changes in pending section:
 Issue #2372: Noted that other kinds of thing have
callSign beyond radio broadcasts, in particular
vehicles/boats and non-radio broadcasts. Added
vehicle, person and BroadcastService (the latter
also covers the initial type, RadioBroadcastService)
to callSign accordingly.
 Issue #2384: Adds three properties to JobPosting
for requirements relating to physical abilities,
sensory abilities and security clearance.
 Issue #2396: Improvements to provide more
information about the employer in JobPosting.
Adds properties for applicationContact,
employerOverview, and allows DefinedTerm to be
used with the industry property.
 Issue #2373: Improvements around real estate
description including the addition of a property
accommodationFloorPlan and type FloorPlan for
use when a number of accomodation entries share
a common layout. Added
numberOfFullBathrooms and yearBuilt. Also
noted that leaseLength is expected on offer and
that datePosted can be applied to
RealEstateListing.
 Issue #2389: Changes to the pending schedule
type: Adds the duration property, extends the
range of byDay to allow for iCal-style rule syntax
and adds the scheduleTimezone property.
 Issue #2418: Added financialAidEligible property
for the types of financial aid available for an
EducationalOccupationalProgram.
 Issue #2429: Added a number of properties to
EducationalOccupationalProgram to help
represent information for determining how long a
program typically takes, when terms typically run,
and when applications are accepted. Specifically:
applicationDeadline, applicationStartDate,
educationalProgramMode, numberOfCredits,
maximumEnrollment, termDuration,
termsPerYear, timeOfDay, typicalCreditsPerTerm.
 Issue #2405: Add guide and recommendation as
new types.
 Issue #2394: Added isResizable to 3DModel.
 Issue #2381: Renamed ProductReturnPolicy (and
related) to MerchantReturnPolicy.
 Issue #2108: (implemented in PR #2352):
Introduced new pending type PronounceableText
enabling phonetic markup of text values.
(Continues)
ILIADIS ET AL. 487
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
Changes in bib section:
 Issue #2366: (implemented in PR #2367): Added
example for audiobook indicating a relationship
with a printed counterpart.
Site improvements
 Issue #2025: Corrected xml encoding value in
schemaorg.Owl file to be“UTF-8”
 Issue #1986: (implemented in PR #2378): Added
test to check for duplicate entries in jsonldcontext
files.
 Issue #2277: (implemented in PR #2388): Fixed
error in definition of eventSchedule property.
5.0 (November 1, 2019) Version 5.0. See planning pages. Vocabulary
Changes in pending section:
 Issue #2372: Extended and redescribed callSign
property to cover other common situations where
it is applicable.
 Issue #2358: Introduced a type WebContent to
allow descriptions to abstract away from the
differences between url-addressable content in
form of WebSite, WebPage or WebPageElement.
 Issue #2374: Introduced HealthTopicContent and
an enumeration of“aspects” of the different
topical aspects found in such content, as well as a
property hasHealthAspect associating
WebContent instances with those identified
aspects.
 Issue #2373: Added properties
accommodationCategory,
numberOfBathroomsTotal,
numberOfFullBathrooms, floorLevel, and
leaseLength to accommodation for detailed real-
estate description. leaseLength also added to
RealEstateListing
 Issue #2322: Linked skills description to formal
definitions of competencies.
Site improvements
 PR #2365: Split codebase that underpins the
Schema.org site into a separate repository, to
simplify interaction with vocabulary definition
and documentation files in the schemaorg
repository area.
4.0 (October 15, 2019) Version 4.0. See planning pages. Vocabulary
Changes in pending section:
 Issue #2348: Added draft types for
RealEstateListing, OfferForPurchase and
OfferForLease.
 Issue #2289: (implemented in PR #2290): Added
types EducationalOccupationalProgram,
WorkBasedProgram and associated properties.
 Issue #373: (implemented in PR #2007): Added
types PodcastSeries, PodcastSeason,
PodcastEpisode and associated properties.
 Issue #2110: (implemented in PR #2142): Added
property subtitleLanguage to BroadcastEvent type.
488 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
 Issue #2341: (implemented in PR #2344): Added
property ineligibleRegion to
ActionAccessSpecification type.
 Issue #2242: (implemented in PR #2345): Added
property gender to SportsTeam type.
 Issue #2329: (implemented in PR #2330): Added
property totalJobOpenings to JobPosting type.
 Issue #2296: (implemented in PR #2297): Added
property employmentUnit to JobPosting type.
Changes in bib section:
 PR #2232: Simplified example for audiobook.
Site improvements
 Issue #2331: (implemented in PR #2332): Fixed
mobile usability issues of site— identified by
Google search console.
 PR #2312: Fixes typo for rdfs:Label URI.
3.9 (August 1, 2019) Version 3.9. See planning pages. Vocabulary
Core changes
 Issue #2294: (implemented in PR #2295): Adding
example for JobPosting.
Changes in pending section:
 Issue #2291: Added StatisticalPopulation,
observation and supporting properties to enable
statements (e.g., aggregate statistics) about sets of
entities that have particular properties.
 Issue #2300: Added ratingExplanation property to
rating (expect type text):“A short explanation(e.g.,
one to two sentences) providing background context
and other information that led to the conclusion
expressed in the rating. This is particularly
applicable to ratings associated with‘fact check’
markup using ClaimReview.”
 Issue #2289 (implemented in PR #2290): Added
types for educational programs:
EducationalOccupationalProgram and
WorkBasedProgram plus supporting properties:
hasCredential (for organization and person types),
occupationalCredentialAwarded,
programPrerequisites, timeToComplete,
trainingSalary, and salaryUponCompletion.’
Site improvements
 PR #2292: Fixed typo in Jane Doe's name in
example for person.
 PR #2285: Corrections to examples identified as
errors by Travis CI scripts.
 PR #2199: Fix to grammar in description of
knowsAbout.
3.8 (July 1, 2019) Version 3.8. See planning pages. Vocabulary
Core changes
 Issue #2294: (implemented in PR #2295): Adding
example for JobPosting.
Changes in pending section:
 Issue #2291: Added StatisticalPopulation,
observation and supporting properties to enable
statements (e.g., aggregate statistics) about sets of
entities that have particular properties.
(Continues)
ILIADIS ET AL. 489
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
 Issue #2300: Added ratingExplanation property to
rating (expect type text):A short explanation(e.g.,
one to two sentences) providing background context
and other information that led to the conclusion
expressed in the rating. This is particularly
applicable to ratings associated with‘fact check’
markup using ClaimReview.
 Issue #2289 (implemented in PR #2290): Added
types for educational programs:
EducationalOccupationalProgram and
WorkBasedProgram plus supporting properties:
hasCredential (for organization and person types),
occupationalCredentialAwarded,
programPrerequisites, timeToComplete,
trainingSalary, and salaryUponCompletion.
Site improvements
 PR #2292: Fixed typo in Jane Doe's name in
example for person.
 PR #2285: Corrections to examples identified as
errors by Travis CI scripts.
 PR #2199: Fix to grammar in description of
knowsAbout.
3.7 (June 1, 2019) Version 3.7. See planning pages. Vocabulary
Core changes
 Issue #2192: Added CategoryCode to
rangeIncludes for property occupationalCategory
and DefinedTerm to rangeIncludes for property
jobTitle.
 Issue #2251: Extended rangeIncludes for property
estimatedSalary to include MonetaryAmount and
number.
 Issue #1848: Updated definitions of addressRegion
and addressLocality that a street address is in a
locality and a locality is in a region.
 Issue #2167: Fixed invalid JSON-LD in examples
showing educationRequirements for person and
occupation.
 Issue #1991: Fixed incorrect links (to
webschemas.
org) in docs/releases.Html.
 Issue #1993: Updated definition and provided
examples for isBasedOn property.
 Issue #2136: Fixing some typos and missing
commas in example for schedule.
Site improvements
 Issue #2132: Added some hierarchy to the
documentation page.
3.6 (May 1, 2019) Version 3.6. See planning pages. Vocabulary
Core changes
Moved from pending to Core:
Other changes in Core section:
 Issue #2202: Restored estimatedSalary as a
property expected on the JobPosting type.
 Issue #1469: Corrected format of example
durations in timeRequired property description.
 Issue #1470: Corrected duration format in
examples for timeRequired.
490 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
 Issue #2188: Added service to rangeIncludes of
orderedItem property.
 Issue #2184: Added LodgingBusiness to
rangeIncludes of numberOfRooms property.
 Issue #2166: Added number formatting advice to
description of number, ratingValue, value,
lowPrice, highPrice, totalPrice properties.
 Issue #2082: Fixed RDFa example for website.
 Issue #2077: Fixed JSON-LD example for
availableLanguage property.
 Issue #2055: Updated text to correctly quote
princess Leia in example for spokenByCharacter
property.
 Issue #2036: Fix broken“url” term in ItemList
example.
 Issue #2013: Fixed typo in hotels.Html.
 Issue #2003: Improvements to descriptions of
campground and CampingPitch, identifying the
differences between British English and American
English for these and associated terms.
 Issue #1989: Replaced meta with link in
isLiveBroadcast example.
 Issue #1937: Added a direct link to developers
page from schemas page.
 Issue #1605: Made CatholicChurch subclass of
church.
Changes in pending section:
 Issue #1909: Added a courseWorkload property for
use with CourseInstance type.
Site improvements
 Issue #2054: Corrected spelling in README.
md file.
 Issue #2215: Corrected display of enumeration
value terms that are more than 1 subclass away
from a parent enumeration value (e.g.,
EvidenceLevelA).
 Issue #2212: Various fixes to examples. Identified
by linter tests.
 Issue #2209: Updates to Travis test.
 Issue #2233: Fixed non-disply of
acknowledgement text on term pages.
 Issue #2229: Stopped the duplication of references
for some types in *-types.Csv download files.
 Issue #2234: Fix to JSON-LD context file—
properties with text in their range should not have
‘@type: “@id”'set.
 Issue #2218: Split Travis tests into stages for easier
reporting/analysis.
3.5 (April 1, 2019) Version 3.5. See planning pages. This release moves a
number of terms from pending into the
Schema.
org core. It also simplifies and clarifies theSchema.
org extension model, reducing our emphasis on
using named subdomains for topical groups of
schemas. New terms introduced in pending area
include improvements for describing projects,
grants and funding agencies; for describing open-
Vocabulary
Core changes
Moved from pending to Core:
 Issue #1004: BroadcastFrequencySpecification,
FMRadioChannel, AMRadioChannel,
broadcastFrequency, broadcastFrequencyValue,
broadcastFrequencyValue, hasBroadcastChannel.
 Issue #1125: PreOrderAction.
(Continues)
ILIADIS ET AL. 491
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
ended date ranges (e.g., datasets); and a substantial
vocabulary for educational and occupational
credentials.
 Issue #1262: BedType.
 Issue #1293: EndorsementRating.
 Issue #2053: SpeakableSpecification, cssSelector,
xpath.
 Issue #1541: menuAddOn.
 Issue #1670: subjectOf.
 Issue #1689: EmployerAggregateRating,
reviewAspect.
 Issue #1698: Occupation, educationRequirements,
estimatedSalary, experienceRequirements,
occupationalCategory, occupationLocation,
qualifications, responsibilities, skills,
hasOccupation, relevantOccupation,
QuantitativeValueDistribution, median,
percentile10, percentile25, percentile75,
percentile90, MonetaryAmountDistribution.
 Issue #1723: FAQPage.
 Issue #1741: MediaSubscription,
ActionAccessSpecification.
 Issue #243: WorkersUnion.
 Issue #743: Distillery.
Other changes in Core section:
 Issue #2017: Added clip to expected values of
video, audio properties. Also amended caption to
be expected on AudioObject, documented a
pattern for describing downloadable captions and
their media format using another MediaObject
with an encodingFormat.
 Issue #2034: Added startTime, endTime properties
as expected for MediaObject type.
 Issue #2038: Add person as an expected type for
byArtist property.
 Issue #2112: Added slogan property, analogous
to logo.
 Issue #2104: Improved description of elevation
property.
 Issue #1030: Noted that encodesCreativeWork is
inverseOf encoding.
 Issue #2021: Added startOffset and endOffset
to clip.
 Issue #1765: Removed superseded status from and
generalized descriptions for spatial and temporal
properties plus expanded range to CreativeWork.
Changes in pending section:
 Issue #1365: In temporalCoverage, added
proposed ISO 8601 notation for open-ended date
ranges, for example, 1972–2001.
 Issue #383: Added initial vocabulary towards
improved support description of project-based
funding, for example to use with dataset citations.
See also DINGO draft, another outcome from the
same Wikidata/Wikibase workshop. New types for
Grant, MonetaryGrant, project, FundingAgency,
FundingScheme, and ResearchProject. Developed
in collaboration with the Wikidata/Wikibase
community.
492 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
 Issue #1591: Added jobLocationType property.
 Issue #2083: Added
applicantLocationRequirements property.
 Issue #2085: Added membershipPointsEarned
property.
 Issue #2140: Added 3DModel type.
 Issue #2109: Added callSign property, and
RadioBroadcastService type.
 Issue #2111: Added broadcastSignalModulation
and broadcastSubChannel for use with
BroadcastFrequencySpecification.
 Issue #1758: Added ArchiveOrganization,
ArchiveComponent types, and archiveHeld,
holdingArchive properties.
 Issue #1759: Added collectionSize and
materialExtent properties.
 Issue #1978: Educational and occupational
credentials vocabulary and examples from the
eocred-schema community group. Added a type
EducationalOccupationalCredential and
properties credentialCategory, educationalLevel,
competencyRequired, recognizedBy. Minor
changes to validIn, validFor,
educationRequirements,
educationalCredentialAwarded, and qualifications
(linking EducationalOccupationalCredentials to
JobPostings, occupations and courses).
 Issue #1968: Replaced use of hasPart and isPartOf
properties on trip type, with new subTrip and
partOfTrip properties.
 Issue #1375: Renamed the various properties and
labels from geospatiallyXyz to geoXyz for brevity,
for example, geoIntersects.
 Issue #1448: Added manuscript, poster, drawing,
and SheetMusic subtypes of CreativeWork.
 Issue #1976: Added ShortStory subtype of
CreativeWork.
 Issue #1816: Added play subtype of CreativeWork.
Site improvements
 Added section to Github README discouraging
large projects without prior discussion.
 Linked Travis-CI from Github README.
 Clarified and simplified the extension mechanism.
3.4 (sdo-telesto; June
15, 2018)
Version 3.4 (working name“sdo-telesto”). See
planning pages. Clarifications around series.
Introduced an example showing ClaimReview of a
clip within a larger media object. A lot of small
fixes and maintenance edits. Numerous additions
to the pending area, including employment and
occupation vocabulary, a claim type to help
explore richer modeling around fact-checks,
tourism-related vocabulary. Other pending area
improvements include amendments to the
legislation vocabulary, trust project additions, and
the proposal of an inverse of the about property,
subjectOf.
Vocabulary
Core changes
 Issue #1902: Improvements to HowTo examples.
See also #1895.
 Issue #1761: Changed mis-abbreviation of Friday
as “Fri” to “Fr.” Per the guidelines for
openingHours, Friday should be abbreviated as
“Fr.” In one set of examples, it was abbreviated
as “Fri.”
 Issue #1820: Hyperlink to new, recommended
DOI resolver.
 Issue #1894: Added reference to cryptocurrencies
in description for“paymentAccepted” and
(Continues)
ILIADIS ET AL. 493
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
“currenciesAccepted” properties. For consistency,
also added to description of properties:
“discountCurrency,”“ price,”“ priceCurrency,”
“currency.” Updated the description additions to
reference ISO 4217 formats, cryptocurrency Ticker
symbols, LETS and other currency types including
single inline examples for each.
 Issue #1090: Clarified series, CreativeWorkSeries,
EventSeries. The series type is now intangible,
rather than having an inappropriate CreativeWork
supertype. We have two subtypes of it,
CreativeWorkSeries (successor to the original
definition of series, which was too generally
named), plus the proposed EventSeries type
(currently in the pending area). These domain-
specific series types also have corresponding
supertypes in CreativeWork and event. See also
issue #447.
 Issue #1155: Clarified that encodingFormat,
fileFormat mean the same thing, converged their
definitions, and made encodingFormat the
preferred term.
 Issue #1824: Fixed typos in tickerSymbol.
 Issue #1833: Added expected type ItemList to
acceptedAnswer, suggestedAnswer.
 Issue #1799: Fixed an error in an example for
question type.
 Issue #1686: Added an extra ClaimReview
example based on a TV clip.
 Issue #1762: Added schema mapping declarations
indicating that“name” is a subproperty of
rdfs:Label, and equivalentProperty of
dcterms:Title.
 Issue #1729: Improvements around HowTo,
including declaration of CreativeWork as its
supertype, and introduction of“step” property
instead of“steps.”
 Issue #1732: Changed HowToSection and
HowToStep (which support the HowTo type) to
have CreativeWork as their supertype.
 Issue #1723: Introduced FAQPage, which
represents a WebPage presenting one or more
“frequently asked questions.”
 Issue #1935: Extend the contentRating property to
also expect the rating type.
 Issue #2020: Extend the byArtist property to also
expect the person type.
Changes in pending section
 Issue #1670: Add a subjectOf to thing as an
inverse property of about.
 Issue #1689: Add EmployerAggregateRating as a
subtype of AggregateRating to differentiate ratings
for the entity as an employer and the
reviewAspect property to review and rating to
allow authors to specify the facet or relevant part
of being reviewed.
494 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
 Issue #1698: Add a occupation type with the
supporting properties, many of which existed for
JobPosting. A Person's occupation can be specified
with hasOccupation. The Occupation's
estimatedSalary is expressed as a
MonetaryAmountDistribution, a subtype of the
new QuantitativeValueDistribution type.
 Issue #1787: Narrowed the range of
legislationJurisdiction to AdministrativeArea
rather than place. Broadened the range of
legislationIdentifier to include URL, to match with
the description of the property.
 Issue #1815: Added proposal for
TouristDestination, TouristTrip, and trip plus
examples.
 Issue #1886: Add basic sdPublisher and
sdDatePublished (and in #1866, sdLicense)
markup, for example, for when structured data
created elsewhere.
 Issue #1866: Added a proposed sdLicense
property.
 Issue #1776: Introduced DefinedTerm as a super
type of the existing proposed term CategoryCode,
to support non-categorical controlled terms.
 Issue #1828: Added a claim type, to make explicit
a concept suggested in the ClaimReview fact-
checking markup.
 Issue #1773: Add a MediaSubscription type with
the supporting properties to describe a
subscription for viewing media. Also added
ActionAccessSpecification to allow authors to
specify when a ConsumeAction requires a
subscription or a purchase.
 Issue #1744: Improvements around legislation
vocabulary. Changed definition of“legislation” to
make it clear that it is a document. Deleted
numerous inverse properties. Fixed range on
legislationType (CategoryCode). Added
legislationJurisdiction as a subproperty of
spatialCoverage. Fixed definitive into
DefinitiveLegalValue to align with other values.
Expanded the definition of legislationIdentifier to
clarify that it can apply to string or URIs. Fixed
and adjusted the examples accordingly.
 Issue #1709: Added an occupation type and
examples, to represent professions.
 Issue #1389: Updated SpeakableSpecification-
related properties,“xpath” and “cssSelector” to
explain how they relate to“WebPageElement.”
Allowed both properties to be expected on
that type.
 Issue #1525: Improvement suggested by trust
project, including addition of
AskPublicNewsArticle, ownershipFundingInfo
and diversityStaffingReport properties, editorial
tweaks to dateline property. Second phase of
(Continues)
ILIADIS ET AL. 495
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
additions included knowsAbout, knowsLanguage
proposals (#1688.)
 Issue #1950: Added CorrectionComment and a
property correction to point to it, as suggested by
the trust project.
Changes in other named extensions
 Issue #1882: Fix to OccupationalTherapy— made
OccupationalTherapy a simple class instead of a
typeof schema:MedicalSpecialty
 Issue #1677: Added (and #1900 improved) autos
documentation.
Site improvements
 Issue #1634: Aliased“rdf:HTML” to “HTML” in
JSON-LD context definitions.
 Issue #1879: Fix to duplicate and missing
properties listings in the CSV outputs for types
and enumeration values (see also #1882).
 Issue #1878: Improvements towards a more
responsive HTML design, thanks to Dan Scott.
 Issue #1857: Updated site search function to use
Google custom search v2 API.
 Issue #1646: Updated various links to use https
when referring to this site.
 Issue #1722: Continuous integration tests now
check RDFa syntax.
 Issue #1946: Linked experimental D3/RDFS and
OWL representations from the developers page.
3.3 (sdo-enceladus;
August 14, 2017)
Version 3.3 (working name“sdo-enceladus”). See
planning pages, specifically #1569 for details.
This release introduces pending types around review,
NewsArticle and article that allow more fine-
grained distinctions to be made. It adds a
TouristAttraction type to the core, and a draft
PublicToilet type as a pending proposal. It adds a
HowTo vocabulary that generalizes recipe-like
structured instructions, and adds some useful
properties to EmailMessage. It also adds a
substantial vocabulary for describing legislation to
the pending section.
Vocabulary
Core changes
 Issue #1459: Improvements to TouristAttraction.
Add a new property touristType to
TouristAttraction, “attraction suitable for type(s)
of tourist. For example, Children, visitors from a
particular country, etc.” Extend the domain of
availableLanguage to TouristAttraction, of
isAccessibleForFree to place, adapting the
definitions accordingly. Add new property
publicAccess to place.“A flag to signal that the
place is accessible by public visitors.”
 Issue #1525: Expanded definition of NewsArticle
from “A news article” and added a news overview
document introducing some proposed additional
terms, and discussing the relationship between
news and related markup for education/learning,
TV, radio, and so forth.
 Issue #647: Add a HowTo type, building upon and
generalizing the existing recipe vocabulary. This
introduces estimatedCost, steps, supply and tool as
new properties, and re-uses performTime,
prepTime, totalTime. We also introduce yield,
which generalizes the existing recipeYield, and
note that performTime generalizes the existing
cookTime. Supporting types HowToItem (with a
requiredQuantity property), HowToSupply and
HowToTool, HowToSection and HowToStep (a
kind of ItemList) are also provided, to allow more
496 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
explicitly structured steps to be described. This
effort has had many contributors over the years—
thanks to all who have helped!
 Issue #1590: Add bccRecipient, ccRecipient, and
toRecipient for use with EmailMessage.
 Moved to Core from pending:
/C14None proposed.
Additions to pending section
 Issue #1457: Add a schedule type, with supporting
properties: repeatFrequency, repeatCount, byDay,
byMonth, byMonthDay, exceptDate,
eventSchedule. These terms are used alongside the
existing startTime and endTime properties. The
main purpose of this new vocabulary is to capture
recurring events in a manner compatible with a
subset of the iCalendar approach.
 Issue #1156: Add legislation, LegalForceStatus,
LegislationObject, LegalValueLevel and other
supporting terms. These terms are based on the
European legislation identifier (ELI) ontology and
the work of the ELI taskforce. ELI is an initiative
of some national legislation publishers endorsed
by EU countries and institutions, to identify,
describe and link legislation on the web.
 Issue #1624: Add a draft PublicToilet type to the
pending section.
 Issue #1577: Add estimatedSalary to JobPosting.
 Issue #1589: Add CriticReview and UserReview to
distinguish common subtypes of review.
 Issue #1576: Add EmployerReview to indicate
reviews that are by a current or former employee,
and that are reviews of that organization's role as
an employer.
 Issue #1525: Add subtypes of NewsArticle:
ReportageNewsArticle, AnalysisNewsArticle,
OpinionNewsArticle, ReviewNewsArticle,
BackgroundNewsArticle to distinguish common
kinds of NewsArticle. Also add a subtype of
article, AdvertiserContentArticle and a news
overview document. Added a subtype of
organization, NewsMediaOrganization, alongside
several “best practice”-oriented properties:
actionableFeedbackPolicy, correctionsPolicy,
diversityPolicy, ethicsPolicy, masthead,
missionCoveragePrioritiesPolicy,
unnamedSourcesPolicy,
verificationFactCheckingPolicy (apart from
ethicsPolicy and diversityPolicy, these are all sub-
properties of publishingPrinciples). These changes
were based in large part upon the work of the
trust project.
 Issue #1437: Add SatiricalArticle type.
Site improvements
 Issue #1582: Added dedicated documentation page
describing background and examples for banking
and finance terms.
(Continues)
ILIADIS ET AL. 497
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
3.2 (sdo-callisto; march
23, 2017)
Version 3.2 (working name“sdo-callisto”). See
planning pages, specifically #1292 for details.
This release introduces new core vocabulary
including mechanisms for describing fact-check
reviews, courses, and menus. It also introduces a
number of newly-proposed terms via the
“pending” area, to encourage discussion,
implementation feedback and other improvements.
Vocabulary
Core changes
 Issue #1209: Added maximumAttendeeCapacity
and remainingAttendeeCapacity for describing
places and events.
 Issue #1361: Broadened about property to be
applicable on events.
 Issue #1364: Broadened genre property to be
applicable on BroadcastChannel.
 Issue #1488: Added identifier as a common super-
property of numerous identifying properties.
 Issue #1288: Added types menu, MenuItem,
MenuSection, and properties hasMenuItem,
hasMenuSection. A proposed menuAddOn
property has also been added to pending for
further design discussion and implementor
feedback. Introduced hasMenu property that
supersedes menu, both for consistency with the
other new menu properties, and to avoid a
property and type having essentially the
same name.
 Moved to Core from pending:
/C14Issue #195: Added course-description terms:
Course, courseCode, coursePrerequisites,
hasCourseInstance, CourseInstance,
courseMode, instructor. Thanks to the schema
course extension community group at W3C,
initiated by LRMI and led by Phil barker.
/C14Issue #1061: Migrated ClaimReview and
claimReviewed for fact-checking reviews into
Core section.
/C14Issue #1100: Added accessMode,
accessModeSufficient, accessibilitySummary
properties to support accessible digital
publishing. This proposal came from the digital
publishing community, and specifically from
the Epub 3.1 accessibility working group.
Additions to pending section
 Issue #1541: Add a menuAddOn property
(originally proposed with other menu-related
terms).
 Issue #1125 added PreOrderAction (a subtype of
TradeAction)
 Issue #1253: Added several terms proposed by the
FIBO project and its community group.
/C14Types: BrokerageAccount,
ExchangeRateSpecification, InvestmentFund,
MoneyTransfer, MortgageLoan,
RepaymentSpecification.
/C14Properties: accountMinimumInflow,
accountOverdraftLimit, amount,
bankAccountType, beneficiaryBank, cashBack,
contactlessPayment, currency,
currentExchangeRate, domiciledMortgage,
downPayment, earlyPrepaymentPenalty,
exchangeRateSpread, floorLimit, gracePeriod,
498 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
loanMortgageMandateAmount,
loanPaymentAmount, loanPaymentFrequency,
loanRepaymentForm, loanType,
monthlyMinimumRepaymentAmount,
numberOfLoanPayments, recourseLoan,
renegotiableLoan.
 Issue #1262: Added BedType.
 Issue #1293: Added EndorsementRating.
 Issue #1375 added GeospatialGeometry and some
draft definitions for associated properties, an
informal collaboration with the W3C spatial data
on the web working group. Initial properties are:
geoContains, geoCoveredBy, geoCovers,
geoCrosses, geoDisjoint, geoEquals, geoIntersects,
geoOverlaps, geoTouches, geoWithin.
 Issue #1389: Added new type
SpeakableSpecification, with properties cssSelector
and xpath, alongside a property on WebPage
called speakable to refer to a
SpeakableSpecification. The purpose (documented
primarily on the speakable property) is to indicate
sections of a document that are highlighted as
particularly suitable for being spoken/read. These
sections are indicated via URL/ID values, XPath
and/or CSS selectors.
 Issue #1397: Added CompleteDateFeed to indicate
completeness of feeds.
 Issue #1423: Added a draft WebAPI.
 Issue #1425: Added a draft
measurementTechnique property, to support
richer dataset description particularly for
scientific data.
 Issue #1495: Added a consortium type, as well as a
LibrarySystem type to represent a particular kind
of library consortium.
 Issue #743: Added a distillery type.
 Issue #894: Added CategoryCode,
CategoryCodeSet, codeValue and inCodeSet to
explore better description of enumerated value
lists.
 Issue #1004: Added broadcastFrequency,
broadcastFrequencyValue and
BroadcastFrequencySpecification for describing
(primarily radio but also TV) frequencies. Also
supporting types FMRadioChannel,
AMRadioChannel, and property
hasBroadcastChannel (inverse:
providesBroadcastService).
Archived into attic section
 The proposed variablesMeasured property has
been removed from pending. A non-plural
variableMeasured property replaced it.
 broadcastSignalModulation was retired august 17,
2016 from pending section.
 The courses proposal while in pending originally
had additional terms— courseCredits,
(Continues)
ILIADIS ET AL. 499
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
courseCreditsUnit, grantsCredential,
previewUrl— which should be archived here.
Site improvements
 Issue #1027: Published a basic robots.Txt file to
avoid a template file being indexed by search
engines.
 Issue #1272: Created an internet of things (IoT)
section, mailing list and discussion document. At
this stage no specific schemas are proposed, only
some basic infrastructure for collaboration and
schema review.
 Issue #1398: Added HTML anchor to support links
to the“incoming” section of pages documenting
types (see example).
 Issue #1483: Added a sitemap.Xml file.
 Issue #53: Added Travis-CI monitoring for test
cases and syntax checking of examples.
 Issue #1351: Improvements to the output formats
of downloads section in developers page.
Quick fixes and examples
 Issue #1475: Clarified that event can have an
audience property.
 Issue #1494: Broadened lender to allow
organizations as possible values.
 Issue #1294: Restored material as a super-property
of artMedium that can be used with any product
or CreativeWork. Also marked artworkSurface as
another specialized sub-property of material. The
material property can now also have product as its
value, allowing branded and manufactured
materials to be described in more detail.
 Issue #1290: Add the word“event” to
isAccessibleForFree definition.
 Issue #1162: Updated text for sameAs— freebase
mention migrated to reference Wikidata.
3.1 (sdo-makemake;
August 9, 2016)
Version 3.1 (working name“sdo-makemake”). See
planning pages, specifically #1212 for details.
This release is primarily concerned with hotel/
accomodation vocabulary, improvements around
dataset, and bug fixes.
Vocabulary
 Issue #915: Added substantial vocabulary for
hotels and related accomodation, alongside a
dedicated documentation page. New vocabulary
includes LodgingBusiness, accommodation, and
several subtypes which can be used (via multiple
typing) alongside the existing offer type. Other
terms include starRating, amenityFeature,
LocationFeatureSpecification, floorSize,
permittedUsage, petsAllowed, checkinTime,
checkoutTime…
 Issue #1203: Fixes for accidental rollbacks in 3.0.
See Github for comprehensive analysis and details.
Restored several definitions: paymentStatus lacked
PaymentStatusType from #518;
breastfeedingWarning, healthCondition,
prescriptionStatus and secondaryPrevention have
been migrated into
health-lifesci.schema.org as
planned; SocialMediaPosting has supertype of
BlogPosting (from #526) rather than Article; genre
expects URL values (from #346); affiliation is a
500 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
sub-property of memberOf (per #596); cookTime,
prepTime and totalTime definitions hyperlink to
ISO 8601 details; publisher property can reference
Person (fix for #1198, restoring #611);
videoFormat is again expected on BroadcastEvent,
ScreeningEvent (and BroadcastService), rather
than TelevisionStation (per #577);
parentOrganization and subOrganization are
noted as mutual inverses (per #g535);
codeSampleType description improved per #343;
netWorth definition now correctly omits
Organization (per #585).
 Issue #900: Extended isAccessibleForFree to be
expected potentially on any event or
CreativeWork.
 Issue #996: Added DateTime to expected values
for startDate, endDate, commentTime.
 Issue #1083: Improvements primarily around
dataset, generalized spatial property of dataset to
become spatialCoverage of any CreativeWork;
similarly generalized temporal as
temporalCoverage. Indicated that spatialCoverage
is a subproperty of contentLocation. Broadened
sponsor to apply to creative works such as
datasets, and added a more specific subproperty to
indicate funder. Amended definition of
MediaObject to match its use as a supertype of
DataDownload. Amended fileFormat to allow
URL as a way of indicating niche or unregistered
file formats (common for scientific datasets).
Added a draft variablesMeasured property to the
pending extension.
Site improvements
 Issue #1234: Enhanced incoming properties
display (instances of [… ] may appear as values for
the following properties) to include properties
from extensions.
 Issue #479: Updated and clarified the datamodel
document, including conformance section.
 Issue #1213: Fixes for site performance problems.
 Issue #1214: Fix for RDFa formatting errors in
per-term pages.
 Issue #1248: Fix for need easy way to download
rdf definition files. Introduces a vocabulary
definition download section providing access to
RDF representations of the vocabulary and
extensions in triple, quad, JSON-LD, and turtle
format.
Quick fixes and examples
 Issue #1151: Broadened version to allow textual
values as well as numbers.
 Issue #1257: Fixed all labels to match
corresponding term IDs exactly.
 Issue #1260: Fixed product example, microdata
was missing itemprop attribute.
(Continues)
ILIADIS ET AL. 501
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
 Issue #1201: Clarified deliveryLeadTime for the
case of on-site pickup.
 Issue #1283: Removed dentist from deprecated
type ProfessionalService, added LocalBusiness as a
supertype.
The following early access fixes were published
between 3.0 and 3.1 releases:
 Issue #1159: Fixed problems with W3C validator,
caching, and misclassification of manufacturer
property which in in core rather than health-
lifesci extension.
 Issue #1165: Improved wording for term pages
that are not in core, to avoid publishers worrying
that they need to change their markup.
 Issue #1136: Fixed term labels to always be
alphanumeric (no“bib:” prefixes etc.)
 Issue #1168: Fixed unit tests to run against
extension schema data as well as core.
 Issue #1169: Fixes for property/type associations
in health-lifesci and pending drafts, identified by
improved unit tests.
 Issue #1174: Fix for missing definition for
“ingredients.”
3.0 (sdo-deimos; May
4, 2016)
Version 3.0 (working name“sdo-deimos”). See
planning pages, specifically #911 for details.
This release introduces three new extensions.
The
meta.schema.org extension contains terms
primarily designed to support the implementation
of the
Schema.org vocabulary itself.
The pending.schema.org extension is a staging area
for work-in-progress terms which have yet to be
accepted into the core vocabulary. Pending terms
are subject to change and should be used with
caution.
The
health-lifesci.schema.org extension is a new
home for our existing medical and healthcare
related terms, as well as potential future
collaborative work.
The initial releases of
bib.schema.org and auto.
schema.org have also been finalized.
In addition to numerous vocabulary-related
improvements, we have added a new“how we
work” document providing an overview of the
project's approach to schema development,
collaboration, versioning and change review. In
particular it documents the use of the new pending
extension, which gives earlier access to proposed
new schema designs, as well the parallel
webschemas.org site which shows the latest work-
in-progress version of the entireschema.org site.
Vocabulary
Core changes
 Issue #845: Added vocabulary for suitability to
restricted diets in recipe (suitableForDiet,
RestrictedDiet).
 Issue #1005: Generalized some properties from
product to apply also to service-audience, brand,
logo, isRelatedTo, isSimilarTo.
 Issue #880: Added disambiguatingDescription to
explicitly indicate short Wikipedia-like
disambiguating descriptions.
 Issue #1048: Added DigitalDocument and
subtypes SpreadsheetDigitalDocument,
PresentationDigitalDocument,
TextDigitalDocument, NoteDigitalDocument. Also
a hasDigitalDocumentPermission property of
these whose value is a
DigitalDocumentPermission type. A
permissionType property of each
DigitalDocumentPermission has values that are
from a DigitalDocumentPermissionType
enumeration: CommentPermission,
ReadPermission, WritePermission. The grantee
property indicates in each case the person,
organization, contact point, or audience that has
been granted that permission.
 Issue #888: Added PreSale to the ItemAvailability
enumerated values.
 Issue #962: Broadened definition of sponsor
property.
 Issue #961: Improved wording of validThrough,
and added JobPosting to allow markup for job
posting closing dates.
502 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
 Issue #1020: Added new subtypes of
CreativeWork: Message and conversation. Marked
EmailMessage as a subtype of message.
 Issue #1079: Created ComputerLanguage,
amended programmingLanguage to expect it (and
text); amended language to focus on natural
languages. Noted that BCP 47 should be used for
natural language tagging, via alternateName
property. Amended availableLanguage to indicate
that text values are expected, that BCP 47 is
encouraged, and to cross-reference with
inLanguage.
 Issue #1092: Amended contributor, actor,
translator, director, composer to apply to event.
 Issue #969: Integrated improvements from FIBO
to core terminology around financial products,
including the addition of MonetaryAmount
(superseding DatedMoneySpecification) and
CompoundPriceSpecification, alongside improved
wording around CreditCard, PriceSpecification.
 Issue #923: Created
schema.org entries for
Monday–Friday and PublicHolidays, based on the
GoodRelations originals. Also clarified
OpeningHoursSpecification and added a
specialOpeningHoursSpecification property to
allow for general opening hours to be overridden.
 Issue #541: Added enumerations for male and
female, but allow other values as well.
 See also issue #492 below; many terms have been
moved from the core into health-lifesci.
auto.
schema.org
 Issue #922: Finalized first release ofauto.schema.
org. Removed“pre-final preview release”
description.bib.schema.org
 Issue #911: Finalized first release ofbib.schema.
org. Removed“pre-final preview release”
description.health-lifesci.schema.org
 Issue #492: Moved a large number of medical/
health terms from core into a health-lifesci
extension.pending.schema.org
The pending extension is a staging area for work-in-
progress terms which have yet to be accepted into
the core vocabulary.
 Issue #1050: Added contentReferenceTime.
 Issue #1062: Added HealthInsurancePlan, a US
health insurance schema.
 Issue #1110: Added accessMode,
accessModeSufficient and accessibilitySummary.
 Issue #447: Added EventSeries.
 Issue #271: Added quotation and
spokenByCharacter.
 Issue #1061: Added ClaimReview and
claimReviewed for fact-checking reviews.
 Issue #1059: Created
pending.schema.org to
enable publication of work-in-progress drafts for
wider review.
(Continues)
ILIADIS ET AL. 503
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
 Issue #1045: Added LinkRole as a subtype of role,
and a linkRelationship property.
 Issues #243: Added WorkersUnion.
 Issue #1004: Added broadcastFrequency to
BroadcastService to specify the over the air
frequency.
 Issue #195: Added snapshot of the evolving
course-related terms being developed by the
course extension community group.
Site improvements
 Issue #1059: Created hosted extensions for“meta”
vocabulary and for“pending” vocabulary under
review. Moved class, property, domainIncludes,
rangeIncludes, inverseOf, supersededBy into meta.
 Issue #256: Implementation of HTTP HEAD for
all pages.
 Issue #1095: ETag and last-modified headers only
for successful page requests.
 Issue #1098: Added categorization of terms listed
on extension home page.
 Issue #990: JSON-LD context file should
enumerate all terms. This will make it easier to
combine the use of
schema.org with other
vocabularies and extensions.
 Issue #1075: Added markdown format processing
of comment fields. This makes the schema editing
process easier, especially for cross-referencing
related terms.
 Issue #178: Integrated rdflib python library. This
improves our ability to parse RDFa and JSON-LD
schema definitions, and makes unit tests easier
to run.
 Issue #1109: We now display when a type is
superseded.
Quick fixes and examples
 [core] issue #1097: partOfOrder and partOfSystem
are no longer marked as sub-properties of isPartOf
since they are not relations between creative
works.
 [core] issue #1102: Examples fixed to avoid
“content” attribute on span element in microdata.
 [core] issue #1066: Cleanup around dataset/
DataCatalog association: Renamed
containedDataCatalog as includedInDataCatalog,
marked it as inverse of dataset and improved
wording of both definitions.
 [core] issue #1073: Removed redundant types
listed for branchCode— place already covered
LocalBusiness and store.
 [core] issue #1081: Added AudiobookFormat to
the BookFormatType, for consistency. Note that
the bib extension also has a dedicated type for
describing audio books.
 [core] issue #950: isBasedOnUrl now called
isBasedOn; isBasedOnUrl still exists but is marked
504 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
as supersededBy isBasedOn. Extended range to
include (for now just) CreativeWork, product.
 [core] issue #929: Marked subEvent and
superEvent as inverses of each other.
 [core] issue #929: The colleague property now also
expects URL values (and for JSON-LD therefore
expects things not strings by default).
 [core] various typo fixes (including #1014).
 [core] issue #966: Fixed bug in PropertyValue
JSON-LD example.
 [core] issue #912: Added education/learning
examples (from Phil barker/LRMI):
learningResourceType, educationalAlignment,
AlignmentObject, educationalFramework,
alignmentType, targetName, targetUrl, audience,
EducationalAudience, typicalAgeRange,
timeRequired, educationalRole.
 [core] issue #919: Fixed Javascript errors caused
by bad markup in 404 pages (published December
10, 2015).
 [core] issue #899: Bugfix for a few pages that were
returning 500 error codes (published December
10, 2015).
 [core] issue #904: Simplified JSON-LD examples
for periodical (published December 10, 2015).
 [core] issue #1015: Fixed spelling of“content” in
FoodEstablishment example.
 [core] issue #997: Expanded sharedContent to
coverage of SocialMediaPosting example.
 [core] issue #992: Removed an example from
QAPage since the example did not illustrate the
term's use.
 [core] issue #836: Markup fixes to examples of
PropertyValue.
 [core] issue #143: Fixed openingHours examples
to use span element instead of time, and some
time examples to use datetime attribute instead of
content.
 [core] issue #3905: CSS fix to actions document.
 [core] issue #511: Microdata examples fixed to use
“href” example on“link” element instead of
“content” on “meta.”
 [core] issue #533: OpeningHoursSpecification
example: Various fixes including better use of
“time” element.
 [bib] issue #984: Bug fixes for
bib.schema.org/
Chapter example.
2.2 (sdo-phobos;
November 5, 2015)
Version 2.2 (working name“sdo-phobos”). This
release combines a range of small additions across
several areas of
schema.org with an ongoing
concern for cleanup and integration of existing
vocabulary. Notable additions include
ExhibitionEvent, barcode, DataFeed,
containsPlace, GeoCircle, geoRadius, geoMidpoint,
providerMobility and actionPlatform. A number of
changes improve our handling of service
Vocabulary
 Issue #773: Added actionPlatform as a simpler
mechanism to specify the platform for EntryPoint
targets.
 Issue #823: Marked homeLocation, workLocation
as subproperties of location, and marked location
as expecting textual values.
 Issue #818: Added OfferCatalog for specifying a
catalog of offers by an organization or service.
(Continues)
ILIADIS ET AL. 505
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
description, including the deprecation of the
ProfessionalService construct. We have kept all the
specific types that were previously considered
ProfessionalService but discourage the use of the
type “ProfessionalService” since it is easily
confused with“service.”
 Issue #817: Added providerMobility to describe
whether a service provider is at a fixed location or
has a dynamic location.
 Issue #445: Added ExhibitionEvent and added a
superproperty of workPresented and
workPerformed to cover event-to-work
relationships such as a work being exhibited.
 Issue #113: Added GeoCircle as a subtype of
GeoShape, providing a more usable mechanism
than circle structured text; added geoRadius,
geoMidpoint to describe the size and location of
these circular areas.
 Issue #323: Added locationCreated to
CreativeWork.
 Issue #811: Renamed containedIn as
containedInPlace, and added an inverse
containsPlace.
 Issue #810: postalCode and addressCountry are
now an expected property for GeoShape and
GeoCoordinates. Adjusted addressCountry to
allow textual values, matching the existing
definition.
 Issue #801: Broadened award, category, offers to
be applicable on service. Extended itemOffered to
expect service as a possible value. Added
LegalService as a supertype for notary, attorney.
Marked ProfessionalService as deprecated, with
some explanation, and added a brief account of
the relationship with service to some of the more
service-oriented local business types for example,
LegalService, HomeAndConstructionBusiness. A
cluster of construction-related local businesses
formerly treated as ProfessionalService continue as
HomeAndConstructionBusiness subtypes. Marked
attorney as deprecated in favor of LegalService per
#784. Added hoursAvailable to service.
 Issue #411 clarification and cleanup around
areaServed, now marked as a super-property of
the more specific eligibleRegion and
availableAtOrFrom properties. Cross-referenced
eligibleRegion and ineligibleRegion. Marked
serviceArea as supersededBy areaServed. Updated
the associated types for areaServed to cover those
used by its sub-properties.
 Issue #808: The address property now anticipates
text values, to support unstructured address data.
 Issue #802: Referenced world Geotic system from
GeoCoordinates properties (elevation, longitude,
latitude); made address an expected property for
GeoCoordinates and GeoShape.
 Issue #796 added offeredBy property to relate an
offer to a person or organization. Inverse of
makesOffer.
 Issue #791 added branchCode to represent codes
identifying stores and other business locations.
506 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
 Issue #790 broadened fileFormat to be usable with
CreativeWork, and improved the description.
 Issue #687: Added barcode as a subtype of
ImageObject.
 Issue #688: Added DataFeed and DataFeedItem to
represent a data feed of structured items and
supportingData for using DataFeed to provide data
to a software application.
 Issue #767: Added countryOfOrigin property to
movie, TVEpisode, TVSeason, and TVSeries.
 Issue #768: Added broadcastOfEvent property to
BroadcastEvent to allow for specifying the event
being broadcasted.
 Issue #432: Added organization to domain of
alumni and to range of alumniOf properties.
Site improvements
 Updated FAQ to clarify CC licensing of docs/
examples and use of https: URLs in
structured data.
 Updated feedback form to permit per-term
feedback and to be explicit that feedback messages
may be shared with the wider community.
 Issue #769: Sorting of multi-inheritance
breadcrumbs on term pages.
 Issue #761: Updated linking structure in“more… ”
section of term pages.
 Listing of extension contents on extension home
pages (eg.
bib.schema.org)
 Term counts added to docs/schemas.Html— the
core vocabulary currently consists of 638 types, 980
properties, and 219 enumeration values.
 List of enabled extensions added to docs/
schemas.Html.
 Various internal software fixes, unit tests and
cleanup.
Quick fixes and examples
 Issue #764 added example for makesOffer.
 Issue #733 added example showing library
availability for book. Also added example for
library and linked it to openingHoursSpecification
as a good example for that too.
 Bulk update to examples: Various fixes to html
syntax, missing quotes and <meta> tags that
should be <link> tags.
 Issue #478: Replaced <meta> tags that should be
<link> tags in periodical examples.
 Several small markup fixes to various examples.
See also issue list for this release.
2.1 (sdo-ganymede;
August 6, 2015)
Version 2.1 (working name“sdo-ganymede”)
includes many small fixes, some new vocabulary,
as well as the first release of the“hosted
extensions” mechanism, featuring bib(liographic),
and auto(mobile) extensions for final review. A
pre-release of this version of
schema.org was
available for review.
Vocabulary
 Issue #611: Added person as expected value for
publisher property.
 Issue #596: Documented that affiliation is a sub-
property of memberOf.
 Issue #207: Added a bridge type under
CivicStructure.
(Continues)
ILIADIS ET AL. 507
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
 Issue #346: Added URL as expected value for
genre property.
 Issue #374: Added report type under article, and a
reportNumber property.
 Issue #577: Amended videoFormat to indicate that
it is expected on BroadcastEvent and
ScreeningEvent, rather than TelevisionStation.
 Issue #535: Broadened domain of
parentOrganization to allow any organization,
rather than only LocalBusiness. Noted
parentOrganization and subOrganization as
inverses.
 Issue #531: Added the lyrics property to
MusicComposition.
 Issue #518: Renamed paymentDue property to
paymentDueDate. Changed paymentStatus
property to expect an enumerated value of type
PaymentStatusType in addition to text. The
options are: PaymentComplete, PaymentDue,
PaymentPastDue, PaymentDeclined and
PaymentAutomaticallyApplied.
 Issue #137: Deprecated UserInteraction and its
children in favor of a new type:
InteractionCounter. InteractionCounter allows for
reporting aggregated statistics by service and type.
Thanks elf Pavlik for collaboration.
 Issue #526: Added new types LiveBlogPosting,
SocialMediaPosting, and DiscussionForumPosting,
alongside supporting properties.
 Issue #334: Updated the controlled values for
accessibilityHazard shown in examples to follow
latest community recommendations:“noFlashing”
is now“noFlashingHazard,”
“noMotionSimulation” is
“noMotionSimulationHazard,” and “noSound” is
“noSoundHazard.”
Site improvements
 Issue #429: Hosted extensions for example,
bib.
schema.org are now enabled and linked from
“core” pages with appropriate navigation and
styling.
 Issue #655: Extension definitions now include an
isPartOf property to link them to the extension.
 Issue #527: Added materials from kickoff
workshop in 2011.
 Issue #78: Multiple supertypes are now displayed
properly. It is possible for severalschema.org types
to apply to a single thing, and for a type to have
multiple parent types. This is relatively rare, but
important to display. For example, anything that
is a LocalBusiness is considered both an
organization and a place; so all subtypes of
LocalBusiness have both as supertypes. We can
now show this more clearly, for example,
ElectronicsStore.
508 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
 Added CSS for explicit styling () in releases page
during steering group review of candidate releases.
 Issue #557, #660, #695, #469: Several DataType-
related navigation fixes, following recent modeling
changes.
 Issue #548: Added a favicon.Ico image. The text is
tiny and not intended for humans to read.
 Behind the scenes: Cleanup and improvements to
python code, unit tests, CSS, filetree layout.
Quick fixes and examples
 Issue #343: Improved description of sampleType.
 Issue #498: We now write“a URL” consistently,
rather than sometimes also using“an URL.”
 Issue #585: Fix description of netWorth, which
erroneously included organization.
 #570: Added RDFa and microdata examples for
WatchAction.
 Added new accessibility examples.
 Numerous small documentation fixes for typos,
markup validity and textual clarity.
 Fixes to several examples including byArtist,
place, question/answer,…
 Issue #552, #644: Fixes for book examples.
 Issue #382: Removed examples that do not
reference WebPage from WebPage.
 Issue #643: Moved bulk of mainEntityOfPage
documentation into dedicated background notes.
See also issue list for this release.
2.0 (sdo-gozer; May 12,
2015)
Version 2.0 consolidates and integrates
schema.org's
existing vocabulary. This version features many
updated definitions, type/property associations and
term names that improve consistency and
usability. It also introduces a new extension
system. Version 2.0 adds various new terms
including mainEntityOfPage and major
contributions from the automotive ontology
community.
Vocabulary
 Issue #262: Added new vocabulary for car: The
new vocabulary includes a number of properties
such as: numberOfAirbags, numberOfAxles,
numberOfForwardGears, fuelConsumption,
fuelEfficiency vehicleEngine,
EngineSpecification… Thanks to Martin Hepp,
Mirek Sopek, Karol Szczepa/C19nski and others in the
automotive ontology community group. We
anticipate substantial additions that build on this
foundation will be contributed as an extension.
 Issue #301: Added a generic property/values
mechanism, building upon
PropertyValueSpecification, StructuredValue and
value; added PropertyValue and
additionalProperty. See examples for usage. This is
a lightweight mechanism to allow markup of
properties that are not easily mapped to existing
schema.org properties. Whenever possible, it is
generally better to use a dedicatedschema.org
property if one exists.
 Issue #301: Added mainEntityOfPage (and an
inverse, mainEntity) to indicate which of the
entities mentioned in a page is its primary topic.
 Issue #225: Added a schemaVersion property, for
use by applications that require more precise
referencing of schema versions.
(Continues)
ILIADIS ET AL. 509
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
 Issue #266: Added OrderItem to allow
ParcelDelivery to be tracked per item, not just on
an entire order.
 Issue #170: Clarifying CommentAction, comment
by deprecating UserComments. Several mentions
of UserComments removed from other terms.
“inLanguage” supersedes “language.” Added a
resultComment property. UserInteraction and
sub-types will be deprecated.
 Issue #300: Answer is now a sub-type of comment.
The “question” property expects“question” type
for its values (rather than text as in AskAction
previously). Added resultComment on
ReplyAction. Cleaned up examples.
 Issue #130: Amended true and false to be
instances (rather than sub-types) of Boolean.
 Issue #218: Amended DataType to model it as a
sub-class of class, with each datatype for example,
Boolean, text, date, DateTime, time, etc. being
classes that have a typeOf DataType. DataTypes
can have sub-types, for example, integer and float
are subtypes of number.
 Issue #328: Added ScreeningEvent to support
movie/video screenings.
 Issue #314: Added MovieClip and VideoGameClip
as parallels to TVClip and RadioClip.
 Issue #122: Added gtin12 property for product.
 Issue #417: Renamed many types and properties,
which had overly generic names. This is no cause
for alarm, the superseded names can still be used,
although we encourage consumers and producers
of
schema.org data to move towards the newer
terminology. CreativeWorkSeason was season,
CreativeWorkSeries was series,
SoftwareSourceCode was code, TaxiService was
taxi, actionApplication was application,
actionOption was option, artMedium was
material, artworkSurface was surface,
availableOnDevice was device, branchOf was
parentOrganization, broadcastTimezone was
timezone, codeSampleType was sampleType,
containsSeason was season, datasetTimeInterval
was temporal, executableLibraryName was
assembly, exerciseCourse was course,
exerciseRelatedDiet was diet,
incentiveCompensation was incentives,
includedDataCatalog was catalog,
isAccessibleForFree was free, jobBenefits was
benefits, runtimePlatform was runtime,
serviceArea was area, serviceOutput was produces,
softwareRequirements was requirements,
targetCollection was collection.
Site improvements
 Issue #429: Implementation of new extension
system.
510 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
 Issue #6: Improved 404 handler for missing pages,
with support for old-style“/person/minister”
extension URLs and action-related“/query-input”
pseudo-properties.
 Issue #318: Added anexperimental JSON(-LD)
view of the hierarchy. This combines D3 with
RDF schema. Thanks to Gregg Kellogg and
Sandro Hawke for collaboration.
 Various behind-the-scenes improvement to the
site software.
Quick fixes and examples
 Issue #119: Added a link to GS1's page giving
background information on
/globalLocationNumber.
 Issue #471: Added a JSON example for
exampleOfWork and workExample.
 Issue #131: Amended category to be applicable to
product
 Issue #8: Fixed description of box to follow the
original rNews definition (instead of accidental
copy of polygon). Added explanatory text to
GeoShape regarding commas/whitespace.
 Issue #224: Changed expected value of
openingHours to be text rather than duration,
since latter is for ISO formats not our custom
micro-syntax.
 Issue #112: Clarified that upvoteCount and
downvoteCount apply to questions, answers and
comments (rather than just to questions).
 Issue #103: Clarified description of
StructuredValue.
 Issue #333: Clarified description of
BreadcrumbList.
 Issue #456: Generalized numberOfEmployees, to
apply to organization as well as to
BusinessAudience.
 Issue #439: Clarified numberOfItems with multi-
page pagination.
 Fixed the mapping from DataCatalog to
dcat:Catalog
 Issue #341: Amended programmingLanguage to
expect a language rather than a thing.
 Issue #365: Extended award for use on
organization, product.
 Issue #145: Marked serviceAudience as
supersededBy the more general audience property.
 Issue #165: Renamed ingredients to
recipeIngredient, improved the description, and
added ItemList as a possible value for
recipeInstructions.
 Issue #171: Removed class as a value of query
property.
 Issue #183: Comment property now applicable to
an RsvpAction, and can have comment as values.
 Issue #193: aggregateRating and review properties
are now expected on brand, event, service.
(Continues)
ILIADIS ET AL. 511
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
 Issue #247: We now write“antonym” instead of
the incorrect“antagonym” in several action
definitions.
 Issue #316: Marked warrantyPromise as
supersededBy warranty.
 Issue #213: Amended eligibleRegion and
ineligibleRegion to have the same associated
types.
 Issue #315: Updated BroadcastService, marking it
as a kind of service rather than just thing.
 Issue #426: Broadened supersededBy to be usable
with classes and enumerations.
 Issue #366: Reworded description of publication to
use “item” instead of a list of types (which had
omitted book), and marked it as applicable to
CreativeWork.
 Issue #288: Added properties related to boarding
passes to FlightReservation.
 Issue #329: Expanded BroadcastService and added
new types CableOrSatelliteService,
BroadcastChannel, TelevisionChannel, and
RadioChannel to support TV/radio schedules.
Thanks, Yves Raimond for careful review.
 Issue #335: Added gameLocation to
VideoGameSeries.
 Issue #336: Added actor and director to series.
 Issue #364: Replaced non-existent award type with
book in WinAction type. Thanks, unor.
 Issue #386: Fixed extra spaces in labels.
See also issue list for this release.
1.93 (sdo-stantz;
February 4, 2015)
Lots of bugfixes and small improvements, plus new
terms to describe visual artworks and invoices.
Vocabulary
 Added VisualArtwork type and supporting
properties— artEdition, artform, material, surface.
Thanks, Paul Watson.
 Added an invoice type to represent invoices/bills,
with additional properties totalPaymentDue,
minimumPaymentDue, accountId,
scheduledPaymentDate, billingPeriod,
paymentStatus, referencesOrder.
 Fix to allow offers on AggregateOffer. Thanks,
Simon Spero, Zinebb.
 Expanded the list of types that musicBy applies to,
matching those of actor and director. Thanks,
Simon Spero.
 Adding priceSpecification to TradeAction type,
fixing #305.
 Adding deliveryMethod to OrderAction type,
fixing #306.
 Adjusted description of width, height and depth
properties to be“the ___ of the item,” rather than
list specific types.
Site improvements
 Added support for linking to #examples within
per-term pages. Thanks, Wes turner.
 Add rangeIncludes to RDFa markup missing from
property pages. Thanks, John Walker.
512 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
Quick fixes and examples
 Fixes to several examples, thanks to Gregg
Kellogg.
 Fixes to book example, thanks to unor.
 Added name property in CreativeWork examples;
improved MedicalScholarlyArticle example,
marking up the abstract using description—
thanks to Dan Scott.
 Corrected a case typo in numberOfEmployees.
Thanks, Stéphane Corlosquet.
 Fixed mistaken use of“MovieGameSeries”;
reported by both Gregg and Simon.
 Fixed valuePattern definition; it takes text values,
not number. Thanks, Holger.
 Fixed definitions for fromLocation, toLocation;
they do not support numeric values. Thanks,
Simon Spero.
 Fixed producer property; it takes an organization
value, rather than applying to organizations.
Thanks, unor.
 Fixed typo: clinicalPharmacology is supersededBy
clinicalPharmacology. Thanks, Marc.
 Fixed an example that used“address” instead of
PostalAddress. Thanks, unor.
 Added 100+ periods/full stops (“.”) to end each
definition.
See also issue list for this release.
1.92 (sdo-venkman;
December 11, 2014)
ItemList and BreadcrumbList changes; sports-related
improvements; added a music vocabulary; video
games. Also weight/height on person; control and
RSVP actions; role names; dated monetary values.
Vocabulary
 Updated ItemList to allow for richer kinds of lists
(including ordering), rather than just strings;
added BreadcrumbList
 The weight and height properties can now be with
the person type. Added netWorth to person.
Added EmployeeRole.
 Added SportsOrganization as a super-type of
SportsTeam, representingsports organizations,
including sports teams, governing bodies, and sports
associations. Added a sport property to indicate
the associated sport(s) for a SportsOrganization;
also added coach and athlete properties. Added
numberedPosition property to OrganizationRole.
Added homeTeam and awayTeam properties to
SportsEvent, alongside a super-property of those,
competitor.
 Added a VideoGame type with two super-types:
SoftwareApplication and a new game type. We
anticipate a need for future work around game,
see issue #169. VideoGame has cheatCode,
gameServer, gamePlatform, playMode and
gameTip properties, plus a few supporting types. A
property softwareHelp has also been added to
SoftwareApplication to indicate supporting
documentation.
 While integrating VideoGame an issue was raised
around the need to describe series of games. As a
result we have made some changes to the series
(Continues)
ILIADIS ET AL. 513
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
type, which previously emphasized only TV and
radio series: Added VideoGameSeries, BookSeries,
and MovieSeries. The recently added periodical
type is also now modeled as a series subtype. Some
redundant type/property associations were also
tidied up. The existing trailer property can now be
used with VideoGame and VideoGameSeries.
 Added ControlAction (previously proposed as
OperateAction). Add expectsAcceptanceOf on
ConsumeAction (previously proposed as
“contingentOnOffer”). Added ineligibleRegion (on
offer, previously proposed as
“notAvailableAtOrFrom”).
 Add rsvpResponse, additionalNumberOfGuests
properties to the existing RsvpAction type (see also
github issue and details). This change also adds an
enumeration RsvpResponseType:
RsvpResponseYes, RsvpResponseNo,
RsvpResponseMaybe. Finally, we add a new
possible ActionStatusType: FailedActionStatus,
alongside an error property linking an action to
more information on the cause of the failure.
 Add roleName to role, superceding namedPosition
(see also issue and details).
 Add to MusicAlbum properties:
albumProductionType, albumReleaseType,
albumRelease (and inverse, releaseOf). Supporting
enumerated types: MusicAlbumProductionType
(CompilationAlbum, DemoAlbum, DJMixAlbum,
LiveAlbum, MixtapeAlbum, RemixAlbum,
SoundtrackAlbum, SpokenWordAlbum,
StudioAlbum). MusicAlbumReleaseType
(AlbumRelease, BroadcastRelease, EPRelease,
SingleRelease). Add new types: MusicRelease,
MusicComposition, the latter with properties
musicArrangement, composer, firstPerformance,
includedComposition, iswcCode, lyricist,
musicCompositionForm, musicalKey, recordedAs
(inverse: recordingOf). Expand track to allow
ItemList values, for lists of MusicRecording, and
genre to apply to MusicGroup.
 Broadened the description of logo property, to
match the types it applies to. See also github issue
and details.
 Added a DatedMoneySpecification type for non-
price monetary values, by analogy with
PriceSpecification and its subtypes. Added amount
and currency properties and tweaked startDate
and endDate property definitions to fit.
 See also blog post…
Site improvements
 Added links to supporting blog posts for role,
action and periodical.
 Added “alt” attributes to all image examples.
 Fixed the full hierarchy page.
514 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
Quick fixes and examples
 Several minor bugfixes.
See also issue list for this release.
1.91 (September 12,
2014)
Offer/price documentation fixes, cleanup and
community contributions.
 Updated text of the price property to include
practical usage guidance, alongside links to
information from GS1 to the gtin-related offer
properties.
 Updated all our examples to follow that guidance;
primarily by using priceCurrency and the
content = attribute.
 Noted our thanks to the OpenDomain project for
our domain name.
 Updated the text of the“image” property to match
its expected types. Thanks, Dan Scott.
 Changed spelling of“supercededBy” to the more
conventional supersededBy. Thanks, Sachini
Aparna Herath.
 Noted that“logo” and “photo” are sub-properties
of “image.” Thanks, Sachini Aparna Herath,
again.
 Fixed two syntax errors in examples (store
opening hours RDFa; book, PublicationVolume
microdata). Thanks, Gregg Kellogg.
 Added Tolkien-based examples for
exampleOfWork/workExample. Thanks, Dan
Scott, again.
 Fixed a bug with our UTF-8 support. Thanks,
Richard Wallis.
1.9 (August 18, 2014) Bibliographic improvements (periodical and more)
alongside seller/broker/provider clarifications.
Several bibliographic improvements, thanks to the
work of the W3C BibExtend community group.
Improved handling of periodicals, articles and
multi-volume works, introducing types and
supporting properties for periodical,
PublicationVolume and PublicationIssue. Adds
new article properties: pageStart, pageEnd and
pagination. CreativeWork gains a convenience
inverse of isPartOf called hasPart, as well as a new
pair of inverses, workExample and
exampleOfWork that link specific and general
perspectives on creative works. Many thanks to all
the BibExtend group members, to Richard Wallis
for chairing, and to Dan Scott for implementing.
Provider/seller vocabulary: This update also clarifies
how to use a set of related terms, integrating
sections of
schema.org that had developed
separately. Full details are documented at W3C
and in Github, alongside an overview document.
The provider property describes a service provider,
service operator, or service performer, while seller
describe the entities which sell or offer a service on
behalf of an actual service provider. We introduce
a more general broker property (replacing the over-
specific bookingAgent), as well as deprecating
vendor and merchant in favor of seller. Regarding
flights and parcel delivery, carrier is superseded by
provider. Please also note that flightNumber
(Continues)
ILIADIS ET AL. 515
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
should now be written in full (i.e.,“UA110” rather
than just“110”). See the supporting documents for
details.
Finally, episodeNumber, seasonNumber and
clipNumber (for TV/radio) have been harmonized
with the periodicals design (issueNumber and
volumeNumber). In each case, both integer and
text values are anticipated. A common
superproperty, position can also be used. This
reflects implementation experience and establishes
a model that can be applied elsewhere, for
example, ongoing work on describing music.
This update also improves the display and navigation
of supersededBy relations between
schema.org
properties (e.g., see seller).
The terms of service document was also updated to
note that Yandex is now aschema.org sponsor and
to adopt the patent terms used by W3C.
(announcement)
1.8 (July 28, 2014) Added WebSite type; broadened isPartOf property. Added a new CreativeWork type, WebSite: “A
WebSite is a set of related web pages and other
items typically served from a single web domain
and accessible via URLs.” also adopts the
suggestion made by the BibExtend group and other
collaborators, to broaden the isPartOf property,
which now relates any CreativeWork to any other
CreativeWork. This release also makes the
potential actions documentation available in
HTML. Several markup fixes from Stéphane
Corlosquet, alongside improvements to the
consistency of encoding/associatedMedia property
definitions thanks to Dan Scott. (announcement)
1.7 (July 8, 2014) Allows image with ImageObject; adds event
organizers, map improvements.
This release amends the image property, noting that
ImageObject is a reasonable value. It also adds an
organizer property to event. Changes around map:
We add and prefer a“hasMap” property which
supersedes the older“map” property, and we add a
mapType property which comes with some
enumerated values: ParkingMap, SeatingMap,
TransitMap, VenueMap. A map might be (but need
not be) also an ImageObject. (announcement)
1.6 (June 16, 2014) Roles, various fixes, site navigation improvements. This release introduced the notion of a role type to
schema.org. See the blog post for details. The role
mechanism applies across all ofschema.org, and
allows simple statements to be elaborated or
qualified, for example with temporal information.
Other changes in this release include the addition
of a license property, and some documentation of
properties used internally by
schema.org's
documentation system (property, class,
supersededBy, inverseOf). Fixed an embarrassing
typo— “dead”— in the diet property— thanks, Dan
Scott. Various other small changes— listed in the
preview announcement (announcement and
candidate release).
516 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
1.5 (May 27, 2014) Tweaks and fixes. Tweaks to definition of “keywords” to indicate that
comma-separated entries are expected. Several typo
fixes from Stéphane Corlosquet. Adds a new
icaoCode text-valued property for airport. Updated
description for flightNumber to note“not including
the airline IATA code.” Added missing actions-
related definitions (urlTemplate, valueName).
(announcement)
1.4 (May 16, 2014) Examples, examples, examples. Added two examples to accompany workPerformed.
Added several local business, company contact and
music event examples. Several glitch and typo fixes
including MedicalEnumeration, thanks to Dan
Scott. Announcement blog post
1.3 (May 1, 2014) Added workPerformed. Added workPerformed, a relationship between an
event and a CreativeWork that is performed at the
event.
1.2 (April 16, 2014) Potential actions. Introduces vocabulary that enables websites to
describe the actions they enable and how these
actions can be invoked. (announcement and blog
post)
1.1 (May 4, 2014) Reservations, Q/A and more. Added a reservation schema. Question/answer sites.
Order changes. Added EmailMessage.
(1) this release of
schema.org adds a finalized
reservations schema, which refines earlier
proposals discussed in the web schemas
community over the last year. See wiki for details.
The reservations vocabulary includes: Reservation,
ReservationPackage, ReservationStatusType, ticket,
flight, EventReservation, FlightReservation,
TrainReservation, BusReservation,
TaxiReservation, LodgingReservation,
RentalCarReservation, ProgramMembership, seat,
vehicle, airline, FoodEstablishmentReservation,
TrainTrip, car, BusTrip, taxi.
(2) Q/A sites
A simple vocabulary for question/answer and FAQ
sites. It adds types for question, answer, and
QAPage.
(3) adds a type EmailMessage, analogous to the
existing WebPage type.
(candidate release drafted as“1.0 g”; not formally
announced but included in the change to github-
based publishing)
1.0f (February 5, 2014) Not-for-profit offer and other fixes. This version adapts the wording around the offer
type to suit non-profit scenarios, such as libraries.
Thanks to Dan Scott and the BibExtend group for
these proposals. This change broadens the
definition of offer and makes associated changes to
ItemAvailability and OfferItemCondition, typically
rewording “the item for sale” to simply say“the
item.” The itemOffered property is now defined
more appropriately as“the item being offered.”
rather than“… Sold.” The “seller” property is now
defined as“the organization or person making the
(Continues)
ILIADIS ET AL. 517
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
offer,” a compromise to support its use for more
kinds of offer. (candidate release and
announcement)
1.0e (December 4,
2013)
Accessibility properties and order type. This release includes a schema for describing orders,
as well as the accessibility properties for
CreativeWork (see discussion). The W3C
WebSchemas wiki has the order proposal and draft
schema. For accessibility, see the blog post for
more background on the collaborations involved.
See also wiki materials and the draft schema.
(announcement)
1.0d (November 21,
2013)
TV/radio; civic services; ContactPoint event and
organization improvements.
TV/radio improvements in collaboration with BBC
and EBU— see guest blog post by Yves Raimond.
For example see TVEpisode.
For background see the TV/radio wiki entry.
Civic services (which includes ContactPoint) was
blogged when first discussed. See also wiki entry.
Example type: GovernmentService.
Event improvements: Wiki entry. Organization
improvements: Wiki entry. In particular, this
update added department, and subOrganization
properties.
(blog announcement).
1.0c (August 7, 2013) Actions (in the past). Introduced a (past-tense) actions vocabulary (see
wiki) this updated added an action type,
supporting properties, and a substantial set of
subtypes. It was followed in 2014 by a mechanism
for describing potential actions. (announcement)
1.0b (July 24, 2013) Added sameAs; broadened citation. Adds sameAs property to thing that makes it easier
to indicate identifying URLs for entities being
described (wiki). The citation property has been
moved up to CreativeWork, from
MedicalScholarlyArticle (wiki). Thanks to the
BibExtend group for suggesting this small but
useful improvement.
(announced)
1.0a (April 5, 2013) Adds LRMI, datasets, audience, technical publishing
vocabulary and more.
For LRMI (learning resource metadata initiative), a
collaboration co-led by Association of Educational
Publishers (AEP) and creative commons: Added
several properties, mainly to CreativeWork. Added
AlignmentObject type, for aligning content to
educational coding schemes. (see wiki).
Added dataset type (collaboration building upon
work at W3C and elsewhere). See also blog, wiki.
Added audience and related types, useful for LRMI
and other applications (wiki).
Added technical publishing vocabulary: TechArticle,
APIReference, code. See also early blog post and
wiki entries for TechArticleSchema,
APIReferenceSchema and CodeSchema.
(announcement)
0.99 (November 8,
2012)
Added good relations e-commerce vocabulary. Added substantial e-commerce vocabulary based on
good relations; re-engineered site to accept RDFa/
518 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A1 (Continued)
Release Overview Description
RDFS schema definitions from community.(wiki)
(announcement blog post and email from Martin
Hepp)
0.98 (October 18, 2012) Fix for requiresSubscription property. A minor bugfix release, which improved the
documentation of requiresSubscription property.
We now encourage its Boolean value to be
represented as true/false rather than yes/no.
0.97 (July 26, 2012) Added DateTime, time datatypes. Added two datatypes in preparation for good
relations integration. (announcement)
0.96 (July 18, 2012) Added additionalType property. Added additionalType property (wiki). “An
additional type for the item, typically used for
adding more specific types from external
vocabularies in microdata syntax. This is a
relationship between something and a class that
the thing is in. In RDFa syntax, it is better to use
the native RDFa syntax— the “typeof” attribute—
for multiple types.
Schema.org tools may have only
weaker understanding of extra types, in particular
those defined externally.” (announcement)
0.95 (June 26, 2012) Added medical/health vocabulary. This release added substantial vocabulary in the
medical/health domain (around 100 classes, 200
properties). The additions are mainly organized
beneath the MedicalEntity type. An overview
document is also provided. From the blog post:
“This collaborative project drew upon search
expertise from the
schema.org partners but also
gained immeasurably through feedback from
expert reviewers including the US NCBI;
physicians at Harvard, Duke and other institutions,
as well as from several health web sites.
Contributions from the W3C healthcare and
Lifesciences group and web schemas community
also helped bridge the complex worlds of web
standards, search and medicine/healthcare.”
(announcement)
0.91 (April 21, 2012) Removed plural “s” suffix from repeatable properties;
added comment type, SoftwareApplication
vocabulary.
Added new properties per Singularity proposal: 23
changes: actor, album, attendee, award, blogPost,
colleague, contactPoint, employee, encoding,
episode, event, founder, map, member, parent,
performer, photo, review, season, sibling,
significantLink, subEvent, track. Each of these
originally had a plural“s” to indicate repeatability.
After discussion in the W3C WebSchemas group,
the consensus was that this was confusing and
worthwhile changing.
This revision added a new type,“Comment,” whose
super-type is CreativeWork (wiki)
Also adds SoftwareApplication and supporting
vocabulary (wiki, original proposal), including
MobileApplication, WebApplication subtypes.
Converged URL/Url spelling. After WebSchemas
discussion, consensus was: For each of embedURL,
contentURL, downloadURL, ensure there is an
equivalent property named with mixed-case:
“embedUrl,”“ contentUrl,”“ downloadUrl.”
ILIADIS ET AL. 519
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A2 Alphabetical list of vocabulary terns inSchema.org release history as of May 11, 2022
A
acceptedAnswer, accessibilityHazard, accessibilitySummary, accessMode, accessModeSufficient, accommodationCategory,
accommodationFloorPlan, accomodation, accountId, accountMinimumInflow, accountOverdraftLimit, acquireLicensePage,
actionableFeedbackPolicy, ActionAccessSpecification, actionApplication, actionOption, actionPlatform, ActionStatusType,
ActivationFee, additionalNumberOfGuests, additionalProperty, additionalType, addressCountry, addressLocality, addressRegion,
AdministrativeArea, AdvertiserContentArticle, AggregateOffer, AggregateRating, albumProductionType, albumRelease,
albumReleaseType, AlignmentObject, alignmentType, AllergiesHealthAspect, alternateName, alumniOf, amenityFeature, AmpStory,
AMRadioChannel, AnalysisNewsArticle, announcementLocation, ApartmentComplex, APIReference, APIReferenceSchema,
applicantLocationRequirements, applicationContact, applicationDeadline, applicationStartDate, ArchiveComponent, archivedAt,
archiveHeld, ArchiveOrganization, areaServed, arrivalBoatTerminal, artEdition, artMedium, artworkSurface, AskAction,
AskPublicNewsArticle, associatedClaimReview, associatedDisease, associatedMedia, associatedMediaReview, associatedReview,
associated, AudiobookFormat, AudioObject, AudioObjectSnapshot, AuthenticContent, availableAtOrFrom, availableLanguage,
availableOnDevice, awayTeam
B
BackgroundNewsArticle, BackOrder, bankAccountType, bccRecipient, BedType, beneficiaryBank, BibExtend, billingDuration,
billingPeriod, billingStart, BioChemEntity, bioChemInteraction, bioChemSimilarity, biologicalRole, Bioschemas, blogPost,
BlogPosting, BoatReservation, BoatTerminal, BoatTrip, BodyMeasurementTypeEnumeration, BookFormatType, bookingAgent,
BookSeries, boolean, branchCode, branchOf, BreadcrumbList, breastfeedingWarning, BroadcastChannel, BroadcastEvent,
broadcastFrequency, BroadcastFrequencySpecification, broadcastFrequencyValue, broadcastOfEvent, BroadcastRelease,
BroadcastService, broadcastSignalModulation, broadcastSubChannel, broadcastTimezone, brokenlinkcheck, BrokerageAccount,
BusinessAudience, businessFunction, BusReservation, BusTrip, byArtist, byDay, byMonth, byMonthDay, byMonthWeek
C
CableOrSatelliteService, callSign, CampingPitch, cashBack, CategoryCode, CategoryCodeSet, CatholicChurch, ccRecipient, cheatCode,
checkinTime, checkoutTime, chemicalComposition, chemicalRole, ChemicalSubstance, childTaxon, CivicStructure, claimInterpreter,
ClaimReview, claimReviewed, CleaningFee, clinicalPharmacology, clipNumber, codeSampleType, CodeSchema, codeValue,
collectionSize, CommentAction, CommentPermission, commentTime, compatability, competencyRequired, CompilationAlbum,
CompleteDateFeed, CompoundPriceSpecification, ComputerLanguage, ConsumeAction, contactlessPayment, ContactPoint,
containedDataCatalog, containedIn, containedInPlace, containsPlace, containsSeason, contentLocation, contentRating,
contentReferenceTime, contentURL, contingentOnOffer, ControlAction, cookTime, copyrightNotice, Corlosquet, CorrectionComment,
correctionsPolicy, countryOfAssembly, countryOfLastProcessing, countryOfOrigin, courseCode, courseCredits, courseCreditsUnit,
CourseInstance, courseMode, coursePrerequisites, courseWorkload, CreativeWork, CreativeWorks, CreativeWorkSeason,
CreativeWorkSeries, credentialCategory, CreditCard, creditText, CriticReview, cssSelector, currenciesAccepted, currentExchangeRate,
customerRemorseReturnFees, customerRemorseReturnLabelSource, customerRemorseReturnShippingFeesAmount
D
DataCatalog, DataDownload, DataFeed, DataFeedItem, datamodel, datasetTimeInterval, DataType, DataType-related, DataTypes,
DatedMoneySpecification datePosted, datePublished, DateTime, dcat, dcterms, dds, DefinedRegion, DefinedTerm,
DefinitiveLegalValue, deliveryLeadTime, DeliveryMethod deliveryTime, DemoAlbum, departureBoatTerminal, DigitalDocument,
DigitalDocumentPermission, DigitalDocumentPermissionType, directApply, disambiguatingDescription, discountCurrency,
DiscussionForumPosting, DistanceFee, diversityPolicy, diversityStaffingReport, DJMixAlbum, DModel, doesNotShip, domainIncludes,
domiciledMortgage, downloadURL, Downpayment, downvoteCount
E
earlyPrepaymentPenalty, editEIDR, educationalAlignment, EducationalAudience, educationalCredentialAwarded,
educationalFramework, educationalLevel, EducationalOccupationalCredential, EducationalOccupationalCredentials,
EducationalOccupationalProgram, EducationalOrganization, educationalProgramMode, educationalRole, educationalUse,
EducationEvents, educationRequirements, eduQuestionType, EffectivenessHealthAspect, ElectronicsStore, eligibleRegion,
EmailMessage, embeddedTextCaption, embedURL, emphasised, EmployeeRole, EmployerAggregateRating, employerOverview,
EmployerReview, employmentUnit, encodesBioChemEntity, encodesCreativeWork, encodingFormat, endDate, endOffset,
EndorsementRating, endTime, EnergyConsumptionDetails, EnergyEfficiencyEnumeration, energyEfficiencyScaleMax,
energyEfficiencyScaleMin, EnergyStarEnergyEfficiencyEnumeration, EngineSpecification, EntryPoint, eocred-schema,
episodeNumber, EPRelease, equivalentProperty, estimatedCost, estimatedSalary, ETag, ethicsPolicy, EUEnergyEfficiencyEnumeration,
eventAttendanceMode, EventMovedOnline, EventReservation, eventSchedule, EventSeries, eventStatus, EvidenceLevelA,
exampleOfWork, exceptDate, ExchangeRateSpecification, exchangeRateSpread, executableLibraryName, exerciseCourse, ExercisePlan,
exerciseRelatedDiet, ExhibitionEvent, expectsAcceptanceOf, experienceInPlaceOfEducation, experienceRequirements
520 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A2 (Continued)
F
FailedActionStatus, FAQPage, favour, fileFormat, filetree, financialAidEligible, firstPerformance, flightNumber, FlightReservation,
floorLevel, floorLimit, FloorPlan, floorSize, FMRadioChannel, FoodEstablishment, FoodEstablishmentReservation, fromLocation,
fuelConsumption, fuelEfficiency, FundingAgency, FundingScheme
G
gameLocation, gamePlatform, gameServer, gameTip, generalised, GeoCircle, geoContains, GeoCoordinates, geoCoveredBy, geoCovers,
geoCrosses, geoDisjoint, geoEquals, geoIntersects, geoMidpoint, geoOverlaps, geoRadius, GeoShape, GeospatialGeometry,
geospatiallyXyz, Geotic, geoTouches, geoWithin, geoXyz, GettingAccessHealthAspect, globalLocationNumber, GoodRelations,
governmentBenefitsInfo, GovernmentBenefitsType, GovernmentService, gracePeriod, grantsCredential
H
hasBioChemEntityPart, hasBioPolymerSequence, hasBroadcastChannel, hasCategoryCode, hasCourse, hasCourseInstance,
hasCredential, hasDefinedTerm, hasDigitalDocumentPermission, hasEnergyConsumptionDetails, hasEnergyEfficiencyCategory,
hasHealthAspect, hasMap, hasMeasurement, hasMenu, hasMenuItem, hasMenuSection, hasMerchantReturnPolicy,
hasMolecularFunction, hasOccupation, hasPart, hasRepresentation, hasVariant, HealthAspectEnumeration, healthCondition,
HealthInsurancePlan, HealthTopicContent, highPrice, holdingArchive, HomeAndConstructionBusiness, homeLocation, homeTeam,
hoursAvailable, HowItWorksHealthAspect, HowOrWhereHealthAspect, HowTo, HowToItem, HowToSection, HowToStep,
HowToSupply, HowToTool, HyperToc, HyperTocEntry
I
icaoCode, ImageGallery, ImageObject, ImageObjectSnapshot, incentiveCompensation, inChI, inChIKey, includedComposition,
includedDataCatalog, includedInDataCatalog, includesObject, inCodeSet, ineligibleRegion, IngredientsHealthAspect, inLanguage,
inLanguage’, inProductGroupWithID, InteractionCounter, interactionStatistic, interpretedAsClaim, inverseOf, InvestmentFund,
InvoicePrice, isAccessibleForFree, isBasedOn, isBasedOnUrl, isEncodedByBioChemEntity, isInvolvedInBiologicalProcess,
isLiveBroadcast, isLocatedInSubcellularLocation, isPartOf, isPartOfBioChemEntity, isRelatedTo, isResizable, isSimilarTo,
issueNumber, isVariantOf, iswcCode, ItemAvailability, itemCondition, itemDefectReturnFees, itemDefectReturnLabelSource,
itemDefectReturnShippingFeesAmount, ItemList, itemOffered, itemReviewed, iupacName, Iussue
J
Javascript, jobBenefits, jobLocationType, JobPosting, JobPostings, jobTitle, jsonldcontext
K
knowsAbout, knowsLanguage
L
layoutImage, LearningResource, learningResourceType, leaseLength, LegalForceStatus, LegalService, LegalValueLevel,
legislationIdentifier, legislationJurisdiction, LegislationObject, legislationType, LibrarySystem, linkRelationship, LinkRole, liographic,
ListPrice, LiveAlbum, LiveBlogPosting, loanMortgageMandateAmount, loanPaymentAmount, loanPaymentFrequency,
loanRepaymentForm, loanType, LocalBusiness, localised, locationCreated, LocationFeatureSpecification, LockerDelivery,
LodgingBusiness, LodgingReservation, lowPrice
M
mainEntity, mainEntityOfPage, maintenance, makesOffer, mapType, marginOfError, materialExtent, MathSolver,
maximumAttendeeCapacity, maximumEnrollment, measurementTechnique, MeasurementTypeEnumeration, MediaGallery,
mediaItemAppearance, MediaManipulationRatingEnumeration, MediaObject, MediaReview, MediaReviewItem, MediaSubscription,
MedicalEntity, MedicalEnumeration, MedicalScholarlyArticle, MedicalSpecialty, memberOf, membershipPointsEarned, menuAddOn,
MenuItem, MenuSection, MerchantReturnPolicy, MerchantReturnPolicySeasonalOverride, MinimumAdvertisedPrice,
minimumPaymentDue, MissingContext, missionCoveragePrioritiesPolicy, MixtapeAlbum, MobileApplication, MolecularEntity,
molecularFormula, molecularWeight, MonetaryAmount, MonetaryAmountDistribution, MonetaryGrant, MoneyTransfer,
monoisotopicMolecularWeight, monthlyMinimumRepaymentAmount, monthsOfExperience, MortgageLoan, MovieClip,
MovieGameSeries, MovieSeries, MusicAlbum, MusicAlbumProductionType, MusicAlbumReleaseType, musicalKey,
musicArrangement, musicBy, MusicComposition, musicCompositionForm, MusicGroup, MusicRecording, MusicRelease
N
namedPosition, negativeNotes, netWorth, NewsArticle, NewsMediaOrganization, NiemanLab, noFlashing’, noFlashingHazard’,
noMotionSimulation’, noMotionSimulationHazard’, nonprofitStatus, NonprofitType, noSound, noSoundHazard,
notAvailableAtOrFrom, NoteDigitalDocument, numberedPosition, numberOfAirbags, numberOfAxles, numberOfBathroomsTotal,
numberOfBedrooms, numberOfCredits, numberOfEmployees, numberOfForwardGears, numberOfFullBathrooms, numberOfItems,
numberOfLoanPayments, numberOfRooms
(Continues)
ILIADIS ET AL. 521
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A2 (Continued)
O
occupationalCategory, occupationalCredentialAwarded, OccupationalExperienceRequirements, OccupationalTherapy,
occupationLocation, OfferCatalog, offeredBy, OfferForLease, OfferForPurchase, OfferItemCondition, OfferShippingDetails,
OpenDomain, openingHours, OpeningHoursSpecification, OperateAction, OpinionNewsArticle, OrderAction, orderedItem,
OrderItem, Organisation, OrganizationRole, originalMediaContextDescription, originalMediaLink, ownershipFundingInfo
P
pageEnd, pageStart, ParcelDelivery, ParcelService, parentItem, parentOrganization, parentTaxon, ParkingMap, partOfOrder,
partOfSystem, partOfTrip, paymentAccepted’, PaymentAutomaticallyApplied, PaymentComplete, PaymentDeclined, paymentDue,
paymentDueDate, PaymentPastDue, paymentStatus, PaymentStatusType, performTime, permissionType, permittedUsage,
petsAllowed, phane, playMode, PodcastEpisode, PodcastSeason, PodcastSeries, positiveNotes, PostalAddress, postalCode,
PostalCodeRangeSpecification, potentialAction, potentialUse, PregnancyHealthAspect, PreOrder, PreOrderAction, prepTime, PreSale,
prescriptionStatus, PresentationDigitalDocument, previewUrl, priceComponentType, PriceComponentTypeEnumeration,
priceCurrency, priceCurrency’, PriceSpecification, priceType, PriceTypeEnumeration, ProductCollection, ProductGroup,
productGroupID, ProductReturnPolicy, ProfessionalService, ProfessionalService’, ProgramMembership, programmingLanguage,
programPrerequisites, PronounceableText, PropertyValue, PropertyValueSpecification, providerMobility, providesBroadcastService,
publicAccess, PublicationIssue, PublicationVolume, PublicHolidays, PublicToilet, publishingPrinciples
Q
QAPage, QualitativeValue, QuantitativeValue, QuantitativeValueDistribution
R
RadioBroadcastService, RadioChannel, RadioClip, Raimond, rangeIncludes, ratingExplanation, ratingValue, rdf, RDFa, rdflib, rdfs,
ReadPermission, RealEstateListing, ReceiveAction, recipeIngredient, recipeInstructions, recipeYield, recognizedBy, recordedAs,
recordingOf, recourseLoan, referencesOrder, releaseOf, relevantOccupation, remainingAttendeeCapacity, RemixAlbum,
renegotiableLoan, RentalCarReservation, RepaymentSpecification, repeatCount, repeatFrequency, ReplyAction,
ReportageNewsArticle, reportNumber, requiredQuantity, requiresSubscription, ResearchProject, ReservationPackage,
ReservationStatusType, restockingFee, RestrictedDiet, resultComment, ReturnFeesEnumeration, returnLabelSource,
ReturnLabelSourceEnumeration, returnMethod, ReturnMethodEnumeration, returnPolicyCountry, returnPolicySeasonalOverride,
returnShippingFeesAmount, reviewAspect, reviewBody, ReviewNewsArticle, rNews, roleName, RsvpAction, rsvpResponse,
RsvpResponseMaybe, RsvpResponseNo, RsvpResponseType, RsvpResponseYes, runtimePlatform
S
Sachini, SafetyHealthAspect, salaryUponCompletion, SalePrice, sameAs, sampleType, SatiricalArticle, scheduledPaymentDate,
scheduleTimezone, schemaorg, schemaVersion, SchoolDistrict, ScreeningEvent, sdDatePublished, sdLicense, sdo-callisto, sdo-callisto’,
sdo-deimos, sdo-deimos’, sdo-enceladus, sdo-enceladus’, sdo-ganymede, sdo-ganymede’, sdo-gozer, sdo-makemake, sdo-makemake’,
sdo-phobos, sdo-phobos’, sdo-stantz, sdo-telesto, sdo-telesto’, sdo-venkman, sdopythonapp, sdPublisher, seasonNumber, SeatingMap,
secondaryPrevention, SeekToAction, serviceArea, serviceAudience, serviceOutput, serviceType, sharedContent, SheetMusic,
ShippingDeliveryTime, shippingDestination, shippingDetails, shippingLabel, shippingRate, ShippingRateSettings,
shippingSettingsLink, ShortStory, significantLink, SingleRelease, sizeGroup, SizeGroupEnumeration, sizeproperty, SizeSpecification,
sizeSystem, SizeSystemEnumeration, SkiResort, SKOS, SocialMediaPosting, SoftwareApplication, softwareHelp,
softwareRequirements, SoftwareSourceCode, SolveMathAction, Sopek, SoundtrackAlbum, spatialCoverage, speakable,
SpeakableSpecification, SpeakableSpecification-related, SpecialAnnouncement, specialOpeningHoursSpecification,
spokenByCharacter, SpokenWordAlbum, SportsActivityLocation, SportsEvent, SportsOrganization, SportsTeam,
SpreadsheetDigitalDocument, starRating, startDate, startOffset, startTime, StatisticalPopulation, StatusEnumeration, StructuredValue,
StudioAlbum, subEvent, subjectOf, subOrganization, subproperties, subproperty, subtitleLanguage, subTrip, suggestedAge,
suggestedAnswer, suggestedMeasurement, suitableForDiet, supercededBy’, superceding, superEvent, superproperty, supersededBy,
supportingData
T
targetCollection, targetName, targetUrl, TaxiReservation, TaxiService, taxonomicRange, taxonRank, TechArticle, TechArticleSchema,
TelevisionChannel, TelevisionStation, temporalCoverage, termDuration, termsPerYear, TextDigitalDocument, tickerSymbol, timeOfDay,
timeRequired, timeToComplete, timezone, titleEIDR, tocContinuation, tocEntry, toLocation, toRecipient, totalJobOpenings,
totalPaymentDue, totalPrice, totalTime, tourBookingPage, TouristAttraction, TouristDestination, TouristTrip, touristType,
TradeAction, trainingSalary, TrainReservation, TrainTrip, TransitMap, transitTimeLabel, TravisCI, TVClip, TVEpisode, TVSeason,
TVSeries, typeof, typeof’, typicalAgeRange, typicalCreditsPerTerm,
U
UnitPriceSpecification, unnamedSourcesPolicy, upvoteCount, url-addressable, urlTemplate, usageInfo, usecase, UserComments,
UserInteraction, UserReview
522 ILIADIS ET AL.
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License


TABLE A2 (Continued)
V
validFor, validIn, validThrough, valueName, valuePattern, valueReference, variableMeasured, variablesMeasured, variesBy,
vehicleEngine, VenueMap, verificationFactCheckingPolicy, videoFormat, VideoGallery, VideoGame, VideoGameClip,
VideoGameSeries, VideoObject, VideoObjectSnapshot, VirtualLocation, VisualArtwork, volumeNumber
W
warrantyPromise, WatchAction, WearableMeasurementTypeEnumeration, WearableSizeGroupEnumeration,
WearableSizeSystemEnumeration, WebAPI, WebApplication, WebContent, webFeed, WebPage, WebPageElement, WebPageElement’,
webschemas, WebSite, Wikibase, Wikidata, WinAction, WorkBasedProgram, WorkersUnion, workExample, workLocation,
workPerformed, workPresented, WritePermission
X
Xpath, xpath’
Y
yearBuilt
Z
Zinebb
ILIADIS ET AL. 523
 23301643, 2025, 2, Downloaded from https://asistdl.onlinelibrary.wiley.com/doi/10.1002/asi.24744 by Consorci De Serveis Universitaris De Catalunya, Wiley Online Library on [14/04/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License

```

## Merged notes from duplicate

_Source file:_ `One schema to rule them all_ How Schema.org models the world of search.md`

[[One schema to rule them all How Schema.org models the world of search.pdf]]

[PDF](https://asistdl-onlinelibrary-wiley-com.sire.ub.edu/doi/epdf/10.1002/asi.24744 "ePDF")

## Abstract

Several industry-specific metadata initiatives have historically facilitated structured data modeling for the web in domains such as commerce, publishing, social media, and so forth. The metadata vocabularies produced by these initiatives allow developers to “wrap” information on the web to provide machine-readable signals for search engines, advertisers, and user-facing content on apps and websites, thus assisting with surfacing facts about people, places, and products. A universal iteration of such a project called [Schema.org](http://schema.org/) started in 2011, resulting from a partnership between Google, Microsoft, Yahoo, and Yandex to collaborate on a single structured data model across domains. Yet, few studies have explored the metadata vocabulary terms in this significant web resource. What terms are included, upon what subject domains do they focus, and how does [Schema.org](http://schema.org/) represent knowledge in its conceptual model? This article presents findings from our extraction and analysis of the documented release history and complete hierarchy on [Schema.org](http://schema.org/) 's developer pages. We provide a semantic network visualization of [Schema.org](http://schema.org/), including an analysis of its modularity and domains, and discuss its global significance concerning fact-checking and COVID-19. We end by theorizing [Schema.org](http://schema.org/) as a gatekeeper of data on the web that authors vocabulary that everyday web users encounter in their searches.

## 1 INTRODUCTION

Metadata are central to web and internet processes in that they help organize and structure data (Greenberg, [2005](#asi24744-bib-0032); Iliadis et al., [2021](#asi24744-bib-0044); Mayernik & Acker, [2018](#asi24744-bib-0061); Pomerantz, [2015](#asi24744-bib-0074)). One can merely think about how search engines or online retailers structure information in results, including menus and knowledge panels. Several industry-specific metadata initiatives have historically facilitated structured data modeling for the web in domains such as commerce, publishing, social media, and so forth (Guns, [2013](#asi24744-bib-0034)). The standardized metadata vocabularies produced by these initiatives allow web developers to “wrap” information on the web to provide machine-readable signals for advertisers and user-facing content on apps and websites. Thus, metadata assist with information search and surfacing specific facts about people, places, and products (Acker, [2021](#asi24744-bib-0002)). Where such efforts were once fragmented across industries, today, this landscape is changing with globally coordinated efforts to create a universal structured data model across fields. The implications of such a model have far-reaching consequences concerning the monopolization, centralization, and exploitation of data resources.[<sup>1</sup>](#asi24744-note-0001_9 "Link to note")

One such project, [Schema.org](http://schema.org/), started in 2011 and is the result of a partnership between Google, Microsoft, Yahoo, and Yandex—organizations that are traditionally commercial competitors but decided to collaborate on a single structured data model for the web to benefit their search products (Guha et al., [2016](#asi24744-bib-0033)). Today, millions of websites and applications use the [Schema.org](http://schema.org/) structured data model to assist with information search and retrieval, including news organizations involved in verifying misinformation and fact-checking with structured data (Adair, [2020](#asi24744-bib-0005)). The schema also feeds data to virtual assistant products such as Alexa and Google Assistant which pull structured data from the web to answer queries (Kollar et al., [2018](#asi24744-bib-0054)). Such practices show the benefits of using a single structured data model for the interoperability of web data across sites and applications. Yet, scholars have not adequately attended to the conceptual model of [Schema.org](http://schema.org/) 's metadata vocabulary and its domain coverage (i.e., what topics it includes) relative to its central role in structuring experiences of the web. In its positioning as a global web schema, [Schema.org](http://schema.org/) acts as a conceptual model of the world for search engines. As such, this partnership between internet companies engenders values, goals, and aspirations that have far-reaching consequences beyond searching for pizza delivery or the latest news headline.

One way to interpret [Schema.org](http://schema.org/) is to accept the definition provided on its website. The [Schema.org](http://schema.org/) website states that the project was made “to make it easier for webmasters to provide us with data so that we may better direct users to their sites.” [Schema.org](http://schema.org/) is a self-described “collaborative, community activity with a mission to create, maintain, and promote schemas for structured data on the internet, on web pages, in email messages, and beyond.” The website makes several other distinctions, including that the metadata “hierarchy presented on this site is not intended to be a “global ontology” of the world…it is still the case that [schema.org](http://schema.org/) is not intended as a universal ontology.” The website also states that “applications from Google, Microsoft, Pinterest, Yandex and others already use these vocabularies to power rich, extensible experiences” ([schema.org](http://schema.org/)). Figure [1](#asi24744-fig-0001) shows the beginning of the [Schema.org](http://schema.org/) metadata vocabulary in plain English. Figure [2](#asi24744-fig-0002) represents a metadata vocabulary item using JavaScript Object Notation for Linked Data (JSON-LD) syntax.

![Details are in the caption following the image](https://asistdl-onlinelibrary-wiley-com.sire.ub.edu/cms/asset/7f57aebb-3c19-4cd0-ac0a-c03ba557d74a/asi24744-fig-0001-m.jpg)

FIGURE 1 Open in figure viewer PowerPoint Beginning of the Schema.org metadata vocabulary ( schema.org )

![](https://asistdl-onlinelibrary-wiley-com.sire.ub.edu/cms/asset/48f8d24b-c49d-476b-a0a8-b84dc54c552a/asi24744-fig-0002-m.jpg)

FIGURE 2 Open in figure viewer PowerPoint Example of a metadata vocabulary item represented in JSON-LD ( schema.org )

As infrastructures for facilitating information interoperability, projects such as [Schema.org](http://schema.org/) are a less visible aspect of the web when compared to platforms like Facebook, TikTok, and Google, but information science scholars have long emphasized the necessary and often invisible power of classification standards in information infrastructures (Bowker et al., [2010](#asi24744-bib-0016); Bowker & Star, [1999](#asi24744-bib-0017); Star, [1999](#asi24744-bib-0083)). Recent advancements in structured data modeling, knowledge graphs, and the reach of the internet allow companies to leverage metadata vocabularies and crawl the machine-readable data on the web as if it were a single database of facts and assertions. Such processes allegedly help these companies represent “knowledge” in their products, like the knowledge panels in search engine results and the maps and menus of service applications (Noy, Gao et al., [2019](#asi24744-bib-0067)). Structured data thus increasingly provide underlying semantics and context-control related to content for developers while also “intuitively” helping users find what they are looking for on apps and websites without relying on specific keywords in their searches. For developers, such structured data modeling allows for a faster, dynamic display of information for users. For users, this data modeling allows for dynamic webbing across platforms like Instagram, Amazon, and Netflix, tracking and anticipating their next search or action. Structured data are at once both hidden and increasingly an expectation of responsive personalization design of platforms (Acker & Donovan, [2019](#asi24744-bib-0003)).

Projects like [Schema.org](http://schema.org/) are a kind of comprehensive “crosswalk” intended to avoid the convoluted intersecting of multiple schemas, which can overburden web administrators and create confusion and can even resolve the multiple schemas problem by harmonizing web information through a central structured data project. Yet, as a global structured data model, [Schema.org](http://schema.org/) is a gatekeeper of structured data on the web. The schema authorizes the metadata vocabulary that web administrators and everyday web users encounter in their platforms and applications. Up to now, relatively few critical studies have explored the development and release of the metadata vocabulary terms in this significant web resource. What terms are included, upon what subject domains do they focus, and how does [Schema.org](http://schema.org/) represent knowledge in its conceptual model? This article presents results from our extraction and analysis of the metadata vocabulary's release history and complete hierarchy located on [Schema.org](http://schema.org/) 's developer pages. We provide a semantic network visualization of [Schema.org](http://schema.org/), including an analysis of its modularity and domains, and discuss its global significance concerning fact-checking and coronavirus (COVID-19). We end by theorizing [Schema.org](http://schema.org/) as a gatekeeper of data on the web that authors vocabulary that everyday web users encounter in their searches.

## 2 DEFINING SCHEMA.ORG

Some terminological clarification is needed to understand [Schema.org](http://schema.org/) 's role across the web, given that the term refers to several things at once. [Schema.org](http://schema.org/) is each of the following: (1) a universal metadata vocabulary, (2) an administrative body with people who work for large internet companies, volunteers, and a governance structure, and (3) a website with code examples, release history, and term hierarchy. A final (4) category might be how [Schema.org](http://schema.org/) is applied and operationalized by web administrators and developers “in the wild.” This process is often orthogonal to its creators’ originally intended aims and purposes. Designs such as the conceptual model offered by [Schema.org](http://schema.org/) 's metadata vocabulary are not consistently implemented in the ways that producers anticipate. In what follows, our concern is not with the implementation of [Schema.org](http://schema.org/) across the web in the “real world” (definition 4) but instead with the metadata vocabulary itself (definition 1). We set aside questions of its organization and governance (definition 2) and website (definition 3) for our discussion and conclusion. We acknowledge that there is frequently a disconnect between design and deployment (Iliadis & Pedersen, [2018](#asi24744-bib-0045); Liao & Iliadis, [2021](#asi24744-bib-0055)), especially in the world of metadata where people design models and tools that fail to reach a critical mass of adopters or differ in their implementation (Maron & Feinberg, [2018](#asi24744-bib-1001)). Such disconnects have been theorized as instances of technological de-scription where there are different conceptualizations between creators and potential users (Akrich, [1992](#asi24744-bib-0006)). We thus reserve some of our broader and speculative claims concerning [Schema.org](http://schema.org/) 's role in gatekeeping for our discussion and conclusion, and suggest additional studies that can be carried out either quantitatively with usage data or qualitatively with user studies. Indeed, studies focusing on [Schema.org](http://schema.org/) 's use, adoption, and validation are beginning to appear (Meusel et al., [2015](#asi24744-bib-0063); Paulheim, [2015](#asi24744-bib-0069); Şimşek et al., [2018](#asi24744-bib-0081)). The present work strictly concerns the metadata vocabulary that [Schema.org](http://schema.org/) offers, and merely theorizes the project's more prominent position on the web as a type of gatekeeper.

## 3 LITERATURE REVIEW

### 3.1 Schema.org's role in semantic platformization

Metadata vocabularies like the kind offered by [Schema.org](http://schema.org/) are part of a long history of implementing machine-readable semantics on the internet to enable greater data integration across platforms. Recent studies into the social significance of data integration tools like application programming interfaces (APIs) have shown that such technologies facilitate platformization (Berry et al., [2015](#asi24744-bib-0014); Bucher, [2013](#asi24744-bib-0019)). Platformization has been said to entail the “extension of social media platforms into the rest of the web and their drive to make external web data ‘platform ready’” (Helmond, [2015](#asi24744-bib-0038)). Concurrently, research into digital information infrastructures (such as the structured data offered by [Schema.org](http://schema.org/)) has developed adjacent to these platform-oriented approaches (Bowker et al., [2010](#asi24744-bib-0016); Edwards et al., [2009](#asi24744-bib-0026)) with a subset focusing on online knowledge infrastructures for sharing things like research data (Edwards et al., [2013](#asi24744-bib-0027); Karasti et al., [2016](#asi24744-bib-0052)) and ensuring their long-term preservation (Acker, [2019](#asi24744-bib-0001); Acker & Kriesberg, [2020](#asi24744-bib-0004)). More recently, there have been calls to combine these infrastructure and platform-based frameworks to examine information exchange mechanisms on the web through digital tools for knowledge sharing (Plantin et al., [2016](#asi24744-bib-0071)).

Our paper builds and extends the critical work on these platform and infrastructure studies in what has been referred to as “knowledge as programmable object” (Plantin et al., [2016](#asi24744-bib-0071)) by explicitly focusing on recent advancements in structured data modeling across web platforms. As Bucher ([2012](#asi24744-bib-0018), [2013](#asi24744-bib-0019)) and Helmond ([2015](#asi24744-bib-0038)) show data portability in the context of web platforms requires a certain level of semantic annotation. This semantic interoperability is perhaps one of several defining features of the web, or what has been referred to by computer scientists as the “semantic web” (Antoniou et al., [2012](#asi24744-bib-0010); Szeredi et al., [2014](#asi24744-bib-0085)). Since its inception as a global project reaching back to the beginnings of the web in the early 1990s, semantic web practitioners have privileged the status of metadata for providing fine-grained levels of contextual expressivity needed for machine-readable web data. Now web semantics are commonplace in products like knowledge panels, virtual assistants like Siri and Alexa that rely on Wikidata, and other sources that engage markup in platformized versions of knowledge representation. [Schema.org](http://schema.org/) thus contributes to the increasing semantic platformization of the web by enabling data integration through applications of its metadata vocabulary.

### 3.2 The semantic web

The semantic web is a longstanding internet project focused on an interconnected group of technologies, standards, and methods for improving data interoperability across the web (Calaresu & Shiri, [2015](#asi24744-bib-0020)). [Schema.org](http://schema.org/) is a modern outgrowth of the semantic web project, which was originally initiated by web inventor Sir Tim Berners-Lee through his World Wide Web Consortium (W3C) standards body. W3C produces web standards such as the Resource Description Framework (RDF) (a structured data model standard).[<sup>2</sup>](#asi24744-note-0002_44 "Link to note") The [Schema.org](http://schema.org/) website plainly states that the data model used therein is “derived from RDF Schema” which Berners-Lee's W3C previously published. [Schema.org](http://schema.org/) founders and leadership also have or had close ties to W3C. These people include Dan Brickley, who runs the daily operations for [Schema.org](http://schema.org/) and is on the steering group as Google's representative (Brickley previously developed RDF and semantic web technology at W3C). Ramanathan Guha, also from Google, initiated [Schema.org](http://schema.org/) and is one of its founders (Guha previously co-edited the RDF Schema specification with Brickley). The website further states that “since April 2015, the W3C [Schema.org](http://schema.org/) Community Group is the main forum for collaboration” and that current Chief Operating Officer of W3C Ralph Swick (along with Vint Cerf) “helped establish the relations between [Schema.org](http://schema.org/) and the W3C.” Though [Schema.org](http://schema.org/) has close ties to the W3C it is not an official part of the W3C nor is it considered one of their standards, indicating on their website that [Schema.org](http://schema.org/) is not “a standards body like the W3C.”

Previous studies have discussed the semantic web before the rise of [Schema.org](http://schema.org/), focusing either on historical and philosophical conceptions of the semantic web, on notable standards bodies like the W3C, or public and institutional use of semantic web technologies such as in libraries, governments, and laboratories. Few studies (McCarthy, [2017](#asi24744-bib-0062); Patel-Schneider, [2014](#asi24744-bib-0068)) have attempted to examine [Schema.org](http://schema.org/) from critical or sociological perspectives, and those that do have not commented on the metadata vocabulary of [Schema.org](http://schema.org/), nor have they provided any substantial empirical evidence of [Schema.org](http://schema.org/) 's domain coverage and conceptual model in this era of semantic platformization.

### 3.3 Critical histories of the semantic web

Several studies have critically examined the social history of the semantic web and its ideal of a universal standard semantics for the internet. Guns ([2013](#asi24744-bib-0034)) charts its linguistic and intellectual history and argues that as features present in early web standards, linking and metadata connect the semantic web to early artificial intelligence work involving semantic networks. Adding to this history, Hallo et al. ([2016](#asi24744-bib-0037)) describes the concept of “linked data” (primarily understood as the second “wave” of the semantic web) and examine libraries' attempts to gather and share data on the semantic web to highlight processes for data integration. Following Guns' theoretical concerns, Hallo et al. discuss the linguistic and conceptual ontologies that underscore linked data and consider the more significant societal and practical implications of global shifts in data storage and accessibility.

Other information researchers map the fascinating conceptual “prehistory” of knowledge representation technologies on the web that have shaped and given rise to the semantic web's ontological and individualized underpinnings. Wang ([2019](#asi24744-bib-0087)) maps a conceptual history of domain analysis and knowledge organization on the semantic web, tracing notable scholars in semantics research. Machado et al. ([2018](#asi24744-bib-0057)) provide a historical concept of the semantic web, beginning in the late 1990s, through an examination of the publications of Berners–Lee. The review draws concrete definitions of linked data and related terms, offering an operationalization of web semantics within the context of data and intelligent, automated information systems.

Similarly, Swanson ([2020](#asi24744-bib-0084)) charts the rise of information systems and their role as new social and economic infrastructures which govern daily life for individuals and institutions alike. Reflecting on historical developments in finance, retail automation, and digital commerce over the last several decades, Swanson provides a foundation and context to understand the semantic web and its embeddedness in the everyday lives of web users. Halford et al. ([2013](#asi24744-bib-0036)) also critically examine semantic web tools and technologies and how these both complicate and structure current iterations of knowledge production on the web. Each of the above studies offers portions of semantic web history, underscoring a critical dimension to web semantics that we further take up in this article.

### 3.4 Conceptualizing digital objects

Other studies have attempted to provide a formal definition for semantic “digital objects” in the context of the semantic web, often interrogating data models such as the triples represented in RDF's modeling of subjects, predicates, and objects. Conceptualizing “digital objects” as semantic data, Hui ([2016](#asi24744-bib-0040)) examines how modern-day semantic systems have a social and philosophical lineage. Campbell ([2009](#asi24744-bib-0021)) takes Foucault's historicization of medical classification techniques and practices and applies them to semantic web technologies. The triadic relationship that emerges is posited as helpful in theorizing the semantic web's taxonomic, descriptive, and analytic dimensions, further addressing semantic search systems in creating technological rationality. Greenberg ([2005](#asi24744-bib-0032)) likewise explores how metadata has been operationalized and offers a reconceptualization of metadata schemes and how the human component involved in shaping digital objects poses critical considerations related to how these technologies permeate and govern aspects of social life.

The work of Kallinikos ([2010](#asi24744-bib-0049)) examines digital technologies and the semantics of information objects and how “information is a subset of culture” (p. 4) including “the meaning of information tokens” (p. 10). Kallinikos et al. ([2010](#asi24744-bib-0050), [2013](#asi24744-bib-0051)) discern “digital objects” on the web and their function by further exploring how search engines ultimately shape the way a digital object is located, authenticated, and understood, arguing that these processes are embedded in a fundamentally social context and that, as such, semantic entities that make these processes possible must take some measure of responsibility for them. McCarthy ([2017](#asi24744-bib-0062)) offers one of the first sociological analyses of [Schema.org](http://schema.org/) and the digital objects which structure the modern semantic web, and, subsequently, how knowledge is represented through semantic triples such as those identified in the RDF data model. McCarthy thus examines the “instability” that accompanies the semantic web, which largely remains invisible through search engines, algorithms, and other associated tools.

### 3.5 Political economies of semantic infrastructures

DeNardis ([2009](#asi24744-bib-0023), [2014](#asi24744-bib-0024)) and Russell ([2011](#asi24744-bib-0079), [2014](#asi24744-bib-0080)) detail the governance of internet infrastructure by examining the roles that institutions such as W3C play where information is controlled, manipulated, and eventually commodified by platform companies. At a lower level of abstraction, Edwards et al. ([2011](#asi24744-bib-0028)) offer a reconceptualization of metadata not as an outcome of fixed product search mechanisms but as a fluid and temporal process of collaboration, arguing that the very nature of metadata renders it a signifier of the unfinished and in-progress. Researchers have foregrounded these explicitly political issues related to networked semantics on the web. Waller's ([2016](#asi24744-bib-0086)) and Poirier's ([2017](#asi24744-bib-0072), [2019](#asi24744-bib-0073)) ethnographic studies examine how infrastructures on the semantic web (e.g., taxonomies, schemas, and ontologies) are built and reveal the power dynamics embedded in their creation and use. Beghtol ([2005](#asi24744-bib-0011)) offers a specific set of global actionable solutions for making more ethical decisions when creating and maintaining knowledge representations in information systems, arguing for more thoughtful treatments of institutionally backed systems. Douglas et al. ([2018](#asi24744-bib-0089)) explore the extent to which linked data provides meaningful solutions for decolonizing archival work, arguing that linked data can better represent more complex connections that can be used to include marginalized perspectives in archives.

In line with these ethical and political insights, Ford and Graham ([2016a](#asi24744-bib-0029), [2016b](#asi24744-bib-0030)) examine linked data and how platforms (e.g., Wikipedia and Google, respectively) utilize linked data to depoliticize cultural constructions of place while dismissing alternative voices through digital tools. Srinivasan ([2013](#asi24744-bib-0082)) argues that research and cultural understandings of ontologies are primarily understood through a Eurocentric perspective, asserting this needs to be de-centered for a more culturally diverse set of codes for new media. Others have examined the political contexts where ontologies are used in military, security, and surveillance contexts (Iliadis, [2018](#asi24744-bib-0041); Iliadis, [2019](#asi24744-bib-0042); Iliadis & Acker, [2022](#asi24744-bib-0043)) and in their service operations.

[Schema.org](http://schema.org/) presents itself as a community collaboration between nonprofits, standards organizations, and corporate partners in the service of web administrators and users who will benefit from the structured data model. Yet, as a seemingly general-use structured data model, [Schema.org](http://schema.org/) distances itself from the label of being a global or universal ontology. [Schema.org](http://schema.org/) thus represents a unique opportunity to study the emergence of a worldwide metadata vocabulary that can play a significant moderating role concerning how web data are shared and displayed on major web applications and platforms. As [Schema.org](http://schema.org/) grows and becomes a critical infrastructure in structured data modeling across the web, the terms and vocabularies expressed through its ontology also represent what the organization considers worthy of knowledge representation. With these conceptual models in mind, we ask the following two research questions concerning how [Schema.org](http://schema.org/) grows its metadata vocabulary:

*RQ1*: *Since the beginning of* [Schema.org](http://schema.org/) *'s release history*, *what kinds of terms have been included in the* [Schema.org](http://schema.org/) *metadata vocabulary?*

*RQ2*: *What do the terms in* [Schema.org](http://schema.org/) *'s metadata vocabulary tell us about* [Schema.org](http://schema.org/) *'s domain coverage* (i.e., *the topic areas of focus*)?

## 4 METHODS

We wanted to learn more about the terms in [Schema.org](http://schema.org/) 's metadata vocabulary and the conceptual model that emerges from it; to answer our research questions, we obtained digital materials from the [Schema.org](http://schema.org/) website and developer pages. First, we scraped the documented release history of the [Schema.org](http://schema.org/) updates and manually created a summary of the kinds of vocabulary topics included for discussion in each release.[<sup>3</sup>](#asi24744-note-0003_76 "Link to note") We then processed the text of the complete release history using Wordlist Maker to extract unique terms from the corpus.[<sup>4</sup>](#asi24744-note-0004_77 "Link to note") We removed non-schema-related words and isolated all the schema terms contained in the release history (*n* = 970). The full text of the [Schema.org](http://schema.org/) release history, documented updates, and an alphabetical list of schema terms are available in Tables [A1](#asi24744-tbl-0002 "Link to table") and [A2](#asi24744-tbl-0003 "Link to table").

Once we obtained the release history and distilled the schema terms, we also wanted to represent the complete metadata vocabulary hierarchy in a data visualization to observe what domain clusters appear (i.e., which terms/topics are more central in the metadata vocabulary). To visualize [Schema.org](http://schema.org/) 's ontology in a semantic network, we downloaded two CSV files (Types and Properties) containing the [Schema.org](http://schema.org/) ontology from the [Schema.org](http://schema.org/) developers page and processed them using Gephi (Bastian et al., [2009](#asi24744-bib-0090)).[<sup>5</sup>](#asi24744-note-0005_81 "Link to note") Using Gephi's interaction techniques, we explored the [Schema.org](http://schema.org/) ontology and customized the visualization by expanding the hierarchy to display the nodes (representing vocabulary terms) and edges (representing subTypeOf relationships). After importing the CSV material to Gephi, the ForceAtlas2 layout algorithm was employed to expand the network for an improved visualization (Jacomy et al., [2014](#asi24744-bib-0047)). The nodes were resized according to their degree ranking (min 100 to max 1,500). The network's modularity was calculated using Gephi's statistics tools to observe communities (i.e., clusters of topics) in the metadata vocabulary (Gephi uses the Louvain method for detecting communities in networks described in Blondel et al. \[[2008](#asi24744-bib-0015)\]). All data we collected can be accessed via the [Schema.org](http://schema.org/) links in the footnotes provided in this section (ours was collected as of 05/11/22). The data thus represent [Schema.org](http://schema.org/) 's metadata vocabulary in a “snapshot” or moment in its growth rather than chronologically over time or by future projections.

## 5 ANALYSIS AND FINDINGS

As of this writing, the [Schema.org](http://schema.org/) release history contains 14 significant updates and 53 total updates ranging from release 0.91 (released April 21, 2012) to release 14.0 (released March 17, 2022). [Schema.org](http://schema.org/) 's vocabulary currently consists of 797 Types, 1,453 Properties, 14 Datatypes, 86 Enumerations, and 462 Enumeration members. The semantic network contains 1,387 nodes and 1,344 edges in a directed graph, which we represent in Figure [3](#asi24744-fig-0003). The network's modularity is 0.925, showing that the network is highly clustered in nature, with communities numbering 73 and an average degree of 0.969. Figure [4](#asi24744-fig-0004) shows the size distribution of nodes among each modularity class. A summary of the types of terms included for discussion in each of the releases is in Table [1](#asi24744-tbl-0001 "Link to table"). The average weighted degree is 0.969 (average total of the weights of edges linked to a node) with a diameter of 5 (the maximum distance between nodes in the graph), an average path length of 2.319 (average number of steps from one random node to another), and a density of 0.001 (how many links between nodes exist compared to how many links between nodes are possible).

![](https://asistdl-onlinelibrary-wiley-com.sire.ub.edu/cms/asset/5d240a53-48e9-4b21-82f2-cde4b353d8c6/asi24744-fig-0003-m.jpg)

FIGURE 3 Open in figure viewer PowerPoint Schema.org semantic network visualization

![](https://asistdl-onlinelibrary-wiley-com.sire.ub.edu/cms/asset/3c29c063-3b25-4487-8806-195441d0349f/asi24744-fig-0004-m.jpg)

FIGURE 4 Open in figure viewer PowerPoint Schema.org modularity size distribution

| Release version (date) | Topics addressed in vocabulary |
| --- | --- |
| 14:14 (2022) | Search and rescue; adult oriented goods and services; online businesses; funding |
| 13:13 (2021) | Biology and life science, biochemistry, molecular entities, and chemicals; merchant return policies, return shipping, damaged products, labels, policies; job applications and postings; fact-checking and misinformation including reviews of media and claims; casual opinion claims unrelated to news or factual records; positive and negative reviews; countries of processing and assembly |
| 12:12 (2021) | Ineligible regions; durations of media episodes; structured sizes and measurement; backorders and item availability; health aspects relating to vaccines, health access, allergies, safety, pregnancy; occupational experience and requirements |
| 11:11.0, 11.01 (2020) | Offline and online events; animated stories; prices, invoices, down payments, cleaning fees, billing start/end dates; seeking and actions related to video content; math actions and solutions; learning and educational resources; copyright and credit notices |
| 10:10.0 (2020) | Educational questions, learning resources, and courses; floorplans and layout images; energy efficiency, consumption |
| 9:9.0 (2020) | Learning resources, creative works, and quizzes; product groups and variations; boat reservations and boat trips |
| 8:8.0 (2020) | Non-profit status, organizations, and types; delivery times, shipping destinations, rates and details; citizenship, legal, and visa requirements for job postings |
| 7:7.0, 7.01, 7.02, 7.03, 7.04 (2020) | School districts; special announcements and locations; hospital reporting; hackathons; start and end times for schedules; COVID-19 |
| 6:6.0 (2020) | Media collections such as images, videos, or media galleries; 3D modeling; financial aid and educational occupational programs; job posting features such as security clearance or physical abilities |
| 5:5.0 (2019) | Health aspects; features within web sites, including pages, sites, and site elements; property information related to accommodations and real estate listings such as bathrooms, floor level, and lease length |
| 4:4.0 (2019) | Real estate information, purchase offers and losing information; podcast information related to series, seasons, episodes; sport teams information, including gender of athlete; job opening, employment, and unemployment information |
| 3:3.0, 3.1, 3.2, 3.3, 3.4, 3.5, 3.6, 3.7, 3.8, 3.9 (2016–2019) | Life sciences; lodging and rental information, amenities, check in times; social media posts; recipe information like cook time and preparation time; health warnings for breastfeeding, prescriptions, and health conditions; course information, enrollment, prerequisites; how to directions for structured steps of instructions; claim type and claim review features to support fact checks; legislation; tourism, tourist attractions |
| 2:2.0, 2.1, 2.2 (2015) | Automotive/car properties, engine specifications, fuel/safety features; exercise courses, exercise related diets, health and fitness actions; payment features such as due dates, actions, receipts; geographic place names for different locations (home, work, gym), including radiuses and midpoints between locations |
| 1:1.1, 1.2, 1.3, 1.4, 1.5, 1.6, 1.7, 1.8, 1.91, 1.92, 1.93 (2013–2015) | Audiences, publishers, technical publishing; citations to scholarly sources, creative works, medical articles; actions, potential and in the past; civic services, government services; television and radio content, video games series, episodes, role names; not-for-profit offers, sales, and item conditions for used goods; reservations for meals, hotels, airlines, or trips; question and answer features for questions, answers, facts; work performance, music events, live event announcements; visual arts, editions, forms, materials, surface |
| 0:0.91, 0.95, 0.96, 0.97, 0.98, 0.99 (2012) | Family members; software applications, mobile applications, web applications; medical and health care entities; time and temporality features, timezones |

The 970 unique terms extracted from the release history range across various fields, and some topics appear to be added out of necessity based on current events. There are terms related to content moderation (an evolving concern given the proliferation of material on social media sites that goes against their terms of service, as explained in Gillespie \[[2018](#asi24744-bib-0031)\] and Roberts \[[2019](#asi24744-bib-0078)\]), fact-checking and misinformation (another area of increasing importance given the recent increase in media manipulation and disinformation campaigns online, as explained in Marwick and Lewis \[[2017](#asi24744-bib-0060)\] and Benkler et al. \[[2018](#asi24744-bib-0012)\]), educational activities, and identifying media artifacts, among many others. Other than the topics that appear to be of increasing global concern, there does not seem to be consistent logic concerning the types and kinds of metadata terms discussed and included in the [Schema.org](http://schema.org/) model. Indeed, possible community extensions to [Schema.org](http://schema.org/) vocabulary are proposed and temporarily hosted on a pending ad hoc basis before they are included in the [Schema.org](http://schema.org/) core, as explained on the website.

These schema terms range from simple entities and relationships in which “regular” everyday web users might be interested (such as locating information about employment or education) to more complex instances where specialists and experts would likely be the beneficiaries of the terms. The range of complexity represented in the unique terms contained in the [Schema.org](http://schema.org/) release history indicates [Schema.org](http://schema.org/) 's coverage and possible application areas, spanning several domains and industries. For example, designating actions on the web are described, such as acquiring license pages and applications, providing feedback policies, or giving opinions, all of which can be used by web administrators to surface such actions in search results. More specialized terms related to fact-checking and misinformation labeling are provided through “review of claim” and “review of media” terms which news organizations can use to mark up their news stories and surface warnings in the news feed. Educational programs, credentials, occupations, events, and requirements terms are included for facilitators to boost these data points in their profiles for potential students searching for information.

While the unique terms in the [Schema.org](http://schema.org/) release history point to areas that have recently been under development, [Schema.org](http://schema.org/) 's current core vocabulary shows what might be considered the earliest and seemingly most important domains for the project. For example, our semantic network offers that the high-level representations in the [Schema.org](http://schema.org/) hierarchy include top-level domains for vocabulary items relating to the categories of Person, Organization, Place, CreativeWork, Intangible, Action, MedicalEntity, and Event. The core categories illustrate the datafication of life within several areas, from tech industries to creative work. These top-level domains are relatively abstract and less specific than the lower-level vocabulary items, clearly indicating that from the beginning, [Schema.org](http://schema.org/) was intended to organize its structured data as knowledge across a wide variety of domains.

Details in our semantic network show several features of the [Schema.org](http://schema.org/) core hierarchy, including which hierarchy terms are subclasses of higher-level domain terms and which terms belong to specific clusters of related terms. For example, the CreativeWork category in the network has a high degree of centrality and connects to media texts, production, and consumption entities. Here, creative works are understood as units or types of labor, illustrating a schema's role in shaping normative standards of cultural production and consumption (Craig & Cunningham, [2019](#asi24744-bib-0022); Napoli & Caplan, [2017](#asi24744-bib-0065)). Similarly, the Place categorization privileges locations related to culture, tourism, and commerce (i.e., where people are likely to spend money and leisure time).

The Intangible category hierarchizes purchasing behaviors and commodities, a common theme among all the second-level entities (beyond the top-level entity Thing). Moreover, some items appear far less tangible than others (e.g., the difference between making a reservation, purchasing a ticket, or enumeration). This category includes sub-level items such as Brand, MerchantReturnPolicy, and MediaSubscription. What is notable here is not necessarily how well these items fit within the assigned category but the extent to which each class is defined by purchasing behaviors, cultural commodities, and creative labor. The privileging of creative work and focus on cultural labor made possible through the metadata vocabulary provided illustrates the complex webs of meaning-making within these spheres and the role that [Schema.org](http://schema.org/) plays in legitimizing and making those meanings accessible to the people who use them. We note here that developers themselves use their labor to mark up their content with the vocabulary and thus are also involved in work by giving their labeling labor to search companies. Scholars have researched such uneven labor practices in the context of data workers. Irani ([2013](#asi24744-bib-0046)) has examined unfair labor practices in the context of microworkers involved with Amazon's Mechanical Turk crowdsourcing website, and Posada ([2022](#asi24744-bib-0075)) has similarly examined unjust labor in the context of data annotators.

Several other interesting entities appear in the [Schema.org](http://schema.org/) hierarchy, including ClaimReview, which enables developers to markup news stories with fact-checks, so they appear as such in search results, and terms related to COVID-19, including CovidTestingFacility, SpecialAnnouncement, and eventAttendanceMode.

### 5.1 Fact-checks and misinformation

Since 2016, [Schema.org](http://schema.org/) appears to have released vocabulary to combat conspiracy theories and misinformation on the internet. One term, ClaimReview, enables developers to markup news stories with fact-checks to appear as such in search results. A detail of the cluster to which ClaimReview belongs in our semantic network is represented in Figure [5](#asi24744-fig-0005). Google announced the display of this feature on October 13, 2016. The use of this tool grew in connection to the fake news debates surrounding the 2016 US presidential election (Bing introduced support for fact-checks using ClaimReview on September 14, 2017). ClaimReview positions [Schema.org](http://schema.org/) and Google as critical arbiters of what is credible, leveraging the perception of their widespread legitimacy as a source of information.

![](https://asistdl-onlinelibrary-wiley-com.sire.ub.edu/cms/asset/0a4344d8-82db-4d31-b51e-0e8e958574b0/asi24744-fig-0005-m.jpg)

FIGURE 5 Open in figure viewer PowerPoint Detail of ClaimReview cluster in Schema.org semantic network

Alexios Mantzarlis, the former News and Information Credibility Lead at Google News Lab, writes that “fact-checking initiatives around the world mark up their work with ClaimReview, which allows fact-checkers to signal—and anyone online to automatically detect—that a webpage contains a fact check” (Mantzarlis, [2019](#asi24744-bib-0059)). Google's Fact Check Explorer is a search feature to discover fact-checks, including those that use the ClaimReview markup. Academic researchers are also interested in ClaimReview and are involved in spreading literacy about the feature. The Duke Reporters’ Lab runs the ClaimReview Project initiative that shares information about the fact-check function (Lim, [2019](#asi24744-bib-0056)). A similar project, Full Fact, is a registered charity and consists of “a team of independent fact-checkers and campaigners who find, expose and counter the harm” (see [fullfact.org](http://fullfact.org/)). Facebook and Google fund Full Fact; the charity works for these companies, including Facebook's Third-Party Fact Checking Program and Google's work on COVID-19 fact-checking.

A recent Full Fact guest blog post at [Schema.org](http://schema.org/) about ClaimReview discusses the link to fact-checking (Dudfield & Dodds, [2021](#asi24744-bib-0025)). The post is titled “Enriching ClaimReview for Fact Checkers” and is written by Andrew Dudfield (Head of Automated Fact Checking at Full Fact) and Leigh Dodds (an open data expert). The post states that ClaimReview is one of the “hidden jewels” of the schema hierarchy because of the way it enrolls human fact-checkers. The authors also note that the Full Fact organization has been “exploring ways to revise and extend the claim review metadata to provide more detail that might enable further reuse and labeling of content, and further insights into the fact checking process.” These areas include consolidating the recommendations and examples for implementing the feature Google and Bing have included in their structured data markup documentation pages. Others describe expanding ClaimReview to include further term identifiers and linking, enriching the markup to include claims, information about errors and corrections, and citing evidence.

### 5.2 COVID-19 and data commons

[Schema.org](http://schema.org/) 's vocabulary about COVID-19 is another example of a rapidly growing topic, thanks to recent current world events. In the first 2 months of the pandemic, [Schema.org](http://schema.org/) fast-tracked the approval of terms in the schema hierarchy to assist with information search and retrieval related to the pandemic. The first such release occurred with version 7.0 on March 17, 2020 and included the fast-track release of terms such as CovidTestingFacility, SpecialAnnouncement, and eventAttendanceMode. Material marked up with these terms can appear on Google's Fact Check page for Coronavirus, in Google and Bing knowledge panels, and is available for retrieval by apps and platforms. These schema features populate some of the rich search results that users can see, allowing them to look up information and possibly take action concerning COVID-19. [Schema.org](http://schema.org/) is also helping a National Science Foundation-funded study for a semantic integration platform to fight COVID-19 (Zverina, [2020](#asi24744-bib-0088)). A detail of the cluster to which CovidTestingFacility belongs in our semantic network is represented in Figure [6](#asi24744-fig-0006).

![](https://asistdl-onlinelibrary-wiley-com.sire.ub.edu/cms/asset/5a069e35-0100-46ab-9ce3-84670ca6596e/asi24744-fig-0006-m.jpg)

FIGURE 6 Open in figure viewer PowerPoint Detail of CovidTestingFacility cluster in Schema.org semantic network

Another initiative tied to [Schema.org](http://schema.org/) relevant to accessing structured COVID-19 data is Data Commons, “an open knowledge database of statistical data started in collaboration with the U.S. Census, Bureau of Labor Statistics, World Bank, and many others” (Raghavan, [2020](#asi24744-bib-0076)). This project assists with finding statistics and presenting them in the knowledge panels when searchers look for something like “Covid-19 cases in Philadelphia.” Its website is “an open knowledge repository that combines data from public datasets using mapped common entities. It includes tools to easily explore and analyze data across different datasets without data cleaning or joining.” [Schema.org](http://schema.org/) is one way these data can map to these familiar entities in emissions, health, water, energy, education, employment, income, and other areas. Specifically, the website states that “ [DataCommons.org](http://datacommons.org/) builds upon on the vocabularies defined by [Schema.org](http://schema.org/).” Google officially announced that it was making Data Commons available directly in Google Search and knowledge panels as a new layer of their Knowledge Graph as of 2020. Since Google announced Dataset Search in 2020, it has indexed almost 25 million datasets; it is “a dataset-discovery tool that provides search capabilities over potentially all datasets published on the Web” and draws heavily on [Schema.org](http://schema.org/) (Noy, Burgess et al., [2019](#asi24744-bib-0066)).

## 6 DISCUSSION: A GLOBAL ONTOLOGY FOR WHOM?

As seen in our semantic network, [Schema.org](http://schema.org/) contains several clusters that address emerging topics of key international importance, including fact-checks and COVID-19. Yet, other terms and clusters concern commerce-related topics, such as shopping, vacationing, and cultural work. However, the domain coverage is not limited to these terms and is very broad, which suggests that [Schema.org](http://schema.org/) is indeed a global ontology, or at least aspires to be. Which leads us to ask the following question: a global ontology for whom?

On the one hand, [Schema.org](http://schema.org/) might not be as “global” in its data interoperability as its creators envisioned. For example, ClaimReview might exacerbate problems related to misinformation or provide a false sense of credibility. Things can be labeled “credible” without regard to the validity of the claim; thus, it would be possible for bad actors to fact-check a claim simply by using the metadata vocabulary. Another thing to consider is that many medical terms seem applicable to privatized US healthcare systems, indicating a type of platform nationalism (Jin, [2015](#asi24744-bib-0048)). On the other hand, [Schema.org](http://schema.org/) does seem to be approximating something like a global ontology. In answer to our research questions, we find that the terms included since the beginning of the [Schema.org](http://schema.org/) ontology span a wide variety of domains and that [Schema.org](http://schema.org/) is not a domain-specific ontology. Instead, it aims to crosswalk several domains specific to human actions and published structured data. The top-level domains are reserved for abstract entities under which more specific domain information can be located. The ontology terms, along with the information in the release history and on [Schema.org](http://schema.org/) 's website, tell us that [Schema.org](http://schema.org/) does aspire to become a global ontology (if it is not already). For example, smaller domain-specific structured data initiatives have been “absorbed” since the rise of [Schema.org](http://schema.org/), as their vocabularies became adopted and instantiated in [Schema.org](http://schema.org/) and thus were made redundant. Existing projects developing [Schema.org](http://schema.org/) extensions to connect their work will likely be eclipsed and outdated.

Some benefits come with using structured data like [Schema.org](http://schema.org/). Certain features are directed at using structured data for social good, including vocabulary items relating to providing information about the COVID-19 pandemic. Yet, [Schema.org](http://schema.org/) is a double bind for web developers who are encouraged to use [Schema.org](http://schema.org/) to increase the findability of their content while simultaneously being victims to how search engines present the information. Google's knowledge panels which show structured data are a way of keeping traffic on their search engine. Such practices illustrate the company's attempt to monopolize information as a semantic middle layer that discourages users from visiting primary sources. Knowledge panels that encourage implicit reliance on auto-populated facts (instead of visiting “external” sites) are a significant part of the internet for users today. For example, one study showed that “62 percent of mobile searches in June 2019 were no-click” and that “people ages 13 to 21” are “twice as likely as respondents over 50 to consider their search complete” once they have seen a “knowledge panel” (Kelley, [2019](#asi24744-bib-0053)).

Indeed, [Schema.org](http://schema.org/) 's structured data model has made searching for facts and known sources easier and faster for people using search engines (in the English language). But the model also has embedded sociocultural biases towards privatized and for-profit contexts. Search engines benefit from closed platforms, cookies and user tracking, data collection from searchers, and targeted advertising in results. The result of retrieving sources and facts in a privatized space presents a kind of capitalist realism (Fisher, [2009](#asi24744-bib-0091)) where every search and click has potential value to platforms, data brokers, and corporations underwritten by advertising mechanics. This reality can be laid bare if one examines the political economy of [Schema.org](http://schema.org/) and the influences of its schema governance, particularly how new terms and features are added (and retired) from the structured data model. Most terms in [Schema.org](http://schema.org/) are directed at financially oriented topics relating to logistics, purchasing, traveling, and so forth. Fewer terms focus on areas that might benefit socioeconomically underprivileged groups. For example, as far as we can tell currently, there is no clear information relating to pro bono legal or immigration services (though there are terms for general legal services), shelter information for humans (rather than pets), food drives (instead of fast food which is included), retirement homes (there is information about hotels). There are many other areas where the hierarchy is aimed at those already privileged (tourism, shopping, etc.). One of the larger subclasses is for different types of stores (including outlets, liquor, and pawn).

[Schema.org](http://schema.org/) 's governance, according to our review of its website and email list, is primarily controlled by Google, which might explain the focus on commodities, services, and purchasing (Andrews, [2020a](#asi24744-bib-0008), [2020b](#asi24744-bib-0009)). According to the project's website, it is also unclear the extent to which Microsoft, Yahoo, and Yandex still have personnel affiliated with the project. [Schema.org](http://schema.org/) could be more transparent and forthcoming with its governance structure and describe who benefits from its structured data. Given that [Schema.org](http://schema.org/) seemingly appears like a Google-run property (due to the decreasing participation of other platform companies), what, then, can web developers and administrators do so that they are not merely giving their labor to a giant platform company that will essentially “take” information from their pages to represent in semantic search results? One option might be to initiate similar or adjacent projects focusing on justice and equity, such as multiple languages or social services.

As we argued above, developers must use the schema for their content to appear in search results or risk becoming less visible. Yet, the very nature of the schema means that content from their sites can be displayed in Google's rich search results, including knowledge panels. These practices result in fewer people visiting their sites once people receive the information they need, which is already extracted and presented by Google. In this way, [Schema.org](http://schema.org/) may contribute to Google searches being dominated by Google information and keeping people on its product, thus substantiating claims of Google's knowledge monopoly. Mager ([2012](#asi24744-bib-0058)) describes how capitalist society shapes search engines through the politics of privatization, and we view such practices occuring with Google's influence over the governance of [Schema.org](http://schema.org/). By engineering software that analyses structured metadata that it controls and uses to provide ontological descriptions of the world, companies like Google have designed technological infrastructure that privileges capitalistic conceptualizations of work, labor, news, life, and technology that favor its platforms, while limiting or ignoring alternatives. Through its ability to surface information sources in retrieval, [Schema.org](http://schema.org/) acts as a regulator and gatekeeper controlled by search engines such as Google. Researchers might also set for themselves the task of locating examples of limitations. For example, researchers may surface semantic errors in information retrieval on products like Google's knowledge panels and Alexa's answers which rely on the markup that [Schema.org](http://schema.org/) provides or may conduct studies to see what content areas are omitted. As we have argued elsewhere, researchers concerned with the power of metadata might also examine the implications of standards engineering in private, closed spaces and how that may influence what internet users can see, access, find, and know (Acker, [2019](#asi24744-bib-0001); Acker, [2021](#asi24744-bib-0002); Iliadis & Acker, [2021](#asi24744-bib-0002)).

Lastly, [Schema.org](http://schema.org/) connects to projects like Wikipedia given its ability to present information alongside Wikipedia infoboxes in search results like knowledge panels and virtual assistant responses (Minhaj & Urs, [2021](#asi24744-bib-0064)). Google has specified its preference for [Schema.org](http://schema.org/) markup and has recommended a preference for JSON-LD over other serializations (such as Microdata and RDFa). The emergence of [Schema.org](http://schema.org/) as the de facto metadata vocabulary on the web and JSON-LD as the preferred serialization offer opportunities for researchers to study these new advancements in the industry. For example, how and why were these models and serializations chosen, how have practitioners implemented them across the web, and what opportunities are there for studying their impact in current search and knowledge discovery paradigms?

## 7 CONCLUSION

Semantic infrastructures such as [Schema.org](http://schema.org/) assert what is possible, standard, and appropriate in web search while consolidating the datafication of information in ways that benefit companies and corporations. The [Schema.org](http://schema.org/) partnership represents a critical juncture where tech companies have evolved to govern how representations of labor, information, cultural commodities, and media products as programmable knowledge are understood and accessed on the web through search. In doing so, platform companies have created a hierarchy of what they think people want to know while underscoring these processes with their marketing and cultural logic. Google's close relationship to [Schema.org](http://schema.org/) and its use of structured data in search results also has implications for growing Google's monopoly in the information ecosystem. Further information studies/science research into structured data will make the organizational role of platform companies more transparent, specifically in knowledge management and new media. We encourage scholars to take up a renewed interest in critical search engine studies (Haider & Sundin, [2019](#asi24744-bib-0035); Rieder, [2022](#asi24744-bib-0077)) to see how new gatekeepers and sociocultural biases are created in the semantic “knowledge” that is constructed and imparted to users by large platform companies.

## Endnotes

- <sup>1</sup> In this article, we use the terms “metadata vocabulary” and “structured data” somewhat interchangeably for the sake of readability, with the key distinction that we view all metadata vocabularies as a form of structured data but not all structured data as a form of metadata.
- <sup>2</sup> There is not enough room in this article to explain the complicated history of the semantic web project; interested readers may see Allemang et al., [2020](#asi24744-bib-0007); Berners-Lee et al., [2001](#asi24744-bib-0013); Calaresu et al., 2015; Guns, [2013](#asi24744-bib-0034); Hitzler, [2021](#asi24744-bib-0039); McCarthy, [2017](#asi24744-bib-0062); Szeredi et al., [2014](#asi24744-bib-0085).
- <sup>3</sup> [https://schema.org/docs/releases.html](https://schema.org/docs/releases.html).
- <sup>4</sup> [https://design215.com/toolbox/wordlist.php](https://design215.com/toolbox/wordlist.php).
- <sup>5</sup> [https://schema.org/docs/developers.html](https://schema.org/docs/developers.html).

## APPENDIX

| Release                               | Overview                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| ------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 14.0 (March 17, 2022)                 | Version 14.0—this release includes improvements proposed via the pending section, including additions around audience restrictions for eCommerce.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | **Vocabulary**  *Changes in Core section*:  - Issue #3026: Fixed incorrect longitude value for empire state building in example eg-0005. - Issue #3059: Added gameEdition for VideoGame by analogy with bookEdition.  *Changes in pending section*:  - Issue #3052: Added a new subtype of organization to distinguish organizations that are search and rescue organizations: SearchRescueOrganization. - Issue #3053: Updated keywords property to clarify that comma-separated usage only applies to textual keywords. Also updated to expect this property in several other high-level types. - Issue #3057: Added DigitalPlatformEnumeration as a convenience enumeration for use with actionPlatform. - Issue #3056: Added funding as a convenient inverse of fundedItem, with the associated types for both properties alligned. Added more examples around Grant. - Issue #3058: Added a new subtype of ConsumeAction called PlayGameAction. - Issue #2989: Added enumeration AdultOrientedEnumeration for use as value for new property hasAdultConsideration. Added hasAdultConsideration for use on offer and product. Also added isFamilyFriendly for use on offer and product in addition to CreativeWork. - Issue #3001: Added new property returnPolicyCountry for use on MerchantReturnPolicy. - Issue #2915: Added new property iso6523Code for use on organization. - Issue #3028: Added OnlineBusiness as a subtype of organization and OnlineStore as a subtype of OnlineBusiness. - Issue #3025: Added CategoryCode as an expected value for category. - Issue #2927: Added provider to action type.  **Site improvements**  PR #2990: Update supporting python version and libraries—RDFLib 6.1, python 3.10.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 13.0 (July 7, 2021)                   | Version 13.0—see planning pages. This release includes improvements proposed via the pending section, in particular a number of terms proposed by the bioschemas project, alongside other additions around e-commerce returns policy markup, job postings, and MediaReview markup.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | **Vocabulary**  *Changes in Core section*:  *Changes in pending section*:  - Issue #2892: Clarifications around blog, BlogPosting and LiveBlogPosting, including better cross-referencing, and acknowledgment of related terminology (“weblog,” and “blog” in the sense of posting). For clarity, the example showing LiveBlogPosting is no longer tagged to show up as an example of blog too. - Issue #2862: Additions proposed by the the bioschemas community. Adds several types for basic life science concepts. A type taxon, with properties: childTaxon parentTaxon taxonRank hasDefinedTerm. A general type BioChemEntity: associatedDisease, bioChemInteraction, bioChemSimilarity, hasBioChemEntityPart, hasRepresentation, isEncodedByBioChemEntity, encodesBioChemEntity, isPartOfBioChemEntity, taxonomicRange, biologicalRole, hasMolecularFunction, isInvolvedInBiologicalProcess, isLocatedInSubcellularLocation. The following types are subtypes of this convenience type. A type MolecularEntity, with properties inChI, inChIKey, iupacName, molecularFormula, molecularWeight, monoisotopicMolecularWeight, smiles. A type ChemicalSubstance with properties chemicalComposition, chemicalRole, potentialUse. A type Gene with additional property hasBioPolymerSequence. A type protein with additional property hasBioPolymerSequence. - Issue #2880: Additions to merchant return policies. Implemented in #2381. Adds ReturnLabelSourceEnumeration, ReturnMethodEnumeration and several enumerated values for these. Also adds several new enumerated values to existing ReturnFeesEnumeration. Adds properties returnMethod, itemDefectReturnFees, customerRemorseReturnFees, returnShippingFeesAmount, itemDefectReturnShippingFeesAmount, customerRemorseReturnShippingFeesAmount, returnLabelSource, itemDefectReturnLabelSource, customerRemorseReturnLabelSource, restockingFee, returnPolicyCountry. A dds new type MerchantReturnPolicySeasonalOverride and new property returnPolicySeasonalOverride. Adds existing additionalProperty and itemCondition to MerchantReturnPolicy and hasMerchantReturnPolicy to offer - Issue #2907: Added directApply property to indicate on a JobPosting whether direct applications are supported. - Issue #2844: Additional detail for MediaReview description. To cross-reference (via link or embedded description) between ClaimReview and MediaReview, two new properties: associatedClaimReview, associatedMediaReview. These are defined as specializations of a common superproperty: associatedReview. To describe exact, specific, “frozen” snapshots of a potentially changing MediaObject, three new types: ImageObjectSnapshot, AudioObjectSnapshot, VideoObjectSnapshot. A new property, sha256, can be used to identify the specific file by a hash of its contents. To group together multiple elements for reference by itemReviewed, a new type: MediaReviewItem. Its property, mediaItemAppearance, can use the “snapshot” types to bundle several different appearances of the same basic media item. For the case of an image with embedded text, a new property: embeddedTextCaption (a subproperty of caption). To characterize the original context of a potentially decontextualized media item, a property originalMediaContextDescription, alongside originalMediaLink, embeddedTextCaption, interpretedAsClaim, claimInterpreter, and archivedAt to provide additional supporting information useful for fact checking and misinformation-related workflows. - Issue #2912: Add a statement type, parallel to claim, for simple statements such as “fun or interesting” facts, to distinguish them from more formal (e.g., fact-checkable) claims. - Issue #2882: Added organization as an expected value for buyer. - Issue #2895: Add actor to PodcastSeries. - Issue #991: Adding countryOfLastProcessing and countryOfAssembly, to improve compatability with GS1. - Issue #2911: Added startOffset, which was accidentally omitted from the SeekToAction definitions previously. - Issue #2825 (also #2823): Added location, startTime and endTime to InteractionCounter. - Issue #2832: Added positiveNotes and negativeNotes properties for review, providing a simple dedicated syntax to support pro/con lists summarizing reviews.  **Site improvements**  - Issue #2790: Schema markup validator: [validator.schema.org](http://validator.schema.org/) is available for review. See documentation for details. - Issue #2891: Published draft [Schema.org](http://schema.org/) feeds specification for implementor discussion and feedback. - Issue #2842: Fixed many examples after review and update of ruby CI tests.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 12.0 (March 8, 2021)                  | Version 12.0—see planning pages. This release consists primarily of additions to the pending section of [schema.org](http://schema.org/), alongside some bugfixes and improvements to core terms.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | **Vocabulary**  *Changes in Core section*:  - Issue #1417: Fixed typo in isLiveBroadcast. - Issue #2786: Updated JSON-LD example in mainEntityOfPage. - Issue #2803: Add ineligibleRegion as expected on the MediaObject type. - Issue #2821: Add duration as expected on the episode type. - Issue #2840: Clarified definition of schemaVersion. - Issue #2803: (implemented in PR #2804): Added property ineligibleRegion to MediaObject type. - See also pending for cases where new terms required minor adjustments to core vocabulary.  *Changes in pending section*:  - Issue #2844: Updates to MediaReview reflecting community work towards clarifying a list of codes for MediaManipulationRatingEnumeration. - Issue #2810: Fixed bug: marginOfError should have values of type QuantitativeValue. - Issue #2811: Additions to support structured sizes and measurements. Implemented in #2819. Adds SizeSystemEnumeration, WearableSizeSystemEnumeration, SizeGroupEnumeration, WearableSizeGroupEnumeration, MeasurementTypeEnumeration, WearableMeasurementTypeEnumeration, BodyMeasurementTypeEnumeration, Size Specification and several initial enumerated values for these. Also add sizeGroup, sizeSystem, hasMeasurement, suggestedMeasurement, suggestedAge. Updated sizeproperty to include the new SizeSpecification type as a potential value. Additional expected values for valueReference: MeasurementTypeEnumeration, text and DefinedTerm. - Issue #2651: Add BackOrder as an enumeration member of ItemAvailability. - Issue #2799: Additional enumerated aspects for HealthAspectEnumeration, and clarified HowOrWhereHealthAspect for the case of vaccines. Additions: GettingAccessHealthAspect, AllergiesHealthAspect, SafetyHealthAspect, EffectivenessHealthAspect, PregnancyHealthAspect, IngredientsHealthAspect, HowItWorksHealthAspect. - Issue #2681: Added vocabulary around JobPosting and occupation so that we can explicitly indicate when degree-level qualification is not required. Added a boolean experienceInPlaceOfEducation property for JobPosting. Also added a new OccupationalExperienceRequirements type as an additional possible value for the existing experienceRequirements property. Added a number-valued property monthsOfExperience for use on OccupationalExperienceRequirements.  **Site improvements**  - PR #2706: Replaced TravisCI with GitHub actions for continuous integration testing of changes to the schemaorg repository. - Issue #2822: Updated punctuation used in breadcrumb path displayed at the top of property pages to reflect that a property is not a subtype of the property type. - PR #2789: Identified and corrected 80+ broken links within site. Created a localized link checking script (brokenlinkcheck.Py) for future testing possibilities. - PR #2800: Reorganized directory structure of repository and development environment to separate out software and test elements (into a software subdirectory) from vocabulary definition elements. - PR #2814: Completed process of moving [Schema.org](http://schema.org/) to https. This step included the move to https of vocabulary term definitions and consequent change to https of the canonical URI displayed under the term pages \[more…\] tag. The web site will continue to respond to both http and https URLs. Download files will continue to support both protocols. - PR #2815: Fixed links in release page that return a 404 response.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 11.01 (December 8, 2020)              | Version 11.01—see planning pages. This interim release consists primarily of bug fixes and site improvements.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | **Site improvements** - Fix invalid link to home page on attic home page. - Reinstated home pages for auto, bib, health-lifesci and meta sections. - Fix invalid links to section home pages on schemas page. - Update wording on pages for terms that are superseded, pending or retired. - Reinstated link to section home page for non-core terms.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 11.0 (November 30, 2020)              | Version 11.0—see planning pages. This release consists primarily of additions to the pending section of [schema.org](http://schema.org/), alongside some bugfixes and improvements to core terms.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | **Vocabulary**  *Changes in Core section*:  - Issue #2733: Fixed typo in description of ReceiveAction. - Issue #2746: Fixed invalid JSON-LD in example # eg-0449 on VideoGame. - Removed redundant property definitions for upvoteCount & downvoteCount. - Issue #2776: Fix invalid term links identified in examples files.  *Changes in pending section*:  - Issue #1842 implemented in PR #2744: Added examples for online and mixed online & offline events. Attached to event, eventAttendanceMode, and VirtualLocation descriptions. - PR #2737: Removed subproperty relationship between hasCategoryCode and hasPart. - Issue #2482 implemented in PR #2736: Added examples for sameAs, titleEIDR, and editEIDR properties. - Issue #2646 implemented in PR #2719: Added new AmpStory type—“A creative work with a visual storytelling format intended to be viewed online, particularly on mobile devices.” This is intended in particular, for works designed for AMP story readers. A more general supertype could be added if there is implementation interest. - Issue #2712 implemented in PR #2716: Added new PriceTypeEnumeration enumeration type with values InvoicePrice, ListPrice, MSRP, MinimumAdvertisedPrice, SRP, SalePrice. Added to range of priceType property on the UnitPriceSpecification and CompoundPriceSpecification types. - Issue #2689 implemented in PR #2715 & PR #2758: Added new PriceComponentTypeEnumeration enumeration type with values installment, subscription, Downpayment, ActivationFee, CleaningFee, DistanceFee. Added to range of new priceComponentType property on type UnitPriceSpecification. Added new billingStart and billingDuration properties on type UnitPriceSpecification. - Issue #2766: Added new HyperToc, HyperTocEntry types, tocEntry, tocContinuation and utterances properties to support navigation and annotation within MediaObject content. - Issue #2722 implemented in PR #2732: Added SeekToAction type to be used as a value for the potentialAction property on a VideoObject type. - Issue #2740 implemented in PR #2752: Added SolveMathAction, for sites than can analyze a mathematical expression, potentially solving or simplifying it. Also added a related type, MathSolver. - Issue 1401 implemented in PR #2745: Adjusted definition of competencyRequired so that it can be used to described the skills, knowledge, ability required in order to understand a learning resource. - Issue #2764 implemented in #2765: Added DefinedTerm to learningResourceType and educationalUse. - Issue 2,659: Added copyrightNotice and creditText, to help improve interoperability between [schema.org](http://schema.org/) and IPTC metadata. - Added missing supertype (intangible) to EnergyConsumptionDetails.  **Site improvements**  - PR #2706: Improvements to underlying site build architecture including separation of vocabulary definition and display logic; move to python 3; and simplified local build and test processes. Full type hierarchy page is now more usable and accessible (collapsible navigation). Copy example to clipboard button added to examples on term definition pages. - PR #2760: Added structured representation of JSON-LD examples tab to examples display on term definition pages. - PR #2726: Removed previous RDFa term description from within html of term definition pages, replace with equivalent JSON-LD script element. - Issue #2747 implemented in PR #2748: Fixed invalid comment syntax in the JSON-LD element of 47 examples.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 10.0 (September 7, 2020)              | Version 10.0—see planning pages. This release consists primarily of additions to the pending section of [schema.org](http://schema.org/), alongside some bugfixes and improvements to core terms.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | **Vocabulary**  *Changes in Core section*:  - Issue #737: Improve support for controlled taxonomies (e.g., SKOS) by supporting URLs into taxonomies for the keywords field: Added URL and DefinedTerm as expected values. - Issue #2647: SkiResort should be a subclass of resort (in addition to the existing SportsActivityLocation supertype). - Issue #2664: a parentItem of a comment should be a comment, not a question. - Issue #2662: The supertype of question should be comment, by analogy with answer. - Issue #881: Changed description to reviewBody in a review example.  *Changes in pending section*:  - Issue #2663: Add a property eduQuestionType for questions that act as practice problems. - Issue #2678: Indicated that learningResourceType is expected on LearningResource. - Issue #2483: Add hasCourse property to EducationalOccupationalProgram to specify which courses are components of a program. - Issue #2690: Add a layoutImage property to FloorPlan to clearly indicate an image that depicts the floorplan. - Issue #2670: Add vocabulary to express the energy efficiency of products. Adds a hasEnergyConsumptionDetails property for use on product to indicate an EnergyConsumptionDetails item which in turn has a hasEnergyEfficiencyCategory property whose values are drawn from enumerations. An enumeration class EnergyEfficiencyEnumeration with two initial subtypes, for EUEnergyEfficiencyEnumeration and EnergyStarEnergyEfficiencyEnumeration. The elements in the EU scheme are ordered, allowing energyEfficiencyScaleMax and energyEfficiencyScaleMin properties to specify the portion of the scale applicable to the relevant product category.  **Site improvements**  - Issue #2663: Updated all examples to use [https://schema.org](https://schema.org/) instead of [http://schema.org](http://schema.org/). - Style guide: Added a style guide for schema authoring to the site, giving conventions for term naming and capitalization.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 9.0 (July 21, 2020)                   | Version 9.0 see planning pages. This release consists primarily of additions to the pending section of [schema.org](http://schema.org/), alongside minimal edits to core terms to integrate the new vocabulary into the larger system.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | **Vocabulary**  *Changes in Core section*:  - Issue #2604: Improvements around enumerations. Some code improvements to present subtyped enumerations more usefully, and addition of a StatusEnumeration type to group numerous enumerations from various kinds of status-related situations. - Issue #2512: Fixed definition of LockerDelivery and ParcelService to correctly define them as enumeration members of DeliveryMethod. - Issue #2268: Defined expected type of several properties in ExercisePlan to be QuantitativeValue instead of the incorrect value of QualitativeValue.  *Changes in health-lifesci section*:  - Issue #2268: Defined expected type of several properties in ExercisePlan to be QuantitativeValue instead of the incorrect value of QualitativeValue.  *Changes in pending section*:  - Issue #1401: Add a type LearningResource to indicate CreativeWorks that have a particular and explicit orientation towards learning, education, skill acquisition and other educational purposes. - Issue #2611: Add a quiz type, as a kind of LearningResource, defined as a “test of knowledge, skills and abilities.” - Issue #2587: Add two properties size and pattern for type product to support common product variant dimensions. - Issue #1797: Add a ProductGroup type to allow modeling of a group of products (variants) that vary along explicitly defined dimensions. Add properties variesBy and hasVariant for type ProductGroup to explicitly define the variant-identifying properties and the list of variants belonging to the group. Adds existing property isVariantOf to type product to indicate the ProductGroup it is a variant of. Adds property productGroupID as explicit identifier for type ProductGroup. Also adds inverse property inProductGroupWithID for type product to identify the product group it is a variant of. - Issue #2605: Clarify the definition of collection to make clear that it covers a broad range of kind of “collection.” Add a ProductCollection type to allow modeling of a collection of products that are commonly bundled together. Extend the existing property includesObject for use with the type ProductCollection to indicate the (type and number of) products that are member of the collection. - Issue #2620: Added several new examples. - Issue #2599: Add byMonthWeek to schedule type. - Issue #1755: Add BoatReservation, BoatTrip (and arrivalBoatTerminal, departureBoatTerminal properties), BoatTerminal types.  **Site improvements**  - Issue #2304: (implemented in PR #2654):Rationalization of dump files. Machine readable vocabulary definition files, available from the developers area, have been rationalized to include definitions from the core plus all sections of the vocabulary. Now download file names have been used to reflect this change. Also introduced two versions of each file, one containing http URIs the other https URIs.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 8.0 (May 1, 2020)                     | Version 8.0 see planning pages. This release consists of additions to the pending section of [schema.org](http://schema.org/).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | **Vocabulary**  *Changes in Core section*:  - N/A  *Changes in pending section*:  - Issue #2543: Add a nonprofitStatus property to indicate non-profit organizations, alongside an initial enumeration of non-profit organization types, NonprofitType. - Issue #2506: Add vocabulary to help online vendors publish information about their shipping-related policies, associatted with an offer using the shippingDetails property. Adds OfferShippingDetails and supporting properties (including deliveryTime, doesNotShip, shippingDestination, shippingLabel, shippingRate, shippingSettingsLink, transitTimeLabel). Also added supporting types ShippingDeliveryTime, DefinedRegion, PostalCodeRangeSpecification, OfferShippingDetails, ShippingRateSettings. - Issue #2427: Simplifies education-related markup for describing what a learning resource teaches or assesses, and its educationalLevel. Allows these properties to be used for EducationEvents. - Issue #2384: Add property to JobPosting for legal requirements relating to eligibility to work such as citizenship, visa or other documentation. - Issue #2469: Add two properties to represent EIDR identifiers: titleEIDR and editEIDR.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 7.04 (April 16, 2020)                 | Version 7.04. See planning pages. This was a minor release, with improvements relating to the COVID-19 response effort.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Vocabulary**  *Changes in Core section*:  - Issue #2540: EducationalOrganization has an additional supertype of CivicStructure, clarifying that it can be used with announcementLocation.  *Changes in pending section*:  - Issue #2534: Improved vocabulary for describing government benefits in the context of a SpecialAnnouncement. A new governmentBenefitsInfo property can now reference a GovernmentService. The existing serviceType property can now optionally use enumerated values from GovernmentBenefitsType. This enumerates several kinds of government benefits. While the list is general purpose, our priority is to support the COVID-19 response. We anticipate adding more structure here in future to better capture per-country systems and new kinds of benefit. As part of this work we also introduce a jurisdiction property as a superproperty of legislationJurisdiction. - Issue #2536: Fixed a bug in the amended definition for category. - Issue #2626: Add a hackathon type. - Issue #2493: Add startTime/endTime to schedule.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 7.03 (April 2, 2020)                  | Version 7.03. See planning pages. This was a minor release, with improvements relating to the COVID-19 response effort.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Vocabulary**  *Changes in pending section*:  - Issue #2521: Adds a document and schema definitions capturing a 1:1 representation of a CDC CSV format for hospital reporting. - Issue #2519: Clarifies that webFeed can be expected on the SpecialAnnouncement type. - Issue #2518: Updated pending draft of 3DModel to place it under MediaObject rather than clutter CreativeWork.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 7.02 (March 31, 2020)                 | Version 7.02. See planning pages. This was a minor release, with improvements relating to the COVID-19 response effort.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Vocabulary**  *Changes in pending section*:  - Issue #2514: Added an announcementLocation property, clarifying how a SpecialAnnouncement can reference both regions and specific places.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 7.01 (March 22, 2020)                 | Version 7.01. See planning pages. This was a minor release, with improvements relating to the COVID-19 response effort.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Vocabulary**  *Core changes*  - N/A  *Changes in pending section*:  - Issue #2500: Added a SchoolDistrict type. - Issue #2497: Added datePosted to SpecialAnnouncement type.  **Site improvements**  - Issue #2495: Added an example for the geographic region of a SpecialAnnouncement.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 7.0 (March 17, 2020)                  | Version 7.0. See planning pages.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | **Vocabulary**  *Core changes*  - Issue #2448: Removed several largely un-used medical health properties whose names were inappropriately general: *Action*, *background*, *cause*, *cost*, *function*, *indication*, *origin*, *outcome*, *overview*, *phase*, *population*, *purpose*, *source*, *subtype*. Note that we do not remove terms casually, but in the current case the usability consequences of keeping them in the system outweighed the benefits of retaining them, even if flagged as archived/superseded. - Issue #1842: Introduced a VirtualLocation type, to support description of events whose location is online. Added eventAttendanceMode to clarify the current attendance mode of an event (online, offline, or a mix). Also added a new enumeration value for eventStatus for event: EventMovedOnline.  *Changes in pending section*:  - Issue #2490: Added (fast track) a SpecialAnnouncement type with several properties and supporting documentation, as a contribution to the global response to the COVID-19 coronavirus pandemic. We expect to iterate on this design after implementator and publisher feedback. - Issue #2460: Added properties to EducationalOccupationalProgram to support cases where it is not clear the distinction between classroom-based and work-based programs. - Issue #2373: Added petsAllowed for use with ApartmentComplex, and petsAllowed, amenityFeature and floorSize to FloorPlan. Created new properties for numberOfBedrooms and a new tourBookingPage. - Issue #2450: Added *draft* type MediaReview, and associated MediaManipulationRatingEnumeration with two example values AuthenticContent and MissingContext. Note that this is editorial work in progress and not a complete design. See also NiemanLab background article on this work. - Issue #2454: Added usageInfo, and acquireLicensePage to CreativeWork.  **Site improvements**  - Reinstated 301 redirect to https for http requests. - Issue #2412: Implemented in sdopythonapp submodule issue #6: Enhancements to CORS support, providing appropriate responses to HTTP OPTIONS request.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 6.0 (January 21, 2020)                | Version 6.0. See planning pages.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | **Vocabulary**  *Core changes*  *Other changes in Core section*:  - Issue #637: Made itemOffered and offers fully inverseOf each other. - Issue #2397: Reworded datePosted to avoid tying this property to overly-specific usecase (i.e., it originally assumed usage only with JobPosting). - Issue #2433: Shortened definition of PreOrder from ItemAvailability enumeration. - Issue #2375: Added note to descriptions for offer and AggregateOffer indicating default businessFunction. - Issue #2309: (implemented in PR #2380): Extended rangeIncludes of datePublished to include DateTime. - Issue #2420: Added MusicRecording as an expected value of audio. - Issue #2421: Added person and organization to the domain for interactionStatistic. - Issue #2139: Added MediaGallery as a super-type of ImageGallery and VideoGallery, to allow for a mixed-media collection page type. - Issue #2382: Added BroadcastService to the domain for inLanguage. - Issue #1951: Added SportsEvent to the domain for sport.  *Changes in pending section*:  - Issue #2372: Noted that other kinds of thing have callSign beyond radio broadcasts, in particular vehicles/boats and non-radio broadcasts. Added vehicle, person and BroadcastService (the latter also covers the initial type, RadioBroadcastService) to callSign accordingly. - Issue #2384: Adds three properties to JobPosting for requirements relating to physical abilities, sensory abilities and security clearance. - Issue #2396: Improvements to provide more information about the employer in JobPosting. Adds properties for applicationContact, employerOverview, and allows DefinedTerm to be used with the industry property. - Issue #2373: Improvements around real estate description including the addition of a property accommodationFloorPlan and type FloorPlan for use when a number of accomodation entries share a common layout. Added numberOfFullBathrooms and yearBuilt. Also noted that leaseLength is expected on offer and that datePosted can be applied to RealEstateListing. - Issue #2389: Changes to the pending schedule type: Adds the duration property, extends the range of byDay to allow for iCal-style rule syntax and adds the scheduleTimezone property. - Issue #2418: Added financialAidEligible property for the types of financial aid available for an EducationalOccupationalProgram. - Issue #2429: Added a number of properties to EducationalOccupationalProgram to help represent information for determining how long a program typically takes, when terms typically run, and when applications are accepted. Specifically: applicationDeadline, applicationStartDate, educationalProgramMode, numberOfCredits, maximumEnrollment, termDuration, termsPerYear, timeOfDay, typicalCreditsPerTerm. - Issue #2405: Add guide and recommendation as new types. - Issue #2394: Added isResizable to 3DModel. - Issue #2381: Renamed ProductReturnPolicy (and related) to MerchantReturnPolicy. - Issue #2108: (implemented in PR #2352): Introduced new pending type PronounceableText enabling phonetic markup of text values.  *Changes in bib section*:  - Issue #2366: (implemented in PR #2367): Added example for audiobook indicating a relationship with a printed counterpart.  **Site improvements**  - Issue #2025: Corrected xml encoding value in schemaorg.Owl file to be “UTF-8” - Issue #1986: (implemented in PR #2378): Added test to check for duplicate entries in jsonldcontext files. - Issue #2277: (implemented in PR #2388): Fixed error in definition of eventSchedule property.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 5.0 (November 1, 2019)                | Version 5.0. See planning pages.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | **Vocabulary**  *Changes in pending section*:  - Issue #2372: Extended and redescribed callSign property to cover other common situations where it is applicable. - Issue #2358: Introduced a type WebContent to allow descriptions to abstract away from the differences between url-addressable content in form of WebSite, WebPage or WebPageElement. - Issue #2374: Introduced HealthTopicContent and an enumeration of “aspects” of the different topical aspects found in such content, as well as a property hasHealthAspect associating WebContent instances with those identified aspects. - Issue #2373: Added properties accommodationCategory, numberOfBathroomsTotal, numberOfFullBathrooms, floorLevel, and leaseLength to accommodation for detailed real-estate description. leaseLength also added to RealEstateListing - Issue #2322: Linked skills description to formal definitions of competencies.  **Site improvements**  - PR #2365: Split codebase that underpins the [Schema.org](http://schema.org/) site into a separate repository, to simplify interaction with vocabulary definition and documentation files in the schemaorg repository area.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 4.0 (October 15, 2019)                | Version 4.0. See planning pages.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | **Vocabulary**  *Changes in pending section*:  - Issue #2348: Added draft types for RealEstateListing, OfferForPurchase and OfferForLease. - Issue #2289: (implemented in PR #2290): Added types EducationalOccupationalProgram, WorkBasedProgram and associated properties. - Issue #373: (implemented in PR #2007): Added types PodcastSeries, PodcastSeason, PodcastEpisode and associated properties. - Issue #2110: (implemented in PR #2142): Added property subtitleLanguage to BroadcastEvent type. - Issue #2341: (implemented in PR #2344): Added property ineligibleRegion to ActionAccessSpecification type. - Issue #2242: (implemented in PR #2345): Added property gender to SportsTeam type. - Issue #2329: (implemented in PR #2330): Added property totalJobOpenings to JobPosting type. - Issue #2296: (implemented in PR #2297): Added property employmentUnit to JobPosting type.  *Changes in bib section*:  - PR #2232: Simplified example for audiobook.  **Site improvements**  - Issue #2331: (implemented in PR #2332): Fixed mobile usability issues of site—identified by Google search console. - PR #2312: Fixes typo for rdfs:Label URI.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 3.9 (August 1, 2019)                  | Version 3.9. See planning pages.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | **Vocabulary**  *Core changes*  - Issue #2294: (implemented in PR #2295): Adding example for JobPosting.  *Changes in pending section*:  - Issue #2291: Added StatisticalPopulation, observation and supporting properties to enable statements (e.g., aggregate statistics) about sets of entities that have particular properties. - Issue #2300: Added ratingExplanation property to rating (expect type text): “ *A short explanation* (e.g., *one to two sentences*) *providing background context and other information that led to the conclusion expressed in the rating*. *This is particularly applicable to ratings associated with ‘fact check’ markup using ClaimReview*.” - Issue #2289 (implemented in PR #2290): Added types for educational programs: EducationalOccupationalProgram and WorkBasedProgram plus supporting properties: hasCredential (for organization and person types), occupationalCredentialAwarded, programPrerequisites, timeToComplete, trainingSalary, and salaryUponCompletion.’  **Site improvements**  - PR #2292: Fixed typo in Jane Doe's name in example for person. - PR #2285: Corrections to examples identified as errors by Travis CI scripts. - PR #2199: Fix to grammar in description of knowsAbout.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 3.8 (July 1, 2019)                    | Version 3.8. See planning pages.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | **Vocabulary**  *Core changes*  - Issue #2294: (implemented in PR #2295): Adding example for JobPosting.  *Changes in pending section*:  - Issue #2291: Added StatisticalPopulation, observation and supporting properties to enable statements (e.g., aggregate statistics) about sets of entities that have particular properties. - Issue #2300: Added ratingExplanation property to rating (expect type text): *A short explanation* (e.g., *one to two sentences*) *providing background context and other information that led to the conclusion expressed in the rating*. *This is particularly applicable to ratings associated with ‘fact check’ markup using ClaimReview*. - Issue #2289 (implemented in PR #2290): Added types for educational programs: EducationalOccupationalProgram and WorkBasedProgram plus supporting properties: hasCredential (for organization and person types), occupationalCredentialAwarded, programPrerequisites, timeToComplete, trainingSalary, and salaryUponCompletion.  **Site improvements**  - PR #2292: Fixed typo in Jane Doe's name in example for person. - PR #2285: Corrections to examples identified as errors by Travis CI scripts. - PR #2199: Fix to grammar in description of knowsAbout.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 3.7 (June 1, 2019)                    | Version 3.7. See planning pages.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | **Vocabulary**  *Core changes*  - Issue #2192: Added CategoryCode to rangeIncludes for property occupationalCategory and DefinedTerm to rangeIncludes for property jobTitle. - Issue #2251: Extended rangeIncludes for property estimatedSalary to include MonetaryAmount and number. - Issue #1848: Updated definitions of addressRegion and addressLocality that a street address is in a locality and a locality is in a region. - Issue #2167: Fixed invalid JSON-LD in examples showing educationRequirements for person and occupation. - Issue #1991: Fixed incorrect links (to [webschemas.org](http://webschemas.org/)) in docs/releases.Html. - Issue #1993: Updated definition and provided examples for isBasedOn property. - Issue #2136: Fixing some typos and missing commas in example for schedule.  **Site improvements**  - Issue #2132: Added some hierarchy to the documentation page.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 3.6 (May 1, 2019)                     | Version 3.6. See planning pages.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | **Vocabulary**  *Core changes*  Moved from pending to Core:  Other changes in Core section:  - Issue #2202: Restored estimatedSalary as a property expected on the JobPosting type. - Issue #1469: Corrected format of example durations in timeRequired property description. - Issue #1470: Corrected duration format in examples for timeRequired. - Issue #2188: Added service to rangeIncludes of orderedItem property. - Issue #2184: Added LodgingBusiness to rangeIncludes of numberOfRooms property. - Issue #2166: Added number formatting advice to description of number, ratingValue, value, lowPrice, highPrice, totalPrice properties. - Issue #2082: Fixed RDFa example for website. - Issue #2077: Fixed JSON-LD example for availableLanguage property. - Issue #2055: Updated text to correctly quote princess Leia in example for spokenByCharacter property. - Issue #2036: Fix broken “url” term in ItemList example. - Issue #2013: Fixed typo in hotels.Html. - Issue #2003: Improvements to descriptions of campground and CampingPitch, identifying the differences between British English and American English for these and associated terms. - Issue #1989: Replaced meta with link in isLiveBroadcast example. - Issue #1937: Added a direct link to developers page from schemas page. - Issue #1605: Made CatholicChurch subclass of church.  *Changes in pending section*:  - Issue #1909: Added a courseWorkload property for use with CourseInstance type.  **Site improvements**  - Issue #2054: Corrected spelling in README.md file. - Issue #2215: Corrected display of enumeration value terms that are more than 1 subclass away from a parent enumeration value (e.g., EvidenceLevelA). - Issue #2212: Various fixes to examples. Identified by linter tests. - Issue #2209: Updates to Travis test. - Issue #2233: Fixed non-disply of acknowledgement text on term pages. - Issue #2229: Stopped the duplication of references for some types in \*-types.Csv download files. - Issue #2234: Fix to JSON-LD context file—properties with text in their range should not have ‘@type: “@id”'set. - Issue #2218: Split Travis tests into stages for easier reporting/analysis.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 3.5 (April 1, 2019)                   | Version 3.5. See planning pages. This release moves a number of terms from pending into the [Schema.org](http://schema.org/) core. It also simplifies and clarifies the [Schema.org](http://schema.org/) extension model, reducing our emphasis on using named subdomains for topical groups of schemas. New terms introduced in pending area include improvements for describing projects, grants and funding agencies; for describing open-ended date ranges (e.g., datasets); and a substantial vocabulary for educational and occupational credentials.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | **Vocabulary**  *Core changes*  Moved from pending to Core:  - Issue #1004: BroadcastFrequencySpecification, FMRadioChannel, AMRadioChannel, broadcastFrequency, broadcastFrequencyValue, broadcastFrequencyValue, hasBroadcastChannel. - Issue #1125: PreOrderAction. - Issue #1262: BedType. - Issue #1293: EndorsementRating. - Issue #2053: SpeakableSpecification, cssSelector, xpath. - Issue #1541: menuAddOn. - Issue #1670: subjectOf. - Issue #1689: EmployerAggregateRating, reviewAspect. - Issue #1698: Occupation, educationRequirements, estimatedSalary, experienceRequirements, occupationalCategory, occupationLocation, qualifications, responsibilities, skills, hasOccupation, relevantOccupation, QuantitativeValueDistribution, median, percentile10, percentile25, percentile75, percentile90, MonetaryAmountDistribution. - Issue #1723: FAQPage. - Issue #1741: MediaSubscription, ActionAccessSpecification. - Issue #243: WorkersUnion. - Issue #743: Distillery.  *Other changes in Core section*:  - Issue #2017: Added clip to expected values of video, audio properties. Also amended caption to be expected on AudioObject, documented a pattern for describing downloadable captions and their media format using another MediaObject with an encodingFormat. - Issue #2034: Added startTime, endTime properties as expected for MediaObject type. - Issue #2038: Add person as an expected type for byArtist property. - Issue #2112: Added slogan property, analogous to logo. - Issue #2104: Improved description of elevation property. - Issue #1030: Noted that encodesCreativeWork is inverseOf encoding. - Issue #2021: Added startOffset and endOffset to clip. - Issue #1765: Removed superseded status from and generalized descriptions for spatial and temporal properties plus expanded range to CreativeWork.  *Changes in pending section*:  - Issue #1365: In temporalCoverage, added proposed ISO 8601 notation for open-ended date ranges, for example, 1972–2001. - Issue #383: Added initial vocabulary towards improved support description of project-based funding, for example to use with dataset citations. See also DINGO draft, another outcome from the same Wikidata/Wikibase workshop. New types for Grant, MonetaryGrant, project, FundingAgency, FundingScheme, and ResearchProject. Developed in collaboration with the Wikidata/Wikibase community. - Issue #1591: Added jobLocationType property. - Issue #2083: Added applicantLocationRequirements property. - Issue #2085: Added membershipPointsEarned property. - Issue #2140: Added 3DModel type. - Issue #2109: Added callSign property, and RadioBroadcastService type. - Issue #2111: Added broadcastSignalModulation and broadcastSubChannel for use with BroadcastFrequencySpecification. - Issue #1758: Added ArchiveOrganization, ArchiveComponent types, and archiveHeld, holdingArchive properties. - Issue #1759: Added collectionSize and materialExtent properties. - Issue #1978: Educational and occupational credentials vocabulary and examples from the eocred-schema community group. Added a type EducationalOccupationalCredential and properties credentialCategory, educationalLevel, competencyRequired, recognizedBy. Minor changes to validIn, validFor, educationRequirements, educationalCredentialAwarded, and qualifications (linking EducationalOccupationalCredentials to JobPostings, occupations and courses). - Issue #1968: Replaced use of hasPart and isPartOf properties on trip type, with new subTrip and partOfTrip properties. - Issue #1375: Renamed the various properties and labels from geospatiallyXyz to geoXyz for brevity, for example, geoIntersects. - Issue #1448: Added manuscript, poster, drawing, and SheetMusic subtypes of CreativeWork. - Issue #1976: Added ShortStory subtype of CreativeWork. - Issue #1816: Added play subtype of CreativeWork.  **Site improvements**  - Added section to Github README discouraging large projects without prior discussion. - Linked Travis-CI from Github README. - Clarified and simplified the extension mechanism.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 3.4 (sdo-telesto; June 15, 2018)      | Version 3.4 (working name “sdo-telesto”). See planning pages. Clarifications around series. Introduced an example showing ClaimReview of a clip within a larger media object. A lot of small fixes and maintenance edits. Numerous additions to the pending area, including employment and occupation vocabulary, a claim type to help explore richer modeling around fact-checks, tourism-related vocabulary. Other pending area improvements include amendments to the legislation vocabulary, trust project additions, and the proposal of an inverse of the about property, subjectOf.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | **Vocabulary**  *Core changes*  - Issue #1902: Improvements to HowTo examples. See also #1895. - Issue #1761: Changed mis-abbreviation of Friday as “Fri” to “Fr.” Per the guidelines for openingHours, Friday should be abbreviated as “Fr.” In one set of examples, it was abbreviated as “Fri.” - Issue #1820: Hyperlink to new, recommended DOI resolver. - Issue #1894: Added reference to cryptocurrencies in description for “paymentAccepted” and “currenciesAccepted” properties. For consistency, also added to description of properties: “discountCurrency,” “price,” “priceCurrency,” “currency.” Updated the description additions to reference ISO 4217 formats, cryptocurrency Ticker symbols, LETS and other currency types including single inline examples for each. - Issue #1090: Clarified series, CreativeWorkSeries, EventSeries. The series type is now intangible, rather than having an inappropriate CreativeWork supertype. We have two subtypes of it, CreativeWorkSeries (successor to the original definition of series, which was too generally named), plus the proposed EventSeries type (currently in the pending area). These domain-specific series types also have corresponding supertypes in CreativeWork and event. See also issue #447. - Issue #1155: Clarified that encodingFormat, fileFormat mean the same thing, converged their definitions, and made encodingFormat the preferred term. - Issue #1824: Fixed typos in tickerSymbol. - Issue #1833: Added expected type ItemList to acceptedAnswer, suggestedAnswer. - Issue #1799: Fixed an error in an example for question type. - Issue #1686: Added an extra ClaimReview example based on a TV clip. - Issue #1762: Added schema mapping declarations indicating that “name” is a subproperty of rdfs:Label, and equivalentProperty of dcterms:Title. - Issue #1729: Improvements around HowTo, including declaration of CreativeWork as its supertype, and introduction of “step” property instead of “steps.” - Issue #1732: Changed HowToSection and HowToStep (which support the HowTo type) to have CreativeWork as their supertype. - Issue #1723: Introduced FAQPage, which represents a WebPage presenting one or more “frequently asked questions.” - Issue #1935: Extend the contentRating property to also expect the rating type. - Issue #2020: Extend the byArtist property to also expect the person type.  *Changes in pending section*  - Issue #1670: Add a subjectOf to thing as an inverse property of about. - Issue #1689: Add EmployerAggregateRating as a subtype of AggregateRating to differentiate ratings for the entity as an employer and the reviewAspect property to review and rating to allow authors to specify the facet or relevant part of being reviewed. - Issue #1698: Add a occupation type with the supporting properties, many of which existed for JobPosting. A Person's occupation can be specified with hasOccupation. The Occupation's estimatedSalary is expressed as a MonetaryAmountDistribution, a subtype of the new QuantitativeValueDistribution type. - Issue #1787: Narrowed the range of legislationJurisdiction to AdministrativeArea rather than place. Broadened the range of legislationIdentifier to include URL, to match with the description of the property. - Issue #1815: Added proposal for TouristDestination, TouristTrip, and trip plus examples. - Issue #1886: Add basic sdPublisher and sdDatePublished (and in #1866, sdLicense) markup, for example, for when structured data created elsewhere. - Issue #1866: Added a proposed sdLicense property. - Issue #1776: Introduced DefinedTerm as a super type of the existing proposed term CategoryCode, to support non-categorical controlled terms. - Issue #1828: Added a claim type, to make explicit a concept suggested in the ClaimReview fact-checking markup. - Issue #1773: Add a MediaSubscription type with the supporting properties to describe a subscription for viewing media. Also added ActionAccessSpecification to allow authors to specify when a ConsumeAction requires a subscription or a purchase. - Issue #1744: Improvements around legislation vocabulary. Changed definition of “legislation” to make it clear that it is a document. Deleted numerous inverse properties. Fixed range on legislationType (CategoryCode). Added legislationJurisdiction as a subproperty of spatialCoverage. Fixed definitive into DefinitiveLegalValue to align with other values. Expanded the definition of legislationIdentifier to clarify that it can apply to string or URIs. Fixed and adjusted the examples accordingly. - Issue #1709: Added an occupation type and examples, to represent professions. - Issue #1389: Updated SpeakableSpecification-related properties, “xpath” and “cssSelector” to explain how they relate to “WebPageElement.” Allowed both properties to be expected on that type. - Issue #1525: Improvement suggested by trust project, including addition of AskPublicNewsArticle, ownershipFundingInfo and diversityStaffingReport properties, editorial tweaks to dateline property. Second phase of additions included knowsAbout, knowsLanguage proposals (#1688.) - Issue #1950: Added CorrectionComment and a property correction to point to it, as suggested by the trust project.  *Changes in other named extensions*  - Issue #1882: Fix to OccupationalTherapy—made OccupationalTherapy a simple class instead of a typeof schema:MedicalSpecialty - Issue #1677: Added (and #1900 improved) autos documentation.  **Site improvements**  - Issue #1634: Aliased “rdf:HTML” to “HTML” in JSON-LD context definitions. - Issue #1879: Fix to duplicate and missing properties listings in the CSV outputs for types and enumeration values (see also #1882). - Issue #1878: Improvements towards a more responsive HTML design, thanks to Dan Scott. - Issue #1857: Updated site search function to use Google custom search v2 API. - Issue #1646: Updated various links to use https when referring to this site. - Issue #1722: Continuous integration tests now check RDFa syntax. - Issue #1946: Linked experimental D3/RDFS and OWL representations from the developers page.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 3.3 (sdo-enceladus; August 14, 2017)  | Version 3.3 (working name “sdo-enceladus”). See planning pages, specifically #1569 for details.  This release introduces pending types around review, NewsArticle and article that allow more fine-grained distinctions to be made. It adds a TouristAttraction type to the core, and a draft PublicToilet type as a pending proposal. It adds a HowTo vocabulary that generalizes recipe-like structured instructions, and adds some useful properties to EmailMessage. It also adds a substantial vocabulary for describing legislation to the pending section.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | **Vocabulary**  *Core changes*  - Issue #1459: Improvements to TouristAttraction. Add a new property touristType to TouristAttraction, “attraction suitable for type(s) of tourist. For example, Children, visitors from a particular country, etc.” Extend the domain of availableLanguage to TouristAttraction, of isAccessibleForFree to place, adapting the definitions accordingly. Add new property publicAccess to place. “A flag to signal that the place is accessible by public visitors.” - Issue #1525: Expanded definition of NewsArticle from “A news article” and added a news overview document introducing some proposed additional terms, and discussing the relationship between news and related markup for education/learning, TV, radio, and so forth. - Issue #647: Add a HowTo type, building upon and generalizing the existing recipe vocabulary. This introduces estimatedCost, steps, supply and tool as new properties, and re-uses performTime, prepTime, totalTime. We also introduce yield, which generalizes the existing recipeYield, and note that performTime generalizes the existing cookTime. Supporting types HowToItem (with a requiredQuantity property), HowToSupply and HowToTool, HowToSection and HowToStep (a kind of ItemList) are also provided, to allow more explicitly structured steps to be described. This effort has had many contributors over the years—thanks to all who have helped! - Issue #1590: Add bccRecipient, ccRecipient, and toRecipient for use with EmailMessage. - Moved to Core from pending: 	- None proposed.  *Additions to pending section*  - Issue #1457: Add a schedule type, with supporting properties: repeatFrequency, repeatCount, byDay, byMonth, byMonthDay, exceptDate, eventSchedule. These terms are used alongside the existing startTime and endTime properties. The main purpose of this new vocabulary is to capture recurring events in a manner compatible with a subset of the iCalendar approach. - Issue #1156: Add legislation, LegalForceStatus, LegislationObject, LegalValueLevel and other supporting terms. These terms are based on the European legislation identifier (ELI) ontology and the work of the ELI taskforce. ELI is an initiative of some national legislation publishers endorsed by EU countries and institutions, to identify, describe and link legislation on the web. - Issue #1624: Add a draft PublicToilet type to the pending section. - Issue #1577: Add estimatedSalary to JobPosting. - Issue #1589: Add CriticReview and UserReview to distinguish common subtypes of review. - Issue #1576: Add EmployerReview to indicate reviews that are by a current or former employee, and that are reviews of that organization's role as an employer. - Issue #1525: Add subtypes of NewsArticle: ReportageNewsArticle, AnalysisNewsArticle, OpinionNewsArticle, ReviewNewsArticle, BackgroundNewsArticle to distinguish common kinds of NewsArticle. Also add a subtype of article, AdvertiserContentArticle and a news overview document. Added a subtype of organization, NewsMediaOrganization, alongside several “best practice”-oriented properties: actionableFeedbackPolicy, correctionsPolicy, diversityPolicy, ethicsPolicy, masthead, missionCoveragePrioritiesPolicy, unnamedSourcesPolicy, verificationFactCheckingPolicy (apart from ethicsPolicy and diversityPolicy, these are all sub-properties of publishingPrinciples). These changes were based in large part upon the work of the trust project. - Issue #1437: Add SatiricalArticle type.  **Site improvements**  - Issue #1582: Added dedicated documentation page describing background and examples for banking and finance terms.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 3.2 (sdo-callisto; march 23, 2017)    | Version 3.2 (working name “sdo-callisto”). See planning pages, specifically #1292 for details.  This release introduces new core vocabulary including mechanisms for describing fact-check reviews, courses, and menus. It also introduces a number of newly-proposed terms via the “pending” area, to encourage discussion, implementation feedback and other improvements.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | **Vocabulary**  *Core changes*  - Issue #1209: Added maximumAttendeeCapacity and remainingAttendeeCapacity for describing places and events. - Issue #1361: Broadened about property to be applicable on events. - Issue #1364: Broadened genre property to be applicable on BroadcastChannel. - Issue #1488: Added identifier as a common super-property of numerous identifying properties. - Issue #1288: Added types menu, MenuItem, MenuSection, and properties hasMenuItem, hasMenuSection. A proposed menuAddOn property has also been added to pending for further design discussion and implementor feedback. Introduced hasMenu property that supersedes menu, both for consistency with the other new menu properties, and to avoid a property and type having essentially the same name. - Moved to Core from pending: 	- Issue #195: Added course-description terms: Course, courseCode, coursePrerequisites, hasCourseInstance, CourseInstance, courseMode, instructor. Thanks to the schema course extension community group at W3C, initiated by LRMI and led by Phil barker. 		- Issue #1061: Migrated ClaimReview and claimReviewed for fact-checking reviews into Core section. 		- Issue #1100: Added accessMode, accessModeSufficient, accessibilitySummary properties to support accessible digital publishing. This proposal came from the digital publishing community, and specifically from the Epub 3.1 accessibility working group.  *Additions to pending section*  - Issue #1541: Add a menuAddOn property (originally proposed with other menu-related terms). - Issue #1125 added PreOrderAction (a subtype of TradeAction) - Issue #1253: Added several terms proposed by the FIBO project and its community group. 	- Types: BrokerageAccount, ExchangeRateSpecification, InvestmentFund, MoneyTransfer, MortgageLoan, RepaymentSpecification. 		- Properties: accountMinimumInflow, accountOverdraftLimit, amount, bankAccountType, beneficiaryBank, cashBack, contactlessPayment, currency, currentExchangeRate, domiciledMortgage, downPayment, earlyPrepaymentPenalty, exchangeRateSpread, floorLimit, gracePeriod, loanMortgageMandateAmount, loanPaymentAmount, loanPaymentFrequency, loanRepaymentForm, loanType, monthlyMinimumRepaymentAmount, numberOfLoanPayments, recourseLoan, renegotiableLoan. - Issue #1262: Added BedType. - Issue #1293: Added EndorsementRating. - Issue #1375 added GeospatialGeometry and some draft definitions for associated properties, an informal collaboration with the W3C spatial data on the web working group. Initial properties are: geoContains, geoCoveredBy, geoCovers, geoCrosses, geoDisjoint, geoEquals, geoIntersects, geoOverlaps, geoTouches, geoWithin. - Issue #1389: Added new type SpeakableSpecification, with properties cssSelector and xpath, alongside a property on WebPage called speakable to refer to a SpeakableSpecification. The purpose (documented primarily on the speakable property) is to indicate sections of a document that are highlighted as particularly suitable for being spoken/read. These sections are indicated via URL/ID values, XPath and/or CSS selectors. - Issue #1397: Added CompleteDateFeed to indicate completeness of feeds. - Issue #1423: Added a draft WebAPI. - Issue #1425: Added a draft measurementTechnique property, to support richer dataset description particularly for scientific data. - Issue #1495: Added a consortium type, as well as a LibrarySystem type to represent a particular kind of library consortium. - Issue #743: Added a distillery type. - Issue #894: Added CategoryCode, CategoryCodeSet, codeValue and inCodeSet to explore better description of enumerated value lists. - Issue #1004: Added broadcastFrequency, broadcastFrequencyValue and BroadcastFrequencySpecification for describing (primarily radio but also TV) frequencies. Also supporting types FMRadioChannel, AMRadioChannel, and property hasBroadcastChannel (inverse: providesBroadcastService).  *Archived into attic section*  - The proposed variablesMeasured property has been removed from pending. A non-plural variableMeasured property replaced it. - broadcastSignalModulation was retired august 17, 2016 from pending section. - The courses proposal while in pending originally had additional terms—courseCredits, courseCreditsUnit, grantsCredential, previewUrl—which should be archived here.  **Site improvements**  - Issue #1027: Published a basic robots.Txt file to avoid a template file being indexed by search engines. - Issue #1272: Created an internet of things (IoT) section, mailing list and discussion document. At this stage no specific schemas are proposed, only some basic infrastructure for collaboration and schema review. - Issue #1398: Added HTML anchor to support links to the “incoming” section of pages documenting types (see example). - Issue #1483: Added a sitemap.Xml file. - Issue #53: Added Travis-CI monitoring for test cases and syntax checking of examples. - Issue #1351: Improvements to the output formats of downloads section in developers page.  **Quick fixes and examples**  - Issue #1475: Clarified that event can have an audience property. - Issue #1494: Broadened lender to allow organizations as possible values. - Issue #1294: Restored material as a super-property of artMedium that can be used with any product or CreativeWork. Also marked artworkSurface as another specialized sub-property of material. The material property can now also have product as its value, allowing branded and manufactured materials to be described in more detail. - Issue #1290: Add the word “event” to isAccessibleForFree definition. - Issue #1162: Updated text for sameAs—freebase mention migrated to reference Wikidata.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 3.1 (sdo-makemake; August 9, 2016)    | Version 3.1 (working name “sdo-makemake”). See planning pages, specifically #1212 for details.  This release is primarily concerned with hotel/accomodation vocabulary, improvements around dataset, and bug fixes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | **Vocabulary**  - Issue #915: Added substantial vocabulary for hotels and related accomodation, alongside a dedicated documentation page. New vocabulary includes LodgingBusiness, accommodation, and several subtypes which can be used (via multiple typing) alongside the existing offer type. Other terms include starRating, amenityFeature, LocationFeatureSpecification, floorSize, permittedUsage, petsAllowed, checkinTime, checkoutTime… - Issue #1203: Fixes for accidental rollbacks in 3.0. See Github for comprehensive analysis and details. Restored several definitions: paymentStatus lacked PaymentStatusType from #518; breastfeedingWarning, healthCondition, prescriptionStatus and secondaryPrevention have been migrated into [health-lifesci.schema.org](http://health-lifesci.schema.org/) as planned; SocialMediaPosting has supertype of BlogPosting (from #526) rather than Article; genre expects URL values (from #346); affiliation is a sub-property of memberOf (per #596); cookTime, prepTime and totalTime definitions hyperlink to ISO 8601 details; publisher property can reference Person (fix for #1198, restoring #611); videoFormat is again expected on BroadcastEvent, ScreeningEvent (and BroadcastService), rather than TelevisionStation (per #577); parentOrganization and subOrganization are noted as mutual inverses (per # g535); codeSampleType description improved per #343; netWorth definition now correctly omits Organization (per #585). - Issue #900: Extended isAccessibleForFree to be expected potentially on any event or CreativeWork. - Issue #996: Added DateTime to expected values for startDate, endDate, commentTime. - Issue #1083: Improvements primarily around dataset, generalized spatial property of dataset to become spatialCoverage of any CreativeWork; similarly generalized temporal as temporalCoverage. Indicated that spatialCoverage is a subproperty of contentLocation. Broadened sponsor to apply to creative works such as datasets, and added a more specific subproperty to indicate funder. Amended definition of MediaObject to match its use as a supertype of DataDownload. Amended fileFormat to allow URL as a way of indicating niche or unregistered file formats (common for scientific datasets). Added a draft variablesMeasured property to the pending extension.  **Site improvements**  - Issue #1234: Enhanced incoming properties display (instances of \[…\] may appear as values for the following properties) to include properties from extensions. - Issue #479: Updated and clarified the datamodel document, including conformance section. - Issue #1213: Fixes for site performance problems. - Issue #1214: Fix for RDFa formatting errors in per-term pages. - Issue #1248: Fix for need easy way to download rdf definition files. Introduces a vocabulary definition download section providing access to RDF representations of the vocabulary and extensions in triple, quad, JSON-LD, and turtle format.  **Quick fixes and examples**  - Issue #1151: Broadened version to allow textual values as well as numbers. - Issue #1257: Fixed all labels to match corresponding term IDs exactly. - Issue #1260: Fixed product example, microdata was missing itemprop attribute. - Issue #1201: Clarified deliveryLeadTime for the case of on-site pickup. - Issue #1283: Removed dentist from deprecated type ProfessionalService, added LocalBusiness as a supertype.  The following early access fixes were published between 3.0 and 3.1 releases:  - Issue #1159: Fixed problems with W3C validator, caching, and misclassification of manufacturer property which in in core rather than health-lifesci extension. - Issue #1165: Improved wording for term pages that are not in core, to avoid publishers worrying that they need to change their markup. - Issue #1136: Fixed term labels to always be alphanumeric (no “bib:” prefixes etc.) - Issue #1168: Fixed unit tests to run against extension schema data as well as core. - Issue #1169: Fixes for property/type associations in health-lifesci and pending drafts, identified by improved unit tests. - Issue #1174: Fix for missing definition for “ingredients.”                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 3.0 (sdo-deimos; May 4, 2016)         | Version 3.0 (working name “sdo-deimos”). See planning pages, specifically #911 for details.  This release introduces three new extensions.  The [meta.schema.org](http://meta.schema.org/) extension contains terms primarily designed to support the implementation of the [Schema.org](http://schema.org/) vocabulary itself.  The [pending.schema.org](http://pending.schema.org/) extension is a staging area for work-in-progress terms which have yet to be accepted into the core vocabulary. Pending terms are subject to change and should be used with caution.  The [health-lifesci.schema.org](http://health-lifesci.schema.org/) extension is a new home for our existing medical and healthcare related terms, as well as potential future collaborative work.  The initial releases of [bib.schema.org](http://bib.schema.org/) and [auto.schema.org](http://auto.schema.org/) have also been finalized.  In addition to numerous vocabulary-related improvements, we have added a new “how we work” document providing an overview of the project's approach to schema development, collaboration, versioning and change review. In particular it documents the use of the new pending extension, which gives earlier access to proposed new schema designs, as well the parallel [webschemas.org](http://webschemas.org/) site which shows the latest work-in-progress version of the entire [schema.org](http://schema.org/) site. | **Vocabulary**  *Core changes*  - Issue #845: Added vocabulary for suitability to restricted diets in recipe (suitableForDiet, RestrictedDiet). - Issue #1005: Generalized some properties from product to apply also to service-audience, brand, logo, isRelatedTo, isSimilarTo. - Issue #880: Added disambiguatingDescription to explicitly indicate short Wikipedia-like disambiguating descriptions. - Issue #1048: Added DigitalDocument and subtypes SpreadsheetDigitalDocument, PresentationDigitalDocument, TextDigitalDocument, NoteDigitalDocument. Also a hasDigitalDocumentPermission property of these whose value is a DigitalDocumentPermission type. A permissionType property of each DigitalDocumentPermission has values that are from a DigitalDocumentPermissionType enumeration: CommentPermission, ReadPermission, WritePermission. The grantee property indicates in each case the person, organization, contact point, or audience that has been granted that permission. - Issue #888: Added PreSale to the ItemAvailability enumerated values. - Issue #962: Broadened definition of sponsor property. - Issue #961: Improved wording of validThrough, and added JobPosting to allow markup for job posting closing dates. - Issue #1020: Added new subtypes of CreativeWork: Message and conversation. Marked EmailMessage as a subtype of message. - Issue #1079: Created ComputerLanguage, amended programmingLanguage to expect it (and text); amended language to focus on natural languages. Noted that BCP 47 should be used for natural language tagging, via alternateName property. Amended availableLanguage to indicate that text values are expected, that BCP 47 is encouraged, and to cross-reference with inLanguage. - Issue #1092: Amended contributor, actor, translator, director, composer to apply to event. - Issue #969: Integrated improvements from FIBO to core terminology around financial products, including the addition of MonetaryAmount (superseding DatedMoneySpecification) and CompoundPriceSpecification, alongside improved wording around CreditCard, PriceSpecification. - Issue #923: Created [schema.org](http://schema.org/) entries for Monday–Friday and PublicHolidays, based on the GoodRelations originals. Also clarified OpeningHoursSpecification and added a specialOpeningHoursSpecification property to allow for general opening hours to be overridden. - Issue #541: Added enumerations for male and female, but allow other values as well. - See also issue #492 below; many terms have been moved from the core into health-lifesci. [auto.schema.org](http://auto.schema.org/) - Issue #922: Finalized first release of [auto.schema.org](http://auto.schema.org/). Removed “pre-final preview release” description. [bib.schema.org](http://bib.schema.org/) - Issue #911: Finalized first release of [bib.schema.org](http://bib.schema.org/). Removed “pre-final preview release” description. [health-lifesci.schema.org](http://health-lifesci.schema.org/) - Issue #492: Moved a large number of medical/health terms from core into a health-lifesci extension. [pending.schema.org](http://pending.schema.org/)  The pending extension is a staging area for work-in-progress terms which have yet to be accepted into the core vocabulary.  - Issue #1050: Added contentReferenceTime. - Issue #1062: Added HealthInsurancePlan, a US health insurance schema. - Issue #1110: Added accessMode, accessModeSufficient and accessibilitySummary. - Issue #447: Added EventSeries. - Issue #271: Added quotation and spokenByCharacter. - Issue #1061: Added ClaimReview and claimReviewed for fact-checking reviews. - Issue #1059: Created [pending.schema.org](http://pending.schema.org/) to enable publication of work-in-progress drafts for wider review. - Issue #1045: Added LinkRole as a subtype of role, and a linkRelationship property. - Issues #243: Added WorkersUnion. - Issue #1004: Added broadcastFrequency to BroadcastService to specify the over the air frequency. - Issue #195: Added snapshot of the evolving course-related terms being developed by the course extension community group.  **Site improvements**  - Issue #1059: Created hosted extensions for “meta” vocabulary and for “pending” vocabulary under review. Moved class, property, domainIncludes, rangeIncludes, inverseOf, supersededBy into meta. - Issue #256: Implementation of HTTP HEAD for all pages. - Issue #1095: ETag and last-modified headers only for successful page requests. - Issue #1098: Added categorization of terms listed on extension home page. - Issue #990: JSON-LD context file should enumerate all terms. This will make it easier to combine the use of [schema.org](http://schema.org/) with other vocabularies and extensions. - Issue #1075: Added markdown format processing of comment fields. This makes the schema editing process easier, especially for cross-referencing related terms. - Issue #178: Integrated rdflib python library. This improves our ability to parse RDFa and JSON-LD schema definitions, and makes unit tests easier to run. - Issue #1109: We now display when a type is superseded.  **Quick fixes and examples**  - \[core\] issue #1097: partOfOrder and partOfSystem are no longer marked as sub-properties of isPartOf since they are not relations between creative works. - \[core\] issue #1102: Examples fixed to avoid “content” attribute on span element in microdata. - \[core\] issue #1066: Cleanup around dataset/DataCatalog association: Renamed containedDataCatalog as includedInDataCatalog, marked it as inverse of dataset and improved wording of both definitions. - \[core\] issue #1073: Removed redundant types listed for branchCode—place already covered LocalBusiness and store. - \[core\] issue #1081: Added AudiobookFormat to the BookFormatType, for consistency. Note that the bib extension also has a dedicated type for describing audio books. - \[core\] issue #950: isBasedOnUrl now called isBasedOn; isBasedOnUrl still exists but is marked as supersededBy isBasedOn. Extended range to include (for now just) CreativeWork, product. - \[core\] issue #929: Marked subEvent and superEvent as inverses of each other. - \[core\] issue #929: The colleague property now also expects URL values (and for JSON-LD therefore expects things not strings by default). - \[core\] various typo fixes (including #1014). - \[core\] issue #966: Fixed bug in PropertyValue JSON-LD example. - \[core\] issue #912: Added education/learning examples (from Phil barker/LRMI): learningResourceType, educationalAlignment, AlignmentObject, educationalFramework, alignmentType, targetName, targetUrl, audience, EducationalAudience, typicalAgeRange, timeRequired, educationalRole. - \[core\] issue #919: Fixed Javascript errors caused by bad markup in 404 pages (published December 10, 2015). - \[core\] issue #899: Bugfix for a few pages that were returning 500 error codes (published December 10, 2015). - \[core\] issue #904: Simplified JSON-LD examples for periodical (published December 10, 2015). - \[core\] issue #1015: Fixed spelling of “content” in FoodEstablishment example. - \[core\] issue #997: Expanded sharedContent to coverage of SocialMediaPosting example. - \[core\] issue #992: Removed an example from QAPage since the example did not illustrate the term's use. - \[core\] issue #836: Markup fixes to examples of PropertyValue. - \[core\] issue #143: Fixed openingHours examples to use span element instead of time, and some time examples to use datetime attribute instead of content. - \[core\] issue #3905: CSS fix to actions document. - \[core\] issue #511: Microdata examples fixed to use “href” example on “link” element instead of “content” on “meta.” - \[core\] issue #533: OpeningHoursSpecification example: Various fixes including better use of “time” element. - \[bib\] issue #984: Bug fixes for [bib.schema.org/Chapter](http://bib.schema.org/Chapter) example. |
| 2.2 (sdo-phobos; November 5, 2015)    | Version 2.2 (working name “sdo-phobos”). This release combines a range of small additions across several areas of [schema.org](http://schema.org/) with an ongoing concern for cleanup and integration of existing vocabulary. Notable additions include ExhibitionEvent, barcode, DataFeed, containsPlace, GeoCircle, geoRadius, geoMidpoint, providerMobility and actionPlatform. A number of changes improve our handling of service description, including the deprecation of the ProfessionalService construct. We have kept all the specific types that were previously considered ProfessionalService but discourage the use of the type “ProfessionalService” since it is easily confused with “service.”                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | **Vocabulary**  - Issue #773: Added actionPlatform as a simpler mechanism to specify the platform for EntryPoint targets. - Issue #823: Marked homeLocation, workLocation as subproperties of location, and marked location as expecting textual values. - Issue #818: Added OfferCatalog for specifying a catalog of offers by an organization or service. - Issue #817: Added providerMobility to describe whether a service provider is at a fixed location or has a dynamic location. - Issue #445: Added ExhibitionEvent and added a superproperty of workPresented and workPerformed to cover event-to-work relationships such as a work being exhibited. - Issue #113: Added GeoCircle as a subtype of GeoShape, providing a more usable mechanism than circle structured text; added geoRadius, geoMidpoint to describe the size and location of these circular areas. - Issue #323: Added locationCreated to CreativeWork. - Issue #811: Renamed containedIn as containedInPlace, and added an inverse containsPlace. - Issue #810: postalCode and addressCountry are now an expected property for GeoShape and GeoCoordinates. Adjusted addressCountry to allow textual values, matching the existing definition. - Issue #801: Broadened award, category, offers to be applicable on service. Extended itemOffered to expect service as a possible value. Added LegalService as a supertype for notary, attorney. Marked ProfessionalService as deprecated, with some explanation, and added a brief account of the relationship with service to some of the more service-oriented local business types for example, LegalService, HomeAndConstructionBusiness. A cluster of construction-related local businesses formerly treated as ProfessionalService continue as HomeAndConstructionBusiness subtypes. Marked attorney as deprecated in favor of LegalService per #784. Added hoursAvailable to service. - Issue #411 clarification and cleanup around areaServed, now marked as a super-property of the more specific eligibleRegion and availableAtOrFrom properties. Cross-referenced eligibleRegion and ineligibleRegion. Marked serviceArea as supersededBy areaServed. Updated the associated types for areaServed to cover those used by its sub-properties. - Issue #808: The address property now anticipates text values, to support unstructured address data. - Issue #802: Referenced world Geotic system from GeoCoordinates properties (elevation, longitude, latitude); made address an expected property for GeoCoordinates and GeoShape. - Issue #796 added offeredBy property to relate an offer to a person or organization. Inverse of makesOffer. - Issue #791 added branchCode to represent codes identifying stores and other business locations. - Issue #790 broadened fileFormat to be usable with CreativeWork, and improved the description. - Issue #687: Added barcode as a subtype of ImageObject. - Issue #688: Added DataFeed and DataFeedItem to represent a data feed of structured items and supportingData for using DataFeed to provide data to a software application. - Issue #767: Added countryOfOrigin property to movie, TVEpisode, TVSeason, and TVSeries. - Issue #768: Added broadcastOfEvent property to BroadcastEvent to allow for specifying the event being broadcasted. - Issue #432: Added organization to domain of alumni and to range of alumniOf properties.  **Site improvements**  - Updated FAQ to clarify CC licensing of docs/examples and use of https: URLs in structured data. - Updated feedback form to permit per-term feedback and to be explicit that feedback messages may be shared with the wider community. - Issue #769: Sorting of multi-inheritance breadcrumbs on term pages. - Issue #761: Updated linking structure in “more…” section of term pages. - Listing of extension contents on extension home pages (eg. [bib.schema.org](http://bib.schema.org/)) - Term counts added to docs/schemas.Html— *the core vocabulary currently consists of 638 types*, *980 properties*, *and 219 enumeration values*. - List of enabled extensions added to docs/schemas.Html. - Various internal software fixes, unit tests and cleanup.  **Quick fixes and examples**  - Issue #764 added example for makesOffer. - Issue #733 added example showing library availability for book. Also added example for library and linked it to openingHoursSpecification as a good example for that too. - Bulk update to examples: Various fixes to html syntax, missing quotes and <meta> tags that should be <link> tags. - Issue #478: Replaced <meta> tags that should be <link> tags in periodical examples. - Several small markup fixes to various examples.  See also issue list for this release.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 2.1 (sdo-ganymede; August 6, 2015)    | Version 2.1 (working name “sdo-ganymede”) includes many small fixes, some new vocabulary, as well as the first release of the “hosted extensions” mechanism, featuring bib(liographic), and auto(mobile) extensions for final review. A pre-release of this version of [schema.org](http://schema.org/) was available for review.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | **Vocabulary**  - Issue #611: Added person as expected value for publisher property. - Issue #596: Documented that affiliation is a sub-property of memberOf. - Issue #207: Added a bridge type under CivicStructure. - Issue #346: Added URL as expected value for genre property. - Issue #374: Added report type under article, and a reportNumber property. - Issue #577: Amended videoFormat to indicate that it is expected on BroadcastEvent and ScreeningEvent, rather than TelevisionStation. - Issue #535: Broadened domain of parentOrganization to allow any organization, rather than only LocalBusiness. Noted parentOrganization and subOrganization as inverses. - Issue #531: Added the lyrics property to MusicComposition. - Issue #518: Renamed paymentDue property to paymentDueDate. Changed paymentStatus property to expect an enumerated value of type PaymentStatusType in addition to text. The options are: PaymentComplete, PaymentDue, PaymentPastDue, PaymentDeclined and PaymentAutomaticallyApplied. - Issue #137: Deprecated UserInteraction and its children in favor of a new type: InteractionCounter. InteractionCounter allows for reporting aggregated statistics by service and type. Thanks elf Pavlik for collaboration. - Issue #526: Added new types LiveBlogPosting, SocialMediaPosting, and DiscussionForumPosting, alongside supporting properties. - Issue #334: Updated the controlled values for accessibilityHazard shown in examples to follow latest community recommendations: “noFlashing” is now “noFlashingHazard,” “noMotionSimulation” is “noMotionSimulationHazard,” and “noSound” is “noSoundHazard.”  **Site improvements**  - Issue #429: Hosted extensions for example, [bib.schema.org](http://bib.schema.org/) are now enabled and linked from “core” pages with appropriate navigation and styling. - Issue #655: Extension definitions now include an isPartOf property to link them to the extension. - Issue #527: Added materials from kickoff workshop in 2011. - Issue #78: Multiple supertypes are now displayed properly. It is possible for several [schema.org](http://schema.org/) types to apply to a single thing, and for a type to have multiple parent types. This is relatively rare, but important to display. For example, anything that is a LocalBusiness is considered both an organization and a place; so all subtypes of LocalBusiness have both as supertypes. We can now show this more clearly, for example, ElectronicsStore. - Added CSS for explicit styling () in releases page during steering group review of candidate releases. - Issue #557, #660, #695, #469: Several DataType-related navigation fixes, following recent modeling changes. - Issue #548: Added a favicon.Ico image. The text is *tiny* and not intended for humans to read. - Behind the scenes: Cleanup and improvements to python code, unit tests, CSS, filetree layout.  **Quick fixes and examples**  - Issue #343: Improved description of sampleType. - Issue #498: We now write “a URL” consistently, rather than sometimes also using “an URL.” - Issue #585: Fix description of netWorth, which erroneously included organization. - #570: Added RDFa and microdata examples for WatchAction. - Added new accessibility examples. - Numerous small documentation fixes for typos, markup validity and textual clarity. - Fixes to several examples including byArtist, place, question/answer, … - Issue #552, #644: Fixes for book examples. - Issue #382: Removed examples that do not reference WebPage from WebPage. - Issue #643: Moved bulk of mainEntityOfPage documentation into dedicated background notes.  See also issue list for this release.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 2.0 (sdo-gozer; May 12, 2015)         | Version 2.0 consolidates and integrates [schema.org](http://schema.org/) 's existing vocabulary. This version features many updated definitions, type/property associations and term names that improve consistency and usability. It also introduces a new extension system. Version 2.0 adds various new terms including mainEntityOfPage and major contributions from the automotive ontology community.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | **Vocabulary**  - Issue #262: Added new vocabulary for car: The new vocabulary includes a number of properties such as: numberOfAirbags, numberOfAxles, numberOfForwardGears, fuelConsumption, fuelEfficiency vehicleEngine, EngineSpecification… Thanks to Martin Hepp, Mirek Sopek, Karol Szczepański and others in the automotive ontology community group. We anticipate substantial additions that build on this foundation will be contributed as an extension. - Issue #301: Added a generic property/values mechanism, building upon PropertyValueSpecification, StructuredValue and value; added PropertyValue and additionalProperty. See examples for usage. This is a lightweight mechanism to allow markup of properties that are not easily mapped to existing [schema.org](http://schema.org/) properties. Whenever possible, it is generally better to use a dedicated [schema.org](http://schema.org/) property if one exists. - Issue #301: Added mainEntityOfPage (and an inverse, mainEntity) to indicate which of the entities mentioned in a page is its primary topic. - Issue #225: Added a schemaVersion property, for use by applications that require more precise referencing of schema versions. - Issue #266: Added OrderItem to allow ParcelDelivery to be tracked per item, not just on an entire order. - Issue #170: Clarifying CommentAction, comment by deprecating UserComments. Several mentions of UserComments removed from other terms. “inLanguage” supersedes “language.” Added a resultComment property. UserInteraction and sub-types will be deprecated. - Issue #300: Answer is now a sub-type of comment. The “question” property expects “question” type for its values (rather than text as in AskAction previously). Added resultComment on ReplyAction. Cleaned up examples. - Issue #130: Amended true and false to be instances (rather than sub-types) of Boolean. - Issue #218: Amended DataType to model it as a sub-class of class, with each datatype for example, Boolean, text, date, DateTime, time, etc. being classes that have a typeOf DataType. DataTypes can have sub-types, for example, integer and float are subtypes of number. - Issue #328: Added ScreeningEvent to support movie/video screenings. - Issue #314: Added MovieClip and VideoGameClip as parallels to TVClip and RadioClip. - Issue #122: Added gtin12 property for product. - Issue #417: Renamed many types and properties, which had overly generic names. This is no cause for alarm, the superseded names can still be used, although we encourage consumers and producers of [schema.org](http://schema.org/) data to move towards the newer terminology. CreativeWorkSeason was season, CreativeWorkSeries was series, SoftwareSourceCode was code, TaxiService was taxi, actionApplication was application, actionOption was option, artMedium was material, artworkSurface was surface, availableOnDevice was device, branchOf was parentOrganization, broadcastTimezone was timezone, codeSampleType was sampleType, containsSeason was season, datasetTimeInterval was temporal, executableLibraryName was assembly, exerciseCourse was course, exerciseRelatedDiet was diet, incentiveCompensation was incentives, includedDataCatalog was catalog, isAccessibleForFree was free, jobBenefits was benefits, runtimePlatform was runtime, serviceArea was area, serviceOutput was produces, softwareRequirements was requirements, targetCollection was collection.  **Site improvements**  - Issue #429: Implementation of new extension system. - Issue #6: Improved 404 handler for missing pages, with support for old-style “/person/minister” extension URLs and action-related “/query-input” pseudo-properties. - Issue #318: Added an *experimental* JSON(-LD) view of the hierarchy. This combines D3 with RDF schema. Thanks to Gregg Kellogg and Sandro Hawke for collaboration. - Various behind-the-scenes improvement to the site software.  **Quick fixes and examples**  - Issue #119: Added a link to GS1's page giving background information on /globalLocationNumber. - Issue #471: Added a JSON example for exampleOfWork and workExample. - Issue #131: Amended category to be applicable to product - Issue #8: Fixed description of box to follow the original rNews definition (instead of accidental copy of polygon). Added explanatory text to GeoShape regarding commas/whitespace. - Issue #224: Changed expected value of openingHours to be text rather than duration, since latter is for ISO formats not our custom micro-syntax. - Issue #112: Clarified that upvoteCount and downvoteCount apply to questions, answers and comments (rather than just to questions). - Issue #103: Clarified description of StructuredValue. - Issue #333: Clarified description of BreadcrumbList. - Issue #456: Generalized numberOfEmployees, to apply to organization as well as to BusinessAudience. - Issue #439: Clarified numberOfItems with multi-page pagination. - Fixed the mapping from DataCatalog to dcat:Catalog - Issue #341: Amended programmingLanguage to expect a language rather than a thing. - Issue #365: Extended award for use on organization, product. - Issue #145: Marked serviceAudience as supersededBy the more general audience property. - Issue #165: Renamed ingredients to recipeIngredient, improved the description, and added ItemList as a possible value for recipeInstructions. - Issue #171: Removed class as a value of query property. - Issue #183: Comment property now applicable to an RsvpAction, and can have comment as values. - Issue #193: aggregateRating and review properties are now expected on brand, event, service. - Issue #247: We now write “antonym” instead of the incorrect “antagonym” in several action definitions. - Issue #316: Marked warrantyPromise as supersededBy warranty. - Issue #213: Amended eligibleRegion and ineligibleRegion to have the same associated types. - Issue #315: Updated BroadcastService, marking it as a kind of service rather than just thing. - Issue #426: Broadened supersededBy to be usable with classes and enumerations. - Issue #366: Reworded description of publication to use “item” instead of a list of types (which had omitted book), and marked it as applicable to CreativeWork. - Issue #288: Added properties related to boarding passes to FlightReservation. - Issue #329: Expanded BroadcastService and added new types CableOrSatelliteService, BroadcastChannel, TelevisionChannel, and RadioChannel to support TV/radio schedules. Thanks, Yves Raimond for careful review. - Issue #335: Added gameLocation to VideoGameSeries. - Issue #336: Added actor and director to series. - Issue #364: Replaced non-existent award type with book in WinAction type. Thanks, unor. - Issue #386: Fixed extra spaces in labels.  See also issue list for this release.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 1.93 (sdo-stantz; February 4, 2015)   | Lots of bugfixes and small improvements, plus new terms to describe visual artworks and invoices.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | **Vocabulary**  - Added VisualArtwork type and supporting properties—artEdition, artform, material, surface. Thanks, Paul Watson. - Added an invoice type to represent invoices/bills, with additional properties totalPaymentDue, minimumPaymentDue, accountId, scheduledPaymentDate, billingPeriod, paymentStatus, referencesOrder. - Fix to allow offers on AggregateOffer. Thanks, Simon Spero, Zinebb. - Expanded the list of types that musicBy applies to, matching those of actor and director. Thanks, Simon Spero. - Adding priceSpecification to TradeAction type, fixing #305. - Adding deliveryMethod to OrderAction type, fixing #306. - Adjusted description of width, height and depth properties to be “the \_\_\_ of the item,” rather than list specific types.  **Site improvements**  - Added support for linking to # examples within per-term pages. Thanks, Wes turner. - Add rangeIncludes to RDFa markup missing from property pages. Thanks, John Walker.  **Quick fixes and examples**  - Fixes to several examples, thanks to Gregg Kellogg. - Fixes to book example, thanks to unor. - Added name property in CreativeWork examples; improved MedicalScholarlyArticle example, marking up the abstract using description—thanks to Dan Scott. - Corrected a case typo in numberOfEmployees. Thanks, Stéphane Corlosquet. - Fixed mistaken use of “MovieGameSeries”; reported by both Gregg and Simon. - Fixed valuePattern definition; it takes text values, not number. Thanks, Holger. - Fixed definitions for fromLocation, toLocation; they do not support numeric values. Thanks, Simon Spero. - Fixed producer property; it takes an organization value, rather than applying to organizations. Thanks, unor. - Fixed typo: clinicalPharmacology is supersededBy clinicalPharmacology. Thanks, Marc. - Fixed an example that used “address” instead of PostalAddress. Thanks, unor. - Added 100+ periods/full stops (“.”) to end each definition.  See also issue list for this release.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 1.92 (sdo-venkman; December 11, 2014) | ItemList and BreadcrumbList changes; sports-related improvements; added a music vocabulary; video games. Also weight/height on person; control and RSVP actions; role names; dated monetary values.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | **Vocabulary**  - Updated ItemList to allow for richer kinds of lists (including ordering), rather than just strings; added BreadcrumbList - The weight and height properties can now be with the person type. Added netWorth to person. Added EmployeeRole. - Added SportsOrganization as a super-type of SportsTeam, representing *sports organizations*, *including sports teams*, *governing bodies*, *and sports associations*. Added a sport property to indicate the associated sport(s) for a SportsOrganization; also added coach and athlete properties. Added numberedPosition property to OrganizationRole. Added homeTeam and awayTeam properties to SportsEvent, alongside a super-property of those, competitor. - Added a VideoGame type with two super-types: SoftwareApplication and a new game type. We anticipate a need for future work around game, see issue #169. VideoGame has cheatCode, gameServer, gamePlatform, playMode and gameTip properties, plus a few supporting types. A property softwareHelp has also been added to SoftwareApplication to indicate supporting documentation. - While integrating VideoGame an issue was raised around the need to describe series of games. As a result we have made some changes to the series type, which previously emphasized only TV and radio series: Added VideoGameSeries, BookSeries, and MovieSeries. The recently added periodical type is also now modeled as a series subtype. Some redundant type/property associations were also tidied up. The existing trailer property can now be used with VideoGame and VideoGameSeries. - Added ControlAction (previously proposed as OperateAction). Add expectsAcceptanceOf on ConsumeAction (previously proposed as “contingentOnOffer”). Added ineligibleRegion (on offer, previously proposed as “notAvailableAtOrFrom”). - Add rsvpResponse, additionalNumberOfGuests properties to the existing RsvpAction type (see also github issue and details). This change also adds an enumeration RsvpResponseType: RsvpResponseYes, RsvpResponseNo, RsvpResponseMaybe. Finally, we add a new possible ActionStatusType: FailedActionStatus, alongside an error property linking an action to more information on the cause of the failure. - Add roleName to role, superceding namedPosition (see also issue and details). - Add to MusicAlbum properties: albumProductionType, albumReleaseType, albumRelease (and inverse, releaseOf). Supporting enumerated types: MusicAlbumProductionType (CompilationAlbum, DemoAlbum, DJMixAlbum, LiveAlbum, MixtapeAlbum, RemixAlbum, SoundtrackAlbum, SpokenWordAlbum, StudioAlbum). MusicAlbumReleaseType (AlbumRelease, BroadcastRelease, EPRelease, SingleRelease). Add new types: MusicRelease, MusicComposition, the latter with properties musicArrangement, composer, firstPerformance, includedComposition, iswcCode, lyricist, musicCompositionForm, musicalKey, recordedAs (inverse: recordingOf). Expand track to allow ItemList values, for lists of MusicRecording, and genre to apply to MusicGroup. - Broadened the description of logo property, to match the types it applies to. See also github issue and details. - Added a DatedMoneySpecification type for non-price monetary values, by analogy with PriceSpecification and its subtypes. Added amount and currency properties and tweaked startDate and endDate property definitions to fit. - See also blog post…  **Site improvements**  - Added links to supporting blog posts for role, action and periodical. - Added “alt” attributes to all image examples. - Fixed the full hierarchy page.  **Quick fixes and examples**  - Several minor bugfixes.  See also issue list for this release.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 1.91 (September 12, 2014)             | Offer/price documentation fixes, cleanup and community contributions.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | - Updated text of the price property to include practical usage guidance, alongside links to information from GS1 to the gtin-related offer properties. - Updated all our examples to follow that guidance; primarily by using priceCurrency and the content = attribute. - Noted our thanks to the OpenDomain project for our domain name. - Updated the text of the “image” property to match its expected types. Thanks, Dan Scott. - Changed spelling of “supercededBy” to the more conventional supersededBy. Thanks, Sachini Aparna Herath. - Noted that “logo” and “photo” are sub-properties of “image.” Thanks, Sachini Aparna Herath, again. - Fixed two syntax errors in examples (store opening hours RDFa; book, PublicationVolume microdata). Thanks, Gregg Kellogg. - Added Tolkien-based examples for exampleOfWork/workExample. Thanks, Dan Scott, again. - Fixed a bug with our UTF-8 support. Thanks, Richard Wallis.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 1.9 (August 18, 2014)                 | Bibliographic improvements (periodical and more) alongside seller/broker/provider clarifications.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Several bibliographic improvements, thanks to the work of the W3C BibExtend community group. Improved handling of periodicals, articles and multi-volume works, introducing types and supporting properties for periodical, PublicationVolume and PublicationIssue. Adds new article properties: pageStart, pageEnd and pagination. CreativeWork gains a convenience inverse of isPartOf called hasPart, as well as a new pair of inverses, workExample and exampleOfWork that link specific and general perspectives on creative works. Many thanks to all the BibExtend group members, to Richard Wallis for chairing, and to Dan Scott for implementing.  Provider/seller vocabulary: This update also clarifies how to use a set of related terms, integrating sections of [schema.org](http://schema.org/) that had developed separately. Full details are documented at W3C and in Github, alongside an overview document. The provider property describes a service provider, service operator, or service performer, while seller describe the entities which sell or offer a service on behalf of an actual service provider. We introduce a more general broker property (replacing the over-specific bookingAgent), as well as deprecating vendor and merchant in favor of seller. Regarding flights and parcel delivery, carrier is superseded by provider. Please also note that flightNumber should now be written in full (i.e., “UA110” rather than just “110”). See the supporting documents for details.  Finally, episodeNumber, seasonNumber and clipNumber (for TV/radio) have been harmonized with the periodicals design (issueNumber and volumeNumber). In each case, both integer and text values are anticipated. A common superproperty, position can also be used. This reflects implementation experience and establishes a model that can be applied elsewhere, for example, ongoing work on describing music.  This update also improves the display and navigation of supersededBy relations between [schema.org](http://schema.org/) properties (e.g., see seller).  The terms of service document was also updated to note that Yandex is now a [schema.org](http://schema.org/) sponsor and to adopt the patent terms used by W3C.  (announcement)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 1.8 (July 28, 2014)                   | Added WebSite type; broadened isPartOf property.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Added a new CreativeWork type, WebSite: “A WebSite is a set of related web pages and other items typically served from a single web domain and accessible via URLs.” also adopts the suggestion made by the BibExtend group and other collaborators, to broaden the isPartOf property, which now relates any CreativeWork to any other CreativeWork. This release also makes the potential actions documentation available in HTML. Several markup fixes from Stéphane Corlosquet, alongside improvements to the consistency of encoding/associatedMedia property definitions thanks to Dan Scott. (announcement)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 1.7 (July 8, 2014)                    | Allows image with ImageObject; adds event organizers, map improvements.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | This release amends the image property, noting that ImageObject is a reasonable value. It also adds an organizer property to event. Changes around map: We add and prefer a “hasMap” property which supersedes the older “map” property, and we add a mapType property which comes with some enumerated values: ParkingMap, SeatingMap, TransitMap, VenueMap. A map might be (but need not be) also an ImageObject. (announcement)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 1.6 (June 16, 2014)                   | Roles, various fixes, site navigation improvements.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | This release introduced the notion of a role type to [schema.org](http://schema.org/). See the blog post for details. The role mechanism applies across all of [schema.org](http://schema.org/), and allows simple statements to be elaborated or qualified, for example with temporal information. Other changes in this release include the addition of a license property, and some documentation of properties used internally by [schema.org](http://schema.org/) 's documentation system (property, class, supersededBy, inverseOf). Fixed an embarrassing typo—“dead”—in the diet property—thanks, Dan Scott. Various other small changes—listed in the preview announcement (announcement and candidate release).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 1.5 (May 27, 2014)                    | Tweaks and fixes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Tweaks to definition of “keywords” to indicate that comma-separated entries are expected. Several typo fixes from Stéphane Corlosquet. Adds a new icaoCode text-valued property for airport. Updated description for flightNumber to note “not including the airline IATA code.” Added missing actions-related definitions (urlTemplate, valueName). (announcement)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 1.4 (May 16, 2014)                    | Examples, examples, examples.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Added two examples to accompany workPerformed. Added several local business, company contact and music event examples. Several glitch and typo fixes including MedicalEnumeration, thanks to Dan Scott. Announcement blog post                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 1.3 (May 1, 2014)                     | Added workPerformed.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Added workPerformed, a relationship between an event and a CreativeWork that is performed at the event.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 1.2 (April 16, 2014)                  | Potential actions.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Introduces vocabulary that enables websites to describe the actions they enable and how these actions can be invoked. (announcement and blog post)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 1.1 (May 4, 2014)                     | Reservations, Q/A and more.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Added a reservation schema. Question/answer sites. Order changes. Added EmailMessage.  (1) this release of [schema.org](http://schema.org/) adds a finalized reservations schema, which refines earlier proposals discussed in the web schemas community over the last year. See wiki for details.  The reservations vocabulary includes: Reservation, ReservationPackage, ReservationStatusType, ticket, flight, EventReservation, FlightReservation, TrainReservation, BusReservation, TaxiReservation, LodgingReservation, RentalCarReservation, ProgramMembership, seat, vehicle, airline, FoodEstablishmentReservation, TrainTrip, car, BusTrip, taxi.  (2) Q/A sites  A simple vocabulary for question/answer and FAQ sites. It adds types for question, answer, and QAPage.  (3) adds a type EmailMessage, analogous to the existing WebPage type.  (candidate release drafted as “1.0 g”; not formally announced but included in the change to github-based publishing)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 1.0f (February 5, 2014)               | Not-for-profit offer and other fixes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | This version adapts the wording around the offer type to suit non-profit scenarios, such as libraries. Thanks to Dan Scott and the BibExtend group for these proposals. This change broadens the definition of offer and makes associated changes to ItemAvailability and OfferItemCondition, typically rewording “the item for sale” to simply say “the item.” The itemOffered property is now defined more appropriately as “the item being offered.” rather than “…Sold.” The “seller” property is now defined as “the organization or person making the offer,” a compromise to support its use for more kinds of offer. (candidate release and announcement)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 1.0e (December 4, 2013)               | Accessibility properties and order type.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | This release includes a schema for describing orders, as well as the accessibility properties for CreativeWork (see discussion). The W3C WebSchemas wiki has the order proposal and draft schema. For accessibility, see the blog post for more background on the collaborations involved. See also wiki materials and the draft schema. (announcement)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 1.0d (November 21, 2013)              | TV/radio; civic services; ContactPoint event and organization improvements.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | TV/radio improvements in collaboration with BBC and EBU—see guest blog post by Yves Raimond. For example see TVEpisode.  For background see the TV/radio wiki entry.  Civic services (which includes ContactPoint) was blogged when first discussed. See also wiki entry. Example type: GovernmentService.  Event improvements: Wiki entry. Organization improvements: Wiki entry. In particular, this update added department, and subOrganization properties.  (blog announcement).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 1.0c (August 7, 2013)                 | Actions (in the past).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Introduced a (past-tense) actions vocabulary (see wiki) this updated added an action type, supporting properties, and a substantial set of subtypes. It was followed in 2014 by a mechanism for describing potential actions. (announcement)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 1.0b (July 24, 2013)                  | Added sameAs; broadened citation.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Adds sameAs property to thing that makes it easier to indicate identifying URLs for entities being described (wiki). The citation property has been moved up to CreativeWork, from MedicalScholarlyArticle (wiki). Thanks to the BibExtend group for suggesting this small but useful improvement.  (announced)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 1.0a (April 5, 2013)                  | Adds LRMI, datasets, audience, technical publishing vocabulary and more.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | For LRMI (learning resource metadata initiative), a collaboration co-led by Association of Educational Publishers (AEP) and creative commons: Added several properties, mainly to CreativeWork. Added AlignmentObject type, for aligning content to educational coding schemes. (see wiki).  Added dataset type (collaboration building upon work at W3C and elsewhere). See also blog, wiki.  Added audience and related types, useful for LRMI and other applications (wiki).  Added technical publishing vocabulary: TechArticle, APIReference, code. See also early blog post and wiki entries for TechArticleSchema, APIReferenceSchema and CodeSchema.  (announcement)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 0.99 (November 8, 2012)               | Added good relations e-commerce vocabulary.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Added substantial e-commerce vocabulary based on good relations; re-engineered site to accept RDFa/RDFS schema definitions from community.(wiki) (announcement blog post and email from Martin Hepp)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 0.98 (October 18, 2012)               | Fix for requiresSubscription property.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | A minor bugfix release, which improved the documentation of requiresSubscription property. We now encourage its Boolean value to be represented as true/false rather than yes/no.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 0.97 (July 26, 2012)                  | Added DateTime, time datatypes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Added two datatypes in preparation for good relations integration. (announcement)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 0.96 (July 18, 2012)                  | Added additionalType property.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | Added additionalType property (wiki). “An additional type for the item, typically used for adding more specific types from external vocabularies in microdata syntax. This is a relationship between something and a class that the thing is in. In RDFa syntax, it is better to use the native RDFa syntax—the “typeof” attribute—for multiple types. [Schema.org](http://schema.org/) tools may have only weaker understanding of extra types, in particular those defined externally.” (announcement)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 0.95 (June 26, 2012)                  | Added medical/health vocabulary.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | This release added substantial vocabulary in the medical/health domain (around 100 classes, 200 properties). The additions are mainly organized beneath the MedicalEntity type. An overview document is also provided. From the blog post:  “This collaborative project drew upon search expertise from the [schema.org](http://schema.org/) partners but also gained immeasurably through feedback from expert reviewers including the US NCBI; physicians at Harvard, Duke and other institutions, as well as from several health web sites. Contributions from the W3C healthcare and Lifesciences group and web schemas community also helped bridge the complex worlds of web standards, search and medicine/healthcare.”  (announcement)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 0.91 (April 21, 2012)                 | Removed plural “s” suffix from repeatable properties; added comment type, SoftwareApplication vocabulary.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Added new properties per Singularity proposal: 23 changes: actor, album, attendee, award, blogPost, colleague, contactPoint, employee, encoding, episode, event, founder, map, member, parent, performer, photo, review, season, sibling, significantLink, subEvent, track. Each of these originally had a plural “s” to indicate repeatability. After discussion in the W3C WebSchemas group, the consensus was that this was confusing and worthwhile changing.  This revision added a new type, “Comment,” whose super-type is CreativeWork (wiki)  Also adds SoftwareApplication and supporting vocabulary (wiki, original proposal), including MobileApplication, WebApplication subtypes.  Converged URL/Url spelling. After WebSchemas discussion, consensus was: For each of embedURL, contentURL, downloadURL, ensure there is an equivalent property named with mixed-case: “embedUrl,” “contentUrl,” “downloadUrl.”                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

**A** acceptedAnswer, accessibilityHazard, accessibilitySummary, accessMode, accessModeSufficient, accommodationCategory, accommodationFloorPlan, accomodation, accountId, accountMinimumInflow, accountOverdraftLimit, acquireLicensePage, actionableFeedbackPolicy, ActionAccessSpecification, actionApplication, actionOption, actionPlatform, ActionStatusType, ActivationFee, additionalNumberOfGuests, additionalProperty, additionalType, addressCountry, addressLocality, addressRegion, AdministrativeArea, AdvertiserContentArticle, AggregateOffer, AggregateRating, albumProductionType, albumRelease, albumReleaseType, AlignmentObject, alignmentType, AllergiesHealthAspect, alternateName, alumniOf, amenityFeature, AmpStory, AMRadioChannel, AnalysisNewsArticle, announcementLocation, ApartmentComplex, APIReference, APIReferenceSchema, applicantLocationRequirements, applicationContact, applicationDeadline, applicationStartDate, ArchiveComponent, archivedAt, archiveHeld, ArchiveOrganization, areaServed, arrivalBoatTerminal, artEdition, artMedium, artworkSurface, AskAction, AskPublicNewsArticle, associatedClaimReview, associatedDisease, associatedMedia, associatedMediaReview, associatedReview, associated, AudiobookFormat, AudioObject, AudioObjectSnapshot, AuthenticContent, availableAtOrFrom, availableLanguage, availableOnDevice, awayTeam **B** BackgroundNewsArticle, BackOrder, bankAccountType, bccRecipient, BedType, beneficiaryBank, BibExtend, billingDuration, billingPeriod, billingStart, BioChemEntity, bioChemInteraction, bioChemSimilarity, biologicalRole, Bioschemas, blogPost, BlogPosting, BoatReservation, BoatTerminal, BoatTrip, BodyMeasurementTypeEnumeration, BookFormatType, bookingAgent, BookSeries, boolean, branchCode, branchOf, BreadcrumbList, breastfeedingWarning, BroadcastChannel, BroadcastEvent, broadcastFrequency, BroadcastFrequencySpecification, broadcastFrequencyValue, broadcastOfEvent, BroadcastRelease, BroadcastService, broadcastSignalModulation, broadcastSubChannel, broadcastTimezone, brokenlinkcheck, BrokerageAccount, BusinessAudience, businessFunction, BusReservation, BusTrip, byArtist, byDay, byMonth, byMonthDay, byMonthWeek **C** CableOrSatelliteService, callSign, CampingPitch, cashBack, CategoryCode, CategoryCodeSet, CatholicChurch, ccRecipient, cheatCode, checkinTime, checkoutTime, chemicalComposition, chemicalRole, ChemicalSubstance, childTaxon, CivicStructure, claimInterpreter, ClaimReview, claimReviewed, CleaningFee, clinicalPharmacology, clipNumber, codeSampleType, CodeSchema, codeValue, collectionSize, CommentAction, CommentPermission, commentTime, compatability, competencyRequired, CompilationAlbum, CompleteDateFeed, CompoundPriceSpecification, ComputerLanguage, ConsumeAction, contactlessPayment, ContactPoint, containedDataCatalog, containedIn, containedInPlace, containsPlace, containsSeason, contentLocation, contentRating, contentReferenceTime, contentURL, contingentOnOffer, ControlAction, cookTime, copyrightNotice, Corlosquet, CorrectionComment, correctionsPolicy, countryOfAssembly, countryOfLastProcessing, countryOfOrigin, courseCode, courseCredits, courseCreditsUnit, CourseInstance, courseMode, coursePrerequisites, courseWorkload, CreativeWork, CreativeWorks, CreativeWorkSeason, CreativeWorkSeries, credentialCategory, CreditCard, creditText, CriticReview, cssSelector, currenciesAccepted, currentExchangeRate, customerRemorseReturnFees, customerRemorseReturnLabelSource, customerRemorseReturnShippingFeesAmount **D** DataCatalog, DataDownload, DataFeed, DataFeedItem, datamodel, datasetTimeInterval, DataType, DataType-related, DataTypes, DatedMoneySpecification datePosted, datePublished, DateTime, dcat, dcterms, dds, DefinedRegion, DefinedTerm, DefinitiveLegalValue, deliveryLeadTime, DeliveryMethod deliveryTime, DemoAlbum, departureBoatTerminal, DigitalDocument, DigitalDocumentPermission, DigitalDocumentPermissionType, directApply, disambiguatingDescription, discountCurrency, DiscussionForumPosting, DistanceFee, diversityPolicy, diversityStaffingReport, DJMixAlbum, DModel, doesNotShip, domainIncludes, domiciledMortgage, downloadURL, Downpayment, downvoteCount **E** earlyPrepaymentPenalty, editEIDR, educationalAlignment, EducationalAudience, educationalCredentialAwarded, educationalFramework, educationalLevel, EducationalOccupationalCredential, EducationalOccupationalCredentials, EducationalOccupationalProgram, EducationalOrganization, educationalProgramMode, educationalRole, educationalUse, EducationEvents, educationRequirements, eduQuestionType, EffectivenessHealthAspect, ElectronicsStore, eligibleRegion, EmailMessage, embeddedTextCaption, embedURL, emphasised, EmployeeRole, EmployerAggregateRating, employerOverview, EmployerReview, employmentUnit, encodesBioChemEntity, encodesCreativeWork, encodingFormat, endDate, endOffset, EndorsementRating, endTime, EnergyConsumptionDetails, EnergyEfficiencyEnumeration, energyEfficiencyScaleMax, energyEfficiencyScaleMin, EnergyStarEnergyEfficiencyEnumeration, EngineSpecification, EntryPoint, eocred-schema, episodeNumber, EPRelease, equivalentProperty, estimatedCost, estimatedSalary, ETag, ethicsPolicy, EUEnergyEfficiencyEnumeration, eventAttendanceMode, EventMovedOnline, EventReservation, eventSchedule, EventSeries, eventStatus, EvidenceLevelA, exampleOfWork, exceptDate, ExchangeRateSpecification, exchangeRateSpread, executableLibraryName, exerciseCourse, ExercisePlan, exerciseRelatedDiet, ExhibitionEvent, expectsAcceptanceOf, experienceInPlaceOfEducation, experienceRequirements **F** FailedActionStatus, FAQPage, favour, fileFormat, filetree, financialAidEligible, firstPerformance, flightNumber, FlightReservation, floorLevel, floorLimit, FloorPlan, floorSize, FMRadioChannel, FoodEstablishment, FoodEstablishmentReservation, fromLocation, fuelConsumption, fuelEfficiency, FundingAgency, FundingScheme **G** gameLocation, gamePlatform, gameServer, gameTip, generalised, GeoCircle, geoContains, GeoCoordinates, geoCoveredBy, geoCovers, geoCrosses, geoDisjoint, geoEquals, geoIntersects, geoMidpoint, geoOverlaps, geoRadius, GeoShape, GeospatialGeometry, geospatiallyXyz, Geotic, geoTouches, geoWithin, geoXyz, GettingAccessHealthAspect, globalLocationNumber, GoodRelations, governmentBenefitsInfo, GovernmentBenefitsType, GovernmentService, gracePeriod, grantsCredential **H** hasBioChemEntityPart, hasBioPolymerSequence, hasBroadcastChannel, hasCategoryCode, hasCourse, hasCourseInstance, hasCredential, hasDefinedTerm, hasDigitalDocumentPermission, hasEnergyConsumptionDetails, hasEnergyEfficiencyCategory, hasHealthAspect, hasMap, hasMeasurement, hasMenu, hasMenuItem, hasMenuSection, hasMerchantReturnPolicy, hasMolecularFunction, hasOccupation, hasPart, hasRepresentation, hasVariant, HealthAspectEnumeration, healthCondition, HealthInsurancePlan, HealthTopicContent, highPrice, holdingArchive, HomeAndConstructionBusiness, homeLocation, homeTeam, hoursAvailable, HowItWorksHealthAspect, HowOrWhereHealthAspect, HowTo, HowToItem, HowToSection, HowToStep, HowToSupply, HowToTool, HyperToc, HyperTocEntry **I** icaoCode, ImageGallery, ImageObject, ImageObjectSnapshot, incentiveCompensation, inChI, inChIKey, includedComposition, includedDataCatalog, includedInDataCatalog, includesObject, inCodeSet, ineligibleRegion, IngredientsHealthAspect, inLanguage, inLanguage’, inProductGroupWithID, InteractionCounter, interactionStatistic, interpretedAsClaim, inverseOf, InvestmentFund, InvoicePrice, isAccessibleForFree, isBasedOn, isBasedOnUrl, isEncodedByBioChemEntity, isInvolvedInBiologicalProcess, isLiveBroadcast, isLocatedInSubcellularLocation, isPartOf, isPartOfBioChemEntity, isRelatedTo, isResizable, isSimilarTo, issueNumber, isVariantOf, iswcCode, ItemAvailability, itemCondition, itemDefectReturnFees, itemDefectReturnLabelSource, itemDefectReturnShippingFeesAmount, ItemList, itemOffered, itemReviewed, iupacName, Iussue **J** Javascript, jobBenefits, jobLocationType, JobPosting, JobPostings, jobTitle, jsonldcontext **K** knowsAbout, knowsLanguage **L** layoutImage, LearningResource, learningResourceType, leaseLength, LegalForceStatus, LegalService, LegalValueLevel, legislationIdentifier, legislationJurisdiction, LegislationObject, legislationType, LibrarySystem, linkRelationship, LinkRole, liographic, ListPrice, LiveAlbum, LiveBlogPosting, loanMortgageMandateAmount, loanPaymentAmount, loanPaymentFrequency, loanRepaymentForm, loanType, LocalBusiness, localised, locationCreated, LocationFeatureSpecification, LockerDelivery, LodgingBusiness, LodgingReservation, lowPrice **M** mainEntity, mainEntityOfPage, maintenance, makesOffer, mapType, marginOfError, materialExtent, MathSolver, maximumAttendeeCapacity, maximumEnrollment, measurementTechnique, MeasurementTypeEnumeration, MediaGallery, mediaItemAppearance, MediaManipulationRatingEnumeration, MediaObject, MediaReview, MediaReviewItem, MediaSubscription, MedicalEntity, MedicalEnumeration, MedicalScholarlyArticle, MedicalSpecialty, memberOf, membershipPointsEarned, menuAddOn, MenuItem, MenuSection, MerchantReturnPolicy, MerchantReturnPolicySeasonalOverride, MinimumAdvertisedPrice, minimumPaymentDue, MissingContext, missionCoveragePrioritiesPolicy, MixtapeAlbum, MobileApplication, MolecularEntity, molecularFormula, molecularWeight, MonetaryAmount, MonetaryAmountDistribution, MonetaryGrant, MoneyTransfer, monoisotopicMolecularWeight, monthlyMinimumRepaymentAmount, monthsOfExperience, MortgageLoan, MovieClip, MovieGameSeries, MovieSeries, MusicAlbum, MusicAlbumProductionType, MusicAlbumReleaseType, musicalKey, musicArrangement, musicBy, MusicComposition, musicCompositionForm, MusicGroup, MusicRecording, MusicRelease **N** namedPosition, negativeNotes, netWorth, NewsArticle, NewsMediaOrganization, NiemanLab, noFlashing’, noFlashingHazard’, noMotionSimulation’, noMotionSimulationHazard’, nonprofitStatus, NonprofitType, noSound, noSoundHazard, notAvailableAtOrFrom, NoteDigitalDocument, numberedPosition, numberOfAirbags, numberOfAxles, numberOfBathroomsTotal, numberOfBedrooms, numberOfCredits, numberOfEmployees, numberOfForwardGears, numberOfFullBathrooms, numberOfItems, numberOfLoanPayments, numberOfRooms **O** occupationalCategory, occupationalCredentialAwarded, OccupationalExperienceRequirements, OccupationalTherapy, occupationLocation, OfferCatalog, offeredBy, OfferForLease, OfferForPurchase, OfferItemCondition, OfferShippingDetails, OpenDomain, openingHours, OpeningHoursSpecification, OperateAction, OpinionNewsArticle, OrderAction, orderedItem, OrderItem, Organisation, OrganizationRole, originalMediaContextDescription, originalMediaLink, ownershipFundingInfo **P** pageEnd, pageStart, ParcelDelivery, ParcelService, parentItem, parentOrganization, parentTaxon, ParkingMap, partOfOrder, partOfSystem, partOfTrip, paymentAccepted’, PaymentAutomaticallyApplied, PaymentComplete, PaymentDeclined, paymentDue, paymentDueDate, PaymentPastDue, paymentStatus, PaymentStatusType, performTime, permissionType, permittedUsage, petsAllowed, phane, playMode, PodcastEpisode, PodcastSeason, PodcastSeries, positiveNotes, PostalAddress, postalCode, PostalCodeRangeSpecification, potentialAction, potentialUse, PregnancyHealthAspect, PreOrder, PreOrderAction, prepTime, PreSale, prescriptionStatus, PresentationDigitalDocument, previewUrl, priceComponentType, PriceComponentTypeEnumeration, priceCurrency, priceCurrency’, PriceSpecification, priceType, PriceTypeEnumeration, ProductCollection, ProductGroup, productGroupID, ProductReturnPolicy, ProfessionalService, ProfessionalService’, ProgramMembership, programmingLanguage, programPrerequisites, PronounceableText, PropertyValue, PropertyValueSpecification, providerMobility, providesBroadcastService, publicAccess, PublicationIssue, PublicationVolume, PublicHolidays, PublicToilet, publishingPrinciples **Q** QAPage, QualitativeValue, QuantitativeValue, QuantitativeValueDistribution **R** RadioBroadcastService, RadioChannel, RadioClip, Raimond, rangeIncludes, ratingExplanation, ratingValue, rdf, RDFa, rdflib, rdfs, ReadPermission, RealEstateListing, ReceiveAction, recipeIngredient, recipeInstructions, recipeYield, recognizedBy, recordedAs, recordingOf, recourseLoan, referencesOrder, releaseOf, relevantOccupation, remainingAttendeeCapacity, RemixAlbum, renegotiableLoan, RentalCarReservation, RepaymentSpecification, repeatCount, repeatFrequency, ReplyAction, ReportageNewsArticle, reportNumber, requiredQuantity, requiresSubscription, ResearchProject, ReservationPackage, ReservationStatusType, restockingFee, RestrictedDiet, resultComment, ReturnFeesEnumeration, returnLabelSource, ReturnLabelSourceEnumeration, returnMethod, ReturnMethodEnumeration, returnPolicyCountry, returnPolicySeasonalOverride, returnShippingFeesAmount, reviewAspect, reviewBody, ReviewNewsArticle, rNews, roleName, RsvpAction, rsvpResponse, RsvpResponseMaybe, RsvpResponseNo, RsvpResponseType, RsvpResponseYes, runtimePlatform **S** Sachini, SafetyHealthAspect, salaryUponCompletion, SalePrice, sameAs, sampleType, SatiricalArticle, scheduledPaymentDate, scheduleTimezone, schemaorg, schemaVersion, SchoolDistrict, ScreeningEvent, sdDatePublished, sdLicense, sdo-callisto, sdo-callisto’, sdo-deimos, sdo-deimos’, sdo-enceladus, sdo-enceladus’, sdo-ganymede, sdo-ganymede’, sdo-gozer, sdo-makemake, sdo-makemake’, sdo-phobos, sdo-phobos’, sdo-stantz, sdo-telesto, sdo-telesto’, sdo-venkman, sdopythonapp, sdPublisher, seasonNumber, SeatingMap, secondaryPrevention, SeekToAction, serviceArea, serviceAudience, serviceOutput, serviceType, sharedContent, SheetMusic, ShippingDeliveryTime, shippingDestination, shippingDetails, shippingLabel, shippingRate, ShippingRateSettings, shippingSettingsLink, ShortStory, significantLink, SingleRelease, sizeGroup, SizeGroupEnumeration, sizeproperty, SizeSpecification, sizeSystem, SizeSystemEnumeration, SkiResort, SKOS, SocialMediaPosting, SoftwareApplication, softwareHelp, softwareRequirements, SoftwareSourceCode, SolveMathAction, Sopek, SoundtrackAlbum, spatialCoverage, speakable, SpeakableSpecification, SpeakableSpecification-related, SpecialAnnouncement, specialOpeningHoursSpecification, spokenByCharacter, SpokenWordAlbum, SportsActivityLocation, SportsEvent, SportsOrganization, SportsTeam, SpreadsheetDigitalDocument, starRating, startDate, startOffset, startTime, StatisticalPopulation, StatusEnumeration, StructuredValue, StudioAlbum, subEvent, subjectOf, subOrganization, subproperties, subproperty, subtitleLanguage, subTrip, suggestedAge, suggestedAnswer, suggestedMeasurement, suitableForDiet, supercededBy’, superceding, superEvent, superproperty, supersededBy, supportingData **T**

targetCollection, targetName, targetUrl, TaxiReservation, TaxiService, taxonomicRange, taxonRank, TechArticle, TechArticleSchema,

TelevisionChannel, TelevisionStation, temporalCoverage, termDuration, termsPerYear, TextDigitalDocument, tickerSymbol, timeOfDay, timeRequired, timeToComplete, timezone, titleEIDR, tocContinuation, tocEntry, toLocation, toRecipient, totalJobOpenings, totalPaymentDue, totalPrice, totalTime, tourBookingPage, TouristAttraction, TouristDestination, TouristTrip, touristType, TradeAction, trainingSalary, TrainReservation, TrainTrip, TransitMap, transitTimeLabel, TravisCI, TVClip, TVEpisode, TVSeason, TVSeries, typeof, typeof’, typicalAgeRange, typicalCreditsPerTerm,

**U** UnitPriceSpecification, unnamedSourcesPolicy, upvoteCount, url-addressable, urlTemplate, usageInfo, usecase, UserComments, UserInteraction, UserReview **V** validFor, validIn, validThrough, valueName, valuePattern, valueReference, variableMeasured, variablesMeasured, variesBy, vehicleEngine, VenueMap, verificationFactCheckingPolicy, videoFormat, VideoGallery, VideoGame, VideoGameClip, VideoGameSeries, VideoObject, VideoObjectSnapshot, VirtualLocation, VisualArtwork, volumeNumber **W** warrantyPromise, WatchAction, WearableMeasurementTypeEnumeration, WearableSizeGroupEnumeration, WearableSizeSystemEnumeration, WebAPI, WebApplication, WebContent, webFeed, WebPage, WebPageElement, WebPageElement’, webschemas, WebSite, Wikibase, Wikidata, WinAction, WorkBasedProgram, WorkersUnion, workExample, workLocation, workPerformed, workPresented, WritePermission **X** Xpath, xpath’ **Y** yearBuilt **Z** Zinebb

## REFERENCES

## Citing Literature

[Download PDF](https://asistdl-onlinelibrary-wiley-com.sire.ub.edu/doi/pdf/10.1002/asi.24744)

back