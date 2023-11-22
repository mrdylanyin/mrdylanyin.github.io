+++
title = "关于 Naive 一些客户端的个人实践"
date = 2023-11-22T23:58:00+08:00
lastmod = 2023-11-23T00:32:07+08:00
draft = false
toc = true
+++

之前的梯子经常被封，无奈套了 Cloudflare（CF），但是速度实在是不怎么稳定。搜索了下，选择了 NaïveProxy。选择它的原因是了解到这个协议被封的概率比较小，这样就不用套 Cloudflare，速度会相比之下更稳定，而且相对来说也比较小众。同时，因为比较小众，所以客户端支持还是比较受限的，通常需要除了客户端外还要安装一个 NaïveProxy 的内核。这里推荐下我使用的客户端：

-   安卓：NekoBox Google Play 和 GitHub 都可以下载。插件安装在 NekoBox 的设置，高级插件，了解更多中找到 NaïveProxy 插件下载安装即可。
-   iOS: Shadowrocket 中选择 HTTP/2 或者 HTTPS，不需要单独安装插件。
-   Windows: NekoRay，可以在 GitHub 下载。插件在 NaïveProxy 的官方 GitHub 仓库的 Releases 中下载。
-   Mac: NekoRay 官方不支持，但是可以在 NekoRay 的 GitHub README 中找到第三方构建的 Mac 软件包（目前最新版 3.24 的软件可能会闪退，建议下载之前的版本）。插件在 NaïveProxy 的官方 GitHub 仓库的 Releases 中下载。
-   Linux: 根据发行版不同，安装方式也不一样，这个可以详细参考 NekoRay 的官方仓库。同样，插件在 NaïveProxy 的官方 GitHub 仓库的 Releases 中下载。
-   OpenWrt: ShadowSocksR Plus+ 插件目前是可以支持 NaïveProxy 的，不需要单独安装插件。
-   同时，几乎所有平台都可以下载 NaïveProxy 中的对应 Release，之后配置 config.json 然后通过命令行运行 naive config.json，之后手动修改系统代理的方式来科学上网。

NaïveProxy 协议基本上只有用户名、密码、域名、端口这几个选项，根据客户端的不同，相应填写即可。如果有其他要填的默认就好。例如，NaïveProxy 的命令行客户端的 config.json 配置示例为：

```json
{
  "listen": "socks://127.0.0.1:1080",
  "proxy": "https://username:password@example.com:443",
  "log": "",
}
```

由于服务器现在还有一个月的时间到期，所以这段时间就当做测试。如果不套 Cloudflare 的话没有被封，新服务器就用这个协议了。
