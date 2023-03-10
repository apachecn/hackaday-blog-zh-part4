# 惊人的 STARGᐰTE 与 DHD 和无限镜像虫洞

> 原文：<https://hackaday.com/2021/03/09/amazing-starg%e1%90%b0te-with-dhd-and-infinity-mirror-wormhole/>

自 1994 年以来,《星际之门宇宙》系列已经衍生出了许多电影、连续剧、书籍、漫画和游戏，并且一直是科幻迷们的最爱。道具制造商和黑客经常尝试建造他们自己的星际之门复制品——爱因斯坦-罗森桥入口，允许在两个遥远的地方之间进行几乎瞬间的旅行。建造一个看起来真实的道具需要很多对细节的关注，而【克里斯蒂安】的[星际之门项目](https://thestargateproject.com/)是一个非常好的入口再现。

[Kristian]的星际之门大部分是 3D 打印的，有一个符号环，带有人字形，当接合时会锁定并点亮。当拨入正确的地址时，通过使用 122 个 RGB 发光二极管的无限镜像效应，虫洞就建立了。呼叫总部设备(DHD)是原始基座形计算机的复制品，有两组同心的 19 个按钮和一个中央激活按钮。

星际之门环由多个 3D 打印片段组装而成，直径 390 毫米。七个人字纹沿着 3D 打印的齿条齿轮移动，由齿轮传动的微型马达驱动。符号环由单独的 NEMA14 步进电机驱动。带有三个背负式马达帽的树莓皮控制各种马达和发光二极管。USB 声卡和有源扬声器在拨号时提供音频效果。一旦蠕虫洞建立，随机播放音频片段。虫洞维持 38 分钟，之后星际之门关闭。

呼叫总部设备是围绕一个定制的圆形 PCB 构建的，该 PCB 包含键盘按钮、led 和 ATmega 32u4 微控制器，该微控制器通过 USB 连接到 Raspberry Pi。39 个 led 是 APA102C 的，因此它们只需要两个 GPIO 引脚。对于键盘，四组九个按钮和另一组三个按钮通过电阻梯连接到模拟 GPIO。这允许所有 39 个按钮通过 5 个模拟输入连接，可能是为了简化 PCB 走线布局。背光按钮键帽分为两部分印刷。半透明的底部覆盖着不透明的符号帽。

让这样的道具看起来像真的一样需要花费很多精力来绘制各个部分，这显示在[Kristian]的最终结果中，一直到星际之门所在的石台。我们希望看到的一个改进是无线 DHD，就像它应该有的那样。这样做应该不会太难，失去星际之门和 DHD 之间的 USB 系绳将是这个惊人项目的一个巨大升级。休息之后看看视频，在[Kristian]的项目页面上还有更多。

如果你是这个系列的粉丝，那么令人惊叹的令人垂涎的星际之门 Horus 头盔是这个星际之门的一个很好的伙伴项目。

 [https://www.youtube.com/embed/EnIeONEcSGc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EnIeONEcSGc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 <https://thestargateproject.com/wp-content/uploads/2021/01/DHD-dialing_404.mp4?_=1>

[https://thestargateproject.com/wp-content/uploads/2021/01/DHD-dialing_404.mp4](https://thestargateproject.com/wp-content/uploads/2021/01/DHD-dialing_404.mp4)

谢谢你的提示，[马丁·舒斯特]