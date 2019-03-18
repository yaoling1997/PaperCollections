##[Google Jump](https://ai.google/research/pubs/pub45617)
<img src="https://i.loli.net/2019/03/18/5c8ef729e427a.png" alt="1.png" title="1.png" />
omnidirectional stereo (ODS) video(全景视频)
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

16个摄像头环状分布
水平360°画面，垂直120°画面
##拓展延伸
[最详细的Google Jump原理解读](http://www.360doc.com/content/17/0530/17/11604731_658493279.shtml)
