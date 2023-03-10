# 黑客日链接:2020 年 7 月 26 日

> 原文：<https://hackaday.com/2020/07/26/hackaday-links-july-26-2020/>

一名澳大利亚少年陷入了困境，因为他涉嫌[泄露了关于在当地医院接受治疗的新冠肺炎患者](https://www.9news.com.au/national/coronavirus-western-australia-wa-data-breach-minor-allegedly-involved-site-shut-down/f80d8b89-47ba-42c4-9a1b-829eee7cb3e6)的敏感医疗信息。虽然西澳大利亚当局很快将这名身份不明的青少年描绘成一名恶意的、戴着巴拉克拉法帽的黑客，他在空闲的日子里侵入安全系统，但一篇叙述[当地媒体](https://www.9news.com.au/national/coronavirus-western-australia-wa-data-breach-medical-records-personal-information-hackers-website-covid19/0c78b0c4-29b1-423a-b39d-735841b203ef)太愿意鹦鹉学舌了，读完令人窒息的标题揭示了真相:这名青少年设置了一个 SDR 来接收来自医院的未加密 POCSAG 寻呼机数据，并建立了一个网页来实时显示这一切。我们之前报道过[不安全寻呼网络在医疗行业](https://hackaday.com/2017/12/24/art-eavesdrops-on-life-and-pagers/)的使用；这是一个众所周知的问题，任何 infosec 专家都不会对此感到惊讶。显然，当局只是希望没有人会花 20 美元买一个特别提款权，花一个下午的时间把所有这些放在一起，而不是解决真正的问题，当发现这一点时，他们把责任推到了孩子身上。

说到射频黑客，即使 2020 年希望大会虚拟化，[他们仍然会举办射频黑客村](https://scheduler.hope.net/hope2020/talk/QHQ38W/)。从时间表来看，还不清楚具体会发生什么；也许就像今年的 GNU 无线电会议 CTF 挑战赛一样，他们会分发音频文件给参与者解码。如果有人参加本周末开始的 HOPE，我们很想听听关于 RF 村——以及开锁村和所有其他景点——是如何组织的报告。这里希望它像 [DEFCON 安全模式的盒式磁带之谜](https://hackaday.com/2020/07/24/hands-on-the-pandemic-def-con-badge-is-an-audio-cassette/)一样酷。

随着 Eben Upton 宣布即将推出的 [Pi 计算模块 4 有望支持 NVMe 存储](https://www.tomshardware.com/news/raspberry-pi-nvme-support-coming)，看起来 Raspberry Pi 家族的性能将得到大幅提升。非易失性存储器 express 规范将允许快速访问存储，并使 Pi 用户用来提高访问速度的许多攻击变得不必要。虽然计算模块的目标是嵌入式系统设计师，但 Upton 也暗示，NVMe 支持可能会成为未来 Pi 4A 的主流 Pi 系列。

太阳上的篝火？这听起来很奇怪，但这就是太阳科学家对新委托的 ESA/NASA 太阳轨道卫星在我们恒星表面显示的亮点的称呼。轨道飞行器最近传回了它的第一张太阳图片，这是滚动表面的特写镜头。他们没有想到第一批图像会揭示一些新的东西，这些图像通常用于校准仪器并确保一切正常，但(相对)微小的亮点被认为是我们从地球上观察到的较大太阳耀斑的较小版本。轨道飞行器传回了一些迷人的图像，非常值得一看。

最后，虽然这是一篇老文章，与黑客无关，但我们偶然发现了蒂姆·厄本关于人类关系数学的观点，并发现它非常有趣，值得分享。要点是，地球上的每个人都是相关的，我们大多数人的近亲繁殖比我们想象的要多得多，这要归功于每个人祖先树的指数增长。例如，你有 128 位曾曾曾曾曾祖父母，他们可能生活在 19 世纪早期。每过一代，这个群体的规模就会翻一番，直到我们最终——在 17 世纪的某个时候——拥有了一个超过当时地球人口的祖先群体。这意味着，在这个过程中的某个地方，你的家族树中的某个人正和同一棵树的一个非常接近的树枝上的某个人在一起。这种结合，可能是第一代或第二代表亲之间的结合，产生了导致你的线索。这被称为血统崩溃，由于共享祖父母，它导致祖先池被大大削减。所以下次有人告诉你他们是 16 世纪皇室的后裔时，你可以直接告诉他们，“哦，是吗？我也是！”大概吧。