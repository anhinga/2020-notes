## Theory problems on DMMs as Transformer-like machines

Consider June 2019 preprint here: https://github.com/anhinga/2019-design-notes/tree/master/research-notes

Consider its Section 3, which explains how to rewrite the two-step cycle of a recurrent DMM in a more
compact fashion (compose a very generic non-linear operation and matrix multiplication).

If one thinks about "recurrent Transformers", this is, in some sense, a Transformer-like way to
express a recurrent DMM.

It should be extremely fruitful to study this set-up more closely.

Some of the key topics are:

 * translate our programming exercises into this set-up;
 * express weight changes as part of the internal dynamics (instead of external modification by "training").
 
---
 
To narrow this down, we can focus on our 2018 experiments in modifying running DMMs on the fly:

We edit a running network on the fly by sending it requests to edit itself. In particular, this enables live-coding, but this is also quite open-ended, since it enables a population of networks to tell each other to modify themselves (these networks can run independently from each other, or can be embedded into a single DMM); of course,  the receiving network doesn’t have to follow an incoming instruction to self-modify blindly, although in the most simple-minded case it would do so. 

(See section 3 of https://www.cs.brandeis.edu/~bukatin/dmm-collaborative-research-agenda.pdf
and section 1.1 of https://www.cs.brandeis.edu/~bukatin/dmm-notes-2018.pdf )

This is a good starting point. 

If we figure out the translation of this particular problem we solved in 2018 to the "recurrent Transformers" set-up,
we'll have a good feel for handling this "recurrent Transformers" set-up
in general in a self-referential fashion.

The "recurrent Transformer" set-up has (generally speaking non-linear) generation of a pair of matrices and their subsequent multiplication
as a repeated work cycle. So, we stop hiding the changing network matrix within the current network output, and instead treating the two matrices in
a symmetric fashion. 

When a neural net is self-modifying, what people think about as "linear part of the work cycle of a neural machine" is actually quadratic; 
in this set-up the quadratic aspect is more explicit: we generate two matrices and then multiply them. (The quadratic aspect of the self-referential
situation was first pointed out to me by Andrey Radul a few years ago.) 
