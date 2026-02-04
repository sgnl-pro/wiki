---
title: TOOLS. Checker
description: 
published: true
date: 2026-02-04T14:16:00.513Z
tags: tools
editor: markdown
dateCreated: 2025-09-21T12:01:58.429Z
---

<sub>**[<   TOOLS FOR NAVIS. Свойства](/ru/tools/navis/properties)     **|**     [TOOLS FOR NAVIS. Проекты   >](/ru/tools/navis/projects)**</sub>

---

> Комплексный инструмент, позволяющий проверять модель на наличие свойств, заполненность значений свойств, на пересечения (Clash Detective), наличие элементов и т.д.
{.is-info}


Нажмите на вкладке SIGNAL PRO на панели Проект → Checker

![image-1684131979882.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXemH-0zmYNVCEGsCH9nD9dUvZPMypTpfCEzww2n9lmrQ1q5mKANSUYS8Yr5CcvTbh8oqEP9Hg41Jper5kvUmsDILT8lPhg6McpWkAOncLn2ijnJuC1cusVoHlrhF4htJVIzxDAYC5MRbmnEYpm7uQ?key=kvd51ahbWRxAG7mrOPv7NQ)

# Вкладки{.tabset}
## Окно Checker
Окно Checker разделено на 3 зоны: проверки, правила и результаты

![image-1684132005497.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfU_Ozp11RkFBGrn4ZcPZppQTREgk5MoIPj9FHao-cmdl1Q7Jefwh73-X1_1GMqIedwOAjB8XX7IYZftCRppiKO5hT7oyKHD3ubRKBv8e_xUIGBuktRzxZa2d6iknmT4pJJU_nxyvu9cRcgN_kBoQ?key=kvd51ahbWRxAG7mrOPv7NQ)

1.  Добавьте одну из шести проверок, нажав  .
2.  Добавьте правила и запустите проверку, нажав “ЗАПУСТИТЬ ВЫБРАННЫЕ ПРОВЕРКИ”.
3.  Просматривайте в модели элементы с ошибками, чтобы составить замечания. Выгружайте результаты проверок в Excel или XML. XML можно подгрузить в Revit , чтобы быстро найти элементы с ошибками и исправить их. Сравнивайте результаты с результатами предыдущей проверки, чтобы увидеть, какие замечания были исправлены.

### Вкладки{.tabset}
#### Зона проверок

> В этой зоне отображается процент выполненных проверок, количество элементов прошедших и не прошедших проверку.
{.is-info}


-   **Нажмите “Добавить проверку”** , чтобы добавить одну из шести проверок
-   **“ЭКСПОРТ”** позволяет выгрузить в XML все проверки с их правилами. Вы можете отправить данный файл с проверками своим коллегам.
-   **“ИМПОРТ”** позволяет загрузить XML файл с проверками.
-   **“ЗАПУСТИТЬ ВЫБРАННЫЕ ПРОВЕРКИ”** запускает проверку напротив которой стоит галочка.
-   **Переключатель “Проверить только выделенные элементы”** позволяет проверить только выделенные в модели элементы
-   **“ЭКСПОРТ ВСЕХ РЕЗУЛЬТАТОВ”** позволяет выгрузить результаты всех проверок в один Excel файл, который можно передать коллегам для исправления элементов, которые не прошли проверку

#### Зона правил

> В этой зоне создаются правила, по которым будет происходить проверка.
{.is-info}


-   **“ЭКСПОРТ”** позволяет выгрузить правила проверки в Excel файл. Данный файл можно дополнить правилами и загрузить обратно в Checker или отправить его коллегам.
-   **“ИМПОРТ”** позволяет загрузить Excel файл с правилами проверки.

#### Зона результатов

> В этой зоне отображаются результаты проверки в виде названия элементов и описания причины, почему элементы не прошли проверку.
{.is-info}


-   **Нажмите “Выбрать все”** , чтобы выделить в модели все элементы не прошедшие проверку.
-   **Нажмите**  рядом с результатом, чтобы выделить в модели один или группу элементов не прошедших проверку.
-   **Нажмите “Сгруппировать результаты”** , чтобы сгруппировать результаты проверок по повторяющимся названиям элементов и описаниям результатов. Таким образом, количество позиций в списке уменьшится и будет проще посмотреть в модели элементы не прошедшие проверку.
-   **Нажмите “Экспорт результатов”**  , чтобы выгрузить результаты проверки в формате Excel или XML. XML можно подгрузить в Revit с помощью команды “Результат проверки” и посмотреть в каких элементах требуется исправить замечания. Также после исправления замечаний данный XML можно сравнить с новыми результатами через команду “Сравнить”.
-   **Нажмите “Сравнить”** и загрузите XML файл с результатами предыдущей проверки, чтобы посмотреть какие замечания были устранены.

## Проверки Checker

![image-1684132695289.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf-PQhZuQURgLeeKuOVVF97khG4jvGRXU3_RG3xNQT5YcCKKGXg0U9oQb5Wp26f0Wyd02kl2mMahRpGjKHm_TWVIs7ks3v1sGQsXDhOoXaQkauVqs6nbC-_MPg9eICuiOo8UfxVd6wGQXKJsoGMeg?key=kvd51ahbWRxAG7mrOPv7NQ)

### Вкладки{.tabset}
#### Наличие свойств

> Проверяет заполненность значения проверочного свойства. Подходит для проверки свойств, которые должны быть заполнены у всех элементов модели.
{.is-info}


Например, проверим, что свойство “Код по классификатору” заполнено у всех элементов

![image-1684132773060.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdAp9qbLnGXthtqKWxZmhFt_lm1HrLDysvEC0lEuXPz2N12om9a1GMadapgX9bVHOAx_ldv-YYDgCgI3-UeHpUCh5CzD49k3ctBVb5h6FW1qzOlbfZXLWcuWq3AM55xI1mHLWks-nd96AfcEAm_3g?key=kvd51ahbWRxAG7mrOPv7NQ)

Добавьте свойство в виде пары “Категория-Свойство” и запустите проверку.

![image-1684132785866.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeXA3GWjguPWrCClsLtVCWaCITVAEIsHNB3Qkiu0fAQPw9qEbhgIMeg9Yphsrux0h60nom2CtESpubUilHgHrmN26pO2nlWlKFNrKbeRYxZyagSMQ0wvRFqnYxKuBnZhQTiGvvpX6ajWS-os5Ko?key=kvd51ahbWRxAG7mrOPv7NQ)

#### Наличие свойств для групп элементов

> Проверяет, что у всех элементов модели, содержащих условное свойство с определенным значением, заполнены проверочные свойства. (В данном контексте условное свойство - это свойство, которое задает начальное условие: Если свойство “Категория” имеет значение “Стены”. Проверочные свойства - это свойства, которые проверяются на наличие заполненного значения.)
{.is-info}


Например, проверим, что у элементов с кодом классификатора “Е2.4.2” и “Е2.3.1.1” заполнены проверочные свойства ”Этаж” и “Корпус”.

![image-1684132830198.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXckfQB3w7Khuy172EWhQOuCDNKDWoE9jt71sca76xISN_ceSO5iJg1nLh5q41nnUSLo-y27nMajbcse5wH6WaeDBxcpDFgpqgBtZSD4ssOS3SgMThbJMGA0nq5sRflj5fDdJ8WFFPXFOOK8c9BHGA?key=kvd51ahbWRxAG7mrOPv7NQ)

-   Добавьте условное свойство в виде пары “Категория-Свойство” и значение данного свойства.
-   Добавьте проверочные свойства в виде пары “Категория-Свойство”

Данную проверку можно запустить на определенный поисковый набор - выбрать его можно нажав на “Наборы” в верхней части зоны правил:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfgPJbL_Jzi2G6LzZx5XGcurHhOMEPdn7iOfWZD8TtBfm-2W7CLPgjqrBQK8RjA9Q1t0yudEF6LOAja_a6fZ9fKtgPJ6eFortU0v9-VvvW6BP9Jtqdeg5xfJJ88aRsbNYu6JBfay7NuToISuwDp?key=kvd51ahbWRxAG7mrOPv7NQ)

По умолчанию проверка запустится по всем элементам модели, либо по выделенным, если это указано перед запуском.

Правила к данной проверке удобнее создавать в таблице Excel:

![image-1684132862233.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe-XVxO_4fN4zC8dF3UER6cREfo5ugCdI4mm1F_sUyemeel6mpEF-TXcDQl9C0eVa7e8KpQq3lCTO5gs3eEU7Wk2f1QgTHVUOTKwhwl8KPH-t6WVCEn8qzjE13Ssv_HHGD0Xk-MYkdXQsI1G9A_aQ?key=kvd51ahbWRxAG7mrOPv7NQ)

-   В столбце A (Правило) перечислите условные свойства в виде пары “Категория-Свойство” через дефис без пробелов, а в столбце B (Значение) укажите значения для данных условных свойств.

![image-1684132871159.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcWcTjcV2e8OOyaUjM4KK7kZ4LrsrPtyVK5i9WnyU_5I0Hykwkudrhy1eGa_aIbWw_ZyCOf9ze3NeCh7E8Up3HjndjHg0CQsmHvXiLCtZAMCXHOMj4-wriYl5C62pZX8acnJySJtyW5BqPR_L2ZZA?key=kvd51ahbWRxAG7mrOPv7NQ)

-   Далее в строке 1 начиная со столбца C перечислите проверочные свойства в виде пары “Категория-Свойство” через дефис без пробелов.
-   Затем заполните ячейки в матрице любыми значениями, например, “1”, чтобы привязать проверочное свойство к условному свойству.
-   Таким образом, получится: “Если свойство “Категория” имеет значение “Стены”, то проверить на заполненность свойства “Имя”, “MP\_Корпус” и т.д.”

Также можно проверять по другим условиям, например по Коду классификатора

![image-1684132887998.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfogA82mee4glJjx70R5QV54wVP6nYoL2HWhift0Ixea7-e4reW1DgUEYHV6GRvMvTShSDcFHvMWZT2ZHW6J08oLtHjY4xgX_TRFsYpX92cJ77kWHz2U5q_jzQjFfe_GMzhxIQwt_74qN12yGdMKg?key=kvd51ahbWRxAG7mrOPv7NQ)

Шаблоны можно скачать по следующим ссылкам:

[_Checker\_Template1.xlsx_](https://wiki.sgnl.pro/app/page/18CaGLQx_pwteleJBblnEP4OxQD4592Cd/view)

[_Checker\_Template2.xlsx_](https://wiki.sgnl.pro/app/page/1YO38qsLTx3pybIGwhqkzlFwEkDIUKHQL/view)

#### Наличие одного из свойств

> Проверяет заполненность значения проверочного свойства, при этом для каждого проверочного свойства задается отдельный список возможных вариантов свойств. Например, когда объем может быть в свойствах “Объем”, ”Volume” или “Dynamo\_Объем”. Если хотя бы один из вариантов имеется в элементе и заполнен, то проверочное свойство считается заполненным.
{.is-info}

Например, проверим, что свойство “Объем” заполнено у всех элементов

![image-1684132967322.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXejskksH4kEidz_K_h_DybbUO9C4dy9C8Tm-qLguGBn1TKuh45PX99RwQrYVO_UPYITzoqI0r6u09jFLyPVM-lLLNUKFUwOfBBHgJ_22SeQSfQ-7qKHpZWdXdKpsdTrrUL-BsmOds3KMGq0y-6CBQ?key=kvd51ahbWRxAG7mrOPv7NQ)

Добавьте свойство и к нему список из возможных вариантов, где в элементе может быть указано данное свойство. Свойства указываются в виде пары “Категория-Свойство”

![image-1684132979590.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfD-z1hCdMLLOrTQLAq1JX7_oT3VI4uwQ8vIFMqxupA5w3PXbnvOk04vNCeRkY8JPggkeKtbQvBgw0M8NWM6xBL_dF8W3gzDRdZOX61dBS_SVWrzN4nO2QbLRvvV8dFXK5HLuirSQZc2L1I5Mw4KA?key=kvd51ahbWRxAG7mrOPv7NQ)

#### Заполненность значений свойств для групп элементов

> Проверяет, что у всех элементов модели, содержащих условное свойство с определенным значением, проверочные свойства имеют конкретное значение.
> 
{.is-info}

Например, проверим, что у элементов с условным свойством “Категория”, имеющим значение “Стены”, проверочное свойство “Толщина” равно “0,200”

![image-1684133015961.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdO-BGrwSPPnXCh5bqxMIYvJ048AEk0KKaLH1xcsyB8_xiua10nu6VV1oixRuyUnidTk0WBZsajPMAle03fZZR5G8sWS1V2aVdgQlyxYbyHKBoFUkn2yGuSCnkCbIPoSWKJx7RqsGF4w-teLdoo?key=kvd51ahbWRxAG7mrOPv7NQ)

-   Добавьте условное свойство в виде пары “Категория-Свойство” и значение данного свойства.

![image-1684133032765.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeOn9mNwctKgpQ_EB3rHcfxWKEEkV-_JW1jzO8aSGOack75PS8DpWpN2GcrAZ-Nu8SfNGB_luNCfkXTD9ccXAB2DriIZ6ufXAtrRKBvrsowsBe8EVMQlUkHN9sXULXwy4QgalA_tq77UkDCCxoxsQ?key=kvd51ahbWRxAG7mrOPv7NQ)

-   Добавьте проверочное свойство в виде пары “Категория-Свойство” и значение, которое должно быть у данного свойства.

#### Проверка на пересечения (Clash Detective)

> Проверяет на пересечения созданные поисковые наборы. Можно проверять элементы на пересечение с другими элементами или на самопересечения.
{.is-info}

Создайте поисковые наборы с элементами с помощью команды [_“Стандартные”_](https://wiki.sgnl.pro/app/page/1TeixpZM_MDT9NRCwhePfMF83tnNJ5UYsHEFLyEFy19Y), которые требуется проверить на пересечения.

-   В настройках SIGNAL создайте [_"Группы наборов"_](https://wiki.sgnl.pro/app/page/1Ag6YjZ3SxSFDHC1m0dE30ckAds75MNJjgSHdjHcVwHc), в которые добавьте ПН с элементами.

![image-1684133086316.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfe4wL_N1WsdLgqDoqRKGv8RooiQjQSbj1PAIDgWdcH7EfOjkStxkj0XKkSrJRrVSVqMQ-phiiqkRPc6tu3IZQ26cz9FHnvGmsGSU4UxiO08rMjWwY4iEo4t5smmT3nypZkp3uKNhbT2MNmHWtFdw?key=kvd51ahbWRxAG7mrOPv7NQ)

-   Добавьте группы наборов, созданные в настройках SIGNAL. Для этого нажмите , выберите группы и нажмите “ОК”.

![image-1684133110782.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcSQ_UXM8_bqQiV3e4rmO7LENWMZvGel10LFk6uBcodSczbXnmbYXCojXuFOmiB0Z-N1Jo4up6Zu6YvSg-hnoXg29y3cJ1nZK8y0EuNRpUlMBX8sc9fHq3KJMBCIHGy-DondDpMgfnfGqONUzBj?key=kvd51ahbWRxAG7mrOPv7NQ)

-   Отметьте галочкой какие группы необходимо проверить на пересечения и запустите проверку. Например, Шахты между собой, Шахты с Гор. конструкциями, Гор. конструкции между собой.
-   При необходимости выставите допуск на пересечения в мм.

#### Наличие элементов

> Проверяет наличие элементов в модели по заданным свойствам.
{.is-info}

Например, проверим, что в модели количество конвекторов составляет 1050 штук.

![image-1684133476886.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcb6rUQiOouoKeIrfqjFmegLelxILssZH4Q4FoDD5GYxDPvl38I6cb2L9JvTUTDwdx1d0kyFka5KgZn7jlTw6x7Agtm5BWCBl4xCSO3wr7gbw7moEmUgGpw9fc1mpC_Q8g6V7VrgSurp02T5YZHwQ?key=kvd51ahbWRxAG7mrOPv7NQ)

-   **В столбце “Свойство”** запишите свойство, указывающее на элементы, в виде пары “Категория-Свойство”.

![image-1684133498348.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeBjuw02RgQE6HyaWxMJ9CeC_flaNmgCPI8gJd3OxEWTT90OOCCs4IfGnMlvOnWhRekW-vYlK1zAscwbKn2VFF7YPoXM2D-srOnc2sCfnTvcY6m_wMCbCWziLyqzulfo2GWiWHYS7dHF7xUiNqh?key=kvd51ahbWRxAG7mrOPv7NQ)

-   **В столбце “Значение”** запишите значение проверочного свойства.
-   **В столбце “Описание”** можете добавить описание к свойству.
-   **В столбце “Кол-во”** запишите количество элементов, которое должно быть в модели.

![image-1684133099740.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfTwtvfFO4S0Z-5ce-UUuhyav2gHsgDRVIwekbf6b533JZ2rXlcKvlHyRHYfq35ER4x8BcICM0iFOGLcMe_QIzdUzXC1ZQakeTCjDLRaZS56qClRjO4G6EDk-KQpDX4nko6hMJYb-l7Cb8u3o80hA?key=kvd51ahbWRxAG7mrOPv7NQ)

![image-1684132647623.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXczpSkfWWen4HXnpFCYfcYeBFNJo58cA47gmlprNef9OaxZvU2K_3rBj7dpp-PB-Slu7Yo05jEmCFSvKfcsVuDbtV21OWFVg3ojMlwjHAaCjeKPfaK8hVia-nZ5GmEC4polQBY-NIURduMMx4Gmeg?key=kvd51ahbWRxAG7mrOPv7NQ)

![image-1684132638045.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc0_pDGlXzt2_PsVB72cmwBBHxSM0WWZkG_-eJu3C4AAu4rpz_6nOSM6H7qxcHRlr2iXP3x66Fd0VZvg_QloZh62jMT54GF4d0HygIy76nv9UvwUPMnaxjGrdMRLO3nCKZLLXq539oMWIQPY_xP?key=kvd51ahbWRxAG7mrOPv7NQ)

![image-1684132628317.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeaS8uYYf0luWy0ZeVpzfG3uiBowMln3P5gSZxUPYFJXxYywdYeg1-7HzcfioFkeNnu9W3NBzzYhCjmQ1tkrIHIvgg2cFR9aN19wsmH6iDjFeyJXzY4INEPtkEAC4hkFBRYjqj3R5wNv9DVf71pVw?key=kvd51ahbWRxAG7mrOPv7NQ)

![image-1684132619714.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdQYMme4Q5xdgXimPBYImSga1ZV9N6dYnCGzobE-VvklOTE6JrLUwPYmry0SUyTL0HMBJGSxuP9RuL-X6SvA4a6CCA2eI36aRaDclJuU08jQxHDj3gsQs1hv48JS7ogPDJI6Ne0hrW5xQp7lR-R2Q?key=kvd51ahbWRxAG7mrOPv7NQ)

![image-1684132609516.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc4A-f2hZlsnoGGtKzXAaTPAYqYvNtWVEHPTtmD17Rq6vrcyMJSGWjEKmRfLRTLsm64fRrPUd_R2jbtxbRd2Sc2BtZyVIFRyViCLH6xuXopUhU4W73SZJ4sieIBdQExo-PxRU7Zt1eRdBf9uXHLPQ?key=kvd51ahbWRxAG7mrOPv7NQ)

![image-1684132146482.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdGSgY_3Nr_xRv342Br82046Y_QQJXpk3jSIlRpIAzvdh34C92HfYVh2RaWq0JWnGpNB3yPTI1RwbNIY_EoFdXt4BzJUBn2SqzO10O1zlWC9JNAy0wt8sjciTQnnCudAXrdiAVTXmz3HrYhV0QRQQ?key=kvd51ahbWRxAG7mrOPv7NQ)

![image-1684132146482.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdxLA7WVQjA4f3fKZJdlYhslAxkn0yc2KXokzDvm8CGPlOiUB4RTk2gorR76ohp2pPs4YQuH7HlLEqNexDjOc7k3It_YbEUtST0vjirf2Uqza_Is-KHzdPMYUAnzUUHd18jDLBqnSmf5WFTdi1KmA?key=kvd51ahbWRxAG7mrOPv7NQ)

#
<sub>**[<   TOOLS FOR NAVIS. Свойства](/ru/tools/navis/properties)     **|**     [TOOLS FOR NAVIS. Проекты   >](/ru/tools/navis/projects)**</sub>