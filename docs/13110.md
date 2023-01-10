# 说朋友，让这个盒子为你打开

> 原文：<https://hackaday.com/2022/03/28/say-friend-and-have-this-box-open-for-you/>

手工制作的礼物很特别，这个也不例外。[John Pender]为他的儿子制作了一个受托尔金启发的盒子,并在 Hackaday.io 上与我们分享了细节。这个独一无二的手工制作的盒子完成了一个角色，并且做得很完美——就像都灵的门一样，你必须用精灵语说“朋友”,盒子就会为你打开。

这款盒子经过精心雕刻和表面处理，可以单独作为一件礼物。然而，使用语音识别功能，这是一个复杂的项目，足以同时涵盖相当多的领域——木工、电子和软件。电子设备布置在数控加工的通道中，一旦盒子准备好收听，LED 灯带就会照亮“说朋友并进来”的铭文。如果你想知道解锁过程是如何进行的，[下面的视频展示了这一切。](https://www.youtube.com/watch?v=ccaJ4VTJv_A)

两个螺线管保持盖子锁定，在它的中心是一个 Pi 零点，操作的大脑。使用小电池和耗电板，电源管理有点复杂。两个电容传感器和一个小型电源管理设备始终通电。当触摸两个传感器时，Pololu 的电源开关模块会唤醒 Pi。反过来，它会像成熟的 Linux 主板一样，慢慢等待时机，一旦听到声音，就会点亮 LED 灯。

[John]不想使用任何基于云的语音识别服务，这种需要预先建立 WiFi 连接的礼物一点也不好玩。相反，他设置并使用 PocketSphinx 进行离线语音识别。这个盒子是给他儿子的一个惊喜，因此，[约翰]不能完全要求声音样本。谢天谢地，PocketSphinx 无需预先训练就能识别短语。还有一个应急机制——在你打开盒子之前，电子设备是无法接触到的。秘诀是将电压施加到两个衬垫上，这将直接解锁螺线管，以防电池耗尽或 Pi 故障。

我们不知道盒子打开后会有什么，但我们只能希望儿子的名字不是巴林。我们感谢[约翰]记录了细节，提醒我们，我们的黑客技能让我们为我们重视的人创造独特而美好的东西。黑客制作的礼物非常棒——我们已经看到了[婚礼的留言簿](https://hackaday.com/2020/09/22/a-digital-guestbook-is-a-perfect-hacker-wedding-gift/)、[情侣的近距离感应 LED 徽章](https://hackaday.com/2019/07/13/a-wedding-gift-fit-for-a-hardware-hacker/)、[基于 ESP32 的 CTF](https://hackaday.com/2018/01/18/capture-the-flag-challenge-is-your-perfect-gift/)，甚至[陨石转盘展示架](https://hackaday.com/2017/03/01/a-meteorite-gift-box/)。

 [https://www.youtube.com/embed/ccaJ4VTJv_A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ccaJ4VTJv_A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

