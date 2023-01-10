# TshWatch 帮助你更多地了解自己

> 原文：<https://hackaday.com/2022/04/03/tshwatch-helps-you-learn-more-about-yourself/>

TshWatch 是[Ivan / @pikot]的一个项目，他已经工作了两年。[Ivan]解释说他的目标是创造一种工具来帮助你了解你的身体状态。当你有压力时，当你很久没有运动时，当你的体温比平均值高时，以及后来，你自己可能没有意识到的处理模式时，要注意。这些都是商业产品所追求的深远目标。

乍一看，它可能像一个健身追踪器一样的手表，但它是一个传感器包装的记录和测量可穿戴设备——有一个漂亮的 E-Ink 屏幕和一个漂亮的橙色腕带，配备了他需要的特定功能，捕捉他想要捕捉的数据并将其发送到他拥有的服务器，并教会他一个全新的硬件世界——他与我们分享的经验。[他带领我们经历了这两年的设计过程](https://hackaday.io/project/184604-tshwatch-watch-based-on-esp32/details)——现在是第五个版本，前三个版本已经进行了试验，第四个版本有了自己的 PCB 和 E-Ink，第五个版本正在进行中，在电池放置规划方面得到了一些 CAD 帮助。应我们的要求，他也给[分享了一些近期 PCB](https://hackaday.io/project/184604/log/204435)的图片！

和传感器，它是！有一个用于心率测量的 MAX30100，一个用于计时和中断的 DS3231 RTC，一个用于非接触式皮肤温度测量的 MLX90615 IR 温度传感器，一个具有硬件加速计步器功能的 LSM6DS3C IMU，以及一个 BME680 空气质量、湿度、压力和温度传感器。尽管 ESP32 的胃口很大，但为了保持手表的低功耗，[Ivan]已经征服了 ESP32 的 ULP——一种低功耗的协处理器，能够与该项目的所有 I2C 设备进行通信。之前从未编写过 ULP 汇编，他最终[为所有相关设备](https://github.com/pikot/tsh-watch)编写了 ULP 驱动程序。因此，它在一次充电后已经可以存活超过 36 小时，他的目标是让它持续一周。

[Ivan]邀请您加入他的努力——为这样一个意义深远且近乎科幻的领域目标制造一个设备需要时间，他可以在未开发的领域使用帮助。到目前为止，他主要从事硬件和固件方面的工作，如果您想在软件、数据记录、设计/CAD 方面提供帮助，或者改进任何其他领域，请[加入 Hackaday.io 聊天室](https://hackaday.io/messages/room/302984)，看看我们能从这里走多远！硬件功能进展[正在 GitHub](https://github.com/pikot/tsh-watch/projects/1) 上追踪，还有一个俄语视频[解释第四版](https://www.youtube.com/watch?v=CB8Ftyo_vDs)的硬件架构和挑战，下面嵌入了英文字幕。

我们黑客在一个旨在帮助我们日常生活的腕戴设备中寻找什么？[在](https://hackaday.com/2019/10/07/ask-hackaday-whats-the-perfect-hacker-smart-watch/)之前，我们已经和大家讨论过了。

 [https://www.youtube.com/embed/CB8Ftyo_vDs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CB8Ftyo_vDs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

