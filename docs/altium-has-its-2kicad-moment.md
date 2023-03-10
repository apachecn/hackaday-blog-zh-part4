# Altium 有它的 2kicad 时刻

> 原文：<https://hackaday.com/2020/04/14/altium-has-its-2kicad-moment/>

在这些地方，我们倾向于成为 KiCad 生活方式的拥护者；有什么比使用可以在任何地方运行的免费开源工具来设计 PCBA 更好的方法呢？但是商业 EDA 包中仍然有一些功能没有进入 KiCad，所以它可能并不总是最好的工具。Altium Designer 是一个受欢迎的非自由选择，但每个座位高达数万美元，对于没有严重需求的用户和企业来说，它并不总是一个很好的选择。

![](img/638acccf75b98722d3ed6158506f2cf9.png)

It’s hard to find an exciting photo of a dialog box

作为一个 KiCad 用户，当你在 Altium 中遇到一个你想使用的设计时，你会怎么做？截至 2020 年 4 月 3 日，[Thomas Pointhuber]已经将一个本地 Altium 导入器的开端合并到 KiCad 中，该导入器可能会在 6.0 版本中发布。正如[Thomas]自己在补丁提交中指出的，这已经不是第一次发布第三方 Altium 导入程序了。他的新作品是由[the sourcer 8]翻译的 [Perl 插件 altium2kicad](https://github.com/thesourcerer8/altium2kicad) 。早在一月份，另一个用户给[留下了一条评论，链接到其他四个](https://gitlab.com/kicad/code/kicad/-/merge_requests/60#note_270402879)处理 Altium 文件的工具(非 KiCad)。

如果你想亲自尝试这个漂亮的新特性， [CNX 有一个很棒的演示](https://www.cnx-software.com/2020/04/05/how-to-build-kicad-on-ubuntu-18-04-and-import-altium-pcb-files/)从源代码构建 KiCad 开始。至于用来测试经典[猎兔犬骨黑源](https://github.com/CircuitCo/-BeagleBone-Black-RevA5)的文件，可以在 GitHub 上找到。休息时间过后，请观看由[Thomas]本人提供的非常无聊但非常激动人心的进口商工作视频。我们迫不及待地想尝试一下！

谢谢你的提示[克里斯·甘梅尔]！

> 最后，将 [#altium](https://twitter.com/hashtag/altium?src=hash&ref_src=twsrc%5Etfw) 板导入到 [#kicad](https://twitter.com/hashtag/kicad?src=hash&ref_src=twsrc%5Etfw) 中只需一次点击(在开发者版本中)。
> 
> 这允许查看和编辑用[#专有](https://twitter.com/hashtag/proprietary?src=hash&ref_src=twsrc%5Etfw)软件设计的[#开源](https://twitter.com/hashtag/opensource?src=hash&ref_src=twsrc%5Etfw)[#硬件](https://twitter.com/hashtag/hardware?src=hash&ref_src=twsrc%5Etfw)，因此，事实上，不是对所有人开放。[pic.twitter.com/oogiJeyynW](https://t.co/oogiJeyynW)
> 
> —Thomas point Huber(@ Chaos _ Robotic)[2020 年 4 月 4 日](https://twitter.com/Chaos_Robotic/status/1246360312133099520?ref_src=twsrc%5Etfw)