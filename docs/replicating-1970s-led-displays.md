# 复制 20 世纪 70 年代的 LED 显示屏

> 原文：<https://hackaday.com/2019/04/14/replicating-1970s-led-displays/>

1971 年，德州仪器发布了别人从未见过的东西。TIL305 是一个字母数字显示器，由发光二极管供电。当然，70 年代初的技术意味着 LED 不是很亮，显示器也很贵，但如果你想要一个简单经典、相对低功耗的显示器，你不会比老式的字母数字 LED 显示器做得更好。

正如你所料，新老库存 TIL305s 仍然昂贵，现在每个人都可以获得廉价的 PCB 制造能力和真正的小 led。DIYTIL305 试图复制复古风格，看起来棒极了。

老式的 TI 制造 TIL305 是一个印刷电路板，可以夹在 DIP-14 插座中。LED 阵列为 5×7 像素，在 0.05 英寸的网格上有一个小数点，还有一个半透明的红色漫射器。PCB 很容易，使用 0201 LEDs，您可以获得所需的 LED 间距。将 PCB 变成 DIP-14 只需要几个机器引脚头，对于扩散器，这个项目使用激光切割铸造丙烯酸。如果你有一台抓放机或一只稳定的手，这就很简单，组装很容易。

最终的 DIYTIL305 板[现在正在测试](https://hackaday.io/project/161694-diytil305/log/161004-finishing-up-diytil305-12)，但是到目前为止结果很好。有了微控制器上的正确代码，这些显示器将通过数字 0 到 9 闪烁，字母表只是多了一点代码。由于这个项目使用 0201 发光二极管，这也意味着绿色，白色，蓝色，橙色和黄色显示器是可能的，这在 1971 年是没有人能想象的。