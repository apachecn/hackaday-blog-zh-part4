# 这些由大脑控制的猫耳朵会随着你的心情而移动

> 原文：<https://hackaday.com/2022/03/19/these-mind-controlled-cat-ears-move-with-your-mood/>

任何一个养猫的人都会告诉你，猫的耳朵是其精神状态的重要标志:如果它们想要引起你的注意，耳朵会向前突出；如果它们生气，耳朵会向后翻；如果它们害怕，耳朵会向下折叠。人类有时戴猫耳发带作为一种时尚声明，但一动不动地坐着这些耳朵更可能让猫困惑，而不是提供任何有意义的交流。

[Jazz DiMauro]旨在通过设计一款能够真正响应你的情绪的猫耳发带来填补这一空白。它通过连续进行脑电图测量并从中提取“注意力”和“冥想”变量来实现这一点。这些值然后被应用到一组伺服系统，允许每个 3D 打印耳朵的双轴运动。脑电图读出设备是一种现成的 MindWave 耳机，通过蓝牙输出其传感器数据。然后 Arduino 读出数据并驱动伺服系统。

将所有这些变成一个可用的可穿戴设备本身就是一个项目:[Jazz]经历了几次迭代，以找到合适的电源和布线策略，直到他们选定了一对锂聚合物电池和一根扁平电缆。最终的结果看起来足够舒适，耳朵的运动看起来流畅自然。剩下的就是用真正的猫来测试它，看看它们现在是否也能最终理解人类的情感。

我们之前已经推出过几款移动猫耳头带:[一款随着头部的运动而移动](https://hackaday.com/2016/02/26/mechatronic-cat-ears-for-the-rest-of-us/)，还有[一款手动控制](https://hackaday.com/2012/02/21/live-out-your-inner-animist-with-animatronic-cat-ears/)。今天的脑电图仪展示了脑电图的另一个应用，它已经被用于从[唤起清醒梦](https://hackaday.com/2012/12/20/modifying-an-eeg-headset-for-lucid-dreaming/)到[玩啤酒乒乓](https://hackaday.com/2020/12/09/mind-controlled-beer-pong-gets-easier-as-you-drink/)的任何事情。

[https://player.vimeo.com/video/262855378](https://player.vimeo.com/video/262855378)