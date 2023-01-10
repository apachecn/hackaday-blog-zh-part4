# 伯德波特积木和墨鱼，一起作为吉他调音师

> 原文：<https://hackaday.com/2018/08/30/the-boldport-cordwood-and-cuttlefish-together-as-a-guitar-tuner/>

正如普通读者所知，在 Hackaday，我们是 PCB 作为一种艺术形式的狂热爱好者。来自[Saar Drimer]的 Boldport 套件在这个舞台上独树一帜，它们是最顶级的艺术品，展示精美，打造愉悦。

然而，一些人发现他们的 Boldport 工具包的问题是，它们太好了。你能拿它们怎么办，当忙于砍它们会破坏它们的美丽？【保罗·加拉格尔】有一个案例的答案，[他用了不止一个套件，而是两个作为吉他调音师项目](https://hackaday.io/project/160667-cordwood-i-guitar-tuner)。

它的核心是一个 Boldport 乌贼 ATmega328 开发板，它的显示器使用积木拼图作为 LED 阵列。所有的细节都可以在 GitHub 页面上找到[，这是他在 Instructables 上找到的](https://github.com/tardate/LittleArduinoProjects/tree/master/BoldportClub/cordwood/tuner)[Arduino 吉他调音师](https://www.instructables.com/id/Arduino-Guitar-Tuner/)的修改版本。特别是，他为驻极体麦克风使用了不同的前置放大器，以及具有 723Hz 截止频率的低通滤波器，以减少混淆 Arduino 算法的谐波含量。

结果是一个简单易用的设备，他的吉他每根弦都有一个 LED，你可以在下面的 YouTube 短片中看到。它加入了我们多年来精选的许多其他调谐器，其中只有一个是[这个带 MIDI-out](https://hackaday.com/2012/10/27/homebrew-guitar-tuner-also-includes-midi-out/) 的 ATmega168 供电项目。

 [https://www.youtube.com/embed/mtyyQwaxYTk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mtyyQwaxYTk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

