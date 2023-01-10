# 反恐精英获得 RGB LED 待遇

> 原文：<https://hackaday.com/2020/02/20/counter-strike-gets-the-rgb-led-treatment/>

受电子竞技活动中过度使用的舞台灯光和烟火的启发，[汉斯·彼得]开始为他的个人*反恐精英:全球攻势*会议开发一个缩小版(没有火焰)。这看起来像是完成这样的事情会涉及到入侵游戏引擎，但事实证明，Valve 足够善良地[实现了一个游戏状态 API，这使得它相对容易](http://embryonic.dk/wordpress/?p=867)。

根据文档， *CS:GO* 客户端可以被配置为定期向 HTTP 服务器发送状态信息。它甚至提供了在 Node.js 中实现简单状态服务器的示例代码，Hans 通过添加一些分析当前游戏状态的条件语句来适应这个项目。

这些功能向连接的 Arduino 发出串行命令，Arduino 进而控制 WS2812B LEDs。Arduino 代码获取 HTTP 服务器提供的信息，并将其分解为不同条件下的各种照明例程，例如赢和输。但是当炸弹被激活时，事情才真正开始运转。

[Hans]想要使闪烁的 led 与游戏中炸弹发出的嘟嘟声同步，但是 API 没有提供足够粒度的数据。因此，他录下了炸弹启动序列的音频，使用 Audacity 精确记录哔哔声的时间，并在他的 Arduino 代码中实现了该序列。在休息后的视频中，你可以看到同步并不完美，但在激烈的战斗中，这一点已经足够接近了。

鉴于《反恐精英》在黑客和游戏玩家心中的特殊地位，人们仍在寻找独特的游戏体验也就不足为奇了。

 [https://www.youtube.com/embed/2S-LiZb1UwQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2S-LiZb1UwQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

