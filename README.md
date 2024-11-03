# Современные методы DevOps
### Задание 

>Написать два докер-файла nginx и postgresql.
В конфиг **nginx** добавить возможность запрета POST запросов `limit_except POST { deny all; }`, а в конфиг базы постгреса добавить автоматическое создание пользователя `test` и пустой базы данных с тем же именем.
В качестве базового образа для **nginx** взять **alpine**, а в качестве базового образа для postgresql взять официальный с сайта [hub.docker.com]().

### Сборка и запуск контейнеров
Сборка образа Nginx
```bash
docker build -t magic-nginx -f Dockerfile-nginx .
```

Сборка образа PostgreSQL
```bash
docker build -t magic-postgres -f Dockerfile-postgres .
```

Запуск контейнеров
```bash
docker run -d -p 8080:80 magic-nginx
docker run -d -p 5432:5432 magic-postgres
```
