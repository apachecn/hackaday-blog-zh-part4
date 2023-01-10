# 真的还是假的？机器人用人工智能寻找沃尔多

> 原文：<https://hackaday.com/2018/08/30/real-or-fake-robot-uses-ai-to-find-waldo/>

过去几周，一些科技网站报道了一种机器人，它可以在“瓦尔多在哪里”的书中找到并指出瓦尔多。由广告公司 Redpepper 设计和建造。机器人手臂是 UARM 金属，树莓皮控制表演。

罗技 c525 网络摄像头捕捉图像，由 Pi 使用 OpenCV 进行处理，然后发送到谷歌基于云的 AutoML 视觉服务。AutoML 使用 Waldo 的大量图像进行训练，这些图像用于尝试模式匹配。如果发现一个模式，坐标就会被传送到皮尤姆，UARM 就会准确地指出沃尔多。

虽然这是一个完全可信的项目，但我们不得不承认一些事情引起了我们的偏见。罗技 c525 的视野(FOV)为 69°。虽然我们没有 UARM 金属的尺寸，但看起来相机在空中不到一英尺。亚马逊声明“Waldo Delux Edition 在哪里”是 10 英寸 x 0.2 英寸 x 12.5 英寸。这意味着打开的书将是 10 英寸×25 英寸。机器人将很难在一张图像中对这么大的表面成像。更重要的是，c525 是一个 720p 的摄像头，所以没有太多的像素密度来进行模式匹配。最后，还有机器人用来指出沃尔多的橡胶手。难道那只手不会挡住左边至少一部分的镜头吗？

我们还不会跳出来说这是假的——机器人完全有可能拍摄了图像的马赛克，并用它来进行模式匹配。红辣椒可能使用了一点电影魔法，使这个过程更有趣。你怎么想呢?请在评论中告诉我们吧！

 [https://www.youtube.com/embed/-i7HMPpxB-Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-i7HMPpxB-Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

