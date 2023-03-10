# 简化工具链

> 原文：<https://hackaday.com/2022/09/03/streamlining-the-toolchain/>

有时候我试着做一些神奇的事情，而且很有效。大多数情况下，这是因为其他人已经为我做了很好的一部分工作，并与我分享。我只是将一些现有的工具拼凑成一个适合我需求的流程。但是当太多的步骤涉及到人工干预时，所有部分的总和往往小于整体。为人们制造的工具只是让人们处于循环中。

例如，我想把我儿子画的一张图做成一枚邮票，通过数控机器和我们在地下室里找到的任何废木料。这很简单，真的。拍摄照片，也许在 GIMP 中稍加调整以获得正确的级别，将它导出到 Inkscape 进行线条检测，甚至可能在那里制作 GCode，或者使用任何方便的 SVG-to-GCode 工具。

虽然这对我来说是现成的，但事实证明这是因为我有使用所有子工具的经验。首先，如果你一开始就获得正确的曝光会有很大帮助，当你相机的测光表瞄准灰色时，这不是微不足道的，但绘图是在白纸上。知道了这一点，我想你可以设置它总是过度曝光。

尽管如此，后期处理还是需要一些经验的。如果你没有玩过图像处理软件*和图像编辑软件*，你就不知道它们会如何交互。最后，要完成数控铣削，需要调整的参数比初学者需要决定的要多。

简而言之，我很快就建立并运行了一个工具链，这是一个成功。但是就把它传递给我儿子而言，这是一个失败，因为他将不得不学习太多的子工具来让它为他工作。真扫兴。我在想，我是否能简化所有的部分，让它们足够好地协同工作，或者我是否只是这个循环中的一员。

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!