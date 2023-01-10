# 使用 AprilTags 让客人打开你的前门

> 原文：<https://hackaday.com/2022/07/08/use-apriltags-to-let-guests-open-your-front-gate/>

[Herb Peyerl]是机器人团队的一员，在他的机器人工作中，了解了 AprilTags 即使是原始的机器视觉也很容易识别的类似 QR 码的可打印图案。后来，当考虑如何让他的客人通过他家的前门时，AprilTags 变成了一个绝妙的解决方案。现在，他需要做的就是给他的客人发一张合适的 AprilTag 的照片，他们可以用智能手机将照片展示在他家前门的摄像头前。

为此，他使用了一个 OpenMV 板——由于它有各种各样的可用库，AprilTag 识别已经嵌入其中，整个脚本只有一百行 MicroPython。一个旧的监控摄像头放弃了它的圆顶形外壳，现在 OpenMV 董事会正在他的物业前门前的一个柱子上履行访客访问职责。他与我们分享了代码，并表示出于安全原因，他个人正在运行一个稍加修改的版本——反正不是一个随机的窃贼可能会偶然发现这个帖子。此外，它看起来像一个窃贼将很容易跳过大门，而不需要任何安全旁路，这种黑客的便利优势是不可否认的。

然而，不太可能的是，一个窃贼正在读这封信，不要难过。我们正好也有一堆黑客适合你。安全系统少得多，从[建造 RFID 钥匙链](https://hackaday.com/2022/06/17/your-buildings-rfid-access-tags-might-be-really-insecure/)到[社区门禁系统](https://hackaday.com/2014/07/14/how-to-hack-your-way-into-your-own-gated-community/)，有时[你需要的只是 12 V 电池。](https://hackaday.com/2020/07/01/pop-open-your-neighbors-front-door-with-12-volts/)如果你不喜欢入室盗窃，那也没关系——我们之前讨论过其他访客访问黑客，例如，[这款 ESP8266 驱动的。](https://hackaday.com/2017/06/04/esp8266-mqtt-remote-gate-entry/)