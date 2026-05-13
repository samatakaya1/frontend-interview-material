[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/react/react.md)
---

# Зачем нужны `key` в списках React?

---

`key` помогает React понять, какой элемент списка изменился, добавился или удалился между рендерами.

Без стабильных ключей React может неправильно переиспользовать элементы и состояние компонентов.

---

#### Пример

```jsx
function TodoList({ todos }) {
  return (
    <ul>
      {todos.map((todo) => (
        <li key={todo.id}>{todo.title}</li>
      ))}
    </ul>
  );
}
```

---

#### Что важно знать?

- `key` должен быть уникальным среди соседних элементов списка.
- Лучше использовать стабильный идентификатор из данных, например `id`.
- Индекс массива можно использовать только если список не сортируется, не фильтруется и элементы не удаляются из середины.
- `key` не передается в компонент как обычный prop.
- Неправильные ключи могут приводить к багам с формами, фокусом и локальным состоянием.

---

#### Итог

`key` нужен не для отображения, а для корректного сопоставления элементов между рендерами. Стабильный `key` делает обновления списка предсказуемыми.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/react/react.md)
