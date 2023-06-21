# homework_de_2-2_physical_structure_db

### Описание:

Docker-контейнер для homework_de_2-2_physical_structure_db. Создает БД библиотеки.

### Шаблон наполнения env-файла:

Создайте файл .env с переменными окружения для работы с базой данных:

```
POSTGRES_PASSWORD=postgres # пароль для подключения к БД (установите свой)
POSTGRES_USER=postgres # логин для подключения к базе данных
POSTGRES_DB=testdb # название базы данных
```

### Команды для запуска приложения в контейнерах:

Собрать контейнер (из папки infra):

```
docker-compose up -d --build
```

Остановить контейнер:

```
docker stop ID-контейнера
```

Запустить контейнер:

```
docker run ID-контейнера
```

Подключиться к работающему контейнеру, запускать интерфейс psql и вносить новые данные:

```
docker exec -it infra-db-1 psql -U postgres testdb
```