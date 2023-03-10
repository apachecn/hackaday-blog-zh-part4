# 一个黑客的圣诞故事

> 原文：<https://hackaday.com/2022/12/24/a-hackers-christmas-story/>

那是圣诞节的前一天晚上，因为我决定今年自己给每个人做礼物，所以我还在拼命工作，想在最后期限前把一切都做好。我为什么要这样对自己？部分原因是因为我喜欢这个过程。

我的妻子有一个想法，我们可以为老年人做一些有趣的装饰性闪光的东西，并挑选了一些动机。然后我儿子把它们画在纸上，我把这些画扫描进去，用 CAD 描绘出来。然后，我们在数控镂铣机上把木头切割成各种形状，结果非常成功。(现在我已经做到了，如果瑞典平板包装商出售的所有这些“古怪”的装饰品不是由三年级学生最初画出来的，我不会感到惊讶。)

然后我的儿子画了它们，我的工作是插入闪烁。为此，我买了一些三线“童话灯”，它们真的很有趣。它们类似 WS2812s，只是它们不是使用四个引脚并将数据向下游转移，而是在一条总线上，每个都有一个硬编码的地址，它们知道自己在串中的位置，每个 LED 只侦听第 n 组 24 位。这意味着要发送 200 个颜色代码来点亮米基阿姨装饰树上的 4 个 led 灯，但就这样吧。

最后一站，也是截至 23 日的最后一站，找出某种木制电池盒，插入 LiPo 和充电电路，并焊接一个开/关开关。到最后一刻了，但事情不都是这样吗？

网上订购肯定会更容易。但这就是付出的精神吗？不要！DIY 的方式让家人聚在一起，让我有时间接触数控机床，提高我的 FreeCAD 技能。在我们编写一些 LED 动画的时候，我的儿子甚至从我的肩膀上看过去。没有什么比手工编码的薄饼更能表达圣诞节了。

祝大家节日快乐！

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!