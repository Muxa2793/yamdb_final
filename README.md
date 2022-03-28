![yamdb_workflow](https://github.com/Muxa2793/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

# YAMDB

## backend_CI/CD_homework

### API_YAMDB

#### Описание

API для создания рецензий на различные произведения искусства.

##### Запуск приложения

- подготовьте ваш сервер:
  - установите [Docker](https://docs.docker.com/engine/install/) и [Docker-compose](https://docs.docker.com/compose/install/)
- Сделайте fork данного репозитория к себе;
- Создайте в Repository secrets на Github следующие секреты:

```bash
SECRET_KEY=your_secret_key_for_django
DB_ENGINE=django.db.backends.postgresql
DB_NAME=postgres
POSTGRES_USER=postgres_user
POSTGRES_PASSWORD=postgres_password
DB_HOST=db
DB_PORT=5432
DOCKER_USERNAME=your_docker_username
DOCKER_PASSWORD=your_docker_password
YANDEX_CLOUD_HOST=your_host_ip (not necessary yandex)
YANDEX_CLOUD_USER=your_host_username (not necessary yandex)
SSH_KEY=your_private_ssh_key
TELEGRAM_TO=your_telegram_id
TELEGRAM_TOKEN=your_bot_token
```

- запустите workflow;
- Создайте суперпользователя на сервере:

```bash
docker-compose exec web python manage.py createsuperuser
```

##### Описание API приложения можно посмотреть в документации проекта после запуска сервера

```bash
GET HOST_IP/redoc/
```

#### Технологии

    Python
    django rest_framework
    docker
    docker-compose

#### Авторы

Команда [Яндекс.Практикума](https://practicum.yandex.ru/profile/python-developer-plus/ "Яндекс.Практикум") и [Михаил Спиридонов](https://t.me/MikhailSpiridonov "Мой Telegram для связи").

#### License

MIT
