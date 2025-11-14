---
title: DASHBOARD. Настройка проекта
description: 
published: true
date: 2025-11-14T11:33:22.397Z
tags: 
editor: markdown
dateCreated: 2025-11-14T11:33:22.397Z
---

<sub>**[<   DOCS. Дополнительно](/ru/docs/more)     **|**     [DASHBOARD. Карточки 10. Общие    >](/ru/dash/cards-10)**</sub>

<details>
<summary>Что нового</summary>
  
> Здесь перечислены основные изменения. Для получения подробностей нажмите на номер версии.
{.is-info}

**Обозначения**
:fire: — новые возможности
:sparkles: — доработки функционала
:hammer_and_wrench: — исправление ошибок

----
**[2025.30](/general/updates/2025-30)** ^09.10.2025^  
:fire: Реализовали копирование карточек **Онлайн** из шаблона проекта.
  
----
**[2025.26](/general/updates/2025-26)** ^11.09.2025^
:hammer_and_wrench: Исправили ошибку, встречающуюся при экспорте PDF в отчёте.

----
**[2025.25](/general/updates/2025-25)** ^04.09.2025^
:hammer_and_wrench: Исправили долгое открытие ролей в настройках.

> Информация о более ранних обновлениях доступна в закрытом Telegam канале для пользователей SIGNAL. Для добавления **[обращайтесь в поддержку](/general/support)**.
{.is-info}

</details>
  
----
  
# Вкладки{.tabset}
  

## 1. Создание отчета {#creating}
  
Создание отчета выполняется в разделе “Управление”.

Для создания отчета выберите нажмите "+" и укажите дату, данные отчета для которой будут актуальны. Последующие отчеты будут формироваться на основе предыдущего

>При создании проекта на основе шаблоного, отчет будет сформирован по умолчанию на основе отчета из шаблона
{.is-info}
  
![dash_creating.png](/sgnl_dash/settings/dash_creating.png)



## 2. Добавление карточек и групп {#adding_card}
  
Добавление и редактирование карточек выполняется в разделе “Управление”.

Сперва необходимо создать группу. С помощью групп можно разделить карточки на разные строительные разделы, локации и т.д., для удобной навигации по отчету.

Для создания группы введите ее название, например, ОБЩИЕ ДАННЫЕ, и нажмите “+”.

![dash_group_creating.png](/sgnl_dash/settings/dash_group_creating.png)



Для создания карточки нажмите “+” внутри группы. В открывшемся окне выберите из списка тип карточки и введите название карточки. Затем нажмите “Сохранить”. Подробное описание каждого типа карточек рассматривается в инструкции далее

![dash_card_creating.png](/sgnl_dash/settings/dash_card_creating.png)

Добавьте группы и карточки в отчет, настройте их положение. После можно приступать к заполнению данных в карточках

![dash_log_edit.png](/sgnl_dash/settings/dash_log_edit.png)

## 3. Публикация отчета {#publication}

Еще не опубликованный отчет не доступен к просмотру для пользователей. Чтобы отчет стал доступен для пользователей необходимо опубликовать его в раздел “Отчет”. Для этого нажмите “Опубликовать отчет”. Ранее опубликованные отчеты остаются доступны для пользователей в разделе “Отчет”.

![dash_log_publish.png](/sgnl_dash/settings/dash_log_publish.png)

## 4. Обновление данных отчета {#updating}
  
>После создания нового отчета необходимо обновить данные по карточкам в соответствии с актуальной информацией по объекту.
\
Обновление данных можно выполнять непосредственно через редактирование карточек, а можно выгрузить отчет в Excel или Google таблицы. После обновления информации в Excel или Google таблицы, их можно импортировать обратно в сервис DASHBOARD.{.is-info}

##### Обновление данных{.tabset}
###### 1. Обновление данных в разделе "Управление" {#manually} 

Все карточки в сервисе DASHBOARD можно обновлять вручную, заполняя поля в настройках карточки.
  
###### 2. Привязка карточек через Google таблицы {#google}
  
В сервисе DASHBOARD присутствует возможность привязки карточек к Google таблице. Это позволяет ускорить процесс добавления/обновления данных в созданных карточках. Привязка в Google таблице осуществляется через именованные диапазоны.


Скачайте весь отчет с сервиса [*DASHBOARD*](https://dash.sgnl.pro/), нажав “Экспорт в Excel”.
  
![log_excel_export.png](/sgnl_dash/settings/log_excel_export.png)


Импортируйте Excel в Google таблицу. Для этого в новой [*Google таблице*](https://docs.google.com/spreadsheets/u/0/) нажмите “Файл” ➤ “Импортировать”. В открывшемся окне перейдите во вкладку “Добавить” и загрузите Excel файл.

![image-1690178993331.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcu7IpcmREZmJdFUKRtFZPdKeK85WUvg7VLaYQTMl7slrU-ZRc4-pGQxcZZLS3v2N32rFPgFrWCq15vBolJ8ms0RpoDaekptWo92ZFGb9RGvy6uJpjWhqoU3pJmw_ziaormqOlr1LFXKi2nnfHd?key=fbjahmDVrqngiYxvm4q7FA =80%x)

Чтобы легче ориентироваться в документе после его импорта, можно изменить названия листов в Google таблице в соответствии с названиями карточек.

![image-1690179006354.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdeUsW5Rf0CNWXdGUmVhUgfadpT4YC93cQz2B_Jx0EYyUVKLsJycTkPJbSMkUxIJngNrqRfm1hQUyh-r3sfrBM0woODscvHghYrb96KxapuOgccU1WTzJw1lAHawRRTKyfmuAzQ3Xea7u9qigNd8A?key=fbjahmDVrqngiYxvm4q7FA)

2\. В сервисе [*DASHBOARD*](https://dash.sgnl.pro/) перейдите в раздел “Привязка”. Скопируйте ссылку на Google таблицу и вставьте ее в поле “Ссылка на Google таблицу”. Затем нажмите “Привязать отчет”.

![dash_google_link.png](/sgnl_dash/settings/dash_google_link.png)





>При создании нового отчета ссылка на Google таблицу сохранится и перейдет в новый отчет
{.is-warning}
  
3\. Наполните отчет Google таблицы необходимыми карточками, располагая их на одном листе как в [шаблоне](https://docs.sgnl.pro/s/f/4d8f615a-27fd-4b1a-a631-c7529eb99f03/i/4b15b902-df5a-4795-b68b-50963eddf283?f=663dec15-0db0-4e70-b152-ceb803fe6ea6) или на разных. Нажмите "Копировать данные карточки", чтобы скопировать данные в буфер обмена. Перейдите в Google таблицы и через Ctrl+V вставьте данные.

![image-1689148845399.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc0kLL66Oi9Cy9Mqfbq0cuPaYoOLNlfiCp1MQn2zwr8-tAj_3ZCtq_p9e_nOUsSD6ft67PF74ymwiosoVPffw0LkIijxnb7_SpWRju3B8BTHafeAZ-nprm_21CWTGX5QT_f90GppbGmKLfdcwoFIg?key=fbjahmDVrqngiYxvm4q7FA =80%x)

>При размещении карточек на одном листе следует располагать их горизонтально, а также не вставлять новую карточку поверх уже стоящей.
{.is-warning}
  
![image-1690179165516.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcAiv4qX_O_s-qn06rcdEgWuDFUFw77PYgq2MWPd5LF_wWVAAUcf3wArW-iPqtwyvGgrtZSH-mJJYVTpm3HfaHTv4KojmhL7SnUbac-mRfTZFzX_Mcjj80Imuf1tEwPXY5Hg04ENclrykrzNi74Ww?key=fbjahmDVrqngiYxvm4q7FA)

4\. Теперь необходимо создать диапазоны для карточек, придерживаясь правила: в один диапазон может входить только одна карточка.

Откройте Именованные диапазоны, нажав “Данные” ➤ “Настроить именованные диапазоны”.

![image-1690179223118.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXecoynOzuxUW6VeDkWvdSGdcb8nDiPByN-0ETQzH_Qhc_jFkcL1-rlLxXxlOS39QNuXoUQn1vzPu1zdea9zn8cyiZloDKTIaDBl1S6kHv7Uo21x8nZlJvLTT5CS17Ws48hwVjh80DbTwT0AtEOjiA?key=fbjahmDVrqngiYxvm4q7FA =70%x)

-   Если карточки располагаются на одном листе, то выделите диапазон из столбцов, в который входит карточка (например, A, B и C), введите Наименование диапазона (например, КС\_2) и нажмите “Готово”. Будет создан диапазон, из которого сервис DASHBOARD будет подтягивать данные карточки. Проделайте данную операцию с остальными карточками.

![image-1690179239440.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXft6ixVD3G2ii1cn4TiHNU4pCkQUZ1BYhKRSgEcwOLYneI0D4Xu_J6e0BP35FWKUIxY6AuQHiBJNnPf6WIZyzCbiO4sq9KJ2E_lWrCtldr0K-v6MBwzFGcxSbHkyMwMkDvbFi_hIou4KZRuNMJFhw?key=fbjahmDVrqngiYxvm4q7FA =70%x)

>Название диапазона может содержать только буквы, цифры и знаки подчеркивания (\_) ; не должно содержать пробелы или знаки препинания; не должно начинаться с цифры.
{.is-info}
  
-   Если карточки располагаются на отдельных листах, то выделите все ячейки на листе, нажав на область пересечения столбцов и строк (горячая клавиша Ctrl+A). Введите Наименование диапазона, например, КС\_2, и нажмите “Готово”.

![image-1690179971625.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeSGJUcskDgJG8guUJN_OK6iJizBMnZWpeebmzlxk5rHt7My-2BYsAxH8lISy9NqEL-ym-GdYJ1w8x_bNXLXWlP-UvVux9Vx7rRrBI1N77g9JKnPodLmEkTmXiAxCujLvQulDTY5HOYR2THWXk-eg?key=fbjahmDVrqngiYxvm4q7FA =70%x)

5\. После добавления необходимых карточек в Google таблицу и создания диапазонов перейдите обратно в сервис DASHBOARD.

Нажмите “Обновить список диапазонов”, чтобы подтянуть созданные диапазоны из Google таблицы.  
Далее привяжите диапазоны к карточкам. Для этого на карточке раскройте список диапазонов и выберите диапазон, соответствующий выбранной карточке. После этого карточка поменяет цвет на темно-синий.



6\. После выбора диапазонов необходимо синхронизировать карточки с Google таблицей, чтобы они получили обновленные данные. Для этого нажмите "Обновить" на самой карточке, чтобы синхронизировать данные одной карточки, или сверху напротив ссылки на Google-таблицу, для синхронизации всего отчета.
![dash_link_updating.png](/sgnl_dash/settings/dash_link_updating.png)
  
#
<sub>**[<   DOCS. Дополнительно](/ru/docs/more)     **|**     [DASHBOARD. Карточки 10. Общие    >](/ru/dash/cards-10)**</sub>