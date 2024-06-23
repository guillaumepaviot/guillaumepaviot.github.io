---
date: 2022-09-05T11:00:59-04:00
description: "Making an AI write poems and learning about NLP along the way"
featured_image: "/images/project-2/baudelaire.jpg"
title: "A poem generator"
---
I'm very interested in how machine learning models can read an write text. The objective of this project is to implement various natural language processing (NLP) algorithms and neural networks at a low level using PyTorch, to get a better understanding of their functionality. I trained these algorithms on Les Fleurs du Mal by the French poet Charles Baudelaire because I'm a fan of his work and was curious of how models would write poetry.

Implemented Neural Networks and NLP Models:

- **Bigram Model**: Takes one or two characters, or one word as input.
- **Bag of Words Model**.
- **Multilayer Perceptron (MLP)**: Based on [Bengio et al. 2003](https://www.jmlr.org/ papers/volume3/bengio03a/bengio03a.pdf), using both characters or words as input.
- **Single-Head Transformer**: Based on [Vaswani et al. 2017](https://arxiv.org/abs/1706.03762).
- **Byte-Pair Encoder**: Based on [Sennrich et al. 2015](https://arxiv.org/abs/1508.07909). applied to the French text.
- **GPT-2 Model**: Currently working on it, it's based on [Radford et al. 2019](https://d4mucfpksywv.cloudfront.net/better-language-models/language_models_are_unsupervised_multitask_learners.pdf), featuring 124M parameters and trained in the cloud.

This project made me learn a lot about complex language models, but also how to implement this kind of models with low-level PyTorch.



[Link to GitHub Repository](https://github.com/guillaumepaviot/poem_generator)

{{< figure src="/images/project-2/embeddingsMLP.png" >}}

*An example of the embeddings in 2 dimensions learned by the MLP algorithm on 35 french characters (26 letters, 1 space character and 8 characters with accents)*