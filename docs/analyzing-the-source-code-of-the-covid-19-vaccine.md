# 分析新冠肺炎疫苗的“源代码”

> 原文：<https://hackaday.com/2020/12/26/analyzing-the-source-code-of-the-covid-19-vaccine/>

计算机程序是用代码编写的，代码有多种形式。在最底层，有机器码和汇编，而像 C 和 Python 这样的高级语言的目标是更易于人类阅读。然而，自然界也有源代码，以 DNA 和 RNA 串的形式存在，其中包含了构建生命的代码。 [[Bert]决定看看由 BioNTech 和 Pfizer 开发的新冠肺炎疫苗 Tozinameran 的 mRNA 源代码。](https://berthub.eu/articles/posts/reverse-engineering-source-code-of-the-biontech-pfizer-vaccine/)

这种分析对普通读者来说足够简单，但仍然解释了生物学前沿的一些高度复杂的概念。从提高效率的密码子替换和避免疫苗被免疫系统破坏的ψ碱基替换，到 RNA 序列开始时所需的复杂初始化字符串，[Bert]清楚地解释了使疫苗成为可能的巧妙编码技巧。特别值得注意的是脯氨酸酶替代，[这是一种在 2017 年开发的技术。](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5584442/)这允许在分离整个病毒的情况下生产冠状病毒刺突蛋白，以便安全地启动免疫系统。

这是一本很好的入门书，我们可以想象它可能会激励一些人更深入地研究遗传学和生物学的丰富世界。我们还特别报道了新冠肺炎的其他前沿新闻；[【Dan Maloney】看看 CRISPR 技术是如何帮助测试工作的](https://hackaday.com/2020/05/27/coronavirus-testing-crispr-technology-set-to-streamline-viral-testing/)。如果说 2020 年的疫情展示了什么，那就是人类在危机面前快速开发新技术的能力。