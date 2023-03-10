# 冲浪传感器增加了寻找终极波浪的深度

> 原文：<https://hackaday.com/2021/10/25/surf-sensor-adds-depth-to-finding-the-ultimate-wave/>

说海洋是一个动态的环境是一种轻描淡写的说法，尤其是在涉及海岸线的时候。海浪撞击，潮汐涨落，无数的变数使得即使是平常的情况也成了猜谜游戏。当[foobarbecue]去冲浪时，他试图考虑所有这些事情。他当地海滩上最好的波浪就在不断移动的沙坝正上方，它们的动态受深度(另一个恒定变量)的影响。【foobarbecue】了解时局的绝妙解决方案？[直接在他的冲浪板上安装一个深度探测器](https://foobarbecue.github.io/surfsonar/)！

“surfsonar”的核心是 Ping 声纳回声探测仪，这是一种为 AUV 和 ROV 设计的声纳传感器。[foobarbecue]将传感器直接嵌入电路板。数据被输入到一个 Raspberry Pi 4b，它在一个 2.13 英寸的电子纸显示帽上显示深度和置信度(对测量有多大把握的百分比)。

电力是由一艘皮苏加尔号提供的。充电是无线完成的，考虑到整个设备是密封在一个经过改造的冲浪板内，我们会说这是非常重要的。

虽然这不是一个低预算的建设，但仍有改进的空间，早期的报告是积极的。一旦远离破碎的波浪，该设备自信地显示深度。更多的测试将会显示 surfsonar 是否能帮助[foobarbecue]找到那个不停移动的沙洲！

冲浪黑客总是受欢迎的，我们已经展示了 [LED 条形照明冲浪板](https://hackaday.com/2020/09/10/surfboard-led-strips-light-up-the-waves/)以及[冲浪窗口](https://hackaday.com/2019/10/24/hang-ten-with-help-from-the-surf-window/)，它会告诉它的主人冲浪是否开始。请务必通过我们的[提示热线](https://hackaday.com/submit-a-tip/)让我们知道你在网上冲浪时发现的任何很酷的技巧！