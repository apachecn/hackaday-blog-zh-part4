# 为卓越性能打造的电视环境照明

> 原文：<https://hackaday.com/2021/06/11/tv-ambient-lighting-built-for-awesome-performance/>

[AndrewMohawk]这些年来看到了各种各样的电视环境照明系统，它们的一个共同点是它们都没有达到他的高标准。有了黑客贸易的工具，他着手建立一个自己的 Ambilight 型系统，真正交付货物。

开发过程充满了障碍和死胡同，但是安德鲁坚持了下来。在解决了 HDCP 和 HDMI 分割器的恼人问题后，他终于能够用 Raspberry Pi 来捕捉传到电视上的视频，并使用 OpenCV 来确定屏幕周围片段的颜色。从那时起，很容易将数据发送到电视后面的一串可寻址 RGB LEDs，以产生所需的效果。

对于所有的辛勤工作，[Andrew]得到的回报是一个环境照明系统，它以健康的 20fps 运行，可以与任何插入电视的 HDMI 视频信号配合工作。它甚至可以自动缩放以不同的纵横比拍摄的视频内容，因此环境显示总是会拾取视频内容的边缘。

安装了 270 个 led，结果是一个令人难以置信的平滑和流畅的环境显示，我们希望在家里有。你也可以建一个，[因为【Andrew】在 Github 上共享了所有代码。](https://github.com/AndrewMohawk/Aurora)作为额外的奖励，[他还给了这个系统一个音频可视化器](https://www.youtube.com/watch?v=f1FLTHJ_s1s)，并用一些*街灯宣言*进行测试，这是有史以来在地球上漫游的最伟大的第三波 ska 乐队。第四波浪潮仍未到来，但我们仍抱有希望。

我们以前见过很多这种类型的黑客；[最令人印象深刻的一个黑客入侵智能电视，让它自己进行视频处理](https://hackaday.com/2021/05/20/roku-tv-hacked-to-run-philips-ambilight-setup/)。休息后的视频。

 [https://www.youtube.com/embed/gOFcNsSOUs8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gOFcNsSOUs8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/f1FLTHJ_s1s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/f1FLTHJ_s1s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

