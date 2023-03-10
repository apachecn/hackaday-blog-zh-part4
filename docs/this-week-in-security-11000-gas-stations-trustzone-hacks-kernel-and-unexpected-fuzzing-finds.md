# 本周安全:11，000 个加油站，TrustZone 黑客内核，以及意想不到的模糊发现

> 原文：<https://hackaday.com/2022/09/16/this-week-in-security-11000-gas-stations-trustzone-hacks-kernel-and-unexpected-fuzzing-finds/>

自动油量计(ATG)是一项很棒的技术，几乎每个加油站都有。他们跟踪燃料水平、温度和其他信息，有时还会连接到空间站的自动化系统。问题是，一堆这样的设备正在监听互联网上的端口 10001，而[其中一些似乎配置错误](https://medium.com/@RoseSecurity/a-theoretically-devastating-cyber-attack-on-americas-gas-stations-ff1d9bbaf1)。多少？先说比较简单的问题，10001 端口开了多少个 IP？ [Masscan](https://github.com/robertdavidgraham/masscan) 是最好的工具之一，【RoseSecurity】发现了超过 85000 个监听设备。开放港口只是一个开始。其中有多少是用字符串`In-Tank Inventory Reports`来响应连接的？截至今年 8 月，Shodan 报告了 11，113 个 IP。[RoseSecurity]编写了一个简单的 Python 脚本，检查每个监听 IP 是否有匹配的设备数量。可怕的是，这种检查是通过发送一个`Get In-Tank Inventory Report`命令来完成的，并检查是否有良好的响应。好像是 11K 个系统，连接到互联网，没有认证。会出什么问题呢？

## 棘手的 JavaScript 技巧

[Gareth Heyes]整理了一本令人印象深刻的 JavaScript 古怪指南。怪异可能是轻描淡写，所以抓紧了。这篇文章的第一部分来自 2016 年，[展示了一种在没有任何括号或字母数字字符的情况下运行 JS 代码的技术](https://portswigger.net/research/executing-non-alphanumeric-javascript-without-parenthesis)。`+!+[]`是一个写 1 的巧妙方法。怎么会？这段代码的神奇之处在于`+`操作符有一个一元用法。我们通常在像`1+2`这样的语句中使用它，其中操作符接受两个输入并对它们求和。一元版本只返回对象的数字表示。`+2`等于 2，`+"2"`等于 2。打开你浏览器的 JS 控制台，试一试。所以在上面的例子中，方括号定义了一个空数组，加号转换成一个数字 0。！是 not 运算符，它会自动将值转换为布尔值(false)，然后进行反转(true)。然后我们将布尔值数值化为 1。得到一个 0 和一个 1 需要做很多工作，但是有了这些，加法可以得到任何其他的数。

下一个技巧是`[][[]]`返回 undefined。这实际上是一个空数组作为数组的索引，因此是未定义的。现在有趣的是`[][[]]+[]`使用了加法运算符，返回的是字符串“undefined”。需要一个额外的技巧来使它可用，我们把这个字符串放在一个数组中，然后引用该数组的第一个索引:`[[][[]]+[]][+[]]`。所有这些使我们能够像对待数组一样对待这个字符串，并使用索引来获取单个字母。由于我们有“未定义”的工作，我们可以把“查找”放在一起。而且由于“find”是一个函数，执行这个不带括号的语句会返回“function find(){[本机代码] }”。使用相同的技巧，你就有更多的角色可以使用。为了实际执行这个拼凑起来的字符串，我们可以使用一个模板文本来获得实际的执行，`Function alert(1)`。现在，在我们讨论新的帖子之前，这个令人费解的 JS 有什么意义呢？跨站点脚本执行(XSS)。如果您可以将足够多的 JS 代码偷偷放入网站的正确位置，当另一个用户查看结果时，您就可以在他们的浏览器中运行您的代码。网站是为了防止这种情况而精心构建的，但像这样的技巧可以用来绕过这些保护。

所以，这就把我们带到了最近的帖子，[第七种不用括号调用 JavaScript 函数的方法](https://portswigger.net/research/the-seventh-way-to-call-a-javascript-function-without-parentheses)。这里是带有[模板文字](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)作为参数的模板函数。看一看`x`x${y}x``。模板文本中的${}构造将运行花括号内的表达式，并将结果代入字符串。这段代码使用一个标记函数做了一些别的事情。有趣的是，当一个标记函数以这种方式被调用时，它获得字符串作为它的第一个参数，但是表达式的原始结果作为它的剩余参数。这也可以用来运行代码。最后看起来像`[].sort.call`${alert}1337``。目前这还是一件新鲜事，但是将来看到混淆的 JS 使用这些技术，我不会感到特别惊讶。

## 通过 TrustZone 进行 Android 黑客攻击

[Tamir Zahavi-Brunner]偶然发现了一个聪明的 Android 漏洞，使用高通可信执行环境(QTEE)来破坏运行的内核。你可能还会看到这个叫做 QSEE，这是该技术的一个老名字。这是标准的可信执行——一个独立的内核运行在与 Linux 内核并行的硬件上，这两个内核使用 qseecom Linux 内核模块进行通信。该模块发送数据和指针的序列化组合，由可信执行端获取，并由 trustlet 执行。想法是 trustlet 将结果写回给定的指针，Android 进程可以读回它。问题是这些共享缓冲区允许重叠，trustlet 最终会在另一个缓冲区的头上写入任意数据。这种内存损坏总是不好的，并且经常被利用。在这里，它可以用于将另一个 trustlet 的输出重定向到内存中的任意位置，就像覆盖内核函数一样。

这里的可取之处是，沙盒应用程序不被允许直接与 qseecom 模块对话，因此需要第二次利用。另一方面，一旦获得许可，就会导致可重复的内核漏洞利用。该漏洞是在 2020 年 10 月报告的，高通直到 2021 年 9 月才修补，这本身就令人担忧。

## 比特和字节

让我们加密即将[按下标有“证书撤销列表](https://letsencrypt.org/2022/09/07/new-life-for-crls.html)的红色大按钮。这项新功能是修复严重损坏的证书撤销过程的一部分。他们真的在努力做这种未来的证明，甚至问一个最糟糕的情况会怎样。如果他们必须撤销当前的所有证书，结果列表将会有 8 GB 重，所以主列表被分成了 128 个片段。

微软团队可以作为一个通信渠道[运行一个远程 shell，所有这些都是通过使用 gif，因此 GIFShell](https://medium.com/@bobbyrsec/gifshell-covert-attack-chain-and-c2-utilizing-microsoft-teams-gifs-1618c4e64ed7) 。这不是利用来获得对机器的控制，而是一系列七个弱点，使隐形通道成为可能。微软认为这是“伟大的研究”，但不认为这是一个漏洞。

谷歌的 OSS-模糊系统对大约 700 个被称为关键的项目进行自动模糊处理。最近发现 TinyGLTF 中的一个 bug，CVE-2022-3008，一个命令注入漏洞。值得注意的是——一个 fuzzing 项目发现了一个逻辑缺陷，它与内存损坏无关。谷歌正在努力扩大他们的 fuzzing 项目可以发现的问题种类，甚至支付了 11，337 美元用于帮助发现漏洞。

FishPig 经历了艰难的几个月，8 月份一名[未知攻击者入侵了他们的分发服务器。他们为在 WordPress 站点上运行 Magento 2 提供了一个付费的集成模块，据估计有超过 200，000 个站点使用这些模块。这些模块在入侵后被分发，包括一个秘密后门。到目前为止，还没有观察到任何控制后门的人采取恶意行动，但](https://arstechnica.com/information-technology/2022/09/breach-of-software-maker-used-to-backdoor-as-many-as-200000-servers/)[仍然建议 FishPig 用户扫描问题。](https://fishpig.co.uk/security-announcements/#X20220913)