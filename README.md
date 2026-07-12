# Awesome Low-Altitude Vision

> A curated list of datasets, papers, benchmarks, and resources for low-altitude UAV vision.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0--1.0-lightgrey.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

Low-altitude UAV vision differs from satellite and ground-level vision in viewpoint, target scale, camera motion, background, and operational constraints. This list covers search and rescue, disaster response, infrastructure inspection, transportation, agriculture, ecology, general aerial perception, and synthetic data.

**English** | [简体中文](README_zh-CN.md)

## Contents

- [Datasets](#datasets)
  - [Search, Rescue, and Public Safety](#search-rescue-and-public-safety)
  - [Disaster and Environmental Hazards](#disaster-and-environmental-hazards)
  - [Infrastructure Inspection](#infrastructure-inspection)
  - [Transportation and Urban Monitoring](#transportation-and-urban-monitoring)
  - [Agriculture, Forestry, and Ecology](#agriculture-forestry-and-ecology)
  - [General-Purpose Aerial Perception](#general-purpose-aerial-perception)
  - [Synthetic and Simulated Data](#synthetic-and-simulated-data)
- [Papers and Benchmarks](#papers-and-benchmarks)
  - [Detection and Tracking](#detection-and-tracking)
  - [Human Understanding and Search and Rescue](#human-understanding-and-search-and-rescue)
  - [Disaster Understanding](#disaster-understanding)
  - [Inspection and Multimodal Perception](#inspection-and-multimodal-perception)
  - [Synthetic Data, Simulation, and Agents](#synthetic-data-simulation-and-agents)
- [Contributing](#contributing)

## Datasets

### Search, Rescue, and Public Safety

| Dataset | Year | Tasks | Modality | Focus | Resources |
|---|---:|---|---|---|---|
| **NOMAD** | 2023 | Detection | RGB video | Occluded people at multiple aerial distances | [Dataset](https://github.com/ArtRuss/NOMAD) · [Paper](https://arxiv.org/abs/2309.09518) |
| **SeaDronesSee** | 2022 | Detection, SOT, MOT | RGB video + metadata | Swimmers, boats, jet skis, rescue appliances, and buoys | [Official site](https://seadronessee.cs.uni-tuebingen.de/) · [Dataset](https://seadronessee.cs.uni-tuebingen.de/dataset) · [Paper](https://openaccess.thecvf.com/content/WACV2022/html/Varga_SeaDronesSee_A_Maritime_Benchmark_for_Detecting_Humans_in_Open_Water_WACV_2022_paper.html) |
| **Manipal UAV Person** | 2020 | Detection | RGB video | Small-person detection under varied weather and lighting | [Dataset](https://github.com/Akshathakrbhat/Manipal-UAV-Person-Dataset) |
| **HERIDAL** | 2019 | Detection | RGB images | People in Mediterranean landscapes for land SAR | [Paper](https://doi.org/10.1007/s11263-019-01177-1) |
| **Okutama-Action** | 2017 | Detection, action recognition | RGB video | Concurrent human actions from an aerial viewpoint | [Dataset](https://okutama-action.org/) · [Paper](https://openaccess.thecvf.com/content_cvpr_2017_workshops/w24/html/Barekatain_Okutama-Action_An_Aerial_CVPR_2017_paper.html) |

### Disaster and Environmental Hazards

| Dataset | Year | Tasks | Modality | Focus | Resources |
|---|---:|---|---|---|---|
| **C2A** | 2024 | Detection | Synthetic RGB | Synthetic humans in disaster-response scenes | [Dataset and code](https://github.com/Ragib-Amin-Nihal/C2A) |
| **RescueNet** | 2023 | Classification, segmentation | RGB | Post-disaster damage and scene understanding | [Paper and data](https://www.nature.com/articles/s41597-023-02799-4) |
| **FloodNet** | 2021 | Classification, segmentation, VQA | RGB | Flooded and non-flooded infrastructure after Hurricane Harvey | [Dataset](https://github.com/BinaLab/FloodNet-Supervised_v1.0) · [Paper](https://arxiv.org/abs/2105.08655) |
| **FLAME** | 2021 | Classification, segmentation | RGB, thermal, video | UAV pile-burn fire monitoring | [Project](https://github.com/AlirezaShamsoshoara/Fire-Detection-UAV-Aerial-Image-Classification-Segmentation-UnmannedAerialVehicle) · [Dataset record](https://doi.org/10.21227/7rk7-ey09) |

### Infrastructure Inspection

| Dataset | Year | Tasks | Modality | Focus | Resources |
|---|---:|---|---|---|---|
| **PTL-AI Furnas** | 2023 | Classification, detection | RGB | Components and faults in power-line maintenance imagery | [Dataset](https://github.com/freds0/PTL-AI_Furnas_Dataset) |
| **TTPLA** | 2020 | Detection, semantic/instance segmentation | RGB | Transmission towers and thin power lines | [Dataset](https://github.com/r3ab/ttpla_dataset) · [Paper](https://openaccess.thecvf.com/content/ACCV2020/html/Abdelfattah_TTPLA_An_Aerial-Image_Dataset_for_Detection_and_Segmentation_of_Transmission_ACCV_2020_paper.html) |

### Transportation and Urban Monitoring

| Dataset | Year | Tasks | Modality | Focus | Resources |
|---|---:|---|---|---|---|
| **AU-AIR** | 2020 | Detection | RGB video + metadata | Low-altitude urban traffic | [Dataset](https://bozcani.github.io/auairdataset) · [Paper](https://doi.org/10.1109/ICRA40945.2020.9197293) |
| **DroneVehicle** | 2020 | Detection | RGB–thermal | Cross-modal vehicle detection with oriented boxes | [Dataset](https://github.com/VisDrone/DroneVehicle) · [Paper](https://arxiv.org/abs/2003.02437) |
| **UAVDT** | 2018 | Detection, SOT, MOT | RGB video | Vehicles under varied altitude, view, weather, and illumination | [Dataset archive](https://zenodo.org/records/14575517) · [Paper](https://openaccess.thecvf.com/content_ECCV_2018/html/Dawei_Du_The_Unmanned_Aerial_ECCV_2018_paper.html) |
| **UAVid** | 2018 | Semantic segmentation | 4K RGB video | Urban roads, buildings, vegetation, vehicles, and people | [Dataset](https://uavid.nl/) · [Paper](https://arxiv.org/abs/1810.10438) |

### Agriculture, Forestry, and Ecology

| Dataset | Year | Tasks | Modality | Focus | Resources |
|---|---:|---|---|---|---|
| **CART** | 2024 | Aerial field-robotics perception | RGB–thermal + GPS/IMU | Rivers, lakes, coastlines, deserts, and forests | [Dataset](https://data.caltech.edu/records/cks6g-ps927) · [Code](https://github.com/aerorobotics/caltech-aerial-rgbt-dataset) · [Paper](https://arxiv.org/abs/2403.08997) |
| **BIRDSAI** | 2020 | Detection, SOT, MOT | Real and synthetic thermal video | Humans and animals in protected areas | [Dataset](https://sites.google.com/view/elizabethbondi/dataset) · [Paper](https://openaccess.thecvf.com/content_WACV_2020/html/Bondi_BIRDSAI_A_Dataset_for_Detection_and_Tracking_in_Aerial_Thermal_Infrared_WACV_2020_paper.html) |

### General-Purpose Aerial Perception

| Dataset | Year | Tasks | Modality | Focus | Resources |
|---|---:|---|---|---|---|
| **VisDrone** | 2018– | Detection, tracking, crowd counting | RGB image/video | Pedestrians and vehicles in diverse urban and rural scenes | [Dataset](https://github.com/VisDrone/VisDrone-Dataset) · [Paper](https://doi.org/10.1109/TPAMI.2021.3119563) |
| **UAV123 / UAV20L** | 2016 | Single-object tracking | RGB video | People, vehicles, boats, and other moving targets | [Project](https://cemse.kaust.edu.sa/ivul/uav123) · [Paper](https://arxiv.org/abs/1605.07109) |

### Synthetic and Simulated Data

| Dataset / tool | Year | Tasks | Focus | Resources |
|---|---:|---|---|---|
| **C2A** | 2024 | Human detection | Synthetic disaster-response scenes | [Dataset and code](https://github.com/Ragib-Amin-Nihal/C2A) |
| **Synthetic SeaDronesSee** | — | Maritime object detection | Generated maritime SAR scenes | [Official dataset page](https://seadronessee.cs.uni-tuebingen.de/dataset) |
| **AirSim** | 2017 | Simulation | UAV sensing and autonomous-vehicle simulation | [Code](https://github.com/microsoft/AirSim) |
| **CARLA** | 2017 | Simulation | Urban simulation with configurable aerial cameras | [Code](https://github.com/carla-simulator/carla) |

## Papers and Benchmarks

### Detection and Tracking

- **Detection and Tracking Meet Drones Challenge** — Pengfei Zhu et al. IEEE TPAMI 2022. [Paper](https://doi.org/10.1109/TPAMI.2021.3119563) · [Benchmark](https://github.com/VisDrone/VisDrone-Dataset)
- **AU-AIR: A Multi-modal Unmanned Aerial Vehicle Dataset for Low Altitude Traffic Surveillance** — Ilker Bozcan and Erdal Kayacan. ICRA 2020. [Paper](https://doi.org/10.1109/ICRA40945.2020.9197293) · [Dataset](https://bozcani.github.io/auairdataset)
- **The Unmanned Aerial Vehicle Benchmark: Object Detection and Tracking** — Dawei Du et al. ECCV 2018. [Paper](https://openaccess.thecvf.com/content_ECCV_2018/html/Dawei_Du_The_Unmanned_Aerial_ECCV_2018_paper.html) · [Data archive](https://zenodo.org/records/14575517)
- **A Benchmark and Simulator for UAV Tracking** — Matthias Mueller et al. ECCV 2016. [Paper](https://arxiv.org/abs/1605.07109) · [Project](https://cemse.kaust.edu.sa/ivul/uav123)

### Human Understanding and Search and Rescue

- **NOMAD: A Natural, Occluded, Multi-scale Aerial Dataset for Emergency Response Scenarios** — 2023. [Paper](https://arxiv.org/abs/2309.09518) · [Dataset](https://github.com/ArtRuss/NOMAD)
- **SeaDronesSee: A Maritime Benchmark for Detecting Humans in Open Water** — Lojze A. Varga et al. WACV 2022. [Paper](https://openaccess.thecvf.com/content/WACV2022/html/Varga_SeaDronesSee_A_Maritime_Benchmark_for_Detecting_Humans_in_Open_Water_WACV_2022_paper.html) · [Project](https://seadronessee.cs.uni-tuebingen.de/)
- **Deep Learning Approach on Aerial Imagery in Supporting Land Search and Rescue Missions** — IJCV 2019. [Paper](https://doi.org/10.1007/s11263-019-01177-1)
- **Okutama-Action: An Aerial View Video Dataset for Concurrent Human Action Detection** — Muhammed Barekatain et al. CVPR Workshops 2017. [Paper](https://openaccess.thecvf.com/content_cvpr_2017_workshops/w24/html/Barekatain_Okutama-Action_An_Aerial_CVPR_2017_paper.html) · [Dataset](https://okutama-action.org/)

### Disaster Understanding

- **RescueNet: A High Resolution UAV Semantic Segmentation Dataset for Natural Disaster Damage Assessment** — Scientific Data 2023. [Paper and data](https://www.nature.com/articles/s41597-023-02799-4)
- **FloodNet: A High Resolution Aerial Imagery Dataset for Post Flood Scene Understanding** — IEEE Access 2021. [Paper](https://arxiv.org/abs/2105.08655) · [Dataset](https://github.com/BinaLab/FloodNet-Supervised_v1.0)
- **Aerial Imagery Pile Burn Detection Using Deep Learning: The FLAME Dataset** — Computer Networks 2021. [Project](https://github.com/AlirezaShamsoshoara/Fire-Detection-UAV-Aerial-Image-Classification-Segmentation-UnmannedAerialVehicle) · [Dataset](https://doi.org/10.21227/7rk7-ey09)

### Inspection and Multimodal Perception

- **CART: Caltech Aerial RGB-Thermal Dataset in the Wild** — 2024. [Paper](https://arxiv.org/abs/2403.08997) · [Dataset](https://data.caltech.edu/records/cks6g-ps927)
- **TTPLA: An Aerial-Image Dataset for Detection and Segmentation of Transmission Towers and Power Lines** — ACCV 2020. [Paper](https://openaccess.thecvf.com/content/ACCV2020/html/Abdelfattah_TTPLA_An_Aerial-Image_Dataset_for_Detection_and_Segmentation_of_Transmission_ACCV_2020_paper.html) · [Dataset](https://github.com/r3ab/ttpla_dataset)
- **BIRDSAI: A Dataset for Detection and Tracking in Aerial Thermal Infrared Videos** — WACV 2020. [Paper](https://openaccess.thecvf.com/content_WACV_2020/html/Bondi_BIRDSAI_A_Dataset_for_Detection_and_Tracking_in_Aerial_Thermal_Infrared_WACV_2020_paper.html) · [Dataset](https://sites.google.com/view/elizabethbondi/dataset)
- **UAVid: A Semantic Segmentation Dataset for UAV Imagery** — 2018. [Paper](https://arxiv.org/abs/1810.10438) · [Dataset](https://uavid.nl/)

### Synthetic Data, Simulation, and Agents

This section tracks work on controllable UAV image generation, simulation-to-real adaptation, prompt and scene planning, automatic annotation, image–text consistency, physical plausibility, and closed-loop generation.

- [Synthetic SeaDronesSee](https://seadronessee.cs.uni-tuebingen.de/dataset)
- [AirSim](https://github.com/microsoft/AirSim)
- [CARLA](https://github.com/carla-simulator/carla)

## Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md) or use the [resource suggestion template](https://github.com/luziqing0416/Awesome-Low-Altitude-Vision/issues/new?template=resource-suggestion.yml).

This repository is an index and does not redistribute datasets or copyrighted papers. Individual resources retain their original licenses.

## License

The list is released under [CC0 1.0](LICENSE).
