---
layout: about
title: About
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

[Email](mailto:omid.mokhtari@uvm.edu) · [CV]({{ '/cv/' | relative_url }}) · [Google Scholar](https://scholar.google.com/citations?user=Y0yF4dMAAAAJ) · [GitHub](https://github.com/OmidMkht) · [LinkedIn](https://www.linkedin.com/in/omidmokhtari)

## Research

My research lies at the intersection of **power system operation and planning**, **mathematical optimization**, and **graph theory**.
My Ph.D. work focuses on optimal network reduction for power systems, in three parts.

**Network reduction for distribution systems.**
I develop [Opti-KRON](https://github.com/OmidMkht/Opti-KRON), which formulates Kron-based reduction of distribution feeders as a mixed-integer optimization problem and produces structure-preserving (radial) reduced models of radial networks.
I extended Opti-KRON to unbalanced three-phase distribution networks and developed a GPU-based search algorithm to improve scalability.

**Network reduction for transmission systems.**
I am currently working on transmission network reduction to accelerate DC optimal power flow and capacity expansion problems.
The main challenge is to aggregate buses and lines while accounting for transmission constraints, particularly line-flow limits, so that the reduced model does not allow infeasible operating points.

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
  Opti-KRON: full, reduced, and radialized network.
</div>

## Education

- **Ph.D.** in Electrical Engineering, University of Vermont (expected Fall 2027)
- **M.Sc.** in Electrical Engineering (Power Systems), Sharif University of Technology, Tehran, Iran
- **B.Sc.** in Electrical Engineering (Power Systems), Imam Khomeini International University, Qazvin, Iran

<!-- Add later when ready: teaching or TA experience, awards and fellowships, and one line on hobbies. -->
