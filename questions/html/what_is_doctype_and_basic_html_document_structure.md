[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/html/html.md)
---

# Что такое `DOCTYPE` и базовая структура HTML-документа?

---

`DOCTYPE` сообщает браузеру, по какому стандарту нужно интерпретировать HTML-документ.

В современном HTML используется короткая запись `<!DOCTYPE html>`. Она включает стандартный режим рендеринга и помогает избежать старого quirks mode, в котором браузер имитирует поведение ранних версий.

---

#### Пример

```html
<!DOCTYPE html>
<html lang="ru">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Page title</title>
  </head>
  <body>
    <h1>Hello</h1>
  </body>
</html>
```

---

#### Что важно знать?

- `html` является корневым элементом страницы.
- Атрибут `lang` помогает браузерам, поисковым системам и ассистивным технологиям.
- В `head` находятся метаданные: кодировка, viewport, title, ссылки на стили и скрипты.
- В `body` находится видимый и интерактивный контент страницы.
- `meta charset="UTF-8"` лучше указывать в начале `head`, чтобы браузер корректно прочитал текст.

---

#### Итог

Базовая структура HTML-документа задает правила чтения страницы, язык, метаданные и место для контента. На интервью важно упомянуть `DOCTYPE`, `html`, `head`, `body`, `charset` и `viewport`.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/html/html.md)
