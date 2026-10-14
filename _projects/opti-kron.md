---
layout: page
title: Opti-KRON
permalink: /projects/opti-kron/
description: Optimal Kron-based reduction of power-system networks.
importance: 1
category: research
github: https://github.com/OmidMkht/Opti-KRON
---

## The problem

Many power-system studies, such as optimal power flow and voltage control, become slow on real distribution feeders, which can have thousands of nodes.
A smaller model that behaves like the original network makes these studies practical.
Opti-KRON builds that smaller model while keeping the voltage error under a limit the user chooses.

{% comment %}
Add a figure here once you have one, for example a feeder before and after reduction, colored by voltage error.

1. Save the image as assets/img/opti-kron-overview.png
2. Delete the "comment" and "endcomment" lines around this block, and these instruction lines.

{% include figure.liquid loading="eager" path="assets/img/opti-kron-overview.png" class="img-fluid rounded z-depth-1" zoomable=true %}
{% endcomment %}

## Kron reduction in one equation

The bus admittance matrix $$\mathbf{Y}$$ describes how every node in the network is electrically connected to every other node.
Split the nodes into a set we keep, $$\mathcal{K}$$, and a set we eliminate, $$\mathcal{E}$$.
Kron reduction gives an equivalent matrix that connects only the kept nodes:

$$
\mathbf{Y}_{\mathrm{red}} = \mathbf{Y}_{\mathcal{K}\mathcal{K}} - \mathbf{Y}_{\mathcal{K}\mathcal{E}} \, \mathbf{Y}_{\mathcal{E}\mathcal{E}}^{-1} \, \mathbf{Y}_{\mathcal{E}\mathcal{K}}
$$

Here $$\mathbf{Y}_{\mathcal{K}\mathcal{E}}$$ is the block of $$\mathbf{Y}$$ with rows for kept nodes and columns for eliminated nodes, and the other blocks are defined the same way.
The reduction is exact when the eliminated nodes carry no load.
Real eliminated nodes do carry load, so that load must be moved to kept nodes, and **which nodes we keep decides how much voltage error the reduced model has**.

## What Opti-KRON adds

Opti-KRON chooses which nodes to keep, and where to move their loads, by solving a mixed-integer optimization problem.
The optimization keeps the largest voltage-magnitude difference between the full and reduced networks below a set limit.
The methods also preserve the radial (tree-like) structure of distribution feeders, handle unbalanced three-phase feeders, and scale to large networks through decomposition and GPU acceleration.

## Results at a glance

Voltage errors are in per unit (p.u.), which means a fraction of the nominal voltage: 0.003 p.u. is 0.3%.

| Paper                | Test network                          | Nodes removed | Largest voltage error |
| :------------------- | :------------------------------------ | :------------ | :-------------------- |
| IEEE TPWRS, 2026     | 533-bus distribution system           | 85%           | below 0.0025 p.u.     |
| IEEE TPWRS, 2026     | 3,499-bus utility feeder              | over 94%      | below 0.002 p.u.      |
| EPSR (PSCC 2026)     | 5,991-node three-phase utility feeder | up to 90%     | below 0.003 p.u.      |
| EPSR (PSCC 2026)     | 8,381-node three-phase utility feeder | up to 80%     | below 0.003 p.u.      |
| arXiv preprint, 2024 | IEEE RTS-96 and Polish 2383-bus       | 80–95%        | DC power flow model   |

On a 1,000-node test case, the GPU version of the three-phase method runs up to 15× faster than the CPU version.

[View the code on GitHub](https://github.com/OmidMkht/Opti-KRON)

## Related publications

{% bibliography --query @*[title~=Kron] %}
