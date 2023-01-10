# 神经网络智能升级安全系统

> 原文：<https://hackaday.com/2019/07/03/neural-network-smartens-up-a-security-system/>

有一个安全摄像头一直在录像固然很好，但仅此一点并不能在发生犯罪时发出警报。运动感应的用途有限，通常由不重要的刺激触发，如移动的阴影或过往的车辆。[Tegwyn☠Twmffat]想要一个更好的农场安全系统，并决定用神经网络来解决这个问题。

安全系统的主要组件是一个装有摄像头和 Movidius 神经计算棒的 Raspberry Pi。这允许 Raspberry Pi 在视频上运行实时对象识别。树莓 Pi 的程序设定是，如果它检测到人类靠近，就会发出警报，但会忽略家庭狗和其他虚假目标。在检测到的情况下，Raspberry Pi 通过 LoRa 向基站发送信号，发出警报。由于一些带有边界框的简单代码，目标越靠近摄像机，警报的音调就越高。

这是一种创建智能安全系统的绝妙方式，而且完全由现成的部件和代码构建而成，更令人印象深刻。神经网络变得越来越有用；它们甚至能知道你的猫什么时候想出去。休息后的视频。

[hack adayprize 2019](https://prize.supplyframe.com)主办单位: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip) 

 [https://www.youtube.com/embed/U6KapET2udQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/U6KapET2udQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

