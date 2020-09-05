## CCC 2020: Continuity, Computability, Constructivity – From Logic to Algorithms

(Online, instead of Faro (Portugal), August 31 – September 4, 2020)

http://cid.uni-trier.de/ccc-2020-continuity-computability-constructivity-from-logic-to-algorithms-faro-portugal-august-31-september-4-2020/

---

Title:

_Higher-order neuromorphic computations with linear streams (extended abstract)_

---

Abstract:

 There is a rich theory linking the ability to endow Scott domains with a structure of vector spaces and the logic of partial contradictions. The discipline of programming with linear streams (streams equipped with an operation of taking a linear combination of several streams) is rich enough to serve as a general purpose programming platform. We call neural machines working with arbitrary linear streams Dataflow Matrix Machines (DMMs). They provide a programming platform where programs can be continuously deformed. We explore self-modifying DMMs with a dedicated neuron Self handling a stream of network-sized matrices.

Published PDF:

https://www.ualg.pt/sites/ualg.pt/files/u13559/ccc_2020_paper_6.pdf

Published slides for my September 3, 2020 talk:

http://cid.uni-trier.de/additional_media/Michael_Bukatin.pdf

## Comment

Historically, dataflow matrix machines emerged from our research on mathematical of partial inconsistency
and vector semantics of programming languages based on bicontinuous domains with
two Scott topologies (see Section 11 of https://arxiv.org/abs/1712.07447 for history of this).

Usually, we forget that programming with linear streams is related to bicontinuous domains,
and we just use plain vector spaces in DMMs and neuromorphic computations, and this is
mostly fine, but we lose the potential hidden in the math of partial inconsistency and
bicontinuous domains.

This conference presentation is an attempt to shed the light on this aspect of
mathematics related to DMMs and to hopefully resume taking advantage of that potential
(in particular, of two-directional monotonic computations with involution,
of paraconsistent fuzzy logic, and so on).

One comment/question during the presentation was whether we actually tried to develop
denotational semantics of DMMs based on bicontinuous domains (we have not, but it would
be very interesting).

Another question is whether we would actually like using lazy computations in DMMs
(the answer is, probably yes, as long as we don't try to make them real-time,
e.g. if we are using all these for audio synthesis or visual animation synthesis in
real time, lazyness tends to be a headache to deal with; otherwise it's fine).
