[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/async/async.md)
---

# Чем отличаются `Promise.all`, `Promise.allSettled`, `Promise.race` и `Promise.any`?

---

Это методы для запуска нескольких асинхронных операций и получения результата по разным правилам.

Главное отличие — что считается успешным результатом и когда общий `Promise` завершается.

---

#### Пример

```js
const requests = [fetchUser(), fetchPosts(), fetchSettings()];

const results = await Promise.all(requests);
```

---

#### Что важно знать?

- `Promise.all` ждет выполнения всех промисов, но падает при первой ошибке.
- `Promise.allSettled` ждет завершения всех промисов и возвращает статусы `fulfilled` или `rejected`.
- `Promise.race` завершается вместе с первым завершившимся промисом, неважно успешно или с ошибкой.
- `Promise.any` возвращает первый успешный результат и падает только если все промисы завершились ошибкой.
- Для независимых запросов часто используют `Promise.all`, чтобы запускать их параллельно.

---

#### Итог

Выбор метода зависит от задачи: нужны все успешные результаты, все статусы, первый любой результат или первый успешный результат.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/async/async.md)
