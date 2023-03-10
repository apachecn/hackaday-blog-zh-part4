# 电压标准的划分

> 原文：<https://hackaday.com/2019/11/28/a-division-in-voltage-standards/>

在我最近的欧洲之行中，我发现转换器不如适配器卖得普遍，这是有原因的。世界上大部分地区接收 50-60 Hz 的 220-240 V 单相电压，除了加拿大、哥伦比亚、日本、台湾、美国、委内瑞拉以及加勒比海和中美洲的其他几个国家之外[数量惊人地少。](https://www.worldstandards.eu/electricity/plug-voltage-by-country/)

虽然大多数国家都有一种确定的插头类型，但拉丁美洲、非洲和亚洲的一些国家针对不同的墙壁插座使用了一系列不兼容的插头，这就需要根据所到地区的不同使用不同的适配器。

虽然在大多数国家，家用电器的电压都有一定程度的标准化，但是是什么导致了 220-240 V 标准和其他国家使用的 100-127 V 标准之间的差异呢？

## 典型住宅电源

市电电源(或电网电源、壁式电源、家用电源)是指家庭和企业中可获得的通用交流电源，通常用于家用电器。主电源的电压和频率可能不同，当然，试图使用不兼容的值会有损坏电器的风险。

最常见的是，电力通过两个或三个有线触点输送到家庭——火线(在电网和家庭之间传输交流电的火线)、零线(完成电路并传输交流电)和地线(将设备连接到大地以防止电击)。

电压值是相对于零线或地线的单根热线的测量值。考虑到家用电线的电阻和家用电器延长线的距离，该值通常会在到达电器时下降，这也是除电源电压之外的值用于电器额定值的原因之一。

我们之前已经写过[电力传输设备](https://hackaday.com/2019/06/11/a-field-guide-to-transmission-lines/)和[典型电线杆](https://hackaday.com/2016/02/22/a-field-guide-to-the-north-american-utility-pole/)上的变压器，用于从两相或三相公用线路为住宅供电。

## 这些电压标准源自哪里？

1882 年，托马斯·爱迪生建立了第一个大型中央发电厂，为伦敦的 968 个灯泡提供 110 V 的直流电(DC)。这被认为是消费者使用的“安全”电压，也是他的灯泡灯丝的最佳电压。

在他的伦敦工厂之后，交流系统开始在美国出现，使用变压器来降低配电系统的高电压。爱迪生的回应是[在 1883 年](https://edison.rutgers.edu/patents/00283986.PDF)为三线配电系统申请专利，为用户提供更大的多功能性，这很快让位于电流的战争(实际上[最近有一部关于这个主题的电影](https://en.wikipedia.org/wiki/The_Current_War))。

在美国，在交流电被证明更优越之后，西屋电气公司采用了 110 VAC 60 Hz 标准。另一方面，欧洲电力公司为了提高配电效率，将电压提高到 240 V。在这一点上，绝缘电线和配电中的安全措施是足够的，240V 不再被认为对用户是危险的，导致 240 VAC 50Hz 标准的广泛采用。

根据与地面的连接情况，他们皮肤的湿度或电阻、他们接触的表面积以及持续时间都会对处理触电死亡的人的实际安全问题产生影响。但在现代，断路器、GFCI 插座(接地故障断路器)和 AFCI 插座(电弧故障断路器)在解决市电触电死亡和火灾问题方面发挥了很大作用。

## 这是我们的系统

这就是现状，也是未来的发展方向。目前还没有在国际上统一标准电源的重大变革计划。从一个系统转换到另一个系统会非常昂贵，而且没有动力这样做。现代电子产品制造商已经在很大程度上解决了这一问题，他们设计了可以在 240 V 或 110 V 电压下正常工作的电源，只需要一个简单的转换器就可以让[各种插座类型](https://hackaday.com/2016/05/19/hackadays-fun-with-international-mains-plugs-and-sockets/)与您所在国家选择的标准完美匹配。

对于直接使用交流电源的设备，插头类型有助于确保销售的是与市场相关的设备。在像美国这样的国家，当需要更高的 240 V 标准时，使用两个热管段对插座进行接线，以从设计为提供 110 V 的电网系统获得 200-240 V。