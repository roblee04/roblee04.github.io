---
title: "Running a Large Language Model on my School Supercomputer"
date: 2024-05-22
draft: false
categories: ["projects"]
tags: ["llm", "hpc", "ai"]
---

## Welcome!

I was having some fun browsing /r/localLLaMA and I saw that llama3 popped up!

At the time it was real good for its parameter size and just in general, so I wanted to try to run it!

Of course, I could've ran it in a Q5 quantized form on my desktop with a 1080ti, however, I felt like using my school funding to use. (T.T 78k per year)

## SCU's WAVE HPC Cluster

As a student in the school of engineering and having taken courses that utilized resources from the HPC, I was able to grab a hold of nodes that included NVIDIA Tesla V100 32G (up to 2x) or AMD Instinct MI100 GPU (up to 8x!).

Because there is often more support (and less issues with NVIDIA) regarding LLM frameworks and libraries I chose to use the V100.

## Setup

ollama backend + ngrok port forwarding + sillytavern frontend

1. Manual install of ollama in .local/bin
2. srun onto your favorite V100 gpu instance
3. ollama serve & and ollama run llama3
4. ngrok localhost:11434 and port forward to your favorite domain
5. connect to silly tavern!
6. ??? Profit

Now you can run your very own AI therapist! (at the cost of your hardware and budget!)