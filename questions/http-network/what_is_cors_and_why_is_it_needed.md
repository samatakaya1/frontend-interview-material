[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/http-network/http-network.md)
---

# Что такое CORS и зачем он нужен?

---

**CORS (Cross-Origin Resource Sharing)** — это механизм браузера, который контролирует, может ли веб-страница отправлять запросы к ресурсу на другом origin.

Origin состоит из протокола, домена и порта. Например, `https://example.com` и `http://example.com` — разные origin.

---

#### Зачем нужен CORS?

Браузер защищает пользователя от небезопасных запросов между разными сайтами. Сервер должен явно разрешить frontend-приложению доступ к ресурсу с помощью специальных HTTP headers.

---

#### Пример заголовка

```http
Access-Control-Allow-Origin: https://example.com
```

Этот заголовок сообщает браузеру, что указанному origin разрешено читать ответ.

---

#### Важно

- CORS проверяется браузером, а не самим JavaScript.
- Ошибка CORS обычно исправляется на сервере.
- Для некоторых запросов браузер сначала отправляет preflight-запрос `OPTIONS`.

---

#### Итог

CORS нужен для безопасного обмена данными между разными origin. На собеседовании важно сказать, что это не ошибка `fetch`, а политика безопасности браузера и сервера.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/http-network/http-network.md)

