---
title: TOOLS. Копирование элементов
description: 
published: true
date: 2026-02-02T11:16:56.485Z
tags: 
editor: markdown
dateCreated: 2025-09-21T13:13:39.334Z
---

<sub>**[<   TOOLS FOR REVIT. Проверка  ](/ru/tools/revit/checker)     **|**     [TOOLS FOR REVIT. Утилиты    >](/ru/tools/revit/attachments)**</sub>

---

# Вкладки{.tabset}
## Зафиксировать элементы

> Инструмент Зафиксировать элементы предназначен для копирования элементов из связанного файла. При копировании, на месте элемента создается НЕ редактируемая геометрия с параметрами. Перед фиксированием элементов рекомендуется указать [_дополнительные параметры_](https://wiki.sgnl.pro/ru/tools/tools-for-revit/copying-params), которые следует скопировать вместе с геометрией. Копирование осуществляется на виде “1. Копирование элементов”. Рекомендуется использовать [_шаблон Строительной модели_](https://docs.sgnl.pro/s/f/4d8f615a-27fd-4b1a-a631-c7529eb99f03) 
{.is-info}

1\. Нажмите на панели Копирование элементов ➤ Зафиксировать элементы

![image-1683718447331.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeQu9tSxAgwFOjRkO3EjSD3WeXuBpAHeH5yaSiEM9pqFtJzVXpDtbnWnsHoFGDfSKwrqrKAKWbbQREbT8gN9hL5Y_PRnosHIXu6FjX5fH7E-Dk_MmT7VHJTzwYnOOSOcIfQoEDLmD4ZpiPLy6y7?key=EO6iZbWODBk6VEvepWY-rw)

Окно настройки инструмента

![revit_7fasufnkfs.png](/sgnl_tools_revit/revit_7fasufnkfs.png)

-   ***Переключатель “Копировать материалы”*** отвечает за визуальное отображение материалов на скопированной геометрии. Рекомендуется держать его выключенным, поскольку копирование с материалами, увеличивает общее время работы команды.
-   ***Переключатель “Включить проверку по ID”*** предотвращает дублирование ранее скопированных элементов. Если необходимо заменить ранее скопированные элементы, удалите устаревшую версию элемента перед копированием. При этом замена элемента влечет за собой замену его id в строительной модели, следовательно, из-за смены id Navisworks не сможет подтянуть данные SIGNAL в новый элемент.
-   ***Переключатель “Создать пирог конструкции”*** разделяет многослойную стену по слоям и копирует каждый слой категорией Части
-   ***Переключатель “Зафиксировать семейтсво/сборку элемента”*** При фиксации элемента в составе сборки фиксируется сразу вся сборка или семейства
-   ***Переключатель “Разделить на примитивы”*** разделяет многокомпонентный элемент на простые элементы геометрии (такие как элементы выдавливания, сдвига или вложенные семейства)
  
2\. Выберите элементы из связанной модели, которые необходимо скопировать, и в левом верхнем углу нажмите Готово

![image-1683718475365.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcscHe3Dh_DoK3gk6VReiEbTcf8pEL-GuY692CglG9J9zKdXHK9rbqnuhp0xT0o7T8PxoKM45RwHU1-pP8aEbJt6YpTy80gVb1HugjqUCOf3IbKj2dpqduGx_3aLyFVDTFSMR48eXRk4a8sEN6U?key=EO6iZbWODBk6VEvepWY-rw)

3\. Выбранные элементы будут скопированы из связанного файла и появятся на виде “2. Создание Строительной модели”. Элементы будут представлять собой НЕ редактируемую геометрию с параметрами.

![image-1684157839451.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfGpfvLdmDTqRbyjpxSIWmr3TQfcUe1vPbdb1ckkkKULdKOxrZepJFSNQ5cSzMILxmM-nqr57vdvlUFe2T_XFLgoxkMGuCgSH9IncJFrdjzJaL7f4mgbMDGbI5hUihusOQnXpfur5QbqglIgfR5yw?key=EO6iZbWODBk6VEvepWY-rw)

## Зафиксировать по параметру

> Инструмент Зафиксировать по параметру предназначен для копирования элементов из связанного файла по определенным параметрам. При копировании, на месте элемента создается НЕ редактируемая геометрия с параметрами. Перед фиксированием элементов рекомендуется указать [_дополнительные параметры_](https://wiki.sgnl.pro/ru/tools/tools-for-revit/copying-params), которые следует скопировать вместе с геометрией. Копирование осуществляется на виде “1. Копирование элементов”. Рекомендуется использовать [_шаблон Строительной модели_](https://youneedawiki.com/app/page/16fpBthMAybTK7EM6Wu0mii9n9UsAk970?p=1q45phxXDh7rGLAjXkfEXgBABHArTZ7gs)
{.is-info}

1\. Нажмите на панели Копирование элементов ➤ Зафиксировать по параметру

![image-1683718488282.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXccdTbaUjleut2x8-3XSfXeSTe74S9nPLXos1MYwNSSK7zTX4MfCQvdTWdwo467Ca_EVat1FlkUKKmLYAIuRwdCn6bO2747FxT-uwdmC8xlvJya7ofenlnTVO8IgCYMILcSWxEuTEzgtj8S7X2VUQ?key=2NTBJ-shrKVVjiepMz0O6g)

2\. Откроется окно настроек инструмента. Добавьте параметры, нажав **“+”**.  В строке с параметрами выберите из выпадающего списка название параметра и значение параметра, по которому будут копироваться элементы из связанной модели.

![revit_jb8hxtromj.png](/sgnl_tools_revit/revit_jb8hxtromj.png)

-   ***Переключатель “Копировать материалы”*** отвечает за визуальное отображение материалов на скопированной геометрии. Рекомендуется держать его выключенным, поскольку копирование с материалами, увеличивает общее время работы команды.
-   ***Переключатель “Включить проверку по ID”*** предотвращает дублирование ранее скопированных элементов. Если необходимо заменить ранее скопированные элементы, удалите устаревшую версию элемента перед копированием. При этом замена элемента влечет за собой замену его id в строительно модели, следовательно, из-за смены id Navisworks не сможет подтянуть данные в новый элемент
-   ***Переключатель “Создать пирог конструкции”*** разделяет многослойную стену по слоям и копирует каждый слой категорией Части
-   ***Переключатель “Зафиксировать семейтсво/сборку элемента”*** При фиксации элемента в составе сборки фиксируется сразу вся сборка или семейства
  
3\. Элементы с указанными параметрами будут скопированы из связанного файла и появятся на виде “2. Создание Строительной модели”. Элементы будут представлять собой НЕ редактируемую геометрию с параметрами.

![image-1684235964784.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeJQ5cPN60FslGfIYW66Psjfys1rS9ERiABxlRPM9iuG77PLksAsDZwvdhsEIeKRamzzVr1iVAygTjnULdJCNCJDPEsjM953vh7ttAg8Jmv4N7Lbd-JxkXELcVE4xZ9Hs2nVY6JiUrqWCZ7XE9a?key=2NTBJ-shrKVVjiepMz0O6g)

## Копировать параметры

Используя команду Копировать параметры можно скопировать недостающие параметры для уже зафиксированных элементов

1\. Нажмите на панели Копирование элементов ➤ Копировать параметры

![image-1683718864919.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeiyr1116-eZbWSF5SUMMVd85gS7VYDFYqd2w5P7YBsvx8xMEwEiINasTSv2Y7KFoxSzpBbtdUMvPlirPPNpt3U2h28mWLXKo6tl3yiWbOoKC_fP5MMsMTN7C7ioYxW5F3upInMGMhzLXml24o5Hg?key=HWsJPc92qPG9kQy2fqoRrg)

Окно настройки инструмента

![image-1683718873805.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXetb9e3F0nUtl3Fs69NvGFkhU78amHAgpWFOvOw0ssh3WjZgYzDNDYoCLRzs4HFWphzFSB1vS1IirKQFRLgbNKbw4TY8WV9hHWV5a_pWWe38HiWg_jY1WdykyohRBrkhhpVf9ovvXunhG8RGQ1s?key=HWsJPc92qPG9kQy2fqoRrg)

-   ***В блоке “Связи для поиска”*** укажите связанную модель, из которой требуется скопировать параметры.
-   ***В блоке “Параметры для копирования”*** укажите параметры, которые требуется скопировать из связанного файла. Параметры для копирования заполняются в Настройках SIGNAL в разделе [_Параметры для копирования_](https://youneedawiki.com/app/page/1Xga4e-2KLC403pfVX6gk2zJ4myTZhYFD8VI_mxCo5Uo)

2\. Выберите элементы, которым нужно скопировать параметры, и в верхнем левом углу нажмите Готово

![image-1683718912303.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdgIjkMA-TLFTz9VIspgHElxg7ze_voYTmXIH_cHeDEOK4QDDJ9xEKc2WfSt670U-Tq_sg4ej-czwAd1fcfB-BkxYGHQkeION2o8eRCKbvOaRjaj0kVbCUtlGe8HsqaPAX23EEjcxbeCNCjnCmPSw?key=HWsJPc92qPG9kQy2fqoRrg)

## Скопировать оси, уровни

> Инструмент позволяет скопировать в строительную модель оси и уровни из связанного файла. Необходимо для создания планов по уровням проектной модели или нарезки элементов на части по осям
{.is-info}

1\. Нажмите на панели Копирование элементов ➤ Скопировать оси, уровни

![image-1683718944877.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXck3Navbh5bwSVT8_i7ZxmCfMYA-cWr-bbaZAklVAvHhCbJwfAYc2FpAuNdu-2LUh27XlHvdeboDShrpNCRbt6N0OaFH0232YHgMg_ZWvzG0sLVFFnmUUzmFNS4p6T8Pa0HnTzd4ijyNNpZlTk84A?key=WmVvIhJEqtm22MruBQaWkg)

Окно настроек инструмента

![image-1683718957426.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe_Q2bpGn9wFxFpt5NQjfaBCMJMpQTO3nPPq0SkRFh-D8cZW65r_p2j_IXlSDEJXXpbs8dBLSiAttEhTM561KHkRYhmBxchgaeSyW-O1q0b9AMdUbvOEvmrANlf5aA-jlkJW6Eb3vYNTFkjGOzR?key=WmVvIhJEqtm22MruBQaWkg)

-   Укажите связанный файл, из которого будут копироваться оси и уровни
-   ***Переключатель “Копировать оси”*** отвечает за копирование осей
-   ***Переключатель “Копировать уровни”*** отвечает за копирование уровней

## Обновить S параметры

> Инструмент обновляет у элементов категории Части геометрические параметры (S Объем, S Площадь, S Длина) и S id history. Требуется при изменении геометрии элемента
{.is-info}

1\. Нажмите на панели Копирование элементов ➤ Обновить S параметры

![image-1683718998425.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcrcqNz4kaPNm-qma52K6kgRTIgupPF3EtbkywqziiVNVzFp1L67-sGPWo7lwfS0ERnY2OBtj2VPaTRby79dcCye2Rz0LIauQ86UWz1lQyZhjGZAl48nKD--pIceWVPEJhVtfbDoiseJxZ1qOI6HQ?key=HHs1-hoSpNAz5Rsa9ZMdgg)

2\. Выберите элементы категории Части, которым требуется обновить параметры, и нажмите Готово

![image-1683718993910.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe-w_BqxDFs6HWAzKkOXsZpZxltvf5-px-oeXQPnyra5nj9ptgcAvMW4rx0NXZXofVnA563O4cd2yyZHZFVh_CFUILzTsd5oZDWzUXUR8524EX4z_moVuV7J0E4mWlRAKzq3jCaOxYsqS73BmXr?key=HHs1-hoSpNAz5Rsa9ZMdgg)

## Создание поверхностей

> Инструмент позволяет создавать поверхности по выбранным граням. С его помощью можно вести накопительную строительную модель по фасадам или внутренней отделке, когда те выполнены однослойной стеной или не смоделированы
{.is-info}

1\. Нажмите на панели Копирование элементов ➤ Создание поверхностей

![image-1683719043463.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeDIYY_bt5UtpWP5C52eji3CQryTHxxMogGS-D8sbekxjlVy1napvUsmptyAGA5GISl9lHC_y3YgfeW45NPBBrT1ofh6NrTZSFZ-KHFXZ8qaIpZkv4K978Qh6B1l-zRHLZvGNDU5VZNQuoaJQdw1w?key=q-zPPVedAJFkbB7Ww6M5Jg)

Окно настроек инструмента

![image-1683719051143.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcW0MuTq8mjsNlCJosC761m-q002x9jlbEoSBdAzRZPn57pH-k9ygFGCoVxUqiV7FmOzF2vvwJFQCdFiXisBYL_uWHfZFNbN6sS2Q4Q4WFdQvaYrTQftaZ-mPeYUvwX8rl2wc5GGS1NGe_l096ZEA?key=q-zPPVedAJFkbB7Ww6M5Jg)

-   Можно добавлять и удалять разные варианты поверхностей со своими параметрами.
-   ***В строке “Имя”*** укажите имя вашего варианта.
-   ***В строке “Категория”*** выберите категорию создаваемой поверхности.  
    ***Примечание:*** некоторые категории не подходят для создания поверхностей, например, такие как Аналитические модели колонн или Сосредоточенные нагрузки.
-   ***В строке “Материал”*** выберите материал создаваемой поверхности.
-   ***В строке “Толщина”*** укажите толщину поверхности в мм.
-   ***В строке “Отступ”*** укажите отступ поверхности от выбранной грани в мм.
-   ***Переключатель “В обратном направлении”*** позволяет выбрать в каком направлении будет выдавливаться поверхность.
-   ***Переключатель “Объединить грани”*** позволяет строить поверхность как одно целое при выборе нескольких граней.

2\. Выберите одну или несколько граней и нажмите Готово

![image-1683719072606.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXepzXL7SkYIptlnJKhBhkX_iVoSXl4Q61H7i0eae8wlN4Wz8ybPfwwK2NPEF2B-ZAoi6_5iG2gcikXDggi7TucSBnyzWQnh-nT4HKHnFIvjpD8sBWEDXaAGqagUGMYCD3CSobzgZ5UWC_kZzmJALA?key=q-zPPVedAJFkbB7Ww6M5Jg)
  
#
<sub>**[<   TOOLS FOR REVIT. Проверка  ](/ru/tools/revit/checker)     **|**     [TOOLS FOR REVIT. Утилиты    >](/ru/tools/revit/attachments)**</sub>