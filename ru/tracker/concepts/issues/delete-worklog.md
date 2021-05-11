# Удалить запись о затраченном времени

Запрос позволяет удалить запись о времени, затраченном на выполнение задачи.

## Формат запроса {#section_fkp_5ng_jfb}

Чтобы удалить записи о затраченном на задачу времени, используйте HTTP-запрос с методом `DELETE`:

```json
DELETE /{{ ver }}/issues/<issue-id>/worklog/<worklog-id>
Host: {{ host }}
Authorization: OAuth <токен>
{{ org-id }}
```

{% include [headings](../../../_includes/tracker/api/headings.md) %}

#### Ресурс {#req-resource}

- **\<issue-id\>**

    Идентификатор или ключ задачи.

- **\<worklog-id\>**

    Идентификатор записи о затраченном времени.


## Формат ответа {#section_wlq_d5g_jfb}

{% list tabs %}

- Запрос выполнен успешно

    В случае успешного выполнения запроса API возвращает ответ с кодом 204. Тело ответа отсутствует.

- Запрос выполнен с ошибкой

    Если запрос не был успешно обработан, ответное сообщение содержит информацию о возникших ошибках:

    HTTP-код ошибки | Описание ошибки
    --------------- | ---------------
    403 Forbidden | У пользователя или приложения нет прав на доступ к ресурсу, запрос отклонен.
    404 Not Found | Запрашиваемый ресурс не найден.
    500 Internal Server Error | Внутренняя ошибка сервиса. Попробуйте повторно отправить запрос через некоторое время.
    503 Service Unavailable | Сервис API временно недоступен.

{% endlist %}