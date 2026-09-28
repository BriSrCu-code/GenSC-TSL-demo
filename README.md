# GenSC-TSL Demo

This repository provides a qualitative demo of **GenSC-TSL**, a target-speaker localization framework for distributed microphone arrays.

Given a multi-speaker recording and an enrollment utterance specifying the target speaker, GenSC-TSL generates target-selective pairwise delay responses and fuses them through a geometry-based GCF decoder to estimate the target trajectory.

## Demo

The following demo shows GenSC-TSL tracking an enrolled moving speaker in a multi-speaker scene. The visualization jointly presents the target activity, GCF localization map, target/non-target trajectories, pairwise localization errors, and frame-wise 2-D position error.

https://github.com/BriSrCu-code/GenSC-TSL-demo/blob/97aafe88033ad36eb2ac70f96302550acb8f655d/demo/demo1.mp4

The visualization includes:

- **Target VAD**: activity of the enrolled target speaker.
- **GCF spatial map**: localization evidence obtained by fusing the predicted pairwise GCC-PHAT-like responses.
- **2-D trajectories**: ground-truth target and non-target trajectories together with the predicted target trajectory.
- **Coordinate trajectories**: predicted and ground-truth \(x\)- and \(y\)-coordinates over time.
- **Pairwise DOA errors**: localization errors associated with individual microphone pairs.
- **2-D localization error**: frame-wise position error of the predicted target trajectory.

The demo illustrates that GenSC-TSL can continuously follow the enrolled speaker while suppressing competing spatial evidence from the non-target speaker.

## Paper

**GenSC-TSL: Selective Target-Speaker Localization via Generative Spatial Correlation for Distributed Microphone Arrays**

Paper: *Coming soon.*
