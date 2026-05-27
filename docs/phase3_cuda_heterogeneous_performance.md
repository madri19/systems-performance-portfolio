# Phase 3 - CUDA Heterogeneous Performance Lab

Repository:

- https://github.com/madri19/cuda-heterogeneous-performance-lab

## Focus

Phase 3 studied CUDA and heterogeneous CPU/GPU performance.

## Platform

- NVIDIA GeForce RTX 3060 Ti
- 8 GiB VRAM
- Compute capability 8.6
- CUDA Toolkit 13.2
- WSL Ubuntu 26.04

## Topics

- CUDA device properties
- vector-add baseline
- CPU vs GPU kernel throughput
- host/device transfer overhead
- GPU memory bandwidth
- grid/block scaling
- shared-memory tiling
- CUDA streams
- pinned memory
- CUDA reduction
- Nsight Systems
- Nsight Compute

## Main Results

Kernel-only GPU vector-add speedup:

- about 18x over CPU

End-to-end vector-add result:

- slower than CPU when host/device transfer was included

Pinned memory:

- significantly reduced transfer-heavy runtime

Shared-memory transpose:

- about 3x faster than naive transpose

Reduction:

- about 43x kernel-only speedup over CPU

## Main Lesson

GPU performance must be evaluated end-to-end.

Fast kernels do not guarantee fast applications if transfer overhead dominates.
