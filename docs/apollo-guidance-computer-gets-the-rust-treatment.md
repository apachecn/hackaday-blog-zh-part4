# 阿波罗制导计算机进行了防锈处理

> 原文：<https://hackaday.com/2022/01/29/apollo-guidance-computer-gets-the-rust-treatment/>

似乎最近所有的酷孩子都在用 Rust 重写传统的 C 程序，所以我们认为，有人决定将内存安全语言与一些历史上最重要的软件结合起来只是时间问题，这些软件是通过一种新的阿波罗制导计算机(AGC)仿真器编写的。由[Felipe]编写的 Apache/MIT 授权仿真器既可以运行由计算机的原始 rope 核心内存制作的 ROM 文件，也可以运行您自己用 AGC4 汇编语言编写的代码。

值得注意的是，名为`ragc`的模拟器需要一些帮助才能提供真实的登月体验。具体来说，代码只是模拟 AGC 本身，并没有重新创建图标显示和键盘(DSKY)模块。为了与虚拟 AGC 上运行的程序进行交互，你还需要安装 yaDSKY2，这是一个开源项目，它以图形方式再现了阿波罗宇航员实际用于输入命令和从计算机获取数据的面板。

当然，下一步将是黑掉对与 DSKY 中的[实体娱乐之一对话的支持，这些年来](https://hackaday.com/2020/09/23/apollo-dsky-replica-looks-the-part/)[一直为这些页面增光添彩](https://hackaday.com/2018/02/02/start-your-apollo-collection-with-an-open-source-dsky/)。鉴于 AGC 的局限性，我们不会称这样的安排有用，但它肯定会成为黑客空间的一个很好的话题。

谢谢你的提示，[CJ]。