[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/data-structures-and-algorithms/data-structures-and-algorithms.md)
---

# Что такое Big O notation?

---

**Big O notation** — это способ описать, как растет время выполнения или потребление памяти алгоритма при увеличении размера входных данных.

Big O не показывает точное время в миллисекундах. Он показывает характер роста.

---

#### Примеры сложности

- `O(1)` — постоянное время.
- `O(log n)` — логарифмический рост.
- `O(n)` — линейный рост.
- `O(n log n)` — часто встречается в эффективных сортировках.
- `O(n²)` — квадратичный рост, например вложенные циклы.

---

#### Пример

```js
function findItem(items, target) {
  for (const item of items) {
    if (item === target) return true;
  }

  return false;
}
```

В худшем случае функция проверит все элементы, поэтому сложность — `O(n)`.

---

#### Итог

Big O помогает сравнивать алгоритмы и понимать, как решение будет вести себя на больших данных. На собеседовании важно уметь оценивать не только время, но и память.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/data-structures-and-algorithms/data-structures-and-algorithms.md)

