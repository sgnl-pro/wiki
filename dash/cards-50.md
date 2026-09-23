---
title: DASHBOARD. Карточки 50. 3D карточки
description: 
published: true
date: 2026-09-23T15:14:48.000Z
tags: dash
editor: markdown
dateCreated: 2025-09-18T13:39:52.568Z
---

<sub>**[<   DASHBOARD. Карточки 40. Объёмы](/ru/dash/cards-40)     **|**     [DASHBOARD. Карточки 60. DOCS    >](/ru/dash/cards-60)**</sub>

<summary style="font-size: 16px; color: #0D47A1; background: #E3F2FD; border-radius: 7px; border: 1px solid #64B5F6; display: flex; gap: 10px; padding: 5px 16px; display: block; margin-top: 10px;">
<span style="flex-grow: 1;"> <a href="/dash/cards-50/updates" onclick="event.stopPropagation();" style="color: inherit; text-decoration: none;">🔄 Что нового (история изменений этого функционала)</a></span>
</summary>

---

# Вкладки{.tabset}
## 50_3D объёмы в BIM по датам
###### 50_3D объёмы в BIM по датам {#card-50}

Карточка показывает 3D-модель и сравнивает плановый и фактический объёмы работ по выбранным датам. По графику можно проследить выполнение работ и опережение или отставание от плана.

![image-1719410224901.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfMZzaczqqrDJKW79jH_xGMakDStpMzoUdsam5Sbh_qGwPAqVMxN7JvVp-yfi_JZjgWryUbAT-iVgDaJkm35PqlpDNqDIv6bxID-2oih1f5Cc4mHuku7dz76HSqgiL1QbG_r8a_QaGbPCvAZj4s?key=YsYWdNWdbJcfmRoINnnzwA)

**Настройка карточки**

1. На вкладке «Основные» выберите модель из DOCS. При необходимости добавьте модель подложки. Укажите плановый и фактический объёмы, единицу измерения и включите отображение списка видов работ, если он нужен в карточке. Если объёмы берутся из модели, поля ручного ввода недоступны.
2. На вкладке «Легенда» настройте подписи цветов и показ легенды в карточке и на превью. Кроме системных цветов можно добавить цвета, заданные в TOOLS.
3. На вкладках «Объёмы», «Площади» и «Длины» проверьте свойства модели, по которым рассчитываются показатели. На вкладке «Типы» выберите дополнительные статусы элементов, которые требуется показывать, и задайте их цвета. На вкладке «Цвета» выберите цветовую схему плана и факта.
4. Сохраните карточку.

![image-1719471733932.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfQk-O4uYL5tRKXmpsQvlNaHiNQbdggGKqsHV-Bb4gjA4xYIHUxuj3dy1qRa1Em9WwqrljJa7nTwC4V_0OK_ES8gmoxQjFh1XeWTqZHkexgtrra5AVTw3cPa6-LC-2LRJ9eBPI30Bu-42E9BZBEGQ?key=YsYWdNWdbJcfmRoINnnzwA)

![image-1719472349093.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe5c9cihXAEesuJdPzbGT2LNk3XR5O9K_lxjgYCloUnzGbks2zCjG6AcTe0o5i8ryPK4MJf8rSnmf6pPFEnk6449PQYWDLzbzdxg5ce2gg5rmqME9kO2Nv_cgtQBQ7NPvXevyUAAY2y-UtZPJ-62Q?key=YsYWdNWdbJcfmRoINnnzwA)

**Просмотр карточки**

Выберите виды работ, даты и при необходимости подрядчика. Список дат поддерживает выбор диапазона; выбранные даты выделяют соответствующие элементы модели. График «План-факт» открывается в просмотре карточки.

![image-1719471599913.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe6B3getW6Oz7wsS4K74lt3qQICdg1glAHv9_yTy5wultr4I3BvRK4aBVPFZ6jzMlzCR_MXDK5ZqqlFKdcDsIa5IwWEH-7YQFXPxkslvANAcYvaDQOKPNtKu8HrMtPKIlCEjjqYjy9Px5UW6ajErg?key=YsYWdNWdbJcfmRoINnnzwA)

Если плановый объём заполнен вручную в настройках, карточка использует его. Если поле пустое, объём рассчитывается по модели. При разных единицах измерения карточка показывает предупреждение — проверьте настройки объёмов и свойств модели.

При наличии права редактирования отчёта в просмотре модели можно сохранить снимок для превью карточки. Этот снимок также используется при экспорте отчёта в PPTX.

![image-1719472462662.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfwNK1n3PtXjNSnOlyoBBm2k1qa9I9F5vkbMryR4ZtkgI1JOaP0W7I6iFolbnpcO9z_D_Fw6dGryc8wP1F8jPOBOgxLm56hrrabPrECrEzLE5__H57xAjGiRkPr_oP8KCVglBNFVSz2hKavKxYyhA?key=YsYWdNWdbJcfmRoINnnzwA)

## 51_3D объём в BIM за период
###### 51_3D объём в BIM за период {#card-51}

Карточка показывает модель и сравнивает плановый и фактический объёмы работ за период. Настройте модель, свойства объёмов, статусы, цвета и легенду так же, как в [карточке 50](#card-50). При просмотре укажите начальную и конечную даты периода; доступны фильтры по видам работ и подрядчику.

![image-1719475867082.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdN9CMcXqwW8_qhsV2ruiAlvmLYZFWLYs334IvpqeaWkIKyb5WRILAa75NlB8yaQsCqhaWRNukUG3jCWxv9fQ7lOaRTLUNGVv7GbBb-wuH1IwoMzdrQRF6eBOXktbjkTr3yNbB6-Te9XH8t8ZKE?key=jGY6qOPVFanfIvvGDWzJ4A)

![image-1719476021131.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfHrPQ2r9tES22qJj9QzDNKPTuUmRaUiIfKZSjOJLDXeoXixM7ID1Amg9JXeW-KEUWyfflrWwZvyug5DPqz7AVrnknJ_rFlniB-P-SLXjIwEDP2AxOzUS90xHLzpou752JvW2BbYUO3-5CU8v5Cwg?key=jGY6qOPVFanfIvvGDWzJ4A)

Если плановый объём задан вручную, он используется вместо значения из модели. При разных единицах измерения проверьте предупреждение в карточке.

## 52_3D Цвета
###### 52_3D Цвета {#card-52}

Карточка показывает модель с раскраской элементов. Цвета можно передать из Navisworks с помощью [«Раскраски» TOOLS](/tools/navis/coloring). В отличие от карточек 50 и 51, здесь не рассчитываются плановый и фактический объёмы.

![chrome_nl4jfnuazc.png](/chrome_nl4jfnuazc.png)

**Настройка карточки**

1. На вкладке «Основные» выберите модель из DOCS и при необходимости модель подложки.
2. На вкладке «Цвета» задайте подписи для системных цветов: красного, жёлтого и зелёного. При необходимости добавьте цвета TOOLS и задайте подписи к ним. Здесь же можно включить легенду на превью.
3. Сохраните карточку.

![chrome_xhf1r2mouw.png](/chrome_xhf1r2mouw.png)

При просмотре карточка показывает модель и настроенную легенду. Нажмите на цвет легенды, чтобы оставить в модели элементы этого цвета. Повторное нажатие отменяет выбор.

![chrome_c6t2sh7xg9.png](/chrome_c6t2sh7xg9.png)

![chrome_slzynondep.png](/chrome_slzynondep.png)

## 52_2_3D Цвета 2
###### 52_2_3D Цвета 2 {#card-52-2}

Карточка позволяет одновременно показать проектную и строительную модели, а также модель подложки. Для проектной и строительной моделей можно отдельно настроить прозрачность.

![Карточка 52_2: проектная и строительная модели](/2026.2_-_карточка_52_2.png)

На вкладке «Основные» выберите проектную и строительную модели из DOCS, при необходимости добавьте подложку и задайте прозрачность. На вкладке «Цвета» подпишите системные цвета и при необходимости добавьте цвета TOOLS. Сохраните карточку. В просмотре нажмите на цвет легенды для выделения соответствующих элементов; повторное нажатие снимает выбор.

#
<sub>**[<   DASHBOARD. Карточки 40. Объёмы](/ru/dash/cards-40)     **|**     [DASHBOARD. Карточки 60. DOCS    >](/ru/dash/cards-60)**</sub>
