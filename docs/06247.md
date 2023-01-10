# 一个整洁的小 OBD 展示给你的车

> 原文：<https://hackaday.com/2020/04/13/a-tidy-little-obd-display-for-your-car/>

许多读者可能会有一个 OBD 加密狗，通过它他们可以窥视他们汽车的内部工作，但我们大多数人可能会将我们的好奇心限制在它提供的蓝牙或 USB 接口上。不过，这并不奇怪，因为[已经改装了他的 OBD 加密狗](https://hackaday.io/project/170820-obd-dash-display)，以暴露其 ELM327 OBD 芯片和蓝牙芯片之间的串行线路。这些信号传到 Arduino，Arduino 为一个小型信息显示器供电，作为汽车仪表盘的补充。这可以显示一系列的读数，就像在休息时的视频中看到的那样，他用它来监控电池，发动机舱内的各种温度和点火参数。

所有的软件和硬件细节[都可以在 GitHub 库](https://github.com/freddy-/obd-dash)中找到。从硬件角度来看，这是一个令人惊讶的简单单元，但它提醒我们，OBD 嗅探加密狗比我们最初想象的更通用，比通过蓝牙连接我们的智能手机好一点。如果你想更深入地了解 OBD，过去我们曾推出过[的开源 OBD 接口](https://hackaday.com/2016/03/27/open-source-obd-ii-adapter/)，以及[的协议回顾](https://hackaday.com/2017/01/04/on-board-diagnostics/)。

 [https://www.youtube.com/embed/8ltNNvUFt8k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8ltNNvUFt8k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

