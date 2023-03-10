# MCH2022 徽章 CTF 解决了，有很多值得借鉴的地方

> 原文：<https://hackaday.com/2022/08/07/mch2022-badge-ctf-solved-with-plenty-to-learn-from/>

在 MCH2022 上你可以找到的所有东西中，有几个 CTF(捕捉旗帜练习)——特别是，每个徽章都包含一个你可以尝试闯入的应用程序——只有两个团队破解了这个！[dojoe]是他们中的一员，他为我们撰写了一个广泛的逆向工程故事——包括 Ghidra 对 Xtensa 代码的反汇编、远程代码执行尝试、ROP 小工具创建，没有留下任何细节。

有一个问题:发给参与者的徽章并不包含真正的旗帜。您必须使用您的个人徽章开发一个漏洞，该徽章只包含一个占位符标志，然后前往徽章帐篷，通过网络将您的漏洞应用到少数几个带有真正标志的徽章之一。有问题的应用程序原来是一个 echo 服务器——发回它收到的所有信息；值得注意的是，某些信息使它崩溃。一个人的崩溃是另一个人利用的可能性，在几次黑客会议之后，[dojoe]的团队在记分牌上获得了他们应得的位置。

如果你一直认为固件逆向工程听起来很酷，并且你也碰巧拥有一个 MCH2022 徽章，那么你应该试着按照[dojoe]的文章中错综复杂的步骤去做。即使对于几乎没有低级编程经验的人来说，由于他的大量解释，重复这种技巧也是现实的，并且您将获得比以前更多的逆向工程经验。

[mch 2022 徽章](https://hackaday.com/2022/05/04/the-mch2022-badge-has-landed/)是复杂工程的特色创造，ESP32 部分只是徽章的一部分——[鉴于它所提供的一切，我们渴望听到](https://hackaday.com/submit-a-tip/)关于你已经完成或将要完成的事情！