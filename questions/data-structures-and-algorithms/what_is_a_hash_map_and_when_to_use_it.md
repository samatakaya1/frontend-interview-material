[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/data-structures-and-algorithms/data-structures-and-algorithms.md)
---

# Что такое hash map и когда её использовать?

---

Hash map — это структура данных для хранения пар ключ-значение с быстрым доступом по ключу.

В JavaScript для этого часто используют `Map` или обычный объект.

---

#### Пример

```js
const counts = new Map();

for (const value of values) {
  counts.set(value, (counts.get(value) ?? 0) + 1);
}
```

---

#### Что важно знать?

- Hash map удобна для подсчета частот.
- Она помогает быстро проверять, встречался ли элемент раньше.
- В среднем операции добавления, удаления и поиска выполняются за `O(1)`.
- `Map` позволяет использовать ключи любого типа.
- Обычный объект чаще используют для строковых ключей.

---

#### Итог

Hash map часто встречается в задачах на поиск, группировку, частоты и удаление дублей. Это один из базовых инструментов для оптимизации алгоритмов.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/data-structures-and-algorithms/data-structures-and-algorithms.md)
