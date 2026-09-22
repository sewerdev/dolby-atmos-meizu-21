<div align="center">

# 🎧 Dolby Atmos for Meizu 21

Ready-to-flash Magisk module that brings Dolby Atmos to the MEIZU 21 (and maybe for 20 series), ported from the Sony Xperia 5V build.

[![Platform](https://img.shields.io/badge/platform-Magisk%20%7C%20KernelSU%20%7C%20APatch-2ea44f?style=flat-square)](#device)
[![Android](https://img.shields.io/badge/Android-16%20(SDK%2036)-3ddc84?style=flat-square&logo=android&logoColor=white)](#device)
[![ABI](https://img.shields.io/badge/ABI-arm64--v8a-6f42c1?style=flat-square)](#device)
[![Telegram](https://img.shields.io/badge/Telegram-%40VestronVulture-26A5E4?style=flat-square&logo=telegram&logoColor=white)](https://t.me/VestronVulture)

**Author:** [sewerdev](https://github.com/sewerdev) &nbsp;·&nbsp; **Telegram:** [@VestronVulture](https://t.me/VestronVulture)

English &nbsp;·&nbsp; [Русский](#русский)

</div>

---

## Device

- **Model:** MEIZU 21 (`meizu_21_CN`)
- **Firmware:** Flyme 12.6.0.0A
- **Android:** 16 (SDK 36)
- **SoC:** Snapdragon 8 Gen 3 (`pineapple`)
- **ABI:** `arm64-v8a` only
- **Root:** Magisk, KernelSU or APatch; tested on Magisk 31 (alpha)

## Install

**Via the Magisk app**

1. Copy `Dolby-Atmos-Meizu-21-v1.0.zip` to your device.
2. Open **Magisk → Modules → Install from storage** and select the zip.
3. Reboot.

**Via ADB**

```bash
adb push *name*.zip /data/local/tmp/
adb shell su -c "magisk --install-module /data/local/tmp/Dolby-Atmos-Meizu-21-v1.0.zip"
adb reboot
```

## Uninstall

```bash
adb shell su -c "rm -rf /data/adb/modules/DolbyAtmos"
adb reboot
```

## Credits

- Upstream port and module scripts by [reiryuki](https://github.com/reiryuki), module code licensed under MIT.
- Dolby™ apps and blobs are © Dolby Laboratories; Motorola/Sony assets belong to their respective owners. They are included only to provide a ready-to-flash build for the Meizu 21 and will be removed on request from the rights holders.

---

<a id="русский"></a>

<div align="center">

# 🎧 Dolby Atmos для Meizu 21

Готовый к прошивке Magisk-модуль с Dolby Atmos для MEIZU 21 (и возможно для 20 линейки), портирован со сборки для Sony Xperia 5V.

**Автор:** [sewerdev](https://github.com/sewerdev) &nbsp;·&nbsp; **Telegram:** [@VestronVulture](https://t.me/VestronVulture)

[English](#-dolby-atmos-for-meizu-21) &nbsp;·&nbsp; Русский

</div>

---

## Устройство

- **Модель:** MEIZU 21 (`meizu_21_CN`)
- **Прошивка:** Flyme 12.6.0.0A
- **Android:** 16 (SDK 36)
- **SoC:** Snapdragon 8 Gen 3 (`pineapple`)
- **ABI:** только `arm64-v8a`
- **Root:** Magisk, KernelSU или APatch; протестировано на Magisk 31 (alpha)

## Установка

**Через приложение Magisk**

1. Скопируйте `Dolby-Atmos-Meizu-21-v1.0.zip` на устройство.
2. Откройте **Magisk → Модули → Установить из памяти** и выберите zip-файл.
3. Перезагрузитесь.

**Через ADB**

```bash
adb push *название*.zip /data/local/tmp/
adb shell su -c "magisk --install-module /data/local/tmp/Dolby-Atmos-Meizu-21-v1.0.zip"
adb reboot
```

## Удаление

```bash
adb shell su -c "rm -rf /data/adb/modules/DolbyAtmos"
adb reboot
```

## Благодарности

- Апстрим-порт и скрипты модуля: [reiryuki](https://github.com/reiryuki), код модуля распространяется под лицензией MIT.
- Приложения и файлы Dolby™ являются собственностью Dolby Laboratories; ресурсы Motorola/Sony принадлежат их правообладателям. Они включены только для того, чтобы дать готовую сборку под Meizu 21, и будут удалены по требованию правообладателей.

