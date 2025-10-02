# toolrecognize

> Для запуска локальной сборки:
> ```bash
> docker compose --file docker-compose.local.yml --env-file local.env  up --build
> ```

> Для запуска dev сборки:
> ```bash
> docker compose --file docker-compose.dev.yml --env-file dev.env  up --build
> ```
> Необходимые A-записи у DNS провайдера для работы dev сборки сервиса:
> 
> ```
> api.domain.ru #Основной REST API
> logs.domain.ru #Вывод логов из контейнеров 
> rmq.domain.ru #Для работы брокера сообщений (по https - консоль, по amqp - сам rmq)
> minio.domain.ru #S3-совместимое хранилище
> domain.ru #Клиентская часть приложения 
> ```
> Необходимые порты для работы dev сборки
>  ```
> 80 (HTTP)
> 443 (HTTPS)
> 5672 (RabbitMQ порт подключения)
> ```
