09:11. Попробовать в PyCharm CE выполнить код из статьи Хабра [Selenium для Python. Глава 2. Первые Шаги](https://habrahabr.ru/post/250921/):
```
# coding:utf8
from selenium import webdriver
from selenium.webdriver.common.keys import Keys  # классом Keys обеспечить взаимодействие с командами клавиатуры F1, ALT

driver = webdriver.Chrome()  # создать элемент класса Chrome WebDriver
driver.get("http://www.python.org")  # методом driver.get перенаправить к странице URL в параметре.
                                     # WebDriver будет ждать пока страница не загрузится полностью
                                     # то есть, событие "onload" игнорируется, прежде чем передать
                                     # контроль тесту или скрипту. Стоит отметить, что если страница использует
                                     # много AJAX-кода при загрузке, то WebDriver может не распознать,
                                     # загрузилась ли она полностью
assert "Python" in driver.title      # утверждение (assertion), что заголовок содержит слово "Python"
elem = driver.find_element_by_name("q")  # использовать способ получения элементов с помощью метода find_element_by_*
elem.send_keys("pycon")              # послать нажатия клавиш (аналогично введению клавиш с клавиатуры)
elem.send_keys(Keys.RETURN)          # что здесь происходит?
assert "No results found." not in driver.page_source  # добавить утверждение, чтобы удостовериться в получении
                                                      # какого-либо результата
driver.close()  # методом close закрыть одну вкладку. Можно вызвать и метод quit для закрытия браузера полностью
```
Получить на выходе:
```
/Users/aleksey/PycharmProjects/setests/venv/bin/python /Users/aleksey/PycharmProjects/setests/habrPost250921.py

Process finished with exit code 0
```
Что означает "Process finished with exit code 0"? Программа отработала без ошибок.

### Что такое assert?

assert позволяет проверять предположения о значениях произвольных данных в произвольном месте программы. По своей сути assert напоминает констатацию факта, расположенную посреди кода программы. В случаях, когда произнесенное утверждение не верно, assert возбуждает исключение. Такое поведение позволяет контролировать выполнение программы в строго определенном русле. Отличие assert от условий заключается в том, что программа с assert не приемлет иного хода событий, считая дальнейшее выполнение программы или функции бессмысленным — [Прим. пер](https://habrahabr.ru/post/250921/).

23.02.2018