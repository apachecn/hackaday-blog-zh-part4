# 将 FPGA 开发带给大众

> 原文：<https://hackaday.com/2019/07/05/bringing-fpga-development-to-the-masses/>

现场可编程门阵列(FPGA)是现代黑客武器库中最令人兴奋的工具之一。如果你能掌握 FPGA，你就能创造出硬件设备，不仅能根据你当前的需求变形和改变，还能以惊人的速度完成重复的任务。唯一的问题是，对于新手来说，使用 FPGAs 可能有点吓人。有人可能会说，这项技术正在等待它的“Arduino”时刻；廉价开发板的推出，加上易于使用的软件，使 FPGA 黑客成为主流。

[![](img/5110ced064534efd59619e9dfa69fb69.png)](https://hackaday.com/wp-content/uploads/2019/07/webfpga_detail.jpg) 如果一切按计划进行，等待可能很快就会结束。[Ryan Jacobs]相信他的项目 [WebFPGA 是最简单快捷的方法，让你接触到这项令人难以置信的技术](https://www.kickstarter.com/projects/ryanmjacobs/webfpga-rapid-fpga-development-system)。从表面上看，硬件可以被视为 Arduino Nano 克隆，在一个小型试验板友好的 PCB 上有一堆 GPIO 引脚和几个 led。毫无疑问，这是一场朴实无华的演讲。有趣的是软件方面:你只需要为 FPGA 开发一个现代的网络浏览器。

目前支持 Chrome、Opera 和 Edge，即使它们运行在相对低端的计算机上。[Ryan]表示，这使得在学校推出 FPGA 课程变得更加容易和便宜，因为学生可以使用现有的 Chromebooks 做任何事情。正如休息后的视频所示，你甚至可以使用足够强大的智能手机在旅途中进行一些 FPGA 黑客攻击。

那么诀窍是什么呢？本质上，繁重的工作是远程完成的:所有的合成都在他们的云后端执行，最终的比特流通过 WebUSB 交付给用户进行安装。如果你更喜欢命令行，[Ryan]说他们目前正在开发工具，可以让你在没有浏览器的情况下与他们的云服务进行所有必要的交互。

更挑剔的黑客读者可能会担心锁定。如果您购买了这些开发板中的一个，却没有服务许可，或者更糟，如果 WebFPGA 破产了，会发生什么？为此，[Ryan]明确表示他们的硬件完全兼容现有的离线 FPGA 开发工具，如开源的 ice storm。

我们已经看到了人们对低成本 FPGA 开发平台的极大兴趣，读者可能还记得围绕 Pano Logic 瘦客户端大甩卖的兴奋之情。尽管[努力使这些系统的开发更加容易](https://hackaday.com/2019/04/19/pano-logic-fgpa-hacking-just-got-easier/)，很难想象门槛会比 WebFPGA 的目标低得多。他们的 Kickstarter 活动已经接近终点，我们非常有兴趣看看该产品将何去何从。

 [https://www.youtube.com/embed/dSsQJl0VENI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dSsQJl0VENI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

