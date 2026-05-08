[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/git/git.md)
---

# Чем отличается merge от rebase в Git?

---

`merge` и `rebase` используются, чтобы перенести изменения из одной ветки в другую, но делают это по-разному.

---

#### Merge

`merge` объединяет истории двух веток и создает merge commit.

```bash
git checkout feature
git merge main
```

Плюс: сохраняется реальная история ветвления. Минус: история может стать более шумной.

---

#### Rebase

`rebase` переносит коммиты текущей ветки поверх другой ветки.

```bash
git checkout feature
git rebase main
```

Плюс: история становится линейной. Минус: rebase переписывает историю коммитов.

---

#### Главное правило

Не стоит делать rebase публичной ветки, с которой уже работают другие разработчики, без договоренности с командой.

---

#### Итог

`merge` сохраняет историю как она была, а `rebase` делает историю линейной. На собеседовании важно объяснить не только команды, но и последствия для истории Git.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/git/git.md)

