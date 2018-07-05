# Тестирование программного обеспечения

Подборка упражнений, задач и решений с доказательствами.

Вопросы:
1. [Which of the following statements BEST describes one of the seven key principles of software testing?](#isqtb1)
1. [Which of the following statements is the MOST valid goal for a test team?](#istqb2)
1. [Which of these tasks would you expect to be performed during the Test Analysis and Design phase of the Fundamental Test Process?](#isqtb3)
1. [Below is a list of problems that can be observed during testing or in production. Which one of these problems is a failure?](#isqtb4)
1. [Which of the following attitudes, qualifications or actions would lead to problems (or conflict) within mixed teams of testers and developers, when observed in reviews and tests?](#isqtb5)

### Which of the following statements BEST describes one of the seven key principles of software testing? <a name="isqtb1"></a>

Answer Set:

a) By using automated testing it is possible to test everything.

b) With sufficient effort and tool support, exhaustive testing is feasible for all software. 

c) It is normally impossible to test all input/output combinations for a software system.

d) The purpose of testing is to demonstrate the absence of defects.

Какое из следующих утверждений ЛУЧШЕ описывает один из семи ключевых принципов тестирования программного обеспечения?

Набор ответов:

a) Используя автоматизированное тестирование, можно протестировать все.

b) При наличии достаточных усилий и поддержки инструмента, полное тестирование возможно для всего программного обеспечения.

c) Обычно невозможно проверить все комбинации ввода / вывода для программной системы.

d) Цель тестирования - продемонстрировать отсутствие дефектов.

a) FALSE – Exhaustive test is impossible, regardless of it being manual or automated. (Section. 1.3; Principle #2)

b) FALSE – Exhaustive testing is impossible, regardless of the amount of effort put into testing (Section. 1.3; Principle #2)

c) TRUE – Principle #2 (Section 1.3) states: “Testing everything (all combinations of inputs and preconditions) is not feasible except for trivial cases”

d) FALSE – This statement is contradicting Principle #1(Section 1.3): Testing shows presence of defects: Testing can show that defects are present, but cannot prove that there are no defects.

a) ЛОЖЬ - Исчерпывающее тестирование невозможно, независимо от того, является ли оно ручным или автоматизированным. (Раздел 1.3, принцип № 2)

b) FALSE - Исчерпывающее тестирование невозможно, независимо от количества усилий, затраченных на тестирование (раздел 1.3, принцип № 2)

c) TRUE - Принцип № 2 (раздел 1.3) гласит: «Тестирование всего (все комбинации входов и предварительных условий) невозможно, за исключением тривиальных случаев»

d) ЛОЖЬ - это утверждение противоречит Принципу № 1 (раздел 1.3): Тестирование показывает наличие дефектов: Тестирование может показать наличие дефектов, но не может доказать, что дефектов нет.

### Which of the following statements is the MOST valid goal for a test team? <a name="isqtb2"></a>

a) To determine whether enough component tests were executed within system testing.

b) To detect as many failures as possible so that defects can be identified and corrected.

c) To prove that all possible defects are identified.

d) To prove that any remaining defects will not cause any failures.

Какое из следующих утверждений является наиболее достоверной целью для команды тестировщиков?

a) Определить, были ли выполнены достаточные компонентное тестирование в рамках системного тестирования.

b) Обнаружить как можно больше дефектов для идентификации и исправления

c) доказать, что идентифицированы все возможные дефекты.

d) доказать, что любые оставшиеся дефекты не вызовут никаких сбоев.

a) FALSE – Component testing is not part of System testing. (Section 2.2.1 and 2.2.3)

b) TRUE – This is the main role of a test team. (Section 1.2, objectives, 1. dot)

c) FALSE – Principle #1 states that exhaustive testing is impossible, so one can never prove that all defects were identified.

d) FALSE – To make an assessment whether a defect will cause a failure or not, one has to detect the defect first. Saying that no remaining defect will cause a failure, implicitly means that all defects were found. This contradicts Principle #1.

a) FALSE - тестирование компонентов не является частью системного тестирования. (Раздел 2.2.1 и 2.2.3)

б) ИСТИНА - Это основная роль тестовой команды. (Раздел 1.2, цели, 1. точка)

c) ЛОЖЬ - Принцип № 1 гласит, что исчерпывающее тестирование невозможно, поэтому невозможно доказать, что все дефекты были идентифицированы.

d) FALSE. Чтобы оценить, приведет ли дефект к сбою или нет, сначала необходимо обнаружить дефект. Говоря, что никакой оставшийся дефект не приведет к сбою, неявно означает, что все дефекты были обнаружены. Это противоречит принципу №1.

### Which of these tasks would you expect to be performed during the Test Analysis and Design phase of the Fundamental Test Process? <a name="isqtb3"></a>

a) Defining test objectives

b) Reviewing the test basis

c) Creating test suites from test procedures

d) Analyzing lessons learned for process improvement

Какую из этих задач вы ожидаете выполнить на этапе Анализа и Проектирования Тестов Основного Процесса Тестирования?

a) Определение целей тестирования

b) Проверка основы тестирования

c) Создание наборов тестов из процедур тестирования

d) Анализ извлеченных уроков для улучшения процесса

a) FALSE – this activity is performed during “Test Planning” phase (section 1.4.1, sentence 1)

b) TRUE – this activity is performed during “Test Analysis and Design” phase (section 1.4.2, 1. dot))

c) FALSE – this activity is performed during “Test Implementation and Execution” phase (section 1.4.3, 3. dot)

d) FALSE – this activity is performed during “Test Closure Activities” phase (section 1.4.5; 6. dot)

a) FALSE - эта деятельность выполняется во время фазы «Планирование тестирования» (раздел 1.4.1, предложение 1)

б) ИСТИНА - эта деятельность выполняется во время фазы «Анализ и проектирование» (раздел 1.4.2, 1. точка))

c) FALSE - эта операция выполняется во время фазы «Реализация и Выполнение Тестов» (раздел 1.4.3, 3. точка)

d) FALSE - эта активность выполняется во время фазы «Действия по Завершению Тестирования» (раздел 11.4.5, 6. точка).

### Below is a list of problems that can be observed during testing or in production. Which one of these problems is a failure? <a name="isqtb4"></a>

a) The product crashed when the user selected an option in a dialog box.

b) One source code file included in the build has the FALSE version.

c) The computation algorithm used FALSE input variables.

d) The developer misinterpreted the requirement for the algorithm.

Ниже приведен список проблем, которые можно наблюдать во время тестирования или производства. Какая из этих проблем является отказом? a) Программа "упала", когда пользователь выбрал опцию в диалоговом окне. b) Один файл исходного кода, включенный в сборку, имеет ОШИБОЧНУЮ версию. c) Алгоритм вычисления использует ОШИБОЧНЫЕ входные переменные. d) Разработчик неправильно истолковал требования к алгоритму.

a) TRUE – A failure is an external manifestation of a defect. A crash is clearly noticeable by user

b) FALSE – This type of mistake will not necessarily lead to a visible or noticeable failure. For example: if the changes in the new version of the source file are only in the comments.

c) FALSE – Use of a FALSE input variable will not necessarily lead to a visible or noticeable failure. For example: if no one uses this specific algorithm; or: if the FALSEly used input variable had a similar value as the TRUE input variable; or: if no one is using the FALSE result from the algorithm. “Defects in software, systems or documents may result in failures, but not all defects do so.” (Section 1.1.2; 1. Par.; 3. dot)

d) FALSE – This type of mistake will not necessarily lead to a visible or noticeable failure. For example: if no one uses this specific algorithm.

a) ИСТИНА - отказ - это внешнее проявление дефекта. отказ (failure): Отклонение компонента или системы от ожидаемого выполнения, эксплуатации или результата. [Fenton]. Краш ясно заметен пользователем

b) FALSE. Этот тип просчета (mistake) не обязательно приведет к видимому или заметному сбою. Например: если изменения в новой версии исходного файла находятся только в комментариях.

c) FALSE - Использование ЛОЖНОЙ входной переменной не обязательно приведет к видимому или заметному сбою. Например: если никто не использует этот конкретный алгоритм; или: если ОШИБОЧНАЯ входная переменная имела такое же значение, как ИСТИННАЯ входная переменная; или: если никто не использует ЛОЖНЫЙ результат из алгоритма. «Дефекты в программном обеспечении, системах или документах могут привести к сбоям, но не все дефекты делают это» (раздел 1.1.2, 1. Par., 3. точка)

d) FALSE. Этот тип просчета (mistake) не обязательно приведет к видимому или заметному сбою. Например: если никто не использует этот конкретный алгоритм.

### Which of the following attitudes, qualifications or actions would lead to problems (or conflict) within mixed teams of testers and developers, when observed in reviews and tests? <a name="isqtb5"></a>

a) Testers and developers are curious and focused on finding defects.

b) Testers and developers are sufficiently qualified to find failures and defects.

c) Testers and developers communicate defects as criticism of people, not as criticism of the software product.

d) Testers expect that there might be defects in the software product which the developers have not found and fixed.

Какие из следующих установок, квалификаций или действий могут привести к проблемам (или конфликту) в смешанных командах тестировщиков и разработчиков, когда они наблюдаются в обзорах и тестах?

a) Тестеры и разработчики любопытны и сосредоточены на поиске дефектов.

b) Тестеры и разработчики обладают достаточной квалификацией для обнаружения сбоев и дефектов.

c) Тестеры и разработчики связывают дефекты как критику людей, а не критику программного продукта.

d) Тестеры ожидают, что в программном продукте могут быть дефекты, которые разработчики не нашли и не зафиксировали.

a) FALSE. There is no situation which leads to conflict. Testers and developers should be focused on finding defects

b) FALSE. This is a preferred situation, there is therefore no problem.

c) TRUE. According to the syllabus, testers and developers should cooperate, and communicating defects as criticism of people would lead to conflict inside the team. (Section 1.5.9; Par. 9; 2. dot)

d) FALSE. The tester’s role in the team is finding defects in the software product that the developers have not found and fixed.

a) ЛОЖЬ. Нет ситуации, которая ведет к конфликту. Тестеры и разработчики должны быть сосредоточены на поиске дефектов

б) ЛОЖЬ. Это предпочтительная ситуация, поэтому нет проблем.

c) ИСТИНА. Согласно программе, тестеры и разработчики должны сотрудничать и сообщать о недостатках, поскольку критика людей приведет к конфликту внутри команды. (Раздел 1.5.9, пункт 9, 2. точка)

d) ЛОЖЬ. Роль тестировщика в команде заключается в обнаружении дефектов в программном продукте, которые разработчики не нашли и не зафиксировали.

25.03.2018. Перейти на [Главную страницу](./)