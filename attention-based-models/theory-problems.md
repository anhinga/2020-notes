## Theory problems on DMMs as Transformers

Consider June 2019 preprint here: https://github.com/anhinga/2019-design-notes/tree/master/research-notes

Consider its Section 3, which explains how to rewrite the two-step cycle of a recurrent DMM in a more
compact fashion (compose a very generic non-linear operation and matrix multiplication).

If one thinks about "recurrent Transformers", this is, in some sense, a Transformer-like way to
express a recurrent DMM.

It should be extremely fruitful to study this set-up more closely.

Some of the key topics are:

 * translate our programming exercises into this set-up;
 * express weight changes as part of the internal dynamics (instead of external modification by "training").
