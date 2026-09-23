# VelaMux for macOS

**[下载 ZIP 安装包 (Releases)](https://github.com/ochikoi/VelaMux-macOS/releases)**

最新版本：**VelaMux 2026.09.23**（二进制移植包，Apple Silicon / macOS 27）。

- [下载新版 ZIP](https://github.com/ochikoi/VelaMux-macOS/releases/download/v2026.09.23/VelaMux-Portable-macOS27-arm64-20260923.zip)
- [下载 SHA256 校验文件](https://github.com/ochikoi/VelaMux-macOS/releases/download/v2026.09.23/VelaMux-Portable-macOS27-arm64-20260923.zip.sha256)

旧版用户安装新版前，请先保存需要的连接信息，并单独保留新版安装包；阅读旧移植包中“彻底卸载 VelaMuxPortable.command”的删除清单后，运行该命令彻底卸载旧版，再解压并安装新版。不支持直接覆盖升级。卸载会删除本地配置和凭据。


VelaMux 是一个面向 MCP 兼容 AI Agent 的 macOS 计算机控制运行环境。

它的核心特点是让 AI Agent 能够在**完全不影响用户前台正常使用电脑的情况下，在后台控制指定的应用窗口**。

Agent 可以在后台对目标窗口进行截图、鼠标点击、键盘输入、滚动、拖拽等操作，而不会抢占用户正在使用的前台窗口，也不会移动用户的真实鼠标。

因此，用户可以继续正常使用自己的 Mac、操作前台应用，而 AI Agent 同时在后台操作另一个应用窗口。

这使 VelaMux 特别适合需要长时间运行 Agent、自动化多个应用，或者希望在 Agent 工作期间继续正常使用电脑的场景。

## 主要能力

VelaMux 通过 MCP 向兼容的 AI Agent 提供 macOS 应用窗口控制能力，包括：

* 获取当前可控制的应用窗口
* 绑定指定窗口
* 后台窗口截图
* 基于坐标的后台鼠标点击
* 后台键盘输入
* 快捷键操作
* 滚动
* 拖拽
* 长按
* 连续画面观察
* 在不同应用窗口之间进行 Agent 操作

VelaMux 的一个核心设计目标，是将 **Agent 的计算机操作与用户自己的前台操作分离**。

传统 Computer Use 在执行任务时通常需要占用当前界面、移动鼠标或切换窗口，而 VelaMux 可以让 Agent 持续操作后台窗口，同时用户继续使用自己的前台桌面。

## 二进制发行版

本仓库提供 VelaMux 面向 macOS 的预编译二进制发行版本。

发行包中包含运行 VelaMux 所需要的主要组件，包括：

* VelaMux Host
* MCP 脚本与运行环境
* 安装与卸载工具
* VelaMux 所需资源
* 独立 Python 3.12 运行时
* 云端连接相关组件

当前 VelaMux 主程序 Host 以预编译二进制形式提供，Swift 主程序源码目前尚未公开。

用户无需另外安装 Xcode、Swift、Homebrew 或 Python。

## 系统兼容性

当前版本主要在以下环境中完成开发和测试：

* Apple Silicon Mac
* macOS 27

其他 macOS 版本以及 Intel Mac 目前尚未完成完整测试。

这并不代表这些环境一定无法运行 VelaMux。较早版本的 macOS、更新版本的 macOS，以及 Intel Mac 都可以尝试运行或进行适配，但目前不能保证所有功能在这些环境中都能够直接正常工作。

后续可以根据实际测试结果逐步补充兼容性信息。

## 安装

从 GitHub Releases 下载最新的 VelaMux ZIP 安装包，完整解压后运行：

**安装 VelaMux.command**

安装器提供以下选项：

1. 仅本地安装
2. 本地 + 云端连接
3. 为已有本地安装追加云端连接
4. 安装失败恢复
5. 保留配置的同版本重装
6. 只检查安装包

普通用户**只需要下载 ZIP 文件即可安装**。

Release 中同时提供 `.sha256` 校验文件，供希望验证下载文件完整性的用户使用；它不是安装所必需的。

## 本地与云端连接

仅本地使用 VelaMux 时，不需要 Runtime API key、Tunnel ID 或云端账号。

如果需要从其他设备或云端 Agent 连接自己的 Mac，可以选择云端安装方式。

云端连接需要用户自己的：

* Runtime API key
* Tunnel ID
* 对应账号与连接权限

每位用户安装的是自己的 VelaMux 实例，并连接自己的私有 MCP 服务。

发布 VelaMux 安装包并不等同于将 VelaMux 提交到 ChatGPT 公共插件目录。

## 权限

VelaMux 需要获得 macOS 提供的相关系统权限才能完成窗口截图和后台控制。

当前跨机测试中主要涉及：

* 辅助功能
* 屏幕录制

实际需要授权的程序可能包括：

* 用户正在使用的 Agent 客户端
* VelaMuxMCPHost
* VelaMux 内置的 Python 3.12

首次运行时 macOS 也可能因为当前发行版本尚未进行 Developer ID 公证而要求用户手动允许程序运行。

具体步骤请参阅发行包中的授权说明。

## License

VelaMux 原作者：

**ochikoi**

GitHub：

https://github.com/ochikoi

当前版本允许在遵守 VelaMux 许可条件的情况下进行使用、商业使用、修改和再次分发。

再次分发时需要保留原作者署名、来源和许可声明；修改版本需要明确注明已经修改，不得冒充原作者发布的未修改版本。

VelaMux 自身许可不会覆盖 Python、tunnel-client 以及其他第三方组件，这些组件继续遵循各自的许可证。

完整许可内容请参阅：

`LICENSE-VelaMux.md`

以及：

`THIRD-PARTY-NOTICES.md`
