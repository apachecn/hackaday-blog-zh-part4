# 大脑移植让一台街机从另一台玩游戏

> 原文：<https://hackaday.com/2020/04/26/brain-transplant-makes-one-arcade-machine-play-games-from-another/>

我们习惯了游戏控制台，其中相同的硬件运行各种不同的游戏，但如果我们仔细看看旧版本的街机柜，我们会发现每个游戏都有独特的定制板。来自相同制造商的一些主板共享共同的硬件特征，即使它们并不完全相同，而[twistedsymphony]已经利用这个[制作了一个老式的 Taito 游戏——*Gun&Frontier*——在另一个游戏的硬件上运行， *Ah Eikou no 甲子园*](https://www.arcade-projects.com/forums/index.php?thread/12882-converting-ah-eikou-no-koshien-to-gun-frontier-taito-f2-hardware/) 。这是一个跨越论坛线程的迷人故事，值得一读，即使你永远不会接触老式街机板。

我们可能会认为选择的工具是逻辑分析仪或类似的东西，但出乎意料的是，这个黑客的解决方案在 MAME 找到了。arcade emulator 隐藏了关于这些电路板的大量信息，从中您可以发现它们的差异并尝试可能的解决方案。硬件黑客出奇的简单，几根博德电线和一个更大的 ROM 额外的地址线。一个可编程逻辑阵列需要转储和重写，以修复图形损坏问题，并在模拟 MAME 的控制器问题后对 ROM 进行了一点调整，但似乎是的，一个游戏可以在另一个游戏上运行。肯定比[需要芯片解封的 Taito hack】要痛苦得多。](https://hackaday.com/2018/04/12/dumping-arcade-roms-the-hard-way/)

[通过[r/反向工程](https://www.reddit.com/r/ReverseEngineering/comments/g54wwo/converting_old_taito_arcade_hardware_to_run_a/)