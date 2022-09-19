---
date: 2022-09-05T11:00:59-04:00
description: "Making an AI write poems and learning about NLP along the way"
featured_image: "/images/project-2/baudelaire.jpg"
title: "A poem generator"
---

The goal of this project is to implement at low levels different NLP algorithms and neural nets in PyTorch to learn more about them.
I train those algorithms on Les Fleurs du Mal written by French poet Charles Baudelaire.

Current language model neural nets implemented:

- Bigram (with one, two character or one word as input)
- Bag of Words
- MLP, along the lines of [Bengio et al. 2003](https://www.jmlr.org/papers/volume3/bengio03a/bengio03a.pdf) (with both characters or word as input)

[Link to GitHub Repository](https://github.com/guillaumepaviot/poem_generator)

{{< figure src="/images/project-2/embeddingsMLP.png" >}}

*An example of the embeddings in 2 dimensions learned by the MLP algorithm on 35 french characters (26 letters, 1 space character and 8 characters with accents)*