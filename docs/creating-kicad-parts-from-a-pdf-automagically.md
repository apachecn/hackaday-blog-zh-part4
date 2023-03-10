# 从 pdf 自动创建 kicad 零件

> 原文：<https://hackaday.com/2018/10/05/creating-kicad-parts-from-a-pdf-automagically/>

对于那些曾经为 Eagle 或 KiCad 努力寻找角色的人来说，有些人会说你做错了。如果你在已有的库中找不到，你应该自己制作零件。这真的是唯一的办法；PCB 设计工具是工具，所以你永远不会成为大师，除非你能自己制作零件。

也就是说，制作示意性零件和足迹是一件痛苦的事情，如果有工具可以自动化这个过程，我们会很乐意使用它。[这正是 uConfig 所做的](https://github.com/Robotips/uConfig)。它自动从 PDF 数据表中提取引出线信息，并将其转换为原理图符号。

uConfig 是来自[sebastien caux]的一个老项目，它已经复活并变成了一个开源工具。它的工作原理是从 PDF 中提取文本块，整理出 pin 号和 pin 标签，并通过相关名称将它们关联起来以制作 pin。它可以作为一个预构建的项目使用(甚至可以用于 Windows！)，工作起来有点像魔术。

下面的视频演示展示了 uConfig 导入 PDF 数据表——在本例中为 pic 32——自动从数据表中提取封装，并将其转换为原理图符号。它甚至看起来好像也能工作。当然，这只是原理图符号，并不是包括封装尺寸在内的全部内容，但就封装尺寸而言，我们可能是在处理标准封装。如果你想开发一个软件工具，它可以获取数据手册，并提供完整的器件、尺寸和所有信息，这就是开始的地方。

 [https://www.youtube.com/embed/hW518srZXXQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hW518srZXXQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

