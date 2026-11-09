# Карта текстур Feral

Этот файл — рабочий чек-лист темы. Перед объявлением набора готовым сверяться с ним и обновлять отметки. Основа инвентаризации — каталог `Assets/` и ссылки на текстуры в Lua. `Feral/` содержит копии слотов, которые меняются выбранной темой; совпадение имени и размеров с базовым файлом обязательно.

Статусы: `[x]` готово и подключено; `[ ]` не сделано; `[~]` проверено частично или намеренно оставлено без темы.

## Feral: 29 слотов темы

### Рамки, здоровье, ресурс

- [x] `Assets/Feral/hp_low_case.tga` — рамка здоровья.
- [x] `Assets/Feral/hp_low_case_miror_s.tga` — зеркальная рамка здоровья.
- [x] `Assets/Feral/hp_low_case_mirror.tga` — рамка игрока.
- [x] `Assets/Feral/hp_low_case_mirror_b.tga` — рамка босса.
- [x] `Assets/Feral/hp_party_cage.tga` — рамка группы.
- [x] `Assets/Feral/hp_pet_cage.tga` — рамка питомца.
- [x] `Assets/Feral/power_low_case_s.tga` — рамка полосы ресурса.
- [x] `Assets/Feral/hp_low_case_miror_s_highlight.tga` — подсветка выбранной рамки.
- [x] `Assets/Feral/hp_party_highlight.tga` — подсветка рамки группы.
- [x] `Assets/Feral/hp_pet_highlight.tga` — подсветка рамки питомца.
- [x] `Assets/Feral/hp_boss_highlight.tga` — подсветка рамки босса.
- [x] `Assets/Feral/cast_back.tga` — подложка кастбара.
- [x] `Assets/Feral/cast_back_outline.tga` — подсветка кастбара.

### Портрет, ауры, ресурсные значки

- [x] `Assets/Feral/orb_case_low.tga` — рамка круглого портрета.
- [x] `Assets/Feral/portrait_frame_lo.tga` — малая рамка портрета.
- [x] `Assets/Feral/actionbutton-border square.tga` — квадратная рамка ауры/кнопки.
- [x] `Assets/Feral/actionbutton-border.tga` — круглая рамка кнопки.
- [x] `Assets/Feral/actionbuttonhighlight.tga` — подсветка кнопки.
- [x] `Assets/Feral/point_diamond.tga` — очко ресурса.
- [x] `Assets/Feral/group-finder-eye-orange.tga` — значок поиска группы.

### Неймплейты, панели, мини-карта и меню

- [x] `Assets/Feral/nameplate_backdrop.tga` — фон неймплейта.
- [x] `Assets/Feral/nameplate_outline.tga` — обводка неймплейта.
- [x] `Assets/Feral/nameplate_glow.tga` — подсветка неймплейта.
- [x] `Assets/Feral/info_bg.tga` — фон инфопанели.
- [x] `Assets/Feral/border-tooltip.tga` — рамка подсказки.
- [x] `Assets/Feral/minimap-border.tga` — обводка мини-карты.
- [x] `Assets/Feral/Background border.tga` — фон игрового меню.
- [x] `Assets/Feral/button wood large.tga` — обычная кнопка игрового меню.
- [x] `Assets/Feral/button red2 large.tga` — бордовая кнопка игрового меню.

Все 29 файлов присутствуют, подключены в `core.lua` и совпадают по пиксельным размерам с соответствующими базовыми слотами. 14 ключевых поверхностей получили отдельные новые иллюстрации; вспомогательные варианты собраны из того же набора мотивов и подогнаны под размеры слотов. Превью игровых TGA: [Feral-theme-assets-preview.png](../Images/Feral-theme-assets-preview.png).

## Остальные текстуры, которые использует аддон

### Кнопки способностей и Masque

- [ ] Добавить отдельный Feral-вариант Masque. Сейчас MyCustomFrames регистрирует `Azerite HEX`; для Feral в `core.lua` всё ещё выбран он. Файлы исходного набора: `Assets/MasqueSkin/actionbutton-backdrop.tga`, `actionbutton-border.tga`, `actionbutton-glow-white.tga`, `actionbutton-pushed.tga`, `actionbutton_circular_mask.tga`.
- [ ] Проверить дополнительные корневые рамки кнопок: `actionbutton-border square2.tga`, `actionbutton-border square highlight.tga`, `actionbutton-highlight.tga`, `button-background.tga`, `button-background-hover.tga`, `actionbutton-mask-circular.tga`.
- [ ] Перевести прямые ссылки на рамки аур/кнопок на `SkinResolve`, чтобы Feral применялся в Extra Button, предпросмотре аур игрока, аурах неймплейтов и подсветке аур.

### Чатовые пузырьки

- [~] `Assets/ChatBubble.blp` и `Assets/ChatBubbleVertical.blp`: текущий `ChatBubble.lua` не ссылается на эти файлы; он очищает фон нативных пузырьков, если включён `hideBackground`. Перед тем как делать новые варианты, решить в рамках темы, должны ли пузырьки оставаться без фона или получить Feral-подложку.

### Иконки мини-меню

- [ ] Сохранить значение каждого значка и добавить к нему общий Feral-ободок/когтистую рамку. Сейчас `MicroMenu.lua` напрямую использует эти файлы, без `SkinResolve`:
  - `Assets/02_crossed_hammers.tga`
  - `Assets/03_target_dart.tga`
  - `Assets/04_shield.tga`
  - `Assets/05_exclamation.tga`
  - `Assets/06_home.tga`
  - `Assets/07_bookmark.tga`
  - `Assets/08_eye.tga`
  - `Assets/09_horseshoe.tga`
  - `Assets/10_skull_banner.tga`
  - `Assets/11_w_emblem.tga`
  - `Assets/12_question_mark.tga`
- [~] `Assets/11_w_emblem_padded.tga` — не найдено в текущем списке значков MicroMenu; проверить, используется ли где-либо ещё.

### Значки ролей, фракций, боя и классификации

- [ ] Решить стиль общей рамки, сохраняя сами пиктограммы читаемыми: `grouprole-icons-heal.tga`, `grouprole-icons-tank.tga`, `icon_badges_dps.tga`, `icon_badges_heal.tga`, `icon_badges_tank.tga`, `icon_badges_lider.tga`.
- [ ] При необходимости добавить Feral-ободок к фракционным значкам, не менять их смысл: `icon_badges_alliance.tga`, `icon_badges_alliance_war_on.tga`, `icon_badges_horde.tga`, `icon_badges_horde_war_on.tga`.
- [ ] Проверить варианты, видимые на неймплейтах и юнитах: `icon_classification_boss.tga`, `icon_classification_elite.tga`, `icon_classification_generic.tga`, `icon_classification_rare.tga`, `icon-combat.tga`, `icon_skull_dead.tga`.
- [~] `raid_target_icons.tga`, `raid_target_icons_small.tga` — атласы игровых маркеров; смысл и цвет маркеров лучше сохранить. Проверить, должен ли Feral влиять на них вообще.
- [ ] Подключить Feral-версию `icon_exit_flight.tga` либо явно оставить стандартную.

### Панели настройки и онбординг

- [ ] Решить, распространять ли Feral-стиль на настройки и мастер установки. Отдельная группа: `SettingsPanelBackground.jpg`, `SettingsPanelWidget.png`, `PlumberSettingsPanel.png`, `OptionToggle.tga`, `Setup_Divider.tga`, `Setup_Dropdown.png`, `Setup_Checkbox.png`, `Setup_ChecklistIcon.png`, `Setup_CheckmarkGreen.blp`, все файлы в `Assets/Setup Assets/`.
- [~] Общие разделители, геометрия масок и служебные текстуры — не декоративные поверхности: `Divider_DropShadow_Vertical.tga`, `Divider_Gradient_Horizontal.tga`, `minimap-mask-opaque.tga`, `minimap-mask-transparent.tga`, `actionbutton-mask-circular.tga`, `blank.tga`. Не менять без отдельной проверки формы/маски.

### Заполнения полос, шрифты и другие ресурсы

- [x] Здоровье остаётся зелёным; энергия кошки и ярость медведя получают цвета из `Units.lua`, а не из запечённых полос.
- [x] Заголовки Feral используют встроенный кириллический шрифт WoW; мелкие подписи и числа сохраняют читаемый основной шрифт.
- [~] `hp_lowmid_bar_miror_s.tga`, `hp_lowmid_bar_miror_b.tga`, `hp_cap_bar.tga`, `hp_cap_bar mirror.tga`, `power_cap_s.tga`, `hp_party_bar.tga`, `hp_pet_bar.tga`, `cast_bar.tga`, `bar-progress.tga` — заполнения/полосы; проверить места применения перед возможной заменой.
- [~] Остальные варианты очков ресурса и маркеров (`point_crystal.tga`, `point_hearth.tga`, `point_plate.tga`, `point_rune1.tga`–`point_rune4.tga`, `point_dk_block.tga`) — тема Feral сейчас меняет только `point_diamond.tga`; проверить, какие варианты доступны в настройках и нужны ли им отдельные мотивы.
- [~] `Assets/Lato-Bold.ttf` и системный шрифт: проверить все вызовы шрифтов, прежде чем объявлять шрифтовую тему полностью покрытой.

## Правило обновления карты

При добавлении или изменении текстуры записать точное имя файла, место использования и статус. «Готово» ставить только после проверки, что Lua действительно выбирает Feral-файл, а не просто после появления файла в `Assets/Feral/`. После визуальной проверки в игре обновить превью и эту карту.
