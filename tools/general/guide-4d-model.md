---
title: Инструкция по работе с 4D моделью
description: 
published: true
date: 2025-09-18T14:04:53.655Z
tags: 
editor: markdown
dateCreated: 2025-06-26T21:33:49.223Z
---

Данная инструкция предназначена для специалистов компании Signal по работе с 4D-моделью на основе проектных моделей и календарного графика строительства Microsoft Project.

## 1\. Создание файла Revit с разбивкой объекта

**Исходные данные**

1.  Проектная модель в формате Revit.
2.  Календарный график строительства Microsoft Project

**Инструменты**

-   ПО Autodesk Revit, Navisworks Manage, Microsoft Project, Excel;
-   Плагины BIMreport для Navisworks Manage;
-   Плагины Signal для Autodesk Revit;
-   Скрипты [*Dynamo*](https://wiki.sgnl.pro/app/page/1pnDCjhrT3TrMauPyd5LY2kUQojPrQ4pN?usp%3Dsharing)*;*
-   Revit-файл для копирования [](https://wiki.sgnl.pro/app/page/1ab-yNz1DcDSAjytlvURwqNbuYHToQSgQ/view)[**"W\_Спецификации для копирования"**](https://acc.autodesk.com/docs/share/projects/5e8469a3-9d9c-4f47-ad48-33dc8cf120cf/files?shareGroupId=33980b0c-491a-461b-aa75-94d40fd1b65e);

Скачайте по ссылкам необходимые файлы скриптов Dynamo и файл проекта для копирования спецификаций в формате .rvt.

**Создание файла**

1.  В Autodesk Revit создайте проект на базе строительного шаблона и подгрузите связью проектную модель.
2.  Создайте формообразующие с учетом местонахождения групп элементов (корпус, секция, этаж)

![1.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcwJMbKZSYEuFoHpdExIHiiqN_A4NWVKfW1HsJYHYkj-0b011GUvBelh8QOK2aWJtwlKSppQ8JggOSzmCjuGcZl4OvzwdSUkM7ahYPDgZawB8q9pZvcWjJVTJHj6w4mMIOkpzRxN18Lq50oDqfdKA?key=1zAn9q4w8I5y0ntdpe0saA)

![2.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfzADMDQ494QZ4hOjafUrMD6QuyY5S7HNsLt21ES8C0bvXpgX70rSIIE03Wj03idJc7fbuwYsr3w5IPyp4QOsCLUCiKVKZBZBfDGbWUiSvDXH8zhYh7gJvR7Wjqn9uMBIMhDhvGTNM1JRuRsQivaw?key=1zAn9q4w8I5y0ntdpe0saA)

![3.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd7ZRXVMsI2_KMd1QdyXNkHeYGzmZ4KIZfoToDwx9356k5SybJxDbUXnZvQjvc-K42hYQ4CqHDjuXNT4nF5z1e7ij03oD3tHenC-AWx4T560gDoLJdu6BndRASzOp-10ghxzuDK0LdP-KgHankweQ?key=1zAn9q4w8I5y0ntdpe0saA)

Копируйте формы на типовые этажи, нажав кнопку "Копирование" и создайте для нетиповых этажей новые элементы формы:

Важно: каждый формообразующий элемент должен находиться по высоте в пределах этажа, по ширине и длине - в пределах корпуса, к которому он будет относиться. \[Количество формообразующих объекта\] = \[Количество этажей секции 1\] + \[Количество этажей секции 2\] +...+  \[Количество этажей секции n\]. Но если во всех секциях одинаковое количество этажей, то можно создать формообразующую на все секции, а потом, при записи параметров, менять параметр “Секция”.

Структуры разбивки объекта могут быть различными для моделей дисциплины АР, КР и ИОС. Так, например, в один пакет модели АР попадает пол этажа который ниже отметки этажа и вертикальные конструкции данного этажа (правило стакана). В пакет КР же попадают вертикальные конструкции этажа и перекрытие выше текущего этажа (правило перевернутого стакана). Также имеется разбивка для фасадов, которая идет снизу до верху, по каждому из фасадов.

В созданных экземплярах форм заполняем ранее добавленные параметры: Корпус, Секция и Этаж.

Параметр “Корпус” = B01 (Т.к. полученные модели относятся к корпусу 1). Префикс B - означает Building. Данный параметр введен для того, чтобы можно было затем использовать фильтрации и группировки по “Содержит B01” в других программах. Номер состоит из двух цифр, чтобы при сортировке по нему не получился следующий результат: 1,11,12,2,3…

Параметр “Секция” = S02. где S - обозначает Section.

В параметр “Этаж” заполняются значения: L-1,L01,L02,L03, T01(для технического этажа)… возможно заполнение F01,F02... - для фасадов, A01... - для фундаментов, Z01... - для кровли.

![4.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdHlVXioc4tLMGIZFrLt9VeXpkcyXTEpH16JZuBXuNQfJCHf7XUqIoxggMrRQaA9LltZDxaAYk19f-35TGPqD_8x1hixEe6CT-9FSmiLNu7bL46xZSb6seqnScWmW2thiQfe2s5G_Vi_3IB5Zvv?key=1zAn9q4w8I5y0ntdpe0saA)

1.  Проверить, все ли параметры заполнены Вы можете создав спецификацию по формообразующим.

В получившейся спецификации можно редактировать значения:

![5.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcKdpGwlvlUC_2WLgd5TifgRPJsVeJdr3gjreKsU3iQShIXZjaOmqxDK3R5jWh3Ay5hn1J05IQqr4fP5jj5sdB52VwYG9Vp-xZInkvxkaFrS2-3wDZBDFpLii55KWEKswi1akuIMpz9TCrghLat2A?key=1zAn9q4w8I5y0ntdpe0saA)

1.  По окончании сохраните модель с формообразующими под определенным именем.

## 2\. Копирование параметров из модели с формообразующими в рабочую модель

1.  Откройте модели РД на основе которых создавались формообразующие.
2.  Добавьте всем категориям элементов, которые Вы собираетесь выгружать в Navisworks параметры “Корпус”, “Секция” и “Этаж” как в п.3 *Создания файла с формообразующими*.

Прим.: выделите все элементы на 3D-виде Navisworks и посмотрите в фильтре все существующие на этом виде категории элементов:

![1.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfuWPOJiKKXpPiBDcf_1rkQJe6ZiRn6e_b30B5WNwaGmTLCAHnJvxYfrgaOeitRYAj8rVtJ2LPCT7pxTybn0-uo7GsSgBoC6jmrTQaBJ6Dn1yaWLMhCRavbEnlzssrxI7hSyOTWr7tFv1POTyhaVQ?key=1zAn9q4w8I5y0ntdpe0saA)

1.  В рабочую модель копируем спецификации из файла [](https://wiki.sgnl.pro/app/page/1ab-yNz1DcDSAjytlvURwqNbuYHToQSgQ/view)[**"W\_Спецификации для копирования"**](https://acc.autodesk.com/docs/share/projects/5e8469a3-9d9c-4f47-ad48-33dc8cf120cf/files?shareGroupId=33980b0c-491a-461b-aa75-94d40fd1b65e).

Во вкладке "Вставить" выберите "Вставить из файла" - "Вставить виды из файла". Укажите "Спецификации" и нажмите кнопку "Выбрать все".

![2.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd8hIGYep3mEAb15PUkMMzEO8on5RVne7z6qhkZfSw_kWfqWLK2i_kGjrgtrv1JvH-QNzgm_luNarPkjgmxjQoG0Qwl4_nvV2nttgQD1e84OpCSUqMhDgJdlVqkOTtMIdP4S1blBp6P5efZGdMtuw?key=1zAn9q4w8I5y0ntdpe0saA)

![3.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfOcAN_roO4RGm1pmw-wZJ_urSFNoZyosjcm5V8JLtN0mkoFKEEDRGFEb7RUTnCvfXsRRdCQn_bbU-jhfGgfTPYVpWK78mbsYg_QJJoAThI-PNKcrF_XMmRrAKX2KsO9EYg5_9iZYIBs3s0VVI6?key=1zAn9q4w8I5y0ntdpe0saA)

Прим.: это делается для того, чтобы добавить сразу всем нужным категориям  параметры “Код1”, “Код2”, “Код3” и “Работа1”, “Работа2”, “Работа3”.

![4.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe6wGlb-B2BxapqIho9zI4V74dgX1q3KL1AevNOhvKeDTNkIs7SxHcTuT9Xq-UdS4z2Rt0km6cygnCXQMpNhxaAfDbqsbRkUghnUZgTPeqENSfwhRSlZ4dzG1ek77TUaQY5G4GZ1F7I_7-8o5yLpQ?key=1zAn9q4w8I5y0ntdpe0saA)

1.  Во всех элементах заполните параметр “Работа1” (“Работа2”, “Работа3” - существуют для того, чтобы работы, которые по коду и по классификатору относятся к одному типу, разделить по другим признакам). Для некоторых элементов это быстрее всего сделать через выгрузку в Excel.

Как заполнить параметр Работа через Excel:

а) Откройте "Диспетчер проекта" и найдите в нем “Ведомости/Спецификации”:

![5.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeiUIieU52TaJv3GLZ6AC7YlJnj7QwgalSRIB4-c8HMJ1J8Dmm4NbnnnCrxqI8S1a9drWpuicsSkJHtO3FsKhSMhicuJiMTnVsOy-pTd7m9wTeBHp4Ib0MnjrW3C9q2xLcX3p0li4xQ4s3g9uu4?key=1zAn9q4w8I5y0ntdpe0saA)

b) Выберите спецификацию “W\_Несколько категорий”, в свойствах спецификации зайдите в настройки “Сортировка/Группирование” и отсортируйте по параметру “Семейство и типоразмер”, укажите "Для каждого экземпляра" и нажмите кнопку "ОК".

![6.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcYIxblQBo80tJSOHauTqBNBB4tzNcINZ1_5jAoTUCmBJXW_MHKnlZ5-xv5scm7fBXjiXtddkQJ7QnlPDMVbQrTvgEQWTb4j3bgVb7Thv7cHJ8KyXjAWZhYwyHI3doKfHRBmO4yBXc9AKTyCyhb5w?key=1zAn9q4w8I5y0ntdpe0saA)

![7.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXenRM6T0TsHu7-OievGTHjMs-HA0zrcH936ukO_jD3R6VdDryn0orForpXl0-qtjC10pgV-BQcAQ_AiHFuTrV4WIu0ba08xqVfnT-mBLrgFcBSogbLgU966SZqmiehoafaCO2l8qrDoTfc5ul8Q?key=1zAn9q4w8I5y0ntdpe0saA)

d) В получившейся спецификации в Excel заполните параметр "По виду работ" всем элементам, кроме отверстий:

![8.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXctdRmqMVD-xeVhjZXpqJEkiyQQeTTByL75K0dL2MUHGMJOBxNX4-5RDyZ9U78HZy-OtiDMewdD8OJPkuYu_abJvF_2NY3AH1yq0xXKKoWLO_kCJV-FczabDn6CVhUt5VqcxIxEkzeGEwUc0LpBWQ?key=1zAn9q4w8I5y0ntdpe0saA)

![9.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfsG-NYhwKR5V-EINJbdJeB73oEVldiI4Gql1wTOs65zwX8GMUbGdGt_VGEZ1cxHuv9kxiqt2f1UemtkFx8wlxBVh20zncyrllBXWQj4ogSC0NddUas6AkRt1gOxg-3TUyygpIBTiLWkJOVFIoU?key=1zAn9q4w8I5y0ntdpe0saA)

1.  e) Через скрипт [*“10.02\_Обновить работы”*](https://wiki.sgnl.pro/app/page/19TRAJSwGI20HToRCy4rF0GCQ0MfM1Qlq/view?usp%3Dsharing) заполните параметр:

![10.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdgK5bjxavGhAge98Y5O9DXXmOE5KlMKAYuKDx9uPL4x4qe0dpWU3xcraFJTEFUc59mgpYhyNGZvUEsPf1rvmEUACfpu86o-LCsshM1na3f4gBvo_9k9zmNMe6RfY6uTyhAZSun94uSgQ1xqun2sg?key=1zAn9q4w8I5y0ntdpe0saA)

f) Повторите этот пункт 4 со всеми оставшимися спецификациями, при необходимости создайте свои спецификации и также их обработайте.

![11.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcCZopRE3w3VOOGtf-5Jk5Oe36WGT_mDJctSQnbaAr4HbEmPXN9BZHmQ1AEBXmkexCU5NCzPdSumaDNMGuH0E-t-kEAFM0Hw10gFMq5Dh_ZkED3tFo4o8HgoQREGL1Nnbfu5pKc2sUfXWJR_bOV0A?key=1zAn9q4w8I5y0ntdpe0saA)

Важно! Обязательно проверьте все ли строки спецификации параметра Работа заполнились и всем ли элементам он присвоился. Вы можете это проверить контрольной выгрузкой в Navisworks. Во вкладке "Файл" - "Экспорт" выберите "NWC":

![12.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfLpCzt7tUtm6qQDc7T3j27LdcxixmwVh3KdqHd_OvQn24m0AqnCInMpDYl3J2dG6jJB_FKpKRJlRTYJc2Kx-aSoExxNr4g8SsXA7Wtr4m4qdhaCK8tJr5eenmKVTDRbHRcq1AsA5xyEhIZYs9gPA?key=1zAn9q4w8I5y0ntdpe0saA)

(Скачайте файл для экспорта из Revit в .nwc по ссылке: [*https://www.autodesk.ru/products/navisworks/autodesk-navisworks-nwc-export-utility*](https://www.autodesk.ru/products/navisworks/autodesk-navisworks-nwc-export-utility))

Нажмите кнопку "Настройки Navisworks", далее в пункте "Считывание файлов" - "Revit", выберите "Текущий вид" для "Экспорта", нажмите "ОК".

![13.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf0G9bX4vORo5NTpiySaaK07QxIlOOP3f4P52Y0z3b_dZOr3_l6y2XG6f7QJlkG4wlfvX9AU5btCYU2bBWbXQqIZpG9EzLJCv_7VrZqAieTh2B-A6RuyLNV92M1yBY9j2621srdahyTR6r_OUQqbw?key=1zAn9q4w8I5y0ntdpe0saA)

![14.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcZNyv-pPQEU-8jP57wF6JX8VbmnOxtH8a5y1fURURfhnLeRjXAW8ofoy639K53wd9y11OrQqDHIgUs1rBJRH77PKbqPMVDMps7iCUbqh7Qq20c2Tvayd0ygTADDIJjlqFqUmV8kwt4KoMkm5uOiQ?key=1zAn9q4w8I5y0ntdpe0saA)

В Navisworks во вкладке "Главная" нажмите кнопки "Выбрать" - "Дерево выбора" - "Найти элементы", выберите нужные пункты и нажмите "Найти все".

Если все коды работ проставлены для всех элементов, то можно снова переходить в рабочий файл в Revit. Если есть элементы, в которых не заполнены коды, то проведите анализ и заполните параметры в Revit.

g) Загрузите модель с формообразующими в проект по общим координатам

![15.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcKXfd8o1Ed-f80fP4v6721utqu3h5cBOhwKaLsgCwabPo9_c8ap2h15a7Lsq73vMdcGEuQu08xMOTLz-rJBW6dMFG-GJjXLYEXBRVkYPEQTkxjMV0n-dd1ygzhho4IxfserN-scgp5dFy0wQPX?key=1zAn9q4w8I5y0ntdpe0saA)

![16.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdswDfZ9JQwbtCiWcTdUNkHS2BEi5KeXvjMDqY0sg-5_K62lstK55ydQa0tmE7JfLBRfWTUeqnyYLEbGK2WEsDgOjPOnKrkVR31mMGrR8wM6PNiAtyDN9uo6R_OXywYSP9i1gnbJcHwNuoWXMFBYA?key=1zAn9q4w8I5y0ntdpe0saA)

Прим.: если связь загружена, но не видна, то проверьте в какой Рабочий набор она была загружена и при надобности перенесите в видимый рабочий набор на виде Navisworks.

1.  Запустите скрипт [*“10.03\_Заполнить коды”*](https://wiki.sgnl.pro/app/page/1BYec7kO1WyvRu6lIwagC-crAXbYnxfz_/view?usp%3Dsharing), выберите связь с формообразующими и после его работы появятся заполненные параметры Код1, Код2, Код3, Корпус, Секция и Этаж:

![17.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcoG7p00DKvXBo5nlEFLmgBrVw00U3sgeif_jL87sHQFTyypfF5fpVoOTCwnML6c8Xn2JOUVxHn_paSSMfh6ENILGEGmGkp7y5kqZVyzGa_FlM6a_V5J11wSEltVrFNUitgHxiPZQpjZDTwBFYi?key=1zAn9q4w8I5y0ntdpe0saA)

Должно получиться так:

![18.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfKOg2Zh1PO35kDJ85VryAg30dx2FEgZQCdjpKCJ6zkJZ64UTuriHfw34n71e9KsZUkXx1y3RCEiD6HGnl3QNJh_bYsRLeH9WWzRYmGQ7r5pgGrlv3qZUiY5EVzg2eBM3rT7kJXwmAAzMwGSc8fzw?key=1zAn9q4w8I5y0ntdpe0saA)

1.  Для того, чтобы заполнить параметр “Код” с учетом параметра “Захватка”, запустите скрипт [*“10.10.Z\_Синхронизировать работы КР”*](https://wiki.sgnl.pro/app/page/1X2KPpIfgQodLS-rSItGcfrlBSF4cP_j8/view?usp%3Dsharing) и после его работы появятся заполненные параметры Код1, Код2, Код3, Корпус, Секция, Этаж и Захватка.
2.  Экспортируйте 3D-вид Navisworks в формате .nwc:

![19.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeWyWI4CB48b7JVqfNwDq8bHYWM-gWwFhddGWg0zGD7i7zHJ34sen8qK1Pk_CT1-qz3c34OWwHI1UGu2jf4ZducWq_O2OpCu9sll2lc-Uvty_VbDDynupJpx9v7YeTNPVdw3fkA5h93cxVgLtJIXQ?key=1zAn9q4w8I5y0ntdpe0saA)

1.  При надобности повторите весь путь со всеми файлами корпусов.

## 3\. Окончательное оформление 4D модели

1.  Для создания сводной модели запустите Navisworks 2020. Затем необходимо нажать кнопку “Добавить”, в появившемся окне выберите путь к папке NWC, поменяйте "Тип файлов" на "Кэш Navisworks (\*.nwc)". Выделите нужные Вам для сводной модели файлы и нажмите кнопку “Открыть”.
2.  Теперь нужно создать поисковые наборы в соответствии с параметром Код, с помощью плагина SIGNAL for Navis “Sets from Excel”.

Чтобы автоматически сформировать поисковые наборы с помощью плагина проделайте следующие пункты:

1.  a) Создайте [*файл Excel-документ*](https://wiki.sgnl.pro/app/page/1f4U0BhPgufoU2iDBMlhG9THRl_eb2DR7/view?usp%3Dsharing)*,* описывающий структуру и правила поисковых наборов:

![1.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfDLbRHkDSr4VI-d2FpqNbIjrg6Hcczp0lbze2bxlxElRuunHxyWmGchlvYaK9v83DddIYvwUWma2Uwd9RH2QFDCiZunKPuQN9q-Pe1AEgx2S8jkO9aGw1jsh4fln5pSzUdaCNWibVqeQJUU7RV?key=1zAn9q4w8I5y0ntdpe0saA)

Прим.:

данный Excel-файл состоит из названий папок:

F1

F1.0

F1.0.0

F1.0.1

где буква F = Folder, т.е. это папка, в которой будут находиться поисковые наборы.

Во втором столбце папки имеют значение наименования, которые будут отображаться в диспетчере поисковых наборов.

Поисковые наборы имеют код в первом столбце, идентичный коду папки, но с заменой на букву W (обозначающую Work).

Таким образом, работа, которая должна будет находиться в папке F1.0.1 будет иметь код W1.0.1

Далее в поисковом наборе указывается "Имя" в диспетчере поисковых наборов.

В столбце C указывается вкладка свойств в "Свойствах объектов", на которой находятся искомые параметры.

В столбце D находится параметр, по значению которого отфильтровываются элементы.

В столбце E находится значение параметра по которому поисковый набор отбирает элементы.

В столбце F указывается условие по которому выполняется поиск элементов:

“=” - равно;

“?” - содержит;

“!=” - не равно;

“d” - определенный.

Далее, по 3 столбца, чередуются следующие параметры для фильтрации по условию "И".

b) Загрузите Excel-файл и проверьте все ли элементы попали в поисковые наборы инструментом "Cкрыть"

![2.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdHqU_ZmyNs_0HAPBdrlT103cjSZIS4krz0Kufopd9TflZ_EcX5qecMhFvUQTw2K0LtbcCYysXkEw3J5Q8QnB9lAhEFSilfhwxXJKufXdiQZym6BpBLAApUEbBh8jyKfjH9wVts7C7IUhjMRVMZJw?key=1zAn9q4w8I5y0ntdpe0saA)

Прим.: чтобы работать с поисковыми наборами, откройте окно "Наборы" и выделите нужные Вам поисковые наборы (можно использовать Shift и Ctrl).

При необходимости обновите поисковый набор, для этого достаточно открыть инструмент “Найти элементы” и выбрать нужный Вам поисковый набор. Поправьте правила, нажмите правой кнопкой мыши на поисковый набор и левой кнопкой мыши на “Обновить”.

1.  Далее импортируйте график производства в MS Project. Либо создайте на основе уже имеющегося упрощенный график производства работ.

![3.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdxLcwalXWrgJFAlBEASz7FK945rSayqK4vkiXa_IlnMAQraLpG_7BIvCIP1K-LA8xAq2VsMgk-TmoHmWCkz_Qe7j_I8Xn4w9BIQQTo52Mye70oZqoFe3CKDi0hlA3H0QOo8GiLo7aOMAn-n-v7?key=1zAn9q4w8I5y0ntdpe0saA)

Настройка соответствия столбцов TimeLiner и Excel:

![4.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdZXeSDWcl_T4p_8vybw5LS9kiZeMK7suQ9F50BAHOOE-CBOXgi9wvnC_yuvCkJZulPi7dgADCJF1_9v92lRniTapGn-HiNQUMXKPW5StJKjXDo7CwbNPffn8CjM45h_c_KuGrlvDChD_MZvVwr?key=1zAn9q4w8I5y0ntdpe0saA)

После добавления источника данных (графика строительства в формате MS Project) необходимо нажать правой кнопкой мыши на строчке с графиком и выбрать “Перестроить иерархия задач” для отображения структуры графика во вкладке “Задачи”.

1.  Чтобы график визуализировался, необходимо присоединить к задачам TimeLiner элементы в соответствии с поисковыми наборами. При условии присвоения одинаковых наименований “Имен задач” в графике и Поисковых наборов в Navisworks Manage есть возможность автоматически присоединить Задачи к Наборам. Для этого Вам необходимо в "Timeliner" во вкладке "Задачи" нажать кнопку "Автоприсоединение" и выбрать пункт “Отображение задач Timeliner из столбца Имя в Наборы объектов с тем же именем, регистр Совпадающие”:

![5.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcFxiSKmY5YiKZHvnEZvSHU1Rb9suijcPlrmkqoL3S6gHhqRz49n5WWHfyrK2Ack7kXeLvIE1AER-7NOozZd5kG-WVrrUt4m3gg0GYiyB_Dbrmz47R7QjZvlPNmbYUXaf3pziIF2k0dVSJh85YcSA?key=1zAn9q4w8I5y0ntdpe0saA)

В столбце "Присоединения" во вкладке "Задачи Timeliner’а" появятся синие записи о присоединении поисковых наборов. Поисковые наборы присоединяются по соответствию наименований самих наборов и задач в графике.

1.  Таким образом, во вкладке "Моделирование" Вы сможете увидеть график производства по дням, с учетом того, что планируется построить, и что уже сделано по факту:

![6.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfNHIGoSgRtLb-m55wJnKuljWt8tWTCzm7GcQPd-g57K1O8NxuMWmXSHxKnGYZwzvqCGMIttkdap_PmJf7B8YbGqb2wL18ZzCH0dbQi_hwS3_wL4F3M3BaVzLxz0xWCxr3XBAGJ2PqDD_WIANQfKQ?key=1zAn9q4w8I5y0ntdpe0saA)

![7.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdVYEIQ03QUiga_YJZIGCXNK4AAX5o7RjNXFj6XKTeVV-VJd0Wqt9eukibluLHqVlz3sp4AkTye3Jy7k43rrPPNgPo-eyYpLudRN8-9JJU7mB_xSC2V0PBOMBK9cUE0D6vieGxyQu9taVMw8qL0?key=1zAn9q4w8I5y0ntdpe0saA)

## 4\. Термины и определения

**Рабочие модели**

Модели формата RVT, в которых ведется работа проектировщиков, из которых выпускаются чертежи. Обычно хранятся на сервере проектировщика, Revit-сервере или в BIM360 Design.

**Разбивка рабочих моделей**

Рабочие модели обычно разделяются по дисциплинам, таким как АР, КР, ОВ, ВК, ЭС, СС, ГП. Зачастую дисциплины соответствуют разделам разрабатываемой документации, но иногда модели объединяют в себе несколько разделов (н-р: как ОВ1 и ОВ2, ВК1 и ВК2), либо наоборот разбиваются на несколько моделей для скорости работы с ними (по принципу максимальной независимости) (н-р: АР-кладовые, АР-фасады, АР-кровля, КР-секция 1, КР-паркинг).

**Среда общих данных**

Серверное пространство, в котором администрируются права доступа и в которое выкладываются файлы. Доступ возможен из любого места, посредством интернет-соединения. Обычно возможно изменение статусов у файлов, выдача замечаний на основе файлов, процесс согласования документов и моделей.

**Выгруженные модели**

Модели, выгруженные в среду общих данных для проверки, согласования, передачи определенного этапа работ, согласно договора.

**Отсоединенные модели**

Модели, скачанные из среды общих данных на локальный компьютер, либо внутренний сервер компании и пересохраненные на данном сервере с отсоединением, для того, чтобы вносить корректировки в эти модели (например заполнять параметры)

**Модель ПОС**

Модель в формате RVT, выполненная по чертежу ПОС в формате dwg в координатах, в которых находятся остальные модели проекта. В модели ПОС должны отображаться временные сооружения, границы участка строительства, ограждение участка, упрощенная существующая топосъемка, упрощенная вертикальная планировка участка, котлован в виде выемки и обратной засыпки, краны.

**Модель структуры объекта**

Модель формата RVT, выполненная из формообразующих элементов (инструмент "Форма"). Данная модель отражает структуру объекта по которой будут делиться элементы и работы, связанные с ними (в различных компаниях и методиках работы это называется: захватки, наряд-заказы, пакеты). ТШН\_СО\_КР\_R19

![8.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcedjdYTEsu16JUNyuHcgiWa39VKn1bJ30hMYKw_HEzHVfGv7etFl5e2K0K9vPaezxodmUg-nt4Vz-nbC-5W4cxkCTJOxu07ef2sCmbSvhRaG7tmIDk2yG9eO6hIJbOhgkbHL5mmnU_CvRgIuHXBA?key=1zAn9q4w8I5y0ntdpe0saA)

**Модели NWC**

Модели, выгруженные из Revit с помощью стандартного функционала "Файл" - "Экспорт" - "NWC '

**Поисковые наборы**

Выборка элементов по определенным правилам. Поисковые наборы позволяют выбирать группы элементов по определенным заранее настроенным правилам. Поисковые наборы можно синхронизировать с позициями в календарном графике, если они совпадают по наименованию.

**Календарный график в Timeliner**

![9.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfT_y53DmDJ5OWgQ255IVadOgrWPAh5TwmuZancE43HXqj9Eo4Z-YPsqS8ipFY8K1sJ1ECFZqySyXzSjLdsfze-4uXATb90q5U9NQwYq5u1kGuyY8MkO3oSevXhmLonZvpBcpcgIvRsw8-XahOR8g?key=1zAn9q4w8I5y0ntdpe0saA)

Инструмент, который позволяет связать календарный график, выполненный в MS Project или Primavera с моделью, выполнить визуализацию процесса строительства и отобразить количество расходования денежных средств на определенную дату. Также данный инструмент позволяет отобразить отклонение план/факт и подсветить отставание по графику. Для этого необходимо указывать фактическое закрытие в графике MS Project.

![10.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcI4wriMkczcRfIOUWJV8Z4J5pICRA4GYLDBuj3N7xqeTRg2JLbgNfUjqlHBEmf1HhyrEE9jvfotZT2jlFh9kw_EFaFrYHmefGrD5BgPxi7YR353aU-DLBUNPVxglFl3whmH3BXNhuf9Z0M62V2DA?key=1zAn9q4w8I5y0ntdpe0saA)

**Сводная модель**

Модель формата NWF, выполненная в программе Navisworks Manage. В данной модели подгружены модели всех дисциплин в формате NWC (выгруженные из Revit). Помимо моделей NWC в сводной модели хранятся настройки Поисковых наборов, Привязки к календарному графику.

**Передача сводной модели в NWF**

Сводная модель в формате NWF - это файл-сборка, который ссылается на файлы NWC. Передавать сборку NWF необходимо вместе со всеми файлами NWC, которые в него подгружены. При этом сохраняйте вложенность и наименование папок в относительном пути от папки NWF.

**Передача сводной модели в NWD**

Для передачи зафиксированной ситуации в одном файле, можно сохранить рабочий файл NWF в формате NWD. Обычно при сохранении файла в формате NWD,  указывается дата (н-р: ТШН-К1-Сводная модель\_27.04.2019.nwd). Сводная модель в формате NWD не является рабочей моделью - это отсоединенная версия модели на определенную дату. Любые дальнейшие операции с данной моделью по добавлению дополнительных файлов будут выглядеть таким образом, будто в формат NWF загружен файл NWD и другие файлы. Так тоже можно работать, но это не рекомендуется, т.к. потребуется двойное обновление (сперва NWC, затем NWD) и у Вас может возникнуть ошибка (когда потребуется передать настройки из файла NWD в NWF - это не получится сделать).