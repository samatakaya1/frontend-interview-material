[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/build-tools/build-tools.md)
---

# Что такое `package.json` и зачем нужны `dependencies` и `devDependencies`?

---

`package.json` — это главный конфигурационный файл JavaScript-проекта. В нем описывают зависимости, скрипты, метаданные проекта и настройки инструментов.

---

#### Что обычно есть в `package.json`?

```json
{
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "test": "vitest"
  },
  "dependencies": {
    "react": "^18.2.0"
  },
  "devDependencies": {
    "vite": "^5.0.0",
    "typescript": "^5.0.0"
  }
}
```

Скрипты позволяют запускать команды через `npm run`, `pnpm` или `yarn`.

---

#### `dependencies`

`dependencies` — это пакеты, которые нужны приложению для работы.

Например: React, роутер, библиотека для запросов, runtime-зависимости.

---

#### `devDependencies`

`devDependencies` — это пакеты, которые нужны только во время разработки, сборки или тестирования.

Например: TypeScript, Vite, ESLint, Prettier, Vitest.

---

#### Итог

`package.json` описывает, как проект устанавливается, запускается, собирается и тестируется. `dependencies` нужны приложению в runtime, а `devDependencies` нужны разработчику и инструментам вокруг проекта.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/build-tools/build-tools.md)
