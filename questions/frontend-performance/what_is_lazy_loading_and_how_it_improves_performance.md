[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/frontend-performance/frontend-performance.md)
---

# Что такое lazy loading и как он улучшает производительность?

---

**Lazy loading** — это подход, при котором ресурс загружается не сразу, а только когда он действительно нужен пользователю.

Это помогает уменьшить начальную загрузку страницы и быстрее показать основной интерфейс.

---

#### Пример с изображением

Для изображений в HTML можно использовать атрибут `loading="lazy"`.

```html
<img src="/gallery/photo.jpg" alt="Фото товара" loading="lazy" />
```

Браузер отложит загрузку изображения, пока оно не окажется близко к видимой области.

---

#### Пример с кодом

В JavaScript можно загружать часть кода динамически.

```js
const Chart = lazy(() => import("./Chart"));
```

Так тяжелый компонент попадет в отдельный chunk и загрузится только при необходимости.

---

#### Что это улучшает?

- Уменьшается размер начального bundle.
- Быстрее загружается первый экран.
- Меньше сетевых запросов на старте.
- Пользователь раньше получает интерактивный интерфейс.

---

#### Итог

Lazy loading полезен для изображений, видео, тяжелых компонентов, страниц и редко используемых модулей. Главное — не откладывать критичный контент, который нужен пользователю сразу.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/frontend-performance/frontend-performance.md)
