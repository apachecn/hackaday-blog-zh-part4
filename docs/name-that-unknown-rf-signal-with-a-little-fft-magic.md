# 用一点 FFT 魔法命名未知的 RF 信号

> 原文：<https://hackaday.com/2020/02/11/name-that-unknown-rf-signal-with-a-little-fft-magic/>

业余无线电乐队曾经是一个听起来可以预测的地方。上下转动表盘，人们听到熟悉的声音——摩尔斯的断奏、边带语音传输的[唐老鸭],以及偶尔传来的无线电报信号的长笛般的颤声。现在，ham 频段充满了编码各种数字信号的奇异信号，每种信号都有独特的声音和独特的解调需求。火腿能做什么？

救援马上就到。[何塞·卡洛斯·鲁埃达]通过修改一个类似 Shazam 的应用程序，在自动分类未知信号方面取得了进展。Shazam 是一款流行的智能手机应用程序，它可以听几秒钟的歌曲，创建一个音频指纹，并在庞大的歌曲数据库中搜索匹配的歌曲。[鲁埃达]使用自制版本的应用程序来搜索音频指纹的 SQL-lite 数据库，其中没有流行音乐的播放列表，而是来自[信号识别维基](https://www.sigidwiki.com/wiki/Database)中每种已知信号类型的样本。该数据库包含每个样本的 FFT 的哈希值，可以很容易地进行搜索。通过一个 5 到 10 秒的信号样本，无论是通过麦克风还是从录音中捕捉到的，他都能够自动识别信号。

无论是 PSK-31 的怪异、不和谐的哀号，还是帕科特的愤怒的嗡嗡声，乐队之间的事情不再是一个谜。我们真的很喜欢这里的想法，并想知道它是否可以扩展到使用 TensorFlow 基于瀑布签名对信号进行可视化解码。在[【Danie Conradie】关于 RF 调制的优秀文章](https://hackaday.com/2020/01/28/rf-modulation-crash-course-for-hackers/)中有一些瀑布式的例子，可以帮助你入门。

[via[RTL-SDR.com](https://www.rtl-sdr.com/shazam-style-automatic-signal-identification-via-the-sigidwiki-database/)