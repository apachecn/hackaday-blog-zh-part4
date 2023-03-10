# 用 Arduino 模拟双耳听觉

> 原文：<https://hackaday.com/2021/11/16/binaural-hearing-modeled-with-an-arduino/>

你不是偶然有两只耳朵的。[Stoppi]有一个关于这个的很棒的帖子，还有一个视频，你可以在下面看到。(原文是德文，但这就是翻译的目的。)拥有两只耳朵的意义在于，你每只耳朵从略微不同的角度和距离接收音频信息，你惊人的大脑可以从这些数据中推断出大量的空间信息。

在 Arduino 演示中，廉价的麦克风板代替了你的耳朵。伺服电机指向声音的方向。这将是一个很好的万圣节道具或噪音敏感的安全摄像头的噱头。

就数学而言，如果你知道声速、传感器之间的距离以及其他一些数据，你最终会得到一个相当简单的三角学问题。用非数学术语来说，很容易理解这种方法的工作原理。如果声音同时传到两个麦克风，那么它一定是从正前方传来的。如果它先碰到左边的麦克风，它一定离那个麦克风更近，反之亦然。如果声音与两个麦克风都在一条直线上，但更靠近左侧，时间延迟将完全是由于传感器之间距离上的声速造成的。如果时间小于这个时间，声音一定在两者之间。

麦克风模块有模拟输出和数字输出。如果声级超过电位计设定的限值，数字输出触发。通过使用这些模块，电路变得简单。只有一个阿鲁迪诺，两个模块，和伺服电机。

现在想象一下，你希望所有这些空间细节都通过你的耳机呈现出来。录制双耳音频是一件事。有兴趣可以 [3D 打印一个虚拟头](https://hackaday.com/2015/06/28/3d-printing-binaural-microphones/)。我们已经看过几次[这样的项目](https://hackaday.com/2020/05/31/homebrew-binaural-microphone-lets-you-listen-like-a-human/)。

 [https://www.youtube.com/embed/-67zhaJvJVQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-67zhaJvJVQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

