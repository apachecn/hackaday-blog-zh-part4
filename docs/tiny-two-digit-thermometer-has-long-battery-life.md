# 微型两位数温度计有很长的电池寿命

> 原文：<https://hackaday.com/2019/05/29/tiny-two-digit-thermometer-has-long-battery-life/>

像他的大部分工作一样，[这个微小的两位数温度计](http://www.technoblogy.com/show?2G8T)显示出【戴维·约翰逊-戴维斯】在有效利用硬件的项目上有诀窍。DS18B20 温度传感器、表面贴装七段 LED 显示器和驱动这一切的 ATtiny84 之间没有任何引脚闲置。温度每 24 秒闪烁一次，设备在其余时间处于深度睡眠状态，一个好的 CR2032 硬币电池应该可以为设备供电近一年。这块木板本身只有大约一英寸见方。

你可能认为每 24 秒才闪烁一次的显示器实际上很难阅读，你是对的。[David]发现观看显示屏，等待一段未知的时间来阅读一些短暂闪现的令人惊讶的数字确实不切实际。为了解决这个问题，小数点会在温度出现之前闪烁。这种倒计时提醒观众即将到来的显示，其代价是电流消耗的增加几乎可以忽略不计。

[David]的项目报告解释了一切是如何运作的。他还逐步介绍了源代码的不同部分，解释了一切是如何工作的，包括低功耗模式。GitHub 库保存了所有的源文件，也可以通过他们便利的共享项目功能直接从奥什公园[订购电路板。](https://oshpark.com/shared_projects/CWZO4SzB)

低功耗增加了项目的复杂性，但回报很容易值得花时间来实现它们。我们对仍然相关的低功耗 WiFi 微控制器进行了详细介绍[，像](https://hackaday.com/2018/12/17/a-deep-dive-into-low-power-wifi-microcontrollers/)[这个气象站](https://hackaday.com/2018/11/04/weather-station-is-a-tutorial-in-low-power-design/)这样的项目展示了实际的低功耗设计工作。