# TeAAL specifications on Loops (OLD)
This directory contains old-style of writing the TeAAL specification for Loops, with input variables `NUM_SM` and `WARP_SIZE`:

Example: 
- `NUM_SM` = 2 (Number of GPU SMs) 
- `WARP_SIZE` = 2 (Number of threads per warp)
- `NUM_THREADS` = `NUM_SM` * `WARP_SIZE` (Total number of threads)