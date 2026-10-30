<div align="center">

# TANDEM

### *For Access Controller*

Use your [**PlayStation Access Controllers**](https://www.playstation.com/en-us/accessories/access-controller/) on PC as an Xbox controller, or as a keyboard and mouse.

[![Latest version](https://img.shields.io/github/v/release/FunWaterCo/TANDEM-releases?label=latest%20version&color=1f6feb&style=for-the-badge)](../../releases/latest)
[![Windows 10 and 11](https://img.shields.io/badge/Windows-10%20%7C%2011-0f766e?style=for-the-badge&logo=windows&logoColor=white)](#getting-started)
[![Downloads](https://img.shields.io/github/downloads/FunWaterCo/TANDEM-releases/total?label=downloads&color=7c3aed&style=for-the-badge&cacheSeconds=3600)](../../releases)

### [Download the latest version](../../releases/latest)

[Español](README.md) · **English** · [Games and known issues](COMPATIBILITY.md)

</div>

---

## What is TANDEM?

TANDEM is a small program that lets your PC recognize and remap up to **two Access Controllers** at the same time, connected over USB, so they work **together as a single controller**.
It's designed for people with motor disabilities (spinal cord injury, quadriplegia, etc.).

TANDEM comes with 3 built-in modes:
<table>
<tr>
<td width="33%" valign="top">

### One controller
Your two controllers are merged into **one Xbox controller** that games recognize.

</td>
<td width="33%" valign="top">

### One per controller
Each Access Controller is **its own Xbox controller**: great for two players.

</td>
<td width="33%" valign="top">

### Keyboard and mouse
Your buttons and stick send **keys, clicks and cursor movement**: macros, shortcuts and much more, with different settings for each controller profile if you like.

</td>
</tr>
</table>

The whole program is available in **Spanish and English**: it asks for your language the first time you open it, and you can change it anytime in *Settings*. There's also a **dark mode**, in *Settings* or in the icon menu next to the clock.

## Getting started

**You'll need:** Windows 10 or 11 (I haven't tested Windows 8 or older), your Access Controllers with **one USB data cable for each** (make sure it's a data cable, not a charge-only one) and **an internet connection the first time you run it**.

1. **Download** [`TANDEM.zip`](../../releases/latest).
2. **Unzip it** wherever you like, for example in *Documents*.
3. **Connect** your Access Controllers with the cables. (I haven't tested Bluetooth.)
4. **Double-click `INICIAR.bat`**.
5. If your PC doesn't have Python, the **official** one is downloaded from python.org and installed **just for TANDEM**.
6. Windows asks **only once** whether to allow changes as administrator: choose **Yes**. That installs the two drivers TANDEM needs (see the section below).
   When it's done, TANDEM **reopens automatically** and it's ready.

After that, it opens in seconds and the Xbox controller turns on automatically.

> **If Windows says “Windows protected your PC”:** choose **More info → Run anyway**. It shows up because the program is new and Windows doesn't know it yet.

> **If Windows 11 blocks it** (*Smart App Control*): turn off Smart App Control. In theory this block shouldn't show up anymore, but with Windows you never know.


<details>
<summary><b>What TANDEM installs on your PC</b></summary>

| What | What for | Where |
|---|---|---|
| **Python 3.12** (official, from python.org) | TANDEM is written in Python. It's only downloaded if your PC didn't have it, and it's installed just for your user | `%LOCALAPPDATA%\AccessXInput\python-oficial` |
| **ViGEmBus** (Nefarius) | Creates the Xbox controller that games see | Windows driver |
| **HidHide** (Nefarius) | Hides your Access Controllers from games while TANDEM uses them, so games don't read the controller twice | Windows driver |
| **Your settings** | Your button setup | `Documents\PS5 ACCESS CONTROLLER SETTINGS` |
| **Backup copies** | The previous version, in case an update goes wrong | `%LOCALAPPDATA%\AccessXInput\respaldo` |

Both drivers are installed with that one-time Windows permission. They're the original ones from Nefarius: TANDEM checks their digital fingerprint before running them. TANDEM only creates a shortcut or opens when Windows starts if you choose to.
</details>

<details>
<summary><b>Uninstall TANDEM completely</b></summary>

1. In TANDEM, open **Settings** and under **Open with Windows** choose **No** (if you had it on).
2. **Close TANDEM completely:** right-click its icon next to the clock (it may be under the ^ arrow) → **Exit TANDEM**. Your controllers stay hidden from other programs until you uninstall HidHide (the next step).
3. In **Settings → Apps → Installed apps** (on Windows 10: *Apps & features*), uninstall:
   - **HidHide**
   - **ViGEm Bus Driver** (it may show up as *Nefarius Virtual Gamepad Emulation Bus Driver*)
   - **Python 3.12.10 (64-bit)**, only if TANDEM installed it and you don't use it for anything else

   If you use HidHide or ViGEmBus with another program (DS4Windows, for example), don't uninstall them.
4. **Restart** the PC.
5. Delete these folders:
   - the folder where you unzipped TANDEM;
   - `%LOCALAPPDATA%\AccessXInput` (type it exactly like that in the File Explorer address bar);
   - `Documents\PS5 ACCESS CONTROLLER SETTINGS` (**this is where your button setups are**: keep a copy of `mapeo.json` if you want to keep them).
6. Delete the **TANDEM** shortcuts from the desktop and the Start menu, if you created them.
</details>

## Security and privacy

| | |
|---|---|
| **Signed updates** | TANDEM only installs a new version if it carries the publisher's digital signature. |
| **No telemetry** | It doesn't send your data anywhere. It only checks here for new versions (and you can turn that off). |
| **Verified installers** | The drivers it needs (ViGEmBus and HidHide) only run if they're *exactly* the original ones. |
| **Everything is optional** | Shortcut, open with Windows, background mode and administrator permissions: nothing happens unless you ask for it. |

## FAQ

For specific games (FiveM, GTA V, No More Heroes, Valorant…) and problems we already know about, see **[Games and known issues](COMPATIBILITY.md)**.

<details>
<summary><b>Who is TANDEM made for?</b></summary>

Honestly, for my brother, who has a spinal cord injury.
He already had two Access Controllers that he plays with on the PlayStation, but using a PC with regular peripherals is very hard for him, and the alternatives we've found for people with spinal cord injuries or limited mobility are quite expensive and hard to get if you don't live in the US.
On top of that, I'm surprised Sony hasn't released an official driver that guarantees Access Controller support on PC, not just to have something to play with, but because of all the **POTENTIAL** these devices have for real, productive use on computers, and because there are A LOT of people with motor disabilities out there who have to get by with unofficial programs and drivers.
Also, even though PC already has options like reWASD and JoyToKey, we decided to make TANDEM simply because we wanted a much simpler and more personal solution. Now we want to share it with the world, as one more option to make these gadgets easier to use on PC.
</details>


<details>
<summary><b>Which controllers work?</b></summary>

**PlayStation Access Controllers**, connected **over USB**. You can use one or two. I haven't tried connecting more than two Access Controllers, but if I get another one I'll let you know, in case anyone finds it useful to have more than two.
So far I've only tested the controllers over USB; I haven't been able to check whether they work the same over Bluetooth.
And well, TECHNICALLY any DirectInput controller works with TANDEM; the thing is that the whole interface and behavior are designed **SPECIFICALLY** with the Access Controller in mind.
</details>

<details>
<summary><b>Linux / macOS support?</b></summary>

Yes, I'm planning to release a Linux build soon, but I want to test it properly first, and for now I chose to prioritize the Windows version because that's what my brother uses.
As for macOS, it looks complicated: I DON'T have a Mac and I don't have anyone who can lend me one either.
</details>

<details>
<summary><b>Support for the expansion ports? (E1 - E4)</b></summary>

I haven't been able to test it. I don't have any peripherals to plug into the expansion ports, and from what I've seen they're kind of expensive. I'm thinking of building some myself, at least to check that buttons and sticks work, and I also hope to get a trigger so I can make sure all 3 input types work perfectly. Stay tuned for future updates.
</details>

<details>
<summary><b>Do I need to install anything first?</b></summary>

No. `INICIAR.bat` gets everything that's missing (Python and the two drivers) the first time you run it.
</details>

<details>
<summary><b>The Windows on-screen keyboard doesn't respond with TANDEM</b></summary>

Windows doesn't let a regular program send keys to “administrator” windows. In TANDEM, tap **Restart as administrator** (it's on the yellow banner, in *Settings* and in the icon menu) and accept the Windows permission.
</details>

<details>
<summary><b>How does it update?</b></summary>

TANDEM lets you know when there's a new version and tells you what's new. If you'd rather do it by hand, download the new `TANDEM.zip` and use it in another folder: your settings live in *Documents* and aren't lost.
</details>

<details>
<summary><b>IT DOESN'T WORK IN VALORANT</b></summary>

:/
It's a limitation of Vanguard, Valorant's anti-cheat, which protects itself from programs that remap inputs. I didn't want to dig any deeper to see if we could force it to work, for fear of getting our account banned, so for now I don't think it's possible to use TANDEM in games that use Vanguard.
More details in [Games and known issues](COMPATIBILITY.md#valorant).
</details>

<details>
<summary><b>Does TANDEM cost anything? Do you accept donations?</b></summary>

TANDEM itself is COMPLETELY FREE. We think Access Controllers are already expensive enough without also CHARGING for software that basically just remaps the inputs to something a PC can recognize.
But if you'd like to support us in some way, you can do it through our [GoFundMe](https://www.gofundme.com/f/ayudame-a-reconstruir-mi-vida-despues-de-un-accidente).
If we open more ways to get in touch or donate at some point, I'll let you know here.
Also keep an eye on our other project, [TRENDIT LABS](https://www.instagram.com/trenditlab/), more info soon.
</details>

---

<div align="center">

**TANDEM - For Access Controller**

<sub>Independent project: not affiliated with or endorsed by Sony or Microsoft. “PlayStation” and “PS5” are trademarks of Sony Interactive Entertainment; “Xbox” and “Windows” are trademarks of Microsoft. They're mentioned only to show what it works with.</sub>

</div>
