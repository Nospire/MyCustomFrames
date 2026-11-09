# Карта текстур Feral

Этот файл — рабочий чек-лист темы. Перед объявлением набора готовым сверяться с ним и обновлять отметки. Основа инвентаризации — каталог `Assets/` и ссылки на текстуры в Lua. `Feral/` содержит копии слотов, которые меняются выбранной темой; совпадение имени и размеров с базовым файлом обязательно.

Статусы: `[x]` готово и подключено; `[ ]` не сделано; `[~]` проверено частично или намеренно оставлено без темы.

## Feral: игровые текстуры, UI и полный набор иконок

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
- [x] `Assets/Feral/point_crystal.tga` — альтернатива очка ресурса 32×32.
- [x] `Assets/Feral/point_hearth.tga` — альтернатива очка ресурса 64×64.
- [x] `Assets/Feral/point_rune1.tga` — вариант руны ресурса.
- [x] `Assets/Feral/point_rune2.tga` — вариант руны ресурса.
- [x] `Assets/Feral/point_rune3.tga` — вариант руны ресурса.
- [x] `Assets/Feral/point_rune4.tga` — вариант руны ресурса.
- [x] `Assets/Feral/point_dk_block.tga` — альтернативный значок ресурса 128×128.
- [x] `Assets/Feral/point_plate.tga` — подложка значков роли и кнопок мини-карты.
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

Все основные текстурыные слоты и 28 иконок подключены в `core.lua`; новые файлы совпадают по размерам и альфа-силуэтам с базовыми слотами. 14 ключевых поверхностей получили отдельные новые иллюстрации; вспомогательные варианты собраны из того же набора мотивов и подогнаны под размеры слотов. Превью игровых TGA: [Feral-theme-assets-preview.png](../Images/Feral-theme-assets-preview.png).

## Остальные текстуры, которые использует аддон

### Кнопки способностей и Masque

- [x] Зарегистрировать отдельный Masque-вариант `MCF Feral Claws`; Feral теперь ссылается на него. Текстуры находятся в `Assets/Feral/MasqueSkin/` (рамка, подложка, подсветка, нажатие и круглая маска).
- [x] Маске отдано имя `MCF Feral Claws` и приложены рамка, фон, нажатие, подсветка и круглая маска. Остался ручной выбор этого скина в группах Bartender/других кнопочных аддонов: API Masque не позволяет надёжно переключить группы, уже созданные сторонними аддонами.
- [x] Дополнительные варианты `actionbutton-border square2.tga`, `actionbutton-border square highlight.tga` и `cursor-highlight.tga` добавлены как переключаемые слоты. `actionbutton-highlight.tga`, `button-background.tga`, `button-background-hover.tga` не вызываются Lua; отдельная геометрическая маска `actionbutton-mask-circular.tga` намеренно остаётся неизменной и используется Extra Button.
- [x] Перевести прямые ссылки на рамки аур/кнопок на `SkinResolve` и добавить обновление уже созданных элементов: Extra Button, ауры игрока, предпросмотр аур и ауры неймплейтов.

### Чатовые пузырьки

- [x] `Assets/ChatBubble.blp` и `Assets/ChatBubbleVertical.blp` не используются `ChatBubble.lua`: фон нативных пузырьков скрывается. Feral-файлы для них не нужны, пока не меняется этот режим.

### Иконки мини-меню

- [x] Все 11 иконок мини-меню полностью перерисованы: сами молоты, мишень, щит, очаг, глаз и остальные предметы выполнены из меха, металла, кожи и кости. `MicroMenu.lua` выбирает варианты темы через `SkinResolve`:
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
- [x] `Assets/11_w_emblem_padded.tga` отсутствует в текущем списке иконок MicroMenu и не вызывается Lua; не является пропуском темы.

### Значки ролей, фракций, боя и классификации

- [x] Значки Альянса и Орды полностью перерисованы как отдельные фракционные эмблемы; сине-золотые цвета Альянса и красные цвета Орды сохранены, версии War Mode имеют отдельный арт: `icon_badges_alliance.tga`, `icon_badges_alliance_war_on.tga`, `icon_badges_horde.tga`, `icon_badges_horde_war_on.tga`.
- [x] Портретные значки ролей DPS/хил/танк/лидер и raid role heal/tank полностью перерисованы отдельными предметами, цвета и символы ролей читаемы: `icon_badges_dps.tga`, `icon_badges_heal.tga`, `icon_badges_tank.tga`, `icon_badges_lider.tga`, `grouprole-icons-heal.tga`, `grouprole-icons-tank.tga`.
- [x] Значки классификации, боя, смерти и выхода из полёта полностью перерисованы; `Nameplates.lua`, `NameplatesNext.lua`, `Portraits.lua` и `Minimap.lua` выбирают их через активную тему: `icon_classification_boss.tga`, `icon_classification_elite.tga`, `icon_classification_generic.tga`, `icon_classification_rare.tga`, `icon-combat.tga`, `icon_skull_dead.tga`, `icon_exit_flight.tga`.
- [x] `raid_target_icons.tga` и `raid_target_icons_small.tga` получили собственные Feral-атласы с исходным порядком и цветовым смыслом маркеров; оба пути внесены в список Feral и `SKINNABLE`.
- [x] Значок полёта сохраняет стандартный функциональный символ с Feral-рамкой; кнопки мини-карты используют подложку `point_plate.tga`.

### Панели настройки и онбординг

- [x] Настройки и мастер первого запуска получили Feral-оформление: `SettingsPanelBackground.jpg`, `SettingsPanelWidget.png`, `PlumberSettingsPanel.png`, `Setup_Divider.tga`, `Setup_Dropdown.png`, `Setup_Checkbox.png`, `Setup_ChecklistIcon.png` и все используемые файлы в `Assets/Feral/Setup Assets/`. `OptionToggle.tga` не существует в ресурсах и больше не применяется; `Setup_CheckmarkGreen.blp` заменён атласным чекмарком. Реализовано обновление созданных контролов и дропдауна редактора неймплейтов после смены темы.
- [x] Разделители `Divider_DropShadow_Vertical.tga` и `Divider_Gradient_Horizontal.tga` имеют Feral-варианты, подключённые к панели настроек. Маски `minimap-mask-opaque.tga`, `minimap-mask-transparent.tga`, `actionbutton-mask-circular.tga` и `blank.tga` намеренно остаются функциональными, без декоративной перекраски: они определяют геометрию/прозрачность.

### Заполнения полос, шрифты и другие ресурсы

- [x] Здоровье остаётся зелёным; энергия кошки и ярость медведя получают цвета из `Units.lua`, а не из запечённых полос.
- [x] Заголовки Feral используют встроенный кириллический шрифт WoW; мелкие подписи и числа сохраняют читаемый основной шрифт.
- [x] Полосы `hp_lowmid_bar_miror_s.tga`, `hp_lowmid_bar_miror_b.tga`, `hp_cap_bar.tga`, `hp_cap_bar mirror.tga`, `power_cap_s.tga`, `hp_party_bar.tga`, `hp_pet_bar.tga`, `cast_bar.tga` и `nameplate_bar.tga` получили нейтральную графитово-меховую фактуру с сохранёнными размерами и альфа-формой. Она не запекает цвета: цвет здоровья, ресурсов и каста по-прежнему задаёт игровая логика. Файлы подключены в `TEX_LIB`, `SKINNABLE` и Feral `files`. `bar-progress.tga` нигде не используется.
- [x] Все варианты очков ресурса (`point_crystal.tga`, `point_diamond.tga`, `point_hearth.tga`, `point_rune1.tga`–`point_rune4.tga`, `point_dk_block.tga`) получают Feral-значок из активной темы; `point_plate.tga` оформляет подложки.
- [x] `Lato-Bold.ttf` не используется. Основной текст остаётся штатным читаемым `FRIZQT`; заголовок главного меню и заголовок панели настроек переключаются на встроенный `MORPHEUS_CYR` в ruRU и `MORPHEUS` в других локалях. Шрифтовые файлы аддона менять не требуется.

В `Assets/Feral/` лежат 37 основных ранее созданных слотов, 28 полностью перерисованных иконок, оба атласа рейдовых маркеров, тема панелей/мастера и нейтральные Feral-заливки полос. Feral-арт использует чёрный мех, тёмный металл, бордовую кожу, кость и небольшие сине-золотые акценты Альянса. Превью полос: [Feral-statusbar-preview.png](../Images/Feral-statusbar-preview.png); превью значков: [Feral-icon-preview.png](../Images/Feral-icon-preview.png); мастер-атласы для правок: [Design/Feral-Icon-Art](Feral-Icon-Art/).

## Итоговый статус

Все реализуемые из аддона пункты карты закрыты. Единственное оставшееся действие пользователя — выбрать `MCF Feral Claws` внутри групп Masque, потому что Masque не предоставляет аддону API для надёжного переключения чужих групп. Динамическая проверка в живой игре не выполнена; статическая проверка файлов, маршрутов темы, размеров и альфа-каналов выполнена перед публикацией.

## Правило обновления карты

При добавлении или изменении текстуры записать точное имя файла, место использования и статус. «Готово» ставить только после проверки, что Lua действительно выбирает Feral-файл, а не просто после появления файла в `Assets/Feral/`. После визуальной проверки в игре обновить превью и эту карту.
