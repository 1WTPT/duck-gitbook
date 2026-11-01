# Сборка мода

## Требования

- Java 25 (JDK 25) для `JAVA_HOME`
- Java 21 для инструментов (`tools/*`)
- Gradle (встроенный через `gradlew.bat`)

## Команды

| Команда | Описание |
|---------|----------|
| `.\gradlew.bat build` | Обычная сборка → `duck-util-<v>.jar` |
| `.\gradlew.bat runClient` | Запуск клиента для тестирования |
| `.\gradlew.bat obfJars` | Сборка с обфускацией → `-obf.jar` |
| `.\gradlew.bat runObfClient` | Запуск обфусцированного клиента |
| `.\gradlew.bat --stop` | Остановить зависший Gradle |

## Выходные файлы

| Файл | Описание |
|------|----------|
| `duck-util-<v>.jar` | Обычная сборка мода |
| `duck-util-<v>-obf.jar` | Обфусцированная сборка |

## Версия

Версия берется из `version` в `gradle.properties` (сейчас 3.2.2). При обновлении:
1. Поднимите версию в `gradle.properties`
2. Обновите `<р>/whats-new.txt` (1-я строка — версия)
3. Сборка записывает версию в `../duck-license-server/min-version.json`

## Ресурсы

Генерация ресурсов (из корня, JDK 21, `<р>` = `src/main/resources/assets/duck-util`):

- Шрифт: `java tools/MsdfAtlasGen.java Montserrat-Regular.ttf <р> montserrat`
- Иконки: `java tools/... lucide.ttf <р> icons $(cat tools/icons.txt)` (+ `font/IconCatalog`)
- Уточки: `tools/DuckRender.java <р>/textures/duck`
- Шары: `tools/BallDigits.java`
- Дурак: `tools/DurakArt.java`

## Ограничения

- Lite-версия не собирать
- Миры не грузить при тестировании
- Мышью не управлять при тестировании
- В сеть не ходить при тестировании