[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/testing/testing.md)
---

# Что такое test pyramid во frontend-тестировании?

---

Test pyramid — это модель распределения тестов по уровням: много быстрых unit-тестов, меньше integration-тестов и немного дорогих e2e-тестов.

Идея в том, чтобы получать быструю обратную связь и не делать весь контроль качества зависимым от медленных сценариев в браузере.

---

#### Пример

```txt
E2E tests         few
Integration tests some
Unit tests        many
```

---

#### Что важно знать?

- Unit-тесты проверяют маленькие функции, компоненты или модули изолированно.
- Integration-тесты проверяют, как несколько частей работают вместе.
- E2E-тесты проверяют пользовательский сценарий целиком в окружении, похожем на реальное.
- Чем выше уровень теста, тем он обычно медленнее и хрупче.
- Хорошая стратегия сочетает уровни, а не заменяет один уровень другим.

---

#### Итог

Test pyramid помогает выбрать разумный баланс тестов: основную массу держать быстрой и дешевой, а критические пользовательские сценарии покрывать e2e.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/testing/testing.md)
