# 用计算机视觉打造自己的自拍无人机

> 原文：<https://hackaday.com/2019/06/30/build-your-own-selfie-drone-with-computer-vision/>

在 2013 年末和 2014 年初，在无人机革命令人兴奋的日子里，有一个杀手级应用——自拍无人机。自拍杆本身已经成为一个笑话，但自拍无人机为科技世界注入了一股新鲜空气。坐立不安纺纱尚未发明，所以这是我们所有的。然而，自拍无人机的时代还没有到来，尽管预订了 4000 万美元，Lily 相机无人机却成了诉讼的对象，而不是联邦航空局的罚款。

技术不断进步，现在你可以打造自己的自拍无人机。[这正是[geaxgx]所做的](https://www.youtube.com/watch?v=RHRQoaqQIgo)，尽管这一构建使用了带有定制软件的现成无人机，而不是从头开始构建一切。

硬件方面，[这是一台 Ryze 泰洛](https://www.ryzerobotics.com/tello)，一台 100 美元的小型四轴飞行器，带有前置摄像头。有了正确的库，你可以将图像传输到计算机，并将飞行命令发送回无人机。是的，自拍无人机的所有处理都发生在非飞行计算机上，因为计算机视觉需要处理能力和电池寿命。

该软件来自 [CMU 的 OpenPose 库](https://github.com/CMU-Perceptual-Computing-Lab/openpose)，这是一个用于检测身体、面部或手部的实时解决方案。有了这个，[geaxgx]就能够悬停无人机，并让他的脸保持在相机画面的中间。虽然没有涉及无人机的运动——无人机只是悬停和左右旋转——但它是一个没有棍子的飞行自拍杆。你可以查看下面的视频，也可以在这里查看[【geaxgx】的 GitHub 上的所有代码。](https://www.youtube.com/redirect?q=https%3A%2F%2Fgithub.com%2Fgeaxgx%2Ftello-openpose&v=RHRQoaqQIgo&redir_token=uMAkFGCEkcWXVWRjulk-unFb9zx8MTU2MTgyNjAwMUAxNTYxNzM5NjAx&event=video_description)

 [https://www.youtube.com/embed/RHRQoaqQIgo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RHRQoaqQIgo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

