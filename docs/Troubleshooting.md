# Troubleshooting

**Permissions were granted but actions or screenshots don't work.**
Run **Check Permissions.command**. It checks again and repeats the live test. You don't need to reinstall.

**macOS says it cannot verify the developer.**
Go to **System Settings > Privacy & Security** and click **Open Anyway**, then press Return in the installer to retry.

**The calibration window doesn't appear.**
macOS is usually waiting for you to approve a prompt. Allow it and let the AI try again.

**Clicks land in the wrong place.**
Recalibrate the client; see [Calibration](Calibration.md).

**The port is already in use.**
Run the installer again and choose another port, or press Return to pick a free one.

**Installation failed partway.**
Run **Install VelaMux.command** again and choose **Recover a failed install**. Your settings are kept.

**Program files are damaged.**
Run **Install VelaMux.command** and choose **Reinstall the same version**. Your settings are kept.

**I use several AI clients.**
Install once per client with a different name each time. Each gets its own port and settings. The uninstaller and permission check ask which one to use.

## Known limitations

- When a menu extends beyond the window and nothing is behind it, that area appears gray in screenshots, but it can still be clicked.
- Not every app is guaranteed to be compatible.

The full guides are also included in the download's `docs` folder.
