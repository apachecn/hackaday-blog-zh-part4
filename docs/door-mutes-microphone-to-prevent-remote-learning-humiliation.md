# 门静音麦克风，以防止远程学习羞辱

> 原文：<https://hackaday.com/2020/11/08/door-mutes-microphone-to-prevent-remote-learning-humiliation/>

在门铃的一种反向扭曲中，[TheStaticTurtle]迅速发明了一个系统，每当有人打开他房间的门时，它就使他电脑的麦克风静音。他住在法国，T2 政府上周五宣布了严格的封锁。像当今世界上许多大学生一样，他现在被迫参加在线课程。尽管他有自己的房间，但偶尔还是会有人闯进来宣布一些事情，这常常让[TheStaticTurtle]感到尴尬。当他的同学突然听到“要不要来点馅饼？”前几天，我忍无可忍了。

他的第一个决定是用磁铁和传感器来感应门的开启，他用热胶把它们粘在门和门框上。然后，他将一根长电缆接到自己的办公桌上，连接到一台带有 DigiSpark 引导程序的 ATTiny 85 上。他编写了固件来模拟特殊的按键组合，然后用他的音频路由软件 Voicemeeter Potato 注册。我们推测他没有使用外部麦克风，在这种情况下，静音可能更容易通过硬件开关来实现。总之，这是一个非常聪明和及时的黑客。如果你处于类似的困境，并且想尝试一下，他已经在 [GitHub](https://github.com/TheStaticTurtle/VoiceMeeterAutoMute) 上发布了源代码。

 [https://www.youtube.com/embed/OW962AcEFpI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OW962AcEFpI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你认识[TheStaticTurtle]桌面上的三角形图案，那是因为我们去年夏天写了他的几个项目，最近的一个是[紧凑型 70 厘米收发器](https://hackaday.com/2020/06/27/433-on-a-stick/)。