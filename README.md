```
  ██╗  ██╗  ██████╗   ██╗   ██╗  ███████╗   ██████╗
  ██║ ██╔╝  ██╔══██╗  ╚██╗ ██╔╝  ██╔════╝  ██╔═══██╗
  █████╔╝   ██████╔╝   ╚████╔╝   ███████╗  ██║   ██║
  ██╔═██╗   ██╔══██╗    ╚██╔╝    ╚════██║  ██║   ██║
  ██║  ██╗  ██║  ██║     ██║     ███████║  ╚██████╔╝
  ╚═╝  ╚═╝  ╚═╝  ╚═╝     ╚═╝     ╚══════╝   ╚═════╝
                      白 河 愁
```

# frpc for Synology

[简体中文](#简体中文) | [繁體中文](#繁體中文) | [English](#english) | [日本語](#日本語)

frpc ([fatedier/frp](https://github.com/fatedier/frp)) client package for Synology NAS, with a built-in web management panel.

---

### English

A Synology SPK package for frpc with a web-based management panel. Easily configure and manage frp client on your Synology NAS through a modern web UI.

### 简体中文

群晖 NAS 专用 frpc 安装包，内置 Web 管理面板。通过简洁的网页界面轻松配置和管理 frp 客户端，实现内网穿透。

### 繁體中文

群暉 NAS 專用 frpc 安裝套件，內建 Web 管理面板。透過簡潔的網頁介面輕鬆設定和管理 frp 用戶端，實現內網穿透。

### 日本語

Synology NAS 向け frpc パッケージ。Web 管理パネルを内蔵し、ブラウザから簡単に frp クライアントの設定・管理ができます。

---

## Features

- Web UI for managing frpc configuration and service (port 8088)
- Support TCP / UDP / HTTP / HTTPS / STCP / XTCP proxy types
- Start / Stop / Restart service control with real-time status & logs
- Form-based proxy rule editor and raw TOML config editor
- Config import / export
- Multi-language support (English, 简体中文, 繁體中文, 日本語)
- Mobile-friendly responsive design

## Installation

1. Download the `.spk` file from [Releases](../../releases)
2. Open Synology DSM, go to **Package Center**
3. Click **Manual Install** and upload the `.spk` file
4. After installation, access the web panel at `http://<NAS_IP>:8088`

## Requirements

- Synology DSM 6.0 or later
- x86_64 architecture

## Configuration

After installation, open the web panel to configure:

1. **Server** - Your frps server address
2. **Port** - frps server port (default: 7000)
3. **Token** - Authentication token (must match frps server)
4. Add proxy rules as needed, then click **Save & Apply**

You can also edit the raw config file at:
```
/var/packages/frpc/target/etc/frpc.toml
```

## Build from Source

Requirements: Go 1.24+, Bash

```bash
./build.sh
```

The output `.spk` file will be generated in the project root.

## Credits

- [fatedier/frp](https://github.com/fatedier/frp) - The upstream frp project

## License

The frpc binary is licensed under the [Apache License 2.0](https://github.com/fatedier/frp/blob/dev/LICENSE).

---

**Author / 作者:** 白河愁 (Kryso)

**Homepage / ホームページ / 主页 / 主頁:** [http://www.ff18.com](http://www.ff18.com)
