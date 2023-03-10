# 游戏机，墙上的游戏机，Alexa 可以帮我全部玩吗？

> 原文：<https://hackaday.com/2021/08/27/consoles-consoles-on-the-wall-can-alexa-help-me-play-them-all/>

如果你收集了很多经典的游戏主机，找到地方把它们都放起来可能是一个挑战。但更大的问题是如何将它们连接到一台最多只有两三个输入的电视上。[【odelot】最近来信告诉我们他是如何用他的声控游戏历史墙解决这两个问题的](https://odelotstuff.wordpress.com/2021/08/16/switcher-extron-with-alexa/)。

为了将系统安装到墙上，[odelot]设计并印刷了角形支架，这些支架连接到特殊形状的 3 mm MDF 上。他们很好地将系统保持在一个视觉上有趣的角度，同时又不引人注意，只有臭名昭著的底部光滑的 Wii 需要一些额外的夹子来防止它滑落。他还打印了一系列的块和管道，毫无疑问是参考了 *Mario Bros.* 的设计，用来固定每个系统的电源和视频电缆。

[![Prototype version of electronics on breadboard](img/c5e8a408178c8a67ae7c9e2e93986dd1.png)](https://hackaday.com/wp-content/uploads/2021/08/alexaconsoles_detail.jpg) 至于将它们都连接到他的电视上，【odelot】拿起了一个八设备 Extron VGA 开关，它具有一个用于远程控制的串行端口。在让所有系统适应适当的视频标准后，他将一个 ESP8266 连接到交换机，并编写了一些代码，将它与亚马逊的 Alexa 语音助手联系起来。

只需说出他想玩的系统的名称，微控制器就会将开关切换到相应的输入端，并打开相应架子下的一圈蓝色发光二极管，以表示选择了哪个控制台。甚至还有一系列固态继电器，最终将控制每个系统的主电源，尽管[odelot]还没有完全实现它。目前，这个项目的电子设备生活在一个相当包装的试验板上，但看起来他正在设计一个合适的 PCB 来清理它的早期阶段。

不满足于简单地控制一个商用 A/V 开关？在过去，我们已经看到[真正专注的控制台收集者从头开始设计他们自己的定制开关](https://hackaday.com/2007/03/14/diy-av-switch/)，[配有一个显示器来显示当前选择的系统的标志](https://hackaday.com/2021/03/30/custom-built-12-port-a-v-switch-keeps-crt-well-fed/)。

 [https://www.youtube.com/embed/pEHMFXgco14?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pEHMFXgco14?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

