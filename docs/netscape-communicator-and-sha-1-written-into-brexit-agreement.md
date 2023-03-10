# 网景通信公司和 SHA-1 写入英国退出欧盟协议

> 原文：<https://hackaday.com/2020/12/28/netscape-communicator-and-sha-1-written-into-brexit-agreement/>

我们同情参与欧盟和英国谈判的公务员，因为在紧张的会议进行到最后一刻后，他们不得不在极短的时间内拼凑出后英国退出欧盟贸易协定的文本。在这类国际协议的通常方式中，双方都声称取得了对鱼类的某种胜利，但文件中真正有趣的部分在于小字。特别是，眼尖的安全研究人员发现，建议使用 1024 位密钥长度的 [Netscape Communicator 4、SHA-1 和 RSA 加密来保护州与州之间的 DNA 数据传输。有争议的段落可以在](https://twitter.com/billatnapier/status/1342877839008411648)[1256 页的协议](https://ec.europa.eu/transparency/regdoc/rep/1/2020/EN/COM-2020-857-F1-EN-ANNEX-1-PART-1.PDF)第 932 页找到。

[![](img/c6c007f9f33b66aecbe56ac9b50cf568.png)](https://hackaday.com/wp-content/uploads/2020/12/Brexit-Netscape-communicator-text.png)

很可能一些 30 岁以下的读者从未使用过网景的产品，即使他们熟悉火狐，Mozilla 的后代软件。Netscape 是早期网络浏览器的先驱，Communicator 4 是该公司从 20 世纪 90 年代后期开始提供的集浏览器和电子邮件于一体的产品。它和它的继任者在微软的 ie 浏览器面前节节败退，最终在 2000 年代末随着 AOL 的所有权一起消失。同时[SHA-1 哈希算法已经被证明容易受到碰撞攻击](https://hackaday.com/2017/02/23/shattered-sha-1-is-broken/)，计算能力已经进步到 1024 位 RSA 加密可以被任何有足够 GPU 能力的人在合理的时间框架内破解。很明显，在起草这份条约的过程中出现了一些问题，我们甚至大胆地认为，一个疲惫的公务员只是简单地从一份 20 世纪 90 年代末的安全文件中进行了剪切和粘贴。

那么，欧洲的立法者现在必须按照条约的要求挖掘古代软件吗？我们希望不会，因为从我们的阅读来看，它们是作为例子而不是指示给出的。然而，我们担心他们的机构可能会像公务员一样对数字安全一无所知，因此，网景品牌的当前所有者 Verizon Communications 可能会接到一些支持电话。