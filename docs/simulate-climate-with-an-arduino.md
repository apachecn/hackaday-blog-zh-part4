# 用 Arduino 模拟气候

> 原文：<https://hackaday.com/2019/08/02/simulate-climate-with-an-arduino/>

温室创造了一个特别适合你想要种植的植物的人工气候。这是通过监控温度和湿度等条件来实现的，并使用通风口、风扇、灌溉和照明设备等来提高温度。但是，你怎么知道什么时候应该提高湿度，或者释放一些内部积聚的热量呢？最简单的方法是使用来自[934Virginia]的由 Arduino 驱动的诺曼气候模拟器,它利用基于 NOAA 天气数据的不同地点或一年中不同时间的数据来模拟特定的生长环境。

Norman 依靠关于目标位置的简单数据输入，从坐标和指定的日期范围返回温度和湿度天气条件的最小/最大值。它广泛使用 Dusk2Dawn 库，并使用数学建模方法模拟其他大气条件，以便对目标气候做出相对准确的估计。在该项目的绘图页上有一些模拟展示了这些数据的样子。

[934 Virginia]Arduino library 使用这些数据来比较您的温室中的目标气候和实际传感器读数之间的差异。从那里你可以手动改变环境，或者如果你运气好，已经有了[一个基于 Arduino 的温室自动化系统](https://hackaday.com/2012/06/05/large-scale-arduino-controlled-greenhouse-does-some-serious-farming/)气候调节可以自动完成。该项目以诺曼·博洛格的名字命名，[，一位著名的土壤科学家，也是一位值得一读的人物。](https://hackaday.com/2018/03/26/norman-borlaug-saves-a-billion/)

**编者按:**本文由原文改写，纠正事实错误。最初的文章错误地聚焦于在不使用传感器的情况下复制气候。这个项目确实需要传感器来比较实际的温室条件和图书馆计算的历史气候条件。我们为此向[934Virginia]道歉，并感谢他们来信指出错误。

图片由[维基共享资源](https://upload.wikimedia.org/wikipedia/commons/8/8f/Greenhouse_for_strawberry.jpg)提供。