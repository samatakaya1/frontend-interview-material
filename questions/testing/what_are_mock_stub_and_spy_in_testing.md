[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/testing/testing.md)
---

# Что такое mock, stub и spy в тестировании?

---

Mock, stub и spy — это тестовые двойники. Они помогают изолировать код от внешних зависимостей: API, таймеров, хранилища, сложных модулей или побочных эффектов.

---

#### Stub

Stub подменяет зависимость и возвращает заранее заданный результат.

```js
const getUser = () => ({ id: 1, name: "Anna" });
```

Он нужен, когда тесту важно получить стабильные данные, а не проверять саму зависимость.

---

#### Spy

Spy следит за вызовами функции: была ли она вызвана, сколько раз и с какими аргументами.

```js
const onSubmit = vi.fn();

expect(onSubmit).toHaveBeenCalledWith(formData);
```

Spy полезен, когда нужно проверить взаимодействие.

---

#### Mock

Mock обычно не только подменяет поведение, но и позволяет проверять ожидания по вызовам.

```js
const api = {
  save: vi.fn().mockResolvedValue({ ok: true }),
};
```

В разных инструментах слова mock, stub и spy могут частично пересекаться, но смысл остается похожим.

---

#### Итог

Stub дает заранее известный ответ, spy наблюдает за вызовами, mock подменяет зависимость и часто проверяет взаимодействие. На собеседовании важно объяснить, что тестовые двойники нужны не ради самих себя, а чтобы сделать тесты стабильными, быстрыми и сфокусированными.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/testing/testing.md)
