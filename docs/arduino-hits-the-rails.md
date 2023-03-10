# Arduino 撞上了铁轨

> 原文：<https://hackaday.com/2018/11/30/arduino-hits-the-rails/>

某些爱好是成群结队的。例如，业余无线电操作员是私人飞行员的情况并不少见。身为音乐家的程序员。制造模型火车的电子人。这最后一个似乎非常适合，因为你可以用简单的电子设备和小型火车做很多有趣的事情。[Jimmy]在名副其实的 DIY 和数字铁路频道，有几个关于用 Arduino 集成铁路设置的视频。这些范围从建造一个 DCC 系统[大约 45 美元](https://www.youtube.com/watch?v=5Z9Kwjp8RuQ)(见下文)到一个[交叉信号](https://www.youtube.com/watch?v=-kqAZqe-W4A)。

频道上其实有不少基础的 Arduino 视频，虽然大部分是针对新手的。然而，如果你是一个火车新手，DCC——数字命令和控制——可能对你来说是新的。DCC 是由国家模拟铁路协会定义的标准。

模型火车从铁轨上获取电能。DCC 也允许数字信息在铁路上传输。信号从正变到负，以指示标记和空白。通过二极管转换电信号，火车或其他设备可以获得恒定的电流供应。然而，监控二极管前线路的设备可以读取数据并将其解释为命令。

为了适应旧设备，您可以拉伸高值或低值，使平均电压为正(正向)或负(反向)。这可能会加热 DC 汽车公司，因此可能会缩短遗留设备的寿命。

这个构建使用了一个可用的 Arduino 库，所以如果你想进入这个协议，你必须完成这个代码。我们不得不考虑是否还有其他地方，在同样的线路上传输电力和数据可能有用。当然，还有其他方法可以做到这一点，但是如果您需要这种能力，这将是一个合理的起点。

如果你想使用 mBed 系统而不是 Arduino，这里有一个很棒的教程。无论哪种方式，它都是你的[下一个咖啡桌](https://hackaday.com/2017/12/22/coffee-table-model-railroad-with-all-the-bells-and-whistles-and-lights-and-sirens/)的不二之选。

 [https://www.youtube.com/embed/5Z9Kwjp8RuQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5Z9Kwjp8RuQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

