# 重现丰田汽车的“油门卡住”问题

> 原文：<https://hackaday.com/2022/10/30/recreating-the-stuck-throttle-problem-on-a-toyota/>

几年前，丰田因其大量乘用车出现重大安全问题而成为新闻焦点。看似随意，某些汽车在没有考虑驾驶员输入的情况下加速，造成许多撞车事故，至少 37 人确认死亡。据报道，他们召回了向前滑动卡住油门踏板的地垫，但这并不能解释所有这些事故。另一次召回是因为油门卡住，[，[科林·奥弗林]在他的测试台上证明了这是一个可能的原因。](https://twitter.com/colinoflynn/status/1586168627338022912)

虽然大多数车龄在 15-20 年以上的乘用车使用从节气门体直接连接到油门踏板的电缆来控制节气门，但大多数制造商已经转向电传操纵系统，该系统从油门踏板获取传感器输入，并将该位置信息发送到车辆的计算机，计算机进而调整节气门位置。这可能制造成本略低，但会给关键系统带来更多的故障模式。

[科林]正在通过在车辆电脑的特定点引入电磁脉冲来重现其中一种故障模式。在现实世界中，这可能是由某种形式的电动势[引起的，其中可能包括宇宙射线](https://spectrum.ieee.org/toyota-problems-caused-by-cosmic-rays)。这引入了计算机似乎无法识别或清除的内存故障。在[Colin]可以可靠地产生的一组正确的情况下，计算机最终会将油门开到最大，这种情况只能通过重启车辆的计算机来纠正。

丰田坚持认为，这些问题已经成功地在驾驶员侧的地毯下解决了，但根据 IEEE 和航空电子等相关行业的其他专业人士的说法，乘用车行业在确保这些系统中有足够的冗余来解决这些类型的故障方面做得非常少。[Colin]确实计划将来在真实车辆中测试他的设置，以确认车辆将在他的实验室场景下实际运行，所以我们应该在将来看到更多关于这方面的信息。如果你正在寻找一辆不受电脑控制相关问题影响的汽车，[看看这辆汽车](https://hackaday.com/2016/05/03/volkswagen-beetle-the-most-hackable-car/)，它甚至不需要电池来驱动，只要你能推动它。

 [https://www.youtube.com/embed/JgjOVe_czmk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JgjOVe_czmk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

