# 达到宁静:将 Git 移植到自制操作系统

> 原文：<https://hackaday.com/2020/02/23/reaching-serenity-porting-git-to-a-homebrew-operating-system/>

生活充满了小小的快乐——比如早上醒来，意识到在你真正起床之前还有足够的时间。或者在城市慢慢苏醒的时候起床观看令人愉快的日出，或者像[Andreas Kling]选择的那样，[将你最喜欢的开发工具移植到你编写的操作系统上](https://www.youtube.com/watch?v=1-7VQwWo2Tg)。

考虑到 90 年代 UI 设计的美学和更简单的 2000 年代 Unix 风格系统内核的功能，以及让自己忙碌的个人原因，[Andreas]不久前开始了 [SerenityOS](https://github.com/SerenityOS/serenity/) 。当然，编写你自己的操作系统总是一个很好的教育练习，但是它需要一定的投入才能超越实验阶段。所以理想情况下，你最终会想把它作为你实际的主系统，然而，作为软件开发人员，[Andreas]缺少一个关键的组件:git。嗯，他决定改变这一点，只是移植它——作为一个喜欢记录他的黑客会议的人，你可以一路观察他。

不可否认，看着某人调整一些构建工具和编译器设置通常听起来一点也不令人兴奋，但对于从头开始编写的正在进行的操作系统来说，这样做又增加了几个层次——从深入研究 libc 实现到对构建环境几乎是逆向工程的方法。如果你对人们解决问题的思维过程和(剧透警告)他们的成功感到高兴，你会喜欢看(安德烈亚斯)。另一方面，如果你对桌面操作系统的新方法更感兴趣，SerenityOS 本身可能值得一试。当然，[还有其他的选择。](https://hackaday.com/2017/08/20/forget-troy-try-helenos/)

 [https://www.youtube.com/embed/1-7VQwWo2Tg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1-7VQwWo2Tg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

