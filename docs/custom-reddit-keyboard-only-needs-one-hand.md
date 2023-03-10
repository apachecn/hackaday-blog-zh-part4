# 自定义 Reddit 键盘只需要一只手

> 原文：<https://hackaday.com/2020/03/17/custom-reddit-keyboard-only-needs-one-hand/>

有时你可能想在吃三明治、扔飞镖或用剑抵挡攻击者时浏览你最喜欢的社交媒体网站。你知道，正常的事情可能只占用你的一只手。如果你曾经遇到过这种情况，那么[这款定制的 Reddit 键盘可能适合你](https://www.reddit.com/r/functionalprint/comments/fhfkki/i_designed_and_printed_a_little_reddit_keyboard/)。

由[jangxx]建造，这个小板子是最简单的。即使你在练习单手打蛋技术时没有寻找浏览/r/cooking 的方法，同样的原理也可以用来快速组装一个宏键盘，满足你的任何特殊需求。

[![](img/4f5698337e3c115095a1e6b592299696.png)](https://hackaday.com/wp-content/uploads/2020/03/redditkb_detail.jpg) 在 3D 打印的外壳内，没有什么比一个 Arduino Pro Micro 和五个樱桃 MX 红色开关更奇特的了。开关已经直接连接到 Arduino 上的 GPIO 引脚，[，剩下的就交给一个简单的草图](https://pastebin.com/XAbJ8ZNz)。[jangxx]以这样一种方式编写代码，您可以轻松地在文件的顶部定义 USB HID 密钥到物理开关的映射，从而可以方便地重用。

虽然这个项目很简单，但我们真的很喜欢[jangxx]在 3D 打印键帽上经历的麻烦。白色的上下箭头允许你浏览文章，中间的键选择你想看的文章。既然是为了 Reddit，自然是快速投票的红蓝按钮。当你想回到文章列表时，只需再次点击中间的按钮。

回到 2011 年，我们看到了一个专门的 Reddit 投票外设，但我们认为简单导航键的加入使这个项目更引人注目。顺便说一句，如果你能想到任何其他*的理由让你想要一个单手键盘来浏览 Reddit…我们绝对不想听到这个。*