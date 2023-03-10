# 双传感器回声定位器以低成本提供高精度

> 原文：<https://hackaday.com/2018/07/12/dual-sensor-echo-locator-gives-high-accuracy-at-low-cost/>

红外线当然有它的用途，但如果你想定位物体，超声波探测要优越得多。它是非接触式的，人耳察觉不到，也不会受到烟雾、灰尘、环境光或傻线的影响。

如果你有一个超声波传感器和一个微控制器，你就可以检测很多有用的东西，比如雨水桶中的水位或者平板电脑沿轨道移动的距离。[如果你有两个传感器和一个微控制器，你可以使用三角学](http://www.instructables.com/id/Dual-Sensor-Echo-Locator/)精确定位定义范围内的任何物体。

[lingib]的双传感器回声定位器使用两个 HY-SRF 05，但便宜和丰富的 HC-sr04 也将工作。两个传感器都被安排成最大的光束重叠，并连接到 Arduino Uno。一个传感器的发射器被胶带挡住了，所以它所做的只是听。

当系统注册对象时，它在加工草图内的网格上显示为一个红点，以及一系列细节，如对象的坐标、它与每个传感器的距离以及由两个传感器和对象形成的三角形的面积。[lingib]报道称，该系统非常准确，休息后将适用于比演示中的 1 米见方大得多的操场。

不想检测物体？超声波传感器足够便宜，可以侵入其他东西，比如这个单向数据通信模块。

 [https://www.youtube.com/embed/R1r_Ga148gw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/R1r_Ga148gw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示，塞特维尔。