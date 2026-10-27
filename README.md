# Monitor Brightness Plus for Stream Deck

Control the brightness of your external monitors (DDC/CI) and Windows **Night Light** from Stream Deck keys and the dials of **Stream Deck +**.

## Brightness – on a dial or a key
The same **Brightness** action works on a dial and on a key.

**On a dial**

| Control | Action |
|---|---|
| Rotate dial | Change brightness by the configured step (1–25 %) |
| Press dial / tap touch strip | Set brightness to 100 % |
| Hold dial / long-tap touch strip | Set brightness to 0 % |

**On a key** – choose what the key does in its settings:

| Key action | What it does |
|---|---|
| Press: 100 % · Hold: 0 % (default) | Same as pressing the dial |
| Increase / Decrease brightness | One step per press; hold the key to keep changing |
| Set to a level | Sets a fixed level, e.g. 70 % |
| Cycle through levels | Moves through a list such as `100, 50, 0` |

The key can show the current brightness as its title.

## Night Light – on a dial or a key

| Control | Action |
|---|---|
| Key | Toggle, turn on, or turn off Night Light (choose in the key's settings) |
| Rotate dial | Change Night Light strength (1–25 % per click) |
| Press dial / tap touch strip | Turn Night Light on or off |

The key icon and the touch strip show whether Night Light is on, also when it is changed in Windows Settings (they update within about 5 seconds).

> **Note:** a few seconds after the strength changes, Windows re-applies the display colours once. This can show as a brief flicker, mostly on dark or video content. Windows does the same with its own Night Light slider, so this is expected and not a plugin error.

## Settings
**Brightness**
- **Title** – label shown on the touch strip (dial)
- **Dial step / Step** – percentage per dial click or key press
- **Monitor #** – `0` = all DDC/CI monitors, `1`, `2`, … = a single monitor
- **Hold time** – how long to hold before brightness goes to 0 %
- **Key action**, **Level**, **Levels**, **Show level** – key only

**Night Light**
- **Action** – toggle, turn on or turn off (key)
- **Title** and **Dial step** (dial)

## Requirements
- Windows 10 / 11, Stream Deck 6.9 or later
- Key actions work on every Stream Deck with keys; dial features need a Stream Deck +
- For brightness: an external monitor with **DDC/CI enabled** in its on-screen menu. Some docks/adapters do not pass DDC/CI through. Features such as dynamic contrast / HDR modes can lock brightness. Built-in laptop displays are not supported.

## How it works
Brightness: the plugin talks to the monitor through the Windows High-Level Monitor Configuration API (`dxva2.dll`) using a small PowerShell helper.

Night Light: Windows has no public API for it, so the plugin reads and writes the same Night Light settings that Windows Settings uses, in the current user's registry. No administrator rights are needed.

No data leaves your computer.

## Support
Open an issue on this page.

## License
Copyright © 2026 NiQzen. All rights reserved. See [LICENSE](LICENSE).
