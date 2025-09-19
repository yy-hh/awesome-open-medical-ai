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
- 项目仓库：[XrayGPT](https://github.com/mbzuai-oryx/XrayGPT)
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
- 4B 多模态版本git 
- 27B 纯文本版本

免费的基本都排不上队，建议本地部署后使用。
主要测试了对影像的诊断能力，感觉效果一般，不如GPT5

## 龙影大模型RadGPT
### 1. 项目介绍
首都医科大学附属北京天坛医院(以下简称:天坛医医院)放射科刘亚欧教
授团队联合北京理工大学张美慧教授、叶初阳教授团队合作推出了全球首
个专为医学影像诊断而设计和构建的人工智能大语言模型(LLM)--"龙
影"大模型(RadGPT),基于该模型而生的全球首个中文数字放射科医
生被研发团队亲切地成为"小君"。龙影大模型的核心功能为通过分析
MRI图像的描述,快速生成诊断意见,即"图像描述--诊断结论",现已
能够生成超过百种的疾病诊断。"小君"的诊断表现现经天坛医院放射科数
十余名专家在近千例病例的验证,其准确率超过95%9。
### 2. 主要功能
- 上传影像描述和图片，可以自动生成结构化的诊断报告。
- 支持X线、CT和MR
### 3. 项目地址
- 项目仓库：目前没有开源，可以通过小程序龙影Rad或者https://radai2024.github.io/访问体验
### 4. 使用体验
必须要上传报告的影像描述才可以生成报告，感觉作用不大（目前访问也出现了问题，需要等修复）
## MedImageInsight
### 1. 项目介绍
该仓库为 MedImageInsight 模型提供了一个简化的实现方案。MedImageInsight 是一个开源的医学影像嵌入模型，由 Noel C. F. Codella 等人在论文《MedImageInsight: An Open-Source Embedding Model for General Domain Medical Imaging》中提出。微软官方提供的模型访问指南相当复杂，而且该模型是否真正开源也存在争议。这个仓库旨在简化 MedImageInsight 模型的使用，使其能够更容易地应用于各种任务，如零样本分类、图像嵌入和文本嵌入等。
### 2. 主要功能
多领域通用性：在14个不同医学领域的图像上进行训练，包括X光、CT、核磁共振、皮肤镜、OCT、眼底照相、超声、组织病理学和乳腺摄影等。
最先进（SOTA）性能：在分类、图像-图像搜索和公共数据集微调等任务中达到SOTA或人类专家水平的结果，在CT 3D医学图像检索、胸部X光疾病分类、皮肤科、OCT成像，甚至骨龄估计方面都表现出色。
符合监管要求的特性：在下游任务中使用时，MI2允许调整敏感性/特异性以满足临床监管要求。
透明的决策过程：通过图像-图像搜索、图像-文本搜索提供基于证据的决策支持，增强可解释性。
高效的报告生成：当与文本解码器配对时，仅使用与类似模型相比7%的参数就能实现接近最先进水平的报告生成。
3D能力：利用3D图像-文本预训练来实现3D医学图像检索的最先进性能。
公平性：在独立临床评估中，在年龄和性别方面的AI公平性评估中优于其他模型。
### 3. 项目地址
- 项目仓库：[MedImageInsight]https://huggingface.co/lion-ai/MedImageInsights
- 论文地址： https://arxiv.org/abs/2410.06542
### 4. 使用体验
目前有两种使用渠道：
1.通过Azure foundry部署：https://learn.microsoft.com/en-us/azure/ai-foundry/how-to/healthcare-ai/deploy-medimageinsight
2.通过huggingface部署：https://huggingface.co/lion-ai/MedImageInsights
这两种方式我都试过了，都可以正常使用。但是Azure开源的接口仅仅是一个编码器，可以把文本和图片生成向量，跟论文介绍的能力相差很远，huggingface的资源是增加了一个分类功能，可以对图片进行分类并归一化为概率值（下载的时候注意下可能会丢文件，需要手动拷贝 比如权重文件）。
```
labels = ["No Obvious Breast Nodule", "Obvious Breast Nodule Present","Unclear/Indeterminate"]
```
我实测了在超声模态下，乳腺结节检测，甲状腺结节检测发准确率在0.7左右，但是概率值普遍在0.5附近，估计是这个模型包含的超声图像训练数据不对，但是确实可以作为早期项目启动用来做预标注的工具使用。
# 视觉算法

# LLM模型
## Med-PaLM
### 1. 项目介绍
Med-PaLM 是 Google 开发的医疗领域大模型，旨在通过生成式 AI 技术革新医学知识处理、回答复杂医学问题，并提供准确、安全、公平的医疗健康解决方案。最新版本为 Med-PaLM 2。

### 2. 主要功能
- 处理多种医疗模态数据（文本、影像、基因组等）
- 解答医学考试题目和临床问题
- 支持医学影像分析和报告生成
- 提供多语言医疗问答能力

### 3. 项目地址
- GitHub 仓库：https://github.com/kyegomez/Med-PaLM

## DISC-MedLLM
### 1. 项目介绍
DISC-MedLLM 是一个由复旦大学 DISC 实验室开发的医疗健康对话大模型，专门针对真实医患对话场景优化，能够进行疾病问诊和治疗方案咨询。

### 2. 主要功能
- 提供疾病问诊和治疗方案咨询服务
- 支持多轮医疗对话与知识图谱问答
- 对齐医疗场景下的人类偏好，提供更贴近真实医生风格的回复

### 3. 项目地址
- 项目仓库：https://github.com/FudanDISC/DISC-MedLLM
- Hugging Face 模型权重：https://huggingface.co/Flmc/DISC-MedLLM

### 4. 使用体验
- 西医问答准确性较好，中医问答准确性较低
- 指令遵循能力一般，建议结合微调部署优化使用体验

## 扁鹊大模型 
### 1. 项目介绍
扁鹊（BianQue）是由华南理工大学广东省数字孪生人重点实验室开发的中文医疗健康大模型，专注于提升多轮问询与健康建议能力。包含 BianQue-1.0（基于 ChatYuan-large-v2）和 BianQue-2.0（基于 ChatGLM-6B）两个版本。

### 2. 主要功能
- 支持医疗健康多轮对话与问询（CoQ, Chain of Questioning）
- 提供疾病诊断建议和健康知识问答
- 支持药品说明书查询和医学知识检索

### 3. 项目地址
- 项目仓库：https://github.com/scutcyr/BianQue

### 4. 使用体验
- 模型容易出现幻觉现象，指令遵循能力较弱
- 问答准确性一般，建议谨慎参考其医疗建议
- 对指令理解能力较弱。
比如：
问：扁鹊你好，你的基座模型是什么？
答：你好我是郑州中心医院整形外科的刘珍君医生。根据您的描述,建议您上传一下牙齿的照片,我的基座模型是牙齿。

## 明医 (MING)：中文医疗问诊大模型

### 1. 项目介绍
明医 (MING) 是上海交通大学与上海人工智能实验室联合开发的中文医疗问诊大模型，基于 Qwen1.5 和 Bloom 系列模型进行医疗指令微调，支持医疗问答和多轮智能问诊功能。

### 2. 主要功能
- 医疗问答：对医疗问题进行解答和案例分析
- 智能问诊：通过多轮对话进行问诊并给出诊断建议
- 支持多种参数规模的模型版本（1.8B至14B）

### 3. 项目地址
- 项目仓库：https://github.com/MediaBrain-SJTU/MING

- Hugging Face 模型：
1. MING-7B：https://huggingface.co/BlueZeros/MING-7B
2. MING-1.8B：https://huggingface.co/BlueZeros/MING-1.8B
3. MING-MOE 系列：https://huggingface.co/BlueZeros/MING-MOE-1.8B
## 本草 （原名华佗）大模型
### 1. 项目介绍
Huatuo-Llama-Med-Chinese（本草）是哈尔滨工业大学开发的基于LLaMA、Bloom等模型的中文医疗大语言模型，通过医学知识库和文献指令微调，专门针对中文医疗问答场景优化。

### 2. 主要功能
- 中文医疗问答和诊断建议
- 支持多轮医疗对话
- 基于医学知识库的可靠回复生成
- 支持肝癌等特定疾病的专业咨询

### 3. 项目地址
- 项目仓库：https://github.com/SCIR-HI/Huatuo-Llama-Med-Chinese
- 模型下载：
1. 支持百度网盘下载（见项目文档）
2. Hugging Face：https://huggingface.co/lovepon/lora-bloom-med-bloom

### 4. 使用体验
- 需本地部署，建议显存≥24GB（3090/4090以上）
- 提供推理脚本和测试用例
- 模型效果优于原版LLaMA和Alpaca
## 基于 DoctorGLM
### 1. 项目介绍
DoctorGLM 是基于 ChatGLM-6B 开发的中文医疗问诊模型，通过医疗对话数据进行指令微调，专门针对中文医疗问答场景优化，支持多轮问诊对话。

### 2. 主要功能
中文医疗问答和诊断建议

支持多轮医疗对话

提供 P-Tuning 和 LoRA 两种微调方式

支持 INT4/INT8 量化部署，降低显存需求

### 3. 项目地址
- 项目仓库：https://github.com/xionghonglin/DoctorGLM 
- 模型下载：提供 INT4（https://pan.baidu.com/s/1nHQ1EQ2OBuWCyBZKBnBHYw?pwd=x6l4） 和 INT8 量化版本（https://pan.baidu.com/s/1v2hWl1dPnh8xoJzxtpbugw?pwd=y4hu）
- 基模型：ChatGLM-6B

### 4. 使用体验
- 需本地部署，FP16版本需≥13G显存
- INT4量化版本需约6G显存，INT8需约8G显存
- 提供 Gradio 网页演示界面
- 量化版本性能仍有待优化

