[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/javascript/javascript.md)
---

# Чем отличаются `var`, `let` и `const`?

---

`var`, `let` и `const` используются для объявления переменных, но отличаются областью видимости, возможностью переобъявления и изменением значения.

---

#### `var`

`var` имеет функциональную область видимости и может быть переобъявлен.

```js
function example() {
  if (true) {
    var value = 10;
  }

  console.log(value); // 10
}
```

`var` поднимается наверх области видимости через hoisting, но значение до строки объявления будет `undefined`.

---

#### `let`

`let` имеет блочную область видимости и позволяет изменить значение переменной.

```js
let count = 1;
count = 2;
```

Повторно объявить `let` в той же области видимости нельзя.

---

#### `const`

`const` тоже имеет блочную область видимости, но не позволяет присвоить переменной новое значение.

```js
const user = { name: "Anna" };

user.name = "Kate"; // можно изменить объект
user = {}; // ошибка
```

Важно: `const` запрещает новое присваивание переменной, но не делает объект неизменяемым.

---

#### Итог

В современном JavaScript обычно используют `const` по умолчанию, `let` — когда значение нужно менять, а `var` стараются избегать из-за функциональной области видимости и более неожиданного поведения.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/javascript/javascript.md)
