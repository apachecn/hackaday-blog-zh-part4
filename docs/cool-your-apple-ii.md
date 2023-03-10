# 简单的风扇控制器帮助苹果二代战胜炎热

> 原文：<https://hackaday.com/2021/08/27/cool-your-apple-ii/>

当年，苹果 II 电脑通常不需要主动冷却。然而，替换硬件的日益稀缺说服了[约书亚·科尔曼]为他的 Apple II+提出了一个更强大的主动冷却解决方案，增加了它在未来几十年继续处理数据的可能性。

Joshua 提到，他记录了他的 Apple II+内部的最高温度为 110 华氏度(超过 43 摄氏度)。对于满载的 Apple II 系统来说，这并不是完全出乎意料的，组件就是为了处理这一点而构建的——6500 微处理器家族的原始数据表显示，CPU 可以处理高达 158 华氏度(70 摄氏度)的温度。不幸的是，我们不再处理全新的组件。几十年前的微处理器不一定有和以前一样的耐热性。所有部件最终都会磨损，而高温肯定会加速老化过程。

为了维护他的系统，约书亚为他的 Apple II+拼凑了一个基于 Arduino 的冷却系统。温度/湿度传感器持续监控机箱内的热状况-当温度过高时，12V 风扇会启动，将新鲜空气吸入主板和扩展卡。简单的冷却曲线减少了风扇电机和继电器的磨损。

这并不是 Apple II 系列的第一个主动冷却系统——在 20 世纪 80 年代，肯辛顿生产了一个受欢迎的(如果不是非常丑陋的话)“系统保护”附件，一个外部螺栓风扇，让东西保持冷却。这些通常部署在学校中，并由寻求增加可靠性的高级用户在最大限度地利用 Apple II 扩展槽时部署，这种配置可能会由于额外的电源要求和减少的气流而增加温度。

这个项目有很大的发展空间。任何想要更进一步的人都可以在 Joshua 的博客上找到项目细节和 Arduino 代码。

这不是约书亚的苹果 II 黑客第一次出现在这个网站上。我们最近报道了他在点阵打印机上打印突发新闻的项目。黑客视频如下。

 [https://www.youtube.com/embed/mzTcfPefdhI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mzTcfPefdhI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

