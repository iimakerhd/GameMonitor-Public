<p align="center">
  <img src="logo.svg" alt="GameMonitor logo" width="120" height="120">
</p>

<h1 align="center">GameMonitor</h1>
<p align="center">A free companion app for League of Legends players</p>

---

GameMonitor runs on your own PC, reads the League client that is already running there, and shows a live dashboard in your browser: champion select, builds, runes, summoner spells, player profiles and item suggestions. No ads, no payments, no account.

This repository is the **public home of GameMonitor**: the website, the downloads and the place to ask questions. It does not contain the program's source code.

- **Website:** https://iimakerhd.github.io/GameMonitor-Public/
- **Download (Windows):** https://github.com/iimakerhd/GameMonitor-Public/releases/latest
- **Privacy Policy:** https://iimakerhd.github.io/GameMonitor-Public/privacy.html
- **Terms of Use:** https://iimakerhd.github.io/GameMonitor-Public/terms.html
- **Questions / bug reports:** https://github.com/iimakerhd/GameMonitor-Public/issues

---

## What is in this repository

| File | What it is |
| --- | --- |
| `index.html` | The product page: what GameMonitor does, how it works, and exactly which Riot technologies it uses. |
| `privacy.html` | The Privacy Policy: what stays on your PC, what is shared only if you opt in, and which outside services are contacted. |
| `terms.html` | The Terms of Use. |
| `style.css` | The one stylesheet shared by the three pages. |
| `logo.svg` | The GameMonitor logo, used on this page and in the product page header. |
| `images/` | Screenshots shown on the product page (added through the GitHub website). |

The pages are plain HTML and CSS. They are published for free with GitHub Pages straight from the `main` branch, so a change to a file here is the change on the website a minute later.

---

## How it works, in short

1. Download and start GameMonitor on a Windows PC. A small status window opens showing the logo, the dashboard URL and a QR code you can scan on your phone.
2. Open the dashboard address in your browser (`http://localhost:5000` on the same PC) or scan the QR code on your phone.
3. Read the notice on the first visit. Sharing anonymous game statistics is optional and off unless you turn it on.
4. Play as usual: the dashboard follows the lobby, champion select and the game.

The full description, including every Riot endpoint family the program uses, is on the [product page](https://iimakerhd.github.io/GameMonitor-Public/).

---

## For the maintainer

- **Publish a new version:** Releases → Draft a new release, tag it `v1.x.x`, attach `GameMonitor.exe`, publish. The app checks for a newer release once an hour and shows an update notice in its status window. The Download button on the website always points at the latest release.
- **Add or change screenshots:** Add file → Upload files, into the `images` folder, with the names `champ-select.png`, `champion-builds.png` and `player-profile.png`. Until a file exists, its slot is hidden on the page.
- **Update the policies:** edit `privacy.html` or `terms.html` and change the "Last updated" date at the top.
- **Keep the page true to the program.** When a feature that uses Riot data is added, changed or removed, the "Which Riot technologies it uses" section of `index.html` and the Privacy Policy must change with it.
- **Dependencies (for building the exe):** `pip install qrcode[pil] pillow requests flask pyinstaller`. To obfuscate before packaging: `pip install pyarmor` then `pyarmor pack -e "--onefile" GameMonitor.py`.

---

## Disclaimer

GameMonitor is an independent, unofficial tool. It isn't endorsed by, affiliated with or sponsored by any game developer or publisher, and it doesn't reflect the views or opinions of any of them or of anyone officially involved in producing or managing their games. All game names, logos and related properties are trademarks or registered trademarks of their respective owners.

GameMonitor isn't endorsed by Riot Games and doesn't reflect the views or opinions of Riot Games or anyone officially involved in producing or managing Riot Games properties. Riot Games, and all associated properties are trademarks or registered trademarks of Riot Games, Inc.

GameMonitor isn't endorsed by Psyonix or Epic Games and doesn't reflect the views or opinions of Psyonix, Epic Games or anyone officially involved in producing or managing Rocket League. Rocket League and all associated properties are trademarks or registered trademarks of Psyonix LLC.
