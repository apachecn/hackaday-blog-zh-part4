# 热门话题 Python 中的位置可视化

> 原文：<https://hackaday.com/2019/12/05/the-heat-of-the-moments-location-visualization-in-python/>

你有没有看过谷歌这些年来收集的关于你的所有信息？当然，这是假设你有一个谷歌账户，但如果你有一个安卓设备，并且隐私问题被便利性所压倒，这是很正常的。考虑到 GPS 现在是一个非常标准的智能手机功能，你不应该感到惊讶，你的整个位置历史很可能也是收集数据的一部分。因此，除非你在过去选择退出不断变化的设置迷宫，否则现在为时已晚，数据已经存在——就这样。那么，我们不妨利用它来为我们自己谋福利，想象一下我们在那里得到了什么。

位置数据自然需要地图作为可视化方法，[luka1199]认为还有什么比用 Python 编写的交互式地理热图[更好，它显示了你生活中的所有热点。该脚本围绕](https://github.com/luka1199/geo-heatmap)[的](https://python-visualization.github.io/folium/)图书馆构建，读取你可以从[的谷歌外卖服务](https://support.google.com/accounts/answer/3024190?hl=en)请求的位置历史的 JSON 转储，并将结果热图叠加在 OpenStreetMap 世界地图上，准备好供你在浏览器中探索。作为 Python，这几乎就是全部，这使得[Luka]的脚本也是一个很好的起点，可以让你自己尝试一下 leav 和地图可视化。

虽然只是简单地看着地图并记住你的生活带你去过的地方本身就很有趣，但你也可能在替代路线规划中实现一些时间优化的潜力，或利用它将你最后的公路旅行路线变成一件艺术品。只是，无论你做什么，都要小心不要意外[泄露一些秘密军事设施的位置](https://hackaday.com/2018/01/28/opt-out-fitness-data-sharing-leads-to-massive-military-locations-leak/)。

[通过 [r/dataisbeautiful](https://www.reddit.com/r/dataisbeautiful/comments/e2zv4w/i_wrote_a_python_script_that_generates_a_geo/)