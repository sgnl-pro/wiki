---
title: TOOLS. Панель
description: 
published: true
date: 2026-05-15T12:04:11.894Z
tags: tools
editor: markdown
dateCreated: 2025-09-21T11:09:12.445Z
---

<sub>**[<   TOOLS FOR NAVIS. Настройки](/ru/tools/navis/settings)     **|**     [TOOLS FOR NAVIS. Согласование   >](/ru/tools/navis/approval)**</sub>

---
# Панель SIGNAL

>Панель SIGNAL позволяет собрать в одном месте информацию об элементе или наборах элементов, содержит различный вспомогательный функционал для удобной работы со свойствами SIGNAL, прикрепления к элементам модели различных документов, взаимодействия с видами работ и быстрой настройки оптимального вида
{.is-info}

![image-1684403221122.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdV1bmw49Rk9Wn_iW-KBxRm9JV2lma4p8tBEp3_WoiWHhbMFjr55Mk6PWuaX2O61ariQz_ALzRC6zTGyWnna19s3Qlim_eFmCvNw2cyhLZH_FL6v0J0ALoNuwq7S3caHas0KdNFM9KXY_ZFAYgkUg?key=tRlsOkJXozCsU1RvreZA6g)
  
  
# Вкладки{.tabset}

  
## Свойства SIGNAL {#attributes}
### Свойства SIGNAL {#attributes}

На данной вкладке отображаются все свойства SIGNAL и их значения, а также [_количественные величины_](https://wiki.sgnl.pro/ru/tools/navis/calculation#common) (Объем/Площадь/Длина/Вес) выбранных элементов.

![image-1684403253959.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdqBrn8Ui5_5dPgHLOaEGVZldtU1agB9bUU4U8U02LFNpzWiavOewKZ_2yIQVZpMIZG3P93bVVyZd2YG2hWvARzEVQGONTRVucYnvGusdTvpI_MCWkiZj1RbGrWtpQRg2pL2O7MNNvfvvzCI9Atyw?key=tRlsOkJXozCsU1RvreZA6g)

-   ***Кнопка “ПРИМЕНИТЬ СТАНДАРТНЫЙ ВИД”*** изменяет настройки видового экрана для более комфортной работы с моделью.
-   ***Кнопка “Редактировать”***  позволяет отредактировать значение свойства у элемента/элементов.

  
  

## Работы {#jobs}
### Работы {#jobs}
  
На данной вкладке отображается настройка видов работ и избранных свойств.

### Виды работ

Настройка позволяет добавить Виды работ, которые будут указываться при использовании инструментов
* [_Завершить/Принять/Запланировать_](https://wiki.sgnl.pro/ru/tools/navis/approval), 
* [_КС-2_](https://wiki.sgnl.pro/ru/tools/navis/export-import#ks2), 
* [_Отчет_](https://wiki.sgnl.pro/ru/tools/navis/export-import#log), 
* [_Бюджет_](https://wiki.sgnl.pro/ru/tools/navis/export-import#budget). 

Подготовьте свою структуру по видам работ, используемую на объекте. Виды работ находятся на панели SIGNAL в вкладке “Работы”

Нажмите на панели Настройки ➤ “Панель” ➤ Вкладка “Работы”

Папки и виды работ можно [_добавить вручную_](https://wiki.sgnl.pro/ru/tools/navis/settings#standart_searchsets), или _импортировать готовый Excel файл_.

![t4n_panel_main.png](/sgnl_tools_navis/panel/t4n_panel_main.png)  
1.  Добавление новой папки.
2.  Добавления нового вида работ.
3.  Импорт/экспорт видов работ в разные форматы. Доступен импорт из Excel, DOCS, MPP, Primavera
4.  Очистить список видов работ.
5.  Если переключатель “Создавать только непустые наборы” активен, то будут созданы только те поисковые наборы, которые удовлетворяют условиям создания ПН. Если переключатель не активен, то буду созданы поисковые наборы по всем видам работ, даже те, у которых условия создания заполнены некорректно. Если условия создания не заполнены, то не зависимо от положения переключателя ПН создан не будет.

С помощью инструмента [_“Работы”_](https://wiki.sgnl.pro/ru/tools/navis/search-sets#jobs) можно создать поисковые наборы видов работ

<details>  
<summary> Импорт из Excel </summary>

![image-1683286603846.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeU6jReyLVlI7mQMfIoxv0_viQJ2sgFg1PY7SNiKUH0VGVAmJidmnBOe7mV1TZUUqruVy_NMFkjNBqv0_h8hgjAr3f3R0eM1SgZvIjlmOj6WUmvHpO81xUSCopVMVnPeBFEqyk0z1nKYjaG6OBpxw?key=jUT98gLp1Q8zkf4jZozAlA)

**_Виды работ:_**

-   ***В столбце “Поз.”*** содержится значение в формате F1, F1.1, F2, F2.1, F2.1.1 или W1, W1.1, W1.2, W2.1.1, где F означает, что данная строка задает папку, а W создает вид работ.

1.1, 2.1, 2.1.1 - задает вложенность папок, т.е. F2.1.1 будет вложена в F2.1, а та в свою очередь в F2.

W2.1.1 - означает, что вид работ должен быть создан внутри папки F2.1.1

> ***Внимание!*** W2.1.1 может и должен повторяться для всех видов работ, которые размещаются в одной папке, т.е. он не увеличивается на последнюю цифру - это не номер по порядку, а указатель на размещение вида работ.
{.is-warning}


-   ***В столбце “Код”*** указывается код работы.
-   ***В столбце “Описание”*** указывается название папки или вида работ.
-   ***В столбце “Ед. изм.”*** указывается единица измерения вида работ(м/м2/м3/шт/кг/т/комплект/%). Для папки единицы измерения не указываются.
-   ***В столбце “Расценка”*** указывается цена за единицу работы.

**_Условия создания ПН:_**

-   ***В столбце “Условие”*** указывается условие И.
-   ***В столбце “Категория”*** указывается название вкладки, в которой находится свойство для условия.
-   ***В столбце “Свойство”*** указывается свойство, которое необходимо для условия.
-   ***В столбце “Значение”*** указывается значение свойства.
-   ***В столбце “Тип”*** указывается оператор (Равно: **\=**), (Не равно: **!=**), (Содержит: **?**), (Не содержит: **!?**), (Определенный: **d**), (Неопределенный: **!d**), (Больше: **\>**), (Больше или равно: **\>=**), (Меньше: **<**), (Меньше или равно: **<=**).

> ***Примечание:*** Столбцы “Условие”, “Категория”, “Свойство”, “Значение” и “Тип” задают одно дополнительное условие, по которому будут создаваться поисковые наборы. Укажите данные столбцы столько раз, сколько дополнительных условий требуется добавить.
{.is-info}


![image-1683286673654.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe2pJKpSlK9M35q5AUavk1ICLo3oX7824fkQ7pMTpWrq4Q3Xg_03sQ56sCqWxBj8-4XTz37fhXg2V431AZ2FaFq-o-4E33-HCN3BD5WtrmRejfeI7mAJCShiRXvT4FWHPxQAVuujbOKD7R907JEOg?key=jUT98gLp1Q8zkf4jZozAlA)

</details>

  
  
  
  
## Избранные свойства {#fav_attributes}
### Избранные свойства {#fav_attributes}
  
Данная настройка собирает в одном месте избранные свойства, которые помогают в создании условий для видов работ и могут быть выгружены в [BIM-Link]() для упрощения поиска только необходимых свойств.

![image-1684403381860.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeG5XgAlqrvemXV7wOhoSTkE2KRezYBv-7AyajHhAtNIFBHhlPhT2x9PzN_fciGgbZTiJSfEgfIcNwGAFH0fpqRoA1BrWh9xT3J9YLNH--Pb7m0QzbkN_CB2UFgnsf6YJ-hO8zzWkzJRxadJyh6?key=TD6yNyO8q0mQqb8xM9spyA)

1\. Нажмите "+" чтобы добавить избранное свойство.

2\. Откроется окно с свойствами проекта. Выберите необходимые свойства и нажмите “ОК”

![image-1684403415494.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe3RNRL7NHypnkDiQ_MO0Fk4CnyeAvUvv-XadRaFCzLUklWEB9glj9rbEdS0dKLgsR3xi4WrJp6b7ZhUjOdExyOgRvcwmpSvFyNnuErIQanWAa_zNejGEJSa_ourYZcbtou_wzg_4F9D94b4Lzp?key=TD6yNyO8q0mQqb8xM9spyA)

Начните вводить значение в поле “ПОИСК” ➤ список покажет свойства, содержащие введенное значение. Левый столбец - “Категория”, правый - “Свойство”.

![image-1684403448843.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcCJayqgZWCHKcXTQG_GeICbwbTYUh2n7AropXemc71Mx_kZ2E67r0rIl1l-Thp2EhBhomKZh6f3WZ-yurjO3YnlHbMGOAdOmoSgO3BieQKh1jH_vrzj37XLUvrG9Ef0nJI6ugMUgwGJAfSlliV?key=TD6yNyO8q0mQqb8xM9spyA)

3\. Выбранные свойства добавятся в список избранных свойств. При выборе какого-либо элемента в столбце “Значение” будет появляться значение свойства выбранного элемента. С помощью избранных свойств можно создать условия для видов работ (См. [_Создание условий)_](https://wiki.sgnl.pro/ru/tools/navis/settings#standart_searchsets)

  
  
  
## Вложения {#attachments}
### Вложения {#attachments}

На данной вкладке отображаются прикрепленные папки и файлы к элементам.

Для прикрепления локальных файлов и папок с Вашего компьютера в настройках [_“Документы”_](https://wiki.sgnl.pro/ru/tools/navis/settings#documents) укажите путь к корневой папке с документами.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXepsh8iEaqwHoHKMHpdBkHJM9NPbNNVTDGXvM6gliPfwVujt3QhTH7_N-sp2qpvtEICJzUTKNYGDvmvV0aULrqhll_CX9p0GQG82bySXhrZ4Qd-eTIyI6IsZQVcypJCCLKZZ8wJJ_qRvPePJTR7rw?key=aqcxwRFcmRWJMTA192jxog)

-   ***Кнопка “Перейти к Web документу”***  позволяет открыть прикрепленную к элементу ссылку на web-страницу.
-   ***Кнопка “Открыть файл”***  позволяет открыть прикрепленный локальный файл или папку
-   ***Кнопка “Открыть папку”***  позволяет открыть прикрепленную локальную папку.
  
-   ***Выберите элемент и нажмите "Файл"*** , чтобы прикрепить локальный файл. Откроется окно с папками и файлами. Поставьте галочку напротив файла или нескольких файлов, и нажмите “ОК”. Файлы прикрепятся к выбранным элементам.

![image-1684403547301.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfkancxCnXbOR2c5V3OKR22csKK90eVfeStPmRNrwOXgtxzydCWmgDioIroODnDCSMaVGzI24ufl4ju2PG-valuTTSij7bgUSm61lzlMFkY100tTSGFakZeJWdP8puKxfEMygugm1ITgnskfmr5vg?key=aqcxwRFcmRWJMTA192jxog)

-   ***Выберите элемент и нажмите "Папка"*** , чтобы прикрепить локальную папку. Откроется окно с папками. Поставьте галочку напротив папки или нескольких папок, и нажмите “ОК”. Папки прикрепятся к выбранным элементам

![image-1684403618907.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfUg45UC4WFlFwrjfltSd49U6UqB54ZsCYMYxm9NGL5AZQiW2-cikMNyXH3EO7kMaO98amfKyohyN12rTrtDFbjnIkwq0E1pJ921Rd-x8UYnScHt-wRazlVtnx6vXwUeuulvjtt15TXpnbtNIWUAg?key=aqcxwRFcmRWJMTA192jxog)

-   **Выберите элемент и нажмите "Ссылка"** , чтобы прикрепить ссылку на web-страницу. Введите ссылку и нажмите ОК.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdTChBa-hbxIyxZREA1i0sYkis5WTSmdeimUO9uAgxT7RFpnBxody1nvj9oikuozTwxYGbwGvcOXXklfWgB1SoBXwoYctqn2xtbLeSSVXhoaU8JwPpJjm8qPI0-VCIQVKAfrDEDcr-NNQqChzxO0w?key=aqcxwRFcmRWJMTA192jxog)

-   **Выберите элемент и нажмите "ISSUE"** , чтобы прикрепить замечание из DOCS. Откроется реестр замечаний, выбранного проекта во вкладке [_“Основные”_](https://wiki.sgnl.pro/ru/tools/navis/settings#general). Выберите замечание и нажмите “Продолжить”. Замечание прикрепится к элементу, цвет элемента изменится в соответствии с настройкой [_“Раскраска”_](https://wiki.sgnl.pro/ru/tools/navis/coloring)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc4e-zJw-Sf00AuUr8KQbWSwGim6qGDZ5FYsexEi0m9opiraE6TE6xztkvNpr6BivLJ9ibrhAYdHNBTT-UXYxXDSmTJjpvbfGSY0NJo_JE59Boep2A4quDNQd3jfXkiXZ-X9jci0YTJcUsf1Nmm?key=aqcxwRFcmRWJMTA192jxog)

-   **Выберите элемент и нажмите "DOCS"** , чтобы прикрепить папку или документ из DOCS. Откроется папочная структура, выбранного проекта во вкладке [_“Основные”_](https://wiki.sgnl.pro/ru/tools/navis/settings#general). Выберите папку или файл и нажмите “Продолжить”

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdNLOdqWq9CWle8h5gZW8AKKg3TfpnroRmyAjoLQzkRKLcVMGsg8XbR3xW4R-31kBln90jGx3lnnGRor3rs1uBuA3PoDZLXLPohHsT3XTHZw5XHJNGxfyJEZPr-ed_CbfRqBBEq1U6SfR-wpAuhKQ?key=aqcxwRFcmRWJMTA192jxog)

Все прикрепленные к элементу вложения записываются в свойства элемента:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd-kFM7TTYVFVTd8KpD9BeC9YEHbpKI7-Tp2whsZGc6m1lq1GPP4CFDHYDstUzDaZH5gAS13Uqcwd-ILci15mRojJgUMPkgWisFKYY5XwVbyBD8ZLugGHcO3o_qIXfUAuHJs1YWHzvCd84ts29nIQ?key=aqcxwRFcmRWJMTA192jxog)



## Пользовательские свойства

На данной вкладке отображаются пользовательские свойства и их значения. Всего есть 4 вида пользовательских свойства: Вычисляемое, Редактируемое, Количество с коэффициентом и Мульти-Вычисляемое.

![image-1684403734980.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeFK6BFYZDdqnTFUY-x6nXgTPfncIR-m-Gxsk_ADMxS_N6cPAxW9IFAxEfEBCXEbjbyy4nBnohpV9GUAkBa7QTYVg4B_ygT8lWHkQ9GqnDlTCIYsy3_-xLnf78cdxfXay698k-I-XU0mqXaUYHVFw?key=dtY1kvnFechnFCTGfw8Gnw)

-   ***Нажмите*** , чтобы добавить одно из четырех пользовательских свойств.

**_Вычисляемое свойство_**

Данное свойство служит для отображения в панели SIGNAL любых существующих свойств в модели.

![image-1684403779759.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdKCLr5ohqUKkLUcLorfzuZQnkGyd_Y1Z6rhinvwgRA2FRgGB5aYGpRWb8UzJ6Gx3OAORGKlUlYdrcvTM8KJAiVzHMuq3ASZljHBpWNYVxmNfwH6bNEUNL6TnEpfKG38qfrb8kHBsSNt0rDTnEOhA?key=dtY1kvnFechnFCTGfw8Gnw)

-   Из списка выберите необходимое свойство и нажмите “ОК”. Для упрощения поиска нужных свойств воспользуйтесь поиском. Для выбранного свойства есть возможность изменить отображаемое имя в панели SIGNAL.

**_Редактируемое свойство_**

В данное свойство можно вписать любое пользовательское редактируемое значение.

![image-1684403855920.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdu6Huxirrp-_0txKFn9tYp7ytQu-O0kR0WGZxWq9ZJTqR1ZwgBQA2OwTJXAsku9tgj-3O9fAvQsUaCPmM1lQtG9b-XQNOuRAZxQFczhwdcUoZwNJNa0Nzsr2fF0QRGrbRiRquMhT13zykZK5vP_Q?key=dtY1kvnFechnFCTGfw8Gnw)

-   ***В строке “Отображаемое имя”*** укажите имя свойства в Панели SIGNAL

![image-1684403828358.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXePn1D4POJ4PKuqLTmcltGUl_hYlZHb1DdPF3OpsBwLkZC0iVrC62Zhd-dAGHULk51vvVCf3rt1kP3xVoX9jPKou7jB68tAUYL5tLkGKSYSLQZSA2kMY1ZofI_LooqZRmwOSN9JDJsUTjzxetssUQ?key=dtY1kvnFechnFCTGfw8Gnw)

-   ***В строке “Свойство”*** укажите имя свойства, которое будет отображаться во вкладке SIGNAL. Имя должно состоять из букв латинского алфавита.
-   ***Нажмите*** , чтобы вписать значение в свойство.

**_Количество с коэффициентом_**

Данное свойство позволяет в панель суммарное значение одного из [_количественных свойств_](https://wiki.sgnl.pro/ru/tools/navis/settings#calculation) (Объем/Площадь/Длина/Вес) с указанным коэффициентом.

![image-1684403939638.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXduWBZrAmb6HU64c1nSyn4xdODXWvc2NqT-I1Wfpyj0g3tpqkg8gv1Mr0PXokSo3XjX5VvkXXTbJZywzYz-2gKwYdD9OqdC2meeZ9chsF8GngMQXSYPIF7rvLhL-rvkpqlWz-2hQ8yJBMNzuD_P1g?key=dtY1kvnFechnFCTGfw8Gnw)

-   Из выпадающего списка выберите количественное свойство, задайте ему коэффициент и нажмите “ОК”

**_Мульти-вычисляемое свойство_**

Данное свойство позволяет отобразить в панели SIGNAL несколько существующих в модели свойств через указанный разделитель.

![image-1684403959892.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXecmOi698mNq1JTGSmK6O-ipYGa0BKBqcypAzgAbmsbvWLIdCbTZ0hm3qUHZembPr20YcX3vZiL8dEoDsD1VqLF2vxG5Y8vP5CfzKjX6n35IoviKYnBa_YtPGl8IzdNdj-WPdgiqBBWKeq98vUt?key=dtY1kvnFechnFCTGfw8Gnw)

-   ***В строке “Отображаемое имя”*** укажите имя свойства в Панели SIGNAL
-   ***Нажмите*** , чтобы добавить свойства. Из выпадающих списков выберите пару “Категория-Свойство”.

![image-1684403994632.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXecBce2ydMtkD-4SeV4OKxgwDaKyQkdfyGok79IDKtzq81Y1TRFmJ2rWmgrOOSQ9DumaIEJkX1a-BOm9pgIfYjdhcOd3fJTIMPO5GIyF9a-GObSeGhAq_Z-XYL-1nSGDBQJdUUSHVhYq5schNTILw?key=dtY1kvnFechnFCTGfw8Gnw)

-   ***В строке “Разделитель”*** укажите значение для разделителя между свойствами, например, дефис “-”


  <sub>**[<   TOOLS FOR NAVIS. Настройки](/ru/tools/navis/settings)     **|**     [TOOLS FOR NAVIS. Согласование   >](/ru/tools/navis/approval)**</sub>