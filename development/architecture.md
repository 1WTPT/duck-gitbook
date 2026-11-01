# Архитектура

Duck Utilbuilt на Fabric для Minecraft 1.21.11. Пакет: `dev.wantop`, ресурсы: `duck-util`, ID мода: `duck-mod`.

## Основные компоненты

| Компонент | Пакет | Описание |
|-----------|-------|----------|
| **Модули** | `dev.wantop.module` | Система модулей и настроек |
| **Интерфейс** | `dev.wantop.ui` | Главное меню, окна, редакторы |
| **Рендер** | `dev.wantop.render` | Отрисовка, шейдеры, эффекты |
| **Цели** | `dev.wantop.target` | Система отслеживания целей |
| **Читы** | `dev.wantop.cheat` | Детекция читов и трекинг |
| **Отчёты** | `dev.wantop.report` | Учёт банов и отчёты |
| **Статистика** | `dev.wantop.stats` | Время работы, КПД |
| **Лицензия** | `dev.wantop.license` | Проверка лицензионного ключа |
| **Социальное** | `dev.wantop.social` | VK, игры, топы |
| **Оптимизация** | `dev.wantop.opt` | Твики производительности |

## Точка входа

- `DuckUtil` — `ModInitializer` (общая инициализация)
- `DuckUtilClient` — `ClientModInitializer` (клиентская инициализация, команды, события)

## Жизненный цикл

1. Загрузка мода Fabric → `DuckUtil.onInitialize()`
2. Инициализация клиента → `DuckUtilClient.onInitializeClient()`
3. Регистрация модулей → `Modules.init()`
4. Каждый тик клиента → `ClientTickEvents.END_CLIENT_TICK` → обновление всех систем

## GUI

Собственные SDF/MSDF-шейдеры, `UiRender.submit`. 1 единица = 1 пиксель при 1080p (`DuckHud.unit()`). Чёрное стекло, темы `T1/T2/T3`, акцент — состояние.

## Конфигурация

- Модули `module/*` → `Modules`
- Настройки `Setting.*` (`visibleWhen`, `section`, `resets`)
- Уведомления — `Toasts.info(Kind…)`
- `DuckConfig`: ключ — `Setting.key`, переезд — `movedFrom`
- Общее — `.duck` (`Configs`, облако — `CloudConfigs` → `configs.js`)
- Только этого ПК — `config/duck-util-local.json`