# Arduino 扮演眼镜

> 原文：<https://hackaday.com/2021/11/22/arduino-plays-the-glasses/>

你有没有在城市街道上看到一个街头艺人戴着眼镜演奏音乐？每个杯子都有不同的水量，敲击时会发出不同的声音。[Cyberlab]一定是看到了他们，创造了一个 [Arduino 机器人，在眼镜上演奏曲子](https://www.instructables.com/Arduino-Robot-Plays-Music-on-Wine-Glasses/)。你可以在下面的视频中看到结果。

如果我们做到了这一点，我们可能会为每个玻璃配备一个螺线管，或者使用一些线性组件，如 3D 打印机轴来选择不同的玻璃。[网络实验室]做了一些更聪明的事情。眼镜会转一圈，步进电机会指向正确的眼镜并激活螺线管。结果非常好，而且比我们的任何想法都简单。

如果你对音乐不感兴趣，你可能想知道如何编写歌曲。有一个例子，从一个网站上获取一个音乐盒乐谱(显然有很多这样的乐谱),并从中删除任何复调音乐。提到的网站甚至有一个编辑器，你可以导入 MIDI 文件，用它们制作一个音乐盒带，然后你可以转换。然后你把每个音符编码成一个从 0 到 6 的数字。

当然，你也要在杯子里装满适量的水。一个钢琴调音手机 app 应该有用。我们以前已经见过以线性方式这样做[。你甚至可以用](https://hackaday.com/2018/07/31/the-precise-science-of-whacking-a-wine-glass/)[一个玻璃杯来放很多音符](https://hackaday.com/2011/10/21/hydrocrystallophone-probably-wont-make-you-insane/)，只要稍加巧妙。

 [https://www.youtube.com/embed/rLxqwWiLklM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rLxqwWiLklM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

