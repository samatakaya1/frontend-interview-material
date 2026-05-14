[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/data-structures-and-algorithms/data-structures-and-algorithms.md)
---

# Что такое рекурсия и когда её использовать?

---

**Рекурсия** — это подход, при котором функция вызывает саму себя для решения меньшей версии той же задачи.

Чтобы рекурсия завершилась, у нее должен быть базовый случай и шаг, который приближает задачу к этому базовому случаю.

---

#### Пример

```js
function factorial(n) {
  if (n <= 1) {
    return 1;
  }

  return n * factorial(n - 1);
}
```

---

#### Что важно знать?

- Базовый случай останавливает рекурсивные вызовы.
- Рекурсивный шаг уменьшает задачу.
- Каждый вызов занимает место в call stack.
- Без базового случая можно получить stack overflow.
- Рекурсия удобна для деревьев, вложенных структур и задач, которые естественно делятся на подзадачи.

---

#### Частая ошибка

Рекурсия не всегда лучше цикла. Для простого линейного прохода цикл может быть понятнее и безопаснее по памяти.

---

#### Итог

Рекурсия хорошо подходит для вложенных и древовидных структур, но требует аккуратного базового случая и понимания расхода памяти на стек вызовов.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/data-structures-and-algorithms/data-structures-and-algorithms.md)
