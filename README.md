# Meeting Environment

Окружение для запуска приложения `meeting`.

## Инструкция

### Окружение

1. Создание образов (все образы лежит в папке `images`):

- `docker build -t meeting_db .` - создание образа БД.
- `docker build -t meeting_nginx .` - создание образа для nginx;
- `docker build -t meeting_backend .` - создание образа для backend;
- `docker build -t meeting_frontend .` - создание образа для frontend;

2. Создайте файлы с переменными среды окружения:

- `db.env` - postgres;
- `mongo.env` - mongo;
- `backend_dev.env` - backend, redis;
- `frontend_dev.env` - frontend;

3. Поднимите postgres `docker-compose up -d DB`.

4. Поднимите redis `docker-compose up -d REDIS`.

### Backend

1. Склонируйте проект в `./app/backend`

2. Установка зависимостей `docker-compose up INSTALL_BACK`.

3. Запуск миграций `docker-compose up MIGRATION_DEV`.

4. Запуск `docker-compose up SERVER_DEV`.

### Frontend

1. Склонируйте проект в `./app/frontend`

2. Установка зависимостей `docker-compose up INSTALL_FRONT`.

3. Запуск `docker-compose up FRONTEND_DEV`.

## Доступные инструкции:

- `DB` - запуск базы данных;
- `REDIS` - запуск базы данных;
- `MIGRATION_DEV` - запуск миграций;
- `INSTALL_BACK` - установка зависимостей backend;
- `INSTALL_FRONT` - установка зависимостей frontend;
- `EMPTY_BACK` - запуск контейнера backend без комманд;
- `EMPTY_FRONT` - запуск контейнера frontend без комманд;
- `SERVER_DEV` - запуск backend в dev режиме;
- `FRONTEND_DEV` - запуск frontend в dev режиме.
