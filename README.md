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
![image](https://github.com/user-attachments/assets/5c2fe4db-9e81-42a8-9fe2-51aa65e6f971)

- pages - пакет, содержащий PageObject классы для взаимодействия со страницами
![image](https://github.com/user-attachments/assets/46f6e79f-8e2b-49c4-9431-9168837f2709)

- tests - пакет с тестами
![image](https://github.com/user-attachments/assets/0025888a-adaf-451c-9488-0cead9bafb3a)

## Жизненный цикл теста:
# Каждый тестовый класс расширяет базовый класс TestBase
![image](https://github.com/user-attachments/assets/49071aaf-6d2b-4f73-9086-83b42c480bb2)
- Перед каждым тестом происходит выполняется конфигурирование драйвера
- Выполняется тестовый сценарий
- После каждого теста в тестовый отчёт прикладываются:
  - Скриншот последнего состояния перед окончанием теста
  - DOM дерево страницы перед окончанием теста
  - Логи из консоли браузера
  - Видео прохождения теста

## Отчёт от тестировании:
### Суммарная информация об итогах тестирования
![image](https://github.com/user-attachments/assets/375d7514-d2d1-4056-b0e5-c064a39f0b72)

### Отчёт о тестах в разрезе сьютов
![image](https://github.com/user-attachments/assets/2ba21d45-edc1-4cc4-b4a7-521cd3860eeb)

### Графики с процентным соотношением успешных/неуспешных, пропущенных тестов; соотношению количества тестов по важности/продолжительности
![image](https://github.com/user-attachments/assets/64964ef2-a384-4ed3-803f-88310e698332)

### Отчёт о тестировании в разрезе Epic / Feature / Story
![image](https://github.com/user-attachments/assets/54a63f19-6711-4c2d-bd80-877a8d35d069)

### Тестовый сценарий состоит из шагов с информацией по выполнению каждого шага
![image](https://github.com/user-attachments/assets/d0bb80f6-8e61-4d82-a513-deeefa3e627a)

### Для каждого тестового сценария в артефакты сохраняется:
- Скриншот последнего состояния перед окончанием теста
![image](https://github.com/user-attachments/assets/54285db2-9f0c-4f7c-ab6f-400cb88fe249)

- DOM дерево страницы перед окончанием теста
![image](https://github.com/user-attachments/assets/273cfca9-4694-4f15-98b8-d52e4fb5a8a9)

- Логи из консоли браузера
![image](https://github.com/user-attachments/assets/67df1eaf-f540-470a-b082-41587332e08d)

- Видео прохождения теста
![image](https://github.com/user-attachments/assets/56864ee1-bd00-4556-a633-597d49b432a0)

https://github.com/user-attachments/assets/8252eaeb-223e-4610-8638-768b7b9c0db1

### Тесты выполняются в несколько потоков для оптимизации времени выполнения
![image](https://github.com/user-attachments/assets/4cddd78b-e5fe-4b97-8231-06832cab21e2)
![image](https://github.com/user-attachments/assets/12ae9f35-802f-4151-a3d0-08c1d7139e6f)

