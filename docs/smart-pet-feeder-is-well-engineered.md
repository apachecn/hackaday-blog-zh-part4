# 智能宠物喂食器设计精良

> 原文：<https://hackaday.com/2021/04/19/smart-pet-feeder-is-well-engineered/>

养宠物有时比养孩子要求更高。宠物主人显然爱他们的宠物，但任何可以减少他们“家务”的事情都是一种受欢迎的解脱。一个大的痛点是在正确的时间和正确的数量喂养它们，尤其是对猫来说。俗话说“狗有主人，猫有杖！”

(塞巴斯蒂安)已经受够了他的猫(斯特拉丘)在奇怪的时间唠叨着要食物。幸运的是，[Sebastian]是一个熟练的制造者，他的[物联网猫喂食器](https://smartsolutions4home.com/ss4h-pf-pet-feeder/)不仅实用，而且设计得非常好。他从头开始设计和建造它，美丽的最终版本显示了他的努力。他的要求很简单。它必须与他的家庭自动化系统集成，必须根据定期的时间表分配食物，当喂食器检测到猫时，在一天的其他时间向他发送通知，以便他可以决定猫是否值得特殊对待，并允许他手动分配猫粮。最后，他还希望它易于拆卸，这样他就可以清洗与食物接触的部分。

对于电子设备，[Sebastian]设计了一个定制板来容纳 ESP12F 模块和所有其他相关部件。除了步进电机之外，其他都安装在 PCB 上。PIR 传感器用于 cat 检测。压电蜂鸣器让猫知道食物准备好了。需要时，可使用按钮手动分配食物。ESP8266 闪存有 [ESPhome](https://esphome.io/) ，允许通过简单而强大的配置文件进行控制，并通过[家庭助手插件](https://esphome.io/guides/getting_started_hassio.html)进行远程控制。如果您有兴趣深入了解一下，[Sebastian]将介绍 ESP 方面的一些关键代码块，以及家庭助手的各种配置和设置选项。

但是到目前为止，他最需要的努力是完善机械设计。他不得不经历几轮原型迭代——毕竟，他的猫值得拥有最好的喂食器设计。设计的基本部分很简单——一个步进电机驱动一个螺旋钻，将猫粮从主容器中推出，放入碗中。查看他博客上详细的组装说明和图片。他的设计最好的部分是它是多么容易把喂食器拆开来清洗。步进电机通过搭扣配合端件固定到位，无需使用任何螺钉。然后主体从电子箱的顶部滑出。休息过后，请观看[Sebastian]的喂猫视频了解详情。

如果这个设计让你渴望为你的猫也做一个，去他的博客上，提供你的邮箱地址，然后[Sebastian]会把这个项目的所有文件都发给你。

如果你的猫对干粮块不满意，你可能应该建造这个[自动喂猫器，沉着地处理湿食物](https://hackaday.com/2019/03/22/auotmated-cat-feeder-handles-wet-food-with-aplomb/)。

 [https://www.youtube.com/embed/lJUztOnBgxA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lJUztOnBgxA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

