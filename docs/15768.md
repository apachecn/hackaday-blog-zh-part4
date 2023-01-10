# ESPHome 电源节日乐高火车套装

> 原文：<https://hackaday.com/2022/12/27/esphome-powers-festive-lego-train-set/>

虽然自 20 世纪中期以来，乐高积木的基本概念可能没有什么变化，但一些组件，如电机和传感器，仍然受到技术进步的影响，最终被淘汰和不受支持。[Travis]在构建节日列车设置时遇到了这个问题，他意识到他没有与火车引擎匹配的速度控制器。没有那部分，引擎只会全速运转，一碰到弯道就出轨。官方的速度控制器已经停产，很难找到，所以[特拉维斯] [不得不求助于建立自己的](https://xodustech.com/projects/esphome-lego-power-functions)。

所需的基本元件是操作电机的 H 桥驱动器和产生 PWM 信号的 ESP8266。为了保持火车引擎的砖状外观完好无损，[特拉维斯]挖空了几块廉价的仿制乐高积木来放置电子设备。他还为 JST 连接器切出插槽，这比乐高积木式连接器方便得多。

[![Two imitation LEGO bricks with electronics inside](img/37a9ceb886de2607d8f475b19a42e877.png)](https://hackaday.com/wp-content/uploads/2022/12/ESPHome-Lego-Train-brick.jpg)ESP8266 运行 ESPHome，使【Travis】能够使用 Home Assistant 控制整个设置。火车被编程为在整点跑几圈，并从藏在煤车上的迷你 MP3 播放器中播放啾啾的声音。那辆车还装有一个标准的 AA 电池盒来为系统供电，这使得更换电池变得很容易，而不必部分拆卸火车。

使用标准的计算机平台有各种方法来控制乐高创造:例如，我们已经看到了为乐高坦克提供动力的 [ESP32。如果你需要更多的计算能力，甚至有一个官方的乐高树莓派帽子](https://hackaday.com/2018/11/01/mini-lego-technic-tank-patrols-your-desk-under-esp32-control/)[。](https://hackaday.com/2021/10/21/new-part-day-raspberry-pi-lego-hat/)

 [https://www.youtube.com/embed/aIK162QnX4M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aIK162QnX4M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

