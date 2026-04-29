---
title: "Auto-tuning LoRA Hyperparameters"
date: 2024-06-01
draft: false
featured: true
weight: 50
thumbnail: "/thumbnails/lora-logo.png"
description: "Optimizing fine-tuning for Llama3, Qwen2, and Mistral using QLoRA and GPTune Bayesian auto-tuning framework to improve training efficiency."
technologies: ["Python", "PyTorch", "QLoRA", "Bayesian Optimization", "GPTune", "LLMs"]
github: "https://github.com/roblee04"
paper: "/files/lora-autotuning.pdf"
status: "Completed"
---

## Applied Auto-tuning on LoRA Hyperparameters

This project focuses on optimizing the fine-tuning process for Large Language Models (LLMs) by efficiently discovering optimal hyperparameters for Quantized Low-Rank Adaptation (QLoRA).

### Overview

Fine-tuning LLMs like Llama 3 8B, Qwen 2 8B, and Mistral 7B requires careful selection of hyperparameters such as rank (r), alpha, and learning rate. Manual tuning is computationally expensive and often sub-optimal. This project implements a pipeline utilizing **GPTune**, a Bayesian auto-tuning framework, to automate this search.

### Key Contributions

- **Efficient Hyperparameter Discovery**: Developed a pipeline that utilizes Bayesian optimization to find the best QLoRA configurations.
- **Model Support**: Validated across multiple state-of-the-art open-source models (Llama 3, Qwen 2, Mistral).
- **Resource Efficiency**: Improved the trade-off between training time and model loss, ensuring high performance without increasing computational overhead.

### Technical Results

- **30% Reduction in Training Loss**: Achieved significantly better convergence compared to random search baselines.
- **Constant Computational Cost**: Maintained training time and perplexity while achieving lower loss.
- **Quantization Integration**: Leveraged 4-bit quantization (QLoRA) to make high-quality fine-tuning accessible on consumer-grade hardware or shared HPC resources.

### Thesis Paper

<div style="margin: 2rem 0; padding: 1rem; background: #f5f5f5; border-radius: 8px;">
  <object data="/files/lora-autotuning.pdf" type="application/pdf" width="100%" height="600px">
    <p>Unable to display PDF file. <a href="/files/lora-autotuning.pdf">Download instead</a>.</p>
  </object>
</div>

[Download PDF →](/files/lora-autotuning.pdf)
