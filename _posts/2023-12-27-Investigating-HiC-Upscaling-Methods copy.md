---
layout: slide
title: A Comprehensive Evaluation of Generalizability of Deep Learning-Based Hi-C Resolution Improvement Methods
excerpt: Genes
# theme: simple
transition: convex
tags: [presentation]
category: presentation
---
<section data-markdown>
  <textarea data-template>

    Hi-C is a widely used technique to study the 3D organization of the genome. Due to its high sequencing cost, most of the generated datasets are of a coarse resolution, which makes it impractical to study finer chromatin features such as Topologically Associating Domains (TADs) and chromatin loops. Multiple deep learning-based methods have recently been proposed to increase the resolution of these datasets by imputing Hi-C reads (typically called upscaling). However, the existing works evaluate these methods on either synthetically downsampled datasets, or a small subset of experimentally generated sparse Hi-C datasets, making it hard to establish their generalizability in the real-world use case. We present our framework—Hi-CY—that compares existing Hi-C resolution upscaling methods on seven experimentally generated low-resolution Hi-C datasets belonging to various levels of read sparsities originating from three cell lines on a comprehensive set of evaluation metrics. Hi-CY also includes four downstream analysis tasks, such as TAD and chromatin loops recall, to provide a thorough report on the generalizability of these methods. We observe that existing deep learning methods fail to generalize to experimentally generated sparse Hi-C datasets, showing a performance reduction of up to 57%. As a potential solution, we find that retraining deep learning-based methods with experimentally generated Hi-C datasets improves performance by up to 31%. More importantly, Hi-CY shows that even with retraining, the existing deep learning-based methods struggle to recover biological features such as chromatin loops and TADs when provided with sparse Hi-C datasets. Our study, through the Hi-CY framework, highlights the need for rigorous evaluation in the future. We identify specific avenues for improvements in the current deep learning-based Hi-C upscaling methods, including but not limited to using experimentally generated datasets for training.

    [Full Paper](https://doi.org/10.3390/genes15010054)
  </textarea>
</section>
