# 将纽约市连接到主干网:认识纽约市的网状网络

> 原文：<https://hackaday.com/2019/06/30/connecting-new-york-city-to-the-backbone-meet-nycs-mesh-network/>

在美国，即使是在像纽约这样的大都市，获得快速和负担得起的互联网也是一个大问题。早在 2013 年，在一个根本不会提供服务的互联网服务提供商卡特尔中，一群纽约市居民首先承担起缓解这种局面的责任，他们建立了自己的网状互联网连接。现在，他们将[安装一个新的超级节点](https://www.nycmesh.net/pressreleases/Release19-06-13),使安装基础远远超出目前服务的 300 栋建筑。

作为一个社区项目， [NYC Mesh](https://www.nycmesh.net/) 作为一个非营利组织运营，其社区成员通过捐款以及与企业的合作来支持这项工作。[它的路由器硬件由](https://www.nycmesh.net/download)现成的设备(重点是 Ubiquiti NanoStation NSM5)组成，这些设备使用包含网状路由功能的定制固件进行闪存。

正如 Vice 的这篇文章提到的，NYC Mesh 是美国 750 个社区主导的宽带项目之一。其中许多使用更传统的配电线固定布线，但 NYC Mesh 完全专注于与[无线网状网络](https://en.wikipedia.org/wiki/Wireless_mesh_network)的无线(WiFi)链接。这有一个显而易见的好处，那就是在连接到[互联网交换点](https://en.wikipedia.org/wiki/Internet_exchange_point) (IXP)的超级节点上提供足够的带宽，以及一个高效的网状路由协议，就可以快速、轻松地连接新的客户端并扩展网络。

一般来说，使用 WiFi 和 RF 的明显缺点是，它们无法免受外部影响，如天气(下雨)、RF 干扰(包括来自其他 WiFi 站的干扰)，当然，如果没有直接的视线，范围也相当有限。在人口密集的城市，如纽约，这不是一个大问题，屋顶之间的短距离跳跃。