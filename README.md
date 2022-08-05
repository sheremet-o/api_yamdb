# Описание

Проект YaMDb собирает отзывы пользователей на различные произведения.

## Стек технологий

## Алгоритм регистрации пользователей
* Пользователь отправляет POST-запрос на добавление нового пользователя с параметрами email и username на эндпоинт /api/v1/auth/signup/.
* YaMDB отправляет письмо с кодом подтверждения (confirmation_code) на адрес email.
* Пользователь отправляет POST-запрос с параметрами username и confirmation_code на эндпоинт /api/v1/auth/token/, в ответе на запрос ему приходит token (JWT-токен).
* При желании пользователь отправляет PATCH-запрос на эндпоинт /api/v1/users/me/ и заполняет поля в своём профайле (описание полей — в документации).

## Установка
1. клонируйте/ скачайте себе репозиторий
2. установите виртуально окружение
3. активируйте venv, установите пакеты из requirements.txt
4. сделайте миграции и запустите проект командой python api_yamdb/manage.py runserver
