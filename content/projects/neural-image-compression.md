---
title: "Neural Image Compression with Text-Guided Encoding"
date: 2024-12-01
draft: false
featured: true
weight: 110
thumbnail: "https://img.youtube.com/vi/YxncWJhUSRs/maxresdefault.jpg"
description: "Enhancing neural image compression by incorporating text captions to improve compression results using deep learning approaches like variational autoencoders."
technologies: ["Python", "Deep Learning", "VAE", "PyTorch", "Computer Vision", "NLP"]
demo: "https://www.youtube.com/watch?v=YxncWJhUSRs"
status: "Completed"
---

## Enhancing Neural Image Compression with Text-Guided Encoding

**Author:** Robin Lee

### Introduction

In the modern digital era, the demand for efficient visual data storage and transmission is critical. While traditional methods like JPEG and PNG are widely used, they often struggle to balance high compression rates with image quality. This has led to the development of deep learning approaches, such as variational autoencoders (VAEs), to optimize image compression. A recent discovery in this field is that incorporating text captions can significantly improve compression results by allowing complex information to be stored in a very small number of bits.

### The TACO Framework

The project is built upon the Text Adaptive Compression (TACO) model, which uses the ELIC (Efficient Learned Image Compression) encoder-decoder as its backbone. TACO uniquely utilizes text captions only during the encoding phase. By doing so, the model is forced to learn high-level information from the text without using it for pixel reconstruction, which reduces unwanted artifacts while preserving fine details and textures.

### Identified Challenges and Proposed Improvements

The research aimed to address several limitations of the original TACO architecture through three independent ablation studies:

1. **Contextual Information Scarcity:** Original captions were short (approx. 15 words), which often failed to fully describe the scene for high-quality reconstruction.

2. **Quadratic Complexity:** The cross-attention mechanism used for text injection has an O(n²) complexity, creating a computational bottleneck as sequence lengths increase.

3. **Embedding Limitations:** Standard CLIP embeddings often treat all tokens with uniform importance, potentially missing critical semantic details.

### Methodology

The study implemented three distinct architectural and data-driven enhancements:

1. **Increased Contextual Information:** Generated new, detailed captions using GPT-4o for the MS-COCO, CLIC, and Kodak datasets. These captions provided deeper reasoning about scenes to create a more information-packed latent representation.

2. **Linear Attention Mechanism:** Replaced standard O(n²) attention with the Linformer mechanism. This promises O(n) linear complexity scaling, maintaining performance while significantly improving efficiency for longer text inputs.

3. **Enhanced Word Encoding:** Integrated TF-IDF weighting and Named Entity Recognition (NER) via spaCy. This approach assigns higher weights (up to 1.5x) to significant tokens like "Eiffel Tower" or "Golden Retriever," ensuring salient features contribute more to the final image representation.

### Experimental Results

The models were trained using the MS-COCO 2014 training split (82,783 images) and evaluated on MS-COCO, CLIC, and Kodak datasets.

- **Increased Context:** Outperformed the TACO baseline in LPIPS (perceptual similarity) and PSNR (pixel fidelity) across various datasets. The reasoning-based captions captured higher levels of detail, leading to more accurate reconstructions.

- **Efficiency:** The implementation of linear attention addressed the quadratic bottleneck, making the model more scalable for future use with longer text sequences.

- **Consistency:** All augmentations maintained competitive FID scores, ensuring that general realism was preserved without introducing new blurriness or artifacts.

### Demo

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; margin: 1.5rem 0;">
  <iframe 
    src="https://www.youtube.com/embed/YxncWJhUSRs" 
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
    allowfullscreen>
  </iframe>
</div>

[Watch on YouTube →](https://www.youtube.com/watch?v=YxncWJhUSRs)

### Conclusion

By augmenting the TACO architecture with richer contextual data, efficient attention mechanisms, and intelligent word weighting, this research demonstrated that text-guided encoding can be pushed further for higher fidelity image compression. These improvements suggest that the future of neural compression lies not just in better pixel-processing, but in the intelligent integration of multimodal contextual data.