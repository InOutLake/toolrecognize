## Задача "Бизнес №4. Сервис для автоматизации приема и выдачи инструментов авиаинженерам на базе машинного обучения и компьютерного зрения"

### Полезные ссылки к проекту
> [Сопроводительная документация к проекту](https://docs.google.com/document/d/1_FEDAf_apgzIffZSavqnj8Fy89nYhQKlHO13FpYFNNQ/edit?tab=t.0)
> 
> [Оригинальный репозиторий клиентской части](https://github.com/X1STY/lct-alft-front)
>
> [Оригинальный репозиторий серверной части](https://github.com/InOutLake/toolrecognize_backend)
> 
> [Swagger UI документация](https://api.sharpmindteam.ru/docs)
> 
> [Веб-приложение](https://sharpmindteam.ru)

### Локальная сборка

> Для запуска локальной сборки:
> ```bash
> docker compose --file docker-compose.local.yml --env-file local.env  up --build
> ```

### Dev сборка

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
