# 使用谷歌日历来记录人类的日子

> 原文：<https://hackaday.com/2022/10/25/using-google-calendar-for-machines-to-keep-track-of-human-days/>

自动化的日常触发器在理论上很简单，除非它需要跟踪人类实际生活的日历。季节性变化、公共假期的变动或者仅仅是度假都是你需要考虑的例外。[Jeremy Rode]喜欢使用谷歌日历来了解最新事件，所以他创建了 [CalendarScraper](https://github.com/jeremyrode/CalendarScraper) ，这是一个简单的脚本，可以让他的机器也使用它。

杰里米需要为他的水疗加热器安装一个定时器，只有当当地的分时电价优惠时，才能打开定时器，从而降低成本。费率根据一天中的时间、一周中的某一天、甚至季节和公共假日而变化。他没有尝试在`cron`工作中手动设置一切，而是创建了一个简短且易于修改的 JavaScript 脚本来跟踪谷歌日历上的事件。

我们已经看到了其他一些从谷歌日历中提取数据的项目，包括一个[回收日提醒](https://hackaday.com/2022/06/11/hackaday-prize-2022-binpal-is-a-convenient-recycling-reminder/)，甚至一个[实体桌面日历](https://hackaday.com/2022/02/02/keep-track-of-your-google-calendar-with-this-custom-build/)。