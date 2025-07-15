# Проект по автоматизации тестирования WEB UI системы eDiscovery

## Используемые инструменты:
1. Язык программирования — Java 17
2. Паттерн проектирования — PageObject
3. Сборщик проекта — Gradle
4. Отчетность — Allure Report
5. Тестовый фреймворк — JUnit 5
6. Библиотека для тестирования WEB UI - Selenide
7. Управление контейнерами с браузерами - Selenoid
8. Контейнеризация - docker

## Структура проекта (пакеты):
- helpers - пакет с вспомогательными классами для настройки драйвера браузера и прикладывания артефактов (скриншоты, логи, видео) в отчёт Allure
![image](/images/project_structure/helpers.png)

- pages - пакет, содержащий PageObject классы для взаимодействия со страницами
![image](/images/project_structure/pages.png)

- tests - пакет с тестами
![image](/images/project_structure/tests.png)

## Жизненный цикл теста:
### Каждый тестовый класс расширяет базовый класс TestBase
![image](/images/testBase.png)
- Перед каждым тестом происходит выполняется конфигурирование драйвера
- Выполняется тестовый сценарий
- После каждого теста в тестовый отчёт прикладываются:
  - Скриншот последнего состояния перед окончанием теста
  - DOM дерево страницы перед окончанием теста
  - Логи из консоли браузера
  - Видео прохождения теста

## Отчёт от тестировании:
### Суммарная информация об итогах тестирования
![image](/images/test_report/overview.png)

### Отчёт о тестах в разрезе сьютов
![image](/images/test_report/suites.png)

### Графики с процентным соотношением успешных/неуспешных, пропущенных тестов; соотношению количества тестов по важности/продолжительности
![image](/images/test_report/graphs.png)

### Отчёт о тестировании в разрезе Epic / Feature / Story
![image](/images/test_report/behaviors.png)

### Тестовый сценарий состоит из шагов с информацией по выполнению каждого шага
![image](/images/test_report/steps.png)

### Для каждого тестового сценария в артефакты сохраняется:
- Скриншот последнего состояния перед окончанием теста
![image](/images/test_report/artifacts/screenshot.png)

- DOM дерево страницы перед окончанием теста
![image](/images/test_report/artifacts/pageSource.png)

- Логи из консоли браузера
![image](/images/test_report/artifacts/logs.png)

- Видео прохождения теста
![image](/images/test_report/artifacts/video.png)

![](/video/artifactsVideo.mp4)

### Тесты выполняются в несколько потоков для оптимизации времени выполнения
![image](/images/test_report/threads.png)
![image](/images/project_structure/threadsGradle.png)

