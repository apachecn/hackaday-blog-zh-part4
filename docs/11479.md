# GPS？有了 Starlink，我们再也不需要它了！

> 原文：<https://hackaday.com/2021/10/10/gps-with-starlink-we-dont-need-it-any-more/>

为了找到你在地球表面的位置，在我们上方的轨道上有各种基于卫星的导航系统，移动电话等设备中的许多接收器芯片组可以使用不止一个。如果你不希望被一个国家政府的系统所束缚，现在有一个选择。虽然它不是来自官方来源，但却是其他东西的副作用。俄亥俄州立大学的研究人员[已经使用 Starlink 卫星宽带星座来获得定位](https://news.osu.edu/spacex-satellite-signals-used-like-gps-to-pinpoint-location-on-earth)，实现了声称的 8 米精度。

新闻稿中关于所用算法的信息很少，但由于它提到它依赖于对每个卫星的位置和速度的预先了解，我们猜测它在一次通过中测量每个卫星信号的多普勒频移，以确定相对位置，该位置可以通过其他 Starlink 飞船的后续观测来改进。

最有趣的是，虽然这项技术利用了 Starlink 网络，但它与服务本身没有任何联系。相反，这是对卫星的完全被动使用，尽管其精度比 GPS 可实现的精度低一个数量级，但它提供的定位仍然足够有用，足以满足大量用户的需求。

今年早些时候，英国政府收购了一家卫星宽带公司[,有报道称这可以填补他们退出欧洲伽利略计划](https://hackaday.com/2020/07/03/spacing-out-oneweb-rescue-starlink-base-stations-and-rocket-tests/)后留下的空白，这是一件有趣的事情。鉴于这一启示，也许他们终究还是发现了什么！

谢谢[Renze]的提示。