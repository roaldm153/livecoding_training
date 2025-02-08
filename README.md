# livecoding


Решение принимается в виде PR из ветки livecoding через отправку в [форму](https://forms.gle/FzAYqKVkSf9CEzXRA).
Разрешается пользоваться только cppreference, любые другие иточники включая ваш прошлый код запрещены

## Задача

Реализовать консольное приложение для фильтрации текста из файла по заданным правилам.


Приложение должно поддержать следующие  два аргумента командной строки:

**--input PATH** - путь к текстовому файлу

**--filterdb PATH**   -  путь к базе правил фильтрации


## Входные данные

* Текстовый файл состоит из одной или более строк, длина каждой не превышает 1024 символа. Слова могут быть разделены только пробелом. 
* Приложение не чувтсвительно к регистру

База правил фильтрации представляет собой текстовый файл, где каждое правило написано с новой строки. Пример:

```
aab
aacd
orl
```

## Выходные данные

В выходной текстовый файл требуется записать содержимое входного текстового файла за исключением тех контекстов, в которых были найдены паттерны, находящиеся в базе правил фильтрации

**Примечание**: контекстом следует считать последовательность, ограниченную с двух сторон пробелами либо началом и концом файла. Длина контекста не может быть больше 128 символов

## Вывод

Программа должна вывести на экран самый часто используемый фильтр и медианный размер отбрасываемого этим фильтром контекста разделённые символом пробела

## Ограничения


Запрещается использовать:

* контейнеры стандартной библиотеки 
* std::string и std::string_view
