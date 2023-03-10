# 通过 GitHub 的空中更新推送 ESP32

> 原文：<https://hackaday.com/2022/12/13/push-esp32-over-the-air-updates-from-github/>

假设你正在做一个 ESP32 项目，要送给你奶奶；她只要插上电源，它就会自动监控她家植物的水位。但是您发现固件中有一个严重缺陷，需要更新它。她会寄回去吗？你会带她通过 Arduino IDE OTA 下载更新吗？最简单的方法是计划和使用类似于[esp _ ghota 的东西，一个由[Justin Hammond]开发的 ota 框架](https://github.com/Fishwaldo/esp_ghota)。

OTA(空中下载)更新是 ESP32 的一个奇妙特性，我们已经覆盖了使它变得容易的库。但是与那些早期的项目相比，esp_ghota 采取了不同的方法。它不是托管一个可以存放二进制文件的 web 服务器，而是着眼于 GitHub 版本。[Justin]必须包含一个流 JSON 解析器，因为 GitHub API 响应往往很强大。工作流程很简单，在 GitHub 上推一个新的 commit 到你的主分支，动作就会触发，构建几个不同的版本。你奶奶家的植物浇水提醒会经常检查是否有新版本推出，并且可以在 littlefs、fatfs 和 spiffs 文件系统上回滚更新。

这是一个令人难以置信的项目，我们怀疑它将对许多人更新他们的项目非常有用。[Justin]甚至包括一个 GitHub 动作示例和一个 ESP32 项目示例。