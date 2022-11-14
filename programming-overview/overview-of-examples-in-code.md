# Overview of DMM-related examples in code

## Pre-DMM dataflow animations (Processing)

Described in https://arxiv.org/abs/1601.00713 ("Almost Continuous Transformations of Software and Higher-order Dataflow Programming")

  * fixed dataflow graph: https://github.com/anhinga/fluid/tree/master/may_9_15_experiment
  
  * dynamically changing dataflow graph: https://github.com/anhinga/fluid/tree/master/jun_28_15_experiment

Further use of this pre-DMM architecture:

  * https://github.com/anhinga/fluid/tree/master/atparty-2018/surreal_webcam

## First DMMs: continuous cellular automata (Processing)

  * Described in Section 4 (page 7) of https://arxiv.org/abs/1601.01050 ("Dataflow Graphs as Matrices and Programming with Higher-order Matrix Elements")

  * Implementation: https://github.com/anhinga/fluid/tree/master/aug_20_15_experiment

  * With fully higher-order matrix elements: Section 4.1 (page 8) of the same paper

  * Implementation: https://github.com/anhinga/fluid/tree/master/aug_24_15_experiment

## First self-referential DMMs (Processing and Clojure)

Described in Appendix D.2 (page 6) of https://arxiv.org/abs/1610.00831

https://github.com/anhinga/fluid/tree/master/Lightweight_Pure_DMMs

First implementation of propagating wave pattern: https://github.com/anhinga/fluid/tree/master/Lightweight_Pure_DMMs/aug_27_16_experiment

Same example in Clojure:

  * https://github.com/jsa-aerial/DMM/blob/master/examples/dmm/oct_19_2016_experiment.clj 
  
  * https://github.com/jsa-aerial/DMM/blob/master/examples/dmm/quil-controlled/jul_6_2017_experiment.clj

Also described in Appendix B.2 (page 6) of https://arxiv.org/abs/1706.00648

## Accumulating the list of mouse clicks (Clojure)

Described in Section 6.3 (pages 18-19) of https://arxiv.org/abs/1712.07447

https://github.com/jsa-aerial/DMM/blob/master/examples/dmm/quil-controlled/jul_13_2017_experiment.clj

## Using self-referential facilities to edit the network on the fly (Clojure)

Described in Section 1.1 (page 3) of https://www.cs.brandeis.edu/~bukatin/dmm-notes-2018.pdf 

https://github.com/jsa-aerial/DMM/tree/master/examples/dmm/quil-controlled/interactive

## Randomly initialized self-referential lightweight pure DMMs (Processing)

With emerging patterns, Section 1.2 (pages 3-4) of https://www.cs.brandeis.edu/~bukatin/dmm-notes-2018.pdf 

https://github.com/anhinga/fluid/tree/master/atparty-2018/game_of_afterlife

https://github.com/anhinga/fluid_drafts

*****************************

## Rough drafts

### Drawing with a mouse (Python)

https://github.com/anhinga/population-of-directions/tree/master/drafts

to be continued at https://github.com/anhinga/typed-dmms

### Initial half-baked attempts at interactive evolution (Processing)

https://github.com/anhinga/fluid/tree/master/Lightweight_Evolutionary

*****************************

## Indirectly related software experiments

### Regularization in intrinsically sparse networks (PyTorch)

https://github.com/anhinga/synapses/blob/master/regularization.md

### Shaders (GLSL and Python/VisPy)

https://github.com/anhinga/2019-python-drafts/tree/master/vispy/atparty-2019

### Prototyping small bits and pieces for the next generation of DMMs (Python and JavaScript)

https://github.com/anhinga/2019-python-drafts

### Initial program synthesis (DMM synthesis, circuit synthesis) experiments (Julia, May-September 2022)

https://github.com/anhinga/DMM-synthesis-lab-journal/blob/main/history.md
