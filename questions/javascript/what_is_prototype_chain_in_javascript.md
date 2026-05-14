[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/javascript/javascript.md)
---

# Что такое prototype chain в JavaScript?

---

**Prototype chain** — это механизм, по которому JavaScript ищет свойства и методы объекта не только в самом объекте, но и в его прототипах.

Если свойства нет в объекте, движок поднимается выше по цепочке прототипов. Поиск продолжается до `null`.

---

#### Пример

```js
const user = {
  name: "Alex",
};

console.log(user.toString()); // метод найден в Object.prototype
```

У объекта `user` нет собственного метода `toString`, но он доступен через цепочку прототипов.

---

#### Что важно знать?

- У каждого обычного объекта есть внутренний прототип.
- Прототип можно получить через `Object.getPrototypeOf(obj)`.
- Методы массивов находятся в `Array.prototype`, методы обычных объектов — в `Object.prototype`.
- Свойство считается собственным, если оно лежит прямо в объекте, а не найдено через прототип.
- Проверять собственные свойства удобно через `Object.hasOwn(obj, key)`.

---

#### Частая ошибка

Не стоит путать `prototype` у функции-конструктора и внутренний прототип конкретного объекта. Свойство `prototype` используется при создании объектов через `new`.

---

#### Итог

Prototype chain объясняет наследование в JavaScript и то, почему объектам доступны методы, которые не объявлены прямо в них.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/javascript/javascript.md)
