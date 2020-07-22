# Transformer attention

The attention model used in Transformers is a development of "content-based neural attention" ([simple-minded-attention.md](https://github.com/anhinga/2020-notes/blob/master/attention-based-models/simple-minded-attention.md)).

The difference is in the way the relevance coefficients are computed. Instead of "value vectors", we have pairs
"key vector, value vactor". One takes a "query vector" of the same dimension as "key vectors", and the
scalar products between "query vectors" and "key vectors" form relevance coefficients
("Attention Is All You Need", https://arxiv.org/abs/1706.03762).

Let's ponder a bit what this means. First, let's introduce "generalized neural attention",
where we allow to take arbitrary coefficients instead of probabilities (that is, we omit _softmax_).

Let's assume for a moment that "key vectors" are orthogonal to each other. Then the "query vector" in
question can be obtained as sum of the "key vectors" with relevance coefficients (so a "generalized neural attention"
is applied to the "key vector", and this retrieves the "query vector" back). If the orthogonality of "key vectors"
is approximate, then this observation also becomes approximate.
