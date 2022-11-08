---
layout: slide
title: Investigating the performance of deep learning methods for Hi-C resolution improvement
excerpt: bioRxiv.org
# theme: simple
transition: convex
tags: [presentation]
category: presentation
---
<section data-markdown>
  <textarea data-template>

    Motivation HiC is a widely used technique to study the 3D organization of the genome. Due to its high sequencing cost, most of the generated datasets are of coarse quality, consequently limiting the quality of the downstream analyses. Recently, multiple deep learning-based methods have been proposed to improve the quality of these data sets by increasing their resolution through upscaling. However, the existing works do not thoroughly evaluate these methods using HiC reproducibility metrics across different HiC experiments to establish their applicability in real-world scenarios. This study extensively compares deep learning-based HiC upscaling methods on real-world, low-quality HiC datasets. We evaluate these models using HiC reproducibility metrics on data from three cell lines – GM12878 (lymphoblastoid), K562 (human erythroleukemic), and IMR90 (lung fibroblast) – obtained from different HiC experiments.

    Results We show that the deep-learning techniques evaluated in this study, trained on downsampled data, cannot upscale real-world, low-quality HiC matrices effectively. More importantly, we also show that retraining these methods on examples of real-world data improves their performance and similarity on target experimental data sets. However, even with retraining, our downstream analyses on the output of these methods suggest that these methods fail to capture the biological signals in the real-world inputs with high sparsity. Therefore, our study highlights the need for rigorous evaluation and identifies specific areas that need improvement concerning current deep learning-based HiC upscaling methods.Motivation HiC is a widely used technique to study the 3D organization of the genome. Due to its high sequencing cost, most of the generated datasets are of coarse quality, consequently limiting the quality of the downstream analyses. Recently, multiple deep learning-based methods have been proposed to improve the quality of these data sets by increasing their resolution through upscaling. However, the existing works do not thoroughly evaluate these methods using HiC reproducibility metrics across different HiC experiments to establish their applicability in real-world scenarios. This study extensively compares deep learning-based HiC upscaling methods on real-world, low-quality HiC datasets. We evaluate these models using HiC reproducibility metrics on data from three cell lines – GM12878 (lymphoblastoid), K562 (human erythroleukemic), and IMR90 (lung fibroblast) – obtained from different HiC experiments. Results We show that the deep-learning techniques evaluated in this study, trained on downsampled data, cannot upscale real-world, low-quality HiC matrices effectively. More importantly, we also show that retraining these methods on examples of real-world data improves their performance and similarity on target experimental data sets. However, even with retraining, our downstream analyses on the output of these methods suggest that these methods fail to capture the biological signals in the real-world inputs with high sparsity. Therefore, our study highlights the need for rigorous evaluation and identifies specific areas that need improvement concerning current deep learning-based HiC upscaling methods.

    [Full Paper](https://www.biorxiv.org/content/10.1101/2022.01.27.477975v1)
  </textarea>
</section>
