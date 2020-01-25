# Overview of programming techniques and examples in DMM literature

## Initial reading

Introduction to https://arxiv.org/abs/1606.09470 ("Programming Patterns in Dataflow Matrix Machines and Generalized Recurrent Neural Nets"),
that's first 6 pages of this paper.

A more recent and high-level description: Section 6 (pages 16-19) of https://arxiv.org/abs/1712.07447 ("Dataflow Matrix Machines and V-values: a Bridge between Programs and Neural Nets")

## Accumulators

With one input: Section 1.3.1 (page 3) of https://arxiv.org/abs/1606.09470, first use Section 3.1 (page 8) of the same paper.

With two inputs, "accum" and "delta" (or "X" and "DeltaX"): introduced in Section 6 (page 4) of https://arxiv.org/abs/1610.00831 
("Notes on Pure Dataflow Matrix Machines: Programming with Self-referential Matrix Transformations").

More details of accumulators with two inputs and a figure: Section 6.1 (pages 16-18) of 
https://arxiv.org/abs/1712.07447

## Self-referential mechanism

Originally introduced: Section 1.4 (page 3) of https://arxiv.org/abs/1605.05296 
("Dataflow matrix machines as programmable, dynamically expandable, self-referential generalized recurrent neural networks").

Details of how that works: Section 3.3-3.7 (page 6-8) of this paper.

Overview for the accumulator with two inputs: Section 7 (pages 20-21) of https://arxiv.org/abs/1712.07447

## Using accumulators in general

  * For the purpose of maintaining the map  "character" => "number of occurrences of that character":
    Section 3.1 (page 8) of https://arxiv.org/abs/1606.09470 (in context of the solution of the first problem
    from "Cracking the Coding Interview" book, Section 1.2 (page 2) and Section 3 (pages 8-10) of this paper).

  * Similarly, a map "word" => "number of occurrences of that word" can be maintained. It's an infinitely-dimenstional
    sparse vector, which can be maintained by a single neuron connected in such a fashion as to form an accumulator.

  * To accumulate a list of mouse clicks using V-values: Section 6.3 (pages 18-19) of https://arxiv.org/abs/1712.07447
  
  * See also the Python examples of drawing with a mouse with an accumulator holding the resulting image
    at the **"Overview of DMM-related examples in code"** in this directory:
    https://github.com/anhinga/2020-notes/blob/master/programming-overview/overview-of-examples-in-code.md

## Using self-referential mechanism

  * To create a wave pattern in the network matrix: Appendix B.2 (page 6) of https://arxiv.org/abs/1706.00648 
    ("Dataflow Matrix Machines as a Model of Computations with Linear Streams")
    
  * To edit a running DMM on the fly: Section 1.1 (page 3) of https://www.cs.brandeis.edu/~bukatin/dmm-notes-2018.pdf
    ("Dataflow matrix machines: recent experiments and notes for next steps")
    
  * To explore emerging patterns in a randomly initialized self-referential DMM: Section 1.2 (pages 3-4) of the same
    paper, https://www.cs.brandeis.edu/~bukatin/dmm-notes-2018.pdf

## Creating a deep copy of a network subgraph on the fly

  * Pre-DMM algorithm and implementation: Section 4.3 (pages 7-8) of https://arxiv.org/abs/1601.00713 
    ("Almost Continuous Transformations of Software and Higher-order Dataflow Programming")
    
  * Matrix-based formalism (not implemented yet): Section 4 (pages 10-12) of https://arxiv.org/abs/1606.09470
  
  * Formulas for matrix-based formalism for Pure DMMs (not implemented): Section 5.2 (pages 3-4) of https://arxiv.org/abs/1610.00831
  
## Non-flat network matrix (using arbitrary V-value as a network matrix)

Not implemented, but discussed in multiple places (prompted by the desire to naturaly share common parts when deep copying network subgraphs instead of duplicating them (this should certainly be feasible if programming with immutable data)).

  * Initial discussion lifted and condensed from e-mails: Section 2.3 (page 5) of 
    https://www.cs.brandeis.edu/~bukatin/dmm-notes-2018.pdf
  
  * More thoughts (but I am uncertain about those thoughts, they are just something to possibly keep in mind): 
    Section 5 (page 3) and Endnote 3 (page 4) of
    https://github.com/anhinga/2019-design-notes/blob/master/research-notes/dmm-notes-june-2019.pdf

  * In the general case (when not only column indices, but also row indices are hierarchical), one needs to formalize
    where in a path the row index ends and the column index starts. One should probably think about this situation in the spirit
    of Section 5.3 (page 16) of https://arxiv.org/abs/1712.07447 (more specifically, one should think about V-values as leaves of
    V-values, so that the overall space is either V tensor product by V or V tensor product by sum of V and R). There is
    some interesting fairly open-ended math here.    

## Overview of DMM-related examples in code

https://github.com/anhinga/2020-notes/blob/master/programming-overview/overview-of-examples-in-code.md
