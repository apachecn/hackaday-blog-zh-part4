# 使用 ESP32 让 Minitel 终端重现生机

> 原文：<https://hackaday.com/2021/11/25/bring-a-minitel-terminal-back-to-life-with-an-esp32/>

我们大多数年龄足够大的人可能在 20 世纪 90 年代的某个时候第一次体验过在线服务，要么是通过 Compuserve 之类的网站，要么是通过 ISP。对于我们的法国读者来说，在线体验将来得更早，因为前瞻性的电信环境导致该国每家每户都有一个 viewdata 终端。这个名为 Minitel 的系统获得了巨大成功，直到 2012 年才最终被关闭。许多终端幸存下来，为项目奠定了良好的基础，这就是[Louis H] [采用并通过 ESP32](https://hackaday.io/project/180473-minitel-esp32) 增强的终端之一。

这个项目的一个特别之处是，与许多其他 Minitel 转换不同的是，它不涉及撕裂终端本身。相反，PCB 插入到单元背面的插座中，并模拟终端与之通话的线路。然后，它可以用作 WiFi 上的 SSH 终端，或者用作 ESP32 本身的串行终端，例如运行 MicroPython 固件。如果你能操作法国 AZERTY 键盘，没有更简单的方法将 viewdata 终端拖到 21 世纪 20 年代，正如你在休息时的视频中看到的那样。

Chez Hackaday，我们喜欢这些 20 世纪 80 年代的怀旧珠宝。事实上，我们非常喜欢这个经典的法国公共网络，以至于我们对它进行了多次特别介绍。这里有一个使用 Arduino 的类似项目[。](https://hackaday.com/2019/02/27/arduino-revives-a-classic-1980s-minitel-terminal/)

 [https://www.youtube.com/embed/iOB85X8F1vI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iOB85X8F1vI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

