# Блок 1 - выбор специализации

## Контрольная работа

***

[Ссылка на репозиторий в ГитХаб](https://github.com/ScherbakovAV/Test_work1.git "Контрольная работа к блоку 1")

* Блок-схема к заданию - в файлах diagram.json и diagram.png
* Программная реализация задачи на языке C# находится в папке Program

### **Задание:**

> *Написать программу, которая из имеющегося массива строк формирует
новый массив из строк, длина которых меньше либо равна 3 символам.*
### **Текстовое описание решения задания**:

1. Пользователь вводит с клавиатуры через пробел произвольное количество элементов будущего массива. Введённая строка присваивается переменной **str** с типом **string**.
2. Производится сравнение длины введённой строки с 0. Если длина равна 0 (пользователь не ввёл ничего), выводится сообщение о ошибке ввода, программа завершает работу. Иначе, выполнение программы продолжается.
3. Создаём массив типа **string[]** с именем **arrayString** из строки **str** с помощью встроенного метода **split**, используя **пробел** (" ") в качестве разделителя.
4. Печатаем массив **arrayString** созданным методом **PrintStrArray()** (описание метода в п.8), принимая на вход сам массив и сообщение пользователю типа **string**.
5. Создаём новый массив **newArray** с типом **string[]**, который получаем из массива строк **arrayString** с помощью созданного метода **ToArrayWithElementsLess()** (описание метода в п. 9).
6. Печатаем массив **newArray** с использованием метода **PrintStrArray()**.
7. Программа завершает работу.
8. *Метод **PrintStrArray()**:*
    1. метод ничего не возвращает (**void**)
    2. печатаем сообщение пользователю, которое принимаем как второй параметр метода - **message** с типом **string**;
    3. печатаем открывающую квадратную скобку **"["**; 
    4. запускаем цикл с шагом 1 со счётчиком **i** от 0 до максимального индекса массива **arr** с типом **string[]** (который принимаем как первый параметр метода):
        * для всех элементов массива, кроме последнего, выводим на печать **"{arr[i]}, "**
        * для последнего элемента массива выводим на печать **"{arr[i]}"**
    5. печатаем закрывающую квадратную скобку **"]"**;
    6. метод завершает работу.
9. *Метод **ArrayWithElementsLess()**:*
    1. метод возвращает массив **arrayTruncated** типа **string[]**;
    2. метод принимает на вход два параметра: массив строк **array** и требуемую длину выводимых строк **elementLength** типа **int** (по умолчанию эта переменнная равна 3, как в условии задачи);
    3. создаём две переменные типа **int** - **newArrayLength** (будущая длина нового массива) и **count** (счётчик);
    4. циклом с шагом 1 со счётчиком **i** от 0 до  максимального индекса массива **array** проходим все элементы этого массива, где условным оператором сравниваем длину элементов с **elementLength** (в данном случае равной 3), и если эта длина меньше или равна **elementLength**, добавляем 1 в переменную-счётчик **newArrayLength**;
    5. создаём новый пустой массив **arrayTruncated** с типом **string[]** и длиной, равной **newArrayLength**;
    6. запускаем цикл с шагом 1 со счётчиком **j** от 0 до  максимального индекса массива **array**, на каждой итерации которого сравниваем каждый элемент массива **array** <= **elementLength**, и в том случае, если условие выпоняется:
        1. записываем в **arrayTruncated[count]** значение элемента **array[j]**;
        2. увеличиваем значение переменной **count** на **1**;
    7. возвращаем заполненный массив строк **arrayTruncated**;
    8. метод завершает работу;

 



