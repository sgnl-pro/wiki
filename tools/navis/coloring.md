---
title: TOOLS. Раскраска
description: 
published: true
date: 2025-10-01T23:18:33.029Z
tags: 
editor: markdown
dateCreated: 2025-09-21T11:37:48.157Z
---

<sub>**[<   TOOLS FOR NAVIS. Расчет](/ru/tools/navis/calculation)     **|**     [TOOLS FOR NAVIS. Экспорт | Импорт   >](/ru/tools/navis/export-import)**</sub>

---

# Вкладки{.tabset}
## Цвет

> Инструмент присваивает элементу пользовательский цвет. Например, можно отмечать выполнение модели определенными цветами.
{.is-info}


1\. Выберите элемент/элементы и нажмите на вкладке SIGNAL на панели Раскраска ➤ Цвет

![image-1683703231611.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXftZVSYsbzTv4JavvtdVmAwYtUTPkfqbCv9lx_YpcR0dBkfEwKVQ_kjg5K0idMbF09idEiGZDMBTnjs69OZp8MS4PgiHe5RWoJ1QK-rjGeC1MBIoAMv6G_Nn-YsG0GrJew8V_xYjwrCuqEoS5LKMw?key=9lhHUWOQlf7pAmMpb993XQ)

2\. Выберите цвет из списка и нажмите “ОК”

![image-1683703241883.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeLJBUv6CledGkwuRJ-DaVJNY_CmArPv8XuLwIWsYRMC_jIOGsFWkX-TxOhpptRKnLbwNWog4FMdFDhUigFOeDW6P5IpWPlBvS9Gq0BRvNpTbMMMdLWmnxceiICFPja3vwRy32lqeoDG4NRZic9?key=9lhHUWOQlf7pAmMpb993XQ)

3\. После присваивания цвета произойдет следующее:

![image-1683703256080.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdQfbwLZ8Fo9an3FLjOFWjk--Iz2-9HfoL4fCx7FPtQ1ZHUFfS8dJPABoJqXeOfBSn6KuvllhvjE3i-l0iF-G5ByLhDJCSZggDnDYkeOatdr6E02J_eLlBFoCNU-cgsUow_iQ59L_EfW8F5ZetFUQ?key=9lhHUWOQlf7pAmMpb993XQ)

-   Выбранные элементы окрашиваются в пользовательский цвет.
-   В свойствах элементов во вкладке *“SIGNAL”* создается параметр *“UserColor”* (Пользовательский цвет).
-   Создается поисковый набор “*UserColor”* соответствующий пользовательскому цвету.

## Раскрасить

> Инструмент раскрашивает элементы согласно значению свойств SIGNAL.
{.is-info}


1\. Нажмите на вкладке SIGNAL на панели Раскраска ➤ Раскрасить

![image-1683703329757.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXff0YdP3PyrCIu4-MnzLOgnPMJcBxw6HREtwXK4uAltx9UU3ZMZVU1fmStTQiosERMSJ7MG2BmGzGmq9DZ4Mp6S85-3GMYl6jyHiGINXR1D82MtNAuje4L9Y0G348hi7VOVnZSNJMzxbNh30A9iIw?key=frSD_mu7b1S_59XbZcG8EA)

2\. Выберите по какому свойству раскрасить элементы:  “UserColor”,  “Color” ,“IssueColor” или по проценту, и нажмите “ОК”.

![image-1688029304575.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXde5wXuf0UVRJkf3JsxnJQU9P86RDF7A4zR-FnO5UpDg6KP8arsDxSU3OJS8Uh5rmIHzJT6b7OOoj3hY5Fkq0KCVhZ7xicWDkZGUYIDx_o_0oCaUJQLlAqbx6x0kScD15RFMettgoyONLfp5gOtPQ?key=frSD_mu7b1S_59XbZcG8EA)

-   ***Переключатель “Обрабатывать только выбранные элементы”*** позволяет раскрасить только выделенные элементы.

> ***Примечание:*** элементы, у которых не заполнено выбранное свойство, раскрашиваются в серый цвет
{.is-info}


Используйте данный инструмент, чтобы в имеющемся документе формата .nwf или .nwd восстановить раскраску элементов по заполненным ранее параметрам "Color"/ "UserColor"/ "IssueColor" для продолжения работы с файлом.

![image-1683703383137.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXePHOcpuW_ch28nLP5YC_Eg9sPLezrfMx65IPe3p8Z_W0h3IOKPp2HwwIT_z8n5tK5jCpFyaTEbr9wkgkX--PNqzJBxsIchVJcGk7w1WHbj3VAe36DcsnkAfUnMNFg_o8b_ecj5vLPhFvd-rV0Y?key=frSD_mu7b1S_59XbZcG8EA)

Для раскраски по проценту выберите цвета, которые будут соответствовать проценту выполнения работ: первый цвет от 0% до 25%; второй цвет от 25% до 75%; третий цвет от 75% до 100%. Из списка выберите вид работ, который требуется раскрасить. Будут раскрашены элементы у которых на вкладке “SIGNAL” присутствует свойство “P\_{Вид работы}” (см. Процент и Импорт процент)

![image-1688029338144.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdSHqXbQDLSfMW6928f6NOu559npKWFPx0ObrsftlQV_2m03JzfpguB7-AZh95noJznHSz0mAiB1-MByaBxbW7GuXBfS287BzwJ-mFNDfKyZaaLbKi-r27GLL_Eu9yzrohkfpxFQ-EPU1FeOnqfCw?key=frSD_mu7b1S_59XbZcG8EA)

## Сбросить Цвет

> Инструмент сбрасывает цвет элемента до значения по умолчанию. Значения параметров “UserColor”,  “Color” и “IssueColor” при этом не меняются. 
{.is-info}

1\. Выберите элементы и нажмите на вкладке SIGNAL на панели Раскраска ➤ Сбросить

![image-1683703441540.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfzn--_7nV5Nl6Kza8ASEoB7ktufFiuUPMi_amA-skmxyvGzQh5tGjcK5ZGEm-qYUpegukZLzBax3qXjSmNJKoTXVbt7my1Fha8A2o64NqYRaWUqeRlSIYa8sEvX9_aOAPjAV5VfQh9CWCSnjfA7A?key=AN5uMck6SoiwAH06V6D7zQ)

2\. Цвет выбранных элементов сброситься до значения по умолчанию. Значения параметров “UserColor”,  “Color” и “IssueColor” при этом не изменятся.

![image-1683703455706.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXezVR_kHh_T3lE1ebfjo4JFYZHg9helWQApItaRDEvC1kseRZJ2-7PcXgk9ayFLP1yFyT6PyZhVhMJ_pdpiqIbEnhEiqa0nSqAxa1aeTqGKWFG2g5XapsBG3nC43kR3k71WpEgG9t3g9He-83iOEg?key=AN5uMck6SoiwAH06V6D7zQ)

## Статус B360

> Инструмент обновляет цвет элемента согласно его статусу в среде BIM 360 (ACC Docs), полученного по ссылке, указанной в свойстве “S URL”. Используется, когда в модели пропали цвета замечаний, но остались заполненные свойства “S URL”, по которым возможно восстановить цвета.
{.is-info}


1\. Нажмите на вкладке SIGNAL на панели Раскраска ➤ Статус B360

![image-1684480270521.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf8a9xDRLXsNmsS48-Kurjr7cQAFSrJF-Ij4AvSsjNlPo6d48C90iSaEArzgSE5sFSpSZsWgSDXaLOIykBjdcZeJVkBcDLVkfqHRphvKR4cqxswxG3kbhuj1aJkRnOOvZjNZ_PzN0x6poLDgiG3Rw?key=gYDv60j7wn26JtHz0aSLHA)

2\. Нажмите “Получить данные”, чтобы получить данные по замечаниям из BIM 360 (ACC Docs), а затем нажмите “ОК”.

![image-1684480283631.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdNriafGW9tL_OIS-XP8kUoVLcFMjLSvGv-F3djSukKxoGs-mVcs_n8VQfIQy0K4zdV-HPh9xPJqUCqlv9rofUbpMjbhhfUNFq35Xd4gqkQMifjX84mHHqIGjPoFBStQAqqcv8Hjv-ClY5Oionu?key=gYDv60j7wn26JtHz0aSLHA)

3\. Элементы будут раскрашены в соответствии со статусом их замечания в BIM 360 (ACC Docs). Соотношения цветов и статусов задается в настройках [_“Раскраска”_](https://wiki.sgnl.pro/app/page/165fGF2LyUPst6ZWaw12UnxbiSHVFcoz_XI6Nh9hozdA).

## По параметрам

> Инструмент позволяет раскрасить элементы модели по указанным свойствам
{.is-info}


1\. Нажмите на вкладке SIGNAL PRO на панели Раскраска  ➤ По параметрам

![image-1683727168417.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd1x6Rhckp0LvSpbrn_jX1VYHLeQRY4_PpWSqsxl8F_XSUBWmJH8vMmiY1dFWAuwDhLfYVR_FFLRxz0z2Ny-OIKE0lEfI7Fv0xXuWTwwEjJlIXN_JC_NOlg95SdIo5CsFLBuXbnZv2wVFwif_6s?key=-YzvzEBSIhsCzI_kuEgzRg)

2\. Откроется окно с настройками раскраски. Добавьте свойства вручную или импортируйте файл Excel, и нажмите “ОК”

![image-1683727192532.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXff6FSzWQAON8ctJ_S-AYKn79y0_q9PMpam0Wv7RmEg-hInrZbc6K46EQ8eVPJ3xEjb6-XX-zCc0WACJM49eKLyz7fFiFpY1UNiWbPFKqgn48zPSAls4Xkv9xbfjiqcsFa4xSCk2tW_xf33YoyWHw?key=-YzvzEBSIhsCzI_kuEgzRg)

-   ***В столбце “Свойство”*** укажите пару ”Категория-Свойство”.

![image-1683727248523.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfaluJyTmY26M5AK3fa1iPPa9PmXyccf1117fqnhV_GmNX0WOajMjvP2hbI7iwV4iEez3XI9H1K1pfP6sa1_KjulXNu9HpzAhB0CLUccZ3Qa8A5c_1VkFnQOzdWIhLl5W9pVccDp3bwOxBqekveRA?key=-YzvzEBSIhsCzI_kuEgzRg)

-   ***В столбце “Значение”*** укажите значение свойства, по которому требуется раскрасить элементы.
-   ***В столбце “Описание”*** укажите описание для поисковых наборов.
-   ***В столбце “Цвет”*** укажите цвет, в которые требуется покрасить элементы. Цвет указывается по палитре RGB через дефис, например “252-82-3”.
-   ***Переключатель “Создать ПН”*** позволяет создать поисковые наборы по указанным свойствам. Укажите Имя папки.

3\. После присваивания цвета произойдет следующее:

![image-1683727595295.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeZLZ0j_oiQkne3im04AxdHgWrZS3nhPAz8YdC_Z2ctSdjixjOeo6S16mcwV4d5mWV6Q7kSIH_iThWEUQ3b6oQrJHwKzKIM6W2waZfqJ0S8Q3XsbQU5BP_hgMgiW2SMUjorgoj3Fly2dqZRr9r28Q?key=-YzvzEBSIhsCzI_kuEgzRg)

-   Элементы окрасятся в цвета, указанные в настройках
-   В панели “Наборы” будет создан ПН по указанным свойствам

## По наборам

> Инструмент позволяет раскрасить элементы модели по предварительно созданным поисковым наборам
{.is-info}


1\. Нажмите на вкладке SIGNAL PRO на панели Раскраска  ➤ По наборам

![image-1683727632468.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdldMw21JV3WKftBwFvTddQ4Wr5rkOVE7DrA1J20ZSymy2nBuF-EaTF4GfLTLKHo6pYRCgYHDyW6Ax0Jq27-tdPinto67rDsZjVMRJ4Wi9KwQ7h_uBdJoz-nkPSpE4CUA-oqXjCN6cY_AGgCiIO?key=XMH0iYHEflHj_Yg5tgZfCQ)

2\. Откроется окно с настройками раскраски. Нажмите 

![image-1683727641942.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeaRYW-phfPb3zur7xLGDJ0CtkWGpsHEajd0IlTWyBD6VBKYidysJi9dBROmr1xGeC6o1zsqZtirlayK1Xrw7DV4lm_XqZeCpSjLNBUTvs3OocixfqFLPYad0IWf4JoM-yIRsgl_gC91wAVe3pCXw?key=XMH0iYHEflHj_Yg5tgZfCQ)

 , чтобы добавить поисковой набор.

![image-1683727656487.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeH67qNdKRgrLQjL-iHbzh-pCyUy98hS2BHRQdOhY97ITzv-SqWPkSlBYhE4fksauh6gf7Y9kPVkoA6TB-sDmE9FRPo0Qtm_HeHG6Llukcrbcrsk7-qR2J6hz1TJf26Ydek_FE_sBuV6irGG9pc?key=XMH0iYHEflHj_Yg5tgZfCQ)

2\. Из списка выберите предварительно созданный поисковый набор и нажмите “ОК”

![image-1683727679140.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc-tnxhdODkCwmNptxTCCbAujSH8cFfCZhhZAX8LfNCpv1ikKY5l27RKdeRo7vOQLV_JHEC0vZVG46j9-BcC6Ucr9-MPEFr1Tkj1u9W_ODGWuBw9VEfelX9xFOkDBASpfxsa0akzr-XsYQUhuiaow?key=XMH0iYHEflHj_Yg5tgZfCQ)

4\. В столбце “Цвет” укажите цвет, в которые требуется покрасить элементы, и нажмите “ОК”. Цвет указывается по палитре RGB через дефис, например “252-82-3”.

![image-1683727729260.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd_G0aneXKk6lXdrehKCLTWkv6xY5Lg_051Ge-bqnffX_zYQGEK_u1cKd3OVs-Ps_EkvSyMEu-bBOaqcIT2Z05Dd9Xol7rqu6jEXychnfTt934BUw0_1buMEnEHrpbjrtYLgsc6fNqJMIsTvvHjBQ?key=XMH0iYHEflHj_Yg5tgZfCQ)

5\. Элементы раскрасятся в указанные цвета

![image-1683727741068.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdu8f25f7kGSPzjhJv2vFhna81ypRX8_cv5oI0hc4051lB6n6rv0o3n8tw-7Ph0_7faxSKJbSls5rs-Nz4ztsTBFBgHOyN7ke-rf4npjcxscjRsetrAsdtitzXeHvAkQl5L1zrdcinyH9rA0SGdKg?key=XMH0iYHEflHj_Yg5tgZfCQ)
  #
  <sub>**[<   TOOLS FOR NAVIS. Расчет](/ru/tools/navis/calculation)     **|**     [TOOLS FOR NAVIS. Экспорт | Импорт   >](/ru/tools/navis/export-import)**</sub>