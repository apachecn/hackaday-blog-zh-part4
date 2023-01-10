# 微型条形码扫描仪一起哔哔你的购物清单

> 原文：<https://hackaday.com/2020/06/12/tiny-barcode-scanner-beeps-your-shopping-list-together/>

带一份纸质清单去杂货店似乎是个好主意，至少在你到那里并尝试使用它之前是这样。你记得带笔了吗？太好了。写字板怎么样，这样你划掉什么东西的时候就不会在纸上打洞了？应用程序更容易做到这一点，尤其是带有复选框的应用程序，但你仍然需要手动输入所有内容。在扔掉包装之前，把你需要的东西的条形码扫描成一个清单不是更容易(也更有趣)吗？

这正是[DavidE281]的[条形码扫描仪](http://www.instructables.com/id/Barcode-Scanner-for-Bring-Shopping-List/)背后的理念，该扫描仪旨在与 Bring 配合使用！app。他所要做的只是扫描一个条形码，产品就会整齐地出现在他手机的列表中。这是一个基于 M5StickC 的简单构建，M5 stickc 是一个 ESP32 开发套件，具有一个小显示器和一个 6 轴 IMU 以及一些其他好东西。[David]将其与具有串行端口的 2D 条形码扫描仪相结合，并设计了一个将它们连接在一起的印刷外壳。

它是这样工作的:M5Stick 通过 MQTT 将条形码发送到运行 Home Assistant 的外部 Raspberry Pi。Pi 在电子表格中进行查找，并将数据发送给 Bring！基于社区构建的 API 的应用程序。同时，它会将产品名称发送回 M5Stick 的显示屏，以确认该产品已被添加到列表中。休息之后，请观看一口大小的演示视频。

扫描条形码超级好玩。[那么，为什么不使用物联网条形码扫描仪来跟踪您拥有的一切呢？](https://hackaday.com/2018/08/15/track-everything-everywhere-with-an-iot-barcode-scanner/)

 [https://www.youtube.com/embed/WjKDoKFwufE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WjKDoKFwufE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

