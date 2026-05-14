[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/frontend-performance/frontend-performance.md)
---

# Что такое мемоизация (memoization) и когда её использовать во frontend?

---

**Мемоизация (memoization)** — это кеширование результата функции для уже встречавшихся входных данных.

Во frontend ее используют, чтобы не повторять дорогие вычисления и не создавать заново значения, которые могут провоцировать лишние рендеры.

---

#### Пример

```js
function memoize(fn) {
  const cache = new Map();

  return function memoized(value) {
    if (cache.has(value)) {
      return cache.get(value);
    }

    const result = fn(value);
    cache.set(value, result);
    return result;
  };
}
```

---

#### Что важно знать?

- Мемоизация полезна для дорогих чистых вычислений.
- Кеш должен строиться по входным данным.
- Для функций с побочными эффектами мемоизация обычно не подходит.
- В React похожую идею используют `useMemo`, `useCallback` и `React.memo`.
- Сам кеш тоже имеет стоимость по памяти.

---

#### Частая ошибка

Не стоит мемоизировать все подряд. Если вычисление дешевое, кеширование может усложнить код и не дать заметного выигрыша.

---

#### Итог

Мемоизация помогает ускорить повторные вычисления, но применять ее стоит там, где есть измеримая стоимость или реальная проблема с лишними рендерами.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/frontend-performance/frontend-performance.md)
