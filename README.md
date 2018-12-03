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