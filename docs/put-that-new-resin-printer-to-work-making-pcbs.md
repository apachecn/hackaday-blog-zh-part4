# 让新的树脂打印机开始生产印刷电路板

> 原文：<https://hackaday.com/2020/10/09/put-that-new-resin-printer-to-work-making-pcbs/>

你可以在 3D 打印机上(相对)快速地制作出所有酷而有用的零件，但遗憾的是你不能只打印 PCB。当然，订购 PCB 又快又简单又便宜，但是能够一次性印刷就像是把针钉在了即时满足表上。

【Peter Liwyj】可能只是想出了[一个方法来做到这一点](https://www.instructables.com/SLA-3D-Printer-Acid-Etched-Circuit-Boards/)。他的 Instructables 帖子详细介绍了他的方法，使用了 Elegoo Mars 树脂打印机和一些巧妙的技巧。首先，将经过适当清洁的电路板铜面朝下放在印刷床上的一滴 SLA 树脂上。他通过中断用于检测归位的光电传感器来欺骗打印机，使其认为平台一直向下到达第一层。他让打印机穿过包含他设计的 STL 文件的一层，在铜上聚合一薄层塑料。轻轻擦去多余的树脂，然后将电路板直接放入氯化铁蚀刻槽中。下面的视频展示了整个过程。 

听起来很简单，但看起来确实很有效。[彼得]不只是偶然发现了这个方法；他系统地研究它，并找到了最有效的方法。他的建议包括使用电工胶带作为垫片，将铜从印刷表面稍微抬起，用 Scotchbrite 而不是砂纸清洁电路板，印刷后不要固化树脂。他的工具链有点不传统——他使用 SketchUp 创建轨迹并导出 STL。但是有[种方法可以将 Gerbers 转换成 STLs](https://solder-stencil.me/) ，所以你最喜欢的 EDA 包也可能适合这个过程。

没有树脂打印机？别担心，FDM 打印机也能工作。

 [https://www.youtube.com/embed/VIiDLfR7loA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VIiDLfR7loA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[abetusk]的提示。