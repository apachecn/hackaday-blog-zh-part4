# 窥视编译器的代码——很多编译器

> 原文：<https://hackaday.com/2019/09/13/peek-into-the-compilers-code-lots-of-compilers/>

我们不知道正常人在争论什么，但我们知道我们花了很多时间争论最好的微控制器，哪个编辑器是最好的，什么语言或编译器做得最好。所有这些编译器的问题是加载它们并挖掘生成的代码。如果你也花时间思考这些事情，你应该看看[Matt god bolt]的[编译器资源管理器](https://godbolt.org)。我们知道托管一个类似 IDE 的网页和编译代码已经过时了——尽管[Matt 的]网站已经存在很长时间了。但是[马特]的做法不同。您在左侧窗格中构建的代码在右侧显示为汇编语言。

也有很多选择。例如，下面是网站示例中的一段 C 代码:

```
int square(int num) {
   return num * num;
}
```

以下是 gcc 9.2 中 x86-64 的相应汇编:

```
square:
  push rbp
  mov rbp, rsp
  mov DWORD PTR [rbp-4], edi
  mov eax, DWORD PTR [rbp-4]
  imul eax, eax
  pop rbp
  ret
```

然而，ARM64 gcc 8.2 输出:

```
square:
  sub sp, sp, #16
  str w0, [sp, 12]
  ldr w1, [sp, 12]
  ldr w0, [sp, 12]
  mul w0, w1, w0
  add sp, sp, 16
  ret
```

包括 AVR 在内的许多编译器都有选项。6502 和 MIPS。更有趣的是，它支持从 FORTRAN 到 Rust 和 Go 的许多其他语言。令人欣慰的是，源代码行的颜色与对应于该行的反汇编区域相匹配。

顺便提一下，如果您愿意，您可以单击底部的 Output 按钮并实际运行您的测试程序。如果你对该系统如何工作感兴趣，有一个[文档](https://xania.org/201609/how-compiler-explorer-runs-on-amazon)描述了该系统如何利用亚马逊的弹性云和 Docker。当然，自从那份文件写出来后，[马特的]做了很多修改，但至少它会给你一个大致的概念，而且你可以随时去他的 [GitHub](https://github.com/mattgodbolt/compiler-explorer-image) 回购中挖掘。

我们已经到了这样一个地步，为了学习的目的，我们有点喜欢这些基于网络的游戏场所。我们可能不会把价值百万美元的超级密码写在上面，但是我们在骗谁呢？没有人真的想阅读我们最新物联网[车库门](https://hackaday.com/2019/07/15/the-trials-and-tribulations-of-building-an-iot-garage-door-opener/)的源代码。