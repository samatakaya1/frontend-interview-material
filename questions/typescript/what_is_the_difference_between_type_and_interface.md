[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/typescript/typescript.md)
---

# Чем отличаются `type` и `interface`?

---

`type` и `interface` в TypeScript часто используют для описания формы объекта.

Во многих случаях они взаимозаменяемы, но между ними есть важные отличия.

---

#### `interface`

`interface` хорошо подходит для описания объектов и публичных контрактов.

```ts
interface User {
  id: number;
  name: string;
}
```

Интерфейсы можно расширять через `extends`.

```ts
interface Admin extends User {
  role: "admin";
}
```

Также интерфейсы поддерживают declaration merging: объявления с одним именем могут объединяться.

---

#### `type`

`type` может описывать не только объекты, но и union, intersection, tuple, primitive aliases и более сложные комбинации типов.

```ts
type Status = "idle" | "loading" | "success" | "error";

type UserWithRole = User & {
  role: string;
};
```

`type` нельзя переоткрыть повторным объявлением с тем же именем.

---

#### Что выбрать?

- Для объектов и публичных API часто выбирают `interface`.
- Для union, tuple и композиции типов чаще нужен `type`.
- Внутри проекта лучше следовать принятому стилю команды.

---

#### Итог

`interface` удобен для объектных контрактов и расширения, а `type` более универсален и подходит для сложных выражений типов. На практике важно не просто знать различия, а выбирать вариант, который лучше читается в конкретном коде.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/typescript/typescript.md)
