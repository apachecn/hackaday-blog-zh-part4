# 自动化炮塔保持宿舍整洁，机械战警风格

> 原文：<https://hackaday.com/2021/12/14/automated-turret-keeps-dorm-clean-robocop-style/>

学生宿舍通常不被认为是最有秩序的地方。无论是水槽里堆积如山的盘子，成堆等待清洗的衣服，还是散落在走廊上的零零碎碎的东西，对于许多宿舍居民来说，打扫卫生都是很不重要的事情。

[Luis Marx]似乎发明了一个有用的解决方案来解决他(或他的室友)的邋遢问题:[一个机器人炮塔](https://www.youtube.com/watch?v=cjKukBJix5g)，它可以向任何留下无人看管的物品的人开火(视频，德语，嵌入下面)。该系统使用一套“杂乱传感器”，可以放置在房子周围的战略位置，并使用超声波传感器检测杂散物体。如果发现任何异常，将通过 WiFi 向主系统发出警报。然后炮塔会搜索附近的任何人，并用小塑料球射击他们。

问题中的炮塔是一个设计精美的套件，由 3D 打印零件制成，由 ESP32 控制。它可以绕轴旋转，并使用两个伺服系统上下倾斜，而它的发射机构由 DC 电机驱动。由于基于摄像头的物体传感器可以识别人类，它可以跟踪目标。整个事情给了我们一点机械战警的感觉；我们还以为它会喊`Pick up those clothes. You have twenty seconds to comply.`

虽然这可能不是解决脏乱宿舍的最终办法，但我们喜欢它背后的创造性思维。我们以前见过[自动瞄准炮塔](https://hackaday.com/2021/06/06/automated-sentry-turret-for-your-secret-lab/)，但不是在像这样的家庭应用中。当然，还有很多其他的[机器人可以帮你做家务](https://hackaday.com/2021/01/28/modded-robot-vacuum-can-whistle-while-it-works/)。

 [https://www.youtube.com/embed/cjKukBJix5g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cjKukBJix5g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

