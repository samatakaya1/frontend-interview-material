[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/css/css.md)
---

# Чем отличаются `static`, `relative`, `absolute`, `fixed` и `sticky`?

---

Свойство `position` определяет, как элемент располагается в документе и относительно чего работают координаты `top`, `right`, `bottom` и `left`.

По умолчанию элементы имеют `position: static` и участвуют в обычном потоке документа.

---

#### Пример

```css
.card {
  position: relative;
}

.badge {
  position: absolute;
  top: 8px;
  right: 8px;
}
```

В этом примере `.badge` будет позиционироваться относительно ближайшего предка с позиционированием, то есть относительно `.card`.

---

#### Что важно знать?

- `static` — обычное поведение элемента, координаты не применяются.
- `relative` — элемент остается в потоке, но может быть визуально сдвинут.
- `absolute` — элемент выходит из потока и позиционируется относительно ближайшего позиционированного предка.
- `fixed` — элемент выходит из потока и позиционируется относительно viewport.
- `sticky` — ведет себя как `relative`, пока не достигает заданного порога, затем становится похожим на `fixed` внутри своего контейнера.

---

#### Частая ошибка

Для `absolute` часто забывают задать `position: relative` родителю. Тогда элемент может позиционироваться не там, где ожидается.

---

#### Итог

Позиционирование важно для тултипов, бейджей, шапок, модальных окон и sticky-навигации. На интервью стоит объяснить, участвует ли элемент в потоке и относительно чего считаются координаты.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/css/css.md)
