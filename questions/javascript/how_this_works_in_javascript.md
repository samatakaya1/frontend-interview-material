[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/javascript/javascript.md)
---

# Как работает `this` в JavaScript?

---

`this` — это специальное значение, которое определяется не местом объявления функции, а способом ее вызова.

Главная идея: чтобы понять `this`, нужно смотреть на то, **как вызвали функцию**.

---

#### Пример

```js
const user = {
  name: "Anna",
  sayName() {
    console.log(this.name);
  }
};

user.sayName(); // "Anna"
```

Вызов идет через объект `user`, поэтому внутри `sayName` значение `this` указывает на `user`.

---

#### Основные правила

- При вызове `object.method()` значение `this` — объект перед точкой.
- При обычном вызове функции `this` зависит от strict mode.
- В стрелочных функциях нет собственного `this`.
- `call`, `apply` и `bind` позволяют явно задать `this`.
- В обработчиках событий `this` часто указывает на элемент, который вызвал обработчик.

---

#### Частая ошибка

```js
const sayName = user.sayName;

sayName(); // this уже не указывает на user
```

Метод был отделен от объекта, поэтому связь с `user` потерялась.

---

#### Итог

`this` в JavaScript зависит от способа вызова функции. На собеседовании важно отдельно упомянуть стрелочные функции: они берут `this` из внешней области видимости.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/javascript/javascript.md)

