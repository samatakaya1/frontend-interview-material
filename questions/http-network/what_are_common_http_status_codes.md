[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/http-network/http-network.md)
---

# Что означают основные HTTP status codes?

---

HTTP status code — это числовой код ответа сервера, который показывает результат обработки запроса.

По коду клиент понимает, успешен ли запрос, нужна ли переадресация или произошла ошибка.

---

#### Пример

```txt
200 OK
201 Created
301 Moved Permanently
400 Bad Request
401 Unauthorized
403 Forbidden
404 Not Found
500 Internal Server Error
```

---

#### Что важно знать?

- `2xx` означает успешную обработку запроса.
- `3xx` означает редирект или необходимость дополнительного действия.
- `4xx` означает ошибку на стороне клиента: неверный запрос, нет авторизации, ресурс не найден.
- `5xx` означает ошибку на стороне сервера.
- `401` — пользователь не аутентифицирован, а `403` — аутентифицирован, но не имеет прав.

---

#### Итог

Status codes помогают быстро понять, что произошло с запросом. На интервью важно знать группы кодов и несколько самых частых примеров.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/http-network/http-network.md)
