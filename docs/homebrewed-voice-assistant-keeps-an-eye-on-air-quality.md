# 自制语音助手关注空气质量

> 原文：<https://hackaday.com/2021/11/05/homebrewed-voice-assistant-keeps-an-eye-on-air-quality/>

语音助手现在可以从各种各样的公司获得，但是，[7402]不喜欢这些设备出于潜在的邪恶目的将数据发送到云的想法。因此，目标变成了建立一个完全离线工作的家庭语音助手，这正是[7402]所实现的。

与商业竞争对手相比，该系统的目标有限。[7402]非常乐意处理有限的理解词汇，作为隐私的交换。这一切都是围绕一个运行 Julius 语音识别库的 Raspberry Pi Zero 构建的。超声波传感器仅用于在人倚靠并直接对系统讲话时激活设备。

功能包括报告天气，开关灯，并建议用户从当地政府的空气质量读数。通过文本到语音以及闪烁的 led 向用户提供反馈。后者用于创建一个古怪的、复古的“思考”动画，以指示系统正在处理，并且确实听到了口头命令。

这是一个简洁的构建，涵盖了商业云设备能够实现的大部分优点。额外的好处是，不需要智能手机应用程序，私营公司也不会影响系统的功能，因为它不依赖外部服务器来运行。

我们以前也见过类似的版本，比如这个 GlaDOS 主题的语音助手。休息后的视频。

[https://player.vimeo.com/video/640926395](https://player.vimeo.com/video/640926395)