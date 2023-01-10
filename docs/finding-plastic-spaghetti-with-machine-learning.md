# 用机器学习寻找塑料意大利面

> 原文：<https://hackaday.com/2019/03/29/finding-plastic-spaghetti-with-machine-learning/>

在 3D 打印机用户中，“意大利面条”是一种常见的术语，指的是打印失败后产生的一团乱麻。害怕他们的打印床变成一盘热的 PLA 意大利面条足以让许多用户整夜或在他们出门时不关机器。因此，我们已经看到了许多方法，允许操作员远程观看他们的打印，以确保一切顺利进行。

但是，除非你打算在出门的时候一直盯着手机，否则一些 PETG 意大利面还是有可能偷偷溜出去。进入[意大利面侦探，一个开源项目，当你不能整天坐着看打印机时，让机器学习接管](https://thespaghettidetective.com/)。他们的系统插入 Octoprint，实时监控你的打印，如果它开始看起来特别粗糙，就暂停打印。这个概念仍在开发中，但从用户提交的结果来看，该系统似乎有识别非食用面条的诀窍。

一旦该软件退出测试，看起来该团队将试图通过提供每月收费的托管和监控服务来赚钱，[但由于它是一个开源项目](https://github.com/TheSpaghettiDetective/TheSpaghettiDetective)，你也可以在自己的机器上运行该软件。虽然文档指出，低级的 Raspberry Pi 不具备处理图像识别例程的能力，所以如果您想自己托管该服务，您需要一台合适的计算机。你放在实验室里的那台旧笔记本电脑可能会派上用场。

正如休息后的视频所展示的那样，该系统的“意大利面信心”是通过一个简单易懂的标准来显示的:绿色是一个好看的打印，红色意味着侦探正在嗅一嗅粘稠的东西。如果您的打印陷入红色太多，Octoprint 会被命令暂停打印。然后，用户可以查看打印机的最后一张图像，并决定要么完全取消打印，要么在意大利面侦探有点过于热心的情况下继续。

坦率地说，这是一个非常好的想法，我们非常有兴趣看看它从这里走向何方。[假设你已经用 Octoprint 控制你的 3D 打印机](http://hackaday.com/2018/01/03/upgrading-a-3d-printer-with-octoprint/)目前有[一些非常聪明的监控系统](http://hackaday.com/2019/03/27/monitor-your-3d-printer-with-node-red-and-tasker/)，但是既然意大利面[不是流氓 3D 打印机唯一能做的](http://hackaday.com/2018/03/18/3d-printer-halts-and-catches-fire-analysis-finds-a-surprising-culprit/)，多一道防线对我们来说听起来是个好主意。

 [https://www.youtube.com/embed/ZpDw9mNBngU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZpDw9mNBngU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

