# 小树是圣诞热的温度计

> 原文：<https://hackaday.com/2019/12/24/tiny-tree-is-a-thermometer-for-christmas-fever/>

厌倦了为节日展示制作 RGB LEDS 动画的常用方法了吗？[用一种非时髦的方式来使用时髦怎么样](https://www.instructables.com/id/The-Google-Trends-Powered-Christmas-Tree/)？

屈服于日益增长的节日狂热，买了一棵最可爱的小圣诞树。一棵特别的树应该有特别的装饰，所以他们用新像素把它包装起来，这些新像素可以一个接一个地从红色变成绿色，然后再变回绿色。这就是时尚的由来:它们变化的速度取决于“圣诞节”作为搜索词的受欢迎程度。

新像素由 Raspberry Pi 3B+控制，它使用 PyTrends 每小时从 Google Trends 获取一次值。该服务返回一个介于 0 到 100 之间的值，其中 100 表示该搜索词非常受欢迎，0 表示可能是一月下旬。每个新像素都连接到一个半透明印刷礼品盒的底部，这个礼品盒在漫射光线方面做得很好。

你知道圣诞树倾向于留到新年吗？由于奖励派对模式，这一次可能会比平时持续更长时间。按下盒子上巧妙伪装成礼物的 arcade 按钮，灯光会以极快的速度从红色变为绿色，然后再变回红色，同时里面的扬声器会播放你选择的派对歌曲。休息之后，请务必观看下的~~演示/构建视频。~~

这棵小树怎么会变得更特别呢？嗯，[一个旋转平台](https://hackaday.com/2019/12/15/old-christmas-tree-gets-a-new-spin/)也没坏处。

 [https://www.youtube.com/embed/JdYQyiK1drk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JdYQyiK1drk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

