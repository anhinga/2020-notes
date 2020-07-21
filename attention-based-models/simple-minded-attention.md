# Comment on the simple-minded pragmatic attention ("content-based neural attention").

The idea due to Dzmitry Bahdanau (Dzmitry Bahdanau, Kyunghyun Cho, Yoshua Bengio, "Neural Machine Translation by Jointly Learning to Align and Translate", https://arxiv.org/abs/1409.0473) is extremely simple. 

There a number of "value vectors",
which are high-dimensional. A model computes relevances of each of those vectors,
and transforms the vector of relevances to the vector of probabilities by applying _softmax_.

Then one "applies the attention defined by this vector of probabilities" by taking
the linear combination of "value vectors" with these probabilities as coefficients.

This is super-simple. The question one wants to ask: "why do you say this resembles attention?",
"why could one think about this scheme as a natural model of attention?".

---

I am going to offer the following explation.

The situation when this terminology works really, really well is the following one.

Assume that the "value vectors" are fairly high-dimensional and sparse (in the sense,
that not too many coordinates of each vector are substantially different from zero;
we'll even think that the number of "leading terms" (coordinates which are quite far from zero)
is small, and then there might be some less prominent non-zero coordinates, but not too many).

Then if you just add them all together (with all coefficient being one), this is not too
far from the union of all these values (ideally, the sparseness is such that different vectors
don't intersect too much, so there is an extra assumtion here that "value vectors" are
"almost independent").

Then multiplication by probabilities before adding them all together would attenuate the
non-attended ones.

If we think that coordinates below some treshold become effectivelt zeros (**in principle,
one could include an explicit sparsification step to zero them out**), then some vectors
will disappear completely from the picture (even their leading "terms" (coordinates) will become
too small), while some other "semi-attended vectors" will remain, but "lose resolution"
(some of their less prominent non-zero coordinates will become too small to register anymore).

Now, this actually starts resembling attention; one only actually sees the "objects" (value vectors),
which one attends to, and there are "semi-attended objects on the 'border of the circle of attention'",
and those semi-attended objects are visible, but with lower resolution/less detail.

Now, this suddenly looks like our familiar attention, and is reasonably consistent with my
introspection of my own visual attention (as long as we can "identify" coordinates of
value vectors with features of visual objects I see.)
