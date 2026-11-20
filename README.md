# GenSC-TSL Demo

This repository provides a qualitative demo of **GenSC-TSL**, a target-speaker localization framework for distributed microphone arrays.

Given a multichannel multi-speaker recording and an enrollment utterance specifying the target speaker, GenSC-TSL generates target-selective pairwise delay responses and fuses them through a GCF decoder using the known microphone geometry to estimate the target trajectory.

## Demo

The demo compares **GenSC-TSL-fixed**, **IPDnet2-TC**, and **SRP-DNN-TC** on the same moving-speaker scene. Each spatial panel shows the method-specific response together with the ground-truth target and non-target trajectories and the estimated target trajectory.

GCF decoding uses three-dimensional geometry. In this simulated scene, microphones and speakers share a common height, and candidate positions are restricted to that horizontal plane. The spatial maps and trajectories are displayed on this plane.

https://github.com/user-attachments/assets/ddfde406-72e4-4736-ab2e-3b5be83708ef

The three spatial panels show, from left to right:

| Method | Displayed spatial response |
| --- | --- |
| **GenSC-TSL-fixed** | GCF map obtained by fusing target-selective pairwise GCC-PHAT-like responses |
| **IPDnet2-TC** | IPD score map |
| **SRP-DNN-TC** | SRP spatial spectrum |

The visualization also includes:

- **Target VAD**: activity of the enrolled target speaker.
- **Coordinate trajectories**: predicted and ground-truth x- and y-coordinates over time.
- **Pairwise DOA errors**: signed angular errors derived from each microphone pair's predicted and ground-truth delay-response peaks.
- **Horizontal position error**: frame-wise Euclidean distance between the predicted and ground-truth target positions on the displayed plane.

The coordinate and error plots correspond to **GenSC-TSL-fixed**. Target-active predictions are shown in red, and target-inactive predictions in dashed gray.

The demo illustrates how GenSC-TSL maintains target association and trajectory continuity while suppressing competing spatial responses from the non-target speaker.

## Paper

**GenSC-TSL: Selective Target-Speaker Localization via Generative Spatial Correlation for Distributed Microphone Arrays**

Paper: *Coming soon.*



