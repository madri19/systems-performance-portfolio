# Systems Performance Portfolio

A three-phase systems-performance portfolio covering embedded Linux, multicore CPU performance, ARM server validation, and CUDA heterogeneous performance.

## Overview

ARM embedded Linux -> multicore Linux systems performance -> ARM server validation -> CUDA GPU performance -> profiling-backed bottleneck analysis

## Projects

| Phase | Repository | Focus |
|---|---|---|
| Phase 1 | [arm-embedded-linux-performance-lab](https://github.com/madri19/arm-embedded-linux-performance-lab) | Embedded ARM Linux, Buildroot, system calls, constrained hardware behavior |
| Phase 2 | [linux-systems-performance-lab](https://github.com/madri19/linux-systems-performance-lab) | Multicore CPU scaling, contention, cache locality, perf/flamegraphs, ARM server smoke validation |
| Phase 3 | [cuda-heterogeneous-performance-lab](https://github.com/madri19/cuda-heterogeneous-performance-lab) | CUDA kernels, memory transfer overhead, GPU bandwidth, shared memory, streams, Nsight profiling |

## Core Lessons

Raw hardware capability is not enough.

Performance is shaped by coordination cost, memory locality, synchronization, transfer overhead, and profiling discipline.

Key lessons:

- More threads do not automatically improve throughput.
- Shared mutable state often destroys scaling.
- Cache-line ownership and false sharing matter.
- Atomics are cheaper than mutexes but still not free.
- Per-thread aggregation often beats shared counters.
- GPU kernels can be much faster than CPU loops.
- GPU end-to-end speed depends on transfer cost.
- Pinned memory can significantly improve transfer-heavy CUDA paths.
- Shared memory helps when it improves global-memory access patterns.
- Profiling tools are necessary to explain bottlenecks.

## Status

Phase 1: complete

Phase 2: complete

Phase 3A: complete
