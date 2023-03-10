# 使用人工智能从 SDR 处理的信号中提取呼号

> 原文：<https://hackaday.com/2018/10/09/using-ai-to-pull-call-signs-from-sdr-processed-signals/>

人工智能目前很受欢迎，所以[Chirs Lam]认为他可以通过使用它从使用 SDR 处理的无线电信号中提取呼号来激发人们对业余无线电的兴趣。正如你将看到的，人工智能做得很好，所以[克里斯]用一种为基因测序发明的算法增强了它。

他的实验很简单。他拿起一个“宝丰”手持无线电收发机，发送包含呼号和一些语音的信息。然后，他用一根 0.5 米长的天线接收，用一点连接硬件和一个 NooElec [SDR dongle](https://hackaday.com/2017/09/05/19-rtl-sdr-dongles-reviewed/) 把它接入他的笔记本电脑。在那里，他使用 SDRSharp 处理信息并输出一个 WAV 文件。然后他把它传给人工智能，谷歌的云语音转文本服务，把它转换成文本。

尽管一次说一个单词，并努力发音清晰，但结果并不理想。在他的例子中，只有呼号和实际信息的前两个词是正确的。或许，如果人工智能在有背景噪声的实际停播对话中接受训练，它会做得更好。这不是完全相同的问题，但我们想起了那些麻省理工学院的研究人员，他们愚弄了谷歌的盗梦空间图像识别器[认为一只乌龟是一把枪](https://hackaday.com/2017/11/03/googles-inception-thinks-this-turtle-is-a-gun/)。

与其训练自己的人工智能，克里斯聪明的解决方案是求助于史密斯-沃特曼算法。这与分析基因时用于寻找相似核酸序列的算法相同。它允许他使用一系列正确的呼号来找到人工智能提出的最佳匹配。正如你在下面的视频中看到的，它得到了正确的呼号。

 [https://www.youtube.com/embed/zkaWAGAkNRY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zkaWAGAkNRY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

