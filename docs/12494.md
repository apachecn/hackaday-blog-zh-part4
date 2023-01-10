# EzCAD 的开源替代品

> 原文：<https://hackaday.com/2022/01/16/open-source-replacement-for-ezcad/>

[Bryce]去年秋天获得了一台光纤激光雕刻机，用于快速 PCB 原型制作。但他很快就对这些设备和类似设备通常配备的标准 EzCAD 软件的局限性感到失望——它是专有的，没有针对 PCB 制造的功能，只能在 Windows 上运行，而且漏洞百出。正如一个人所做的，[Bryce]决定抛弃 EzCAD 并[编写他自己的工具，Balor](https://www.bryce.pw/engraver.html) ，以佛摩人之王的名字命名。

[Bryce]机器中的控制器板是北京 JCZ LMCV4-FIBER-M 板，包含 Altera FPGA 和 Cypress 8051 USB 控制器。到目前为止，他还不需要转储或修改 FPGA 或 8051 代码。相反，他通过观察运行 know 操作的 EzCAD 副本生成的 USB 操作来整理命令。很多雕刻系统都使用这种控制板，但[Bryce]希望从使用不同板的用户那里收集数据转储，以便扩展库。

Balor 是用 Python 编写的，提供了一套命令行工具，旨在用于雕刻师的工程应用，尽管也支持常规激光打标。您可以从[项目的 GitLab 资源库](https://gitlab.com/bryce15/balor)下载该程序。他在 Linux 上运行它，但它应该可以在 Mac 和 Windows 上运行(如果您有任何可移植性问题，请告诉他)。看看我们去年写的关于[用这些激光制造 PCB](https://hackaday.com/2021/01/11/laser-blasts-out-high-quality-pcbs/)的文章。你在你的店里使用激光雕刻机制作快速原型板吗？请在评论中告诉我们你的设置。