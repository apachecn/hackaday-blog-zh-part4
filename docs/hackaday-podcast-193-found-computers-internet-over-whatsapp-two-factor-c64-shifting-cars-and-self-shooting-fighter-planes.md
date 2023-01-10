# 黑客日播客 193:发现电脑，WhatsApp 上的互联网，双因素 C64，移动汽车，和自拍战斗机

> 原文：<https://hackaday.com/2022/11/18/hackaday-podcast-193-found-computers-internet-over-whatsapp-two-factor-c64-shifting-cars-and-self-shooting-fighter-planes/>

本周，主编埃利奥特·威廉姆斯和特约撰稿人丹·马洛尼回顾了这一周的行动文献。我们几乎可以在任何东西里找到 Linux 机器，包括路边的电视和安全得惊人的电动汽车充电器。没有网络？没问题——只需通过 WhatsApp 隧道 IP 即可！我们将看到 3D 打印机可以重新用于廉价的实验室自动化，构建有史以来最差但最酷的 2FA 加密狗，并看到摇摇欲坠的卡塔如何让您的旧主板认为任何 ISA 卡都插入其中。担心驾驶电动汽车会是一次无聊的经历？别担心——也许你还是会被挡在外面。但是如果你这样做了，请放心，我们会做大量细致的工程来确定它是否安全。呃，至少我们希望如此…

[//html5-player.libsyn.com/embed/episode/id/25062870/height/90/theme/custom/thumbnail/yes/direction/backward/render-playlist/no/custom-color/000000/](//html5-player.libsyn.com/embed/episode/id/25062870/height/90/theme/custom/thumbnail/yes/direction/backward/render-playlist/no/custom-color/000000/)

为了安全起见，请下载播客。

如果你想继续关注，请点击下面的链接，并一如既往地在评论中告诉我们你对这一集的看法！

Where to Follow Hackaday Podcast

### 关注 Hackaday 播客的地方:

*   [谷歌播客](https://podcasts.google.com/feed/aHR0cDovL2ZlZWRzLnNvdW5kY2xvdWQuY29tL3VzZXJzL3NvdW5kY2xvdWQ6dXNlcnM6OTM5MTM0NzIvc291bmRzLnJzcw)
*   [iTunes](https://itunes.apple.com/us/podcast/hackaday-podcast/id1447409683)
*   [Spotify](https://open.spotify.com/show/3NRV0mhZa8xeRT0EyLPaIp)
*   [装订机](https://www.stitcher.com/podcast/hackaday-podcast)
*   [RSS](http://hackaday.libsyn.com/rss)

## 第 193 集节目预告:

#### 新闻:

*   Artemis 1 的成功使 SLS 成为有史以来最强大的火箭
*   [电子音乐节(埃利奥特经常去的地方)](https://electronica.de/en/)

#### 那是什么声音？

*   恭喜[利昂 E]猜测我是在折磨一个业余爱好伺服。
*   【埃利奥特】的[随机图像哈希脚本](https://gist.github.com/hexagon5un/472df972efd6a72c1e33fdf047a4b4e3)

#### 本周有趣的黑客:

*   [通过 WhatsApp 拨号上网](https://hackaday.com/2022/11/13/dial-up-internet-over-whatsapp/)
    *   [GitHub–adiwajshing/Baileys:轻量级全功能 WhatsApp Web +多设备 API](https://github.com/adiwajshing/Baileys)
    *   [使用 ESP8266 的 DNS 隧道](https://hackaday.com/2015/07/01/dns-tunneling-with-an-esp8266/)
    *   [DNS 隧道:通过他人的 WiFi 获取数据](https://hackaday.com/2016/08/07/getting-the-data-out-over-other-peoples-wifi/)
    *   [通过 ICMP 隧道传输 IP 流量](https://hackaday.com/2009/08/21/tunneling-ip-traffic-over-icmp/)
*   [用 Commodore 64 生成双因素认证码](https://hackaday.com/2022/11/14/generating-two-factor-authentication-codes-with-a-commodore-64/)
    *   [TOTP 算法解释–protect imus 解决方案](https://www.protectimus.com/blog/totp-algorithm-explained/)
    *   [内部双因素认证应用](https://hackaday.com/2017/10/16/inside-two-factor-authentication-apps/)
*   [用 Raspberry Pi 和 FPGA 仿真任何 ISA 卡](https://hackaday.com/2022/11/13/emulate-any-isa-card-with-a-raspberry-pi-and-an-fpga/)
    *   [Pi Pico W 做 PCMCIA，拿到这个 IBM PC110 上线](https://hackaday.com/2022/09/25/pi-pico-w-does-pcmcia-gets-this-ibm-pc110-online/)
*   [逆向工程揭示 EV 充电器有安全感](https://hackaday.com/2022/11/16/reverse-engineering-reveals-ev-charger-has-a-sense-of-security/)
    *   [欺骗智能电表在工作台上工作](https://hackaday.com/2022/03/31/tricking-a-smart-meter-into-working-on-the-bench/)
*   [一台单板电脑从一台电视机](https://hackaday.com/2022/11/14/a-single-board-computer-from-a-tv/)
    *   [主 ninakali/chip_scavenger GitHub 的 chip _ scavenger/src/scavenger](https://github.com/ninakali/chip_scavenger/tree/main/src/scavenge)
    *   [瘦客户机和智能手机取代 3D 打印机的 Raspberry Pi 和触摸屏](https://hackaday.com/2022/11/04/thin-client-and-smartphone-step-in-for-3d-printers-raspberry-pi-and-touchscreen/)
*   [3D 打印机用于轻型实验室自动化任务](https://hackaday.com/2022/11/11/3d-printer-repurposed-for-light-duty-lab-automation-tasks/)

#### 快速破解:

*   埃利奥特的选择:
    *   万圣节，骑自行车的骷髅在街上游荡
    *   [漂亮娇小的 Picolibc 动力处理器](https://hackaday.com/2022/11/14/pretty-petite-picolibc-powers-processors/)
    *   [经过训练的可穿戴式咳嗽传感器](https://hackaday.com/2022/11/15/wearable-sensor-trained-to-count-coughs/)
    *   [快速原型法测量急流中的浊度](https://hackaday.com/2022/11/15/rapid-prototyping-to-measure-turbidity-in-rapids/)
*   丹的选择:
    *   [使用谐波驱动的 DIY 赤道支架](https://hackaday.com/2022/11/10/a-diy-equatorial-mount-using-harmonic-drives/)
    *   [用调光灯泡测试器给老式电子设备通电，不那么不安全](https://hackaday.com/2022/11/13/power-up-vintage-electronics-less-unsafely-with-a-dim-bulb-tester/)
    *   [直击宝丰的内心](https://hackaday.com/2022/11/15/getting-to-the-heart-of-a-baofeng/)
    *   [自动镜头盖帮助相机拍摄太空发射](https://hackaday.com/2022/11/14/automatic-lens-cover-helps-cameras-cover-space-launches/)

#### 不能错过的文章:

*   [电动汽车销售的症结:人们仍然想要手动变速器](https://hackaday.com/2022/11/15/ev-sales-sticking-point-people-still-want-manual-transmissions/)
*   物理模型的重要性:如何不打自己的脚或其他地方
    *   [小心常识工程](https://hackaday.com/2016/10/10/beware-common-sense-engineering/)