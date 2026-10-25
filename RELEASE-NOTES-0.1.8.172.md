# Blood Money VR — Alpha 3 (0.1.8.172)

This release brings the connection/settings launcher and recent gameplay fixes into one installer. Updating now installs the complete current settings profile, so disabled options from an older installation cannot silently carry over.

## Install or update

Close Blood Money and its VR helpers, then run `BloodMoneyVR-0.1.8.172-Setup.exe`. Select your game executable and a separate mod folder. The installer replaces the previous registered copy and updates its shortcuts, including when you choose a different folder. Game files and saves are unchanged.

**Every installation, update and same-version reinstall replaces all seven mod INIs with this release's defaults.** This resets modifier choices, manual VR/audio settings, calibration and weapon-grip adjustments. The game path, launcher connection choice and launcher language are kept. If you want to reuse a manual adjustment, make your own copy before updating and reapply that adjustment afterward.

The supplied profile enables all 14 visible modifiers except **Physical crouching**. Physical reload remains disabled; ordinary button reload is available.

## Change modifiers

1. Open **Blood Money VR Settings** from the desktop or Start menu, or run `Settings-BloodMoney-VR.cmd` in the installed mod folder.
2. Open **Modifiers**. Use **Verified** and **Experimental** to browse the two lists. Each checkbox has a description.
3. Enable or disable the options you want. For example, disable **Automatic reload** for manual button reloads, or enable **Physical crouching** to crouch by lowering the headset. With physical crouching off, use B; recenter with F7 or a held right-stick click when sitting down.
4. Click **Save & play** to save both pages and launch. **Save** only saves the current page. Restart an already-running game to apply changes.

For normal play, use **Blood Money VR**. It uses the selected game and connection without reopening settings. In **Connection & game**, choose Quest Link/Air Link, Virtual Desktop (VDXR), SteamVR or system OpenXR. Connect the headset through that application before launching. Optional Steam/SteamVR shortcuts should point to the installed `BloodMoneyVR.exe`.

## Changes since 0.1.8.171

- Settings shortcuts are available on the desktop and in Start, with a settings entry inside the installed folder. Connection checks and executable compatibility checks help identify missing runtimes or an unknown game build.
- Reload startup messages follow the active mode. A launch-error dialog contains output from that attempt, without old success messages from earlier runs.
- Punches, gun-butt strikes and non-blade object hits use nonlethal head/body handling: head hits can knock out; body hits react, deal small nonlethal damage and accumulate a knockout. Blade swings retain lethal damage. These physical combat options are in **Experimental**.
- Coins use the original distraction behavior and are excluded from the mod's added hit/damage/knockout logic.
- Painkillers and adrenaline can be used by selecting them in inventory, holding the chosen hand's grip and closing inventory. Releasing grip before closing cancels the selection.
- A right-held fiber wire accepts its own trigger without requiring a second grip. Ordinary unlocked doors offer **Open Door** while crouching alongside the keyhole action.
- Attack recognition has been revised for victims and witnesses. The latest delayed recognition/report-to-guard behavior for civilians still needs manual mission testing.

## Compatibility and feedback

Steam Blood Money with Quest/Touch remains the primary setup. Virtual Desktop/VDXR head and hand tracking were checked locally. This does not establish compatibility with every mission, headset or OpenXR runtime; experimental combat and civilian recognition still need gameplay feedback.

Report the version, mission, headset/connection and reproduction steps. `Collect-Diagnostics.cmd` creates a local report for you to review and share manually. No game files or automatic report uploads are included.

---

## По-русски

### Установка и обновление

Закройте игру и VR-процессы и запустите `BloodMoneyVR-0.1.8.172-Setup.exe`. Выберите EXE игры и отдельную папку мода. Установщик заменит прежнюю зарегистрированную копию и обновит ярлыки, в том числе при смене папки. Файлы и сохранения игры не меняются.

**Каждая установка, обновление и переустановка той же версии заменяет все семь INI мода настройками этого выпуска.** Сбрасываются модификаторы, ручные настройки VR/звука, калибровка и положения хвата оружия. Путь к игре, способ подключения и язык лаунчера сохраняются. Нужные ручные правки предварительно скопируйте и внесите заново после обновления.

По умолчанию включены все 14 видимых модификаторов, кроме **«Физического приседания»**. Физическая перезарядка выключена; обычная кнопочная перезарядка доступна.

### Как менять модификаторы

1. Откройте **«Настройки Blood Money VR»** на рабочем столе или в «Пуск», либо `Settings-BloodMoney-VR.cmd` в установленной папке. При английском языке ярлык называется **Blood Money VR Settings**.
2. Перейдите в **«Модификаторы»**. Настройки разделены на **«Проверенные»** и **«Экспериментальные»**; у каждой галочки есть пояснение.
3. Выберите нужные функции. Например, отключите **«Автоперезарядку»**, чтобы перезаряжать кнопкой, или включите **«Физическое приседание»**, чтобы приседать опусканием шлема. Без этой галочки приседание работает по B. Для игры сидя сядьте и отцентрируйте вид по F7 или удержанием правого стика.
4. **«Сохранить и играть»** сохраняет обе страницы и запускает мод. **«Сохранить»** сохраняет только текущую страницу. Уже запущенную игру нужно перезапустить.

Для обычного запуска используйте **Blood Money VR**: заново открывать настройки каждый раз не требуется. В разделе **«Подключение и игра»** выберите Link/Air Link, Virtual Desktop (VDXR), SteamVR или системный OpenXR и подключите шлем через соответствующее приложение. Дополнительный ярлык в Steam/SteamVR должен вести на установленный `BloodMoneyVR.exe`.

### Что изменилось

- Настройки доступны с рабочего стола, из «Пуск» и из папки мода. Проверки подключения и EXE показывают доступность среды и совместимость выбранной игры.
- Исправлены сообщения о физической перезарядке при выключенной функции. Ошибка запуска показывает вывод текущей попытки.
- Кулак, приклад и брошенные предметы получают несмертельную логику попаданий в голову и тело; холодное оружие сохраняет смертельный урон. Эти физические механики находятся в «Экспериментальных».
- Монетка отвлекает по штатным правилам, без дополнительного урона или оглушения.
- Болеутоляющее и адреналин применяются выбором в инвентаре, удержанием хвата и закрытием инвентаря. Если отпустить хват до закрытия, выбор отменяется.
- Удавка в правой руке запускается её курком без второго хвата. В приседе у обычной незапертой двери доступны и замочная скважина, и отдельное открытие двери.
- Доработано распознавание нападающего пострадавшим и свидетелями. Последнее изменение отложенного опознания гражданскими и жалобы охране ещё требует ручной проверки в миссиях.

Основной вариант — Steam Blood Money и Quest/Touch. Работа головы и рук через Virtual Desktop/VDXR проверена локально; полное прохождение всех миссий и проверка всех шлемов/OpenXR-сред не заявляются. Для отзыва укажите версию, миссию, шлем, подключение и шаги воспроизведения. `Collect-Diagnostics.cmd` собирает локальный отчёт для ручной проверки и передачи.
