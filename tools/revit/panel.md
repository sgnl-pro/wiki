---
title: TOOLS. Панель
description: 
published: true
date: 2026-02-04T14:17:09.166Z
tags: tools
editor: markdown
dateCreated: 2025-09-21T13:06:43.878Z
---

<sub>**[<   TOOLS FOR REVIT. Настройки  ](/ru/tools/revit/settings)     **|**     [TOOLS FOR REVIT. Проверка    >](/ru/tools/revit/checker)**</sub>

---

> Настройка позволяет добавить Виды работ, которые будут указываться при использовании [_инструментов Завершить/Принять/Запланировать_](https://wiki.sgnl.pro/app/page/1F_NQGrCyKvBs3TK006Kjjpemo_sPDwrdym1S8PKnCbc). Подготовьте свою структуру по видам работ, используемую на объекте. Укажите Код и Имя работы, единицу измерения и цену за единицу.
{.is-info}

Нажмите на панели Настройки ➤ Настройки ➤ Виды работ

Папки и виды работ можно добавить вручную, или импортировать готовый Excel файл (см. принцип заполнения таблицы Excel).

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc7b6o55Kfe47fhtBj6EflrUjN3bEEW_UNnT6gE0hWBTIqL-0pEKpSFe7Qf2LUSMnOmJVRlzRu6geBwaqWrcSWAqm0rq5XsPffipiMpgzHMOQ64EALNMHIvRm8Fc65_0aY?key=1C8NQxdVVYUOzLIlAZ67ZQ)

1.  Добавление новой папки.
2.  Добавления нового вида работ.
3.  Импорт видов работ из таблицы Excel.
4.  Импорт видов работ файла XML из Primavera
5.  Экспорт видов работ в таблицу Excel.
6.  Очистить список видов работ.

### ***Принцип заполнения таблицы Excel:***

![image-1683718297139.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc0pFjwFWG53XMeUkXWoTAmhBieI9i0wUmEAYXVLe9xpRgyrgdefKxxQlA9O2M083DoRA4kzRD0kgF7tYmiN8xIr-IaNSncvTCvV_AMo3djP8Z79kOhdqCSykSOrroGqyCkvuIViHM57lbbF_6G?key=1C8NQxdVVYUOzLIlAZ67ZQ)

-   ***В столбце “Поз.”*** содержится значение в формате F1, F1.1, F2, F2.1, F2.1.1 или W1, W1.1, W1.2, W2.1.1, где F означает, что данная строка задает папку, а W создает вид работ.

1.1, 2.1, 2.1.1 - задает вложенность папок, т.е. F2.1.1 будет вложена в F2.1, а та в свою очередь в F2.

W2.1.1 - означает, что вид работ должен быть создан внутри папки F2.1.1

> **Внимание!** W2.1.1 может и должен повторяться для всех видов работ, которые размещаются в одной папке, т.е. он не увеличивается на последнюю цифру - это не номер по порядку, а указатель на размещение вида работ.
{.is-warning}


-   ***В столбце “Код”*** указывается код работы.
-   ***В столбце “Описание”*** указывается название папки или вида работ.
-   ***В столбце “Ед. изм.”*** указывается единица измерения вида работ. Для папки единицы измерения не указываются.
-   ***В столбце “Расценка”*** указывается цена за единицу работы, которая используется для выгрузки КС-2 в Tools For Navisworks
  
#
<sub>**[<   TOOLS FOR REVIT. Настройки  ](/ru/tools/revit/settings)     **|**     [TOOLS FOR REVIT. Проверка    >](/ru/tools/revit/checker)**</sub>