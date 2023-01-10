# 升级你的墨镜来寻找丢失的物品

> 原文：<https://hackaday.com/2019/12/07/upgrade-your-shades-to-find-lost-items/>

曾经希望你能增强你的视觉吗？

[Nick Bild]的最新技术通过[定位物体(或人)的位置](https://github.com/nickbild/artemis)并用激光追踪它们来帮助你找到它们。这种被称为 Artemis 的设备可以锁在你的眼镜上，并可以被配置为定位特定的物体。

从该设备收集的图像被传输到 NVIDIA Jetson AGX Xavier 板，该板使用 SSD300(单次多盒检测)模型来定位对象。该模型用 [COCO 数据集](https://pytorch.org/hub/nvidia_deeplearningexamples_ssd/)进行了预训练，以识别和定位来自 OpenCV 中阈值化图像的给定输入的 80 种不同对象类型。一旦目标被识别和定位，激光二极管就会激活。

可能由于当前的阈值，演示主要在中性背景下放置较远的对象上运行。将计算机视觉与物理设备结合起来以增强体验，而不是简单地处理和分析数据，这是一种有趣的应用。

该设备使用两个伺服系统来控制激光:一个用于 X 轴控制，另一个用于 Y 轴控制。这些控制由 Adafruit Itsy Bitsy M4 高速微控制器执行。

也许再多一点训练，我们可能就不会再有“沃尔多在哪里”这个难题了。

看看我们其他的太阳镜黑客，从[家庭自动化](https://hackaday.com/2019/08/15/home-automation-at-a-glance-using-ai-glasses/)到[使用液晶显示器](https://hackaday.com/2019/10/22/the-futures-so-bright-i-gotta-wear-lcds/)来减少前灯的眩光。

 [https://www.youtube.com/embed/zOmJOMlqhAQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zOmJOMlqhAQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

