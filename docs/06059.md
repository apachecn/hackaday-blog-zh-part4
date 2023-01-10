# 用普通手动复苏器设计的 MIT 呼吸机:提交给 FDA 检测

> 原文：<https://hackaday.com/2020/03/23/mit-ventilator-designed-with-common-manual-resuscitator-submitted-for-fda-testing/>

在世界许多地方，新冠肺炎疫情造成了医院空间、人员、医疗用品和设备的短缺。严重的病例可能需要呼吸支持，但可用的呼吸机只有这么多。考虑到这一点，[麻省理工学院正致力于 FDA 对紧急呼吸机系统](https://e-vent.mit.edu/) (E-Vent)的批准。他们已经将设计提交给 FDA 进行快速审核。该项目是开源的，所以一旦他们获得批准，团队将发布复制它所需的所有数据。

这个设计实际上很简单，使用了一个很普通的东西:手动复苏器。毫无疑问，你已经在你最喜欢的医学节目中看到过这些。它是当主角为了拯救病人而英勇斗争时，某人紧握的袋子。当然，让几千人连续几天坐着挤压袋子是不太实际的，这就是为什么他们包括了一个 Arduino 控制的电机来自动化这个过程。

棘手的是，强迫空气进入肺部并不总是对他们有好处。即使健康的肺部也会因为过度的膨胀而受到压力，已经有肺部问题的人可能只能处理健康人所能处理的十分之一。这就是为什么该设备需要一个闭环控制系统来监控患者的压力并调整流量。

> 任何解决方案都应仅在由临床专业人员直接监控的医疗环境中使用。虽然就功能、灵活性和临床疗效而言，MIT E-Vent 不能取代 FDA 批准的 ICU 呼吸机，但预计它在帮助释放现有供应或在没有其他选择的生死攸关的情况下具有实用性。
> 
> 此外，任何低成本呼吸机系统必须非常注意为临床医生提供密切控制和监测潮气量、吸气压力、bpm 和 I/E 比的能力，并且能够以 PEEP、PIP 监测、过滤和适应个体患者参数的形式提供额外的支持。我们认识到，并希望向任何寻求制造低成本紧急呼吸机的人强调，未能正确考虑这些因素会导致严重的长期伤害或死亡。

这不是一个独特的想法，麻省理工学院的团队提供了其他类似项目的链接。团队的工作还没有完全上线，因为他们还在测试。例如，挤压袋子的丙烯酸装置可能不能很好地承受重复应力。该团队可能会关注危机前的其他项目。例如，看看下面视频中去年在一次会议上展示的[空气装置](https://the-air-project.github.io/)。还有一份来自约翰·霍普金斯医院居民[的有趣文件。](https://docs.google.com/document/d/1FNPwrQjB1qW1330s5-S_-VB0vDHajMWKieJRjINCNeE/preview?fbclid=IwAR3ugu1SGMsacwKi6ycAKJFOMduInSO4WVM8rgmC4CgMJY6cKaGBNR14mpM)

几乎和设备本身一样有趣的是人们对设计的评论。这是一个很好的例子，说明了互联网是如何开辟全新的方式来合作解决像这样的关键问题的。

当然，我们也看到了在[新冠肺炎测试](https://hackaday.com/2020/03/10/open-source-collaboration-tackles-covid-19-testing/)上的合作。如果你想帮忙，你可以把你的计算能力添加到虚拟超级计算机[折叠蛋白质中，以帮助找到治疗方法](https://hackaday.com/2020/03/18/join-team-hackaday-to-crunch-covid-19-through-foldinghome/)。

 [https://www.youtube.com/embed/0yB5J2ihjF8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0yB5J2ihjF8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

