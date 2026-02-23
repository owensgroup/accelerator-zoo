# TeAAL specifications on Loops
This directory contains TeAAL specifications written based on different load balance strategy from [Loops](https://github.com/gunrock/loops).

Variants:
- SpMV: Original = Thread-Mapped, Group-Mapped, Work-Oriented = Merge Path (WIP)
- SpMM: Thread-Mapped, Group-Mapped
- SpGEMM: Thread-Mapped, Group-Mapped

Terminology (From [A Programming Model for GPU Load Balancing](https://arxiv.org/abs/2301.04792)):
- Work item/atom: A single unit of work that is to be scheduled onto the GPU. We assume that all work atoms have an equal cost during execution.
- Work tile: A collection of work items. Work tiles may have different costs during execution. Work is most logically parallelized over work tiles but is often most efficiently parallelized over work atoms, and mapping between work tiles and work atoms may be expensive and complex.
- Work set: A set of work tiles that together comprise the entire working problem. Tiles within a tile set must be independent (and thus can run in parallel across multiple processors).