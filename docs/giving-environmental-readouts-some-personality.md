# 赋予环境读数一些个性

> 原文：<https://hackaday.com/2022/09/25/giving-environmental-readouts-some-personality/>

了解一个地区的空气质量指数可能是一件很方便的事情，但这是一个枯燥无味的数字，不是吗？好吧，这一切都随着[Andrew Kleindolph]的 [AQI 连环画](http://www.extrasleepy.com/#/aqi-funnies/)而改变了:一个友好的幽灵角色在漫画小组演示中展示了实时 AQI 数据的可视化表示。背景、情绪和信息都是根据当前条件生成的，提供了一些变化(和随机的形容词)来修饰事物。

[![](img/d66547434ffc74fb7ae1d12a62fc0d6e.png)](https://hackaday.com/wp-content/uploads/2022/09/AQI-Funnies-Inside.jpg) 我们喜欢对超净演示的关注，电子纸屏幕看起来棒极了。该单元内部有一个树莓 Pi，它使用 Python 与 AirNow.gov API(T4)对话，以获取当地情况，并每四个小时更新一次(对于感兴趣的人，AirNow 也有许多看起来有用的小部件(T6))。)

外壳是 3D 打印的，[Andrew]使用了一个 [Witty Pi](https://www.uugear.com/product/witty-pi-4-mini/) 进行电源管理和电池保护。显示器是彩色电子纸显示器，不仅看起来很棒，而且具有不需要电源的优势，除非显示器正在更新。当需要时，Pi 可以被唤醒以用新信息更新屏幕，否则它会花费时间休眠。

[Andrew]擅长友好地展示带有潜在严肃性的信息，正如我们看到的[他对令人讨厌的产品召回的友好提醒](https://hackaday.com/2019/08/19/a-friendly-reminder-that-you-might-be-in-danger/)。