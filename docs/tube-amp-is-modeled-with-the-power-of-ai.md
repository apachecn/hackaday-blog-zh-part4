# 电子管放大器是用人工智能的力量建模的

> 原文：<https://hackaday.com/2020/10/11/tube-amp-is-modeled-with-the-power-of-ai/>

硬件有某种魔力和独特性，尤其是在音频方面。电子管放大器众所周知，深受音频发烧友和音乐家的喜爱。然而，这种独特性也带来了代价，即 gear 会占用空间，并且不能超出其设计用途进行配置。[keyth72]已经决定自己承担起[重现小芬德布鲁斯小管吉他放大器](https://github.com/keyth72/SmartGuitarAmp)的流畅声音。但它没有使用硬件或标准音频软件，而是使用了人工智能的魔力。

在某些方面，重新创造一个转变正是人工智能的设计目的。有一个清晰和可记录的输入和一个类似的输出。在这种情况下，[keyth72]录制了几个吉他会话，吉他音频通过他们想要重新创建的设备发送。使用 WaveNet，他们创建了一个模型，将转换实时应用于输入音频。增益和均衡器旋钮在模型本身之外处理，以保持简单。GitHub 页面包含了如何训练你自己的模型[的说明。](https://github.com/keyth72/PedalNetRT)

虽然该模型只是简单地近似真实的硬件，但听起来仍然令人印象深刻，也许下次你需要你的[自制放大器](https://hackaday.com/2018/07/30/a-stereo-tube-amp-for-less-than-5/)或[吉他踏板](https://hackaday.com/2017/12/20/taking-a-guitar-pedal-from-concept-into-production/)的特定声音时，你可能会用你的电脑来代替。

 [https://www.youtube.com/embed/I9DElOaZvHo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/I9DElOaZvHo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

