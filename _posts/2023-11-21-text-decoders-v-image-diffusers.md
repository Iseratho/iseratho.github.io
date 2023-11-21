---
layout: post
title: "Comparing Text Decoders and Image Diffusers"
date: 2023-11-21
tags: [research, ai]
---

# Comparing Text Decoders and Image Diffusers

> Subtle differences can be really important. Here, I argue that not every type of generation should be treated equally. Image generation is conditioned using encoders, while many text generation models lack this component.

**2022:** The year 2022 had two breakthroughs in artificial intelligence: image diffusion (with diffusers like DALL-E) and text generation (with decoders like GPT). Both solve solve problems in a similar fashion. They use a prompt to generate an output (image or text). While in the past, vision models tended to dominate the media, language models have since overtaken them.

**(Text) conditioning for image diffusion.** Diffusion models need to be guided to be useful. The natural way to guide image generation is through input prompts. That's why CLIP (Contrastive Language–Image Pre-training) and similar are an integral part of image generation. Basically, a common understanding between image and text is trained using encoders that generate embeddings. The image generation can then be conditioned on the text. Given some noise and the prompt, the model iteratively denoises the image based on the information provided in the prompt. This process is not only effective but also intuitive.

**Deviation in text-to-text models with decoders.** While Transformers work in a similar vein, many models use decoders only. Hence, they do not condition on the input prompts, but only continue the text through decoding. Concerning image diffusion, it would be somewhat similar to provide a half-denoised image as input rather than using text conditioning. Actually, such a mechanism can be used for conditional image-to-image diffusion, where noise is added to the input image. However, text decoding works by sequential addition of new tokens rather than concurrent improvements of pixels globally. Therefore, the decoder can start to deviate from the initial instructions over time, which is opposite to text-conditioned diffusion models. 

**Output comparison.** Most images generated from scratch (which is typically the case for diffusion models) do not need to adhere to truth but just require subjective judgments about whether they fit or not. For brevity, I will omit a discussion on deep fakes here, which blurs those lines. However, most text responses are generated to satisfy an information need and thus depend on objective truths. Subsequently, the validation process is different. For images, it is enough to rate them based on your preference. For text, other important considerations are syntax, semantics, but especially also factuality. 

**TLDR** The generation processes in text and images differ at the moment. Partially, the difference is due to different input formats, i.e., tokens/words vs. pixels/patches. Nevertheless, the recent convergence of image and text models suggests that the processes should become more similar. One potential direction is envisioned by LeCun with JEPA (Joint-Embedding Predictive Architecture) which emphasizes the importance of encoders.

> Version 0.1; Errata: -
