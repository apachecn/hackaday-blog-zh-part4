# 绘图仪用胶带卷制作标签

> 原文：<https://hackaday.com/2022/09/03/plotter-churns-out-labels-with-roll-of-tape/>

不管你喜不喜欢，不时整理你的工作空间是一项必要的工作。标签对于驯服最难驾驭的长椅大有帮助，但是手写标签并不理想。为了寻找更简洁的东西，[桑迪]建造了一个简单的[笔式绘图仪，在一卷胶带](https://hackaday.io/project/186912-diy-label-printing-machine)上写标签。

![Pen plotter writing on roll of masking tape](img/e0e480b3691c1c22243ed678fec36c01.png)

绘图仪使用常见的 3D 打印机组件，如步进器、驱动器、皮带和轨道。该磁带持有人印有灵活的手臂握得很紧，伺服系统用于在书写时升高和降低笔。

[定制控制板](https://oshwlab.com/sharmaz747/multipurpose-pcb_copy_copy_copy)包括一个 Arduino Nano 克隆和一对步进驱动器，以及一个可选的蓝牙模块，可以针对各种机器控制应用进行配置。一对 Android 应用程序用于生成 g 代码，并将其从手机发送到 Arduino 上加载的 GRBL 固件。

这似乎属于“入门级”定制自动化工具的范畴，它有助于在重复任务上节省一些时间和精力，而不会超出预算。我们将包括我们在这个类别中[见过的各种](https://hackaday.com/2022/06/07/automate-parts-kitting-with-this-innovative-smd-tape-slicer/)[元件胶带切割器](https://hackaday.com/2020/02/07/automatic-component-tape-cutter-for-when-your-electronics-kit-hits-the-big-time/)，以及用于手动 PCB 组装的[智能构建平台](https://hackaday.com/2022/06/07/automate-parts-kitting-with-this-innovative-smd-tape-slicer/)