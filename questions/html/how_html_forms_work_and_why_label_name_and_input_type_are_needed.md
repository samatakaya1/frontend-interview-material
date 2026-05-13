[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/html/html.md)
---

# Как работают HTML-формы и зачем нужны `label`, `name` и `input type`?

---

HTML-форма собирает данные пользователя и отправляет их на сервер или передает JavaScript-коду для обработки.

Основные элементы формы — это `form`, поля ввода, подписи к ним и кнопка отправки.

---

#### Пример

```html
<form action="/login" method="post">
  <label for="email">Email</label>
  <input id="email" name="email" type="email" required>

  <button type="submit">Submit</button>
</form>
```

---

#### Что важно знать?

- `label` связывает текстовую подпись с полем и улучшает доступность.
- Атрибут `for` у `label` должен совпадать с `id` поля.
- `name` определяет имя параметра, с которым значение поля уйдет при отправке формы.
- `type` помогает браузеру выбрать правильное поведение: `email`, `password`, `checkbox`, `radio`, `submit` и другие.
- Нативная HTML-валидация работает через атрибуты вроде `required`, `minlength`, `pattern`.

---

#### Итог

Формы в HTML — это не просто набор полей. Хорошая форма использует правильные типы полей, связанные `label` и понятные `name`, чтобы быть удобной, доступной и корректно передавать данные.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/html/html.md)
