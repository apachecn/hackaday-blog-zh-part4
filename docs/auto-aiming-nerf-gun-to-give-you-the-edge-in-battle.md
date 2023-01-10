# 自动瞄准 Nerf 枪给你在战斗中的优势

> 原文：<https://hackaday.com/2021/06/03/auto-aiming-nerf-gun-to-give-you-the-edge-in-battle/>

有没有希望在你的下一场 nerf 战争中有一些机器人增强功能？好了，是时候翻翻零件箱，为自己造一把 [nerf 枪了，aimbot 内置于](https://www.youtube.com/watch?v=GoZubkaNvcE)，由【3Dprintedlife】提供。(视频，嵌在下面。)

这把枪从[【蛞蝓队长】的开源 nerf 枪的可怕目录](http://captainslug.com/)中借来的设计开始。[3Dprintedlife]修改了设计，在下部和上部之间包括一个双轴万向节，由一对步进电机通过 Arduino 驱动。对于自动瞄准，添加了一个连接到运行 OpenCV 的 Raspberry Pi 的相机模块。当用户半按下扳机时，OpenCV 将开始跟踪位于画面中心的任何东西，并主动调整万向节，以保持枪支对准物体，直到用户开火。触发机构由一对微型开关组成，它们启动一个伺服机构来释放扣机。它还能够跟踪移动目标或进入视野的任何人脸。

我们认为这是一个非常有趣的项目，在这个过程中可以学到很多东西。把它安装在遥控坦克上，你就可以在你的后院进行激烈的战斗。所有的文件都可以在 GitHub 上找到。

打一场漂亮的老仗，你永远不会嫌老。无论你是想成为一名狙击手、T2 机枪还是 T4 重型武器专家，每个角色都有适合的武器。

 [https://www.youtube.com/embed/GoZubkaNvcE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GoZubkaNvcE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

