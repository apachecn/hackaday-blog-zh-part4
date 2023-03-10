# 黑客将热裂解器变成 usb 键盘

> 原文：<https://hackaday.com/2020/06/24/hacker-turns-thermal-clacker-into-usb-keyboard/>

早在有笔记本电脑和随后的上网本之前，就有这些可爱的热敏打字机/文字处理器，它们的粉丝亲切地称之为婴儿楔形物或楔形物。这些迷人的小机器可以用两种不同的方式将文字写在纸上:你可以使用极其昂贵的小色带盒和普通复印纸，或者你可以走简单的路线，给自己买一卷 96 英尺的热感传真纸，然后打字直到你想撕掉那一页。

[【David】很幸运，几乎不花一分钱就买到了一台工作状态良好的佳能 S-70，认为它会成为一个很棒的 USB 键盘](http://cowlark.com/2019-11-03-keyboard/index.html)，我们同意这一点。现在控制它的 PSoC 5 可能有点过头了，但它非常实惠，而且它就在桌子上，只等着一个用途。额外的好处是——它有足够的 I/O 给[所有那些响亮可爱的按键开关](https://www.youtube.com/watch?v=Wj29_DuSvYU)。

[![](img/76c766cce65a87a398a307531e6b2706.png)](https://hackaday.com/wp-content/uploads/2020/06/typewriter-guts.jpg) 让这些小楔子留在打字机阵营中的一个原因是换档锁定功能，只有按下 Shift 键才能解除锁定，在他被迫移除它之前，它在板上有自己的分立逻辑电路。

那个小屏幕是纯粹的文字处理器，用来显示打字缓冲区——在打印头将它们提交到纸上之前，你有机会纠正的所有字符。在一次对文字处理软件的胜利中，屏幕被重新用于显示当前的字数。

他很友好地[发布了他的固件](https://github.com/davidgiven/maxii-keyboard/tree/master/typestar4-keyboard.cydsn)以及建造的实时镜头。休息后观看他在野外的演示，然后留下来观看建造传奇的第一部分。

十年前，便携式文字处理器仍在生产，尽管它们主要面向小学市场，作为键盘输入训练器。我们自己的[汤姆·纳尔迪]最近拆除了一个名为 Writer 的模型，它依靠 IR 发送文件。

 [https://www.youtube.com/embed/xyb-1SYlELY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xyb-1SYlELY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/B-mBX9irb4A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/B-mBX9irb4A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

