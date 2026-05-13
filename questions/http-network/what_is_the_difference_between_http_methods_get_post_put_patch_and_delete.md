[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/http-network/http-network.md)
---

# Чем отличаются HTTP-методы `GET`, `POST`, `PUT`, `PATCH` и `DELETE`?

---

HTTP-метод показывает намерение клиента: получить данные, создать ресурс, заменить его, частично обновить или удалить.

---

#### `GET`

Используется для получения данных.

```http
GET /users/1
```

`GET` не должен изменять состояние на сервере.

---

#### `POST`

Обычно используется для создания нового ресурса или запуска действия.

```http
POST /users
```

Тело запроса содержит данные для создания.

---

#### `PUT`

Используется для полной замены ресурса.

```http
PUT /users/1
```

Клиент отправляет новое полное состояние ресурса.

---

#### `PATCH`

Используется для частичного обновления ресурса.

```http
PATCH /users/1
```

Клиент отправляет только поля, которые нужно изменить.

---

#### `DELETE`

Используется для удаления ресурса.

```http
DELETE /users/1
```

---

#### Итог

`GET` получает данные, `POST` создает или запускает действие, `PUT` заменяет ресурс целиком, `PATCH` обновляет часть ресурса, `DELETE` удаляет. На собеседовании важно объяснять не только названия методов, но и их смысл в API-дизайне.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/http-network/http-network.md)
