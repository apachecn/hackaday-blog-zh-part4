# 你知道的，带激光的文本投影仪

> 原文：<https://hackaday.com/2019/02/14/text-projector-with-you-know-lasers/>

当[伊利亚萨姆的]激光文本投影仪首次出现时，我们错过了它，也许是因为原始文章是俄语的。然而，他最近[用英语](https://habr.com/en/post/438618/)转帖，这真的引起了我们的注意。你可以在下面看到一个简短的视频。

投影仪使用光栅扫描，光束通过网格图案中的每个点。这个设计使用了一个廉价激光笔的激光和一个旧激光打印机的回收镜模块。激光指针二极管被证明是有点弱，所以一个 DVD 激光器最终投入使用。DVD 电机也提供垂直扫描，这只是一个镜子的轻微摆动。蓝色药丸 CPU 提供所有的智能。你可以在 [GitHub](https://github.com/iliasam/LaserText) 上找到代码。

投影仪的尺寸相当有限，最大分辨率为 32×14。一些显示器使用用激光绘制的矢量方案。这是更明亮和更有能力的，但也更难安排，因为激光必须在一个复杂的运动中快速移动。光栅扫描更容易完成。

当激光即将开始击中垂直扫描镜时，光传感器会告诉 CPU。显然，有其他方法可以让镜子移动，但逻辑是一样的。

我们已经看到[伊利亚萨姆]对激光很感兴趣。他黑进了我们之前看过的测距仪、甚至 T2 的 3D 扫描仪。

 [https://www.youtube.com/embed/7rWy6-go_y8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7rWy6-go_y8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

