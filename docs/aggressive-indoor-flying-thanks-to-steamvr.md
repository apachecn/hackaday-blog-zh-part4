# 由于 SteamVR，室内飞行更具侵略性

> 原文：<https://hackaday.com/2020/06/30/aggressive-indoor-flying-thanks-to-steamvr/>

随着封锁条例席卷全球，许多人发现自己在室内度过了太多时间，却没有太多事情可做。[彼得·霍尔]就是这样一个人，对飞行四轴飞行器情有独钟。与大自然无缘，他转而努力寻找一种方式，让在室内飞行成为一种更令人兴奋的体验。我们可以说他成功了。

该设置涉及使用 SteamVR 虚拟现实跟踪器来监控房间内四轴飞行器的位置。然后，这些数据被高速传回四轴飞行器，为自动驾驶仪提供快速、准确的数据来执行机动操作。PyOpenVR 用于进行运动跟踪，并与 MAVProxy 结合使用，通过 MAVLink 将信息发送回直升机的 ArduPilot。

虽然这样的设置可以用来简单地阻止直升机撞上东西，但[彼得]不喜欢半途而废。相反，他充分利用了该系统的能力，[使直升机能够在一个难以置信的小空间内积极飞行](https://youtu.be/m5bwoiHsn8M)。

这是一个令人印象深刻的设置，我们确信它可以进一步应用于那些探索无人机在室内使用的人。我们也看到 MAVLink 被用于邪恶的目的。休息后的视频。

 [https://www.youtube.com/embed/m5bwoiHsn8M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/m5bwoiHsn8M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

