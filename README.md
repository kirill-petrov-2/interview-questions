# Вопросы с собесов

<a id="top"></a>

| №   | Вопрос                                                                   |
| --- | ------------------------------------------------------------------------ |
| 1   | [Что такое Singleton](#1)                                                |
| 2   | [Классы и строки являются ссылочным типом?](#2)                          |
| 3   | [Демонизация Node.js](#3)                                                |
| 4   | [Чем отличаются коллекции `Set` и `Map`](#4)                             |
| 5   | [Oбласти видимости у `let` и `const`](#5)                                |
| 6   | [Контекст стрелочной функции](#6)                                        |
| 7   | [Особенности Node.js](#7)                                                |
| 8   | [Что делает super у класса?](#8)                                         |
| 9   | [Плюсы Реакта](#9)                                                       |
| 10  | [Что такое NaN](#10)                                                     |
| 11  | [Что такое AJAX?](#11)                                                   |
| 12  | [ХУКИ](#12)                                                              |
| 13  | [Жизненный цикл компонента](#13)                                         |
| 14  | [CORS](#14)                                                              |
| 15  | [EVENT LOOP](#15)                                                        |
| 16  | [Для чего используется `new`?](#16)                                      |
| 17  | [Что такое запоминание или мемоизация](#17)                              |
| 18  | [В чем разница между обычной функцией и функциональным выражением?](#18) |
| 19  | [Какие приемы работы с асинхронным кодом в JS Вы знаете?](#19)           |
| 20  | [Как проверить, является ли значение массивом?](#20)                     |
| 21  | [SPREAD и REST операторы](#21)                                           |
| 22  | [Что такое промисы (Promises)?](#22)                                     |

<!-- ## <a id="22"></a> 
[`↑ scroll up`](#top) -->

## <a id="22"></a> Что такое промисы (Promises)? //!

Промисы — это один из приемов работы с асинхронным кодом в JS. Они возвращают результат асинхронной операции.

4 СОСТОЯНИЯ: ожидание (pending), исполнено (fulfilled) - операция завершена успешно. отклонено (rejected) - операция завершена с ошибкой.

В качестве параметров конструктор промиса принимает resolve и reject. В resolve записывается результат выполнения, в reject — причина невыполнения.
Результат может быть обработан в методе .then,
ошибка — в методе .catch.
Метод .then также возвращает промис, поэтому мы можем использовать цепочку, состоящую из нескольких .then.

[`↑ scroll up`](#top)

## <a id="21"></a> SPREAD и REST операторы

Разница состоит в том, что с помощью spread мы передаем или распространяем данные массива на другие данные, а с помощью rest — получаем все параметры функции и помещаем их в массив

[`↑ scroll up`](#top)

## <a id="20"></a> Как проверить, является ли значение массивом?

Array.isArray(массив)

[`↑ scroll up`](#top)

## <a id="19"></a> Какие приемы работы с асинхронным кодом в JS Вы знаете?

Функции обратного вызова (Callbacks).
Промисы (Promises).
Async/await.

[`↑ scroll up`](#top)

## <a id="18"></a> В чем разница между обычной функцией и функциональным выражением?

Обычная функция всплывает, а функциональное выражение нет

```javascript
// функция
function hoistedFunc(){
    console.log('I am hoisted')
}
// функциональное выражение
var notHoistedFunc = function(){
    console.log('I will not be hoisted!')
}
```

[`↑ scroll up`](#top)

## <a id="17"></a> Что такое запоминание или мемоизация

Мемоизация — это прием создания функции, способной запоминать ранее вычисленные результаты или значения. Преимущество мемоизации заключается в том, что мы избегаем повторного выполнения функции с одинаковыми аргументами. Недостатком является то, что мы вынуждены выделять дополнительную память для сохранения результатов

[`↑ scroll up`](#top)

## <a id="16"></a> Для чего используется `new`?

Ключевое слово «new» используется в функциях-конструкторах для создания нового объекта (нового экземпляра класса).

[`↑ scroll up`](#top)

## <a id="15"></a> EVENT LOOP

Event Loop это цикл, который ожидает задачи, выполняет их и ожидает поступления новых задач.
Асинхронные операции не блокируют поток, они регистрируются и возвращаются в поток после выполнения и очистки стека вызовов(основного потока).

[`↑ scroll up`](#top)

## <a id="14"></a> CORS

технология браузеров, которая позволяет предоставить веб-страницам доступ к ресурсам другого домена.

[`↑ scroll up`](#top)

## <a id="13"></a> Жизненный цикл компонента

- Mounting - рендер
- Updation - когда меняется стэйт
- Unmounting - рендер другого компонента

[`↑ scroll up`](#top)

## <a id="12"></a> ХУКИ

- useState
- useEffect
- useContext
- useReducer
- useParams
- useHistory
- useRef
- useMemo
- useCalback
- …

[`↑ scroll up`](#top)

## <a id="11"></a> Что такое AJAX?

AJAX или Asyncronous JavaScript and XML — это набор взаимосвязанных технологий, которые позволяют работать с данными в асинхронном режиме. Это означает, что мы можем отправлять данные на сервер и получать данные с него без перезагрузки веб-страницы.

[`↑ scroll up`](#top)

## <a id="10"></a> Что такое NaN

NaN (не число) — это значение, получаемое в результате выполнения числовой операции над нечисловым значением.

В JS есть встроенный метод isNaN, позволяющий проверять, является ли значение NaN

[`↑ scroll up`](#top)

## <a id="9"></a> Плюсы Реакта

Оптимизирует процесс отрисовки интерфейсов

[`↑ scroll up`](#top)

## <a id="8"></a> Что делает super у класса?

- При переопределении конструктора:
  - Обязателен вызов конструктора родителя `super()` в конструкторе Child до обращения к `this`.
- При переопределении другого метода:
  - Мы можем вызвать `super.method()` в методе Child для обращения к методу родителя Parent.

[`↑ scroll up`](#top)

## <a id="7"></a> Особенности Node.js

- среда выполнения для js; по сути — движок V8 + ряд механизмов, позволяющих выполнять js-код вне браузера
- позволяет с помощью кода, написанного на js, взаимодействовать с файловой системой компьютера, системой ввода/вывода и другими сущностями, которые недоступны из браузера
- поддержка модульности;
- возможность не только слать запросы, но и получать и обрабатывать;
- менеджер зависимостей (npm);

[`↑ scroll up`](#top)

## <a id="1"></a> Что такое Singleton

Паттерн программирования, должен гарантированно иметь лишь один объект, и к этому объекту должен быть предоставлен глобальный доступ.

[`↑ scroll up`](#top)

## <a id="2"></a> Классы и строки являются ссылочным типом?

Классы - да, строки нет.

Строки примитивный тип данных, в них ссылок нет, а вот объекты - это ссылочный тип.

[`↑ scroll up`](#top)

## <a id="3"></a> Демонизация Node.js

nodemon, supervisor, …

[`↑ scroll up`](#top)

## <a id="4"></a> Чем отличаются коллекции **Set** и **Map**

У `Set` уникальные значения, у `Map` ключ-значение.

[`↑ scroll up`](#top)

## <a id="5"></a> Oбласти видимости у `let` и `const`

ОВ переменных:

- `let`, `const` – блочная { … }. Видны только после объявления. При использовании в цикле, для каждой итерации создаётся своя переменная.
- `var` – глобальная. Доступ из любого места в коде. Переменная var – одна на все итерации цикла и видна даже после цикла:

```javascript
// С var прокатит:
console.log(hello) // undefined
var hello = "Hello"

// C let и const — нет:
console.log(hello) // Reference error
let hello = "Hello"

console.log(bye) // Reference error
const bye = "Bye"
```

[`↑ scroll up`](#top)

## <a id="6"></a> Контекст стрелочной функции

Стрелочные функции не имеют собственного контекста выполнения. На практике это означает, что они наследуют сущности `this` и `arguments` от родительской функции.

[`↑ scroll up`](#top)
