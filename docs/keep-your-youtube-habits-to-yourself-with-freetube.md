# 用 FreeTube 保持你的 YouTube 习惯

> 原文：<https://hackaday.com/2020/10/07/keep-your-youtube-habits-to-yourself-with-freetube/>

如果你通常的 YouTube 观看选择涵盖了各种各样的音乐、科技主题、烹饪、历史以及任何介于两者之间的内容，你迟早会被一些“推荐给你”的视频所困扰。当它播放了 10 个小时的苏联宣传合唱团音乐时，你可能会开始想知道一个被人工智能接管的世界实际上会是什么样子，并意识到你的浏览器的匿名/隐私模式真的不仅仅是为了秘密购买生日礼物。如果你真的喜欢甚至依赖整个订阅频道的概念，事情会变得有点棘手，在当今用户数据驱动的商业模式世界中，这自然很难与隐私保持一致。

进入对话:[FreeTube 项目](https://freetubeapp.io/)，一个跨平台的应用程序，它的[任务](https://freetubeapp.io/about.php)是重新获得隐私，把自己数据的控制权放回用户手中。绕过 YouTube 和它的播放器，观看历史和订阅(这仍然是可能的)只保存在你自己的本地计算机上，你可以从 YouTube 导入它们中的任何一个，并导出它们以在另一个设备上的 FreeTube 中使用(或返回到 YouTube)。更好的是，它不会在没有明确告诉它的情况下加载视频评论，当然它也会屏蔽广告。

最初，[Invidious API](https://github.com/iv-org/invidious)用于获取内容，并且仍然作为后备选项受到支持，但是 FreeTube 现在有了自己的提取器 API。所有源代码都可以从[该项目的 GitHub 库](https://github.com/FreeTubeApp/FreeTube)获得，以及[为 Linux(包括 ARM)、Windows 和 Mac 预建的包](https://github.com/FreeTubeApp/FreeTube/releases)。该应用程序本身是使用 Electron 创建的，这可能会引起一些人的注意，因为它包含了整个浏览器渲染引擎，本质上只是将一个网站伪装成独立的应用程序。但是[正如 FAQ 解决](https://github.com/FreeTubeApp/FreeTube/wiki/F.A.Q.#i-hate-electron--why-cant-you-use-literally-anything-else)一样，这允许容易的跨平台支持，并且帮助这个项目，否则将只限于 Linux，到达尽可能多的人。这是我们书中的一个有效观点。

请记住，FreeTube 只是一个播放器，更多的是 YouTube 本身的包装，所以 YouTube 仍然可以看到你的 IP 和与服务的交互。如果你想完全匿名，这不是一个银弹，将需要额外的步骤，如使用 VPN。不像其他服务[那样，你可以用本地的替代服务](https://hackaday.com/2018/09/03/fosscon-2018-developing-the-freedombox/)来代替，以避免跟踪和分析，如果你真的想有一个有用的选择，内容服务就有点棘手了。因此，这是一个很好的折衷方案，也适用于所有人，不管他们的技术背景如何。让我们只希望它不会打破太多的[下次一些 API 的变化](https://hackaday.com/2019/08/01/a-farewell-to-youtube-sub-counters-set-to-break-with-api-change/)。