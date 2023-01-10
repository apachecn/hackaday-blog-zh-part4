# 一种只有一个或非门运算器的无 CPU 计算机

> 原文：<https://hackaday.com/2020/11/23/a-cpu-less-computer-with-a-single-nor-gate-alu/>

这些天我们看到了很多离散逻辑计算机构建，我们都很喜欢它们。但过了一会儿，他们就互相融合了。那么，如果离散逻辑爱好者想脱颖而出，他们该怎么做呢？也许这种只有一个或非门而不是算术逻辑单元的无 CPU 计算机足以成为黑客的 flex？我们当然这样认为。

我们必须承认，当我们第一次看到[Dennis Kuschel]的“MyNor”时，我们认为所有的逻辑都将被离散的 Nor 门模拟，当然，这些门可以以各种组合连接起来，产生每隔一个逻辑门。虽然那真的很酷，但[丹尼斯]选择了另一条路。位于设计非常精美的 PCB 中间的是一个小露头，一对分立晶体管和一个电阻。它们构成了或非门，与 MyNor 的微码一起执行通常由 ALU 完成的所有操作。

虽然使 MyNor 非常慢，但它的优势是不需要不再生产的 74 系列芯片，如 74LS181 ALU。它可能很慢，但正如下面的视频所示，在几个类似架构的附加卡的帮助下，它仍然可以玩扫雷和俄罗斯方块，并充当一个像样的计算器。

我们真的很喜欢这个版本的外观，我们祝贺[丹尼斯]完成了它。他已经开源了所有的东西，所以你可以自由地构建你自己的。或者，看看我们展示的其他一些无 CPU 计算机:有[Gigatron](https://hackaday.com/2019/03/25/how-the-gigatron-ttl-microcomputer-works/)、[Dis-Integrated 6502](https://hackaday.com/2016/05/24/how-the-dis-integrated-6502-came-to-be/)，或者[这种 8 位无 CPU 机器](https://hackaday.com/2019/05/09/cpu-made-from-74hc-chips-is-a-glorious-mess/)的跳线丛林。

 [https://www.youtube.com/embed/jUIO-ai_RB8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jUIO-ai_RB8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

