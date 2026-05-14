[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/build-tools/build-tools.md)
---

# Что такое Babel и зачем нужна транспиляция (transpilation)?

---

**Babel** — это инструмент, который преобразует современный JavaScript в код, совместимый с выбранными браузерами или окружениями.

Такое преобразование часто называют транспиляцией (transpilation): код остается JavaScript, но меняется синтаксис или добавляются вспомогательные функции.

---

#### Пример

```js
const title = user?.profile?.title ?? "Untitled";
```

Babel может преобразовать такой код, если целевые браузеры не поддерживают нужный синтаксис.

---

#### Что важно знать?

- Babel работает через плагины и пресеты.
- `@babel/preset-env` подбирает преобразования под список целевых браузеров.
- Babel преобразует синтаксис, но не всегда добавляет API времени выполнения.
- Для новых API могут понадобиться полифилы (polyfills).
- В современных сборщиках часть задач может выполнять esbuild или SWC.

---

#### Частая ошибка

Транспиляция и полифил — не одно и то же. Транспиляция меняет синтаксис, а полифил добавляет отсутствующую функциональность во время выполнения.

---

#### Итог

Babel помогает использовать современный JavaScript и при этом поддерживать нужные окружения. На интервью важно различать синтаксические преобразования и полифилы.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/build-tools/build-tools.md)
