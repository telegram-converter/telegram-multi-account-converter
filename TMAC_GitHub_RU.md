<div align="center">

# TMAC - Telegram Multi-Account Converter

**Пять Telegram-конвертеров в одном настольном приложении.**

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

### 🌐 Языки

[English](TMAC_GitHub_EN.md) · Русский — этот файл · [简体中文](TMAC_GitHub_CN.md)

---

## 🔄 Направления конвертации

| # | Направление | Вход | Выход | Ре-авторизация |
|---|-------------|------|-------|-------|
| 1 | **Сессия → Сессия+JSON** | файлы `.session` (Telethon / Pyrogram) | пересобранные `.session` + `.json` (Telethon / Pyrogram) | ✅ Да |
| 2 | **TDATA → Сессия** | папки `tdata` Telegram Desktop | `.session` + `.json` для каждого аккаунта (Telethon / Pyrogram) | ✅ Да |
| 3 | **Сессия → TDATA** | файлы `.session` (+ `.json`) (Telethon / Pyrogram) | папка `tdata` Telegram Desktop (+ опционально файлы `.session` (+ `.json`) (Telethon / Pyrogram)) | ✅ Да |
| 4 | **Мобильный → Сессия** | `tgnet.dat` (официальное приложение) · `td.binlog` (Telegram X) | SESSION+JSON (Telethon / Pyrogram) · опционально TDATA | ❌ Нет |
| 5 | **AuthKey → Сессия** | файл ключей: `HASH:DC_ID` / `DC_ID:HASH` / StringSession | `.session` (Telethon / Pyrogram) (+ `.json` · опционально TDATA) | ✅ Да |

> Почти каждое направление поддерживает **переавторизацию** (новая сессия через QR-код) и **офлайн-конвертацию** там, где это позволяет формат.

---

## ⚙️ Возможности

| Возможность | Описание |
|-------------|----------|
| Режимы работы | **Старая сессия** (сохранить) · **Новая сессия** (QR-перелогин) · **Только отключение** |
| Отключение сессий | Завершение других сессий аккаунта во время конвертации (Kill Old Session) |
| Экспорт HEX:DC | Опция **SAVE AUTH:DC** пишет ключ авторизации (`HASH:DC_ID`) рядом со сконвертированной сессией |
| Pyrogram-выход | Опциональные копии Pyrogram-сессий вместе с Telethon-выходом |
| Эмуляция устройств | Android / Android X / iPhone / Desktop — отдельно для старой и новой сессии, свои пары API:HASH |
| Управление JSON | **Use my JSON** — поля устройства и языка берутся из вашего JSON |
| 2FA | Ручной ввод или автоматический импорт из TXT-файла |
| Прокси | HTTP / SOCKS5 со встроенной проверкой |
| Многопоточность | Любое число параллельных потоков конвертации |
| Офлайн-конвертация | Холодная конвертация без подключения к аккаунту |
| Сортировка результатов | Valid / Invalid / Timed-out / Bad 2FA — по отдельным папкам |
| Резервная копия | Исходные файлы копируются перед обработкой |
| Интерфейс | Переключение EN / RU / ZH внутри приложения · темы · отчёт о прогоне · полный журнал |

---

## ⏱️ Пробный период

- **24 часа** или **25 аккаунтов** — что наступит раньше.
- Без карты — просто убедитесь, что инструмент подходит для ваших задач.

---

## 💳 Тарифы

| Тариф | Лимиты |
|-------|--------|
| **Monthly** | 30 дней или 1 000 аккаунтов — что наступит раньше |
| **Annual** | 365 дней или 10 000 аккаунтов — что наступит раньше |
| **Permanent** | Пожизненно · без лимита аккаунтов |

---

## 📥 Загрузка

**Всегда последняя версия** → [telegram-converter.com](https://telegram-converter.com/converter/telegram-multi-account-converter/)

---

## 🖼️ Скриншоты

<img width="256" alt="TMAC_RU_001" src="https://github.com/user-attachments/assets/33221da3-81e0-4291-ba16-f3a35d39e9e4" />
<img width="256" alt="TMAC_RU_002" src="https://github.com/user-attachments/assets/ee4ec6a8-b71d-4208-ab11-a57ee4f88820" />
<img width="256" alt="TMAC_RU_003" src="https://github.com/user-attachments/assets/9bc6f4d1-81ae-4f0e-90fb-7077887c0fca" />
<img width="256" alt="TMAC_RU_004" src="https://github.com/user-attachments/assets/329f0cb5-76da-4d0d-a5d5-f1920e24c700" />
<img width="256" alt="TMAC_RU_005" src="https://github.com/user-attachments/assets/c36a2a72-b061-4078-9808-eafd5366e567" />
<img width="256" alt="TMAC_RU_006" src="https://github.com/user-attachments/assets/78375282-36e6-4a82-897d-5195406d851e" />
<img width="256" alt="TMAC_RU_007" src="https://github.com/user-attachments/assets/1da5b88f-17fa-4484-b7e0-1b775b0a98c3" />

---

## ❓ FAQ

<details>
<summary><b>Чем отличаются режимы «Старая сессия» и «Новая сессия»?</b></summary>
Старая сессия сохраняет текущую авторизацию и пересобирает сессию под выбранный профиль устройства. Новая сессия выполняет полный перелогин по QR-коду и создаёт совершенно новую сессию.
</details>

<details>
<summary><b>Можно ли конвертировать без подключения к Telegram?</b></summary>
Да — офлайн (холодная) конвертация доступна для сессийных направлений: аккаунт разбирается на компоненты локально, сеть не нужна. Направление «Мобильный» работает только онлайн.
</details>

<details>
<summary><b>Что сохраняет SAVE AUTH:DC (HEX:DC)?</b></summary>
Только ключ авторизации и его дата-центр (<code>HASH:DC_ID</code>). Детали устройства не сохраняются и неизвестны — дальнейшее использование данных HEX:DC на ваш страх и риск.
</details>

<details>
<summary><b>Куда попадают результаты?</b></summary>
В сортировочные папки рядом с папкой назначения: <code>_Good_*</code>, <code>_Bad_*</code>, <code>_TimeOut_*</code>, <code>_Bad_2FA_*</code>. Результаты перелогина — в <code>_New_Session</code>.
</details>

<details>
<summary><b>Как работает пробный период?</b></summary>
Полный доступ на 24 часа или 25 аккаунтов — что наступит раньше. Без карты.
</details>

---

## 📬 Контакты и поддержка

| Канал | Ссылка |
|-------|--------|
| Email | manager[@]telegram-converter.com |
| Telegram | [Написать](https://telegram-converter.com/telegram-contact) |
| Discord | [Написать](https://telegram-converter.com/discord-contact) |
| Matrix | [Написать](https://telegram-converter.com/matrix-contact) |
| Сайт | https://telegram-converter.com/ |

---

## ☕️ Донаты

**Купить нам кофе** — [Задонатить](https://nowpayments.io/donation/mcv)

Спасибо за поддержку!
