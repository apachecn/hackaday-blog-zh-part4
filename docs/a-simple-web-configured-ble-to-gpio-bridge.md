# 一个简单的 Web 配置的 BLE 到 GPIO 桥

> 原文：<https://hackaday.com/2022/09/06/a-simple-web-configured-ble-to-gpio-bridge/>

[Daniel Dakhno]一直处于这样一种情况，即以最小的努力读取或控制一些数字 IO 引脚的状态的能力将非常有用。为了满足这种简单的需求，他们不想继续编译代码，而是使用基于 nRF51 的模块作为物理接口，并开发了一种通用固件，可以通过简单的 web 界面进行配置。NRF51-IO 模块诞生了，它的工作是与你面前的任何设备配对，只要它支持 BLE，并直接访问那些 IO 引脚。

固件不是作为一个相当慢的逻辑分析器，而是主要用于静态配置。 [web 应用](https://ble.nullco.de/)向 nRF51 板发送一个配置包，然后将其编程到闪存中并重启，读取更新的配置并将其应用到 IO 引脚。只要有电，这些输出就会持续。等式的阅读端也可以通过网页执行，但我们没有机会验证这一点。代码实现了[蓝牙自动化 IO 服务](https://www.bluetooth.com/specifications/specs/automation-io-service-1-0/)以及[二进制传感器服务](https://www.bluetooth.com/specifications/specs/binary-sensor-service-1-0/)，所以如果你有访问这些服务的应用程序，那么你应该能够启动它并使用它，尽管由于缺乏 nRF51 板，我们没有亲自测试过。我们注意到[家庭助理自动化平台支持 BT 二进制传感器](https://www.home-assistant.io/integrations/binary_sensor/)，这可能对一些需要无线控制和传感的人有很大帮助。

如果你需要一个遥感应用的实际例子，这里有一个使用 nRF51 的[物理邮箱状态监控器](https://hackaday.com/2022/05/30/check-your-mailbox-using-the-airtag-infrastructure/)。当我们想到蓝牙和传感器时，这里有一个为一些超级便宜的环境传感器定制的[固件，让它们摆脱供应商的束缚。](https://hackaday.com/2020/11/17/custom-firmware-for-cheap-bluetooth-thermometers/)

标题图像:Ubahnverleih， [CC0](https://commons.wikimedia.org/wiki/File:NRF51822_Bluetooth_4.0_Modul.jpg) 。