# 重建 Mac SE 逻辑板

> 原文：<https://hackaday.com/2021/02/08/recreating-the-mac-se-logic-board/>

当[Kai Robinson]发现自己面临拯救尽可能多的 Mac SE 的艰巨任务时，合乎逻辑但令人生畏的答案是[为本来会报废的机器重新创建 Mac SE 逻辑板](https://68kmla.org/forums/topic/60059-reverse-engineering-the-macintosh-se-pcb-custom-chips-for-11-reproduction/)。这些机器已有 30 多年的历史，婴儿车的电池经常漏液，损坏零件和痕迹。假设逻辑板是一个简单的通孔~~两个~~四层板，这能有多难？

第一步是获得一些参考照片，因此[Kai]开始拆焊板上的所有东西。元件的清单和焊料的年代使这成为一项艰巨的任务。然后通过使用扫描仪和一些 Inkscape 魔法将图像合并在一起~~产生了一个合成图像。~~在图形软件中。

[Kai]没有简单地将引脚放在正确的位置并重新布线所有的网表，而是选择复制原始 SE 板的痕迹。[Kai]和论坛上的其他几个人一直在测试主板，并跟踪设计中的最后几个错误和缺陷。这里有一个未连接的引脚，那里有一个阻抗匹配不正确的电阻。如果任何人需要新的逻辑板 PCB，他们很快就会准备好 Gerbers 和设计文件。

在 Hackaday，我们喜欢麦金塔电脑已经不是什么秘密了。我们已经看到[为它定制的新外壳](https://hackaday.com/2019/01/21/the-greatest-computer-ever-now-gets-a-new-injection-molded-clear-case/)和现在为它定制的新印刷电路板。这确实会让我们思考，想知道接下来会发生什么？

感谢[Toru173]发送这封邮件！