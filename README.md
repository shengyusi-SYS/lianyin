<p align="center">
  <a href="https://lianyin.eztools.fun/zh-cn/">
    <img src="assets/lianyin_brand.png" alt="涟音 LianYin" width="600">
  </a>
</p>

# 涟音 LianYin

中文 · [English](README.en.md) · [官网](https://lianyin.eztools.fun)

涟音是一款支持多设备协作的分布式跨平台本地音乐播放器。

本仓库仅做发布与技术分享，不包括完整源码。

## 支持平台

| 平台 | 架构 | GUI | CLI · 预览版 |
| --- | --- | --- | --- |
| Windows | x86_64 | EXE 安装包 | 一键安装 / ZIP |
| macOS | Apple 芯片 | DMG | 一键安装 / tar.gz |
| Linux | x86_64 | AppImage | 一键安装 / tar.gz |
| Android | arm64-v8a | APK | — |
| Docker / NAS | Linux amd64、arm64 | — | 容器镜像 / Compose |

[GUI 安装](https://lianyin.eztools.fun/zh-cn/manual?edition=gui#install) · [CLI 安装](https://lianyin.eztools.fun/zh-cn/manual?edition=cli#install) · [Docker 部署](https://lianyin.eztools.fun/zh-cn/manual?edition=cli#docker)

内存占用：以windows版为例，gui版常驻工作集内存约200M~400M，cli版约45M。

## 功能

- **同步播放**：将多台设备编成一组，精确同步播放，适合聚会和多房间同步。
- **分组播放**：让不同设备组播放不同的音乐，例如书房和客厅各听各的。
- **共享播放**：各自使用自己的设备和耳机，一起听同一首歌。
- **跨设备播放**：用手机选择电脑或外部音乐库中的音乐，在另一台设备或它连接的音箱上播放。

<br>

- **音乐库来源**：本地文件夹、WebDAV、 Navidrome、[musicfs](https://github.com/shengyusi-SYS/musicfs)。
- **曲库更新**：本地曲库支持快速扫描和文件变化监听，外部曲库可在启动时更新；也可手动更新指定音乐库。
- **共享与收藏**：分享曲库和歌单。收藏后可获取更新，更新时可比较并选择歌曲信息；也可保存一份自行整理。

<br>

- **多播放队列**：每个编组都有自己的播放队列列表，灵感来自musicolet。
- **易编辑的队列**：提供可还原的字段排序、随机排序，以及拖拽编辑，也能将队列复制到其它分组或保存为歌单

CLI 版当前提供曲库管理和共享，主要面向 NAS 等环境，其他能力待接入。

## 下载与使用

[下载涟音](https://lianyin.eztools.fun/zh-cn/#download) · [使用手册](https://lianyin.eztools.fun/zh-cn/manual)

目前处于 Early Access（抢先体验）阶段。

本地播放免费，无需登录。

注册登录后，可试用 14 天多 **多设备互联功能** ，最多激活 3 台设备。

## 购买与激活

涟音的 **多设备互联功能** 采用一次性买断，当前仅提供 **[支持者版](https://lianyin.eztools.fun/zh-cn/#early-access)** 一种。

US$19.99，10台激活额度，可重新绑定激活。

一次购买，额度全平台通用。

| 渠道 | 价格 | 备注 |
| --- | --- | --- |
| [itch.io](https://shengyusi-sys.itch.io/lianyin-founder) | US$19.99 起 | 建议价 US$24.99 |
| Steam | — | 即将上线 |

## 技术概览

涟音主要使用 Rust 开发，将 Bevy 游戏引擎作为跨平台GUI框架。

| 技术 | 用途 |
| --- | --- |
| Bevy UI / ECS | 跨平台 GUI 基础 |
| Iroh / QUIC | P2P 直连，端到端加密，NAT 穿透 |
| Rodio / Symphonia / CPAL | 音频播放 |
| Sendspin | 多设备精确同步 |

## 部分开源

除了公开 fork 的依赖外，涟音会逐步开源一部分内部工具，目的是为有相同需求的开发者提供便利和参考：

| 项目 | 简介 |
| --- | --- |
| [bevy_ui_scroll](https://github.com/shengyusi-SYS/bevy_ui_scroll) | 滚动增强：滚轮、触摸惯性、吸附与下拉刷新 |
| [bevy_ui_virtual_list](https://github.com/shengyusi-SYS/bevy_ui_virtual_list) | 定高虚拟列表：按可视区域复用行实体，支持自定义行内容 |
| [bevy_ui_router](https://github.com/shengyusi-SYS/bevy_ui_router) | UI 路由：页面导航、历史返回、Keep-Alive、滚动位置恢复与过渡动画 |
| [bevy_video](https://github.com/shengyusi-SYS/bevy_video) | 视频播放器：开发中，基于 libmpv，输出为 Bevy 纹理 |

这些项目基本都由 AI 开发，前三个已用于涟音，可能依赖涟音维护的其他 fork。

---

[联系与反馈](mailto:contact@lianyin.eztools.fun) · [条款与隐私](https://lianyin.eztools.fun/zh-cn/legal)
