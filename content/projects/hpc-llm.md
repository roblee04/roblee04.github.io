---
title: "LLM on HPC Cluster"
date: 2024-05-22
draft: false
featured: false
weight: 40
thumbnail: "/thumbnails/meta-ollama-llama3.png"
description: "Running Llama 3 and other large language models on SCU's WAVE HPC cluster with NVIDIA V100 GPUs for research and experimentation."
technologies: ["Python", "Ollama", "LLM", "HPC", "SLURM", "Docker"]
github: "https://github.com/roblee04"
status: "Completed"
---

## Running LLMs on SCU's Supercomputer

A project exploring running large language models on SCU's WAVE HPC cluster with NVIDIA V100 GPUs.

### Overview

I was having fun browsing /r/localLLaMA and saw that llama3 had just been released. At the time, it was state-of-the-art for its parameter size, so I wanted to run it!

### Technical Setup

- **Hardware**: NVIDIA Tesla V100 32G GPUs on SCU's WAVE cluster
- **Software**: Ollama backend + ngrok port forwarding + SillyTavern frontend
- **Model**: Llama 3 (various quantizations)

### Steps

1. Manual install of ollama in `.local/bin`
2. `srun` onto a V100 GPU instance
3. Run `ollama serve &` and `ollama run llama3`
4. Port forward with ngrok
5. Connect to SillyTavern frontend

### Key Learnings

- HPC job scheduling with SLURM
- LLM inference optimization
- GPU resource management
- Network tunneling for remote access

### Outcome

Successfully ran Llama 3 with reasonable inference speeds on the V100, demonstrating the feasibility of running LLMs on academic HPC resources.

[Read the full blog post →](/post/hpc_llm/)