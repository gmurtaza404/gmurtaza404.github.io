---
layout: page
title: GrapHiC
description: Predicting high quality bulk Hi-C contact maps from sparse Hi-C contact maps
img: assets/img/graphic.png
importance: 2
category: Brown University
related_publications: false
---

Hi-C is a widely used technique to study the 3D organization of the genome. Due to its high sequencing cost, most of the generated datasets are of a coarse resolution, which makes it impractical to study finer chromatin features such as Topologically Associating Domains (TADs) and chromatin loops. Multiple deep learning-based methods have recently been proposed to increase the resolution of these datasets by imputing Hi-C reads (typically called upscaling). However, the existing works evaluate these methods on either synthetically downsampled datasets, or a small subset of experimentally generated sparse Hi-C datasets, making it hard to establish their generalizability in the real-world use case. We present our framework—Hi-CY—that compares existing Hi-C resolution upscaling methods on seven experimentally generated low-resolution Hi-C datasets belonging to various levels of read sparsities originating from three cell lines on a comprehensive set of evaluation metrics. Hi-CY also includes four downstream analysis tasks, such as TAD and chromatin loops recall, to provide a thorough report on the generalizability of these methods. We observe that existing deep learning methods fail to generalize to experimentally generated sparse Hi-C datasets, showing a performance reduction of up to 57%. As a potential solution, we find that retraining deep learning-based methods with experimentally generated Hi-C datasets improves performance by up to 31%. More importantly, Hi-CY shows that even with retraining, the existing deep learning-based methods struggle to recover biological features such as chromatin loops and TADs when provided with sparse Hi-C datasets. Our study, through the Hi-CY framework, highlights the need for rigorous evaluation in the future. We identify specific avenues for improvements in the current deep learning-based Hi-C upscaling methods, including but not limited to using experimentally generated datasets for training.

The code is available at: https://github.com/rsinghlab/Hi-CY

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/hicy.png" title="Hi-Cy workflow" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Overview of our benchmarking framework Hi-CY: (A) Data pre-processing pipeline. We (1) filtered the Hi-C matrices with the same MAPQ value (≥30), (2) normalized them with the same KR normalization algorithm to ensure a fair comparison, (3) removed inter-chromosomal contacts because of their extremely sparse nature, (4) performed a 0–1 normalization on the intra-chromosomal matrices to reduce the impact of extreme values; and (5) cropped appropriately sized sub-matrices to ensure that the input is in the correct format for each upscaling algorithm. (B) We upscaled the sub-matrices using a wide variety of deep learning-based upscaling models (and Gaussian Smoothing) and then recombined them to form upscaled intra-chromosomal Hi-C matrices. (C) We combined multiple Hi-C similarity metrics, correlation-based metrics and downstream analyses, like chromatin loops and TAD recovery analysis, to provide a comprehensive report that we can use to analyze the performance of each upscaling model.
</div>
