# 本周安全:补丁星期一之谜，CentOS 8 和 CentOS 流，俄罗斯监视，和 CSRF

> 原文：<https://hackaday.com/2019/09/27/this-week-in-security-patch-monday-mysteries-centos-8-and-centos-stream-russian-surveillance-and-csrf/>

所以这周的第一件事有点神秘。微软[为 ie 浏览器发布了一个过时的补丁](https://portal.msrc.microsoft.com/en-US/security-guidance/advisory/CVE-2019-1367)。来自微软的可利用性评估表明，该漏洞正在被积极利用，但没有太多的细节可用。我们来看看都发布了哪些信息，看看有什么可以学习的。

> 脚本引擎处理 Internet Explorer 内存中对象的方式中存在一个远程代码执行漏洞。

这是一个远程代码执行漏洞，它影响 Internet Explorer，它存在于脚本引擎中，它是由于内存中的对象被错误处理而发生的。我们可以做一些猜测，但是在本文的后面，我们会得到一些其他的线索。解决方法是禁用`jscript.dll`，影响是有限的，因为`jscript9.dll`是默认的 JavaScript 引擎。`jscript.dll`显然是一个网站可以请求的遗留 JavaScript 引擎。

“Jscript”是微软称之为 JavaScript 的~~无耻复制~~实现。出于兼容性原因，较旧的`jscript.dll`似乎出现在较新版本的 Internet Explorer 中。所以老版本的 JavaScript 库如何处理对象是个问题。任何网站都可以请求这个遗留引擎，所以攻击载体基本上是无限的。

周期外补丁所隐含的紧迫性，结合围绕此补丁的其他怪异沉默，表明这 0 天可能被用于有针对性的攻击。我们希望最终会披露细节。

### CentOS 8 和 CentOS Stream

CentOS 8 于本周发布，是红帽企业版 Linux (RHEL) 8 的社区重新打包版。2014 年，红帽宣布 CentOS 正式成为红帽赞助项目。本周还公布了 CentOS Stream。

Fedora 发行版长期以来一直是即将到来的 RHEL 版本的测试平台，RHEL 8 基于 Fedora 28。CentOS Stream 将作为“中游”发行版，一个从 Fedora 获取更新的滚动版本，最终将成为未来的 RHEL/CentOS 版本。CentOS 主分发流究竟领先多远还有待观察。CentOS 的一个长期存在的问题是，当一个版本走到生命的尽头时，一些软件版本已经非常旧了。尽管安全补丁很快被移植到这些旧版本上，但还是会出现一些安全问题。例如，CentOS 7 包含 PHP 5.4，但没有安装新版本 PHP 的官方路径。WordPress 现在需要 PHP 5.6.20 作为最早支持的 PHP 版本。Red Hat 可能会对 PHP 5.4 进行修复，但这无助于 WordPress 的过时安装，它运行在最新的 CentOS 机器上。

希望 CentOS Stream 能够在 Fedora 的前沿步伐和 CentOS/RHEL 令人沮丧的缓慢步伐之间提供急需的中间地带。

### 俄罗斯的监视

一名诺基亚员工[不小心将一个公司驱动器](https://techcrunch.com/2019/09/18/russia-sorm-nokia-surveillance/)备份到了他的家庭存储设备上，这是无意中可以访问互联网的。这个硬盘上的数据是俄罗斯 SORM(T3)的详细信息，这是俄罗斯政府的窃听计划。透露的数据量惊人，1.7 太字节。密码、管理网址，甚至精确的物理位置都包括在内。信息的广度让人怀疑这是否真的是一次事故，或者这是另一次斯诺登式的数据泄露。顺便说一句，目前还不清楚被披露的窃听活动是否像斯诺登披露的那样广泛或繁重。

### PHPMyAdmin CSRF

在你的服务器上运行 PHPMyAdmin？你应该去更新一下。4.9.1 版本于 21 日周六发布，包含对 [CVE-2019-12922](https://seclists.org/fulldisclosure/2019/Sep/23) 的修复。此漏洞是跨站点请求伪造，或 CSRF。CSRF 攻击可以简单到一个网站上的图像链接，链接到另一个网站，并在第二个网站上触发一个操作。让我们看看 PHPMyAdmin 的例子:

```

img src="
http://server/phpmyadmin/setup/index.php?page=servers&mode=remove&id=1";
style="display:none;"

```

一个隐藏的图像实际上会触发一个 HTTP GET 请求，请求服务器的页面，并试图删除第一个条目。如果用户登录到链接指向的 PHPMyAdmin 服务器，命令将自动完成。这就是 HTTP GET 请求不应该改变状态，而应该只检索信息的原因之一。以这种方式生成 HTTP POST 消息要困难得多，尽管并非不可能。