---
title: DOCS. Настройки проекта
description: 
published: true
date: 2025-10-24T07:45:02.758Z
tags: 
editor: markdown
dateCreated: 2025-09-09T08:02:36.643Z
---

<sub>**[<   DOCS. Введение](/ru/docs/intro)     **|**     [DOCS. Документы   >](/ru/docs/folders)**</sub>
> Описанные здесь функции доступны только **Администратору** компании
> {.is-warning}

> См. также **[настройки компании в SIGNAL HUB](/ru/hub/admin)**
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
:fire: **Реализовали экспорт настроек типов согласований.**
  
----
**[2025.30](/general/updates/2025-30)** ^09.10.2025^  
:sparkles: Реализовали поиск по роли в списках с выбором пользователей и ролей.
  
----
**[2025.29](/general/updates/2025-29)** ^03.10.2025^
:hammer_and_wrench: Исправили ошибку, при которой после обновления страницы не отображался выбранный пользователь в поле **Получатель** в настройках пакета передачи.  

----
**[2025.26](/general/updates/2025-26)** ^11.09.2025^
:hammer_and_wrench: Поправили отображение анимации чек-бокса в настройках согласований.

----
**[2025.25](/general/updates/2025-25)** ^04.09.2025^
:fire: Реализовали обновление настроек типов замечаний и согласований из другого проекта.
:fire: Реализовали вывод информации о файле при штамповании документа и соответствующую настройку.
:hammer_and_wrench: Исправили работу переключателя **Установить цвет пометок в соответствии со статусом замечания** в настройках замечаний.
  
> Информация о более ранних обновлениях доступна в закрытом Telegam канале для пользователей SIGNAL. Для добавления **[обращайетесь в поддержку](/general/support)**.
{.is-info}

</details>
  
----

Чтобы зайти в **Настройки проекта** в интерфейсе SIGNAL DOCS, нажмите на свой **профиль** в правом верхнем углу → **Настройки.** Изменения сохраняются сразу. Все внесённые изменения влияют только на текущий проект (отображается в левом верхнем углу).

# Вкладки{.tabset}
## 1. Замечания
###### 1. Замечания {#issues}

> См. также видеоинструкцию по настройке замечаний и атрибутов: [Telegram](https://t.me/signal_docs/198) [YouTube](https://youtu.be/0ki2I6Tl2KE)	[Rutube](https://rutube.ru/video/ff98be6edbe568e45ddec40a0ebce695/) [VK](https://vk.com/wall-223002264_14)
{.is-info}

Администратор проекта имеет доступ как к настройкам замечаний проекта, так и к редактированию любого замечания (см. [инструкцию по работе с замечаниями для пользователя](/ru/docs/issues)).

Управляйте типами замечаний проекта, доступами к ним определённых ролей, настройками и атрибутами. При выборе в левой части типа замечания в правой части отображаются его свойства.

> Доступно обновление настроек из другого проекта, если в нём типы имеют такое же название. См. далее **10. Обновление настроек**
{.is-success}

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcN7p4G_ZoYr_-N0jF6nQKeD0LJSHkKJhd88g3-CjV3oPI-DfOlktlMChzLbtOnH5-JjQj29o_A2vRglqPfRKftg9UHVfhLKhCi9HbDXKHUKHKiuiFjn2BSQ15XA7BtJ7Ag06FQaNPED0rn9xxL?key=DikC-fotJxKF9jvBMPQYCw)
### Вкладки{.tabset}
#### 1.1. Типы замечаний

Вы можете добавлять, переименовывать, копировать и удалять любые типы замечаний:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfqkx19vDS6iOptWrfKszAdcsGbddapcO1RsGqW8lDRORNoN0TgjUWyR0JtUt7dF-qAFr5DytlQKpLUgqcFr2aZsqRZ4KCcoKHFtYQPb-j-REOmb_5TYUxQ0qaumEFniTUJ_ZFS95al4ZpndjcJqQ?key=DikC-fotJxKF9jvBMPQYCw)

#### 1.2. Доступы

> См. также видеоинструкцию по ролевым доступам замечаний: [Telegram](https://t.me/signal_docs/208) [YouTube](https://youtu.be/X0aCckILkgc)	[Rutube](https://rutube.ru/video/df489d86a1ea6129a017b0d04bba640a/) [VK](https://vk.com/wall-223002264_19)
{.is-info}

Доступ к типу замечания определяется ролью пользователя (см. [HUB. Администратор → Создание ролей](/ru/hub/admin)) и его назначением на замечание.

> Пользователь может видеть следующие замечания в реестре:
> • назначенные ему (ответственный)
> • назначенные им (автор)
> • в которых он стоит наблюдателем
> • доступные для его роли (просмотр, создание и редактирование)
{.is-info}

> Пользователь может создавать следующие замечания:
> • доступные для его роли (создание и редактирование)
{.is-success}

> Пользователь может полностью редактировать (заполнять атрибуты, прикреплять вложения, менять статус) следующие замечания:
> • доступные для его роли (редактирование)
{.is-warning}

Для прав доступа действует логика повышения, т.е. если у роли стоит доступ на редактирование, то по умолчанию у нее есть доступ и для создания, и для просмотра.

Автор и ответственный при создании замечания имеют права на редактирование в конкретном замечании вне зависимости от роли.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc_ZRf3qW1mz4RMSNokBNvsSngkO2XFE05EKKefWUmrSGkPZoWOhtMm3x5d4NgiTZ9Rlayur5JHwgpZWR208uOtM67X6ghXdYehubFMx7FeD8VlQIooTAwFyKvhr7NKpT9i6GQJCPPiy2MUtRU8EQ?key=DikC-fotJxKF9jvBMPQYCw)

#### 1.3. Общие
Для типа замечаний доступны следующие общие настройки:
1. **Ответственный по умолчанию** — можно назначить роль или конкретного пользователя. В этом случае поле `Ответственный` в карточке замечания данного типа будет заполняться автоматически
1. **Срок устранения по умолчанию** — при необходимости указывается количество дней на устранение замечания. Итоговая дата будет сформирована по формуле `Дата создания замечания + Срок устранения по умолчанию`
1. **Пометка обязательна в PDF файлах**
1. **Описание обязательно** — если пользователь не заполнит поле `Описание` в карточке замечания, система не даст возможность сохранить замечание
1. **Дата устранения обязательна** — если пользователь не заполнит поле `Дата устранения` в карточке замечания, система не даст возможность сохранить замечание
1. **Статусы с обязательным комментарием**

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcegYChxvQgn26dBobcNZfkDDtUpsltNcJ6hgBSsMU6N0Fw3Hi3iUnJzzy4_MKI6Y8cpDv_MimCOOa_RfKL8255SCKgqt_F5Mqrv75b3vkNQoBCE1-17dJzHTKVyhKCmZo?key=DikC-fotJxKF9jvBMPQYCw)

#### 1.4. Атрибуты
Каждому типу замечания можно назначить атрибуты, в которых пользователь сможет указать дополнительную информацию по замечанию. Атрибуты добавляются из общего перечня, который настраивается для текущего проекта (см. далее **4. Атрибуты**).

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe4bGFglUBagjMQDugWoNB93gjVQbGdIFwL1kvYZHaK20h7MEfc3yGHrYru75eFuXjTfG6Mecd_EV8tKiKV_G1xfZeHr5SXjpzi0ede4tIz10jFirl9BN7iQn_My6INJ9pgAk49rSFyAAqI3-FcgQ?key=DikC-fotJxKF9jvBMPQYCw)

## 2. Согласования
###### 2. Согласования {#reviews}
  
> См. также видеоинструкцию по настройке маршрутов согласования: [Telegram](https://t.me/signal_docs/223) [YouTube](https://youtu.be/sJSfiUyzFkM)	[Rutube](https://rutube.ru/video/private/2a701de2947896e9640b16a4b3ee289b/?p=DZVhkcrU6mNHRJL7Cej3pQ) [VK](https://vk.com/video-223002264_456239043)
{.is-info}

В настройках согласования Администратор создает маршруты согласований для текущего проекта. В маршрутах назначаются, уровни доступа к согласованию, этапы согласований с ответственными за проверку документации пользователями. Также настраиваются статусы, штампование, подписание, копирование и оповещения. См. также [инструкцию по работе с согласованиями для пользователя](/ru/docs/reviews).

> Доступно обновление настроек из другого проекта, если в нём типы имеют такое же название. См. далее **10. Обновление настроек**
{.is-success}

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeSSWZcekF6T85BiF-pkhDM4Vogrq3lslLkT6mwIJoV2eu_cGmKPYlwmAC-cllbHILHlAK8fCd84WAjswNzjEDRZP570Mj7V-Qn1zsW6vw6g_LHd0gSeYUj7FCA5pdvjO0dGp5LA89pyHC8i3aVzA?key=WxzNGmtFs96UM_eMLcTLzg)
### Вкладки{.tabset}
#### 2.1. Доступы
Для каждого маршрута согласования можно назначить права доступа: кто будет видеть комплекты в реестре согласований, кто сможет инициировать согласования, кто сможет редактировать комплекты согласования.

> Пользователь может видеть следующие комплекты в реестре:
• Назначенные ему (ответственный любого этапа)
• Назначенные им (Инициатор) (может инициировать только с доступом на создание и редактирование)
• Доступные для его роли (просмотр, создание и редактирование)
{.is-info}

> Пользователь может создавать (добавлять файлы, обновлять версии, удалять файлы, перезапускать) следующие комплекты:
> • Доступные для его роли (создание и редактирование)
{.is-success}

> Пользователь может полностью редактировать следующие комплекты:
> • Доступные для его роли (редактирование)
{.is-warning}

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfeduGKDhgQKjo-QmZ1pgPuPBGbuZI1IsaR2AAO8gxiX0iS4bijoggA2ICNd5MKVfy9beF1Pqu8Ng-IwyR8M12TaDQvvxYt4HbJyVHS-VKAbX2QC3ENWHXFZqASau99rs6wAk-Me7u0nuoZrzSBmQ?key=WxzNGmtFs96UM_eMLcTLzg)

#### 2.2. Этапы согласований
Здесь назначаются пользователи или роли, ответственные за проверку документации. В процессе согласования каждый указанный ответственный на своем этапе проверяет документы из комплекта и ставит им соответствующие статусы. Можно указать до 20 ответственных.

Срок согласования устанавливается в кружке напротив ответственного (до 31 дней).

Если ответственный с включенным замком 

![image-1705928249611.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcAwQIQM8fMeGKHXcD-0CxmottOYrqeK1PdCHxEEgykea1xKQ42NYSfgwWp0ET14hBT1n3tW8ICzjgV1fC7zSiz7pCkuNcZxIL-pyyyxQFtFgiP4LfJ9B-Ba5fE_s25PT8zDP9QtMPuvShAY7DjwQ?key=WxzNGmtFs96UM_eMLcTLzg)

отклонит документ в комплекте как не прошедший проверку, то документ заблокируется и ответственные на следующих этапах согласования не смогут поставить статус для этого документа. Если замок отключен, то в случае отклонения файла, он все равно перейдет на проверку к следующему ответственному.

По умолчанию процесс согласования проходит последовательно 

![image-1705928267079.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf3dfsHCsnaDdcsC4gYq7AImxh9-rxYHI-6ZNUCVygO6VNcNaBnIyMyGUYk7AN6nb0g9GcO0O3zW7Kzk7vGJ4cDrXu9GsoeknYIa9q-up7rfyOue457-4962-Ob-smDAYJElgtGXlpzU7bNFbawlQ?key=WxzNGmtFs96UM_eMLcTLzg)

но начиная от трех пользователей появляется возможность выбрать параллельный 

![image-1705928275270.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdG6WtQpEXMGbSrt3v6H3ACsJkDEJEGNlegRE0kBHT4CVUCPjyQ6GnxhV8V7ylYF_ItAyK83jQV5Kznlka6nPij7aojm_KLpJWW4BxkPOg3WPUJVpizHVdurDzwUBFCbIi1Xe-y8ldyAaWiY8Rj?key=WxzNGmtFs96UM_eMLcTLzg)

порядок согласования. Таким образом, параллельный этап запускается и становится активным вместе с предыдущим.

Например, в данном случае этап 2 будет идти вместе с этапом 1.

![image-1705928364715.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf3KwhT6QwyRoKyFrHVpE9yo-rL3ZUG5LQmQrr-XLyavQMkOx6tUQH37nRwTlLB0L1SQ1lrTRsy8aJfXhyn4xu_kG83PytAwi0mQkhsMvkdmCkhHld6wMD3CfXF5ISg6F3EmJue59tbpFt_NlzvRQ?key=WxzNGmtFs96UM_eMLcTLzg)

#### 2.3. Статусы

В поле “Статус” выбирается тип статуса, являющийся логической опцией, отвечающей за продвижение документа к следующему этапу согласования: Утверждено или Отклонено. Таким образом, утвержденный документ переходит к следующему этапу согласования, а отклоненный документ не переходит.

![image-1705928408533.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfdpFt8fnGDJfWwpVYfsBXapte8HHIvXLKo_YefA3H-i1kdhGYkVqCpADe9t8VVp9nStiXY4_8sIflcMriK_5ThYxvUXY6eJuHg2fDMV2eUC0Au8VIu1oiYkt4pdpcRrQtdE_Aq7KQwL5X_64kYHQ?key=WxzNGmtFs96UM_eMLcTLzg)

В последующих полях указываются название и иконка статуса, которые будут отображаться для пользователей в процессе согласования. Можно добавить до 10 статусов.

#### 2.4. Штампование

На этапе “Штампование” проставляются штампы и QR на документы из комплекта.

Сначала из списка выбирается тип штампования:

-   Штамп - будет проставлен только Штамп
-   QR-код - будет проставлен только QR
-   Штамп и QR-код - будут проставлены Штамп и QR
-   Не штамповать

![image-1705928420720.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXca6bdP0aI8ymPjD7BhfIQmCLDtvowWs-rBiqOI0Yo5q5o_OrSIvV6k9Leo5470fkBWY-PjJ5HxFofoTx-dr68z2OR4hsPAGzTlbieygRvNFfAVM6Sf988Uq-16yaGr-kCgxRQGd_sMkmeL0uUgVw?key=WxzNGmtFs96UM_eMLcTLzg)

Затем выбирается Ответственный за этап штампования, который проверяет правильность штампования документов.

-   Если выбрана опция "Завершать этап автоматически", то при успешной обработке всех файлов (штампование) этап автоматически переходит на следующий. Однако, если произошла ошибка хотя бы с одним файлом, Ответственный получает уведомление на электронную почту о возникшей ошибке. В таком случае, Ответственному требуется принять соответствующие меры: либо повторно отправить файл для штампования, либо продолжить согласование без этого файла.
-   Если опция "Завершать этап автоматически" не выбрана, то после штампования файлов ответственному всегда приходит уведомление по электронной почте о завершении этапа. Он проверяет правильность нанесения штампов и принимает решение о продолжении согласования. Если все в порядке, он может перейти к следующему этапу. Если есть ошибки, то Ответственный повторно отправляет файлы для штампования или продолжает согласование без них.

Для QR и Штампа заполните страницы наложения (страницы, на которые будут нанесены штамп и QR). Для Штампа также заполните поля Компания, ФИО и Должность.

По умолчанию для полей “Масштаб”, “Отступ” и “Размер” заполнены оптимальные значения для простановки штампа и QR. При необходимости замените данные значения.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeoKXsJa-XFsbJuPWRm18pk6osbBKp69YGmPqyKB_OiR1TVmeiZ11a7eAOB78v3RK4j38hvrqwJ2gNrUqMCuS8fejybfoRnV1NkAKG95pIUAXSqOeBNSss8fYV5zegVA8Q4dRbWd5GQsNwue7hRDw?key=WxzNGmtFs96UM_eMLcTLzg)

#### 2.5. Подписания

На этапах подписания назначаются пользователи или роли, которые ответственны за подписание документов с помощью ЭЦП. Также указывается срок подписания документов (до 31 дней).

Подписать документ можно двумя способами: встроенной подписью или отдельным sig файлом. Встроенной подписью можно подписать только PDF.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe69CIItS94WQ06zE616P1h9ZQ0QNpybcbOWBQNm1AASVo32mwmmxIBzcVwfmJRk3AEA1BwsSRQ3dy-AsFND-NYWmwtI0uuQwCB6uhheDdoRe0zWI9FvbORAdF-T5WXpe1km8WpEJxCU6HgyUP7?key=WxzNGmtFs96UM_eMLcTLzg)

Как и этапы согласования, подписания могут проходить последовательно или параллельно

#### 2.6. Копирование

На данном этапе указывается папка, в которую необходимо скопировать проштампованные документы из комплекта.

![image-1705928611272.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc86mV80j4A1Jv12xq5k11Vn4Rwfxz76UcFDSd0SGSl5cXlFacUNxRPCfqZkmym9LNg_IO1t3sPKpXx2NCRcI2izqLWaQiWJWc6tdAQwHIT492FwQNRIFpY9dxGmVFmiFutBCByzKnCWn6RXfoRwg?key=WxzNGmtFs96UM_eMLcTLzg)

Можно выбрать несколько вариантов копирования:

-   Не копировать
-   Копировать в конкретную папку - Папка для копирования указывается в настройках согласования
-   Отстроить структуру - Указываются две папки: исходящая папка - это та, относительно которой считывается путь до согласованного и копируемого файла. Входящая папка - это та папка, в которой дублируется аналогичная структура папок для складывания копируемых файлов.
-   Указать папку на финальном этапе согласования - Ответственный на последнем этапе согласования указывает папку, куда будут скопированы файлы из комплекта

#### 2.7. Оповещение

Опция Оповещения позволяет указать пользователя, роль или Email, которым будет приходить полный отчет о согласовании после его завершения

![image-1705928699336.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfXjjenmWbHIl3qr9tZ4PC07YB9UMxRAodGMzjVIGVwKxohfRysIoDe-ozHMF6n65vnSUr2F0M1lQV4KHGS_yDNwO6Z3Y47QOZzoNhtPMgz0OfJUaALD4nzvPQIDOwV7_MnwMkSxYLjlX2OHDho?key=WxzNGmtFs96UM_eMLcTLzg)

## 3. Передача
###### 3. Передача {#documentsTransfer}

> См. [инструкцию по работе с передачей для пользователя](/ru/docs/documentsTransfers)
{.is-info}

## 4. Атрибуты
###### 4. Атрибуты {#attributes}
  
> См. также видеоинструкцию по настройке замечаний и атрибутов: [Telegram](https://t.me/sgnlpro/198) [YouTube](https://youtu.be/0ki2I6Tl2KE)	[Rutube](https://rutube.ru/video/ff98be6edbe568e45ddec40a0ebce695/) [VK](https://vk.com/wall-223002264_14)
{.is-info}

Атрибуты -- дополнительные поля для заполнения информации по замечаниям, папкам и файлам.

Атрибуты создаются администратором.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeBSru7dO3P1Pazz21uZ8dMsw01MI0l710h1b8T1FubVH3OE0uadcZRlxu57QeElKNAjDV2eXLiBVaeqDvk3R8v-3tc_WfcuUocbx1PVs50P35HY3Mw0WniBxg0eOc1jwHuJ5nSD_ZccxRV1PrD1Q?key=DMy4N3yohGr1J0s7rFEk7w)

Заполнить поля:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcwRy6X5Nt0Jpq7AarP0E3wTTuhkmynE_wv7G6fHGQcj34y3Jv-DAIh8mfjnwUtgJBzG2MA_rXuyFVcS25KaeT2OntOaqLcPrCnV6FIbMQad2QRcj4wLtYF6ZwYBEzLBk5euOCMlzLKjucafGKhSQ?key=DMy4N3yohGr1J0s7rFEk7w)

Типы атрибутов:

-   **“Текст”** позволяет пользователю ввести произвольный текст для предоставления дополнительной информации, пояснений или комментариев к замечанию.
-   **"Да/Нет"** представляет собой логическое значение, которое позволяет пользователю выбрать один из двух вариантов ответа: "Да" или "Нет". Он используется для получения простого ответа на вопрос.
-   **“Список”** используется для предоставления пользователю списка предопределенных вариантов ответа, например, для выбора вида работ, вида нарушения и т.д.
-   **"Дата"** позволяет пользователю выбрать дату или ввести ее вручную. Он используется для указания временных меток или сроков выполнения, связанных с замечанием.

Тип назначения:

-   **Файл** \- атрибут назначается на папку,но заполняется к каждому файлу отдельно внутри папки. Значение атрибута будет копироваться в замечания к файлам в папке,если данный тип атрибута будет добавлен в указанный тип замечания.
-   **Папка** - атрибут может быть добавлен на папку и редактироваться как свойство папки. Значение атрибута будет копироваться в замечания к файлам в папке,если данный тип атрибута будет добавлен в указанный тип замечания.
-   **Отсутствует** \- атрибут только для замечаний.

Каждый атрибут может быть обязательным или необязательным. За это отвечает переключатель

![image-1703763310200.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfFtI5aXO9fjGHTAi4wJo3UpiX51MxDqIm2GRgNa0F2r_k8P1a0NKG4pF-5osnDDpC-EH1s0qj3AeEW2frxWv0WX2kxrRC_QjgEEOO7l9tG_9Qu-T74rocjzNqgrOKn31MWD_I1NcYjdw_ZzNEA?key=DMy4N3yohGr1J0s7rFEk7w)

### Пример:

Создать атрибут

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXexvqgujuuFwLEcVK9ViXiDGeJWLTpx2KUOXQ3zGn8hR1X8COUhGwtKYMnw7SqukqIAatpm_GS-vgW90MN-79_DBfCNNzXhlh6fCVSGkGCU0mBZztg87xlixnwrrijXLXkIy-b8DhI9KAJjUYf7iw?key=DMy4N3yohGr1J0s7rFEk7w)

Добавить атрибут в тип замечания

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe2jUN-ehplC3vSilKCcLCtzHY2gEFNqfWUBmhmP4i6_lFn6eaUumVjWfbWCmT-RgfgQXKBunWKpCwdDKe_NnlnsIqkSAbGLT2yDBdsEvNP4DdxsLF6JP8YG5qwHEoGlgwoAxiBm2vjhkqgTS1s?key=DMy4N3yohGr1J0s7rFEk7w)

Назначить атрибут на папку

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe9riE-4mxmFW2TRXUFtT8R28xzspXfAzZa5AzCt-ds0j7-pySHEP03UbOxQMADZb95k99pdPVMZCUDisJnfnJi7GemJrBA0ZZef56dL89kx2sWBOmQWkgLHbl1efd4KElBkJRLUQV1bq_ZWL-RwA?key=DMy4N3yohGr1J0s7rFEk7w)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdEzoYx0aIcjCffGSRUwT7Gc3Q3th-r5MFV52y2rDzt4ywG63BADGQy8ELZpwcPyaDQFBZoXuCrgZT5I0af9bl8sCpWSGFMRJO9OzrOfDV9BP_tz1vZnh9VzWXfNaDPT4hV3Srl-Aqw2q7GZHja6A?key=DMy4N3yohGr1J0s7rFEk7w)

Открыть настройки

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfuVOgKpNPaWYiJfP_Ec_2HRDucdqR5_vyFYU25yrvT22VK903p4UXd65pBqzMKS3hnFcrY5tMvT-OZIab2T3PpkJHsp_WGutaXoQ3TvNplQRHVcBEfckP2CPo1kD19TIhectFdf1MjMq2NTm4iMA?key=DMy4N3yohGr1J0s7rFEk7w)

Назначить атрибут на файл в папке

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXclRi14EfzbhnpkQiYJvdj2qJ5vNpAX5HV3rUUE5fj0LEaonCfZPk7L0BJ7Cr8Mlip365hlQw1Kv4T3yVkHgC4gnZ-u3nBIlLyD65OWopudJuhE8rrSYsj7Vze6KDehFEAO1wAWL9OOVYkp57sb?key=DMy4N3yohGr1J0s7rFEk7w)

Введите значение:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfqY7IlCfzGeuduzad4XAguWSFViSWBYCWq25pMeR0q0s_1QZFjdaDnED_6w6Mcridggd5ZlyPtBGyCLrzCjpO91Rk5cocIb_y_9frcWMxLRynCA3VUoDOyns-8ZOAYtTAdd4T6epH8PWYCTFBZEg?key=DMy4N3yohGr1J0s7rFEk7w)

Создать замечание к файлу. Атрибут заполнится автоматически

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeTisz4zdOdHNvAyy0xVZLdLwVgTIgKffdNb5Nq5AhVccwaNabT2F9xMW0AahBGD_4xwoev_QuRVr_3juUjWWJ67lKa-fC2IRp_0woccV51ZobQoLZOS3xegjCbej-P-LmlOrT-ZCbfNia-6HTq_w?key=DMy4N3yohGr1J0s7rFEk7w)

## 5. Сервер
###### 5. Сервер {#server}
  
> См. [DOCS. Дополнительно → Установка MinIO на Linux / Windows](/ru/docs/more)
{.is-info}
  
> См. также видеоинструкцию по прочим настройкам: [Telegram](https://t.me/sgnlpro/231) [YouTube](https://youtu.be/sisd758B0tM)	[Rutube](https://rutube.ru/video/private/da44a5f3ead58f1d37c4e7bba841833b/?p=_mjhTQOP2yHqHrhM15zYdA) [VK](https://vk.com/video-223002264_456239046)
{.is-info}

## 6. Сервисы
###### 6. Сервисы {#services}
  
> См. также [DOCS. Дополнительно → Интеграция с Tangl](/ru/docs/more)
{.is-info}
  
> См. также видеоинструкцию по прочим настройкам: [Telegram](https://t.me/sgnlpro/231) [YouTube](https://youtu.be/sisd758B0tM)	[Rutube](https://rutube.ru/video/private/da44a5f3ead58f1d37c4e7bba841833b/?p=_mjhTQOP2yHqHrhM15zYdA) [VK](https://vk.com/video-223002264_456239046)
{.is-info}

Для просмотра 3D моделей в сервисе SIGNAL DOCS используются **Forge Viewer** и/или **Tangl Viewer**. Администратор проекта может выбрать, каким вьювером просматривать модели для каждого проекта. Переключение находится в "Настройках" в разделе “Сервисы".

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdJKntu5PbfCiBxAg_PYaLBCmcvkBXXsPjt9350pvu3LgOGoqN_EeEQIVmeo9glzf4HSt8KRjdLbpNgycsTV9slZx9QgefaMu8dBpsoPACvzS5bCGJSedpTzJbkNzsPKOg?key=mSlD0f1iO2mqCDbxSYrHzQ)

**Forge Viewer** позволяет просмотреть следующие форматы файлов:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeEPxyBT1yqLC3G6KS64ka2CneTJJDfysi6VXZwppvGZNM2k22YHOgXfhz-mdGsTnyCAo4b0KLuVgxlyruRwbnwvmo0VRFSqbja2kSVAfF7mao2GYZA1OpnVnKbrHlMZ1aGLKk-A-kbhHItcb__?key=mSlD0f1iO2mqCDbxSYrHzQ)

**Tangl Viewer** позволяет просмотреть IFC формат и RVT (с помощью плагина). 

## 7. Уведомления
###### 7. Уведомления {#notifications}
  
> См. [DOCS. Уведомления](/ru/docs/notifications)
{.is-info}
 
> См. также видеоинструкцию по прочим настройкам: [Telegram](https://t.me/sgnlpro/231) [YouTube](https://youtu.be/sisd758B0tM)	[Rutube](https://rutube.ru/video/private/da44a5f3ead58f1d37c4e7bba841833b/?p=_mjhTQOP2yHqHrhM15zYdA) [VK](https://vk.com/video-223002264_456239046)
{.is-info}

## 8. Доверенности
###### 8. Доверенности {#powerOfAttorney}
  
> См. видеоинструкцию по прочим настройкам: [Telegram](https://t.me/sgnlpro/231) [YouTube](https://youtu.be/sisd758B0tM)	[Rutube](https://rutube.ru/video/private/da44a5f3ead58f1d37c4e7bba841833b/?p=_mjhTQOP2yHqHrhM15zYdA) [VK](https://vk.com/video-223002264_456239046)
{.is-info}

## 9. Права доступа
###### 9. Права доступа {#foldersPermissions}

> См. также видеоинструкцию по настройке прав доступа: [Telegram](https://t.me/sgnlpro/194) [YouTube](https://youtu.be/QwunTC_lYDo?si=KzwE04tc3VoZgmfk)	[Rutube](https://rutube.ru/video/328b9099b6b7bea60e0235993cab47ab/?r=wd) [VK](https://vk.com/wall-223002264_13)
{.is-info}

В SIGNAL DOCS администраторы проекта могут давать различные права доступа пользователям и ролям на конкретные папки.

-   **Просмотр** \- пользователи могут только открывать и просматривать файлы в папках
-   **Скачивание** - пользователи получают возможность скачивать файлы из папок
-   **Загрузка** - пользователи получают возможность загружать свои файлы в папку
-   **Редактирование** - пользователи получают полный доступ на редактирование файлов в папке (удаление, переименование и т.д.)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcWQWZqiRxX7JS_D20YPLEFX7eV26pgTIHa7CeFRjB1lqkoocLLWfFkDwjHxHFt9suT83T5nc3DyxK7kv9WOPtZJPgEJ9JxOqgU8Ajc6ewir1BQCw9qH12RLgCGvhFvyJCXt1rHmbSD8C3skqHx?key=H_gsEk68-7fVudPNDTx0iQ)

### Способ 1. Настройки прав доступа в настройках
1\. Перейдите в “Настройки” раздел “Права доступа”

2\. Строками является папочная структура проекта. Колонки отвечают за уровень доступа. В ячейках выберите роли, в соответствии с их доступом к папкам

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdHl7VFjffKFYIRlREV8BTxmfCPoGAkhhmozKYOe491o4mWV2y-vcIGucf0Pt10fW9rJRoJXHoMSZGDJS3iIYKJjbaPboEGG4GO_v-3_uSGZPBdlEVRG2KMp1EBx7aclAs?key=H_gsEk68-7fVudPNDTx0iQ)


### Способ 2. Настройки прав доступа через папочную структуру
> См. [DOCS. Документы → Дерево проекта → Настройка прав доступа к папкам](/ru/docs/folders)
{.is-info}
  
## 10. XML документы
###### 10. XML документы {#xml}
Создайте тип схемы, настройте доступы на просмотр, создание и редактирование и загрузите нужные файлы XSD (шаблоны XML), например с [сайта Минстроя](https://www.minstroyrf.gov.ru/tim/xml-skhemy).

## 11. Обновление настроек
###### 11. Обновление настроек {#updating}
  
При работе в SIGNAL DOCS администратор может обновить параметры замечаний и согласований текущего проекта из другого  (например шаблонного) проекта.
1. В шаблонном проекте, в настройках администратора, отредактируйте замечание или согласование и настройте его необходимые параметры:
![update-issues-reviews-1.png](/update-issues-reviews-1.png)
2. Зайдите в другой проект (в примере: из `Проекта 0` в `Проект 1`), создайте замечание / согласование с таким же названием как в шаблонном проекте и нажмите **Обновить настройки из другого проекта:**
![update-issues-reviews-2.png](/update-issues-reviews-2.png)
3. Выберите шаблонный проект и необходимые типы замечаний/  согласований, настройки которых хотите обновить:
![update-issues-reviews-3.png](/update-issues-reviews-3.png)
4. Выберите, какие параметры нужно обновить:
![update-issues-reviews-4.png](/update-issues-reviews-4.png)
5. Нажмите **Завершить,** после чего в замечаниях / согласованиях текущего проекта обновятся выбранные параметры:
![update-issues-reviews-5.png](/update-issues-reviews-5.png)
> 
> Для замечаний к переносу доступны настройки **Доступы** и **Общие**
{.is-warning}

> Для согласований к переносу доступны настройки: **Доступы, Этапы, Статусы, Подписания, Оповещения**
{.is-warning}

#
<sub>**[<   DOCS. Введение](/ru/docs/intro)     **|**     [DOCS. Документы   >](/ru/docs/folders)**</sub>