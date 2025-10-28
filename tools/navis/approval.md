---
title: TOOLS. Согласование
description: 
published: true
date: 2025-10-01T23:15:45.344Z
tags: 
editor: markdown
dateCreated: 2025-09-21T11:29:02.534Z
---

<sub>**[<   TOOLS FOR NAVIS. Виды работ](/ru/tools/navis/works)     **|**     [TOOLS FOR NAVIS. Расчет   >](/ru/tools/navis/calculation)**</sub>

---

# Вкладки{.tabset}
## Завершить/Принять/Запланировать

Используя команды Завершить (Completed), Принять (Accepted) и Запланировать (Planned) можно присвоить соответствующий статус элементам.

1\. Выберите элемент/элементы и нажмите на вкладке SIGNAL на панели Согласование ➤ Завершить/Принят/Запланировать

![image-1688029260966.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdm-oFoQDxht-fAf87hsKCPdD4Hd7LirBXh6AJkCq_5cU7lmKMVLMQQJQY1QN8iK5R9yVW-VUlSU5Fqr66-J7SkAYEit_gBg9tRZEb08lB0w6IApUZhXgvlj8fPjEsgpSvLwZATMjlyoRR-QRJUow?key=y84hG1tGSPT0ueaXfEQOLw)

-   **Завершить** - дата фактического выполнения.
-   **Принять** - дата согласования/оплаты по КС-2,3.
-   **Запланировать** - плановая дата с назначением исполнителя.

Окна настроек команд Завершить/Принять/Запланировать выглядят одинаково

![image-1683289600307.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeQEjsWQJkyub8aMkdBWhFy78Dq_sUApm4DqgJtfrSCUmEzBx3jKaAwVc5SGo4aXt-C38eO2LA_ngg5pqFGMNqF77MN628EORA_hv5rC74l8Ij-Xbfmbm0SHA0TZAepfkiKv9Fcu0Xg58U-wRUi?key=y84hG1tGSPT0ueaXfEQOLw)

-   ***В строке “Дата”*** укажите дату завершения работы
-   ***В строке “Вид работ”*** выберите из списка вид работы, связанный с элементом. Работы можно добавлять двумя способами - ручной ввод или импорт таблицы Excel (см. подробнее [_“Настройка видов работ”_](https://youneedawiki.com/app/page/1dhz_RYu3DczaEesG4yRQP9sK60FLyuz8SEMJI7nmX-w))
-   ***В строке “Исполнитель”*** выберите из списка компанию, которая выполняет заданный вид работ. Компанию можно добавить в Настройках плагина Сигнал (см. подробнее [_“Настройка компаний”_](https://youneedawiki.com/app/page/1byu2jCgStsBBE-1zBEfPIjNFxIvRgIgLO45Z09pW2XI))
-   ***Кнопка “Очистить свойства”*** удаляет значения S параметров у выбранных элементов

2\. После присвоения статуса происходит следующее:

-   В свойствах выбранных элементов во вкладке “SIGNAL” появляются соответствующие свойства *“Completed”, “Accepted” и “Planned”*. Так же появляются свойства *“Work”, “Unit”, “Color”, “Contractor”.*
-   Создаются поисковые наборы *“Completed”, “Accepted” ,“Planned” и “Color”*
-   Выбранные элементы окрашиваются в соответствующие статусу цвета. По умолчанию Completed - Зеленый, Accepted - Фиолетовый, Planned - голубой. По желанию цвета можно поменять в настройках плагина (см. [_Раскраска_](https://youneedawiki.com/app/page/165fGF2LyUPst6ZWaw12UnxbiSHVFcoz_XI6Nh9hozdA))

![image-1683289668766.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd6rB8l-q5WYrT1z3Og75_T2HPCzyxrPgMpUCGUACoio_Z_SwddcC6eiMlBrcucgqQ5gPHyI4EUmhq9k65noNcguCEeWzCgapgmMX6kC9UkBD-yxACkI0pTqpIkDOv1KLHKo78LvyabVzH4FNOw?key=y84hG1tGSPT0ueaXfEQOLw)

![image-1683289654130.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfesfaZweWzfLRMLyd3VFFI9_7jR6V2_SqP-bQDngPyPpZg_TBiBzX6l9GUSS9aceNdIngPId7iJjbSIkMM8SaZkAR1MW9QxlHVfl7xi4lEZ2qtND5iTWsquhkTkAPcpur33gEBJH_73Dhw-Rjr9w?key=y84hG1tGSPT0ueaXfEQOLw)

![image-1683289638537.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfqCC2cYOEKdjr3ssSSahmQ2HE_jxtoY2N4dC38XDT4raslZ85fTryuA8rOSWb4qR-AXPeebgTm1KqAh_ui0_m4rlCatIC1JJIKqbbxLRjiYSOKzViNlpdTY9WQcPNFfSOqmHR32GYPWKM-9j_MuA?key=y84hG1tGSPT0ueaXfEQOLw)

## Процент

> Инструмент предоставляет возможность записать процент выполненных работ для каждого элемента модели. Например, его можно использовать для оценки прогресса выполнения инженерных сетей с разбивкой по этажам, квартирам или по помещениям. Это позволяет более точно контролировать прогресс работ и оценить степень завершенности проекта.{.is-info}

1\. Выберите элемент/элементы и нажмите на вкладке SIGNAL на панели Согласование ➤ Процент

![image-1688029077358.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdkPWkMaq0lEIbZGPYD5FClRYi-peCOR9iu0cT_w7ljC9ISsPV3Yk_yIexYtski4bAt_91aMflojjfkHFaExN4JcLTQdQiQXLRO4CeXHrDIODqK2RJmKhm3-vrYdtDt5XJIKMSz78LFUJ-RfpYkzw?key=i-4zDvsgwTb3ZQgDXeB9kw)

2\. В открывшемся окне укажите процент выполнения работы и из выпадающего списка выберите вид работы. Нажмите “ОК“

![image-1688029097577.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcSp8Ei2RcPqoJnZ3UoZhGDpVKoYyoS0bJC-peUyb9B1_UEfIQhUtsc-6Vtf4p2_q-mOqNk3bX8kndSxCQdvD1MzwPPu5HSeKfY5vIy4UuBw_JnJU8hc_NNlWdQ5KpO24bObYh_FTNqbi9zmzoOZw?key=i-4zDvsgwTb3ZQgDXeB9kw)

-   Чтобы виды работ попали в список, требуется для них в Панели SIGNAL поставить единицы измерения %

![image-1688029120294.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeAu19_PMesB1rLkc7uxTIrnF9MotolL9_QzS8NJ4bKRlpl_sUDzd8N_bY6hyIpX0UWxzKObSC9sPNMpCCg7SjvHP96laqRs7zgwcgM8-mTA85FayLg2j4B7vPaHFOx7B7_A_FQZhELydbQr3lX?key=i-4zDvsgwTb3ZQgDXeB9kw)

3\. После присвоения процента происходит следующее:

-   В свойствах выбранных элементов во вкладке “SIGNAL” появляется соответствующее свойство “P\_{Вид работы}”

![image-1688029141423.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcbs0bv1Z_CH22eRqtj-AFIlFLrYNhUSt41YdhxbBulF_7lcU42s0UoGyiyLNC3rP1xfkATKCy8wBfEZJ0NsTbuszk0xBx6uGFT-GO5JLPqvl9ZYHjrTmG89i3pJutCMr0WvNiva2NDZob1ARK0?key=i-4zDvsgwTb3ZQgDXeB9kw)

-   Создаются поисковые наборы с значением процента

![image-1688029159255.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf7OmdXcmWUUMnfK39bANvOuP-qduJSK6f7xcEY7LSHUkbAN_4mSFKmU_0ORAqVZgbNMY8F4rWFzX-Dyjnff7J9DlNoYmQ9k-8ZmEFzTD4q4in4hRxE7jNZv5qJo-9JFubg9LeX83HxZNI2CAWA?key=i-4zDvsgwTb3ZQgDXeB9kw)

4\. Для того чтобы раскрасить элементы по проценту воспользуйтесь инструментом [_“Раскрасить”_](https://wiki.sgnl.pro/app/page/1sKveQeB11oVjviyFR_BPtaX1OzUCGXkbAwkLJ_8uMJ8)

![image-1688029176622.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXePDZ1Tny4EMlNEplNCRUYL31ntE9G0pZDcX9iUt_rjpPT8SsYW2eGQlaz10C5G0caVLP3hBtLbGLzctuAx5m9BkAh56I5vmgYaDXZVpVhKQ6unGVvkMv5puCrwt_70O8r7tCtuPvFQ0avnfXWCsQ?key=i-4zDvsgwTb3ZQgDXeB9kw)

## Копировать из R

Инструмент используется для копирования S параметров согласования из вкладки “Объект” в вкладку “SIGNAL”, если присвоение статусов ([_закрытие работ_](https://wiki.sgnl.pro/app/page/1zKM2m_O8NPfp5ETOf5NXd1MkKZfEhWvHyyJyEXGYUaM)) производилось в Revit.

1\. Нажмите на вкладке SIGNAL на панели Согласование ➤ Копировать из R

![image-1688029273985.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXefWhm00NdiHrR1P8i8HzuMTFD_sW9DfJ1rFfDCM9IeWQJoOaBE25KnAHP1xbkF3itVIomZVniTHD0fO73GEMelD12LoPjNyILwaeNzQLGT-5WGKsIm6Iy6i4OKX8ewLYvWZwC7Uz8qIlSImxP0Qw?key=Hmk684qvnczX_w97ZRPBTg)

2\. В элементах, которым присвоены статусы, свойства*“S Completed”, “S Accepted” и “S Planned”, а также “S Work”, “S Unit”, “S Color”, “S Contractor”* из вкладки “Объект” скопируются в вкладку “SIGNAL”

![image-1683289905105.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdZpnoNRIzJc1aMt6ACEobZoRGg5bdR3RGMRKI6-TSG3WkCIzK7iMOAHTiaXxDgnj64jfrYcljtZexOWFnRxEKmrCO_c2V6TSH13UZYPEixsiItfqqVWxYOWgH4Oop3Y3-vR0BjUElmvbLm-sCE?key=Hmk684qvnczX_w97ZRPBTg)
  #
  <sub>**[<   TOOLS FOR NAVIS. Виды работ](/ru/tools/navis/works)     **|**     [TOOLS FOR NAVIS. Расчет   >](/ru/tools/navis/calculation)**</sub>