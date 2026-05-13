[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/html/html.md)
---

# Чем отличаются `block`, `inline` и `inline-block` элементы?

---

Эти значения определяют, как элемент ведет себя в потоке документа: занимает ли он всю строку, может ли находиться внутри строки текста и можно ли задавать ему размеры.

---

#### `block`

Блочный элемент начинается с новой строки и по умолчанию занимает всю доступную ширину родителя.

Примеры: `<div>`, `<p>`, `<section>`, `<h1>`.

```html
<div>Первый блок</div>
<div>Второй блок</div>
```

Для блочных элементов работают `width`, `height`, `margin` и `padding`.

---

#### `inline`

Строчный элемент не начинает новую строку и занимает только ширину своего содержимого.

Примеры: `<span>`, `<a>`, `<strong>`, `<em>`.

```html
<span>Текст</span>
<span>в одной строке</span>
```

Для `inline`-элементов `width` и `height` обычно не работают так, как для блоков.

---

#### `inline-block`

`inline-block` ведет себя как строчный элемент снаружи, но как блочный внутри.

Он может стоять в одной строке с другими элементами, но ему можно задавать `width`, `height`, `padding` и `margin`.

```css
.button {
  display: inline-block;
  width: 120px;
  padding: 8px 12px;
}
```

---

#### Итог

`block` занимает отдельную строку, `inline` живет внутри строки текста, а `inline-block` совмещает оба поведения. На собеседовании важно показать, что отличие не только во внешнем расположении, но и в том, как работают размеры и отступы.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/html/html.md)
