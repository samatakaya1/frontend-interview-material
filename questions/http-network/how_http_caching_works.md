[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/http-network/http-network.md)
---

# Как работает HTTP-кэширование?

---

HTTP-кэширование позволяет браузеру или промежуточному кэшу повторно использовать уже полученный ответ вместо нового запроса к серверу.

Кэширование ускоряет загрузку, снижает нагрузку на сеть и сервер, но требует корректных HTTP-заголовков.

---

#### Пример

```http
Cache-Control: max-age=3600
ETag: "app-v1"
```

`Cache-Control` говорит, как долго ответ можно считать свежим, а `ETag` помогает проверить, изменился ли ресурс.

---

#### Что важно знать?

- `Cache-Control: max-age=...` задает время свежести ответа.
- `no-cache` требует перепроверки у сервера перед использованием кэша.
- `no-store` запрещает сохранять ответ.
- `ETag` и `Last-Modified` используются для условных запросов.
- Если ресурс не изменился, сервер может ответить `304 Not Modified`.

---

#### Частая ошибка

`no-cache` не означает "не кэшировать". Он означает, что кэшированный ответ нужно валидировать перед повторным использованием.

---

#### Итог

HTTP-кэширование строится на заголовках свежести и валидации. На интервью важно различать `max-age`, `no-cache`, `no-store`, `ETag` и ответ `304`.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/http-network/http-network.md)
