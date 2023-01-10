# 使用这款 Arduino 驱动的幻灯片旋转木马数字化您的幻灯片

> 原文：<https://hackaday.com/2022/11/15/digitize-your-slide-deck-with-this-arduino-powered-slide-carousel/>

如果你超过了一定的年龄，你可能还记得 Powerpoint 之前 35 毫米幻灯片放映的氛围。摇摇晃晃的屏幕正在展开，黑暗的房间，投影仪风扇的柔和嗡嗡声，屏幕上略微模糊的图片，以及投影仪加载下一张幻灯片时那种明确无误的咔嚓声。如今，你很难找到愿意支起屏幕，把房间变暗，只为了看几张照片的人，所以如果你还有幻灯片，你可能会想把它们数字化。如果你还留着你的投影仪，那么这甚至不需要那么困难，正如[斯科特·劳伦斯] [在他的最新项目](https://www.youtube.com/watch?v=x3WkqTZ-UXk)中所展示的。

[Scott]进行了一次设置，将 DLSR(在本例中为尼康 D70)直接连接到柯达 760 幻灯片转盘。这种连接是通过一个 3D 打印的适配器实现的，适配器的一侧安装在尼康的微距镜头上，另一侧则可以滑入旋转木马的镜头槽中。该适配器还带有一个瞄准相机接收器的红外发射器，以触发其远程快门释放功能。

旋转木马的原始光源被一个紧凑型 LED 工作室灯取代，这允许精确的亮度控制，当然与原始的白炽灯泡相比，它仍然很好，很酷。灯光、相机和转盘电机都通过一个由 Arduino Leonardo 驱动的中央用户界面进行控制，该界面可以自动推进转盘并指示相机拍照，从而免去了对大量幻灯片进行数字化的繁重工作。

[Scott]计划很快在 GitHub 上提供该软件和 STL 文件，这样任何人都可以将他们的投影仪变成数字化仪。然而，如果你放错了投影仪，[一个简单的 3D 打印幻灯片适配器也适用于小型幻灯片。](https://hackaday.com/2021/10/12/3d-printed-adapter-puts-slides-in-their-best-light/)

 [https://www.youtube.com/embed/x3WkqTZ-UXk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/x3WkqTZ-UXk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

