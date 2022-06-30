# Meeting Environment

Окружение для запуска приложения `meeting`.

## Инструкция

1. Склонируйте проекты:
  - `./app/backend` - backend;
  - `./app/frontend` - frontend.

2. Создание образов (все образы лежит в папке `images`): 
  - `docker build -t meeting_backend .` - создание образа для backend;
  - `docker build -t meeting_db .` - создание образа БД.

3. Создайте файлы с переменными среды окружения:
  - `db.env` - БД;
  - `backend_dev.env` - dev сервера (находится в `app/backend`репозиторие);
  - `frontend_dev.env` - dev frontend (находится в `app/frontend`репозиторие);

4. Поднимите БД `docker-compose up DB`.

5. Запуск миграций `docker-compose up MIGRATION_DEV`.

6. Запуск миграций `docker-compose up SERVER_DEV`.

## Доступные инструкции:
- `DB` - запуск базы данных;
- `MIGRATION_DEV` - запуск миграций;
- `SERVER_DEV` - запуск сервера в dev режиме.

