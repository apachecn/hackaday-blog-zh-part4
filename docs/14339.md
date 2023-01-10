# 一个可定制的宏面板，可以让任何人摇尾巴

> 原文：<https://hackaday.com/2022/07/28/a-customizable-macropad-to-make-anyones-tail-wag/>

[Gili Yankovitch]一直想要一种宏键盘，用于所有那些击杀 boss 的连击，他在玩 WoW 时一直藏着他巫师袍的袖子。十七年后，他终于接受挑战，造了一个。但实际上，这是一种保守的说法，因为 [Paws 是一种可定制的宏 pad，可以结束所有可定制的宏 pad](https://medium.com/@giliya/id-rather-be-shiny-c33492550b08)。

这个东西完全是定制的，但同时也是千篇一律的——但我们的意思是尽可能做到最好。爪子可以做成任何形状或形式，而且相当容易。你会问，这怎么可能？每个钥匙都有自己的微控制器。

是的，每个键都有一个 ATtiny85 和一个可爱的小带状电缆，这些组成了一个令牌环网，它可以与 Arduino 通信，Arduino 为计算机提供键盘接口。为了让事情变得更简单，[Gili]构建了一个简单的编程 UI，它可以自动识别配置和按键数量，并让用户选择最重要的部分 LED 的颜色。

[Gili]希望结合自 2020 年初最糟糕的时间线开始以来他学到的所有技能——嵌入式软件、CAD、电子和 PCB 设计。我们希望将网络添加到该列表中，特别是因为他找到了一个很好的解决方法来解决 I C 的缓慢和 tiny85s 与 Arduino 之间的通信限制。虽然[吉利]可能一开始就有一个很高的要求，但他绝对完成了。想拿到设计文件吗？[爬上 GitHub](https://github.com/gili-yankovitch/paws-module) 就行了。

如果你的定制兴趣更集中在什么程序上，一定要看看 [Keybon](https://hackaday.io/project/176239-keybon-adaptive-macro-keyboard) ，它是我们的[奇怪输入和特殊外设竞赛](https://hackaday.com/2022/07/13/overwhelmed-by-odd-inputs-the-contest-winners-and-more/)的众多令人敬畏的获胜者之一。