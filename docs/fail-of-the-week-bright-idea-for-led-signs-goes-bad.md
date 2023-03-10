# 本周失败:LED 标志的好主意变坏了

> 原文：<https://hackaday.com/2020/05/08/fail-of-the-week-bright-idea-for-led-signs-goes-bad/>

通常，当我们选择一个项目获得“本周失败”荣誉时，是因为这个项目的技术出了问题。但是[【Leo Fernekes】的创新 LED 标志系统](https://www.youtube.com/watch?v=KcIGiyKuHYc)的技术从来不是问题；正是扩大生产规模的现实以及破碎的专利流程给这个有前途的项目埋下了一颗钉子，在下面的视频中[Leo]将其简洁地总结为“发明家的悖论”。

里欧几年前的想法非常聪明。他注意到，在廉价的预制 LED 招牌和昂贵的可编程招牌之间没有中间地带，所以他试图填补这一空白。结果是一个巧妙的“LED 引脚”，一个带有 RGB LED 和微控制器以及少量支持组件的微型模块。主要的想法是，每个引脚将在闪存中存储它自己的显示动画部分。每个引脚都有两个端子，分别连接到所连接电路板两侧的金属覆层。这两个导体不仅为所有引脚提供电源，还通过低频方波实现同步。[Leo]为动画编程的方法——在每个针上使用一个光传感器来接收来自视频投影仪的信号——可能比针本身更巧妙。

[Leo]的想法似乎注定要伟大，但是，唉，扩大规模的残酷现实打击了他。每个原型引脚的零件数量很少，但为了经济地制造，整个 BOM 必须减少到几乎为零。这意味着需要一个 ASIC，但是为它准备工具所花费的时间和费用太多了，难以承受。[Leo]对专利游戏也没什么好说的，这是他在这家企业中的商业伙伴坚持玩的。视频中有很多细节，但他用一句精辟的话总结道:“专利真烂。”

看了这个视频，很难不为[Leo]感到难过，他花了这么多时间来获得正确的技术，却没有可行的方法来获得投资回报。对于我们这些自以为是发明家的人来说，这是一个发人深省的故事，也是一个警示性的故事，告诉我们参与一个显然是为了公司利益而不是发明者个人利益的专利系统的危险。正如我们自己的鲍勃·巴德利(Bob Baddeley)向我们展示的那样，赢得这场游戏并非不可能，但很容易失败。

 [https://www.youtube.com/embed/KcIGiyKuHYc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KcIGiyKuHYc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[th_in_gs]的提示。