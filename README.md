# Команды

- 1. Запуск контейнера

```bash
docker run hello-world
```

- 18. Публикация портов контейнера

```bash
docker run -d -p 8080:80 nginx
```

- 19. Разные порты для разных контейнеров

```bash
docker run -d -p 8080:80 nginx
docker run -d -p 8081:80 nginx
```

- 20. Подключение портов

```bash
docker run -d -v ${PWD}/nginx:/usr/share/nginx/html -p 8088:80 nginx
```

- 22. Автоматическое удаление остановленных контейнеров

```bash
docker run -it --rm busybox
```

- 23. Разделение команды на строки

```bash
docker run \
    --name my-nginx \
    -d \
    -v ${PWD}/nginx:/usr/share/nginx/html \
    -p 8088:80 \
    --rm \
    nginx
```
