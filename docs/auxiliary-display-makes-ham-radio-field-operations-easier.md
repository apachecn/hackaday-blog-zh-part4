# 辅助显示器使业余无线电现场操作更容易

> 原文：<https://hackaday.com/2020/08/29/auxiliary-display-makes-ham-radio-field-operations-easier/>

尽管古老的八重洲 FT-817 收发器可能会受到业余无线电运营商的欢迎，但它也不是没有缺陷，特别是在用户界面方面。[Andy (G7UHN)]痛苦地熟悉这些缺陷，所以他为 FT-817 设计了[这个辅助显示和控制面板，使其操作稍微容易一些。](https://swling.com/blog/2020/08/andy-builds-a-genius-companion-control-display-for-the-yaesu-ft-817-transceiver/)

享受业余无线电的方式有很多，但更受欢迎的方式之一是走出小屋，在户外工作。从海边到山顶，火腿喜欢给他们的装备一些新鲜空气和阳光。电池供电的多模式全波段 FT-817 非常适合这些短途旅行，但为了将尽可能多的无线电装进一个小包装，八重洲的工程师们不得不在控制上做出妥协。收音机的许多最常用的功能都隐藏在需要多次点击和旋转才能访问的菜单中，而不是布满按钮。

[Andy]的解决方案是一个印刷电路板，上面有一个 Arduino Nano、一个 LCD 屏幕和一大堆实际按钮。该板位于机箱顶部，通过 8 针迷你 DIN 电缆使用有记录和无记录的 CAT 或[计算机辅助收发器](https://en.wikipedia.org/wiki/Computer_Aided_Transceiver)命令与无线电通信。LCD 显示各种功能的当前状态，按钮提供了更改这些功能的便捷途径，主要是通过向收音机发送按键。

向[安迪]致敬，感谢他解决了这个项目。我们之前见过的唯一一个 FT-817 黑客很有用，但简单得多，而且不需要 KiCad，这一次[Andy]不得不自学。