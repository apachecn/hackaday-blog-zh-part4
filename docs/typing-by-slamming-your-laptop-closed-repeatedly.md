# 关上笔记本电脑打字。反复地

> 原文：<https://hackaday.com/2020/04/04/typing-by-slamming-your-laptop-closed-repeatedly/>

你是否有时觉得你定制的机械键盘不够响亮，不足以显示你超强的黑客能力？或者你需要一种更有力的方式在互联网上对错误的人大喊大叫吗？对于所有这些和更多的内容，[Jesse Li]已经用一套[bash 脚本覆盖了你，它允许你通过反复关闭笔记本电脑](//github.com/veggiedefender/open-and-shut/)来打字，使用莫尔斯电码。

![](img/f107c876c9a5c6b9cb9e926f6fb23abd.png)

Not the fastest way to type, but definitely the most forceful

脚本非常简单，从 ACPI(高级配置和电源接口)接收盖子打开/关闭事件，记录打开和关闭的时间戳，并将时间转换为点和破折号。在砰的一声达到要求的节奏后，你打开盖子看角色出现。

为什么会想要这个？嗯，你现在可以合上你的笔记本电脑来输入字母 E，而不是锁住它。也许在一部 B 级动作片里，当你被恐怖分子挟持时，可以用它来发送紧急信息。否则，我们认为这只是一个有趣的小黑客，可能是隔离引起的无聊的产物。

莫尔斯电码，也被称为 CW，仍然令人惊讶地被业余无线电爱好者广泛使用，因为它擅长在信号条件差的时候跨越洲际距离获取信息，而且只支持 CW 的业余无线电设备很便宜，而且[很容易自己组装](https://hackaday.com/2019/11/09/just-how-simple-can-a-transceiver-be/)。我们还介绍了[科赫学习 CW](https://hackaday.com/2020/02/21/learning-morse-code-the-ludwig-koch-way/) 的方法，所以在隔离期间不要害怕涉猎一点。