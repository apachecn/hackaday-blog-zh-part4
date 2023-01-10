# RSS 打印机给你你想要的硬拷贝新闻

> 原文：<https://hackaday.com/2022/04/16/rss-printer-gives-you-the-hard-copy-news-you-desire/>

昔日，世界各地的办公室里，电传打字机和连续送纸的点阵打印机以硬拷贝形式大量输出数据。[Jan Derogee]想要一点那种老派的魅力，于是他开始用自己拥有的一台古老的打印机制造一台 RSS 新闻打印机。

该版本依赖于 ESP8266，支持 WiFi 的微控制器能够随时在线跳转并查询 RSS 订阅内容。它从 XML 文件中获取标题、描述和出版日期信息，并将其格式化以输出到打印机。然后，微控制器通过 Commodore 串行接口将数据发送到 Brother HR-5C 打印机。与同时代的点阵打印机不同，HR-5C 是热敏打印机。一旦装上一卷合适的纸，它就可以连续打印，不需要任何难以找到来源的墨带。

随着无线互联网和 210 毫米热敏打印纸的不断供应，[简]的系统应该在未来几年为他提供新闻摘要。[我们以前也见过类似的复古新闻字幕项目](https://hackaday.com/2021/01/18/apple-ii-prints-off-the-breaking-news/)。休息后的视频。

 [https://www.youtube.com/embed/CKv37Jkw3jI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CKv37Jkw3jI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

