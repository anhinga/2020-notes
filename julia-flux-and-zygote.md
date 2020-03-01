# Julia Flux and Zygote

Should we start implementing DMMs in Julia?

## Julia Flux blog post

Building a Language and Compiler for Machine Learning

https://julialang.org/blog/2018/12/ml-language-compiler/

## Julia Zygote

Julia Flux is based on the new source-to-source system of automatic differentiation, **Zygote**,
which claims to be the best in the world at the moment 
(it is certainly better than anything I've seen so far):

https://github.com/FluxML/Zygote.jl

https://arxiv.org/abs/1810.07951

https://arxiv.org/abs/1907.07587

(See, in particular, Section 5, "Related Work", of the latest version of the paper (March 2019).)

They say that the approach can support the full flexibility and dynamism of the Julia language, 
including control flow, nesting, mutation, recursion, closures, data structures (structs, dictionaries, etc.), 
higher-order functions, and other language constructs, 
and that the output is given to an existing compiler to produce highly efficient differentiated code.

## Julia Flux

It is presented as **"the ML library that doesn't make you tensor"**.

https://github.com/FluxML/Flux.jl

_So, this seems to be a perfect fit for dataflow matrix machines, 
where we can truly benefit from not having to contort things into fixed-shape tensors 
and from the ability to take gradients of arbitrary source code._

This is a great framework for many other machine learning applications as well.

Fashionable Modelling with Flux: https://arxiv.org/abs/1811.01457

Their front page is very cool:

https://fluxml.ai/
