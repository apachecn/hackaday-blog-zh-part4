# 无示波器时钟测试？

> 原文：<https://hackaday.com/2022/03/11/clock-testing-sans-oscilloscope/>

和很多修东西的人一样，【学电子维修】有一个示波器。但在用它测试主板晶体振荡器后，他开始思考没有示波器的人如何做同样的测试。他买了一个[频率计数器/晶体测试仪套件](https://www.youtube.com/watch?v=n5N-NZyYYMg),相当便宜——不到 10 美元。他建造了它，然后试着看看它在电路中的效果如何。

该套件有一个不寻常的使用 7 段显示器排序显示菜单的话。有一个插座可以插入一个晶体进行测试，但这对于预期的应用来说是行不通的。他做了一个小扩展器来简化晶体的连接，即使它们是表面贴装的。他最终在计数器输入端添加了一个 BNC 插座，但起初只是直接连接了一些测试引线。

那么与使用示波器相比，使用频率计进行探测的效果如何呢？你会认为它应该没有真正的问题。一方面，从计数器读取频率应该更容易，特别是如果你没有显示波形数据的示波器。另一方面，计数器不会给出任何关于时钟源质量的数据。很吵吗？干净？50%占空比还是 10%？没有瞄准镜看不出来。然而，事实证明，由于某种原因，廉价的计数器不会从主板上读取高频时钟信号。但是，它能够测量风扇 PWM 信号。

我们假设廉价的频率计数器没有合适的输入级，并且正在加载晶体振荡器。电线探针可能也没有任何帮助。一个合适的频率计数器可能会起作用，但一个有频率计数器功能的便宜的电表并没有更好的表现。他还将一个示波器探头连接到两个设备上，也没有得到更好的结果。我们想知道探头上的 10X 设置是否会减少电路的负载。我们也认为我们之前报道过的前置放大器黑客可能会有所帮助。

最后，这个便宜的小装置似乎没有达到他最初的目的。但是对于一个简单的晶体测试器和频率计数器来说，这已经足够便宜了。虽然一个合适的频率计数器可能会起作用，但是[示波器的成本越来越低](https://hackaday.com/2022/02/26/60-pc-oscilloscope-review/)，而且它们可以做得更多。