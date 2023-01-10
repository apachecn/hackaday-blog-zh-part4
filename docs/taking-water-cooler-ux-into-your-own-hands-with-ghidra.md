# 与 Ghidra 一起将水冷却器 UX 掌握在自己手中

> 原文：<https://hackaday.com/2022/01/02/taking-water-cooler-ux-into-your-own-hands-with-ghidra/>

不知道 Ghidra 是什么的读者可能会想象某种售后水冷却器固件或主板——这是回流炉的常见黑客做法。Robbe Derks 所做的同样令人印象深刻和鼓舞人心:一个[水冷却器固件模块](https://practicapp.com/binary-modding-a-watercooler/)增加了免提水分配，不需要任何硬件模块或从头编写替代固件。

拆开了冷却器，【Robbe】在主板上发现了一个 PIC18F6527，令人惊讶的是，它没有固件回读保护。即使缺少 PICkit 也没有阻止他——他*只是*使用 Arduino 转储固件，[共享转储代码供我们重用](https://github.com/robbederks/watercooler/tree/master/arduino_dumper)，并且最终的转储在同一个存储库中可用。

从那以后，他让 Ghidra 参与反汇编代码，同时以一种我们都可以学习的方式记录这个过程，并展示 Ghidra 的妙招。必须进行仔细的规划，以决定挂钩哪些函数以及何时、在何处定位所有额外的逻辑，以便它和主固件之间没有不必要的干扰，并采取额外的步骤来反编译新修补的二进制文件，以验证它看起来可行，然后实际上用它来刷新冷却器。

最终的结果是，如果定义其用户交互原则的人被允许使其足够复杂的话，一个水冷却器可以完全按照它应该工作的方式工作。我们可以争论这是否应该是一个股票功能，但无论如何，很高兴知道我们黑客仍然有一些能力使我们的设备变得友好——即使它们没有操作系统。当然，我们每一个人都可以想到一个早就应该像这样提高可用性的设备。你有哪些例子？

我们已经讨论了相当多的涉及 Ghidra 的黑客攻击，但是我们永远不会觉得已经足够了。[给空气质量计打补丁用华氏](https://hackaday.com/2021/02/15/ghidra-used-to-patch-fahrenheit-into-an-air-quality-meter/)怎么样？或者另一篇关于破解 GBA 游戏的很有教育意义的文章[？或许，](https://hackaday.com/2021/07/16/cracking-a-gba-game-with-nsa-tools/)[解放一个 Linux 驱动的 4G 路由器](https://hackaday.com/2021/07/15/using-ghidra-to-extract-a-router-configuration-encryption-key/)来重新配置它，超越厂商定义的界限？如果你心中有自己的目标，并希望开始你的固件逆向工程之旅，我们可以肯定地说，你不会错过我们在 Ghidra 上的 HackadayU 课程[。](https://hackaday.com/2020/07/30/learn-software-reverse-engineering-ghidra-class-videos-from-hackadayu-now-available/)