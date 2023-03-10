# 回流期间导致 led 发光的神秘效果

> 原文：<https://hackaday.com/2022/02/09/mystery-effect-causing-leds-to-glow-during-reflow/>

有时你会注意到一些你无法解释的小事。[Greg Davill]本周发现自己就处于这样的情况，他注意到在对一些电路板进行回流时，一些绿色发光二极管发出微弱的光。自然，【格雷格】着手调查。

绿色发光二极管被连接起来作为电源指示器，[Greg]怀疑电路板上的聚合物帽可能会以某种方式产生一个小电流，导致发光二极管稍微亮一点。一个简单的测试是将一个聚合物帽直接连接到万用表上。当用热风枪加热时，仪表显示“在 5-10 uA 范围内”的小电流

更进一步，[Greg]将一个 LED 焊接到盖子上，并再次加热，这次加热到 100°c。LED 发光，在撤去热量后继续发光约 60 秒。谜团也变得更深了——[ Greg]注意到这只发生在“新”电容器上。一旦它们经历了一个热循环，当加热时，盖子将不再点亮 LED。

这是一个奇怪的案例，Twitter 上有许多关于致病机制的猜测。从热电效应到电容器内部化学反应的解释。如果你对这里发生的事情有内幕消息，请不要犹豫，在评论中告诉我们。与此同时，看看[Greg]的一些最好的作品——[一个发光的 D20 骰子，有 2400 个巨大的 led。](https://hackaday.com/2021/04/03/you-can-now-build-your-own-glowing-led-d20-with-a-whopping-2400-leds/)

【感谢 J Peterson 的提示！]