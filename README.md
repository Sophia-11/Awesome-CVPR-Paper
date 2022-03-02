# CVPR 2022\2021\2020\2019\2018\2017 最新文章下载
## [CVPR2022录用名单](./CVPR2022/Readme.md)
### CVPR2022 百度云正在准备中
### 公众号【计算机视觉联盟】后台回复 CVPR2021 获得百度云
## CVPR2021最全1660篇pdf(4.3G)
链接: https://pan.baidu.com/s/1GWkqUOcO6KMOu-uLJrSpbA 提取码: vwkx 

### 目录
#### 【0】CVPR2022录取结果公布
#### 【1】CVPR2021录取结果公布
#### 【2】CVPR2021最新更新文章
#### 【3】CVPR2020、2019、2018、2017下载链接
#### 【4】CVPR近年来最佳论文

update：2022/03/02  更新部分文章解读

#### 【0】CVPR2022录取结果公布
* [CVPR2022录用名单](./CVPR2022/Readme.md)
* 还在更新中....未完待续

---------------------
### 【1】CVPR2021录取结果公布
* 公众号【计算机视觉联盟】后台回复  CVPR2021   下载最新论文
* [CVPR 2021](./CVPR2021/README.md)
* [CVPR 2021所有录取文章](./CVPR2021/CVPR2021_accept_all_papers.md)

--------------

### 【2】CVPR2021最新更新论文

##### Fully Convolutional Networks for Panoptic Segmentation

本文旨在使用全卷积形式统一地表达和预测物体和周边环境，从而实现准确高效的全景分割。具体来说，本文提出卷积核生成器将每个物体和每类环境的语义信息编码至不同的卷结核中，并同高分辨率的特征图卷积直接输出每个前景和背景的分割结果。通过这种方法，物体和环境的个体差异和语义一致性可以被分别保留下来。该方法在多个全景分割数据集上均取得速度和精度的当前最佳结果。
👉关键词：统一表达，动态卷积，全景分割
arxiv: https://arxiv.org/abs/2012.00720
github: https://github.com/yanwei-li/PanopticFCN

oral论文
##### FFB6D: A Full Flow Bidirectional Fusion Network for 6D Pose Estimation
FFB6D提出一种网络全流双向融合的RGBD表征学习框架并应用于6D位姿估计问题。我们发现现有的表征学习方法都没能很好地利用RGB中的外观信息和深度图(点云)中的几何信息这两种互补的数据源。

对此，我们设计了一种双向稠密融合模块并应用到CNN和点云网络的每个编码和解码层。这种全流双向融合机制能让两个网络充分利用彼此提取的局部和全局互补信息，从而获得更好的表征用于下游预测任务。此外，在输出表征选择上，我们结合物品的纹理和几何信息设计了一种SIFT-FPS关键点选择算法，简化了网络定位关键点的难度并提升了位姿精度。我们的方法在多个基准上都获得显著的提升。并且这种RGBD表征学习骨干网络能通过级联不同的预测网络，应用在更多以RGBD为输入的视觉任务上。
👉关键词：RGBD表征学习，3D视觉，6D位姿估计
PDF: https://arxiv.org/abs/2103.02242
code: https://github.com/ethnhe/FFB6D


##### RepVGG: Making VGG-style ConvNets Great Again
科学技术总是螺旋式地上升。我们“复兴”了VGG式单路极简卷积神经网络架构，一路3x3卷到底，在速度和性能上达到SOTA水平，在ImageNet上超过80%正确率。

为了克服VGG式架构训练困难的问题，我们使用结构重参数化（structural re-parameterization）在训练时的模型中构造恒等映射和1x1卷积分支，然后在训练结束后将其等效融合进3x3卷积中去，因而推理时模型仅包含3x3卷积。这一架构没有任何分支结构，因此其并行度很高，速度很快。且由于主体部分仅有“3x3-ReLU”这一种算子，特别适合用于定制硬件。
👉关键词：结构重参数化，极简架构，高效模型
https://arxiv.org/abs/2101.03697


##### Dynamic Region-Aware Convolution
本文提出一种新的卷积操作----动态区域注意卷积（DRConv: Dynamic Region-Aware Convolution），该卷积可以根据特征相似度为不同平面区域分配定制的卷积核。这种卷积方式相较于传统卷积极大地增强了对图像语义信息多样性的建模能力。标准卷积层可以增加卷积核的数量以提取更多的视觉元素，但会导致较高的计算成本。DRConv使用可学习的分配器将逐渐增加的卷积核转移到平面维度，这不仅提高了卷积的表示能力，而且还保持了计算成本和平移不变性。

DRConv是一种用于处理语义信息分布复杂多变的有效而优雅的方法，它可以以其即插即用特性替代任何现有网络中的标准卷积，且对于轻量级网络的性能有显著提升。本文在各种模型（MobileNet系列，ShuffleNetV2等）和任务（分类，面部识别，检测和分割）上对DRConv进行了评估，在ImageNet分类中，基于DRConv的ShuffleNetV2-0.5×在46M计算量的水平下可实现67.1％的性能，相对基准提升6.3％。
https://arxiv.org/abs/2003.12243


##### Diverse Branch Block: Building a Convolution as an Inception-like Unit
我们提出一种卷积网络基本模块（DBB），用以丰富模型训练时的微观结构而不改变其宏观架构，以此提升其性能。这种模块可以在训练后通过结构重参数化（structural re-parameterization）等效转换为一个卷积，因而不引入任何额外的推理开销。图片

我们归纳了六种可以此种等效转换的结构，包括1x1-KxK连续卷积、average pooling等，并用这六种变换给出了一种代表性的形似Inception的DBB实例，在多种架构上均取得了显著的性能提升。我们通过实验确认了“训练时非线性”（而推理时是线性的，如BN）和“多样的链接”（比如1x1+3x3效果好于3x3+3x3）是DBB有效的关键。
👉关键词：结构重参数化，无推理开销，无痛提升


##### Generalized Few-Shot Object Detection without Forgetting

过去的工作大都聚焦在小类样本类别性能而牺牲了大类样本的性能。本文提出一种无遗忘效应的小类样本目标检测器，能够在实现更好的小类样本类别性能的同时，不掉落大类样本类别的性能。在本文中，我们发现了预训练的检测器很少在未见过的类别上产生假阳性预测，且还发现RPN并非理想的类别无关组件。基于这两点发现，我们设计了Re-detector和Bias-Balanced RPN两个简单而有效的结构，只增加少量参数和推断时间即可实现无遗忘效应的小类样本目标检测。
👉关键词：小样本学习，目标检测

##### Distribution Alignment: A Unified Framework for Long-tail Visual Recognition
本文提出了一个处理含有长尾数据分布的视觉识别任务的统一框架。我们首先针对现有的处理长尾问题的两阶段的方法进行了实验分析，找出现有方法主要的性能瓶颈。基于实验分析，我们提出了一种分布对齐策略来系统性解决长尾视觉任务。

该框架基于两阶段方法设计，在第一阶段，使用instance-balanced 采样策略进行特征表示学习(representation learning)。在第二阶段，我们首先设计了一个input-aware的对齐函数，以实现对输入数据的得分进行矫正。同时，为了引入数据集分布的先验，我们设计了一个泛化重加权(Generalized Re-weight)方案， 来处理图像分类，语义分割，物体检测和实例分割等多种视觉任务场景。我们在四个任务上验证了我们的方法，在各个任务上均取得了明显的性能提升。
👉关键词：图像分类，语义分割，物体检测，实例分割


##### End-to-End Object Detection with Fully Convolutional Network

本文首次在全卷积目标检测器上去除了NMS（非极大值抑制）后处理，做到了端到端训练。我们分析了主流一阶段目标检测方法，并发现传统的一对多标签分配策略是这些方法依赖NMS的关键，并由此提出了预测感知的一对一标签分配策略。此外，为了提升一对一标签分配的性能，我们提出了增强特征表征能力的模块，和加速模型收敛的辅助损失函数。我们的方法在无NMS的情况下达到了与主流一阶段目标检测方法相当的性能。在密集场景上，我们的方法的召回率超过了依赖NMS的目标检测方法的理论上限。
👉关键词：端到端检测，标签分配，全卷积网络
https://arxiv.org/abs/2012.03544


##### OTA: Optimal Transport Assignment for Object Detection

我们提出了一种基于最优传输理论的目标检测样本匹配策略，利用全局信息来寻找最优样本匹配的结果，相对于现有的样本匹配技术，具有如下优势：1). 检测精度高。全局最优的匹配结果能帮助检测器以稳定高效的方式训练，最终在COCO数据集上达到最优检测性能。2). 适用场景广。现有的目标检测算法在遇到诸如目标密集或被严重遮挡等复杂场景时，需要重新设计策略或者调整参数，而最优传输模型在全局建模的过程中包括了寻找最优解的过程，不用做任何额外的调整，在各种目标密集、遮挡严重的场景下也能达到最先进的性能，具有很大的应用潜力。
👉关键词：目标检测、最优传输、样本匹配策略


##### IQDet: Instance-wise Quality Distribution Sampling for Object Detection

由于一阶段检测器的标签分配有静态、没有考虑目标框的全局信息等不足，我们提出了一种基于目标质量分布采样的目标检测器。在本文中，我们提出质量分布编码模块QDE和质量分布采样模块QDS，通过提取目标框的区域特征，并基于高斯混合模型来对预测框的质量分布进行建模，来动态的选择检测框的正负样本分配。本方法只涉及训练阶段标签分配，就可以在COCO等多个数据集上实现当前最佳结果。
👉关键词：标签分配


##### FSCE: Few-Shot Object Detection via Contrastive Proposal Encoding

论文提出的FSCE方法旨在从优化特征表示的角度去解决小样本物体检测问题。小样本物体检测任务中受限于目标样本的数目稀少，对目标样本的分类正确与否往往对最终的性能有很大的影响。FSCE借助对比学习的思想对相关候选框进行编码优化其特征表示，加强特征的类内紧凑和类间相斥，最后方法在常见的COCO和Pascal VOC数据集上都得到有效提升。
👉关键词：小样本目标检测，对比学习
论文链接：https://arxiv.org/abs/2103.05950

* Neural Architecture Search with Random Labels

现有的主流NAS算法通过子网络在验证集上的预测性能来进行模型搜索，但是在参数共享机制下，验证集上的预测性能和模型真实性能存在较大的差异。我们首次打破了这种基于预测性能进行模型评估的范式，从模型收敛速度的角度来进行子网络评估并假设：模型收敛速度越快，其对应的预测性能越高。

基于模型收敛性框架，我们发现模型收敛性与图像真实标签无关，便进一步提出使用随机标签进行超网络训练的新NAS范式-RLNAS。RLNAS在多个数据集（NAS-Bench-201，ImageNet）以及多个搜索空间（DARTS，MobileNet-like）进行了验证，实验结果表明RLNAS仅使用随机标签搜索出来的结构便能达到现有的NAS SOTA的水平。RLNAS初听比较反直觉，但其出乎意料的好结果为NAS社区提出了一组更强的基线，同时也进一步启发了对NAS本质的思考。
👉关键词：神经网络架构搜索，模型收敛性假设，随机标签
https://arxiv.org/abs/2101.11834


* Rethinking the Heatmap Regression for Bottom-up Human Pose Estimation

目前人体姿态估计算法都是使用的热力图回归来得到最后的关节点。这些方法通常使用固定标准差的二维高斯核覆盖所有骨架关键点来构造真实热力图，并使用真实热力图来监督模型。由于不同人的关节点的真实热力图都是使用同一高斯核来构造，所以这一方法没有考虑不同人的尺度区别，会造成标签的歧义性，影响模型效果。

本论文提出了一种尺度自适应热力图回归，可以根据人体大小自适应生成构造标签所需的标准差，从而使得模型对不同尺度的人体更加鲁棒；并提出权重自适应回归平衡正负样本，进一步挖掘尺度自适应热力图回归效果。本论文最终在自底向上人体姿态估计中取得了目前最先进性能。
👉关键词：人体姿态估计、自底向上、自适应热力图回归
https://arxiv.org/abs/2012.15175
https://github.com/greatlog/SWAHR-HumanPose

* General Instance Distillation for Object Detection

GID提出了一种基于检测任务的新型蒸馏方法。通过从teacher和studnet中分别提取general instance (GI)，并提出GISM模块自适应选择差异大的instance进行feature-based、relation-based以及response-based蒸馏。本方法首次将关系型知识蒸馏应用于检测框架，且将蒸馏目标从独立考虑的正负样本蒸馏统一为更本质GI蒸馏，过程中不依赖于GT，且达到SOTA。
👉关键词：目标检测，知识蒸馏
https://arxiv.org/abs/2103.02340


* Activate or Not: Learning Customized Activation


我们提出一种新的激活函数ACON (activate or not)，可以自适应地学习激活与否。ACON建立了ReLU和Swish的联系：我们发现虽然两者形式很不一样，但Swish是ReLU的一种平滑形式。基于这个发现，我们进而提出更多变体，如meta-acon，相比于SENet取得了两倍的无cost涨点。我们在多个任务上验证了这个简洁有效的激活函数的泛化性能。
👉关键词：激活函数、神经网络
https://arxiv.org/abs/2009.04759


* You Only Look One-level Feature

在本文中，我们首先分析了FPN在单阶段检测器RetinaNet中的作用，通过实验发现FPN中将不同尺度的物体分配到不同层级检测的分治思想对检测结果影响很大。从优化角度来说，该思想将检测中的优化问题分解，使得优化学习变得更为简单，提高了检测精度。然而，FPN基于多层级特征的设计使得检测方法的网络结构变得复杂、引入了额外的计算量、并且拖慢了检测的速度。为了避免上述几个问题，本文提出在单层级上对所有尺度的物体进行检测；同时，针对单层级特征检测中难以优化的问题，提出了空洞编码器与均衡匹配的解决方案。

本文提出的基于单层级特征的检测器YOLOF，在只使用C5特征的情况下，其检测精度也能与基于FPN的RetinaNet相当，同时检测速度是RetinaNet的2.5倍。另外，与同样只使用C5特征的DETR相比，YOLOF能在收敛速度更快的情况下（7x）达到与之相当的性能。
   👉关键词：单阶段目标检测、单尺度特征、检测速度与精度平衡
https://arxiv.org/abs/2103.09460
https://github.com/megvii-model/YOLOF


* Points as Queries: Weakly Semi-supervised Object Detection by Points


在不增加标注成本的条件下，提升检测器的性能，是本文研究的目标。本文选择少量边界框辅以大量点标注的方式训练检测器。选择点标注是因其信息丰富：包含实例的位置和类别信息，同时标注成本低。本文通过将点编码器扩展至DETR的方式，提出Point DETR，整体框架为：通过边界框数据训练Point DETR；将点标注编码为查询，预测伪框；通过边界框和伪框数据，训练学生模型。在COCO数据集上，仅使用20%完全标注的数据，我们的检测器可达33.3AP，超过基线2.0AP。 
👉关键词：目标检测，半监督，弱监督



* Practical Wide-Angle Portraits Correction with Deep Structured Models


广角镜头因其广阔的视野而备受喜爱，但存在镜头畸变和透视失真问题，表现为背景线条弯曲、人脸拉伸挤压倾斜等。为此，本文构建了一个由线校正网络，人脸校正网络和过渡模块组成的级联去畸变网络，使得背景呈现透视投影而人脸区域呈现立体投影，并且在两个区域平滑过渡，从而在保持FOV的同时消除各种畸变。本方法不需要相机参数，可达到实时，定性和定量评估均超越了现有方法。
👉关键词：广角人像畸变校正，深度级联网络



* UPFlow:Upsampling Pyramid for Unsupervised Optical Flow Learning

我们提出了一种新的无监督光流学习方法UPFlow。我们发现目前的无监督光流方法在多尺度金字塔处理中有两个问题：flow上采样过程中存在插值模糊的问题和多尺度flow缺乏监督的问题。对此，我们提出来一种自引导的上采样模块，利用了一个插值flow和一个插值map来改变上采样插值的机制，从而实现了更加精细的上采样。另外，我们提出来将网络的最终输出结果作为伪标签来监督多尺度flow的学习。基于这些改进，我们的方法能够得到更加清晰、锐利的光流结果。我们在多个光流基准数据集上进行了实验，包括Sintel、KITTI 2012和KITTI 2015。UPFlow的性能比目前最好的无监督光流算法超出了约20%。
👉关键词：光流估计、无监督学习
https://arxiv.org/abs/2012.00212



* NBNet: Noise Basis Learning for Image Denoising with Subspace Projection


NBNet是一种解决图像降噪问题的框架。我们以一种新颖的观点来解决这个问题：图像自适应的投影。具体来说，我们学习一组特征空间上的子空间，图像降噪可以通过选择合适的信号子空间并往该子空间上投影来完成。相比于以往一卷到底的网络结构，NBNet通过投影，能自然且更高效地提取和利用图像中的结构信息，特别是弱纹理区域，以此来帮助我们复原图像。通过这样简单的方式，NBNet以更少的计算量在DND和SIDD两个benchmark上拿到了SOTA。
👉关键词：图像降噪，子空间
https://arxiv.org/abs/2012.15028



* Dynamic Metric Learning: Towards a Scalable Metric Space to Accommodate Multiple Semantic Scales

该工作将度量学中一个重要的属性“动态范围”引入到深度度量学习，从而得到一个新的任务叫做“动态度量学习”。我们发现，以往的深度度量其实只蕴含一个刻度，例如仅仅区分人脸、行人是相似还是不相似。这样的量具无论多精确，在实际使用中都是灵活不足、用途有限的。实际上，我们日常的量具通常具有动态范围，例如尺子总是有多个刻度（例如1mm、1cm乃至10cm）来测量不同尺度的物体。我们认为，深度度量学习领域已经到了需要引入动态范围的时候了。因为，视觉概念本身就有着不同的大小，“动物”、“植物”都对应大尺度，而“麋鹿”却对应相对较小的尺度。在小尺度下，两只麋鹿可能看上去很不一样，但是在另一个大尺度下，同样两只麋鹿却应该被认为非常相似。

为此，我们提出了这个动态度量学习任务，它要求学到一个单独的度量空间，能够同时为语义大小不同的视觉概念提供相似性度量。此外，我们还构建了三个多尺度数据集，并提出了一个简单的基准方法。我们相信，动态范围将成为深度度量学习不可或缺的属性，并为深度度量学习整个领域带来新的视角和新的应用场景。


* 3D Graph Anatomy Geometry-Integrated Network for Pancreatic Mass Segmentation, Diagnosis, and Quantitative Patient Management

* Deep Lesion Tracker: Monitoring Lesions in 4D Longitudinal Imaging Studies
https://arxiv.org/abs/2012.04872

* Automatic Vertebra Localization and Identification in CT by Spine Rectification and Anatomically-constrained Optimization
https://arxiv.org/abs/2012.07947

* 3D CNNs with Adaptive Temporal Feature Resolutions
https://arxiv.org/abs/2011.08652

* KeepAugment: A Simple Information-Preserving Data Augmentation
https://arxiv.org/pdf/2011.11778.pdf

* Hijack-GAN: Unintended-Use of Pretrained, Black-Box GANs
https://arxiv.org/pdf/2011.14107.pdf

* D-NeRF: Neural Radiance Fields for Dynamic Scenes
https://arxiv.org/abs/2011.13961

* Coarse-Fine Networks for Temporal Activity Detection in Videos

* Instance Localization for Self-supervised Detection Pretraining
https://arxiv.org/pdf/2102.08318.pdf
https://github.com/limbo0000/InstanceLoc

* Weakly-supervised Grounded Visual Question Answering using Capsules

* 4D Panoptic LiDAR Segmentation
https://arxiv.org/abs/2102.12472

* Dogfight: Detecting Drones from Drone Videos

* Multiple Instance Active Learning for Object Detection
https://github.com/yuantn/MIAL/raw/master/paper.pdf
https://github.com/yuantn/MIAL

* Reconsidering Representation Alignment for Multi-view Clustering

* Self-supervised Simultaneous Multi-Step Prediction of Road Dynamics and Cost Map

* Image-to-image Translation via Hierarchical Style Disentanglement
Xinyang Li, Shengchuan Zhang, Jie Hu, Liujuan Cao, Xiaopeng Hong, Xudong Mao, Feiyue Huang, Yongjian Wu, Rongrong Ji
https://arxiv.org/abs/2103.01456
https://github.com/imlixinyang/HiSD

* FLAVR: Flow-Agnostic Video Representations for Fast Frame Interpolation
https://arxiv.org/pdf/2012.08512.pdf
https://tarun005.github.io/FLAVR/Code
https://tarun005.github.io/FLAVR/

* Patch-NetVLAD: Multi-Scale Fusion of Locally-Global Descriptors for Place Recognition
Stephen Hausler, Sourav Garg, Ming Xu, Michael Milford, Tobias Fischer
https://arxiv.org/abs/2103.01486

* Depth from Camera Motion and Object Detection
Brent A. Griffin, Jason J. Corso
https://arxiv.org/abs/2103.01468

* UP-DETR: Unsupervised Pre-training for Object Detection with Transformers
https://arxiv.org/pdf/2011.09094.pdf

* Multi-Stage Progressive Image Restoration
https://arxiv.org/abs/2102.02808
https://github.com/swz30/MPRNet

* Weakly Supervised Learning of Rigid 3D Scene Flow
https://arxiv.org/pdf/2102.08945.pdf
https://arxiv.org/pdf/2102.08945.pdf
https://3dsceneflow.github.io/

* Exploring Complementary Strengths of Invariant and Equivariant Representations for Few-Shot Learning
Mamshad Nayeem Rizve, Salman Khan, Fahad Shahbaz Khan, Mubarak Shah
https://arxiv.org/abs/2103.01315

* Re-labeling ImageNet: from Single to Multi-Labels, from Global to Localized Labels
https://arxiv.org/abs/2101.05022
https://github.com/naver-ai/relabel_imagenet

* Rethinking Channel Dimensions for Efficient Model Design
https://arxiv.org/abs/2007.00992
https://github.com/clovaai/rexnet

* Coarse-Fine Networks for Temporal Activity Detection in Videos
Kumara Kahatapitiya, Michael S. Ryoo
https://arxiv.org/abs/2103.01302

* A Deep Emulator for Secondary Motion of 3D Characters
Mianlun Zheng, Yi Zhou, Duygu Ceylan, Jernej Barbic
https://arxiv.org/abs/2103.01261

* Fair Attribute Classification through Latent Space De-biasing
https://arxiv.org/abs/2012.01469
https://github.com/princetonvisualai/gan-debiasing
https://princetonvisualai.github.io/gan-debiasing/

* Auto-Exposure Fusion for Single-Image Shadow Removal
Lan Fu, Changqing Zhou, Qing Guo, Felix Juefei-Xu, Hongkai Yu, Wei Feng, Yang Liu, Song Wang
https://arxiv.org/abs/2103.01255

* Less is More: CLIPBERT for Video-and-Language Learning via Sparse Sampling
https://arxiv.org/pdf/2102.06183.pdf
https://github.com/jayleicn/ClipBERT

* MetaSCI: Scalable and Adaptive Reconstruction for Video Compressive Sensing
Zhengjue Wang, Hao Zhang, Ziheng Cheng, Bo Chen, Xin Yuan
https://arxiv.org/abs/2103.01786

* AttentiveNAS: Improving Neural Architecture Search via Attentive
https://arxiv.org/pdf/2011.09011.pdf

* Diffusion Probabilistic Models for 3D Point Cloud Generation
Shitong Luo, Wei Hu
https://arxiv.org/abs/2103.01458

* There is More than Meets the Eye: Self-Supervised Multi-Object Detection and Tracking with Sound by Distilling Multimodal Knowledge
Francisco Rivera Valverde, Juana Valeria Hurtado, Abhinav Valada
https://arxiv.org/abs/2103.01353
http://rl.uni-freiburg.de/research/multimodal-distill

* Encoding in Style: a StyleGAN Encoder for Image-to-Image Translation
https://arxiv.org/abs/2008.00951
https://github.com/eladrich/pixel2style2pixel
https://eladrich.github.io/pixel2style2pixel/

* Hierarchical and Partially Observable Goal-driven Policy Learning with Goals Relational Graph
Xin Ye, Yezhou Yang
https://arxiv.org/abs/2103.01350

* RepVGG: Making VGG-style ConvNets Great Again
https://arxiv.org/abs/2101.03697
https://github.com/megvii-model/RepVGG

* Transformer Interpretability Beyond Attention Visualization
https://arxiv.org/pdf/2012.09838.pdf
https://github.com/hila-chefer/Transformer-Explainability

* PREDATOR: Registration of 3D Point Clouds with Low Overlap
https://arxiv.org/pdf/2011.13005.pdf
https://github.com/ShengyuH/OverlapPredator
https://overlappredator.github.io/

* Multiresolution Knowledge Distillation for Anomaly Detection
https://arxiv.org/abs/2011.11108

* Positive-Unlabeled Data Purification in the Wild for Object Detection

* Data-Free Knowledge Distillation For Image Super-Resolution

* Manifold Regularized Dynamic Network Pruning

* Pre-Trained Image Processing Transformer
https://arxiv.org/pdf/2012.00364.pdf

* ReNAS: Relativistic Evaluation of Neural Architecture Search
https://arxiv.org/pdf/1910.01523.pdf

* AdderSR: Towards Energy Efficient Image Super-Resolution
https://arxiv.org/pdf/2009.08891.pdf
https://github.com/huawei-noah/AdderNet

* Learning Student Networks in the Wild
https://arxiv.org/pdf/1904.01186.pdf
https://github.com/huawei-noah/DAFL
https://www.zhihu.com/question/446299297

* HourNAS: Extremely Fast Neural Architecture Search Through an Hourglass Lens
https://arxiv.org/pdf/2005.14446.pdf

* Probabilistic Embeddings for Cross-Modal Retrieval
https://arxiv.org/abs/2101.05068

* PLOP: Learning without Forgetting for Continual Semantic Segmentation
https://arxiv.org/abs/2011.11390

* Rainbow Memory: Continual Learning with a Memory of Diverse Samples

* Exploiting Spatial Dimensions of Latent in GAN for Real-time Image Editing




----------------
### 【3】CVPR2020、2019、2018、2017下载链接

## CVPR 2020
* 公众号【计算机视觉联盟】后台回复  CVPR2020   下载最新论文
* [CVPR 2020](./CVPR2020/README.md)

## CVPR 2019
* [CVPR 2019 Paper List ](./CVPR%202019/CVPR%202019%20Paper%20List)
* [CVPR 2019 Paper](./CVPR%202019/CVPR%202019%20Paper)

## CVPR 2018
* [CVPR 2018 Paper List ](./CVPR%202018/CVPR%202018%20Paper%20List)
* [CVPR 2018 Paper](./CVPR%202018/CVPR%202018%20Paper)

## CVPR 2017
* [CVPR 2017 Paper List ](./CVPR%202017/CVPR%202017%20PaperList)
* [CVPR 2017 Paper](./CVPR%202017/CVPR%202017%20Paper)

## CVPR 2020
1.GhostNet: More Features from Cheap Operations（超越Mobilenet v3的架构）
论文链接：https://arxiv.org/pdf/1911.11907arxiv.org
模型（在ARM CPU上的表现惊人）：https://github.com/iamhankai/ghostnetgithub.com

We beat other SOTA lightweight CNNs such as MobileNetV3 and FBNet.

2. AdderNet: Do We Really Need Multiplications in Deep Learning? （加法神经网络）
在大规模神经网络和数据集上取得了非常好的表现
论文链接：https://arxiv.org/pdf/1912.13200arxiv.org

3. Frequency Domain Compact 3D Convolutional Neural Networks （3dCNN压缩）
论文链接：https://arxiv.org/pdf/1909.04977arxiv.org
开源代码：https://github.com/huawei-noah/CARSgithub.com

4. A Semi-Supervised Assessor of Neural Architectures （神经网络精度预测器 NAS）

5. Hit-Detector: Hierarchical Trinity Architecture Search for Object Detection （NAS 检测）
backbone-neck-head一起搜索， 三位一体

6. CARS: Contunuous Evolution for Efficient Neural Architecture Search (连续进化的NAS)
高效，具备可微和进化的多重优势，且能输出帕累托前研

7. On Positive-Unlabeled Classification in GAN （PU+GAN）

8. Learning multiview 3D point cloud registration（3D点云）
论文链接：arxiv.org/abs/2001.05119

9. Multi-Modal Domain Adaptation for Fine-Grained Action Recognition（细粒度动作识别）
论文链接：arxiv.org/abs/2001.09691

10. Action Modifiers:Learning from Adverbs in Instructional Video
论文链接：arxiv.org/abs/1912.06617

11. PolarMask: Single Shot Instance Segmentation with Polar Representation（实例分割建模）
论文链接：arxiv.org/abs/1909.13226
论文解读：https://zhuanlan.zhihu.com/p/84890413
开源代码：https://github.com/xieenze/PolarMask

12. Rethinking Performance Estimation in Neural Architecture Search（NAS）
由于block wise neural architecture search中真正消耗时间的是performance estimation部分，本文针对 block wise的NAS找到了最优参数，速度更快，且相关度更高。

13. Distribution Aware Coordinate Representation for Human Pose Estimation（人体姿态估计）
论文链接：arxiv.org/abs/1910.06278
Github：https://github.com/ilovepose/DarkPose
作者团队主页：https://ilovepose.github.io/coco/

### 更新

1. 视觉常识R-CNN，Visual Commonsense R-CNN

https://arxiv.org/abs/2002.12204


2. Out-of-distribution图像检测

https://arxiv.org/abs/2002.11297


3. 模糊视频帧插值，Blurry Video Frame Interpolation

https://arxiv.org/abs/2002.12259


4. 元迁移学习零样本超分

https://arxiv.org/abs/2002.12213

5. 3D室内场景理解

https://arxiv.org/abs/2002.12212



6.从有偏训练生成无偏场景图

https://arxiv.org/abs/2002.11949



7. 自动编码双瓶颈哈希

https://arxiv.org/abs/2002.11930

8. 一种用于人类轨迹预测的社会时空图卷积神经网络

https://arxiv.org/abs/2002.11927


9. 面向面向深度人脸识别的通用表示学习

https://arxiv.org/abs/2002.11841


10. 视觉表示泛化性

https://arxiv.org/abs/1912.03330


11. 减弱上下文偏差

https://arxiv.org/abs/2002.11812


12. 可迁移元技能的无监督强化学习

https://arxiv.org/abs/1911.07450


13. 快速准确时空视频超分

https://arxiv.org/abs/2002.11616


14. 对象关系图Teacher推荐学习的视频captioning

https://arxiv.org/abs/2002.11566


15. 弱监督物体定位路由再思考

https://arxiv.org/abs/2002.11359


16. 通过预培训学习视觉和语言导航的通用代理

https://arxiv.org/pdf/2002.10638.pdf


17. GhostNet轻量级神经网络

https://arxiv.org/pdf/1911.11907.pdf



18. AdderNet:在深度学习中，我们真的需要乘法吗?

https://arxiv.org/pdf/1912.13200.pdf


19. CARS:高效神经结构搜索的持续进化

https://arxiv.org/abs/1909.04977


20. 通过协作式的迭代级联微调来移除单图像中的反射

https://arxiv.org/abs/1911.06634


21. 深度神经网络的滤波嫁接

https://arxiv.org/pdf/2001.05868.pdf


22.  PolarMask：将实例分割统一到FCN

https://arxiv.org/pdf/1909.13226.pdf


23. 半监督语义图像分割

https://arxiv.org/pdf/1811.07073.pdf



24. 通过选择性的特征再生来抵御通用攻击

https://arxiv.org/pdf/1906.03444.pdf


25. 实时的基于细粒度草图的图像检索

https://arxiv.org/abs/2002.10310


26. 用子问题询问VQA模型

https://arxiv.org/abs/1906.03444


27. 从2D范例中学习神经三维纹理空间

https://geometry.cs.ucl.ac.uk/projects/2020/neuraltexture/


28. NestedVAE:通过薄弱的监督来隔离共同因素

https://arxiv.org/abs/2002.11576


29. 实现多未来轨迹预测

https://arxiv.org/pdf/1912.06445.pdf



30. 使用序列注意力模型进行稳健的图像分类

https://arxiv.org/pdf/1912.02184







# 【4】CVPR近年来最佳论文

<tbody><tr><td rowspan="1"><b>2018</b></td><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=Taskonomy:+Disentangling+Task+Transfer+Learning&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=Zamir">Taskonomy: Disentangling Task Transfer Learning</a></td><td>Amir R. Zamir, Stanford University<a href="#" onclick="this.nextSibling.style.display = 'block'; this.style.display = 'none'; return false;">; et al.</a><div>Alexander Sax, Stanford University<br>William Shen, Stanford University<br>Leonidas Guibas, Stanford University<br>Jitendra Malik, University of California Berkeley<br>Silvio Savarese, Stanford University</div></td></tr><tr><td rowspan="2"><b>2017</b></td><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=Densely+Connected+Convolutional+Networks&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=Liu">Densely Connected Convolutional Networks</a></td><td>Zhuang Liu, Tsinghua University<a href="#" onclick="this.nextSibling.style.display = 'block'; this.style.display = 'none'; return false;">; et al.</a><div>Gao Huang, Cornell University<br>Laurens van der Maaten, Facebook AI Research<br>Kilian Q. Weinberger, Cornell University</div></td></tr><tr><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=Learning+from+Simulated+and+Unsupervised+Images+through+Adversarial+Training&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=Shrivastava">Learning from Simulated and Unsupervised Images through Adversarial Training</a></td><td>Ashish Shrivastava, Apple Inc.<a href="#" onclick="this.nextSibling.style.display = 'block'; this.style.display = 'none'; return false;">; et al.</a><div>Tomas Pfister, Apple Inc.<br>Oncel Tuzel, Apple Inc.<br>Josh Susskind, Apple Inc.<br>Wenda Wang, Apple Inc.<br>Russ Webb, Apple Inc.</div></td></tr><tr><td rowspan="1"><b>2016</b></td><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=Deep+Residual+Learning+for+Image+Recognition&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=He">Deep Residual Learning for Image Recognition</a></td><td>Kaiming He, Microsoft Research<a href="#" onclick="this.nextSibling.style.display = 'block'; this.style.display = 'none'; return false;">; et al.</a><div>Xiangyu Zhang, Microsoft Research<br>Shaoqing Ren, Microsoft Research<br>Jian Sun, Microsoft Research</div></td></tr><tr><td rowspan="1"><b>2015</b></td><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=DynamicFusion:+Reconstruction+and+Tracking+of+Non-rigid+Scenes+in+Real-Time&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=Newcombe">DynamicFusion: Reconstruction and Tracking of Non-rigid Scenes in Real-Time</a></td><td>Richard A. Newcombe, University of Washington<a href="#" onclick="this.nextSibling.style.display = 'block'; this.style.display = 'none'; return false;">; et al.</a><div>Dieter Fox, University of Washington<br>Steven M. Seitz, University of Washington</div></td></tr><tr><td rowspan="1"><b>2014</b></td><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=What+Camera+Motion+Reveals+About+Shape+with+Unknown+BRDF&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=Chandraker">What Camera Motion Reveals About Shape with Unknown BRDF</a></td><td>Manmohan Chandraker, NEC Labs America</td></tr><tr><td rowspan="1"><b>2013</b></td><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=Fast,+Accurate+Detection+of+100,000+Object+Classes+on+a+Single+Machine&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=Dean">Fast, Accurate Detection of 100,000 Object Classes on a Single Machine</a></td><td>Thomas Dean, Google<a href="#" onclick="this.nextSibling.style.display = 'block'; this.style.display = 'none'; return false;">; et al.</a><div>Mark A. Ruzon, Google<br>Mark Segal, Google<br>Jonathon Shlens, Google<br>Sudheendra Vijayanarasimhan, Google<br>Jay Yagnik, Google</div></td></tr><tr><td rowspan="1"><b>2012</b></td><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=A+Simple+Prior-free+Method+for+Non-Rigid+Structure-from-Motion+Factorization&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=Dai">A Simple Prior-free Method for Non-Rigid Structure-from-Motion Factorization</a></td><td>Yuchao Dai, Northwestern Polytechnical University<a href="#" onclick="this.nextSibling.style.display = 'block'; this.style.display = 'none'; return false;">; et al.</a><div>Hongdong Li, Australian National University<br>Mingyi He, Northwestern Polytechnical University</div></td></tr><tr><td rowspan="1"><b>2011</b></td><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=Real-time+Human+Pose+Recognition+in+Parts+from+Single+Depth+Images&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=Shotton">Real-time Human Pose Recognition in Parts from Single Depth Images</a></td><td>Jamie Shotton, Microsoft Research<a href="#" onclick="this.nextSibling.style.display = 'block'; this.style.display = 'none'; return false;">; et al.</a><div>Andrew Fitzgibbon, Microsoft Research<br>Mat Cook, Microsoft Research<br>Toby Sharp, Microsoft Research<br>Mark Finocchio, Microsoft Research<br>Richard Moore, Microsoft Research<br>Alex Kipman, Microsoft Research<br>Andrew Blake, Microsoft Research</div></td></tr><tr><td rowspan="1"><b>2010</b></td><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=Efficient+Computation+of+Robust+Low-Rank+Matrix+Approximations+in+the+Presence+of+Missing+Data+using+the+L1+Norm&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=Eriksson">Efficient Computation of Robust Low-Rank Matrix Approximations in the Presence of Missing Data usi...</a></td><td>Anders Eriksson &amp; Anton va den Hendel, University of Adelaide</td></tr><tr><td rowspan="1"><b>2009</b></td><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=Single+Image+Haze+Removal+Using+Dark+Channel+Prior&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=He">Single Image Haze Removal Using Dark Channel Prior</a></td><td>Kaiming He, The Chinese University of Hong Kong<a href="#" onclick="this.nextSibling.style.display = 'block'; this.style.display = 'none'; return false;">; et al.</a><div>Jian Sun, Microsoft Research<br>Xiaoou Tang, The Chinese University of Hong Kong</div></td></tr><tr><td rowspan="2"><b>2008</b></td><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=Global+Stereo+Reconstruction+under+Second+Order+Smoothness+Priors&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=Woodford">Global Stereo Reconstruction under Second Order Smoothness Priors</a></td><td>Oliver Woodford, University of Oxford<a href="#" onclick="this.nextSibling.style.display = 'block'; this.style.display = 'none'; return false;">; et al.</a><div>Ian Reid, Oxford Brookes University<br>Philip Torr, University of Oxford<br>Andrew Fitzgibbon, Microsoft Research</div></td></tr><tr><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=Beyond+Sliding+Windows:+Object+Localization+by+Efficient+Subwindow+Search&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=Lampert">Beyond Sliding Windows: Object Localization by Efficient Subwindow Search</a></td><td>Chistoph H. Lampert, Max Planck Institut<a href="#" onclick="this.nextSibling.style.display = 'block'; this.style.display = 'none'; return false;">; et al.</a><div>Matthew B. Blaschko, Max Planck Institut<br>Thomas Hodmann, Google</div></td></tr><tr><td rowspan="1"><b>2007</b></td><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=Dynamic+3D+Scene+Analysis+from+a+Moving+Vehicle&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=Leibe">Dynamic 3D Scene Analysis from a Moving Vehicle</a></td><td>Bastian Leibe, ETH Zurich<a href="#" onclick="this.nextSibling.style.display = 'block'; this.style.display = 'none'; return false;">; et al.</a><div>Nico Cornelis, Katholieke Universiteit Leuven<br>Kurt COrnelis, Katholieke Universiteit Leuven<br>Luc Van Gool, ETH Zurich</div></td></tr><tr><td rowspan="1"><b>2006</b></td><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=Putting+Objects+in+Perspective&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=Hoiem">Putting Objects in Perspective</a></td><td>Derek Hoiem, Carnegie Mellon University<a href="#" onclick="this.nextSibling.style.display = 'block'; this.style.display = 'none'; return false;">; et al.</a><div>Alexei Efros, Carnegie Mellon University<br>Martial Hebert, Carnegie Mellon University</div></td></tr><tr><td rowspan="1"><b>2005</b></td><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=Real-Time+Non-Rigid+Surface+Detection&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=Pilet">Real-Time Non-Rigid Surface Detection</a></td><td>Julien Pilet, École Polytechnique Fédérale de Lausanne<a href="#" onclick="this.nextSibling.style.display = 'block'; this.style.display = 'none'; return false;">; et al.</a><div>Vincent Lepetit, École Polytechnique Fédérale de Lausanne<br>Pascal Fua, École Polytechnique Fédérale de Lausanne</div></td></tr><tr><td rowspan="1"><b>2004</b></td><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=Programmable+Imaging+using+a+Digital+Micromirror+Array&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=Nayar">Programmable Imaging using a Digital Micromirror Array</a></td><td>Shree K. Nayar, Columbia University<a href="#" onclick="this.nextSibling.style.display = 'block'; this.style.display = 'none'; return false;">; et al.</a><div>Vlad Branzoi, Columbia University<br>Terry E. Boult, University of Colorado</div></td></tr><tr><td rowspan="1"><b>2003</b></td><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=Object+Class+Recognition+by+Unsupervised+Scale-Invariant+Learning&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=Fergus">Object Class Recognition by Unsupervised Scale-Invariant Learning</a></td><td>Rob Fergus, University of Oxford<a href="#" onclick="this.nextSibling.style.display = 'block'; this.style.display = 'none'; return false;">; et al.</a><div>Pietro Perona, California Institute of Technology<br>Andrew Zisserman, University of Oxford</div></td></tr><tr><td rowspan="1"><b>2001</b></td><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=Morphable+3D+models+from+video&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=Brand">Morphable 3D models from video</a></td><td>Matthew Brand, Mitsubishi Electric Research Laboratories</td></tr><tr><td rowspan="1"><b>2000</b></td><td><a href="http://scholar.google.com/scholar?as_q=&amp;num=10&amp;btnG=Search+Scholar&amp;as_epq=Real-Time+Tracking+of+Non-Rigid+Objects+using+Mean+Shift&amp;as_oq=&amp;as_eq=&amp;as_occt=any&amp;as_sauthors=Comaniciu">Real-Time Tracking of Non-Rigid Objects using Mean Shift</a></td><td>Dorin Comaniciu, Siemens Corporate Research<a href="#" onclick="this.nextSibling.style.display = 'block'; this.style.display = 'none'; return false;">; et al.</a><div>Visvanathan Ramesh, Siemens Corporate Research<br>Peter Meer, Rutgers University</div></td></tr></tbody>
