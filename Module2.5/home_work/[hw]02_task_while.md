## "Кратные пяти из диапазона"

### Задание

Даны два целые числа a и b.

Выведите на экран все целые **кратные 5** от a до b включительно.

### Формат входных данных

Даны два целые числа. **Не гарантируется**, что a < b. \
Если a > b, то выводим все числа из диапазона [b, a].

### Формат выходных данных

Выведите все числа, требуемые по условию задачи.

### Решение задачи

```python
a = int(input("a: "))
b = int(input("b: "))

arr_start = int(input('начало диапазона: '))
arr_end = int(input('конец диапазона: '))
if arr_start > arr_end:
    arr_start = arr_start + arr_end
    arr_end = arr_start - arr_end
    arr_start = arr_start - arr_end
counter = arr_start
while counter <= arr_end:
    if counter % 5 == 0:
        print(counter)
    counter += 1
```
