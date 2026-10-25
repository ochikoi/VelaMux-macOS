# Calibration

VelaMux clicks where the AI points in a screenshot. Because AI clients resize screenshots differently, each client is calibrated once.

## What happens

1. The first time a client uses VelaMux, a full-screen window called **VelaMux Calibration** opens with nine numbered markers.
2. The AI clicks markers 1 to 9 in order. Until it finishes, VelaMux only lets it list windows.
3. After the last marker, VelaMux saves the result and closes the window. Clicks are accurate from then on; no restart is needed.

If the clicks were too far off, the window opens again on the next try.

If the window doesn't appear, macOS is probably waiting for you to approve a prompt. Allow it, then let the AI try again.

## Rulers instead of calibration

Click **Use rulers instead** in the calibration window. Screenshots then include coordinate rulers and the AI reads positions from them.

## Recalibrating

If clicks start missing after you update your AI client, recalibrate by running this in Terminal (replace `<id>` with your install's name, shown at the end of installation):

```sh
~/Library/Application\ Support/VelaMuxPortable-<id>/app/velamux-calibrate clear
```

The next time the client uses VelaMux, the calibration window opens again. `velamux-calibrate status` shows the current mode of each client.
