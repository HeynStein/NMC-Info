# No More Cookies — project information

This repository holds **public information** for the browser extension **No More Cookies** (Google Chrome and other **Chromium** browsers with **Manifest V3**).

The extension **source code** is maintained in a **private** GitHub repository and is **not** published here.

> **Status:** Pre-release / friend testing. In the popup, optional **Block Newsletters** appears under **PRO** with a **Preview** note until a subscription offering is live.

---

## What it does (high level)

- Tries to **decline or dismiss** common cookie consent banners and CMPs across many EU languages, with extra handling for large platforms (e.g. Meta, Google / YouTube) and conservative behavior on some public broadcasters and Schibsted-style “consent or pay” sites where automatic reject is not appropriate.
- Applies **local, in-browser** fixes when sites still trap scrolling or leave broken overlays after a banner is handled—so pages stay usable where possible. Not every site behaves the same; some cases (e.g. occasional CMP timing) are still being improved.
- **Optional:** If you turn it on, **Block Newsletters** (preview) uses on-page heuristics to reduce some email-capture modals; a short grace period applies when you open subscribe flows yourself.

---

## Privacy

- **[Privacy Policy](PRIVACY.md)** — local storage, on-page behavior, optional **Report bug** submissions (Google Forms: **base site URL** only, not the full page address), and related details.

---

## Get the extension

- *Chrome Web Store listing — link will be added when published.*

For testers building from source, use the maintainer’s private repo or distributed package (not this repository).

---

## Contact

- **Issues / feedback:** open an issue in this repository, or email **cptheynstein@gmail.com**.

## Developer

- **HeynStein** on GitHub: https://github.com/HeynStein

---

*Last updated: 5 April 2026*
