# 为了乐趣和利益窃听卫星

> 原文：<https://hackaday.com/2020/08/20/eavesdropping-on-satellites-for-fun-and-profit/>

地球同步卫星从赤道上空 36，000 公里的高处环绕地球，是非常有用的设备。根据它们停放的位置，它们可以一次控制全球三分之一的视野，这使它们成为完美的通信中继站。但是，正如[詹姆斯·帕沃尔]在他的 DEF CON 安全模式演讲中指出的那样，地球同步卫星通信链路通常远不安全。

詹姆斯，哲学博士。牛津大学系统安全专业的学生说，他的利用依赖于卫星下行信号覆盖的广阔区域，再加上事后才想到的安全性，如果卫星服务提供商甚至想到过的话。这种懒散的方法让他只使用一个普通的数字卫星电视天线和一个 PC 调谐器卡——那些现成的东西，你真的要花 300 多美元才能买到——来获取敏感信息。

虽然将卫星的数字信号解码成可解析的东西可以在商业应用中完成，但[James]和他的同事们开发了一个定制工具 GSExtract，从高空传来的经常有噪声的信号中提取数据。该设置返回了惊人的大量信息，如海事运营商将船员的护照信息从船上转发到岸上，地中海游轮上的销售点终端信息，以及喷气式客机上的机上娱乐系统。最后一个例子尤其令人震惊，因为它揭示了专用于保持乘客满意的系统与驾驶舱中的系统之间的可利用联系，而这显然不应该是这样的。

我们发现[詹姆斯]对卫星通信中这些弱点的见解非常有趣，值得花 45 分钟来观看下面的视频，也许可以亲自尝试这些漏洞，这相当于[边信道攻击](https://hackaday.com/2020/03/09/fear-of-potato-chips-samy-kamkars-side-channel-attack-roundup/)。

 [https://www.youtube.com/embed/ku0Q_Wey4K0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ku0Q_Wey4K0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

