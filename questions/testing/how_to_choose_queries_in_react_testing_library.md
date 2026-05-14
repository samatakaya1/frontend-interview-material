[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/testing/testing.md)
---

# Как выбирать запросы (queries) в React Testing Library?

---

React Testing Library рекомендует искать элементы так, как их воспринимает пользователь. Поэтому приоритет имеют запросы (queries) по роли, доступному имени, `label` и видимому тексту.

Такой подход делает тесты ближе к реальному поведению интерфейса и часто улучшает доступность.

---

#### Пример

```jsx
screen.getByRole("button", { name: "Save" });
screen.getByLabelText("Email");
```

---

#### Что важно знать?

- `getByRole` обычно лучший выбор для кнопок, ссылок, полей, заголовков и других семантических элементов.
- `getByLabelText` хорошо подходит для полей формы.
- `getByText` полезен для видимого текста, но может быть менее устойчивым.
- `getByTestId` лучше оставлять как запасной вариант.
- Для асинхронного появления элемента используют `findBy...`.
- Если элемент может отсутствовать, используют `queryBy...`.

---

#### Частая ошибка

Не стоит начинать с CSS-селекторов или `data-testid`, если элемент можно найти через роль или label. Такой тест хуже отражает пользовательский сценарий.

---

#### Итог

Выбор запроса должен идти от пользовательского восприятия к техническим деталям: сначала `role` и `label`, затем текст, и только потом `data-testid`.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/testing/testing.md)
