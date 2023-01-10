# 打破你的示波器的带宽障碍

> 原文：<https://hackaday.com/2019/01/24/break-your-scopes-bandwidth-barrier/>

示波器带宽是一件棘手的事情。100 MHz 示波器将具有 100 MHz 正弦波的规定衰减(70%)。不过，这并不是全部情况，因为我们并不总是测量正弦波。例如，一个 100 MHz 的方波将具有 100 MHz、300 MHz 的正弦波分量和其他奇次谐波。然而，这并不是说 100 MHz 的示波器不能显示更高频率的东西——它只是没有获得正确的 y 轴。是德科技的[Daniel Bogdanoff]决定跳出框框思考，于是[制作了一个关于使用超出其带宽规格的示波器的视频](https://www.youtube.com/watch?v=S8eSDjyRceg)。你可以在下面看到这个视频。

[Daniel]称之为“规范攻击”,但它们并不是真正的范围攻击。它们只是不关心作用域额定带宽的方法。在这篇特殊的技术说明文章中，他展示了使用 70 MHz 示波器触发电路的频率计数器实际上可以读取高达 410 MHz 的频率。一个 100 兆赫的示波器能读出几乎 530 兆赫的信号。

有趣的是，频率计数器从示波器的触发电路工作，它有自己的信号路径，不经过模数转换器。当然，您的示波器可能还具有频率测量功能，可以读取屏幕上的轨迹。这可能也行得通，因为你并不真的关心信号衰减了多少，只是为了读取频率。不管怎么说，这是一个放在你包里的巧妙的技巧。

老实说，我们很惊讶示波器制造商没有把这作为规范的一部分来描述和评价。我们非常确定在 70 MHz 范围内的普通探头在 400 MHz 时表现不像承诺的那样，所以这可能是它们不表现的部分原因。

如果你有一些闲钱，你可以买一个 110 GHz 的示波器，这对任何人来说都足够了。当然，示波器不仅仅是它的带宽，但是如果你想了解更多关于[测试带宽](https://hackaday.com/2016/10/05/choosing-a-scope-examining-bandwidth/)的信息，我们已经在一些新老示波器上做了。

 [https://www.youtube.com/embed/S8eSDjyRceg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/S8eSDjyRceg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

