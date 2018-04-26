Как запустить скрипт из текущего окна? Alt+Shift+F10. Что происходит в ping? Зачем столько символов? Нет, нужно книгу читать и из книги повторять.

11:35. Эл Свейгарт "Автоматизация рутинных задач с помощью Python", 2017 год. Закрыть PyCharm Edu, поскольку согласно содержания книги следует использовать IDLE.

11:43. Эл расскажет про функцию str() на 55 странице, когда PycharnEdu предлагал задачу с этой функцией на третьем из 50 шагов урока. Пропустить "Содержание" длящееся по 21 страницу включительно.

11:53. Воспринимать книгу не как справочник, а как руководство для начинающих. 26 страница.

12:03. Предназначение книги - научиться писать простой одноразовый код. Работоспособные программы с минимальными усилиями. Не ожидать обсуждения понятия "объектно-ориентированный подход"? Почему? Другое почему - почему мне интересно программирование? Потому что мне нравится строительство конструктора? А инструкции в программировании это строительные блоки для комбинации и реализации сложных решений? Что такое исходный код? Это инструкции.

12:13. Как выполняется исходных код? Программное обеспечение последовательно выполняет кажду строку кода, начиная с первой, пока не будет достигнут конец программы. Попробовать набрать первую строку исходного кода с 27 страницы? ```passwordFile = open('SecretPasswordFile.txt')```. В IDLE это неудобно, поскольку после получения сообщения
```
Traceback (most recent call last):
  File "<pyshell#3>", line 1, in <module>
    passwordFile = open('SecretPasswordFile.txt')
FileNotFoundError: [Errno 2] No such file or directory: 'SecretPasswordFile.txt'
```
нельзя удобно повторить запуск кода. Запустить PyCharm CE. Попробовать ввести первой код Эла Свейгарта:

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
и получить на выходе:
```
/Users/aleksey/PycharmProjects/setests/venv/bin/python /Users/aleksey/PycharmProjects/setests/venv/sveigart.py
Введите пароль
12345
Отказано в доступе

Process finished with exit code 0
```

Добавил в файл SecretPasswordFile.txt пароль 67890 и еще раз запустить код, попробовать сохраненный пароль:
```
/Users/aleksey/PycharmProjects/setests/venv/bin/python /Users/aleksey/PycharmProjects/setests/venv/sveigart.py
Введите пароль
67890
Отказано в доступе

Process finished with exit code 0
```
Ввести 12345 и ожидать про слишком легкий пароль, но получить:
```
/Users/aleksey/PycharmProjects/setests/venv/bin/python /Users/aleksey/PycharmProjects/setests/venv/sveigart.py
Введите пароль
12345
Отказано в доступе

Process finished with exit code 0
```

22.02.2018