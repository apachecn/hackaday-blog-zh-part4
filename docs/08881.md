# 从 Miata 发动机中删除凸轮轴

> 原文：<https://hackaday.com/2021/02/24/deleting-the-camshafts-from-a-miata-engine/>

无凸轮汽车发动机的想法已经出现了一段时间，但迄今为止仅限于原型和超级汽车。[Wesley Kagan]已经做了一段时间的 DIY 版本，并成功地将马自达 Miata 改装成无凸轮气门系统。休息之后看视频。

汽车制造商已经有许多 R&D 项目来[消除凸轮轴](https://hackaday.com/2016/02/16/where-are-all-the-camless-engines/)以实现独立的气门正时，但该技术只在科尼赛克 hypercars 上有过商业应用。[韦斯利]在一辆便宜的[单缸港口货运发动机](https://hackaday.com/2020/12/17/hypercar-valve-technology-on-a-harbour-freight-engine/)上开始了这次冒险，并证明了基本概念，所以他决定升级到一辆实际的汽车。他首先采购了一个废车场发动机头进行改装，并作为完整项目车上发动机头的替代物。一个现成的双作用气缸安装在每个阀门上，并通过一个定制的适配器连接到阀杆上。双作用气缸允许阀门在气压下打开和关闭，但[Wesley]仍然增加了轻型复位弹簧，以便在气动系统出现任何问题时保持阀门关闭。

控制器是一个 Arduino，它接收来自工厂曲轴的定时信号，并通过 MOSFETs 操作气动电磁阀。在将新的头部和控制箱安装到 Miata 后，花了几天的时间进行调整，以使发动机平稳运行。最初的测试是在他的车库中使用压缩机进行的，但这被一个安装在 Miata 行李箱中的小型压缩机和储气罐所取代，用于驾驶测试。

虽然气动系统在短途试驾中表现良好，但压缩机噪音很大，增加了几个故障点。[Wesley]还在研究一个电磁驱动系统，这将需要电池和交流发电机提供更多的电流，但他认为与压缩空气相比，这是一个更好的长期解决方案。然而，他仍在努力寻找符合要求规格的螺线管。

[Wesley]将开放他所有的设计和代码，希望其他人能够修改和改进设计。结果可能会非常有趣，所以我们希望围绕这些无摄像头转换开发一个社区。

 [https://www.youtube.com/embed/E9KJ_f7REGw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/E9KJ_f7REGw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/_Ljwk-ByvjI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_Ljwk-ByvjI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

