[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/async/async.md)
---

# Как обрабатывать ошибки в `Promise` и `async/await`?

---

Ошибки в асинхронном JavaScript обычно обрабатывают через `.catch()` у `Promise` или через `try...catch` внутри `async`-функции.

`async/await` не меняет природу ошибки: отклоненный промис превращается в исключение в месте, где используется `await`.

---

#### Пример

```js
async function loadUser(id) {
  try {
    const response = await fetch(`/api/users/${id}`);

    if (!response.ok) {
      throw new Error(`Request failed: ${response.status}`);
    }

    const user = await response.json();

    return user;
  } catch (error) {
    console.error("Failed to load user", error);
    return null;
  }
}
```

---

#### Что важно знать?

- `.catch()` перехватывает отклонение в цепочке промисов.
- `try...catch` ловит ошибку только у тех операций, для которых выполнен `await` внутри блока `try`.
- Если забыть `await`, ошибка может не попасть в ожидаемый `catch`.
- Ошибку можно обработать локально или пробросить выше через `throw`.
- `finally` подходит для очистки состояния: скрыть loader, закрыть ресурс, сбросить флаг.

---

#### Частая ошибка

`Promise`, который возвращает `fetch`, не отклоняется при HTTP-статусах вроде `404` или `500`. Он отклоняется при сетевой ошибке. Статус ответа нужно проверять отдельно через `response.ok`.

---

#### Итог

Для цепочек промисов используют `.catch()`, для `async/await` чаще используют `try...catch`. Хороший ответ на интервью должен отдельно упомянуть `response.ok`, `finally` и проброс ошибки наверх.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/async/async.md)
