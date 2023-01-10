# 将基于距离的 CAD 带到下一个级别

> 原文：<https://hackaday.com/2022/11/28/taking-distance-based-cad-to-the-next-level/>

对于那些经常建模 CAD 模型的人来说，一对卡尺是必不可少的，因为它允许合理精确的测量来适应特定的零件。然而，[杰森·哈里斯]将这一概念推向了一个新的高度，推出了一款基于[符号距离函数的 CAD 工具 SDFX](https://hackaday.io/project/85451-sdfx) 。

对于那些不知道的人，带符号的距离函数可以告诉你从一个给定点到模型的最近部分有多近。该模型被表示为提供一些令人兴奋的好处的单个函数。例如，倒角和锉削在传统的 CAD 程序中通常非常复杂，而在 SDF 设置中则微不足道。SDFX 是一个 golang 库，允许您编写 golang 程序来描述模型。OpenSCAD 是 Hackaday 的最爱，因为它是一个漂亮的参数化代码优先 CAD 软件包。但是从最好的方面来说，它的语法和语言有些笨拙。使用 golang 而不是 [DSL](https://en.wikipedia.org/wiki/Domain-specific_language) 的优势在于，你可以利用一种全功能语言带来的所有好处。例如，您可以导出多个对象，发出网络请求，并与 GUI 库接口以[重新创建类似 OpenSCAD 定制器](https://hackaday.com/2017/06/27/a-crash-course-in-thingiverse-customizer/)的东西。

使用行进正方形将对象渲染到 STL。然后，它们可以用任何你喜欢的切片软件打印出来。这是一个优秀的项目，有很棒的 API 和近百个例子。

代码[在 GitHub](https://github.com/deadsy/sdfx) 上有麻省理工学院的许可。