# 给太阳能 PIR 灯添加 MQTT

> 原文：<https://hackaday.com/2021/05/06/adding-mqtt-to-a-solar-powered-pir-light/>

ESP wifi 模块的尺寸和价格使其迅速成为物联网设备的首选构建模块之一。不幸的是，它们不是特别适合非常低功率的应用。[LittlePetieWheat]想要在一个便宜的 PIR 太阳能灯上添加 MQTT，所以他将一个 ESP 与 Attiny85 配对，以保持严格的功率预算。

这些灯大多包含某种无名微控制器，用于监控模拟 PIR 传感器，并根据需要打开 led。[LittlePetieWheat]将 PIR 传感器替换为提供数字输出的传感器，以简化接口。Attiny 充当项目的低功耗大脑。它的任务包括读取太阳能电池板和电池电压，以及 PIR 输出。当传感器检测到移动时，它会激活一个聪明的小[锁存电源电路](https://hackaday.com/2020/05/18/esp32-trail-camera-goes-the-distance-on-aa-batteries/)来给 ESP01 供电，时间长度足以发送 MQTT 消息。只有当太阳能电池板不供电时，led 才会亮起。太阳能储存在 18650 电池中。

Attiny85 可能不是一个强大的处理器，但它非常适合像这样简单的低功耗应用。我们还看到它通过运行[微型机器学习模型](https://hackaday.com/2020/01/07/tiny-machine-learning-on-the-attiny85/)，或者[通过 I2C](https://hackaday.com/2018/10/20/i2c-bootloader-for-attiny85-lets-other-micros-push-firmware-updates/) 接收软件更新，将其推向极限。

 [https://www.youtube.com/embed/q5F9G3MiBK4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/q5F9G3MiBK4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

