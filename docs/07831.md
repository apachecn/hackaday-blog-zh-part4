# 直接来自 ECU 的摩托车仪表板

> 原文：<https://hackaday.com/2020/09/21/a-motorcycle-dashboard-straight-from-the-ecu/>

经典摩托车是信息展示的狂野西部。摩托车通常缺少最基本的仪表，如燃油表，有时甚至没有速度计，从 20 年前开始，摩托车在仪表组设计方面已经取得了很大的进步。然而，仍然有一些改进的空间，幸运的是，许多现代自行车都有一个 ECU 模块，可以用来获取一些额外的信息，正如[mickwheelz]用他的辅助摩托车仪表板展示的[。](https://github.com/mickwheelz/Honda-Motorcycle-Dash)

该显示器是为现代本田 enduro 制造的，基于 ESP32 模块。ESP32 通过诊断插座直接连接到 ECU，不像其他类似的产品专门与 CAN 总线接口。它可以监控自行车的所有活动，包括发动机温度、油门位置、进气温度以及自行车是否处于空档。[mickwheelz]还增加了一个外部 GPS 传感器，因此新的显示器也可以向他显示同一单元内的 GPS 速度和位置信息。

[mickwheelz]赞扬了其他几个在本田 ECU 方面取得进展的人。[Gonzo]使用 Raspberry Pi 和更基本的屏幕创建了一个类似的构建，但在收集这个构建的信息方面发挥了重要作用。不过，如果你正在为你那辆缺少 ECU 的古董摩托车寻找任何类型的展示，我们建议你用谢妮管制成的[速度计](https://hackaday.com/2015/07/16/nixie-tube-speedometer-in-motorcycle-handlebars/)。