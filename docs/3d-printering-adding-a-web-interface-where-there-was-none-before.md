# 3D 打印:在以前没有的地方增加一个网络界面

> 原文：<https://hackaday.com/2021/12/31/3d-printering-adding-a-web-interface-where-there-was-none-before/>

[伦佐·米希尔蒂]给自己弄了一台中国 3D 打印机，特别是一台飞行熊幽灵 5。(破解名，嗯？)令他颇为恼火的是，虽然 MKS Robin Nano 控制器确实集成了 Wi-FI 模块，但它没有提供基于浏览器的监控界面。退一步说，在这个时代，这似乎有点目光短浅。伦佐对这种情况一点也不满意，他继续使用 websockets 编写专用的 Wi-Fi 固件，但没有在一系列详细的博客文章中完整地记录他的旅程。

由此产生的 BeePrint web 界面支持管理打印机时所期望的所有常用功能，从监控准备阶段的预热，到通过连接的 IP 摄像头监视潜在的意大利面条怪物。都是好东西。[伦佐]使用了一个 [ESP32-cam](https://www.olimex.com/Products/IoT/ESP32/ESP32-CAM/) ，这是我们在 Olimex 的朋友提供的一个低成本的 200 万像素单元，但我们怀疑在组合中添加自己的 IP 摄像头不会非常困难。

【伦佐】有一个 [YT 频道](https://www.youtube.com/c/RenzoMischianti/videos)详细介绍了相当多的其他项目，在我们看来，这绝对值得一些观看时间。

自从恐龙漫游以来，我们一直在报道 3D 打印机黑客。这是我们在快速搜索中能找到的最古老，也是最奇怪的帖子之一。有人想找些更古老的东西吗？

 [https://www.youtube.com/embed/VzX84yEbjKM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VzX84yEbjKM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

