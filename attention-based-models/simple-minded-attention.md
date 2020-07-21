# Comment on the simple-minded pragmatic attention ("content-based neural attention").

The idea due to Dzmitry Bahdanau (Dzmitry Bahdanau, Kyunghyun Cho, Yoshua Bengio, "Neural Machine Translation by Jointly Learning to Align and Translate", https://arxiv.org/abs/1409.0473) is extremely simple. 

There a number of "value vectors",
which are high-dimensional. A model computes relevances of each of those vectors,
and transforms the vector of relevances to probabilities by applying _softmax_.

Then one "applies the attention defined by this vector of probabilities" by taking
the linear combination of "value vectors" with these probabilities as coefficients.

This is super-simple. The question one wants to ask: "why do you say this resembles attention",
"why could one think aboyt this scheme as a natural model of attention"?

---

I am going to offer the following explation.


