# Comment on the simple-minded pragmatic attention ("content-based neural attention").

The idea due to Dzmitry Bahdanau is extremely simple. There a number of "value vectors",
which are high-dimensional. A model computes relevances of each of those vectors,
and transforms the vector of relevances to probabilities by applying _softmax_.

