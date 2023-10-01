## Links:
* https://github.com/NosovArtem/prometheus_spring_web_example
* http://localhost:8080/actuator/prometheus
* http://localhost:8080/api/hello
* http://localhost:9090/targets

## Настройка Grafana
### Grafana должна быть в тойже сети что и prometheus:

1. user/password -> admin/admin
2. В поиск -> Data source -> Prometheus server URL -> http://prometheus:9090 -> Save & Test
3. В поиск -> Dashboard -> New Dashboard


### Docker commands:

1. Список запущенных контейнеров:

```
docker compose up -d
```

```
docker compose down
```

```
docker ps
```

2. Список всех контейнеров (включая остановленные)

```
docker ps -a
```

3. Больше информации о контейнере

```
docker inspect <container-id>
```

4. Удалить один или несколько контейнеров.

```
docker rm <container-id-1> <container-id-2>
```

5. Удалить все остановленные контейнеры

```
docker container prune
```

6. Остановить контейнер

```
docker stop <container-id>
```

7. Логи

```
docker logs <container-id>
docker logs -f my-container # Следить за логами в режиме "живого" вывода
docker logs --since 2022-01-01T00:00:00Z my-container # Вывести логи, начиная с определенного времени
docker logs --tail 100 my-container # Вывести последние 100 строк логов
```

8. Подключиться к linux контейнеру

```
docker exec -it <my-container> sh
```


