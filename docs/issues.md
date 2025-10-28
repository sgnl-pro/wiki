---
title: DOCS. Замечания
description: 
published: true
date: 2025-10-24T07:48:22.454Z
tags: 
editor: markdown
dateCreated: 2025-09-09T12:10:08.827Z
---

<sub>**[<   DOCS. Работа в файлах](/ru/docs/viewers)     **|**     [DOCS. Согласования   >](/ru/docs/reviews)**</sub>

> См. также видеоинструкцию по работе с замечаниями: **[Telegram](https://t.me/signal_docs/305) [YouTube](https://youtu.be/yON9Jtl_ifg)	[Rutube](https://rutube.ru/video/5adeaf2ce0acb999e8ff5b2568b5e6a8/) [VK](https://vkvideo.ru/video-223002264_456239085)**
{.is-info}

<details>
<summary>Что нового</summary>
  
> Здесь перечислены основные изменения. Для получения подробностей нажмите на номер версии.
{.is-info}

**Обозначения**
:fire: — новые возможности
:sparkles: — доработки функционала
:hammer_and_wrench: — исправление ошибок

----
**[2025.32](/general/updates/2025-32)** ^23.10.2025^
:fire: **Добавили событие и письмо о получении замечания ответственным.**
:sparkles: Добавили запись об изменении атрибутов в журнал замечания.
:hammer_and_wrench: Исправили сбрасывание быстрых фильтров в замечаниях.
  
----
**[2025.30](/general/updates/2025-30)** ^09.10.2025^
:sparkles: Отключили возможность удаления пометок ответственному.
:sparkles: Реализовали поиск по роли в списках с выбором пользователей и ролей.
:hammer_and_wrench: Исправили ошибку, когда при открытии в замечании удаленного вложенного файла повторно открывалось окно DOCS.
  
----
**[2025.29](/general/updates/2025-29)** ^03.10.2025^
:fire: Реализовали массовое редактирование замечаний для пользователей.
:hammer_and_wrench: Исправили количество просроченных дней в реестре, когда их больше 30.
  

----
**[2025.28](/general/updates/2025-28)** ^25.09.2025^
:hammer_and_wrench: Поправили сортировку типов в реестре.

----
**[2025.27](/general/updates/2025-27)** ^18.09.2025^
:hammer_and_wrench: Поправили экспорт замечаний в PDF.

----
**[2025.25](/general/updates/2025-25)** ^04.09.2025^
:sparkles: Убрали в замечаниях у ответственного статус **Не принято.**

> Информация о более ранних обновлениях доступна в закрытом Telegam канале для пользователей SIGNAL. Для добавления **[обращайетесь в поддержку](/general/support)**.
{.is-info}

</details>
  
----

В сервисе SIGNAL DOCS реализовано создание замечаний для файлов любого формата. Замечания создаются как в самом документе, так и из реестра замечаний без привязки к документу.

# Вкладки{.tabset}
## 1. Создание замечаний к документам
###### 1. Создание замечаний к документам {#documents}

Пользователь SIGNAL DOCS может создать замечание. Доступ к редактированию замечания имеют сам Автор замечания, Ответственный за устранение замечания и Администратор проекта.

Для создания замечания без привязки к документу перейдите в раздел “Замечания” и нажмите 

![image-1703763408406.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfm8vXjfvQZDlkksCFe5UesK6CGPOxlAP_ORi7piq1xUkmr1Ruyl_lQyu6K2wMr6WpiKEA91zZnK8lPQIZ3fbxzbNVAWu8uFU5oflM8sWfwnKqZdbXmB8GdfsVYC_PZU6W6_wS-YztUziXgRB_Qdw?key=cnL3kvpEZPujFMNQA9w79A)

в левом верхнем углу. В открывшемся окне заполните форму замечания.

![image-1703763418884.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXemihQVM5cdlByRXwKIwLw2GvK-JjZMRCXh2jnYtJTcS9iU25blj1RX8An7QV24ZD2LRWk-jOPTFmCtAE5W4I8l8aL-rqI4TnkHRRjBzFauJTOpy28zCrIeufryIhYrPDpQFm7rhT3FhRCQgL5OqQ?key=cnL3kvpEZPujFMNQA9w79A)

Для создания замечания, привязанного к документу, откройте любой файл и в правой части экрана нажмите 

![image-1703763431065.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXek95ZV6SVRgs9zvH0I1wsx8MmMmqXYMj8bOfrItmS7_3B3ABMZDm2LbsgwjGMwYTJKfrYvNlC9fkQ9Vsdl9o_f4OyhI5qQ6EoysMGvADi88eE4ZIc5WtM8oKPQGdHQ4TGATiLfysVVTAc80kI1?key=cnL3kvpEZPujFMNQA9w79A)

[.](https://wiki.sgnl.pro/uploads/images/gallery/2023-12/image-1703763431065.png)

![image-1703763444345.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXePvEUqMtfu2Wj3EgWG9VrOgRccflTYaUWE18nA9R5KGPbPBMedIou3LLtnjtZjMStkcxu3loMsnzEELxZ7V7pMF7fw1wlX4WFAPlQH1cRPQMRARMVaaBPmGYbHR2_Vca8-iiMFEmeU7hxgbzEJ6Q?key=cnL3kvpEZPujFMNQA9w79A)

В левой части экрана откроется форма замечания, которую необходимо заполнить:

-   **Тип замечания** - типы настраиваются администратором проекта. Каждый тип имеет собственное предназначение и пользовательские атрибуты.
-   **Название** \- краткое наименование замечания, отображаемое в реестре замечаний и по смыслу относящееся к типу.
-   **Ответственный** - указываются ответственные за устранение замечания пользователь или роль, являющиеся участниками проекта. Ответственному будет направлено уведомление на электронную почту о создании замечания.
-   **Наблюдатели** - указываются сторонние роли и пользователи, которые смогут отслеживать замечание и писать комментарии.
-   **Статус** - обозначает этап работы с замечанием. При изменении статуса аудитор, ответственный и наблюдатели получают уведомление на почту.
-   Статус **“Черновик”** ответственному не будет отправлено письмо на электронную почту.
-   Статус **“Открыто”** выбирается при создании замечания, ответственному будет отправлено сообщение на электронную почту.
-   Статус **“В работе”** устанавливает ответственный, если согласен с выданным замечанием и берет его в работу.
-   Статус **“Отклонено”** устанавливает ответственный в случаях,когда не согласен с выданным замечанием, а также пишет комментарий в поле.
-   Статус **“На проверке”** устанавливает ответственный после устранения замечаний и загрузки новой версии документа на проверку.
-   Статус **“Закрыто”** устанавливает аудитор в случае устранения замечания.
-   Статус **“Не принято”** устанавливает аудитор в случае если он не удовлетворен устранением замечания.
-   Статус **“Удалено”** \- замечание было создано по ошибке.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfVDjUgKQyyE5lhJFXBK52v4SsUAgglQRtA9wQZDaS4Lk9mgmcpdDpY6gOB8PPzxmFW6T5tEZXB3n46yOH9UXAicwBpwgSiMJZH4WDY9AfJFHkqqTJ7kAF1RYOh62Ow97Y?key=cnL3kvpEZPujFMNQA9w79A)

-   **Описание** - заполняется для более подробного описания замечания.
-   **Дата устранения** - указывается дата, до которой нужно отработать замечание
-   **Вложения** - добавление к замечанию дополнительных файлов (локальных, из DOCS или URL ссылок).
-   **Пользовательские атрибуты** (при наличии) - создаются администратором проекта и используются для добавления дополнительной информации к замечанию, например, Вид нарушения, Вид работ, Категория и т.д.

В документах PDF и Изображениях можно оставлять пометки для каждого замечания. На выбор доступно 5 типов пометок: Стрелка, Прямоугольник, Карандаш, Текст и Эллипс. Оставленные пометки сохраняются во всех версиях документа.

![image-1703763461434.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXflTIjh0fGeHocey5g0Y6EMgODycOTvy70wX7zhEl6k38ORN3bTOsBOEkh3GeStgeRDDq0_2puBh_KEd_sByXfG3ZHWrzglwzmLk6wHqhZcR4fzzLvedCxMA4SLoRZpEuwWO4nIBKUY7JBjKepvkA?key=cnL3kvpEZPujFMNQA9w79A)

В документе рядом с пометкой отображается ID номер замечания, к которому оставлена данная пометка. 

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfEuYQzpdKcOOJ51sVXuZ8gzDDILQl412ITCSsoC0s4RYRUo6r5PhMKtnImql9ts9BOMuHKAeB4TQx0RUzeoEDpjvmW-dXzohZl7hQwPlMBWhzTvhPN86tMPstGYRCOq0HcwIyUVGr-dfVhn9p6eQ?key=cnL3kvpEZPujFMNQA9w79A)

После создания или смены статуса замечания ответственному пользователю и автору замечания будет приходить письмо на Email, уведомляющее о создании или смене статуса замечания.

![image-1703763472179.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXekFlgyKv-k7Y91DXpBPEpcJ-XlxcT1BI12TmYKHnxT5ryTg27-L_mHckM0d9dVi167j24zMAikqDJwelsuT7NqiGBmJBTCdt9ewCoJwakM8jtbekdXsMWeQS1dVjXgnDAaF_pdKmyuLgcJMUJo4A?key=cnL3kvpEZPujFMNQA9w79A)

Перейдя по ссылке в письме, пользователь может открыть документ и подробнее ознакомиться с назначенным ему замечанием.

Чтобы открыть или закрыть список замечаний в текущем файле, нажмите 

![image-1703763484337.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcn03hoESaHR5oENEqmmbTENa21-qEqRJO3FKvq3p1zPNQthIxQHD5UK4orE6Jewbvoki69ICElC8Y-eo9_kRVrvJGqouxEcxeZzdXP3MGuJoVG3yTIe5ZBqOINz-a5KXI1m7H461kuNBXS37OZdg?key=cnL3kvpEZPujFMNQA9w79A)

 в верхней части документа.

![image-1703763492808.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeC4znQSftHmEgYt9H_00YXwoSIbwWIMpOp4K1x96l9nVzcXpaOAh4wYq8sWCiDqlo9ymXNsnMwiKa-daTze6qFhUfhffoF4k3hAjF1TVcn7XzcDMWsznuF3hf5r-WP-H6RhmaS5hfmyETt2G3v?key=cnL3kvpEZPujFMNQA9w79A)

Ответственный может сменить статус замечаний на **“В работе”**, **“На проверке”**,**“Отклонено”.**

## 2. Создание замечаний к моделям
###### 2. Создание замечаний к моделям {#models}
  
### Вкладки{.tabset}
#### 2.1. Forge Viewer

Для создания замечаний откройте файл модели через **Forge Viewer** и в правой части экрана нажмите

![image-1703763431065.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdbbmj5wK332QSQFScqdVVZcKKDgiZoEnZkOVtj30Owl625o8xdi90rbdyYOH-g2DKD3KQAqQIuxWXv-5nfHmJvnLsttqTiF3iyYnUyOHXhF1bDi3y8RS2LLeMOANb7DWLWshTfGwNTXI8t6DZ42Q?key=cnL3kvpEZPujFMNQA9w79A)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdHC0Yta5CQrjIyVHGVnJbMWEB22kWoohWIwDN7BftDcTsz1a1pTXmzBIPrLsIDXwUtAYBzuyaJndMyamKCpJrEFUutT3jx4-fuKud08GlY6r0YYrYpYv_32Yqma5xZ5Vh3CItIXuNqFidDSUngtQ?key=cnL3kvpEZPujFMNQA9w79A)

Заполните поля, при необходимости, выберите один или несколько элементов(через Ctrl),к которым будет привязано замечание, нажмите сохранить выбор. После этого ID элементов отобразятся в теле замечания. Выделить элементы в модели, можно нажав на

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe-CJu_PMwjdfvt69RbGW3WwEE5ImCbLMWsh8dMyfjZchgUv3VHOFWDorjc_tZ4uwZYhwVoSUjrOpTdfYwKyL4P3TV2ngCYzwxrvzDwiyoI9lacwccOEZNDWzihhXHUhkIyh_ZGY_XZj6WR-Ua0ZA?key=cnL3kvpEZPujFMNQA9w79A)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXedrCn_fUBhU8eWD0u91_90qXq0G8rhngnKupG8oopGfj8W77JV-vziIy7J2V6vhvJy2pfYM9HAqimA2VAaBXxuVIxg2dDtCR-yKhLd-ffo6R94_uygnHTpXuEWvvZJ1tB3Iha5AT5V9I8qo91DVw?key=cnL3kvpEZPujFMNQA9w79A)

Помимо привязки замечания к элементам, есть возможность сделать пометки на виде. Для этого нажмите 

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcraMESf-Z9x9xJ4JRuL3mAGZNZA2Q8cM_Qyun8bQt7ZybC2VFcm94el7Gfm1xS6z3FjL-9In0ffrI0axQQGfo-wSEzJBOXFWUnQlyHxEDyIHEqtqCO8yZQ_PbApwVIK-Q?key=cnL3kvpEZPujFMNQA9w79A)

 на преднастроенном виде и сделайте пометки. Пометка с изображением вида появится во вложенных файлах к замечанию.

#### 2.2. Tangl Viewer

Для создания замечаний откройте файл модели через **Tangl Viewer**  и в правой части экрана нажмите

![image-1703763431065.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdnfw1os8wo_h0Ufd9esJajUVpP3V5w-VneOS4ZgxqCCQlFx5e9kvyu4stppiCrEKk8TcYS9YDtaE0xN6KscFycZv0TTV3UxhexT6FRR0XdGnAlnzYHplI8oAzReyayDbjHsh6qx4tT7cBIa1FGoA?key=cnL3kvpEZPujFMNQA9w79A)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcu5ZUT--hEyPUvqMBKp5-63T-TDFgczYI9cmGzb1rpa7VguPPXkew5LEPOubwiExe7Ju2A_FWkdChnnDsmyKIFHmKjWjvX5Kc28oDYQhWB-3XIFWnxE7DksHOA41aE_wxaKa0CV8Tb-UQvFMaOWw?key=cnL3kvpEZPujFMNQA9w79A)

Заполните поля замечания.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcn0LRls873mkIdy7_pFZjnj4-PDZ2bQai5zrerTq7_BdITO1cemYOLOpqFvDNpka_vq8afqP6mlQD4y8ZJ_hsucIQ1ucb_ycDT_rJu1eKxhS-gVfnij2VBLhRzMVexJUH9pvz4XhrGmJ8FND9dow?key=cnL3kvpEZPujFMNQA9w79A)

## 3. Реестр замечаний
###### 3. Реестр замечаний {#register}
  
> См. также видеоинструкцию по работе с реестром замечаний: [Telegram](https://t.me/signal_docs/303) [YouTube](https://youtu.be/x99hg1513T0)	[Rutube](https://rutube.ru/video/fd149dcd26349dbe0b3f6243bea8bba4/) [VK](https://vkvideo.ru/video-223002264_456239083)
{.is-info}
  
Все созданные в проекте замечания хранятся в табличной форме разделе “Замечания”.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdaYXenocwOnKZS5V4wYYLvb_zRlrMFrpuHg3J3XDgO04Xzr00Ni4yf9mqzxyJcHKwirXceYc1i9S4NdUCtjrseLtwu4gnPpStR-EUVcStcxKKff8TAgwpvjHDKD0IRiWS3af3jWyK1zJawMBoC?key=cnL3kvpEZPujFMNQA9w79A)

В реестре отображается необходимая информация о замечаниях:

-   Номер и статус замечания
-   Тип замечания
-   Название
-   Описание
-   Ответственный за устранение замечания
-   Файл - при нажатии на поле открывается документ, которому назначено замечание
-   Номер версии файла, к которому относится замечание
-   Кем добавлено замечание
-   Дата последнего изменения замечания

Для просмотра и редактирования замечания, нажмите на строку замечания в реестре.

![image-1703763690634.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeQ7bKSR--Pk_3C9fpC06UVic7TZo4EU_5pDG6IGBZI1yIxE10v5Hw4JntxIifFajzyuAds-r___pvQDJtMQGv3311sItdi9O-QhI7-5QvKyRk9j-g_QsAq-9esxGISHBMdWOHZOhNIB0r-LpqL5w?key=cnL3kvpEZPujFMNQA9w79A)

Чтобы открыть документ, в котором создано замечание, нажмите на путь к файлу в поле “Документ”

Для навигации по реестру Вы можете воспользоваться поиском по названию замечания, его описанию и по названию файла, а также фильтрами в верхнем правом углу экрана.

![image-1711090062404.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfhFjtMp8d7K_wwF7Wx4ikD6X100ESIFPMRoJEy6v7YNPp-6seV0m4OD5xO2sSo4LMCH3IhBTSfOYcZEnN8GfxwXcdY6A4AgHT2KMs-b0vykC3yGnIfS5xa6s3D3k3g9kqQiVmgPAvEd0AH_grp?key=cnL3kvpEZPujFMNQA9w79A)

Все замечания/отфильтрованные замечания можно экспортировать в форматах Excel и PDF

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdrDghDJoES8s-C-_-CbRAeg_NoOYuh21JDvpLey1xGZ5lYhDznkfsuY2wQUTOKCld8zjG_jYaV4rH_ypYP4hpHLWGJrmUTQlBIrMEx930Jos-cYJPLBX_t_JwdJ52wMFg?key=cnL3kvpEZPujFMNQA9w79A)

При экспорте в PDF открывается окно с настройками экспортируемых полей. Максимальное количество замечаний в одном файле ограничено 100 единицами.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcpbx2Ujeo-wfM5Cfo888FKPHJ5cPtSrhf7sHWO0kkQA9pEQyDsWubPqMZbUjCcM_gStq8up5IkeZ2W4hGSGpL74A0ht_TivZoicXTrTrXsKk7FBjbefUh-x7FwfvMDaA?key=cnL3kvpEZPujFMNQA9w79A)

Из реестра Excel есть возможность перейти к документу, в котором выдано замечание, нажав на файл.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcqjzCT7pIOvIz2ViG_zAJRYbx94u3I9Af9JcucJfwwj8jGxUGKnN9X1OvVrSAvvfpdduVJrovpORRYqR5czu98I2pTK3dDqUQkdSUs9d0HIxEN0ckHWNY625wZFxV-c1XF7vqTzS7wL9pRHKak?key=cnL3kvpEZPujFMNQA9w79A)

### Пакетный перенос пометок между листами PDF

Иногда случается ситуация, когда в новой версии документации изменился порядок листов, из-за чего пометки, созданные ранее, оказываются не на изначальных листах. Чтобы была возможность быстро вернуть пометки на свои места в DOCS есть функция пакетного перемещения.

Для того чтобы воспользоваться ей перейдите в файл и нажмите 

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc8S8PZGrlXpvLJq4xidE_PlWPXxQUGYIZz-x1REEWk-Cv3vE8qSllPxgG18zpWy_Jz2X4ZLe6a5LUHD4tWnZgAvPUOWmKYqw-vZnzXRlPNF9UQa06xtA5HyQjK-qmSWeA?key=cnL3kvpEZPujFMNQA9w79A)

  в левой верхней части экрана. Откроется окно перемещения пометок:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd_fokjN9iWCaJINMK20qH_5gIgiVv_6JQN63Co0q6qNDUB3deb-FuytLt23z6ZCadW2seATk4tZvaAtqI-HzTgwDf7NGNLfoy1XcjMJ6aiqqhYRIltHZGgZRXLfntGPao?key=cnL3kvpEZPujFMNQA9w79A)

1 - Выберите предыдущую версию файла, с корректным расположением пометок

2 - Расположение пометок на предыдущей версии

3 - Переместите пометки на нужные листы с помощью стрелок

## 4. Администрирование
###### 4. Администрирование {#admin}
  
> См. [Настройки проекта → Замечания](/ru/docs/settings)
{.is-info}


#
<sub>**[<   DOCS. Работа в файлах](/ru/docs/viewers)     **|**     [DOCS. Согласования   >](/ru/docs/reviews)**</sub>