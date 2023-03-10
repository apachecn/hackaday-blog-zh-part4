# 传言公司将收获洗衣机用于集成电路

> 原文：<https://hackaday.com/2022/07/05/companies-rumored-to-harvest-washing-machines-for-ics/>

《连线》杂志和 [SCMP](https://www.scmp.com/business/article/3175018/some-chip-starved-manufacturers-are-scavenging-silicon-washing-machines) 正在报道芯片短缺领域的有趣琐事。显然，一些大型企业集团正在购买新的洗衣机，清理他们无法获得的芯片。在我的想象中，一个制作室里有技术熟练的工程师，重型电动螺丝刀和脱焊工具包放在他们旁边的地板上，一台拆了一半的洗衣机即将露出控制板，中间有一个 STM32。这可能不是最需要技术的工作，但这是一种节奏的改变，嘿，只要速度保持不变？

不管是哪家公司在做这件事，他们肯定会遇到难题。其中一篇文章举了一个例子，一个价值 35 万美元的光谱仪制造因缺少一个 0.5 美元的零件而停滞不前——虽然这听起来有些夸张，但这是有可能的。对于汽车制造商来说，这种差异并不可怕，但仍然足够严重，没有达到生产目标会产生除财务以外的后果。为了最终能够将一辆价值 3 万美元的汽车从装配线上移走，购买一台 150 美元的洗衣机可能确实是有意义的。

# 无论如何，运输——勉强

公司想出了一大堆办法让产品不断走出家门。从良好的旧代码优化，到部分排除功能的运输汽车，当然，购买严重标记的芯片，即使它们的来源是可疑的。至少，如果你的车没有一些基本的功能，可能有一个很好的理由——击败[功能即服务](https://hackaday.com/2021/12/30/new-cars-will-nickle-and-dime-you-its-automotive-as-a-service/)的事情。然而，即使是像大众、特斯拉和丰田这样的公司也在遭受损失，没有达到他们的目标，包括财务和公关方面的损失。

人们总是对解决集成电路短缺问题寄予厚望。芯片出现又消失，工具箱被制造出来，很酷的新替代零件被发现。然而，如果你在管理一家公司的生产流程，在某个时候，你必须打破“这可能明天就结束了”和“我们做得还不够”之间的不确定状态。你要么采取孤注一掷的措施，要么你可能会发现自己失业了。

你可能会认为这种情况现在应该已经解决了——毕竟，差不多两年前就已经开始了！当然，总会有新的复杂情况出现。俄罗斯对乌克兰发动的战争中断了一些供应链，使得部分产品更加昂贵。中国的新冠肺炎工厂定期停工，三月份的一场地震[导致一些日本工厂停工](https://www.cnbc.com/2022/03/17/quake-in-japan-kills-two-halts-factories-cuts-power-to-thousands-of-homes.html)，TSMC 的产能也将在 2023 年售罄——没有给那些不幸被列入计划的人留下多少希望。

# 回收的反面

这种情况让我想起了去年来自[Unbinare]的[Maurits Fennits]的[Remoticon 演示文稿](https://hackaday.com/2022/01/06/remoticon-2021-unbinare-brings-a-reverse-engineering-toolkit-into-recycling/)——创建一个逆向工程工具包，以便能够重用部件，除非无法通过业务关系获得专有信息。Unbinare 的工具包令人印象深刻，我希望至少有一些工具在解决芯片短缺问题时得到了很好的利用。

另一方面，为了一个芯片而拆卸全新的设备会产生更多的电子垃圾，即使这在经济上是有意义的。我们不能现实地期望有问题的公司会把这些洗衣机恢复到工作状态并重新投放市场；整个拆卸和拆焊操作可能也相当具有破坏性。

当然，洗衣机的事情不可能经常发生，也没有迹象表明这是一个孤立的事件。然而，如果使用了这样的方法，我希望它们至少能引起一些反思。例如，人们可能会梦想苹果公司被迫面对它的亲和力，即粉碎它们本应回收的设备——而不是真正有意义的回收形式。恐怕这不会发生了。

在过去的一两年里，我们已经拆除了许多原型，从 STM32 到包含 Raspberry Pi 的原型。请告诉我们你最近的“回收零件，让新项目焕发生机”之旅！