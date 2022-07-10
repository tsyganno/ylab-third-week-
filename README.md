# ylab-third-week




1. Задача на декоратор с кешированием результата. Секция статьи "1. Задача на декоратор с кешированием результата."
Напишите функцию-декоратор, которая сохранит (закэширует) значение декорируемой функции multiplier (Чистая функция). Если декорируемая функция будет вызвана повторно с теми же параметрами — декоратор должен вернуть сохранённый результат, не выполняя функцию.

В качестве структуры для кэша, можете использовать словарь в Python.





2. Задача на декоратор с параметрами. Секция статьи "2. Задача на декоратор с параметрами."
Надо написать декоратор для повторного выполнения декорируемой функции через некоторое время. Использует наивный экспоненциальный рост времени повтора (factor) до граничного времени ожидания (border_sleep_time).

В качестве параметров декоратор будет получать:

call_count - число, описывающее кол-во раз запуска функций;
start_sleep_time - начальное время повтора;
factor - во сколько раз нужно увеличить время ожидания;
border_sleep_time - граничное время ожидания.
Формула:

t = start_sleep_time * 2^(n) if t < border_sleep_time
t = border_sleep_time if t >= border_sleep_time
