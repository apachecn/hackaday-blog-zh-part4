# 本周的安全:OpenSSH、Git 和 NGINX 0-day

> 原文：<https://hackaday.com/2022/04/15/this-week-in-security-openssh-git-and-sort-of-nginx-0-day/>

OpenSSH 已经[发布了他们的 9.0 版本](https://www.openssh.com/releasenotes.html)，它包含了一对安全变化。与我们在这里讨论的大多数版本不同，这个版本有安全加固来防止问题，而不是对当前问题的紧急修复。首先，古老的 scp/rcp 协议已经被删除。你的`scp`命令现在将使用 SFTP。更有趣的安全变化是新的默认密钥交换，NTRU 算法。NTRU 被认为是量子力学的。

快速入门:现代加密依赖于陷门函数——在一个方向上很容易执行的计算，但很难逆转。第一个这样的方案是 Diffie-Hellman 密钥交换，它使用大素数相乘。乘法很容易，但分解结果是一个非常困难的问题。如果有捷径可以让保理业务变得更容易，Diffie-Hellman 的安全性就会受损。这样的捷径理论上已经在 Shor 的算法中找到了。(理论上，在包括椭圆曲线在内的其他方案中也发现了类似的缺陷。)

 [https://www.youtube.com/embed/lvTqbM5Dq4Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lvTqbM5Dq4Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Shor 的算法其实挺巧妙的。上面的视频比我解释得好得多，但关键是它依赖于一个可以内置到量子计算机中的功能，因此可以一次性处理许多可能的解决方案，不正确的解决方案相互抵消，只留下一个可能是正确的输出。问题是尖端的量子计算机已经设法将 21 分解成它的质因数。提醒你，不是 21 位数，而是 21。

我们离承诺的量子计算密码启示录还有很长的路要走。那么，为什么项目要实施抗量子协议呢？“现在捕获，以后解密”的场景。因为密钥交换协议可能会受到攻击，所以现在可以捕获整个 SSH 会话，一旦有量子计算机打破握手，整个会话就可以离线解密。谁也说不准一家公司或一个民族国家要多久才能拥有一台实用的量子计算机。即使再过 20 年，一些数据仍然是敏感的，可能会被解密。

NTRU 使用[点阵上的矢量数学](https://www.youtube.com/watch?v=37Ri1jpl5p8)作为单向函数，因为它仍然可以很好地抵御经典计算机，而且还没有发现针对它的量子加速攻击。以防 NTRU 以一种不可预见的方式变得脆弱，它将与以前的标准 x25519(一种椭圆曲线解决方案)相结合。

## NSO 瞄准欧盟？

NSO 集团的软件再次出现在尴尬的地方。这一次，ForcedEntry 似乎被用来试图对欧盟委员会的官员妥协。NSO 否认了这一指控，声称他们的工具不可能对所报道的企图负责。请记住，NSO 出售其间谍软件给多个政府将很少监督这些政府如何处理它。应该明确的是，这几乎肯定不是以色列政府，甚至也不是 NSO 直接针对欧盟的。一些报道让这一点变得有些模糊。有趣的是，受影响的委员不是被欧盟的专业人士发现，而是被苹果通过电子邮件通知的。

## Git 问题

Git for Windows 刚刚发布了一轮更新来修复 [CVE-2022-24765](https://nvd.nist.gov/vuln/detail/CVE-2022-24765) 。这里的问题是 Windows 驱动器根目录下的`.git`文件夹被视为合法 Git 目录之外的任何 Git 操作的有效配置。危险在于另一个用户或恶意程序可以创建这个目录，下次运行 Git 时，可以通过 config 触发任意命令。

[![](img/276ef92f0093102feeb25b95bc1c142a.png)](https://hackaday.com/wp-content/uploads/2022/04/NotGitBleed2Color.png)

说到 Git，有一个有趣的数据泄露刚刚公布，[notgitbleade](https://www.notgitbleed.com/)。奇怪的名字？[Aaron Devaney]和[Will Deane]在 2021 年发现了这个问题，并选择“GitBleed”作为他们的漏洞名称，但另一组研究人员用[一个类似但不同的问题](https://wwws.nightwatchcybersecurity.com/2022/02/11/gitbleed/)击败了他们。不是那些太把自己当回事的人，选择了半开玩笑的方式。

实际的问题是开发人员和我们在做 git 推送时的肌肉记忆。提交，推送到 Github，输入用户名和密码。然而，当进行第一次提交时，Git 会询问您的姓名和电子邮件。如果不注意，给它一个用户名和密码太容易了。当然，我听到你嘲笑，不超过一小撮开发人员会犯这种错误。根据他们的发现推断，这些年来，超过 50，000 个密码在提交元数据中泄露。

## 社会域名抢注和接管

我们已经讨论过域/子域接管，在这种情况下，一个域已被允许过期，但仍被认为是活跃的。来自[Utku Sen] 的一款[新工具可以让你寻找同样容易受到攻击的社交媒体链接。想象一下，我打算链接到我的 Twitter 账户，](https://github.com/utkusen/socialhunter)[让你们跟着我去那里](https://twitter.com/jp_bennett)，但是我打错了链接。如果在拼写错误的链接处还没有帐户，有人可以创建一个并假装是我。作为证据，甚至有一篇我链接到(假)账户的文章。哎呦！这就是 socialhunter 的用武之地。把它指向一个网址，它就会寻找虚假的社交媒体链接。显然，许多 bug bounty 程序会将此类错别字视为有效问题，所以开始工作吧！

## 亚马逊 RDS 抢劫案

一些漏洞发现读起来就像一部老式的恶作剧电影，而[就是其中之一](https://blog.lightspin.io/aws-rds-critical-security-vulnerability)。Lightspin 的研究人员正在研究亚马逊关系数据库服务(RDS)，这是亚马逊的云数据库产品。RDS 数据库引擎的一个选项是 PostgreSQL。有一些方法可以避开 SQL 引擎并在机器上运行代码，但是明显的漏洞被堵住了:你没有真正的超级用户权限，不能加载不可信的语言扩展，等等。有一些可用的扩展，`log_fwd`是有趣的一个。这使您可以将日志文件作为外部表来访问，这对调试非常有用。如果您可以调查日志文件，那么您也可以用这个技巧检查其他文件吗？研究人员尝试过，试图导入`../../../../../etc/passwd`。这自然会引发一个错误。生活不可能那么容易。

几个请求之后，很明显有一个模式匹配验证器函数正在阻塞路径遍历。PostgreSQL 使用外部数据包装器来访问外部数据，就像这样，并且它们包括验证器函数作为可选特性。可选的，你可以在运行时禁用它们。那么，禁用验证器，然后尝试访问`passwd`文件？财源滚滚。

PostgreSQL 守护进程可以读取的文件系统上的任何文件，用户也可以读取。在寻找任何有趣的东西后，出现了术语`grover`。在一系列链接的配置文件之后，最终发现了一个 API 凭证。这个凭证允许作为一个内部 AWS 服务`csd-grover-role`访问 AWS。在这一点上，研究人员已经揭开了面纱，并在 AWS 后端发挥作用。他们称之为一天的工作，并将发现提交给亚马逊。AWS 安全部门验证了这个漏洞，确认它在过去没有被利用，并且奇怪地对`grover`服务是什么守口如瓶。不管怎样，错误已经修复，这是一个逃离 AWS 沙箱的有趣故事。

## NGINX 0 天—也许

就在本专栏即将付印之际，有传言称 [NGINX 可能会在野外利用](https://therecord.media/f5-investigating-reports-of-nginx-zero-day/)0 天。似乎 NGINX 中的 LDAP 引用实现特别容易受到攻击。F5 已经[确认确实存在问题](https://www.nginx.com/blog/addressing-security-weaknesses-nginx-ldap-reference-implementation/)。有一些安全补丁被推送到`nginx-ldap-auth`回购协议中，大概是为了解决这个问题。BlueHornet 是泄露漏洞的组织，而[已经发表了它对这个故事的看法](https://github.com/AgainstTheWest/NginxDay)。在 NGINX 中使用 LDAP？这是一个需要仔细研究的问题。