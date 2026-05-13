[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/accessibility/accessibility.md)
---

# Зачем нужны `alt` у изображений и доступные имена элементов?

---

`alt` описывает содержимое изображения для пользователей, которые не видят картинку или используют скринридер.

Доступное имя элемента помогает ассистивным технологиям понять, что делает кнопка, ссылка, поле ввода или другой интерактивный элемент.

---

#### Пример

```html
<img src="sales-chart.png" alt="Sales grew by 12% in April">

<button aria-label="Close modal">X</button>
```

---

#### Что важно знать?

- Информативное изображение должно иметь полезный `alt`.
- Декоративное изображение обычно получает пустой `alt=""`, чтобы скринридер его пропустил.
- Кнопка с одной иконкой должна иметь понятное доступное имя.
- Доступное имя может приходить из текста элемента, `aria-label`, `aria-labelledby` или связанного `label`.
- Не стоит писать `alt="image"` или `alt="picture"` — это не помогает понять смысл.

---

#### Итог

`alt` и доступные имена делают интерфейс понятным для скринридеров и клавиатурной навигации. Это базовая часть доступной верстки, а не дополнительная опция.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/accessibility/accessibility.md)
