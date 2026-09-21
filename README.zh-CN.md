# amux 发行包

[English](README.md) | [简体中文](README.zh-CN.md)

[amux](https://amuxos.com/) 官方二进制下载仓库。
本仓库维护发行附件和安装说明，应用源码在独立的 `amuxos/amux` 仓库维护。

## 安装

先安装并登录 Codex、Claude 或 Pi，再下载安装器：

```sh
curl -fsSL https://github.com/amuxos/amux-releases/releases/latest/download/install.sh -o /tmp/amux-install.sh
bash /tmp/amux-install.sh --runtime codex
```

使用 `--runtime claude` 或 `--runtime pi` 选择其他已安装的 Agent。
添加 `--feishu` 可配置飞书机器人。原生 Agent 自行管理其登录凭据。
使用 `--version vX.Y.Z` 选择指定版本。

支持 macOS（Apple Silicon 和 Intel）、Linux（x86-64 和 ARM64）。
Claude 还需要 Node.js 22 或更新版本。

## 更新

```sh
amux update --restart
```

更新保留配置和用户数据。发行附件包含 SHA256 校验文件及 `latest.json` 平台清单。
指定版本的附件保持不变，最新版本地址指向当前稳定版。

## 发行版本

[下载发行包](https://github.com/amuxos/amux-releases/releases)。
构建和测试在源码仓完成，本仓库只发布安装脚本、编译产物、校验文件和版本元数据。
每个包均附带许可证和第三方声明。
