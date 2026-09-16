# EnvPrior-BEVFusion

Environment semantic prior enhanced camera-LiDAR BEVFusion for 3D object detection on the nuScenes benchmark.

## Overview

EnvPrior-BEVFusion augments a BEVFusion-style camera-LiDAR detector with offline environment semantic priors. Environment attributes are extracted from the front-view camera image using a vision-language model and encoded with a frozen CLIP text encoder. The cached scene-level semantic embedding is used for environment-conditioned recalibration of the fused BEV representation. During training, a GT-center local prototype regularization branch aligns instance-level BEV features with environment-conditioned class prototypes through a contrastive objective. The prototype regularization branch is disabled during inference.

## Benchmark

- Dataset: nuScenes
- Task: 3D object detection
- Sensors: multi-view cameras and LiDAR
- Detection categories: the standard 10 nuScenes classes
- External pretrained semantic models: used for offline environment-prior generation

## Project status

The manuscript is currently in preparation. This repository is provided as a project landing page for benchmark submission provenance. Source code, trained models, detailed experimental settings, and the paper link will be updated after public release.

## Publication

See [PUBLICATION.md](PUBLICATION.md) for the current publication status.
