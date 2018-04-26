### Комбинаторика

1. Решение задачи №1:
> Очевидно, число разных путей из Киева до Новгорода-Северского равно ```4 Х 2 = 8```, так как, выбрав один из четырех возможных способов путешествия от Киева до Чернигова, имеем два возможных способа путешествия от Чернигова до Новгорода-Северского (рис. 1).
> ![](https://lh3.googleusercontent.com/Q7LtcojkE1ws-004sLfmvAkXz9fKLaHHU7xzxAGel_UskuWi7c4ZJ8GdK68C9OkTAQSt9yWMW17fKRw4zbKU6jurD8CiZKU8uBGGA1gwxQ24_lWYmqF8vvLRRnRNaKUWMXLJoGABt5RU8XROjcGjHX-XLc2Q97j5KTEwkwOUbEkP0jbkhPMh_eUQEwLHO9QWBzjKm_P959s2UHSaNl0DSWG2VJRlAenW74pvON8U85LLyb29onJzet3qQZKOxb4-KJxTLu-qRso1Rst3LnQjei2J16O8T2B00dnSg6N0ALYtQVRWNjHWqbKe_8zXhlCLn19l7EGBW9AiHBnMxb65C2tuSSpuSsHwrcSAM9LS5s5n97kkL7lRjJC89k-z1792VErk6JJkdVAV1uiGCdJQj3SgUvZoZk5in-49Etz4M2mw0dJddlI-9jG_WEKhf7cXRtugdQVZbEqj000dZE4n_8FReGCSQF6sDk7XX7qOiVnbmCPYtvziL388gSbCxamktLaxv0cenG2OUBV6jeouhjdsoYXSP83dG94n3bqqQbpTW1aYXdpsUX06lBJt9xA3yseG3HQdfpii6lAwxjq-i-GE1kyVK21ymqb41gwp0BJYVEuNKAZWU1kbbK2YtIsTT0913ZY7VkW4PhP2PzndjpusumXrMTso=w1125-h307-no)

> Соображения, которые были приведены при решении задачи 1, доказывают справедливость следующего простого утверждения, которое будем называть _основным правилом комбинаторики_.

> Если некоторый выбор ```А``` можно осуществить m различными способами, а для каждого из этих способов некоторый другой выбор B можно осуществить n способами, то выбор ```A``` и ```B``` (в указанном порядке) можно осуществить ```m Х n``` способами.

> Иначе говоря, если некоторое действие (например, выбор пути от Киева до Чернигова) можно осуществить m различными способами, после чего другое действие (выбор пути от Чернигова до Новгорода-Северского) можно осуществить n способами, то два действия вместе (выбор пути от Киева до Чернигова, выбор пути от Чернигова до Новгорода-Северского) можно осуществить ```m Х n``` способами.

2. Решение задачи №2:

> Золотую медаль может получить одна из 16 команд. После того как определен владелец золотой медали, серебряную медаль может иметь одна из 15 команд. Следовательно, общее число способов, которыми могу быть распределены золотая и серебряная медали, равно ```16 X 15 = 240```.

> Сформулируем теперь основное правило комбинаторики (правило умножения) в общем виде.

> Пусть требует выполнить одно за другим ```k``` действий. Если первое действие можно выполнить n<sub>1</sub> способами, второе действие - n<sub>2</sub> способами, третье действие - n<sub>3</sub> способами и так до k-го действия, которое можно выполнить n<sub>k</sub> способами, то все ```k``` действий вместе могут быть выполнены

> n<sub>1</sub> X n<sub>2</sub> X n<sub>3</sub> X ... n<sub>k</sub>

> способами.

2. Решение задачи №3:

> а) первой цифрой числа может быть одна из 5 цифр 1, 2, 3, 4, 5 (0 не может быть первой цифрой, потому что в таком случае число не четырехзначное); если первая цифра выбрана, то вторая может быть выбрана 5 способами, третья - 4 способами, четвертая - 3 способами, согласно правилу умножения общее число способов равно 5 X 5 X 4 X 3 = 300.

> б) Первой цифрой может быть одна из цифр 1, 2, 3, 4, 5 (5 возможностей), для каждой из следующих цифр имеет 6 возможностей (0, 1, 2, 3, 4, 5). Следовательно, число искомых числе равно 5 Х 6 Х 6 Х 6 = 5 Х 6<sup>3</sup> = 1080.

### Тестирование программного обеспечения

1. Which of the following statements BEST describes one of the seven key principles of software testing?

> a) FALSE – Exhaustive test is impossible, regardless of it being manual or automated. (Section. 1.3; Principle #2)
b) FALSE – Exhaustive testing is impossible, regardless of the amount of effort put into testing (Section. 1.3; Principle #2)
c) TRUE – Principle #2 (Section 1.3) states: “Testing everything (all combinations of inputs and preconditions) is not feasible except for trivial cases”
d) FALSE – This statement is contradicting Principle #1(Section 1.3): Testing shows presence of defects: Testing can show that defects are present, but cannot prove that there are no defects.

> a) ЛОЖЬ - Исчерпывающее тестирование невозможно, независимо от того, является ли оно ручным или автоматизированным. (Раздел 1.3, принцип № 2)
b) FALSE - Исчерпывающее тестирование невозможно, независимо от количества усилий, затраченных на тестирование (раздел 1.3, принцип № 2)
c) TRUE - Принцип № 2 (раздел 1.3) гласит: «Тестирование всего (все комбинации входов и предварительных условий) невозможно, за исключением тривиальных случаев»
d) ЛОЖЬ - это утверждение противоречит Принципу № 1 (раздел 1.3): Тестирование показывает наличие дефектов: Тестирование может показать наличие дефектов, но не может доказать, что дефектов нет.

2. Which of the following statements is the MOST valid goal for a test team?

> a) FALSE – Component testing is not part of System testing. (Section 2.2.1 and 2.2.3)
b) TRUE – This is the main role of a test team. (Section 1.2, objectives, 1. dot)
c) FALSE – Principle #1 states that exhaustive testing is impossible, so one can never prove that all defects were identified.
d) FALSE – To make an assessment whether a defect will cause a failure or not, one has to detect the defect first. Saying that no remaining defect will cause a failure, implicitly means that all defects were found. This contradicts Principle #1.

> a) FALSE - тестирование компонентов не является частью системного тестирования. (Раздел 2.2.1 и 2.2.3)
б) ИСТИНА - Это основная роль тестовой команды. (Раздел 1.2, цели, 1. точка)
c) ЛОЖЬ - Принцип № 1 гласит, что исчерпывающее тестирование невозможно, поэтому невозможно доказать, что все дефекты были идентифицированы.
d) FALSE. Чтобы оценить, приведет ли дефект к сбою или нет, сначала необходимо обнаружить дефект. Говоря, что никакой оставшийся дефект не приведет к сбою, неявно означает, что все дефекты были обнаружены. Это противоречит принципу №1.

3. Which of these tasks would you expect to be performed during the Test Analysis and Design phase of the Fundamental Test Process?

> a) FALSE – this activity is performed during “Test Planning” phase (section 1.4.1, sentence 1)
b) TRUE – this activity is performed during “Test Analysis and Design” phase (section 1.4.2, 1. dot))
c) FALSE – this activity is performed during “Test Implementation and Execution” phase (section 1.4.3, 3. dot)
d) FALSE – this activity is performed during “Test Closure Activities” phase (section 1.4.5; 6. dot)

> a) FALSE - эта деятельность выполняется во время фазы «Планирование тестирования» (раздел 1.4.1, предложение 1)
б) ИСТИНА - эта деятельность выполняется во время фазы «Анализ и проектирование» (раздел 1.4.2, 1. точка))
c) FALSE - эта операция выполняется во время фазы «Реализация и Выполнение Тестов» (раздел 1.4.3, 3. точка)
d) FALSE - эта активность выполняется во время фазы «Действия по Завершению Тестирования» (раздел 1.4.5, 6. точка).

4. Below is a list of problems that can be observed during testing or in production. Which one of these problems is a failure?

> a) TRUE – A failure is an external manifestation of a defect. A crash is clearly noticeable by user
b) FALSE – This type of mistake will not necessarily lead to a visible or noticeable failure. For example: if the changes in the new version of the source file are only in the comments.
c) FALSE – Use of a FALSE input variable will not necessarily lead to a visible or noticeable failure. For example: if no one uses this specific algorithm; or: if the FALSEly used input variable had a similar value as the TRUE input variable; or: if no one is using the FALSE result from the algorithm. “Defects in software, systems or documents may result in failures, but not all defects do so.” (Section 1.1.2; 1. Par.; 3. dot)
d) FALSE – This type of mistake will not necessarily lead to a visible or noticeable failure. For example: if no one uses this specific algorithm.

> a) ИСТИНА - отказ - это внешнее проявление дефекта. отказ (failure): Отклонение компонента или системы от ожидаемого выполнения, эксплуатации или результата. [Fenton]. Краш ясно заметен пользователем
b) FALSE. Этот тип просчета (mistake) не обязательно приведет к видимому или заметному сбою. Например: если изменения в новой версии исходного файла находятся только в комментариях.
c) FALSE - Использование ЛОЖНОЙ входной переменной не обязательно приведет к видимому или заметному сбою. Например: если никто не использует этот конкретный алгоритм; или: если ОШИБОЧНАЯ входная переменная имела такое же значение, как ИСТИННАЯ входная переменная; или: если никто не использует ЛОЖНЫЙ результат из алгоритма. «Дефекты в программном обеспечении, системах или документах могут привести к сбоям, но не все дефекты делают это» (раздел 1.1.2, 1. Par., 3. точка)
d) FALSE. Этот тип просчета (mistake) не обязательно приведет к видимому или заметному сбою. Например: если никто не использует этот конкретный алгоритм.

5. Which of the following attitudes, qualifications or actions would lead to problems (or conflict) within mixed teams of testers and developers, when observed in reviews and tests?

> a) FALSE. There is no situation which leads to conflict. Testers and developers should be focused on finding defects
b) FALSE. This is a preferred situation, there is therefore no problem.
c) TRUE. According to the syllabus, testers and developers should cooperate, and communicating defects as criticism of people would lead to conflict inside the team. (Section 1.5.9; Par. 9; 2. dot)
d) FALSE. The tester’s role in the team is finding defects in the software product that the developers have not found and fixed.

> a) ЛОЖЬ. Нет ситуации, которая ведет к конфликту. Тестеры и разработчики должны быть сосредоточены на поиске дефектов
б) ЛОЖЬ. Это предпочтительная ситуация, поэтому нет проблем.
c) ИСТИНА. Согласно программе, тестеры и разработчики должны сотрудничать и сообщать о недостатках, поскольку критика людей приведет к конфликту внутри команды. (Раздел 1.5.9, пункт 9, 2. точка)
d) ЛОЖЬ. Роль тестировщика в команде заключается в обнаружении дефектов в программном продукте, которые разработчики не нашли и не зафиксировали.

6. Which of the following statements correctly describes the difference between testing and debugging?

> a) FALSE. Testing does not identify the source of defects (Section 1.2).
b) TRUE. Dynamic testing shows failures caused by defects; debugging finds, analyzes, and removes the causes of failures in the software (Section 1.2).
c) FALSE. Testing does not remove faults (Section 1.2).
d) FALSE. Dynamic testing does not prevent the causes of failures (Section 1.3).

> a) ЛОЖЬ. Тестирование не определяет источник дефектов (раздел 1.2).
б) ИСТИНА. Динамическое тестирование показывает сбои, вызванные дефектами; отладки, анализ и устранение причин сбоев в программном обеспечении (раздел 1.2).
c) ЛОЖЬ. Тестирование не устраняет неисправности (раздел 1.2). Отладка – это действия разработчиков, которые находят, анализируют и устраняют причину отказа. Повторное тестирование гарантирует, что изменение действительно предотвращает отказ.
d) ЛОЖЬ. ЛОЖЬ поскольку динамическое тестирование показывает, а не предотвращает сбои. Отладка да, устраняет ошибки или помогает их найти. Нужно уточнить. Динамическое тестирование может выявить отказы, вызванные дефектами. Отладка - это действия разработчиков, которые находят, анализируют и устраняют причину отказов. Раздел 1.2.

7. Which of the following statements BEST describes non-functional testing?

> a) FALSE, this is a definition of system testing (Section 2.2.3).
b) FALSE, this is a function of white box testing (Section 3.3 and Section 6.1.4).
c) FALSE, it is a definition of black box testing (Section 4.2).
d) TRUE, testing system characteristics, such as usability, reliability, or maintainability is non-functional testing (Section 2.3.2).

> A) ЛОЖЬ поскольку соответствие требованиям это функциональное тестирование
B) ЛОЖЬ ни разу функциональное тестирование не касается стандартов кодирования. Стандарты кодирования - это структурное тестирование
C) ВОЗМОЖНО ведь нефункциональное тестирование не является структурным тестированием
В) ИСТИНА. Нефункциональное требования и характеристик - это надежность, практичность, эффективность, сопровождаемость и переносимость. Раздел 1.1.4.

8. When working with software development models, what is it important to do?

> a) TRUE – Models provide general guidelines – not an accurate and step-by-step process that has to be followed to the letter. (Section 2.1)
b) FALSE – The waterfall is only one of the possible models a team can choose to follow.
c) FALSE – The V-model (Section 2.1.1) is not compatible with iterative models. (Section 2.1.2) So the described flow does not make sense.
d) FALSE – Models are chosen to fit the situation and project and not vice versa (Section 2.1, last Par.)

> a) ИСТИНА - Модели предоставляют общие рекомендации - не точный и пошаговый процесс, который должен соблюдаться в письме. (Раздел 2.1)
б) ЛОЖЬ - Водопад - это только одна из возможных моделей, которые команда может выбрать.
c) FALSE - V-модель (раздел 2.1.1) несовместима с итерационными моделями. (Раздел 2.1.2). Таким образом, описанный поток не имеет смысла.
d) FALSE - Модели выбраны так, чтобы они соответствовали ситуации и проектам, а не наоборот (раздел 2.1, последний параграф).

9. Which of the following is a characteristic of good testing and applies to any software development life cycle model?

> a) FALSE – This is TRUE only for projects that have acceptance tests. Some projects do not have this test level. (see Section 2.1).
b) FALSE – There are cases where some test levels are not necessarily needed. For example: when getting code from 3rd party, component testing is not needed.
c) FALSE – Testers should be involved much earlier than when the code is available. For example, testers should be involved in requirements specification reviews. (Section 1.4.2)
d) TRUE – “In any life cycle model, there are several characteristics of good testing: For every development activity there is a corresponding testing activity.” (Section 2.1.3)

> a) FALSE - это TRUE только для проектов, имеющих приемочные тесты. Некоторые проекты не имеют этого уровня тестирования. (см. раздел 2.1). ЛОЖЬ согласно 2.2.4 "Приемочное тестирование оценивает готовность системы к развертыванию и использованию, хотя это не обязательно самый последний уровень тестирования".
b) ЛОЖЬ - Есть случаи, когда некоторые уровни тестирования необязательно необходимы. Например: при получении кода от стороннего участника тестирование компонентов не требуется.
c) FALSE - Тестеры должны быть задействованы гораздо раньше, чем когда код доступен. Есть "Принцип 3 – Раннее тестирование. Чтобы найти дефекты как можно раньше, активности по тестированию должны быть начаты как можно раньше в жизненном цикле разработки программного обеспечения или системы, и должны быть сфокусированы на определенных целях". Например, тестировщики должны участвовать в обзорах спецификаций требований. (Раздел 1.4.2)
d) ИСТИНА - «В любой модели жизненного цикла существует несколько характеристик хорошего тестирования: для каждой деятельности в области разработки существует соответствующая тестовая деятельность» (раздел 2.1.3)

10. Which of the following is an example of maintenance testing?

> Maintenance testing. Testing the changes to an operational system or the impact of a changed environment to an operational system. Тестирование в период сопровождения (maintenance testing): Тестирование изменений в действующей системе или влияния изменений в окружении на действующу систему.

> a) FALSE – Testing a new system is not “maintenance testing” (Section 2.4).
b) TRUE – testing the system’s ability to perform after an environment change is considered “maintenance testing”. (Section 2.4).
c) FALSE – Dealing with Acceptance Test failures is not “maintenance testing” (cf. Section 2.4).
d) FALSE – Integration of functions is not a testing activity (cf. Section 2.2.2)

> a) FALSE. Тестирование новой системы не является «тестированием в период сопровождения» (раздел 2.4).
б) ИСТИНА - проверка способности системы функционировать после изменения среды считается «тестированием в период обсулижвания». (Раздел 2.4).
c) ЛОЖЬ - Работа с ошибками приемочного испытания не является «тестированием в период обслуживания» (см. раздел 2.4).
d) ЛОЖЬ - Интеграция функций не является тестовой деятельностью (см. раздел 2.2.2).

11. К каким из характеристик качества по ISO 25010 относятся описанные требования? Перечислите номера соответствующих характеристик качества в первом столбце строки с описаниями требований в приведенной ниже таблице.

> 1. Функциональность.
> 2. Надежность.
> 3. Эффективность, производительность
> 4. Удобство использования
> 5. Переносимость
> 6. Удобство сопровождения
> 7. Совместимость
> 8. Защищенность

> | № | Требование |
| - | - |
| Надежность (reliability) | Система должна работать 24 часа в сутки, 7 дней в неделю. Допустимый простой составляет 10 минут в год. |
| | Код каждого класса должен быть снабжен комментариями, описывающими все задачи, решаемые его объектами. |
| | Относительная погрешность не должна превосходить 10<sup>-15</sup> при вызове одной функции, и 10<sup>-8</sup> для всего вычисления с учетом накопления ошибок |
| Защита, защищенность (security) | Доступ пользователя к счетам должен быть невозможен без аутентификации |
| Удобство использования (usability) | Пользователь, имеющий специальность "финансовая аналитика", должен осваивать основные возможности системы не более чем за один день |
| | Web-сайт должен поддерживать одновременную работу с 10 000 пользователей. |

> 4.1.2 _Эффективность, производительность (efficiency)_: Связь точности и полноты достижения пользователями целей с израсходованными ресурсами (ИСО 9241-11). Примечание. Соответствующие ресурсы могут включать в себя время выполнения задачи (человече­ские ресурсы), материалы или финансовые затраты на использование.
> 4.2.3 _Совместимость (compatibility)_: Способность продукта, системы или компонента обменивать­ ся информацией с другими продуктами, системами или компонентами, и/или выполнять требуемые функции при совместном использовании одних и тех же аппаратных средств или программной среды. Примечание. Это определение адаптировано из ИСО/МЭК/ИИЕЕ 24765.

> 4.2.4 _Удобство использования (usability)_: Степень, в которой продукт или система могут быть использованы определенными пользователями для достижения конкретных целей с эффективностью, результативностью и удовлетворенностью в заданном контексте использования. Примечания. 1) Это определение адаптировано из ИСО 9241-210. 2) Удобство использования может быть либо задано или измерено как характеристика качества продукта в
терминах ее подхарактеристик, либо задано или измерено непосредственно показателями, которые составляют подмножество качества при использовании.

> 4.2.5 _Надежность (reliability)_: Степень выполнения системой, продуктом или компонентом опреде­ленных функций при указанных условиях в течение установленного периода времени. Примечания. 1) Это определение было адаптировано из (ИСО/МЭК/ИИЕЕ 24765). 2) В программном обеспечении износа не происходит. Проблемы с надежностью возникают из-за недостатков в требованиях, при разработке и реализации или из-за изменений условий использования. 3) Характеристики функциональной надежности программного обеспечения включают в себя готовность и либо присущие ей, либо внешние влияющие факторы, такие как надежность и доступность (включая отказоустой­чивость и восстанавливаемость), безопасность (включая обеспечение конфиденциальности и целостность), при­годность для обслуживания, долговечность и техническую поддержку. Примечание — Во избежание противоречий термин «удобство использования» (4.2.4) определен, как подмножество качества при использовании, в состав которого входят эффективность, производительность и удовлетворенность.

> 4.2.6 _Защита, защищенность (security)_: Степень защищенности информации и данных, обеспе­ чиваемая продуктом или системой путем ограничения доступа людей, других продуктов или систем к данным в соответствии с типами и уровнями авторизации. Примечания. 1) Защищенность применима также и к данным при передаче в случаях, когда данные сохраняются непосред­ ственно в продукте или системе или вне их. 2) Жизнестойкость (survivability) (степень, в которой продукт или система продолжают выполнять свою мис­ сию, предоставляя основные услуги своевременно, несмотря на присутствие атак) обеспечивается восстанавли­ ваемостью (см. 4.2.5.4). 3) Защищенность, иммунитет (immunity) (степень устойчивости продукта или системы к атакам) обеспечива­ ется целостностью (см. 4.2.6.2). 4) Защищенность (security) вносит свой вклад в доверие (trust) (см. 4.1.3.2).

> 4.2.8 _Переносимость, мобильность (portability)_: Степень простоты эффективного и рациональ­ного переноса системы, продукта или компонента из одной среды (аппаратных средств, программного обеспечения, операционных условий или условий использования) в другую. Примечания. 1) Это определение адаптировано из (ИСО/МЭК/ИИЕЕ 24765). 2) Переносимость можно интерпретировать либо как присущее продукту или системе свойство продукта или
системы, упрощающее процесс переноса, либо как качество при использовании, предназначенное для переноса продукта или системы.

### Linux

1. Who is the inventor of Linux? Кто является изобретателем Linux?
```
a. ЛОЖЬ. Ричард Мэттью Столлман — основатель движения свободного ПО, проекта GNU, Фонда свободных программ и Лиги за свободу программирования.
b. ИСТИНА. Воодушевлённый прочтением книги Эндрю Таненбаума, посвящённой операционной системе Minix, Линус создал Linux — ядро операционной системы GNU/Linux, являющейся на данный момент самой распространённой из свободных операционных систем.
c. ЛОЖЬ. Э́ндрю Стюарт Таненба́ум (англ. Andrew Stuart Tanenbaum) (родился 16 марта, 1944 года) — профессор Амстердамского свободного университета, где возглавляет группу разработчиков компьютерных систем; защитил докторскую диссертацию по физике в Калифорнийском университете в Беркли. Известен как автор Minix (свободная Unix-подобная операционная система для студенческих лабораторий), книг по компьютерным наукам и RFID-вируса. Также является главным разработчиком пакета «Amsterdam Compiler Kit». Сам он считает свою преподавательскую деятельность наиболее важной[8].
d. ЛОЖЬ. Кен То́мпсон — пионер компьютерной науки, известен за свой вклад в создание языка программирования C и операционной системы UNIX.
```
1. Дать команду ```man ssh```.
1. Нажать клавишу ```q```.
1. Набрать ```pwd```.
1. ```ls```.
1. ```ls -l```.
1. ```mkdir test```.
1. ```rmdir test```.
1. Использовать команду ```cd ..```.
1. Набрать ```cd```.
1. ```cd Application\ Support```.
1. Набрать первые 3-4 символа названия и нажать ```Tab```.
1. ```clear```.
1. ```sqlite3 name_database```, ```.tables```.
1. ```> file```.
1. ```nano file```.
1. ```Ctrl+X```.
1. ```cat file```.
1. ```diff readme.md summary.md```.
1. ```cat file >> file_two```.
1. ```grep 'дымовое' *```.
1. ```df -h```.
1. Набрать ```ls -R > all.txt```

### SQL

1. ```SELECT yarn FROM company_yarn WHERE company = 'Семеновская пряжа';```
1.
1. ```SELECT yarn, Count(*) FROM company_yarn WHERE company = 'Пехорский текстиль';```
1. ```SELECT client.name_client, product.name_product FROM product INNER JOIN shop ON product.id_product = shop.id_product INNER JOIN client ON shop.id_client = client.id_client;```
1. решить и заполнить
1. решить и заполнить
1. ```DROP TABLE manandwoman```.
1. ```.show```, ```.headers ON```, ```.mode column```.
1. ```SELECT COUNT(*) FROM manandwoman;```.
1. ```SELECT gender, COUNT (*) FROM manandwoman GROUP by gender;```
1. ```SELECT * FROM manandwoman WHERE birthday < '2000-03-06';```.

27.02.2018