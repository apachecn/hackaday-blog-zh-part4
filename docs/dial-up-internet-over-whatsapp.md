# 通过 WhatsApp 拨号上网

> 原文：<https://hackaday.com/2022/11/13/dial-up-internet-over-whatsapp/>

当我们从 Supercon 2022 返回时，我们注意到许多航空公司提供免费的机上信息。虽然抱怨座位大小的信息很方便，但这并不像上网那样令人兴奋。在空中，我们想知道通过消息传送建立互联网连接有多难。有趣的是，[Aleix Rodríguez Alameda]有一个项目[正是通过 Whatsapp 隧道传输流量来实现这一点。](https://github.com/aleixrodriala/wa-tunnel)

在[Aleix]的案例中，手机运营商在南美旅行时对互联网数据非常吝啬，但通常会提供无限制的 WhatsApp 数据。因此，提前设置了两个帐户。服务器位于一个帐户上，充当更广泛的互联网的代理，并侦听服务器帐户的消息。然后，当处于受限访问设置时，客户端与 WebSocket 连接并发送消息。将 WhatsApp 消息转换为客户端可以使用的互联网连接的真正技巧是从本地 nodeJS web 服务器公开一个端口。它通过 WebSocket 连接到 WhatsApp API，然后充当代理。然后，使用 curl 或 Firefox 设置流量通过该端口重定向。

数据包被拆分是为了防止你发送太多消息，因为在他们的测试中，[Aleix]的账户很快就被封禁了。你不应该期待非常快的速度，因为 300kbps 在测试期间是非常典型的，根据维基百科，[大约是拨号通过 V.44 压缩](https://en.wikipedia.org/wiki/Dial-up_Internet_access)获得的速度。

这大约与通过 NRF23L01 无线电传输的 TCP/IP 的速度相同。