<div align="center">
  
# TMAC - Telegram Multi-Account Converter

**Five Telegram converters in one desktop application.**

[![Repo](https://img.shields.io/badge/github-repo-blue?logo=github)](https://github.com/telegram-converter)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%2F%2011-0078D6?logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgMGgxMS4zNzd2MTEuMzcyaC0xMS4zNzd6bTEyLjYyMyAwaDExLjM3N3YxMS4zNzJoLTExLjM3N3pNMCAxMi42MjNoMTEuMzc3VjI0SDBabTEyLjYyMyAwaDExLjM3N1YyNEgxMi42MjN6Ii8+PC9zdmc+)](https://telegram-converter.com/)
[![Converters](https://img.shields.io/badge/converters-5%20in%201-7B68EE?logo=convertio&logoColor=white)](https://telegram-converter.com/)
[![Interface](https://img.shields.io/badge/interface-EN%20%7C%20RU%20%7C%20ZH-brightgreen?logo=googletranslate)](https://telegram-converter.com/)

[![Website](https://img.shields.io/badge/website-click_to_open-blue?logo=googlechrome)](https://telegram-converter.com/)
[![License](https://img.shields.io/badge/License-Commercial-red?logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0iI2ZmZiIgZD0iTTE0LDJIMTBWNEgxNFYyTTE5LDRIMTVWNkgxOVY0TTUsNEg5VjZINVY0TTE5LDhIMTVWMTBIMTlWOE01LDhIOVYxMEg1VjhNMTQsOFYxMEgxMFY4SDE0TTUsMTJIOVYxNEg1VjEyTTE5LDEySDE1VjE0SDE5VjEyTTE0LDEySDEwVjE0SDE0VjEyTTUsMTZIOVYxOEg1VjE2TTE5LDE2SDE1VjE4SDE5VjE2TTE0LDE2SDEwVjE4SDE0VjE2TTEyLDIwQzEwLjksMjAgMTAsMTkuMSAxMCwxOEgxNEMxNCwxOS4xIDEzLjEsMjAgMTIsMjBaIi8+PC9zdmc+)](https://telegram-converter.com/#pricing)
[![Terms & Conditions](https://img.shields.io/badge/Terms%20%26%20Conditions-Informational-blue?logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0iI2ZmZiIgZD0iTTE0IDJIMTBWNEgxNFYyTTUgNEg5VjZINVY0TTE5IDRIMTVWNkgxOVY0TTUgOEg5VjEwSDVWOE0xOSA4SDE1VjEwSDE5VjhNMTQgOEgxMFYxMEgxNFY4TTUgMTJIOVYxNEg1VjEyTTE5IDEySDE1VjE0SDE5VjEyTTE0IDEySDEwVjE0SDE0VjEyTTUgMTZIOVYxOEg1VjE2TTE5IDE2SDE1VjE4SDE5VjE2TTE0IDE2SDEwVjE4SDE0VjE2TTEyIDIwQzEwLjkgMjAgMTAgMTkuMSAxMCAxOEgxNEMxNCAxOS4xIDEzLjEgMjAgMTIgMjBaIi8+PC9zdmc+)](https://telegram-converter.com/terms-of-use/)


</div>

---

---

### 🌐 Languages

English — this file · [Русский](TMAC_GitHub_RU.md) · [简体中文](TMAC_GitHub_CN.md)

---

## 🔄 Conversion directions

| # | Direction | Input | Output | Re-Authorization |
|---|-----------|-------|--------|-------|
| 1 | **Session → Session+JSON** | `.session` files (Telethon / Pyrogram) | Rebuilt `.session` + `.json` (Telethon / Pyrogram) | ✅ Yes |
| 2 | **TDATA → Session** | Telegram Desktop `tdata` folders | `.session` + `.json` per account (Telethon / Pyrogram) | ✅ Yes |
| 3 | **Session → TDATA** | `.session` files (+ `.json`) (Telethon / Pyrogram) | Telegram Desktop `tdata` folder (+ optional `.session` files (+ `.json`) (Telethon / Pyrogram)) | ✅ Yes |
| 4 | **Mobile → Session** | `tgnet.dat` (official app) · `td.binlog` (Telegram X) | SESSION+JSON (Telethon / Pyrogram) · optional TDATA | ❌ No |
| 5 | **AuthKey → Session** | Key file: `HASH:DC_ID` / `DC_ID:HASH` / StringSession | `.session` (Telethon / Pyrogram) (+ `.json` · optional TDATA) | ✅ Yes |

> Almost every direction supports **re-authorization** (a fresh session via QR login) and **offline cold conversion** where the format allows it.

---

## ⚙️ Key features

| Feature | Details |
|---------|---------|
| Work modes | **Old Session** (keep) · **New Session** (QR re-auth) · **Only Kill** |
| Session cleanup | Terminate other account sessions during conversion (Kill Old Session) |
| HEX:DC export | Optional **SAVE AUTH:DC** writes the auth key (`HASH:DC_ID`) next to the converted session |
| Pyrogram output | Optional Pyrogram session copies alongside the Telethon output |
| Device emulation | Android / Android X / iPhone / Desktop — separate for old & new sessions, custom API:HASH pairs |
| JSON control | **Use my JSON** — device & language fields taken from your own JSON |
| 2FA handling | Manual password or automatic import from a TXT file |
| Proxy support | HTTP / SOCKS5 with a built-in checker |
| Multithreading | Any number of parallel conversion threads |
| Offline conversion | Cold conversion without connecting to the account |
| Result sorting | Valid / Invalid / Timed-out / Bad 2FA → separate folders |
| Source backup | Original files copied before processing |
| Interface | Built-in EN / RU / ZH switch · themes · run report · full console journal |

---

## ⏱️ Free Trial

- **24 hours** or **25 accounts** — whichever comes first.
- No card required — just verify it works for your use-case.

---

## 💳 Plans

| Plan | Limits |
|------|--------|
| **Monthly** | 30 days or 1 000 accounts — whichever comes first |
| **Annual** | 365 days or 10 000 accounts — whichever comes first |
| **Permanent** | Lifetime · unlimited accounts |

---

## 📥 Download

**Always the latest release** → [telegram-converter.com](https://telegram-converter.com/converter/telegram-multi-account-converter/)

---

## 🖼️ Screenshots

<!-- TODO: add screenshot URLs -->

---

## ❓ FAQ

<details>
<summary><b>What is the difference between Old Session and New Session?</b></summary>
Old Session keeps the current authorization and re-saves the session under a new device profile. New Session performs a full re-login (QR code) and produces a completely fresh session.
</details>

<details>
<summary><b>Can I convert without connecting to Telegram?</b></summary>
Yes — offline (cold) conversion is available for the session-based directions: the account is parsed into its components locally, no network needed. The Mobile direction is online-only.
</details>

<details>
<summary><b>What does SAVE AUTH:DC (HEX:DC) save?</b></summary>
Only the authorization key and its data center (<code>HASH:DC_ID</code>). Device details are not saved and not known — further use of HEX:DC data is at your own risk.
</details>

<details>
<summary><b>Where do the results go?</b></summary>
Into sorted folders next to the destination: <code>_Good_*</code>, <code>_Bad_*</code>, <code>_TimeOut_*</code>, <code>_Bad_2FA_*</code>. Re-auth results go to <code>_New_Session</code>.
</details>

<details>
<summary><b>How does the free trial work?</b></summary>
Full access for 24 hours or 25 accounts — whichever comes first. No card required.
</details>

---

## 📬 Contact & Support

| Channel | Link |
|---------|------|
| Email | manager[@]telegram-converter.com |
| Telegram | [Send message](https://telegram-converter.com/telegram-contact) |
| Discord | [Send message](https://telegram-converter.com/discord-contact) |
| Matrix | [Send message](https://telegram-converter.com/matrix-contact) |
| Website | https://telegram-converter.com/ |

---

## ☕️ Donations

**Buy us a coffee** — [Donate](https://nowpayments.io/donation/mcv)

Thank you for your support!
