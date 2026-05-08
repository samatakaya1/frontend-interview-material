[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/architecture/architecture.md)
---

# Как разделять UI-логику и бизнес-логику во frontend-приложении?

---

**UI-логика** отвечает за отображение интерфейса и пользовательские взаимодействия.

**Бизнес-логика** отвечает за правила приложения: расчеты, проверки, преобразование данных, условия доступности действий и работу с доменными сущностями.

---

#### Пример разделения

Компонент может отвечать за ввод пользователя и рендер:

```jsx
function CartTotal({ items }) {
  return <span>{calculateTotal(items)}</span>;
}
```

А расчет лучше вынести в отдельную функцию:

```js
function calculateTotal(items) {
  return items.reduce((sum, item) => sum + item.price * item.count, 0);
}
```

---

#### Зачем разделять?

- Компоненты становятся проще.
- Бизнес-правила легче тестировать.
- Логику можно переиспользовать.
- Изменения в UI меньше влияют на правила приложения.

---

#### Итог

Хорошая frontend-архитектура не держит всю логику внутри компонентов. На собеседовании важно показать, что UI должен быть тонким слоем, а правила приложения — отдельными функциями, моделями или сервисами.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/architecture/architecture.md)

