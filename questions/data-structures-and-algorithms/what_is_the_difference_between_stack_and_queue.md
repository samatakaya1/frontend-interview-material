[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/data-structures-and-algorithms/data-structures-and-algorithms.md)
---

# Чем отличаются stack и queue?

---

Stack и queue — это структуры данных для хранения элементов с разными правилами добавления и удаления.

---

#### Stack

Stack работает по принципу **LIFO**: last in, first out. Последний добавленный элемент выходит первым.

```js
const stack = [];

stack.push("first");
stack.push("second");

console.log(stack.pop()); // "second"
```

Примеры использования: история переходов, undo/redo, call stack, проверка скобок.

---

#### Queue

Queue работает по принципу **FIFO**: first in, first out. Первый добавленный элемент выходит первым.

```js
const queue = [];

queue.push("first");
queue.push("second");

console.log(queue.shift()); // "first"
```

Примеры использования: очередь задач, обработка сообщений, BFS, планирование операций.

---

#### Итог

Stack забирает элементы с конца, queue — с начала. На собеседовании важно назвать принципы LIFO и FIFO и привести пример, где каждая структура данных естественно подходит.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/data-structures-and-algorithms/data-structures-and-algorithms.md)
