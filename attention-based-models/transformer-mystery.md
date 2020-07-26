# Transformer Mystery: the Unreasonable Effectiveness of Multilayer Attention Models

Transformers delivered more than they promised, and more than one could have expected at the first glance.

The original motivation of Transformer models was two-fold: easy modelling of long-range dependencies and
nice parallelization. That's very cool, but why on Earth does this result in the ability to synthesize
parse trees (e.g. "Visualizing and Measuring the Geometry of BERT", https://arxiv.org/abs/1906.02715)?

---

Shedding more light on this is likely to become a popular research subject.

At the moment we have some hints. For example, if one agrees with the 2019 version of 
"The Consciousness Prior" essay by Yoshua Bengio, https://arxiv.org/abs/1709.08568 , then one
can observe that Transformers fullfill a number of desiderata from this essay
(although, not the modulating feedback, which is absent in Transformers).

Note that there was an earlier paper linking a different (and more biorealistic) model of
attention to consciousness in mammals: "Towards a Neurobiological Theory of Consciousness" 
by Francis Crick and Christof Koch, _Seminars in the Neurosciences_ (1990), **2**, pp. 263-275, 
https://authors.library.caltech.edu/40352/1/148.pdf

This might make us develop a stronger belief in the premises of "The Consciousness Prior" essay
(it is strange that that essay does not reference the Crick-Koch paper; of course, Crick-Koch
later started to say that it is more complicated than that, so one might say that they stopped
agreeing with their own 1990 paper, but I suspect their initial
simple and straightforward approach was closer to the "true theory", than what they did afterwards).

---

Another hint might come from the theory of Dataflow Matrix Machines. We know that if one takes
recurrent neural networks and replaces streams of numbers by the streams of vectors on the level
of single neurons, this greatly increases expressive power of the resulting formalism. E.g. one can
use the resulting neural machines as a full-strength general-purpose programming platform with
continuously deformable programs, one obtains neural machines which can easily and fluently
modify themselves in highly compositional ways, etc.

The key element of "content-based neural attention" is taking linear combinations of high-dimensional
vectors, and it is rewritten via matrix multiplication in the context of Transformers.

Exactly the same thing happens in Dataflow Matrix Machines - linear combinations of high-dimensional
vectors which get rewritten via matrix multiplication.

Of course, there are differences. On one hand, there are a number of features of Dataflow Matrix Machines
which are likely to make them more expressive than Transformers (which can be thought of as an important subclass
of Dataflow Matrix Machines). On the other hand, we know that Transformers are nicely trainable,
that the resulting models actually do take advantage of their expressive power, whereas no one has yet established
that Dataflow Matrix Machines are nicely trainable in a practical sense.

---

If one thinks how a biological cell is "interpreting" its DNA by cascade of gene expression regulation
("often, one gene regulator controls another, and so on, in a https://en.wikipedia.org/wiki/Gene_regulatory_network),
one finds a lot of parallels with how a transformer is "interpreting" a text via
multilayered attention.
