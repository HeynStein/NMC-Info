# Privacy Policy — No More Cookies

**Last updated:** April 5, 2026

This Privacy Policy describes how the **No More Cookies** browser extension (“**the Extension**”) handles information when you install and use it. It applies to the Extension distributed for **Google Chrome** and other **Chromium-based browsers** that support **Manifest V3**.

The Extension is developed by **HeynStein** (“**we**,” “**us**”).

**Contact**

- GitHub: https://github.com/HeynStein  
- Email: **cptheynstein@gmail.com**

If you do not agree with this policy, please do not use the Extension.

---

## Summary (plain language)

- The Extension helps reduce interruptions from cookie consent prompts and, if you turn it on, certain newsletter / email-capture overlays.
- Most behavior runs **locally in your browser**.
- To do that, the Extension may **change how pages look and behave** on sites you visit (for example by applying **inline CSS** or adjusting attributes such as scroll lock and `inert`) so banners can be dismissed and the page stays scrollable and clickable. Those changes happen **on your device**; we do **not** receive the page HTML or your browsing content from that process.
- Settings and statistics are stored **on your device** (not on servers we operate).
- If you use **Report bug** in the Extension popup, some **diagnostic information** is sent to **Google** via **Google Forms**, including **only the site’s base URL** (not the full page link).
- We **do not sell** your data. The Extension is **not directed at children under 13** (or the minimum age in your country).

---

## What the Extension does

**Cookie consent:** The Extension tries to decline or dismiss common cookie banners and consent prompts on sites you visit (including various consent management platforms). Where sites leave behind invisible “locks” (e.g. dark overlays, blocked scrolling, or non-clickable content), the Extension may apply additional **local** fixes so normal browsing can continue.

**Optional newsletter blocking (preview):** If enabled in the popup, the Extension may try to dismiss certain newsletter / email signup overlays using on-page heuristics.

**Statistics:** The popup may show counts of blocked events, including totals and per-website summaries. Per-site values are keyed to the **top-level page hostname** (the site in the address bar) when the browser provides it, so they stay consistent even if a banner or widget runs inside an embedded frame.

---

## Permissions and why they are used

As shown in the browser’s permission prompt, the Extension may request:

| Permission   | Purpose |
|--------------|---------|
| `storage`    | Save on/off state, optional feature toggles, and local statistics. |
| `tabs`       | Support popup actions (e.g. reloading the active tab after setting changes), light handling for single-page app navigation, and—when updating statistics—the background may read the **active tab’s URL** to map per-site counters to the **top-level** hostname (http/https only). That processing stays in the extension. **Bug reports** only send the **base site URL** (origin), not the full page address — see below. |
| `activeTab`  | Access aligned with using the Extension from the browser toolbar for the current tab when applicable. |

The Extension uses **content scripts** with broad site coverage because consent banners and related UI can appear on many websites and sometimes inside **embedded frames** (`iframes`).

---

## Data we process and where it is stored

### A) Local storage on your device (`chrome.storage.local`)

Stored only on your device (we do not receive this automatically) may include:

- Whether the Extension is enabled or disabled  
- Optional toggles (e.g. newsletter blocking preview)  
- Numeric counters (totals and per-host values shown in the popup; per-host keys follow the top-level page hostname where applicable)  
- A timestamp used for a short bug-report cooldown, if implemented  

You can remove Extension data using your browser’s settings. The popup may offer **per-category reset controls** to clear cookie and/or newsletter counters separately.

**We do not run a backend** that collects this local data by default.

### B) Data processed in memory on webpages

To find and interact with banners, buttons, and overlays, the Extension reads and acts on the **page structure (DOM)** and **computed styles** of sites you visit (including frames where applicable). This happens **entirely on your device**.

**What “acting on the page” means:** The Extension may inject or override **CSS** (including via the extension’s own stylesheet and via **inline styles** on specific elements), adjust **attributes** (for example to reduce scroll or pointer “locks”), and programmatically **click** visible controls that correspond to decline / dismiss actions. It does **not** remove DOM nodes in a way intended to crash sites; when elements are hidden, that is generally done with CSS (e.g. `display`, `visibility`, `opacity`, `pointer-events`) rather than deleting nodes.

**What is not sent to us by default:** The full text of pages you read, form values you type, passwords, or other page content are **not** transmitted to our servers as part of normal Extension operation. The only **optional** outbound data path described in this policy is **bug reports** (see below).

---

## Optional bug reports (third party: Google)

The popup may include **Report bug**. Using it is **voluntary**.

If you submit a report, the Extension sends a request to **Google Forms** (`https://docs.google.com/forms/...`). **Google** processes that submission under Google’s terms and privacy policy.

**Information that may be sent can include:**

- The **base URL of the site** you report from (scheme + host + `/` only, e.g. `https://www.example.com/`) — **not** the full address (no path, query string, or fragment), so specific articles or private-looking URL segments are not included  
- **Extension version**  
- **Context hints** such as time zone / locale-related hints and a **User-Agent** string (as available in the browser environment)  
- **Date/time** fields used to organize responses  
- An **optional comment** you type  
- **Summary statistics** from the Extension’s counters (as implemented in your version)

Do **not** put passwords, payment card data, national ID numbers, health data, or other highly sensitive information in bug reports.

---

## Legal bases (EEA / UK)

Depending on your region:

- **Local settings and statistics** support providing the Extension and its UI.  
- **Bug reports** are based on your **consent** when you choose to submit them.

You can stop sending bug reports by not using that feature. You can change or clear local data in the browser.

---

## Retention

- **Local storage** stays on your device until you clear it or uninstall the Extension, subject to browser behavior.  
- **Google Forms** data is retained according to **Google’s** practices and the form owner’s Google account / form settings.

---

## Sharing

We do not sell your personal information.

Bug reports you send go to **Google** as described. We may use submissions to fix bugs and improve the Extension.

---

## Security

No browser extension or transmission is perfectly secure. Avoid putting sensitive information in optional report fields.

---

## Children

The Extension is not aimed at children under **13** (or the minimum age where you live). If you believe a child submitted personal data via a bug report, contact us at the email above.

---

## International users

Processing occurs on **your device** when you browse. Bug reports may be handled on **Google** infrastructure, which may involve **international transfers** depending on Google’s operations.

---

## Changes to this policy

We may update this document. The **Last updated** date at the top will change when we do. For the published copy, updates will appear in the repository where this file is hosted (e.g. your **NMC-Info** repo on GitHub).

---

## Source code

This file may live in a public **information** repository. The Extension **source code** may be kept **private** and is not necessarily published alongside this policy.

---

## Contact

- GitHub: https://github.com/HeynStein  
- Email: **cptheynstein@gmail.com**
