# Possible attention-related experiments

## Adding feedback to Transformers

Something in the style of "Learning to Combine Top-Down and Bottom-Up Signals in Recurrent Neural Networks with Attention over Modules",
https://arxiv.org/abs/2006.16981 , but that paper is only doing it inside a two-layer system which is not good enough to really test
this idea of "The Conscious Prior" essay. 

Instead, one
should take a small-scale easy-to-train version of a Transformer, and see what adding feedback connections to modulate
the forward flow might do.

## DMM neural achitecture search

Let's decompose the Transformer attention into its mathematical components: matrix multiplication,
applying softmax to matrix rows (or columns), matrix transposition, and add a handful of other operations,
so that we can at least express the rest of the Transformer-related pieces.

Let's then perform some form of neural-architecture search. It might be in the style of
"AutoML-Zero: Evolving Machine Learning Algorithms From Scratch", https://arxiv.org/abs/2003.03384 ,
or it might be a much more compact and fast scheme, e.g. "Neural Architecture Search without Training",
https://arxiv.org/abs/2006.04647 , or "Few-shot Neural Architecture Search", https://arxiv.org/abs/2006.06863
