[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/javascript/javascript.md)
---

# Чем отличаются `==` и `===` в JavaScript?

---

`==` сравнивает значения с приведением типов, а `===` сравнивает значения без неявного приведения типов.

Поэтому `===` обычно безопаснее и предсказуемее.

---

#### Пример

```js
console.log(0 == false); // true
console.log(0 === false); // false

console.log("5" == 5); // true
console.log("5" === 5); // false
```

---

#### Что важно знать?

- `==` перед сравнением может преобразовать строку в число, boolean в число или выполнить другие неочевидные преобразования.
- `===` возвращает `true` только если совпадают и значение, и тип.
- На собеседовании важно упомянуть, что `null == undefined` возвращает `true`, но `null === undefined` возвращает `false`.
- В обычном коде чаще используют `===`, чтобы избежать ошибок из-за coercion.

---

#### Итог

`===` — строгая проверка без приведения типов. `==` может быть полезен в редких случаях, но требует хорошего понимания правил coercion.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/javascript/javascript.md)
