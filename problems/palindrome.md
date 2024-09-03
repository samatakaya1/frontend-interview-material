# Задача "Палиндром"


> Палиндром — слово, предложение или последовательность символов,
> которая абсолютно одинаково читается как в привычном направлении, так
> и в обратном. К примеру, “Anna” — это палиндром, а “table” и “John” —
> нет.


## Постановка

Дана строка, нужно написать функцию, которая позволяет вернуть значение true, если строка является палиндромом, и false — если нет. При этом нужно учитывать пробелы и знаки препинания.

> palindrome('**racecar**') === true

> palindrome('**table**') === false

## Разбор решения

Основная идея здесь — перевернуть строку в обратном направлении. Если «реверсная» строка полностью идентична исходной, значит, мы получили палиндром и функция должна вернуть значение true. Если же нет — false.


## Код

```js
const palindrome = str => {
  str = str.toLowerCase()
  return str === str.split('').reverse().join('')
}
```