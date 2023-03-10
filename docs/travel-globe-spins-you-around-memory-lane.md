# 旅行地球仪让你在记忆里旋转

> 原文：<https://hackaday.com/2020/07/04/travel-globe-spins-you-around-memory-lane/>

谈到旅游纪念品，我们都有自己的偏好——每当我们看到它时，都会想起过去假期的记忆和感受的小东西，无论是陈词滥调的冰箱贴，一些当地特产，还是我们拍的照片集。但也有一些旅程无法总结成一个单一的项目，可能需要更多的创造力。对[Jonathan]来说，是去年的环球旅行让他和[Maria]去了欧洲、亚洲和大洋洲的很多地方，他发现了一个很好的记忆方式:[一个互动的激光切割旅游地球仪，显示了他们去过的所有地方](https://www.robopenguins.com/icosahedron-travel-globe/)。

用激光切割机建造一个球体当然有点棘手，所以[Jonathan]选择了二十面体形状的[Dymaxion map](https://en.wikipedia.org/wiki/Dymaxion_map)投影(想象一个大的 d20 骰子),并在上面燃烧世界。地球仪内部是一个 ESP8266，一个 MPU-6050 IMU，以及一束使用 [WLED](https://github.com/Aircoookie/WLED) 库照亮旅行地点的 LED。他从 IMU 获取数据，定制了 WLED 库来确定地球仪的位置，并以不同的颜色突出显示面向顶部的位置。

虽然这本身就已经是一个很好的纪念品，但[乔纳森]并没有就此止步。使用谷歌的 *My Maps* 服务，你可以创建带有自己兴趣点的自定义地图，并附上照片等，ESP8266 还可以将旅行地图作为网页。将 IMU 数据提供给处理地图 API 的 JavaScript 代码，地球仪本身现在也可以作为输入设备来控制虚拟地图。因此，每当地球仪被物理旋转以突出显示某个位置时，网页的地图就会聚焦到相同的位置，并随机显示他们在那里拍摄的照片。看看下面的视频，看看这一切都在行动中。

这是一个很好的方式来回忆一次难忘的旅程，即使是多年以后，虽然它可能不灵活，但它似乎是一次值得一个独立设备的旅行。另外，Dymaxion 地图绝对是一个有趣的投影——所以这里有一个可折叠的地图。如果你喜欢在地球仪上追踪东西，[这里有一个显示国际空间站](https://hackaday.com/2019/12/10/globe-lamp-tracks-the-iss-for-you/)位置的地图。

 [https://www.youtube.com/embed/zYjybxHBsHM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zYjybxHBsHM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

