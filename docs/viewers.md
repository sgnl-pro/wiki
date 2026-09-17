---
title: DOCS. Работа в файлах
description: 
published: true
date: 2026-09-17T17:36:18.107Z
tags: 
editor: markdown
dateCreated: 2025-10-16T13:16:45.534Z
---

<sub>**[<   DOCS. Документы](/ru/docs/folders)     **|**     [DOCS. Замечания   >](/ru/docs/issues)** </sub>
  
<summary style="font-size: 16px; color: #0D47A1; background: #E3F2FD; border-radius: 7px; border: 1px solid #64B5F6; display: flex; gap: 10px; padding: 5px 16px; display: block; margin-top: 10px;">
<span style="flex-grow: 1;"><a href="/docs/viewers/updates" onclick="event.stopPropagation();" style="color: inherit; text-decoration: none;">🔄 Что нового (история изменений этого функционала)</a></span>
</summary>

----
  
<div class="toc-grid">
  <!-- 1. Офисные документы -->
  <div class="toc-card toc-green">
    <h4 class="toc-card-title"><a href="#1-офисные-документы">1. Офисные документы</a></h4>
    <ul class="toc-list">
      <li><a href="#office"><span class="toc-badge">1.1</span> Работа с DOCX, XLSX, PPTX</a></li>
      <li><a href="#mpp"><span class="toc-badge">1.2</span> Создание графиков MPP</a></li>
    </ul>
  </div>

  <!-- 2. CAD -->
  <div class="toc-card toc-green">
    <h4 class="toc-card-title"><a href="#2-cad">2. CAD</a></h4>
    <ul class="toc-list">
      <li><a href="#bim"><span class="toc-badge">2.1</span> Просмотр BIM-моделей</a></li>
      <li><a href="#assemblies"><span class="toc-badge">2.2</span> Сборки BIM-моделей</a></li>
      <li><a href="#modelCompare"><span class="toc-badge">2.3</span> Сравнение BIM-моделей</a></li>
      <li><a href="#potree_viewer"><span class="toc-badge">2.4</span> Просмотр облаков точек</a></li>
      <li><a href="#dwg_viewer"><span class="toc-badge">2.5</span> Просмотр DWG</a></li>
      <li><a href="#dwg_compare"><span class="toc-badge">2.6</span> Сравнение DWG</a></li>
    </ul>
  </div>

  <!-- 3. PDF -->
  <div class="toc-card toc-green">
    <h4 class="toc-card-title"><a href="#3-pdf">3. PDF</a></h4>
    <ul class="toc-list">
      <li><a href="#pdf"><span class="toc-badge">3.1</span> Просмотр PDF</a></li>
      <li><a href="#drawingCompare"><span class="toc-badge">3.2</span> Сравнение PDF</a></li>
    </ul>
  </div>

  <!-- 4. Прочее -->
  <div class="toc-card toc-green">
    <h4 class="toc-card-title"><a href="#4-прочее">4. Прочее</a></h4>
    <ul class="toc-list">
      <li><a href="#xml"><span class="toc-badge">4.1</span> Создание документов XML</a></li>
      <li><a href="#markdown"><span class="toc-badge">4.2</span> Создание интерактивных справок</a></li>
    </ul>
  </div>
</div>
  
----
  
# Вкладки {.tabset}

  
## 1. Офисные документы

  
SIGNAL поддерживает форматы файлов Microsoft Office в двух просмотрщиках - Collabora и MS Office. Первый просмотрщик также поддерживает и редактуру документа прямо в браузере.
  
### Вкладки {.tabset}
  
  
#### 1.1. Работа с DOCX, XLSX, PPTX
##### 1.1. Работа с DOCX, XLSX, PPTX {#office}
  
> См. также [пользовательскую справку](https://help.collaboraoffice.com/latest/en-US/text/shared/05/new_help.html) от разработчика офисного редактора.
{.is-info}

  
  При открытии офисного формата файла (doc. xls. и др.) появляется интерфейс ранее назначенного просмотрщика, по стандарту первым открывается Collabora. 
  ![снимок_экрана_2026-05-15_141653.png](/снимок_экрана_2026-05-15_141653.png)
  	В верхней части интерфейса можно активировать редактор офисных форматов. Он работает как программа Word и Excel и повторяет их стандартный, знакомый интерфейс. При редактировании файлов, для других пользователей над файлом появлеятся иконка замка, что не дает другим пользователям перемещать, переименовывать или как-то взаимодействовать с файлом пока идет редактирование документа. Значок замка пропадает либо после выхода из сессии редактирования пользователем, либо автоматически через несколько минут.
  ![снимок_экрана_2026-05-15_142101.png](/снимок_экрана_2026-05-15_142101.png)
  Редактирование файла возможно несколькими пользователями одновременно, как при работе в форматах Google Docs, то есть пользователи видят курсоры других пользователей и их внесенные изменения в настоящем времени.

В Collabora можно сравнить текущую версию офисного документа с файлом на устройстве. Откройте меню сравнения, выберите файл и подтвердите загрузку: редактор покажет различия между документами.

![Сравнение офисных документов](/release_notes/2026.16_-_сравнение_файлов.png =1200x)
  
  
  
  
  
  
  
  
  
#### 1.2. Создание графиков MPP
##### 1.2. Создание графиков MPP {#mpp}

В SIGNAL DOCS можно создать и редактировать график Ганта в собственном формате `.sgmpp`. Через кнопку **«+»** создайте график, откройте его и перейдите в режим редактирования.

В таблице графика можно создавать задачи и группы, задавать названия и сроки, менять иерархию и связывать задачи зависимостями. Связь можно создать на временной шкале, перетащив указатель от одной задачи к другой. Даты и длительность задач согласованы с календарём графика.

Редактор поддерживает работу с клавиатуры: перемещение по таблице, выбор и редактирование ячеек, а также копирование, вырезание и вставку задач. Панель инструментов позволяет отменять и повторять изменения. После завершения редактирования сохраните график.

![Редактор графика Ганта](/release_notes/2026-17-график_ганта.png =1200x)
  
  
  
  
## 2. CAD
### Вкладки {.tabset}

  
  
  
#### 2.1. Просмотр BIM-моделей
##### 2.1. Просмотр BIM-моделей {#bim}
  
> См. также видеоинструкцию по работе с BIM моделями: [Telegram](https://t.me/signal_docs/316)
{.is-info}
  
> Среда общих данных SIGNAL DOCS поддерживает работу цифровыми информационными моделями прямо в браузере вашего устройства. Просматривайте свойства изменений, комментируйте модели а также сравнивайте их версии
{.is-info}  

На текущий момент в SIGNAL DOCS Представлено 3 просмотрщика моделей - Autodesk Forge, Tangl Viewer, SIGNAL Viewer
  
|              | Autodesk Forge                | Tangl Viewer | SIGNAL Viewer |
|-----------------------|-------------------------------|--------------|---------------|
| **Форматы файлов**        | .rvt .nwd .nwc .fbx .skp .ifc | .rvt .ifc    | .glb .ifc .rvt .nwd .nwc          |
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
  
##### SIGNAL Viewer
 
**SIGNAL Viewer** поддерживает модели в форматах GLB, IFC, RVT, NWD и NWC.

В просмотрщике можно выбрать элементы модели и создать замечание с привязкой к ним. При последующем открытии замечания связанные элементы изолируются, а камера фокусируется на них. SIGNAL Viewer также открывает модели по публичным ссылкам и показывает облака точек Gaussian Splat PLY без предварительной серверной конвертации.

На узких экранах инструменты распределяются по нескольким строкам. Панели структуры модели, свойств и настроек можно изменять по ширине и высоте мышью или касанием; при изменении размера окна и повороте устройства они остаются в видимой области.
  
![sgnl_viewer_main.png](/sgnl_docs/docs_workwithfiles/sgnl_viewer_main.png =70%x)
  
1. Линейка для измерений
2. Дерево модели
3. Свойства элементов
4. Сечение
5. Настройки
6. Видовой куб

Чтобы создать сечение параллельно выбранной поверхности, откройте инструмент сечения и включите режим **«Сечение по грани»**. Указатель примет форму перекрестия. Нажмите на поверхность модели: плоскость сечения пройдёт через точку нажатия параллельно этой поверхности и скроет половину модели, обращённую к камере.

##### Tangl Viewer
  
**Tangl Viewer** еще один просмотрщик, доступный пользователям SIGNAL DOCS. Tangl поддерживает форматы IFC и RVT, а также позволяет напрямую интегрироваться с модулями Tangl (при наличии лицензии у компании) 

При отправке файла в обработку SIGNAL DOCS передаёт в Tangl текущее имя модели. Если после обработки переименовать файл в DOCS, имя модели в Tangl автоматически не изменится. Повторная отправка уже обработанной версии сейчас не поддерживается: чтобы передать новое имя, загрузите новую версию файла и отправьте её в обработку Tangl.
    
  
![tangl_viewer_main.png](/sgnl_docs/docs_workwithfiles/tangl_viewer_main.png =70%x) 
  

#### 2.2. Сборки BIM-моделей
##### 2.2. Сборки BIM-моделей {#assemblies}
  
> См. также видеоинструкцию по работе с BIM моделями: [Telegram](https://t.me/signal_docs/316)
{.is-info}
  
В SIGNAL DOCS есть возможность собрать сводную модель проекта. Со сводной моделью также доступны инструменты замечаний и все стандартные инструменты просмотра BIM-моделей.

Для создания сборки нажмите “+” и выберите “Сборка”

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcxWLQfbRDIlcxqqAtTF8C4yL9knpfDfP8u5hvBVP7k3O_iVOTeM1KXwe9GaETv4QgUqq6Ii8NacDCCXu-De2nOxIOEZd5O0b6kcudRTgqrPeQwAw9k4MG9GfTNCksXwuE?key=Sq65MbBALlfgU7uhYqZ_IW0t =70%x)

В окне создания сборки введите “Название”, выберите исходную папку, в которой хранятся модели и выберите модели, которые необходимо включить в сборку.

По умолчанию модели совмещаются по внутреннему началу, однако есть возможность дополнительно настроить координаты для каждой модели. Нажмите “Создать”

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXemr0Ypqu73EotRJrlMzvGD8ah5XfP1HfBfGAH3t4TIWPJENUCgEZvOsYjmFIOauk7cNBguY8IvbN_NQNIZgkAfNvfHF-pTd9s4NeuJrv2bE2zgWpOypvh7D9S9wp42_A?key=Sq65MbBALlfgU7uhYqZ_IW0t =50%x)

В просмотрщике будут доступны все функции выбранного вьювера.

Если у включённых в сборку моделей появились новые версии, используйте действие **«Обновить версии»**. Перед обновлением система показывает, какие модели используют неактуальные версии.

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
  
  
  
  
  
  
#### 2.4. Просмотр облаков точек
##### 2.4. Просмотр облаков точек {#potree_viewer}
SIGNAL DOCS имеет возможность работы с облаками точек. Файл облака точек загружается и запускает в формате .las через конвертер и вьювер Potree.  На данный момент максимальный объем файла - 5 гб.
  ![облако_в_доксе.jpg](/облако_в_доксе.jpg)
    В просмотрщике доступна панель инструментов:
1. Точка координат
2. Измерение расстояния в плоскости между точками
3. Измерение высоты между точками
4. Измерение площади
5. Очистка
  
  ![облака_точек.jpg](/облака_точек.jpg)

  
  
  
  
  
  
#### 2.5 Просмотр DWG
##### 2.5 Просмотр DWG {#dwg_viewer}
  
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
  
  
  
  
  
  
  
  
## 3. PDF
### Вкладки {.tabset}

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



  
  
## 4. Прочее
### Вкладки {.tabset}
  
  
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
