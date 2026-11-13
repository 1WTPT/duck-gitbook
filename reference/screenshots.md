---
description: >-
  Меню и HUD Duck Util, Снежный голем и New Year Mode 4.0, а также Drone, Dark
  Summon, топор и Последняя дуэль в скриншотах.
---

# Интерфейс в скриншотах

Настоящие снимки интерфейса и визуальных сцен. Версия указана в подписи: базовые экраны — 3.3, сцены прежнего выпуска — 3.4, актуальные окна — 4.0. Ранее снятые демонстрации эффектов отмечены как архивные. Для примеров проверок, заявок и сетевых функций использованы демонстрационные ники и данные. Нажмите на изображение, чтобы рассмотреть его в полном размере.

## Личные напоминания о сменах — 4.0

Сохранение ключа в Спекхелпере сразу подключает расписание и включает напоминания. При уже привязанном VK других действий нет. Для первого подключения команда привязки появляется автоматически; после отправки боту настройка завершена. На снимках демонстрационные данные.

![Спекхелпер с управлением ключом и напоминаниями](../.gitbook/assets/ban-routing-4.0-spec-menu.png)

![Автоматическая команда привязки личного VK](../.gitbook/assets/reminders-link-4.0.png)

![Включённые напоминания после сохранения ключа](../.gitbook/assets/reminders-enabled-4.0.png)

[Управление и ограничения напоминаний](../nastroika/spec-helper.md)

## Меню, бинды и запись — 4.0

Карандаш показывает все доступные пункты. Глаз скрывает пункт, зачёркнутый глаз возвращает; шесть точек отдельно меняют порядок. Настройки сохраняются в конфиге.

![Карандаш: скрытые разделы с зачёркнутым глазом, отдельно шесть точек](../.gitbook/assets/duck-40-sidebar-eyes-edit.png)

![Обычное меню со скрытыми разделами](../.gitbook/assets/duck-40-sidebar-hidden.png)

![Бинды 4.0: отдельный спек заявки и «Следующий»](../.gitbook/assets/duck-40-shift-binds.png)

[Главное меню](../nastroika/duck-screen.md) · [Клавиши](../nastroika/keybindings.md)

## Рабочий Спекхелпер — 4.0

В GUI и HUD старые заявки идут первыми. «Следующий» завершает текущую и выбирает самую старую оставшуюся. После конца смены можно доработать очередь. «Наказать» у участника и «Бан» в HUD открывают обычное меню цели с игровыми командами. Отдельные «Бан на сайте» под заявкой и «Бан: сайт» в шапке HUD ведут к tink.work; в окне сайта можно выбрать игрока, срок и причину. Все ники демонстрационные; реальные наказания не выдавались.

![Развёрнутый Спекхелпер: очередь от старых к новым и обычные наказания и отдельный бан на сайте](../.gitbook/assets/ban-routing-4.0-spec-wide.png)

![Обычное меню Спекхелпера с единственной кнопкой «Следующий»](../.gitbook/assets/ban-routing-4.0-spec-menu.png)

![Отдельное подтверждение tink.work с выбором участника](../.gitbook/assets/ban-routing-4.0-site-ban-player.png)

![HUD: обычное наказание и отдельный бан на сайте](../.gitbook/assets/ban-routing-4.0-spec-hud.png)

Шестерёнка управляет автоспеком после «Следующий», задержкой и мини-HUD с одной активной заявкой.

![Шестерёнка Спекхелпера: автоспек, задержка 0,6 с и мини-HUD](../.gitbook/assets/duck-40-shift-settings.png)

![Мини-спекхелпер с активной заявкой и её участниками](../.gitbook/assets/duck-40-shift-hud-mini.png)

[Управление Спекхелпером и ограничения интеграции](../nastroika/spec-helper.md)

## Смены и запись — 4.0

В обновлённых окнах 4.0 используются отдельные панели для видео, текста ответа и назначенных заявок. На снимках демонстрационные данные.

![Окно ответа на апелляцию с демонстрационным клипом](../.gitbook/assets/appeal-4.0.png)

![Начало записи: с подтверждения смены по умолчанию или с первого спека](../.gitbook/assets/duck-40-recording-start-settings.png)

[Спекхелпер](../nastroika/spec-helper.md) · [Записи](../nastroika/records-screen.md)

## Снежный голем — 4.0

Бан-эффект на основе скелета: появление в алых спиралях частиц, подход и выстрел снежком. На големе объёмная красно-белая шапка с кубиком-помпоном. Все кадры сняты в отдельном тестовом мире, без настоящего бана.

<figure><img src="../.gitbook/assets/snow-golem-3.5-summon.png" alt="Снежный голем появляется из земли в красных спиралях частиц"><figcaption><p>Появление Снежного голема · архивная демонстрационная сцена.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/snow-golem-3.5-hat.png" alt="Объёмная красная шапка с белым кантом и кубиком-помпоном на снежном големе"><figcaption><p>Снежный голем и новогодняя шапка · архивная демонстрационная сцена.</p></figcaption></figure>

[Настройки появления, выстрела и случайного выбора](../moduli/ban-effect.md)

## New Year Mode — 4.0

Снег, игрушки и гирлянды включаются в **Right Shift → Разное → Interface → Меню → New Year Mode**. По умолчанию выключено. Украшения развёрнуты под разными углами и расположены на разной высоте; снежный налёт на нижней стороне игрушек повторяет форму шара или звезды, с неровной кромкой и мягкой тенью. Красные и изумрудные шары, золотые звёзды и цветные лампочки сгенерированы в высоком разрешении и плавно уменьшаются под размер GUI. Шапка плотно заходит на раму и закрывает верхние углы. Все снимки ниже сделаны в отдельном тестовом клиенте; HUD сохраняет обычный вид.

<figure><img src="../.gitbook/assets/preview-snow-4.0.png" alt="Снежные шапки с игрушками и гирляндами на меню и окне предпросмотра"><figcaption><p>Меню и предпросмотр · New Year Mode, Duck Util 4.0.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/dialog-snow-4.0.png" alt="Диалог логов со снежной шапкой"><figcaption><p>Диалоги Duck Util · New Year Mode, версия 4.0. Демонстрационные данные.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/wheel-snow-4.0.png" alt="Снежная шапка повторяет верхнюю дугу кругового меню цели"><figcaption><p>Круговое меню цели · New Year Mode, Duck Util 4.0.</p></figcaption></figure>

[Как включить и что меняет режим](../moduli/interface.md)

## Последняя дуэль — 3.4

<figure><img src="../.gitbook/assets/effects-3.4/last-duel.png" alt="Отдельная камера Последней дуэли с мечом и копией игрока"><figcaption><p>Последняя дуэль · Duck Util 3.4. Отдельный тестовый мир, без реального бана.</p></figcaption></figure>

[Камера, управление и виртуальная платформа](../moduli/last-duel.md)

## Drone и новые сцены

<figure><img src="../.gitbook/assets/effects-3.4/drone-fpv.png" alt="FPV Drone приближается к игроку"><figcaption><p>FPV Drone · Демонстрационная сцена 3.4.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/effects-3.4/dark-summon.png" alt="Dark Summon обхватывает копию игрока по бокам"><figcaption><p>Dark Summon · Демонстрационная сцена 3.4.</p></figcaption></figure>

[Drone, топор и остальные бан-эффекты](../moduli/ban-effect.md) · [Настройки Dark Summon](../moduli/dark-summon.md)

## Меню и модули

<figure><img src="../.gitbook/assets/screenshots-3.3/module-theme.png" alt="Настройки модулей в едином меню"><figcaption><p>Настройки модулей в едином меню · Duck Util 3.3.</p></figcaption></figure>

[Список модулей](../vozmozhnosti/modules-overview.md) · [Главное меню](../nastroika/duck-screen.md) · [Клавиши](../nastroika/keybindings.md)

## Рабочие страницы 3.3

<figure><img src="../.gitbook/assets/screenshots-3.3/page-check.png" alt="Проверка и переписка"><figcaption><p>Проверка и переписка · Duck Util 3.3. Демонстрационные данные.</p></figcaption></figure>

[Рабочие страницы](../nastroika/menu-pages.md) · [Ветка](../nastroika/branch-screen.md)

## HUD и свой дизайн

<figure><img src="../.gitbook/assets/screenshots-3.3/hud-editor.png" alt="Редактор собственного вида HUD"><figcaption><p>Редактор собственного вида HUD · Duck Util 3.3.</p></figcaption></figure>

[Расположение панелей и редактор](../nastroika/hud-editor.md) · [HUD в игре](../vozmozhnosti/hud.md) · [Обмен конфигами](../vozmozhnosti/configs.md)

## Цель и эффекты

<figure><img src="../.gitbook/assets/screenshots-3.3/module-ban-effect.png" alt="El Drifto в предпросмотре настроек"><figcaption><p>El Drifto в предпросмотре настроек · Duck Util 3.3.</p></figcaption></figure>

[Три вида меню цели](../nastroika/target-menu-ui.md) · [Ban Effect](../moduli/ban-effect.md) · [Player Model](../moduli/player-model.md)

## Игры и сообщество

<figure><img src="../.gitbook/assets/screenshots-3.3/durak.png" alt="Дурак в Duck Util"><figcaption><p>Дурак в Duck Util · Duck Util 3.3. Демонстрационные данные.</p></figcaption></figure>

[Все игровые экраны](../vozmozhnosti/games.md) · [Сообщество](../nastroika/social-view.md)
