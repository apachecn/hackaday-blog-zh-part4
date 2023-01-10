# 以威胁的方式遏制网瘾

> 原文：<https://hackaday.com/2019/07/15/curbing-internet-addiction-in-a-threatening-manner/>

那些有自己孩子的人可能会说，现在的年轻人上网时间太多了。[尼克]决定紧急叫停它，并制作了[这个巧妙的互联网死亡开关，用](https://www.youtube.com/watch?v=3Unz3OAnC6E)来威胁青少年。这个红色的大按钮外表看起来很不起眼，但只要你一按下它，它就会立刻切断所有的网络流量，这是它的标签。重置切换按钮，连接就恢复了，就这么简单。

为了实现这一点，[Nick]在外壳内安装了一个 Raspberry Pi Zero W，以及一个电池和一个无线充电电路，以实现便携性和完全无线操作。该按钮连接到 Pi 的 GPIO，并通过 SSH over WiFi 向路由器发出命令，其中一个侦听信号的脚本告诉它放弃与外界通信的网络接口。这很简单，很干净，你可以随身携带，作为对那些胆敢违抗你的人的警告。我们喜欢它。

我们过去见过的红色大按钮的另一个用途是交流电源定时器，但是如果你把它变成 USB 设备，你可以用它做任何事情。休息之后看看这个。

 [https://www.youtube.com/embed/3Unz3OAnC6E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3Unz3OAnC6E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢[朱利安]的提示！