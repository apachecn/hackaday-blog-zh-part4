# 新的 Kinect 传感器将焦点从游戏玩家转移到开发人员

> 原文：<https://hackaday.com/2019/02/26/new-kinect-sensor-switch-focus-from-gamers-to-developers/>

微软的 Kinect 作为游戏外设可能没有获得成功，但认识到深度传感器太酷了，不能让它死掉，即使在 Xbox 游戏外设停产后，开发仍在继续。本周他们的最新版本出现了，我们可以以 Azure Kinect DK 的形式获得它。这是一个开发者工具包，专注于探索这项技术的新应用，而不是我们在自己的项目中使用之前必须破解的游戏外设。

它被封装在一个通过 USB-C 插入 PC 的外围设备中，比去年宣布的核心深度传感器模块[多，但比完整的消费产品少。浏览其](https://hackaday.com/2018/05/10/microsoft-kinect-episode-iv-a-new-hope/) [10 页的规格(PDF)](http://www.aka.ms/kinectdocs) 并与第二代 Kinect 感应条进行比较，我们可以看到这项技术是如何发展的。物理尺寸和重量已经下降，功耗也是如此。辅助功能得到了改善，麦克风阵列得到了扩展，IMU 除了加速度计之外还带有陀螺仪，RGB 摄像头也升级到了 4K 分辨率。

但是这场秀的明星是一种新的连续波飞行时间深度传感器，在 2018 年 IEEE ISSCC 会议上展示。(全文需要 IEEE 会员资格，但摘要形式可以通过 ResearchGate 在[获得。)在它的诸多进步中，我们预计影响最大的是它的视野。默认的 75 x 65 度已经比它的前辈更好了(第一代 Kinect 为 64 x 45，第二代为 70 x 60)，但是可以选择通过切换到 120 x 120 度的广角模式来换取覆盖范围。*明显比其他深度相机*宽，如](https://www.researchgate.net/publication/323818253_IMpixel_65nm_BSI_320MHz_demodulated_TOF_Image_sensor_with_3mm_global_shutter_pixels_and_analog_binning)[英特尔的 RealSense D400](https://software.intel.com/en-us/realsense/d400) 系列或 [Occipital 的结构](https://structure.io/)。

另一个有趣的特性是内置同步。许多使用多个 Kinect 传感器的项目遇到了问题，因为它们相互干扰。当然，人们围绕这个问题进行了黑客攻击，但现在他们不必这样做了:商用 3.5 毫米插孔允许多个 Azure Kinect DK 以菊花链形式连接在一起，因此它们可以很好地轮流播放。

从它的名字来看，我们担心这个产品会在某种程度上需要微软的 Azure 云服务，如果没有它，它会变得很弱。根据目前公布的信息，似乎开发人员可以访问与以前的传感器相同的所有数据流。Azure 搭售采用可选 SDK 的形式，使上传数据等事情更容易在 Azure 基于云的识别服务中处理。

最后，Azure Kinect DK 399 美元的价格明显高于 Kinect 游戏外设，但对于开发者来说，这是一款低容量产品。或许基于这种技术的大批量消费产品成本会更低，但这仍有待观察。与此同时，您有解决类似问题的替代工具。例如，如果你正在[构建自己的 AR 耳机](https://hackaday.com/2019/02/18/immersive-augmented-reality-on-a-budget/)，你可能会使用[英特尔最新的 RealSense 摄像头](https://hackaday.com/2019/02/10/new-part-day-mapping-with-realsense-cameras-for-200/)进行基于视觉的内外运动跟踪。