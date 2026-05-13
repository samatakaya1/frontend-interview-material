[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/browser-api/browser-api.md)
---

# Что такое делегирование событий?

---

Делегирование событий — это прием, при котором обработчик ставят на общего родителя, а не на каждый дочерний элемент отдельно.

Он работает благодаря всплытию событий: событие сначала возникает на целевом элементе, а затем поднимается к родителям.

---

#### Пример

```js
const list = document.querySelector(".todo-list");

list.addEventListener("click", (event) => {
  const button = event.target.closest("button[data-id]");

  if (!button) {
    return;
  }

  removeTodo(button.dataset.id);
});
```

---

#### Что важно знать?

- Делегирование уменьшает количество обработчиков в DOM.
- Оно удобно для списков, таблиц, меню и элементов, которые добавляются динамически.
- Нужно проверять, что событие пришло именно от нужного элемента.
- Метод `closest` помогает найти подходящего предка от `event.target`.
- Делегирование не подходит для событий, которые не всплывают.

---

#### Итог

Делегирование событий делает обработку DOM-событий проще и эффективнее, особенно когда элементов много или они создаются после загрузки страницы.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/browser-api/browser-api.md)
