[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/typescript/typescript.md)
---

# Что такое narrowing в TypeScript?

---

Narrowing — это сужение типа переменной после проверки в коде.

TypeScript анализирует условия и понимает, какой более конкретный тип доступен внутри определенной ветки.

---

#### Пример

```ts
function formatValue(value: string | number) {
  if (typeof value === "number") {
    return value.toFixed(2);
  }

  return value.trim();
}
```

---

#### Что важно знать?

- `typeof` помогает сужать примитивы: `string`, `number`, `boolean`, `undefined`.
- `instanceof` подходит для классов и объектов, созданных через конструктор.
- Проверка свойства через `in` помогает различать объекты в union type.
- Пользовательские type guards позволяют вынести проверку в отдельную функцию.
- После сужения TypeScript разрешает методы и свойства конкретного типа.

---

#### Итог

Narrowing делает работу с union types безопасной: сначала проверяем тип, потом используем возможности конкретного значения.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/typescript/typescript.md)
