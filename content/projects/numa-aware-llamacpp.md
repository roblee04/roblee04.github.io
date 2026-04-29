---
title: "NUMA-Aware llama.cpp"
date: 2025-01-15
draft: false
featured: true
weight: 10
thumbnail: "/thumbnails/llamacpp-logo.png"
description: "High-performance optimizations for llama.cpp to maximize efficiency on multi-socket server hardware by replicating model weights across NUMA nodes."
technologies: ["C++", "GGML", "NUMA", "Performance Optimization", "Linux APIs"]
github: "https://github.com/roblee04/numa_llamacpp"
status: "Completed"
---

## NUMA-Aware llama.cpp

This project implements high-performance optimizations for the llama.cpp inference engine to maximize efficiency on multi-socket server hardware.

### Overview

Standard LLM inference often suffers from memory bandwidth bottlenecks on multi-socket (NUMA) systems. By replicating model weights across NUMA nodes and enforcing strict thread affinity, this optimization eliminates interconnect bottlenecks and significantly improves performance.

### Key Features

- **Dual-Buffer Weight Replication**: Replicates model weights in local DRAM banks for each NUMA node.
- **Strict Thread Pinning**: Ensures worker threads remain on their assigned cores to maximize cache locality.
- **Surgical Implementation**: Integrated as a clean, gated extension to the GGML backend.
- **Zero-Overhead Hooking**: Uses a pointer-swapping hook in the core GEMM (matrix multiplication) kernels.

### Technical Accomplishments

- **Significant Speedups**:
  - **1.75× increase** for Llama 3.3 70B on dual AMD EPYC 9654 hardware.
  - **1.45× increase** for Llama 3 8B.
- **Interconnect Optimization**: Reduced cross-socket Infinity Fabric traffic to near zero.
- **Memory Locality**: Guaranteed 100% local DRAM reads for model weights.

### Source Code

[View on GitHub →](https://github.com/roblee04/numa_llamacpp)
