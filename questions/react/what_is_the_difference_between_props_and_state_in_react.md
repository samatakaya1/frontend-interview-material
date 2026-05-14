[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/react/react.md)
---

# Чем отличаются `props` и `state` в React?

---

`props` — это данные, которые компонент получает от родителя. `state` — это внутренние данные компонента, которые могут меняться со временем и вызывать повторный рендер.

Главное отличие: `props` для компонента являются входными параметрами, а `state` принадлежит самому компоненту.

---

#### Пример

```jsx
function Counter({ step }) {
  const [count, setCount] = useState(0);

  return (
    <button onClick={() => setCount(count + step)}>
      {count}
    </button>
  );
}
```

`step` приходит через `props`, а `count` хранится в `state`.

---

#### Что важно знать?

- `props` передаются сверху вниз от родителя к дочернему компоненту.
- Компонент не должен изменять свои `props` напрямую.
- `state` изменяют через setter, например `setCount`.
- Изменение `props` или `state` может привести к повторному рендеру.
- Если несколько компонентов должны использовать одни данные, состояние часто поднимают к общему родителю.

---

#### Частая ошибка

Не стоит копировать `props` в `state` без причины. Это может привести к рассинхронизации данных.

---

#### Итог

`props` описывают вход компонента, `state` описывает его изменяемое внутреннее состояние. Это базовое различие помогает проектировать предсказуемые React-компоненты.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/react/react.md)
