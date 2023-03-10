# 您的 PI 的 Web API

> 原文：<https://hackaday.com/2019/10/01/a-web-api-for-your-pi/>

有许多方法可以将一个项目连接到互联网上，并且有许多基于互联网的服务可以处理与硬件的对话。但对于普通人来说，最普遍的因特网协议可能是 web 浏览器，而最容易访问的编程环境之一就在其中。要是稍微懂点 HTML 和 Javascript 的人能在他们的 Raspberry Pi 上找到 GPIO 引脚就好了！

如果这是你的愿望，那么[维克多·里贝罗]的 rpia pi 就能提供帮助。顾名思义，它是你的 Raspberry PI 的 API，特别是它为 Pi 的 GPIO 库提供了一个简单的 web 可访问的端点包装器[，从这里可以访问它的扩展端口管脚。通过在 Pi 的 web 服务器的地址上精心设计一个简单的路径，每个 pin 都可以被读取或写入，虽然它对于该平台来说不是最快或最完善的硬件接口，但可以使它成为最容易访问的接口之一。](https://github.com/victorqribeiro/rpiapi)

安全性来自 Apache 通过`.htaccess`文件提供的密码保护目录，因此建议用户非常仔细地考虑将其连接到公共 IP 地址的含义。但是对于非安全专家来说，它仍然有潜力成为一个非常有用的工具，可以用来控制小型单板计算机的硬件。这并不是第一次尝试这种想法，因为我们已经在 Pi 的早期看到过[一个 PHP 示例](https://hackaday.com/2012/05/05/controlling-raspberry-pi-expansion-pins-with-a-web-interface/)以及一个[依赖于 MySQL](https://hackaday.com/2013/02/02/easy-web-interface-with-gpio-access-runs-on-raspberry-pi/) ，但这似乎是一个比其他更简单的选择。