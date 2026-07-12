# 低空视觉资源精选

> 面向低空无人机视觉的数据集、论文、基准与研究资源索引。

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0--1.0-lightgrey.svg)](LICENSE)
[![欢迎贡献](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

[English](README.md) | **简体中文**

低空无人机视觉与卫星遥感、地面视觉存在明显差异，通常面临俯视视角、目标尺度小、相机持续运动、背景复杂以及真实任务约束强等问题。本仓库重点整理目标检测、目标跟踪、语义分割、海上搜救、灾害响应、多模态感知与合成数据生成相关资源。

## 目录

- [数据集分类与详细清单](datasets/README.md)
  - 通用无人机感知
  - 海上搜救
  - 灾害响应
  - 多模态与跨光谱感知
- [论文与基准分类](papers/README.md)
  - 检测与跟踪
  - 海上搜救
  - 灾害场景理解
  - 合成数据、仿真与智能体
- [贡献指南](CONTRIBUTING.md)

## 首批精选数据集

| 数据集 | 主要任务 | 场景 | 资源 |
|---|---|---|---|
| **SeaDronesSee** | 检测、单目标/多目标跟踪 | 海上搜救 | [官网](https://seadronessee.cs.uni-tuebingen.de/) · [论文](https://openaccess.thecvf.com/content/WACV2022/html/Varga_SeaDronesSee_A_Maritime_Benchmark_for_Detecting_Humans_in_Open_Water_WACV_2022_paper.html) |
| **VisDrone** | 检测、跟踪、人群计数 | 城市与乡村无人机影像 | [数据集](https://github.com/VisDrone/VisDrone-Dataset) · [论文](https://doi.org/10.1109/TPAMI.2021.3119563) |
| **UAVDT** | 检测与跟踪 | 低空交通监控 | [项目](https://sites.google.com/site/daviddo0323/projects/uavdt) · [论文](https://openaccess.thecvf.com/content_ECCV_2018/html/Dawei_Du_The_Unmanned_Aerial_ECCV_2018_paper.html) |
| **FloodNet** | 分类、分割、视觉问答 | 洪灾后场景理解 | [数据集](https://github.com/BinaLab/FloodNet-Supervised_v1.0) · [论文](https://arxiv.org/abs/2105.08655) |
| **RescueNet** | 分类与分割 | 灾后损毁评估 | [论文与数据说明](https://www.nature.com/articles/s41597-023-02799-4) |

完整信息请查看[数据集清单](datasets/README.md)。

## 重点研究方向

- 运动航拍平台下的小目标检测
- 搜救视频中的人员识别与帧筛选
- 海上落水人员检测和跟踪
- 灾后场景理解与损毁评估
- RGB–红外及多传感器融合
- 合成无人机图像与仿真到真实迁移
- 视觉语言模型辅助标注与质量评估
- 基于智能体的闭环数据生成

## 收录范围

原则上收录由无人机或相近低空平台采集、并且与低空视觉任务直接相关的资源。纯卫星遥感数据通常不收录，除非其研究明确结合了低空无人机数据。

本仓库只提供学术资源索引，不重新分发数据集和论文 PDF。使用前请检查原始许可证、访问条件、隐私要求及允许用途。

## 参与贡献

欢迎补充新数据集、论文、基准、代码和调查综述。提交前请阅读[贡献指南](CONTRIBUTING.md)，也可以直接使用资源推荐 Issue 模板。

## 许可证

本资源清单采用 [CC0 1.0](LICENSE)。被收录的数据集、论文、代码和媒体仍遵循其各自的原始许可证。
