# Papers and Benchmarks

[Home](../README.md) · [中文主页](../README_zh-CN.md) · [Datasets](../datasets/README.md)

The list begins with benchmark-defining and dataset papers. Method papers, surveys, and synthetic-data research will be expanded as verified entries are contributed.

## Detection and Tracking

- **A Benchmark and Simulator for UAV Tracking** — Matthias Mueller, Neil Smith, Bernard Ghanem. ECCV 2016. [Paper](https://arxiv.org/abs/1605.07109) · [Project](https://cemse.kaust.edu.sa/ivul/uav123)
- **The Unmanned Aerial Vehicle Benchmark: Object Detection and Tracking** — Dawei Du et al. ECCV 2018. [Paper](https://openaccess.thecvf.com/content_ECCV_2018/html/Dawei_Du_The_Unmanned_Aerial_ECCV_2018_paper.html) · [Project](https://sites.google.com/site/daviddo0323/projects/uavdt)
- **Detection and Tracking Meet Drones Challenge** — Pengfei Zhu et al. IEEE TPAMI 2022. [Paper](https://doi.org/10.1109/TPAMI.2021.3119563) · [Benchmark](https://github.com/VisDrone/VisDrone-Dataset)
- **AU-AIR: A Multi-modal Unmanned Aerial Vehicle Dataset for Low Altitude Traffic Surveillance** — Ilker Bozcan, Erdal Kayacan. ICRA 2020. [Paper](https://doi.org/10.1109/ICRA40945.2020.9197293) · [Dataset](https://bozcani.github.io/auairdataset)

## Human Understanding

- **Okutama-Action: An Aerial View Video Dataset for Concurrent Human Action Detection** — Muhammed Barekatain et al. CVPR Workshops 2017. [Paper](https://openaccess.thecvf.com/content_cvpr_2017_workshops/w24/html/Barekatain_Okutama-Action_An_Aerial_CVPR_2017_paper.html) · [Dataset](https://okutama-action.org/)

## Maritime Search and Rescue

- **SeaDronesSee: A Maritime Benchmark for Detecting Humans in Open Water** — Lojze A. Varga et al. WACV 2022. [Paper](https://openaccess.thecvf.com/content/WACV2022/html/Varga_SeaDronesSee_A_Maritime_Benchmark_for_Detecting_Humans_in_Open_Water_WACV_2022_paper.html) · [Project](https://seadronessee.cs.uni-tuebingen.de/)

## Disaster Understanding

- **FloodNet: A High Resolution Aerial Imagery Dataset for Post Flood Scene Understanding** — Maryam Rahnemoonfar et al. IEEE Access 2021. [Paper](https://arxiv.org/abs/2105.08655) · [Dataset](https://github.com/BinaLab/FloodNet-Supervised_v1.0)
- **RescueNet: A High Resolution UAV Semantic Segmentation Dataset for Natural Disaster Damage Assessment** — Scientific Data 2023. [Paper and data](https://www.nature.com/articles/s41597-023-02799-4)

## Semantic Segmentation

- **UAVid: A Semantic Segmentation Dataset for UAV Imagery** — Ye Lyu et al. 2018. [Paper](https://arxiv.org/abs/1810.10438) · [Dataset](https://uavid.nl/)

## Multimodal and Cross-Spectral Vision

- **Drone-based RGB-Infrared Cross-Modality Vehicle Detection via Uncertainty-Aware Learning** — 2020. [Paper](https://arxiv.org/abs/2003.02437) · [Dataset](https://github.com/VisDrone/DroneVehicle)

## Synthetic Data, Simulation, and Agents

This section is reserved for work that directly supports low-altitude image synthesis, scene planning, simulation-to-real transfer, controllable generation, automatic annotation, or closed-loop quality evaluation.

### Foundational Tools

- **AirSim** — an open-source simulator for autonomous vehicles and UAV research. [Code](https://github.com/microsoft/AirSim)
- **CARLA** — an autonomous-driving simulator that can support aerial-camera data generation. [Code](https://github.com/carla-simulator/carla)
- **Synthetic SeaDronesSee** — synthetic maritime SAR data linked by the official benchmark. [Dataset page](https://seadronessee.cs.uni-tuebingen.de/dataset)

### Topics Being Curated

- Prompt and scene planning for controllable UAV image generation
- Domain adaptation and LoRA-based visual adaptation
- Vision-language-assisted bounding-box annotation
- Image–text consistency, physical plausibility, and distribution evaluation
- Iterative generation, rejection, editing, and regeneration agents
- Positive/negative frame generation for realistic search-and-rescue video pipelines

## Related Resource Lists

- [Awesome VisDrone](https://github.com/VisDrone/Awesome-VisDrone)
- [UAV-Vision](https://github.com/wangdongdut/UAV-Vision)
- [Awesome Dataset Distillation](https://github.com/Guang000/Awesome-Dataset-Distillation)

## Entry Format

```markdown
- **Paper title** — Authors. Venue Year. [Paper](URL) · [Code](URL) · [Project](URL)
```

Prefer the publisher page, CVF Open Access, arXiv, or an author-maintained project. Avoid unauthorized PDF mirrors.
