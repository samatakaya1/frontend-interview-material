[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список задач](https://github.com/samatakaya1/Interview-material/blob/main/problems/problems.md)
---
# Задача "Реализовать функцию map без использования встроенных методов прототипа массива"

### Требование

Реализовать функцию `map` без использования встроенных методов прототипа массива, таких как `Array.prototype.map`. Функция должна быть написана на TypeScript и поддерживать строгую типизацию. Основное требование — корректно обрабатывать элементы массива, включая разреженные массивы, и предоставлять удобный интерфейс для работы с массивами любых типов.

---

### Условие

Напишите функцию `map`, которая принимает два аргумента:
1. Массив произвольных элементов типа `T[]`.
2. Функцию обратного вызова `(value: T, index: number, array: T[]) => U`, которая преобразует каждый элемент массива.

Функция должна возвращать новый массив типа `U[]`, где каждый элемент является результатом применения функции обратного вызова к соответствующему элементу исходного массива.

**Особенности:**
- Поддержка строгой типизации в TypeScript.
- Корректная обработка разреженных массивов (например, `[1, , 3]`).
- Генерация ошибок, если входные данные некорректны:
    - Первый аргумент не является массивом.
    - Второй аргумент не является функцией.

Пример:
```typescript
map([1, 2, 3], x => x * 2); // Результат: [2, 4, 6]
```

---

### Решение

```typescript
function map<T, U>(array: T[], callback: (value: T, index: number, array: T[]) => U): U[] {
  if (!Array.isArray(array)) {
    throw new TypeError('Первый аргумент должен быть массивом');
  }
  if (typeof callback !== 'function') {
    throw new TypeError('Второй аргумент должен быть функцией');
  }

  const result: U[] = [];
  for (let i = 0; i < array.length; i++) {
    // Учитываем разреженные массивы
    if (i in array) {
      result.push(callback(array[i], i, array));
    }
  }
  return result;
}

// Примеры использования:

// Пример 1: Умножение чисел на 2
const numbers = [1, 2, 3, 4];
const doubled = map(numbers, (num) => num * 2);
console.log(doubled); // [2, 4, 6, 8]

// Пример 2: Преобразование строк в их длины
const words = ['hello', 'world'];
const lengths = map(words, (word) => word.length);
console.log(lengths); // [5, 5]

// Пример 3: Обработка разреженного массива
const sparseArray = [1, , 3]; // Второй элемент "пустой"
const processed = map(sparseArray, (num, index) => num || index);
console.log(processed); // [1, 1, 3]
```

---
[<- К списку задач](https://github.com/samatakaya1/Interview-material/blob/main/problems/problems.md)
