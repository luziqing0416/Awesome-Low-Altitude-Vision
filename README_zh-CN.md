# 低空视觉资源精选

> 面向低空无人机视觉的数据集、研究论文、工具与资源索引。

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![License: CC0-1.0](https://img.shields.io/badge/License-CC0--1.0-lightgrey.svg)](LICENSE) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

低空无人机视觉与卫星遥感和地面视觉在视角、目标尺度、相机运动、背景及任务约束等方面存在明显差异。本清单优先关注搜索救援、灾害监测与基础设施巡检，同时保留可能提供迁移借鉴的其他低空应用领域。

[English](README.md) | **简体中文**

## 目录

- [数据集](#数据集)：[搜索与救援](#1-搜索与救援) · [灾害监测与评估](#2-灾害监测与评估) · [基础设施巡检](#3-基础设施巡检) · [人员与人群理解](#4-人员与人群理解) · [交通与城市监测](#5-交通与城市监测) · [农业林业与生态监测](#6-农业林业与生态监测) · [通用基准](#7-通用无人机视觉基准) · [合成数据](#8-合成无人机数据集)
- [研究论文](#研究论文)
- [工具与资源](#工具与资源)

## 数据集

**数据规模**一栏记录能够核验的公开图像、标注帧或视频数量；不同版本和评测赛道的统计可能存在差异。

### 1. 搜索与救援

| 数据集 | 年份 | 数据来源 | 任务 | 数据规模 | 主要对象/场景 | 资源 |
|---|---:|---|---|---|---|---|
| **NOMAD** | 2023 | 真实无人机拍摄（人为构造） | 目标检测 | 42,825帧；100名参与者 | 五种航拍距离下受到遮挡的人员 | [数据](https://github.com/ArtRuss/NOMAD) · [论文](https://arxiv.org/abs/2309.09518) |
| **SeaDronesSee** | 2022 | 真实无人机拍摄（含构造场景） | 目标检测、单目标跟踪、多目标跟踪 | 超过54,000帧；超过400,000个实例 | 落水者、船只、摩托艇、救生设施和浮标 | [官网](https://seadronessee.cs.uni-tuebingen.de/) · [数据](https://seadronessee.cs.uni-tuebingen.de/dataset) · [论文](https://openaccess.thecvf.com/content/WACV2022/html/Varga_SeaDronesSee_A_Maritime_Benchmark_for_Detecting_Humans_in_Open_Water_WACV_2022_paper.html) |
| **HERIDAL** | 2019 | 真实无人机拍摄（含构造场景） | 目标检测 | 1,600余张图像；68,750余个派生图像块 | 荒野及地中海地貌中的人员 | [论文](https://doi.org/10.1007/s11263-019-01177-1) |
| **Post-Disaster Survivor** | — | 真实无人机 | 目标检测 | 879张图像 | 灾后废墟中的幸存者 | [数据](https://github.com/HaoqianSong/Post-Disaster-Dataset) |

### 2. 灾害监测与评估

| 数据集 | 年份 | 数据来源 | 任务 | 数据规模 | 主要对象/场景 | 资源 |
|---|---:|---|---|---|---|---|
| **RescueNet** | 2023 | 真实无人机 | 分类、语义分割、视觉问答 | 4,494张图像 | 建筑损毁、道路阻塞、废墟、水域和车辆 | [数据](https://github.com/BinaLab/RescueNet-A-High-Resolution-Post-Disaster-UAV-Dataset-for-Semantic-Segmentation) · [论文](https://www.nature.com/articles/s41597-023-02799-4) |
| **FloodNet** | 2021 | 真实无人机 | 分类、语义分割、视觉问答 | 2,343张图像 | 受淹与未受淹的道路、建筑等基础设施 | [数据](https://github.com/BinaLab/FloodNet-Supervised_v1.0) · [论文](https://arxiv.org/abs/2105.08655) |
| **FLAME** | 2021 | 真实无人机 | 分类、分割 | 47,992张标注帧；2,003张分割掩码 | 火灾分类与燃烧区域分割 | [项目](https://github.com/AlirezaShamsoshoara/Fire-目标检测-UAV-Aerial-Image-Classification-Segmentation-UnmannedAerialVehicle) · [数据](https://doi.org/10.21227/7rk7-ey09) |

### 3. 基础设施巡检

| 数据集 | 年份 | 数据来源 | 任务 | 数据规模 | 主要对象 | 资源 |
|---|---:|---|---|---|---|---|
| **PTL-AI Furnas** | 2022 | 真实巡检影像 | 分类、故障识别 | 6,295张图像 | 输电线路部件及故障 | [数据](https://github.com/freds0/PTL-AI_Furnas_Dataset) · [论文](https://ieeexplore.ieee.org/document/9991806) |
| **TTPLA** | 2020 | 真实航拍 | 目标检测, semantic/instance segmentation | 1,100张原始4K图像；8,987个标注实例 | 输电塔和电力线 | [数据](https://github.com/r3ab/ttpla_dataset) · [论文](https://openaccess.thecvf.com/content/ACCV2020/html/Abdelfattah_TTPLA_An_Aerial-Image_Dataset_for_目标检测_and_Segmentation_of_Transmission_ACCV_2020_paper.html) |

### 4. 人员与人群理解

| 数据集 | 年份 | 数据来源 | 任务 | 数据规模 | 主要对象/场景 | 资源 |
|---|---:|---|---|---|---|---|
| **Manipal UAV Person** | 2023 | 真实无人机 | 目标检测 | 33段视频；13,462张图像；153,112个人体实例 | 不同尺度、姿态、天气和光照条件下的小尺度人员 | [数据](https://github.com/Akshathakrbhat/Manipal-UAV-Person-Dataset) · [论文](https://doi.org/10.1016/j.isprsjprs.2022.11.022) |
| **Okutama-Action** | 2017 | 真实无人机 | 目标检测、动作识别 | 43分钟；12段视频；77,365张标注帧 | 室外场景中的多人并发动作 | [数据](https://okutama-action.org/) · [论文](https://openaccess.thecvf.com/content_cvpr_2017_workshops/w24/html/Barekatain_Okutama-Action_An_Aerial_CVPR_2017_paper.html) |

### 5. 交通与城市监测

| 数据集 | 年份 | 任务 | 数据规模 | 主要对象/场景 | 资源 |
|---|---:|---|---|---|---|
| **AU-AIR** | 2020 | 目标检测 | 32,823张标注帧；132,034个目标实例 | 城市交通参与者及飞行元数据 | [数据](https://bozcani.github.io/auairdataset) · [论文](https://doi.org/10.1109/ICRA40945.2020.9197293) |
| **DroneVehicle** | 2020 | RGB–热红外检测 | 56,878张图像（28,439对） | 采用旋转框标注的车辆 | [数据](https://github.com/VisDrone/DroneVehicle) · [论文](https://arxiv.org/abs/2003.02437) |
| **UAVDT** | 2018 | 目标检测、单目标跟踪、多目标跟踪 | 100段序列；约80,000帧；超过800,000个标注框 | 不同飞行高度、视角、天气和光照下的车辆 | [数据存档](https://zenodo.org/records/14575517) · [论文](https://openaccess.thecvf.com/content_ECCV_2018/html/Dawei_Du_The_Unmanned_Aerial_ECCV_2018_paper.html) |
| **UAVid** | 2018 | 语义分割 | 30段序列；300张精细标注帧 | 道路、建筑、植被、车辆和人员 | [数据](https://uavid.nl/) · [论文](https://arxiv.org/abs/1810.10438) |

### 6. 农业、林业与生态监测

| 数据集 | 年份 | 数据来源 | 任务 | 数据规模 | 主要对象/场景 | 资源 |
|---|---:|---|---|---|---|---|
| **CART** | 2024 | 真实无人机 | RGB–热红外低空机器人感知 | 多段同步飞行序列，详见发布页面 | 河流、湖泊、海岸、沙漠和森林 | [数据](https://data.caltech.edu/records/cks6g-ps927) · [代码](https://github.com/aerorobotics/caltech-aerial-rgbt-dataset) · [论文](https://arxiv.org/abs/2403.08997) |
| **BIRDSAI** | 2020 | 真实与合成混合 | 目标检测、单目标跟踪、多目标跟踪 | 48段真实视频＋124段合成视频 | 自然保护区中的人员与野生动物 | [数据](https://sites.google.com/view/elizabethbondi/dataset) · [论文](https://openaccess.thecvf.com/content_WACV_2020/html/Bondi_BIRDSAI_A_Dataset_for_目标检测_and_Tracking_in_Aerial_Thermal_Infrared_WACV_2020_paper.html) |

### 7. 通用无人机视觉基准

| 数据集 | 年份 | 任务 | 数据规模 | 主要对象/场景 | 资源 |
|---|---:|---|---|---|---|
| **VisDrone** | 2018– | 目标检测、目标跟踪、人群计数 | 10,209张图像；288段视频/261,908帧；超过260万个标注框 | 城乡场景中的人员和车辆 | [数据](https://github.com/VisDrone/VisDrone-Dataset) · [论文](https://doi.org/10.1109/TPAMI.2021.3119563) |
| **UAV123 / UAV20L** | 2016 | 单目标跟踪 | 123段序列；超过110,000帧 | 人员、车辆、船只等多类目标 | [项目](https://cemse.kaust.edu.sa/ivul/uav123) · [论文](https://arxiv.org/abs/1605.07109) |

### 8. 合成无人机数据集

本节作为横向索引使用：合成数据集可以同时出现在其主要应用类别中，便于读者分别按应用场景和数据来源查找。

| 数据集 | 年份 | 生成方式/来源 | 应用场景 | 数据规模 | 主要用途 | 资源 |
|---|---:|---|---|---|---|---|
| **C2A** | 2024 | 灾害背景与人体组合 | 搜索与救援 | 10,215张图像；超过360,000个人体实例 | 灾害场景人员检测与姿态多样性 | [数据/代码](https://github.com/Ragib-Amin-Nihal/C2A) · [论文](https://arxiv.org/abs/2408.04922) |
| **Synthetic SeaDronesSee** | — | 海上场景仿真/渲染 | 搜索与救援 | 随版本变化 | 目标检测, augmentation, sim-to-real | [官方发布](https://seadronessee.cs.uni-tuebingen.de/dataset) |
| **BIRDSAI Synthetic** | 2020 | AirSim-W热红外仿真 | 生态监测 | 124段合成视频 | 热红外检测、跟踪与域适配 | [数据](https://sites.google.com/view/elizabethbondi/dataset) · [论文](https://openaccess.thecvf.com/content_WACV_2020/html/Bondi_BIRDSAI_A_Dataset_for_目标检测_and_Tracking_in_Aerial_Thermal_Infrared_WACV_2020_paper.html) |
| **VictimDet composites** | 2022 | 和谐化受害者合成图像 | 搜索与救援 | 详见项目发布 | 用于训练灾害受害者检测器 | [数据/代码](https://github.com/noahzn/VictimDet) |

## 研究论文

数据集介绍论文已经放在对应的数据表格中。本节仅收录方法、系统、综述和综合比较研究，不重复列出数据集原始论文。

### 1. 无人机视觉感知

包括目标检测、目标跟踪、视频理解、语义与实例分割、动作识别和小目标感知。*论文待继续整理。*

### 2. 多模态学习与泛化

包括多传感器与元数据融合、跨域泛化、域适配和仿真到真实迁移。*论文待继续整理。*

### 3. 合成数据与数据中心学习

包括仿真、生成模型、数据增强、自动标注、数据筛选和质量评价。*论文待继续整理。*

### 4. 视觉语言模型、智能体与综述

包括视觉语言模型辅助标注、Prompt与场景规划、智能体闭环、综述和综合基准。*论文待继续整理。*

### 5. 低空应用系统

包括搜索救援、灾害响应、基础设施巡检、交通监测、农业生态和机载部署等端到端系统。*论文待继续整理。*

## 工具与资源

- **仿真与生成工具：** [AirSim](https://github.com/microsoft/AirSim) · [CARLA](https://github.com/carla-simulator/carla)
- **相关资源清单：** [Awesome VisDrone](https://github.com/VisDrone/Awesome-VisDrone) · [UAV-Vision](https://github.com/wangdongdut/UAV-Vision) · [Awesome Water Surface Perception](https://github.com/WaterScenes/Awesome-Water-Surface-Perception) · [Awesome Dataset Distillation](https://github.com/Guang000/Awesome-Dataset-Distillation)

## 参与贡献

请阅读[贡献指南](CONTRIBUTING.md)，或使用[资源推荐Issue模板](https://github.com/luziqing0416/Awesome-Low-Altitude-Vision/issues/new?template=resource-suggestion.yml). 本仓库仅提供资源索引，不重新分发数据集或受版权保护的论文。

## 许可证

[CC0 1.0](LICENSE). 被收录资源仍遵循各自的原始许可证。
