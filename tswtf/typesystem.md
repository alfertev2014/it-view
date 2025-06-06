# Что есть система типов

Язык программирования представляет собой *формальную систему*, состоящую из **спецификации** и **реализаций**, на которые могут опираться **инструменты**. Спецификация языка - это **синтакис** исходного кода и его **семантика**. Реализация может представлять собой *интерпретатор* с некоторой средой исполнения или *компилятор*, который транслирует исходный код в код для целевой среды исполнения. Инструментами, сопровождающими язык, являются различные *анализаторы* кода, *отладчики*, *IDE*.

Для обсуждения систем типов важна будет семантика. В формальном виде, семантика - это набор правил, определяющих смысл выражений исходного кода. Эти правила описывают процесс вычисления выражений, порядок исполнения действий и другие правила, тем или иным образом раскрывающие смысл выражений.

JavaScript имеет спецификацию ECMAScript, где строго определены синтаксис и семантика различных версий языка и поведение его стандартной библиотеки. **TypeScript не имеет спецификации в формальном виде.** Подразумевается, что смысл исходного кода на языке TypeScript определяется реализацией компилятора tsc (исходный код которого громоздкий и не самый простой). Это ещё одна проблема TypeScript, которая не позволяет легко рассуждать о языке, пристально изучать его, разрабатывать для него инструменты и альтернативные реализации.

Целевая среда исполнения с которой связана реализация языка программирования, тоже может рассматриваться в виде спецификации её поведения отдельно от деталей реализации, которые не интересны при рассуждениях. Предполагается, что реализация среды исполнения соответствует её спецификации. Семантика языка программирования, реализация которого предполагает использование определённой среды исполнения, может быть выражена через её спецификацию.

Целевой средой исполнения для TypeScript является среда исполнения JavaScript-кода, например, браузер или Node.js. Можно было бы описать семантику TypeScript как отображение на семантику JavaScript. При желании можно было бы написать формальную спецификацию TypeScript и как она соотносится с JavaScript, но разработка TypeScript такая активная, что этим никто не занимается и считается нецелесообразным. Тем не менее, некоторая подразумеваемая спецификация, зашитая в компилятор, у нас как бы есть.

Теперь вспомним, что исходный код пишется для решения задач, алгоритм которых можно сформулировать на своём предметно-специфичном языке спецификаций. Доказательство того, что результирующее поведение программы будет соответствовать формальной спецификации решения задачи, называется *верификацией*.
