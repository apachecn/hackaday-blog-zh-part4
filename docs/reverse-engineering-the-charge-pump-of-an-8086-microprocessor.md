# 8086 微处理器电荷泵的逆向工程

> 原文：<https://hackaday.com/2020/07/31/reverse-engineering-the-charge-pump-of-an-8086-microprocessor/>

你可能会认为 8086 微处理器，一个 40 岁的芯片，板上只有 29000 个晶体管，引发了 16 位 PC 革命，不会再有更多的故事可讲了。但是正如[Ken Shirriff]所发现的，从芯片照片中逆向工程芯片揭示了一些隐藏的深度。

[Ken]探索这种古老芯片的重点是电荷泵，他解释说这是一种用于在芯片衬底上提供偏置电压的电路。早期的芯片通常从引脚获得-5 伏的偏置电压，这意味着设计人员必须提供双极性电源。为了减少将 8086 集成到设计中所需的工程工作量，英特尔选择了片上电荷泵来产生偏置电压。该电路由一个由三个反相器组成的环形振荡器、一对晶体管和一些充当止回阀的二极管组成。通过交替地给电容器充电并相对于衬底切换其极性，产生了所需的-5 伏偏压。

考虑到所需的电路，[Ken]很容易在芯片上找到它。电荷泵占用了相对较大的芯片空间，这表明英特尔在决定采用它时做出了工程决策。[Ken]深入到电路的一个非常低的层次，详细介绍了 MOSFETs 是如何构建的，以及为什么使用八个晶体管而不是两个二极管。像往常一样，他的芯片照片质量一流，他对芯片内部情况的解释也是如此。

如果你不知何故偶然发现了[Ken]的作品，你会得到真正的享受。首先，你会想看看他是如何发现 8087 协处理器的芯片中的 [pi 的，或者](https://hackaday.com/2020/05/20/looking-for-pi-in-the-8087-math-coprocessor-chip/)[他对不同 Game Boy 音频芯片](https://hackaday.com/2020/06/27/comparing-bare-silicon-on-two-game-boy-audio-chips/)的芯片级探索。