[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/architecture/architecture.md)
---

# Что такое state management и когда нужен глобальный store?

---

**State management** — это подход к хранению, изменению и передаче состояния приложения.

Состояние может быть локальным внутри компонента, общим для нескольких частей интерфейса или серверным, загружаемым через API.

---

#### Локальное состояние

Если данные нужны только одному компоненту или небольшой группе дочерних компонентов, обычно достаточно локального state.

```jsx
function Dropdown() {
  const [isOpen, setIsOpen] = useState(false);

  return <button onClick={() => setIsOpen(!isOpen)}>Toggle</button>;
}
```

Такой state проще понимать и поддерживать.

---

#### Когда нужен глобальный store?

Глобальный store полезен, когда одно состояние нужно многим независимым частям приложения.

Примеры:

- данные авторизованного пользователя;
- настройки приложения;
- корзина;
- сложный workflow между разными экранами;
- состояние, которое неудобно передавать через много уровней props.

---

#### Когда глобальный store не нужен?

Не стоит выносить все состояние в глобальное хранилище автоматически. Это может усложнить код, добавить лишние зависимости и сделать изменения менее очевидными.

Часто достаточно `useState`, `useReducer`, context или библиотеки для server state, например React Query.

---

#### Итог

State management — это не обязательно Redux или глобальный store. Хороший выбор зависит от области использования данных: чем уже область, тем ближе к компоненту стоит держать состояние.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/architecture/architecture.md)
