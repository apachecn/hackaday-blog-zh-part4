# 太阳能物联网传感器避免葡萄酒批次过热

> 原文：<https://hackaday.com/2018/11/25/solar-powered-iot-sensor-saves-wine-batch-from-overheating/>

酿酒不仅仅是按照食谱来做，这是一个需要监控和管理的化学过程，以获得最佳效果。批量越大，出问题越痛苦。这意味着小型葡萄园的风险很高，比如 one [Mare]合作的家庭，他们没有足够的资源购买高端设备，但与大型酿酒商有着相同的需求。监控最有用的东西是发酵过程的温度曲线，并且[Mare]使用 LoRa 无线和太阳能创建了一个出色的物联网系统来做这件事。

仅仅测量发酵液的温度是不够的；观察温度如何随时间变化对于理解过程和发现任何问题至关重要。[Mare]最初使用树莓 Pi、I2C 温度传感器和连接到数据库的 Wi-Fi 来进行监控。这是成功的，但也是矫枉过正。为了改进系统，Raspberry Pi 被一个 [LoRaDunchy 板](https://github.com/s54mtb/LoRaDunchy)取代，这是一个基于 STM 的模块，由[【马雷】自己设计](http://e.pavlin.si/2018/06/20/loradunchy-arduino-nano-pin-compatibile-lora-module-with-power-management/)，与 Arduino Nano 引脚兼容。它包括电池充电器、电源管理和 LoRa 无线通信。添加太阳能电池和锂聚合物电池只是象征性地切断了电源线。

检测发酵的温度是通过将温度传感器密封在一个薄铝管中，并将其放入桶中来完成的。它仍然存在，LoRaDunchy 板定期醒来读取传感器并在返回睡眠前通过 LoRa 报告温度，同时从电池中吸取能量，电池又通过太阳能充电。

这是一个优雅的系统，已经得到了回报。当温度持续 10 分钟超过 24 摄氏度时，一个 500 升的大桶葡萄酒就会发出警报。一封电子邮件提醒允许所有者开始混合溶液并添加冰水，以阻止失控的反应。温度下降，缓慢的发酵重新开始，这要感谢收集正确数据的双重力量，然后用它做一些有意义的事情。

葡萄园和 LoRa 之前已经合作过，例如旨在实现节水农业的 Vinduino 项目。如果你对 LoRa 不熟悉，在 ESP32 项目页面上的 [LoRa 包含了一个很好的入门，如果这里显示的模块上的天线对你来说很熟悉，那是因为我们最近推出了](https://hackaday.com/2018/06/24/lora-with-the-esp32/)[【马雷】关于用回收的电线](https://hackaday.com/2018/11/19/diy-mini-helical-antennas-from-salvaged-co-ax-cable/)制作 DIY LoRa 天线的指南。