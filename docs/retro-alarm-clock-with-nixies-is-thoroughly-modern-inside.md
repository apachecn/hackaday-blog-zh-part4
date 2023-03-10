# 带有 Nixies 的复古闹钟内部非常现代

> 原文：<https://hackaday.com/2022/12/10/retro-alarm-clock-with-nixies-is-thoroughly-modern-inside/>

我们在 Hackaday 展示了很多时钟，但是出于某种原因，闹钟似乎不太受欢迎。也许这是因为没有人喜欢早上被叫醒，或者仅仅是因为每个人都已经在用智能手机做这件事了。无论如何，我们很高兴为您带来[Manuel Tosone]的[漂亮的数码管闹钟](https://hackaday.io/project/188572-nixie-alarm-clock)，它巧妙地将现代和经典技术结合在一个包装中。

[![An alarm clock with a Nixie tube display, opened](img/7a5de0db24551bb5ebbfca9ac80d69ee.png)](https://hackaday.com/wp-content/uploads/2022/12/Nixie-alarm-clock-inside.jpg) 时钟和闹铃功能由定制主板上的 PIC24 微控制器实现。它通过带有备用电池的实时时钟来跟踪时间，并在醒来时播放 SD 卡上的歌曲。一个 2x 3w D 类音频放大器加上一对立体声扬声器应该能够唤醒即使是最沉的睡眠者。

当然，真正的派对用品是时钟的显示屏:四个四合一的谢妮管显示时间，氖管显示星期几。Nixies 所需的 180 V 电压由基于 MC34063A 的升压转换器产生，该转换器也为氖管供电。

[Manuel]没有为每个数码管使用标准的限流电阻，而是设计了一系列基于晶体管的电流源:这使得可以对灯管的亮度进行线性控制，即使灯管老化，也应该保持光量恒定。各个段由 SN75468 达林顿阵列切换，不需要那些难以找到的 SN74141 驱动器。

主板和显示器装在一个 3D 打印的外壳中，模仿了 20 世纪 80 年代的数字闹钟风格，但由于这些谢妮电子管的存在，又有了 20 世纪 70 年代的美好转折。[【Manuel】的 GitHub 页面](https://github.com/ts-manuel/Nixie-Alarm-Clock)有所有的原理图以及描述电路操作的大量文档——如果你打算自己建立一个谢妮项目，这是一个极好的资源。如果你不喜欢数码管，你也可以用 VFD 管做一个闹钟[，或者甚至](https://hackaday.com/2019/06/14/stylish-alarm-clock-rocks-a-vfd/)[滚动你自己的发光模拟表盘](https://hackaday.com/2016/10/15/not-just-another-alarm-clock/)。

 [https://www.youtube.com/embed/ghkEFtqIfFI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ghkEFtqIfFI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

