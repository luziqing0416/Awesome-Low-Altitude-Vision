# Awesome Low-Altitude Vision

> A curated list of datasets, research papers, tools, and resources for low-altitude UAV vision.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![License: CC0-1.0](https://img.shields.io/badge/License-CC0--1.0-lightgrey.svg)](LICENSE) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

This repository covers low-altitude onboard aerial perception. Cameras or sensors may be carried by UAVs, helicopters, or other low-altitude aircraft and should observe people, objects, infrastructure, terrain, or water below/around the platform. Datasets in which UAVs themselves are the detection or tracking targets—such as anti-UAV surveillance recorded from the ground or another external platform—are excluded.

Low-altitude UAV vision differs from satellite and ground-level vision in viewpoint, target scale, camera motion, background, and operational constraints. This list prioritizes search and rescue, disaster monitoring, and infrastructure inspection while retaining other domains that may offer transferable insights.

**English** | [简体中文](README_zh-CN.md)

## Contents

- [Datasets](#datasets): [SAR](#1-search-and-rescue) · [Disaster](#2-disaster-monitoring-and-assessment) · [Inspection](#3-infrastructure-inspection) · [Human](#4-human-and-crowd-understanding) · [Transportation](#5-transportation-and-urban-monitoring) · [Agriculture & Ecology](#6-agriculture-forestry-and-ecological-monitoring) · [Thermal & Multimodal](#7-thermal-and-multimodal-perception) · [Multi-Drone](#8-multi-drone-collaborative-perception) · [Embodied AI & VLN](#9-embodied-ai-and-vision-language-navigation) · [General Benchmarks](#10-general-uav-vision-benchmarks) · [Synthetic](#11-synthetic-uav-datasets)
- [Research Papers](#research-papers)
- [Tools and Resources](#tools-and-resources)

## Datasets

The **Scale** column reports released images, annotated frames, or videos when verifiable. Counts may differ across versions and benchmark tracks.

### 1. Search and Rescue

| Dataset | Year | Source | Tasks | Scale | Main subjects / scenes | Resources |
|---|---:|---|---|---|---|---|
| **NOMAD** | 2023 | Staged real UAV | Detection | 42,825 frames; 100 actors | Occluded people at five aerial distances | [Data](https://github.com/ArtRuss/NOMAD) · [Paper](https://arxiv.org/abs/2309.09518) |
| **SeaDronesSee** | 2022 | Staged/real UAV | Detection, SOT, MOT | 54,000+ frames; 400,000+ instances | Swimmers, boats, jet skis, rescue appliances, buoys | [Site](https://seadronessee.cs.uni-tuebingen.de/) · [Data](https://seadronessee.cs.uni-tuebingen.de/dataset) · [Paper](https://openaccess.thecvf.com/content/WACV2022/html/Varga_SeaDronesSee_A_Maritime_Benchmark_for_Detecting_Humans_in_Open_Water_WACV_2022_paper.html) |
| **HERIDAL** | 2019 | Real/staged UAV | Detection | 1,600+ images; 68,750+ derived patches | People in wilderness and Mediterranean landscapes | [Paper](https://doi.org/10.1007/s11263-019-01177-1) |
| **Post-Disaster Survivor** | — | Real UAV | Detection | 879 images | Survivors in post-disaster ruins | [Data](https://github.com/HaoqianSong/Post-Disaster-Dataset) |

### 2. Disaster Monitoring and Assessment

| Dataset | Year | Source | Tasks | Scale | Main subjects / scenes | Resources |
|---|---:|---|---|---|---|---|
| **LADI** | 2023 | Real low-altitude aircraft/UAV | Multi-label disaster classification | — | Oblique disaster-response imagery collected during events from 2015–2023 | [Data](https://registry.opendata.aws/ladi/) · [Overview](https://github.com/ladi-dataset/ladi-overview) |
| **RescueNet** | 2023 | Real UAV | Classification, segmentation, VQA | 4,494 images | Damage, blocked roads, debris, water, vehicles | [Data](https://github.com/BinaLab/RescueNet-A-High-Resolution-Post-Disaster-UAV-Dataset-for-Semantic-Segmentation) · [Paper](https://www.nature.com/articles/s41597-023-02799-4) |
| **FloodNet** | 2021 | Real UAV | Classification, segmentation, VQA | 2,343 images | Flooded/non-flooded infrastructure | [Data](https://github.com/BinaLab/FloodNet-Supervised_v1.0) · [Paper](https://arxiv.org/abs/2105.08655) |
| **FLAME** | 2021 | Real UAV | Classification, segmentation | 47,992 labeled frames; 2,003 masks | Fire classification and pile-burn segmentation | [Project](https://github.com/AlirezaShamsoshoara/Fire-Detection-UAV-Aerial-Image-Classification-Segmentation-UnmannedAerialVehicle) · [Data](https://doi.org/10.21227/7rk7-ey09) |
| **FIReStereo** | 2024 | Real UAV | Depth perception, detection | 204,594 stereo IR pairs | Fire and smoke scenes with binocular thermal-infrared and RGB for emergency response | Check · CMU fire-scene UAV stereo dataset |
| **HazyDet** | 2024 | Real UAV + synthetic haze | Detection | See release | Drone-view object detection across multiple haze concentrations with depth cues | [Data/code](https://github.com/GrokCV/HazyDet) · [Paper](https://arxiv.org/abs/2409.19833) |
| **UAV-AWID** | 2024 | Real UAV | Detection | See release | Adverse weather and image degradation (rain, motion blur, noise) at multiple severity levels | [Data/code](https://github.com/AdnanMunir338/UAV-AWID) |

### 3. Infrastructure Inspection

| Dataset | Year | Source | Tasks | Scale | Main subjects | Resources |
|---|---:|---|---|---|---|---|
| **InsPLAD** | 2023 | Real UAV inspection | Detection, defect classification, anomaly detection | 10,607 Full-HD images; 28,933 asset instances | 17 power-line asset types and six defect types | [Project/data](https://andreluizbvs.github.io/InsPLAD/) · [Code](https://github.com/andreluizbvs/InsPLAD) · [Paper](https://arxiv.org/abs/2311.01619) |
| **PLD-UAV (PLDU/PLDM)** | 2022 | Real UAV | Power-line segmentation | 11,210 images; 240,553 labeled line objects | Urban and mountain power lines with pixel-level masks | [Data/code](https://github.com/SnorkerHeng/PLD-UAV) |
| **PTL-AI Furnas** | 2022 | Real inspection | Classification, fault recognition | 6,295 images | Power-line components and faults | [Data](https://github.com/freds0/PTL-AI_Furnas_Dataset) · [Paper](https://ieeexplore.ieee.org/document/9991806) |
| **STN PLAD** | 2021 | Real UAV | Detection | 2,409 annotated objects | Towers, insulators, spacers, plates, and Stockbridge dampers | [Data/code](https://github.com/andreluizbvs/PLAD) · [Paper](https://doi.org/10.1109/SIBGRAPI54419.2021.00037) |
| **TTPLA** | 2020 | Real aerial | Detection, semantic/instance segmentation | 1,100 original 4K images; 8,987 instances | Transmission towers and power lines | [Data](https://github.com/r3ab/ttpla_dataset) · [Paper](https://openaccess.thecvf.com/content/ACCV2020/html/Abdelfattah_TTPLA_An_Aerial-Image_Dataset_for_Detection_and_Segmentation_of_Transmission_ACCV_2020_paper.html) |

### 4. Human and Crowd Understanding

| Dataset | Year | Source | Tasks | Scale | Main subjects / scenes | Resources |
|---|---:|---|---|---|---|---|
| **HIT-UAV** | 2023 | Real UAV | Thermal person/vehicle detection | 2,898 thermal images; 24,899 instances | People and vehicles with altitude, view-angle, and daylight metadata | [Data/code](https://github.com/suojiashun/HIT-UAV-Infrared-Thermal-Dataset) |
| **Manipal UAV Person** | 2023 | Real UAV | Detection | 33 videos; 13,462 images; 153,112 instances | Small persons under varied scale, pose, weather, and lighting | [Data](https://github.com/Akshathakrbhat/Manipal-UAV-Person-Dataset) · [Paper](https://doi.org/10.1016/j.isprsjprs.2022.11.022) |
| **UAV-Human** | 2021 | Real UAV | Action recognition, pose, ReID, attribute recognition | 67,428 video clips; 119 subjects | Multimodal human behavior across locations, views, and illumination | [Data/code](https://github.com/SUTDCV/UAV-Human) · [Paper](https://openaccess.thecvf.com/content/CVPR2021/html/Li_UAV-Human_A_Large_Benchmark_for_Human_Behavior_Understanding_With_Unmanned_Aerial_CVPR_2021_paper.html) |
| **DroneCrowd** | 2020 | Real UAV | Crowd counting | 112 video clips; 33,600 frames; 4.8M head annotations | Dense crowds across multiple locations and weather conditions | [Data/code](https://github.com/VisDrone/DroneCrowd) |
| **Okutama-Action** | 2017 | Real UAV | Detection, action recognition | 43 min; 12 videos; 77,365 frames | Concurrent outdoor human actions | [Data](https://okutama-action.org/) · [Paper](https://openaccess.thecvf.com/content_cvpr_2017_workshops/w24/html/Barekatain_Okutama-Action_An_Aerial_CVPR_2017_paper.html) |

### 5. Transportation and Urban Monitoring

| Dataset | Year | Tasks | Scale | Main subjects / scenes | Resources |
|---|---:|---|---|---|---|
| **MiTra** | 2025 | Detection, tracking, trajectory analysis | Raw drone video + stitched trajectories; see release | Mixed traffic and lane-change behavior | [Paper/data](https://www.nature.com/articles/s41597-025-05472-0) |
| **DRIFT** | 2025 | Multi-camera traffic analysis | Synchronized videos over nine intersections; see release | Network-level traffic trajectories at about 250 m altitude | [Paper](https://arxiv.org/abs/2504.11019) |
| **UTUAV** | 2025 | Vehicle detection | — | Medellín urban traffic with a high proportion of motorcycles | [Paper](https://www.mdpi.com/2504-446X/10/1/15) |
| **VDD (Varied Drone Dataset)** | 2025 | Semantic segmentation | 400 pixel-level annotated high-resolution images | Urban, industrial, rural, and natural scenes with 7 semantic classes across varied camera angles and lighting | [Data/code](https://github.com/RussRobin/VDD) · [Paper](https://arxiv.org/abs/2305.13608) |
| **AU-AIR** | 2020 | Detection | 32,823 frames; 132,034 instances | Urban traffic + flight metadata | [Data](https://bozcani.github.io/auairdataset) · [Paper](https://doi.org/10.1109/ICRA40945.2020.9197293) |
| **DroneVehicle** | 2020 | RGB–thermal detection | 56,878 images (28,439 pairs) | Vehicles with oriented boxes | [Data](https://github.com/VisDrone/DroneVehicle) · [Paper](https://arxiv.org/abs/2003.02437) |
| **SDD (Stanford Drone Dataset)** | 2016 | Detection, tracking, trajectory prediction | Top-down campus video; see release | Dense pedestrian and vehicle trajectories in a university campus | [Data](https://cvgl.stanford.edu/projects/uav_data/) · [Paper](https://cvgl.stanford.edu/papers/eccv16_robicquet.pdf) |
| **UAVDT** | 2018 | Detection, SOT, MOT | 100 sequences; ~80,000 frames; 800,000+ boxes | Vehicles under varied altitude, view, weather, lighting | [Archive](https://zenodo.org/records/14575517) · [Paper](https://openaccess.thecvf.com/content_ECCV_2018/html/Dawei_Du_The_Unmanned_Aerial_ECCV_2018_paper.html) |
| **UAVid** | 2018 | Semantic segmentation | 30 sequences; 300 annotated frames | Roads, buildings, vegetation, vehicles, people | [Data](https://uavid.nl/) · [Paper](https://arxiv.org/abs/1810.10438) |

### 6. Agriculture, Forestry, and Ecological Monitoring

| Dataset | Year | Source | Tasks | Scale | Main subjects / scenes | Resources |
|---|---:|---|---|---|---|---|
| **WildlifeMapper Dataset** | 2024 | Low-altitude aerial/UAV | Multi-species detection and identification | 11,000 images; 28,000 annotations | African mammals and multi-species aerial surveys | [Data/code](https://github.com/UCSB-VRL/WildlifeMapper) |
| **WAID** | 2023 | Real UAV | Wildlife detection | 14,375 images | Six wildlife species across varied habitats and conditions | [Data/code](https://github.com/xiaohuicui/WAID) · [Paper](https://www.mdpi.com/2076-3417/13/18/10397) |
| **CART** | 2024 | Real UAV | RGB–thermal field robotics | Multiple synchronized flight sequences; see release | Rivers, lakes, coasts, deserts, forests | [Data](https://data.caltech.edu/records/cks6g-ps927) · [Code](https://github.com/aerorobotics/caltech-aerial-rgbt-dataset) · [Paper](https://arxiv.org/abs/2403.08997) |
| **BIRDSAI** | 2020 | Real + synthetic | Detection, SOT, MOT | 48 real + 124 synthetic videos | Humans and animals in protected areas | [Data](https://sites.google.com/view/elizabethbondi/dataset) · [Paper](https://openaccess.thecvf.com/content_WACV_2020/html/Bondi_BIRDSAI_A_Dataset_for_Detection_and_Tracking_in_Aerial_Thermal_Infrared_WACV_2020_paper.html) |

### 7. Thermal and Multimodal Perception

| Dataset | Year | Source | Tasks | Scale | Main subjects / scenes | Resources |
|---|---:|---|---|---|---|---|
| **HiAI** | 2025 | Real high-altitude UAV | RGB–T tracking | 150 aligned RGB-IR video pairs | Diverse scenes for high-altitude infrared-visible UAV tracking | Check · High-altitude RGB-infrared tracking benchmark |
| **RTDOD** | 2023 | Real UAV | RGB–thermal domain-incremental detection | See release | UAV-view ground objects under domain-incremental settings | [Data/code](https://github.com/fenght96/RTDOD) · [Paper](https://www.sciencedirect.com/science/article/pii/S0262885623002097) |
| **DroneRGBT** | 2020 | Real UAV | RGB–T crowd counting | 3,600 aligned RGB-thermal pairs | Crowd counting from drone perspective across modalities | [Data/code](https://github.com/VisDrone/DroneRGBT) |
| **Salient Map Thermal Dataset** | 2020 | Real UAV | Thermal salient object detection | 2,975 annotated images | Day/night urban scenes for UAV thermal saliency | Check · Google Drive dataset for thermal saliency |
| **ASL-TID** | 2014 | Airborne (helicopter/UAV) | Thermal tracking | See release | People and vehicles from a moving airborne thermal-infrared camera | [Data](https://projects.asl.ethz.ch/datasets/doku.php?id=ir_dataset) |

### 8. Multi-Drone Collaborative Perception

| Dataset | Year | Source | Tasks | Scale | Main subjects / scenes | Resources |
|---|---:|---|---|---|---|---|
| **UAV3D** | 2024 | Synthetic (Carla) | 3D detection, tracking | Large-scale benchmark | 3D object detection and tracking for single and multi-UAV cooperation | [Data/code](https://github.com/huiyegit/UAV3D) · NeurIPS 2024 |
| **Air-Co-Pred / AirCopBench** | 2023 | Synthetic | Cooperative trajectory prediction | See release | Multi-UAV cooperative perception and trajectory prediction | Check · Embodied City benchmark |
| **MAVREC** | 2023 | Real UAV + ground | Recognition | 500K+ frames; 1.1M boxes | Multi-view aerial recognition combining drone and ground cameras | Check · Multi-view recognition dataset |
| **CoPerception-UAVs** | 2022 | Synthetic | Collaborative 2D/3D detection | 5 UAVs; see release | Collaborative perception supporting 2D/3D detection and BEV segmentation | [Project](https://siheng-chen.github.io/dataset/coperception-uav/) |
| **MDMT** | 2022 | Real UAV | Multi-drone MOT | 88 dual-view videos; 39,678 frames | Pedestrians, bicycles, and vehicles from synchronized dual-drone viewpoints | [Data/code](https://github.com/VisDrone/Multi-Drone-Multi-Object-Detection-and-Tracking) |
| **MDOT** | 2020 | Real UAV | Multi-drone SOT | See release | First multi-drone single-object tracking benchmark across 10 attributes | Check · Multi-drone collaborative tracking |

### 9. Embodied AI and Vision-Language Navigation

| Dataset | Year | Source | Tasks | Scale | Main subjects / scenes | Resources |
|---|---:|---|---|---|---|---|
| **AeroVerse** | 2024 | Synthetic | VLN, VQA, multi-task | Large-scale benchmark | UAV embodied agent benchmark suite with first-person aerial data across five tasks | [Paper](https://arxiv.org/abs/2408.15511) |
| **CityNav** | 2024 | Synthetic (real-city 3D) | VLN | 32,000+ instructions | Language-guided UAV navigation over real city 3D point clouds with human demonstrations | [Project](https://water-cookie.github.io/city-nav-proj/) · [Paper](https://arxiv.org/abs/2406.14240) |
| **OpenUAV** | 2024 | Synthetic | VLN | 12,000 trajectory-instruction pairs | Photorealistic UAV VLN with 6-DoF flight dynamics | Check · Photorealistic VLN platform |
| **UAV-VisLoc** | 2024 | Real UAV + satellite | Visual localization | 6,742 UAV images; 11 locations | Cross-view UAV-to-satellite geo-localization in GNSS-denied environments | [Data/code](https://github.com/intellisensing/uav-visloc) · [Paper](https://arxiv.org/abs/2405.11936) |
| **AerialVLN** | 2023 | Synthetic (UE4) | VLN | 8,446 paths; 25 city scenes | First UAV vision-language navigation benchmark | [Data/code](https://github.com/AirVLN/AirVLN) · [Paper](https://openaccess.thecvf.com/content/ICCV2023/papers/Liu_AerialVLN_Vision-and-Language_Navigation_for_UAVs_ICCV_2023_paper.pdf) |
| **UrbanBIS** | 2023 | Real UAV oblique photography | 3D semantic/instance segmentation | 2.5 billion points; 6 cities | Large-scale urban building instance segmentation from UAV oblique imagery | [Project](https://vcc.tech/UrbanBIS) · [Paper](https://arxiv.org/abs/2305.02627) |
| **AVDN** | 2022 | Synthetic (AirSim) | Vision-and-dialog navigation | 3,064 trajectories | Dialog-based aerial vision-language navigation with multi-turn interactions | Check · CMU aerial dialog navigation dataset |

### 10. General UAV Vision Benchmarks

| Dataset | Year | Tasks | Scale | Main subjects / scenes | Resources |
|---|---:|---|---|---|---|
| **CODrone** | 2025 | Oriented object detection | — | Multi-scene UAV imagery designed for cross-domain robustness and practical OOD | [Data/code](https://github.com/AHideoKuzeA/CODrone-A-Comprehensive-Oriented-Object-Detection-benchmark-for-UAV) · [Paper](https://arxiv.org/abs/2504.20032) |
| **WildUAV** | 2022 | Monocular depth estimation | 1,500+ high-resolution RGB images with reference depth and pose | Nadir and oblique outdoor aerial scenes | [Data/code](https://github.com/hrflr/wuav) · [Paper](https://doi.org/10.1109/LRA.2022.3154489) |
| **UAVBench + UAVIT-1M (NWPU)** | 2026 | MLLM evaluation and instruction tuning | UAVBench: 966K samples / 43 test units; UAVIT-1M: 1.24M instructions over 789K real images | Image/region classification and captioning, VQA, detection, grounding, and other low-altitude vision-language tasks | [Project](https://uavbench.github.io/) · [Data](https://huggingface.co/datasets/ZhanYang-nwpu/UAVBench) · [Paper](https://arxiv.org/abs/2603.14336) |
| **SpatialSky-Bench / SpatialSky-Dataset** | 2025 | VLM spatial reasoning and UAV navigation | SpatialSky-Dataset: 1M annotated samples; 13 benchmark subcategories | Environmental perception, distance/height, bounding boxes, landing safety, and scene understanding | [Code/data](https://github.com/linglingxiansen/SpatialSKy) · [Paper](https://arxiv.org/abs/2511.13269) |
| **MM-UAVBench** | 2025 | MLLM perception, cognition, and planning | 1,549 video clips + 2,873 images; 19 tasks | Object/scene/event understanding and aerial/ground-agent planning | [Code/data](https://github.com/AI9Stars/MM-UAVBench) |
| **VisDrone** | 2018 | Detection, tracking, crowd counting | 10,209 images; 288 clips / 261,908 frames; 2.6M+ boxes | People and vehicles in urban/rural scenes | [Data](https://github.com/VisDrone/VisDrone-Dataset) · [Paper](https://doi.org/10.1109/TPAMI.2021.3119563) |
| **UAV123 / UAV20L** | 2016 | SOT | 123 sequences; 110,000+ frames | People, vehicles, boats, other targets | [Project](https://cemse.kaust.edu.sa/ivul/uav123) · [Paper](https://arxiv.org/abs/1605.07109) |

### 11. Synthetic UAV Datasets

A cross-cutting index: synthetic datasets may also appear under their primary application category.

| Dataset | Year | Generation/source | Application | Scale | Intended use | Resources |
|---|---:|---|---|---|---|---|
| **UEMM-Air** | 2024 | UE+AirSim synthetic | Multi-modal perception | 120K+ sequences; six paired modalities | Detection, segmentation, retrieval, and cross-modal understanding | [Data/code](https://github.com/1e12Leon/UEMM-Air) · [Paper](https://arxiv.org/abs/2406.06230) |
| **SkyScenes** | 2024 | Synthetic | City-scale perception | See release | Urban aerial multi-modal perception and segmentation | Check · Synthetic city-scale aerial benchmark |
| **SynDrone** | 2023 | Unreal Engine synthetic | Urban scene understanding | 72,000 frames; multi-modal | Multi-modal (RGB, depth, LiDAR) urban UAV segmentation | Check · UE synthetic multi-modal data |
| **UAVBench (UAEU/Khalifa)** | 2025 | LLM-generated structured flight scenarios and MCQs | Agentic UAV reasoning | 50,000 validated JSON scenarios + 50,000 multiple-choice questions | Mission planning, risk, navigation, ethics, resource constraints, and multi-agent reasoning; text/structured data rather than a vision dataset | [Data/code](https://github.com/maferrag/UAVBench) · [Paper](https://arxiv.org/abs/2511.11252) |
| **C2A** | 2024 | Composited humans + disaster backgrounds | SAR | 10,215 images; 360,000+ instances | Disaster human detection and pose diversity | [Data/code](https://github.com/Ragib-Amin-Nihal/C2A) · [Paper](https://arxiv.org/abs/2408.04922) |
| **Synthetic SeaDronesSee** | — | Pre-generated maritime synthetic data produced with a generation tool | SAR | — | Downloadable synthetic training data for maritime detection, augmentation, and sim-to-real research | [Official release](https://seadronessee.cs.uni-tuebingen.de/dataset) |
| **BIRDSAI Synthetic** | 2020 | AirSim-W thermal simulation | Ecology | 124 videos | Thermal detection/tracking and domain adaptation | [Data](https://sites.google.com/view/elizabethbondi/dataset) · [Paper](https://openaccess.thecvf.com/content_WACV_2020/html/Bondi_BIRDSAI_A_Dataset_for_Detection_and_Tracking_in_Aerial_Thermal_Infrared_WACV_2020_paper.html) |
| **VictimDet composites** | 2022 | Pre-generated composites produced by a harmonization pipeline | SAR | 1,936 images (512×512) with body-part boxes | Fine-tuning disaster-victim detectors; downloadable data and code support reproduction or extension | [Data/code](https://github.com/noahzn/VictimDet) |

## Research Papers

Dataset-introduction papers are linked in the tables above. This section is reserved for method, system, survey, and comparative research.

### 1. UAV Visual Perception

Detection, tracking, video understanding, segmentation, action recognition, and small-object perception.

| Year | Paper | Venue | Tags | Resources |
|---:|---|---|---|---|
| 2026 | Visual Prototype Conditioned Focal Region Generation for UAV-Based Object Detection | CVPR | Detection, tiny objects, focal regions | [Paper](https://openaccess.thecvf.com/content/CVPR2026/html/Li_Visual_Prototype_Conditioned_Focal_Region_Generation_for_UAV-Based_Object_Detection_CVPR_2026_paper.html) |
| 2026 | Toward Low-Cost yet Effective Temporal Learning for UAV Tracking | CVPR | Tracking, temporal learning, efficiency | [Paper](https://openaccess.thecvf.com/content/CVPR2026/html/Xue_Toward_Low-Cost_yet_Effective_Temporal_Learning_for_UAV_Tracking_CVPR_2026_paper.html) |
| 2026 | Rethinking Occlusion Modeling for UAV Tracking | CVPR | Tracking, occlusion, efficient transformers | [Paper](https://openaccess.thecvf.com/content/CVPR2026/html/Zhang_Rethinking_Occlusion_Modeling_for_UAV_Tracking_CVPR_2026_paper.html) |
| 2025 | PointSR: Self-Regularized Point Supervision for Drone-View Object Detection | CVPR | Detection, point supervision, pseudo boxes | [Paper](https://openaccess.thecvf.com/content/CVPR2025/html/Li_PointSR_Self-Regularized_Point_Supervision_for_Drone-View_Object_Detection_CVPR_2025_paper.html) |
| 2025 | Learning Occlusion-Robust Vision Transformers for Real-Time UAV Tracking | CVPR | Tracking, occlusion, real time | [Paper](https://openaccess.thecvf.com/content/CVPR2025/html/Wu_Learning_Occlusion-Robust_Vision_Transformers_for_Real-Time_UAV_Tracking_CVPR_2025_paper.html) |
| 2025 | Similarity-Guided Layer-Adaptive Vision Transformer for UAV Tracking | CVPR | Tracking, lightweight ViT | [Paper](https://openaccess.thecvf.com/content/CVPR2025/html/Xue_Similarity-Guided_Layer-Adaptive_Vision_Transformer_for_UAV_Tracking_CVPR_2025_paper.html) |
| 2024 | HazyDet: Open-Source Benchmark for Drone-View Object Detection with Depth-Cues in Hazy Scenes | arXiv | Detection, haze, adverse weather | [Paper](https://arxiv.org/abs/2409.19833) · [Code](https://github.com/GrokCV/HazyDet) |
| 2023 | Adaptive Sparse Convolutional Networks with Global Context Enhancement for Faster Object Detection on Drone Images | CVPR | Detection, sparse convolution, onboard efficiency | [Paper](https://openaccess.thecvf.com/content/CVPR2023/html/Du_Adaptive_Sparse_Convolutional_Networks_With_Global_Context_Enhancement_for_Faster_CVPR_2023_paper.html) |
| 2019 | Delving into Robust Object Detection from Unmanned Aerial Vehicles: A Deep Nuisance Disentanglement Approach | ICCV | Detection, robustness, nuisance disentanglement | [Paper](https://openaccess.thecvf.com/content_ICCV_2019/html/Wu_Delving_Into_Robust_Object_Detection_From_Unmanned_Aerial_Vehicles_A_ICCV_2019_paper.html) |

### 2. Multimodal Learning and Generalization

Sensor/metadata fusion, cross-domain generalization, domain adaptation, and sim-to-real.

| Year | Paper | Venue | Tags | Resources |
|---:|---|---|---|---|
| 2025 | MUST: The First Dataset and Unified Framework for Multispectral UAV Single Object Tracking | CVPR | RGB-T, tracking, multimodal fusion | [Paper](https://openaccess.thecvf.com/content/CVPR2025/html/Qin_MUST_The_First_Dataset_and_Unified_Framework_for_Multispectral_UAV_CVPR_2025_paper.html) |
| 2025 | UAVScenes: A Multi-Modal Dataset for UAVs | ICCV | Camera, LiDAR, multimodal perception | [Paper](https://openaccess.thecvf.com/content/ICCV2025/html/Wang_UAVScenes_A_Multi-Modal_Dataset_for_UAVs_ICCV_2025_paper.html) |

### 3. Synthetic Data and Data-Centric Learning

Simulation, generation, augmentation, annotation, filtering, and quality evaluation.

| Year | Paper | Venue | Tags | Resources |
|---:|---|---|---|---|
| 2026 | AirSim360: A Panoramic Simulation Platform within Drone View | CVPR | Simulation, panoramic UAV view, closed loop | [Paper](https://openaccess.thecvf.com/content/CVPR2026/html/Ge_AirSim360_A_Panoramic_Simulation_Platform_within_Drone_View_CVPR_2026_paper.html) |

### 4. Vision-Language Models, Agents, and Surveys

VLM-assisted annotation, prompt/scene planning, agentic loops, vision-language navigation, surveys, and comparative benchmarks.

| Year | Paper | Venue | Tags | Resources |
|---:|---|---|---|---|
| 2025 | Where Does It Exist from the Low-Altitude: Spatial Aerial Video Grounding | NeurIPS | Vision-language grounding, aerial video, small objects | [Paper](https://proceedings.neurips.cc/paper_files/paper/2025/hash/76c5401551bbe8337dc38a2bd5eb394e-Abstract-Conference.html) |
| 2025 | Embodied Crowd Counting | NeurIPS | Embodied perception, MLLM, active UAV observation | [Paper](https://proceedings.neurips.cc/paper_files/paper/2025/hash/6aa3267e3a0f7c2c718036d08d482a51-Abstract-Conference.html) |
| 2024 | Recent Advances for Aerial Object Detection: A Survey | ACM Computing Surveys | Survey, detection, aerial vision | [Paper](https://dl.acm.org/doi/10.1145/3664598) |
| 2023 | AerialVLN: Vision-and-Language Navigation for UAVs | ICCV | Vision-language navigation, UAV, embodied AI | [Paper](https://openaccess.thecvf.com/content/ICCV2023/papers/Liu_AerialVLN_Vision-and-Language_Navigation_for_UAVs_ICCV_2023_paper.pdf) · [Dataset](https://github.com/AirVLN/AirVLN) |
| 2024 | UAV3D: A Large-scale 3D Perception Benchmark for Unmanned Aerial Vehicles | NeurIPS | 3D perception, multi-UAV cooperation | [Code](https://github.com/huiyegit/UAV3D) |

### 5. Low-Altitude Application Systems

End-to-end SAR, disaster, inspection, traffic, agriculture/ecology, and onboard systems.

| Year | Paper | Venue | Tags | Resources |
|---:|---|---|---|---|
| 2026 | PiLoT: Neural Pixel-to-3D Registration for UAV-Based Ego and Target Geo-Localization | CVPR | Geo-localization, onboard deployment, synthetic-to-real | [Paper](https://openaccess.thecvf.com/content/CVPR2026/html/Cheng_PiLoT_Neural_Pixel-to-3D_Registration_for_UAV-Based_Ego_and_Target_Geo-localization_CVPR_2026_paper.html) |

## Tools and Resources

- **Simulators:** [AirSim](https://github.com/microsoft/AirSim) · [CARLA](https://github.com/carla-simulator/carla)
- **Related lists:** [Awesome VisDrone](https://github.com/VisDrone/Awesome-VisDrone) · [UAV-Vision](https://github.com/wangdongdut/UAV-Vision) · [Awesome Water Surface Perception](https://github.com/WaterScenes/Awesome-Water-Surface-Perception) · [Awesome Dataset Distillation](https://github.com/Guang000/Awesome-Dataset-Distillation)

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) or use the [resource suggestion template](https://github.com/luziqing0416/Awesome-Low-Altitude-Vision/issues/new?template=resource-suggestion.yml). This repository is an index and does not redistribute datasets or copyrighted papers.

## License

[CC0 1.0](LICENSE). Individual resources retain their original licenses.
