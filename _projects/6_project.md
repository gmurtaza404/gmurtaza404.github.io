---
layout: page
title: MissIt
description: Measuring the effect of high memory utilization on QoE in low-end mobile devices
img: assets/img/memory-pressure.png
importance: 6
category: work
related_publications: false
---

Mobile devices have become the primary mode of Internet access. Yet, differences in mobile hardware resources, such as device memory, coupled with the rising complexity of Web pages can lead to widely different quality of experience for users. In this work, we analyze how device memory usage affects Web browsing performance. We quantify the memory footprint of popular Web pages over different mobile devices, mobile browsers, and Android versions, analyze the induced memory distribution across different browser components (e.g., JavaScript engine and compositor), investigate how performance gets impacted under memory pressure and propose optimizations to reduce the memory footprint of Web browsing. We show that these optimizations can improve performance and reduce chances of browser crashes in low memory scenarios.

The full manuscript is available at: https://www.andrew.cmu.edu/user/theophib/papers/CCR20.pdf

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/memory-pressure.png" title="memory utilization" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Memory consumed by the Browser, Renderer, and GPU processes for Alexa top 100 Websites (sorted by memory consumed – left to right)
</div>
