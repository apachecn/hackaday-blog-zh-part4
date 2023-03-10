# 永远不要忘记再次打开抽油烟机

> 原文：<https://hackaday.com/2021/01/04/never-forget-to-turn-on-the-cooker-hood-again/>

抽油烟机是去除厨房多余烟雾和蒸汽的绝妙发明。但像所有电动设备一样，它只有在打开时才能工作。这是[彼得]面临的问题，他的家人都是热情的厨师，却经常忘记按开关。他的解决方案？[一个自动抽油烟机开关，在使用时打开](http://peter.turczak.de/content/projects/abzug/index.html)，并在使用后保持足够长的时间，以完全驱散油烟。

它的核心是三相炉子电源线上的电流变压器，我们可以通过 Arduino 从这些设备上读取数据。它们有一个分流电阻来产生电压，其交流输出置于参考 DC 电压上，为微控制器引脚供电。阻抗相当高，因此当传感器必须放置在离微控制器一定距离的地方时，就需要一个运算放大器缓冲器。这些读数会导致 Arduino 触发一对继电器来打开或关闭抽油烟机。我们可以想象，家庭厨房对它来说是一个更加舒适的环境。

炊具开着的时候也会带来相当大的危险。为此，我们过去也推出过[烹饪报警器](https://hackaday.com/2018/12/09/stove-alarm-keeps-the-kitchen-safe/)。

头图:Pbroks13， [CC BY-SA 3.0](https://commons.wikimedia.org/wiki/File:Modern_Kitchen.jpg) 。