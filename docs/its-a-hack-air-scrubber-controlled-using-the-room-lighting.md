# 这是一个黑客:利用室内照明控制空气洗涤器

> 原文：<https://hackaday.com/2021/10/16/its-a-hack-air-scrubber-controlled-using-the-room-lighting/>

有些产品看起来就是设计得让人讨厌。[hardmar]发现安装在他儿子的地下室木工车间的[空气过滤系统](https://hackaday.io/project/181852-automated-jet-air-filtration-remote-control)被定向为最佳气流，但实际上并不适合打开和关闭这个东西。由于某种原因，该装置的一侧有一个单一的视线红外接收器，当安装在某些位置时，会迫使用户处于完全错误的位置来使用所提供的遥控器。

我们发现，专门设计用于不同方向安装的设备没有在不同位置安装红外接收器来确保良好的可控性，这有时有点无益。仅仅为了打开某个东西，就必须把自己扭曲到某个特定的位置，这很快就会变得令人讨厌，有些人可能根本就不在乎。

适当控制灰尘对持续的健康至关重要，在任何工作场所或共享区域都至关重要。当你加工木头时，会产生很多灰尘。这是不可避免的，它渗透到每一个地方，包括你的肺。PPE 是不够的。即使在你自己的店里，你也应该尽你所能控制灰尘的产生。选项从集中抽取到每台机器解决方案都有所不同，通常还会增加安装在天花板上的空气洗涤器，以捕捉那些细微颗粒。

[hardmar]没有解决 IR 放置问题，而是想将该装置连接到照明系统，以便一旦有人打开适当的灯，它就可以通电，然后在用户离开后保持固定的时间，以便继续擦洗空气。他的简单方法是首先记录和分析遥控器使用的红外协议，并对 Arduino 进行编程，使其能够发送开/关命令。接下来，他连接了一个瞄准灯光的光电晶体管，以提供必要的“用户在场”触发，告诉 Arduino 何时激活洗涤器。超级简单有效。我们喜欢这种非侵入式的方法，这种方法可以让现成的设备适应我们的特定要求，甚至不用给它看螺丝刀。

正如[哈德曼]所承认的，这种技术实现得并不完美，只是足够让它工作，这很好，有时你只是有工作要做，仅此而已。