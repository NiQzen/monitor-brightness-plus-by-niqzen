# Monitor Brightness Plus for Stream Deck

Control the brightness of your external monitors (DDC/CI) and Windows Night Light right from your Stream Deck.

Works on every Stream Deck model with keys. On a Stream Deck +, you can also use the dials and the touch strip.

## Brightness on a dial (Stream Deck +)
- **Rotate:** adjust brightness by a configurable step (1–25%)
- **Press or tap:** 100%
- **Hold or long-tap:** 0%

## Brightness on a key
Choose what each key does:
- **Press: 100% · Hold: 0%**
- **Increase or decrease brightness** (hold the key to keep changing)
- **Set a fixed level**, e.g. 70%
- **Cycle through levels**, e.g. `100, 50, 0`

The key can show the current brightness as its title.

## Night Light
- **On a key:** toggle, turn on or turn off Windows Night Light
- **On a dial:** rotate to change its strength, press or tap to turn it on or off
- **Schedule:** turn Night Light on and off at set times, e.g. on at 21:00 and off at 07:00. It follows the Windows clock, and you can still switch it by hand in between.

The key and the touch strip show whether Night Light is on, also when it is changed in Windows.

## Settings
- **Monitor #:** `0` controls all DDC/CI monitors together; enter `1`, `2`, … to control one monitor. With several monitors, add one action per monitor.
- **Key action**, **Level**, **Levels**, **Show level** (brightness key)
- **Step / Dial step:** percentage per key press or dial click
- **Hold time:** how long to hold before brightness goes to 0%
- **Schedule**, **Turn on at**, **Turn off at** (Night Light, shared by all Night Light keys and dials)

## Setup
1. Turn on **DDC/CI** in your monitor's on-screen menu (often under *Setup*, *System* or *Others*). Many monitors have it on by default.
2. Drag the **Brightness** action onto a key or a dial, pick the monitor, and on a key choose what it does.
3. Optional: drag the **Night Light** action onto a key or a dial. To switch it automatically, turn on **Schedule** in its settings.

If the action shows a warning triangle, the monitor did not answer. Check that DDC/CI is on, connect the monitor directly (some docks and adapters don't pass DDC/CI through), and turn off dynamic contrast, eco or HDR picture modes, which can lock brightness.

If Night Light is also scheduled in Windows Settings, turn that schedule off so the two don't conflict.

> **Note:** a few seconds after the Night Light strength changes, Windows re-applies the display colours once. This can show as a brief flicker. Windows' own Night Light slider does the same, so it is expected.

## Requirements
- Windows 10 / 11, Stream Deck 6.9 or later
- For brightness: an external monitor with DDC/CI enabled. Built-in laptop displays are not supported.
- Night Light needs no administrator rights.

No data leaves your computer.

## Release notes

### 1.1.0
- **New: Night Light schedule.** Turn on **Schedule** in the settings of any Night Light key or dial and pick when Night Light turns on and off, for example on at 21:00 and off at 07:00.
- The schedule follows the Windows clock and is shared by all Night Light keys and dials. It keeps running even when no Night Light action is on screen.
- Night Light switches only at the set times, so you can still change it by hand in between.
- A switch missed while the PC was asleep or Stream Deck was closed is applied when it wakes or starts.

### 1.0.0
- First release: monitor brightness on Stream Deck + dials and on keys (press for 100% / hold for 0%, increase, decrease, set a level, cycle through levels), and Windows Night Light on keys and dials.

## Support
Open an issue on this page.

## License
Copyright © 2026 NiQzen. All rights reserved. See [LICENSE](LICENSE).
