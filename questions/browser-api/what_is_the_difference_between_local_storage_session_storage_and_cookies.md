[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/browser-api/browser-api.md)
---

# Чем отличаются `localStorage`, `sessionStorage` и cookies?

---

`localStorage`, `sessionStorage` и cookies позволяют хранить данные в браузере, но отличаются сроком жизни, размером и тем, отправляются ли данные на сервер.

---

#### `localStorage`

Хранит данные без срока истечения, пока пользователь или приложение их не удалит.

```js
localStorage.setItem("theme", "dark");
const theme = localStorage.getItem("theme");
```

Подходит для настроек интерфейса, темы, небольших пользовательских предпочтений.

---

#### `sessionStorage`

Хранит данные только в рамках одной вкладки браузера.

```js
sessionStorage.setItem("draft", "text");
```

После закрытия вкладки данные удаляются. Подходит для временного состояния формы или шага сценария.

---

#### Cookies

Cookies могут иметь срок жизни и автоматически отправляются браузером на сервер вместе с HTTP-запросами к подходящему домену.

```http
Set-Cookie: sessionId=abc123; HttpOnly; Secure; SameSite=Lax
```

Их часто используют для сессий, авторизации и серверных сценариев.

---

#### Главное отличие

- `localStorage` живет долго и доступен JavaScript.
- `sessionStorage` живет до закрытия вкладки.
- Cookies могут отправляться на сервер автоматически.
- Для чувствительных токенов важны флаги `HttpOnly`, `Secure` и `SameSite`.

---

#### Итог

Для локальных настроек обычно подходит `localStorage`, для временных данных вкладки — `sessionStorage`, а для серверной сессии — cookies с правильными security-флагами.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/browser-api/browser-api.md)
