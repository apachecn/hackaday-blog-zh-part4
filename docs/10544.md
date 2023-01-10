# 模拟游戏机打印机的实际纸张输出

> 原文：<https://hackaday.com/2021/06/25/simulating-the-game-boy-printers-actual-paper-output/>

有时候，我们欣赏电子设备并不是因为它们的出色性能和清晰的输出，而是因为它们以一种独特而迷人的方式吸引着我们。Game Boy 相机和它的伙伴 Game Boy 打印机正是因为这个原因而备受喜爱。[【Raphael BOICHOT】决定用代码模拟后者打印机输出的模拟现实，并着手进行繁重的编码任务。](https://github.com/Raphael-Boichot/GameboyPrinterPaperSimulation)

结果是 Game Boy 打印机纸张模拟，它很好地再现了原始热敏打印机的粒状、有点嘈杂的输出。该模拟是在对原始打印机输出的多次高分辨率扫描的帮助下进行编码的，这使得[Raphael]能够创建一个数学模型，描述当热热敏打印头投入使用时，原始数字像素化图像是如何产生的。

从一个点开始的东西变成了一个成熟的仿真包，可以在 MATLAB 和 Octave 中运行。它允许最终用户生成看起来合法的 Game Boy 打印机输出图像，而实际上不必拥有打印机和一卷热敏纸。

我们以前见过任天堂备受喜爱的打印机，比如这次将它变成 8 位照片枪的黑客攻击。如果你自己也在摆弄热敏打印机，[一定要让我们知道！](http://hackaday.com/submit-a-tip)