---
title: Утилиты - Автообработка
description: 
published: true
date: 2025-09-21T13:17:57.028Z
tags: 
editor: markdown
dateCreated: 2025-06-27T12:08:34.267Z
---

### **Автообработка**

Инструмент помогает BIM специалистам автоматизировать процесс выгрузки и проверки Revit моделей, расположенных как на локальном компьютере, так и на Ревит-сервере. Плагин в указанное время без участия специалиста сохраняет RVT файлы в указанную директорию, выгружает их в форматы NWC и IFC, проверяет командой "Checker" и классифицирует модели с помощью “Код по условию”.

**Примечание:** Плагин можно запускать из любого Revit файла, даже из пустого. Версия обрабатываемых Revit файлов должна совпадать с версией Revit, с которого запускается плагин. Не закрывайте инструмент и не выключайте компьютер до завершения процесса Автообработки.

1\. Нажмите на панели Утилиты ➤ Автообработка

![image-1697535256664.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeXOIPlkmx7OkBpQf7GTzDuoaub9fvM-Kw5-PoGQfh53zjaZHza6M1MHNYZH3uic_YtfMNPidxkdqqQUTS4jqObTcwpQ9SjuMMmmBuGXIYI4fZoM-KKeMsUYtGlGEULvohu3fbRGlR4n2gP8dWd2g?key=eZQrGNoK3AtGdzk6p2pboQ)

2\. В окне "Задачи" нажмите + и добавьте действия, которые будут по порядку совершаться над выбранными файлами.

![image-1703066473403.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdtFcZP1MsvgY-a7foolMJE5ABfnnnYRCQicl0lL2hQZYlSL6MQb8oMn6-92upqiA3Nr2wdTB0VmKoKn3aYcrGnwTp_oUU43CIJ9K2LW_eNLDseyQg6jbuE6bidFSA-tvIjzBwmrcHvpjM9Ui1j?key=eZQrGNoK3AtGdzk6p2pboQ)

Порядок воспроизведения задач можно изменить, перетащив их.

![image-1703169272347.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdbuMbkr-4YLT9p5tVLfVJX7HjLn2HcfeOPZ1iNXNVE4H-lVcgYm-HpiX3smyzWwK3mPiyg5qE25dr4KnIPhSqm-FetmTxi9ObhYLFRwd92Ds9oT5kzwNu4NJZPA2-CVcfNLWef87H0QTbUPfub?key=eZQrGNoK3AtGdzk6p2pboQ)

-   [**_“Код по условию”_**](https://youneedawiki.com/app/page/13PMTPC2kgQs_xTyobyOCd3uWQ0S9rRwFUu5j82kj4TM) назначает код по классификатору всем элементам по определенным условиям. Правила берутся из файла, откуда запускается Автообработка

**Примечание**: Необходимо использовать эту задачу с отключенной опцией "Открывать файлы с отсоединением от центральной модели". В противном случае все изменения не сохранятся в исходном файле.

-   [**_“Checker”_**](https://youneedawiki.com/app/page/1oO30Ot53EHyk0JRDfJw8leG514l3mVeucYlNQJVVoUI) проверяет выбранные модели на наличие параметров в элементах и заполненность значений этих параметров. Итогом проверки служат Excel файлы с результатами проверок. Правила проверки берутся из файла, откуда запускается Автообработка. В инструменте [_"Checker"_](https://youneedawiki.com/app/page/1oO30Ot53EHyk0JRDfJw8leG514l3mVeucYlNQJVVoUI) необходимо поставить галочки напротив производимых проверок.
-   **“Сохранить в”** сохраняет выбранные файлы в формат RVT в указанную директорию. Для сохранения моделей с совместной работой рекомендуется использовать опцию "Открывать файлы с отсоединением от центральной модели".
-   **"Экспорт в NWC"** экспортирует выбранные модели в формат NWC в указанную директорию, с использованием текущих настроек экспорта. Экспорт происходит с вида "Navisworks". Если в файле нет вида Navisworks, то экспорт происходит с первого попавшегося вида, содержащего слово "Navisworks", например "BIM\_Navisworks" или "Navisworks КР". Если в файле нет подходящих видом, то происходит экспорт всей модели.
-   **"Экспорт в IFC"** экспортирует выбранные модели в формат IFC в указанную директорию.

**Примечание:** Директория для экспорта указывается в поле “Папка экспорта” внизу окна.

3\. В окне “Файлы” нажмите 

![image-1697535302085.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcOgViaPMesQsB_8zHqja4xgiLZSy8-DpFTYV3pPCAFG_IQZ9nid_K-TfupCwVUsysc2kNsk65wd5IK85YWzC5zE6cwsP3YgAVq36jk2TyKW2h0Sj0ya37FTFlYNDFcHtTyiloU3nb5z70uLfu5TA?key=eZQrGNoK3AtGdzk6p2pboQ)

, чтобы выбрать файлы формата RVT с локального компьютера, или 

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

**Примечание:** Данную опцию необходимо использовать только с командами экспорта, т.к. внесенные изменения командой “Код по условию” не будут сохранены в исходном файле.

-   **“Закрыть наборы”** позволяет закрыть указанные рабочие наборы при открытии обрабатываемого файла. Например, можно закрыть рабочий набор с связанными файлами, чтобы обрабатываемые модели открывались быстрее.  
     
-   В папке экспорта указывается директория для экспорта файлов.

![image-1703169511120.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc8fH3R5LCneIBfHZIqI-hL_m-7NBi_KLqCJaWOk6mxzOu2njrUkvx73CRW6WFSkY4S06gfXzwOMp3VGvRUKFU1he_StUlCX50tKFin47BiFhgeGWULMOtdcPYCF7WwLS2gmCFx4eioxBtFD3qB?key=eZQrGNoK3AtGdzk6p2pboQ)

5\. После настройки запуска нажмите “СТАРТ”. В указанное время плагин начнет поочередно открывать выбранные модели и совершать над ними указанные задачи. Не закрывайте инструмент и не выключайте компьютер до завершения процесса Автообработки.

![image-1703169440550.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcJMYDpvkK_w2T-_Hc__ZP2mUZPzVXXnH2aqSGzqS5bFUzbdPi3QqYUseF02JMRFxS5WDBX6ZxnvWN8Wf85abjNswwJgGf8y26Z2Fcvfu65a8athaSJuxEXD4wQ3JuH-xL42f51v018lBF8rKah1Q?key=eZQrGNoK3AtGdzk6p2pboQ)

Процесс работы плагина можно наблюдать в окне “Лог”. Здесь будут записываться все результаты выполненных действий, а также ошибки, возникшие в процессе автообработки. Результаты можно открыть в формате .txt, нажав 

![image-1697535359721.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfDlY84YvcamVOzx_s3g03uRB8RQtE3I-lS7U_jbCz6BWrQJlgmjMmbEJzrFPbOfob8RClr9hVKxc6Ac6c-5IRqt01wdveKF1zFhuTwv2E2-KfL5t0KGm5gxOf2EM6X6q0o7VLn5bbIPPMx-is5Dw?key=eZQrGNoK3AtGdzk6p2pboQ)

, и сохранить на локальный компьютер.

![image-1703169412943.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcU2XwqyTNVzdj0tgoC-d3HelgwTz2tTygcd2OqBRpitdpylg-XB5Q3HK35p97svlMxE9RB5V3IL1bca46CCmXLWBLl6cudEhf9_Sdu1yKqaGd1g7Vu-s_ESydv0h_PPiQCeHuys3r-d8py28zD?key=eZQrGNoK3AtGdzk6p2pboQ)