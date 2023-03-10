# 用于栅眼热传感器的新型分线板

> 原文：<https://hackaday.com/2020/05/18/new-breakout-board-for-grid-eye-thermal-sensor/>

松下的栅眼传感器本质上是一种低成本的 8×8 热成像仪，具有 60 度的视野，一个漂亮的分线板使其更容易集成到项目中。[Pure Engineering]已经为网格眼开发了一款[升级版的便捷分线板，目前正在接受订单。新的分线板不到一英寸见方，被称为*网格 2* (不要与主要组件的名称混淆，松下的](https://groupgets.com/campaigns/765-puremodules-grideye2) [AMG8833 网格眼](https://na.industrial.panasonic.com/products/sensors/sensors-automotive-industrial-applications/grid-eye-infrared-array-sensor)。)

[![](img/db8b248efe6b2b445f0b377a6586f595.png)](https://hackaday.com/wp-content/uploads/2020/05/GridEye2-with-CH341A.jpg)

GridEye2 connected to CH341A dev board, allowing easy PC interface over USB.

与 Grid-EYE 接口的一种常见方式是通过 I2C，但为了使在 PC 上的连接和开发更加简单，[Pure Engineering]已经确保新单元可以直接插入他们的(可选)CH341A 开发板，以提供 USB 接口。在 Linux 机器上安装和运行就像为 CH341A 安装 [Linux 驱动程序一样简单，使用](https://github.com/gschorcht/i2c-ch341-usb)[示例 C 代码](https://github.com/PureEngineering/GridEYE-Breakout/blob/master/firmware/linux_demo/main.c)开始从连接的 GridEye2 板上读取热量数据。

Grid-EYE 是一个低成本、功能强大的小设备，[与 LED 矩阵显示器](https://hackaday.com/2017/06/05/diy-grid-eye-ir-camera/)配合良好，在更先进的方面，一个简单的[高斯插值在应用于低分辨率传感器](https://hackaday.com/2019/09/29/diy-thermal-imager-uses-diy-gaussian-blur/)时会产生惊人的效果，使它们看起来比实际分辨率更高。