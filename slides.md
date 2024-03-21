---
title: WMI.II-CVaPR-S #1
---

# Visual Segmentation

Multimodal LLM techniques for
AI-augmented Computer Vision and
prompt engineering.
  
### 

### 

Marcin Dąbrowski

2024-03-21

---

## Introduction

With the advent of large language models (LLMs) and their application to visual-based tasks arose a need for "tokenization", or segmentation of visual input objects that could be better bound to LLMs.

Conversely, segmentation could also be useful within classical computer vision (CV) pipelines.
<!-- .element: class="fragment" -->

---

## Part I:
### prior approaches to multimodal encoding

---

### Naver ViLT (5 February 2021)

<sup>Vision-and-Language Transformer</sup>

<img preload="auto" width="60%" height="60%" src="https://www.aizhongguo.xyz/posts/evolution-of-multimodality/images/ViLT-model-view.png" style="background-color:#fad6a5" />

<sup>Single-encoder image-text matching with masking</sup>

---

### Google ALIGN (11 February 2021)

<sup>A Large-scale ImaGe and Noisy-text embedding</sup>

<img preload="auto" width="60%" height="60%" src="https://www.aizhongguo.xyz/posts/evolution-of-multimodality/images/ALIGN_exp.png" style="background-color:#fad6a5" />

<sup>Dual encoder to align representations with contrastive loss</sup>

---

### ClosedAI CLIP (26 February 2021)

<sup>Contrastive Language-Image Pre-Training</sup>

<img preload="auto" width="60%" height="60%" src="https://www.aizhongguo.xyz/posts/evolution-of-multimodality/images/clip_illustrate.png" style="background-color:#fad6a5" />

<sup>Contrastive Representation Learning (CRL)</br>over relationships modeling</sup>

---

### Salesforce ALBEF (16 July 2021)

<sup>Align Before Fuse</sup>

<img preload="auto" width="60%" height="60%" src="https://www.aizhongguo.xyz/posts/evolution-of-multimodality/images/ALBEF-exp.png" style="background-color:#fad6a5" />

<sup>contrastive loss alignment before inclusion</br>into multimodal encoder</sup>

---

### Microsoft VLMo (3 November 2021)

<sup>Vision-Language Pretrained Model</sup>

<img preload="auto" width="50%" height="50%" src="https://www.aizhongguo.xyz/posts/evolution-of-multimodality/images/VLMO-exp.png" style="background-color:#fad6a5" />

<sup>combined learning of specialized encoders with transformer</sup>

---

### Salesforce BLIP (28 January 2022)

<sup>Bootstrapping Language-Image Pre-training</sup>

<img preload="auto" width="60%" height="60%" src="https://www.aizhongguo.xyz/posts/evolution-of-multimodality/images/BLIP-exp2.png" style="background-color:#fad6a5" />

<sup>mixed encoder-decoder with captioning and filtering</sup>

---

### 金山 Monkey (11 November 2022)

<img preload="auto" width="60%" height="60%" src="https://www.aizhongguo.xyz/posts/evolution-of-multimodality/images/Monkey-exp1.png" style="background-color:#fad6a5" />

<sup>sliding window approach to visual encoding</sup>

---

### Facebook SAM (5 Apr 2023)

<sup>SegmentAnything Model</sup>

<img preload="auto" width="60%" src="https://viso.ai/wp-content/uploads/2023/12/architecture-segment-anything-model-sam-1060x226.jpg" style="background-color:#fad6a5" />

<sup>image encoder — prompt encoder — mask decoder chain</sup>

III

### Part II: current top contender:

## Facebook Segment Anything

---
### What is Segment Anything

* SA model: promptable, zero-shot masking model

* SA-1B dataset: 1M 8K resolution images, 1.1B segmentation masks
<!-- .element: class="fragment" -->

* SA Task: prompt to segmentation taskset
<!-- .element: class="fragment" -->

* SA Data Engine: model-automated masks collector
<!-- .element: class="fragment" -->

---

### What can it do?
<video data-autoplay preload="auto" muted loop height="50%" width="50%" src="https://segment-anything.com/assets/section-1.1a.mp4"></video>

selectively mask elements of the input image

III

### What can it do?
<video data-autoplay preload="auto" muted loop height="50%" width="50%" src="https://segment-anything.com/assets/section-1.1b.mp4"></video>

segment every element of the input image

III

### What can it do?
<video data-autoplay preload="auto" muted loop height="50%" width="50%" src="https://segment-anything.com/assets/section-1.1c.mp4"></video>

generate multiple masks for the given input image

III

### What can it do?
<video data-autoplay preload="auto" muted loop height="50%" width="50%" src="https://segment-anything.com/assets/section-1.2a.mp4"></video>

pointer-based segment selection

III

### What can it do?
<video data-autoplay preload="auto" muted loop height="50%" width="50%" src="https://segment-anything.com/assets/section-1.2b.mp4"></video>

prompt-originated bounding box generation

---

### Aims of Segment Anything

* Toolset for and of foundation models
<!-- .element: class="fragment" -->
* Components for tighter integration of CV and ML
<!-- .element: class="fragment" -->
* яєѕρσηѕιвℓє αятιƒι¢ιαℓ ιηтєℓℓιgєη¢є
<!-- .element: class="fragment" -->

---

<sup><sub>Questions?</sub></sup>

---

Sources (in order of appearance):

Arxiv: 2102.03334, Arxiv: 2102.05918,</br>Arxiv: 2103.00020, Arxiv: 2107.07651,</br>Arxiv: 2111.02358, Arxiv: 2201.12086,</br>Arxiv: 2311.06607, segment-anything.com

<!-- dev run: reveal-md slides.md  --watch --theme moon --disable-auto-open -->