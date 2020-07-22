# Transformer attention

The attention model used in Transformers is a development of "content-based neural attention" ([simple-minded-attention.md](https://github.com/anhinga/2020-notes/blob/master/attention-based-models/simple-minded-attention.md))

The difference is in the way the relevance coefficients are computed. Instead of "value vectors", we have pairs
"key vector, value vactor". One takes a "query vector" of the same dimension as "key vectors", and the
scalar products between "query vectors" and "key vectors" form relevance coefficients
("Attention Is All You Need", https://arxiv.org/abs/1706.03762).
