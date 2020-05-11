## Inspired by "10 lines thesis" by Jürgen Schmidhuber

The ICLR 2020, had a workshop _"Beyond “Tabula Rasa” in Reinforcement Learning (BeTR-RL): 
Agents that remember, adapt, and generalize"_
(April 26, 2020):

http://www.betr-rl.ml/2020/

http://www.betr-rl.ml/2020/program/

The panel with all 4 invited speakers + Jürgen Schmidhuber starts around 2:40 in the video. 
At 3:36, Jürgen Schmidhuber makes a radical remark that at the end of the day there will be a 
10-line program generating advanced super-human AI, and with the benefit of hindsight 
we'll say that it was obvious and it was strange that we have not found it earlier
(pieces are already there, we just need to join them together, he says, "we are almost there")

Here is my attempt at making a verbatim transcript:

_'It seems to me that many of the basic principles are already understood.
And it's more a question of taking these different well-understood puzzle pieces and 
put them together in such a way that everybody in hindsight will say 
"oh, that's so simple, why did not we think of that half a century ago". 
At the end, it is going to be 10 lines of code or something, 
and it is going to combine [...] the artificial curiosity thing, 
and the metalearning thing, in a totally natural and completely obvious, 
in hindsight obvious, way, and at the moment I strongly believe it is 
just about getting these puzzle pieces together. We have all the pieces, 
and we just have to plug them down in the right positions. We are almost there! 
And in hindsight we'll be able to say: 
"that's so simple, any high school student will be able to learn it... 
how to build a general AI based on these simple principles".'_

This "10 lines metaphor" is not new for him, here is what he said in 2017

https://www.theguardian.com/technology/2017/apr/18/robot-man-artificial-intelligence-computer-milky-way

_“The central algorithm for intelligence is incredibly short. 
The algorithm that allows systems to self-improve is perhaps 10 lines of pseudocode. 
What we are missing at the moment is perhaps just another five lines.”_

---

### *** "10 lines" as a meditation topic ***

An interesting meditation exercise is as follows.

Assume that there is a moment (now or in the future), where the thesis
that approximately 10 lines of sufficiently high-level computer code could
generate AI is literally correct. Assume that a good chunk of Internet is
available for such a process (although, it's OK to assume that it is
a static snapshot of a subset of Internet within a sandbox environment;
of course, the question of whether an effective sandbox for such a
situation is at all possible is a whole separate long story, long discussion,
and long study).

Assume that this chunk of Internet, in particular, contains a fairly large subset of
public github, of arxiv, and of wikipedia. The meditation exercise is,
then, what these 10 lines of AI-generating code might look like.

This is, obviously, a series of meditation exercises. Each particular
exercise depends on your assumptions about the path by which you and/or
community arrived at the imagined moment in question.

---

### *** Dataflow Matrix Machines and "10 lines" ***

DMM formalism might be quite useful for some of these meditations.

The awareness of the key DMM concepts might inspire new and different
architectures for those possible "10 lines" drafts.

The following ideas were mostly developed in 2015-2017 in a series
of papers and preprints. The reference paper is,
_Dataflow Matrix Machines and V-values: a Bridge between Programs and Neural Nets_,
https://arxiv.org/abs/1712.07447

A recent overview of the current state of DMM research which was written
for the AI-GAs community is
_Synergy between AI-generating algorithms and dataflow matrix machines_
(March 2020)
https://github.com/anhinga/2020-notes/tree/master/research-notes

---

  * The essence of neural model of computations is that 
    linear and non-linear computations are interleaved. 
    Hence, the natural degree of generality for neuromorphic computations 
    is to work not with streams of numbers, but with arbitrary streams
    supporting the notion of linear combination of several streams (**linear streams**).

  * There is a variety of kinds of linear streams (streams of finite-dimensional
    tensors of fixed shape is only one, most familiar corner case; there can
    be streams of elements representing infinite-dimensional vectors; or
    even streams of elements of arbitrary nature (e.g. streams can be combined
    with coefficients by taking generalized stochastic sums, even if the
    elements themselves cannot be so combined).
    
  * **V-values** ("flexible tensors with tree-shaped indices") are especially
    convenient and useful for many of our purposes. One can think about these
    structures as nested dictionaries, as prefix trees, as mixed-rank tensors,
    or as formal linear combination of finite strings.

  * We are also going to use
      * Arbitrary fixed or variable arity of activation functions
      * A rich library of powerful built-in activation functions
      * Unbounded network size (⇒ unbounded memory)
      * Self-referential and self-modification facilities:  
        ability to change weights, topology, and the size of the active part dynamically, on the fly.
   
  * Then we obtain a formalism for very expressive and flexible neural machines,
    which we call **Dataflow Matrix Machines (DMMs)**.
  
  * RNNs are known to be Turing-complete in the presence of unbounded memory,
    but they are too low-level, and a number of people are suggesting that they
    might be closer to an esoteric programming language, and that their
    pragmatic programming power is less than power of a general purpose programming
    language. DMMs seem to have full power of a practical dataflow programming language
    or of a functional reactive programming language. So we are actually obtaining
    a pragmatic programming formalism, where one can **continuously deform programs**.
    One can choose whether to have large networks with a lot of weights, or whether to have
    compact powerful networks (programs) which have only a few weights and neurons, 
    but use highly expressive powerful neurons and streams, or anything in between.
    
  * A variety of self-modification algorithms for recurrent neural networks were explored
    by the AI community. However, it is always difficult to introduce new ways to
    self-modify RNNs, and one cannot freely and flexibly mix-and-match different
    self-modification schemas. With DMMs, one can have single neurons accumulating and
    transforming streams of entire network matrices. So one can have a neuron **Self**,
    outputting the next version of an entire network matrix on each step (if one computes
    with immutable data and shared common substructures, this can be done in
    an efficient incremental manner). **Self** can take updates to the network matrix
    from the other neurons and incorporate them. This allows to flexibly combine
    any transformations of network matrices (one can take linear combinations of such
    transformations, compose them, etc).

---

I think this formalism is likely to be useful in the context of fruitful meditations
on the "10 lines thesis" by Jürgen Schmidhuber.
 
