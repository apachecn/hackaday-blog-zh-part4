# Arduino Nano 的简易音乐可视化工具

> 原文：<https://hackaday.com/2021/12/08/an-easy-music-visualizer-with-the-arduino-nano/>

闪烁的 led 固然很好，但如果它们能与环境声音或音乐同步就更好了。[mircemk]已经构建了 LUMAZOID 可视化工具来实现这一点，[依靠一些 staple maker 组件来实现这一点。](https://hackaday.io/project/182899-diy-lumazoid-arduino-music-visualiser)

该版本是开源的，设计用于 60、120 或 180 WS2812B LEDs 灯串。Arduino Nano 负责运行该节目，通过其模数转换器捕捉音频。灵敏度电位计可以适当地设置输入电平。

从那里开始，进行快速傅立叶变换，提供不同频率范围内的音频强度数据。LUMAZOID 可以设置为只响应低音或整体响应所有频率。该数据随后被用于使 led 随着节拍及时脉动。

这是一个有趣的项目，演示了构建音频反应可视化工具所需的基本技术。我们以前也在这个领域看到过其他一些伟大的构建。休息后的视频。

 [https://www.youtube.com/embed/iYkC5pUFRbk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iYkC5pUFRbk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

