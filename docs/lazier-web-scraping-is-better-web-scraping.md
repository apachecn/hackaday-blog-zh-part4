# “懒惰”的网页抓取是更好的网页抓取

> 原文：<https://hackaday.com/2022/02/07/lazier-web-scraping-is-better-web-scraping/>

曾经需要从网页上获取数据吗？解析数据内容被称为 web 抓取，Doug Guthrie 有一些技巧可以让从网页中挖掘数据的过程变得更简单、更高效，并附有 Python 代码示例。他以从 Yahoo Finance 获取数据为例，因为从 Stack Overflow 上出现问题的频率来看，这显然是一个非常常见的用例。然而，一般概念是相当广泛适用的。

![](img/436f6e780887aeb6ac157d8898d25825.png) [Doug]表明，虽然解析网页中的特定数据(例如，股票价格)并不困难，但有时有更简单快捷的方法。在雅虎财经的例子中，我们大多数人看的网页并不是显示数据的真正来源，它只是一个前端。

更有效地收集数据的一种方法是找到数据源。以 Yahoo Finance 为例，显示在网页上的数据来自最终用户完全可以访问的 JavaScript 变量，并且更容易解析和处理。另一种方法是降低一个级别，从与前端 web 页面相同的位置检索 JSON 格式的数据；完全忽略前端，本质上把它当成一个非官方的 API。这两种方法不仅比解析最终结果更容易，而且更快、更可靠。

人们如何找到这些资源？[Doug]给出了一些很好的建议，包括如何使用网络浏览器的开发工具来搜寻 XHR 的请求。这些方法并不适用于所有情况，但它们绝对值得研究，看看它们是否是一种选择。另一个需要记住的资源是 [woob(浏览器之外的网络)](https://hackaday.com/2022/01/17/hack-the-web-without-a-browser/)，它有一个令人印象深刻的后端列表，可用于阅读网络内容并与之交互。所以如果你的程序需要数据，但是数据在网页上？不要让这阻止你！