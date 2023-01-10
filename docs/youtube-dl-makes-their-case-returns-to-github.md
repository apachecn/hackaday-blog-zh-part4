# Youtube-dl 提出他们的理由，回到 GitHub

> 原文：<https://hackaday.com/2020/11/16/youtube-dl-makes-their-case-returns-to-github/>

上个月，受欢迎的节目 *youtube-dl* 的 GitHub 存储库被关闭，以回应美国唱片工业协会(RIAA)提交的 DMCA 关闭通知。RIAA 投诉的关键在于，该工具可以用来下载从各种平台下载的音乐的本地副本，他们表示，几个有版权的音乐文件被列为存储库中的单元测试，这一事实支持了这一说法。

虽然许多人认为这是对强大的 Python 程序真正用途的严重歪曲，但 RIAA 的观点并非完全没有价值。因此，GitHub 被迫遵从 DMCA 的要求，直到情况得到澄清。[今天，我们很高兴地向大家报告已经发生的事情](https://github.com/github/dmca/blob/e00bfb544e93bfd3066fe1699171964dd2dc29e0/2020/11/2020-11-16-RIAA-reversal-effletter.pdf),*YouTube-dl*库已经正式恢复。

以电子前沿基金会为代表， *youtube-dl* 的当前维护者在今天下午的一封信中向 GitHub 的 DMCA 代理人陈述了他们的情况，信中解释了该工具是如何工作的，并直接解决了受版权保护的视频被用作源代码中的测试案例的问题。他们坚持认为他们的程序没有绕过任何 DRM，并且客户端和服务器之间的交换就像用户用 web 浏览器查看资源一样。此外，他们认为，出于测试软件功能的目的下载几秒钟有版权的材料属于合理使用。尽管如此，[他们还是决定删除所有提及问题歌曲的内容，以避免任何不当的暗示。](https://github.com/ytdl-org/youtube-dl/commit/1fb034d029c8b7feafe45f64e6a0808663ad315e)

在此期间， [GitHub 与 *youtube-dl* 开发者密切合作，发布了他们自己的声明，以配合 EFF 信函](https://github.blog/2020-11-16-standing-up-for-developers-youtube-dl-is-back/)。他们解释说，RIAA 最初投诉的性质迫使他们采取行动，但他们从来不认为拆除存储库是正确的决定。具体来说，他们指出了用户可能希望保留流媒体的本地副本的无数合法理由。虽然 GitHub 表示，他们很高兴这个问题很快得到解决，但他们将对内部审查流程进行一些更改，以帮助防止进一步的轻率关闭。具体来说，该公司表示，他们将与技术和法律专家合作，在进一步升级之前审查有问题的源代码，如果对声明的有效性有任何模糊之处，他们将站在开发者一边。

在 youtube-dl 被关闭后，互联网[迅速为其辩护，我们很高兴地看到 GitHub 兑现了他们的承诺，与开发者合作，迅速让资源库重新上线。虽然开源代码的本质意味着社区永远不会面临失去这一重要工具的危险，但是项目的开发能够公开进行符合每个人的最大利益。](https://hackaday.com/2020/10/27/community-rallies-behind-youtube-dl-after-dmca-takedown/)