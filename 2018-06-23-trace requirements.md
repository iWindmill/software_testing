# Двунаправленная трассируемость между тестовым базисом и тестовым сценарием

## Содержание
1. [«Сертифицированный тестировщик. Программа обучения Базового уровня»](#istqb_f)
2. [«Тестирование программного обеспечения. Базовый курс»](#<a name="kulikov"></a>)

### «Сертифицированный тестировщик Программа обучения Базового уровня» <a name="istqb_f"></a>

Версия 2011 от 13 апреля 2011 года, International Software Testing Qualifications Board, Андрей Конушин (председатель), Александр Александров, Алексей Александров, Татьяна Смехнова, Елена Абрамова. 36/101 страница:

**1.4.2 Анализ и проектирование тестов**

Для анализа и проектирования тестов поставлены следующие основные задачи:
... Создание двунаправленной трассируемости между тестовым базисом и тестовым сценарием...

**1.4.3 Реализация и выполнение тестов**

Для реализации и выполнения тестов поставлены следующие основные задачи:
- ...
- Проверка и обновление двунаправленной трассируемости между тестовым базисом и тестовым сценарием...

**4.1 Процесс разработки тестов**

Установление трассируемости от тестовых условий назад к спецификациям и требованиям позволяет как определить последствия при изменяющихся требованиях, так и установить покрытие требований набором тестов. При анализе тестирования реализуется детализированный подход к тестированию с целью выбора методов проектирования тестов, основываясь, в том числе, на выявленных рисках (см. Главу 5).

**5.1.2 Задачи руководителя тестирования и тестировщика**

Типичные задачи руководителя тестирования могут включать:
- ...
- Установка адекватного управления конфигурацией для обеспечения трассируемости тестирования...

**5.4 Управление конфигурацией**

Для тестирования управление конфигурацией может гарантировать:
- Все пункты того, что нужно протестировать, определены, контролируются по версиям, все изменения учитываются, связаны с разрабатываемыми элементами (объекты тестирования) и друг с другом так, что бы обеспечить трассировку на протяжении всего процесса тестирования...

### «Тестирование программного обеспечения. Базовый курс» <a name="kulikov"></a>

![Святослав Куликов, EPAM](https://lh3.googleusercontent.com/N6l4LtcWxQUMlqQxxBl9xaVmubSyTRk3WZYl88rWmVcQRgJKbe925enFh4zMaa0Fgi7myy_kUosDiOP2yp1sfVMME2hjTgPL2Z7zIwuTFD_VbS08_RRD6cPgB1qDm2xbfkAbpsW3massg0LRJffdImuDolqNvKqckBaJAYIblpY6zqWOigjnYiu-l_VdNIIMb-eZc6iVqbZrzQZ5Qoqr7Er8QURTjYuFmNacP7pOU7Vq60Wse2F9hmN0NQoPBUSLCAIYqW_Ux1RFaERGB5aj1u7HkmlVCQs5u1m0U5QV61VptZQq3h8idbnEs3gtG8c2zU89NX_zkpbHkK2Ws5X5x_v6fxf9-IrYFsaBMsyGaea6v-u2rl9aybLbWcJzlaC8u0MuKtPY1TKf4NnR-mKMduW6ROOn7tLLleiXBhXTBWC8tTkat3b4JcwixGpBx2nMZxfMewUdB9LAJDv0AXng8zKQE2V2WuZ5kVdgoeGaqU-M30F39uCiDir0hAVtzSe6zMhYcGXLH9a6DHIY5OVrSMhptKzHv652cZDHq3MpMlZOQ-w-5-IXsob4YPIoU_79XvOEboxzycRjmGT3TmQUKgggxhihaD1S9tDowYjKQqiEmGYcLmoHLs2vF5e3-7Gv5vhFJRanCPO_yZxzfykfMwkMR2x7vxc3=w1225-h816-no)

Святослав Куликов. Версия книги 1.2.1 от 02.08.2017, EPAM Systems. 114-/295 страницы:

Спецификация требований (software requirements specification, SRS 83) объединяет в себе описание всех требований уровня продукта и может представлять собой весьма объёмный документ (сотни и тысячи страниц).

Поскольку требований может быть очень много, а их приходится не только единожды написать и согласовать между собой, но и постоянно обновлять, работу проектной команды по управлению требованиями значительно облегчают соответствующие инструментальные средства (requirements management tools 84, 85).

Для более глубокого понимания принципов создания, организации и использования набора требований рекомендуется ознакомиться с фундаментальной работой Карла Вигерса «Разработка требований к программному обеспечению» («Software Requirements (3rd Edition) (Developer Best Practices)», Karl Wiegers, Joy Beatty). В этой же книге (в приложениях) приведены крайне наглядные учебные примеры документов, описывающих требования различного уровня.

84 Requirements management tool. A tool that supports the recording of requirements, requirements attributes (e.g. priority, knowledge responsible) and annotation, and facilitates traceability through layers of requirements and requirements change management. Some requirements management tools also provide facilities for static analysis, such as consistency checking and violations to predefined requirements rules. [ISTQB Glossary]

85 Обширный список инструментальных средств управления требованиями можно найти здесь:
http://makingofsoftware.com/resources/list-of-rm-tools

23.06.2018. Перейти на [Главную страницу](./)