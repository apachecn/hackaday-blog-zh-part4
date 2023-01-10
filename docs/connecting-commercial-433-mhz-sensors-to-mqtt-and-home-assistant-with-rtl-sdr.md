# 利用 RTL-SDR 将商用 433 MHz 传感器连接到 MQTT 和家庭助理

> 原文：<https://hackaday.com/2022/12/26/connecting-commercial-433-mhz-sensors-to-mqtt-and-home-assistant-with-rtl-sdr/>

当[Elixir of Progress]考虑在他们的房子周围设置环境传感器来跟踪温度、湿度等信息时，使用 WiFi 连接传感器的明显想法由于缺乏 WiFi 覆盖范围而行不通。虽然 Zigbee (Z-wave)传感器的覆盖范围比 WiFi 更大，但它们显然更昂贵、更专有，并且需要特殊的收发器集线器。这就是气象站的 433 MHz 传感器[出现的原因](https://cohost.org/Elixir-Of-Progress/post/463783-probing-weather-in-h)。

这个想法很简单:几乎所有这些传感器——其中许多是户外使用的——都使用未经许可的 433 MHz 频谱，使用廉价的 RTL-SDR(软件定义无线电)USB 加密狗可以轻松捕获这些频谱。随着来自这些传感器的数据流被捕获，开源的 [rtl_433](https://github.com/merbanan/rtl_433) 项目能够为广泛支持的传感器自动解码这些数据流。

虽然基于 Realtek RTL2832 和其他 RTL SDR 的价格非常便宜，但应该注意的是，这些 SDR 可能会非常热。在这个项目中，没有对 IC 进行散热处理，而是选择偶尔监听，让 RTL-SDR 接收器在监听期间冷却下来。

从那里获取数据到家庭助理，InfluxDB 或类似的是很容易的，因为 rtl_433 可以直接输出解码数据到一个流入数据库，MQTT 经纪人以及其他格式。在这种情况下，数据是通过 MQTT 发送的，Home Assistant 实例被配置为将这些 MQTT 主题视为传感器。通过仔细记录每个传感器的位置，可以建立一个由 433 MHz 传感器组成的密集、极低功耗网络，用于监控和家庭自动化。