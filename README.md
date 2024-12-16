# closure

1. Реализуйте функцию `seq(...args)` с использованием замыканий и чеининга,
которая может быть вызвана по цепочке с произвольным количеством функций, а
первый вызов со значением типа `Number` приведет к исполнению переданных ранее
функций и возвращаемый результат должен быть, как в приведенных примерах:

```js
seq(x => x + 7)
   (x => x * 2)(5)

// Результат: 17
```

```js
seq(x => x * 2)
   (x => x + 7)(5)

// Результат: 24
```

```js
seq(x => x + 1)
   (x => x * 2)
   (x => x / 3)
   (x => x - 4)(7)

// Результат: 3
```

2. Реализуйте функцию `array()` создающую функциональный объект, который
содержит массив в своем замыкании и обеспечивает следующий интерфейс доступа
к нему:
- Создание нового экземпляра `const a = array();`
- Получение элемента по индексу `a(i)`
- Добавление элемента в конец `a.push(value)`
- Удаление последнего элемента и получение его значения `a.pop()`

Пример использования:
```js
const arr = array();

arr.push('first');
arr.push('second');
arr.push('third');

console.log(arr(0)); // Выводит: first
console.log(arr(1)); // Выводит: second
console.log(arr(2)); // Выводит: third

console.log(arr.pop()); // Выводит: third
console.log(arr.pop()); // Выводит: second
console.log(arr.pop()); // Выводит: first

console.log(arr.pop()); // Выводит: undefined
```
