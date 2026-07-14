## Resource type

- [✅] Dataset
- [✅] Paper
- [✅] Benchmark
- [ ] Code or tool
- [ ] Survey or resource list
- [ ] Metadata/link correction

## Summary

<!-- What does this pull request add or correct? -->

新增 29 个符合低空无人机视觉收录范围的数据集及其关联论文，并新增 3 个分类目录。

### 新增数据集（按分类）

**灾害与恶劣环境（3个）：**
- FIReStereo (2024) — 火灾场景立体红外+RGB深度感知
- HazyDet (2024) — 雾天无人机目标检测基准（含深度线索）
- UAV-AWID (2024) — 恶劣天气与图像退化（雨/运动模糊/噪声）

**交通与城市场景（2个）：**
- VDD / Varied Drone Dataset (2025) — 多场景（城市/工业/乡村/自然）语义分割，7类标注
- SDD / Stanford Drone Dataset (2016) — 斯坦福校园俯拍行人/车辆轨迹，支持检测、跟踪、行为预测

**热红外与多模态感知（5个）：**
- HiAI (2025) — 高空RGB-红外双模态无人机目标跟踪
- RTDOD (2023) — RGB-热红外域增量无人机目标检测
- DroneRGBT (2020) — RGB-热红外跨模态无人机人群计数（3,600对齐图像）
- Salient Map Thermal Dataset (2020) — 2,975张无人机热红外显著目标检测标注
- ASL-TID (2014) — ETH Zurich早期机载热红外行人/车辆跟踪基准

**多无人机协同感知（6个）：**
- UAV3D (2024, NeurIPS) — 大规模单机/多机3D协同检测与跟踪基准
- Air-Co-Pred / AirCopBench (2023) — 多无人机协同轨迹预测
- MAVREC (2023) — 无人机+地面多视角航空识别（50万+帧，110万标注框）
- CoPerception-UAVs (2022) — 5架无人机协同2D/3D检测与BEV分割
- MDMT (2022) — 双无人机同步多目标跟踪（88段视频，39,678帧）
- MDOT (2020) — 首个多无人机协同单目标跟踪基准

**具身智能与视觉语言导航（7个）：**
- AeroVerse (2024) — 无人机具身智能体基准套件
- CityNav (2024) — 城市级语言引导无人机导航（32,000+指令）
- OpenUAV (2024) — 照片级真实感无人机VLN平台
- UAV-VisLoc (2024) — 无人机视觉定位（跨视角匹配卫星地图）
- AerialVLN (2023, ICCV) — 首个无人机视觉语言导航基准
- UrbanBIS (2023) — 大规模城市建筑实例分割（倾斜摄影，6城市，25亿点）
- AVDN (2022) — 对话式空中视觉语言导航

**合成数据（3个）：**
- UEMM-Air (2024) — UE+AirSim六种配对多模态合成数据（120K+序列）
- SkyScenes (2024) — 城市级合成航空多模态感知
- SynDrone (2023) — UE合成多模态（RGB/深度/LiDAR）城市无人机数据

### 新增分类目录

在 datasets/README.md 和主 README.md 中新增 3 个分类：
- **Thermal and Multimodal Perception**（热红外与多模态感知）
- **Multi-Drone Collaborative Perception**（多无人机协同感知）
- **Embodied AI and Vision-Language Navigation**（具身智能与视觉语言导航）

### 排除的数据集（经核实不符合收录标准）

| 数据集 | 排除原因 |
|---|---|
| Oxford RobotCar | 地面车辆（Nissan LEAF）采集，非无人机/航空平台 |
| VEDAI | 高空航空测绘影像（犹他州AGRC），非无人机 |
| COWC | 15cm GSD高空航空影像（ISPRS/政府航测），非无人机 |
| DOTA / iSAID | Google Earth / 卫星影像（GF-2, JL-1），非无人机 |
| RarePlanes | Maxar WorldView卫星影像，非无人机 |
| TinyPerson | 图像采集自互联网视频，非受控无人机采集 |
| ARIO | 通用具身机器人（机械臂/室内导航），不含无人机数据 |
| AnimalDrone | xlsx提供的arXiv链接指向无关论文（COVID），无法验证 |
| DroneDeploy | 为商业平台名称而非特定命名数据集 |
| State-Air | 多次搜索未找到可靠来源 |
| OpenBench | 与已收录的 UAVBench (UAEU/Khalifa) 描述高度重合 |
| DroneSwarms / DroneBird / NPS-Drones / ARD-MAV / Anti-UAV | 反无人机监控类（以无人机本身为检测/跟踪目标），不符合收录范围 |

## Source verification

### 数据集来源验证

- [SDD](https://cvgl.stanford.edu/projects/uav_data/) — 斯坦福官方项目页，无人机采集
- [VDD](https://github.com/RussRobin/VDD) — GitHub官方仓库，JVCI 2025论文
- [HazyDet](https://github.com/GrokCV/HazyDet) — GitHub官方仓库，arXiv:2409.19833
- [UAV-AWID](https://github.com/AdnanMunir338/UAV-AWID) — GitHub官方仓库
- [FIReStereo] — CMU数据集，被南航2025低空视觉综述收录
- [ASL-TID](https://projects.asl.ethz.ch/datasets/doku.php?id=ir_dataset) — ETH Zurich官方数据集页
- [DroneRGBT](https://github.com/VisDrone/DroneRGBT) — VisDrone官方GitHub
- [RTDOD](https://github.com/fenght96/RTDOD) — GitHub官方仓库，Image and Vision Computing 2023
- [HiAI] — 被南航2025低空视觉综述收录为高空红外-可见光跟踪数据集
- [Salient Map Thermal Dataset] — 被南航2025低空视觉综述收录为热红外显著目标数据集
- [MDMT](https://github.com/VisDrone/Multi-Drone-Multi-Object-Detection-and-Tracking) — VisDrone官方GitHub，IEEE TMM 2023
- [CoPerception-UAVs](https://siheng-chen.github.io/dataset/coperception-uav/) — 项目官方页
- [UAV3D](https://github.com/huiyegit/UAV3D) — GitHub官方仓库，NeurIPS 2024
- [MAVREC] — 被南航2025低空视觉综述收录为多视角航空识别数据集
- [MDOT] — 被南航2025低空视觉综述收录为首个多无人机协同跟踪基准
- [Air-Co-Pred / AirCopBench] — 被南航2025低空视觉综述收录为多无人机协同预测基准
- [AerialVLN](https://github.com/AirVLN/AirVLN) — GitHub官方仓库，ICCV 2023
- [UrbanBIS](https://vcc.tech/UrbanBIS) — 项目官方页，arXiv:2305.02627
- [CityNav](https://water-cookie.github.io/city-nav-proj/) — 项目官方页，arXiv:2406.14240
- [AeroVerse](https://arxiv.org/abs/2408.15511) — arXiv论文
- [UAV-VisLoc](https://github.com/intellisensing/uav-visloc) — GitHub官方仓库，arXiv:2405.11936
- [AVDN] — CMU对话式空中导航数据集，被南航2025低空视觉综述收录
- [OpenUAV] — 被南航2025低空视觉综述收录为照片级VLN平台
- [UEMM-Air](https://github.com/1e12Leon/UEMM-Air) — GitHub官方仓库，arXiv:2406.06230，ACM MM 2025
- [SkyScenes] — 被南航2025低空视觉综述收录为城市级合成航空感知数据集
- [SynDrone] — 被南航2025低空视觉综述收录为UE合成多模态无人机数据集

### 排除数据集来源验证

- [Oxford RobotCar](https://robotcar-dataset.robots.ox.ac.uk/) — 官方页明确为车载采集
- [VEDAI](https://downloads.greyc.fr/vedai/) — 数据来自犹他州AGRC航空测绘
- [COWC](https://gdo152.llnl.gov/cowc/) — 官方页明确为15cm GSD航空测绘
- [DOTA](https://captain-whu.github.io/DOTA/dataset.html) — 官方页明确图像来源为Google Earth/卫星
- [iSAID](https://captain-whu.github.io/iSAID/) — 与DOTA同源（卫星+航空影像）
- [RarePlanes](https://www.cosmiqworks.org/rareplanes/) — Maxar WorldView卫星数据
- [TinyPerson](https://github.com/ucas-vg/TinyBenchmark) — 论文3.1节明确图像采集自互联网
- [ARIO](https://imaei.github.io/project_pages/ario/) — 官方页为机械臂/室内导航，无无人机数据

### 关键参考来源

- 孙一铭等.《面向无人机的低空视觉数据集研究综述》. 数据采集与处理, 2025, 40(2): 274-302. DOI:10.16337/j.1004-9037.2025.02.002

### 许可/访问条件

所有新增数据集均标注了访问条件（Open / Check / 非商业等），详见 datasets/README.md 中对应条目。

## Checklist

- [x] The resource is directly relevant to low-altitude UAV vision.
- [x] I checked for duplicates.
- [x] I used official, publisher, or author-maintained links.
- [x] I did not upload copyrighted PDFs or restricted dataset files.
- [x] The description is factual and concise.
