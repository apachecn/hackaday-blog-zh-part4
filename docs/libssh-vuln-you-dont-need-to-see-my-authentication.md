# LibSSH Vuln:你不需要看到我的认证

> 原文：<https://hackaday.com/2018/10/16/libssh-vuln-you-dont-need-to-see-my-authentication/>

另一天，另一个 CVE(常见漏洞和暴露)。为一个漏洞分配一个 CVE 编号是一个真实的标记，表明您遇到了真正的问题。 [CVE-2018-10933](http://www.libssh.org/security/advisories/CVE-2018-10933.txt) 对于 libssh 来说是最坏的情况。只需一个响应，攻击者就可以完全绕过身份验证，获得对系统的完全访问权限。

在惊慌失措地拔掉服务器的电源线之前，要知道 libssh 不是 OpenSSH 的一部分。您的 Linux 机器几乎肯定使用 OpenSSH 作为 SSH 守护进程，并且这个守护进程不容易受到这个特定问题的影响。Libssh 确实出现在一些重要的地方，最值得注意的可能是 Github 和[他们的安全团队已经宣布](https://twitter.com/GitHubSecurity/status/1052317333379723265)他们的实现没有漏洞。

Libssh 发布了一个新版本来解决这个问题。休息之后请继续关注细节。

正如人们所预料的那样，libssh 项目在其客户机和服务器实现之间共享代码。当新连接完成握手过程时，有不同的回调来处理数据包类型。SSH 协议定义了在处理身份验证请求时要发送的几个响应。其中一个消息是 USERAUTH_SUCCESS，服务器发送它来通知客户端身份验证成功，请求的服务准备好了。

```

/**
 * @internal
 *
 * @brief Handles a SSH_USERAUTH_SUCCESS packet.
 *
 * It is also used to communicate the new to the upper levels.
 */
SSH_PACKET_CALLBACK(ssh_packet_userauth_success) {
  (void)packet;
  (void)type;
  (void)user;

  SSH_LOG(SSH_LOG_DEBUG, &quot;Authentication successful&quot;);
  SSH_LOG(SSH_LOG_TRACE, &quot;Received SSH_USERAUTH_SUCCESS&quot;);

  session-&gt;auth.state = SSH_AUTH_STATE_SUCCESS;

```

您可能已经开始猜测这里的漏洞了。Libssh 没有一种机制来确定在当前的连接状态下是否允许传入数据包。攻击者可以启动一个连接，服务器将发送身份验证质询，攻击者可以用 USERAUTH_SUCCESS 响应进行回复。问题是这个响应只能由服务器发送，而不能由客户端发送，并且只能在认证完成之后发送。

由于共享代码，服务器错误地跳转到该消息类型的处理程序，并将身份验证阶段标记为完成。此时，守护程序会建立 SSH 连接，就像客户端已经通过了身份验证一样，为攻击者铺上红地毯。

该漏洞是由 NCC 集团的 Peter Winter-Smith 发现的，他私下向 libssh 披露了该问题。今天发布了 libssh 的更新版本，同时发布了问题的详细信息。如果您已经安装了 libssh，特别是如果您正在使用服务器组件，请安装这个重要的更新。

这是一个令人讨厌的 bug，但幸运的是 libssh 没有被广泛用作 ssh 服务器，而是更多地被用作 SSH 客户端。