# N64 上的鼠标和键盘控制

> 原文：<https://hackaday.com/2021/10/01/mouse-and-keyboard-controls-on-the-n64/>

任天堂 64 游戏机是 3D 游戏时代的先驱之一。然而，它的控制器的设计我们今天不会认为是理想的。对于在 N64 上如此受欢迎的 FPS 游戏，鼠标和键盘可以做得更好。【伪君子】着手让它发生。

N64 轮询控制器并接收返回的按钮和模拟杆数据。控制器发送四个字节，其中 14 位包含按钮，8 位分别包含模拟杆的水平轴和垂直轴。因此，如果来自 PC 的键盘按压和鼠标移动可以被泵送到微控制器，该微控制器将数据重新格式化成 N64 可以理解的信号，那么一切都会很好地工作。

最初尝试使用从[詹姆斯·瑞德] 借来的[代码工作时，遇到了按键和动作到达 N64 之间有 3 秒钟滞后的问题。升级到更快的微控制器只会让事情变得更糟，滞后时间达到了整整 16 秒。问题？该项目借用的代码将按键存储在缓冲区中，这造成了延迟。一旦被消灭，这个系统就起作用了。](https://medium.com/james-reads-developer-projects/n64-microcontroller-controller-12c76acde194)

该软件的安装程序是可用的，但如果你想使用它，你必须对运行一个奇怪的可执行文件[感到舒服。](https://www.dropbox.com/s/i1qnxla98qz4oh8/PC64v1.1Setup.exe?dl=0)我们以前也见过类似的工作，[，比如 USB64 项目](https://hackaday.com/2020/09/29/new-controllers-on-old-nintendos-with-usb64/)。休息后的视频。

 [https://www.youtube.com/embed/qIYolx_Cl24?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qIYolx_Cl24?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 Keith Fulkerson 的提示！]