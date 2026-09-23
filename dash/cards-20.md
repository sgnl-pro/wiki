---
title: DASHBOARD. Карточки 20. Деньги
description:
published: true
date: 2026-09-23T12:16:26.000Z
tags: dash
editor: markdown
dateCreated: 2025-09-18T13:21:31.877Z
---

<sub>**[<   DASHBOARD. Карточки 10. Общие](/ru/dash/cards-10)     **|**     [DASHBOARD. Карточки 30. Сроки    >](/ru/dash/cards-30)**</sub>

<summary style="font-size: 16px; color: #0D47A1; background: #E3F2FD; border-radius: 7px; border: 1px solid #64B5F6; display: flex; gap: 10px; padding: 5px 16px; display: block; margin-top: 10px;">
<span style="flex-grow: 1;"> <a href="/dash/cards-20/updates" onclick="event.stopPropagation();" style="color: inherit; text-decoration: none;">🔄 Что нового (история изменений этого функционала)</a></span>
</summary>

---

# Вкладки{.tabset}
## 20_Процент освоения денег
###### 20_Процент освоения денег {#card-20}

Карточка показывает степень освоения денежных средств объекта в процентном соотношении: план/факт/осталось. Например, можно визуализировать общий процент освоения денежных средств по всему объекту или процент освоения по отдельному виду работы.

Отображение карточки в режиме пользователя

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdRVL6sATY9L3Dv66y7pFbQmVQVDaFVc3clBa737eov7lYWL1_zdo45Jo06tUOJHui0XM9i5ovzr-IO-KHqkYLQB1o3PMajsxaQi8sKH0Pt2tgIXD0JMQyWLk1Xc_mUPZmPj_G3GWx7DTWSYielVw?key=887Aaw5M9mjjgbnP7IUNLw)

-   Окружность целиком — весь объем денежных средств (100%)
-   Синяя полуокружность — фактическое освоение
-   Серая полуокружность — плановое освоение

**Настройка карточки**

1\. Основные настройки

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdszvH6urRotw3mv24VyyAvRlvdU2-VajWcucTCTn-k2fyFn6ULxcYmBlXpSv_nsTgzg7FhxJRYFWZTfZza10UZsYmsjI_SNCN0i3hJwk0F_Pm3l1x9DcoOoJq4gSqCNs1vEaRnsZOT-YQskUn6NQ?key=887Aaw5M9mjjgbnP7IUNLw)

-   ***В строке «Название»*** впишите название объекта/подрядчика или вида работ, по которому хотите отобразить процент освоения средств.
-   ***В строке «План»*** впишите плановое освоение.
-   ***В строке «Факт»*** впишите фактическое освоение.
-   ***В строке «Ед. изм.»*** впишите единицу измерения для отображения.

## 21_Общая накопительная по деньгам
###### 21_Общая накопительная по деньгам {#card-21}

Карточка отображает планирование бюджета строительства: оплата принятых конструкций, удержанные деньги, данные об авансе.

**Отображение карточки**

![image-1681298475900.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc7gz_IHCi28nMd5tnUTmglZMFbu6b2ek9EBWk5kZWWAVpU45ZmFBQ3YkKlmQnwTgT9TQ1rFwbjR4M7CBeCXM1YheuvgZmxqzKqu4H4QTUFk3oODCcFGhL5_2UZ5JBMqFKWXd1Go4MdzNUxmIfFuA?key=MHvS0J4XLMea1KtJ_XIgQg =300x)
![21_2.png](/sgnl_dash/20_money/21_2.png =300x)

**Настройка карточки**

<details>
<summary>Шаблон Excel</summary>

|        |                              |
|-----------------------------------|------------|
| Заголовок                         |         21 |
| Статус                            |    TRUE    |
| Url изображения                   |            |
| Тип                               | money      |
|                                   |            |
| Название                          | Монолит    |
| Дата                              | 12.12.2025 |
| Ед. изм.                          | ₽          |
| Закрыто в счет аванса             |      90000 |
| К оплате за                       | Январь     |
| Гарантийное удержание             |      10000 |
| KS-2                              |      80000 |
| Удержано по Предписаниям          |      15000 |
| Предъявлено к закрытию            |      70000 |
| Рекомендовано к удержанию         |      24000 |
| Общая стоимость                   |     150000 |
| Аванс всего                       |     150000 |
| Скрыть "Удержано по предписаниям" |    FALSE   |
{.dense}

</details>

**Заполнение карточки вручную**

![image-1681298506449.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcGqJ51PiwyGmxORdbRvhdbQQC8pVXs2ytSe49eyi4LIJhXDShOE4TW7g_tHhwmduApJajhvrrxA2Mvic8aMVIZ6pt95JpXzYNMdWUHoBjOn-uMytP6eEyHV92WEt7kUShKxIAhkGJgXmQx_Zoj?key=MHvS0J4XLMea1KtJ_XIgQg)

-   ***Переключатель «Скрыть Удержано по Предписаниям»*** скрывает в карточке поле «Удержано по Предписаниям»

**Заполнение карточки с помощью Excel**

-   Откройте пример заполнения карточки и скачайте его в формате Excel кнопкой «Экспорт».

![image-1681299797321.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdVNxiSc3ptOy6Iv-0vR6SlCUBXfYRJ-5PptcwjnDBxH0WoTcpkVQw3PCWNtabXMGjf-JZfNTj8AF2XdPCCMFdKB4WtaWIW5_DAB5OIKuOpR-tDozFfubieiVPBNV_xsDc5qeakb79VgsuEGxy9OQ?key=MHvS0J4XLMea1KtJ_XIgQg)

-   Заполните таблицу Excel в соответствии с вашим проектом
-   В настройках карточки нажмите «Вставить данные» и вставьте значения из столбца «Значение» сочетанием Ctrl+C и Ctrl+V.

![image-1681300471892.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXciTFLJkxP5xH1o-_kydOXt-4OK7Rv4PNaT_GhFfWvF0MIlEp15njRpKLynM_XYoVsHsKJW_RvXV8DGmJZuwwtU8Alw_SJ5-vlVp3nW_NBnxdIsCEPy548oovl16hDnl1qOYZ0pYgAstSKdjfSp?key=MHvS0J4XLMea1KtJ_XIgQg)

![image-1681299734093.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcRMbaF5nWLPEo3meD95EX3OcWoRmgCWpUenP9pVmkMG9k_PHhozXC4UzrTcriCGbxVo6kVbrs_7S_3mt1WNQ5vwUicceEGv5AH7JGFeHK9TySOlbgSf-nqI_r3MhCbopyCZ5FHAWvFM1X6ZmSeZw?key=MHvS0J4XLMea1KtJ_XIgQg)

## 21_2_Общая накопительная по деньгам 2
###### 21_2_Общая накопительная по деньгам 2 {#card-21-2}

Вариант [карточки 21](#card-21) с обновлённым оформлением. В настройках задайте общую стоимость, аванс, оплаченные работы, удержания и показатели отчётного периода. Можно выбрать размерность сумм (тысячи, миллионы или миллиарды), округление и единицу измерения. Поля «% аванса от остатка» позволяют задать подпись и процент; процент ограничен диапазоном от 0 до 100. При необходимости скройте строку «Удержано по предписаниям» или включите показ дробных значений.

## 22_Освоение денег по месяцам
###### 22_Освоение денег по месяцам {#card-22}

Визуализация данных о том, сколько по факту оплачено и/или по плану.

[Шаблон «Деньги по месяцам»](https://docs.sgnl.pro/s/f/4d8f615a-27fd-4b1a-a631-c7529eb99f03)

**Отображение карточки в режиме пользователя**

В режиме просмотра отчёта:

![43_Деньги по месяцам.jpg](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdQkd9dbCFZ1ZPun4I9Q2GovH6ZsHBKMQeb7kue45jGgvOtAvLh1Wey04WcZNPRz1OBNnOSf1jjvm72IzTm4Hs9ymGsGUYK5KK04RYpAE9DRFb9vqFhf1HiH6g3eWF0QJ6Pm8y5MfyIJmEZl0yfHw?key=X_gNv6zfO4a7j-sEGl0Nxg)

При открытии карточки:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcaY6wTjwHr6mLke0z_ilA85EhXt5BNyHni61cCbCTEplmBcuhsB8NSn4dKAXTtHkw-LfsIOnwDEIgRpKGMc2ulSysJo5wnGLMGdlQmuUN8RuFmGkMVlLidIBF5JvpHo2diIMjjxu241AWBTQyI?key=X_gNv6zfO4a7j-sEGl0Nxg)

**Заполнение карточки**

В настройках задайте начальный и конечный месяцы, текущий месяц, общую сумму и единицу измерения. В таблице укажите для каждого месяца план и факт. Можно вставить данные из буфера обмена; пример формата доступен в настройках карточки. Два ряда за один месяц добавить нельзя.

Для импорта из 1С сначала загрузите выгрузку в формате JSON или TXT в папку проекта в DOCS. Затем в настройках карточки откройте «Импорт из 1С», выберите папку, типы документов и компании, данные которых нужно собрать. После импорта факт и месяцы импортированных строк заполняются из файла; вручную в этих строках можно изменить план. Дополнительные строки можно добавить вручную. При повторном импорте указанный план сохраняется. Для обновления данных из выбранной папки используйте кнопку обновления рядом с импортом.

## 23_Освоение денег по месяцам с прогнозом
###### 23_Освоение денег по месяцам с прогнозом {#card-23}

Визуализация данных о том, сколько по факту оплачено и/или по плану, а также с учетом корректировки бюджета проекта.

**Отображение карточки в режиме пользователя**

В режиме просмотра отчёта:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfLyc_XI0I4ZCqm5in6NExFFnj7Zp4AjT7JDU5wDV588xZyyZbvXbxSjyAFdLssf39QY-_KbLvORwDzgJ29ICdQmbbDmPYyB_z_wB8omzx4E3XJlFTHDSHAuQn4mXm1ySDp9neak0-dFEdQ4NXwYg?key=Y0-sORLm-ptITFI_ISE7qg)

При открытии карточки:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfF9LOL1O5YhLCoE8KWuNPCkSsu1eunAB-y5-zeGVHAFTeU9ZCB3y07HZ1yWFzgk3i0tIziF90JlEJdF2j8uqVlMXpBIeHrsD37K4saZWIXXXeJAVcwGEDTvx53BlgiYCActnV-zWW6oIr6GIx6sQ?key=Y0-sORLm-ptITFI_ISE7qg)

**Заполнение карточки**

В настройках задайте начальный и конечный месяцы, текущий месяц, общую сумму и единицу измерения. Для каждого месяца заполните прогноз, план и факт. Данные можно ввести в таблицу или вставить из буфера обмена; пример формата доступен в настройках карточки.

## 24_План-факт финансирования
###### 24_План-факт финансирования {#card-24}

Карточка показывает соблюдение графика финансирования и прибыль по месяцам. Для каждого месяца заполните «План», «Получено» и «Затрачено». Прибыль рассчитывается как разница между полученными и затраченными средствами.

![Карточка «План-факт финансирования»](/release_notes/2026-7_-_карточка_24_.png)

В настройках задайте начальный и конечный месяцы, текущий месяц, общую сумму и единицу измерения. Затем заполните месяцы в таблице. Данные также можно вставить из буфера обмена; пример формата доступен в настройках карточки.

#
<sub>**[<   DASHBOARD. Карточки 10. Общие](/ru/dash/cards-10)     **|**     [DASHBOARD. Карточки 30. Сроки    >](/ru/dash/cards-30)**</sub>
