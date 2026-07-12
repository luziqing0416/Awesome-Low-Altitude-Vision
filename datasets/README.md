# Low-Altitude Vision Datasets

[Home](../README.md) · [中文主页](../README_zh-CN.md) · [Papers](../papers/README.md)

## Organization Standard

The repository uses a two-level organization:

1. **Primary grouping: application scenario** — the real-world problem for which the data were collected.
2. **Secondary descriptors: task and modality** — comparable tags that make cross-domain reuse visible.

Within each scenario, datasets are sorted by **release year in descending order**. A dataset appears once under its primary scenario; cross-domain relevance is expressed through tags rather than duplicate entries.

### Application Taxonomy

| Category | Typical scenes and targets |
|---|---|
| Search, rescue, and public safety | Missing persons, swimmers, disaster victims, emergency exercises |
| Disaster and environmental hazards | Floods, fires, damaged buildings and roads |
| Infrastructure inspection | Power lines, towers, insulators, bridges, pavements, wind turbines |
| Transportation and urban monitoring | Vehicles, pedestrians, traffic flow, urban scene parsing |
| Agriculture and forestry | Crops, weeds, plant stress, forests, fire monitoring |
| Ecology and wildlife | Animals, humans, anti-poaching, habitat monitoring |
| General-purpose aerial perception | Broad multi-scene benchmarks without one dominant application |
| Synthetic and simulated data | Generated or simulated low-altitude imagery for training and evaluation |

### Standard Task Tags

`Cls` classification · `Det` object detection · `SOT` single-object tracking · `MOT` multi-object tracking · `SemSeg` semantic segmentation · `InstSeg` instance segmentation · `VQA` visual question answering · `Action` action recognition · `Loc` localization

### Standard Modality Tags

`RGB` visible imagery · `TIR` thermal infrared · `RGB-T` aligned RGB and thermal · `MS` multispectral · `Video` temporal sequences · `Meta` flight/environment metadata · `Syn` synthetic imagery

### Source and Access Policy

Links are prioritized in this order:

1. official dataset or author-maintained project;
2. publisher/CVF/arXiv paper page;
3. trusted archival copy such as Zenodo;
4. clearly labeled community mirror only when no maintained official download exists.

`Open` means a public download was located; `Request` means registration or author approval may be required; `Archive` means an archival copy is used because the original project page is unavailable; `Check` means users should verify current availability and terms.

## 1. Search, Rescue, and Public Safety

| Dataset | Year | Task tags | Modality | Focus | Access and resources |
|---|---:|---|---|---|---|
| **NOMAD** | 2023 | Det | RGB, Video | Occluded people at five aerial distances; walking, lying, and hiding | Open · [Dataset](https://github.com/ArtRuss/NOMAD) · [Paper](https://arxiv.org/abs/2309.09518) |
| **SeaDronesSee** | 2022 | Det, SOT, MOT | RGB, Video, Meta | Swimmers, boats, jet skis, life-saving appliances, and buoys | Open · [Official site](https://seadronessee.cs.uni-tuebingen.de/) · [Dataset](https://seadronessee.cs.uni-tuebingen.de/dataset) · [Paper](https://openaccess.thecvf.com/content/WACV2022/html/Varga_SeaDronesSee_A_Maritime_Benchmark_for_Detecting_Humans_in_Open_Water_WACV_2022_paper.html) |
| **Manipal UAV Person Dataset** | 2020 | Det | RGB, Video | Small-person detection across varied weather, lighting, and UAV platforms | Open · [Dataset](https://github.com/Akshathakrbhat/Manipal-UAV-Person-Dataset) |
| **HERIDAL** | 2019 | Det | RGB | People in Mediterranean landscapes for land search and rescue | Check · [Paper](https://doi.org/10.1007/s11263-019-01177-1) |
| **Okutama-Action** | 2017 | Det, Action | RGB, Video | Concurrent human actions from an aerial viewpoint | Open · [Dataset](https://okutama-action.org/) · [Paper](https://openaccess.thecvf.com/content_cvpr_2017_workshops/w24/html/Barekatain_Okutama-Action_An_Aerial_CVPR_2017_paper.html) |

## 2. Disaster and Environmental Hazards

| Dataset | Year | Task tags | Modality | Focus | Access and resources |
|---|---:|---|---|---|---|
| **RescueNet** | 2023 | Cls, SemSeg | RGB | Post-disaster damage and scene understanding | Open · [Paper and data](https://www.nature.com/articles/s41597-023-02799-4) |
| **FloodNet** | 2021 | Cls, SemSeg, VQA | RGB | Post-Hurricane Harvey flooded and non-flooded infrastructure | Open · [Dataset](https://github.com/BinaLab/FloodNet-Supervised_v1.0) · [Paper](https://arxiv.org/abs/2105.08655) |
| **FLAME** | 2021 | Cls, SemSeg | RGB, TIR, Video | UAV pile-burn imagery for fire classification and segmentation | Open/non-commercial terms · [Project/code](https://github.com/AlirezaShamsoshoara/Fire-Detection-UAV-Aerial-Image-Classification-Segmentation-UnmannedAerialVehicle) · [Dataset record](https://doi.org/10.21227/7rk7-ey09) |
| **C2A** | 2024 | Det | Syn | Synthetic humans and disaster-response scenes | Open · [Dataset/code](https://github.com/Ragib-Amin-Nihal/C2A) · synthetic-only |

## 3. Infrastructure Inspection

| Dataset | Year | Task tags | Modality | Focus | Access and resources |
|---|---:|---|---|---|---|
| **PTL-AI Furnas** | 2023 | Cls, Det | RGB | Components and faults in real power-transmission-line maintenance imagery | Open · [Dataset](https://github.com/freds0/PTL-AI_Furnas_Dataset) |
| **TTPLA** | 2020 | Det, SemSeg, InstSeg | RGB | Transmission towers and thin power lines under varied views and backgrounds | Open · [Dataset](https://github.com/r3ab/ttpla_dataset) · [Paper](https://openaccess.thecvf.com/content/ACCV2020/html/Abdelfattah_TTPLA_An_Aerial-Image_Dataset_for_Detection_and_Segmentation_of_Transmission_ACCV_2020_paper.html) |

> This category intentionally remains broad. Future additions may cover bridges, façades, roofs, railways, roads, pipelines, solar panels, and wind turbines, provided the imagery was collected from a UAV or comparable low-altitude platform.

## 4. Transportation and Urban Monitoring

| Dataset | Year | Task tags | Modality | Focus | Access and resources |
|---|---:|---|---|---|---|
| **AU-AIR** | 2020 | Det | RGB, Video, Meta | Low-altitude urban traffic with flight and sensor metadata | Open · [Dataset](https://bozcani.github.io/auairdataset) · [Paper](https://doi.org/10.1109/ICRA40945.2020.9197293) |
| **DroneVehicle** | 2020 | Det | RGB-T | Cross-modal vehicle detection with oriented bounding boxes | Open · [Dataset](https://github.com/VisDrone/DroneVehicle) · [Paper](https://arxiv.org/abs/2003.02437) |
| **UAVDT** | 2018 | Det, SOT, MOT | RGB, Video | Vehicles across altitude, view, weather, and illumination conditions | Archive · [Dataset archive](https://zenodo.org/records/14575517) · [ECCV paper](https://openaccess.thecvf.com/content_ECCV_2018/html/Dawei_Du_The_Unmanned_Aerial_ECCV_2018_paper.html) |
| **UAVid** | 2018 | SemSeg | RGB, Video | 4K urban roads, buildings, vegetation, vehicles, and people | Open · [Dataset](https://uavid.nl/) · [Paper](https://arxiv.org/abs/1810.10438) |

## 5. Agriculture and Forestry

This category is retained because crop-scale targets, repetitive textures, multispectral sensors, seasonal domain shifts, and fine-grained segmentation can inform low-altitude data generation and evaluation.

| Dataset | Year | Task tags | Modality | Focus | Access and resources |
|---|---:|---|---|---|---|
| **FLAME** | 2021 | Cls, SemSeg | RGB, TIR, Video | Prescribed fire monitoring from UAVs | Listed under [Disaster and Environmental Hazards](#2-disaster-and-environmental-hazards) |

> Candidate agricultural datasets must clearly document UAV acquisition. Satellite-only and unspecified “aerial” datasets are not added by default.

## 6. Ecology and Wildlife

| Dataset | Year | Task tags | Modality | Focus | Access and resources |
|---|---:|---|---|---|---|
| **CART (Caltech Aerial RGB-Thermal)** | 2024 | Perception, localization | RGB-T, Meta | Rivers, lakes, coastlines, deserts, and forests for aerial field robotics | Open · [Dataset](https://data.caltech.edu/records/cks6g-ps927) · [Code](https://github.com/aerorobotics/caltech-aerial-rgbt-dataset) · [Paper](https://arxiv.org/abs/2403.08997) |
| **BIRDSAI** | 2020 | Det, SOT, MOT | TIR, Video, Syn | Humans and animals in protected areas, including real and synthetic thermal video | Open · [Dataset page](https://sites.google.com/view/elizabethbondi/dataset) · [Paper](https://openaccess.thecvf.com/content_WACV_2020/html/Bondi_BIRDSAI_A_Dataset_for_Detection_and_Tracking_in_Aerial_Thermal_Infrared_WACV_2020_paper.html) |

## 7. General-Purpose Aerial Perception

| Dataset | Year | Task tags | Modality | Focus | Access and resources |
|---|---:|---|---|---|---|
| **VisDrone** | 2018– | Det, SOT, MOT, crowd counting | RGB, Video | Diverse pedestrians and vehicles in urban and rural scenes | Open · [Dataset](https://github.com/VisDrone/VisDrone-Dataset) · [Paper](https://doi.org/10.1109/TPAMI.2021.3119563) |
| **UAV123 / UAV20L** | 2016 | SOT | RGB, Video | People, vehicles, boats, and other moving targets | Open · [Project](https://cemse.kaust.edu.sa/ivul/uav123) · [Paper](https://arxiv.org/abs/1605.07109) |

## 8. Synthetic and Simulated Data

| Dataset / tool | Year | Task tags | Modality | Focus | Access and resources |
|---|---:|---|---|---|---|
| **C2A** | 2024 | Det | Syn | Composited/synthetic disaster scenarios for human detection | Open · [Dataset/code](https://github.com/Ragib-Amin-Nihal/C2A) |
| **Synthetic SeaDronesSee** | — | Det | Syn | Generated maritime SAR scenes and objects | Open · [Official dataset page](https://seadronessee.cs.uni-tuebingen.de/dataset) |
| **AirSim** | 2017 | Simulation | RGB, depth, segmentation, sensors | UAV and autonomous-vehicle simulation | Open · [Code](https://github.com/microsoft/AirSim) |

## Dataset Metadata Checklist

Every future entry should record, when available:

- official name, version, release year, and maintenance status;
- real, synthetic, or mixed origin;
- UAV/platform type, altitude or GSD, camera angle, and geographic setting;
- image/video modality, sensor type, resolution, and environmental metadata;
- scene categories, target taxonomy, positive/negative-frame distribution, and target scale;
- official tasks, annotation types/formats, sequence information, and split protocol;
- dataset size, license, ethics/privacy notes, access procedure, and redistribution restrictions;
- official project, stable download/archive, paper, code, and benchmark links.

For search-and-rescue research, **negative-frame availability**, **continuous-video structure**, **target prevalence**, **target size**, and **real versus staged collection** are especially important. These fields will be added progressively when verified from primary sources.

> A listing does not imply permission to redistribute or use a dataset commercially. Check the original terms before use.
