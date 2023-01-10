# 一个巨大的按钮让他们全部静音

> 原文：<https://hackaday.com/2021/07/20/one-giant-button-to-mute-them-all/>

今年的第二轮 Hackaday 奖即将结束，我们要求您想出让在家工作的生活焕然一新的方法。这里有一个我们可能都可以使用的按钮——[一个大的紧急静音按钮，也可以通过额外的点击](https://hackaday.io/project/180695)关闭视频。你知道，万一你的孩子或你的室友决定光着身子走来走去。

[Colin Russell-Conway]的与软件无关的静音按钮使用了一个 Seeeduino Xiao 和旋转编码器，加上三个动量，这赋予了它作为媒体控制器的第二个功能。当静音打开时，两大块 LED 灯条变得闪闪发光，否则会一直亮着，并根据视频会议类型进行颜色编码——蓝色表示 Zoom 和 Starleaf，绿色表示 Webex，紫色表示团队。

[Colin]创建的配套应用程序使用 Windows Management Instrumentation(WMI)来检查哪个程序控制麦克风。每当按下静音按钮时，该应用程序都会记录下当前节目的焦点，切换到活动的视频会议，将其静音，然后切换回 reddit 或 twitch 或当孩子开始在浴室里尖叫时你所关注的任何内容。休息后请欣赏演示。

我们中的一些人喜欢在视频会议结束后庆祝一下。对于那些人，有[拉链出口](https://hackaday.com/2020/12/28/a-pull-chain-to-end-your-zoom-pain/)。

 [https://www.youtube.com/embed/qabKWWq_SRY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qabKWWq_SRY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[hack adayprize 2021](https://prize.supplyframe.com)主办单位:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)