[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/browser-api/browser-api.md)
---

# Что такое Fetch API и как обрабатывать ошибки ответа?

---

**Fetch API** — это браузерный интерфейс для выполнения HTTP-запросов. Функция `fetch()` возвращает `Promise`, который выполняется с объектом `Response`.

Важно помнить: `fetch` не считает HTTP-статусы `400` или `500` сетевой ошибкой. Такой ответ нужно проверять вручную.

---

#### Пример

```js
async function getTodos() {
  const response = await fetch("/api/todos");

  if (!response.ok) {
    throw new Error(`Request failed: ${response.status}`);
  }

  return response.json();
}
```

---

#### Что важно знать?

- `fetch(url, options)` позволяет указать метод, headers, body и другие параметры.
- Для JSON-ответа обычно вызывают `response.json()`.
- Для JSON-запроса нужно передать `JSON.stringify(data)` и заголовок `Content-Type`.
- Сетевые ошибки попадают в `catch`, а HTTP-ошибки нужно проверять через `response.ok`.
- Запрос можно отменить через `AbortController`.

---

#### Частая ошибка

Нельзя передавать обычный объект в `body` без сериализации. Для JSON нужно использовать `JSON.stringify`.

---

#### Итог

Fetch API — стандартный способ делать HTTP-запросы в браузере. На интервью важно сказать, что `Promise`, который возвращает `fetch`, не отклоняется из-за HTTP-статусов 4xx/5xx.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/browser-api/browser-api.md)
