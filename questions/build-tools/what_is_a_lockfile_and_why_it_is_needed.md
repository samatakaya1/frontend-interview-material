[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/build-tools/build-tools.md)
---

# Что такое lockfile и зачем он нужен?

---

Lockfile фиксирует точные версии установленных зависимостей и их вложенных зависимостей.

Примеры lockfile: `package-lock.json`, `yarn.lock`, `pnpm-lock.yaml`.

---

#### Пример

```bash
npm install
git add package.json package-lock.json
```

---

#### Что важно знать?

- `package.json` описывает диапазоны версий зависимостей.
- Lockfile фиксирует конкретное дерево установленных пакетов.
- Благодаря lockfile команда и CI получают одинаковые версии зависимостей.
- Lockfile нужно коммитить в репозиторий приложения.
- Не стоит вручную редактировать lockfile без необходимости — его обновляет package manager.

---

#### Итог

Lockfile делает установку зависимостей воспроизводимой. Он снижает риск ситуации, когда у разных разработчиков один и тот же проект работает по-разному.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/build-tools/build-tools.md)
