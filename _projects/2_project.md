---
layout: page
title: Hi-Cy
description: Benchmarking Hi-C resolution improvement frameworks
img: assets/img/graphic.png
importance: 3
category: Brown University
related_publications: false
---

Hi-C experiments allow researchers to study and understand the 3D genome organization and its regulatory function. Unfortunately, sequencing costs and technical constraints severely restrict access to high-quality Hi-C data for many cell types. Existing frameworks rely on a sparse Hi-C dataset or cheaper-to-acquire ChIP-seq data to predict Hi-C contact maps with high read coverage. However, these methods fail to generalize to sparse or cross-cell-type inputs because they do not account for the contributions of epigenomic features or the impact of the structural neighborhood in predicting Hi-C reads. We propose GrapHiC, which combines Hi-C and ChIP-seq in a graph representation, allowing more accurate embedding of structural and epigenomic features. Each node represents a binned genomic region, and we assign edge weights using the observed Hi-C reads. Additionally, we embed ChIP-seq and relative positional information as node attributes, allowing our representation to capture structural neighborhoods and the contributions of proteins and their modifications for predicting Hi-C reads. We show that GrapHiC generalizes better than the current state-of-the-art on cross-cell-type settings and sparse Hi-C inputs. Moreover, we can utilize our framework to impute Hi-C reads even when no Hi-C contact map is available, thus making high-quality Hi-C data accessible for many cell types.

The code is available at: https://github.com/rsinghlab/GrapHiC

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/graphic.png" title="GrapHiC architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Inputs and pre-processing pipeline:  In this portion of the pipeline, we normalize Hi-C contact maps and create a Hi-C graph using Hi-C data as its edges and genomic loci as the nodes, with auxiliary genomic signals and positional encodings as node attributes. GrapHiC: we use the sparse input Hi-C graph to generate a denser Hi-C graph. The Graph encoder takes in the Hi-C graph and generates latent node representations that our graph decoder utilizes to impute a dense Hi-C contact matrix.
</div>
