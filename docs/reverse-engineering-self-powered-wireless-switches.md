# 逆向工程自供电无线交换机

> 原文：<https://hackaday.com/2021/05/02/reverse-engineering-self-powered-wireless-switches/>

过多的无线通信技术切断了许多应用的通信线路，但这些设备仍然需要电源。对于家庭自动化来说，这可能意味着电池或主电源，但还有一种我们不常看到的替代品:动能。[Bigclivecom]从易贝购买了一些[动力开关](https://youtu.be/9Pw7U0XFgUM)，并对其进行了通常的逆向工程处理。

对于市场营销来说，这些开关不需要外部电源或电池来发送无线信号。相反，它从开关本身的磁锁定动作中获取能量。当开关启动时，由于穿过线圈铁芯的磁场极性快速变化，线圈中会感应出小电流。通过一系列二极管和电阻，能量被储存在一个电容器中，然后被用来为一个小型发射器芯片供电。天线线圈缠绕在开关外壳上。

接收器侧由市电供电，包括一个灯光继电器输出。这将是非常好的有一个黑客友好的项目模块。我们很想知道这些设备的功能范围。

飞利浦 Hue Tap 开关内部也使用了同样的技术，几年前 Adafruit 曾拆除过这种开关。如果你想了解更多关于射频调制的知识，请查看我们不久前发布的[速成文章](https://hackaday.com/2020/01/28/rf-modulation-crash-course-for-hackers/)。当然，如果你想做一些实验， [RTL SDR](https://hackaday.com/2019/07/31/rtl-sdr-seven-years-later/) 是一个不可或缺的廉价工具。

 [https://www.youtube.com/embed/9Pw7U0XFgUM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9Pw7U0XFgUM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

