# 收银机热键板在钱上

> 原文：<https://hackaday.com/2019/08/08/cash-register-hotkey-board-is-on-the-money/>

当面对一堆免费的电子产品时，有时你会抓住它们“有朝一日”的潜力。其他时候，你很清楚自己在追求什么。[布莱斯]从学校免费得到一个大的旧收银机，因为他们已经开始使用广场或其他东西。作为副作用，他得到了两个 VFD 和一个螺线管，但他真的很喜欢那个坚固的键盘和它的纸标签键帽，定制的时机已经成熟。

[两个小时的逆向工程之后](https://brycedombrowski.com/2019/08/summer-2019-custom-hotkey-keypad-project/)，他知道哪里的按钮按得足够好，可以够到一个山寨的 Arduino Pro Micro 和几个移位寄存器。[Bryce]希望他的热键板能够处理键盘按键和媒体键输入，所以他选择了 [HID-Project](https://github.com/NicoHood/HID) 库，而不是标准版本的 Arduino。当然，制作你自己的热键板的全部意义在于定制。对布莱斯来说，这意味着他必须写的所有工程报告都有单词快捷方式和快速查阅希腊字母。挖那个半衰期λ！

什么？你没有免费电子产品的使用权？你可以用街机按钮做一个热键板。这些东西真的很难对付。