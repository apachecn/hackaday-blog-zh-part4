# 你的电影声音太大了吗？听不到对话？这个电路可以有所帮助。

> 原文：<https://hackaday.com/2021/09/29/is-your-movie-too-loud-cant-hear-the-dialogue-this-circuit-can-help/>

每个人都喜欢看电影，也就是说，只要你能听到屏幕上的人物在说什么。[GreatScott]在观看 BladeRunner 2049 时发现第二部分很难，[所以他设计了一个自动音量调节器来辅助](https://www.instructables.com/Automatic-Volume-Adjuster-for-LOUD-MOVIE-MUSIC/)。

在高层次上，解决方案相当简单；当电影中播放很响的音乐时，调低音量。挑战在于如何真正做到这一点。第一步是控制音量。为了避免修改或损坏他的音响系统，[GreatScott]选择通过红外模拟遥控器的音量信号。使用 Arduino 非常方便的非远程库及其内置的解码功能，他能够用自己的红外 LED 识别和复制信号。

这个过程的第二步是测量电影的音量。[GreatScott]通过麦克风和放大器电路实现了这一点，然后将其连接到构建核心的 Arduino Pro Micro 的模拟引脚之一。由于被采样的音频可能具有高达 20 kHz 的频率，因此 ADC 预分频器必须从其标准值进行调整，该值仅允许在低于 5 kHz 的频率下进行测量。

第三步是编写算法来检测嘈杂的音乐并相应地调整音量。Arduino 将测量音频，直到检测到大于死区值的声音，该值由两个板载电位计中的一个设定。这将触发 Arduino 启动一个计时器，查看超过上限的频率。如果只是一两声偶尔的巨响(像尖叫、拍手、吹口哨等。)Arduino 不会采取任何行动，但是快速连续的多个大噪音将会触发红外 LED 上的音量降低命令。第二个电位计允许调整这个计时器的临界值，这样你就可以根据电影使系统反应更快或更慢。

一旦检测到声音下降到临界值以下，Arduino 就会认为电影回到了对话状态，并将音量提高到之前降低的倍数，让您回到理想的音量。

也许你是那种更关心电影视觉效果而不是声音的人。在这种情况下，[这种电子纸电影显示](https://hackaday.com/2020/08/23/e-paper-display-shows-movies-very-very-slowly/)将非常适合给你时间欣赏每一帧！

 [https://www.youtube.com/embed/j1V2I-otdzk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/j1V2I-otdzk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

