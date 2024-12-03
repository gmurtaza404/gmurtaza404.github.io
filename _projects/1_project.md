---
layout: page
title: scGrapHiC
description: Predicting pseudo-bulk scHi-C from scRNA-seq
img: assets/img/scgraphic.jpeg
importance: 1
category: work
related_publications: false
---

Single-cell Hi-C (scHi-C) protocol helps identify cell-type-specific chromatin interactions and sheds light on cell differentiation and disease progression. Despite providing crucial insights, scHi-C data is often underutilized due to the high cost and the complexity of the experimental protocol. We present a deep learning framework, scGrapHiC, that predicts pseudo-bulk scHi-C contact maps using pseudo-bulk scRNA-seq data. Specifically, scGrapHiC performs graph deconvolution to extract genome-wide single-cell interactions from a bulk Hi-C contact map using scRNA-seq as a guiding signal. Our evaluations show that scGrapHiC, trained on 7 cell-type co-assay datasets, outperforms typical sequence encoder approaches. For example, scGrapHiC achieves a substantial improvement of $23.2\%$ in recovering cell-type-specific Topologically Associating Domains over the baselines. It also generalizes to unseen embryo and brain tissue samples. scGrapHiC is a novel method to generate cell-type-specific scHi-C contact maps using widely available genomic signals that enables the study of cell-type-specific chromatin interactions.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/scgraphic.jpeg" title="scGrapHiC architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    scGrapHiC is a deep learning framework that extracts cell-type specific scHi-C from a bulk Hi-C contact map using scRNA-seq as a guide signal. scGrapHiC has four major components: The first component - Positional Encoding - extracts the positional encodings from the bulk Hi-C and concatenates them with our input node feature set that contains scRNA-seq, CTCF, and CpG scores. The second component - Node Feature Processor - maps this feature set into a joint representation space. The third component - Graph Encoder - produces a node latent set that represents the likelihood of contacts being extracted via deconvolution on the bulk Hi-C using the provided joint node feature set as a guide signal. The last component - Graph Decoder - maps these likelihoods to the scHi-C output space.
</div>
