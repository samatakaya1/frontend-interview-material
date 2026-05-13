[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/react/react.md)
---

# Чем отличаются controlled и uncontrolled components?

---

В React controlled и uncontrolled components чаще всего обсуждают на примере форм.

Главное отличие в том, где хранится текущее значение поля: в React state или внутри DOM-элемента.

---

#### Controlled component

Controlled component управляется через React state.

```jsx
function SearchInput() {
  const [value, setValue] = useState("");

  return (
    <input
      value={value}
      onChange={(event) => setValue(event.target.value)}
    />
  );
}
```

React знает актуальное значение поля на каждом рендере. Это удобно для валидации, форматирования, зависимых полей и условной логики.

---

#### Uncontrolled component

Uncontrolled component хранит значение внутри DOM. React получает его через `ref` только когда это нужно.

```jsx
function SearchInput() {
  const inputRef = useRef(null);

  function handleSubmit() {
    console.log(inputRef.current.value);
  }

  return <input ref={inputRef} />;
}
```

Такой подход может быть проще для небольших форм или интеграции с внешними библиотеками.

---

#### Итог

Controlled components дают больше контроля и лучше подходят для сложных форм. Uncontrolled components проще, когда значение не нужно постоянно синхронизировать с React state. На собеседовании важно сказать, что оба подхода валидны, но controlled чаще используют в управляемых интерфейсах.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/react/react.md)
