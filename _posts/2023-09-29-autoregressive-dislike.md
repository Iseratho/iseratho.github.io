---
layout: post
title: "I don't like auto-regressive LMs"
date: 2023-09-29
tags: [research, ai]
---

# I don't like auto-regressive LMs

> It is no secret that I am skeptical about the capabilities of pure autoregressive LMs like GPT. On the flip side, I am a big fan of autoencoding models (e.g., BERT). In this post, I am briefly going to state my opinion on the two parts of the Transformer architecture.

**The Transformer Architecture.** The Transformer architecture consists of two parts, an autoencoding encoder and an autoregressive decoder, which are connected via cross-attention. The encoder is responsible for natural language understanding (NLU), while the decoder is responsible for natural language generation (NLG). The two parts can be used individually for language modeling (LM) and are suited for distinct tasks (e.g., text classification vs text continuation). 

**Order matters.** Encoders can be trained bidirectional with masked LM, while decoders are trained unidirectional with causal LM. And herein lies my big concern with decoder-only models. For encoder models, the sequence matters less to correctly classify a piece of text (as the underlying embeddings will be rather similar when pooled). However, the generated text is greatly influenced by the input order in decoder models (i.e., significant variations). This is why prompt engineering is a much greater focus in decoder models (e.g., requesting a step-by-step solution to increase accuracy). Also, evaluation is more intuitive in encoder models than decoders. Compare it to students exams, where fill-in-the-blank tests (masked LM) are easier graded than written essays (causal LM).

**Retrieval vs Generation.** Transformers will profoundly change how we interact with information. Nowadays, encoders are already often employed in information retrieval systems. Unfortunately, decoder-only models are by some seen as a potential substitute (e.g., asking ChatGPT rather than googling). This leads to the well-known problem with the veracity of decoder models, which cannot provide sources (besides remembering some of them). Hence, NLU should be an integral part either by using the full Transformer architecture or encoders as a separate module. Both options could even be combined, as is the case in retrieval-augmented generation. First, we use encoders to find suitable passages to a question and then we use a transformer to generate a coherent answer with sources. 

**Future Direction** Besides its initial attention, encoder models like BERT have fallen out-of-favor in the news. Nevertheless, NLU problems are still very common, but often use the less accurate decoder model as a proxy (e.g., providing labels as prompts and parsing the generated output). Even for NLG, most use cases go beyond simple text continuation. Considering traditional auto-complete use cases, it is typically less concerned about generating sequences but improving text in general (e.g., rephrasing an e-mail from scratch, rather than merely completing it). While decoder-only models perform intriguingly well in most scenarios, I hereby argue to not neglect the encoder part and more sophisticated architectures in general.

**TLDR** I find auto-regressive LMs without combining them with auto-encoding LMs ill-suited for most tasks. Both work fundamentally different, which is why one should not substitute for the other. Hence, seeing decoder only models like ChatGPT as the solution for everything is incorrect.

> Version 0.1; Errata: -
