# Implicit MetaLearning

_Roughly speaking_, one can talk about two kinds of metalearning. One is _metalearning on the level of methods
of learning/methods of synthesis_: better optimizers,
better population-based methods, better evolutionary methods, or any mixture of those. This kind of metalearning
is of particular interest to me, but we are not talking about it here.

Another kind of metalearning is _metalearning on the level of model_: learning a model with properties that it is learning new
tasks better (usually, with a fixed optimizer). This kind of metalearning is the one which is particularly popular
lately (see, e.g. Model-Agnostic Meta-Learning, https://bair.berkeley.edu/blog/2017/07/18/learning-to-learn/ ).

The fact that inexpensive transfer learning or inexpensive fine-tuning is possible in many machine learning models
such as neural nets and transformers implies that **implicit metalearning** is happening during their training
or pretraining.

We know that rich structure is formed within neural nets and transformers during training, and it is likely
that that rich structure is what making the resulting model a convenient and efficient starting point for
further learning.
