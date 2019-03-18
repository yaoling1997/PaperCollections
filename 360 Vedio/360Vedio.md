##[Google Jump](https://ai.google/research/pubs/pub45617)
<img src="https://i.loli.net/2019/03/18/5c8ef729e427a.png" alt="1.png" title="1.png" />
omnidirectional stereo (ODS) video(全景立体视频)
mosaicing(图像拼接)
elevation（仰角）
azimuth（方位角）
Jump是一个完整的VR捕捉系统，一个最优化捕捉真实场景和事件的为VR头显和视频服务的平台。
有以下三个评判准则：
1.观看者能感觉置身于捕捉的场景中
2.观看者能看到立体的视频
3.视频流可以被现有工具编辑，在头显中被实时渲染
遇到的挑战：
1.ods投影不是为vr设计的。比如ods在重新投影到VR头显的透视图时是违反[极线约束(epipolar constraint)](https://blog.csdn.net/ccblogger/article/details/72900316)的，然而偏差是很小的，并且只有在非常近的物体和极端的角度的时候偏差才会很大
2.如何设计相机和缝合系统来制作ods视频。我们提出了只用现成相机就能组成的环状ods相机系统
<img src="https://i.loli.net/2019/03/18/5c8f308b9a8f3.png" alt="1_1.png" title="1_1.png" />
将ods全景图渲染到透视图，需要将ods全景图上的每一条光线投影到场景的几何体再映射到透视图上。
我们可以使用由一个无限球体组成的代理几何体，这与只考虑方向不考虑原点是等价的，但是只对远距离内容有效，近距离物体会有扭曲
<img src="https://i.loli.net/2019/03/18/5c8f2f20d2e0f.png" alt="2.png" title="2.png" />
<img src="https://i.loli.net/2019/03/18/5c8f311bdecaf.png" alt="3.png" title="3.png" />
画面的垂直扭曲
<img src="https://i.loli.net/2019/03/18/5c8f3470d94db.png" alt="4.png" title="4.png" />
<img src="https://i.loli.net/2019/03/18/5c8f347056455.png" alt="5.png" title="5.png" />
可以通过减小相机和ODS viewing circle的距离来减小扭曲程度
两种不同的相机布局：
第一种，一半的相机捕捉通过左眼的光线，另一半捕捉通过右眼的，所需支架更小
第二种，每个相机捕捉通过左右眼的光线，所需支架更大
<img src="https://i.loli.net/2019/03/18/5c8f37ee32b03.png" alt="6.png" title="6.png" />
接下来的讨论都是基于第二种的
支架几何体由支架半径R、水平视野γ和相机个数n组成
<img src="https://i.loli.net/2019/03/18/5c8f3dc279c8e.png" alt="7.png" title="7.png" />
<img src="https://i.loli.net/2019/03/18/5c8f3dc2939ac.png" alt="8.png" title="8.png" />
缝合图像的流程：
<img src="https://i.loli.net/2019/03/18/5c8f3e171cf3f.png" alt="9.png" title="9.png" />
缝合算法必须处理大量的数据
输入是16个2704*2028 30 FPS的视频流，输出是一个8192*8192的视频流(单眼是8192*4096，左眼在右眼上面)，在一台机器上跑每一帧(包含16张图)要花60s处理，也就是说一个小时的视频要花75天处理。为了能够实时处理我们用了很多机器，即便是这样一个小时的视频也要花大约10小时处理
<img src="https://i.loli.net/2019/03/18/5c8f460d66c68.png" alt="10.png" title="10.png" />
16个摄像头环状分布
水平360°画面，垂直120°画面
##拓展延伸
[最详细的Google Jump原理解读](http://www.360doc.com/content/17/0530/17/11604731_658493279.shtml)
