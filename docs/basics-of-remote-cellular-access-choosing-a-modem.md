# 远程蜂窝接入基础——选择调制解调器

> 原文：<https://hackaday.com/2020/12/18/basics-of-remote-cellular-access-choosing-a-modem/>

这些天来，我们有幸拥有跨越地球大片区域的蜂窝数据网络。总的来说，他们习惯于看电视节目和在网上与陌生人争论。然而，它们也是一个很好的工具，可以用来与远程位置的硬件进行交互，特别是在有线连接不切实际的移动位置。

在这个系列中，我们来看看正确进行远程蜂窝管理的技巧和诀窍。首先，你需要一个数据连接，所以让我们来看看如何选择调制解调器。

## 选择很多

当购买蜂窝数据调制解调器时，很难在众多选择中找到合适的。这一领域的调制解调器通常针对非常特殊的使用情况进行销售；在消费者层面，许多都被设计成简单的家庭宽带解决方案，而在商业领域，它们的主要目标是为餐馆和咖啡馆提供免费 WiFi。对于在远程管理中的使用，某些功能的存在可能是至关重要的，所以在花你辛苦赚来的钱之前做你的研究是值得的。我们在下面列出了一些常见的选项。

### 消费者模型

![](img/82d19fe1a55296618404fb4457b8a62e.png)

The Sierra Aircard 320U is ancient now, with limited frequency bands available. Its flimsy flexible connector is also a drawback. However, its ease of configuration with Linux systems makes it a dream to use in remote access situations. Unlike many others, it acts as a Direct IP connection, not appearing as a separate router.

世界各地的许多电信提供商都出售廉价的 USB 加密狗来连接互联网，这些加密狗最初随着 3G 的兴起而变得流行。在 5G 时代，它们现在有点不太常见，市场更多地转向支持 WiFi 的设备，这些设备可以在几个用户之间共享互联网。这些设备通常不到 50 美元，用于预付费和合约数据计划。

这些设备通常是初露头角的发烧友构建需要通过蜂窝网络进行远程管理的项目的第一站。然而，它们有一些限制，这使得它们在这种用途上不那么有吸引力。针对家庭用户，他们通常被提供最少配置选项的固件严重锁定。它们通常不能被设置为端口转发，即使你能说服你的电信公司给你一个真正的 IP 地址而不是电信级 NAT。更糟糕的是，许多主机本身就像一个路由器，增加了另一层 NAT，使事情变得更加复杂。也许最令人沮丧的是，对于这些电信公司提供的调制解调器，印在盒子上的型号通常不能很好地指导你得到的是什么。

一个完美的例子是华为 E8327。这带来了大量的子模型，各种版本的调制解调器在不同的路由模式下工作，在不同的频段上工作，有些甚至省略了外部天线连接器等主要功能。通常情况下，在你打开盒子并揭开盖子之前，你不可能确切地知道这款设备有什么功能，而在这种情况下，你就无法把设备退回来退款了。

然而，并非一切都没了。VPN 的使用有助于解决 NAT 问题，对于更喜欢冒险的人来说，一些型号甚至在网上更深入、更黑暗的论坛上提供定制固件。对于真正囊中羞涩的人来说，对于那些愿意应对不可避免的头痛的人来说，它们是一个可行的选择。在这一领域，通常有一些调制解调器因其可配置性和易用性而脱颖而出。这位作者用现在已经老化的 Sierra Aircard 320U 取得了巨大成功，而其他人用华为 E3372-607 找到了运气。根据之前的警告，你不会想意外地得到一个 e 3372-608-thar be dragons。

### 商业和工业硬件

对于那些不愿意浪费时间的人来说，更严肃的硬件自然是可用的。商业和工业级设备的成本自然会更高，但通常是完全解锁的，可以随心所欲地配置。这也避免了 SIM 卡锁定的痛苦，允许你使用任何你想要的网络。

[![](img/22190271b60b7c2905fe1dbad319d0a7.png)](https://hackaday.com/wp-content/uploads/2020/11/ltemodems-wrack.jpg)

Going with industrial-grade hardware means you get other nice-to-haves, like full-size antenna connectors and rack mounting capability.

在低端，像 [Sixfab LTE Base Hat](https://sixfab.com/product/raspberry-pi-base-hat-3g-4g-lte-minipcie-cards/?utm_medium=ppc&utm_campaign=DSA+Page+Feed+%7C+Well+Performing+Countries+%7C+All+Users+%7C+All+Devices&utm_term=&utm_source=adwords&hsa_src=g&hsa_net=adwords&hsa_kw=&hsa_tgt=dsa-455300353588&hsa_ad=467021815429&hsa_grp=108494316886&hsa_mt=b&hsa_acc=6308888758&hsa_ver=3&hsa_cam=11182900312&gclid=CjwKCAiAkan9BRAqEiwAP9X6UYCmuWVTjFYCsxhgiAlb6GbNARABlGQmbkJRK7j_0Dn3F7MQDXQwCRoCFEYQAvD_BwE) 这样的产品提供了简单的蜂窝数据连接。根据所选的具体配套器件，它可以根据世界各地的情况进行设置，并针对低功耗或高吞吐量进行优化。在高端，你可以拥有任何你想要的功能，只要你的笔记本足够大。

[双 SIM 卡选项](https://www.dlink.com.au/business-solutions/DWM-312-4G-LTE-Dual-SIM-M2M-VPN-Router)带来了故障转移功能的优势，可在信号差时保持您的远程系统在线，[而其他产品则打包了多个 LAN 端口，以支持许多系统。](https://www.iot-store.com.au/collections/iot-networking-comms/products/industrial-dual-sim-4g-lte-wifi-wireless-router-usr-808-au)市场上甚至有专门设计用于[通过 4G/LTE 远程监控串行终端硬件的设备。](https://inhandgo.com/products/indtu332-industrialserial-to-cellular-modem-lte-cat?utm_medium=cpc&utm_source=google&utm_campaign=Google%20Shopping&currency=USD&gclid=CjwKCAiAkan9BRAqEiwAP9X6UXNFndx7YcnHUU2wSexGF5j22N4KCyz2WuVqNhF_uVqcd52kgSltXxoC0u0QAvD_BwE&variant=33806232125579)这一级别的大多数设备还支持内置的 VPN，这使得访问您的远程机器变得更加容易，就像它们在本地网络上一样。

在这个级别，你通常可以在购买前与经销商或零售商讨论你到底需要什么功能。这与在模糊的论坛上搜寻消费者卡上的信息形成了鲜明的对比，对于任何时间就是金钱的严肃的工程目的来说，这都是可行的方法。这样的硬件(通常)也能得到制造商更好的支持，因为预计您将在需要高正常运行时间和良好可靠性的情况下使用它。

### 摘要

最终，您决定使用的硬件将取决于您的使用情形。如果你正在做一个需要*工作的严肃项目，*选择合适的工业硬件将是一条可行之路。如果你是一名黑客或制造者，对远程构建很感兴趣，节省几块钱可能会弥补启动和运行时的一些麻烦。当然，Hackaday 社区中有很多人都曾去过那里并建造了那个 T3，所以一定要在评论中提出你对选择合适的蜂窝调制解调器的最佳建议。黑客快乐！