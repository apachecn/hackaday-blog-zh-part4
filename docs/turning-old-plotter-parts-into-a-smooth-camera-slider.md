# 将旧绘图仪零件变成平滑的相机滑块

> 原文：<https://hackaday.com/2022/04/07/turning-old-plotter-parts-into-a-smooth-camera-slider/>

拆开旧的东西，重新使用零件来制造新的东西，这是许多黑客最初在机械和电子工程领域起步的方式。但是，即使在工业界工作了多年，每当有人给我们提供一个旧设备的“零件”时，我们仍然会感到兴奋，并立即开始想象我们可以用里面的元件制造出什么东西。

[![A GoPro mounted on a moving platform made from recycled parts](img/64aab8e8dade029fb144b953c6fdab59.png)](https://hackaday.com/wp-content/uploads/2022/04/Tobogan-side-view.jpg) 所以当【维克多·弗罗斯特】得到一台旧的 Cricut 绘图仪时，他意识到他可以用它的零件[来制作他一直计划制作的相机滑块](https://hackaday.io/project/184693-tobogan-mini-camera-slider)。绘图仪的 X 平台由步进电机控制，非常适合来回移动相机平台。[Victor]想要以一种“徒手”的方式构建整个系统，而不需要进行详细的设计或购买任何新部件。所以他把手伸进他的零件箱，找出了一个 Arduino，一个 16×2 的 LCD，一些电线和按钮，还有几块 MDF。

相机支架只是一块钢，GoPro 的磁性支架可以锁定在上面，但[Victor]保留了安装适当三脚架球头的可能性。Arduino 通过 Adafruit 电机护罩驱动步进电机，在 LCD 上运行简单的用户界面。用户可以设置所需的终点和速度，然后根据需要来回运行相机。这样，软件就像硬件设计一样遵循“保持简单”的原则。

如果你打算制作自己的相机滑块，如果你碰巧有一台旧的绘图仪，[Victor]的设计应该很容易复制。如果没有，你可以试试[这个简单却设计精良的模型](https://hackaday.com/2022/02/22/super-simple-camera-slider-with-a-neat-twist/)。想要更多吗？然后看看[这个奇特的多轴摄像机运动控制装置](https://hackaday.com/2021/05/21/perfecting-a-3d-printed-camera-motion-control-rig/)。

 [https://www.youtube.com/embed/sYULMjaJssM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sYULMjaJssM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

