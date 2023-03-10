# 本周安全:Npm 定时泄漏，西门子万能钥匙，和 PHP 在巴布亚新几内亚

> 原文：<https://hackaday.com/2022/10/14/this-week-in-security-npm-timing-leak-siemens-universal-key-and-php-in-png/>

首先是来自[Aqua Nautilus]研究团队的一些聪明的[魔法，他们发现了一个泄露私有 npm 包信息的定时攻击。设置是这样的，npm 托管公共和私有 node.js 包。公共包对每个人都是可用的，但是私有包是“限定范围的”，这意味着它们位于私有名称空间“@owner/packagename”中，一般公众是无法访问的。试图访问包会导致 HTTP 404 错误，这与试图拉一个不存在的包是同样的错误。](https://blog.aquasec.com/private-packages-disclosed-via-timing-attack-on-npm)

[![](img/4c47f3544f3d7deee51295056f16349c.png)](https://hackaday.com/wp-content/uploads/2022/10/response_time.png) 
聪明的一点是不断尝试，并真正注意反应。使用 npm 的 API 连续五次请求目标包的信息。如果包名没有被使用，那么所有五个请求都将花费预期的时间。该请求到达服务的后端，执行查找，然后得到响应。另一方面，如果您的目标包确实存在，但是是私有的，那么第一个请求返回时会有预期的延迟，其他四个请求会立即返回。似乎 npm 具有可以缓存私有包的 404 响应的前端。这种响应时间的差异意味着您可以在私有范围内映射出给定组织使用的私有包名称。

现在这一切都非常有趣，但当与域名抢注和[依赖性混淆](https://medium.com/@alex.birsan/dependency-confusion-4a5d60fec610)问题结合起来时，它变成了一种似是而非的攻击。这些攻击是实现同一目标的两种方法，让 node.js 部署运行恶意包，而不是开发人员想要的合法包。一种依赖于打字错误，但是依赖混淆仅仅依赖于开发者没有明确定义包的范围。

## 西门子把钥匙留在了点火器上

西门子在近 10 年前发布了 TIA 门户网站的第 12 版，此次更新在门户网站与其 SIMATIC S7-1200 和 S7-1500 产品之间增加了非对称加密功能。简单地说，他们的工业控制器开始使用 HTTPS 与控制器软件对话。这是一件好事。不幸的是，用于 HTTPS 连接的私钥存在于控制器硬件中，并且每个发货的单元都有相同的密钥。

真正有趣的是 Claroty 的团队是如何发现这一切的。工业控制器是用一种特定的高级语言编程的，这种语言严格用于自动化逻辑。指针、内存管理和其他常见的易受攻击的向量在这里没有出现。这些程序被编译成定制的字节码，在控制器上的受控环境中运行。因此，很自然地，我们的研究人员对字节码进行了逆向工程，并编写了他们自己的编译器，以访问那些底层特性。击败内置于该环境中的安全控制仍然是一个挑战，但他们最终发现了一个可以将指针设置为任意值的函数，允许内核读写。包括读取万能钥匙。

这就把我们带到了第一个真正的攻击，拥有这个秘密但共享的密钥。根据配置的不同，有时可以下载配置 blob 而不进行身份验证。该数据集中包含的一项是加密的密码散列，它是使用——您猜对了——通用密钥加密的。有了密钥，攻击者就可以下载哈希、解密，然后使用哈希进行身份验证。

然后，有了 HTTPS 证书的秘密密钥，就可以进行人们能想到的所有正常的恶作剧:捕获流量并解密，或者进行中间人攻击。最新的固件和门户更新已经修复了这些问题，[西门子已经发布公告](https://cert-portal.siemens.com/productcert/html/ssa-568427.html)承认这些问题。参见下面的视频，了解逃离矩阵并在这些机器上真正执行代码的第一手故事。

(Hackaday 的母公司 Supplyframe 归西门子所有。)

 [https://www.youtube.com/embed/r-dmxU1gEl0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/r-dmxU1gEl0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## Valid PNG，Valid PHP

一个文件作为多种完全不同的文件格式是有效的，这总有一些奇怪的有趣之处。在这种情况下，[PNG 文件也是有效的 PHP](https://www.synacktiv.com/publications/persistent-php-payloads-in-pngs-how-to-inject-php-code-in-an-image-and-keep-it-there.html) 。这里的安全角度是，很多网站允许你上传 png，然后查看。如果 PNG 实际上也可以是一个 PHP 文件，你就有了一个即时的 webshell。现在可能有一些不安全的站点，在那里上传一个脚本很简单，但是许多上传者库至少会检查文件对于指定的 mimetype 是否有效。简单地说，它必须是一个有效的 PNG `if set to `image/png`。但这就够了吗？`

 `PNG 文件可以包含注释。当 web 服务器提供一个也包含二进制 PNG 数据的`.php`文件时，它会做什么？在许多情况下，它像对待任何其他文件一样对待它，发送原始数据直到它找到一个`<?php`标记，在这里它可能只是开始执行 PHP 脚本。下一个问题是，如何创建这样一个文件，使得 PHP 脚本在压缩、调整大小和其他净化步骤中保持不变？讨论的第一种方法是使用文本块，它通常用于存储标题、作者等。在许多情况下，嵌入文本的这些位将通过任何修改保持不变。

另一种更难的方法是将文本作为图像数据直接嵌入。有一个 PLTE 块，在那里可以定义定制的调色板条目。这些可以是任何值，但长度必须是 3 的倍数，最多 768 个字符。更难的是使用[实际的 IDAT 块](https://www.idontplaydarts.com/2012/06/encoding-web-shells-in-png-idat-chunks/)，也就是实际的有效像素数据。这的确是很深的魔法。

## zone minder——情况可能会更糟

这是一个切中要害的问题，因为它是我推荐的一个项目中的三个漏洞之一，我偶尔会为它投代码。[IT 战壕]在 30 日联系了这个项目，提出了三个漏洞,这些漏洞放在一起可能会非常糟糕。首先是日志注入漏洞，web 用户可以将任意数据推入 ZM 日志，没有速率限制。需要摄像机停止记录吗？用日志消息填满驱动器。消息本身和发送它的组件都可以任意设置。

接下来是 CSRF 旁路。跨站点请求伪造是一种攻击，在这种攻击中，最终用户的浏览器仅仅通过发出 HTTP 请求就采取了用户不希望的操作。ZM 使用 CSRF 令牌来防止此类问题，这是一个由 web 服务提供的随机令牌，必须包含在任何 POST 请求中。ZM 的绕过之处在于，像删除录音这样的一些操作可以作为 GET 请求来执行，这不需要令牌。哎呦。

最后一个问题可能是最糟糕的，因为它是一个跨站点脚本(XSS)问题。日志注入问题也支持这一点，因为“文件”字段可以包含任意 HTML 代码，包括脚本标记。将这三个问题放在一起，具有仅查看权限的用户可以插入删除或禁用命令，该命令将在管理员查看日志时触发。这很糟糕，但至少这不是一个预授权漏洞。1.36.27 修复，7 号发布。如果您碰巧停留在 1.34 系列的版本中，这几个其他问题是突出的，并且没有为该废弃版本计划进一步的版本。感谢【壕 IT】的发现和举报！

## 微软不断送出的礼物

还记得[Exchange 0 天](https://gteltsc.vn/blog/warning-new-attack-campaign-utilized-a-new-0day-rce-vulnerability-on-microsoft-exchange-server-12715.html)吗，它是自动发现端点的一个老问题的一种变通方法？嗯，它仍然没有被修补，并且[推荐的解决方法已经更新了多次，因为它们已经被轻易绕过](https://msrc-blog.microsoft.com/2022/09/29/customer-guidance-for-reported-zero-day-vulnerabilities-in-microsoft-exchange-server/)。现在可能是时候拔掉自动发现的插头，并在您使用它时阻止所有外部访问 IIS 了。

## Python 和用户域执行

最后一个红队快速提示。您已经在服务器上弹出了 shell，并且想要引入一些工具来开始探索环境。Root 是以只读方式挂载的，并且您的临时目录都是挂载的`noexec`。如何将二进制文件加载到系统中并运行它？如果安装了 Python，那么你可以使用 [`ulexecve`](https://github.com/anvilsecure/ulexecve/) 。[【文森特·伯格】写了这个工具并有了故事](https://www.anvilsecure.com/blog/userland-execution-of-binaries-directly-from-python.html)。它的工作方式同样令人印象深刻，因为它下载并解析给定的二进制文件，手动将其加载到内存中并生成跳转缓冲区。最后，它将代码执行跳转到新的二进制文件中，该文件永远不需要写入磁盘。棘手。`