![yamdb_workflow](https://github.com/Muxa2793/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

# YAMDB

## backend_CI/CD_homework

### API_YAMDB

#### Описание

API для создания рецензий на различные произведения искусства.

##### Запуск приложения

- Создайте в корне папки `infra` файл .env следующего наполнения:

```bash
SECRET_KEY=your_secret_key_for_django
DB_ENGINE=django.db.backends.postgresql
DB_NAME=postgres
POSTGRES_USER=postgres_user
POSTGRES_PASSWORD=postgres_password
DB_HOST=db
DB_PORT=5432
```

- Выполните следующую команду из папки `infra`:

```bash
docker-compose up -d --build
```

- После запуска контейнеров выполните следующие команды:

```bash
docker-compose exec web python manage.py migrate
docker-compose exec web python manage.py collectstatic --no-input
```

- Создайте суперпользователя:

```bash
docker-compose exec web python manage.py createsuperuser
```

##### Описание API приложения можно посмотреть в документации проекта после запуска сервера

```bash
GET http://127.0.0.1:8000/redoc/
```

#### Технологии

    Python
    django rest_framework

#### Авторы

Команда [Яндекс.Практикума](http://example.com/ "Яндекс.Практикум") и [Михаил Спиридонов](https://t.me/MikhailSpiridonov "Мой Telegram для связи").

#### License

MIT
