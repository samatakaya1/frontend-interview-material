[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/accessibility/accessibility.md)
---

# Что такое ARIA и когда его использовать?

---

**ARIA (Accessible Rich Internet Applications)** — это набор HTML-атрибутов, которые помогают assistive technologies понимать элементы интерфейса, если обычной семантики HTML недостаточно.

---

#### Пример

```html
<button aria-expanded="false" aria-controls="menu">
  Menu
</button>

<ul id="menu" hidden>
  <li>Profile</li>
  <li>Settings</li>
</ul>
```

`aria-expanded` сообщает, раскрыт ли связанный элемент.

---

#### Когда использовать ARIA?

- Для сложных кастомных компонентов.
- Когда нельзя выразить состояние обычным HTML.
- Для подсказок screen reader.

---

#### Важное правило

Если можно использовать нативный HTML-элемент, лучше использовать его. Например, `button` лучше, чем `div role="button"`.

---

#### Итог

ARIA дополняет семантический HTML, но не заменяет его. На собеседовании важно сказать: сначала нативная семантика, потом ARIA только там, где она действительно нужна.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/accessibility/accessibility.md)

