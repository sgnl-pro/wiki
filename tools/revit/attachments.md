---
title: TOOLS. Утилиты
description: 
published: true
date: 2025-10-01T23:25:52.964Z
tags: 
editor: markdown
dateCreated: 2025-09-21T13:22:22.479Z
---

<sub>**[<   TOOLS FOR REVIT. Копирование элементов  ](/ru/tools/revit/copying)     **|**     [TOOLS FOR REVIT. Приемка   >](/ru/tools/revit/acceptance)**</sub>

---

# Вкладки{.tabset}
## Переключить стадию

> Инструмент Переключить стадию предназначен для отображения выполненных на строительной площадке элементов на виде “3. Строительная модель (Navisworks)”. Команда меняет в выбранном элементе значение параметра “Стадия возведения” на значение указанное в Настройках SIGNAL в разделе [_Основные_](https://youneedawiki.com/app/page/1VZKa5VY-eaElXKzpwmKikcohhV8KuNG6iiBaAzT5Lc4) (по умолчанию это “Выполнено”).
{.is-info}

1\. Откройте вид “2. Создание Строительной модели” и выберите элементы, которые фактически выполнены на стройплощадке

2\. Нажмите на панели Утилиты ➤ Переключить стадию

![image-1683718520427.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXftn7QuDe-FoIBI0uoSUrmM-RS7QnccykQS5llYnvlTf-LB2b26WRhBAsYvlYBFOvmYrdVdOLCgX0EKf-n02tc1_5reO99NhABNJCdeOzWDey7DFem8jlArdSBCztl2iM2ZrBSRB-aI_Kra0-kG9Q?key=wAhQR5dq-yA1zW_QmvLuhw)

Выбранные элементы окрасятся в зеленый цвет на виде “2.Создание Строительной модели” и появятся на виде “3. Строительная модель (Navisworks)”.

![image-1683718533877.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeorRyID_-wc5bnbZEhng0c_eUonPRVcFcFcnK9SR8GYEJOV_z_C4gX4fk5SYX_rzmY_NHq61vMUZT2tIcdiWR-6mE11UmXQ-_m04WudvFkjXo2MaGiJd-SHHXWK1bbEbvO6OXZtHVFAEXdCu5N8Q?key=wAhQR5dq-yA1zW_QmvLuhw)

> ***Примечание***: Для ручного переключения стадии в "Свойствах" элементов найдите параметр “Стадия возведения” и поменяйте его с “Проектной модели” на “Выполнено”:
{.is-info}

![image-1683718548596.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc20qFK44DNiK5ME4a6fw_vjDlR6eiuFDwL2LwUIPX-PcBny5SzlalZN48u5s43W63Xlwv0bai6Qb_QgWpy55HTKN4sy4X9yggl2IySc4EbpKQhABRx-7KYbeaMTF4st415xfUQBOfNMGZEovvvcA?key=wAhQR5dq-yA1zW_QmvLuhw)

> ***Примечание***: Для ручного изменения стадии у частей, необходимо снять галочку с пункта “Стадия возведения по исходному”:
{.is-info}

![image-1683718572026.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXebq17SOkDmDEIJufZPk44EA5yMaU6O9YSIoQISz864eKGGzK-vHvtEf6P-9wNTturTWMr-XPNC5Nxr3tSwo233QJax9jk22I3eO5VjJujIlvPEthy1Y2lChM1HaMJyrBPJHnVclr-cmzjURFYS?key=wAhQR5dq-yA1zW_QmvLuhw)

## Изменения модели

> Инструмент позволяет выделить в строительной модели элементы, которые были изменены в обновленной версии проектной модели с помощью плагина SIGNAL для Revit
{.is-info}

1\. Нажмите на панели Утилиты ➤ Изменения модели

![image-1684826746467.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdGMS3JXYtkbFlfJGSmb-R9awL6xRSmjuG5_ugEfjqLjfI87Pe-DlVZmqUJSv4aWf2oMJh_mzzjiZ45ETI4kOSShOQ7qKPrGXC1IoguMWzVhIVqrxMOCdULdt_6RWvxj55lYNZQ3_nk18J9oqPHEg?key=J4Hsgp6F5olSD9BBXBr6Cw)

2\. Загрузите CSV файл полученный из BIM 360 Docs (ACC Docs) (см. подробнее [_“Определение измененных элементов в СМ”_](https://youneedawiki.com/app/page/1rZwoVD818Yba-6qnne9tID0-xGXeAX2_BSnbAKIn0SQ))

![image-1683719119305.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc9yfeNASl0G1vv3jFuARcSffYJoVP1mtzDA-YWg9QRomuxSdU5OnzMQ5cyPUXfmf_nJrLEJbq6XMWNyvAQG1NomTKcMFFD0A2GM8XotZIHb8aTGomTsMCL9zaH7M8vCBtFFvslb4HLd0SJsvHd7g?key=J4Hsgp6F5olSD9BBXBr6Cw)

3\. В измененные элементы добавляется параметр S Compare. На виде “4. Изменения в модели” измененные элементы окрашиваются в соответствии с значением параметра S Compare

![image-1683719141922.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcy_VsiUp4Od17Tu4DQOw_3gGBH_nVGvycjOjgSPH45YFOtJO4TRBn3VvS42zEq6UlbvIVeh10fF_N71oKbv-1x_lObTNYNgJiTSdFnGrs3v7OuY5srFLqAh6fLCXSa1YHzk-JLcLE_XR2mQsC4iA?key=J4Hsgp6F5olSD9BBXBr6Cw)

-   Removed - Удален
-   Added - Добавлен
-   Geometry - Изменение геометрии
-   Move - Изменение положения
-   Parameter -Изменение параметра

![image-1683719208142.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeL8jVPdkCGxHzXXq8pB0CUSkuSMCjLoOqsJSdKetnMcBgEQ2aM14VQUOFqeCxVSuAMZBO00aAr8G5u5Kwlf9YYwlIWL7eOBkl-gDG4ZYcYPxP46hJg0i0Hxrzd_VxhjNL-UfRYdnqh8ymB61I3?key=J4Hsgp6F5olSD9BBXBr6Cw)

## Определить местоположение

> Инструмент позволяет определить местоположение элементов модели по отношению к уровню и ближайшим осям сетки осей с записью результата в параметр “S Местоположение”
{.is-info}

1\. Нажмите на панели Утилиты ➤ Определить местоположение

![image-1683719220708.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeFVVfdG8mB-u4_yk3LsyNmZhX0X3SY6LxMfZDeVQLGQ7yAURJDExQdfC1aYRl454cSvAV3NIMaw-fmkOWcZRmpqydzZmczrPrjb1Rh7ZYQUDPeOeAZozrebooZudHUacTCEVDnhQfumTEMw55N?key=Aaaw4CrTpTP-qTvJv2JC_w)

2\. Выберите элементы модели и в левом верхнем углу нажмите Готово

![image-1683719239418.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdTgnB5PL_yQoNFrmSIyiLfxkZciy8RlvYq6hQPwJT4y-GUSKnl_xpx1PyYPxIClJwWWy4QBTi_LF62mlsEPruklSStCHb6FZG10480X8ddBmbZZv9OH4BwxbyQPPecWla5oCW4eVebnv80lMdCyg?key=Aaaw4CrTpTP-qTvJv2JC_w)

3\. Выберите из списка параметр осей, в котором содержиться название осей. Например, параметр Имя.

![image-1683719249409.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXecDxEgaQMOYOaE-ZxUIcYBe-Zc7vWmu_g9jQDCvM67zJtHzexJhZbeED2JEFSqOg7ZwvYCRX7mXuhF5XZt0GPv8jh1_Fr-cAUJJxMwxpX9TVNwCZMm37MqURUWN86dKE4xR7ACNtMMqMA82bi6?key=Aaaw4CrTpTP-qTvJv2JC_w)

4\. У выбранных элементов создался параметр “S Местоположение”, в котором указано расположение элемента в осях и указана отметка элемента в метрах. Например, отметка +23,340 м, в осях 1.1-2, в осях Б.1-Г

![image-1683719259962.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeKDGmZhvr4GS6wAi-l-AKGegtOVmep3WbRcoLLjCn1d--CPzDvrqcIhZxVRGKBEzZYZF6E5yJ8Lvtb9OaWo-sDWEcI3bJ4dNFjiFk2CFoIeHauz5E1OmLoIGoLwmxBjHRXNmzu5ZL15_A5qk9TIg?key=Aaaw4CrTpTP-qTvJv2JC_w)

## Видимость связей

> Инструмент позволяет управлять видимостью связей на текущем виде. Аналог вкладки Связанные файлы в Переопределении видимости/графики, который можно привязать на горячую клавишу.
{.is-info}

1\. Нажмите на панели Утилиты ➤ Видимость связей

![image-1683719278760.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeOZ7MLp6C_fEW6Dw4LDveHMYhgyMwPVvo0V88wK_UNq5LoKJ83wwLMpQCIbJDkqpu9LK7hGHSS8mGTCevbNxd0a8iwHcqJyvZOrGnY2IQUl_g_KnKJEZdrE8W08jrS2o3OhsDxtresV0rlik6Liw?key=pnr3iREOubCbJgYhEOJzaw)

2\. Уберите галочку с связного файла, который необходимо скрыть на текущем виде

![image-1683719282494.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfMff2zANFWqCpmSFmJqukZC1u8Y4iuSEbSX7PDrYcrWkgG-dLIGa61kGJcfijZkA2kwPTQLP-t_B1STWFq1ls4zf3tYvpWGrzModlufJTYzO67GvdawLX93ykyJwVdWYMERi1MSifaKZ1KI2Bilg?key=pnr3iREOubCbJgYhEOJzaw)

## Автообработка

> Инструмент помогает BIM специалистам автоматизировать процесс выгрузки и проверки Revit моделей, расположенных как на локальном компьютере, так и на Ревит-сервере. Плагин в указанное время без участия специалиста сохраняет RVT файлы в указанную директорию, выгружает их в форматы NWC и IFC, проверяет командой "Checker" и классифицирует модели с помощью “Код по условию”.
{.is-info}

> **Примечание:** Плагин можно запускать из любого Revit файла, даже из пустого. Версия обрабатываемых Revit файлов должна совпадать с версией Revit, с которого запускается плагин. Не закрывайте инструмент и не выключайте компьютер до завершения процесса Автообработки.
{.is-info}

1\. Нажмите на панели Утилиты ➤ Автообработка

![image-1697535256664.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeXOIPlkmx7OkBpQf7GTzDuoaub9fvM-Kw5-PoGQfh53zjaZHza6M1MHNYZH3uic_YtfMNPidxkdqqQUTS4jqObTcwpQ9SjuMMmmBuGXIYI4fZoM-KKeMsUYtGlGEULvohu3fbRGlR4n2gP8dWd2g?key=eZQrGNoK3AtGdzk6p2pboQ)

2\. В окне "Задачи" нажмите + и добавьте действия, которые будут по порядку совершаться над выбранными файлами.

![image-1703066473403.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdtFcZP1MsvgY-a7foolMJE5ABfnnnYRCQicl0lL2hQZYlSL6MQb8oMn6-92upqiA3Nr2wdTB0VmKoKn3aYcrGnwTp_oUU43CIJ9K2LW_eNLDseyQg6jbuE6bidFSA-tvIjzBwmrcHvpjM9Ui1j?key=eZQrGNoK3AtGdzk6p2pboQ)

Порядок воспроизведения задач можно изменить, перетащив их.

![image-1703169272347.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdbuMbkr-4YLT9p5tVLfVJX7HjLn2HcfeOPZ1iNXNVE4H-lVcgYm-HpiX3smyzWwK3mPiyg5qE25dr4KnIPhSqm-FetmTxi9ObhYLFRwd92Ds9oT5kzwNu4NJZPA2-CVcfNLWef87H0QTbUPfub?key=eZQrGNoK3AtGdzk6p2pboQ)

-   [**_“Код по условию”_**](https://youneedawiki.com/app/page/13PMTPC2kgQs_xTyobyOCd3uWQ0S9rRwFUu5j82kj4TM) назначает код по классификатору всем элементам по определенным условиям. Правила берутся из файла, откуда запускается Автообработка

> **Примечание**: Необходимо использовать эту задачу с отключенной опцией "Открывать файлы с отсоединением от центральной модели". В противном случае все изменения не сохранятся в исходном файле.
{.is-info}

-   [**_“Checker”_**](https://youneedawiki.com/app/page/1oO30Ot53EHyk0JRDfJw8leG514l3mVeucYlNQJVVoUI) проверяет выбранные модели на наличие параметров в элементах и заполненность значений этих параметров. Итогом проверки служат Excel файлы с результатами проверок. Правила проверки берутся из файла, откуда запускается Автообработка. В инструменте [_"Checker"_](https://youneedawiki.com/app/page/1oO30Ot53EHyk0JRDfJw8leG514l3mVeucYlNQJVVoUI) необходимо поставить галочки напротив производимых проверок.
-   **“Сохранить в”** сохраняет выбранные файлы в формат RVT в указанную директорию. Для сохранения моделей с совместной работой рекомендуется использовать опцию "Открывать файлы с отсоединением от центральной модели".
-   **"Экспорт в NWC"** экспортирует выбранные модели в формат NWC в указанную директорию, с использованием текущих настроек экспорта. Экспорт происходит с вида "Navisworks". Если в файле нет вида Navisworks, то экспорт происходит с первого попавшегося вида, содержащего слово "Navisworks", например "BIM\_Navisworks" или "Navisworks КР". Если в файле нет подходящих видом, то происходит экспорт всей модели.
-   **"Экспорт в IFC"** экспортирует выбранные модели в формат IFC в указанную директорию.

> **Примечание:** Директория для экспорта указывается в поле “Папка экспорта” внизу окна.
{.is-info}

3\. В окне “Файлы” нажмите 

![image-1697535302085.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcOgViaPMesQsB_8zHqja4xgiLZSy8-DpFTYV3pPCAFG_IQZ9nid_K-TfupCwVUsysc2kNsk65wd5IK85YWzC5zE6cwsP3YgAVq36jk2TyKW2h0Sj0ya37FTFlYNDFcHtTyiloU3nb5z70uLfu5TA?key=eZQrGNoK3AtGdzk6p2pboQ)

чтобы выбрать файлы формата RVT с локального компьютера, или 

![image-1697535315809.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXficYmA3zbpP_BNDYj64_n-v3tKNCt_B14dUaxJ-HUZp_dnVGPuv2fSjzku40I5XjIqujYxjKdRekqHFz0VSl4Nr1ihTzXQCLD1Jauw8a0fAbcxTdZgNjsgIcdYWMDB4LTXGLsicaAOKCIJiaTqcg?key=eZQrGNoK3AtGdzk6p2pboQ)

, чтобы выбрать файлы с Ревит-сервера. К выбранным файлам будут применяться ранее указанные задачи.

![image-1703066859542.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdxPUbXOKB0RXXmoVBVq78dS1l9ti4yqyL3bEOPpw6zFzh2CiNEJ7utJMcdxsAOlYK3oFNFRh4FeOmj6lFAknmlIGBNNT9HLLPfwFW_qd4D_0GJxZszBVm8Fl3eoTYslG-NKaBOpRkRW3U9jfAy?key=eZQrGNoK3AtGdzk6p2pboQ)

4\. Окно “Настройки” содержит разные варианты запуска Автообработки.

![image-1703169345011.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeiA7tZAn1wAi85lrUYf5DKpA5Dzc9zS5sxen-V1B0cmzvmKR51aKrQ7t_gdSU3WBL-vKY_67xu_HQV0FeSKdhKeu2496Rqa7iSeC2FzsxpUluatvgDmxomBSji7DrbazNw3XecQRhSNefHY32Rpg?key=eZQrGNoK3AtGdzk6p2pboQ)

-   Вы можете выбрать запуск **_по дате_** или **_по дням_**.

Для разовой обработки модели воспользуйтесь запуском **_по дате_**. Плагин запуститься один раз в указанные дату и время.

![image-1703169373494.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe3ZL54raLW7b84s97BSPDBWL_f5ExnZju9bdasVpiXKlniQ0oQ-H0EK-eCdgi-N62bWIP35hqdHYFUHAeY3tB_qESfJfrMK3uSSOBekBkUmNKqo3Ub0eo2C4fhpYiSEOXp9MWRCNvu4gYdtkBI?key=eZQrGNoK3AtGdzk6p2pboQ)

Для регулярной обработки файлов выберите запуск **_по дням_**. Плагин будет запускаться в указанные дни в одно и тоже время.

![image-1703169377244.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcaWXhLGkGcbeTfhyophUZAeyMoRk0e5Ux7GmPFSAOj9VJq3RaPQN8uxkM3aApHBWD1T8f15KyhdyYC0-33ls3kN3Xn5nlV0M28MmnqEe79nNq9LN_WZ-HLOtBG1osJMsxdME9OVRtXhC2mRhvGrQ?key=eZQrGNoK3AtGdzk6p2pboQ)

-   Опция **"Открывать файлы с отсоединением от центральной модели"** позволяет открыть с отсоединением модели с совместной работой. Это необходимо при сохранении таких моделей в формат RVT для дальнейшей их передачи, например, заказчику.

> **Примечание:** Данную опцию необходимо использовать только с командами экспорта, т.к. внесенные изменения командой “Код по условию” не будут сохранены в исходном файле.
{.is-info}

-   **“Закрыть наборы”** позволяет закрыть указанные рабочие наборы при открытии обрабатываемого файла. Например, можно закрыть рабочий набор с связанными файлами, чтобы обрабатываемые модели открывались быстрее.  
     
-   В папке экспорта указывается директория для экспорта файлов.

![image-1703169511120.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc8fH3R5LCneIBfHZIqI-hL_m-7NBi_KLqCJaWOk6mxzOu2njrUkvx73CRW6WFSkY4S06gfXzwOMp3VGvRUKFU1he_StUlCX50tKFin47BiFhgeGWULMOtdcPYCF7WwLS2gmCFx4eioxBtFD3qB?key=eZQrGNoK3AtGdzk6p2pboQ)

5\. После настройки запуска нажмите “СТАРТ”. В указанное время плагин начнет поочередно открывать выбранные модели и совершать над ними указанные задачи. Не закрывайте инструмент и не выключайте компьютер до завершения процесса Автообработки.

![image-1703169440550.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcJMYDpvkK_w2T-_Hc__ZP2mUZPzVXXnH2aqSGzqS5bFUzbdPi3QqYUseF02JMRFxS5WDBX6ZxnvWN8Wf85abjNswwJgGf8y26Z2Fcvfu65a8athaSJuxEXD4wQ3JuH-xL42f51v018lBF8rKah1Q?key=eZQrGNoK3AtGdzk6p2pboQ)

Процесс работы плагина можно наблюдать в окне “Лог”. Здесь будут записываться все результаты выполненных действий, а также ошибки, возникшие в процессе автообработки. Результаты можно открыть в формате .txt, нажав 

![image-1697535359721.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfDlY84YvcamVOzx_s3g03uRB8RQtE3I-lS7U_jbCz6BWrQJlgmjMmbEJzrFPbOfob8RClr9hVKxc6Ac6c-5IRqt01wdveKF1zFhuTwv2E2-KfL5t0KGm5gxOf2EM6X6q0o7VLn5bbIPPMx-is5Dw?key=eZQrGNoK3AtGdzk6p2pboQ)

, и сохранить на локальный компьютер.

![image-1703169412943.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcU2XwqyTNVzdj0tgoC-d3HelgwTz2tTygcd2OqBRpitdpylg-XB5Q3HK35p97svlMxE9RB5V3IL1bca46CCmXLWBLl6cudEhf9_Sdu1yKqaGd1g7Vu-s_ESydv0h_PPiQCeHuys3r-d8py28zD?key=eZQrGNoK3AtGdzk6p2pboQ)

## Видимость облаков точек

> Инструмент позволяет включать или отключать отображение облаков точек на текущем виде. Для удобства можно привязать инструмент на горячую клавишу.
{.is-info}

1\. Нажмите на панели Утилиты ➤ Видимость облаков точек

![image-1683719313791.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdbc5XYNBJ3U2rzOr20I50CnBpWQl9sfs9DEQolelkWUPqm3JE68UkWotUUwha7TVoAPHqJUF307l51uqBZKpYmrceDso4n5n5rJLXVhp_pTNRSaXDK8QzFonfJ-hq414S_GeTtTg7GQFdZdUAarg?key=JdEBItDdM88qX7VZ4TKO9g)

## Серверная обработка

> *Инструмент помогает BIM-специалистам автоматизировать процесс выгрузки и проверки Revit-моделей, расположенных как на локальном компьютере, так и на Ревит-сервере. Плагин можно настроить под задачи, которые будут действовать по установленным сценариям. В указанную дату и время, плагин автоматически выполнит сценарии задач для каждого выбранного файла Revit. От простого открытия и проверки данных файла, до автоматической нарезки квартир по параметрам и экспорта в NWC и IFC.*
{.is-info}

Для вызова утилиты, нажмите во вкладке SIGNAL PRO в категории Утилиты “Серверная обработка”   
 
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcWUKh__FQ_pzHfS6PLk9ifNVmFWzvjuCK7-gA49jVtRH39wtTFMvUyJbCSKhNd9m5GB2jZormhu1JfDjBt2RFnLoFv7icskBFs526XdZRuf7ylqjy30swXkPohiREVYNV0j-MMCQ?key=yp7HKceSXo588Q-RfsVx8Q)
 
После чего откроется окно утилиты:  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcTRbfpfMongMzFvS-kJ9eeTCkcmdEG_byt_R-j4O3CgbBLpvynkhQnL3-zVP9e9uLXTsL-fdjR-Bo0eRBGFyoOdJcvOCOYXVqhM6XL2nPgftygehyOSvGysQQB7ANPyTkd8hR_Sw?key=yp7HKceSXo588Q-RfsVx8Q)

### Вкладка “Задания” 

> представляет из себя окно, в котором можно добавить задания на обработку. Эти задания также можно экспортировать в xml файлы и импортировать готовые.
{.is-info}

В окне “Файлы” нажмите 

![image-1697535302085.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcqIZgqTZQxihZv4Gv4f1vc4SuARGQ2qLKTje4hnyVOtYH7Atw1uzKJ330lvnPoreCjFy6wEB_an1u3VvwCiXOhUD-GmhrnPAQdG3FihsXcYMVNvAZ84QC6K9OGgvHPscmCJFRR?key=yp7HKceSXo588Q-RfsVx8Q)

чтобы выбрать файлы формата RVT с локального компьютера, или 

![image-1697535315809.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdUSzCCEoF6XRYMAUxD9xXNBslwlYtsCkas2ykS0Q5VlCxQ8yKf_scNYV3R0yUTq6zSUoUsIXF7sYkO5m6NFug3OFewgWgmfZxVU4e8n1u2KxNA42ExYRAgdnaidhI_LJFPW3gjHw?key=yp7HKceSXo588Q-RfsVx8Q)

чтобы выбрать файлы с Ревит-сервера. К выбранным файлам будут применяться ранее указанные задачи.

Порядок воспроизведения задач можно изменить, перетащив их.

Вы можете выбрать запуск **_по дате_** или **_по дням_**.

Для разовой обработки модели воспользуйтесь запуском **_по дате_**. Плагин запуститься один раз в указанные дату и время.

![image-1703169373494.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXduQj4RmzzeBI377_rcmmuLNEXUEqymqfaXJ4t2ZJk0qAmVNsMkNWe8ionYqpR2yDLd977RP1bMe9TEcMDSST7lg_9BEpJvqv8kgE3zn2imX4aQrh0_la2jM77o4m2rZx8KQ_YU?key=yp7HKceSXo588Q-RfsVx8Q)

Для регулярной обработки файлов выберите запуск **_по дням_**. Плагин будет запускаться в указанные дни в одно и тоже время.

![image-1703169377244.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdibhcpqBd7TBfLJcQHnR0QEdC_PsZ-otEGrQ34KoJjVbtKnJzlZ4hR_N3jBL9sPC2wPHQDo6XjalVOPVrc7vxweOm5nxbtacqW5WhCl-Kf_PtaBb9E7pGyjIVR_tn7z_YymXhu?key=yp7HKceSXo588Q-RfsVx8Q)

Можно сохранить отчет локально по указанному пути или загрузить отчет в проект DOCS, указав проект и папку.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXccIJ80P727eWpgLJkClzaCm9VIbsMm8QdbV_2g45mpRuLRopvzGGb1r42SOIcoZbNmVudCyjlIfGuWWLV1klnspJ45MLVcdCXS1pjQvakrlbfNDTVlFuOSzLMhlu3azFRImf2c?key=yp7HKceSXo588Q-RfsVx8Q)

Обработка файлов в Заданиях действует по сценариям, они ставятся на файлы через выпадающий список.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdHS834iAHJ5afh7LkN3QZarUoRE_Gu-CLsJvyqJmAaW1b2SUQU_Yv5yV8ZLCm28zTOHro4I9Z95BuuHIix_VCkrzZ0sa_6cspsY1MB29S_I-WDdeZyKuT0BUtAQtiWIf_dlJuknA?key=yp7HKceSXo588Q-RfsVx8Q)

### Вкладка “Сценарии”

представляет схожее окно что и “Задания”. В ней можно создавать, экспортировать и импортировать сценарии действий по которому будут следовать созданные ранее задания.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf_jekRSymZPzIYKHLwfGGsary_lMHcNTSHZhDPN05JLyBOSUfxrP1P85NP2qZ5EaJbORqs9UFs6egNvYwWWVpisldkE7Up8JCtSYNBhbvMdco1dLPoPBA1MH0DZ-0PmZI3viiufA?key=yp7HKceSXo588Q-RfsVx8Q)

Сценарий должен иметь задачи, автоматически в каждом сценарии есть три основные задачи: “Проверить”, “Собрать информацию”, “Открытие и сохранение”. Также можно добавить 8 готовых задач при нажатии кнопки “Добавить”.

#### Открытие и сохранение

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfHtAu94h1aJfKCrhs23wG0oJtRnrqhBfQ8Fl0fXSiACw6k-pB4dtEdYJcmWSx0mpu6wOkkfdlV2R6r5jmsFZHhgrbu_1PKcKYDZoF0EtOlUFF0TGfnCM9K2vwsHhTwHPb1h_wi?key=yp7HKceSXo588Q-RfsVx8Q)

**1\. Открытие файла.** Открывает обрабатываемый проект либо с отсоединением от облачного хранилища, то есть локально. Либо без отсоединения от сервера.

Можно также поставить сохранение рабочих наборов при открытии или нет. Также задать список рабочих наборов, которые будут закрыты при чтении обрабатываемого файла.

**2\. Закрытие файла.** Функция позволяет выбрать действие при закрытии обрабатываемого файла: его можно закрыть с сохранением в пути где файл изначально открывался; не сохранять файл; или же “закрыть с сохранением как”.

“Закрыть с сохранением как” расширяет возможности сохранения:

**3\. Сохранить в папку.** Сохраняет файл в указанный путь при закрытии проекта.

**4\. Сохранить в DOCS.** Сохраняет файл в указанный проект и папку в DOCS. Также можно настроить обработку моделей в Autodesk Forge и Tangl Viewer для дальнейшей работы в DOCS

**5\. Добавить дату.** Добавляет актуальную дату в название файла при сохранении в путь.

**6\. Добавить в папку с датой.** Добавляет папку с датой в названии, папка содержит сохраненный файл.

**7\. Загрузить в Tangl.** Позволяет загрузить сохраненный файл в модули Tangl Value и Tangl Control. Подробнее о загрузке и интеграции данного решения [**_здесь_**](https://wiki.sgnl.pro/ru/docs/additional/tangl)

Добавление проверок включает в себя 8 категорий задач:

#### **1\. Количество элементов** 

 данная задача подсчитывает количество элементом модели в отчет. В задаче можно указать учитывать помещения и учитывать пространства модели.

#### **2\. Листы в файле** 

 данная задача собирает информацию и подсчет листов в файле. Можно включить листы только с размещенными видами, а также параметризировать выбранные листы.

#### **3\. Предупреждения Revit**

 данная задача собирает предупреждения в проекте, по каждому типу. Также можно создать фильтры которые могут пропустить конкретные предупреждения.

#### **4\. Сбор объемов по элементам**

 данная задача собирает объем элементов по заданным фильтрам. Также можно изменить количественные показатели.

#### **5\. Сбор объемов по помещениям**

 данная задача собирает объемы помещений по заданным фильтрам. Также можно изменить количественный показатель.

#### **6\. Экспорт**

задача добавляет в сценарий экспорт в форматы NWC и IFC.   
NWC экспортирует выбранные модели в формат NWC в указанную директорию, с использованием текущих настроек экспорта. Экспорт происходит с вида "Navisworks". Если в файле нет вида Navisworks, то экспорт происходит с первого попавшегося вида, содержащего слово "Navisworks". Если в файле нет подходящих видом, то происходит экспорт всей модели.  
IFC экспортирует выбранные модели в формат IFC в указанную директорию.

#### **7\. Код по локации**

 задача позволяет задать сформированное значение целевому параметру элемента, попадающего внутрь формообразующей. Значение формируется из значений параметров формообразующей. Для каждого параметра формообразующей можно добавить префикс и суффикс. Суффикс имеет ограниченную длину в один символ и не задается для последнего параметра.

#### **8\. Нарезка квартир**

 задача позволяет создать нарезки квартир по формообразующим с параметрами кода, самого кода, префиксов и пути сохранений. Также можно экспортировать в NWC.

### Запуск и логи

После настройки запуска нажмите “СТАРТ” (см. 1). В указанное время плагин начнет поочередно открывать выбранные модели и совершать над ними указанные задачи. Не закрывайте инструмент и не выключайте компьютер до завершения процесса. Для моментального выполнения процесса можете нажать кнопку “Запустить задание” во вкладке “Задания” (см. 2).

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXddox0gY92kPAYH3EtItK44np8gPI7fZVO72whj7N5T7bY29AvjFMMFZKf6X3l0JwKxfOqFJWan0bx-ERTXS9bTbaa7f7QT3eNhfZp3C5uSi4_gdR_m_CBccgZ2XTV4VruRoILd0w?key=yp7HKceSXo588Q-RfsVx8Q)

Процесс работы плагина можно наблюдать в окне “Лог”. Его можно посмотреть как в окне заданий во вкладке “Лог” (см. 1), так и в основных вкладках (см. 2).

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdlJnP1HRcLPGWjbO3NqNBcn2potAZ1k1_60GOF7BoNXrMuLrKLKVJg6lUGeNEkf9qfNCYacQ65rz0ak6qebExG2cC2EKEw50qPY-DC3Vq8Yk_sBIt6W1zPUF7YcTnNtyjPzf3esQ?key=yp7HKceSXo588Q-RfsVx8Q)

В основной вкладке “Лог” будут показаны события всех заданий, в то время как в окне конкретного задания будет показан лог этого задания.

Основное окно “Лог” с журналом событий

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdqX4OtkNxoQhvcFZyhRjoNFxgtk8wlFEJ6uLFMWDpyC6-BMOXWONZKQtUauC-02KYNvdnhTwTeFBNj9PXWFnN3NsRQzTKrqnaY2Mb4Gx8pUcZ73ukda8yhfpOHROY4VSmGM7QfzA?key=yp7HKceSXo588Q-RfsVx8Q)

Здесь будут записываться все результаты выполненных действий, а также ошибки, возникшие в процессе серверной обработки. Результаты можно открыть в формате .txt, нажав на 

![image-1697535359721.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdbsmIgEHBxhh5VosbLlDoVmRZ2DzX3uED3A46ukilMhHMOi_G1R5EFlP8jhHR-rhCvZIARq7A-PHQftrBnQRdhSGbc9UoGAoCdXn7JxP01DnualqyRhM4EWMDrOJP1_zkqZyqfVw?key=yp7HKceSXo588Q-RfsVx8Q)

и сохранить на локальный компьютер.

## Нарезка квартир

*Инструмент помогает создавать 3D -модели квартир для их дальнейшей передачи клиенту.* 

*Подготовьте формообразующие фигуры в отдельном файле, установите параметры для квартир, загрузите их как связь в основные файлы и нарежьте квартиры с помощью данного плагина.*

### Подготовка

#### Создание формообразующих

Для того чтобы использовать утилиту “Нарезка квартир” заранее создайте файл где будут расположены формообразующие(системное семейство: формы), использующиеся для разметки квартир.

В подготовительном файле формообразующих  используйте связь файла архитектуры (или другого раздела) как подложку, чтобы с помощью неё разметить формы квартир. Сами формообразующие создаются через вкладку Формы и генплан, нажав на кнопку Форма в контексте.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdhx1Xn-cOdFiTlBq5ujHH28bQXKi6LvJ3tIIT0Dy6W3pZ1iyGACSJBXwUEm786_5ot_ZekRZVXnWTr0JFgIOWAQgfscLxicA57Wlq4A7L5fgYgOC0nOrwrPgQqPfCvMhowjo-N?key=YKT5IiDW3PatwqeGKkX1_w)

#### Создание параметра

Для работы с утилитой, в файле формообразующих необходимо установить параметр с кодами квартир, он нужен для определения самих формообразующих при работе с плагином, а также в этот параметр будет вписываться коды квартир

Для создания параметра квартир, нужно зайти в раздел Управление и нажать на кнопку Общие параметры.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXckOjsmtk2qBq06ehAnQHtIVlm2FtiweSHqKd6WMdrfq_XUQLdKU2CAKunBbgrgpMw-PCa9wqVznKK7oAYKcis5r9MixMnnXNM4vTnDyb2WxTQQKVmQXF5CrrBPKj3L0vhorD7QRg?key=YKT5IiDW3PatwqeGKkX1_w)

После чего по порядку создайте файл, в него создайте группу, а в группу создайте параметр.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfDb_v7Mb14a26uNvJSlS-XjUGYswYWOP87P46zlAQMMSCc_NzQVC675lmsVKXpPl9IHeG-9ICXCzYgZXhNtXRl_3GhlOziGRKthdGamECrvgO9nfCkEw9S285TQdOfka3WAhYxbA?key=YKT5IiDW3PatwqeGKkX1_w)

Параметр можете назвать как угодно, он должен быть с типом параметр - текст, в случае примера параметр называется “Параметр\_квартир”. После создания, зайдите в Параметры проекта (иконка выше от Общих Параметров).

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeLhCHsvdJ2oPFYV6vgbYrdli-LPLrugbPgWSYgJrRbVd_zRPUSHDXseUFuiUg7nJFAM-qsiNSy4mUZEHh710rK_oypYL1N140eOGKJOp9uCDrDq7GwVdDNvZ8igv7_HYlOWsvVTg?key=YKT5IiDW3PatwqeGKkX1_w)

В окне Параметров проекта, нажмите кнопку Создания. После чего откроется окно редактирования свойств параметра.

В окне Свойства параметра, в графе Тип параметра выберите кнопку Общий параметр и загрузите ранее созданный “Параметр\_квартир”. В данные параметра ничего уже заполнять не нужно, для удобства можете выбрать в Группирование параметров его расположение (опционально). Дайте этому параметру свойство Экземпляра и самое главное присвойте ему категорию Формы. После чего нажмите ОК. (При успешном добавлении, параметр будет в списках доступных)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc000N1YcKcJnmBZiiJ27JhiRy6IWMtqr0F_wrXnuw7qAPNueQxDfBYFIPAqBd45YNsJ5T1uxKcn_Rh0uFs-GFslPm68q40Zbv8NF273its-m1Vllm13nfnBInw4PseGKvDe1LLGw?key=YKT5IiDW3PatwqeGKkX1_w)

После создания “Параметра\_квартир” в семействе Формы, он появится в его Свойствах.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf1SUT-VmL07FWyiyr_UF1VRhkhX-83bHS-9IpNmk42ZVnO46-RVIEXbHrOL6b1FLO6O1uS85ZZ6jKE5bKyG9lV-46kSH2-18TiJt9qzeCkqqOpesb2JvcZDjGI61V-QrY48tFS9A?key=YKT5IiDW3PatwqeGKkX1_w)

Установите в этот параметр необходимые вам коды квартир, например 1-2, 1-3 и т.д. В будущем это пригодится для определения квартир которые нужно нарезать.

### Нарезка квартир

Для вызова утилиты, нажмите во вкладке SIGNAL PRO в категории Утилиты -  “Нарезка квартир” (ВАЖНО: Утилита открывается только в 3D-виде). Эту утилиту нужно вызывать только в файле который вы хотите нарезать на квартиры (например: файл АР, ОВиК и ВК)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfEH2d9l_Z10DNlrlboLPtyBYbsdrwd0fChwfwKSrBv2Au6W29HUFIE_6Q06D170ryqD7b9yhrArUrBZ8tlEr1-4yUe8i0EEzPNBNCjcBUym1kPLnYGqb_Bv3pEAigsGGbJfuxycg?key=YKT5IiDW3PatwqeGKkX1_w)

После чего, вам откроется окно утилиты.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdgdOuKdSNhz1pTksgfclViwO7g6UCNAEtSqdhZtDUmQD2X5WOr1ip4v8cI-8A60VBmX1GkMM7plDjHLb9HsvzwVj1Cm5k5o-P-TAtoQJRFY752hKIa3looEo9wE1dfjSrAT8fy3Q?key=YKT5IiDW3PatwqeGKkX1_w)

 В графу “Параметр с кодами квартир”, как упоминалось ранее, мы вписываем подготовленный параметр (в примере это “Параметр\_квартир”). Это укажет плагину на нужные формообразующие с указанным атрибутом.

 В графу “Коды квартир” мы указываем все нужные нам квартиры, которые мы определили в атрибуте “Параметр\_квартир”. (Например: 1-1, 1-2 и т.д.).

 В графу “Префикс файлов” записываем любой удобный вам текст для наименования созданного файла квартир. По умолчанию, программа выбирает наименование открытого файла.

 Путь сохранения файлов - это путь куда будут сохранены будущие файлы квартир.

 Экспортировать в NWC - эта функция позволяет экспортировать файлы в формат Navisworks. Удобно для сборки разных связей, по типу АР и ВК в единое целое. (ВАЖНО: при экспорте в формат NWC, файлы в формате RVT не будут созданы).

### Сборка квартир в Navisworks

> Экспорт в Navisworks представляет из себя множество файлов квартир, разных разделов. Открывать каждую будет трудоемко и не имеет смысла.
{.is-info}

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcDIMdfpbMyyAhtXMUIYHZAxOXIhI2Znm9scJyhPH1qa9wD51zV6D66SaifSJWISDOOIVFv53h9P27lT7ThSyszhu9hIh6x6UAxu_wjR8_XkCos86MDbJDAt0x8SgJ4jhWFG_is?key=YKT5IiDW3PatwqeGKkX1_w)

Для сборки полноценной модели квартиры со всеми разделами в одном файле, запустите в NWC в начале основной файл нарезанной квартиры (например АР).

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd8MNbiR0vwxIg6L_dCggARfG2k7kBf3pW1xeiX51fptUw2R6tn18asT3uGgsUxUD69UIySYmfWPPsl4zJ4Df9CDEfQj_Ohqy5DD_bKJqXMM0Ly0PBqTjBdt1Uz9SQNI9m1XcyxnQ?key=YKT5IiDW3PatwqeGKkX1_w)

После открытия файла, вы можете добавить активные связи других разделов через кнопку Добавить во вкладке Главная - Проект.

После чего, другой раздел нарезанной квартиры добавится в общую модель.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdPda5qBTptTRbjMajhegaRuLQPnZfiQO3yPWiVaA9zozRSZUhejLVBgii_HXoUtyyvzh4N-6toNWvGsGVotfczC1Zw0k-y23arAK0pGRBp41wocw33Lk_ez1VXOKZkY0xeiZ209Q?key=YKT5IiDW3PatwqeGKkX1_w)

Часть раздела ВК и КР отдельно.

Модель в общем виде после добавления активной связи.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdmpK2c6_erQSDNsSWwlUAbQ5ODLQQQmqADiKTz0sZ1WvHXE3-svmFYgXh-lOEgq2FH9wPIAh6ovD6hYF_hB5h6aj_Z83LGlPvNkgvzuOjGKsn-2NwBR_T7PZCASctrn81Hj9SA2w?key=YKT5IiDW3PatwqeGKkX1_w)

Так, в одну общую модель добавьте все остальные необходимые разделы, которые были сделаны с помощью плагина. Сохраните файл NWC как отдельную сборку, после чего нарезанная квартира будет готова для публикации.

### Простой просмотр в DOCS

При публикации файла NWC в SIGNAL DOCS, существует функция “Простого просмотра”. Нажмите на файл сборки в DOCS правой кнопкой мыши и выберите “Поделиться”.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcJVpSBr3bqMB4efRclXnKb5x4pXjNEtPGhtICn8uEfVrMxUqnbofxSrr1_5B6YysNPtjrf_5Gd-ga_uUOUbcWRPJKeG0DNhMLMeIYm5tO_Yx6fjQlJeOD1j5kU7GrhSfTZe_1QPg?key=YKT5IiDW3PatwqeGKkX1_w)

После чего вам откроется окно выбора. В котором нужно поставить Тип публикации - Простой просмотр.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc-EtT0ns_WARhmi7xjXbshHxJtmwF7ad9nJFWFAMyiDe8KkR_9-2SMTXLP4jnrVTwIkuh_5vYR4Nro178F2O9kMJWxSrISK_K0w1CAgu0ZkNcCDV2A_-2byRF0yM046wvt1iKHXA?key=YKT5IiDW3PatwqeGKkX1_w)

После чего будет доступна ссылка в том же окне. Перейдя по ней, пользователь независимо от наличия лицензии, мощности устройства и т.д. может просмотреть готовую сборку в более легкой версии.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXct-0qg9Eob3Op6KeiJ6XeMZ4SLAZFA3jB8mNGzTdxIhX9WxB8kwS1myY6gkbH0ZjT-mhjbbUo8AXgyjvkzlMOmM_hJkDmx1eMG9vPT-vzj6eaGO7WUd9jSsQZGzaxJXrQ8oEoJbA?key=YKT5IiDW3PatwqeGKkX1_w)

В этой облегченной версии визуализации, доступны несколько функций:

Линейка измерения, для замера расстояния между объектами, а также Наборы выбора, позволяющие выбрать как конструктивные элементы, так и инженерные сети.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeodR8kTcha29xPEdcRYjWA8kkFtGSPBrSbabsK7obRNMD38AVF1447a0iFtH22VLQbAn60gHX1OYiqBI24r_vTQcM3Ul3ei9tB3QAgI5ZksyikGqmbwtoysFCYr661qawGODnASA?key=YKT5IiDW3PatwqeGKkX1_w)

Также, в этой версии можно перейти в 2D-вид и воспользоваться всеми вышеперечисленными функциями.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXei49IXkhtCzWY8OI1BR4_r1Wqhe8XbvH2AEAU1DbE9Vl5LP7hqIsyvRp2ShJKRNI1n54BcxxRQzhAfED43qjJhhnECOASIUTE1WcniUXleH3wHQnQvkq_w82HAVYmuxfSPa32HbQ?key=YKT5IiDW3PatwqeGKkX1_w)

Данная функция будет удобна для клиентов не имеющих доступ к SIGNAL DOCS и она не требует мощных устройств, саму модель можно разместить на публичных сайтах. Так, пользователь может без проблем посмотреть квартиру и определенные системы в 3 и 2D-видах, при необходимости сделать замеры.
  
#
<sub>**[<   TOOLS FOR REVIT. Копирование элементов  ](/ru/tools/revit/copying)     **|**     [TOOLS FOR REVIT. Приемка   >](/ru/tools/revit/acceptance)**</sub>