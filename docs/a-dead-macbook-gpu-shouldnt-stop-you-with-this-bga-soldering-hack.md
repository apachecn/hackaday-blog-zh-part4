# 一个死了的 Macbook GPU 不应该阻止你，这个 BGA 焊接黑客

> 原文：<https://hackaday.com/2020/06/28/a-dead-macbook-gpu-shouldnt-stop-you-with-this-bga-soldering-hack/>

在一些 2011 年的 Macbook Pro 型号上，镭龙 GPU 有失败的趋势。这应该意味着计算机的游戏结束了，但令人惊讶的是，它的主板上有两个而不是一个 GPU。英特尔处理器也有一个 GPU，苹果使用 FPGA 中的一堆逻辑在它们之间随意切换。社区已经产生了新的 FPGA 代码，以在其英特尔 GPU 上复活一个死亡的 Mac，但代价是失去亮度控制。[【ayilm 1】通过一个聪明的 BGA 返工黑客](http://advancedreworks.com/forum/showthread.php/gmux-bypass-native-brightness-control-3680.html)恢复了亮度，该黑客获得了英特尔 BD82HM65 平台控制器中枢芯片上存在的亮度控制线，但没有在 Macbook 中使用。

我们已经习惯了 Hackaday 令人印象深刻的焊接工作，我们已经看到了我们的布线直接连接到翻转的 BGA 芯片上的球。这是一个类似的想法，但在另一个层面上，原位 BGA 上的一部分顶部绝缘被移除，以暴露承载所需信号的球上方的微孔。一根细线焊接到裸露焊盘上，并连接到一片铜带上以提供机械强度，一根漆包铜线从铜带连接到 PCB 的另一侧。它带有 [FPGA 代码](https://github.com/ayilm1/gMUXBypass)来利用它，但即使对于非 Macbook 用户来说，这也是一件令人印象深刻的作品。[这也不是我们看到的第一次对 Macbook 进行精细焊接修复](https://hackaday.com/2019/07/09/liquid-damaged-macbook-saved-with-a-keen-eye/)。

感谢[lightpink784]的提示。