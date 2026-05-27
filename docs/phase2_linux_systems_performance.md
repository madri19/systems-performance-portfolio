# Phase 2 - Linux Systems Performance Lab

Repository:

- https://github.com/madri19/linux-systems-performance-lab

## Focus

Phase 2 studied multicore Linux performance on x86_64 desktop hardware and validated selected results on ARM server hardware.

## Phase 2A

Platform:

- AMD Ryzen 5 5600X
- x86_64
- 6 physical cores
- 12 logical CPUs
- WSL2 Linux

Topics:

- CPU-bound scaling
- false sharing
- mutex contention
- atomic contention
- CPU affinity
- memory bandwidth
- cache locality
- allocator behavior
- thread pools
- producer/consumer queues
- SPSC ring buffers
- perf/flamegraph analysis

## Phase 2B

Platform:

- AWS Graviton4
- Arm Neoverse-V2
- aarch64
- c8g.xlarge
- 4 vCPUs

Purpose:

- prove the benchmark suite builds and runs on ARM server-class hardware
- capture initial x86-to-ARM comparison data
- document ARM PMU/perf caveats

## Main Lesson

Multicore CPU performance is usually limited by coordination and locality costs:

- shared hot state
- cache-line ownership
- lock contention
- atomic contention
- memory locality loss
- queue contention
- allocator overhead
