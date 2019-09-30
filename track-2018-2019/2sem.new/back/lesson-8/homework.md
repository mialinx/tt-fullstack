## Домашнее задание 8


### Разворачивание проекта в Docker

Для выполнения ДЗ необходимо установить Docker и Docker-Compose

### Создание Dockerfile для Flask приложения

В качестве базового использовать образ `ubuntu:16.04` или `python:3.5`.
Директория проекта должна быть проброшена как volume.
При старте контейнер должен запускать внутри себя gunicorn с вашим приложением.

### Создание docker-compose для проекта

В compose файле нужно описать и связать: Flask приложение (обязательно) и/или
сервер базы данных (на ваш выбор какой, если не используете инстанс). При необходимости frontend-сервер (nginx)
так же запустить в отдельном контейнере.

Дополнительный баллы (в размере 5 штук) если сумеете прикрутить elasticsearch.

### Создание Makefile для проекта

Создать Makefile со следующими целями
- `run` для запуска проекта
- `stop` для остановки проекта
- `migrate` для применения миграций
- `test` для запуска тестов

### Критерии сдачи

Преподаватель должен иметь возможность, имея установленными только git, docker и docker-compose
склонировать проект, выполить команды `make test` и увидеть успешное выполнение тестов проекта.