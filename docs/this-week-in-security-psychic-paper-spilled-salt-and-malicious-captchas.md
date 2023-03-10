# 本周安全:精神纸，撒盐，和恶意验证码

> 原文：<https://hackaday.com/2020/05/08/this-week-in-security-psychic-paper-spilled-salt-and-malicious-captchas/>

苹果最近修补了一个安全问题，[修复了灵异纸 0 天](https://siguza.github.io/psychicpaper/)。坦白地说，这是[Siguza]在 iOS 如何处理应用程序代码签名中的 XML 数据时发现的一个有点令人尴尬的缺陷，该代码签名允许他访问 iOS 系统上的任何权限，包括在沙箱外运行。

iOS 上的授权是应用程序可以请求的一组权限。这些权利范围从前面提到的`com.apple.private.security.no-container`到`platform-application`，这告诉系统这是一个官方的苹果应用程序。正如人们所预料的那样，苹果公司严格控制授权，只允许在其官方商店托管的应用程序上的某些授权。即使是开发者签名的应用也极其有限，只允许两种权限。

该系统通过 XML 列表文档工作，该文档是签名应用程序的一部分。XML 是 HTML 的亲戚，但是有更严格的规则。[Siguza]发现 iOS 包含 4 种不同的 XML 解析器，它们处理畸形 XML 的方式略有不同。有趣的是，其中一个解析器进行安全检查，而另一个解析器用于实际的权限实现。这种不匹配是否可能包含漏洞？当然有。

> 撕裂我的第一个 0 天，绝对是有史以来最好的沙盒逃生:

```
<key>应用标识</key>
<字符串>…</字符串>
<！——><！–>
<key>平台-应用</key>
<true/>
<key>com . apple . private . security . no-container</key>
<true/>
<key>task _ for _ PID-allow</key>
<true/>
<––>
```

> —Siguza(@ S1 guza)[2020 年 4 月 29 日](https://twitter.com/s1guza/status/1255641164885131268?ref_src=twsrc%5Etfw)