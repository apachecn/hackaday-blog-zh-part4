# 名字石帮助你问候同事

> 原文：<https://hackaday.com/2019/09/16/name-stone-helps-you-greet-coworkers/>

当开始一份新工作时，记住同事的名字可能是一项艰巨的任务。做好这一点是建立牢固职业关系的关键。[Ahad]注意到[Marcos]正在努力解决这个问题，所以[建造了名字石头](https://www.youtube.com/watch?v=Wb7zlCrwNiE)来帮助解决这个问题。

石头这个名字由一些强大的硬件组成，包裹在一个 3D 打印的盒子里，让人想起奇异博士的 Agamotto 之眼。在里面，有一个 Jetson Nano——一个围绕机器学习任务构建的任何项目的优秀平台。它与麦克风和摄像头相结合，从环境中收集数据。

[Ahad]然后开始训练神经网络来帮助完成基本的识别任务。拍摄同事的视频，然后使用 PyTorch 将这些帧用于训练卷积神经网络。类似地，一系列的音频片段被用来再次训练一个网络，通过他们的声音来识别个人，使用 MFCC 技术。激活石头后，该设备将捕捉图像或简短的声音片段，并处理数据以识别目标同事并提醒【马科斯】他们的名字。

这是一个非常有用的项目，给新员工，帮助他们过渡到新的工作场所。当然，[普适的面部识别技术确实存在一些弊端。](https://hackaday.com/2019/01/02/your-face-is-going-places-you-may-not-like/)休息后的视频。

 [https://www.youtube.com/embed/Wb7zlCrwNiE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Wb7zlCrwNiE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

