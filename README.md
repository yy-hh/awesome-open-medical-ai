# 多模态算法
## XrayGPT
### 1. 使用场项目介绍景
通过XrayGPT，用户可以上传X光片，获取X光片的分析结果，包括疾病诊断、疾病类型、疾病位置、疾病严重程度等。
### 2. 主要功能
- 基于深度学习的X光片分析算法，准确率高
- 支持多疾病类型的分析，包括肺炎、COVID-19、肺部疾病等
- 支持用户自定义分析参数，满足不同用户的需求
- 支持批量分析，用户可以上传多张X光片，获取批量分析结果
### 3. 项目地址
- 项目仓库：[XrayGPT](https://github.com/yourusername/XrayGPT)
- 项目文档：[XrayGPT文档](https://yourusername.github.io/XrayGPT/)
### 4. 使用体验
感觉项目已经无人维护，项目部署存在依赖冲突，项目文档也无法访问

## MONAI
### 1. 项目介绍
Project MONAI是一个基于PyTorch的开源项目，用于医疗图像分析。它提供了一系列的深度学习模型和工具，用于处理医疗图像数据，包括图像分类、图像分割、图像生成等。
### 2. 主要功能
- 提供了一系列的深度学习模型，包括UNet、ResNet、VGG等
- 提供了一系列的图像预处理和后处理工具，包括图像增强、图像归一化、图像裁剪等
- 提供了一系列的图像分析工具，包括图像分类、图像分割、图像生成等
### 3. 项目地址
- 项目仓库：[Project MONAI](https://github.com/Project-MONAI/MONAI)
- 项目文档：[Project MONAI文档](https://docs.monai.io/en/latest/)
### 4. 使用体验
主要是体验了Core框架，基于pytorch 做了很多封装，还提供了40个预训练模型，以CT和MRI为主
| 维度 | PyTorch（通用框架） | MONAI（医学影像专用框架） |
|------|-------------------|------------------------|
| 框架定位 | 通用深度学习框架 | 基于 PyTorch 的医学影像 AI 工具包 |
| 数据读取 | 需手动使用 SimpleITK、Nibabel 等库处理 NIfTI/DICOM | 内置 LoadImage、CacheDataset、PersistentDataset，直接支持医学影像格式 |
| 数据预处理 | 需自己实现重采样、归一化、3D 增强等 | 提供 100+ 医学影像专用 transforms（HU 归一化、3D 裁剪、Patch 采样等） |
| 模型库 | 手动实现 UNet、VNet、SegResNet 等 | 内置大量医学影像模型，并提供医学数据集预训练权重 |
| 指标计算 | 需手写 Dice、Hausdorff 等医学特有指标 | 内置 Dice、Hausdorff、SurfaceDistance 等标准指标 |
| 训练循环 | 需自写训练/验证/推理代码 | 内置 Trainer、Evaluator、AMP 和多 GPU 支持 |
| 生态工具 | 无专门医学工具 | 提供 MONAI Label（标注）、MONAI Deploy（部署）等扩展 |
| 灵活性 | 完全自由度，但重复造轮子 | 高度封装，快速搭建标准 pipeline |

## medgemma
### 1. 项目介绍
MedGemma 是 Gemma 3 变体的集合，经过专门训练以提升医疗文本和图像理解能力。开发者可以使用 MedGemma 来加速构建基于医疗保健的 AI 应用程序。MedGemma 有两个版本：4B 多模态版本和 27B 纯文本版本。
### 2. 主要功能
- 提供了一系列的深度学习模型，包括UNet、ResNet、VGG等
- 提供了一系列的图像预处理和后处理工具，包括图像增强、图像归一化、图像裁剪等
- 提供了一系列的图像分析工具，包括图像分类、图像分割、图像生成等
### 3. 项目地址
- 项目仓库：[MedGemma](https://github.com/Google-Health/medgemma)
### 4. 使用体验
提供了一个线上体验地址：https://dr7.ai/medgemma
- 4B 多模态版本：https://dr7.ai/medgemma-4b
- 27B 纯文本版本：https://dr7.ai/medgemma-27b
免费的基本都排不上队，建议本地部署后使用。