# 家酿双耳麦克风让你像人一样听

> 原文：<https://hackaday.com/2020/05/31/homebrew-binaural-microphone-lets-you-listen-like-a-human/>

我们人类可能没有超能力，但我们拥有的传感器套件仍然令人印象深刻。我们有双目视觉，可以自动聚焦并检测单个光子，皮肤上布满了触觉、热量和疼痛传感器，嗅觉可以检测到万亿分之一的化学物质。我们的听觉也非常强大，这让我们不仅可以听到 140 分贝范围内的声音，还可以相当精确地定位其来源，这要归功于我们头上的一对耳朵。

重现双耳音频捕捉能力是这个自制 3D 麦克风背后的想法。商业上可用的仿真头麦克风[完全超出了【LeoMakes】和大多数凡人的价格范围](https://daleproaudio.com/products/neumann-ku-100-dummy-head-binaural-stereo-microphone-system)，所以他的是用泡沫人体模型头和预制硅橡胶耳朵做的预算，你可以[买到现成的](https://www.amazon.com/Ear-Model-One-Pair-Artificial/dp/B075WTRYZP)，因为你当然可以。

一旦经过[梵高]处理，耳朵就会附着在泡沫头的两侧，将声音传递给微型驻极体拾音器。[Leo]艰难地认识到，这些小胶囊麦克风不能使用 48 伏的幻像电源，传统上是通过电缆连接到录音室麦克风；他用一个与麦克风引线并联的电阻解决了这个问题。一个滤波电容，一个平衡音频线路上冷线和地之间的 RC 网络，以及一个由脱焊编织巧妙形成的屏蔽，解决了 RF 噪声问题。

休息后的视频显示了构建和测试结果，戴上耳机后非常有说服力。如果你想建立自己的，但需要了解更多关于平衡音频和幻像电源，我们有一个关于主题的简短入门[可能会有所帮助。](https://hackaday.com/2018/07/27/the-hot-and-cold-of-balanced-audio)

 [https://www.youtube.com/embed/eh_hX4Q-Si0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eh_hX4Q-Si0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

