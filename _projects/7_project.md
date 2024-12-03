---
layout: page
title: Ark data analysis
description: Measuring internet path length fluctuations
img: assets/img/memory-pressure.png
importance: 7
category: LUMS
related_publications: false
---

I analyzed terabytes of traceroute data from the CAIDA Archipelago (Ark) Measurement Infrastructure to quantify the instability in the internet routes. The analysis was conducted to inform critical design decisions in the Tracerouter project which aimed to identify IPs that geo locked internet content. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/path_length_fluctuations.png" title="memory utilization" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The CDF shows that almost 70% of the paths show zero path length fluctuation across a 10 year window with almost 95% of paths show fluctuation of less than three.
</div>
