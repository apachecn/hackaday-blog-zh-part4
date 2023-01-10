# 老树莓皮的 Vulkan

> 原文：<https://hackaday.com/2020/06/22/vulkan-for-the-pi-3/>

如果你认为新的树莓派 4 得到了所有的爱，那是情有可原的。例如，Raspberry Pi 基金会正在为 GPU 开发驱动程序，以支持 Vulkan 3D 图形 API。

但是那些有着粗糙的旧 Pi 板的人不应该绝望。[Martin Thomas]是一名为 Nvidia [工作的开发人员，他在业余时间开发了一个驱动程序，将 Vulkan 带到了 Broadcom VideoCore IV](https://github.com/Yours3lf/rpi-vk-driver) 。他称之为[第一个 GPU](https://twitter.com/0martint/status/1273883659959926785) 的底层驱动，[展示了它在 Pi 3](https://twitter.com/0martint/status/1274012749174013954) 上运行《雷神之锤 3》。

从技术上来说，它不是官方的 Vulkan，因为它不具备所有要求的标准一致性，但考虑到硬件的限制，它已经尽可能接近了。资源库中给出了构建驱动程序和安装 Vulkan 加载程序的完整说明，因此修补者应该可以尝试一下。这可能是游戏玩家最感兴趣的，因为许多游戏引擎都支持 Vulkan。

Pi 4 可能会让这个家族在 64 位的方向上走得更远，但这证明了老狗也有生命。