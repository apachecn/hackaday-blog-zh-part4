# 用一份可启动的简历展示你的技能

> 原文：<https://hackaday.com/2019/03/23/show-your-skills-with-a-bootable-cv/>

找工作是件吃力不讨好的事。你寄出你的简历，它会加入一千份其他的简历中。你到底能做些什么来让你的职业脱颖而出，抓住招聘者的眼球？

[![Your bootable CV isn't eye-catching if the recruiter uses GitHub to view the PDF.](img/8757b45564390e2485e2d2a45a43d07b.png)](https://hackaday.com/wp-content/uploads/2019/03/github-pdf-fail.jpg)

Your bootable CV isn’t eye-catching if the recruiter uses GitHub to view the PDF.

如果你是[巴勃罗·希门尼斯·马特奥]，答案就够直接了。简单地用 x86 引导程序将文档组合成 PDF 格式，以制作一个可读的文档，该文档也将引导 x86 计算机系统。他可以通过将引导程序文件添加到 PDF 中相对容易地做到这一点，只要 CV 的“%PDF”头保持在前 1024 个字节内，它就仍然是一个可读的文档。确实如此，尽管正如我们的 GitHub 截图所示，并不是在*所有的* PDF 阅读器中。

一个可启动的 PDF 是非常酷的，我们必须向他的努力致敬，他把它放在我们面前，希望能促进职业生涯，但公平地说，这是一个以前做过的把戏。所以是时候将注意力转向引导加载程序本身了，它的代码以一个注释非常好的汇编文件的形式出现，该文件加载一些精灵和一个 VGA 屏幕的边框，看起来好像它可能是自上而下的冒险游戏中的第一个房间。通过这段代码，我们可以体会到 bootloader 有多简单，这本身就让这个项目值得再看一眼。

如果你对编写自己的引导程序感兴趣，[这肯定是我们过去讨论过的话题](https://hackaday.com/2017/10/23/write-your-own-x86-bootloader/)。有可能把可引导图像做得非常小，[甚至小到适合一条 Tweet](https://hackaday.com/2018/08/02/cd-image-via-twitter-a-handcrafted-game-disc/) 。