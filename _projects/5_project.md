---
layout: page
title: MissIt
description: Low bit rate network stack
img: assets/img/missit.png
importance: 5
category: LUMS
related_publications: false
---

Mobile devices have become the primary mode for Internet access in developing countries. Yet typical data plans and SMS costs can be overwhelming for low income users in these countries. In this paper, we explore the design and usability of a free but extremely low bit rate communication channel to address this challenge. We propose, a data communication channel that uses to transmit messages between phones, thereby sacrificing performance in exchange for low cost. While the data rate of is extremely low (<1 bps), our prototype implementation and small scale user studies explore the feasibility of this idea for different types of messaging scenarios. Our results show that could be a viable option for messaging scenarios that require short, pre-determined responses (e.g., survey questions) while for traditional SMS-style messaging, a suitable user interface and other customizations are likely required to make it a viable option for users.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/missit.png" title="MissIt Network Stack" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Timing diagram illustrating the delays involved in the MissIt network stack for data communication.
</div>
