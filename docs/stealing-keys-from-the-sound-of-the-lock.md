# 从锁的声音中偷钥匙

> 原文：<https://hackaday.com/2020/08/22/stealing-keys-from-the-sound-of-the-lock/>

如果你聪明的话，你不会在几分钟内把你家的钥匙交给一个陌生人，对吗？但是每次你用你的钥匙开门时，你可能正在广播攻击者制作他们自己的副本所需要的一切。原来这一切都是因为钥匙插进锁里的声音。

新加坡的研究人员报告说，分析钥匙滑过销子时的金属咔哒声给他们提供了 3D 打印工作钥匙所需的数据。《T2 日报》发表的研究是收费的，但[的合著者【Soundarya Ramesh 的】网站](https://soundaryaramesh.github.io/projects/)上有一份副本，概述了用于将锁销上钥匙齿的卡嗒声解码成可用数据的算法。

攻击不需要特殊的硬件。该团队使用普通智能手机的音频捕捉。虽然在受害者插入钥匙时将手机靠近锁可能会有问题，但不难想象被黑客攻击的手机或智能门铃会为攻击者拾取音频。远程麦克风或隐藏的窃听器也是可能的。

当然，还有一些实际问题。一些键有一个平台，导致一些点击跳过，所以算法必须处理这一点。听起来最终的结果是少量的密钥可能性，而不仅仅是集中在一个密钥上，但是即使你必须随身携带三四个密钥才能进入，这仍然是一个非常可行的漏洞。

下一步是找到合适的防御。我们听说软化插销可能会减少咔哒声，但我们想知道是否可以在插入钥匙时放一些故意发出响亮咔哒声的东西来掩盖插销的柔和咔哒声。

虽然录音很好，但有时一张[图片甚至更好](https://hackaday.com/2015/09/18/dear-tsa-this-is-why-you-shouldnt-post-pictures-of-your-keys-online/)。当然，如果你想去老学校，你可以 [3D 打印你的开锁工具](https://hackaday.com/2014/12/01/3d-printing-lock-picks/)。

 [https://www.youtube.com/embed/bxyAa_txM34?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bxyAa_txM34?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

