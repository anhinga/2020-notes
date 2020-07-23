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

Note that there was an earlier paper linking
