# 复古风格的热感相机

> 原文：<https://hackaday.com/2020/04/17/a-thermal-camera-with-a-vintage-twist/>

如今，我们往往重视复古技术的高超设计。因此，当一个破旧的电子产品被赋予新的用途时，这是值得称赞的。这些类型的建筑正是马丁·曼德所喜欢的，他证实了这一点，他将 1979 年的阿波罗微波监视器改造成了热感相机。

被其独特的设计所吸引，[马丁·曼德]在二手市场上买到了最初的微波监视器，尽管这个设备并不完全处于崭新的状态。据推测，这种类型的探测器用于监测工业环境中人员暴露于微波辐射的情况。

在移除所有内脏后，他用一个树莓 Pi Zero W、Adafruit 热感相机、1.3 英寸 TFT 显示屏和一个 USB 电池组取代了它们。尤其令人高兴的是，[马丁·曼德]能够不依靠 3D 打印来安装所有组件，而是用废塑料手工雕刻一些定制面板和支架。

该软件基于 Python，自动将拍摄的图像上传到一个 [Adafruit。IO](https://io.adafruit.com/) 仪表盘。8 x 8 像素的传感器分辨率不是很高，但通过使用[双三次插值](https://en.wikipedia.org/wiki/Bicubic_interpolation)，他能够将其转换为 32 x 32 的图像，这足以为他的猫和其他家居用品拍摄一些有趣的照片。

同样值得一试的还有其他一些复古技术，比如他的[盒式 Pi IoT scroller](https://hackaday.com/2020/03/10/iot-cassette-scroller-never-needs-a-pencil/) 。

 [https://www.youtube.com/embed/1xjRJExzPR8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1xjRJExzPR8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

