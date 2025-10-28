---
title: Методология работы со строительной моделью
description: 
published: true
date: 2025-09-18T14:14:43.017Z
tags: 
editor: markdown
dateCreated: 2025-06-26T21:34:32.884Z
---

## **1\. Подготовка файла строительной модели**

Перед началом работы с строительной моделью требуется создать файл Revit по шаблону, подгрузить в него проекты, по которым необходимо вести строительную модель, настроить виды для дальнейшей работы.

#### Работа в Revit

1\. Скачайте крайнюю версию плагина [_по ссылке_](https://tools.sgnl.pro/?tab=Plugins)

2\. Скачайте файл (формат .rte) шаблона Revit [_по ссылке_](https://docs.sgnl.pro/s/f/4d8f615a-27fd-4b1a-a631-c7529eb99f03) 

3\. Откройте Revit, выберите “Создать” новый файл. При выборе шаблона нажмите “Обзор”, найдите сохраненный файл [](https://wiki.sgnl.pro/app/page/14ugCPXTGnBl3AaT-JTpKSRflcLZRZ-cb/view?usp%3Dsharing)шаблона, формат файла обязательно должен быть .rte, нажмите “ОК”.

![image-1691587535997.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeOsU4s9QkNwIvLSYnnxulXLauzgJFHIqDsUGiiefmHh8sdCczdmn7-2Bs_Ua_4YmGAek3IvoArTFqT05zatBKM9LiSwV7fQte82FEB0QLzngyQzOkZFYuA29jvCDeSHAyDuIcjbKwVlvushyN6?key=C1Q208mvu67IIZhzUVfjzQ)

4\. В новом файле откройте вкладку “Вставить”, нажмите “Связь Revit”, выберите файл, из которого Вы будете копировать элементы.

![image-1691394572790.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc2Rlr_MZqhdNZutov2k3cqKqLGpq7GN755_M4ie3bC3xKvNF_1jxWK1mKeNEM3wRomyJWJ5kQvFKGXxS4hqslmTObnS1iXeUGzEi_2jKvnUcLlND4PlgWhGx4M6C365H5zrY7wjbG-NVxeOAOt5A?key=C1Q208mvu67IIZhzUVfjzQ)

5\. Если Вы загружаете первый файл связи в новый, созданный по шаблону файл, обязательно выберите вариант размещения файла “Авто - От базовой точки проекта до базовой точки проекта".

![image-1691394591693.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdittqTf8tLu97uAggPSw6afo-GsU5gVWn4ZvDcWrb1fYP8jKQ0c4FbK1M2MYfmxbrZhX-eIGbZ5417Fweon8psclMZ4QWocwnFSxNeFerEmnNvVyDGKqsQVBI5a_EqrnhQRXA_X09lLE_x6DNiwg?key=C1Q208mvu67IIZhzUVfjzQ)

6\. Если появляется ошибка о том что “Вложенные связи не найдены”, нажмите “Закрыть”, чтобы это сообщение больше не появлялось поставьте галочку напротив “Больше не показывать это сообщение”.

![image-1691394605343.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfxe89G7xo3ybUMLGMPZQgi1cDJXHogFVFjvs7ToLsiYKmo0TqW1bvqSvV5BMFnik-AivyFsaZtgx-1llyuCGPDelI3bbTWEIQpMey7Xo41bX35jIrvvMweLuogD2N6BS6ZUrjwf_ZYahJfxQWUhQ?key=C1Q208mvu67IIZhzUVfjzQ)

7\. Во вкладке “Управление” - "Местоположение проекта" нажмите кнопку “Координаты”, в появившемся меню нажмите “Получить координаты”. Наведите курсор на модель из связи и нажмите левую кнопку мыши.

***Важно:*** Получить координаты модели необходимо вне зависимости от количества загружаемых связей. Даже для одной модели это важный шаг

![image-1691394615876.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXes_GC736uswtqE2Fn_1LhSdbziKuMGtTvMndmK2BkaLRPoEaegqxgJQopYD-LqsNHDN9T99Df7RPKKDMYaSHW4F-sloHYbmioRXXG3XIooFlGn2xr0yNfk7osn4VbeGt5UPon6wqsk2a1WtvLntg?key=C1Q208mvu67IIZhzUVfjzQ)

8\. После того как координаты получены из связи, загружая дополнительные файлы связей, в настройках размещения необходимо выбирать “Авто - По общим координатам”.

![image-1691394625838.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcnLsCeA0L4Psxc1xLSQIixnxxAON3HseESl08mWmM3Jql3wQsqoLoYRDoCee1LTVFPuI1Hxwo76iCdUOJy8GF-kEAFEplqyb0N2Zc94PENaYaggEkpJ14UYHtAgCO2QR6eq2FIAAH98Whf7NZEEg?key=C1Q208mvu67IIZhzUVfjzQ)

Если совмещение по общим координатам не произошло, значит у проектировщика не настроены общие координаты для файлов. Нажмите “От базовой точки проекта до базовой точки проекта”.

9\. В новом файле на виде “1. Копирование элементов” в правом верхнем углу окна нажмите “Вписать”.

![image-1691394641181.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcR4moS9grPn_XMXcVDgjE-iKYrjb5303bW8ndujDOHnZTc7fvrio99aQmKGyH-VcszG4aXnzX6pMvLTYkCtip16FjXZie8bdgrt9LhQkHa-7fOPk1a7h9q5Us0dO1_8Y_3NeiggwLBmoD4DG9Dvg?key=C1Q208mvu67IIZhzUVfjzQ)

10\. Выберите появившуюся связь и во вкладке “Изменить” нажмите “Прикрепить”.

![image-1691394651257.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeQpY7cIdYQHCDjQlVQk2Pkb-NibmwZsiud2IRvL8tnsQmIxMv-3oahe3uoNSVusx8gXt1a5Ni80CKd59DAMulJ4ogmdAuLjL3JjjqX1JE-6mr4-lPQWHl79N89SD3EAPkvasO72NRFd7BmOSwRyQ?key=C1Q208mvu67IIZhzUVfjzQ)

Повторите со всеми остальными связями.

11\. Когда все необходимые файлы связей добавлены, во вкладке “Вид” ➤ “Шаблоны видов” выберите “Управление шаблонами видов”.

![image-1691394664981.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdAmmQDEWgxrl-KOvmzvAsNeWptcaC2GNWl_ICx6rRUMoZPeXJgz6SnuUQ0CcNWsYzQi4wCQSUImPyAl-IWC5JIhdd9xbh4lqv9hURCJi7aWl3pIKWEAUSGoabYo65bPIvnFXSeAmh2ysXCZeDuxA?key=C1Q208mvu67IIZhzUVfjzQ)

В открывшимся окне для Шаблона “1. Копирование элементов” для Параметра “RVT-связи переопределение” нажмите "Изменить".

![image-1691394675722.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfv_cq9huM4pxqQQNdGYBM_Eh38kvJytX7qNGj6ejjQNjAN9waqNZ5OL9CV1cciKU4uKXFpBl9LtmMvho4JV7qn3Sug3uEUfUowRqKWXy_HkymL3NmfQSMTEGPukCBeUvXSX-0L62Bs8C2XpIAfpQ?key=C1Q208mvu67IIZhzUVfjzQ)

Для всех связанных файлов, включите режим “Подложка”, чтобы при дальнейшем копировании элементов можно было отличить скопированные элементы от связанного файла.

![image-1691394684437.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdRA_enGkHVmsparvT1Z4-woQUUfZxUiNEGGJU_nMf53nsiseAzIaVUOZf-JBhBpgulKEP3MXR3E_RN6-v9NtartLAPcap-6_IjbUUix6qvS9WFCN2PyXdHSxsh8QKxiZ7RHztk79K9qHnAS0Eo9A?key=C1Q208mvu67IIZhzUVfjzQ)

Далее для Шаблонов “2. Создание элементов” и “3. Строительная модель” для Параметра “RVT-связи переопределение” нажмите "Изменить".

![image-1691394694050.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdUfkB6C6IG7x3eAiNrZu8Yh2HB39HHn9GJgOhnVO5gd1iVeC8vhL0W2EUSBdQo9ZzyndfYpbU0zITC-n5sXKLSqNmvIN733REtHANK6SaRaVHxeV1erzkIOKnW6fy2ZrukjMm0JcXjHYe17s00gg?key=C1Q208mvu67IIZhzUVfjzQ)

Для всех связанных файлов, отключите видимость.

![image-1691394712880.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeFrzuYz-eEc2KQDG9SlM3SIJZrciI9aGFwJEXPV_B_dECZBpF7l1IJRUXUN8S2hD8h2ASAwyP2pyfBcTSiDV6BiwLOpb_In_j-n69sje9PscX1WhhkHjN3s3eIfMYOYKT_an__bxCCYzsrCLpb?key=C1Q208mvu67IIZhzUVfjzQ)

![image-1691394717516.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfDOfyWpE9SLqXaBF3kAmvSSXf9Wzgb0_3KNiLxSDCFlZ7jK0C2DJ5UqPlWhA8lcQC19QPc5asCNAfxb3MOXPRpy1tdRdjl07qPFCP0KiLkLtbXzV11brhIlHVtAzsVaMcWM6wp2T-WFQnwF00PyA?key=C1Q208mvu67IIZhzUVfjzQ)

12\. Теперь новый файл готов к копированию в него элементов. Сохраните его.

![image-1691394725936.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeltIgBb4xorrFPp4WBOtuLGY11zE-Yvv_EeulwSUxO8w9HkFFu5_KAThBNZ8DEY3b_4cE_Gfrt7P403-JaLAhVdmsIdk93cFZ9bszltwseg0Gg2ZOwd7BSTO6DBVZDA9bo-daeHvrEFwV93uL6aw?key=C1Q208mvu67IIZhzUVfjzQ)

![image-1691394730401.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdSnLrj90Bew2rpZ5SMNpty9X5RfL9PQfeT8bASFsA9sF8QBwLddCvxg92wJO6KKKztfT-93wj4mIIsK-R1nOqefZXlAqLf_RUckx9GMqBGjCrjIM292Z0mnGdUAGW4dlPwP7_zKuEbcB1GMod17w?key=C1Q208mvu67IIZhzUVfjzQ)

## **2\. Перенос элементов из связанного файла**

После подготовки проекта необходимо перенести элементы из связанного файла в строительную модель. Копирование элементов с созданием НЕ редактируемой геометрии осуществляется командами [_“Зафиксировать элементы”_](https://wiki.sgnl.pro/app/page/1LMMgq5eSluhD6v71p6J_XSZb1EgCrDTMEF6oV9gmBQw) или [_“Зафиксировать по параметру”_](https://wiki.sgnl.pro/app/page/1TozqI0mk9eJwvgVq5rnqGyIqBzFfKthhbrH9edjlq9g) на виде “1. Копирование элементов”.

Перед фиксированием элементов рекомендуется указать [_"дополнительные параметры"_](https://wiki.sgnl.pro/app/page/1Xga4e-2KLC403pfVX6gk2zJ4myTZhYFD8VI_mxCo5Uo), которые будут копироваться из связанного файла вместе с геометрией. Например, Этаж, Код по классификатору, Имя типа и т.д.

1\. Откройте вид  “1. Копирование элементов”. Нажмите на панели Копирование элементов ➤ [_“Зафиксировать элементы”_](https://wiki.sgnl.pro/app/page/1LMMgq5eSluhD6v71p6J_XSZb1EgCrDTMEF6oV9gmBQw)

![image-1691399990410.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc0d1-VSlRju_ngw_K7w_yK23USh9EBtc1cip_XYKFsadNT2F_qW7CLubKminvdq8Ch7i5ab6FZQkn3bAhZ12QlQ5diX4hR7bpy8p9eTRx7Po4PA45VSGIup212svFdR_3xdWAzQSkMjIAbF1B6kA?key=C1Q208mvu67IIZhzUVfjzQ)

2\. Выберите элементы, которые необходимо скопировать, и в левом верхнем углу нажмите готово. Обычно переносится часть элементов, которые выполнены на строительной площадке.

![image-1691400031991.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf3IPi_0jh4Yp_lo9qcjgMm9kupoxwVqcdqsRB9LpljEmmf8CAUULnsAbSWWjVgj6VdxpPG0cJeafSCnyE5Qy9nQO25szDPYv63M4wUVrt31Su01qlWVtIQkR6LmyaLBraeJr4mieLG0EHU9TKQ?key=C1Q208mvu67IIZhzUVfjzQ)

3\. Скопированные элементы появятся на виде “2. Создание строительной модели”

![image-1691400058503.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXff5d-W610GbvNZdGsss5O9w0ASbWz-RaOJH9_UZs3yVsPgonCEyZnoK5IJvJFZmPvc06HN9e1Nj4waftX5-NqzJr9TL1q-hf-BC9fzdBfcQapXGKwq_mX9QesBPcuLZdmcqnvx5FdOdSppObQtwQ?key=C1Q208mvu67IIZhzUVfjzQ)

## **3\. Создание захваток**

**1\. Создание элементов редактируемой геометрии**

Если у Вас есть какие-то элементы, фиксация выполнения которых происходит поэтапно, их необходимо конвертировать в редактируемую геометрию.

1.  На виде 2. Создание строительной модели элементы делят на захватки. Выберите элемент-Создание-Разделить части

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcEuiXT4ux8lWlvWobdKRAEFkKeSP6kTXTzSJTAVedTyaSUagCe7zajTAonTyyN2IehMLCYWrI6SPY987vqkDTHZdq9kJa5T2rLoftLzKF3kes6R7ospcLDcubZ_xD8unFgfV6LOiRhW8JX_kq7?key=C1Q208mvu67IIZhzUVfjzQ)

Редактировать эскиз:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeuU6mELVy3PF6ImkxnpKYuraeJOTw7jxSD2ZxzJZ9LY94xaP9o83jNpqc7FhSr7d4611pmnLvNqShi1oIdfhJmm_enTqccO1PZNWLsVpGHBiDR4dahflVnWF5jLjU18WdmBQB1DAoLwYajbnnn?key=C1Q208mvu67IIZhzUVfjzQ)

Задать плоскость, в которой будет проводиться линия разделения

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd8fMr1uJeKglWhJQ5raXy0Y3ASVDdmhFuJifVjOKBw0E8KfJXVqDtIAHeZAivVPc2Ppd4-S19z_tGaRqP55R2y3Q9FZCdTYmXMGwoMaMpQ6PoRoPCAw345GojI4zom_N7kxMAGAmfIgQJtZGdz?key=C1Q208mvu67IIZhzUVfjzQ)

Щелкнуть по плоскости элемента, затем выбрать инструмент и провести линию разделения.

После этого нажать 2 раза на

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfRVNoYbXNtnz3Scwsjlo5gxeF6Q-rqZaxMGZWHiurowuNAG8_zurodyTiz64IIMEz96md_FdX-RSme9fvzh3ThIQH9ByydYTm7YTwRAI9XnXjmKtVjwQwh4u2RsjQNwlFTZdgoUN-oMpv5nLLa?key=C1Q208mvu67IIZhzUVfjzQ)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdJ3tZEUq7jzKH18BUvcOjrY9VzbYnFsuNmgJKHpBZ9ctVZdGiaYqkEqm08LQ5Pi9Kjpj5WkGOupZGPRJhKugGnpHsmaFddSFqbXfghsSO3TpaayofCDDRBgE7QXecksKE9hAVrUZKs4yaJZTiitQ?key=C1Q208mvu67IIZhzUVfjzQ)

1.  Выполненные элементы необходимо выбрать и сменить стадию на выполнено

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeZ5pkLY72pnj6dKmnM5eQEVWOiLD1CCF-AnaPVXR0ERqp4ZMnu-DVu14f_GkOvt-JnS7Ko0r48_Y0wYRHo1nw5GLimmQAAhC-xnZcjIRzggBH3aW7AxWv8E4yXyaKxid_LXviEADwg9OMWvnSaQA?key=C1Q208mvu67IIZhzUVfjzQ)

1.  После внесения всех изменений в модель, открыть вид 3. Строительная модель.

## **4\. Присвоение статусов элементам модели**

Следующим этапом, после переноса элементов в строительную модель и нарезки их на захватки, является присвоение соответствующего статуса (Завершить / Принять / Запланировать) элементам строительной модели, фактически выполненных на строительной площадке.

#### Закрытие работ в Navisworks

1\. Для того чтобы присвоить статусы элементам в Navisworks потребуется выполнить дополнительные действия:

-   Выгрузить модель в NWC
-   Закрыть работы в Navisworks

2\. Выгрузите вид “3. Строительная модель (Navisworks)” из Revit в NWC. (см. пункт Очистка файла и выгрузка NWC).

**_Очистка файла и выгрузка NWC_**

Если файл строительной модели начинает работать медленно, очистите временную информацию, которая в нём создаётся в результате работы скриптов.

Во вкладке "Управление" найдите кнопку “Удалить неиспользуемые”. Далее нажмите “Ок”.

![image-1691396954465.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfyHr5djmIpKAyKv7iufXIMP0KBzlyTwNrlyM6z3oRosGvmc5IfZD8KCuMm2275Iehg49_39PRuxO4QBa8PjN8EtadYH3Mr0GmrseE9d4pqI4WCrefHxMTczH-RUl0KIoEQuS-hraXB1W5B6Wd6hw?key=C1Q208mvu67IIZhzUVfjzQ)

Для дальнейшей работы необходимо выгрузить Проект из Revit в NWC. Перед выгрузкой следует просмотреть "Настройки Navisworks". Слева в пункте "Считывание файлов" - "Revit" должна стоять галочка “Преобразовать элементы конструкции”. Эту настройку нужно проделать один раз при первом экспорте, при повторных экспортах она уже будет активна. Если она не будет включена, элементы Частей не экспортируются в Navisworks.

![image-1691396963536.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXchtLxwItPjG6MxcfU8aeHpBrFlbiLP74tauuBmCeRM_jthFj5ZQQLxzcp40T7mCV5N7mMxTxYWh37YrOMX1CiIVqG2AobjdCp516IWNrfmQhOounjmV-d4lwGVCOr8cSl-cvLidRYrqkBG9lPHpw?key=C1Q208mvu67IIZhzUVfjzQ)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcx_4nD9tuenwjGOdYfGc0ymWkeIhUW5TKc-qQVLIggfYDDCZg8njdC-OPG55fYC3OT_emXx5r-Q8QpsyAY8dacfPPjRc0IAmDBcQM_io3znjMf5Mm0sWhJi_C9mu41j_LU9WfxRV11QjeAkMJQ?key=C1Q208mvu67IIZhzUVfjzQ)

3\. Необходимо определиться с видами работ. Рекомендовано называть виды работ также, как они указаны в смете/КС-2. Это необходимо для выгрузки объемов из модели и проверки КС-2.

4\. Для создания видов работ перейдите в панель-работы. Подробное описание работы с панелью доступно по [_ссылке_](https://wiki.sgnl.pro/app/page/1VgR0WxMUPH7f2WfrVm4Qt_kXynuZnXnKmUT7ITd2SZo).

Для возможности последующей выгрузки объемов в Excel, на данном этапе необходимо обязательно указать единицу измерения у каждого вида работ.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeVKTxp0hoVNIzgh9798aPDn4IXMvdrbUtY3OgMIuZ3lHwtApReAh6SXkvmjDkwCPxWtiT_EBKTA0Tv8NYUt1K8Gcd7us3HgPVSERob5R_bdW26Q692m3_rpaYU4gkTkzRsjcnZopniat8nwvvE9A?key=C1Q208mvu67IIZhzUVfjzQ)

5\. Заполнение дат выполнения работ. Выбрать элемент/ты, которые относятся к одному виду работ и выполнены за одну дату. На вкладке SIGNAL-Завершить-Ввести дату и выбрать из списка подходящий вид работ.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfBzWJAh92JnBcirjKVS0Pq_yJuGJCKRcEdYwe8PJuj5Ul2snYSjb5acbl_uQJgBoVL5LHfv94-UGNjhWO4FH2mEhGWQX8gSsYk4K5TlwtSSh003kLiJHZEVZ0xZ0s8POOoSUKIDLRL1HPtcPlRFw?key=C1Q208mvu67IIZhzUVfjzQ)

6.После добавления дат в элементы вписываются указанные свойства

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdVXajdZ2sP4el4PmyAmdwC5g5I8xw-Q1W1G8Z7s2MnsF2HxFducaF_Gt1V_QtpdrrIpTn7PNruZsz3YjyISkYAgGYpFrK7swrxyb3m4oTqI0eANEnzVKsiOIsvgxii8YL6gUeXc0Hyw8M2WBXtUQ?key=C1Q208mvu67IIZhzUVfjzQ)

7\. Создаются поисковые наборы по видам работ и по датам

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeiJpQ64JLQc1NT7KaBH0yMKrlttAIjLxVduJXqdRKxS5S_nQaFR1tDNFgtsOnMiR1rJsPPQO1KEQL3Wi4XojvPxe2c-0Nh4ARLNAzYwke2-aJftHwpee0mTebTBtV9TJFGvp5v5EUvJPzVMGdZ?key=C1Q208mvu67IIZhzUVfjzQ)

8\. Для получения объемов работ необходимо воспользоваться экспортом в Excel

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXccouVIROfJUtZRxYqNjmHIb8RiHUjjlvfFbJyBeKkeHZqyKnX2QZjgbxM4JSJn-xaP2vyO43wyR3un7JwlqNljxUx9_BWjS9Q_Dqdxefp5GgjvKHdF7Z6KW_c7fGUS0_3PrDsfnqYlx2SYn9WWVg?key=C1Q208mvu67IIZhzUVfjzQ)

9\. Выбрать папку

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfYowvIwjd6RqZPos0TB9v4NSBSgKdYqdeoWzFRWOe3t_gzuUB3KQ-sewWgDQjYDOR-aaAGvkYY2Zp4hxtvD2c6572j8vz6fNp_-qTKSjJBaqEg4Sgb-AJ3XynAVyOAQPi9Q3YSbqi2c61pw9xODw?key=C1Q208mvu67IIZhzUVfjzQ)

10.Сохранить файл Excel на компьютере.