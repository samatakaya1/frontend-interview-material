[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список тем](https://github.com/samatakaya1/Interview-material/blob/main/questions/questions.md) [/ Список вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/git/git.md)
---

# Что такое `git stash` и когда его использовать?

---

`git stash` временно сохраняет незакоммиченные изменения и очищает рабочее дерево.

Это удобно, когда нужно быстро переключиться на другую ветку, подтянуть изменения или проверить задачу без текущего незавершенного кода.

---

#### Пример

```bash
git stash push -m "WIP navbar"
git pull --rebase
git stash pop
```

---

#### Что важно знать?

- `git stash push` сохраняет изменения в специальное хранилище.
- `git stash list` показывает сохраненные stash-записи.
- `git stash pop` применяет последний stash и удаляет его из списка.
- `git stash apply` применяет stash, но оставляет его в списке.
- При применении stash могут возникнуть конфликты, как при merge.

---

#### Итог

`git stash` — это временная полка для незавершенных изменений. Его стоит использовать для короткого переключения контекста, а не как замену нормальным коммитам.

---
[<- К списку вопросов](https://github.com/samatakaya1/Interview-material/blob/main/questions/git/git.md)
