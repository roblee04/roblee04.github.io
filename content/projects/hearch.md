---
title: "Hearch - Serendipity-Focused Search Engine"
date: 2024-11-15
draft: false
featured: true
weight: 105
thumbnail: "/thumbnails/maple.png"
description: "A research search engine designed to combat commercial bloat and filter bubbles through anti-SEO heuristics and cross-lingual retrieval."
technologies: ["Python", "NLP", "LLM", "Information Retrieval", "BM25", "Translation"]
paper: "/files/hearch.pdf"
status: "Completed"
---

## Hearch - A Serendipity-Focused Search Engine

**Authors:** Robin Lee, Harsh Rao

### The Problem: "Economics of Search"

The original goal of search engines—to optimize for informational relevance—has been compromised by:

- **Aggressive SEO:** High-profit motives lead to results dominated by commercial entities.

- **Homogenized Results:** Search landscapes are increasingly characterized by a lack of variety and "commercial bloat".

- **Obscured "Small Web":** Independent and human-authored content is often buried under high-utility but low-serendipity sources.

### Creative Solutions

To combat these issues and bring back "serendipity" to searching, Hearch utilizes several innovative methods:

#### 1. Anti-SEO Heuristics

The engine uses a hybrid ranking algorithm. It combines the standard BM25 probabilistic function with unique "Anti-SEO" penalties derived from a page's Document Object Model (DOM) to prioritize structural integrity over commercial optimization.

#### 2. Generative Query Expansion

Leverages Large Language Models (LLMs) to expand user queries, helping to find relevant information even when exact keywords aren't used.

#### 3. Cross-Lingual Retrieval

To break through the "Anglophone filter bubble," the engine is designed to retrieve and translate relevant content from multiple languages.

#### 4. Focus on Serendipity

Rather than just engagement or popularity, Hearch prioritizes finding high-quality, diverse, and surprising information that traditional engines might ignore.

### Project Report

<div style="margin: 2rem 0; padding: 1rem; background: #f5f5f5; border-radius: 8px;">
  <object data="/files/hearch.pdf" type="application/pdf" width="100%" height="600px">
    <p>Unable to display PDF file. <a href="/files/hearch.pdf">Download instead</a>.</p>
  </object>
</div>

[Download PDF →](/files/hearch.pdf)

### Conclusion

Hearch represents an exploration into alternative search paradigms that prioritize information diversity and serendipity over commercial interests. By combining anti-SEO techniques with modern NLP capabilities, we demonstrate that more equitable information retrieval is possible.