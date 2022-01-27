# Тестовое задание. Тир.
Задание выполняется на C# без использования .NET или других фреймворков. Реализовать консольное приложение с выводом результатов на экран.

Для проведения корпоративного мероприятия компания посетила тир в составе 13 человек.

В стрелковом тире 6 направлений для стрельбы (аналог дорожек в боулинге) и 2 инструктора закрепленных за своими тремя направлениями. Т.к. направлений меньше числа стрелков, стрелки сформировали живую очередь.

Правила тира допускают выполнение стрельбы только по команде инструктора для каждого из стрелков. Таким образом, одновременную стрельбу могут вести только 2 направления.

Каждому стрелку доступно 5 подходов к направлению. После выполнения стрельбы, стрелок уступает место следующему ожидающему в очереди, а сам, если необходимо продолжить стрельбы, встает последним в очередь.

Стрельбы состоят из следующих последовательных действий:

|            | Длительность действия (таймаут до сообщения), случайное число, от-до, секунды | Сообщение                | Ограничение                                                                     |
| ---------- | :--------------------------------------------------------------------------: | ------------------------ | ------------------------------------------------------------------------------- |
| Стрелок    | 3-10                                                                         | Занял направление!       | Ограничений нет, смена стрелка производится при наличии свободного направления. |
| Инструктор | 2-6                                                                          | Подготовится к стрельбе! | Только в присутствии инструктора.                                               |
| Стрелок    | 1-4                                                                          | К стрельбе готов!        | Только в присутствии инструктора.                                               |
| Инструктор | 1-2                                                                          | Произвести стрельбу!     | Только в присутствии инструктора.                                               |
| Стрелок    | 5-15                                                                         | Стрельбу окончил!        | Только в присутствии инструктора.                                               |

Задача
Реализовать программу, которая при проведении стрельб:

- выводит сообщения в консоль вида Направление {G}, инструктор {T}, стрелок {S}: {M}. Например: Направление 2, инструктор 1, стрелок 5: К стрельбе готов!;
- считает сумму времени затраченного на все события, длительность всего мероприятия (стрельб) и, по его окончании, выводит сообщение Сумма затраченного времени: {A}. Длительность стрельб: {B} в формате минут и секунд. Например: Сумма затраченного времени: 3 минуты 2 секунды. Длительность стрельб: 1 минута 21 секунда.
