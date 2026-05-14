[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список задач](https://github.com/samatakaya1/Interview-material/blob/main/problems/problems.md)
---

# Задача "Реализовать функцию memoize"

## Постановка 📖

Необходимо написать функцию `memoize(fn)`, которая возвращает новую функцию. Эта новая функция должна кешировать результат вызова `fn` для уже встречавшихся аргументов.

Если обертку вызывают повторно с теми же аргументами, нужно вернуть значение из кеша без повторного вызова исходной функции.

---

## Требования ⚠️

- Нужно сохранить корректный контекст `this`.
- Функция должна работать с любым количеством аргументов.
- Для одинаковых аргументов и одинакового контекста `this` исходная функция должна вызываться только один раз.
- В базовой версии считаем, что аргументы можно безопасно сериализовать через `JSON.stringify(args)`.
- Решение должно быть понятно для базового frontend-собеседования.

---

## Пример

```js
function slowSum(a, b) {
  console.log("calculate");
  return a + b;
}

const memoizedSum = memoize(slowSum);

console.log(memoizedSum(2, 3)); // logs "calculate", then 5
console.log(memoizedSum(2, 3)); // 5
```

---

## Решение

```js
function memoize(fn) {
  const objectContextCache = new WeakMap();
  const primitiveContextCache = new Map();

  function getContextCache(context) {
    const isObjectContext =
      context !== null &&
      (typeof context === "object" || typeof context === "function");

    const rootCache = isObjectContext ? objectContextCache : primitiveContextCache;

    if (!rootCache.has(context)) {
      rootCache.set(context, new Map());
    }

    return rootCache.get(context);
  }

  return function memoized(...args) {
    const cache = getContextCache(this);
    const key = JSON.stringify(args);

    if (cache.has(key)) {
      return cache.get(key);
    }

    const result = fn.apply(this, args);
    cache.set(key, result);

    return result;
  };
}
```

---

## Разбор решения

Главная идея — хранить кеш в замыкании и разделять его по контексту вызова.

Для объектного `this` используется `WeakMap`, чтобы кеш не удерживал объект в памяти дольше необходимого. Для примитивного `this` используется обычный `Map`.

При каждом вызове:

1. Для текущего `this` выбирается отдельный кеш.
2. Аргументы превращаются в строковый ключ.
3. Если ключ уже есть в `cache`, возвращается сохраненный результат.
4. Если ключа нет, вызывается исходная функция.
5. Результат сохраняется в кеш и возвращается.

Метод `fn.apply(this, args)` нужен, чтобы сохранить контекст и передать все аргументы исходной функции.

Ограничение этой учебной версии — ключ через `JSON.stringify(args)` подходит только для простых сериализуемых аргументов. Для функций, символов, циклических объектов или случаев, где важна identity объектов, нужна более надежная стратегия ключей.

---

## Где используется memoize?

- Кеширование дорогих чистых вычислений.
- Повторное использование результата форматирования данных.
- Оптимизация вычисляемых селекторов.
- Снижение количества одинаковых расчетов в UI.

---

## Оценка сложности

#### Время выполнения:

Для повторного вызова с уже известными аргументами доступ к кешу выполняется в среднем за **O(1)**. Создание ключа через `JSON.stringify(args)` зависит от размера аргументов.

#### Пространственная сложность:

Используется **O(n)** дополнительной памяти, где `n` — количество уникальных наборов аргументов в кеше.

---

## Тесты

```js
let calls = 0;

const memoizedDouble = memoize((value) => {
  calls += 1;
  return value * 2;
});

console.log(memoizedDouble(4)); // 8
console.log(memoizedDouble(4)); // 8
console.log(calls); // 1

let contextCalls = 0;

const multiplyByFactor = memoize(function (value) {
  contextCalls += 1;
  return this.factor * value;
});

const doubleContext = { factor: 2 };
const tripleContext = { factor: 3 };

console.log(multiplyByFactor.call(doubleContext, 5)); // 10
console.log(multiplyByFactor.call(doubleContext, 5)); // 10
console.log(multiplyByFactor.call(tripleContext, 5)); // 15
console.log(contextCalls); // 2
```

---
[<- К списку задач](https://github.com/samatakaya1/Interview-material/blob/main/problems/problems.md)
