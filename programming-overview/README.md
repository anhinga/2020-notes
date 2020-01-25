# Overview of programming techniques and examples in DMM literature

## Initial reading

Introduction to https://arxiv.org/abs/1606.09470 ("Programming Patterns in Dataflow Matrix Machines and Generalized Recurrent Neural Nets"),
that's first 6 pages of this paper.

## Accumulators

With one input: Section 1.3.1 (page 3) of https://arxiv.org/abs/1606.09470, first use Section 3.1 (page 8) of the same paper.

With two inputs, "accum" and "delta" (or "X" and "DeltaX"): introduced in Section 6 (page 4) of https://arxiv.org/abs/1610.00831 
("Notes on Pure Dataflow Matrix Machines: Programming with Self-referential Matrix Transformations").

More details of accumulators with two inputs and a figure: Section 6.1 (pages 16-18) of 
https://arxiv.org/abs/1712.07447 ("Dataflow Matrix Machines and V-values: a Bridge between Programs and Neural Nets")

## Self-referential mechanism

Originally introduced: Section 1.4 (page 3) of https://arxiv.org/abs/1605.05296 
("Dataflow matrix machines as programmable, dynamically expandable, self-referential generalized recurrent neural networks").

Details of how that works: Section 3.3-3.7 (page 6-8) of this paper.

Overview for the accumulator with two inputs: Section 7 (pages 20-21) of https://arxiv.org/abs/1712.07447

## Using accumulators in general

  * For the purpose of maintaining the map  "character" => "number of occurences of that character":
    Section 3.1 (page 8) of https://arxiv.org/abs/1606.09470 (in context of the solution of the first problem
    from "Cracking the Coding Interview" book, Section 1.2 (page 2) and Section 3 (pages 8-10) of this paper.

  * Similarly, a map "word" => "number of occurences of that word" can be maintained. It's an infinitely-dimenstional
    sparse vector, which can be maintained by a single neuron connected in such a fashion as to form an accumulator.



## Using self-referential mechanism
