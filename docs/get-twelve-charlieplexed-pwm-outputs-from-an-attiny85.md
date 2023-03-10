# 从 ATtiny85 获得 12 个 Charlieplexed PWM 输出

> 原文：<https://hackaday.com/2019/02/24/get-twelve-charlieplexed-pwm-outputs-from-an-attiny85/>

我们大多数人都知道，charlieplexing 可以从相对较少的 I/O 引脚驱动大量的 led，但[戴维·约翰逊-戴维斯]展示了为该方法增加另一个维度，以创建单独控制的 PWM 输出。他的 ATtiny85 有 12 个 led，每个都有单独设置的亮度级别，并且只使用了设备上五个 I/O 引脚中的四个。

每个 LED 可以分配 0(完全关闭)和 63(完全打开)之间的亮度。PWM 是利用 ATtiny85 中的一个定时器产生一个周期性中断来完成的，中断的 ISR 负责为每个 charlieplexed 输出设置必要的开和关时间比。结果呢？12 个无闪烁的 led，具有可单独寻址的亮度水平，使用 8 引脚微控制器和几个无源元件安装在一个小试验板上。ATtiny85 上甚至还有一个 I/O 引脚，用于接受命令或读取传感器。

[大卫]真的从 ATtiny 系列微控制器的紧凑项目中挤出了很多，比如他的[微型函数发生器](https://hackaday.com/2018/03/02/tiny-function-generator-on-the-attiny85-complete-with-oled/)(最近[得到了更新](http://www.technoblogy.com/show?2FCL))。)他还展示了虽然 charlieplexing 通常与 led 一起使用， [charlieplexing 也可以与开关](https://hackaday.com/2018/02/04/a-game-that-does-more-with-less/)一起使用。