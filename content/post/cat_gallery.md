---
title: "Making of Cat Gallery! Part 1"
date: 2024-07-18
draft: false
categories: ["projects"]
tags: ["cats", "server", "ai"]
---

## Motivation and Inspiration

Mimi and Leo, my two cats. I love them.

Modern search engines aren't very good at finding pictures (only via metadata). I think vision models are pretty cool.

## What's the basic idea?

Have an API to do the search!

- provided by the image server
- files live on the image server
- actually, the image server does all the computation

The API is then called by some static site.

In this case, it is cat_gallery aka our website. In order to achieve these goals, I am using Flask for the image server and React for my frontend.

## What is this magical API?

For simplicity and ease of use, I am using RCLIP, an open-source utility that makes it really easy to use CLIP vision transformer models.

This API essentially just parses the JSON payload that it's given and sends it straight to rclip to be processed.

## Where do the images come from?

Mainly two places:
- cat faces dataset on HuggingFace
- this wonderful dude who preprocessed a bunch of other cat datasets

## What does it look like right now?

Well, pretty good actually.

Basically everything you can do in rclip, you can do in here:
- Multiterm queries
- Term weighting
- Image to image search

## Next steps

- More pictures (I gotta scrape images)
- Faster API / faster inference
  - Horizontal (hardware) or vertical improvements (software)
  - More parallel / batched or more CPU/GPU
  - Potential upside in using a vector database instead of SQL
- Cooler frontend (I am trash at doing UI/UX)
- Deployment
  - Free React deployment is easy
  - Free Backend deployment is hard
  - AWS lambda functions concern of losing infinite money due to infinite scaling
- Handling many users
  - Currently Synchronous, maybe turn to Async for scaling
- Duplicate removal