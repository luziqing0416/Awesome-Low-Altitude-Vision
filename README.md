# Awesome Low-Altitude Vision

> A curated list of datasets, papers, benchmarks, and resources for low-altitude UAV vision.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0--1.0-lightgrey.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

Low-altitude UAV vision differs from satellite and ground-level vision in viewpoint, target scale, camera motion, background, and operational constraints. The collection covers search and rescue, disaster response, infrastructure inspection, transportation, agriculture, ecology, general aerial perception, and synthetic data.

**English** | [简体中文](README_zh-CN.md)

## Organization

Resources are organized primarily by **application scenario**. Visual tasks and sensor modalities are recorded as standardized tags, and entries within each scenario are sorted by **release year (newest first)**.

- [Datasets](datasets/README.md)
  - Search, rescue, and public safety
  - Disaster and environmental hazards
  - Infrastructure inspection
  - Transportation and urban monitoring
  - Agriculture and forestry
  - Ecology and wildlife
  - General-purpose aerial perception
  - Synthetic and simulated data
- [Papers and benchmarks](papers/README.md)
- [Contributing](CONTRIBUTING.md)

## Featured Datasets

| Dataset | Tasks | Primary scenario | Resources |
|---|---|---|---|
| **SeaDronesSee** | Detection and tracking | Maritime search and rescue | [Official site](https://seadronessee.cs.uni-tuebingen.de/) · [Paper](https://openaccess.thecvf.com/content/WACV2022/html/Varga_SeaDronesSee_A_Maritime_Benchmark_for_Detecting_Humans_in_Open_Water_WACV_2022_paper.html) |
| **NOMAD** | Occluded-person detection | Land search and rescue | [Dataset](https://github.com/ArtRuss/NOMAD) · [Paper](https://arxiv.org/abs/2309.09518) |
| **RescueNet / FloodNet** | Classification, segmentation, VQA | Disaster understanding | [RescueNet](https://www.nature.com/articles/s41597-023-02799-4) · [FloodNet](https://github.com/BinaLab/FloodNet-Supervised_v1.0) |
| **TTPLA** | Detection and segmentation | Power-line inspection | [Dataset](https://github.com/r3ab/ttpla_dataset) · [Paper](https://openaccess.thecvf.com/content/ACCV2020/html/Abdelfattah_TTPLA_An_Aerial-Image_Dataset_for_Detection_and_Segmentation_of_Transmission_ACCV_2020_paper.html) |
| **UAVDT** | Detection and tracking | Traffic monitoring | [Dataset archive](https://zenodo.org/records/14575517) · [Paper](https://openaccess.thecvf.com/content_ECCV_2018/html/Dawei_Du_The_Unmanned_Aerial_ECCV_2018_paper.html) |
| **BIRDSAI** | Detection and tracking | Thermal wildlife monitoring | [Dataset](https://sites.google.com/view/elizabethbondi/dataset) · [Paper](https://openaccess.thecvf.com/content_WACV_2020/html/Bondi_BIRDSAI_A_Dataset_for_Detection_and_Tracking_in_Aerial_Thermal_Infrared_WACV_2020_paper.html) |

➡️ See the [complete dataset taxonomy and index](datasets/README.md).

## Inclusion Principles

- The resource must involve UAVs or a comparable low-altitude aerial platform.
- Application-specific datasets are retained even when they are outside search and rescue, because their sensing, annotation, domain-shift, and small-object challenges may transfer.
- Satellite-only datasets are normally excluded.
- Official or author-maintained sources are preferred; stable archives are clearly labeled when original links fail.
- Real, synthetic, and mixed datasets are explicitly distinguished.
- This repository indexes resources and does not redistribute datasets or copyrighted PDFs.

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) or use the [resource suggestion issue template](https://github.com/luziqing0416/Awesome-Low-Altitude-Vision/issues/new?template=resource-suggestion.yml).

## License

The curated list is released under [CC0 1.0](LICENSE). Individual resources retain their original licenses.
