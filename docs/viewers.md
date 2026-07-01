---
title: DOCS. Работа в файлах
description: 
published: true
date: 2026-07-01T14:58:11.185Z
tags: 
editor: markdown
dateCreated: 2025-10-16T13:16:45.534Z
---

<sub>**[<   DOCS. Документы](/ru/docs/folders)     **|**     [DOCS. Замечания   >](/ru/docs/issues)** </sub>
  
<details>
    <summary style="font-size: 16px; color: #0D47A1; background: #E3F2FD; border-radius: 7px; border: 1px solid #64B5F6; display: flex; gap: 10px">
        <span style="font-size: 20px;">🔄</span>
        <span style="flex-grow: 1;">Что нового в этом разделе</span>
</summary>
  
> Здесь перечислены основные изменения. Для получения подробностей нажмите на номер версии.
{.is-info}

**Обозначения**
:fire: — новые возможности
:sparkles: — доработки функционала
:hammer_and_wrench: — исправление ошибок

----
**[2026.8](/general/updates/2026-8)** ^07.05.2026^
  
:fire: Реализовали ленту с предпросмотром всех файлов.
  
:fire: Реализовали создание и редактирование сборок по общим координатам и внутренним началам.
  
:sparkles: В браузере модели для файлов Navisworks при просмотре в Forge добавили поиск по Id элемента.
  
:sparkles: В сборках добавили кнопку `Вернуться к общему виду`, которая отображается при переключении на другие виды моделей.
  
:hammer_and_wrench:  Поправили калибровку и устранили ещё несколько небольших ошибок линейки PDF в мобильной версии.

:hammer_and_wrench: В Forge вместо идентификаторов в обозревателе документов теперь отображаются имена файлов.

:hammer_and_wrench: Исправили ошибку, при которой закрывалась сборка при добавлении вложения в замечание.
  
----
**[2026.7](/general/updates/2026-7)** ^23.04.2026^
  
:sparkles: В ошибку при открытии Forge добавили кнопки включения прокси.
  
:sparkles: Сняли ограничение у пользователей с доступом на `Загрузку` редактировать офисные документы.
  
:sparkles: Отключили автосохранение офисных документов, чтобы избежать большого количества версий (временное решение).
  
:hammer_and_wrench: Вернули работоспособность кнопки `Печать` при просмотре PDF в мобильной версии.
  
----
**[2026.6](/general/updates/2026-6)** ^09.04.2026^
  
:fire: Реализовали линейку — инструмент измерения расстояния между двумя точками при просмотре PDF.
  
:sparkles: Добавили дополнительный прокси для Forge (три точки в правом верхнем углу).
  
:sparkles: Оптимизировали открытие больших PDF с помощью серверной синхронизации.
  
:sparkles: На верхней панели файла вывели путь до корневой папки.
  
:hammer_and_wrench: Исправили ошибку при изменении настроек отображения в сравнении PDF.
  
:hammer_and_wrench: Поправли закрытие офисных документов в мобильной версии.
  
----
**[2026.5](/general/updates/2026-5)** ^26.03.2026^
  
:fire: Встроили онлайн-редактор офисных документов.
  
:fire: Встроили просмотрщик облаков точек до 5 Гб.
  
:sparkles: В сборки добавили версии файлов с возможностью перехода к ним и предупреждение, если используются неактуальные версии.

:sparkles: В замечаниях в сборках теперь доступны функции прикрепления элементов и пометки.
  
:hammer_and_wrench: Исправили некорректное отображение некоторых шрифтов при серверной обработке PDF.
  
----
**[2026.4](/general/updates/2026-4)** ^12.03.2026^
  
:fire: Реализовали просмотр всех опубликованных листов всех моделей в сборке.
  
:sparkles: Добавили поиск и выделение элемента по Id в Forge.
  
----
**[2026.3](/general/updates/2026-3)** ^03.03.2026^
  
:sparkles: Оптимизировали серверную конвертацию больших PDF.
  
:sparkles: Добавили дату создания версии при просмотре в Forge.

:sparkles: Добавили кнопку Свернуть все в браузере модели в Forge.

:sparkles: Внесли ряд доработок в новый график Ганта.
  
----
**[2025.40](/general/updates/2025-40)** ^17.12.2025^
  
:sparkles: Внесли ряд улучшений в новый график Ганта.
  
----
**[2025.39](/general/updates/2025-39)** ^11.12.2025^

:hammer_and_wrench: Исправили перелистывание страниц в обозревателе при переключении страниц в PDF в Forge.

:hammer_and_wrench: Исправили ошибку, при которой импортировались лишние строки в MPP.
  
----
**[2025.38](/general/updates/2025-38)** ^04.12.2025^
  
:fire: Вывели статус согласования и реализовали работу с согласованием прямо из файла.
  
:fire: Реализовали функционал создания и редактирования графиков Ганта в DOCS в собственном расширении .sgmpp, который в дальнейшем планируем развивать в отдельном модуле для постановки задач.
  
:hammer_and_wrench: Убрали окно выбора просмотрщика моделей Tangl или Forge в случае, если в настройках проекта включен только один из них. Теперь модели открываются сразу в нужном просмотрщике.
  
:hammer_and_wrench: Поправили, чтобы для просмотра актуального статуса обработки модели не приходилось обновлять страницу.
  
:hammer_and_wrench: Исправили некоторые другие ошибки при взаимодействии с моделями.
  
----
**[2025.36](/general/updates/2025-36)** ^20.11.2025^
  
:hammer_and_wrench: Устранили проблему блокировки антивирусом при скачивании больших файлов.
  
:hammer_and_wrench: Устранили проблему сжатия некоторых чертежей при сравнении двух версий DWG файлов в Forge.
  
----
**[2025.35](/general/updates/2025-35)** ^13.11.2025^
  
:fire: Добавили функцию печати из PDF.
  
----
**[2025.34](/general/updates/2025-34)** ^06.11.2025^
  
:sparkles: Добавили новые функции просмотра модели в Tangl: включение / отключение прогрессивного рендера, настройки графики, включение / отключение перспективной камеры.
  
----
**[2025.33](/general/updates/2025-33)** ^30.10.2025^
  
:sparkles: Сделали изменение масштаба листа при просмотре PDF при нажатии Enter / Esc / смене фокуса. Изменение масштаба по истечении времени убрали.
  
----
**[2025.32](/general/updates/2025-32)** ^23.10.2025^
  
:fire: Реализовали создание электронных документов по XML-схемам.

----
**[2025.31](/general/updates/2025-31)** ^16.10.2025^
  
:fire: Реализовали конвертер Tangl для Revit файлов.
  
----
**[2025.30](/general/updates/2025-30)** ^09.10.2025^
  
:fire: Реализовали создание текстовых файлов прямо в DOCS.

----
**[2025.27](/general/updates/2025-27)** ^18.09.2025^
  
:fire: Реализовали альтернативный вьювер для просмотра DOCX и EXCEL.
  
:hammer_and_wrench: Устранили долгую загрузку листа PDF при повороте.
  
:hammer_and_wrench: Поправили названия моделей в сборках (вместо названий отображались идентификаторы).

> Информация о более ранних обновлениях доступна в закрытом Telegam канале для пользователей SIGNAL. Для добавления **[обращайтесь в поддержку](/general/support)**.
{.is-info}

</details>

----

# Вкладки{.tabset}

  
## Офисные документы

  
  SIGNAL поддерживает форматы файлов Microsoft Office в двух просмотрщиках - Collabora и MS Office. Первый просмотрщик также поддерживает и редактуру документа прямо в браузере.
  
### Вкладки{.tabset}
  
  
#### 1.1. Работа с DOCX, XLSX, PPTX
##### 1.1. Работа с DOCX, XLSX, PPTX {#office}
  
> См. также [пользовательскую справку](https://help.collaboraoffice.com/latest/en-US/text/shared/05/new_help.html) от разработчика офисного редактора.
{.is-info}

  
  При открытии офисного формата файла (doc. xls. и др.) появляется интерфейс ранее назначенного просмотрщика, по стандарту первым открывается Collabora. 
  ![снимок_экрана_2026-05-15_141653.png](/снимок_экрана_2026-05-15_141653.png)
  	В верхней части интерфейса можно активировать редактор офисных форматов. Он работает как программа Word и Excel и повторяет их стандартный, знакомый интерфейс. При редактировании файлов, для других пользователей над файлом появлеятся иконка замка, что не дает другим пользователям перемещать, переименовывать или как-то взаимодействовать с файлом пока идет редактирование документа. Значок замка пропадает либо после выхода из сессии редактирования пользователем, либо автоматически через несколько минут.
  ![снимок_экрана_2026-05-15_142101.png](/снимок_экрана_2026-05-15_142101.png)
  Редактирование файла возможно несколькими пользователями одновременно, как при работе в форматах Google Docs, то есть пользователи видят курсоры других пользователей и их внесенные изменения в настоящем времени.
  
  
  
  
  
  
  
  
  
#### 1.2. Создание графиков MPP
##### 1.2. Создание графиков MPP {#mpp}
  
  Через кнопку "+" можно создать редактируемый файл MPP в котором можно создавать задачи, назначать на них срок выполнения и привязывать друг к другу.
  ![chrome_x8yynr0qjz.png](/chrome_x8yynr0qjz.png)
  Внутри файла, задачи создаются через кнопку "Редактировать", после чего в пустые колонки можно внести названия задачи и его срок
  ![chrome_t2qpwabnjd.png](/chrome_t2qpwabnjd.png)
  Сам визуальный график также редактируемый и ячейки задач можно привязывать друг к другу удерживая левую кнопку мыши по ячейкам.
  
  
  
  
## CAD
### Вкладки{.tabset}

  
  
  
#### 2.1. Просмотр BIM-моделей
##### 2.1. Просмотр BIM-моделей {#bim}
  
> См. также видеоинструкцию по работе с BIM моделями: [Telegram](https://t.me/signal_docs/316)
{.is-info}
  
> Среда общих данных SIGNAL DOCS поддерживает работу цифровыми информационными моделями прямо в браузере вашего устройства. Просматривайте свойства изменений, комментируйте модели а также сравнивайте их версии
{.is-info}  

На текущий момент в SIGNAL DOCS Представлено 3 просмотрщика моделей - Autodesk Forge, Tangl Viewer, SIGNAL Viewer
  
|              | Autodesk Forge                | Tangl Viewer | SIGNAL Viewer |
|-----------------------|-------------------------------|--------------|---------------|
| **Форматы файлов**        | .rvt .nwd .nwc .fbx .skp .ifc | .rvt .ifc    | .glb          |
| **Инструменты измерения** | +                             | +            | +             |
| **Инструменты сечение**   | +                             | +            | +             |
| **Свойства элементов**    | +                             | +            | +             |
| **Дерево проекта**        | +                             | +            | +             |
| **Сборки файлов**         | +                             | +            | -             |
| **От 1ого лица**          | +                             | -            | -             |
| **Сравнение версий**      | +                             | -            | -             |
| **Пометки в файлах**      | Привязка к элементу, рисунок  | -            | -             |  
  
Для открытия модели необходимо один раз ее обработать. Для этого нажмите ПКМ на файле → “Обработать в Autodesk” и/или “Обработать в Tangl”. Для обработки несколько моделей воспользуйтесь соответствующими кнопками на панели инструментов.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdaGpEX-ZoaHsyYBhqCGFC64bsCbFTUhYKlsH4WMucWC_XzOZLNefvJ1PVNGxC7-Pe9jCReMQwxRdNJ3daiW9IkrBYcK0hcw114NAPg1SON9ESyEaX54m0LGuXYgNYBVz9Zs8uYhWd80EW2mFRqjA?key=i8J0tGtIeCmYFt7QxAzbTw =70%x)

 
##### Autodesk Forge
  
В **Forge Viewer** доступен стандартный набор инструментов для просмотра моделей.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfeiL0vxXYVsOLFp8EZdtfqp5ilqY6CRW6yWM_umrcBY1PJ20g7H4Gj_2ecV28U53bNnqvnuu7M8x5Zv3JQBfxNeDeYdxTMnB2El17U5ixHEVzs8oO6kPJUQQCKLEo-eDyOjzg03dCTJWQeprYzTg?key=i8J0tGtIeCmYFt7QxAzbTw =70%x)

1.  Обход от первого лица
2.  Линейка для измерений
3.  Сечение
4.  Обозреватель документов
5.  Уровни
6.  Состав модели
7.  Свойства элементов
8.  Настройки
9.  Избранные свойства
  
##### Signal Viewer NEW!
 
  
**SIGNAL Viewer** работает со специальным форматом файлов .glb. Прямая конвертация моделей в данный формат из .rvt .ifc .nwc будет доступна в ближайшем будущем.
  
![sgnl_viewer_main.png](/sgnl_docs/docs_workwithfiles/sgnl_viewer_main.png =70%x)
  
1. Линейка для измерений
2. Дерево модели
3. Свойства элементов
4. Сечение
5. Настройки
6. Видовой куб

##### Tangl Viewer
  
**Tangl Viewer** еще один просмотрщик, доступный пользователям SIGNAL DOCS. Tangl поддерживает форматы IFC и RVT, а также позволяет напрямую интегрироваться с модулями Tangl (при наличии лицензии у компании) 
    
  
![tangl_viewer_main.png](/sgnl_docs/docs_workwithfiles/tangl_viewer_main.png =70%x) 
  

#### 2.2. Сборки BIM-моделей
##### 2.2. Сборки BIM-моделей {#assemblies}
  
> См. также видеоинструкцию по работе с BIM моделями: [Telegram](https://t.me/signal_docs/316)
{.is-info}
  
В SIGNAL DOCS есть возможность собрать сводную модель проекта. Со сводной моделью также доступны инструменты замечаний и все стандартные инструменты просмотра BIM моделей.

Для создания сборки нажмите “+” и выберите “Сборка”

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcxWLQfbRDIlcxqqAtTF8C4yL9knpfDfP8u5hvBVP7k3O_iVOTeM1KXwe9GaETv4QgUqq6Ii8NacDCCXu-De2nOxIOEZd5O0b6kcudRTgqrPeQwAw9k4MG9GfTNCksXwuE?key=Sq65MbBALlfgU7uhYqZ_IW0t =70%x)

В окне создания сборки введите “Название”, выберите исходную папку, в которой хранятся модели и выберите модели, которые необходимо включить в сборку.

По умолчанию модели совмещаются по внутреннему началу, однако есть возможность дополнительно настроить координаты для каждой модели. Нажмите “Создать”

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXemr0Ypqu73EotRJrlMzvGD8ah5XfP1HfBfGAH3t4TIWPJENUCgEZvOsYjmFIOauk7cNBguY8IvbN_NQNIZgkAfNvfHF-pTd9s4NeuJrv2bE2zgWpOypvh7D9S9wp42_A?key=Sq65MbBALlfgU7uhYqZ_IW0t =50%x)

В просмотрщике будут доступны все функции выбранного вьювера.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfE3dXlLbbxT3sUjWUrNVY5uInQYtS0sBFU_tbdJvJs419RP1VYN3JnKfbpflluF8s6v0aRFxSGQ1yR0PmAM7T0zodaN6x16jYpnfr3XOpkxG3ko16czKyik3Ulz7ePtp4?key=Sq65MbBALlfgU7uhYqZ_IW0t =70%x)
  
  

  
  
  
  
#### 2.3. Сравнение BIM-моделей
##### 2.3. Сравнение BIM-моделей {#modelCompare}
  
> См. также видеоинструкцию по работе с BIM моделями: [Telegram](https://t.me/signal_docs/316)
{.is-info}
  
Для перехода в режим сравнения нажмите 

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcwNlc7fxVs3g4s_Lk4l9FQQpIRciBeJsutaMb_SXENQvAsPhPbf849c2Yz6sXV_ymaSSLEgjAZUVMUOK1-61jw_g942f4WvP0LJzRIZ5W3GzfZ2AI5LurZwkI3jXpJmM-c7H9DYfZZ7z7fvxMZFg?key=KHpy2DnF1z7IiMGX0Lup-A )

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdlXCnUIyfRWXSJlFsrRrTqKptSEmhK7s2ubKp0VXJ6uCu1UqHejpGAdvprDrmu3J0PcjzjqtIZCHadzIMK480wTtnbIcf7LUUudtKo92jP-GKsWQHPnGP00xJHrK7IKHdXUy4x6v0LRKmYJkFOFw?key=KHpy2DnF1z7IiMGX0Lup-A =70%x)

Далее необходимо выбрать версию для сравнения, либо любой другой файл

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdY_QXYrK7wByfoIcdpDz52QdYC87TRhRnpjGvFgxpkTaz4cSMeTnoc7fkN61gfVQRteDbS7TSoQsxHVgawnL2UtpwtuIv-Cj-1Q_Tqc9BszvOwBULYA7xqa3euRH-FMXk-rMQmNCuAnUINIc3cvA?key=KHpy2DnF1z7IiMGX0Lup-A =50%x)

Результаты сравнения:

**Добавлено** \- элементы,появившиеся в более поздней версии файла

**Удалено** \- элементы,удаленные из более поздней версии файла

**Изменено** \- элементы, у которых изменили геометрию и/или заполнение параметров

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfXnZD0o7Mnmft7CIo531M0Yi0Ka_eJQ5TgrIukOgRuX1pCiyZOvaLlrJAMg9OwqE8Fa154VtZRE8U6FliB2A-IrzMVGmHInjaQU3GLEgjzbn3Bo4yA2D6zKXFdnFvkwvB4iQAQpKVy5BQnuaQyyQ?key=KHpy2DnF1z7IiMGX0Lup-A =70%x)

**Затронутые дисциплины** - фильтры для переключения результатов по дисциплинам:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeWB5xxmUc7NSwPHCuiqNtr052s5P6Oh7nI0btuYFHuID6cj1PVqSMJ1InSoqn4QuIMFN6VAaPbbRfjwKZ77W3aNLZ8v7-PvGoJYx9I-RKwzzw99bGfUsadkNSBVOpCf09Xo3yDLh6S_COykSOAyQ?key=KHpy2DnF1z7IiMGX0Lup-A =50%x)

**Тип изменения** \- фильтры для переключения результатов между различными типами изменений:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdy-lD-Oo57ks00w49q3K5-eXjSirwNaxpahuDOr8TvlC9gUWBPtAdKqF46cAN6nrMdFwnrLGMtl7P6hiuORA-AX3z0housywj61gaPxVHu47-u5hZk9QZagaXXe9P_90zfMOmWQvReDENIhywwMQ?key=KHpy2DnF1z7IiMGX0Lup-A =30%x)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXev51gwxTGU4UMZEZ9cAlu3knqLoCUnv70pQSv5Cc86vRCT19ErJMHD1EdLiL9C5za6JaxU-knfSXErkA5i2bsNAVu_rAQ_BEyNxTClPbZKTMKenaeaHoSGFpUAnph5UP_0IG_K_eNaASUBgftR?key=KHpy2DnF1z7IiMGX0Lup-A =50%x)
  
  
  
  
  
  
#### 2.5. Просмотр облаков точек
##### 2.5. Просмотр облаков точек {#potree_viewer}
SIGNAL DOCS имеет возможность работы с облаками точек. Файл облака точек загружается и запускает в формате .las через конвертер и вьювер Potree.  На данный момент максимальный объем файла - 5 гб.
  ![облако_в_доксе.jpg](/облако_в_доксе.jpg)
    В просмотрщике доступна панель инструментов:
1. Точка координат
2. Измерение расстояния в плоскости между точками
3. Измерение высоты между точками
4. Измерение площади
5. Очистка
  
  ![облака_точек.jpg](/облака_точек.jpg)

  
  
  
  
  
  
#### 2.6 Просмотр DWG
##### 2.6 Просмотр DWG {#dwg_viewer}
  
Просмотрщик Autodesk Forge также работает с AutoCAD, чертежи можно загружать в формате .dwg .dwf и других. Также поддерживается возможность открытия чертежа из pdf формата во все том же просмотрщике Forge, через кнопку "А" в верхней панели интерфейса [PDF-просмотрщика](https://wiki.sgnl.pro/ru/docs/viewers#pdf)
  
  ![снимок_экрана_2026-05-15_150136.png](/снимок_экрана_2026-05-15_150136.png)
  
  Интерфейс AutoCAD похож на просмотрщик BIM-моделей, но с некоторыми отличиями. Если открывать DWG чертеж, то интерфейс полностью повторяет Forge при открытии BIM.
  1. **First Person** - включает вид от первого лица (не работает в чертежах)
  2. **Добавить плоскость** - позволяет обрезать часть модели (в чертежах будет работать только Y плоскость)
  3. **Измерение** - позволяет измерить расстояние, угол, площадь и дугу на чертежах. Также при необходимости можно откалибровать показатели и параметры измерения.
  4. **Select Text** - позволяет выделить текстовые форматы на чертеже.
  5. **Уровни** - обрезает указанные уровни. (на чертежах не работает)
  6. **Обозреватель документов** - открывает окно с листами загруженными в чертеж.
  7. **Параметры** - дополнительные пользовательские параметры отображения.
  8. **Диспетчер слоев** - позволяет скрыть/показать определенные слои и типы.
  9. **Свойства** - показывает свойства выделенного элемента.
  10. **Избранные свойства** - показывает определенные заданные свойства выделенного элемента.
  
  ![chrome_pxnj9tuo3c.png](/chrome_pxnj9tuo3c.png)
  
  При открытии PDF в формате AutoCAD интерфейс инструментов заметно уменьшен.
  1. **Измерение** - позволяет измерить расстояние, угол, площадь и дугу на чертежах. Также при необходимости можно откалибровать показатели и параметры измерения.
  2. **Обозреватель документов** - открывает окно с листами загруженными в чертеж.
  3. **Select Text** - позволяет выделить текстовые форматы на чертеже.
  4. **Параметры** - дополнительные пользовательские параметры отображения.
  5. **Показать превью файлов** - показывает изображения соседних файлов находящихся в папке и позволяет перемещать к ним (**ВАЖНО**: просмотрщик меняется на стандартный PDF)
  
#### 2.6 Сравнение DWG
##### 2.6 Сравнение DWG {#dwg_compare}
  Форматы DWG сравниваются точно также как и PDF-чертежи через кнопку Сравнения в верхнем правом углу.
  
 ![chrome_kbuzgnik7t.png](/chrome_kbuzgnik7t.png)
  
  При нажатии на кнопку Сравнения, можете выбрать предыдущую версию ранее загруженную в СОД или выбрать абсолютно другой файл из хранилища.
  
  ![chrome_iq2s1rgrgu.png](/chrome_iq2s1rgrgu.png)
  
  Сравнение происходит путем либо наложения, либо разделением экрана. Интерфейс также меняет функциональные кнопки:
  1. **Верхняя часть сравнения** - показывает сравниваемые листы чертежей, а также позволяет выбирать их и сравнивать разные листы с двух сравниваемых чертежей.
  2. **Сравниваемые документы** - показывает детальную информацию сравниваемых чертежей, позволяет убрать/показать цвета сравнения и выровнять чертежи.
  3. **Наложение/Рядом** - позволяет менять виды сравнение на **Наложение** (накладывает два листа друг на друга с разными цветами: красный - старая версия, синий - новая версия) и **Рядом** (разбивает экран на две части, с ползунком который расширяет то или иное окно версий).
  4. **Закрыть панель** - убирает панель **Сравниваемых документов**
  ![chrome_4xskvcsquj.png](/chrome_4xskvcsquj.png)
  
  
  
  
  
  
  
  
## PDF
### Вкладки{.tabset}

#### 3.1. Просмотр PDF
##### 3.1. Просмотр PDF {#pdf}
> См. также видеоинструкцию по работе с PDF: [Telegram](https://t.me/signal_docs/284) [YouTube](https://youtu.be/APrrvpOYETM)	[Rutube](https://rutube.ru/video/6c121c69bdea591e00e8cee06e5cbdc1/) [VK](https://vkvideo.ru/video-223002264_456239070)
{.is-info}

> Наведитесь на инструмент, чтобы увидеть подсказку
{.is-info}
  
<div style="position: relative; display: inline-block;">
  
  <!-- Изображение -->
  <img src="/sgnl_docs/docs_workwithfiles/pdf_viewer_main.png" style="display: block; width: 1024px; height: auto;">

  <!-- Группа 1: Верхняя панель (левая часть) -->
  <div class="hotspot-zone" style="position: absolute; left: 1px; top: 40px; width: 50px; height: 50px;">
    <span class="tooltip-orange">Постраничная навигация</span>
  </div>
  
  <div class="hotspot-zone" style="position: absolute; left: 50px; top: 40px; width: 50px; height: 50px;">
    <span class="tooltip-orange">Масштабирование по размеру экрана</span>
  </div>
  
  <div class="hotspot-zone" style="position: absolute; left: 100px; top: 40px; width: 50px; height: 50px;">
    <span class="tooltip-orange">Список замечаний по документу</span>
  </div>
  
  <div class="hotspot-zone" style="position: absolute; left: 150px; top: 40px; width: 50px; height: 50px;">
    <span class="tooltip-orange">Подписать документ ЭЦП</span>
  </div>
  
  <div class="hotspot-zone" style="position: absolute; left: 200px; top: 40px; width: 50px; height: 50px;">
    <span class="tooltip-orange">Скрыть пометки аудитора</span>
  </div>
  
  <div class="hotspot-zone" style="position: absolute; left: 250px; top: 40px; width: 50px; height: 50px;">
    <span class="tooltip-orange">Переместить пометки между листами</span>
  </div>

  <!-- Группа 2: Верхняя панель (центральные инструменты) -->
  <div class="hotspot-zone" style="position: absolute; left: 340px; top: 40px; width: 100px; height: 50px;">
    <span class="tooltip-orange">Навигация по листам</span>
  </div>
  
  <div class="hotspot-zone" style="position: absolute; left: 460px; top: 40px; width: 140px; height: 50px;">
    <span class="tooltip-orange">Масштаб листа</span>
  </div>
  
  <div class="hotspot-zone" style="position: absolute; left: 600px; top: 40px; width: 120px; height: 50px;">
    <span class="tooltip-orange">Поворот листа</span>
  </div>

  <!-- Группа 3: Верхняя панель (правая часть) -->
  <div class="hotspot-zone" style="position: absolute; left: 770px; top: 40px; width: 50px; height: 50px;">
    <span class="tooltip-orange">Серверная генерация листа</span>
  </div>
  
  <div class="hotspot-zone" style="position: absolute; left: 820px; top: 40px; width: 50px; height: 50px;">
    <span class="tooltip-orange">Открыть в Autodesk Forge</span>
  </div>
  
  <div class="hotspot-zone" style="position: absolute; left: 870px; top: 40px; width: 50px; height: 50px;">
    <span class="tooltip-orange">Скачать файл</span>
  </div>
  
  <div class="hotspot-zone" style="position: absolute; left: 920px; top: 40px; width: 50px; height: 50px;">
    <span class="tooltip-orange">Сравнение версий</span>
  </div>
  
  <div class="hotspot-zone" style="position: absolute; left: 970px; top: 40px; width: 50px; height: 50px;">
    <span class="tooltip-orange">Печать документа</span>
  </div>

  <!-- Группа 4: Правая плавающая панель -->
  <div class="hotspot-zone" style="position: absolute; left: 950px; top: 160px; width: 60px; height: 60px;">
    <span class="tooltip-orange">Создать замечание</span>
  </div>
  
  <div class="hotspot-zone" style="position: absolute; left: 950px; top: 230px; width: 60px; height: 120px;">
    <span class="tooltip-orange">Приблизить/отдалить</span>
  </div>
  
  <div class="hotspot-zone" style="position: absolute; left: 950px; top: 360px; width: 60px; height: 120px;">
    <span class="tooltip-orange">Перелистывание документа</span>
  </div>
  
  <div class="hotspot-zone" style="position: absolute; left: 950px; top: 490px; width: 60px; height: 120px;">
    <span class="tooltip-orange">Переключение между документами</span>
  </div>

</div>

  
  
#### 3.2. Сравнение PDF
##### 3.2. Сравнение PDF {#drawingCompare}

> См. также видеоинструкцию по работе с PDF: [Telegram](https://t.me/signal_docs/284) [YouTube](https://youtu.be/APrrvpOYETM)	[Rutube](https://rutube.ru/video/6c121c69bdea591e00e8cee06e5cbdc1/) [VK](https://vkvideo.ru/video-223002264_456239070)
{.is-info}
  
Для перехода в режим сравнения нажмите

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeyLYyjLgDSRyeb5q-aOvc5Qfha8qy7ca5xhnurAPA7lA6xhWUmqmCOiiRKrYTL2d8THumxDax0qD_CTkvH6DsGUY4F1j9VKzjWDT-P1V3KpYT7CCYY9yM7-i3ZGCrZlDN3R4HyL422kT9rcXe2-w?key=G5mC2kC-3FTUbBlnmOZq9Q )

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdYY33hW928BaunEFdom3lmxGFFqKzJd9K8UaRUl7uHDhdVpSwj9_8gslC7G7YpWWcwm1-FeT3l3vc2Wu_Fd5u4mLKwnE89ReL9UIeoNtiBmrNrEI8u9fWIm8QmFnDYoF5PnnqtbbE9fu66Ctto?key=G5mC2kC-3FTUbBlnmOZq9Q =70%x)

Далее необходимо выбрать версию для сравнения.

При необходимости, есть возможность для сравнения  выбрать другой файл, загруженный в систему SIGNAL DOCS.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdUxYhLZtHFuuIbmGTwyL1yLLXJYtW5rTBUe8QYpXpiyRbLr_2BKtHvmyC_89z1Ux1aa2ervmWybHn6Uibrrq-50zada_osj0jiBozlGrH6x073iV8RHUZ9plY2gdReNS7G1dkGHNZV7jl-Q5A5?key=G5mC2kC-3FTUbBlnmOZq9Q =30%x)

Откроется окно сравнения документов.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcBi_qrMV4hXirifIssfm9Ms74XIzGOdi6OcnCaFafh4EkDqSRkz3cMNq_s5Sa7SBLZABhkVWjGK6n2Rw5MyJxoFTJRnsUnxOLEXMfbo3QDMfKtdnDLcXlNO5ZVjV4iMXKktfuIbefWD3-aWccOUA?key=G5mC2kC-3FTUbBlnmOZq9Q =70%x)

1.  Выбор листа для сравнения
2.  Вкл/откл видимость версии
3.  Результат сравнения
4.  Поворот против часовой стрелки
5.  Поворот по часовой стрелке
6.  Масштаб
7.  Настройки
8.  Смещение версий друг относительно друга
9.  Масштабирование версий файла
10.  Масштабирование окна просмотра
11.  Переключение между страницами

**Настройки**

1.  **Детализация изображения**

Отвечает за четкость изображения.

Чем выше детализация,тем четче текст в файле.

1.  **Порог соответствия**

Отвечает за четкость сравнения при наложении двух версий файлов.

Чем меньше значение, тем более точное совпадение при наложении должно быть,чтобы при отображении результата совпадающие части отображались серым цветом.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeh4bGT8_AW43uzxcv3CllCRJinQQSHUJdZ674_SuT-DrmTSRYZjHbXiuoRli7F6-T8a18ykTk-pVK3q_1PrWBq0zk20DHWd34q2qWekPl9INUyn4INT3QP-9pos8hMatDQRncLMQYCZS3oajsDcw?key=G5mC2kC-3FTUbBlnmOZq9Q)

**Смещение версий файлов**

![image-1718885032968.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf8TQDnF_Y5MQHjLOXzTGzdc-6-unwPCgX7gnkSCgYpMaTl9nH-kloKGPY-qHprzCYG4V1RzE3RV4D3-qt5BrxOxT-CILBm7vawqUT-xvsxQ7phV6KUzReLqzJjkPPB2Y9UQbq8VZXdxxD9WTjlUg?key=G5mC2kC-3FTUbBlnmOZq9Q =70%x)

**Поворот сравниваемых файлов**

![image-1718885114301.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfd1jJ0ysZRYDGLkcBi_p2z5OnDz7CXUJZQIpOuZU_qsAqiLVwQCiry4T4VB7WLje8e-CAlCNzQqPo9atiZh8fo3Xbw_b70__-4YpO8eyXXkurd8K_TBKqhVz8gUsc1Owb2vQY5byXBpWBdFJLr?key=G5mC2kC-3FTUbBlnmOZq9Q =70%x)

**Масштабирование версий файла**

![image-1719396933792.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc3eBd9XxWlu7UuJZ94beyhYRf2DnvfvcemqCACflV0dBXY_5G9NqDHGMmYeVHcKu1GCEKXpOIrCeLXmrQf6qKRQln9aZ-o07oWUVN0J-VxUjVZfCXqIHTWSBeV-tpwv_GNm2Uv7NGWLH7_gAo?key=G5mC2kC-3FTUbBlnmOZq9Q =70%x)



  
  
## Прочее
### Вкладки{.tabset}
  
  
#### 4.1. Создание документов XML
##### 4.1. Создание документов XML {#xml}
  
> См. также видео **[XML-документы по XSD-схемам в SIGNAL DOCS](https://vkvideo.ru/video-230401166_456239025)**
{.is-info}

1. В [настройках проекта](/docs/settings#xml) администратор создаёт тип схемы, настроить доступы и загрузить нужные файлы XSD (шаблоны XML), например с [сайта Минстроя](https://www.minstroyrf.gov.ru/tim/xml-skhemy).
2. Пользователь с правами на создание схемы этого типа использует его при создании XML в любой доступной папке.
3. После корректного заполнения всех полей можно скачать готовый XML. Если не все поля заполнены, то в любом случае сохраняется черновик, к которому можно вернуться позже.

![xml_документы.png](/xml_документы.png =70%x)

  
  
  
  
#### 4.2. Создание интерактивных справок
##### 4.1. Создание интерактивных справок {#markdown}
  В SIGNAL можно создавать и загружать текстовые документы, которые также можно редактировать прямо в СОДе. Особенно выделяется формат .md который автоматически принимает форму справочного документа в той папке в которую он загружен и поддерживает форматы markdown
  ![снимок_экрана_2026-05-15_144740.png](/снимок_экрана_2026-05-15_144740.png)
  
  
<sub>**[<   DOCS. Документы](/ru/docs/folders)     **|**     [DOCS. Замечания   >](/ru/docs/issues)** </sub>