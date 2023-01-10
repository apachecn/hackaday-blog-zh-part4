# 谷歌和苹果透露他们的冠状病毒接触追踪计划:我们踢轮胎

> 原文：<https://hackaday.com/2020/04/16/google-and-apple-reveal-their-corona-tracing-plans-we-kick-the-tires/>

谷歌(Google)和苹果(Apple)联手发布了一个通用 API，该 API 将在其手机操作系统上运行，使应用程序能够跟踪你“接触”到的人，以减缓新冠肺炎疫情的传播。这是一个极其艰巨的任务，要做到自愿，尽可能尊重个人隐私，不依赖潜在的易受攻击的集中式服务，并且不会产生太多的误报，结果要么被忽略，要么造成大规模恐慌。或许更重要的是，它必须有效。

## 减缓扩散

当我写这篇文章时，新冠肺炎疫情似乎正在从不受控制的指数增长转向可能更容易管理的增长，但我们还不清楚是否会看到尽头。迄今为止，这已经要求数亿人进入实质上的自愿隔离状态。但那是个钝器。在一个理想的世界里，如果你能以某种方式检测每个人并隔离那些接触过病毒的人，你可以在几周内在全球范围内阻止这种疾病。在现实世界中，真正全面的测试是不可能的，并且由于两个因素，找出谁被隔离是非常困难的:新冠肺炎有很长的潜伏期，在此期间它仍然是可传播的，以及[一些甚至大多数人不知道他们患有此病](https://science.sciencemag.org/content/early/2020/03/24/science.abb3221)。你怎么能阻止你看不到的东西，甚至当你能察觉的时候，已经晚了一个星期。

一种有希望的方法是隔离那些在隐形传染期间与已知病例有过接触的人。要做到这一点，基本上就是记下你在过去一两周内接触过的每个人的日记，然后如果你最终检测出新冠肺炎阳性，提醒他们所有人，这样他们就可以在检测出阳性之前防止感染他人:跟踪和追踪。医生可以通过采访测试呈阳性的患者来做到这一点(这是我们经常听到的“接触追踪”)，但记忆是不完美的。输入技术解决方案。

## 蓝牙邻近追踪

苹果和谷歌推出的系统旨在允许人们查看他们是否与携带新冠肺炎病毒的其他人有过接触，同时尽可能尊重他们的隐私。这大体上类似于由罗恩·里维斯领导的麻省理工学院团队[、欧洲学术团体和新加坡开源 BlueTrace 系统](http://news.mit.edu/2020/bluetooth-covid-19-contact-tracing-0409)提出的建议。核心思想是每部手机使用蓝牙 LE 发射一个伪随机数，射程很短。附近的其他手机听到信号并记住它们。当一个手机的主人被诊断患有新冠肺炎病毒时，这个人发出的号码就会被释放，你的手机可以查看它的数据库中是否存储了这些号码，这表明你有潜在的暴露风险，也许应该进行测试。

值得注意的是，与韩国或以色列的追踪方式不同，不需要地理定位数据就能知道谁和谁关系密切。随机数变化频繁，无法用来全天跟踪你的手机，但它们是由一个单独的每日密钥生成的，一旦你测试呈阳性，就可以用这个密钥将它们联系在一起。

(在新加坡，政府卫生部也收到了每个人接收到的信标的副本，并可以亲自进行后续检测。尽管这无疑非常有效，但由于美国的 HIPAA 隐私规则和欧洲类似的患者隐私法，这种集中的方法可能是不合法的。我们不是律师。)

## 密码

[![](img/b5c5838aa0b1773113405614665b71ae.png)](https://hackaday.com/wp-content/uploads/2020/04/google_apple_schedule.png) 在[苹果/谷歌加密方案](https://covid19-static.cdn-apple.com/applications/covid19/current/static/contact-tracing/pdf/ContactTracing-CryptographySpecification.pdf) (PDF)中，你的手机会一次性生成一个专用于你设备的秘密“追踪密钥”。然后，它使用该密钥每天生成一个“每日跟踪密钥”，随后每 15 分钟从每日密钥生成一个“滚动邻近标识符”。每一个更频繁的密钥都是由带有时间戳的[散列](https://en.wikipedia.org/wiki/Cryptographic_hash_function)从其父密钥生成的，这使得几乎不可能沿着链向上，例如，从信标发出的邻近标识符中推断出你的每日密钥，但是在下游方向，一切都可以很容易地被验证。32 个*字节*的跟踪密钥足够大，因此发生冲突的可能性极小，而且特定于个人的跟踪密钥永远不需要泄露。

如果你的测试结果是阳性的，你被传染的时间窗口的每日密钥被上传到一个“诊断服务器”,该服务器然后将这些每日密钥发送到所有参与的电话，允许每个设备对照它从服务器获得的传染人天数列表来检查它接收到的信标。你的曝光数据永远都不需要离开你的手机。

诊断服务器使用传染性个体的每日密钥，以便您的手机能够区分单个短期联系(仅看到某个每日密钥中的一个标识符)和更长、更危险的联系(看到同一个受感染的每日密钥中的多个 15 分钟标识符)，即使您的手机无法随着时间的推移将滚动的邻近标识符链接在一起。因为每日密钥是以单向方式从您的秘密跟踪密钥中获得的，所以如果您被感染，服务器不需要知道您的任何身份信息。

美国公民自由联盟(ACLU)在提议的计划之前编写了一份白皮书(T1 ),但涵盖了他们希望在隐私和安全方面解决的问题，从这个角度来看，当前的提议得分相当高。它与其他保护隐私的“接触追踪”提议一致，这也令人放心。

## 会出什么问题呢？

对这个系统最明显的担心是它会产生大量的误报。蓝牙信号可以穿透病毒不能穿透的墙。我们想象一个高层公寓大楼的电梯旅行“感染”住在电梯井无线电范围内的每个人。在我们当地的杂货店，收银员相当安全地位于一个大的丙烯酸屏蔽后面，但蓝牙可以直接穿过它。好消息是，这些偶遇可能很短暂，系统可以将这些单一事件视为低暴露风险，以避免用户因错误警报而不知所措。如果人们被要求在上传他们的日常密钥之前测试阳性，而不是手机自动做一些事情，这可以防止连锁反应。

[![](img/1c485fcfc84e3064db029709061beef7.png)](https://hackaday.com/wp-content/uploads/2020/04/hands.jpg) 但如果系统剔除了所有的短联系人，它也会漏掉那个在卫生纸通道从你身边走过时刚刚打了个喷嚏的发烧家伙。除了假阳性，还会有真阳性的未检测。蓝牙信号范围可能是实际暴露的一个不错的替代，但它并不完美。蓝牙不知道你洗过手没有。

密钥的级联散列使得伪造系统变得相当困难。想象一下你想骗我们以为我们已经暴露了。您可能会无意中听到一些与我们相同的信标，但由于单向哈希，您将很难推导出一个每日密钥，该密钥将在那个确切的时间产生我们收到的滚动标识符。

## 混乱，钥匙丢失，它只是一个 API

然而，我们看不到的是，是什么阻止了一个恶意的人声称他们的新冠肺炎病毒检测呈阳性，而事实并非如此。如果对诊断服务器的报告没有进行某种方式的审计，那么可能就不会有那么多反社会的个人在公共场合拿着手机到处走，然后报告，从而制造一场虚幻的疫情。或者用可编程蓝牙设备做同样的事情。诊断服务器的访问权限是否仅限于医生？谁啊。怎么会？当一个无赖得到凭证时会发生什么？

[![](img/914281aa8d808451c25ef3142c28f90a.png)](https://hackaday.com/wp-content/uploads/2020/04/tracing_keys.jpg) 一个秘密追踪密钥的存在，即使它应该只驻留在你的手机上，也是一个巨大的安全和隐私风险。这是城堡的钥匙。手机可能是你拥有的最不安全的计算设备——泄露你的数据的应用程序比比皆是，无论是故意恶意的还是由只想更好地了解你的公司创建的。如果我们幸运的话，这个追踪密钥被加密存储在手机上，至少使它更难被获取。但是它不能被安全地存储(读:hashed ),因为它需要被系统直接使用来生成每日密钥。

诊断密钥可以撤销吗？当 COVID 测试产生假阳性时会发生什么？你当然希望能够解除对系统中所有人的警告。或者在向服务器注册之前，我们需要两次后续的阳性测试吗？而且一个人被检测后多久会传染？我们希望被确诊的患者呆在家里，但我们不会天真到相信这种情况总是会发生。每日密钥的报告何时停止？谁阻止它？

这就把我们带到了应用程序。苹果和谷歌提出的只是一个应用编程接口(API ),最终将被一个操作系统级的服务所取代。这个基础设施只允许第三方创建他们的蓝牙跟踪器应用程序、诊断服务器和基础设施的所有其他部分。那里的工作仍然是 TBD。这些自然要由可信的机构来写，可能是国家卫生机构。即使这是一个坚实的基础，信任也必须放在更高的位置。例如，它在规范中说，“(诊断)服务器不得保留来自客户端的元数据”，我们必须相信他们这样做是正确的，否则匿名的承诺将处于危险之中。

我们几乎可以肯定，恶意的新冠肺炎应用程序也会被编写来利用天真的用户——看看最近一系列与冠状病毒相关的网络钓鱼就知道了。

## 行得通吗？

这是一个未知的领域，我们真的不确定这种大规模的追踪工作是否可行。类似这样的事情在新加坡确实奏效了，但是还有很多令人困惑的因素。首先，新加坡的系统直接向卫生部报告接触情况，此后会有一个人跟踪你的情况。在遏制行动中动员起来的原始男女力量不应被低估。其次，新加坡也经历过[非典](https://en.wikipedia.org/wiki/2002%E2%80%932004_SARS_outbreak)，2005 年新加坡动员起来抗击禽流感，效果惊人。他们有应对流行病的经验，及早发现了新冠肺炎疫情，并以一种在欧洲或美国不再可行的方式领先于疾病。所有这些都是独立于蓝牙追踪的。

但随着这种疾病持续存在，医院不堪重负的严重危险减弱，总有一天，比自我隔离更温和的预防措施会再次变得合理。或许到那时，一款手机应用程序将是不二之选。如果是这样的话，做好准备可能会有好处。

[![](img/8600caa3375d912affe112618bcbba6f.png)](https://hackaday.com/wp-content/uploads/2020/04/tests.jpg) 能行吗？首先，这完全独立于服务器或哈希算法，如果新冠肺炎测试不是广泛和容易获得的，这一切都没有意义。如果没有人接受测试，系统将无法警告人们，反过来他们也不会接受测试。该系统完全依赖于处于危险中的参与者接受测试的能力，具有讽刺意味的是，适当的测试和医疗护理可能会使该系统变得无关紧要。

人性在这里也会对我们不利。如果有人连续几天收到警告，但并不觉得恶心，他们会无视闪烁的红色警告信号，在疾病传播的否认中走一周。在新加坡的系统中，一个社会工作者会过来帮助你，在这方面是完全不同的。

最后，收养是房间里的大象。这些应用程序还没有被编写出来，但它们将是自愿的，如果没有人使用它们也没什么帮助。但另一方面，如果联系追踪*得到广泛应用，它将变得更加有效，这将在良性循环中吸引更多的参与者。*

## 细节决定成败

苹果/谷歌系统的框架看起来相当稳固，剩下的大部分警告看起来都隐藏在实现中。误报和漏报之间的权衡取决于系统读取为“传染性”的蓝牙接触的数量和类型。应用程序和服务器安全是 TBD，但原则上可以妥善处理。假设所有的附带资源，比如容易获得的新冠肺炎测试，都可以发挥作用，那么剩下的就是困难的部分了。我们怎样才能确保尽可能顺利地进行呢？

[![](img/0ceb5d9a58b76d763b120d7e8237b45d.png)](https://hackaday.com/wp-content/uploads/2020/04/covid-laptops-privacy-1_thumbnail.png) 电子前沿基金会[在苹果/谷歌框架发布后不久](https://www.eff.org/deeplinks/2020/04/challenge-proximity-apps-covid-19-contact-tracing)发布了一份报告，虽然它对基础给予了认可，但它也对基于该框架开发的任何应用程序提供了一系列保护措施。同意、尽量减少数据收集、信息安全、透明、没有偏见以及一旦危机结束就终止数据的能力是他们的指导方针。这些也符合德国混乱计算机俱乐部的建议，他们额外推动开源代码，允许那些担心他们的数据如何被处理的人审计代码。

令人振奋的是，谷歌和苹果也解决了许多隐私问题，但我们希望听到一些讨论，讨论他们在一切结束后关闭整个事情的标准是什么。全球疫情也许是为了更大的利益脱下锡纸帽子的好时机，但是我们不希望无处不在的接触追踪成为新常态。

虽然有些人可能会认为隐私问题和软件细节是让我们通过新冠肺炎疫情的次要问题，但这个项目的成败取决于人们是否选择加入，在应该接受测试的时候接受测试，以及在出现阳性结果时的适当行为。人们只有在信任这个系统的情况下才会选择加入，只有当这个系统越简单越好的时候，他们才会接受测试。这两个只有一个可以用软件解决。