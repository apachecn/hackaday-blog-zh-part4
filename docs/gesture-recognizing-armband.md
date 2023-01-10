# 一种手势识别臂章

> 原文：<https://hackaday.com/2021/01/02/gesture-recognizing-armband/>

手势识别通常涉及某种光学系统观察你的手，但加州大学伯克利分校的研究人员采取了不同的方法。相反，他们正在监控控制肌肉的前臂电信号，并创建一个机器学习模型来识别手势。

该传感器系统是一个灵活的宠物臂带，上面用银导电墨水丝网印刷了 64 个电极，连接到一个独立的人工智能处理模块。由于每个人的手臂略有不同，该系统需要针对特定用户进行训练，但这也意味着特定的电信号不必在学习识别模式时被隔离。

其中具有挑战性的部分是，模式不会随着时间的推移而保持不变，而是会根据出汗、手臂位置等因素而变化，甚至只是生物变化。为了处理这种情况，该模型可以随着信号的变化在设备上随时间更新自身。我们欣赏的这项研究的另一部分是，所有的推理、训练和更新都发生在臂带中的人工智能芯片上。无需将数据发送到外部设备或“云”进行处理、更新或第三方数据挖掘。不幸的是，包含所有细节的[研究论文](https://www.nature.com/articles/s41928-020-00510-8)在付费墙后面。

这项技术最明显的应用是在修复术中，但是它也可以作为任何人的通用计算机输入。替代输入设备在 2020 年黑客日奖中占据重要地位，包括为脑瘫患者提供的[通用遥控器](https://hackaday.com/2020/10/06/gesture-controller-for-roku-and-universal-keyboard-built-by-ucpla-dream-team/)，以及用于嘴巴的[字节操纵杆](https://hackaday.com/2020/11/07/the-byte-is-the-grand-prize-winner-of-the-2020-hackaday-prize/)。

 [https://www.youtube.com/embed/z3D9WBfUKsQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/z3D9WBfUKsQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示！