# 机器人让远程同事享受办公室恶作剧

> 原文：<https://hackaday.com/2019/10/17/robot-allows-remote-colleagues-to-enjoy-office-shenanigans/>

[Esther Rietmann]和同事们制造了一个[远程呈现机器人](https://tryolabs.com/blog/hackathon-robot-remote-work-iot-computer-vision/)，让在家工作的队友在办公室里有一个虚拟但实际的存在。远程呈现机器人就像安装在 Roomba 上的平板电脑，除了音频/视频连接之外，还提供运动功能。它是在 48 小时的黑客马拉松中建造的，在引擎盖下有点粗糙，并且错过了一些功能，例如双向视频馈送。但总的来说，它基本上做到了人们对这种设备的期望。

主体结构是用廉价的铝型材和板材建造的。Raspberry Pi 是电子硬件的核心，由伺服安装的 Pi 摄像头和扬声器麦克风对负责视频和音频。两个 DC 电机由 Pi 控制的 H 桥驱动，一个空转脚轮作为第三个轮子。整个装置由一个电源组供电。缺少的一个重要东西是 HDMI 显示器，它可以显示来自远程笔记本电脑摄像头的视频。这可能是由于时间限制，但是这个特性作为未来的升级应该不会太难。双方都能看到对方是很重要的。

该软件是围绕 WebRTC 协议构建的，来自 [UV4L](https://www.linux-projects.org/uv4l/) 的 [WebRTC 扩展](https://www.linux-projects.org/uv4l/webrtc-extension/)完成了大部分繁重的工作。UV4L 流服务器不仅提供自己的内置 web 应用程序和服务，还在另一个端口上嵌入了通用 web 服务器，允许用户运行和部署自己的自定义 web 应用程序。这使得[Esther Rietmann]的团队能够构建一个基本但功能强大的前端，从远程接口传输数据以控制机器人。远程计算机运行 Python 控制脚本，作为系统服务运行，以控制驱动电机和摄像机伺服。

该团队还尝试添加基本的物体、手势和动作识别功能。这是使用 [PoseNet](https://github.com/tensorflow/tfjs-models/tree/master/posenet) 完成的，这是一种机器学习模型，允许在浏览器中使用 TensorFlowJS 进行实时人体姿势估计，允许他们展示一些姿势检测能力。这可以作为机器人的“跟我来”功能。

另一个缺失的功能是大多数其他商业远程呈现机器人都有的传感器套件，用于避免共谋、物体检测和感知，如微型开关、红外/超声波探测器、飞行时间相机或激光雷达。给机器人增加一个或几个传感器是相对容易的。

如果你想为自己构建一个，可以看看 Github 上的[代码库](https://github.com/tryolabs/vierjavibot)和下面的视频。

 [https://www.youtube.com/embed/ujTBNP5BuRQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ujTBNP5BuRQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/lKbGat8Bfus?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lKbGat8Bfus?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

