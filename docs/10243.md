# 将 API 用于本 ArduinoJson 演练

> 原文：<https://hackaday.com/2021/05/28/put-apis-to-work-wth-this-arduinojson-walkthrough/>

这个社区出名的一件事是人们会在多大程度上满足一个明显的需求。看看 Arduino 可用的大量库，作为人们如何愿意投入时间使困难任务变得更容易的例子，通常只是虚拟的拍拍背。

库作者的上一层是那些不厌其烦地解释所有这些库如何在现实世界的应用程序中工作的人。[Brian Lough]最近接受了这一挑战，他对 ArduinoJSON 库的使用进行了全面的解释，这是一个非常有用但经常令人困惑的库，它使物联网项目变得更加容易。

对 ArduinoJSON 解释器的需求不要怀疑它的作者 benot Blanchon，他在记录库方面做得非常出色；更多的是意识到 JSON 本身的性质意味着使用它的库将会很复杂。[Brian]在这里的贡献是分享他在真实世界的 ESP32 示例中启动和运行 ArduinoJSON 的见解，以及处理解析人类可读文本文件的潜在缺陷，该文本文件可用于使用微控制器的有限资源表示几乎任何数据对象。除了这些基础知识，我们发现关于指针如何引用动态 JSON 文档对象的警告特别有用；关于使用过滤器筛选大型数据集的内容也很有用。

感谢[Brian]抽出时间公布这些有价值的信息。希望这能鼓励其他人以同样清晰简洁的方式分享来之不易的知识财富。

 [https://www.youtube.com/embed/NYP_CxdYzLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NYP_CxdYzLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

