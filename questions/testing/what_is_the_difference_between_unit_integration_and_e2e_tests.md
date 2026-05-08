[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/testing/testing.md)
---

# Чем отличаются unit, integration и e2e тесты?

---

Тесты отличаются уровнем проверки: от маленьких изолированных частей до полного пользовательского сценария.

---

#### Unit tests

Проверяют небольшую часть кода изолированно: функцию, хук, компонент или утилиту.

```js
expect(sum(2, 3)).toBe(5);
```

Обычно быстрые и простые в поддержке.

---

#### Integration tests

Проверяют, как несколько частей системы работают вместе: компонент с формой, API-слой с обработкой данных, несколько модулей в одном сценарии.

---

#### E2E tests

Проверяют приложение глазами пользователя: открыть страницу, заполнить форму, нажать кнопку, увидеть результат.

Часто пишутся на Playwright или Cypress.

---

#### Итог

Unit-тесты проверяют детали, integration-тесты проверяют связи, e2e-тесты проверяют реальные сценарии. На собеседовании важно показать понимание пирамиды тестирования и компромисса между скоростью, надежностью и покрытием.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/testing/testing.md)

