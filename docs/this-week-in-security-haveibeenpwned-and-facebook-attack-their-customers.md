# 本周安全:哈韦本 Pwned 和脸书攻击他们的客户

> 原文：<https://hackaday.com/2020/06/19/this-week-in-security-haveibeenpwned-and-facebook-attack-their-customers/>

在这里，我们都是 haveibeenpwned.com 的粉丝，但本周我的办公桌上出现了一个奇怪的故事——[特洛伊·亨特] [在他们的一封电子邮件中写了一封恶意的 SQL 注入](https://fyr.io/2020/05/30/haveibeenpwned-com-pwned-our-helpdesk-glpi-9-4-5-sql-injection/)！那个攻击字符串是一个简单的`';--`

等等，那看起来不眼熟吗？你还记得 haveibeenpwned 网页上的标题吗？对，就是`';--have i been pwned?`。这是一个关于 SQL 注入的巧妙的内部笑话，是该公司品牌的一部分。一份自动公告被发送给一家碰巧使用 GLPI 服务台软件的公司。那家公司，由于即将变得显而易见的原因，不应该被命名，正在运行一个稍微过时的 GLPI 安装。那封电子邮件生成了一张自动支持票，从神奇的符号集合开始。当技术人员自行分配门票时，SQL 注入错误被触发，他们的整个门票数据库被清除。故事圆满结束，多亏了一个好的备份，公司[学到了宝贵的一课](https://xkcd.com/327/)。

> 很明显，一封[@ haveibenpwned](https://twitter.com/haveibeenpwned?ref_src=twsrc%5Etfw)电子邮件由于我在邮件内容中加入的 SQL 注入模式而清除了整个票务系统🤣https://t.co/orhcCA05RO
> 
> —特洛伊·亨特(@ Troy Hunt)[2020 年 6 月 3 日](https://twitter.com/troyhunt/status/1268309629437526018?ref_src=twsrc%5Etfw)