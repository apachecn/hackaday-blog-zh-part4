# 盲文键盘找到自己的声音

> 原文：<https://hackaday.com/2019/05/17/braille-keyboard-finds-its-voice/>

如果你有严重的视觉障碍，使用电脑并不容易。[Dhiraj]有一个项目允许精通盲文的人使用这种语言进行输入。除了设置手指的位置，该设备还可以读取您键入时按下的按键。根据[Dhiraj]的说法，使用一些第三方软件甚至可以创建 Word 文档。

你可以在下面的视频中看到成品。这是创意最难的项目之一。读取六个按钮并将它们转换成字符相当简单。每个盲文字符使用一个由六个凸起组成的单元，按钮模仿这些凸起(尽管是为你的手指设计的)。

我们的想法是，在第一个开关上有一些触觉反馈可能会很好，因为目标用户可能看不到开关。也许音频听起来有点粗糙，但那可能是扬声器。也许一个专用的空格键和一个不用移动手就能选择字母和数字的更简单的方法也不错。这些都不难解决。

代码非常简单，虽然我们可以看到你可能会得到一些错误的击键。Arduino 每隔 250 毫秒读取七个输入开关(第七个开关是字母/数字选择)。然后一个巨大的 if 语句将字母解码。就风格而言，我们可能会构建一个数字，并使用它从一个数组中进行选择，因为有 7 个开关，它将只占用 128 个字节。然而更重要的是，我们可能会等待至少一个开关转换来开始解码。开关为高电平有效，因此我们可能会这样写:

```
unsigned code,oldcode;
code=oldcode=0;
do {
   oldcode=code;
   code=read_button_code();  // get current code
   } while (oldcode<=code);
// process oldcode
```

如果这看起来令人困惑，试几个例子(你也可以在网上[做这个](https://onlinegdb.com/r1g2x-i2V))。首先，旧代码是零，所以代码永远不会小于零(注意整数是无符号的)。只要位不断被设置，code 就会大于或等于 oldcode。然而，如果任何一位从 1 变到 0，那么代码的总幅度一定小于 oldcode。这触发了处理过程。当然，您可能还想对 read_button_code 中的开关进行去抖，以确保您也有一个稳定的输入。

尽管如此，这是一个多么伟大和有用的想法，而且在原始设计的基础上建立起来也很容易。我们以前见过一个盲文平板电脑。如果你在下一块 PCB 上有多余的空间，你总是可以替换一些[社区标志](https://hackaday.com/2017/10/31/making-braille-signs-out-of-pcbs/)。

 [https://www.youtube.com/embed/wdiBibZHQBw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wdiBibZHQBw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

