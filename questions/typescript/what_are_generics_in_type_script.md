[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/typescript/typescript.md)
---

# Что такое Generics в TypeScript?

---

**Generics** — это механизм TypeScript, который позволяет создавать функции, типы, интерфейсы и классы, работающие с разными типами данных, сохраняя строгую типизацию.

Generics полезны, когда заранее неизвестно, с каким типом будет работать код, но важно сохранить связь между входными и выходными данными.

---

#### Пример

```typescript
function identity<T>(value: T): T {
  return value;
}

const numberValue = identity<number>(10);
const stringValue = identity<string>("hello");
```

`T` — это параметр типа. Он подставляется при использовании функции.

---

#### Зачем нужны Generics?

- Позволяют переиспользовать код для разных типов.
- Сохраняют информацию о типе вместо использования `any`.
- Помогают описывать коллекции, API-ответы, утилиты и компоненты.
- Делают код гибким, но типобезопасным.

---

#### Итог

Generics нужны, когда код должен быть универсальным, но не должен терять типы. На собеседовании важно показать разницу между `generic` и `any`: `any` отключает проверку, а generic сохраняет ее.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/typescript/typescript.md)

