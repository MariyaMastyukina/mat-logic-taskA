# mat-logic-taskA
**Task A. Разбор утверждения**

  * Имя входного файла: стандартный ввод
  
  * Имя выходного файла: стандартный вывод

  * Ограничение по времени: 2 секунды

  * Ограничение по памяти: 256 мегабайт

На вход вашей программе дается утверждение в следующей грамматике:
1. <Файл> ::= <Выражение>
2. <Выражение> ::= <Дизъюнкция> | <Дизъюнкция> ‘->’ <Выражение>
3. <Дизъюнкция> ::= <Конъюнкция> | <Дизъюнкция> ‘|’ <Конъюнкция>
4. <Конъюнкция> ::= <Отрицание> | <Конъюнкция> ‘&’ <Отрицание>
5. <Отрицание> ::= ‘!’ <Отрицание> | <Переменная> | ‘(’ <Выражение> ‘)’
6. <Переменная> ::= (‘A’ . . . ‘Z’) {‘A’ . . . ‘Z’ | ‘0’ . . . ‘9’ | ‘'’}

Имена переменных не содержат пробелов. Между символами оператора ‘->’ нет пробелов. В
остальных местах пробелы могут присутствовать. Символы табуляции и возврата каретки должны
трактоваться как пробелы.

Вам требуется написать программу, разбирающую утверждение и строящую его дерево разбора,
и выводящую полученное дерево в единственной строке без пробелов в следующей грамматике:
1. <Файл> ::= <Вершина>
2. <Вершина> ::= ‘(’ <Знак> ‘,’ <Вершина> ‘,’ <Вершина> ‘)’ | ‘(!’<Вершина>‘)’ | <Переменная>
3. <Знак> ::= ‘->’ | ‘|’ | ‘&’
4. <Переменная> ::= (‘A’ . . . ‘Z’) {‘A’ . . . ‘Z’ | ‘0’ . . . ‘9’ | ‘’’}

*Формат входных данных*

В единственной строке входного файла дано утверждение в грамматике из условия. Размер
входного файла не превышает 100 КБ.

*Формат выходных данных*

В единственной строке выходного файла выведите дерево разбора утверждения без пробелов.

**Task C. Теорема Гливенко**
* Имя входного файла: стандартный ввод
* Имя выходного файла: стандартный вывод
* Ограничение по времени: 15 секунд
* Ограничение по памяти: 512 мегабайт

На вход вашей программе дается корректное доказательство утверждения α в классическом
исчислении высказываний. Доказательство записано с использованием грамматики из предыдущего
задания.

Вам требуется построить корректное доказательство утверждения ¬¬α в интуиционистском исчислении высказываний.

*Формат входных данных*

Во входном файле задано доказательство утверждения α в классическом исчислении высказываний. Размер входного файла не превышает 5 КБ.

*Формат выходных данных*

Файл должен содержать корректное доказательство утверждения ¬¬α в интуиционистском исчислении высказываний в том же контексте, что доказательство α во входном файле.