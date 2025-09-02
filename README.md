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
主要测试了对影像的诊断能力，感觉效果一般，不如GPT5
# 视觉算法
## 目标检测
### 1. YOLO（You Only Look Once）
一种实时目标检测系统，由Joseph Redmon等人在2015年首次提出。YOLO的设计理念是将目标检测问题视为一个回归问题，从输入图像直接预测目标的边界框和类别概率。YOLO系列模型因其高效的实时性能和较高的检测精度而广泛应用于各种计算机视觉任务中。YOLO系列模型因其高效的实时检测能力和不断提升的检测精度，已成为计算机视觉领域目标检测的一个重要基准，并被广泛应用于自动驾驶、监控系统、智能设备等多个领域。
- 项目仓库：

[yolo-v8](https://github.com/DataXujing/YOLOv8)

[yolo-v9](https://github.com/WongKinYiu/yolov9) 

[yolo-v13](https://github.com/iMoonLab/yolov13) 

### 2. mmdetection
MMDetection 是一个开源的、基于 PyTorch 的目标检测工具箱，由香港中文大学的多媒体实验（Multimedia Laboratory, CUHK）开发。它是 OpenMMLab 项目的一部分，旨在为研究人员和工程师提供一个灵活、易用且高效的目标检测框架。包含yolo，maskrcnn，faster-rcnn等多种检测算法。
- 项目仓库：
[mmdetection](https://github.com/open-mmlab/mmdetection)

## 目标分割
### 1. UNet
U-Net 是一种用于生物医学图像分割的卷积神经网络（CNN）架构，由 Olaf Ronneberger 等人在 2015 年提出。它因其在医学图像分割任务中的卓越表现而广受欢迎。
- 项目仓库：
[Unet-pytorch](https://github.com/milesial/Pytorch-UNet)
### 2.nnUNet
nnU-Net（no-new-Net）是一个自动化的神经网络框架，专门用于医学图像分割任务。它由Fabian Isensee等人在2020年提出，旨在通过自动化的方式优化神经网络架构和训练流程，以在不同的医学图像分割任务中实现高性能。nnU-Net通过自动化的方式简化了医学图像分割模型的开发流程，大大提高了开发效率和模型性能，是医学影像分析领域的重要工具。
- 项目仓库：[nnUNet](https://github.com/MIC-DKFZ/nnUNet) 

### 3. unet衍生变种
resunet
denseunet
... 

## 超分辨率
### 1. srcnn
SRCNN（Super-Resolution Convolutional Neural Network）是最早的基于深度学习的图像超分辨率方法之一，由 Dong 等人在 2014 年提出。SRCNN 的设计简单而有效，它引入了卷积神经网络（CNN）来解决图像超分辨率问题。
- 项目仓库：[srcnn](https://github.com/yjn870/SRCNN-pytorch) 
### 2. srgan
SRGAN（Super-Resolution Generative Adversarial Network）是一种用于图像超分辨率的生成对抗网络（GAN）方法，由 Ledig 等人在 2017 年提出。SRGAN 是通过结合生成对抗网络的思想，生成更逼真和细节丰富的高分辨率图像的一种方法。在实际训练过程中，判别器损失和生成器损失非常难调，很容易崩溃。
- 项目仓库：[srgan](https://github.com/leftthomas/SRGAN) 
### 3. sr3
SR3（Super-Resolution via Repeated Refinement）是一种由 OpenAI 提出的基于扩散模型的图像超分辨率方法。与传统的生成对抗网络（GAN）不同，SR3 利用扩散过程来逐步提高图像的分辨率。
- 项目仓库：[sr3](https://github.com/Janspiry/Image-Super-Resolution-via-Iterative-Refinement) 

# LLM算法