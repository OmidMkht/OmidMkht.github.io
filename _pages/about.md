---
layout: about
title: about
permalink: /
subtitle: Ph.D. student in Electrical Engineering · University of Vermont

profile:
  align: right
  image: omid.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>Burlington, Vermont</p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

I am a Ph.D. student in Electrical Engineering at the [University of Vermont](https://www.uvm.edu/cems/ebe), advised by [Mads R. Almassalkhi](https://madsalma.github.io/) and [Samuel Chevalier](https://samchevalier.github.io/).
I expect to complete my Ph.D. in Fall 2027 and am looking for postdoctoral positions.

[Email](mailto:omid.mokhtari@uvm.edu) · [CV]({{ '/cv/' | relative_url }}) · [Google Scholar](https://scholar.google.com/citations?user=Y0yF4dMAAAAJ) · [ORCID](https://orcid.org/0009-0001-6204-1612) · [GitHub](https://github.com/OmidMkht) · [LinkedIn](https://www.linkedin.com/in/omidmokhtari)

## Research

My Ph.D. research focuses on optimal network reduction for power systems, building on **mathematical optimization** and **graph theory**. It has three parts.

**Network reduction for distribution systems.**
I develop [Opti-KRON](https://github.com/OmidMkht/Opti-KRON), which formulates Kron-based reduction of distribution feeders as a mixed-integer optimization problem.
It produces structure-preserving (radial) reduced models of radial networks, extends to unbalanced three-phase feeders, and runs on GPUs for large systems.

**Network reduction for transmission systems.**
For large meshed transmission networks, I partition the network graph into communities with community detection and reduce each community in parallel.

**Sensor placement.**
I use optimal network reduction to place a limited budget of sensors in radial (tree-structured) distribution networks, supporting data-driven power flow and voltage estimation with sparse real-time measurements.

<div class="row mt-3">
  <div class="col-sm-6 mt-3 mt-sm-0">
    {% include video.liquid path="assets/video/opti-kron-full-to-radial.mp4" class="img-fluid rounded z-depth-1" autoplay=true loop=true muted=true controls=true %}
  </div>
  <div class="col-sm-6 mt-3 mt-sm-0">
    {% include figure.liquid loading="lazy" path="assets/img/opti-kron-layers.png" class="img-fluid rounded z-depth-1" zoomable=true cache_bust=true alt="Opti-KRON: full, reduced, and radialized network layers" %}
  </div>
</div>
<div class="caption">
  Opti-KRON on a radial feeder. Left: animation of the full network, its optimal Kron-based reduction, and radialization of the reduced model. Right: the same three stages as layers.
</div>

During my M.Sc. at Sharif University of Technology, I worked on the co-planning of merchant energy storage systems and transmission systems.

## A little more about me

I received my B.Sc. in Electrical Engineering (power systems) from Imam Khomeini International University in Qazvin, Iran.

I serve as a reviewer for _IEEE Transactions on Power Systems_, _Electric Power Systems Research_, and the American Control Conference (ACC).

<!-- Add later when ready: teaching or TA experience, awards and fellowships, and one line on hobbies. -->
