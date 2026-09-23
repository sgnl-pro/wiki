---
title: DOCS. Публикация файлов
description: 
published: true
date: 2026-09-23T07:21:29.295Z
tags: docs
editor: markdown
dateCreated: 2025-09-09T12:32:31.629Z
---

<sub>**[<   DOCS. Передача](/ru/docs/documentsTransfers)     **|**     [DOCS. Уведомления   >](/ru/docs/notifications)**</sub>

<summary style="font-size: 16px; color: #0D47A1; background: #E3F2FD; border-radius: 7px; border: 1px solid #64B5F6; display: flex; gap: 10px; padding: 5px 16px; display: block; margin-top: 10px;">
<span style="flex-grow: 1;"> <a href="/docs/sharedSettings/updates" onclick="event.stopPropagation();" style="color: inherit; text-decoration: none;">🔄 Что нового (история изменений этого функционала)</a></span>
</summary>

----
# Вкладки{.tabset}
## 1. Публикация файлов и папок
###### 1. Публикация файлов и папок {#publicdocuments}

В SIGNAL DOCS можно открыть доступ к файлу или папке по публичной ссылке. Получателю ссылки не нужен аккаунт SIGNAL. Возможность создавать публичные ссылки регулируется администратором проекта в [настройках проекта](/docs/settings#functions).

1. Нажмите правой кнопкой мыши на файл или папку и выберите «Поделиться».

![chrome_1vphseyhmx.png](/chrome_1vphseyhmx.png)

2. В окне «Публичный доступ» выберите тип публикации и при необходимости настройте версию и срок действия ссылки. Нажмите «Открыть доступ». Публичная ссылка скопируется в буфер обмена.

![chrome_9v3whjmizs.png](/chrome_9v3whjmizs.png)

Тип публикации определяет, может ли получатель скачать содержимое:

- «Только просмотр» — просмотр без скачивания.
- «Просмотр и скачивание» — просмотр и скачивание. Этот вариант доступен, если у вас есть право скачивать файл или содержимое папки.
- «Простой просмотр» — просмотр BIM-модели с ограниченным набором инструментов. Вариант доступен для BIM-файлов, когда в проекте включён Forge Viewer.

![chrome_ax9x6mb95g.png](/chrome_ax9x6mb95g.png)

![chrome_qvjzy0vfpy.png](/chrome_qvjzy0vfpy.png)

Настройка «Поделиться только текущей актуальной версией» закрепляет версию файла, которая была актуальной при создании ссылки. Без неё ссылка открывает актуальную версию файла, в том числе после загрузки новой. Для папки эта настройка также доступна; для комплекта файлов её нет. Если включить «Дату истечения срока действия», выберите дату в пределах двух лет. После неё ссылка перестанет открываться.

![chrome_vhwyq8misx.png](/chrome_vhwyq8misx.png)

3. По ссылке на папку получатель может просматривать доступные вложенные папки и файлы. Скачивание доступно только при типе публикации «Просмотр и скачивание».

![chrome_9ymmvb2od0.png](/chrome_9ymmvb2od0.png)

4. Опубликованные файлы и папки помечены значком публичного доступа:

![image-1703748741610.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeZhHwagBsgQh4qJm-MoEWCYkydIFbbbokzkttJjfqUcUdH1IIyNBJ3F0wie2aj8t9sx1sA1VssVE6VQuwbuCcRUFfA9FKGSO-J2emcup2cqreuRRZkYthYZRrGQ9uMqnNYbtCR3ynTpcOvR2Dv?key=jsauY7gtcpEA07Snv4NNyw)

Нажмите на него, чтобы скопировать ссылку, изменить настройки публикации или отключить доступ. При наведении на значок отображаются автор и дата публикации, тип, опубликованная версия и срок действия, если он задан.

![chrome_iwblhhlo04.png](/chrome_iwblhhlo04.png)

## 2. Публикация моделей
###### 2. Публикация моделей {#publicmodels}

Публичную ссылку на BIM-модель можно открыть в доступном для неё просмотрщике, в том числе в SIGNAL Viewer. Если для модели доступны несколько вариантов, получатель выбирает просмотрщик при открытии ссылки. Для режима «Простой просмотр» используется Forge Viewer с ограниченным набором инструментов.

Для простого просмотра администратор может настроить [отображение элементов и их свойств, наборы выбора и информационное сообщение](/docs/settings#services). Сообщение, если оно включено, отображается получателю при открытии модели.

![simpleview_user.png](/sgnl_docs/docs_publication/simpleview_user.png )

На снимке: 1 — линейка для измерений; 2 — наборы выбора, сгруппированные по конфигурации; 3 — переключение 2D/3D; 4 — показ помещений.

## 3. Публичные ссылки
###### 3. Публичные ссылки {#publicadmin}

Администратор проекта может открыть раздел «Публичные ссылки» и увидеть ссылки, созданные в проекте. В таблице показаны название файла или папки, сама ссылка, автор и дата публикации, тип публикации, опубликованная версия и дата истечения срока. По названию можно перейти к объекту в проекте. У ссылки доступны действия для изменения настроек, копирования и отключения доступа.

![chrome_9hdypyvgjc.png](/chrome_9hdypyvgjc.png)

![chrome_trjhazgu0u.png](/chrome_trjhazgu0u.png)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeyYgH5wNi8b1g7QVwSieYcefqhlAH5yhLAAODneC6s7FATz_iGMZKX3roF_rZVRTqeGx0yOCq6ts6uukDUSRpZcnOZfOTKAFWkjYsxPu154yDnl5G0Yql88ZBZ49YdEAo?key=jsauY7gtcpEA07Snv4NNyw =70%x)

#
<sub>**[<   DOCS. Передача](/ru/docs/documentsTransfers)     **|**     [DOCS. Уведомления   >](/ru/docs/notifications)**</sub>
