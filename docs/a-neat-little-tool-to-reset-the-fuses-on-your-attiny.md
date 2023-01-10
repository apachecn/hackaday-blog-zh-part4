# 一个整洁的小工具来重置你衣服上的保险丝

> 原文：<https://hackaday.com/2022/04/16/a-neat-little-tool-to-reset-the-fuses-on-your-attiny/>

如果你是一个经验丰富的黑客，你可能在某个时候遇到了一个问题，并想到“让我们制作一个工具来自动化它”。几个小时后，您得到了您的工具，但随后意识到您在制作工具上投入的工作量远远超过了您手动解决原始问题所需的工作量。不过这真的没关系:开发一个奇特的工具可能是一次有益的经历，它会教会你更多关于原始问题的知识，这是你在其他情况下所学不到的。【sjm4306】的 [ATtiny 高压保险丝重置器](https://hackaday.io/project/184867-attiny-high-voltage-fuse-reset-er)是一个聪明的设备，坚定地属于这一类。

它解决的问题是任何使用过 Atmel/Microchip 的 ATtiny 系列微控制器的人都熟悉的:错误地设置一个配置保险丝，你就不能再对你的芯片重新编程。将 ATtiny 恢复到其原始配置需要一个高压编程步骤，包括将 reset 引脚拉至 12 V，否则就是一个 5 V 系统。你可以简单地抓住一个备用的 12 V 电源，用几个晶体管组装一个电平转换器，但这有什么意思呢？

[sjm4306]的解决方案建立在一个漂亮的紫色 PCB 上，其中包含一个 ATmega328、一个有机发光二极管显示器和一些插座，以适应各种版本的 ATtiny 系列微控制器。要产生所需的 12 V 电压，只需使用现成的升压转换器 IC 即可。但相反，他认为用分立元件制作这样的电路并用 ATmega 控制它会很有趣。毕竟，这种芯片已经包含了产生 PWM 信号的定时器和测量转换器输出电压的 ADC，所以它只需以 PID 控制器的形式编写一些控制逻辑。

正如你在下面的视频中看到的，最终的结果是一个方便的小 PCB，它使用 5 V USB 电源，只需按一下按钮，就可以重置你衣服上的保险丝。有时候，做好一件事的简单工具就是你所需要的全部；然而，如果你正在寻找一个一体化的 AVR 编程器，也支持高压编程，看看这个 AVR 多工具。

 [https://www.youtube.com/embed/9Nkms_qPnng?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9Nkms_qPnng?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

