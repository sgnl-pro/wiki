---
title: DASHBOARD. Настройка проекта
description:
published: true
date: 2026-09-23T11:31:43.000Z
tags: dash
editor: markdown
dateCreated: 2025-11-14T11:33:22.397Z
---

<sub>**[<   DASHBOARD. Введение](/ru/dash/intro)     **|**     [DASHBOARD. Все карточки    >](/ru/dash/cards)**</sub>

<summary style="font-size: 16px; color: #0D47A1; background: #E3F2FD; border-radius: 7px; border: 1px solid #64B5F6; display: flex; gap: 10px; padding: 5px 16px; display: block; margin-top: 10px;">
<span style="flex-grow: 1;"> <a href="/dash/settings/updates" onclick="event.stopPropagation();" style="color: inherit; text-decoration: none;">🔄 Что нового (история изменений этого функционала)</a></span>
</summary>

----

# Вкладки{.tabset}

## 1. Создание отчёта {#creating}

Создание отчёта выполняется на вкладке «Управление» при наличии соответствующего доступа.

Для создания отчёта нажмите «+» и укажите дату, на которую будут актуальны его данные. Если в проекте уже есть текущий отчёт, новый создаётся на его основе. В окне создания можно также импортировать отчёт из Excel-файла.

> При создании проекта по шаблону отчёт формируется на основе отчёта из шаблона.
{.is-info}

![dash_creating.png](/sgnl_dash/settings/dash_creating.png)


## 2. Добавление карточек и групп {#adding_card}

Добавление и редактирование карточек выполняется на вкладке «Управление» при наличии доступа к группе или отчёту.

Сначала создайте группу. С помощью групп можно разделить карточки по строительным разделам или локациям для удобной навигации по отчёту.

Для создания группы введите её название, например «Общие данные», и нажмите «+».

![dash_group_creating.png](/sgnl_dash/settings/dash_group_creating.png)


Для создания карточки нажмите «+» внутри группы. Выберите тип карточки, введите её название и нажмите «Сохранить». Описание типов карточек приведено в [каталоге](/dash/cards).

![dash_card_creating.png](/sgnl_dash/settings/dash_card_creating.png)

Добавьте группы и карточки в отчёт, расположите их в нужном порядке и заполните данные карточек.

![dash_log_edit.png](/sgnl_dash/settings/dash_log_edit.png)

## 3. Обновление данных отчёта {#updating}

После создания отчёта обновите данные карточек. Их можно заполнить вручную или привязать к Google Таблице либо XLSX-файлу из DOCS. Доступность источников зависит от настроек продукта. На вкладке «Привязка» выберите источник данных для отчёта. При переключении источника система предупреждает о сбросе прежней привязки файла или диапазонов карточек.

Для карточек, которые получают данные из DOCS, используйте кнопку обновления карточки, группы или отчёта. Во вкладках «Онлайн», «Мой отчёт» и «Отчёт компании» есть кнопка «Обновить данные» и дата последнего обновления. При первом открытии за день данные обновляются автоматически.

##### Обновление данных{.tabset}
###### 1. Обновление данных на вкладке «Управление» {#manually}

Карточки с ручным вводом можно обновлять, заполняя поля в настройках карточки. Некоторые типы получают данные из DOCS и настраиваются иначе; подробности приведены в статьях о соответствующих [карточках](/dash/cards).

###### 2. Привязка через Google Таблицы {#google}

Если в продукте доступна привязка к Google Таблицам, выберите этот источник на вкладке «Привязка». Для каждой карточки понадобится отдельный именованный диапазон.

1. На вкладке «Управление» нажмите «Экспорт в Excel», чтобы скачать отчёт.

![log_excel_export.png](/sgnl_dash/settings/log_excel_export.png)

2. В новой [Google Таблице](https://docs.google.com/spreadsheets/u/0/) выберите «Файл» → «Импортировать» → «Добавить» и загрузите скачанный Excel-файл.

![image-1690178993331.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcu7IpcmREZmJdFUKRtFZPdKeK85WUvg7VLaYQTMl7slrU-ZRc4-pGQxcZZLS3v2N32rFPgFrWCq15vBolJ8ms0RpoDaekptWo92ZFGb9RGvy6uJpjWhqoU3pJmw_ziaormqOlr1LFXKi2nnfHd?key=fbjahmDVrqngiYxvm4q7FA =80%x)

При необходимости переименуйте листы Google Таблицы по названиям карточек.

![image-1690179006354.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdeUsW5Rf0CNWXdGUmVhUgfadpT4YC93cQz2B_Jx0EYyUVKLsJycTkPJbSMkUxIJngNrqRfm1hQUyh-r3sfrBM0woODscvHghYrb96KxapuOgccU1WTzJw1lAHawRRTKyfmuAzQ3Xea7u9qigNd8A?key=fbjahmDVrqngiYxvm4q7FA)

3. На вкладке «Привязка» вставьте ссылку на таблицу в поле «Ссылка на Google таблицу» и нажмите «Привязать отчёт».

![dash_google_link.png](/sgnl_dash/settings/dash_google_link.png)



> При создании следующего отчёта ссылка на Google Таблицу сохраняется.
{.is-warning}

4. Разместите данные карточек на одном листе, как в [шаблоне](https://docs.sgnl.pro/s/f/4d8f615a-27fd-4b1a-a631-c7529eb99f03/i/4b15b902-df5a-4795-b68b-50963eddf283?f=663dec15-0db0-4e70-b152-ceb803fe6ea6), или на разных листах. Чтобы перенести данные карточки, нажмите «Копировать данные карточки» в DASHBOARD и вставьте их в таблицу сочетанием Ctrl+V.

![image-1689148845399.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc0kLL66Oi9Cy9Mqfbq0cuPaYoOLNlfiCp1MQn2zwr8-tAj_3ZCtq_p9e_nOUsSD6ft67PF74ymwiosoVPffw0LkIijxnb7_SpWRju3B8BTHafeAZ-nprm_21CWTGX5QT_f90GppbGmKLfdcwoFIg?key=fbjahmDVrqngiYxvm4q7FA =60%x)

> Если карточки находятся на одном листе, располагайте их горизонтально и не вставляйте данные новой карточки поверх существующей.
{.is-warning}

![image-1690179165516.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcAiv4qX_O_s-qn06rcdEgWuDFUFw77PYgq2MWPd5LF_wWVAAUcf3wArW-iPqtwyvGgrtZSH-mJJYVTpm3HfaHTv4KojmhL7SnUbac-mRfTZFzX_Mcjj80Imuf1tEwPXY5Hg04ENclrykrzNi74Ww?key=fbjahmDVrqngiYxvm4q7FA =60%x)

5. Создайте отдельный именованный диапазон для каждой карточки. В Google Таблице выберите «Данные» → «Настроить именованные диапазоны».

![image-1690179223118.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXecoynOzuxUW6VeDkWvdSGdcb8nDiPByN-0ETQzH_Qhc_jFkcL1-rlLxXxlOS39QNuXoUQn1vzPu1zdea9zn8cyiZloDKTIaDBl1S6kHv7Uo21x8nZlJvLTT5CS17Ws48hwVjh80DbTwT0AtEOjiA?key=fbjahmDVrqngiYxvm4q7FA =70%x)

-   Если карточки находятся на одном листе, выделите столбцы карточки, например A–C, введите название диапазона, например `КС_2`, и нажмите «Готово». Повторите для остальных карточек.

![image-1690179239440.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXft6ixVD3G2ii1cn4TiHNU4pCkQUZ1BYhKRSgEcwOLYneI0D4Xu_J6e0BP35FWKUIxY6AuQHiBJNnPf6WIZyzCbiO4sq9KJ2E_lWrCtldr0K-v6MBwzFGcxSbHkyMwMkDvbFi_hIou4KZRuNMJFhw?key=fbjahmDVrqngiYxvm4q7FA =70%x)

> Название диапазона может содержать буквы, цифры и подчёркивание. Оно не должно начинаться с цифры или содержать пробелы и знаки препинания.
{.is-info}

-   Если карточки находятся на отдельных листах, выделите ячейки нужного листа сочетанием Ctrl+A, введите название диапазона и нажмите «Готово».

![image-1690179971625.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeSGJUcskDgJG8guUJN_OK6iJizBMnZWpeebmzlxk5rHt7My-2BYsAxH8lISy9NqEL-ym-GdYJ1w8x_bNXLXWlP-UvVux9Vx7rRrBI1N77g9JKnPodLmEkTmXiAxCujLvQulDTY5HOYR2THWXk-eg?key=fbjahmDVrqngiYxvm4q7FA =70%x)

6. Вернитесь в DASHBOARD и нажмите «Обновить список диапазонов». У каждой карточки выберите соответствующий диапазон из списка.


7. Нажмите кнопку обновления у карточки для синхронизации одной карточки или кнопку рядом со ссылкой на таблицу для синхронизации всего отчёта.
![dash_link_updating.png](/sgnl_dash/settings/dash_link_updating.png)

###### 3. Привязка через XLSX-файл из DOCS {#xlsx}

1. Загрузите XLSX-файл в проект DOCS. В файле создайте отдельный именованный диапазон для каждой карточки, данные которой хотите обновлять.
2. На вкладке «Привязка» выберите источник «XLSX-файл из SIGNAL DOCS». Нажмите на поле выбора файла и укажите загруженный XLSX-файл.
3. Если вы изменили именованные диапазоны в файле, нажмите кнопку обновления списка диапазонов рядом с выбранным файлом. Для нужной карточки выберите её диапазон в поле «Диапазон».
4. После изменения данных файла нажмите кнопку обновления у карточки или кнопку обновления всего отчёта на панели привязки. Файл в DOCS можно редактировать онлайн.

Карточки 33, 34 и 18 в списке привязки не показываются. Их источники данных выбираются в настройках самих карточек.

## 4. Публикация отчёта {#publication}

Неопубликованный отчёт недоступен пользователям на вкладке «Отчёт». Чтобы открыть его для просмотра, на вкладке «Управление» нажмите «Опубликовать отчёт». В окне публикации при необходимости добавьте комментарий и подтвердите действие. Ранее опубликованные отчёты остаются доступны для просмотра. Публикация требует соответствующего доступа.

![dash_log_publish.png](/sgnl_dash/settings/dash_log_publish.png)

## 5. Настройки проекта {#permissions}

Раздел «Настройки» доступен администратору. На уровне компании во вкладке «Доступы» можно выбрать роли и пользователей, которым разрешён просмотр отчёта компании. Выберите их в поле «Просмотр» и нажмите «Сохранить».

На уровне проекта во вкладке «Уведомления» настраиваются уведомления по проекту. Во вкладке «Публичные доступы» администратор управляет публичными ссылками на карточки.

Права на работу с конкретным отчётом задаются на вкладке «Управление»: через шестерёнку — на создание, удаление и публикацию отчёта, а также изменение показателей; через карандаш — на группы и карточки. Доступы к группам и карточкам можно настраивать отдельно.

<sub>**[<   DASHBOARD. Введение](/ru/dash/intro)     **|**     [DASHBOARD. Все карточки    >](/ru/dash/cards)**</sub>
