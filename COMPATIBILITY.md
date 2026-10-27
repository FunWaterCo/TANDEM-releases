# Games and known issues

Known information about specific games and common problems, and how to fix them. This page is updated over time: TANDEM opens it from **Settings → Games and known issues** and from its icon menu, next to the clock.

*[Versión en español](COMPATIBILIDAD.md)*

## Games

| Game | Does it work? | In short |
|---|---|---|
| [FiveM and GTA V (Legacy)](#fivem-and-gta-v-legacy) | Yes, with two in-game settings | Exclusive fullscreen and mouse on “DirectInput” |
| [No More Heroes](#no-more-heroes) | Yes | The first time, close the game and open it again |
| [Valorant](#valorant) | No | Its anti-cheat blocks what TANDEM sends |

### FiveM and GTA V (Legacy)

**With TANDEM's “Keyboard and mouse”.** Without the settings below, the cursor jumps to the top-left corner, a second cursor appears and the camera moves on its own, especially when FiveM notifications show up.

**What to do** (inside the game: the FiveM launcher doesn't have these settings):

1. Open the game and, in the **advanced graphics** settings, set the display to **exclusive fullscreen** (not windowed or borderless).
2. In the mouse settings, set **“Mouse input method”** to **“DirectInput”**.

With those two settings, the mouse and the camera work normally. With “Windows” it seems to work, but the camera still jumps from time to time.

### No More Heroes

The first time you open the game after installing TANDEM, it may not respond to the controller even though TANDEM says it's on.

**What to do:** close the game and open it again, with TANDEM open. It only happens that first time: the game saw your Access Controllers before TANDEM finished hiding them.

**Tip for any game:** open TANDEM and turn on the Xbox controller **before** you open the game. Many games only look for controllers when they start.

### Valorant

**It doesn't work.** Its anti-cheat (Vanguard) deliberately blocks keyboard and mouse input sent by any program, and TANDEM warns you when Valorant is in front. Making it work would require a dedicated signed driver (like the one paid programs such as reWASD use), which costs money this project can't cover, with no guarantee that it would work. Don't try to force it: you could put your account at risk.

## Known issues

| What happens | What to do |
|---|---|
| The Windows on-screen keyboard (or another “administrator” window) doesn't respond | In TANDEM, tap **Restart as administrator** (on the yellow banner, in Settings or in the icon menu) and accept the Windows permission. |
| Windows says “Windows protected your PC” when you open TANDEM | Choose **More info → Run anyway**. It shows up because the program is new and Windows doesn't know it yet. |
| The game doesn't respond, or your controller is player 2 or higher | TANDEM tells you which controller has the player 1 slot. Unplug that controller for a few seconds (or tap **Move to player 1**) and, if the game was already open, close it and open it again. |
| TANDEM doesn't find your Access Controllers | Close Steam, DS4Windows or any other program that may be using them, and make sure the USB cable is a data cable (not just a charging one). |
| TANDEM says a game could still see your Access Controller directly | Unplug that controller and plug it back in once. |

## Not tested yet

- **Bluetooth** connection (only USB has been tested).
- Devices plugged into expansion ports **E1 to E4**.
- More than two Access Controllers at once.
- Windows 8 or older.

## A game doesn't work well?

Report it in the [**Issues**](../../issues) tab of this repository: which game it is, which TANDEM mode you use (“One controller”, “One per controller” or “Keyboard and mouse”) and what happens. Solutions are added to this page.
