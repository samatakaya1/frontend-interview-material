[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/css/css.md)
---

# Что такое блочная модель CSS?

---

Блочная модель CSS описывает, из каких частей состоит размер элемента на странице.

У каждого элемента есть область контента, внутренние отступы `padding`, рамка `border` и внешние отступы `margin`.

---

#### Пример

```css
.card {
  width: 300px;
  padding: 16px;
  border: 1px solid #cccccc;
  margin: 24px;
}
```

---

#### Что важно знать?

- `content` — область, где находится текст, изображение или другой контент.
- `padding` добавляет пространство внутри элемента между контентом и рамкой.
- `border` находится вокруг `padding`.
- `margin` добавляет расстояние снаружи элемента.
- По умолчанию `width` задает ширину только контента.
- `box-sizing: border-box` включает `padding` и `border` в заданную ширину элемента.

---

#### Итог

Блочная модель помогает понимать реальные размеры элементов и расстояния между ними. На практике часто используют `box-sizing: border-box`, чтобы верстка была предсказуемее.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/css/css.md)
