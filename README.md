# 🍵 Matcha Web Executor

> **The cleanest web-based script executor. Built for speed. Powered by Matcha.**

![Version](https://img.shields.io/badge/version-7.0-556b2f?style=flat-square)
![License](https://img.shields.io/badge/license-GNU%20GPL%20v3-adc178?style=flat-square)
![Platform](https://img.shields.io/badge/platform-Chrome%20%7C%20Edge-fefae0?style=flat-square)
![Manifest](https://img.shields.io/badge/manifest-v3-556b2f?style=flat-square)

---

## What is Matcha?

Matcha Web Executor is a lightweight Chrome extension that lets you inject JavaScript directly into any webpage — running in the page's **MAIN world**, meaning your scripts have full access to every global variable, game object, and API the page exposes.

No bloat. No setup. Open it, paste your script, hit inject.

---

## Features

- **MAIN World Injection** — Scripts run with full page access, not sandboxed
- **Cloud Script Hub** — Pulls your script library directly from a GitHub Gist, update scripts without ever touching the extension
- **Clean Slate** — One button purges every injected script instantly
- **Persistent Editor** — Your last script is saved and restored automatically
- **Skid Protection** — Integrity check locks the executor if the branding is tampered with
- **Retry on Failure** — Hub fetch failures show a retry button instead of a blank screen
- **Secret Menu** — There's a hidden override protocol. Find it yourself
- **Ctrl+Enter** — Inject without touching the mouse
- **MV3 Compliant** — Built on Manifest V3, the current Chrome extension standard

---

## Bundled Scripts

| Script | Site | Version |
|---|---|---|
| Matcha Baker ULTRA | orteil.dashnet.org/cookieclicker | v6.0 |
| Matcha Clicker PRO | cpstest.org | v2.0 |
| Matcha Cursed Notepad | justnotepad.com | v5.0 |

> **✍️ Want to submit your own scripts?**  
> Community script submission is coming soon — once the official Matcha Discord launches, members will be able to contribute scripts directly to the hub. Stay tuned.

---

## Installation

1. Download the latest release zip from the [Releases](https://github.com/NotVen0x/MatchaWebExecutor/releases) page
2. Extract the folder anywhere on your machine
3. Open Chrome and navigate to `chrome://extensions`
4. Enable **Developer Mode** in the top right corner
5. Click **Load Unpacked** and select the extracted folder
6. Pin the extension and open any supported site

> **Android** — Use [Kiwi Browser](https://play.google.com/store/apps/details?id=com.kiwibrowser.browser) and load the zip via the Extensions menu  
> **iOS** — Not currently supported, research in progress

---

## Setting Up the Script Hub

The HUB tab loads scripts from a GitHub Gist. To point it at your own library:

1. Create a GitHub Gist with a `.json` file
2. Format it like this:

```json
[
  {
    "name": "My Script",
    "game": "example.com",
    "code": "(function(){ console.log('hello'); })();"
  }
]
```

3. Click **Raw** on the Gist and copy the URL
4. Paste it into `background.js` as the `HUB_URL` value
5. Reload the extension on `chrome://extensions`

---

## Project Structure

```
MatchaWebExecutor/
├── manifest.json      — Extension config (MV3)
├── background.js      — Service worker, handles Gist fetching
├── popup.html         — UI layout and styles
├── popup.js           — All extension logic
├── icon.png           — Extension icon
└── LICENSE.txt        — GNU GPL v3 license
```

---

## Releases

| Version | Codename | Notes |
|---|---|---|
| v7.0 | Smooth as Hell | TikTok launch build, full rebuild |
| v6.0 | Ultra Edition | MAIN world injection, hub resilience |
| v3.0 | Cloud Edition | First public release, Script Hub introduced |

Full release history → [github.com/NotVen0x/MatchaWebExecutor/releases](https://github.com/NotVen0x/MatchaWebExecutor/releases)

---

## License

GNU General Public License v3.0 — open source, transparent, built for the community.  
See [LICENSE.txt](LICENSE.txt) for full terms.

---

## Credits

| Role | Credit |
|---|---|
| Project Lead & Developer | Ven0x |
| Distribution | Netlify |
| Extension Platform | Chrome MV3 |

---

<div align="center">
  <sub>© 2026 Matcha Hub · Ven0x Development</sub>
</div>
