---
title: TOOLS. Согласование
description: 
published: true
date: 2026-05-15T12:03:31.173Z
tags: tools
editor: markdown
dateCreated: 2025-09-21T11:29:02.534Z
---

<sub>**[<   TOOLS FOR NAVIS. Панель](/ru/tools/navis/panel)     **|**     [TOOLS FOR NAVIS. Расчет   >](/ru/tools/navis/calculation)**</sub>

---
>Во вкладке "Согласования" располагаются инструменты для проставления текущего статуса элементам модели. Данные функции нужны для создания строительной модели и ее дальнейшей [визуализации в модуле DASHBOARD](https://wiki.sgnl.pro/ru/dash/cards-50)
{.is-info}  
  
  
![roamer_3hyzsqq4u3.png](/sgnl_tools_navis/approval/roamer_3hyzsqq4u3.png)
  
  
# Вкладки{.tabset}
 
  
  
## Статусы {#statuses}
### Завершить/Принять/Закрыть/Запланировать {#statuses}  

Используя команды Завершить (Completed), Принять (Accepted), Запланировать (Planned), Закрыть (Closed) можно присвоить соответствующий статус элементам.

1\. Выберите элемент/элементы и нажмите на вкладке SIGNAL на панели Согласование ➤ Завершить/Принять/Запланировать/Закрыть


-   **Завершить** - дата фактического выполнения.
-   **Принять** - дата согласования и приема строительным контролем
-   **Запланировать** - плановая дата с назначением исполнителя.
-   **Закрыть** - дата фактического закрытия работ и оплаты по КС2,3

Окна настроек команд Завершить/Принять/Запланировать выглядят одинаково

![image-1683289600307.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeQEjsWQJkyub8aMkdBWhFy78Dq_sUApm4DqgJtfrSCUmEzBx3jKaAwVc5SGo4aXt-C38eO2LA_ngg5pqFGMNqF77MN628EORA_hv5rC74l8Ij-Xbfmbm0SHA0TZAepfkiKv9Fcu0Xg58U-wRUi?key=y84hG1tGSPT0ueaXfEQOLw)

-   ***В строке “Дата”*** укажите дату завершения работы
-   ***В строке “Вид работ”*** выберите из списка вид работы, связанный с элементом. Работы можно добавлять двумя способами - ручной ввод или импорт таблицы Excel (см. подробнее [_“Настройка видов работ”_](https://wiki.sgnl.pro/ru/tools/navis/panel#jobs))
-   ***В строке “Исполнитель”*** выберите из списка компанию, которая выполняет заданный вид работ. Компанию можно добавить в Настройках плагина Сигнал (см. подробнее [_“Настройка компаний”_](https://wiki.sgnl.pro/ru/tools/navis/settings#companies))
-   ***Кнопка “Очистить свойства”*** удаляет значения S параметров у выбранных элементов

2\. После присвоения статуса происходит следующее:

-   В свойствах выбранных элементов во вкладке “SIGNAL” появляются соответствующие свойства *“Completed”, “Accepted” и “Planned”, "Closed"*. Так же появляются свойства *“Work”, “Unit”, “Color”, “Contractor”.*
-   Создаются поисковые наборы *“Completed”, “Accepted” ,“Planned”, "Closed" и “Color”*
-   Выбранные элементы окрашиваются в соответствующие статусу цвета. По умолчанию Completed - Зеленый, Accepted - Фиолетовый, Closed - жёлтый, Planned - голубой. По желанию цвета можно поменять в настройках плагина (см. [_Раскраска_](https://wiki.sgnl.pro/ru/tools/navis/settings#painting))

![image-1683289668766.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd6rB8l-q5WYrT1z3Og75_T2HPCzyxrPgMpUCGUACoio_Z_SwddcC6eiMlBrcucgqQ5gPHyI4EUmhq9k65noNcguCEeWzCgapgmMX6kC9UkBD-yxACkI0pTqpIkDOv1KLHKo78LvyabVzH4FNOw?key=y84hG1tGSPT0ueaXfEQOLw)

![image-1683289654130.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfesfaZweWzfLRMLyd3VFFI9_7jR6V2_SqP-bQDngPyPpZg_TBiBzX6l9GUSS9aceNdIngPId7iJjbSIkMM8SaZkAR1MW9QxlHVfl7xi4lEZ2qtND5iTWsquhkTkAPcpur33gEBJH_73Dhw-Rjr9w?key=y84hG1tGSPT0ueaXfEQOLw)

![image-1683289638537.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfqCC2cYOEKdjr3ssSSahmQ2HE_jxtoY2N4dC38XDT4raslZ85fTryuA8rOSWb4qR-AXPeebgTm1KqAh_ui0_m4rlCatIC1JJIKqbbxLRjiYSOKzViNlpdTY9WQcPNFfSOqmHR32GYPWKM-9j_MuA?key=y84hG1tGSPT0ueaXfEQOLw)

  
  
  
  
## Процент {#procent}
### Процент {#procent}
> Инструмент предоставляет возможность записать процент выполненных работ для каждого элемента модели. Например, его можно использовать для оценки прогресса выполнения инженерных сетей с разбивкой по этажам, квартирам или по помещениям. Это позволяет более точно контролировать прогресс работ и оценить степень завершенности проекта.{.is-info}

1\. Выберите элемент/элементы и нажмите на вкладке SIGNAL на панели Согласование ➤ Процент


2\. В открывшемся окне укажите процент выполнения работы и из выпадающего списка выберите вид работы. Нажмите “ОК“

![image-1688029097577.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcSp8Ei2RcPqoJnZ3UoZhGDpVKoYyoS0bJC-peUyb9B1_UEfIQhUtsc-6Vtf4p2_q-mOqNk3bX8kndSxCQdvD1MzwPPu5HSeKfY5vIy4UuBw_JnJU8hc_NNlWdQ5KpO24bObYh_FTNqbi9zmzoOZw?key=i-4zDvsgwTb3ZQgDXeB9kw)

-   Чтобы виды работ попали в список, требуется для них в Панели SIGNAL поставить единицы измерения %

![image-1688029120294.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeAu19_PMesB1rLkc7uxTIrnF9MotolL9_QzS8NJ4bKRlpl_sUDzd8N_bY6hyIpX0UWxzKObSC9sPNMpCCg7SjvHP96laqRs7zgwcgM8-mTA85FayLg2j4B7vPaHFOx7B7_A_FQZhELydbQr3lX?key=i-4zDvsgwTb3ZQgDXeB9kw)

3\. После присвоения процента происходит следующее:

-   В свойствах выбранных элементов во вкладке “SIGNAL” появляется соответствующее свойство “P\_{Вид работы}”

![image-1688029141423.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcbs0bv1Z_CH22eRqtj-AFIlFLrYNhUSt41YdhxbBulF_7lcU42s0UoGyiyLNC3rP1xfkATKCy8wBfEZJ0NsTbuszk0xBx6uGFT-GO5JLPqvl9ZYHjrTmG89i3pJutCMr0WvNiva2NDZob1ARK0?key=i-4zDvsgwTb3ZQgDXeB9kw)

-   Создаются поисковые наборы с значением процента

![image-1688029159255.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf7OmdXcmWUUMnfK39bANvOuP-qduJSK6f7xcEY7LSHUkbAN_4mSFKmU_0ORAqVZgbNMY8F4rWFzX-Dyjnff7J9DlNoYmQ9k-8ZmEFzTD4q4in4hRxE7jNZv5qJo-9JFubg9LeX83HxZNI2CAWA?key=i-4zDvsgwTb3ZQgDXeB9kw)

4\. Для того чтобы раскрасить элементы по проценту воспользуйтесь инструментом [_“Раскрасить”_](https://wiki.sgnl.pro/ru/tools/navis/coloring#painting)

![image-1688029176622.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXePDZ1Tny4EMlNEplNCRUYL31ntE9G0pZDcX9iUt_rjpPT8SsYW2eGQlaz10C5G0caVLP3hBtLbGLzctuAx5m9BkAh56I5vmgYaDXZVpVhKQ6unGVvkMv5puCrwt_70O8r7tCtuPvFQ0avnfXWCsQ?key=i-4zDvsgwTb3ZQgDXeB9kw)


  #
<sub>**[<   TOOLS FOR NAVIS. Панель](/ru/tools/navis/panel)     **|**     [TOOLS FOR NAVIS. Расчет   >](/ru/tools/navis/calculation)**</sub>