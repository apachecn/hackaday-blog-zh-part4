# Python 脚本向每个扬声器发送自己的声音文件

> 原文：<https://hackaday.com/2019/02/14/python-script-sends-each-speaker-its-own-sound-file/>

对于音频，您想要的扬声器数量通常取决于信号的音轨或声道数量。一个用于单声道，两个用于立体声，四个用于四声道，五个或更多用于环绕声等等。但所有这些扬声器本质上都在播放“单一”音频信号的不同音轨。如果您想要一个音频设备同时播放八首不同的歌曲，并且每首歌曲都通过管道传输到它自己的扬声器，该怎么办？这是跨学科艺术家 Sara Dittrich 给[Devon Bray]的工作，是她的“会说话的大耳朵”装置项目之一。他使用现成的硬件和软件构建了一个设备来在多个输出设备上播放多个声音文件。

但是，也许像这样的黑客可以在许多应用中有用，而不仅仅是艺术装置。它可以用在密室中，您可能希望各种音频流同时同步开始，或者作为 DJ 控制台的一部分，将一个音频流发送到扬声器，另一个发送到耳机，或者在游戏中，您必须以正确的顺序和速度在满是扬声器的房间中奔跑，以听完整的句子来寻找线索。

他的博客文章列出了所需的各种硬件的链接，尽管所有这些都很普通，并且代码由 [github 库](https://github.com/esologic/pear)托管。该项目的核心是 python 的 [Sounddevice](https://python-sounddevice.readthedocs.io/en/0.3.12/) 库。该库的文档很少，所以[Bray]的说明很方便。他的代码让你“用。wav 文件以数字顺序命名，并通过连接到主机的 USB 声音设备一遍又一遍地播放它们，一旦最长的文件播放完，就循环播放所有文件。作为奖励，他展示了如何从连接的 USB 驱动器自动加载和播放声音文件。这让你可以在 Raspberry Pi 上交换播放列表，而无需使用键盘/鼠标、SSH 或 RDP。

休息后，请查看视频，了解该项目的快速摘要。

 [https://www.youtube.com/embed/k1c2qlfvjBQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/k1c2qlfvjBQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

