---
layout: post
title: "LLMs: Current State, Hype, and Future"
date: 2023-09-14
tags: [research, ai]
---

# LLMs: Current State, Hype, and Future

> In this article, I briefly summarize my takeaways derived from interesting points raised during several discussions at RANLP'23. Of course, the main focus was on the Transformer architecture and large language models (LLMs). Although written in a non-academic tone, parts of the following text assume an intermediate understanding of the main concepts employed in LLMs. 

**LLMs are impressive.** Large language models (LLMs) achieve *remarkable results in various NLP tasks*, such as Question Answering, Translation, and Summarization. As LLMs can be applied to virtually all problems that can be formulated with languages (or tokenized), we can be very optimistic about their benefits for scientific advancements. Besides, LLMs could even benefit notoriously difficult tasks, such as fact-checking by individually checking each claim in an argument, or supporting research by generating synthetic data. 

One reason for their performance is they can be *trained very efficiently*. By masking subsequent tokens in the decoder, we can train the model by predicting the next tokens in parallel rather than iteratively. This fact, together with more training data and more computing resources, allows the upscaling of models to achieve such groundbreaking results.

**LLMs still have shortcomings.** While the training of LLMs is very efficient, the generation mostly still relies on a rather slow iterative process. Moreover, the performance in certain areas is still lackluster. Unlike the suggestions of media reports, mass employment has yet to happen. Even *neural machine translation* (i.e., the original areas for Transformers) is far from being solved. So far, LLMs cannot replace professional translators, especially when considering high-stakes situations. 

The *lack of proper understanding* of language becomes more evident when considering specific long-standing problems of natural language understanding, such as coreference resolution. Furthermore, what information LLMs really capture in their dense layers (i.e., the part where the world knowledge is presumably stored) remains largely unknown. 

But how can LLMs solve far more complex tasks, such as writing *coherent long sequences of text*, seemingly without requiring proper knowledge of individual parts?

**LLMs are deceptive.** The key element of LLMs being so convincing to humans resides in their fluency. By *cleverly sampling words*, the generated sequences are phenomenally consistent. Herein lies to key component of LLMs, namely the attention mechanism, which (by "paying attention to the important positions") establishes that no word feels out of place. 

Humans foolishly misinterpret such *fluency of language* with intelligence, especially when the provided sequences are long (as LLMs tend to generate). However, being able to fool others would still not qualify for the "sparks of intelligence" that LLMs apparently possess. 

The other key observation is that *fluency automatically pulls along fidelity*. Therefore, by being able to better wield language, LLMs also become more expressive. 

**Will LLMs surpass humans?** As LLMs continue to get better at language, one could reasonably assume that it is just a question of time to surpass human performance/intelligence. Such discussion becomes more philosophical. Critically, we lack a generally agreed upon *measure of linguistic performance/intelligence*. Hence, there is no reliable way for measurement and comparison. 

The difficulty of answering such questions becomes evident when trying to consider the trajectory of the quality of linguistic works. For instance, whether today's novels are better than older ones is up for debate with no apparent answer. Presuming that human linguistic capabilities stayed constant over the last decades/centuries, it similarly seems logical that *LLMs might plateau* at some point. 

In general, there is *no reliable way to predict the long-term future of LLMs* at this point, as it depends on the upcoming advancements in the field. Hence, the best course of action is to help advance the current state-of-the-art.

**TLDR** In sum, LLMs are and will become a useful tool in many tasks. However, current LLMs are still limited in their capabilities, especially regarding language understanding. Nevertheless, there is hype around LLMs partially due to them being very convincing to humans. The fear that LLMs will make humans obsolete is of a philosophical nature and seems unwarranted at the moment.

> Version 0.1; Errata: -
