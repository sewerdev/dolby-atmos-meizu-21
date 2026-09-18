[README.md](https://github.com/user-attachments/files/32383606/README.md)
# dolby-atmos-meizu-21
dolby atmos port for meizu 21 from Xperia 5V
<div align="center">

# 🎧 Dolby Atmos for Meizu 21

**Ready-to-flash Magisk module that brings Dolby Atmos to the MEIZU 21**
<sub>Flyme 12.6 · Android 16 · Snapdragon 8 Gen 3 · arm64-v8a</sub>

[![Platform](https://img.shields.io/badge/platform-Magisk%20%7C%20KernelSU%20%7C%20APatch-2ea44f?style=flat-square)](#install)
[![Android](https://img.shields.io/badge/Android-16%20(SDK%2036)-3ddc84?style=flat-square&logo=android&logoColor=white)](#device)
[![ABI](https://img.shields.io/badge/ABI-arm64--v8a-6f42c1?style=flat-square)](#device)
[![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)](LICENSE)
[![Telegram](https://img.shields.io/badge/Telegram-%40VestronVulture-26A5E4?style=flat-square&logo=telegram&logoColor=white)](https://t.me/VestronVulture)

**Author:** [sewerdev](https://github.com/sewerdev) · Telegram: [t.me/VestronVulture](https://t.me/VestronVulture)

**🇬🇧 English** · [🇷🇺 Русский](#русский)

</div>

---

## ⬇️ Download

Grab **`Dolby-Atmos-Meizu-21-v1.0.zip`** from the [**Releases**](../../releases) page and flash it with
Magisk / KernelSU / APatch.

## ✨ Features

- 🔊 **Dolby Atmos (DAP) processing, always on** — no in-app toggle needed, works in **every player**
  (Spotify, Auxio, YouTube, …).
- 🎚 Ships the **Dolby Sound** UI app with profiles, IEQ presets and a graphic equalizer.
- 🔇 **No loud burst on pause** — the AOSP `dynamics_processing` "volume controller" that reset the
  chain gain to unity on stop is removed.
- 🎵 **Works in Spotify** — Compress Offload is disabled so apps on that path don't bypass the effect
  chain; `RAW`/`FAST` stay enabled, so there is **no added latency**.
- 🧩 **One single module** — the audio-policy fix is merged inside; nothing else to flash.

## 📸 Screenshots

<p align="center">
  <img src="docs/screenshots/01-main.png" width="30%">
  <img src="docs/screenshots/02-app.png" width="30%">
  <img src="docs/screenshots/03-app.png" width="30%">
</p>

## 📱 Device

| | |
|---|---|
| **Model** | MEIZU 21 (`meizu_21_CN`) |
| **Firmware** | Flyme 12.6.0.0A |
| **Android** | 16 (SDK 36) |
| **SoC** | Snapdragon 8 Gen 3 (`pineapple`) |
| **ABI** | `arm64-v8a` only |
| **Root** | Magisk 31 (alpha) |

## 🚀 Install

```bash
adb push Dolby-Atmos-Meizu-21-v1.0.zip /data/local/tmp/
adb shell su -c "magisk --install-module /data/local/tmp/Dolby-Atmos-Meizu-21-v1.0.zip"
adb reboot
```

## 🗑 Uninstall

```bash
adb shell su -c "rm -rf /data/adb/modules/DolbyAtmos"
adb reboot
```

## 🧠 What's inside

A repack of [reiryuki](https://github.com/reiryuki)'s
**Dolby-Atmos-Sony-Xperia-5-V-Magisk-Module** with the **Audio Compatibility Patch Reborn**
policy fix merged inside, plus the specific patches for this device.
Full details: [`patches/PATCHES.md`](patches/PATCHES.md) · engineering report:
[`docs/REPORT.html`](docs/REPORT.html).

```
Dolby-Atmos-Meizu-21-v1.0.zip   # ready-to-flash module  → also on Releases
docs/screenshots/               # app screenshots
docs/REPORT.html                # build & engineering report
patches/PATCHES.md              # exactly what changed vs upstream
build/                          # PowerShell build scripts
```

## 🛠 Troubleshooting

| Symptom | Fix |
|---|---|
| No sound / bootloop | hold **Vol-** while booting (Magisk safe mode), or `adb shell su -c "rm -rf /data/adb/modules/DolbyAtmos"` + reboot |
| Dolby not audible in Spotify | make sure you flashed **this** module (Compress Offload is already disabled inside) |
| Loud burst on pause | fixed in v1.0 — reinstall and reboot |
| BT headset profile doesn't auto-switch | known limitation of this UI; audio is still processed |

## 🙏 Credits

- Upstream ports & module scripts — **[reiryuki](https://github.com/reiryuki)** (MIT for the module code).
- Dolby™ apps/blobs are © **Dolby Laboratories**; Motorola/Sony assets belong to their owners.
  Included only to provide a ready-to-flash build for the Meizu 21 — rights holders may request removal.
- Scripts & documentation here — **MIT** ([LICENSE](LICENSE)).

---

<a name="русский"></a>

<div align="center">

# 🎧 Dolby Atmos для Meizu 21

**Готовый к прошивке Magisk-модуль с Dolby Atmos для MEIZU 21**
<sub>Flyme 12.6 · Android 16 · Snapdragon 8 Gen 3 · только arm64-v8a</sub>

**Автор:** [sewerdev](https://github.com/sewerdev) · Telegram: [t.me/VestronVulture](https://t.me/VestronVulture)

[🇬🇧 English](#-dolby-atmos-for-meizu-21) · **🇷🇺 Русский**

</div>

## ⬇️ Скачать

Берите **`Dolby-Atmos-Meizu-21-v1.0.zip`** на странице [**Releases**](../../releases) и прошивайте
через Magisk / KernelSU / APatch.

## ✨ Возможности

- 🔊 **Обработка Dolby Atmos (DAP) всегда включена** — тумблер в приложении не нужен, работает во
  **всех плеерах** (Spotify, Auxio, YouTube, …).
- 🎚 В комплекте приложение **Dolby Sound** — профили, IEQ-пресеты и графический эквалайзер.
- 🔇 **Нет громкого «выброса» на паузе** — AOSP-эффект `dynamics_processing` (использовался как
  регулятор громкости цепочки и сбрасывал гейн в максимум при остановке) удалён.
- 🎵 **Работает в Spotify** — Compress Offload отключён, чтобы приложения на этом пути не обходили
  цепочку эффектов; `RAW`/`FAST` не тронуты, поэтому **лишней задержки нет**.
- 🧩 **Один цельный модуль** — фикс аудиополитики влит внутрь, больше ничего прошивать не нужно.

## 📸 Скриншоты

<p align="center">
  <img src="docs/screenshots/01-main.png" width="30%">
  <img src="docs/screenshots/02-app.png" width="30%">
  <img src="docs/screenshots/03-app.png" width="30%">
</p>

## 📱 Устройство

| | |
|---|---|
| **Модель** | MEIZU 21 (`meizu_21_CN`) |
| **Прошивка** | Flyme 12.6.0.0A |
| **Android** | 16 (SDK 36) |
| **SoC** | Snapdragon 8 Gen 3 (`pineapple`) |
| **ABI** | только `arm64-v8a` |
| **Root** | Magisk 31 (alpha) |

## 🚀 Установка

```bash
adb push Dolby-Atmos-Meizu-21-v1.0.zip /data/local/tmp/
adb shell su -c "magisk --install-module /data/local/tmp/Dolby-Atmos-Meizu-21-v1.0.zip"
adb reboot
```

## 🗑 Удаление

```bash
adb shell su -c "rm -rf /data/adb/modules/DolbyAtmos"
adb reboot
```

## 🧠 Что внутри

Репак модуля [reiryuki](https://github.com/reiryuki)
**Dolby-Atmos-Sony-Xperia-5-V-Magisk-Module** с влитым внутрь фиксом **Audio Compatibility Patch
Reborn** и патчами под это устройство. Подробности — [`patches/PATCHES.md`](patches/PATCHES.md),
инженерный отчёт — [`docs/REPORT.html`](docs/REPORT.html).

```
Dolby-Atmos-Meizu-21-v1.0.zip   # готовый к прошивке модуль  → также в Releases
docs/screenshots/               # скриншоты приложения
docs/REPORT.html                # отчёт по сборке
patches/PATCHES.md              # что именно изменено против апстрима
build/                          # скрипты сборки (PowerShell)
```

## 🛠 Решение проблем

| Симптом | Что делать |
|---|---|
| Нет звука / bootloop | зажать **Vol-** при загрузке (Magisk safe mode) или `adb shell su -c "rm -rf /data/adb/modules/DolbyAtmos"` + ребут |
| Dolby не слышно в Spotify | убедитесь, что прошит **этот** модуль (Compress Offload внутри уже отключён) |
| Громкий щелчок на паузе | исправлено в v1.0 — переустановите и перезагрузитесь |
| Профиль гарнитуры не переключается автоматически | известное ограничение этого UI; звук всё равно обрабатывается |

## 🙏 Благодарности

- Апстрим-порты и скрипты модуля — **[reiryuki](https://github.com/reiryuki)** (MIT на код модуля).
- Dolby™-приложения и блобы © **Dolby Laboratories**; ассеты Motorola/Sony — их правообладателям.
  Включены только чтобы дать готовую сборку для Meizu 21; правообладатели могут потребовать удаления.
- Скрипты и документация здесь — **MIT** ([LICENSE](LICENSE)).

<div align="center"><sub>Сделано с ❤️ для Meizu 21 · <a href="https://github.com/sewerdev">github.com/sewerdev</a> · <a href="https://t.me/VestronVulture">t.me/VestronVulture</a></sub></div>
