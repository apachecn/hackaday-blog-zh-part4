# 用 PCB 和灯光制作的伦敦地铁实况地图

> 原文：<https://hackaday.com/2020/07/05/live-map-of-london-tube-created-in-pcb-and-lights/>

如果你经常乘坐公共交通系统，了解火车或公共汽车何时到达以及是否有任何延误会很有帮助。我们可能会将平板电脑安装在墙上，但这依赖于保持操作系统、软件及其库的更新。为了真正的可靠性，你需要直接在硬件中构建，[这正是这张伦敦地铁系统地图所使用的](https://www.ianvisits.co.uk/blog/2020/06/23/check-out-this-london-tube-map-made-from-a-working-circuit-board/)。

基本地图直接印在印刷电路板上，每条主要路线上的发光二极管指示列车的当前位置。一些小芯片处理 WiFi 连接——在我们看来是 ESP8266——并从伦敦地铁 API 中提取有关列车的信息(实际上不可能在硬件中为这个项目构建*一切*。硬件可以很容易地重新编程，与 PCB 布局，这可以适应其他公共交通相当容易。

即使抛开硬件和软件方法在设计上的哲学差异，我们仍然欣赏 PCB 上 led 的美感。事实上，自从价格在过去二十年里大幅下降以来，我们已经看到了大量的印刷电路板艺术品。

感谢[Al]的提示！