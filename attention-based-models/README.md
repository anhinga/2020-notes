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

