---
title: Копирование элементов - Зафиксировать Элементы
description: 
published: true
date: 2025-09-21T13:11:00.981Z
tags: 
editor: markdown
dateCreated: 2025-06-27T12:01:36.289Z
---

### **Зафиксировать элементы**

Инструмент Зафиксировать элементы предназначен для копирования элементов из связанного файла. При копировании, на месте элемента создается НЕ редактируемая геометрия с параметрами. Перед фиксированием элементов рекомендуется указать [_дополнительные параметры_](https://wiki.sgnl.pro/ru/tools/tools-for-revit/copying-params), которые следует скопировать вместе с геометрией. Копирование осуществляется на виде “1. Копирование элементов”. Рекомендуется использовать [_шаблон Строительной модели_](https://docs.sgnl.pro/s/f/4d8f615a-27fd-4b1a-a631-c7529eb99f03) 

1\. Нажмите на панели Копирование элементов ➤ Зафиксировать элементы

![image-1683718447331.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeQu9tSxAgwFOjRkO3EjSD3WeXuBpAHeH5yaSiEM9pqFtJzVXpDtbnWnsHoFGDfSKwrqrKAKWbbQREbT8gN9hL5Y_PRnosHIXu6FjX5fH7E-Dk_MmT7VHJTzwYnOOSOcIfQoEDLmD4ZpiPLy6y7?key=EO6iZbWODBk6VEvepWY-rw)

Окно настройки инструмента

![image-1683718457453.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd0q-6eq7G8Vfmi3c1FI_RG0_V_c5cc6kT7eJtAr0sCI5jxF7zVmLs8eZKuS0MT8DaqnlgeDSMNchoxoEdD2hwOuyWQ7oBooBqx574AJGHEcNCQJLpfChd7pJSAyedG7zqt0TeTQiMf_Y53aUvR9Q?key=EO6iZbWODBk6VEvepWY-rw)

-   ***Переключатель “Копировать материалы”*** отвечает за визуальное отображение материалов на скопированной геометрии. Рекомендуется держать его выключенным, поскольку копирование с материалами, увеличивает общее время работы команды.
-   ***Переключатель “Включить проверку по ID”*** предотвращает дублирование ранее скопированных элементов. Если необходимо заменить ранее скопированные элементы, удалите устаревшую версию элемента перед копированием. При этом замена элемента влечет за собой замену его id в строительной модели, следовательно, из-за смены id Navisworks не сможет подтянуть данные SIGNAL в новый элемент.
-   ***Переключатель “Создать пирог конструкции”*** разделяет многослойную стену по слоям и копирует каждый слой категорией Части

2\. Выберите элементы из связанной модели, которые необходимо скопировать, и в левом верхнем углу нажмите Готово

![image-1683718475365.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcscHe3Dh_DoK3gk6VReiEbTcf8pEL-GuY692CglG9J9zKdXHK9rbqnuhp0xT0o7T8PxoKM45RwHU1-pP8aEbJt6YpTy80gVb1HugjqUCOf3IbKj2dpqduGx_3aLyFVDTFSMR48eXRk4a8sEN6U?key=EO6iZbWODBk6VEvepWY-rw)

3\. Выбранные элементы будут скопированы из связанного файла и появятся на виде “2. Создание Строительной модели”. Элементы будут представлять собой НЕ редактируемую геометрию с параметрами.

![image-1684157839451.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfGpfvLdmDTqRbyjpxSIWmr3TQfcUe1vPbdb1ckkkKULdKOxrZepJFSNQ5cSzMILxmM-nqr57vdvlUFe2T_XFLgoxkMGuCgSH9IncJFrdjzJaL7f4mgbMDGbI5hUihusOQnXpfur5QbqglIgfR5yw?key=EO6iZbWODBk6VEvepWY-rw)