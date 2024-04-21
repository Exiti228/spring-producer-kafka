## Быстрый старт
* `docker compose up` для запуска Kafka.
## API
```http
POST {URL}:8081/metrics
```
## Формат запроса
```JSON
{
  "metricsId" : "string",
  "metrics" : [
    {
      "usedTime": 0,
      "usedMemory" : 0,
      "serviceName": "string",
      "wasError" : false
    },
    {
      "usedMemory" : 0,
      "serviceName":"string",
      "wasError" : false,
      "usedTime": 0
    }
  ]
}
```
Происходит валидация сообщения: metricsId, metrics не должны быть NULL. Если валидация пройдена, то сообщение отправится в Kafka.