# PaperCollections
##Methodology for Assessing Mesh-Based Contact Point Methods

1.基于三维物体网格，给出了一种接触点的定义方式：三维坐标、法向量、穿透程度。

2.给出了8种接触点计算方法。

3.用于仿真模拟三维物体接触场景。

##Shape2Pose Human-Centric Shape Analysis

给定一个三维形状，算法能够预测一个人的姿势。输入一个模型，将表面区域分类为潜在的接触点（较暗的颜色表示较高的置信度），找到人的骨架的末端感受器的概率分布，找到最佳的姿势。

##Inferring Forces and Learning Human Utilities From Videos

论文贡献：1.在人和物体交互过程中用基于物理的柔体动力学模拟去推断看不见的物理量（力和压强）。2.给定由RGB-D传感器获得的静态场景，我们提出的架构思考了相关的物理学知识为了综合创造性的，物理稳定的坐在对象上的方式。3.通过结合传统的机器路径规划，我们的架构可以生成一个静态坐姿再推广到动态运动序列。4.通过人的演示，我们的系统学会了如何生成人体各部分力的直方图，从而有效定义了人类效用，例如根据身体各部分的力来定义舒适性。5.提供了一种生成人体模型的方法

##Reasoning about Object Affordances

使用MLN(Markov Logic Network)学习一个知识库(KB)。给定学习的知识库，展示一系列视觉推断任务能通过不训练独特的分类器的方式被统一的框架解决。推断任务包括可供性预测以及人体姿态的对象识别。

#CVPR2018

begin

##Weakly and Semi Supervised Human Body Part Parsing via Pose-Guided Knowledge Transfer

二维rgb图像+骨架->人体各个部位分割

##A Papier-Mach ˆ e Approach to Learning 3D Surface Generation

基于单张rgb图像或三维点云生成物体的三维网格（效果不是特别好）

##Real-Time Seamless Single Shot 6D Object Pose Prediction

输入单张rgb图像，检测图中物体并给出该物体的六个自由度的预测结果

##Single-Image Depth Estimation Based on Fourier Domain Analysis

输入单张rgb图像，预测图像的深度信息

##Learning to Estimate 3D Human Pose and Shape from a Single Color Image

单张rgb图像，基于smpl模型预测人体三维姿势

##Deep Extreme Cut From Extreme Points to Object Segmentation

输入单张rgb图像，分割出里面的物体

##PAD-Net Multi-Tasks Guided Prediction-and-Distillation Network

输入单张rgb图像，输出场景分割和深度估计结果

##Recurrent Scene Parsing with Perspective Understanding in the Loop

输入单张rgb图像给出深度预测

##Human Semantic Parsing for Person Re-identification

输入rgb图像，给出像素级的人的各部位分割

##Multi-Evidence Filtering and Fusion for Multi-Label Classification, Object Detection and

输入rgb图像，输出物体的定位结果和划分结果

##Bootstrapping the Performance of Webly Supervised Semantic Segmentation

输入rgb图像，输出物体的划分结果

##A Bi-directional Message Passing Model for Salient Object Detection

输入rgb图像，输出物体的特征图结果（突出对象的检测结果）

##Matryoshka Networks Predicting 3D Geometry via Nested Shape Layers

输入单个对象的rgb图像，给出该对象三维物体重建结果

##Deep Ordinal Regression Network for Monocular Depth Estimation

输入rgb图像，输出深度预测结果

##MegaDepth Learning Single-View Depth Prediction from Internet Photos

输入rgb图像，输出深度预测结果

##Monocular 3D Pose and Shape Estimation of Multiple People in Natural Scenes

输入rgb图像，给出人各部位的划分，再建出人体三维模型

##AdaDepth Unsupervised Content Congruent Adaptation for Depth Estimation

输入rgb图像，给出深度估计

##Pix3D Dataset and Methods for Single-Image 3D Shape Modeling

输入rgb图像，检索图像中物体对应的三维模型并给出该模型的位姿估计(将三维模型与图像中的物体对齐)

##3D Pose Estimation and 3D Model Retrieval for Objects in the Wild

输入rgb图像，检索图像中物体对应的三维模型并给出该模型的位姿估计(将三维模型与图像中的物体对齐)

##3D-RCNN Instance-level 3D Object Reconstruction via Render-and-Compare

输入rgb图像，重建出人体模型和三维物体模型

##Structured Attention Guided Convolutional Neural Fields for Monocular Depth Estimation

输入rgb图像，给出深度预测

##MaskLab Instance Segmentation by Refining Object Detection with Semantic

输入rgb图像，给出人和物体的划分结果

##Learning to Segment Every Thing

输入rgb图像，划分出所有的人和物（像素级）

##Im2Struct Recovering 3D Shape Structure from a Single RGB Image

输入含单个物体的rgb图像，用基本的几何体构建该物体三维模型

##Trust your Model Light Field Depth Estimation with inline Occlusion Handling

输入rgb图像，给出深度预测

##3D Human Pose Estimation in the Wild by Adversarial Learning

输入rgb图像，给出人的三维骨架预测结果

##Aperture Supervision for Monocular Depth Estimation

输入rgb图像，给出深度估计

##Dense Decoder Shortcut Connections for Single-Pass Semantic Segmentation

输入rgb图像，给出对象的语义分割(分割出图像中的物体，像素级)

##Fully Convolutional Adaptation Networks for Semantic Segmentation

输入rgb图像，给出对象的语义分割(分割出图像中的物体，像素级)

##End-to-end Recovery of Human Shape and Pose

输入rgb图像，估计出对应的三维人体模型，并给出图像上人各个部位的划分

##Context Encoding for Semantic Segmentation

输入rgb图像，给出对象的语义分割(分割出图像中的物体，像素级)

##Ordinal Depth Supervision for 3D Human Pose Estimation

输入rgb图像，给出人体三维骨架预测

##Multi-Task Learning Using Uncertainty to Weigh Losses

输入rgb图像，分割出图像中的物体并给出图的深度预测

##Path Aggregation Network for Instance Segmentation

输入rgb图像，给出对象的语义分割(分割出图像中的物体，像素级)

end