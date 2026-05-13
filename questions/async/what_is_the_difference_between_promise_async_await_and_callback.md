[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/async/async.md)
---

# Чем отличаются `Promise`, `async/await` и callback?

---

Callback, `Promise` и `async/await` — это способы работать с асинхронным кодом в JavaScript.

Они решают похожую задачу, но отличаются читаемостью, обработкой ошибок и способом композиции асинхронных операций.

---

#### Callback

Callback — это функция, которую передают другой функции, чтобы вызвать позже.

```js
loadUser(id, function (user) {
  console.log(user);
});
```

Минус callback-подхода — сложность при большом количестве последовательных операций. Код может превратиться в глубокую вложенность.

---

#### Promise

`Promise` представляет результат асинхронной операции: успешный или ошибочный.

```js
fetch("/api/user")
  .then((response) => response.json())
  .then((user) => console.log(user))
  .catch((error) => console.error(error));
```

`Promise` упрощает цепочки асинхронных действий и дает единый способ обрабатывать ошибки через `.catch`.

---

#### `async/await`

`async/await` — это синтаксис поверх `Promise`, который позволяет писать асинхронный код похожим на синхронный.

```js
async function loadUser() {
  try {
    const response = await fetch("/api/user");
    const user = await response.json();
    console.log(user);
  } catch (error) {
    console.error(error);
  }
}
```

Такой код часто проще читать, особенно когда операции идут последовательно.

---

#### Итог

Callback — базовый способ передать действие на потом. `Promise` описывает будущий результат асинхронной операции. `async/await` делает работу с `Promise` более читаемой. На практике в современном коде чаще используют `async/await`, но важно понимать, что внутри он все равно работает через `Promise`.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/async/async.md)
