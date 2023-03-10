# 谢妮拍摄定时器添加到浓缩咖啡机有用的优雅

> 原文：<https://hackaday.com/2021/03/26/nixie-shot-timer-adds-useful-elegance-to-espresso-machine/>

一旦你把咖啡豆磨碎并夯实，就要掌握好时间来制作一杯完美的浓缩咖啡了。理想情况下，萃取应该持续 20-30 秒，从第一滴深色的咖啡滴到顶部的棕褐色和虎纹克莉玛，让咖啡回味无穷。

[![](img/1d581b67df59c3f62d6d7b85780bd13b.png)](https://hackaday.com/wp-content/uploads/2021/03/nixie-shot-timer-guts.jpg) 【马可】有一台漂亮的浓缩咖啡机，只缺少一样东西:[一个同样漂亮的数码管显示的计时器](https://voot.de/projects/nixie-shot-timer/)。[Marco]没有弄乱电线，而是采用了非侵入性的方法，正在使用一个 DIY 线圈来检测浓缩咖啡机泵的磁场，并启动一个计时器。

基于 LM358 的运算放大器放大机器感应的电流，并将其馈入 Arduino Nano，后者进行 FFT 计算。[Marco]发现了一种高压接口驱动器，可以将 170 V 电压切换到 Nixies，而不是使用两把晶体管。休息过后，你可以去买一瓶纯白葡萄酒，看看它。

最后一批 Nixies 可能是在 20 世纪 80 年代大规模生产的，但不要害怕——Dali bor Farny 正在保持梦想并制造新的 Nixies。

 [https://www.youtube.com/embed/X-ks6YiHkdw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/X-ks6YiHkdw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

