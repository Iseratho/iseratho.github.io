---
layout: post
title: "Blog Journey on LLMs"
date: 2023-12-12
tags: [research, ai, meta]
image: /images/journey_to_the_top.jpg
---

# Blog Journey on LLMs

> Welcome to my blog. In this post, I provide the initial structure of my blog, some basic info, as well as personal notes on the first few topics that I covered. 

I had the idea of creating my own blog for a long time, but did not find a good topic to write on. However, after having so many discussions regarding AI, in particular on LLMs, I finally found my inspiration. Apparently, many people are in awe of the current models, while I see lots of room for improvement. 
Given that I already worked with Transformers for a couple of years, it seems like an ideal fit. Especially, after I visited a conference, where I learned a lot more about the inner workings of large language models (e.g., about the creation of Jais), which I wanted to summarize. 

In the following, I provide a brief overview of my first **tetralogy**, which is a critical reflection on the current LLM advancements. It goes from we are at the moment to where we should go:

- At first, we look at **Why are LLMs so good** in: [LLMs: Current State, Hype, and Future](/2023/09/14/llm-state.html)
- Then we discuss **Why current models should be rethought nonetheless** in: [I don't like auto-regressive LMs](/2023/09/29/autoregressive-dislike.html)
- We supplement this discussion with **Why encoders are important for both Image and Text Generation** in: [Comparing Text Decoders and Image Diffusers](/2023/11/21/text-decoders-v-image-diffusers.html)
- Finally, we conclude by considering **Why we need to go beyond (step back from) prompt engineering** in: [Retracing and Returning from Prompt Engineering](/2023/12/08/prompt-engineering.html)

The target group of this initial part of my blog is people with intermediate knowledge of AI. Note that, while my research applies Transformer models, I do not design and develop novel architectures. Hence, I decided to present my thoughts in a non-scientific way to emphasize that it is NOT an expert opinion and thus also omit supporting my arguments with citations. My goal is to make people reflect critically on the current generative AI models rather than providing conclusive evidence.

Finally, I want to disclose that the banner images were created with Copilot. Why I still like image generators conditioned on text can be read in my blog ;-)

This concludes the first series of my blog. I might revisit it, if newer models (e.g., Gemini being a recent example) would truly lead to fundamental advancements. If you want to learn more about Transformers, I recommend the information on HuggingFace, e.g., their course: [https://huggingface.co/learn/nlp-course/](https://huggingface.co/learn/nlp-course/)

> Version 0.1; Errata: -

---

## Prompts used for Images

Always started a new topic with a balanced configuration in [Copilot](https://copilot.microsoft.com/):  

1. Create an image of A person worshipping a robot.
2. Create an image of The disgusted face looking at loops.
3. Create an image of Fighting match banner: a book on the left "vs." a painting on the right.
4. Create an image of Striked out keyboard typing.
5. Create an image of A person climbing a mountain with shining light at the top.
