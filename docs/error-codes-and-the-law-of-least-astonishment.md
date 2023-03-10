# 错误代码和最小惊讶定律

> 原文：<https://hackaday.com/2021/12/17/error-codes-and-the-law-of-least-astonishment/>

你知道最小惊讶定律吗？我不确定它的起源，但我首先从编程的优秀的“[陶”那里学到了它。简而言之，这是一个原则，即软件应该总是以最少让用户吃惊的方式来响应用户。换句话说，打印文档不应该把它从你的文件系统中删除。](https://www.mit.edu/~xela/tao.html)

遵循最小惊讶定律，当程序遇到硬错误时应该怎么做？你可能会说它应该让用户知道。不幸的是，如今许多系统只是将其掩盖起来。

我想是从 Windows 开始的。或者是苹果电脑。人们的想法是，最终用户太愚蠢或者太害怕错误代码或详细的消息，所以我们只是将它们排除在外。例证:我妻子的 iPhone 不能上传图片。我不是专家，因为我带着一个 Android 设备，但我同意看看它。无论我怎么尝试，我都得到同样无用的消息:“现在无法上传照片。请稍后再试。这不仅不太能说明问题，而且还意味着问题出在某个可以在以后自我修复的东西上，比如网络。

真正的罪魁祸首？iCloud 的服务条款已经改变，她没有接受新的合同。我有一种感觉，它可能会在某个时候突然出现，要求她这样做，但不管出于什么原因，她错过了。除非你深入了解设置并勾选同意这些条款，否则“以后”永远不会发生。

但不仅仅是 iPhones。Windows 中有很多类似的东西，你只希望在事件查看器中有一个日志，提供更多的细节。我现在在 Linux 上也看到了更多，尽管如果你知道如何找到它，通常在某个地方会有一个日志文件。虽然我知道有错误的程序有让用户吃惊的风险，但是如果没有错误的解释，那就更令人吃惊了。想象一下，如果你的银行给你发了一张纸条:你的账户有问题。所以你回应:“我透支了吗？”他们回答，“没有。”现在怎么办？这就是今天许多软件错误的状态。

在桌面系统或网站上真的没有借口。然而，你可能想要原谅微小的嵌入式系统。不要！我最近将 3D 打印机固件 Marlin 移植到 ANET A8 板上，这是一种 8 位处理器，内存很少，已经在 Repetier 固件上使用了多年。我第一次尝试自动水平探测时，得到的信息是:探测失败。就是这样。

我同意你，你可以打开自动调试来获得更多信息，但我已经达到 98%的闪存利用率，所以这将需要暂时删除一些功能并重建代码。但是为什么不像过去那样做:

```
unit global_error=0;
void do_something(void) {
   global_error=1;
   if (process1()==FAIL)  return;
   global_error++;
   if (process2()==FAIL) return;
. . .

   global_error=0;
   return;
}
```

这个不占多大空间。现在，您可以报告类似探测失败(8)这样的情况，我至少可以查看代码并确定失败的第 8 步是什么。我敢肯定，有人甚至会贴出一个代码列表，说明在这种情况下它们意味着什么。

开销太大？告诉我出错的程序计数器。这在过去是很常见的做法。当然，这需要你[有一个内存映射文件，并知道如何读取它](https://hackaday.com/2021/12/16/keynote-video-elecia-white-finds-treasure-in-memory-map/)，但总比没有好。

我们花很多时间思考项目和软件应该如何工作。但我们也需要花时间思考，当它们不起作用时会发生什么。我们可以进行在线调试或连接逻辑分析仪，这很好，但这对我们的用户没有帮助。即使只是为了你，为什么不让自己轻松一点呢？

正如我们之前说过的，“没有太多的信息”除了防止系统错误，你还可以帮助用户[不要让自己震惊](https://hackaday.com/2021/08/25/tech-in-plain-site-check-digits-and-human-error/)。

图片来源:[Elisa Ventur]via Unsplash.com