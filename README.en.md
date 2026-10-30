<p align="center">
  <a href="https://lianyin.eztools.fun/en/">
    <img src="assets/lianyin_brand.png" alt="LianYin" width="600">
  </a>
</p>

# LianYin · 涟音

[中文](README.md) · English · [Website](https://lianyin.eztools.fun)

LianYin is a distributed, cross-platform local music player that lets your devices work together.

This repository hosts releases and technical write-ups, not the full source code.

## Supported platforms

| Platform | Architecture | GUI | CLI · Preview |
| --- | --- | --- | --- |
| Windows | x86_64 | EXE installer | Quick install / ZIP |
| macOS | Apple silicon | DMG | Quick install / tar.gz |
| Linux | x86_64 | AppImage | Quick install / tar.gz |
| Android | arm64-v8a | APK | — |
| Docker / NAS | Linux amd64, arm64 | — | Container image / Compose |

[GUI installation](https://lianyin.eztools.fun/en/manual?edition=gui#install) · [CLI installation](https://lianyin.eztools.fun/en/manual?edition=cli#install) · [Docker setup](https://lianyin.eztools.fun/en/manual?edition=cli#docker)

On Windows, typical working-set memory usage is 200–400 MB for the GUI and about 45 MB for the CLI.

## Features

- **Synchronized playback**: group devices for precisely synchronized playback at gatherings or across rooms.
- **Separate playback groups**: play different music in different groups, such as the study and living room.
- **Shared playback**: listen to the same song together, each using your own device and headphones.
- **Cross-device playback**: use your phone to choose music from your computer or an external library and play it on another device or its connected speakers.

<br>

- **Library sources**: local folders, WebDAV, Navidrome, and [musicfs](https://github.com/shengyusi-SYS/musicfs).
- **Library updates**: use quick scans and file-change monitoring for local folders, update external libraries at startup, or manually update a selected library.
- **Sharing and favorites**: share libraries and playlists. Follow them for updates, compare and choose track information when it changes, or save a copy to organize yourself.

<br>

- **Multiple playback queues**: each device group has its own list of queues, inspired by Musicolet.
- **Flexible queue editing**: sort by fields or shuffle, restore the original order, and rearrange tracks by dragging. Copy queues to other groups or save them as playlists.

The CLI currently provides library management and sharing, primarily for NAS and similar environments. Other capabilities are planned.

## Download and use

[Download LianYin](https://lianyin.eztools.fun/en/#download) · [User manual](https://lianyin.eztools.fun/en/manual)

LianYin is currently in Early Access.

Local playback is free and requires no sign-in.

Create an account and sign in to try **multi-device features** free for 14 days on up to 3 devices.

## Purchase and activation

The **[Supporter Edition](https://lianyin.eztools.fun/en/#early-access)** is the only paid edition. It unlocks **multi-device features** with a one-time purchase.

US$19.99 covers up to 10 activated devices. You can reassign slots when switching devices.

One purchase covers all supported platforms.

| Channel | Price | Notes |
| --- | --- | --- |
| [itch.io](https://shengyusi-sys.itch.io/lianyin-founder) | From US$19.99 | Suggested price: US$24.99 |
| Steam | — | Coming soon |

## Technology

LianYin is developed primarily in Rust, using the Bevy game engine as its cross-platform GUI framework.

| Technology | Role |
| --- | --- |
| Bevy UI / ECS | Cross-platform GUI foundation |
| Iroh / QUIC | Direct P2P connections, end-to-end encryption, and NAT traversal |
| Rodio / Symphonia / CPAL | Audio playback |
| Sendspin | Precise multi-device synchronization |

## Open-source components

Alongside public forks of dependencies, LianYin will gradually open-source selected internal tools to help developers with similar needs.

| Project | Description |
| --- | --- |
| [bevy_ui_scroll](https://github.com/shengyusi-SYS/bevy_ui_scroll) | Enhanced scrolling: mouse wheel input, touch inertia, scroll snapping, and pull-to-refresh |
| [bevy_ui_virtual_list](https://github.com/shengyusi-SYS/bevy_ui_virtual_list) | Fixed-height virtual lists , with pooled row entities and custom row content |
| [bevy_ui_router](https://github.com/shengyusi-SYS/bevy_ui_router) | UI routing: navigation, history, Keep-Alive, scroll restoration, and transitions |
| [bevy_video](https://github.com/shengyusi-SYS/bevy_video) | Video player in development, based on libmpv with output to a Bevy texture |

These projects are largely AI-developed. LianYin already uses the first three; they may depend on other forks maintained for LianYin.

---

[Contact and feedback](mailto:contact@lianyin.eztools.fun) · [Terms and privacy](https://lianyin.eztools.fun/en/legal)
