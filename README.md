# Meeting Environment

Окружение для запуска приложения `meeting`.

## Инструкция

1. Склонируйте проекты:
  - `./app/backend` - backend;
  - `./app/frontend` - frontend.

2. Создайте файлы с переменными среды окружения:
  - `db.env` - БД;
  - `backend_dev.env` - dev сервера (находится в `app/backend`репозиторие);
  - `frontend_dev.env` - dev frontend (находится в `app/frontend`репозиторие);

3. Поднимите БД `docker-compose up DB`.

4. Запуск миграций `docker-compose up MIGRATION_DEV`.

5. Запуск миграций `docker-compose up SERVER_DEV`.

## Доступные инструкции:
- `DB` - запуск базы данных;
- `MIGRATION_DEV` - запуск миграций;
- `SERVER_DEV` - запуск сервера в dev режиме.

