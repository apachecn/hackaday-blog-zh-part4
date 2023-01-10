# GitHub ESP32 OTA 更新，现在是 MicroPython 风格

> 原文：<https://hackaday.com/2022/12/23/github-esp32-ota-updates-now-in-micropython-flavor/>

如果你能用一个单一的代码库来更新你所有的小型网络黑客，那不是很好吗？几周前，我们写了一个项目，使用 ESP32 C SDK 从 GitHub 自动下载对 ESP32 的 OTA 更新。[Pascal]在评论中问道，“但是 MicroPython 呢？”发出挑战后，[turptax]编写了`ugit.py`–[一个简单的库，将所有来自公共 GitHub Python repo 的代码直接镜像到运行 Micropython](https://github.com/turfptax/ugit) 的 gizmo 上。

[阻尼]写了关于[Senko](https://github.com/RangerDigital/senko)的文章，这是另一个做类似事情的库，但是那时[turptax]已经完成了。嘭！部分速度是因为 MicroPython 包含了完成工作所需的一切——[解析流 JSON 是原始黑客的难点](https://hackaday.com/2022/12/13/push-esp32-over-the-air-updates-from-github/)。MicroPython 让这些事情变得简单。

对于拥有一小群独立设备的黑客来说，这是一个绝妙的主意。因为`ugit.py`本身相当简单易读，如果你需要定制它来完成你自己的投标，那也没问题。请确保当您存储您的 WiFi 验证信息时，它不会公开显示。([turptax]，我可以登录你家的 WiFi 吗？)

[turptax]会用这个做什么？我们猜测它将会把代码部署到[他那令人敬畏的开放式肌肉感应装置](https://hackaday.com/2022/10/20/forearm-muscle-contraction-sensor-is-useful-component-for-open-source-prosthetics/)上。我们要用它做什么？为姻亲准备的闪闪发光的圣诞装饰品，现在可以远程更新，他们甚至不用学习什么是“回购”。

 [https://www.youtube.com/embed/UX87SrdqIoc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UX87SrdqIoc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

