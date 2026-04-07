# No More Cookies — project information

This repository holds **public information** for the browser extension **No More Cookies** (Google Chrome and other **Chromium** browsers with **Manifest V3**).

The extension **source code** is maintained in a **private** GitHub repository and is **not** published here.

> **Status:** Pre-release / friend testing. In the popup, optional **Block Newsletters** appears under **PRO** with a **Preview** note until a subscription offering is live.

---

## What it does (high level)

- Tries to **decline or dismiss** common cookie consent banners and CMPs across many EU languages, with extra handling for large platforms (e.g. Meta, Google / YouTube) and conservative behavior on some public broadcasters and Schibsted-style “consent or pay” sites where automatic reject is not appropriate.
- Applies **local, in-browser** fixes when sites still trap scrolling or leave broken overlays after a banner is handled—so pages stay usable where possible. This now includes visual normalization for dimmed SPA content shells (scoped force-reset of `filter` / `backdrop-filter` / `opacity` on trusted roots when needed). Not every site behaves the same; some cases (e.g. occasional CMP timing) are still being improved.
- **Optional:** If you turn it on, **Block Newsletters** (preview) uses on-page heuristics to reduce some email-capture modals; a short grace period applies when you open subscribe flows yourself.
- **Statistics:** The popup can show **totals** and **per-site** counts (keyed to the **top-level page hostname** in the address bar, so numbers stay meaningful when banners run inside embedded frames). You can **reset** cookie-only or newsletter-only counters from the popup.

---

## Privacy

- **[Privacy Policy](PRIVACY.md)** — local storage, on-page behavior (including extension CSS, inline adjustments, and scoped visual normalization overrides on trusted content roots when pages remain dimmed), optional **Report bug** submissions (Google Forms: **base site URL** only, not the full page address; short system summary, not the full raw User-Agent string), and related details.

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

*Last updated: 7 April 2026*
