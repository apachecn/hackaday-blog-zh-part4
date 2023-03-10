# 游泳池温度监视器安抚幸运但沮丧的孩子

> 原文：<https://hackaday.com/2021/05/02/pool-temperature-monitor-mollifies-fortunate-but-frustrated-children/>

当你可以在爷爷奶奶家的私人泳池里狂欢时，谁还需要城市泳池呢？不必等到阵亡将士纪念日周末，那时气温将在五月的第一周达到华氏 90 度。但是，如果终于到了去游泳的时候，而游泳池本身却在 [![](img/ca0d9187477a5bde18044b6637fc5a55.png)](https://hackaday.com/wp-content/uploads/2021/04/pool-temp-inner.jpg) 几英里之外，你怎么能安抚那些每天都想知道的孙子们呢？虽然祖父母可能更喜欢收到你的来信，但没有必要每小时打电话来打扰他们。你只需要建造一个漂浮的远程泳池温度监测器，它每 30 分钟向冰箱上一个与孩子眼睛等高的 Adafruit MagTag 广播一次。

在商业泳池温度监测器的成本和所有提到不确定 Wi-Fi 连接的评论之间，听起来似乎[布莱克]最好推出自己的解决方案。浮动部分内部是一个 ESP32、一个 DS18B 温度传感器和一个 18650 电池。身体的大部分是聚氯乙烯，除了 3D 打印的圆环，其中有一些泡沫用于浮力。底部的几个 BBs 使这个东西保持直立。目前，它显示的是水温，但[Blake]的最终目标是同时显示气温。

也许天气仍然太冷而不能游泳，但是大多数日子阳光灿烂。为什么不利用它的能量来加热水呢？