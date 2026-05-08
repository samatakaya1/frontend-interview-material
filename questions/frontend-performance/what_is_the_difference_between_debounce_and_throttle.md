[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/frontend-performance/frontend-performance.md)
---

# Чем отличаются debounce и throttle?

---

`debounce` и `throttle` ограничивают частоту вызова функции. Они часто используются для оптимизации обработчиков событий.

---

#### Debounce

`debounce` откладывает выполнение функции до тех пор, пока события не перестанут происходить.

Подходит для поиска по вводу:

```js
// запрос отправляется только после паузы в наборе текста
```

---

#### Throttle

`throttle` разрешает выполнять функцию не чаще одного раза за указанный интервал.

Подходит для scroll или resize:

```js
// обработчик scroll выполняется максимум раз в 200 мс
```

---

#### Главное отличие

- `debounce` ждет паузу.
- `throttle` выполняет функцию регулярно, но с ограничением по частоте.

---

#### Итог

`debounce` полезен, когда нужен финальный результат после серии событий. `throttle` полезен, когда нужно регулярно реагировать на поток событий без перегрузки браузера.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/frontend-performance/frontend-performance.md)

