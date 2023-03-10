# pinkphone 获得热成像背包

> 原文：<https://hackaday.com/2020/08/03/pinephone-gets-thermal-imaging-backpack/>

当你购买一部大众市场手机时，你就决定信任一长串拥有你私人数据的公司。虽然任何一个消费者都很难完全审计哪怕是一项消费技术，但已经有人努力在一定程度上解决这个问题。Pinephone 就是这样一个例子，它注重开放性，允许用户完全控制硬件。[Martijn Braam]是这种设备的骄傲拥有者，[并利用这种态度为手机添加了热像仪](https://blog.brixit.nl/making-a-backcover-extension-for-the-pinephone/)。

由于 Pinephone 硬件易于扩展的特性，构建并不困难。手机的后部有六个弹簧针，携带着 I2C 总线和电源。[Martin]从修改带有触点的手机后盖开始，以便与弹簧针接口。完成后，用双面胶将 [MLX90640](https://www.melexis.com/en/product/MLX90640/Far-Infrared-Thermal-Sensor-Array) 热像仪贴在箱子上，并连接到接口。

虽然该传感器的 32×24 输出不会帮助您构建尖端的热寻的导弹，但它是一种经济实惠的传感器，性能良好，适合低端热成像任务。我们以前也报道过热成像硬件的拆卸。