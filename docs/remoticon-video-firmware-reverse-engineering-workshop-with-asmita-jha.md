# Remoticon 视频:固件逆向工程研讨会与阿释密达 Jha

> 原文：<https://hackaday.com/2020/11/19/remoticon-video-firmware-reverse-engineering-workshop-with-asmita-jha/>

把东西拆开来看看它们是如何工作的是理解一个系统的重要部分，这对软件和硬件都一样。你可以[通过阿释密达·贾的研讨会](https://www.youtube.com/watch?v=ccgB3UuCxjE)开始你的固件逆向工程技能，该研讨会在 Hackaday Remoticon 现场直播。该视频刚刚发布，可在下面找到，以及她在实际操作实验中涉及的更多内容。

 [https://www.youtube.com/embed/ccgB3UuCxjE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ccgB3UuCxjE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



当研究一个不熟悉的二进制文件时，从哪里开始呢？两小时研讨会的第一部分解决这个问题。阿释密达采用系统的方法来计算出你已经得到了什么，以及什么方法最有可能成功。

静态分析所需的工具可能是您已经熟悉的名字:Binwalk、John the Ripper、Ghidra、Firmwalker、FACT Tool 和 EXPLIoT Firmware Auditor。四个实验室中的三个使用这些工具来练习一些事情，如提取固件二进制文件以找到硬编码的凭证，修改和重新打包二进制文件，以及破解内部找到的密码。还有一个动态分析的例子，其中编译固件的硬件架构不同于您用于逆向工程的计算机。在这种情况下，你可以使用 Qemu 的风格来理解它。

在研讨会进行到一半时，动手实验开始了。您可以使用研讨会页面上的研讨会幻灯片和设置说明[进行操作。](https://hackaday.io/project/175081-remoticon-intro-to-firmware-reverse-engineering)