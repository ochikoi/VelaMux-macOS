# VelaMux for macOS

**[Download the latest release](https://github.com/ochikoi/VelaMux-macOS/releases/latest)**

VelaMux lets AI agents operate macOS app windows in the background. The AI can click, type, scroll, drag and use menus and dialogs in a window while you keep using your Mac: your real mouse pointer doesn't move and your foreground app keeps focus.

It works with any MCP-compatible AI client, such as Claude Code, Codex or ChatGPT.

## Features

- **Background control**: the AI works in its own window without taking over your mouse, keyboard or foreground app.
- **Accurate pixel clicking**: each AI client is calibrated once automatically, so clicks land where the model intends. A ruler mode is also available.
- **Menus, dialogs and file panels**: popup menus, sheets, save dialogs and file pickers are included in screenshots and can be operated directly.
- **Visible virtual pointer**: an animated on-screen pointer shows where the AI is acting and whether it is working or idle.
- **All common actions**: click, right-click, typing, keyboard shortcuts, scrolling, dragging and long press, plus batches of steps in one call.
- **One instance per AI client**: install separate copies for different clients, each with its own port and settings.
- **Local or cloud**: use it on this Mac only, or connect it to a cloud agent through your own private tunnel.

## Requirements

- Apple Silicon Mac
- macOS 27

Other macOS versions and Intel Macs have not been fully tested.

Everything needed is included in the download. You don't need to install Xcode, Homebrew or Python.

## Install

1. Download the ZIP from [Releases](https://github.com/ochikoi/VelaMux-macOS/releases/latest) and extract it.
2. Double-click **Install VelaMux.command**.
3. Choose **Local install only** (or **Local + cloud install** if you want cloud access).
4. Enter a name for the AI client you'll use, such as `Claude Code`, and press Return to accept the suggested port.
5. Follow the prompts to grant permissions (see below). The installer then runs a short live test in its own test window.
6. Add the MCP address shown at the end (usually `http://127.0.0.1:18792/mcp`) to your AI client.

The download is not notarized by Apple. If macOS says it cannot verify the developer, go to **System Settings > Privacy & Security** and click **Open Anyway**.

## Permissions

VelaMux needs **Accessibility** and **Screen Recording**. The installer asks for them and opens the right settings page; turn on the switches, then press Return in the installer window. If something isn't working yet, the installer waits so you can try again. macOS may also ask you to grant a permission to your AI client app; follow the prompt if it appears.

You can run **Check Permissions.command** at any time to grant permissions again and repeat the live test. See [Permissions](docs/Permissions.md).

## First use

The first time an AI client uses VelaMux, a full-screen **VelaMux Calibration** window opens and the AI clicks nine numbered markers. This happens once per client and takes under a minute. If you prefer not to calibrate, click **Use rulers instead**. See [Calibration](docs/Calibration.md).

A typical session: the AI lists windows, binds the one it should work in, then acts and checks the result from screenshots.

## Upgrading and uninstalling

To remove VelaMux, double-click **Uninstall VelaMux.command**, review the list of files to be deleted, and press Return to confirm.

Installing over an older version is not supported. To upgrade, save any connection details you need, uninstall the old version with the uninstaller from its own package, then install the new version. Uninstalling deletes local settings and credentials.

## More help

- [Permissions](docs/Permissions.md)
- [Calibration](docs/Calibration.md)
- [Cloud connection](docs/Cloud-Connection.md)
- [Troubleshooting](docs/Troubleshooting.md)

## License

VelaMux is created by [ochikoi](https://github.com/ochikoi) and distributed as a prebuilt binary; the source code is not currently published.

You may use, modify and redistribute VelaMux, including commercially, as long as you keep the author attribution, the source link and the license, and clearly mark modified versions. Third-party components such as Python and tunnel-client remain under their own licenses.

See [LICENSE.md](LICENSE.md) and [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).
