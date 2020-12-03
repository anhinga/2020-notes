## Machines with matrix multiplication as a key element.

In [theory-problems.md](https://github.com/anhinga/2020-notes/blob/master/attention-based-models/theory-problems.md)
I consider the rewrite of DMMs in a form emphasizing duality between network matrix and another matrix which is
a vector of vector data.

This is a very interesting exercise, and, in particular, I have been working with machines which compose a _bilinear operation
of matrix multiplication_ and a general operation of generating a pair of matrices to be multiplied afterwards.

---

**INSERT:** explorations of this setup which I performed in October and November (there is quite a bit of uncommitted things at the moment,
both theoretical and related to some Julia experiments).

---

It's Dec 3 now, and here I want to write down some more recent (Nov 28) considerations.

Let's step back and recall that this architecture is also a generalization of digital audio synthesis via composition of
unit generators (which is, in fact, an unrecognized form of neural networks).

One of the most productive neurons in that setup is the neuron with 3 inputs and _sin(a*x+y)_ as an activation function.
It allows various audiomodulations and such. We need to consider a matrix generalization of this neuron.

It should be something like _F(AxX+Y)_, and since _A,X,Y_ are rectangular matrices of different dimensions (MxK,KxN,MxN - all these numbers
can be positive integers or infinity),
it is probably optimal to also have 3 output matrices (this way, _F=Id_ case is naturally included).

This way different _F_ and different compositions would provide different "generalized modulations" and such.

---

On the other hand, generalizing from "universal differential equations" and from "differential programming",
one can include any machine learning model into a "differentiable program" ("differential" might be an overkill here,
at least it does not need to be more differentiable than ReLU, although continuity does help, so
"continuous programming" might be the terminology I prefer as slightly less demanding).

And, in particular, _F(AxX+Y)_ can be includes into an arbitrary program of this kind (e.g. into an
arbitrary program suitable for Julia Flux). So, while the "pure scenario" would require us to
assemble a neat **"matrix multiplication machine"** by composing various _F(AxX+Y)_ and _G(AxX+Y)_ and such,
the "mixed pragmatic scenario" just allows us to incorporate _F(AxX+Y)_ operations into "differential
programs" (e.g. Julia Flux programs, which can include other kinds of models and a rather general Julia code).

