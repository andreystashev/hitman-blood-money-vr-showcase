# Blood Money VR — Alpha 4 (0.1.8.173)

This update focuses on Steam Link/SteamVR startup, OpenXR controller pointing, stereo frame pairing and headset audio. The settings launcher and the Alpha 3 gameplay/modifier profile remain available.

[Download Alpha 4](https://github.com/andreystashev/hitman-blood-money-vr-showcase/releases/tag/v0.1.8.173-alpha.4) · [Installation](INSTALLATION.md) · [Controls](CONTROLS.md) · [Troubleshooting](TROUBLESHOOTING.md)

## Install or update

Close Blood Money and its VR helpers, then run `BloodMoneyVR-0.1.8.173-Setup.exe`. Select the original game's executable and a separate writable mod folder. Setup replaces the previous registered copy and updates its shortcuts. Game files and saves are unchanged.

**Every install, update and same-version reinstall replaces all seven mod INIs with this release's defaults.** Modifier choices, manual VR/audio settings, calibration and weapon grips are reset. The selected game, launcher connection and language are kept; the play launcher now reapplies that saved connection after the reset.

## Launch with Steam Link

1. Install Steam/SteamVR on the PC and Steam Link on Quest. Connect to this PC from Steam Link in the headset and wake both controllers. Close other VR games.
2. Open **Blood Money VR Settings → Connection & game**, choose **SteamVR** and your game, then click **Save & play**.
3. The launcher opens SteamVR if necessary and checks the connected headset, tracking and compositor before starting Blood Money. If the connection is not ready, the game has not been started: complete the VR connection, put on the headset and choose **Retry**.
4. Close the dashboard/Desktop overlay and focus Blood Money. The menu is shown on a panel in VR; load a mission for stereo gameplay. Recenter by holding right stick click for about 0.65 seconds.

A streamed desktop alone is not a SteamVR VR connection. **Check headset** inspects an existing connection without starting SteamVR or the game; **Save & play** performs the launch sequence. Later launches can use **Blood Money VR** without reopening Settings.

No extra game entry in VD or SteamVR is required. An optional Steam/SteamVR library shortcut should target the installed `BloodMoneyVR.exe`, not the original game. The Steam edition starts through Steam when launched with the mod. For VD, select **Virtual Desktop (VDXR)** and connect to the PC in Virtual Desktop before playing. For Link/Air Link, enter its PC VR session and select that connection.

## Fixes in this update

- Saved connection choices are used after an update resets the rendering INI.
- VR module loading waits for the native game window and renderer. Loading DLLs successfully no longer counts as confirmation that VR output is working: pending or failed output is reported separately. Focus the running game and use F9 to retry headset output after restoring the connection.
- OpenXR controller pointing is corrected for SteamVR/VDXR, addressing hands and weapons angled upward by about 90 degrees.
- SteamVR receives matching left/right eye images from the same stereo pair.
- The OpenXR host supplies a headset playback hint when the runtime has no audio-device extension. Steam Link can select **Steam Streaming Speakers** even with Oculus/Virtual Desktop outputs installed and an older per-game preference. **Steam Streaming Microphone** is excluded from automatic playback. The mod checks active game audio sessions and leaves the global Windows output unchanged.

## Change modifiers

Open **Blood Money VR Settings → Modifiers**, choose **Verified** or **Experimental**, change the checkboxes and save. **Save & play** saves both pages and launches; **Save** saves the current page. Restart an already-running game to apply changes.

All 14 visible modifiers are enabled except **Physical crouching**. Disable **Automatic reload** for button-only empty-magazine reloads. Enable **Physical crouching** to crouch by lowering the headset; with it off, use B. For seated play, sit and recenter normally. Physical magazine reloads and body pouches remain disabled. See the [Alpha 3 notes](RELEASE-NOTES-0.1.8.172.md) for the retained combat, consumable and door changes.

This is still an alpha. Weapon-specific foregrips, experimental combat, civilian reporting and mission-specific interactions need more feedback. Local Quest/Touch connection checks do not establish compatibility with every headset or mission. Report the exact version, headset/connection, mission and steps. `Collect-Diagnostics.cmd` creates a local report for review and manual sharing; nothing is uploaded automatically.

---

## По-русски

### Установка и запуск через Steam Link

Закройте Blood Money и её VR-процессы, затем запустите `BloodMoneyVR-0.1.8.173-Setup.exe`. Установщик заменит прежнюю зарегистрированную копию и обновит ярлыки. Файлы и сохранения игры не меняются.

**Каждая установка и переустановка заменяет все семь INI настройками этого выпуска.** Модификаторы, ручные VR/аудионастройки, калибровка и положения хвата сбрасываются. Путь к игре, подключение и язык лаунчера сохраняются; при запуске выбранное подключение снова применяется после сброса INI.

1. Установите Steam и SteamVR на ПК, Steam Link — на Quest. Подключитесь к этому ПК из Steam Link в шлеме, разбудите контроллеры и закройте другие VR-игры.
2. Откройте **«Настройки Blood Money VR → Подключение и игра»**, выберите **SteamVR**, затем **«Сохранить и играть»**.
3. Лаунчер сам откроет SteamVR при необходимости и проверит подключённый шлем, отслеживание и готовность вывода перед запуском игры. Если подключение ещё не готово, игра не запускается: завершите VR-подключение, наденьте шлем и нажмите **«Повторить»**.
4. Закройте панель SteamVR/рабочий стол и выберите окно Blood Money. Меню отображается на панели в VR; стереоизображение игры проверяйте после загрузки миссии. Для центровки удерживайте нажатие правого стика около 0,65 секунды.

Трансляция рабочего стола сама по себе не означает, что SteamVR получила VR-подключение. Кнопка **«Проверить шлем»** проверяет уже работающую связь, но не открывает SteamVR и не запускает игру. Полную последовательность выполняет **«Сохранить и играть»**. В дальнейшем достаточно обычного ярлыка **Blood Money VR**.

Добавлять игру в SteamVR или VD не требуется. Если нужен отдельный пункт в библиотеке Steam/SteamVR, добавьте установленный `BloodMoneyVR.exe` как стороннюю игру. Обычный запуск оригинальной игры из Steam мод не загружает; мод сам использует Steam для Steam-издания. Для VD выберите **Virtual Desktop (VDXR)** и сначала подключите шлем к ПК в VD; для Link/Air Link войдите в его PC VR-сессию и выберите соответствующее подключение.

### Что исправлено

- Выбранное подключение сохраняет действие после обновления и сброса INI.
- Модули VR загружаются после готовности окна и рендера игры. Успешная загрузка DLL больше не выдаётся за подтверждение изображения в шлеме: ожидание и ошибка показываются отдельно. После восстановления подключения можно выбрать окно работающей игры и нажать F9 для повторной попытки.
- Исправлено направление контроллеров OpenXR, включая руки и оружие, смотревшие вверх примерно на 90° в SteamVR/VDXR.
- Левый и правый глаз SteamVR получают изображения из одной стереопары.
- Улучшен автоматический выбор звука: для Steam Link выбирается **Steam Streaming Speakers**, даже если установлены аудиоустройства Oculus/VD и у игры осталась старая настройка. **Steam Streaming Microphone** исключён из автоматического выбора вывода. Проверяются аудиосессии игры; глобальный аудиовыход Windows не меняется.

### Модификаторы

Откройте **«Настройки Blood Money VR → Модификаторы»** и выберите **«Проверенные»** или **«Экспериментальные»**. У каждой галочки есть пояснение. **«Сохранить и играть»** сохраняет обе страницы и запускает мод; **«Сохранить»** — текущую страницу. Уже запущенную игру нужно перезапустить.

По умолчанию включены все 14 видимых модификаторов, кроме **«Физического приседания»**. Отключите **«Автоперезарядку»**, если хотите перезаряжать пустое оружие только кнопкой. Без физического приседания используется B; для игры сидя достаточно сесть и отцентрироваться. Физическая перезарядка магазинами и подсумки выключены.

Это альфа: отдельные хваты оружия, экспериментальные удары, жалобы гражданских и действия в миссиях ещё требуют проверки. В отзыве укажите версию, шлем, подключение, миссию и шаги воспроизведения. `Collect-Diagnostics.cmd` создаёт локальный отчёт для ручной проверки и передачи, без автоматической отправки.
