# 一个微波炉修理甚至机械键盘爱好者也会喜欢

> 原文：<https://hackaday.com/2020/11/15/a-microwave-repair-even-mechanical-keyboard-fans-will-love/>

微波炉的设计和制造已经优化到一度昂贵的电器现在几乎是一次性的。尽管经济状况不佳，但有些人还是忍不住要修理东西，尤其是当你有机会以时尚的方式修理的时候。因此，我们提出[这个微波修复](https://github.com/dekuNukem/pimp_my_microwave)与它的完全不必要的，但神话般的装饰。

[dekuNukem]极其便宜的二手微波炉的终结始于许多电器首先出现故障的地方——薄膜键盘。无法再可靠地按下按钮，[dekuNukem]找出了原始键盘的矩阵布线排列，并用一些按钮开关和一块废弃的 perfboard 拼凑了一个小键盘。连接到主印刷电路板，这是一个有效和廉价的解决方案，如果有点天真的一面。

为了让事情活跃起来，[dekuNukem]转向了 [duckyPad](https://hackaday.com/2017/11/10/an-awesome-open-mechanical-keyboard/) ，这是一个可热插拔的 macropad，带有机械开关，当然还有 RGB LEDs。从这里开始，事情变得有趣了；由于 duckyPad 输出串行数据，微波炉内部需要一个适配器。一个 STM32 微控制器和一对 ADG714 模拟开关实现了这一目的，电源来自原始 PCB。

完成的修复相当华丽，现在[dekuNukem]拥有了世界上唯一一台带有 clicky 键盘的微波炉。更重要的是，它很有效。

 [https://www.youtube.com/embed/BKcvKsYxbbo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BKcvKsYxbbo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

