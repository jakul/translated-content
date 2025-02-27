---
title: Compile
slug: Glossary/Compile
tags:
  - Глоссарий
translation_of: Glossary/Compile
original_slug: Глоссарий/Compile
---
Компиляция - это процесс преобразования компьютерной программы, написанной на данном [языке](/ru/Glossary/Computer_Programming), в эквивалентную программу на другом языке. Компилятор - это программа для выполнения этой задачи. Иногда эту задачу называют также "assembling" или "build", что, как правило, свидетельствует о том, что выполняется не только компиляция, например, упаковка в двоичном формате.

Обычно компилятор преобразует язык более высокого уровня, такой как C или [Java](ru/Glossary/Java) который понимает человек, в машинный язык, такой как ассемблер, который понимает процессор. Некоторые компиляторы, которые переводят между языками схожего уровня, называются транспайлерами или кросс-компиляторами, например, для компиляции с TypeScript на [JavaScript](ru/Glossary/JavaScript). Они считаются инструментами производительности.

Большинство компиляторов работают либо перед исполнением (AOT), либо во время исполнения (JIT). Как программист, вы обычно вызываете AOT-компиляторы из командной строки или из {{Glossary("IDE")}}. Самый известный "gcc" - это один из примеров.
JIT компиляторы обычно прозрачны для вас и используются для повышения производительности. Например, в браузере: Firefox' [SpiderMonkey](/ru/SpiderMonkey) JavaScript Engine имеет встроенный JIT, который скомпилирует JavaScript на сайте в машинный код, пока вы его просматриваете, чтобы он работал быстрее. Такие проекты, как [WebAssembly](/ru/WebAssembly), работают над тем, чтобы сделать это ещё лучше.

## Смотрите также

### Общие сведения

- [Компилятор](https://ru.wikipedia.org/wiki/Компилятор) - Wikipedia
- The [GNU Compiler Collection (GCC)](https://gcc.gnu.org)

### Обучающие ресурсы

- [Введение в компиляторы](https://medium.com/basecs/a-deeper-inspection-into-compilation-and-interpretation-d98952ebc842)
- [Большой список учебных материалов на StackOverflow](http://stackoverflow.com/a/1672/133203)
