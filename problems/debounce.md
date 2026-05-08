[/ Меню](https://github.com/samatakaya1/Interview-material/blob/main/README.md)   [/ Список задач](https://github.com/samatakaya1/Interview-material/blob/main/problems/problems.md)
---

# Задача "Реализовать функцию debounce"

## Постановка 📖

Необходимо написать функцию `debounce(fn, delay)`, которая возвращает новую функцию. Эта новая функция откладывает вызов `fn` до тех пор, пока после последнего вызова не пройдет `delay` миллисекунд.

Если возвращенная функция вызывается несколько раз подряд, предыдущий таймер должен сбрасываться, а исходная функция должна выполниться только один раз — после последнего вызова.

---

## Требования ⚠️

- Нельзя вызывать `fn` сразу при каждом вызове обертки.
- Нужно использовать `setTimeout` и `clearTimeout`.
- Нужно передавать в `fn` последние аргументы.
- Нужно сохранить корректный контекст `this`.
- Функция должна работать с любым количеством аргументов.

---

## Пример

```js
function search(value) {
  console.log("Search:", value);
}

const debouncedSearch = debounce(search, 500);

debouncedSearch("r");
debouncedSearch("re");
debouncedSearch("rea");
debouncedSearch("react");

// Через 500 мс выполнится только:
// Search: react
```

---

## Решение

```js
function debounce(fn, delay) {
  let timerId;

  return function debounced(...args) {
    clearTimeout(timerId);

    timerId = setTimeout(() => {
      fn.apply(this, args);
    }, delay);
  };
}
```

---

## Разбор решения

Главная идея — хранить идентификатор таймера `timerId` в замыкании.

При каждом вызове `debounced`:

1. Предыдущий таймер отменяется через `clearTimeout(timerId)`.
2. Создается новый таймер через `setTimeout`.
3. Если новых вызовов не было в течение `delay` миллисекунд, вызывается исходная функция `fn`.

Метод `fn.apply(this, args)` нужен, чтобы передать исходной функции:

- актуальный контекст `this`;
- последние аргументы, с которыми была вызвана обертка.

---

## Где используется debounce?

- Поиск при вводе текста.
- Автосохранение формы.
- Валидация поля после окончания ввода.
- Обработка событий `resize`.
- Отправка аналитики после серии пользовательских действий.

---

## Оценка сложности

#### Время выполнения:

Один вызов обертки выполняется за **O(1)**, потому что мы только очищаем старый таймер и создаем новый.

#### Пространственная сложность:

Используется **O(1)** дополнительной памяти для хранения `timerId`.

---

## Тесты

```js
const log = debounce((value) => {
  console.log(value);
}, 300);

log("first");
log("second");
log("third");

// Через 300 мс будет выведено только:
// third
```

---
[<- К списку задач](https://github.com/samatakaya1/Interview-material/blob/main/problems/problems.md)

