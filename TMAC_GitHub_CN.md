<div align="center">

# TMAC - Telegram Multi-Account Converter

**五合一的 Telegram 桌面转换工具。**

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

### 🌐 语言

[English](README.md) · [Русский](TMAC_GitHub_RU.md) · 简体中文 — 本文件

---

## 🔄 转换方向

| # | 方向 | 输入 | 输出 | 重新授权 |
|---|------|------|------|-------|
| 1 | **会话 → 会话+JSON** | `.session` 文件（Telethon / Pyrogram） | 按设备配置重建的 `.session` + `.json`（Telethon / Pyrogram） | ✅ 是 |
| 2 | **TDATA → 会话** | Telegram Desktop `tdata` 文件夹 | 每个账号一份 `.session` + `.json`（Telethon / Pyrogram） | ✅ 是 |
| 3 | **会话 → TDATA** | `.session` 文件（+ `.json`）（Telethon / Pyrogram） | Telegram Desktop `tdata` 文件夹（+ 可选 `.session` 文件（+ `.json`）（Telethon / Pyrogram）） | ✅ 是 |
| 4 | **移动 → 会话** | `tgnet.dat`（官方应用）· `td.binlog`（Telegram X） | SESSION+JSON（Telethon / Pyrogram）· 可选 TDATA | ❌ 否 |
| 5 | **AuthKey → 会话** | 密钥文件：`HASH:DC_ID` / `DC_ID:HASH` / StringSession | `.session`（Telethon / Pyrogram）（+ `.json` · 可选 TDATA） | ✅ 是 |

> 几乎每个方向都支持**重新授权**（二维码全新登录），并在格式允许时支持**离线冷转换**。

---

## ⚙️ 核心功能

| 功能 | 说明 |
|------|------|
| 工作模式 | **旧会话**（保留）· **新会话**（二维码重新登录）· **仅断开** |
| 会话清理 | 转换期间结束账号的其他会话（Kill Old Session） |
| HEX:DC 导出 | 可选的 **SAVE AUTH:DC** 在转换后的会话旁边写入授权密钥（`HASH:DC_ID`） |
| Pyrogram 输出 | 在 Telethon 输出之外，可选保存 Pyrogram 会话副本 |
| 设备仿真 | Android / Android X / iPhone / Desktop — 旧会话与新会话可分别设置，支持自定义 API:HASH |
| JSON 控制 | **Use my JSON** — 设备与语言字段直接使用你的 JSON |
| 2FA 处理 | 手动输入，或从 TXT 文件自动导入 |
| 代理支持 | HTTP / SOCKS5，内置检测 |
| 多线程 | 任意数量的并行转换线程 |
| 离线转换 | 无需连接账号的冷转换 |
| 结果分类 | Valid / Invalid / Timed-out / Bad 2FA — 独立文件夹 |
| 源文件备份 | 处理前自动复制原始文件 |
| 界面 | 应用内切换 EN / RU / ZH · 主题 · 运行报告 · 完整控制台日志 |

---

## ⏱️ 免费试用

- **24 小时**或 **25 个账号** — 以先到者为准。
- 无需绑卡 — 先确认它适合你的使用场景。

---

## 💳 套餐

| 套餐 | 限制 |
|------|------|
| **Monthly** | 30 天或 1 000 个账号 — 以先到者为准 |
| **Annual** | 365 天或 10 000 个账号 — 以先到者为准 |
| **Permanent** | 永久 · 无限制账号 |

---

## 📥 下载

**始终提供最新版本** → [telegram-converter.com](https://telegram-converter.com/converter/telegram-multi-account-converter/)

---

## 🖼️ 截图

<!-- TODO: 添加截图链接 -->

---

## ❓ FAQ

<details>
<summary><b>旧会话和新会话有什么区别？</b></summary>
旧会话保留当前授权，并按所选设备配置重建会话。新会话通过二维码完整重新登录，生成全新的会话。
</details>

<details>
<summary><b>可以不连接 Telegram 进行转换吗？</b></summary>
可以 — 基于会话的方向支持离线（冷）转换：账号在本地被拆解为各个组件，无需网络。移动方向仅支持在线。
</details>

<details>
<summary><b>SAVE AUTH:DC（HEX:DC）保存了什么？</b></summary>
仅授权密钥及其数据中心（<code>HASH:DC_ID</code>）。不会保存设备细节，也无法得知 — 继续使用 HEX:DC 数据的风险由您自行承担。
</details>

<details>
<summary><b>结果保存在哪里？</b></summary>
在目标目录旁的分类文件夹中：<code>_Good_*</code>、<code>_Bad_*</code>、<code>_TimeOut_*</code>、<code>_Bad_2FA_*</code>。重新登录的结果保存在 <code>_New_Session</code>。
</details>

<details>
<summary><b>免费试用如何运作？</b></summary>
完整访问 24 小时或 25 个账号 — 以先到者为准。无需绑卡。
</details>

---

## 📬 联系与支持

| 渠道 | 链接 |
|------|------|
| Email | manager[@]telegram-converter.com |
| Telegram | [发送消息](https://telegram-converter.com/telegram-contact) |
| Discord | [发送消息](https://telegram-converter.com/discord-contact) |
| Matrix | [发送消息](https://telegram-converter.com/matrix-contact) |
| 官网 | https://telegram-converter.com/ |

---

## ☕️ 捐赠

**请我们喝杯咖啡** — [捐赠](https://nowpayments.io/donation/mcv)

感谢你的支持！
