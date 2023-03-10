# 一个易于制作的 Pi 驱动的口袋密码伙伴

> 原文：<https://hackaday.com/2022/10/31/an-easy-to-make-pi-powered-pocket-password-pal/>

有时，我们看到一个项目，它很清楚——它的创建者非常想让新来者也能理解一个项目想法；而今天的项目就是其中的一个案例。[novamostra]的项目[by OPM](https://novamostra.com/2022/10/23/byopm/)——自带密码管理器——是一个 Pi 零功耗设备，可以随身携带密码。这个项目采用了 Pi Zero 的 USB 小工具功能，将其集成到 Bitwarden 支持的密码管理工具包中，以创建一个局域网连接的密码存储，并使教程足够简单，任何人都可以按照它来构建自己的教程。

对于物理部分，组装说明简单明了——你只需要焊接一个按钮来满足硬件要求，如果你想让 Pi Zero way 更加便于携带，还有一个薄的 3D 可打印外壳！对于软件部分，这些说明会一步一步地引导您设置一个带有 Raspbian 映像的 SD 卡，然后安装所有工具并配置一个通过 USB 小工具接口进行联网的系统。从这里，您可以设置一个 Bitwarden 实例，并有选择地学习将它连接到相应的浏览器扩展。由于该设备的目标是密码管理和存储，它还会提醒你进行备份，特别指出你想要跟踪的文件。

总的来说，这样的设备可以帮助你随身携带你的密码，无论你需要它们，即使你的 Raspberry Pi 技能到目前为止是最低的，你也可以建立它，它保证会给你一种只有一个目的明确的自建口袋小工具才能给你的感觉！正在寻找不太依赖网络而更倾向于命令行的东西吗？这里有一个支持按钮和屏幕的 [Pi Zero 小工具](https://hackaday.com/2016/08/19/hackaday-prize-entry-a-raspberry-pi-password-manager/)，它使用了`pass`。