### Тестовое задание на позицию junior python разработчик

написать API, который бы по интервалу дат возвращал статистику по часам:
* количество всего заказов за час
* количество успешных заказов за час (статус = `SUCCESS`)
* среднее количество заказов за последние 7 часов
* отношение количества заказов за час к количеству заказов в тот же час предыдущего дня
* количество уникальных райдеров за час (учитывая заказы всех статусов)
* количество уникальных драйверов за час (учитывая заказы всех статусов)

в качестве источника данных использовать `fake-orders.csv`

Предполагается использование Flask и Pandas


### Пример работы получившегося сервиса

Request:
```
{
  date_start: '2016-06-02',
  date_end: '2016-06-02'
}
```

Response:
```
[{
  time: '2016-06-02T00:00:00Z',
  orders: 7,
  success_orders: 6,
  orders_mean_7h: 5.25,
  orders_h_over_h_24h: 0.95,
  riders: 4,
  drivers: 2
}, {
  time: '2016-06-02T01:00:00Z',
  orders: 12,
  success_orders: 9,
  orders_mean_7h: 7,
  orders_h_over_h_24h: 0.97,
  riders: 11,
  drivers: 6
},..]
```
