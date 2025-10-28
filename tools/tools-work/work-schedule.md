---
title: Утилиты - График работ
description: 
published: true
date: 2025-09-21T12:28:00.317Z
tags: 
editor: markdown
dateCreated: 2025-06-27T11:43:38.262Z
---

### **График работ**

Комплексный инструмент, который позволяет создать график производства работ в виде диаграммы ганта при помощи удобного графического интерфейса, а также визуализировать построение модели по созданному графику

**_Общий алгоритм работы с инструментом:_**

-   Сначала на вкладке График работ необходимо создать или импортировать укрупненные виды работ из MS Project или Primavera в формате XML. Эти виды работ были предварительно согласованы в договоре и нужны для отслеживания даты начала детализированных работ.
-   Затем создайте или импортируйте детализированные виды работ, которые привязаны к элементам модели с помощью условий создания (см. подробнее [_условия создания видов работ_](https://wiki.sgnl.pro/app/page/1dhz_RYu3DczaEesG4yRQP9sK60FLyuz8SEMJI7nmX-w)). С помощью этих видов работ будет составлен Сетевой график.
-   Откройте Календарь и настройте рабочие и выходные дни в соответствии с производственным календарем на объекте.
-   Перейдите во вкладку Сетевого графика и с помощью узлов создайте сетевой график. Укрупненные работы являются начальным узлами и служат как отправная точка для детализированных работ. Перетаскивайте узлы с работами в область сетевого графика и последовательно соединяйте их, указывая длительность работ. При необходимости можно добавлять смещения по дням, например, для затвердения бетона.
-   Когда Сетевой график будет готов вернитесь в График работ и нажмите "Применить Сетевой график". Таким образом, внизу будет построена диаграмма Ганта по детализированным видам работ.  
    Данный график можно визуализировать в модели

**_ВКЛАДКА ГРАФИК РАБОТ_**

![image-1688990900060.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcJqK-F1voFMD32iU9cnn9bM46LxQRdps1x0F5WVipJeKExHWBwK79cS4q6BT-WLhAw6SKOBR5EkBwIzU7Y1NG0TEjW0yv9wQa3LpxkVYIqiqR1HLc4FiaZm6f3yfbWGH8CPB6UNBzbb-OKtRQh?key=cARGhuBZ11N3r9azo6cjFA)

-   В верхней части находятся укрупненные работы, которые были согласованы в договоре генерального подряда, и диаграмма ганта для укрупненных работ. Данные работы нужны, чтобы привязать к ним детализированные работы
-   В нижней части находятся детализированные виды работ с привязкой к элементам и диаграмма Ганта для этих работ. На основе этих работ будет построен сетевой график, по которому в свою очередь будет построена диаграмма Ганта

**Создание укрупненных работ**

_Способ 1 - Ручное создание_

1\. Нажмите “Добавить папку” на верхней панели, чтобы создать папку для укрупненных работ. Кнопка, расположенная в контекстном меню, создает папку в папке.

![image-1688991151922.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXet2Gn-V1ut_3IAlqrgN5lq9YNVq6f62YO3SAc1KGiV4tOD5wGFk6MhA-cYXui23Vj17Zdkq4I-57H7nwP6BXJGJ6xuGZBshtaXldeYm_-k4lRVbK51_QBdnkfCoky9nz_MWnarGo1Rq_qHc2GN?key=cARGhuBZ11N3r9azo6cjFA)

2\. Нажмите “Добавить укрупненную работу” на верхней панели, чтобы создать укрупненную работу. Кнопка, расположенная в контекстном меню, создает укрупненную работу внутри папки

![image-1688991166374.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcelX0xV8Pzs8mb8wQzN9DSHD9u0_iAM14kDsAvsBZKk1GkWssoZFJhb0E8q4TKZL9kWaatsGkI2OpH-s11-qd8d5EiWTFc0y456iBNBKbhZz2EiZ5JK4VKqWWReu-bxiyofNnnZIHIbIxbhh2-?key=cARGhuBZ11N3r9azo6cjFA)

3\. Укажите Начало, Окончание и Длительность работы ➤ укрупненная работа отобразится на диаграмме Ганта.

![image-1688991182948.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXctjMVtTGqyjyQCxz-vk7UvHKh7a9qBPBZVD-Dzjd4N4l8WVdObbNQadSxCH_MWoKtsk0_IsCgF3NJDL4ic145LWDnb1IV3whx5NHHe1hCy38guWNZa_Xg-hULs-Qz1ceGV8HcSCfX1p8sLQ1wJEw?key=cARGhuBZ11N3r9azo6cjFA)

_Способ 2. - Импорт укрупненных работ_

“Импорт укрупненных работ” позволяет импортировать укрупненные работы с привязанными датами из MS Project или Primavera в формате XML

![image-1688991218770.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXciTaKoIuBj3wX-JAO3FoNNyGe1xJISHYos4zDjRWdcSu1v7r-UHmJF6LmuPl5Bq5Cl4-taZRS8J0N8a0tsbzcVB0HlklyFLO0GVCK7yNUTNVrwYNCfysVR5fUuKSDIVz_hLogcAizGtdDG8ZFz?key=cARGhuBZ11N3r9azo6cjFA)

**Создание детализированных работ**

Данные работы создаются в видах работ (см. [_Виды работ_](https://wiki.sgnl.pro/app/page/1dhz_RYu3DczaEesG4yRQP9sK60FLyuz8SEMJI7nmX-w)[_)_](https://wiki.sgnl.pro/link/127#bkmrk-work-type). На основе этих работ будет построен сетевой график, по которому в свою очередь будет построена диаграмма Ганта. Для возможности визуализации построения модели, а также для просмотра объема работ требуется указать условия создания для данных видов работ (см. [_Условия создания видов работ_](https://wiki.sgnl.pro/app/page/1dhz_RYu3DczaEesG4yRQP9sK60FLyuz8SEMJI7nmX-w))

**Календарь**

Благодаря гибкой настройке календаря, Вы можете выставить рабочие и выходные дни в соответствии с Вашим производственным графиком. Продолжительность работ зависит от рабочего графика, что означает, что продолжительность работы учитывает только рабочие дни.

![image-1688991584720.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdUrOW97G4GBMelpEPKUrPAfqlzDCI5pX1hZ3iQtYt0uctNNN4MlnwAy9MnE0vToFtSU1eLYBog5Y3mi02OFdaVEFLtoGQpN-q2g9ZSnuzWmBX8DPcHOjKEtM0DtIp4ZvnvA1tLzytE_A0v7HJxbQ?key=cARGhuBZ11N3r9azo6cjFA)

-   В поле "Рабочие дни" укажите количество рабочих дней в неделе для проекта и нажмите “Очистить”.
-   Для более гибкой настройки нажмите на дату в календаре, чтобы сделать день рабочим или выходным

**Визуализация**

Визуализация - это инструмент, который используется для создания временных линий, которые отображают последовательность возведения строительного объекта. Он позволяет пользователям визуализировать и анализировать изменения, происходящие в проекте на протяжении определенного периода времени.

Предварительно требуется создать поисковые наборы видов работ с помощью команды [_“Работы”_](https://wiki.sgnl.pro/app/page/1-B8HMIqIDN4CnwWo3yZXYVBYlf7Lq4anPwmk5eLtGXw).

1\. Нажмите “Визуализация” и в открывшемся окне отметьте галочками работы, которые вы хотите визуализировать. Затем нажмите “Принять”.

![image-1688991696209.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfoNKcqH4SHdwit4oQo7qG16ToLMbtkpHT04sojAY0y-RX0Bg6bbDXQi5POmHO-31FiTgb8UkLM-dOwCLkvhGYmp28f61fR3pDytCiveWlFBzO25WUUvjREFKyxO7JlD_efJAxQ4ob3CcBw_-t5OQ?key=cARGhuBZ11N3r9azo6cjFA)

2\. Откроется окно визуализации. Выберите дату начала визуализации и вариант шага (День; Неделя; Месяц; Дата окончания - переключение следующего шага идет по датам окончания работ).

![image-1688991711529.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd-KaYK8p4w5AHv95UILud4jv7VenestzciT52N0_OgXimG2xrL7ASMV2IMh-fpUV6xC58_YF3wT0uTjj87_8OZBbHmUIaRa5RN0LJVV62830W3I2psliTn93TaICVicyBj_hi9MuCi7oS8Vr7g?key=cARGhuBZ11N3r9azo6cjFA)

-   Выберите дату начала визуализации
-   Выберите вариант шага: День; Неделя; Месяц; Дата окончания - переключение следующего шага идет по датам окончания работ. Отчетный период в Календаре определяет, какие дни будут отображаться при визуализации с вариантом шага Неделя.

![image-1688991729487.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXelChXnUvXEIUU6xZ4X0zfHfN9wbGpdUxu0zX-sBnHouStDG0yhWbm7j8g-s7MOo-kHpqGAUyikefJLbQxy7jfLMiNtI9s_RbHpXVRYc15u_RnJA3JqbCZePbE-wHgdW4XkuAxWhIIn1vgQE7d0?key=cARGhuBZ11N3r9azo6cjFA)

-   Запустите визуализацию

**_ВКЛАДКА СЕТЕВОЙ ГРАФИК_**

Сетевой график позволяет планировать сроки и очередность строительства объекта с помощью узлов с привязкой к укрупненным работам. По узлам видно четкую последовательность работ с их продолжительностью, что упрощает создание диаграммы Ганта.

Узлы - это объекты, содержащие виды работ, которые соединяются между собой для формирования последовательности строительства объекта.

**Создание узлов**

Окно сетевого графика разделено на три части: слева вверху Укрупненные работы, слева внизу детализированные работы и справа рабочая область с узлами.

![image-1688991824499.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfYeMjUBjh_Z4hgRXwKzRz4q5HCiMeIsXEf2Z-8RUbTSWd4gjnGp3UMTpS8Zti9LvCFjzodzP_mMtm9su34LvBoOsrZObuzv1fEGQ97N6CqiJyqyxahRz7pyMUH9csGscEOlEacc0gLkuVXqbNdZQ?key=cARGhuBZ11N3r9azo6cjFA)

1\. Перетащите укрупненную работу в рабочую область

![image-1688991842062.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcGOGz-xQPY25tKXJTzdIy1Qhge4GC90HU1sPL6GtpvHY8Es7YXAgWdWyeOyXZlRsA6-wFAC3U1vx81K2fcgQCQf5FkYXVwJup3AQQLiDG2QgLlINzP0H5TSMfJ0guPexHSTh6Uy1aimVH5O7Q2ag?key=cARGhuBZ11N3r9azo6cjFA)

Будет создан узел с укрупненной работой. Этот узел показывает и задает дату начала работ, например, начало монтажа монолита выше нуля. Данная дата начала работы взята из укрупненных работ, которые Вы ранее импортировали во вкладке График работ

![image-1688991851484.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXelFeeVxFSDsZAYFhRqgOWX_pDzbFs5kvKXaSI5pqc4aq8iWa6q4JO93ahYGQeY1X1vGtbUF6wyX4lJz4eW7DflNC3Dei3Q8XjmjDZtOGc5a2JnbgH0T43sAhbySen-7F6xOOkkssnPO-kB4NdcUw?key=cARGhuBZ11N3r9azo6cjFA)

Если необходимо построить график работ по одному виду работ, например, только Монолит или только Кладка, то можно использовать узел “Начало работ”. Данный узел не привязан к укрупненным работам и всегда находится в рабочей области. Укажите дату начала работ.

![image-1691673118291.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf1EO8uD5YJXsKTcD-F_c-KdlsOnn2vWflhIWtzesQTlGhHs4_724z3Bqzs-t_xOANxhxpS-ivHr-AZ9HZRsssOJDCM3tQlK427gvvP0BG45saHjG97Whf2L1PKIu4g4XZx5tD5r2t2InTJaF1z?key=cARGhuBZ11N3r9azo6cjFA)

2\. Перетащите детализированную работу в рабочую область

![image-1688992224034.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd-5aiCg5LR_gSMSYveRcTVZ_cSC5brhRkO7SYs2LYspCLDYWEfnZwjoT_e-OKC0h86bBwbY9V1vpDJ4GAmKHc7GtJZgm9uLPTf-dXYSYSaF8LoUmE6qntAcQ7y0G9W6nGIEbv3ldc_Uq7vwf0wWA?key=cARGhuBZ11N3r9azo6cjFA)

Будет создан узел с детализированной работой. Данный узел получает на вход дату начала работы, прибавляет к ней длительность работы и на выходе выдает дату окончания работы.

![image-1688991864435.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfRX0FyBm_wmJSvdLKxdHKkh6-dTbriSVuDdRwORDGqhXuWzJWX6SNkHzCYaKv0vRq60liFUx36oJcSqRW6VkRdFKCI8ue9c_WKmkmYBiXIHGhAgVgng2707hvcjwPii3FE0vFwmX2zCZK6HOf9mA?key=cARGhuBZ11N3r9azo6cjFA)

-   Заполните “Код работы”, например, 4.1.1
-   Укажите “Код локации”, например, L01
-   Укажите длительность работы и единицы измерения
-   Набор нужен для отслеживания объема работы по условиям создания (см. пункт Объемы работ)

3\. Соедините узел укрупненной работы с узлом детализированной работы. Для этого наведите на выход укрупненной работы, зажмите ЛКМ и перетащите связь до входа детализированной работы. Таким образом, узел с детализированной работой получит на вход дату начала работы.

![image-1688991882924.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf4jIe9z0KG3BAptP-0JpH9bP8N01J05yPnpLcWZTl5Lm7p2LwkDFhaqNIdnEKIfCjWMmtkxdv8o1QXIH_dkiMPNIdMp67o4bdksXwNuW6CkQ4Esj9JJFjVvrO5SOoAixCW5XyuUyY387XBPT-yWQ?key=cARGhuBZ11N3r9azo6cjFA)

Затем соедините детализированную работу со следующей детализированной работой и т.д. Таким образом, на примере получим, что монтаж стен третьего этажа начнется после того как закончиться монтаж перекрытий второго этажа длительностью 5 дней.

![image-1688991897099.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc6DPnuQhr5ZUOdPM-h3G8wvKLjrBnQF4UFEgKux-rdsH-2SpwPGcqZn_zJadBrak605dBwAFZcxfcN9Hm_EV61JPXMDOhnXEC8JCNdB0QjXpTs3BFJCaNpTWmjtXAMin2nKYYeZfxFT0FdfpiP?key=cARGhuBZ11N3r9azo6cjFA)

4\. При необходимости задайте смещение для начала следующей работы, например, чтобы следующая работа начиналась после набора прочности бетона.

Нажмите ПКМ в рабочей области ➤ Добавить смещение

![image-1688991923674.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXddH-Tc55CBS2GyDdYsOXUc81Hgz7ZBJdSmrvfskU3LexHegKR6Zif5V8E3gKllLYzYyB6xoXPnvh290ibhAfaRSmGapAj2EnWV1i6INYEneG7s3PCf-WUxDqxzcrKdXCJibnmjeWXIQNNQKvX4?key=cARGhuBZ11N3r9azo6cjFA)

Смещение получает на вход дату окончания работы, прибавляет к ней смещение по календарным дням и на выход выдает дату начала следующей работы.

Задайте смещение и соедините ее с работами

![image-1688991936544.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfhRVTgYbJSOL6Hfr8UaeRmdzvtG5PxJH7UEkTbpNM516B3Zz3eWgxEzElwapP91O1RLfuW2EXFzxKhoJAQ9cYLO-Rr8SHi23g5Z511CMBISyR_gM_MR9Pf41gpr5hYk12KeNke1Agezop1nVcmlQ?key=cARGhuBZ11N3r9azo6cjFA)

5\. Также имеется возможность создать свой узел, который не будет связан с видами работ в панели SIGNAL и не будет учитываться в подсчете объемов, но необходим для учета работ при построении графика работ.

Нажмите ПКМ в рабочей области ➤ Добавить новый узел

![image-1688991965322.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf0GpiqX72bgPLKNw28-eRt6Oxa5kTgj0fWZ0FjdFd6gmYb5f9M0xfm6BiDkdDwJjBKTgKBfSHEjlDS6uN7dL6EA15PxzJO7H2wwGSXOUSXmUE5fiR_2y6GzQGHixvTxukMygzDcvFbfYSPAJjr?key=cARGhuBZ11N3r9azo6cjFA)

Данный узел не показывает объемы, т.к. работа не указана в панели SIGNAL и у него невозможно указать условия создания.

6\. На выход к одному узлу можно подсоединить несколько работ, например, чтобы задать параллельный монтаж фасадов здания

![image-1688991948948.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfQIklgHBFqZrV2OO0Zhl5vwtiUwKev6wSkf6XpkAfoI-fZZ4qCI16jR42GuYQvy4tCCKrSlefA8qWHnFK-EafZyXFMdbD7pcijb0CPh9nI6-V27c9916-iMe8RycgNGUYAhl3AOXwVRARDbF-GbQ?key=cARGhuBZ11N3r9azo6cjFA)

-   На вход к одному узлу можно подать несколько работ. Тогда работа будет начинаться по наиболее поздней дате окончания присоединенных работ.

7\. Продолжайте соединять работы друг за другом как они должны идти на строительной площадке, указывая продолжительность работ и по необходимости смещения по времени.

8\. После завершения построения сетевого графика перейдите на вкладку “График работ” и нажмите “Применить сетевой график”. Таким образом, по данным из сетевого графика будет построена диаграмма Ганта для уточненных работ

![image-1688991984709.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeOX8orA29k515ryJd9jVtzDkah7G4Q1d-eEeawhDlUn40wxCtdH9vxq86jneV_HacNq90-kw_O1nGIf_1QbJoJiXNo4pjSWvAfjiKpFCiWHwfO3kPFegF9z9CdEqCuyAl1g7K7GR3W5tbyR3mJ?key=cARGhuBZ11N3r9azo6cjFA)

**Объемы работ**

Для определения объема работ необходимо в панели SIGNAL в видах работ заполнить условия создания видов работ (см. Условия создания).

1\. На вкладке Сетевой график нажмите “ИМПОРТ ПН”

![image-1689000414241.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf5vOQHZI6BbfQRD5xZWskVVAV3ipo6u25KjEbT52mnXCLC9e70nk-Ax5ebMjIvl8PHe5p_ojPRXBxcOBxLSKzUg3DZxdh-C1XP8YE-DqKbRgugdcioXrEemKNRW8c2twuYBfeVIAYYsHf_KA3n?key=cARGhuBZ11N3r9azo6cjFA)

2\. На узлах появятся объемы работ и соответствующие статусы:

![image-1689000426138.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcSwBMNF4E757kyBaFjikQjDY3UwB44QVmTinYYxs3Wsbh-Ypbo70-uIgb0lKh8du1Hfit4D7uUjG32rg3I-ZtgS5FotqLMkWE5NHR3ms35iR8F3Ilp0fEllg8WqZwyRh7dgP_1oFAXVm2og-1IfQ?key=cARGhuBZ11N3r9azo6cjFA)

-    ПН найден в текущем проекте. Данный вид работ присутствует в видах работ в панели SIGNAL и у него корректно заполнены условия создания.
-    ПН найден в текущем проекте, но объем равен 0. Данный вид работ присутствует в видах работ в панели SIGNAL, но у него у некорректно заполнены или вовсе отсутствуют условия создания.
-    [](https://wiki.sgnl.pro/uploads/images/gallery/2023-07/image-1689000452549.png)ПН не найден в текущем объекте. Данный вид работ отсутствует в видах работ в панели SIGNAL, а создан исключительно в графике работ.

**Пакетное редактирование узлов**

Пакетное редактирование узлов позволяет задать единицы измерения и длительность сразу для нескольких узлов.

Нажмите 

![image-1689000474365.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXemI0sCKUbdN2jkwT5-yCWYa5GJXR7XXZ3I8sI7Oz5PlUEMno4iaJyIdpkplLwOCXCb0ZXaxG4gwGl49NDYIGv0t9OSfIYNF77QqlGleL5w_Oo3v3q9pE5QB359blnKNL4F34iPFt5TU7tXMabVMA?key=cARGhuBZ11N3r9azo6cjFA)

 в правой части рабочей области сетевого графика

Окно пакетного редактирования узлов

![image-1689000487068.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfWCECgw7FHNSYRBnB56mGSFNBo2FQDnw-HNjSQnN2MHEzQ3FeMpv1wMabYc9-cT9dn3QwXYpYj0yWPH1lpPMSGGlABb6kJmx3Ys8vHsruOZcJ0KXVM4R3DY8rsTnGVBOKeeRw3-YCZbkUwMA4Gvg?key=cARGhuBZ11N3r9azo6cjFA)

-   В списке выберите узлы, необходимые для редактирования.
-   Снизу в строке “Единицы измерения” выберите единицы измерения, которые требуется присвоить выбранным узлам, и нажмите   
     
-   Снизу в строке “Длительность” укажите длительность, которую требуется присвоить выбранным узлам, и нажмите  
     

**Импорт и экспорт узлов**

![image-1689000560353.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcFKGbOVq4hoymc8v268z_Rp7X7nJE1GbmpNSKxC7P7xyuCUl449kRC9NXQ8kVdKVehx7eaOZA0hNvgb4e6DgvYIAhdVIaC3zJtqqJPJKI09xuJHBdsHxLzdYQXCgW-hKdH-8K5oudEZbJJ6p-mkw?key=cARGhuBZ11N3r9azo6cjFA)

1\. Для экспорта узлов в формате XML нажмите "ЭКСПОРТ". Данные узлы можно отправить своим коллегам.

2\. Для импорта узлов нажмите "ИМПОРТ"

3\. Для экспорта определенных узлов выберите данные узлы и нажмите 

![image-1689000594265.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf6Qhdi_eyV0o5Vje8qDMAYge6D5u3_pLgnOODfurtEKJE3ofS093-x7qD6-j6ltZh_cgxb2GSwjimZB51EpS4Vd-nQzzLkIlxVxfLDLAuXYIRleaDX0oqr2e9ptnasQfkK3MJjR57Vc_EgYqpc?key=cARGhuBZ11N3r9azo6cjFA)

 в правой части рабочей области

**Выравнивание узлов**

Используйте инструменты выравнивания для того, чтобы выровнять узлы по вертикали или горизонтали.

Выберите узлы и нажмите одну из кнопок в правой части рабочей области:

-    Выровнять по левой грани узлов
-    Выровнять по правой грани узлов
-    Выровнять по верхней грани узлов
-    Выровнять по нижней грани узлов

**Создание ПН Planned**

Инструмент создает поисковые наборы Planned по планируемым датам завершения работ, благодаря чему данную модель можно подгрузить в карточки “План-Факт” модуля DASHBOARD как модель с плановыми работами.

Предварительно требуется создать поисковые наборы видов работ с помощью команды [_“Работы”_](https://wiki.sgnl.pro/app/page/1-B8HMIqIDN4CnwWo3yZXYVBYlf7Lq4anPwmk5eLtGXw)

1\. Нажмите “Создать ПН”

![image-1690894185752.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdqBKZY_t_OB93QATekiHRsmfxl9ktpdk0LW02SNVrI84keCZ6UMZKiNjVLa2XndVuLtRH2oHM7Ne0MX7Req1SrtE_1EFRvDV85cYBpgXfbmCjik045VzkTH3oPXwj7gSnBGMG8ElLtgb1hsHal3A?key=cARGhuBZ11N3r9azo6cjFA)

2\. В элементах во вкладке “SIGNAL” будет создано свойство Planned. По этому свойству в панели “Наборы” будут созданы соответствующие поисковые наборы с плановыми датами. Данную модель можно будет использовать как плановую модель для карточек [_“План-Факт”_](https://wiki.sgnl.pro/books/32-dashboard) модуля DASHBOARD

![image-1690894475789.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeiy2iNgTXxZ7TaSauRFM7KL51QLg5DCMKHXUqeJ32OvOJNo0io4R9_QABvqlcRHr4kl6j6rx3nR4adG8kcTR1HVKfdATXKu4SQQw95A1nxajHtY9VmewXPPzjrbn_5yw0jLLLmtNXZaPi2zrrH4Q?key=cARGhuBZ11N3r9azo6cjFA)

![image-1689000621217.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfvLOKuBxsc4dPsquovWtoweGrvsAE8p_BI6dmANxF2R3G-sBq4f0pZlrJseneEsG0ofnK9LWGgPOIdm1bHd8-7eNipS-cTcVHYK43Wm61q7bfezfT20dIWSPMyUZc5yN-XyzZKgJ3trmmQMomjrg?key=cARGhuBZ11N3r9azo6cjFA)

![image-1689000616051.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdl7RP6OGocIa6Tk4xDcQpOxsnl8iGxQZIDL4FuK1QkePnFoa9TLUcZt8s4GsoM4B3l_PHyTLAy57-DQZzdXHzURRxdRrmGzXMvT92U2N1ucJCSLykmJpuDPd4iK7lWPanRF0DI2YwokqjYP_2pVg?key=cARGhuBZ11N3r9azo6cjFA)

![image-1689000610153.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXctj5K0PIM53OGCTP5jXgdgJIGb2buKH9SKDoWieeTsfFIj7tlSePGE2jSSkq54Q7zTR0vj-2AcYkJzhvu6p-ckahdDJoc_p7chzzo1moSXalTO1Y9X2jIjyvq_5DH0mwssDkDzt1qvwjTvcc6peQ?key=cARGhuBZ11N3r9azo6cjFA)

![image-1689000605262.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe5iPzBnbEsJd9VYqyTg8B7ip_Ez5g3giFru6hJ-YNXHVCssbEEuFlpMb7acawkmZ46IcQVuXI5jTQA7-10iVJZ2aoGtrPAuBYhLpNweKayvLQ4SmJkUw3UFp1z0l2zOy99xvHyywfBxpdm5_y7jw?key=cARGhuBZ11N3r9azo6cjFA)

![image-1689000536383.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdz6dRuSI7OyUe8dw8m0JNhIl-rstpQ-ZvPoHEVzlgensifFTF98Xy77xYlCEHTcSCfoE-N0-cWcdK46Ee1nxXbHANAJ8UQZn6GNWx3By2BhfTQti3Rq6Vgc64B8ubs4qSp9HKFYIR5IAZztKuw2Q?key=cARGhuBZ11N3r9azo6cjFA)

![image-1689000524338.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfxifmpJxXZT2XFlTOU71R0RsouPQTYfMRF_rbZ8trqA8Fv6YQWUtbgmq0KpjEyL5MYQpfMZHdXFaYbbNCwrWAtAJQbx0kPrPZm36gB6CLhmzTMjCBWRRhEsk0IINJCbsrI-gKAU1xuSEg4eLUseg?key=cARGhuBZ11N3r9azo6cjFA)

![image-1689000452549.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcDlTAXHR_EsDtbtIfDfzGJm0Qk5CdGB4Ezy8YZHvDiYZ_XxUwqIKnOlcAbsnbGLvPl2OrDE9Sif2dXIGxcr3HgWjvlKCd5gAS44rHJl41-cpZS5AvO0Sp2xoqvS0OuReOH5HVmIVC2c-CPQ_jC-A?key=cARGhuBZ11N3r9azo6cjFA)

![image-1689000445919.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfto2KE3IE3stuukx5sFpIPWTbE3tR8wgQvryA2dHOK6Vst2Lt-keq6Ij0ip0-ENgendai6KNtaNDeMi7w4yV7onWmj_Gj2NdsnPVJ5ttXhumfskvA4nGLcbqHp_4b29JF-JrPyL5l1gBVgAGzU9Q?key=cARGhuBZ11N3r9azo6cjFA)

![image-1689000437859.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeE7jBdb_Wj9MQ39MaEEbJA9h8Q2mHSQd6Mr7DJMstNKcU4JqFuAoY4tCE6f7pzzIZD5u-0Hl5AeZfRcxiEUViW-gcwrRudkSP0j8NUEhENR1_gnqYCX6hMk8rTBw5TWFWnob1JBpCItICWVCdH?key=cARGhuBZ11N3r9azo6cjFA)