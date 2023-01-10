# 本周安全:统一码罢工，NPM 再次，和 PS5 破解的第一步

> 原文：<https://hackaday.com/2021/11/12/this-week-in-security-unicode-strikes-npm-again-and-first-steps-to-ps5-crack/>

也许我们用 ASCII 真的更好。在我的时代，我们有 256 个字符的空间，甚至没有使用其中的 128 个，我们拿走了我们得到的。Unicode 让计算机可以使用世界上的各种语言，但也打开了一扇无形的后门。这是一个类似于上周的木马源故事的技术。虽然特洛伊木马源代码使用从右到左的编码来操作看起来不错的代码，但来自 Certitude 的这次攻击使用的 Unicode 字符看似空白，但被认为是有效的变量名。

`const { timeout,ㅤ} = req.query;`
其实是:
`const { timeout,\u3164} = req.query;`

额外的逗号可能会给你一些提示，但除非你非常熟悉一种语言，否则你可能会把它当作一种语法怪癖而不予理会，然后继续前进。再次使用相同的技巧可以让隐藏的恶意代码包含在要运行的命令列表中，从而形成一个难以发现的后门。

第二个技巧是使用“易混淆”的字符，如ǃ，U+01C3。它看起来像一个普通的感叹号，所以你不会对`if(environmentǃ=ENV_PROD){`眨一下眼睛，但在这种情况下，`environmentǃ`是一个新变量。这个开发专用代码块中的任何东西实际上都是启用的——想象一下可能会导致的混乱。

这两个都不是突破性的漏洞，但它们绝对是需要警惕的技术。作者建议，项目可以通过简单地将源代码限制为仅包含 ASCII 字符来缓解这些 Unicode 技术。这不是一个*好的*解决方案，但这是一个解决方案。

## 更多的 REvil 逮捕

显然，让自己成为整个西方世界的敌人是被捕的好方法，[REvil 成员正在继续学习](https://www.bbc.com/news/technology-59215167)。[金粉行动](https://www.europol.europa.eu/newsroom/news/five-affiliates-to-sodinokibi/revil-unplugged)今年已经逮捕了 7 人，最近一次是在罗马尼亚。这也是导致[不再勒索项目](https://www.nomoreransom.org/en/index.html)的执法努力。

## 打破 PS5

我们已经有一段时间没有听到 Fail0verflow 的任何消息了，但是他们带着针对 PS5 的新作品回来了。他们已经找到了系统的根加密密钥。这并不像最初看起来那么严重，因为在设备上运行定制软件仍然需要签名密钥。这应该允许解密设备固件，然后在引导加载程序和固件中寻找错误，这可能会导致未来的 PS5 越狱。如果你一直希望 PS5 有一个自制的场景，你的时间可能就要到了。

> 翻译:我们得到了所有(对称的)ps5 根密钥。它们都可以从软件中获得——包括每个控制台的根密钥，如果你看得够仔细的话！[https://t.co/ulbq4LOWW0](https://t.co/ulbq4LOWW0)
> 
> —失败 0 溢出(@失败 0 溢出)[2021 年 11 月 8 日](https://twitter.com/fail0verflow/status/1457526453105569793?ref_src=twsrc%5Etfw)