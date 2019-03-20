##[Google Jump](https://ai.google/research/pubs/pub45617)
可以拍3d全景视频
16个摄像头环状分布
水平360°画面，垂直120°画面
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
支架几何体的参数由支架半径R、水平视野γ和相机个数n组成
<img src="https://i.loli.net/2019/03/18/5c8f3dc279c8e.png" alt="7.png" title="7.png" />
<img src="https://i.loli.net/2019/03/18/5c8f3dc2939ac.png" alt="8.png" title="8.png" />
缝合图像的流程：
<img src="https://i.loli.net/2019/03/18/5c8f3e171cf3f.png" alt="9.png" title="9.png" />
缝合算法必须处理大量的数据
输入是16个2704\*2028 30 FPS的视频流，输出是一个8192\*8192的视频流(单眼是8192\*4096，左眼在右眼上面)，在一台机器上跑每一帧(包含16张图)要花60s处理，也就是说一个小时的视频要花75天处理。为了能够实时处理我们用了很多机器，即便是这样一个小时的视频也要花大约10小时处理
<img src="https://i.loli.net/2019/03/18/5c8f460d66c68.png" alt="10.png" title="10.png" />

##[Facebook Surround360](https://code.fb.com/video-engineering/introducing-facebook-surround-360-an-open-high-quality-3d-360-video-capture-system/)
<img src="https://i.loli.net/2019/03/18/5c8f508b02265.png" alt="1.png" title="1.png" />
[github](https://github.com/facebook/Surround360)
可以拍3d全景视频
侧边由14个相机围成的圆盘阵列组成，顶部有一个[鱼眼镜头](https://baike.baidu.com/item/鱼眼镜头/343506?fr=aladdin)，底部有两个鱼眼镜头，所以可以呈现出360°无死角三维全景图。
##[Facebook x6 x24](https://www.immersiveshooter.com/2017/04/19/facebook-announces-two-new-volumetric-video-cameras-launch-2017/)
<img src="https://i.loli.net/2019/03/18/5c8f57ca50764.png" alt="2.png" title="2.png" />
2017年4月就已亮相，支持用户体验六自由度的视频内容[(视频演示，需翻墙)](https://www.youtube.com/watch?v=Ho2BbFN2owQ)，然而直到现在都没有新的消息，应该是还不够成熟吧。

##拓展延伸
[最详细的Google Jump原理解读](http://www.360doc.com/content/17/0530/17/11604731_658493279.shtml)
[google jump](https://ai.google/research/pubs/pub45617)
[facebook360](https://facebook360.fb.com/)
[由FaceBook总结的关于VR AR的术语](https://facebook360.fb.com/glossary/)
[Introducing Facebook Surround 360: An open, high-quality 3D-360 video capture system](https://code.fb.com/video-engineering/introducing-facebook-surround-360-an-open-high-quality-3d-360-video-capture-system/)
[Facebook Surround360 学习笔记--（1）系统简介](https://blog.csdn.net/electech6/article/details/53618965)
[Facebook announces two new volumetric video cameras to launch in 2017](https://www.immersiveshooter.com/2017/04/19/facebook-announces-two-new-volumetric-video-cameras-launch-2017/)
[Hands-On: Facebook’s New 24 Lens Camera Turns Real Life Into High Quality VR](https://uploadvr.com/facebook-surround-360-x24-hands-on/)
[上面链接的中文版](http://www.sohu.com/a/135242882_636408)
[Facebook, RED partner on 360 camera capturing 6 degrees of freedom](https://www.immersiveshooter.com/2018/05/02/facebook-red-partner-deliver-360-camera/)
[Facebook 的新款 360 度相机能以六个自由度进行拍摄](https://cn.engadget.com/2017/04/20/facebook-surround-360-x24-x6/)
[深扒FacebookSurround360 x24/x6全景相机研发过程](http://www.sohu.com/a/135407615_520324)