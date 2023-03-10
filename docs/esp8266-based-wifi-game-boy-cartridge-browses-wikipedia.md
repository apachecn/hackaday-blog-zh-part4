# 基于 ESP8266 的 WiFi 游戏男孩墨盒浏览维基百科

> 原文：<https://hackaday.com/2021/12/18/esp8266-based-wifi-game-boy-cartridge-browses-wikipedia/>

[Sebastian Staacks]偶然发现了他以前的 Game Boy，并且(像你一样)想知道最近将 WiFi 接口楔入标准墨盒的尝试发生了什么。过了一会儿，得出的结论是，人们处理问题的方式让问题变得太难了，因此受到了伤害。显然，这意味着有必要坚持到底，并建立一些东西，这正是他用他的 [WiFi 游戏男孩墨盒所做的。](https://there.oughta.be/a/wifi-game-boy-cartridge)

最近的一个趋势是将一个快速的微控制器连接到总线上，然后将整个接口的把戏转移到软件中。这在某些情况下很好，但是对于 GB 接口，就不那么容易了。GB 由夏普 LR35902 驱动，运行速度超过 4 MHz，但其机器周期需要 4 个时钟，指令速率仅为 1 MHz。盒式接口直接显示原始 CPU 总线。这有好有坏。这是好的，因为它支持各种扩展模块，如相机、打印机和其他定制外设，但这是坏的，因为全速与 CPU 接口的负担正好落在墨盒的职权范围内。

![](img/25fcf323d700f1eba4b5ec02441ce466.png)

Staacks 没有试图将总线直接连接到快速微控制器，而是采取了不同的方法；通过使用分立逻辑对地址总线进行解码，可以轻松获得嵌入式 ESP8266 和插座式 EEPROM 的芯片选择。前者的时钟也被选通并发送到 ESP8266，产生一个中断来唤醒它。EEPROM 存储一个简单的应用程序，其工作是通过 ESP8266 WiFi 堆栈显示 OSD 键盘并向维基百科发送请求。生成的文本将显示在 160×144 点阵显示器上。应用程序只需丢弃发送给它的第一个数据字节，然后重试访问，就可以降低 ESP8266 的中断延迟。这样，ESP8266 可以将大部分时间用于处理无线任务，只是偶尔停下来与应用程序交换一个字节。一个简单的解决方案，看起来确实有效！如果你准备构建其中的一个并编写你自己的应用程序，你可以[漫步到 GitHub](https://github.com/Staacks/wifi-game-boy-cartridge) 上，克隆你自己的一个副本并开始工作！

我们之前已经看到了一些这样做的尝试，[davedarko] [尝试了这个项目](https://hackaday.io/project/20769-wifi-game-boy-cartridge/discussion-83227)，如果你[搜索 hackaday.io，你会得到大量的 GB hacks 来浏览](https://hackaday.io/projects?tag=gameboy&range=month)。最后，[最近的一条 twitter 帖子](https://twitter.com/systemoflevers/status/1471586665949016065?t=OZrQKaS_UfU3PYQNInAiRg&s=19)也指出了[另一项与 Wi-Fi](https://www.systemoflevers.com/blog/2021/12/16/gameboy-wifi-cart/) 类似的努力，但开发仍在进行中。我们稍后再来查看！

 [https://www.youtube.com/embed/QS4fzElm8zk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QS4fzElm8zk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

