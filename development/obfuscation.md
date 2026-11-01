# Обфускация и защита кода

Duck Util использует многоуровневую защиту кода.

## ProGuard

Команда: `.\gradlew obfJars` → создаёт `-obf.jar`:
- Все классы упаковываются в пакет `dev.wantop.o`
- Имена заменяются по словарю `tools/proguard-dict.txt`
- `-keep` для миксинов, точек входа, `values()`/`valueOf` энумов

## Шифрование строк

Инструмент `tools/stringobf`:
- Шифр строк с ключом из имени класса
- Срез generic-сигнатур (не затрагивает миксины)
- Статические вызовы между классами через `invokedynamic`

## Проверка обфускации

- `tools/ObfCheck.java` (JDK 21 + asm, asm-tree)
- `.\gradlew runObfClient` (`run-obf`, ключей нет)

## Ограничения

- Рефлексию по именам классов мода не заводить (имена обфусцированы)
- Миксины не обфусцируются

## Сборка

Обычная сборка: `.\gradlew build` → `duck-util-<v>.jar`  
Lite-версия не собирается.

## Java версии

- Сборка и запуск: JDK 25 (`JAVA_HOME`)
- Инструменты обфускации: JDK 21 (`C:\Program Files\Eclipse Adoptium\jdk-21.0.11.10-hotspot\bin\`)
- API — только через `javap` по `minecraftMaven/…build.6-v2.jar`