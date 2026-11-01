# События и хуки

Список основных событий и хуков, используемых в Duck Util.

## Клиентские события Fabric

| Событие | Описание |
|---------|----------|
| `ClientTickEvents.END_CLIENT_TICK` | Основной цикл обновления всех систем мода |
| `ClientLifecycleEvents` | События жизненного цикла клиента |
| `ScreenEvents` | События экранов (открытие, закрытие) |
| `ScreenMouseEvents` | События мыши на экранах |
| `ClientPlayConnectionEvents` | События подключения к серверу |
| `ClientReceiveMessageEvents` | Получение сообщений из чата |
| `ClientSendMessageEvents` | Отправка сообщений в чат |
| `WorldRenderEvents` | Отрисовка мира |
| `HudElementRegistry` | Регистрация элементов HUD |

## Внутренние системы

| Система | Метод | Описание |
|---------|-------|----------|
| `Modules` | `tick(client)` | Обновление всех модулей каждый тик |
| `Modules` | `init()` | Инициализация и регистрация модулей |
| `DuckConfig` | `tick()` | Обновление конфигурации |
| `License` | `ok()` | Проверка активности лицензии |
| `Toasts` | `info(Kind, ...)` | Показ уведомления |
| `CheckTracker` | `tick(client)` | Отслеживание проверок |
| `QuickResponses` | `tick(client)` | Быстрые ответы на сообщения |
| `TargetManager` | `tick(client, ...)` | Обновление цели |
| `BanLog` | `tick()` | Обновление лога банов |
| `Playtime` | `tick()` | Таймер времени игры |
| `WorkTimer` | `tick(client)` | Таймер работы |
| `KpdGoals` | `tick()` | Цели КПД |
| `ChatBans` | `tick(client)` | Отслеживание банов в чате |
| `Detector` | `tick(client)` | Детектор читов |
| `BanEffects` | `tick(client)` | Эффекты банов |
| `ModulePreview` | `tick(client)` | Предпросмотр модулей |

## Обработка сообщений

- `suggestPlayers` — подсказка ников из таба для аргументов команд
- `ChatBans.tick` — обработка бан-сообщений из чата
- `QuickResponses.tick` — быстрые ответы с галочкой (`FixTimer`, 2 мин)

## Отрисовка

- `UiRender.submit` — отправка на отрисовку (SDF/MSDF шейдеры)
- `DuckHud.unit()` — 1 единица = 1 пиксель при 1080p
- `GlassScreen.glassAmount` — количество стекла фона
- `post_effect/glass_*` — пост-эффекты стекла

## Ввод

- `keyPressed(KeyInput)` — обработка нажатий клавиш
- `mouseClicked(Click, doubled)` — обработка кликов мыши
- `charTyped(CharInput)` — ввод символов

## Потокобезопасность

Из фоновых потоков только через `MinecraftClient.execute`.