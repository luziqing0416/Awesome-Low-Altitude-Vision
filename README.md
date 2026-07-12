# Awesome Low-Altitude Vision

> A curated list of datasets, papers, benchmarks, and resources for low-altitude UAV vision.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0--1.0-lightgrey.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

Low-altitude UAV vision differs from satellite and ground-level vision in viewpoint, target scale, camera motion, background, and operational constraints. This repository focuses on object detection, tracking, segmentation, search and rescue, disaster response, maritime perception, multimodal sensing, and synthetic-data generation.

**English** | [简体中文](README_zh-CN.md)

## Contents

- [Datasets](datasets/README.md)
  - General UAV perception
  - Maritime search and rescue
  - Disaster response
  - Multimodal and cross-spectral perception
- [Papers](papers/README.md)
  - Detection and tracking
  - Maritime search and rescue
  - Disaster understanding
  - Synthetic data, simulation, and agents
- [Contributing](CONTRIBUTING.md)

## Featured Datasets

| Dataset | Tasks | Primary scenario | Resources |
|---|---|---|---|
| **SeaDronesSee** | Detection, single-/multi-object tracking | Maritime search and rescue | [Official site](https://seadronessee.cs.uni-tuebingen.de/) · [Paper](https://openaccess.thecvf.com/content/WACV2022/html/Varga_SeaDronesSee_A_Maritime_Benchmark_for_Detecting_Humans_in_Open_Water_WACV_2022_paper.html) |
| **VisDrone** | Detection, tracking, crowd counting | Urban and rural UAV imagery | [Dataset](https://github.com/VisDrone/VisDrone-Dataset) · [Paper](https://doi.org/10.1109/TPAMI.2021.3119563) |
| **UAVDT** | Detection and tracking | Low-altitude traffic monitoring | [Project](https://sites.google.com/site/daviddo0323/projects/uavdt) · [Paper](https://openaccess.thecvf.com/content_ECCV_2018/html/Dawei_Du_The_Unmanned_Aerial_ECCV_2018_paper.html) |
| **FloodNet** | Classification, segmentation, VQA | Post-flood scene understanding | [Dataset](https://github.com/BinaLab/FloodNet-Supervised_v1.0) · [Paper](https://arxiv.org/abs/2105.08655) |
| **RescueNet** | Classification and segmentation | Post-disaster damage assessment | [Paper and data](https://www.nature.com/articles/s41597-023-02799-4) |

➡️ See the [complete dataset index](datasets/README.md).

## Featured Research Topics

- Small-object detection from moving aerial platforms
- Person detection and frame filtering for search-and-rescue video
- Maritime swimmer detection and tracking
- Post-disaster scene understanding
- RGB–thermal and multisensor fusion
- Synthetic UAV imagery and simulation-to-real adaptation
- Vision-language-assisted annotation and quality evaluation
- Agent-based, closed-loop data generation

➡️ See the [paper and benchmark index](papers/README.md).

## Scope

Included resources should be directly relevant to imagery captured by UAVs or comparable low-altitude aerial platforms. Satellite-only remote-sensing resources are generally excluded unless they are explicitly combined with low-altitude UAV data.

This repository is an index and does **not** redistribute datasets or paper PDFs. Always check the original license, access conditions, privacy requirements, and permitted uses.

## Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md) or use the [resource suggestion issue template](https://github.com/luziqing0416/Awesome-Low-Altitude-Vision/issues/new?template=resource-suggestion.yml).

Useful additions include:

- newly released datasets and benchmarks;
- high-quality surveys and reproducible methods;
- corrected metadata or broken links;
- license and access information;
- resources for realistic low-altitude search-and-rescue workflows.

## Acknowledgements

The organization of this repository is inspired by the wider Awesome-list community and resources such as [Awesome Dataset Distillation](https://github.com/Guang000/Awesome-Dataset-Distillation) and [Awesome VisDrone](https://github.com/VisDrone/Awesome-VisDrone).

## License

The curated list is released under [CC0 1.0](LICENSE). Individual datasets, papers, codebases, and media retain their original licenses.
