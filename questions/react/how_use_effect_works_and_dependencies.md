[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/react/react.md)
---

# Как работает `useEffect` и массив зависимостей?

---

`useEffect` — это React Hook для выполнения побочных эффектов после рендера компонента.

Побочные эффекты — это действия, которые выходят за рамки обычного вычисления JSX: запросы к API, подписки, таймеры, работа с `localStorage` или ручное изменение DOM.

---

#### Пример

```jsx
useEffect(() => {
  document.title = `Count: ${count}`;
}, [count]);
```

Эффект выполнится после первого рендера и затем каждый раз, когда изменится `count`.

---

#### Как работает массив зависимостей?

- Без массива зависимостей эффект выполняется после каждого рендера.
- `[]` означает выполнить эффект только после первого рендера.
- `[value]` означает выполнить эффект при первом рендере и при изменении `value`.
- Функция, возвращенная из эффекта, используется для очистки.

---

#### Пример очистки

```jsx
useEffect(() => {
  const id = setInterval(() => {
    console.log("tick");
  }, 1000);

  return () => clearInterval(id);
}, []);
```

---

#### Итог

`useEffect` связывает React-компонент с внешним миром. На собеседовании важно объяснить зависимости и cleanup, потому что ошибки в них часто приводят к лишним запросам, утечкам памяти и устаревшим данным.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/react/react.md)

