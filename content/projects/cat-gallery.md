---
title: "Cat Gallery - AI Image Search"
date: 2024-07-18
draft: false
featured: true
thumbnail: "/thumbnails/cat.png"
description: "An AI-powered image search application using CLIP vision transformers to find similar cat pictures with semantic search capabilities."
technologies: ["Python", "Flask", "React", "CLIP", "RCLIP", "Computer Vision"]
github: "https://github.com/roblee04"
status: "In Progress"
---

## Cat Gallery - AI-Powered Image Search

An AI-powered image search application that uses vision transformers to find similar cat pictures!

### Motivation

Mimi and Leo, my two cats. I love them! Modern search engines aren't very good at finding pictures (only via metadata). Vision models are pretty cool!

### How It Works

1. **Image Server**: Flask backend with RCLIP for embedding generation
2. **Frontend**: React-based UI for search queries
3. **Search**: Uses CLIP vision transformer models for semantic image search

### Features

- **Multiterm queries**: Search with multiple keywords
- **Term weighting**: Weight search terms for better results
- **Image to image search**: Find similar images

### Data Sources

- Cat faces dataset from HuggingFace
- Preprocessed cat datasets

### Technical Stack

- Flask for the image server
- React for the frontend
- RCLIP for CLIP model inference
- SQL for image embeddings storage

### Future Plans

- Faster inference with GPU acceleration
- Vector database for better performance
- More images and better scraping
- Cloud deployment with AWS Lambda

[Read the full blog post →](/post/cat_gallery/)