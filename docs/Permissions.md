# Permissions

VelaMux needs two macOS permissions:

- **Accessibility**: to click, type and scroll in app windows.
- **Screen Recording**: to take screenshots of the window the AI is working in.

## Granting permissions

The installer walks you through this right after installing:

1. Allow each macOS prompt that appears.
2. In **System Settings > Privacy & Security**, turn on the switch for VelaMux under Accessibility and Screen Recording. The entry may be shown as `python3.12`.
3. Return to the installer window and press Return.

If macOS also asks to grant a permission to your AI client app, allow it as prompted.

If VelaMux isn't listed in the settings page, type `f` at the installer prompt. Finder shows the app so you can drag it into the list.

Once permissions work, the installer runs a short live test in its own test window. Don't touch that window until the test finishes.

## If you skip or the test fails

Your installation is kept. Double-click **Check Permissions.command** in the downloaded folder whenever you're ready to continue; you don't need to reinstall. Stop any AI task that's using VelaMux first.

## "Cannot verify the developer"

VelaMux is not notarized by Apple, so macOS may block it the first time. Click **Done**, go to **System Settings > Privacy & Security**, click **Open Anyway**, then go back to the installer and press Return.

## Connecting your AI client

Connect each AI client to the MCP address shown at the end of installation (usually `http://127.0.0.1:18792/mcp`). Using that address means the permissions you just granted apply; starting VelaMux another way may cause macOS to ask again.
