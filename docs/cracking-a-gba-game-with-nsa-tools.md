# 用 NSA 工具破解 GBA 游戏

> 原文：<https://hackaday.com/2021/07/16/cracking-a-gba-game-with-nsa-tools/>

[Wrongbaud]是日本凯剧风格电影的超级粉丝，包括《哥斯拉》和《金刚》。为了庆祝一部新电影的上映，他决定着手几个项目，看看这两个怪物如何与其他传奇怪物抗衡。在这个项目中，他使用的是 Ghidra，以另一个传说中的凯居命名，[来对抗 Game Boy Advance 游戏《孔:亚特兰蒂斯之王》](https://wrongbaud.github.io/posts/kong-vs-ghidra/)的密码系统。

因为这个项目是一个操作指南，[wrongbaud]展示了如何在 Ghidra 中搜索可能已经具备 GBA 分析和仿真所需功能的现有脚本。当没有的时候，他还演示了如何编写脚本来自动化代码分析，然后继续破解游戏中的级别密码系统。

在这个游戏中找到密码的关键是在代码中寻找 7 个字符长的值，经过一些搜索后，[wrongbaud]最终能够锁定负责处理密码的代码。一旦找到一个蛮力的方法是自动寻找可行的密码，并从那里游戏正式 pwned。对于任何对安全性、逆向工程或者仅仅是二进制工作方式感兴趣的人来说，这是相当详细的分解。当然，[并不是我们见过的唯一一个用这个软件工具提取密码的例子](https://hackaday.com/2021/07/15/using-ghidra-to-extract-a-router-configuration-encryption-key/)。