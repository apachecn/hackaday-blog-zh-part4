# 永恒的背光日历

> 原文：<https://hackaday.com/2020/09/08/a-backlit-calendar-for-all-eternity/>

阳历与七天工作周相结合的不规则性的优势在于，它们为纸日历行业提供了持续的年收入来源。早在可持续发展成为一个流行话题之前，人们就发明了可重复使用的万年历，但这些日历的非数字版本有时是很难解释的复杂表格。[andrei.erdei]创造了一个[自动万年历](https://www.instructables.com/id/Backlit-Automated-Perpetual-Calendar-a-CNC-Project/)，它主要是硬件，但使用一些数字技巧来克服这些问题。

日历由烟熏丙烯酸夹层板组成，由一些 WS2812Bs 条从背后照亮。虽然面板可以用激光切割机加工，但[andrei.erdei]使用了 CNC，这使他可以在背板上磨一些凹槽来固定 LED 灯条。数字的模板被简单地打印在纸上，背景通过在同一张纸上打印几次而变得不透明。电子设备包括一个 ESP8266，它从 NTP 服务器获取数据，并在工作日和周末以不同颜色点亮相应的 led。

这种类型的万年历的经典版本使用[滑动框架](https://hackaday.com/2020/07/11/a-desk-calendar-with-a-difference/)，但我们也看到了基于[移动齿轮](https://hackaday.com/2020/07/26/concentric-rings-keep-this-calendar-perpetually-up-to-date/)的完全不同的版本。

休息后的视频。

 [https://www.youtube.com/embed/qE_cd2mV8AY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qE_cd2mV8AY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

