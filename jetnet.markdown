---
layout: page
title: JetNet
permalink: /jetnet/
---

# JetNet

[https://zenodo.org/record/4834876#.YRRECS1w3mE](Zenodo Link)

---
## Description

JetNet, derived from Ref. 1, consists of simulated jets with transverse momenta $$p_T$$ ≈ 1 TeV, originating from gluons, top quarks, and light quarks produced in 13 TeV proton-proton collisions in a simplified detector. Jets are limited to a maximum of 30 particles (selecting the highest $$p_T$$ particles). Jets with fewer than 30 particles are zero-padded up to 30; in addition there is an extra `mask` feature in the dataset which is set to 1 if the particle is real and 0 if the particle has been zero-padded. The other three particles features are the relative angular coordinates $$\eta^\mathrm{rel} = \eta^\mathrm{particle} - \eta^\mathrm{jet}$$ and $$\phi^\mathrm{rel} = \phi^\mathrm{particle} - \phi^\mathrm{jet} \pmod{2\pi}$$, and the relative transverse momentum $$p_T^\mathrm{rel} = p_T^\mathrm{particle}/p_T^\mathrm{jet}$$.

_____
## Format

The dataset has been published in a CSV format with `N * 30` rows, where `N` is the number of total jets in each class, and 4 columns representing the particle features in order: [$$\eta^\mathrm{rel}, \phi^\mathrm{rel}, p_T^\mathrm{rel}$$,  mask].

_____
## Published Results on JetNet

### Generation

<table>
    <thead>
        <tr>
            <th rowspan=2>Model</th>
            <th rowspan=2>Class</th>
            <th colspan=6>Metrics</th>
        </tr>
        <tr>
            <th>W1-M (\(10^{-3}\))</th>
            <th>W1-P (\(10^{-3}\))</th>
            <th>W1-EFP (\(10^{-5}\))</th>
            <th>FPND</th>
            <th>COV</th>
            <th>MMD</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=3 align="center">MPGAN [1]</td>
            <td>Gluons</td>
            <td align="center">1.8 ± 0.2</td>
            <td align="center">0.6 ± 0.2</td>
            <td align="center">0.9 ± 0.4</td>
            <td align="center">3.2</td>
            <td align="center">0.54</td>
            <td align="center">0.036</td>
        </tr>
        <tr>
            <td>Top quarks</td>
            <td align="center">2.1 ± 0.2</td>
            <td align="center">0.7 ± 0.1</td>
            <td align="center">1.8 ± 0.8</td>
            <td align="center">6.4</td>
            <td align="center">0.56</td>
            <td align="center">0.071</td>
        </tr>
        <tr>
            <td>Light quarks</td>
            <td align="center">2.1 ± 0.1</td>
            <td align="center">0.6 ± 0.1</td>
            <td align="center">0.9 ± 0.4</td>
            <td align="center">2.4</td>
            <td align="center">0.54</td>
            <td align="center">0.026</td>
        </tr>
    </tbody>
</table>

[1] Kansal et al., [arxiv:2106.11535](https://arxiv.org/abs/2106.11535), 2021

_____
## Tutorials and Notebooks

Coming soon...
