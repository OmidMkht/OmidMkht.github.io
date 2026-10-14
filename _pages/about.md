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

I am a Ph.D. student in Electrical Engineering at the [University of Vermont](https://www.uvm.edu/cems/ebe), advised by Mads R. Almassalkhi and [Samuel Chevalier](https://samchevalier.github.io/).
I expect to complete my Ph.D. in Fall 2027 and am looking for postdoctoral positions.

My research makes large power-grid models small enough to compute with, without losing the accuracy engineers need.
Real distribution feeders can have thousands of nodes, which makes many optimization and control problems slow or impractical to solve.
I develop optimization methods that shrink these network models while keeping a guaranteed bound on voltage error.
For example, on real utility feeders with 3,499 to 8,381 nodes, my methods remove 80–94% of the nodes while keeping the voltage error below 0.3% of nominal voltage.

[Email](mailto:omid.mokhtari@uvm.edu) · [CV]({{ '/cv/' | relative_url }}) · [Google Scholar](https://scholar.google.com/citations?user=Y0yF4dMAAAAJ) · [GitHub](https://github.com/OmidMkht) · [LinkedIn](https://www.linkedin.com/in/omidmokhtari)

## Research

**Optimal network reduction.**
[Opti-KRON]({{ '/projects/opti-kron/' | relative_url }}) uses optimization to decide which nodes of a power network to merge, so the smaller model still reproduces the original voltages.
I have developed versions for radial distribution networks and for unbalanced three-phase feeders.

**Scalable computation.**
To handle networks with thousands of nodes, I split them into communities that are reduced in parallel, and I run the reduction on GPUs (up to 15× faster than on CPUs in our tests).

**Estimation with few sensors.**
With collaborators, I study data-driven power flow and sensor placement, which estimate grid voltages with errors below 0.1% when only about a quarter of locations have sensors.

## A little more about me

Before coming to Vermont, I earned an M.Sc. in Electrical Engineering (power systems) at Sharif University of Technology, where I worked on co-planning merchant energy storage with transmission systems.
I received my B.Sc. in Electrical Engineering from Imam Khomeini International University in Qazvin, Iran.

I serve as a reviewer for _IEEE Transactions on Power Systems_, _Electric Power Systems Research_, and the American Control Conference (ACC).

<!-- Add later when ready: teaching or TA experience, awards and fellowships, and one line on hobbies. -->
