# Причинно-следственные диаграммы для проектирования тестов

Препятствие - разбиение данных на классы эквивалентности и анализ граничных значений не позволяют эффективно протестировать комбинации входных условий. Появляется ощущение чрезмерной произвольности выбора входных условий, халтурно выполненной работы, соблазн превысить бюджет тестирования и продолжать тестирование. Возможный вариант устранения препятствия - использовать систематический способ выбора подмножества входных условий. Например найти высокорезультативные тесты при помощи метода причинно-следственных диаграмм (cause-and-effect diagrams). Здесь возникает еще одно препятствие - причинно-следственная диаграмма представляет собой отдельный язык в виде "нотации" для понимания которой по мнению Гленфорда Майерса "никаких знаний электроники, кроме понимания правил булевой алгебры (то есть умения работать с логическими операторами and, or и not), не требуется". Между тем выглядит нотация причинно-следственных диаграмм специфично, если не отталкивающе.

##### Какие этапы необходимо пройти для построения тестов методом причинно следственных-диаграмм?

"Искусство тестирования программ", Гленфорд Майерс, Том Баджетт, Кори Сандлер. Третье издание, издательство "Далектика", 2015 год. Глава "Проектирование тестов", 82 страница:

1. Спецификация разбивается на части, с которыми легче работать. Это приходится делать, поскольку причинно-следственные диаграммы для больших спецификаций разрастаются до чудовищных размеров. Например, при тестировании интернет-магазина в качестве одной из таких частей может быть взято описание операций выбора и верификации отдельного элемента каталога товаров, помещаемого в корзину покупателю. При тестировании дизайна веб-страницы можно выбрать одиночную ветвь меню или даже меньшую навигационную цепочку.
2. В спецификации определяются причины и следствия.
3. Семантическое содержание спецификации анализируется и преобразуются в булев граф, связывающий причины и следствия. Полученный граф называется причинно-следственной диаграммой.
4. Диаграмма снабжается примечаниями, задающими ограничения и описывающими комбинации причин и (или) следствий, реализация которых невозможно из-за синтаксических или внешних ограничений.
5. Путём методичного прослеживания состояний условий диаграмма преобразуются в таблицу решений с ограниченными входами (limited-entry desicion table). Каждый столбец таблицы решений соответствую тесту.
6. Столбцы таблицы решение преобразуются в тесты.

##### Что такое причина, следствие в причинно-следственных диаграммах?

"Искусство тестирования программ", Гленфорд Майерс, Том Баджетт, Кори Сандлер. Третье издание, издательство "Далектика", 2015 год. Глава "Проектирование тестов", 82 страница:

Причина - это отдельное входное условие или класс эквивалентности входных условий. Следствие - это выходное условие или преобразование системы (долговременное воздействие, которое входное условие оказывает на состояние программы или системы). Например, если выполнения транзакции приводит к обновлению записи в файле или базе данных, то внесённые изменения является преобразованием системы, тогда как сообщения системы об этом было по выходным условием.

##### Как найти причины и следствия?

"Искусство тестирования программ", Гленфорд Майерс, Том Баджетт, Кори Сандлер. Третье издание, издательство "Далектика", 2015 год. Глава "Проектирование тестов", 82 страница:

Причины и следствия определяются путём последовательного (слово за словом) чтения спецификации и подчеркивания тех слов или фраз, которые описывает причины и следствия. Каждой причине и каждому следствию присваивается уникальный номер.

##### Что представляет из себя базовая нотация причинно-следственных диаграмм?

"Искусство тестирования программ", Гленфорд Майерс, Том Баджетт, Кори Сандлер. Третье издание, издательство "Далектика", 2015 год. Глава "Проектирование тестов", 83 страница:

Каждый узел диаграммы может находиться в двух состояниях: 0 или 1, где "0" представляет состояние "отсутствует", а "1" представляет состояние "присутствует".

![](https://lh3.googleusercontent.com/SoYJ8GHvssiFvC36hM8CMXOi8giyuwklNwVdQJoP-Qh79RA_wiRsktghPeK9AihzcyTU3kDY3gqJ7xMvkWMD5kjAVOqx47uLDSNNXZo4fzvPQdZyIYUEErxl5rXXlgXwsNPLXtq_xRvi0pcyWJXP8OeZyahiAf2gYRTsjodAQzikMD9hgr7KW_8UyKUneQBSqtHvncWu0-BNLqJh7q3JJDvI-KAqdpRgeewgwIkO_-GVDPMZ3RiVPPjz-asrRCTyMpl1-_NCGR9fEyslubm0-vxcrRue5tmzS_oRn-eYSm1FtKj_y0PBej1nnf1x7Bw5CcQJ0lTk7KVfg6_FDvINGi25c7OnoGrCl8ESS4I4vA-lr7dVzjATe1mG439549HnoRf1YH4QGh5qfkU81C3p0DFIO-3Fcll-aTxYDU76JeSrve4Zk4q04M9f8HPZwZDg-bnzBaitQBV9CWANo41ZwOODEzC0IizNLUQqlXCHbsZieAGKb3dhFrkCYNwLn_REPOoaeqa0jJlzTHw25fvsqkJqEMiS_RuhwIcw9HkhppT12PQuE2AipL6VPW3EaAsPLo1nkci9_KWLMWxxNemVpOpPZhzm0cPkTAJuRVjvoaUpXITzMHKCHHxKQjzbET2yiQ6bZ3IuRLdbvz0mhAX6CS12AF_bhFHcwucgOYWv92ZWI3I9wBL-ZBP4x66tOAKIpTYTWjHKTrQd6Lt3B39kb6G9=w719-h179-no)

Функция *тождество* устанавливает, что если *a* равно 1, то и *b* равно 1; если *a* равно 0, то и *b* равно 0.

![](https://lh3.googleusercontent.com/R9SsOILn4I9V6G9f-_xA8YLGHTy4VtQaJR316uBK3nv-lWhbVXYC1h8zE8u5gtREF1laC24SX94pN1IoeSjfsO-i7j9sVYFcoZH74xk6gMH-Fcu1dUP7SC7QFhZgTyJVcgV7peaRmPo9nj_Zm3RU6ZBWbKLXGoL5AZxoBqxjkMMNv7g-V1cU5yeWbSRh_NQm6dsfASx_tyOFadgwo8H4XEVvNdJPivwfg5tuu7quHq2CtTgo7Miin7VjwwBDhvXjH54YKy6039pHycNxFZO2fgU4HJSZ6OmNQNEOcc4TGO_Xkgvdn3pAV5rcIyIRtFtGSnXxxrbrFSdU_6TiTlRCXgrF8nJUXxdYiaabCobUtBleTG881Kg710FmPgOmvkZXqf9lz-JJ-3w4F6RrMjbhrhFZcg5a7Kgzx-s0-uCy8Flvz2_VYB3mdbCHZI9zl4tvUfpjWvuefkflwk19Uuf5HrgVxN4FYwA9dF-yxaH4IgO5x6Xa41TkrcKT6IUSoEXJDU5FUXTEjmf5CBpgHaBkJfBCwDCHshkSDoFE36eOcQKYHmecIP_mFsMu-yRIDhNer9uQuhGbF4uejZ3WJkoKoyWZcHYO_lssaMp05UXfnrXgG7M1ghoJljuKpkVQPk9C8iYA-L8VnernPSGhnWsHu5MjORWqIu-5dw_Ksa9y9vfr9V1wfUZFfN4uv0C_oJHv8pML_Ptuu-dGjCKp-GkaLKqf=w630-h184-no)

Функция not устанавливает, что если *a* равно 1, то *b* равно 0; если *a* равно 0, то *b* равно 1.

![](https://lh3.googleusercontent.com/zanrSb8_KQFER_VyVFtEu2FplpEpv6JgJlukZLHwziDCvUAKDwixSstlQEGzbdPY8DL9z5PcjQ6oSa5x9tVWek3Szo-LkWgLmJmdBQoC7hbvtBwU_PJwUSv5ObuQqffQhKu9epYCRHoNyEgqzko-tJPKTYR5396fNlHs1y6vTS9Tgp1Xj-cPrIxAMmfZhPuyrZr5BckWPA1laZqrfJEBSWnMBxRCPSEun-vjXVNnZmvKZ3NbO9U9ly-IGkDqaIg81CaRiGbTHF7Lj28G7YV5lypUPl-ZTleTePO1lGif4MNz7qQBF3cpeWFZQgIbeSYOE36ZAawpPmmJdmVD9kvr2agO5tLla-tt7zBsov3URZ8DyCYgk0zH_5GgpMYcA8_9RccIuCuVy-FOCcaYn0vvKoF5lbQvrPadpi0FUjbHbXlHMcYkeEpkD9MkRGzOoTQXePaTzqU8KUJ7MA4IlfpJXuaNvUCY4EhjqEQW3LsLvBymjYFpMZT_moh788_1Zbk2cFfyRrQbTcB9HmzQ3jys_maUy_bZPqETWGzIfaCAzUjiRkuNLUN0nhQDe07sWhyms6FuZA20B1Pv0UHZDFuApzPWYVzYxGQGrcSkq_zTwSE1Lp-EYkG42jp1XknZWn5lmH4WNkKQJ-PP4PTJbK9juyVNlbJP9BUQnzBmTIZBg9lVAjzXUAuOP3FgvWqlRufgIldNogSUpjQVomO-4mHZl5PN=w444-h546-no)

Функция and устанавливает, что если и *a*, и *b* равно 1, то *c* равно 1; если и *a*, и *b* равно 0, то *c* равно 0.

![](https://lh3.googleusercontent.com/Ilms_ZRoDg71uJWXYusuXA8CoFNhPzWhJ3DeI49oQcK9fULIwUksx3Pywy7PDIDwy0jEHku2cnjlgCHS-aa8yOWNsKf1B0MwWvsYJiV3lhEd3o7jUwKvViClJ0Qr77slHZhtWH6Cy5Dw00M5CqTiLQUYNvTEdy69RiqXmHJyDaKLxKaooz_Ydrzpe5ndaTYxvIuGA7lteeEHYaqcsP35Y7b5q8XhipOe-lzz1RniSWN99C0Jirm5bXky_T8CJkNvW5STeqGuiyEXoQ5hmuotlTsFlG1UatFFcTD861025BZ6wWXbwmTgkvWBMM7-Ynwi_EKLfbLCYlaETq97_V1wajyxduFb5ZvYB-M1Q70rc4BunZ8C-s7UKwuJXFeEjQl7qcZ3vNzXj6ANaroRE80OOnlFSrAfiKzP6wvgDlLm7jciio4_uVRPO8P51taqAQ2RLIanfpC0TpinsKbipT8yDdqni5mcgd8XPowGivaSlqSW533UTvEZ2Uni_YF0jxhPpUz4mA8Eb8tio5esrH45tkISWcTmeHaxPWDs0LrJcR5H-Xlq15g8nXn5cYTu1geutmtt1J4wCe91KB6FsYk8pJiWK22YdpGlIE13HqCcY_I89SHVQeZz9NsEgY-Ob-FWNPdcW_s1rQErZKlguJRCwaVZTZklsddKqASCSqexkB05Mg-Ikc0KlIHhPUpf4a3IUpY09mRWLFB62pVbKdoNzHvq=w418-h542-no)

Функция or устанавливает, что если *a*, или *b*, или *c* равно 1, то *d* равно 1; если *a*, или *b*, или *c* равно 0, то *d* равно 0.

##### Какое число входов могут иметь функции в нотации причинно-следственных диаграмм?

Функция *тождество* и функция *not* могут иметь по одной точке входа. Функции *or* и *and* могут иметь любое число входов.

##### Как работает базовая нотация, используемая в причинно-следственных диаграммах на примере конкретного пункта спецификации?

Страница 83-84:

Символ в колонке 1 должен быть буквой "А" или "В", а символ в колонке 2 - цифрой. В этом случае файл обновляется. Если первый символ некорректен, то выводится сообщение Х12, а если второй символ не является цифрой - сообщение Х13.

Здесь причинами являются:

- 1 - символ в колонке 1 является буквой "А";
- 2 - символ в колонке 1 является буквой "В";
- 3 - символ в колонке 2 является цифрой,

а следствиями:

- 70 - файл обновляется;
- 71 - выводится сообщение Х12;
- 72 выводится сообщение Х13.

![](https://lh3.googleusercontent.com/6Pt5qpdPgZApH5g2L3D48AmhgaJq8exj5Kz_ZHo0LUj__RZTlQQQhoBVJkfk8GQ4uDprfKUTqr9kQnRhkt-eT9yQgovPT0X5up18j9JPJubBFKfQ7nBqM48Nsug7NvQF1npdD9k2EFnsHlvDe83AskUkut11IMKl3DxPdv60lFjm7r7KiTh3f__rcyyrwOkqH21siUaj6xTUr_kGOjPXl54Z3rrbF9v7Gf2s8sIafH1nKNnpP0cnDF8DvuKNzVWIIw5R8y1R-makRlhE3PA9UtMFv_lJ9ylGazb8RQ--GO-tg2bmJSK5mp31VM8jpegrNgLguF8LzRBEqoTrQjUt0gA_srkzNNC_AXIOXYlmr2PZKW_kPxXVydC_hAxHh9XMloiPhNFQegK5r_sNaeWtlLNDqx9RFGz29PogRcmFZ0YKXBV1GcmyZUfz1elKZ7zYC6zLpIR9GP6yUvpDkIKPZF9EkciTv4y7FwiXH7d1zbAR_J7QADb_AvONY2-vibDZyB3vF4JZkvJ0MTFftULPZP9Sa7PPWP1NXpC-X7q_ZrmaVtlG6zS4YomLovtKCPPDx2OcKnEvcwmuom2YBDzpa_go413vmQknSmD2-PTZE8jzDVMi97cg-fuZhiC5VMbcgaaXlT_fM527wyj8g8LPiEwSL6KNRbiOVVsyptSVnP1tpDDvVpXCG44YmlAZFFRBuV0Xt1XZlzcSHkrDP86hYJ-Y=w718-h362-no)

Причинно-следственная диаграмма для данного примера показана на рисунке 4.6. Обратите внимание на создание промежуточного узла 11. Дабы убедиться в том, что диаграмма действительно представляет данную спецификацию, необходимо поочерёдно задавать все возможные состояния причин и проверять, принимают ли при этом следствия корректные значения. Для читателей, знакомых с логическими диаграммами, на рисунке 4.7 приведена эквивалентная логическая схема.



##### Появившиеся вопросы на которые пока не могу дать ответа

1. Что такое семантическое содержание спецификации?
2. Что такое булев граф?
3. Что за синтаксические или внешние ограничения на причинно-следственной диаграмме?
4. Чем таблица решений отличается от таблицу решений с ограниченными входами (limited-entry desicion table)?
