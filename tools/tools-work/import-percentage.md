---
title: Экспорт/Импорт - Импорт процента
description: 
published: true
date: 2025-09-21T11:49:57.941Z
tags: 
editor: markdown
dateCreated: 2025-06-27T11:42:36.549Z
---

### **Импорт процента**

Инструмент позволяет импортировать в элементы модели процент выполнения работ из Excel. Например, его можно использовать для оценки прогресса выполнения инженерных сетей с разбивкой по этажам, квартирам или по помещениям. Это позволяет более точно контролировать прогресс работ и оценить степень завершенности проекта.

1\. Нажмите на вкладке SIGNAL PRO на панели Экспорт | Импорт ➤ Импорт процента

![image-1688029692605.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeSboCvSDWJsRPpyD8DfLylK8E9mfKnVj1bs4ATHO2lynbPB7czKUaBZsveySW14b_VuJ7vuQUmIQkN76D-I8FQm-vDTshsSs0am4MuF0-1694IwzTk-mo4rqTP6YkBdJOZHNTyqtNxwzwO_lSV?key=HN--DieFzm94qLpYmm381Q)

2\. В открывшемся окне выберите файл формата Excel и нажмите “Открыть”

![image-1688029717377.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeyw2-IX1hKqJOiSXh8zf7wPgZD_8SXPjXgHRqJfR4DE-v5ZWshW9vuQpZu-rngwl62Zd2HNK_WYgmeSoo2xCh2gnnL_HdXyBfkJuIaH2nF3SIjj2NXUS-xJ8vsgaYjXcMWVI9OIzD5Rax_51IBeQ?key=HN--DieFzm94qLpYmm381Q)

Структура Excel выглядит следующим образом:

![image-1688029735806.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfKxMtEODfg1cZ2U1qZ9FOjI0fxqfobBQ3y2xHtKrPqG7JIo3TBr7fFO6Wbx41LkOIR6DyMYpaEPyYKgGraA7YrgIwU1FQBDdUiT5kaCGr4lhQlxU7VYf9_ZusAtshLNBCYte51Zja029JTfJuZ4A?key=HN--DieFzm94qLpYmm381Q)

-   Первые три столбца (A,B,C) отвечают за свойства и их значения, по которым плагин будет искать элементы, в которые требуется вписать процент. Свойства записываются в виде “Категория-Свойство”. Не обязательно все три столбца могут быть заполнены.

![image-1688029749243.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc11dseJn0Bl2xScET6Oqvj8ZJhf8hTl6Ub8r2JD31f6UZsyKbYAFz5xFTdnMqaqjsmR77FMb5xxwZzTX2k98ieR2F-2XK093uj6ythcWPSnuveaWFf9OWmeRGTiQt1yxFsrebVaX4uUIZvY8MF?key=HN--DieFzm94qLpYmm381Q)

-   В последующих столбцах указываются виды работ и процент выполнения. Данные значения плагин запишет в элементы. Если у вида работ отсутствует КОД , то указывается только наименование работы, например, Розеточная сеть. Если у работы присутствует КОД, то указывается так: КОД “пробел” - “пробел” НАИМЕНОВАНИЕ. (Например, 4.1.1 - Монтаж ОВ1).

3\. После импорта в свойствах элементов во вкладке “SIGNAL” появляется соответствующее свойство “P\_{Вид работы}”, а также значение процента выполненной работы

![image-1688029773683.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXexk-syYlThmDK8ZJXLDUXLRa91MGrbdYpatTD5dJ8O2h9v8GrQrXsJ5SDFq-K6G0MP6m6MsnlKp7Hwk-JbOA6m8aLt_1PjG8cQnEPHGC6YWHwtnU1PiOs-vd8zDr3kuTWKVVl8BST5c8LogGwQyA?key=HN--DieFzm94qLpYmm381Q)

4\. Для того чтобы раскрасить элементы по проценту воспользуйтесь инструментом [_“Раскрасить”_](https://wiki.sgnl.pro/app/page/1sKveQeB11oVjviyFR_BPtaX1OzUCGXkbAwkLJ_8uMJ8)

![image-1688029788328.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfbMj8BMK1d6LFnZ8BVbvnJYhKmLtFRTfqLuEI8AGaxqQxR3t3vgFLI0W8TUHxqsdqz1bFViVqMrs8-Ga2fegJP9QjsZkoH32vk4qMw4WjPeApLpvUJQU1JG3dlPg2nU7huikb04mRzVkEQ7-PUCg?key=HN--DieFzm94qLpYmm381Q)