# 本周在安全:阿帕奇噩梦，REvil 逮捕？和终极里克罗尔

> 原文：<https://hackaday.com/2021/10/08/this-week-in-security-apache-nightmare-revil-arrests-and-the-ultimate-rickroll/>

Apache HTTP Server 版本 2.4.49 有一个很大的漏洞，并且已经在攻击中被利用。 [CVE-2021-41773](https://httpd.apache.org/security/vulnerabilities_24.html) 是一个简单的路径遍历漏洞，其中`%2e`编码用于绕过过滤。谢天谢地，这个 bug 是在最新版本 2.4.49 中引入的，并且已经发布了一个修补程序 2.4.50。

`curl --data "echo;id" 'http://127.0.0.1:80/cgi-bin/.%2e/.%2e/.%2e/.%2e/bin/sh'`

如果返回的不是 403 错误，那么您的服务器可能存在漏洞。值得指出的是，Apache 附带了一个配置块来缓解这一漏洞。

`# Deny access to the entirety of your server's filesystem. You must
# explicitly permit access to web content directories in other
# blocks below.
#
<Directory />
AllowOverride none
Require all denied
</Directory>`

## 互联网停滞的那一天

你可能已经注意到周一互联网上的一点混乱。脸书退出了近六个小时。虽然休息对一些人来说很好，但对另一些人来说却是个大问题。到底发生了什么？最明显的原因是 Facebook.com 域将 nxdomain 返回到 DNS 查找。这导致了一些有趣的推文，屏幕上显示 Facebook.com 出售。

> 多少钱？[https://t.co/fH0zXw7rV9](https://t.co/fH0zXw7rV9)
> 
> —jack⚡️(@杰克)[2021 年 10 月 4 日](https://twitter.com/jack/status/1445079948432117778?ref_src=twsrc%5Etfw)