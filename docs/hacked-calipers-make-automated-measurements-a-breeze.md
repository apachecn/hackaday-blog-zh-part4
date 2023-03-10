# 黑客卡尺使自动化测量变得轻而易举

> 原文：<https://hackaday.com/2019/07/04/hacked-calipers-make-automated-measurements-a-breeze/>

现在，带有有线接口来捕捉当前读数的数字卡尺已经不是什么新鲜事了。但是好的都很贵，说真的，把一根 75 美元的电缆插到电脑上有什么意思呢？因此，当[Max Holliday]被要求[设计一些卡尺来自动采集数据](https://www.notion.so/Hacking-Digital-Calipers-3ee7726f11ca431694dc70a1977516e4)时，他必须发挥创造力。

[Max]发现廉价的 Harbor Freight 数字卡尺有一个可以盖住串行连接器的门，这使它们成为黑客攻击的完美目标。一点互联网调查揭示了连接器的引脚排列以及大多数数字卡尺使用的串行协议的一些细节:24 位数据包是 6 个 4 位字。[Max]使用了他的 [SAM32](https://github.com/maholli/SAM32) ，这是一个简洁的开源板，带有 SAMD51 和 ESP32，可以运行 CircuitPython。一个反相缓冲器将串行线与电路板连接，电路板的大小正好适合安装在卡钳头的背面。很难判断[Max]是如何触发读数的，但 SAM32 是作为 USB 设备安装的，并将按键直接发送到电子表格——是的，对于 ESP32，它可能是无线的，但他的客户特别要求有线设置。获取多个读数很容易，因为用户再也不用把卡尺换成笔了。

像这样的廉价卡钳非常容易破解——你可以[添加蓝牙](https://hackaday.com/2013/06/20/giving-digital-calipers-bluetooth/)、[把它们变成铣床的 DROs](https://hackaday.com/2014/01/19/three-axis-position-indicator-with-digital-calipers/) ，甚至[让它们说话](https://hackaday.com/2011/11/09/talking-digital-calipers-make-engineering-more-accessible/)。