# Attention-based Models

Biologically-oriented vs pragmatic models of attention, Transformer revolution, the Consciousness prior, etc.

## Intro

The immediate impulse for this subdirectory is the next stage of Transformer revolution, the qualitative shift
associated with GPT-3 and OpenAI API, which started publicly two months ago, on May 20, 2020:

https://www.cs.brandeis.edu/~bukatin/transformer_revolution.html

This is "the AlexNet moment" of the Transformer revolution, and we should expect that people will
hybridize all kinds of things with Transformers and other attention-based models in the near future,
just like they hybridized all kinds of approaches with "Deep Nets" in recent years, obtaining
a variety of architectures such as Deep Probabilistic Programming, Deep Neuroevolution, etc.

I am going to write various attention-related sketches here.

On one hand there are biological-oriented models of attention based on synchronized spiking of neurons
with a particular frequency (e.g. famous "40hz"), and pragmatic models of attention, such as converting a vector of
"relevance coefficients" to a vector of probabilities, and using these probabilities as coefficients to
sum a collection of "value vectors" together.

Here it would be practicularly interesting to see, if these classes of attention models can be linked
together, e.g. if biological-oriented models can be used to approximate pragmatic models of
attention (I don't know what might have been done in this direction already).

Another issue of interests for me is whether biological models of attention can be useful for
creation of "mini-Transformers" (Transformer-like models which would be expressive, but
more modest in terms of required computational resources, especially for training).

Another point of acute interest for me is to explore various ways of hybridization between
dataflow matrix machines and various attention-based approaches, both for pragmatic and
for biological-oriented attention (here the architectures might be Transformer-like,
Recurrent Independent Mechanisms-like, or something else).

Note that there were proposals to understand "consciousness" via attention-like mechanisms
(both in biological systems, via synchronized oscillations, and in artificial systems,
via pragmatic attention used to create information bottleneck).

---

There is a bit of mystery about simple-minded pragmatic attention, the so-called
"content-based neural attention": why a linear combination of value vectors is a good model
of attention? I am trying to explain this in 
[simple-minded-attention.md](https://github.com/anhinga/2020-notes/blob/master/attention-based-models/simple-minded-attention.md).

The attention used in Transformers is a development of the "content-based neural attention":
[transformer-attention.md](https://github.com/anhinga/2020-notes/blob/master/attention-based-models/transformer-attention.md).

Discussing the "Transformers' mystery", namely their "unreasonable effectiveness":
[transformer-mystery.md](https://github.com/anhinga/2020-notes/blob/master/attention-based-models/transformer-mystery.md).

Some of the possible attention-related experiments:
[possible-experiments.md](https://github.com/anhinga/2020-notes/blob/master/attention-based-models/possible-experiments.md).

Remarks on implicit metalearning in neural nets and Transformers:
[implicit-metalearning.md](https://github.com/anhinga/2020-notes/blob/master/attention-based-models/implicit-metalearning.md).

Selected less known papers on Transformers:
[selected-papers.md](https://github.com/anhinga/2020-notes/blob/master/attention-based-models/selected-papers.md).
