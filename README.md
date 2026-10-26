# API_CI_TestHW — REST API-тесты мобильного банка

[![Build status](https://ci.appveyor.com/api/projects/status/wcv6899rlgf69kbp?svg=true)](https://ci.appveyor.com/project/MetsukiSutemi0979/api-ci-testhw)

Домашняя работа курса «Тестировщик»: тестирование REST API сервиса мобильного банка.

## Что покрыто
- Методы `GET /api/v1/demo/accounts` и связанные сценарии
- Проверка статус-кодов, формата ответа, валидация JSON-ответа
- Эволюция тестов от простого `given().get(...)` до `RequestSpecBuilder` с общими пред/постусловиями (V1 → V6)

## Стек
- Java 15, Gradle, JUnit 5
- REST Assured (Given-When-Then, спецификации запросов, `LogDetail`)
- CI: AppVeyor (бейдж выше)

## Запуск
```PowerShell
java -jar ./artifacts/app-mbank.jar   # SUT на localhost:9999
./gradlew clean test
```