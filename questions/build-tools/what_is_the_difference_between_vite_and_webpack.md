[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/build-tools/build-tools.md)
---

# Чем Vite отличается от Webpack?

---

**Webpack** и **Vite** — это инструменты для сборки frontend-проектов, но они по-разному работают во время разработки.

---

#### Webpack

Webpack обычно собирает проект в bundle перед запуском dev server. Он очень гибкий и подходит для сложных конфигураций, но в больших проектах может запускаться медленнее.

---

#### Vite

Vite в режиме разработки использует нативные ES modules браузера. Он отдает файлы по запросу и поэтому обычно стартует быстрее.

Для production-сборки Vite использует Rollup.

---

#### Главное отличие

- Webpack делает акцент на универсальной bundling-конфигурации.
- Vite делает акцент на быстрой разработке и современном ESM-подходе.

---

#### Итог

Vite часто выбирают для новых проектов из-за скорости и простой настройки, а Webpack остается мощным инструментом для проектов со сложной инфраструктурой.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/build-tools/build-tools.md)

