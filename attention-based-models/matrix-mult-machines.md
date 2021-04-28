## Machines with matrix multiplication as a key element.

In [theory-problems.md](https://github.com/anhinga/2020-notes/blob/master/attention-based-models/theory-problems.md)
I consider the rewrite of DMMs in a form emphasizing duality between network matrix and another matrix which is
a vector of vector data.

This is a very interesting exercise, and, in particular, I have been working with machines which compose a _bilinear operation
of matrix multiplication_ and a general operation of generating a pair of matrices to be multiplied afterwards.

---

From explorations of this setup which I performed in Oct-Nov 2020:

  * It is easy to make sure that, roughly speaking, **"both matrices are includes verbatim into their product"**.
    Just concatenate them with unit matrices from the appropriate sides. This is important, because it enabled
    "including identity functions" into this setup (and we know these days that having **"identity as one of the
    available activation functions"** is often crucial).
  * It makes sense to **interpret monochrome images as matrices and multiply them**. The results are
    visually interesting, especially if **one normalizes rows of the left matrix and columns of the right one**,
    and it is likely that there is plenty of hidden structure in the resulting matrices as well.
    This is a very promising line of exploration. I have now posted some initial Julia Jupyter notebooks (Dec 2020-Jan 2020)
    exploring this: https://github.com/anhinga/julia-notebooks/tree/main/images-as-matrices (and now there are
    further (Mar 2020-Apr 2020) explorations here and at
    https://github.com/anhinga/julia-notebooks/tree/main/grimoire-team/variations)
        
---

It's Dec 3 now, and here I want to write down some more recent (Nov 28) considerations.

Let's step back and recall that this architecture is also a generalization of digital audio synthesis via composition of
unit generators (which is, in fact, an unrecognized form of neural networks).

One of the most productive neurons in that setup is the neuron with 3 inputs and _sin(a*x+y)_ as an activation function.
It allows various audiomodulations and such. We need to consider a matrix generalization of this neuron.

It should be something like _F(AxX+Y)_, and since _A,X,Y_ are rectangular matrices of different dimensions (MxK,KxN,MxN - all these numbers
can be positive integers or infinity),
it is probably optimal to also have 3 output matrices (this way, the case of _Id_ instead of _(A,X,Y) => F(AxX+Y)_ is naturally included).

This way different _F_ and different compositions would provide different "generalized modulations" and such.

---

On the other hand, generalizing from "universal differential equations" and from "differential programming",
one can include any machine learning model into a "differentiable program" ("differential" might be an overkill here,
at least it does not need to be more differentiable than ReLU, although continuity does help, so
"continuous programming" might be the terminology I prefer as slightly less demanding).

And, in particular, _F(AxX+Y)_ can be included into an arbitrary program of this kind (e.g. into an
arbitrary program suitable for Julia Flux). So, while the "pure scenario" would require us to
assemble a neat **"matrix multiplication machine"** by composing various _F(AxX+Y)_ and _G(AxX+Y)_ and such,
the "mixed pragmatic scenario" just allows us to incorporate _F(AxX+Y)_ operations into "differential
programs" (e.g. Julia Flux programs, which can include other kinds of models and a rather general Julia code).

---

The difference here is that if fragments are embedded into a Julia program, then the program itself is fixed.

Or, at least, the only meta-learning being immediately available would _generally speaking_ be along the lines of
conventional program synthesis for discrete programs; that's unless the Julia program in question has some special
structure allowing for better meta-learning. In particular, if what we code in Julia is all in the DMM style,
and connectors are via linear combinations of linear streams, then continuous meta-learning is available
(because this would then be just a DMM formalism, with its meta-learning via continuous changes of connectivity
matrices).

