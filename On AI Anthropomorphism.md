---
title: On AI Anthropomorphism
source: https://medium.com/human-centered-ai/on-ai-anthropomorphism-abff4cecc5ae
author: "[[Chenhao Tan]]"
published: 2023-04-10
created: 2026-04-29
description: by Ben Shneiderman (University of Maryland, US) and Michael Muller (IBM Research, US)
tags:
  - op/doc/tool
DOI:
Type:
year:
---
![](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*O2dNhJcuNgI7E_sPkK9Mog.png)

Is AI’s nature as a tool or an anthropomorphized social agent? Source: Dreamstudio.

## Introduction

Anthropomorphism is the act of projecting human-like qualities or behavior onto non-human entities, such as when people give animals, objects, or natural phenomena human-like characteristics or emotions. There have been long-standing debates over the use of anthropomorphic designs for AI-based systems, stretching back (at least) to an early panel at the ACM Computer-Human Interaction Conference titled, “Anthropomorphism: from ELIZA to Terminator 2” (Don et al., 1992).

The design issues surrounding anthropomorphism include whether:

1. a human agent-like character should be shown on a screen,
2. computers should present themselves as human-like social actors with text or voice user interfaces,
3. computer prompts or responses should use first person pronouns, e.g., “I would be glad to help you”, and
4. users prefer alternative, *direct manipulation* designs that allow them to click, drag, zoom, or touch.

This article features a series of e-mail exchanges between [Ben Shneiderman](https://www.cs.umd.edu/users/ben/) and [Michael Muller](https://research.ibm.com/people/michael-muller) on the topic of anthropomorphism in human-centered AI systems. Their debate began when Ben criticized GPT-4’s use of “I” in its responses in his 94th weekly [Google Group note on Human-Centered AI (March 15, 2023](https://groups.google.com/g/human-centered-ai/)). Michael responded, triggering a lively email exchange.

Michael and Ben continued to exchange notes during March and April 2023, and Eds. Chenhao Tan, Justin Weisz, and Werner Geyer suggested that their arguments be made public. This article represents a lightly-edited version of the email exchange, segmented into four parts:

We conclude the article with a [brief summary of the debate](#bb4b), written by Eds. Chenhao Tan and Justin Weisz.

During the exchange, additional people were brought into the conversation to add commentary and perspective. We will be publishing their perspectives in upcoming articles ([see below for a list](#ef02)). If you would like to add your voice to the mix, please reach out to [Chenhao Tan](mailto:chenhao@uchicago.edu).

## The Debate

### Part I — On anthropomorphism

**Ben Shneiderman**: A particular concern that I have is the way GPT-4 output uses first person pronouns, suggesting it is human, for example: “My apologies, but I won’t be able to help you with that request.” The simple alternative of “GPT-4 has been designed by OpenAI so that it does not respond to requests like this one” would clarify responsibility and avoid the deceptive use of first person pronouns. In my world, machines are not an “I” and shouldn’t pretend to be human.

**Michael Muller**: First, we humans have been addressing artifacts and natural entities as person-like beings for a very long time. Demetrius of Phelerum wrote about prosopopoeia (personification) before 280 BCE. The [Wikipedia entry about prosopopoeia](https://en.wikipedia.org/wiki/Prosopopoeia) provides an example from the Book of Sirach, in which “Wisdom sings her own praises, / among her own people she proclaims her glory.” There are many accounts of created beings that take on a form of awareness or agency, from the historical golem (not the Tolkien one, called “gollum”) to Mary Wollstonecraft Shelley and all the way back to the myth of Pygmalion and Galatea.

So I think there is plenty of precedent for us to address made-things as having human-like qualities. Reeves and Nass (1996) pursued this concept as a research program, specifically about computers as social actors. See also my critique of their position in Interacting with Computers (Muller, 2004), in which I reviewed the longer history of personification.

Second, we are just now exploring what it means for an algorithm to be a non-determinate conversational partner. The LLMs are, I agree, stochastic parrots, and hence “mind”-less. Nonetheless, they have a convincing social presence. We don’t yet know what we can do with that social presence. (I say “do” in a pragmatism sense of “what we can use it for.”) Beyond all the current irritating (and sometimes dangerous) AI hype, there are research questions here about what kind of entities we are building, and about how we will relate to them. IMHO, we don’t know yet.

I suspect that we will need to break down our human / non-human binary into a dimension, or into multiple dimensions. In a conventional EuroWestern way of thinking, we already do this in our relationship to animals. For most of us, a rock is just a rock (but note that some Indigenous and Aboriginal philosophies would challenge that statement). Similarly, some animals — newts, for example — have interesting personhood only in Capek’s work (Capek et al., 1996), but not in our interactions with them (and I remember that Capek’s companion work about relationships-gone-wrong, was about robots (Capek, 2004)). Elizabeth Phillips and colleagues (2016) have explored the deeper relationships that we have with some animals, with dogs being the primary example of a social presence. See also Haraway’s (2003) concepts in companion species, and intriguingly Fijn’s (2011) work on human relationships with Mongolian lasso-pole ponies. And so, there are gradations to consider, rather than a simple human / non-human distinction related to animals.

Phillips et al. (2016) were using human-animal relationships to think about human-AI relationships. I think that, as with animals, there are degrees of sociality, or degrees of social presence, that may be applicable to computational things. I don’t think we know enough yet to foreclose these possibilities.

If you ask me about the themes in your post about fraud and manipulation, I am right beside you about protecting people, and I would support strict regulations to protect people from AIs that are feigning human-ness in order to fool people. To me, that is a separate set of concerns from how we explore new technologies, newly-publicized technologies, and newly-reinterpreted technologies (all of which may be used for pondering possible futures), so long as our explorations are honest, fully-disclosed, and without malice.

### Part II — Anthropomorphic computing systems

**Ben Shneiderman:** Yes, I agree that personhood has been used for artifacts from Aristotle and will continue to be used. I don’t think that I can kill this zombie idea.

However, zombie ideas can have problematic impacts. It’s one thing for an ordinary artifact user to make human-like references for boats, cars, or Roombas, but I see it as a problem when designers use that language, resulting in poor products. The long history of failed anthropomorphic systems goes back even before Microsoft BOB and Clippie, but it has continued to produce billion dollar failures. The most recent serious deadly design mistake was Elon Musk’s insistence that since human drivers used only eyes, his Teslas would use only video. By preventing the use of radar or LIDAR, over the objections of his engineers, he has designed a suboptimal system that produces deadly results.

For me, metaphors matter (Lakoff & Johnson, 2006), so designers should be alert to how their belief that computers should communicate in natural language, just like people do, lead to their failure to use computer capabilities such as information abundant displays of visual information.

Further support for shifting from anthropomorphism to designs that give users greater control comes from sociologist Lewis Mumford. I was strongly influenced by his classic book, *Technics and Civilization* (1936)*,* which offers a clear analysis in the chapter on “The Obstacle of Animism.” Mumford describes how initial designs based on human or animal models are an obstacle that needs to be overcome in developing new technologies: “the most ineffective kind of machine is the realistic mechanical imitation of a man\[/woman\] or another animal.” Mumford’s point is that the distinctive capabilities of technology, such as wheels, jet engines, or high resolution computer displays may be overlooked if designers stick with the “bio-inspired” notions, such as conversational interfaces. Therefore, it is understandable that anthropomorphic phrasing would be offered as an initial design for AI systems, but getting beyond this stage will enable designers to take better advantage of sophisticated algorithms, huge databases, superhuman sensors, information abundant displays, and superior user interfaces.

**Michael Muller**: For me, the core question is: “How Can Humans Relate to Non-Human Intelligences?” Anthropomorphism is one possible response, but not the only one, and not the only relevant topic.

You and I agree that words matter, and that metaphors matter. That’s why I was so interested in the work by Phillips et al. (2016). They were seeking useful metaphors (plural) for AIs (plural) by looking at human relationships with animals. That’s true, in a different way, in much of Haraway’s work (2003).

As I wrote earlier, my language for our shared question is: “How Can Humans Relate to Non-Human Intelligences?” For me, that is closer to the core issue, and anthropomorphism is a sub-question among many possible explorations of strange non-human entities. Anthropomorphism is one metaphorical approach to new ideas and new entities. In my view, metaphors become figures of thought, through which we can articulate some of that strangeness. (Following contemporary rhetorical theory, I wrote “figures of thought” (e.g., Lakoff, 1986; Lakoff & Johnson, 2008) not just “figures and speech,” and again I think we agree.) I’d like us to explore metaphors about LLMs, to help us to think about “what” they “are,” but also what they might be, or might become.

Phrased in that way, I hope that our use of (human) language can help us to open a conceptual space about the nature of the computational things that we are making and interacting with. I think metaphor will be useful, and so will the broader category of analogy. These things are now VERY layered. For example, while everyone is talking about LLMs and FMs, some of us (including you and I) are thinking hard about the UIs to those LLMs.

The LLM layer is probably a “we” — after all, it contains the non-consensually harvested materials from hundreds of thousands of humans. Or maybe I should have said “captured materials.” Or “stolen voices.”

The UI layer may be an “I”, because that’s the style of interaction that seems to work for us humans. I think you would prefer that the UI layer is an “it” — or maybe that it should refer to itself in the third person, like the injured ancillary (cyborg soldier) in Ann Leckie’s Imperial Radch books (Leckie, 2013) who tries to dissuade a rescue attempt by saying, “Fleet Captain… with all respect, this injury is too severe to be worth repairing.”

Characteristically, I’m more interested in opening possibilities, than in preventing failures. Yes, Clippy and BOB were failures, but that doesn’t mean that all personifications will be failures. Our experiments with a personified UI to a LLM have been quite successful. No one who uses our Programmer’s Assistant prototype (Ross et al. 2023) is confused about its ontological status. No one mistakes it as anything other than a smart toaster, but it turns out to be a transformatively helpful smart toaster. (Not “transformatively smart,” just “transformatively helpful.”) So now we have Clippie and BOB as examples of failures, but we also have our Programmer’s Assistant as an example of a success (and perhaps some of the older Nass and Reeves’ experiments, too). Anthropomorphism doesn’t necessarily lead to problems.

IMHO, UIs to LLMs are a genuinely new design space. We don’t yet know what the crucial factors of this space are. I suspect that those factors will interact with one another. For example, when is anthropomorphism beneficial, and when is it harmful? (i.e., what other factors interact with personification?) When we write HCXAI messages (and implied messages), which attributes will be important, and when, and for whom? See e.g. Upol Ehsan’s and Samir Passi’s paper on XAI with two user groups and three genres of messages (Ehsan et al., 2021). And what “thinking tools” (e.g., figures of thought) can help us to explore this new design space?

### Part III — Intelligent, not intelligent, or a continuum?

**Ben Shneiderman:** Michael suggests that our shared question is “How Can Humans Relate to Non-Human Intelligences?” But I disagree that machines should be described as intelligent. I reserve certain words such as think, know, understand, intelligence, knowledge, wisdom, etc. for people, and find other words for describing what machines do. I have done this in all six editions of *Designing the User Interface* (2016) and I think it was an important productive decision.

Reading Simone Natale’s book (2021) would be helpful. He says that anthropomorphic and humanoid robots are a compelling idea, but they have historically led to failed products. He describes the “banal deception” of many applications and the “straight up deliberate deception”, which are both “as central to AI’s functioning as the circuits, software, and data that make it run.” Natale has wonderful insights about the willingness of people to be deceived.

I respect Michael and his long devotion to participatory design and value him as a colleague, so I really hope to steer Michael away from a problematic belief in non-human intelligence.

Remember that about a quarter of the population fear computers, especially when the design suggests that computers are like people (Liang and Lee, 2017; Sprinkle, 2017; Strait et al., 2017). Others have also suggested that “anthropomorphising systems can lead to overreliance or unsafe use” (Weidinger et al., 2022).

By elevating machines to human capabilities, we diminish the specialness of people. I’m eager to preserve the distinction and clarify responsibility. So I do not think machines should use first-person pronouns, but should describe who is responsible for the system or simply respond in a machine-like way. Sometimes it takes a little imagination to get the right phrasing, but it is best when it is more compact.

In the early days of banking machines the social game was repeatedly tried with “Tillie the Teller,” “Harvey Wallbanker,” etc. that were chatty, e.g., “Good Morning. What can I do for you today?” but these failed, giving way to “Would you like to deposit or withdraw?” or even more compactly just giving buttons to touch for what customers wanted. Users shifted to designs that enabled them to accomplish their tasks as quickly as possible, while giving them the sense that they were operating a machine.

The issue is NOT if humans can relate to a deceptive social machine — of course they can. The issue is “Do we recognize that humans and machines are different categories?” or “Will we respect human dignity, by designing effective machines that enhance human self efficacy and responsibility?” The 2M+ apps in the Apple Store are mostly based on direct manipulation. Major applications like Amazon shopping, Google search, navigation, etc. avoid human-like designs because they have come to understand that they are suboptimal and unpopular. Can Michael point to 3 widely used apps that have a human-like interface?

**Michael Muller:** Part of my position is based on human-animal relationships. There is some kind of intelligence in a dog, and particularly in a highly-trained dog like a guide dog or a sheepdog (Phillips et al., 2016) or a lasso-pole pony (Fjin, 2011). There is a different, much colder kind of intelligence in a falcon (Soma, 2013). And yet another kind of intelligence in an ox (Phillips et al., 2016). We do have relationships with those animals.

I think sheepdogs and hunting dogs present interesting cases. We (humans, not Michael) send them out to do things (Kaminski and Nitzschner, 2013). We coordinate our actions with them — sometimes over distances. They coordinate their actions with us.

Then there are amoebas and paramecia, which can sense and respond, but don’t have much that we would think of as a brain, and still less of a mind.

But dogs are an intermediate case. They have a social presence. They have something like a mind. They have their own goals, and sometimes their goals and our goals may be aligned, and sometimes not. Sometimes we can change their minds. Sometimes they can change our minds. I think that makes them seem like non-human intelligences.

That being said, I don’t see LLMs (or, more properly, the UIs to LLMs) as having goals, intentions, and certainly not minds. The UIs that we have built do have social presence. We can design them so that they seem to have distinct personalities — even though we know that smart toasters don’t have personalities. Parrots have something like personalities, but not stochastic parrots (Bender et al., 2021). But stochastic parrots can have a kind of social presence. That makes them strange and new, because they mix attributes of toasters and of social beings. People have written about the “uncanny valley.” When I said “strange,” I could have said “uncanny.” I think they are usefully, productively strange. They help us to think new, experimental thoughts.

I still think of intelligence as a continuum, not a binary. We could anchor that continuum with amoebas at one end and humans at the other end. It’s the murky region in-between that interests me. That’s because I think of it as a region of hybridity or “third space.” A strange space. In my 1995 Aarhus paper (Muller, 1995), and again in the Handbook chapter with Allison Druin (Muller and Druin, 2012), we claimed that these spaces of inter-mixture of cultures are fertile places for new understandings and different knowledge, exactly because they are strange. I think that human-AI relationships can also be hybrid spaces of novelty.

If you say that neither animals nor algorithms have specifically human intelligence, then I’m right there with you. So far, we humans are still kind of special — although recent ethological papers suggest that we are not quite as special as we used to think we are.

For me, it’s not a matter of metaphor. It’s a matter of possibilities, and of murky but interesting in-betweens.

I accept that you reject the notion of non-human intelligences. I think that’s where our “debate” may be focused. We don’t have to agree. However, we do need to agree on a title. If you don’t want a title about non-human intelligences, then maybe we could try a less specific title, such as “Relationships of humans and AIs”?

**Ben Shneiderman**: Thanks for your further reply and discussion of animals as an intermediate case. For me the distinguishing issue is responsibility, so it is important to remember that pet owners are legally and morally responsible for what their pets do.

The discussion becomes more complex if we consider humans who are not fully responsible for their actions, such as those who have taken alcohol or drugs that interfere with their intelligence, memory, perceptual, cognitive, and motor abilities.

## Get Chenhao Tan’s stories in your inbox

Join Medium for free to get updates from this writer.

==So you could say intelligence is a continuum, but responsibility is more binary and is an important factor in design.== I think the discussion cannot be limited to intelligence, but must include memory, perceptual, cognitive, and motor abilities.

I’m interested in stressing design which clarifies that AI tools are designed by humans and organizations, which are legally responsible for what they do and for what the tools do, although tools can be misused, etc.

Our debate is interesting, but even the choice of title divides us. You suggest “Relationships of humans and AIs”? I suppose it is reasonable to discuss “Relationships of humans and cars/boats/bulldozers/lightbulbs”, but the word “relationships” suggests something like a peer relationship, granting too much to AIs. I would be happier with “Designing future AI systems to serve human needs.” For me, human needs includes environmental and biodiversity preservation and the [UN Sustainability Development Goals](https://www.un.org/sustainabledevelopment/sustainable-development-goals/).

### Part IV — On the use of “I”

**Michael Muller:** I forgot to respond about commercial chatbots that respond in first-person singular. Of course, there are many examples from the current LLMs. Whether these services are economically viable today, the companies that make them are [betting on their commercial and competitive viability](https://www.pcmag.com/news/chatgpt-alternatives-ai-chatbots-ready-to-answer-your-burning-questions): Bard, Bing, HuggingFace Open Assistant, and so on.

However, those are the UIs that you have been objecting to. Here are examples from a few years earlier. Suhel et al. (2020) describe banking chatbots that use first-person singular. My bank has a similar feature. [IGT Solutions](https://www.igtsolutions.com/services/cx-transformation/conversational-ai/) offer a chatbot for airline reservations and FAQs. [SABA Hospitality](https://sabahospitality.com/) has a similar offering for hotel reservations and guest services. These are commercial offerings that use first-person singular chatbots.

Researchers have used this kind of paradigm (i.e., AI referring to itself as “I” or “me”) in work related to Nass’s and Reeve’s research program’ “Computers Are Social Actors” (e.g., Reeves and Nass, 1996). I can find an example as early as 1998 (Elliott and Brzezinski, 1998), and I suspect that some of the prior decade’s papers also had this kind of dialog. I think you will object more strongly to Strommen’s description of children’s toys referring to themselves as “I” (Bergman (ed.), 2000).

I agree that there is a history of people rejecting chatbots. In our experience, the acceptance issue is about poor match of the user’s request to the chatbot’s set of intents (i.e., mapping request to response). We’ve been seeing that the current LLMs seem to provide more appropriate responses, perhaps exactly because they do not use the previous generation’s mapping of utterances-to-intents. I’m not sure that people reject chatbots that use a pronoun. I think they reject chatbots that provide poor service. We may need to do more systematic analyses of the factors that lead to acceptance and the factors that lead to failure.

**Ben Shneiderman:** Thanks for getting back to the issue of pronouns. You are correct that there are commercial chatbots, which have succeeded with “I” usage. However, as you point out many textual customer service chatbots have failed because they were just not that helpful.

A further example in your favor is the success of Alexa and Siri, which are voice-based user interfaces (VUIs) that use “I” pronouns. With VUIs compact presentations and clever designs have made “I” acceptable, but the calculus changes with visual user interfaces.

However, telephone-based voice response systems that guide users through a menu tree seem to have moved from early use of “I” to “you” pronouns in examples I have looked at, e.g. “You can type or say 1 to hear opening hours…” (as opposed to the awkward “If you type or say 1, I will give you the opening hours…”).

One further comment is that you write “there is a history of people rejecting chatbots”. I think our discussion will be more concrete if we distinguish different user communities. Most users do not notice if the interface is “I” or “you”, but some users strongly dislike the deception of “I” while some users strongly like the sense of empowerment they gain with a “you” design. I wish I knew the percentage in each category, especially separated by gender, age, computer experience, etc. Another interesting question is whether the preference for pronouns is changing over the years.

My final point is about Reeves and Nass’ CASA theory (1996). I enjoyed my arguments in with Cliff Nass about these issues, although I won the 1995 bet about the future of Microsoft BOB, which he consulted on, but I expected to fail — I just didn’t expect that it would fail so totally that there was no version 2, it simply was removed from the market within a year. While Reeves & Nass’ studies demonstrated that users would respond to computers socially, they did not consider the alternative hypothesis, which was that users would prefer the direct manipulation interfaces that have remained dominant in the Apple and Android Stores and web-based laptop designs.

In conclusion, while there are situations in which computers can become commercial successes by pretending to be a person, the dominant design remains the mobile device touchscreen and the web-based mouse clicks that keep users in control and avoids the anthropomorphic design (I would say trap!). I think there is a clear alternative to anthropomorphism. The issue is bigger than pronouns.

While we were wrapping up this discussion, online discussions emerged, such as [this blog post](https://livepaola.substack.com/p/an-ethical-ai-never-says-i) from Paola Bonomo (2023).

## Debate Summary

*by Chenhao Tan and Justin D. Weisz*

As editors of the [Human-Centered AI Medium publication](http://medium.com/human-centered-ai), we are grateful that Michael and Ben shared their valuable insights on the issue of anthropomorphism. In particular, we found their discussion thought-provoking and clarifying on several core issues. Here are three main takeaways from this debate:

- Both Michael and Ben agree that the choice of using “I” (i.e., anthropomorphism) can have a significant impact on users.
- Ben takes a clear stance on a binary distinction between human and non-human intelligence and highlights the importance of responsibility: designers & developers should take responsibility for AI-infused tools.
- Michael, in comparison, embraces a more fluid attitude towards intelligence as a continuum by presenting numerous analogies with human-animal relationships. He argues that there is a “murky region in-between” human intelligence and the intelligence exhibited by amoebas, which is interesting and underexplored as a design space.

This debate highlights one of the difficult issues we face when designing human-centered AI systems: should these systems personify themselves and reference themselves using first-person pronouns? We were astonished to learn how much evidence exists supporting both sides of the argument.

## Share your perspective

Where do you stand on the issue of anthropomorphism in AI systems? Whose argument convinced you more? Do you have a different perspective? We would love to hear your point of view! Please reach out to [Chenhao Tan](mailto:chenhao@uchicago.edu) if you would like your well-informed commentary included in this discussion.

Here are commentaries shared by others in the community.

- [Pattie Maes](https://medium.com/human-centered-ai/on-ai-anthropomorphism-commentary-by-pattie-maes-8e664827c640) (MIT Media Lab, US) — *April 10, 2023*
- [Susan Brennan](https://medium.com/human-centered-ai/on-ai-anthropomorphism-commentary-by-susan-brennan-ffd2e2785beb) (Stony Brook University, US) — *April 10, 2023*
- [Ron Wakkary](https://medium.com/human-centered-ai/on-ai-anthropomorphism-commentary-by-ron-wakkary-f086e1f9e85b) (Simon Frasier University, Canada) — *April 18, 2023*
- [Mary Lou Maher](https://medium.com/human-centered-ai/on-ai-anthropomorphism-a-commentary-9dfdf7a34f24) (University of North Carolina, Charlotte, US) — *April 26, 2023*
- [Alex Taylor](https://medium.com/human-centered-ai/on-ai-anthropomorphism-commentary-by-alex-taylor-4e72029a3006) (City University of London, UK) — *June 1, 2023*

## References

- Bender, E. M., Gebru, T., McMillan-Major, A., & Mitchell, S. (2021, March). On the Dangers of Stochastic Parrots: Can Language Models Be Too Big?. In *Proceedings of the 2021 ACM conference on fairness, accountability, and transparency* (pp. 610–623).
- Bergman, E. (Ed.). (2000). *Information appliances and beyond: interaction design for consumer products*. Morgan Kaufmann.
- Bonomo, P., (March 25, 2023). An Ethical AI Never Says “I”. [https://livepaola.substack.com/p/an-ethical-ai-never-says-i](https://livepaola.substack.com/p/an-ethical-ai-never-says-i)
- Capek, K. (2004). *RUR (Rossum’s universal robots)*. Penguin.
- Capek, K., Weatherall, M., & Weatherall, R. (1996). *War with the Newts*. Northwestern University Press.
- Don, A., Brennan, S., Laurel, B., & Shneiderman, B. (1992, June). Anthropomorphism: from ELIZA to Terminator 2. In *Proceedings of the SIGCHI Conference on Human Factors in Computing Systems* (pp. 67–70).
- Elliott, C., & Brzezinski, J. (1998). Autonomous agents as synthetic characters. *AI magazine*, *19* (2), 13–13.
- Fijn, N. (2011). *Living with herds: human-animal coexistence in Mongolia*. Cambridge University Press.
- Haraway, D. J. (2003). *The companion species manifesto: Dogs, people, and significant otherness* (Vol. 1, pp. 3–17). Chicago: Prickly Paradigm Press..
- Kaminski, J., & Nitzschner, M. (2013). Do dogs get the point? A review of dog–human communication ability. *Learning and Motivation*, *44* (4), 294–302.
- Lakoff, G. (1986). A figure of thought. *Metaphor and symbol*, *1* (3), 215–225.
- Lakoff, G., & Johnson, M. (2008). Metaphors we live by. University of Chicago Press.
- Leckie, A. (2013). *The Imperial Radch Boxed Trilogy*. Orbit.
- Liang, Y. and Lee, S. A. (2017). Fear of Autonomous Robots and Artificial Intelligence: Evidence from National Representative Data with Probability Sampling. *International Journal of Social Robotics,* 9(3): 379–84.
- Muller, M.J. (1995). Ethnocritical Heuristics for HCI Work with Users and Other Stakeholders. In *Proceedings of Computers in Context: Joining Forces in Design*, pp. 10–19 (Aarhus Denmark, 1995).
- Muller, M. (2004). Multiple paradigms in affective computing. *Interacting with Computers* 16.4 (2004): 759–768.
- Muller, M. J., & Druin, A. (2012). Participatory design: The third space in human–computer interaction. In J. Jacko (ed), *The Human–Computer Interaction Handbook* (pp. 1125–1153). CRC Press.
- Mumford, L. (1936, 2010). *Technics and civilization*. University of Chicago Press.
- Natale. S. (2021). *Deceitful media: Artificial intelligence and social life after the Turing test*. Oxford University Press, USA.
- Phillips, E., Schaefer, K. E., Billings, D. R., Jentsch, F., & Hancock, P. A. (2016). Human-animal teams as an analog for future human-robot teams: Influencing design and fostering trust. *Journal of Human-Robot Interaction*, *5* (1), 100–125.
- Reeves, B., & Nass, C. (1996). *The media equation: How people treat computers, television, and new media like real people*. Cambridge, UK.
- Ross, S. I., Martinez, F., Houde, S., Muller, M., & Weisz, J. D. (2023, March). The programmer’s assistant: Conversational interaction with a large language model for software development. In Proceedings of the 28th International Conference on Intelligent User Interfaces (pp. 491–514).
- Shneiderman, B., Plaisant, C., Cohen, M. S., Jacobs, S., Elmqvist, N., & Diakopoulos, N. (2016). *Designing the user interface: strategies for effective human-computer interaction*. Pearson.
- Soma, T. (2013, April). Ethnoarchaeology of ancient falconry in East Asia. In *The Asian Conference on Cultural Studies 2013: Official conference proceedings* (pp. 81–95).
- Suhel, S. F., Shukla, V. K., Vyas, S., & Mishra, V. P. (2020, June). Conversation to automation in banking through chatbot using artificial machine intelligence language. In *2020 8th International Conference on Reliability, Infocom Technologies and Optimization (Trends and Future Directions)(ICRITO)* (pp. 611–618). IEEE.
- Sprinkle, T. (2017). *Robophobia: Bridging the Uncanny Valley*. American Society of Mechanical Engineers.
- Strait, M. K., Aguillon, C., Contreras, V. and Garcia, N. (2017). The Public’s Perception of Humanlike Robots: Online Social Commentary Reflects an Appearance-Based Uncanny Valley, a General Fear of a “Technology Takeover”, and the Unabashed Sexualization of Female-Gendered Robots. *Proc. 26th IEEE International Symposium on Robot and Human Interactive Communication (RO-MAN).* IEEE, 1418–23.
- Weidinger, L., Uesato, J., Rauh, M., Griffin, C., Huang, P. S., Mellor, J., … & Gabriel, I. (2022, June). Taxonomy of risks posed by language models. In *2022 ACM Conference on Fairness, Accountability, and Transparency* (pp. 214–229).