# 像素化文本不是一个好主意

> 原文：<https://hackaday.com/2022/02/23/pixelating-text-not-a-good-idea/>

在过去十年左右的时间里，人们对计算机安全已经变得更加了解了。大多数人都知道发送包含敏感信息的文档是不允许的，所以许多人尝试编校文档，并取得了不同程度的成功。一种常见的策略是用黑盒替换文本，但有时您会看到老练的用户将他们想要保密的图像或文档的一部分像素化。如果你对文本这样做，要小心。可以通过[软件](https://github.com/bishopfox/unredacter)对像素化图像进行解压缩。

看起来这个算法非常简单。它只是猜测字母，将它们像素化，然后匹配结果。你必须估计像素的大小，但这通常并不难做到。代码是使用 TypeScript 构建的，虽然这个过程确实需要一些手工准备，但是如果您有足够的动力，没有什么看起来非常困难或者不能自动化的。

你不像以前那样经常看到它，但已经有很多法律和政府丑闻，有人[通过在 PDF 上放一个黑盒](https://www.americanbar.org/groups/judicial/publications/judges_journal/2019/spring/embarrassing-redaction-failures/)来编辑文件，所以它在打印时被隐藏，但文本仍在文件中。如果你知道如何查看文件，旧的文字处理器通常也不会真的删除文本。脑海中浮现出[脸书的估值](https://hackaday.com/2009/02/12/pdf-redaction-still-not-working/)。更不用说[国家法律和政策中心](https://hackaday.com/2008/08/01/exposing-poorly-redacted-pdfs/)被糟糕的编辑技术刺痛。