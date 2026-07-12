# Low-Altitude Vision Datasets

[Home](../README.md) · [中文主页](../README_zh-CN.md) · [Papers](../papers/README.md)

This index records the dataset's official benchmark tasks rather than every possible downstream use. “Size” values are intentionally omitted when dataset versions or official splits differ; consult the linked source for exact statistics.

## General UAV Perception

| Dataset | Year | Tasks | Modality | Scenes / targets | Resources |
|---|---:|---|---|---|---|
| **VisDrone** | 2018– | Detection, tracking, crowd counting | RGB image/video | Pedestrians and vehicles; urban and rural scenes | [Dataset](https://github.com/VisDrone/VisDrone-Dataset) · [Paper](https://doi.org/10.1109/TPAMI.2021.3119563) |
| **UAVDT** | 2018 | Detection, single-/multi-object tracking | RGB video | Vehicles under varied altitude, view, weather, and illumination | [Project](https://sites.google.com/site/daviddo0323/projects/uavdt) · [Paper](https://openaccess.thecvf.com/content_ECCV_2018/html/Dawei_Du_The_Unmanned_Aerial_ECCV_2018_paper.html) |
| **UAV123 / UAV20L** | 2016 | Single-object tracking | RGB video | People, vehicles, boats, and other moving targets | [Project](https://cemse.kaust.edu.sa/ivul/uav123) · [Paper](https://arxiv.org/abs/1605.07109) |
| **AU-AIR** | 2020 | Detection and traffic understanding | RGB + flight/sensor metadata | Low-altitude urban traffic | [Dataset](https://bozcani.github.io/auairdataset) · [Paper](https://doi.org/10.1109/ICRA40945.2020.9197293) |
| **UAVid** | 2018 | Semantic segmentation | 4K RGB video | Urban roads, buildings, vegetation, vehicles, and people | [Dataset](https://uavid.nl/) · [Paper](https://arxiv.org/abs/1810.10438) |
| **Okutama-Action** | 2017 | Human detection and action recognition | RGB video | Human actions observed from UAVs | [Dataset](https://okutama-action.org/) · [Paper](https://openaccess.thecvf.com/content_cvpr_2017_workshops/w24/html/Barekatain_Okutama-Action_An_Aerial_CVPR_2017_paper.html) |

## Maritime Search and Rescue

| Dataset | Year | Tasks | Modality / annotations | Resources |
|---|---:|---|---|---|
| **SeaDronesSee** | 2022 | Detection, SOT, MOT | RGB UAV imagery; swimmers, boats, jet skis, life-saving appliances, buoys; environmental metadata | [Official site](https://seadronessee.cs.uni-tuebingen.de/) · [Dataset](https://seadronessee.cs.uni-tuebingen.de/dataset) · [Paper](https://openaccess.thecvf.com/content/WACV2022/html/Varga_SeaDronesSee_A_Maritime_Benchmark_for_Detecting_Humans_in_Open_Water_WACV_2022_paper.html) |
| **Synthetic SeaDronesSee** | — | Synthetic maritime object detection | Generated maritime SAR scenes linked by the benchmark maintainers | [Dataset page](https://seadronessee.cs.uni-tuebingen.de/dataset) |

## Disaster Response

| Dataset | Year | Tasks | Scene / annotations | Resources |
|---|---:|---|---|---|
| **FloodNet** | 2021 | Classification, segmentation, VQA | High-resolution post-Hurricane Harvey UAS imagery with flooded/non-flooded infrastructure labels | [Dataset](https://github.com/BinaLab/FloodNet-Supervised_v1.0) · [Paper](https://arxiv.org/abs/2105.08655) |
| **RescueNet** | 2023 | Classification and segmentation | High-resolution post-disaster UAV imagery with damage and scene classes | [Paper and data](https://www.nature.com/articles/s41597-023-02799-4) |

## Multimodal and Cross-Spectral Perception

| Dataset | Year | Tasks | Modality / annotations | Resources |
|---|---:|---|---|---|
| **DroneVehicle** | 2020 | Vehicle detection | Paired RGB and infrared UAV imagery with oriented bounding boxes | [Dataset](https://github.com/VisDrone/DroneVehicle) · [Paper](https://arxiv.org/abs/2003.02437) |

## Suggested Metadata for Future Entries

- Official name and version
- Release year
- Acquisition platform and altitude range
- Image/video modality and sensor type
- Scene, target categories, and negative-frame availability
- Official tasks and annotation formats
- Dataset size and train/validation/test split
- License, access procedure, and redistribution restrictions
- Paper, project, download, code, and benchmark links

> Dataset licenses and terms vary. A listing here does not imply permission to redistribute or use a dataset commercially.
