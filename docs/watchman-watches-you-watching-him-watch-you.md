# 守夜人看着你，看着他看着你

> 原文：<https://hackaday.com/2020/03/15/watchman-watches-you-watching-him-watch-you/>

在这一点上，社会已经有超过三十年的时间来适应蓝人乐团。也许这就是为什么我们对格雷厄姆·杰赛普的面部跟踪守望者感到不那么不安的原因。或者是因为它让我们想起了《T2:下一代星际旅行》中的数据。坦白地说，这实在是太酷了，不能被认为是令人毛骨悚然的。

[![](img/710458611a4e5c6d55501b421f491285.png)](https://hackaday.com/wp-content/uploads/2020/03/laser-eyeballs.png) 看守人通过安装在他额头上作为第三只眼睛的摄像头模块的视频来识别人脸。摄像头连接到一个戴着谷歌 AIY 视觉帽子的 Pi Zero。Pi 将面部位置转换为伺服位置，并将它们传送给位于额叶区域的 Arduino UNO，以相应地移动眼球和眼睑。

[格雷厄姆]起初在跟踪准确性方面有点问题，所以他暂时用 5 mW 的激光取代了瞳孔，并通过跟踪他头部的打印替身来校准它们，以避免烧毁他的视网膜。

这个项目建立在[Tjahzi] 和[Will Cogley]的电子眼球运动的基础上。我们只能想象如果看守人有一双[【威尔】的难以置信的逼真的眼球](https://hackaday.com/2019/10/29/peep-these-ultra-real-3d-printed-eyeballs/)会有多棒。不管怎样，我们都完全相信看守人会在未来几周捍卫我们微薄的卫生纸供应。休息之后，请查看一个简短的演示，以及[Graham]网站上的更多剪辑。

 [https://www.youtube.com/embed/xo8RRXo4SKw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xo8RRXo4SKw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Via [reddit](https://www.reddit.com/r/raspberry_pi/comments/ff78qs/i_made_a_robot_that_looks_at_you/)