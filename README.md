# Mouse2Yoke v2.1 (BETA)

**Fly X-Plane 12 with just the mouse - on Linux, Windows and macOS. No joystick, no vJoy, no extra software.**

By **Capitão Zelker** · YouTube: [@CaptainZelker](https://www.youtube.com/@CaptainZelker)

> **BETA.** Developed on Linux (CachyOS). Validated on Linux and Windows with the Cessna 172, the default 737 and the Zibo 737. The macOS build is **untested** (no Mac was available) - feedback is very welcome, please open an *Issue* here on GitHub.

---

## Features

- **Mouse = yoke.** Mouse position on screen = yoke position (screen edge = full deflection).
- Only a small **+ crosshair** is drawn. X-Plane's default mouse-yoke box is hidden automatically.
- **Hold the left button = rudder.** Move the mouse sideways (two green bars show the travel). Release and the rudder returns to neutral.
- **Coordinated turns:** in the air the rudder follows the roll gently, so the ball stays centered - no pedals needed.
- **Taxi with the mouse:** on the ground, moving the mouse sideways steers the nose wheel through the rudder (fades out between 15 and 40 kt).
- **One key toggles it.** Switching OFF leaves the yoke exactly where it was, as if you were holding it by hand. Switching ON causes no jump: a **yellow +** shows where the yoke is, and the mouse takes over when you move onto it.
- The right button still looks around.
- **New in 2.1 - optional Tiller mode (taxi only):** a second key switches to a nose-wheel tiller. Only the nose wheel is controlled (up to 60 degrees), so big airliners can turn sharply; ailerons, elevator and rudder are left alone. Flight mode and tiller mode are exclusive - turning one on turns the other off. The tiller is refused in flight and above 45 kt (an on-screen message tells you) and switches itself off if you pass 45 kt.

## Install

1. Download **`Mouse2Yoke_v2.1_BETA.zip`** from the [Releases](../../releases) page.
2. Extract it and copy the **`Mouse2Yoke`** folder into `X-Plane 12/Resources/plugins/`. You should end up with:
   - Linux: `Resources/plugins/Mouse2Yoke/lin_x64/Mouse2Yoke.xpl`
   - Windows: `Resources/plugins/Mouse2Yoke/win_x64/Mouse2Yoke.xpl`
   - macOS: `Resources/plugins/Mouse2Yoke/mac_x64/Mouse2Yoke.xpl`
3. Start X-Plane 12. Go to **Settings > Keyboard**, find **"Mouse2Yoke: toggle mouse yoke control"** and assign a key (for example **Y**).
4. Optional: assign another key (for example **U**) to **"Mouse2Yoke: toggle nose-wheel tiller (optional, taxi only)"**, listed right below the main command.
5. Load an aircraft, press the key and fly with the mouse.

**macOS only:** the plugin is not signed, so macOS may block it after download. Open Terminal and run (adjust the path):

```
xattr -dr com.apple.quarantine "/path/to/X-Plane 12/Resources/plugins/Mouse2Yoke"
```

Requirements: X-Plane 12 on 64-bit Windows, 64-bit Linux (any recent distribution) or macOS 11+ (Intel and Apple Silicon).

## Menu

**Plugins > Mouse2Yoke** switches on/off: mouse yoke, automatic rudder coordination, nose-wheel steering on the ground, tiller mode, release and re-center the yoke, and reload `settings.ini`.

## Settings

Everything is in `Mouse2Yoke/settings.ini` (every option is commented). After editing, use *Plugins > Mouse2Yoke > Reload settings.ini*. The most useful ones:

| Option | What it does |
|---|---|
| `coord_gain` | How much rudder in turns (raise it if the ball slips to the outside) |
| `taxi_gain` | Strength of rudder steering on the ground |
| `tiller_max_deg` | Maximum nose-wheel angle in tiller mode |
| `rudder_distance` | Mouse travel needed for full rudder |
| `deadzone` / `expo` | Dead zone and softness around the center |
| `invert_pitch` | Inverts pitch |
| `crosshair_size` | Size of the crosshair |

## Notes

- While mouse yoke is **on**, the **left** button belongs to the plugin (rudder). To click cockpit switches, toggle it off - the yoke stays where it was.
- If something does not work, send the lines starting with `[Mouse2Yoke]` from X-Plane's `Log.txt`.

---

- Video guide and presentation (English): https://youtu.be/-8XMg17xlDg?si=_CTSgY20rEgvcga2

- Video Tutorial e Apresentação (Português-Brasil): https://youtu.be/BEou1FPSKXY?si=EdYAQJj99fjxi_kw

*Inspired by BetterMouseYoke (X-Plane 11) by Torben Könke. Mouse2Yoke is a new, independent plugin written from scratch for X-Plane 12, not derived from the original. Not affiliated with Laminar Research.*
