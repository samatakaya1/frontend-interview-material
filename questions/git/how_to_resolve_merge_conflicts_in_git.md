[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/git/git.md)
---

# Как разрешать merge conflicts в Git?

---

Merge conflict возникает, когда Git не может автоматически объединить изменения из разных веток. Обычно это происходит, если одни и те же строки были изменены по-разному.

Разрешение конфликта — это ручной выбор итогового состояния файла, после чего файл нужно добавить в индекс и завершить merge или rebase.

---

#### Пример

```txt
[текущая версия]
const title = "Main";

[версия из feature]
const title = "Feature";
```

Нужно убрать конфликтные маркеры и оставить корректный итоговый код.

---

#### Что важно знать?

- `git status` показывает файлы с конфликтами.
- Внутри файла Git оставляет маркеры `<<<<<<<`, `=======`, `>>>>>>>`.
- После ручного исправления нужно выполнить `git add <file>`.
- Для merge обычно затем выполняют `git commit`.
- Для rebase после `git add` выполняют `git rebase --continue`.

---

#### Частая ошибка

Нельзя оставлять конфликтные маркеры в коде. Перед завершением merge полезно найти их через поиск по `<<<<<<<`.

---

#### Итог

Разрешить конфликт значит осознанно собрать итоговую версию файла, проверить ее, добавить файл в индекс и завершить текущую Git-операцию.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/git/git.md)
