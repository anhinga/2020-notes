# Implicit MetaLearning

_Roughly speaking_, one can talk about two kinds of metalearning. One is _metalearning on the level of methods
of learning/methods of synthesis_: better optimizers,
better population-based methods, better evolutionary methods, or any mixture of those. This kind of metalearning
is of particular interest to me, but we are not talking about it here.

Another kind of metalearning is _metalearning on the level of model_: learning a model with properties that it is learning new
tasks better (usually, with a fixed optimizer). This kind of metalearning is the one which is particularly popular
lately (see, e.g. Model-Agnostic Meta-Learning, https://bair.berkeley.edu/blog/2017/07/18/learning-to-learn/ ).

The fact that inexpensive transfer learning or inexpensive fine-tuning is possible in many machine learning models
such as neural nets and transformers implies that **implicit metalearning on the level of model** is happening during their training
or pretraining.

We know that rich structure is formed within neural nets and transformers during training, there were a lot
of studies visualizing that structure, and it is likely
that that rich structure is what making the resulting model a convenient and efficient starting point for
further learning.

GPT-3 takes this **implicit metalearning** to an entirely new level. Here is what one of the first authors
of the GPT-3 paper is writing about this in the following thread:

https://twitter.com/nottombrown/status/1266188687219384320

```
Language models are few shot learners! We find that larger models can often (but not always) perform NLP tasks given only natural language prompt and a few examples in the context. No fine-tuning.

This "in-context learning" happens entirely within the forward-pass on a single sequence. We study this in the zero-, one- and few-shot settings.

One way to think about this: In-context learning is the inner loop of meta-learning, and unsupervised pre-training is the outer loop. To do well at pre-training, a language model needs to learn to quickly recognize patterns within the context of a given sequence.
```
