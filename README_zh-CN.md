# 低空视觉资源精选

> 面向低空无人机视觉的数据集、论文、基准与研究资源索引。

[English](README.md) | **简体中文**

低空无人机视觉通常面临俯视视角、目标尺度小、相机运动、复杂背景和真实任务约束。本清单同时保留搜救、灾害响应、基础设施巡检、交通、农业、生态、通用视觉与合成数据资源。

## 目录

- [数据集](#数据集)
  - [搜索救援与公共安全](#搜索救援与公共安全)
  - [灾害与环境风险](#灾害与环境风险)
  - [基础设施巡检](#基础设施巡检)
  - [交通与城市监测](#交通与城市监测)
  - [农业林业与生态](#农业林业与生态)
  - [通用低空视觉](#通用低空视觉)
  - [合成与仿真数据](#合成与仿真数据)
- [论文与基准](#论文与基准)
- [参与贡献](#参与贡献)

## 数据集

### 搜索救援与公共安全

| 数据集 | 年份 | 任务 | 模态 | 主要内容 | 资源 |
|---|---:|---|---|---|---|
| **NOMAD** | 2023 | 检测 | RGB视频 | 多飞行距离、遮挡条件下的人员 | [数据集](https://github.com/ArtRuss/NOMAD) · [论文](https://arxiv.org/abs/2309.09518) |
| **SeaDronesSee** | 2022 | 检测、单/多目标跟踪 | RGB视频+元数据 | 落水者、船、摩托艇、救生设施和浮标 | [官网](https://seadronessee.cs.uni-tuebingen.de/) · [数据](https://seadronessee.cs.uni-tuebingen.de/dataset) · [论文](https://openaccess.thecvf.com/content/WACV2022/html/Varga_SeaDronesSee_A_Maritime_Benchmark_for_Detecting_Humans_in_Open_Water_WACV_2022_paper.html) |
| **Manipal UAV Person** | 2020 | 检测 | RGB视频 | 不同天气、光照和平台下的小尺度人员 | [数据集](https://github.com/Akshathakrbhat/Manipal-UAV-Person-Dataset) |
| **HERIDAL** | 2019 | 检测 | RGB图像 | 地中海地貌中的陆地搜救人员 | [论文](https://doi.org/10.1007/s11263-019-01177-1) |
| **Okutama-Action** | 2017 | 检测、动作识别 | RGB视频 | 航拍视角下的多人动作 | [数据集](https://okutama-action.org/) · [论文](https://openaccess.thecvf.com/content_cvpr_2017_workshops/w24/html/Barekatain_Okutama-Action_An_Aerial_CVPR_2017_paper.html) |

### 灾害与环境风险

| 数据集 | 年份 | 任务 | 模态 | 主要内容 | 资源 |
|---|---:|---|---|---|---|
| **C2A** | 2024 | 检测 | 合成RGB | 合成灾害响应场景中的人员 | [数据与代码](https://github.com/Ragib-Amin-Nihal/C2A) |
| **RescueNet** | 2023 | 分类、分割 | RGB | 灾后损毁和场景理解 | [论文与数据](https://www.nature.com/articles/s41597-023-02799-4) |
| **FloodNet** | 2021 | 分类、分割、视觉问答 | RGB | 飓风后受淹与未受淹基础设施 | [数据集](https://github.com/BinaLab/FloodNet-Supervised_v1.0) · [论文](https://arxiv.org/abs/2105.08655) |
| **FLAME** | 2021 | 分类、分割 | RGB、热红外、视频 | 无人机火灾监测 | [项目](https://github.com/AlirezaShamsoshoara/Fire-Detection-UAV-Aerial-Image-Classification-Segmentation-UnmannedAerialVehicle) · [数据](https://doi.org/10.21227/7rk7-ey09) |

### 基础设施巡检

| 数据集 | 年份 | 任务 | 主要内容 | 资源 |
|---|---:|---|---|---|
| **PTL-AI Furnas** | 2023 | 分类、检测 | 输电线路部件和故障 | [数据集](https://github.com/freds0/PTL-AI_Furnas_Dataset) |
| **TTPLA** | 2020 | 检测、语义/实例分割 | 输电塔和细电力线 | [数据集](https://github.com/r3ab/ttpla_dataset) · [论文](https://openaccess.thecvf.com/content/ACCV2020/html/Abdelfattah_TTPLA_An_Aerial-Image_Dataset_for_Detection_and_Segmentation_of_Transmission_ACCV_2020_paper.html) |

### 交通与城市监测

| 数据集 | 年份 | 任务 | 模态 | 主要内容 | 资源 |
|---|---:|---|---|---|---|
| **AU-AIR** | 2020 | 检测 | RGB视频+元数据 | 低空城市交通 | [数据](https://bozcani.github.io/auairdataset) · [论文](https://doi.org/10.1109/ICRA40945.2020.9197293) |
| **DroneVehicle** | 2020 | 检测 | RGB–热红外 | 跨模态车辆与旋转框 | [数据](https://github.com/VisDrone/DroneVehicle) · [论文](https://arxiv.org/abs/2003.02437) |
| **UAVDT** | 2018 | 检测、单/多目标跟踪 | RGB视频 | 不同高度、视角、天气和光照下的车辆 | [数据存档](https://zenodo.org/records/14575517) · [论文](https://openaccess.thecvf.com/content_ECCV_2018/html/Dawei_Du_The_Unmanned_Aerial_ECCV_2018_paper.html) |
| **UAVid** | 2018 | 语义分割 | 4K RGB视频 | 城市道路、建筑、植被、车辆和人员 | [数据](https://uavid.nl/) · [论文](https://arxiv.org/abs/1810.10438) |

### 农业林业与生态

| 数据集 | 年份 | 任务 | 模态 | 主要内容 | 资源 |
|---|---:|---|---|---|---|
| **CART** | 2024 | 低空机器人感知 | RGB–热红外+GPS/IMU | 河流、湖泊、海岸、沙漠和森林 | [数据](https://data.caltech.edu/records/cks6g-ps927) · [代码](https://github.com/aerorobotics/caltech-aerial-rgbt-dataset) · [论文](https://arxiv.org/abs/2403.08997) |
| **BIRDSAI** | 2020 | 检测、单/多目标跟踪 | 真实与合成热红外视频 | 保护区中的人员与野生动物 | [数据](https://sites.google.com/view/elizabethbondi/dataset) · [论文](https://openaccess.thecvf.com/content_WACV_2020/html/Bondi_BIRDSAI_A_Dataset_for_Detection_and_Tracking_in_Aerial_Thermal_Infrared_WACV_2020_paper.html) |

### 通用低空视觉

| 数据集 | 年份 | 任务 | 主要内容 | 资源 |
|---|---:|---|---|---|
| **VisDrone** | 2018– | 检测、跟踪、人群计数 | 城乡场景中的行人与车辆 | [数据](https://github.com/VisDrone/VisDrone-Dataset) · [论文](https://doi.org/10.1109/TPAMI.2021.3119563) |
| **UAV123 / UAV20L** | 2016 | 单目标跟踪 | 人员、车辆、船只等目标 | [项目](https://cemse.kaust.edu.sa/ivul/uav123) · [论文](https://arxiv.org/abs/1605.07109) |

### 合成与仿真数据

| 数据集/工具 | 年份 | 用途 | 资源 |
|---|---:|---|---|
| **C2A** | 2024 | 合成灾害人员检测 | [数据与代码](https://github.com/Ragib-Amin-Nihal/C2A) |
| **Synthetic SeaDronesSee** | — | 合成海上搜救目标检测 | [官方数据页](https://seadronessee.cs.uni-tuebingen.de/dataset) |
| **AirSim** | 2017 | 无人机与自动驾驶仿真 | [代码](https://github.com/microsoft/AirSim) |
| **CARLA** | 2017 | 城市仿真与可配置航拍相机 | [代码](https://github.com/carla-simulator/carla) |

## 论文与基准

### 检测与跟踪

- **Detection and Tracking Meet Drones Challenge** — IEEE TPAMI 2022。[论文](https://doi.org/10.1109/TPAMI.2021.3119563)
- **AU-AIR: A Multi-modal Unmanned Aerial Vehicle Dataset for Low Altitude Traffic Surveillance** — ICRA 2020。[论文](https://doi.org/10.1109/ICRA40945.2020.9197293)
- **The Unmanned Aerial Vehicle Benchmark: Object Detection and Tracking** — ECCV 2018。[论文](https://openaccess.thecvf.com/content_ECCV_2018/html/Dawei_Du_The_Unmanned_Aerial_ECCV_2018_paper.html)
- **A Benchmark and Simulator for UAV Tracking** — ECCV 2016。[论文](https://arxiv.org/abs/1605.07109)

### 人员理解与搜救

- **NOMAD: A Natural, Occluded, Multi-scale Aerial Dataset for Emergency Response Scenarios** — 2023。[论文](https://arxiv.org/abs/2309.09518)
- **SeaDronesSee: A Maritime Benchmark for Detecting Humans in Open Water** — WACV 2022。[论文](https://openaccess.thecvf.com/content/WACV2022/html/Varga_SeaDronesSee_A_Maritime_Benchmark_for_Detecting_Humans_in_Open_Water_WACV_2022_paper.html)
- **Deep Learning Approach on Aerial Imagery in Supporting Land Search and Rescue Missions** — IJCV 2019。[论文](https://doi.org/10.1007/s11263-019-01177-1)
- **Okutama-Action: An Aerial View Video Dataset for Concurrent Human Action Detection** — CVPR Workshops 2017。[论文](https://openaccess.thecvf.com/content_cvpr_2017_workshops/w24/html/Barekatain_Okutama-Action_An_Aerial_CVPR_2017_paper.html)

### 灾害、巡检与多模态

- **CART: Caltech Aerial RGB-Thermal Dataset in the Wild** — 2024。[论文](https://arxiv.org/abs/2403.08997)
- **RescueNet** — Scientific Data 2023。[论文](https://www.nature.com/articles/s41597-023-02799-4)
- **FloodNet** — IEEE Access 2021。[论文](https://arxiv.org/abs/2105.08655)
- **The FLAME Dataset** — Computer Networks 2021。[项目与数据](https://github.com/AlirezaShamsoshoara/Fire-Detection-UAV-Aerial-Image-Classification-Segmentation-UnmannedAerialVehicle)
- **TTPLA** — ACCV 2020。[论文](https://openaccess.thecvf.com/content/ACCV2020/html/Abdelfattah_TTPLA_An_Aerial-Image_Dataset_for_Detection_and_Segmentation_of_Transmission_ACCV_2020_paper.html)
- **BIRDSAI** — WACV 2020。[论文](https://openaccess.thecvf.com/content_WACV_2020/html/Bondi_BIRDSAI_A_Dataset_for_Detection_and_Tracking_in_Aerial_Thermal_Infrared_WACV_2020_paper.html)

### 合成数据、仿真与智能体

本节将继续收录低空场景可控生成、仿真到真实迁移、自动标注、图文一致性、物理合理性以及闭环生成智能体相关工作。

- [Synthetic SeaDronesSee](https://seadronessee.cs.uni-tuebingen.de/dataset)
- [AirSim](https://github.com/microsoft/AirSim)
- [CARLA](https://github.com/carla-simulator/carla)

## 参与贡献

欢迎通过 [Issue 模板](https://github.com/luziqing0416/Awesome-Low-Altitude-Vision/issues/new?template=resource-suggestion.yml) 或 Pull Request 推荐资源。详细维护规范见 [CONTRIBUTING.md](CONTRIBUTING.md)。

本仓库仅提供索引，不重新分发数据集或受版权保护的论文。
