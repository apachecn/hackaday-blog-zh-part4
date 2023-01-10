# MIDI 控制器——来自扭线垫？

> 原文：<https://hackaday.com/2021/05/09/a-midi-controller-from-a-twister-mat/>

扭扭乐，这是一种有点尴尬但却异常有趣的地板扭曲游戏，我们大多数人对圣诞节派对都有模糊的年轻记忆。缠绕垫可以用作输入设备吗？在与一位朋友交谈后，盖伊·杜邦[用这 24 个彩色圆点做出了这个](https://hackaday.io/project/179348-twister-mat-midi-controller)。

给一个地板大小的塑料垫子布线并不像看起来那么容易，早期用铜箔和电容式触摸传感器芯片进行的实验被证明是失败的。替代物以力敏电阻的形式出现，由一对 MCP3008 多路复用模数转换器读取。这些然后被一个做所有 MIDI 魔术的 ESP32 读取。我们在休息时间下面的视频中看到了完整的细节，包括他在机器人语音随机移动发生器的提示下，按照节拍播放 Twister 的有趣场景，我们可以看到这种设备有一些潜力。

我们以前没有见过另一个缠绕垫，但是力敏电阻已经出现在分辨率更高的阵列中。是[LED 地面游戏控制器](https://hackaday.com/2016/11/07/neopixels-light-the-way-in-pressure-sensitive-floor/)让我们经历了这一切。

 [https://www.youtube.com/embed/3Di2NhG_JFw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3Di2NhG_JFw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

