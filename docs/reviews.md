---
title: DOCS. Согласования
description: 
published: true
date: 2025-12-05T08:16:58.996Z
tags: 
editor: markdown
dateCreated: 2025-09-09T12:22:52.543Z
---

<sub>**[<   DOCS. Замечания](/ru/docs/issues)     **|**     [DOCS. Передача   >](/ru/docs/documentsTransfers)**</sub>
 
<details>
<summary>Что нового</summary>
  
> Здесь перечислены основные изменения. Для получения подробностей нажмите на номер версии.
{.is-info}

**Обозначения**
:fire: — новые возможности
:sparkles: — доработки функционала
:hammer_and_wrench: — исправление ошибок

----
**[2025.38](/general/updates/2025-38)** ^04.12.2025^

**:fire: Вывели статус согласования и реализовали работу с согласованием прямо из файла.**
  
**:fire: Реализовали группы согласований, которые можно задать в настройках типа и затем использовать для фильтрации согласований в реестре.**
  
:sparkles: Добавили копирование значений атрибутов файлов и коментариев версий при копировании через согласование. Атрибуты копируются только в случае создания первой версии нового файла (существующие атрибуты не перетираются).
  
:hammer_and_wrench: Убрали лишние поля при отклонении согласования на финальном этапе: выбор папки, чек-бокс о завершении с замечаниями и тип штампования.

----
**[2025.33](/general/updates/2025-33)** ^30.10.2025^

:sparkles: Добавили проверку при старте согласования на то, что есть хотя бы один пользователь с назначенной ролью. Если нет, процесс запустить нельзя.

:sparkles: Добавили поле для ввода комментария при завершении (в том числе отмены) согласования.

:hammer_and_wrench: Исправили расчет времени до конца согласования этапа.

:hammer_and_wrench: Поправили отображение встроенной подписи в файле после повторного подписания.
  
----
**[2025.31](/general/updates/2025-31)** ^16.10.2025^

:sparkles: Добавили кнопку перехода в комплект согласования после создания его из документов.

:sparkles: Добавили автоматическое напоминание по этапу согласования в последний день этапа.

:hammer_and_wrench: Исправили отображение отклонённых комплектов согласования в статусе **Черновик** при фильтрации.

:hammer_and_wrench: Исправили значение дельты завершённых согласований при экспорте.

:hammer_and_wrench: Исправили ошибку, при которой файл SIG отображался со штампом в комплекте согласования.

:hammer_and_wrench: Исправили ошибку, при которой при добавлении файлов в комплект согласования отображались не все комплекты.
  
----
**[2025.30](/general/updates/2025-30)** ^09.10.2025^

:sparkles: При создании пакета передачи из согласования теперь отправляются только выбранные галочками файлы.

:sparkles: Реализовали поиск по роли в списках с выбором пользователей и ролей.

:hammer_and_wrench: Поправили отображение подписей при некоторых сценариях.
  
----
**[2025.29](/general/updates/2025-29)** ^03.10.2025^

:fire: Реализовали повторное оповещение на текущем этапе согласования.

:hammer_and_wrench: Поправили отображение встроенной подписи у файла после согласования.

:hammer_and_wrench: Поправили удаление договорной и плановой дат из согласования.
  
----
**[2025.28](/general/updates/2025-28)** ^25.09.2025^

:sparkles: Добавили столбцы **Ответственный** и **Тип согласования** при экспорте согласований с файлами в Excel.

:hammer_and_wrench: Исправили ошибку записи договорной даты вместо плановой при экспорте согласований в Excel, а также отсутствие договорной даты при отсутствии плановой.

----
**[2025.27](/general/updates/2025-27)** ^18.09.2025^

:hammer_and_wrench: Исправили ошибку, при которой не отображались типы согласования при повторном запуске согласования.

----
**[2025.26](/general/updates/2025-26)** ^11.09.2025^

:hammer_and_wrench: Поправили, чтобы при создании комплекта согласования в выпадающем списке отображались только доступные пользователю типы согласований.

----
**[2025.25](/general/updates/2025-25)** ^04.09.2025^

:fire: Реализовали вывод информации о файле при штамповании документа.

:hammer_and_wrench: Исправили быстрый фильтр по роли.

> Информация о более ранних обновлениях доступна в закрытом Telegam канале для пользователей SIGNAL. Для добавления **[обращайтесь в поддержку](/general/support)**.
{.is-info}

</details>
 
----

# Вкладки{.tabset}
## 1. Создание согласования
###### 1. Создание согласования {#creating}
  
Для создания комплекта согласования перейдите в раздел "Согласования", нажмите “+” и в открывшемся окне заполните следующие  поля:

-   “Название” комплекта.
-   “Шифр” комплекта.
-   “Договорную дату” окончания процесса согласования. Договорная дата копируется в плановую, однако обе эти даты при необходимости можно заменить в дальнейшем
-   Выберите преднастроенный “Тип согласования".

![image-1705928780375.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeHcV4uMQD4rpjvvL9EWW2ON0lBpYB6V8jeMhIh7Q4iqmCJic66WZELZHzFfszhhT1PIn67RvG8BOS9kqukAGUgyOc9ngvWAv6Hif0vRWqk2fRmrm1kIeD6UfqZZebyR-qfK33DEWHJj1-50nlc4w?key=kHkyNYzGl_KhR1C7-5sbTA =70%x)

Затем откройте созданный комплект согласования или любой другой комплект из списка, нажав на строку в реестре, и добавьте файлы к комплекту. Добавление файлов в комплект осуществляется как из комплекта согласования, так и из раздела “Документы”.

-   Для добавления файлов непосредственно из комплекта, нажмите “+” и в открывшемся окне выберите необходимые документы.

![image-1705928800266.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcSJ8KtnCuhNGagOtE7YEkC5YbHD6UsWd34O98Tmypzadx0Vyd500NvjarUJQnq3BZjo7PvS4SCCcvWxtvYzqNvZJCbZDmsMVWZI8kIE5ePiwoSHdC3zE0SY42lwKd5TfvXrU2fOpQdrrERlzs-?key=kHkyNYzGl_KhR1C7-5sbTA =70%x)

-   Чтобы добавить файлы из раздела “Документы”, нажмите ПКМ → Добавить в согласования.

![image-1705928814895.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf_BRTTqAEjD4AdZjeOI7-sRMU2v-VgTEX76859J5PWeDthGNIsYQCOQl2k7Q7VsYXUj6b5C4ToMax2938p1uSVTbFozRyYrulVmDE8q_5rN5Yspxg0Z3aAMqxnRre_BNkCMgXRuLGp15SFPlBJTg?key=kHkyNYzGl_KhR1C7-5sbTA =70%x)

В верхней части находятся этапы согласования, при наведении на которые отображается информация об этапе. В правой части отображается состояние статусов каждого файла на этапе.

![image-1705928829667.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXczj2heOPfRyrCJS1YFV0xLngGt1zDR89_ZhoFyINk9oTTYsJlPzocF_tW_K8GDr5wwNfi6czSpawy1Pf2dJogw-jh4wRhoAyZnvBCwjCsZX44BTjQVJol4SqEyM7ueHjKl-sxxz918iVtEbhU6?key=kHkyNYzGl_KhR1C7-5sbTA =70%x)

**Условные обозначения:**

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf3OCVssbLrdgU_ojzxLJQMSLWc5T11tBJ5vXU7dFOJxzDbgFXueYXlUGjZfjN1F6J7rPfJhm2PBqeuHg2wQgS9EbCIFUV1KJFBCBbNXMzZV_WHzfFdUIUmWb--Mm2wvmuhM5UmVpNkHGP4Jc-HqQ?key=kHkyNYzGl_KhR1C7-5sbTA =50%x)
  
Далее см. [2. Запуск согласования](#start)

## 2. Запуск согласования
###### 2. Запуск согласования {#start}
  
Кнопка “Отправить” запускает процесс согласования.

![image-1705928915823.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXchmNmkjVbjylJA9SpfJka2m26VHcgZvxBoedHzTjhzLJ_UzdFasx9Vcrv_EbD40epdUETxl7JMXEOHE9CsSByUmDmqp5eN20pG7pgfoRNgkFetKxhzw7qmXDHYb4QlM2-7wRf72X8GJ5NNgjdL?key=kHkyNYzGl_KhR1C7-5sbTA)

Ответственному на первом этапе приходит оповещение на Email, сообщающее, что ему назначен комплект на согласование с указанием сроков проверки данного комплекта. Ссылка в письме открывает непосредственно комплект согласования.

![image-1705928927291.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf3aY3ZJjidvcGC-BWlg_yKz2rnq2GM17NGNJrEDyv4-2Vu41Zn9bb39Dn6YSLc-rX4SnDvr69EUg4I9A5aDD1nDJzmSA101toKKZzf9FRRPU7qUrw3Ql2eEAeZI1vUjJAKC5gM3NvqCZklooJmhA?key=kHkyNYzGl_KhR1C7-5sbTA)

Всем участникам процесса согласования файлы доступны только для чтения. Ответственный проверяет документы в комплекте, при необходимости выдает замечания и затем присваивает соответствующие преднастроенные администратором проекта статусы для каждого файла.

![image-1705928938984.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdx8WC88uP-Pv0_ZC_EzoIKvxQkElQayjkgIgEaxicmd0l45Q_g38DxpebY0rT-EEUgKk9jWIrDFtzxIbTz4LoPQqjYOfxqY1UwZMo5fdiYEDXf6SQOKMcF-tAADbixWbpxQhBvbBaxZxag7Go5sQ?key=kHkyNYzGl_KhR1C7-5sbTA =70%x)

-   Для установки статуса нескольким файлам, выберите их галочками, а затем в панели инструментов присвойте статус.
-   Для установки статуса одному файлу, выберите статус в правой части экрана.

После присвоения статусов нажмите  “Завершить этап” в правой верхней части экрана и оставьте комментарий для этапа, например, если файл был утвержден с замечаниями. Также есть возможность копировать комментарий с предыдущего этапа

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeTJwgNwToW1kvdBOOfk58bpcW8e4XmUgnpJlyeXjCHJ38a9ZSWwtIJEeisnPSuZ5BicKOBGpuDzitcK1ab45rGSCXILUZ4jA6Vyw1SI9q2GMp4de0kJAqxhOsRg-1laLq5kCOt4FFrEbPw4uFIAw?key=kHkyNYzGl_KhR1C7-5sbTA =70%x)

После завершения этапа комплект перейдет на другой этап согласования к следующему ответственному. Для получения подробной информации о предыдущем этапе наведите на иконку этапа.

![image-1705928981253.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf6Ha1d32Nqkq0jeDfJuHoO79lpBOubNO13rsWfZNbJxSZWd1DFCjupEoDyvIrsq8I_V_Npp2T8gMK58KHHqGD8Y8de-WuHEoatgLrM3XGhdILXwxv5MZCDrx8QbxoJbGt-BxIT-Z6NG4ClUkqBcQ?key=kHkyNYzGl_KhR1C7-5sbTA =70%x)

После создания замечаний к документу, в окне согласования отображается список замечаний по данному комплекту.

При смене статуса замечаний на **“Закрыто”**, замечание удаляется из списка замечаний по комплекту и отображается только в общем реестре замечаний.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXejGFfJE5sxJIrLR0dAye48xbyT6Xv8sk8CXYf08bA0qunW7G87B2z4Mw7vjVWRphNUr475QHvlPAmRhiCOdQD8QTYfyeZ2jo5K2wNWMJtCk35uVM41UpDGW0ZUrY7U4_FtXTXUqPl8zm1pRcTh1A?key=kHkyNYzGl_KhR1C7-5sbTA =70%x)

На этапе подписания документов при попытке завершить этап без подписи ЭЦП появится предупреждающее окно

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfpKIXzcefu9aQ-evlw82hbQHSzYC0EwFniOTC9yPQb9MeXOdOomYh7UKyzTPumc8B59hLyWXflf4GaEndTNa48s6gXD1eqgINo-4kbbA8zKUYebcSE9Muuj304FA9FypwX0HJklPzV1wSsL89V3w?key=kHkyNYzGl_KhR1C7-5sbTA =50%x)

При загрузке новой версии на согласование необходимо зайти в уже созданный комплект согласования, выбрать файлы и нажать 

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeGVorKVW5f8Z3lxpDrfJ74knjdrjN7746QiiuP49vBy85900oYArAEOQ5NgeUXcztm2UlSkbWcmVR3zMGDGU0cObCDWAmAjhPcXgi-zo4MSNqVc9dJoGPAoL8iDxbwb_ZzFNyhD6DOqRncoTCV?key=kHkyNYzGl_KhR1C7-5sbTA)

 - обновить версию.

При попытке отправить на согласование не актуальную версию документа появится предупреждающее окно

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfzZid6EsoS53ojKUEPOHPC64t3GxXVuCjpvSJ5S88OGcsPXCJjW99Hl12MhB_eG6fP1Q4mRc_1VmbZ7IQs8dHMIY6mDzcE-lPKE7GUQ4arqM0oAl1FycPg2CROWM6TvNmc5yPHJoOQ_AN3wri_Dw?key=kHkyNYzGl_KhR1C7-5sbTA =70%x)

Из согласования можно перейти к папке, в которую загружены файлы. Для этого ПКМ по файлу → Открыть папку.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdj8Z6F5Qa46uZYt2_7bkYzW9vBcXdK8Y97rkoBHWLJW9bXdF7gqrfr5LRGeJ6cyU_gtjJ5w6WDxkGDcrtRyEAPWvfmgP5l3hN9-VGBkS3FQMMthdwUKibQLeVn71Ddx79h2VSsGJ0yoSKSHfvw?key=kHkyNYzGl_KhR1C7-5sbTA =70%x)

После завершения процесса согласования появляется кнопка "Открыть папку", которая перенаправляет пользователя в папку, куда скопирован согласованный файл.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcgAkTEU6rGkb4nb9qTwJkjfppV5Q28YfkTjVwXts7QuuwpVdXATEZfpaXDrEsYw4FZ9u-ARn1OxhdH8z-Y70zC6Vf_l34HJrhb1R5sIX8VB-H6y14eLYbbuVlqMBrZfKcfLT0VkyF528Hy4WZ9eQ?key=kHkyNYzGl_KhR1C7-5sbTA =70%x)

## 3. Реестр согласований
###### 3. Реестр согласований {#register}

Все созданные в проекте комплекты согласования хранятся в табличной форме в разделе “Согласования”.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeDteF3KR42TZ0lfsUjExQeBwzkMFvdGJZfWzfFu4yhEH02vyW65-yjmdT_Bln-n9oo15GPGHpLG3yBnZgRvhg31dC5a2pyZ9xtReipiu1BwqqqDzWSGTGZ1J852r6hwHFfeN6qgKpihnYOhCaMDg?key=kHkyNYzGl_KhR1C7-5sbTA =70%x)

В реестре отображается необходимая информация о комплектах:

-   Номер и статус комплекта
-   Шифр комплекта
-   Название комплекта
-   Тип согласования
-   Договорная дата окончания согласования комплекта
-   Плановая дата окончания согласования комплекта
-   ΔД - разница между текущей датой и договорной
-   ΔП - разница между текущей датой и плановой
-   Дата первой отправки комплекта на согласование
-   Дата запуска на согласование текущей версии комплекта
-   Разница между текущей датой и плановой датой окончания согласования
-   Количество согласованных файлов к комплекте
-   Ответственный на текущем этапе согласования
-   Состояние процесса согласования

Для просмотра и редактирования комплекта, нажмите на строку согласования в реестре.

Для выгрузки реестра согласований необходимо выбрать “Экспорт”.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdWwWyFafdBB3LM3mDRRhxeDFP1197OKqiDggqQA3hC9oxJ4VFRkO3QO3QnJZn1zFHjoHSZ2CXwaMezkqhEdZ3omktdiWISUSl5LyJElLFfVrDLcISAOVZi2WzcMElPly_nwlHLrkPjAfDi1i1pQw?key=kHkyNYzGl_KhR1C7-5sbTA =70%x)

При выборе “Экспорт” выгружается таблица,аналогичная таблице в SIGNAL DOCS.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe51aYiWlzkHAhNfo_ULjCkkBzNOtV4TMN0ohi0NRUmgyuNufOaXKgnygjP2tVbhA7KbvYO9Ndw5iBtZ5gcXkrh9-9tyHD_FMzA-6tK4ja32oBvXxAHtPLuUGI1ExfKTxZszPQUtvGI1lAapNTNVg?key=kHkyNYzGl_KhR1C7-5sbTA =70%x)

При выборе “Экспорт с файлами” выгружается информация по каждому загруженному в комплект файлу,а также по каждому этапу согласований.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdUVODN4O1wGSfAKsXqk6K2O1LaZXVylhwDseZTCTxlqkowM88RIWohqqY0h6PNwmWC6w8pLD_YYLuuJ0xPVDul2goKgzj-lkAoFRiUd2PGhp0LWGNqLiaceED055Q8O8N_H7TdfYZ8aP4WneYbOw?key=kHkyNYzGl_KhR1C7-5sbTA =70%x)

## 4. Штамп и QR-код
###### 4. Штамп и QR-код {#stamping}
  
В процессе согласования комплекта есть возможность проставить штамп “В производство работ” и QR-код на документы. Для настройки необходимо обратиться к администратору проекта.

Если комплект согласован с замечаниями, то QR-код на листах желтого цвета.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdgz3zin7aXYG4vzpDpkcRW0cQLmshsRAu5JP-EgHnZ_r5yPyFX2XCYLIlSKqSrjJQlIAJ5sIdbglu4uXmDvQRfMAcY1OKeeZX4x8kzKKNF8qoHBZKO9WGTQ82ooJr5_96igVkJGwTkDovVSRUp?key=G9iO9SIlYFRrOTHZMZ_KDQ)

При сканировании QR-кода камерой телефона открывается страница в браузере с отметкой о действии документа.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXegbNDzJvi55vkdl7EN07BH3-MwLXUFEdqnN_cwnvshIe9pnZUpIFGU2GZXA-Np2S5ff1mzqolsPZ6d4Veoa1kFV3iw1ku9YenXg1OT2GDkQ-ePs1diPUxkHwQ6XGPcOfWzkKFtEKtam8uET2QX?key=G9iO9SIlYFRrOTHZMZ_KDQ =30%x)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe_9CGNmKPWK7copUHwR-cjkqHCG-Gp5gcuRexdojG6WvMaJk8F0eidjEJRMMu79V-e4aHdZgWZq88ge791SZ_ovP7L6-30YHJBFZIyuB0JD4EgrJ2Sp8iQcoqVj_GQGyRXVsIqQGXpr1KPwd0t?key=G9iO9SIlYFRrOTHZMZ_KDQ =30%x)

При переходе по ссылке с данной странице можно открыть документ для просмотра. При наличии учетной записи и доступа к данному проекту.

## 5. Администрирование
###### 5. Администрирование {#admin}
  
> См. [Настройки проекта → Согласования](/docs/settings)
{.is-info}


#
<sub>**[<   DOCS. Замечания](/ru/docs/issues)     **|**     [DOCS. Передача   >](/ru/docs/documentsTransfers)**</sub>