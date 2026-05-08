[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/browser-api/browser-api.md)
---

# Что такое всплытие и погружение событий?

---

В браузере событие проходит через DOM в несколько фаз.

**Capturing** — фаза погружения, когда событие идет от `window` и `document` к целевому элементу.

**Bubbling** — фаза всплытия, когда событие идет от целевого элемента обратно вверх по DOM-дереву.

---

#### Пример

```html
<div id="parent">
  <button id="button">Click</button>
</div>
```

```js
parent.addEventListener("click", () => {
  console.log("parent");
});

button.addEventListener("click", () => {
  console.log("button");
});
```

При клике на кнопку сначала сработает обработчик кнопки, потом обработчик родителя, потому что по умолчанию используется bubbling.

---

#### Что важно знать?

- `event.target` — элемент, на котором произошло событие.
- `event.currentTarget` — элемент, на котором сейчас выполняется обработчик.
- `event.stopPropagation()` останавливает дальнейшее распространение события.
- Третий аргумент `addEventListener` может включить фазу capturing.

---

#### Итог

Понимание bubbling и capturing помогает правильно работать с обработчиками событий и использовать делегирование событий.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/browser-api/browser-api.md)

