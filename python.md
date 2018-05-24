### Hello, World!

22.02.2018 11:15. Попробовать образовательный проект в PyCharm. Один из первых шагов - ```print("Hello, world! My name is Aleksey")``` отдает:

```
Hello, world! My name is Aleksey

Process finished with exit code 0
```

Comments in Python start with the hash character (#) and include the whole line. You can use Ctrl + / to comment or uncomment the whole line in PyCharm. Add a new comment to the file.

Комментарии в Python начинаются с символа hash (#) и включают всю строку. Вы можете использовать Ctrl + /, чтобы комментировать или раскомментировать всю строку в PyCharm. Добавьте новый комментарий к файлу.

11:25. Variables are used to store values so we can refer to them later. A variable is like a label, and you use the '=' symbol, known as the assignment operator, to assign a value to a variable. An assignment can be chained, e.g. a = b = 2. Change the value stored in the variable greetings. 

### Переменные

Переменные используются для хранения значений, поэтому мы можем ссылаться на них позже. Переменная походит на метку, и вы используете символ '=', называемый оператором присваивания, для назначения значения переменной. Назначение может быть прикованным/сцепленным, например. a = b = 2. Измените значение, сохраненное в объявленных переменных.

```
a = b = 2  # This is called a "chained assignment". It assigns the value 2 to variables "a" and "b".
print("a = " + str(a))   # We'll explain the expression str(a) later in the course. For now it is used to convert the  variable "a" to a string.
print("b = " + str(b))

greetings = "greetings"
print("greetings = " + str(greetings))
greetings = 127
print("greetings = " + str(greetings))
```

### Комбинации клавиш

Как запустить скрипт из текущего окна? Alt+Shift+F10. Что происходит в print? Зачем столько символов? Нет, нужно книгу читать и из книги повторять.

11:35. Эл Свейгарт "Автоматизация рутинных задач с помощью Python", 2017 год. Закрыть PyCharm Edu, поскольку согласно содержания книги следует использовать IDLE.

11:43. Эл расскажет про функцию str() на 55 странице, когда PycharnEdu предлагал задачу с этой функцией на третьем из 50 шагов урока. Пропустить "Содержание" длящееся по 21 страницу включительно.

11:53. Воспринимать книгу не как справочник, а как руководство для начинающих. 26 страница.

12:03. Предназначение книги - научиться писать простой одноразовый код. Работоспособные программы с минимальными усилиями. Не ожидать обсуждения понятия "объектно-ориентированный подход"? Почему? Другое почему - почему мне интересно программирование? Потому что мне нравится строительство конструктора? А инструкции в программировании это строительные блоки для комбинации и реализации сложных решений? Что такое исходный код? Это инструкции.

12:13. Как выполняется исходных код? Программное обеспечение последовательно выполняет кажду строку кода, начиная с первой, пока не будет достигнут конец программы. Попробовать набрать и запустить исходный код с 27 страницы книги Эла Свейгарта. В IDLE это неудобно, поскольку после получения сообщения
```
Traceback (most recent call last):
  File "<pyshell#3>", line 1, in <module>
    passwordFile = open('SecretPasswordFile.txt')
FileNotFoundError: [Errno 2] No such file or directory: 'SecretPasswordFile.txt'
```
нельзя удобно повторить запуск кода. Запустить PyCharm CE.

### UTF-8

Попробовать объявить стандарт кодирования текста для хранения и передачи символов Юникода, поддерживающего буквы кириллицы:
```
# coding:utf8
passwordFile = open('SecretPasswordFile.txt')
secretPassword = passwordFile.read()
print('Введите пароль')
typedPassword = input()
if typedPassword == secretPassword:
    print('Доступ разрешен')
    if typedPassword == '12345':
        print('Рекомендуем установить более сложный пароль!')
else:
    print('Отказано в доступе')
```
и на выходе
```
/Users/aleksey/PycharmProjects/setests/venv/bin/python /Users/aleksey/PycharmProjects/setests/venv/sveigart.py
Введите пароль
12345
Отказано в доступе

Process finished with exit code 0
```

добавить в файл SecretPasswordFile.txt пароль 67890 и попробовать ввести его на запрос программы. Получить на выходе:
```
/Users/aleksey/PycharmProjects/setests/venv/bin/python /Users/aleksey/PycharmProjects/setests/venv/sveigart.py
Введите пароль
67890
Отказано в доступе

Process finished with exit code 0
```
Ввести 12345 и ожидать сообщения про слишком легкий пароль, но получить сообщение:
```
/Users/aleksey/PycharmProjects/setests/venv/bin/python /Users/aleksey/PycharmProjects/setests/venv/sveigart.py
Введите пароль
12345
Отказано в доступе

Process finished with exit code 0
```

