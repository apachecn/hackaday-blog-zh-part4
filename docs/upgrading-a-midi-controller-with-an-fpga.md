# 用 FPGA 升级 MIDI 控制器

> 原文：<https://hackaday.com/2019/09/29/upgrading-a-midi-controller-with-an-fpga/>

虽然 MIDI 中的“M”代表“musical ”,但是这个标准也可以用于其他事情。[s-ol]一直致力于 VJ 设置(混合视频而不是音乐)，使用各种基于电位计的硬件和 MIDI 将一切连接在一起。在对电位计的漂移感到沮丧之后，他开始为整个装备配备定制的编码器。

[s-ol]围绕 FPGA 设计了基于旋转编码器的电路板。它监控编码器的变化，控制每个旋钮的八个 RGB LEDs，甚至在铝制旋钮本身上进行电容触摸感应。FPGA 通过 SPI 与 Arduino 主控制器通信，Arduino 主控制器通过串行接口与 PC 通信。这是[s-ol]第一次投入到 FPGA 项目中，看起来他很成功！。

即使您没有混合视频或音乐，这些编码器也可能对标准模拟电位计不够准确或精确的任何项目有用，或者如果您只需要可以快速拨入特定值的东西。电位计在许多不同的方面都有不足，但是如果你不想替换它们，你可以[修改电位计以适合你的目的](https://hackaday.com/2015/02/11/digitally-controlled-pot-taper/)。

 <https://hackaday.com/wp-content/uploads/2019/09/videomp4.mp4?_=1>

[https://hackaday.com/wp-content/uploads/2019/09/videomp4.mp4](https://hackaday.com/wp-content/uploads/2019/09/videomp4.mp4)