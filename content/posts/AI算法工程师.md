---
title: AI算法工程师
subtitle:
date: 2025-05-13T14:06:38+08:00
slug: 3e78a2f
draft: false
author:
  name: 赵容博
  link:
  email:
  avatar:
description:
keywords:
license:
comment: false
weight: 0
tags:
  - draft
categories:
  - draft
hiddenFromHomePage: false
hiddenFromSearch: false
hiddenFromRelated: false
hiddenFromFeed: false
summary:
resources:
  - name: featured-image
    src: featured-image.jpg
  - name: featured-image-preview
    src: featured-image-preview.jpg
toc: true
math: false
lightgallery: false
password:
message:
repost:
  enable: true
  url:

# See details front matter: https://fixit.lruihao.cn/documentation/content-management/introduction/#front-matter
---

<!--more-->

## AI 算法工程师（视觉感知方向）

### 岗位职责

1. 相机硬件的选型、调试和标定等相关工作；
2. 设计、开发和优化视觉算法和模型，以解决图像识别、目标检测、目标跟踪、图像分割等问题；
3. 开发和推进基于深度学习的单目深度拟合、双目立体匹配算法应用落地；
4. 调研和推进 3D 人体姿态估计算法、6D 物体姿态估计算法的评估和应用；
5. 跟进基于深度学习的前沿视觉 SLAM 算法；
6. 负责视觉算法开发、调试、部署和落地；

### 任职要求

1. 熟悉相机 sensor 工作原理、ISP 图像处理流程、相机基本参数及标定, 了解图像质量的主客观评估标准；
2. 熟悉主流的神经网络架构(ResNet、ViT 等)， 目标检测算法(如 YOLO、DETR 等)， 语义分割算法(Mask2Former、SAM 等)；
3. 熟悉至少一种常用的单目深度拟合算法(如 DepthAnything 等), 至少熟悉一种双目立体匹配算法(如 LightStereo 等)；
4. 了解主流的 3D 人体姿态估计算法(如 PoseFormer 等)或 6D 物体姿态估计算法(如 FoundationPose 等)的优先；
5. 了解主流的端到端视觉 SLAM 算法(如 DROID-SLAM 等)， 了解基于 Gaussian Splatting 的 SLAM(如 SplaTAM)的优先；
6. 熟练掌握 pytorch 等框架，熟悉常见的深度学习模型，并掌握相关的实现、训练、调优、部署等工作；
7. 熟悉 C++和 Python 编程语言，具备良好的编程习惯和较好的工程化能力；
8. 具有计算机科学、电子工程或相关专业全日制本科及以上学历； 2 年及以上工作经验。

## 学习计划

### 第一阶段：硬件基础与算法框架（1-3个月）

**目标**：掌握相机硬件全流程与深度学习基础能力

1. **相机硬件专项**（4周）
   - 学习《Computer Vision: Algorithms and Applications》第2章（成像原理）
   - 实践OpenCV相机标定模块（张正友标定法）
   - 使用MATLAB/ROS工具进行ISP流程模拟实验
   - 搭建图像质量评估体系（PSNR/SSIM → 新指标：LPIPS/CSIQ）
2. **算法框架升级**（4周）
   - 深度学习框架：
     - PyTorch高级特性（分布式训练/量化部署）
     - ONNX/TensorRT部署实战（YOLOv8部署案例）
   - 搭建算法基线：
     - 复现YOLOv8改进策略（损失函数/标签分配）
     - 实现Mask2Former的实例分割pipeline

### 第二阶段：立体视觉与深度估计（4-6个月）

**目标**：建立三维视觉技术栈

1. **单目深度估计**（4周）
   - 精读Depth Anything论文（CVPR 2024）
   - 使用NYU Depth V2数据集训练改进模型
   - 设计轻量化方案（知识蒸馏→移动端部署）
2. **双目立体匹配**（4周）
   - 研究LightStereo的工业级优化策略
   - 在SceneFlow数据集上开展对比实验
   - 开发FPGA加速方案（HLS代码优化）
3. **3D姿态估计**（4周）
   - 复现PoseFormer的时序建模模块
   - 在Human3.6M数据集上优化推理速度
   - 探索FoundationPose的zero-shot能力

### 第三阶段：SLAM与前沿技术（7-9个月）

**目标**：构建SLAM技术体系并追踪前沿

1. **经典SLAM系统**（5周）
   - 手撕ORB-SLAM3核心模块（特征提取/优化）
   - 在TUM数据集上完成完整轨迹评测
   - 开发ROS实时运行系统
2. **深度学习SLAM**（4周）
   - 分析DROID-SLAM的BA优化策略
   - 复现SplaTAM的Gaussian Splatting实现
   - 在Replica数据集进行三维重建对比
3. **论文精读计划**（持续）
   - 每周精读2篇CVPR/ICCV最新论文
   - 建立技术趋势分析文档（GitHub仓库维护）

### 第四阶段：工程化实战（10-12个月）

**目标**：打造完整的项目闭环

1. **工业级项目开发**（8周）
   - 设计端到端视觉系统：从相机选型（IMX477 vs OV4689）到算法部署
   - 开发自动化标定工具链（含异常检测模块）
   - 构建质量监控系统（Drift检测/在线校准）
2. **性能优化专项**（4周）
   - 算法级优化：模型剪枝（LayerDrop）
   - 硬件级优化：GPU TensorCore加速
   - 系统级优化：多线程流水线设计
3. **作品集构建**（持续）
   - GitHub维护3个高质量项目：
     1. 实时多目标跟踪系统
     2. 嵌入式双目深度解决方案
     3. 基于NeRF的SLAM系统
   - 撰写技术博客（Medium/知乎专栏）

### 学习资源推荐：

1. 硬件方向：《CMOS图像传感器电路设计》
2. 算法方向：《Multiple View Geometry in Computer Vision》
3. 工程实践：《CUDA C++ Best Practices Guide》
4. 论文库：CVF Open Access + arXiv每日推送

### 关键实施策略：

1. 建立技术雷达图：每月更新各技术维度能力值
2. 参与Kaggle竞赛：至少完成2个计算机视觉赛事
3. 硬件投入：搭建含Jetson Orin+工业相机的开发平台
4. 参加CVPR/IROS等会议（线上资源）了解工业界最新需求

建议每周保持30小时有效学习时间（含项目实践），重点关注技术深度的纵向突破而非广度覆盖，每阶段结束时输出可展示的成果物。同时建议与行业从业者保持交流（如GitHub贡献、技术社区答疑），培养工程思维和产品意识。
