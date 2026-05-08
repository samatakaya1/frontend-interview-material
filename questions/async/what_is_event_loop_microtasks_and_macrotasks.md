[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/async/async.md)
---

# Что такое Event Loop, microtasks и macrotasks?

---

**Event Loop** — это механизм, который позволяет JavaScript выполнять асинхронный код, несмотря на то что основной поток выполнения однопоточный.

Он следит за call stack и очередями задач. Когда call stack пуст, Event Loop берет следующую задачу и передает ее на выполнение.

---

#### Пример

```js
console.log("start");

setTimeout(() => console.log("timeout"), 0);

Promise.resolve().then(() => console.log("promise"));

console.log("end");
```

Результат:

```text
start
end
promise
timeout
```

---

#### Почему так?

- Синхронный код выполняется первым.
- `Promise.then` попадает в очередь microtasks.
- `setTimeout` попадает в очередь macrotasks.
- Microtasks выполняются раньше macrotasks.

---

#### Итог

Event Loop объясняет порядок выполнения синхронного и асинхронного кода. На собеседовании часто просят предсказать вывод кода с `setTimeout`, `Promise` и `console.log`.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/async/async.md)

