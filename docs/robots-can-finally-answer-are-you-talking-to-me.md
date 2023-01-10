# 机器人终于可以回答，你在和我说话吗？

> 原文：<https://hackaday.com/2020/11/08/robots-can-finally-answer-are-you-talking-to-me/>

语音助手，爱他们也好，恨他们也罢，越来越司空见惯。语音助手的一个问题是多个设备在同一个地方收听的情况。当给定一个命令时，哪个设备应该响应？CMU 未来界面小组的研究人员[Karan Ahuja]、[Andy Kong]、[Mayank Goel]和[Chris Harrison]给出了答案；智能助理应该尝试[推断用户是否面对他们想要与之对话的设备](https://karan-ahuja.com/dov.html)。他们称之为声音方向或 DoV。

目前，智能助手使用简单的比赛来看谁先听到。原因是你最接近的设备可能会首先听到它。然而，在有回声的情况下，或者当你与多个设备距离相等时，结果对用户来说似乎是任意的。

DoV 的实现使用 python sklearn 工具包中的额外树分类器。考虑了其他几种机器学习算法，但最终效率胜出，选择了 Extra-Trees。这项研究的另一个有趣的方面是确定面对到底意味着什么。该团队让人类“听众”代替智能助手。“说话者”会说出关键短语，而“听者”则决定说话者是否面对他们。基于他们对朝向的定义，该系统可以以 90%的准确度确定某人是否正对着设备，通过每个房间的校准，该准确度上升到 93%。

他们的算法以及他们收集的数据已经在 GitHub 上开源。也许当你在[打造自己的语音助手](https://hackaday.com/2017/01/26/build-your-own-p-brain/)时，你可以加入 DoV 来提高唤醒词的准确性。

 [https://www.youtube.com/embed/TLl-N61LBMg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TLl-N61LBMg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Karan]发送此邮件！