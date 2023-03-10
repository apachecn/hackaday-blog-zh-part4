# ESP8266 语音控制立体声平衡

> 原文：<https://hackaday.com/2018/09/19/voice-controlled-stereo-balance-with-esp8266/>

立体声系统假设听众位于扬声器之间，这样就可以从两侧均等地传递声音。这也是为什么接收器有一个“平衡”调节，所以听众可以通过改变扬声器的相对音量来虚拟地移动音频的中心点。你应该调整你的扬声器平衡，使你正常的坐姿居中，但是当然你不可能每次听音乐或看东西时都在那个位置。

[![](img/82c943eaf28c100b4c6dfba29db65302.png)](https://hackaday.com/wp-content/uploads/2018/09/espvol_detail.jpg) 【维杰·米勒】在[中写下了他对流动听众](https://hackaday.io/project/160842-center-surround-sound)问题的独特解决方案。他想出了一个系统，可以调节他的扬声器的音量，而不必接触接收器的设置，事实上，他不必接触任何东西。通过利用在他的计算机上运行的可配置语音控制软件，他的基于 ESP8266 的小设备完成了所有工作。

每个扬声器都有自己的设备，由 3D 打印外壳内的 NodeMCU ESP8266 和 X9C104 数字电位计组成。这个小工具上的音频端子板允许他将它连接在扬声器和接收器之间，使[Vije]能够通过软件调节音量。他发布在 Hackaday.io 项目页面上的源代码使用了一个非常简单的 REST 风格的 API，根据命中 ESP8266 IP 地址的 HTTP 请求来改变扬声器音量。

该项目的第二部分是一台运行 VoiceAttack 的计算机，它让[Vije]根据软件听到的内容分配不同的动作。当他说出适当的命令时，软件就会通过并向系统中的节点发出 HTTP 请求。目前一切都是为两个扬声器设置的，但通过对软件进行一些调整，扩展到更多扬声器(甚至房间)应该不会太难。

这不是我们见过的第一个声控扬声器，但它确实以独特的方式解决了一个非常具体的问题。我们很有兴趣看到下一个合乎逻辑的步骤，那就是[将这项技术集成到扬声器本身](https://hackaday.com/2017/09/14/remote-controlled-streaming-speakers/)。

 [https://www.youtube.com/embed/G7Hfdf2yHYs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/G7Hfdf2yHYs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

