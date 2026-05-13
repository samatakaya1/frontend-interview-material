[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список задач](https://github.com/samatakaya1/Interview-material/blob/main/problems/problems.md)
---

# Задача "Реализовать функцию groupBy"

## Постановка 📖

Необходимо написать функцию `groupBy(items, getKey)`, которая принимает массив элементов и функцию для получения ключа группы.

Функция должна вернуть объект, где каждый ключ — это имя группы, а значение — массив элементов, попавших в эту группу.

---

## Требования ⚠️

- Первый аргумент должен быть массивом.
- Второй аргумент должен быть функцией.
- Функция `getKey` должна вызываться для каждого элемента массива.
- Элементы с одинаковым ключом должны попадать в один массив.
- Порядок элементов внутри каждой группы должен сохраняться.

---

## Пример

```js
const users = [
  { name: "Ann", role: "admin" },
  { name: "Bob", role: "user" },
  { name: "Kate", role: "admin" },
];

console.log(groupBy(users, (user) => user.role));

// {
//   admin: [
//     { name: "Ann", role: "admin" },
//     { name: "Kate", role: "admin" },
//   ],
//   user: [
//     { name: "Bob", role: "user" },
//   ],
// }
```

---

## Решение

```js
function groupBy(items, getKey) {
  if (!Array.isArray(items)) {
    throw new TypeError("items must be an array");
  }

  if (typeof getKey !== "function") {
    throw new TypeError("getKey must be a function");
  }

  return items.reduce((groups, item, index) => {
    const key = String(getKey(item, index, items));

    if (!Object.prototype.hasOwnProperty.call(groups, key)) {
      groups[key] = [];
    }

    groups[key].push(item);

    return groups;
  }, {});
}
```

---

## Разбор решения

Главная идея — пройти по массиву один раз и постепенно собрать объект с группами.

На каждой итерации:

1. Получаем ключ группы через `getKey`.
2. Приводим ключ к строке, потому что ключи обычного объекта являются строками или символами.
3. Если такой группы еще нет, создаем для нее пустой массив.
4. Добавляем текущий элемент в нужную группу.

Проверка через `hasOwnProperty` нужна, чтобы отличать собственные ключи объекта от свойств из прототипа.

---

## Оценка сложности

#### Время выполнения:

Алгоритм проходит по массиву один раз, поэтому сложность — **O(n)**.

#### Пространственная сложность:

Дополнительная память зависит от количества элементов в итоговых группах, поэтому сложность — **O(n)**.

---

## Тесты

```js
console.log(groupBy([1, 2, 3, 4], (number) => (number % 2 === 0 ? "even" : "odd")));
// { odd: [1, 3], even: [2, 4] }

console.log(groupBy(["one", "two", "six"], (word) => word.length));
// { 3: ["one", "two", "six"] }

console.log(groupBy([], (item) => item));
// {}
```

---
[<- К списку задач](https://github.com/samatakaya1/Interview-material/blob/main/problems/problems.md)
