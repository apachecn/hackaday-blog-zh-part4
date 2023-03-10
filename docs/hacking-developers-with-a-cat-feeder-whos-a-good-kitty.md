# 用喂猫器攻击开发者:谁是好猫咪？

> 原文：<https://hackaday.com/2022/10/12/hacking-developers-with-a-cat-feeder-whos-a-good-kitty/>

我们中的大多数人可能都知道完成一些编码工作的苦差事，只有单调乏味的几个小时在等待着我们。如果当我们做一些有成效的事情时，比如提交一份承诺或其他衡量进展的措施，这种单调乏味会被偶尔的奖励打断吗？当[约翰·帕蒂]的目光落在其中一个自动喂猫器上时，这大概就是他最初的想法。无论是猫还是开发者，谁不喜欢听到美味食物落入碗中的叮当声呢？

目标宠物喂食器是 PetKit Fresh Element Solo，它允许通过喂食机制喂食尺寸为 12×12 mm(任何方向)的物体。幸运的是，[John]最喜欢的黑巧克力杏仁糖符合这些要求，他开始着手解决在 cat feeder 设备上触发手动喂食事件所需的 REST API 调用，使用现有的 [PyPetKit Python 库](https://github.com/morganpartee/pyPetKit)来完成连接到 PetKit 的服务器并与之通信的繁重工作，因为 feeder 当然是一个物联网设备。

这意味着事件流仍然依赖于 PetKit 的“云”，这可能会激发一些有事业心的黑客制作一个单机版本，其开发可能会通过一个常规的 treat 来辅助[John]的解决方案。在采用这种解决方案之前，一定要和你的任何宠物讨论一下，因为他们可能不太理解为什么每当出现**叮当** 的声音时，他们就没有奖励。

[https://www.youtube.com/embed/D2GqVWuo-yY?feature=oembed](https://www.youtube.com/embed/D2GqVWuo-yY?feature=oembed)