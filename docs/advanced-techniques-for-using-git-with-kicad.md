# 使用 Git 和 KiCAD 的高级技术

> 原文：<https://hackaday.com/2018/09/19/advanced-techniques-for-using-git-with-kicad/>

对于大多数开发人员来说，“分布式版本控制”可能意味着 git。但是 git 本身不能很好地处理二进制文件，如图像、zip 文件等，因为 git 不知道如何理解任意字节块的结构。因此，当试图找出如何跟踪大多数 EDA 工具创建的设计文件中的变化时，git 没有得到认可，设计师可能会被困在 SVN 地狱中。事实证明，虽然 KiCAD 的设计文件可能没有像。txt，它们*从根本上来说是*文本文件(如果你曾经试图绕过 KiCAD 的一些限制，你可能会知道)。通过对[【吉恩·诺尔】的指南](https://jnavila.github.io/plotkicadsch/)做一些调整，你将会变得与众不同。亲的和。sch 泰然自若。

该文档有几个部分(它实际上是另一个工具的开始，我们已经在[的另一篇文章](https://hackaday.com/2018/09/19/visual-schematic-diffs-in-kicad-help-find-changes/)中提到过)。第一部分描述了回购应该跟踪哪些文件，以及哪些。gitignore 可以配置为避免。如果这没有任何意义，那么花时间学习如何用魔法保持一个干净的回购是值得的。gitignore 文件，git 将查找该文件，以查看是否有应该避免暂存的文件类型或路径。

第二部分描述了如何使用两个漂亮的 git 特性， [cleaning 和 smudging](https://git-scm.com/book/en/v2/Customizing-Git-Git-Attributes#_keyword_expansion) ，在文件签入和签出 repo 时动态地修改文件。[jean-nol]观察到，即使没有面向用户的更改，KiCAD 也会接触到某些文件，这会使补丁集中出现不相关的更改。他建议的过滤器通过在文件被签入时去除那些改变来防止这种情况。相当狡猾。