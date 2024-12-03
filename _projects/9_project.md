---
layout: page
title: GDPR compliance with Service Meshes
description: Service meshes make it easier to enforce GDPR compliance
img: assets/img/service_mesh_gdpr.png
importance: 9
category: work
related_publications: false
---

Through a swift migration that took place in early 2000s, many companies moved their data and services to clouds. This rapid adoption allowed little opportunity for the researchers
to study the downsides of such massive shift in terms of privacy. Therefore, soon after the change, companies started to suffer detrimental data breaches. As a response, the European Union passed some regulations (e.g., GDPR) to mandate privacy requirements on companies handling data related to EU citizens. As a result, the companies started to abide with the rules by changing their widely deployed systems. Such a change is still on progress and requires massive engineering efforts because of the design issues inherent within the old systems. Another shift that we are witnessing is a widespread adoption of Service Meshes. In this project, we argue that using the standard tools that a service mesh manager such as Istio provides, it is possible to satisfy at least some of the most important rules mandated by GDPR.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/service_mesh_gdpr.png" title="overhead" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Effect of imposing 2000 GDPR compliance rules on end-to-end latency.
</div>
