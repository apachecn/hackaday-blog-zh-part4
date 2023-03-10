# 备份加密的 ZFS 数据而不解密，即使 TrueNAS 不批准

> 原文：<https://hackaday.com/2022/08/11/back-up-encrypted-zfs-data-without-decrypting-it-even-if-truenas-doesnt-approve/>

[Michael Lynch]最近用基于 ZFS 的自建解决方案替换了他的 Synology NAS，这是一个具有简洁功能的文件系统:无需先解密即可备份加密数据。唯一的问题是[Michael]正在使用 TrueNAS，而 TrueNAS 只想将未加密的 ZFS 数据备份到另一个 TrueNAS 系统。[幸运的是，有一种方法可以解决这个问题](https://mtlynch.io/zfs-encrypted-backups/)，这种方法并不复杂，但肯定需要利用正确的工具。它还为 ZFS 如何处理这些事情提供了一个教育演练。

解决方案是[少量的 shell 脚本](https://github.com/mtlynch/zfs-encrypted-backup)来管理加密数据集的完整和增量备份和恢复，而不必先解密数据。如上所述，这是默认情况下 [TrueNAS](https://www.truenas.com/) 会处理的事情，但前提是目的地也是 TrueNAS 系统。现在，[Michael]只需做一点额外的工作，就可以将备份发送到异地云存储。

[Michael]使用了一个额外的技巧来监控他的备份。他利用一项名为 [Cronitor](https://cronitor.io/) 的付费(但有免费等级)服务。从网站的特性来看，这不是很明显，但是有一种方法可以实现 cron 作业监控，不需要添加任何软件。这部分是如何工作的:Cronitor 提供了一个定制的、唯一的 URL。如果该 URL 没有被定期访问(例如，因为 cron 作业失败)，那么用户会得到通知。通过将它集成到现有的 cron 作业中，可以通知用户。这样的集成看起来像这样:

```
0 0 3 * * monthly-job && curl --silent https://cronitor.link/p/<API-KEY>/monthly-job?state=complete
```

简而言之，如果 cron 作业运行成功，`curl`通过访问自定义 URL 进行登记。如果没有发生这种情况，用户会收到通知。没有添加软件，只是简单地利用免费服务来增加一些安心。

备份很容易被忽视，所以也许是时候[花点时间考虑一下你为数据存储做了什么](https://hackaday.com/2020/01/20/new-year-habits-what-do-you-do-for-data-storage/)，包括你如何从灾难中恢复。