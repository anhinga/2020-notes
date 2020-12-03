## Machines with matrix multiplication as a key element.

In [theory-problems.md](https://github.com/anhinga/2020-notes/blob/master/attention-based-models/theory-problems.md)
I consider the rewrite of DMMs in a form emphasizing duality between network matrix and another matrix which is
a vector of vector data.

This is a very interesting exercise, and, in particular, I have been working with machines which compose a bilinear operation
of matrix multiplication and a general operation of generating a pair of matrices to be multiplied.

---

**INSERT:** explorations of this setup which I performed in October and November (there is quite a bit of uncommitted things at the moment,
both theoretical and related to some Julia experiments).

---

It's Dec 3 now, and here I want to write down some more recent (Nov 28) considerations.

Let's step back and recall that this architecture is also a generalization of digital audio synthesis via composition of
unit generators (which is, in fact, an unrecognized form of neural networks).

One of the most productive neurons in that setup is the neuron with 3 inputs and _sin(a*x+y)_ as an activation function.
It allows various audiomodulations and such. We need to consider a matrix generalization of this neuron.
