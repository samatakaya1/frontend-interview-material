[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/css/css.md)
---

# Чем отличаются Flexbox и Grid, и когда что использовать?

---

**Flexbox** и **Grid** — это CSS-инструменты для построения layout, но они решают разные задачи.

Flexbox лучше подходит для расположения элементов в одном направлении: строка или колонка. Grid удобнее, когда нужно управлять сеткой сразу по двум осям: строками и колонками.

---

#### Flexbox

Flexbox используют для одномерных раскладок.

```css
.toolbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 12px;
}
```

Подходит для меню, тулбаров, карточек в ряд, выравнивания кнопок и простого распределения пространства.

---

#### Grid

Grid используют для двумерных раскладок.

```css
.layout {
  display: grid;
  grid-template-columns: 240px 1fr;
  grid-template-rows: auto 1fr;
  gap: 16px;
}
```

Подходит для страниц, дашбордов, галерей, сложных сеток и layout с явными колонками и строками.

---

#### Главное отличие

- Flexbox распределяет элементы вдоль одной основной оси.
- Grid позволяет явно описать строки и колонки.
- Flexbox чаще используют внутри компонентов.
- Grid чаще используют для структуры страницы или крупного блока.

---

#### Итог

Если нужно выстроить элементы в ряд или колонку — чаще всего подойдет Flexbox. Если нужно управлять полноценной сеткой по горизонтали и вертикали — лучше использовать Grid.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/css/css.md)
