# **Отчет о выполнении Домашнего задания №3**

## *Выполнил* Шатравка Даниил Алексанрович БПИ212

## *Вариант 38*

---

## На 4 балла

### Условие задачи

Список чисел. Вывести список всех натуральных чисел, содержащих
от 4 до 9 значащих цифр, которые после умножения на n, будут содержать
все те же самые цифры в произвольной последовательности и в произвольном количестве. Входные данные: целое положительное число n, больше
единицы и меньше десяти (2..9). Количество потоков также является вход-
ным параметром.

### Модель вычисления

Программа разбивает диапазон $[10^4; 10^9]$ чисел на равные части, которые передаются потокам. Каждый поток проверяет числа на соответствие условию и выводит их в файл.

### Входные данные

При запуске пользователь может передать через аргументы командной строки количество потоков, входной и выходной файлы. Если аргументы не переданы, то программа использует значения по умолчанию.

### Приложение

Программа написана на языке C++ с использованием библиотеки PThread. Исходный код программы можно найти [здесь](task5.cpp).

## на 5 баллов

### Комментарии

Файл содержащий код программы, прокомментирован на английском языке.

### Сценарий поведения потоковых единиц

Каждый поток проверяет каждое число из диапазона на соответствие условию, совершая 5 действий:

1. Число раскладывается на цифры и записывается в массив.
2. Число умножается на n.
3. Результат умножения раскладывается на цифры и записывается в массив.
4. Сравниваются массивы цифр.
5. Если массивы совпадают, то число выводится в файл.

## На 6 баллов

### Описание работы программы

Программа получает число n, которое будет умножаться на числа из диапазона. Используя число активных потоков, программа разбивает диапазон на равные части, которые передаются потокам. Каждый поток проверяет каждое число из диапазона на соответствие условию и выводит его в файл. Каждое число раскладывается на составляющие цифры, затем число умножается на n и результат также раскладывается на составляющие цифры. Далее сравниваются два массива, содержащие цифры числа и его произведения. Если массивы совпадают, то число удовлетворяет условию и выводится в файл.

### Ввод данных из командной строки

Ввод данных организован с помощью параметров командой строки, описанными [здесь](#входные-данные).

## На 7 баллов

### Ввод и вывод данных при помощи файлов

В программе реализован ввод и вывод из файла. Входной файл должен содержать одно целое число от 1 до 9. Выходной файл содержит числа, удовлетворяющие условию.
Имена файлов передаются в качестве параметров командной строки.

Вывод в консоль не предусмотрен ввиду того, что количество чисел, удовлетворяющих условию, может быть очень большим.

Примеры входных данных находятся [здесь](./Tests/).

Невозможно представить примеры выходных данных, так как файлы содержат очень большое количество чисел и github не позволяет загружать файлы размером более 100 Мб.

## На 8 баллов

### Генератор значений

При отсутствии входного файла программа генерирует случайное число от 1 до 9 и использует его в качестве n.
