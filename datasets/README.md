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
| Disaster and environmental hazards | Floods, fires, damaged buildings and roads, hazy and adverse weather |
| Infrastructure inspection | Power lines, towers, insulators, bridges, pavements, wind turbines |
| Transportation and urban monitoring | Vehicles, pedestrians, traffic flow, urban scene parsing, trajectory prediction |
| Agriculture and forestry | Crops, weeds, plant stress, forests, fire monitoring |
| Ecology and wildlife | Animals, humans, anti-poaching, habitat monitoring |
| Thermal and multimodal perception | RGB-thermal detection, tracking, and cross-modal fusion |
| Multi-drone collaborative perception | Cooperative detection, tracking, and prediction from multiple UAVs |
| Embodied AI and vision-language navigation | Language-guided navigation, dialog, and agent benchmarks |
| General-purpose aerial perception | Broad multi-scene benchmarks without one dominant application |
| Synthetic and simulated data | Generated or simulated low-altitude imagery for training and evaluation |

### Standard Task Tags

`Cls` classification · `Det` object detection · `SOT` single-object tracking · `MOT` multi-object tracking · `SemSeg` semantic segmentation · `InstSeg` instance segmentation · `VQA` visual question answering · `Action` action recognition · `Loc` localization · `VLN` vision-language navigation · `Count` crowd counting · `Pred` trajectory prediction · `3DDet` 3D detection

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
| **FIReStereo** | 2024 | Depth, Det | RGB, TIR (stereo), LiDAR, Meta | Fire and smoke scenes with binocular stereo infrared and RGB for emergency-response depth perception | Check · CMU dataset for fire-scene UAV stereo perception |
| **RescueNet** | 2023 | Cls, SemSeg | RGB | Post-disaster damage and scene understanding | Open · [Paper and data](https://www.nature.com/articles/s41597-023-02799-4) |
| **FloodNet** | 2021 | Cls, SemSeg, VQA | RGB | Post-Hurricane Harvey flooded and non-flooded infrastructure | Open · [Dataset](https://github.com/BinaLab/FloodNet-Supervised_v1.0) · [Paper](https://arxiv.org/abs/2105.08655) |
| **FLAME** | 2021 | Cls, SemSeg | RGB, TIR, Video | UAV pile-burn imagery for fire classification and segmentation | Open/non-commercial terms · [Project/code](https://github.com/AlirezaShamsoshoara/Fire-Detection-UAV-Aerial-Image-Classification-Segmentation-UnmannedAerialVehicle) · [Dataset record](https://doi.org/10.21227/7rk7-ey09) |
| **HazyDet** | 2024 | Det | RGB, Depth | Drone-view object detection under varied haze concentrations with depth cues | Open · [Dataset/code](https://github.com/GrokCV/HazyDet) · [Paper](https://arxiv.org/abs/2409.19833) |
| **UAV-AWID** | 2024 | Det | RGB | Adverse weather and image degradation (rain, motion blur, noise) at multiple severity levels | Open · [Dataset/code](https://github.com/AdnanMunir338/UAV-AWID) |
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
| **VDD (Varied Drone Dataset)** | 2025 | SemSeg | RGB | Multi-scene urban/industrial/rural/natural semantic segmentation with 7 classes across varied camera angles and lighting | Open · [Dataset/code](https://github.com/RussRobin/VDD) · [Paper](https://arxiv.org/abs/2305.13608) |
| **AU-AIR** | 2020 | Det | RGB, Video, Meta | Low-altitude urban traffic with flight and sensor metadata | Open · [Dataset](https://bozcani.github.io/auairdataset) · [Paper](https://doi.org/10.1109/ICRA40945.2020.9197293) |
| **DroneVehicle** | 2020 | Det | RGB-T | Cross-modal vehicle detection with oriented bounding boxes | Open · [Dataset](https://github.com/VisDrone/DroneVehicle) · [Paper](https://arxiv.org/abs/2003.02437) |
| **SDD (Stanford Drone Dataset)** | 2016 | Det, MOT, Pred | RGB, Video | Top-down aerial video of a university campus with dense pedestrian and vehicle trajectory annotations for detection, tracking, and behavior prediction | Open · [Dataset](https://cvgl.stanford.edu/projects/uav_data/) · [Paper](https://cvgl.stanford.edu/papers/eccv16_robicquet.pdf) |
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

## 7. Thermal and Multimodal Perception

| Dataset | Year | Task tags | Modality | Focus | Access and resources |
|---|---:|---|---|---|---|
| **HiAI** | 2025 | SOT | RGB-T, Video | High-altitude RGB-infrared UAV tracking with 150 aligned video pairs across diverse scenes | Check · High-altitude infrared-visible tracking benchmark |
| **RTDOD** | 2023 | Det | RGB-T | Large-scale RGB-thermal domain-incremental object detection from UAV perspective | Open · [Dataset/code](https://github.com/fenght96/RTDOD) · [Paper](https://www.sciencedirect.com/science/article/pii/S0262885623002097) |
| **DroneRGBT** | 2020 | Count | RGB-T | RGB-thermal cross-modal crowd counting from drone viewpoint with 3,600 aligned image pairs | Open · [Dataset/code](https://github.com/VisDrone/DroneRGBT) |
| **Salient Map Thermal Dataset** | 2020 | Det, Salient object detection | RGB-T | 2,975 annotated day/night RGB-thermal images for salient object detection and feature enhancement | Check · Google Drive dataset for UAV thermal saliency |
| **ASL-TID** | 2014 | SOT, MOT | TIR | Early airborne thermal-infrared benchmark with person and vehicle annotations from a moving aerial platform | Open · [Dataset](https://projects.asl.ethz.ch/datasets/doku.php?id=ir_dataset) |

## 8. Multi-Drone Collaborative Perception

| Dataset | Year | Task tags | Modality | Focus | Access and resources |
|---|---:|---|---|---|---|
| **UAV3D** | 2024 | 3DDet, MOT | Syn | Large-scale 3D object detection and tracking benchmark for single and multi-UAV cooperative perception | Open · [Dataset/code](https://github.com/huiyegit/UAV3D) · NeurIPS 2024 |
| **Air-Co-Pred / AirCopBench** | 2023 | Pred | Syn | Multi-UAV cooperative trajectory prediction benchmark | Check · Embodied City benchmark for cooperative perception and prediction |
| **MAVREC** | 2023 | Cls | RGB, Video | Multi-view aerial recognition combining drone and ground camera videos with over 500K frames and 1.1M bounding boxes | Check · Multi-view (drone + ground) recognition dataset |
| **CoPerception-UAVs** | 2022 | Det, 3DDet | Syn | Five-UAV collaborative perception benchmark supporting 2D/3D detection and BEV segmentation | Open · [Dataset/code](https://siheng-chen.github.io/dataset/coperception-uav/) |
| **MDMT** | 2022 | MOT | RGB, Video | Dual-drone multi-object tracking with 88 synchronized dual-view videos addressing cross-view occlusion | Open · [Dataset/code](https://github.com/VisDrone/Multi-Drone-Multi-Object-Detection-and-Tracking) |
| **MDOT** | 2020 | SOT | RGB, Video | First multi-drone single-object tracking dataset with dual/triple-UAV cooperative scenarios across 10 scene attributes | Check · Multi-drone collaborative tracking benchmark |

## 9. Embodied AI and Vision-Language Navigation

| Dataset | Year | Task tags | Modality | Focus | Access and resources |
|---|---:|---|---|---|---|
| **AeroVerse** | 2024 | VLN, VQA, Multi-task | Syn | UAV embodied agent benchmark suite with large-scale first-person aerial pre-training data and five downstream tasks | Open · [Paper](https://arxiv.org/abs/2408.15511) · Embodied aerospace world models |
| **CityNav** | 2024 | VLN | Syn | City-scale language-guided UAV navigation with 32,000+ natural-language instructions and human demonstration trajectories over real city 3D point clouds | Open · [Dataset/code](https://water-cookie.github.io/city-nav-proj/) · [Paper](https://arxiv.org/abs/2406.14240) |
| **OpenUAV** | 2024 | VLN | Syn | Photorealistic UAV vision-language navigation platform with 6-DoF flight dynamics and 12,000 trajectory-instruction pairs | Check · Photorealistic VLN simulation platform |
| **UAV-VisLoc** | 2024 | Loc | RGB, Meta | Large-scale UAV visual localization across 11 Chinese locations with 6,742 UAV images matched to satellite maps for GNSS-denied geo-localization | Open · [Dataset/code](https://github.com/intellisensing/uav-visloc) · [Paper](https://arxiv.org/abs/2405.11936) |
| **AerialVLN** | 2023 | VLN | Syn | First UAV vision-language navigation benchmark built in UE4 with 25 city scenes and 8,446 annotated paths and instructions | Open · [Dataset/code](https://github.com/AirVLN/AirVLN) · [Paper](https://openaccess.thecvf.com/content/ICCV2023/papers/Liu_AerialVLN_Vision-and-Language_Navigation_for_UAVs_ICCV_2023_paper.pdf) |
| **UrbanBIS** | 2023 | SemSeg, InstSeg, 3D | RGB, Point cloud | Large-scale urban building instance segmentation from real UAV oblique photography covering 6 cities with 2.5 billion points | Open · [Dataset](https://vcc.tech/UrbanBIS) · [Paper](https://arxiv.org/abs/2305.02627) |
| **AVDN** | 2022 | VLN, Dialog | Syn | Aerial vision-and-dialog navigation with 3,064 trajectories and multi-turn interactions | Check · CMU dialog-based aerial navigation dataset |

## 10. General-Purpose Aerial Perception

| Dataset | Year | Task tags | Modality | Focus | Access and resources |
|---|---:|---|---|---|---|
| **VisDrone** | 2018– | Det, SOT, MOT, crowd counting | RGB, Video | Diverse pedestrians and vehicles in urban and rural scenes | Open · [Dataset](https://github.com/VisDrone/VisDrone-Dataset) · [Paper](https://doi.org/10.1109/TPAMI.2021.3119563) |
| **UAV123 / UAV20L** | 2016 | SOT | RGB, Video | People, vehicles, boats, and other moving targets | Open · [Project](https://cemse.kaust.edu.sa/ivul/uav123) · [Paper](https://arxiv.org/abs/1605.07109) |

## 11. Synthetic and Simulated Data

| Dataset / tool | Year | Task tags | Modality | Focus | Access and resources |
|---|---:|---|---|---|---|
| **UEMM-Air** | 2024 | Det, Seg, Retrieval | Syn | Synthetic multi-modal UAV dataset built with UE+AirSim providing six paired modalities (120K+ sequences) for detection, segmentation, and cross-modal understanding | Open · [Dataset/code](https://github.com/1e12Leon/UEMM-Air) · [Paper](https://arxiv.org/abs/2406.06230) |
| **SkyScenes** | 2024 | SemSeg, Det, Depth | Syn | City-scale synthetic aerial/UAV multi-modal perception dataset | Check · Synthetic urban aerial perception benchmark |
| **SynDrone** | 2023 | SemSeg | Syn | Multi-modal (RGB, depth, LiDAR) synthetic UAV dataset with 72,000 frames for urban scene understanding | Check · Unreal Engine synthetic multi-modal UAV data |
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
