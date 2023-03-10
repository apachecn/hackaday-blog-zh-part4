# 对吸烟者进行逆向工程

> 原文：<https://hackaday.com/2022/08/19/reverse-engineering-a-smoker/>

在世界的某些地方，以特定地区的方式烹饪肉类是当地文化的重要组成部分。从美国南部的烧烤，到南非的 boerewors 和 braaivleis，再到法属加拿大的蒙特利尔熏肉，几乎每个地方都有自己的特色烧烤。以至于制作这些食物的工具的制造商包括各种各样的小工具来监控有时长达几天的烹饪各种肉块的过程。[【mega Marco 833】的吸烟者](https://github.com/megamarco833/pitboss-smoker-esp32/blob/main/README.md)，不过，包括一些他自己设计的工具。

该吸烟器由一家名为 Pitboss 的公司制造，包括一个旋转开关和控制板，用于保持吸烟器内的精确温度。该开关通过改变发送到小型微控制器的电压值来工作。通过将 ESP32 连接到该开关，[megamarco833]可以远程改变吸烟者的烟雾水平和温度。在软件方面，它使用 Node-RED 和 Domoticz 的组合来处理自动化和控制。

对于可以持续几个小时(如果不是几天)的户外烹饪来说，如果你想做些什么而不是手动监控肉类温度那么长时间，像这样的远程吸烟器是一个非常宝贵的工具。此外，如果你选择的烧烤架或吸烟器还没有某种类型的嵌入式控制板，我们已经看到了[模拟烹饪工具，适用于与此相同的目的](https://hackaday.com/2022/08/09/smoking-meat-finds-natural-home-in-the-cloud/)。

感谢[Peter]提供的提示，并帮助[megamarco833]进行控制板的逆向工程！