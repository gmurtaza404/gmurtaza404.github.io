---
layout: page
title: WebOptProfiler
description: Causal model for web page loading process
img: assets/img/weboptprofiler.png
importance: 4
category: work
related_publications: false
---

Despite decades of research on mobile webpage optimizations, little is known about how these optimizations interoperate. Moreover, there has been little systematic work to understand the scenarios wherein combinations of these optimizations excel. Without a comprehensive understanding of how these optimizations compose with each other and under what conditions they excel, operators cannot determine which optimizations to adopt, and, similarly, developers do not know where to focus their efforts.
In this paper, we argue that developers should be required to evaluate and characterize the broader interactions between their proposed optimizations and other optimizations - this is in addition to demonstrating the potential benefits of their approach. To aide developers in characterizing these broader interactions, we propose an analytical model which decomposes web optimizations into virtual speedup functions that operate on well-understood browser processing phases (e.g., processing, rendering, layout, etc., for an object) and we present a web browser-oriented causal profiler which empirically explores interactions between optimizations by using their analytical models to speed up different parts of the Browser during a page load. Our system, WebOptProfiler, identifies and addresses practical issues in extending causal profiling to the webpage optimization domain and provides an algorithm for extracting an analytical model from readily available browser traces.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/weboptprofiler.png" title="WebOptProfiler workflow" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    WebOptProfiler Architecture.
</div>
