# OpenCV 和深度相机发现杂草

> 原文：<https://hackaday.com/2021/01/31/opencv-and-depth-camera-spots-weeds/>

使用视觉技术来识别农业中的杂草是一个积极发展的领域，一个研究小组最近分享了他们在开源计算机视觉库 [OpenCV](https://opencv.org/) 的帮助下使用机器视觉和深度信息的组合来识别和绘制杂草的方法。农业是人们吃饭的方式，改善杂草管理是其最重要的挑战之一。

[![](img/862394c3c857158c8602cacaf71f78a3.png)](https://hackaday.com/wp-content/uploads/2021/01/image-21.png) 目前许多杂草检测和分类工作都使用花哨(且昂贵)的多光谱相机，但 **PhenoCV-WeedCam** 主要依赖于 [OAK-D](https://store.opencv.ai/products/oak-d) 立体深度相机。该系统仍在开发中，但比概念验证更进一步。便携式设置使用树莓 Pi、立体摄像单元、电源组和 Android 平板电脑进行接口，目前需要一个听话的人来移动和指向它们。

这是对为发展而收集数据的动手工作的有趣一瞥。有了来自许多不同环境的大量野外数据，该系统可以使用这些数据来识别每张图像中的草、阔叶植物和土壤。这本身是有用的，但是深度信息也允许系统估计总体植物密度以及试图确定任何特定植物的生长中心。知道杂草的存在是一回事，但是精确地清除它——例如用机器人手臂上的激光或微型除草机——知道杂草实际上是从哪里生长出来的是一个重要的细节。

phenom cv-weed cam(GitHub 库)还不能进行实时分析，但结果是有希望的，这是下一步。该系统目前必须由人携带，但最终可能会连接到[一个专门用于穿越田野的机器人平台](https://hackaday.com/2019/12/14/arrbot-is-a-fast-way-to-get-out-standing-in-a-new-field-of-robotics/)。