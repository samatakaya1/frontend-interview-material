[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/typescript/typescript.md)
---

# Что такое utility types в TypeScript?

---

**Utility types** — это встроенные типы TypeScript, которые помогают создавать новые типы на основе существующих.

Они позволяют не дублировать описания объектов и точнее выражать намерение в типах.

---

#### Пример

```ts
type User = {
  id: string;
  name: string;
  email: string;
};

type UserPreview = Pick<User, "id" | "name">;
type UserPatch = Partial<User>;
```

---

#### Что важно знать?

- `Partial<T>` делает все поля необязательными.
- `Required<T>` делает все поля обязательными.
- `Pick<T, K>` выбирает часть полей.
- `Omit<T, K>` исключает часть полей.
- `Readonly<T>` запрещает менять поля.
- `Record<K, T>` описывает объект с ключами `K` и значениями `T`.

---

#### Частая ошибка

Не стоит заменять utility types ручным копированием похожих типов. Это увеличивает риск расхождения, когда исходная модель изменится.

---

#### Итог

Utility types помогают переиспользовать типы и описывать производные структуры данных компактно и безопасно.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/typescript/typescript.md)
