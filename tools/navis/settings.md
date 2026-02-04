---
title: TOOLS. Настройки
description: 
published: true
date: 2026-02-04T14:13:26.112Z
tags: tools
editor: markdown
dateCreated: 2025-09-21T11:03:08.040Z
---

<sub>**[<   TOOLS. Методология работы](/ru/tools/general/methodology)     **|**     [TOOLS FOR NAVIS. Панель    >](/ru/tools/navis/panel)**</sub>

---

# Вкладки{.tabset}
## Основные
Настройки плагина SIGNAL TOOLS for Navisworks находятся на панели Настройки ➤ Настройки

![image-1683797920357.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf8UlPG6Lb0z7W1pfkQUxpq2UrJ1kcn6wbcABLWx6JX1aN1mDM3iVANWROUv5-0Vb3W2RyGNIH0PhXBIE_SFD_rdFW-qfMlSbcHWuNy8IDIiNNrSaeX1kMvQLYQRcvFMXX85WaQGum4E5uo-oVx8A?key=RyU3QcfxdhVsnxrCcipjXw)

### Основные

Проверка лицензии выполняется при начале использования функционала плагина. Модуль TOOLS делится на TOOLS Lite и TOOLS PRO. TOOLS Lite поставляется вместе с DASHBOARD и автоматически подхватывает из него авторизацию. TOOLS PRO поставляется отдельно и имеет отдельную авторизацию.

Нажмите на панели Настройки ➤ Настройки ➤ Количественное свойство

![image-1683295534994.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfguj6hjaZrnye_htTmbw5lWMzbS_9Sx_oJ9HTJhN4KgyuZ-PBum_6Wko89Zt7RO92-wspLEDd-RMsX9VCdJNEjd1WGJ41I_uUh94EgEWqkdNO483n91mLl2v3Ih6okChNOBiYw7SVB4AxgZL4Ufw?key=RyU3QcfxdhVsnxrCcipjXw)

1.  Войдите под Вашей учетной записью.
2.  Экспорт настроек плагина в файл формата XML. Файл с настройками можно отправить коллегам, чтобы при работе с плагином они использовали один и те же настройки.
3.  Импорт настроек плагина в формате XML.

## Раскраска

Настройка позволяет указать цвета для раскраски элементов при использовании определенных команд.

Нажмите на панели Настройки ➤ Настройки ➤ Раскраски

![image-1683295598676.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcnSsjDCr-lrRQPg4lGFEvZG8orCvu8VznC-k76d02Oi26Ep1MnRUOQXmiuIcU9jtKrfLLFyUEzx-WGTG8Bpb6hQCdsU9AB_ebKt8hMd3DY6onxffnYPw43dEABoaYgvTVPlVkeRb5KDqyvZ1fpmQ?key=SG6Qvs8ywnM8DuZFDlvpbw)

-   В верхней части окна выберите из выпадающего списка цвета, которыми будут красится элементы, после выполнения определенных команд.

> ***Примечание:*** Для команд [_“Завершить”, “Принять” и “Запланировать”_](https://wiki.sgnl.pro/ru/tools/tools-work/approval-complete-accept-schedule) цвет будет задаваться в свойство SIGNAL-Color. Для команд  “Комментарий” и “Замечание” цвет будет задаваться в свойство SIGNAL - IssueColor.
{.is-info}


-   В нижней части окна представлены допустимые названия статусов замечаний (Issue) для файлов из DOCS. Для каждого цвета укажите через запятую название статусов. При импорте замечаний из DOCS командой [_“Из DOCS”_](https://wiki.sgnl.pro/ru/tools/tools-work/issues-from-docs) элементы будут окрашиваться в цвета указанных статусов.

> ***Примечание:*** Если какой-то статус не требует раскраски, просто удалите его из всех списков
{.is-info}

## Документы

В данной настройке указывается корневая папка c локальными документами. Из корневой папки можно привязывать папки и файлы к элементам модели через вкладку "Документы" в "Панели SIGNAL". При привязке документа путь будет скрыт и указан только путь после корневой папки.

Нажмите на панели Настройки ➤ Настройки ➤ Документы

![image-1683295699967.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdJf7XUn5JrTRM2WUlG91m6ubFzr0NRhKGpHn8YB5zMb_jCacBQM3JyFAW8c_9E0aPeaLWejvdp1ylGoLhaSD3cRBCpWwZy_0Q6P4-aK_kLZUPt3gGHlpLHxQ8XKsD1N8UmjK3RglEUodg1W4Nu_A?key=1DB8wO-NffGvbw4fprv9qQ)

-   Выберите путь к папке с документами, нажав "..."

***_Пример использования_***

После привязки к элементам всей необходимой документации, Вы можете отправить архив с документами и моделью в формате NWD другому Пользователю. Пользователь сохраняет архив на локальном компьютере или сервере, затем разархивирует его и указывает в модели новый путь к корневой папке. Таким образом, все документы подтянуться в модель.

## Количественное свойство

В текущем списке задаются пары “Категория-Свойство”, являющиеся критериями для сбора суммарных числовых характеристик элементов (Объем/Площадь/Длина/Вес) при работе с разделом [_"Расчеты"_](https://wiki.sgnl.pro/ru/tools/tools-work/calculation-valqw). Если у элемента имеется хотя бы одно свойство в указанной категории, то из этого свойства берется значение для подсчета. Порядок параметров в списке соответствует порядку поиска параметров у элемента.

1\. Нажмите на панели Настройки ➤ Настройки ➤ Количественное свойство

![image-1683298926292.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf3WWk4eM1IS3jg64b3plWuBOTi-gRmiPm0mXv2Tk24kaFFXS3pEq2oWy-XtmiTZ0E_taB1_sVF1Fh-rjsNPGuKjPvl0DF8U6M5vlej3JGabyHUVR8nIrKa3DpQT8wky5OJ2LUgZ5zAqYrLQzhs9A?key=k6iRdsF6jiaLjR-r1Qvtng)

-   Для добавления новой пары “Категория-Свойство” нажмите .
-   В строку “Категория” впишите название вкладки, в котором находится нужное свойство.
-   В строку “Свойство” впишите название свойства, откуда будет браться значение.
-   Третий столбец с коэффициентом служит для перевода между единицами измерения, например, м в км или кг в т.

> ***Важно:*** Названия должны вписываться точь-в-точь как прописано в панели свойств, с соблюдением заглавных букв, пробелов, дефисов и т.д., для того чтобы плагин мог найти данные категорию и свойство.
{.is-warning}


2\. При необходимости создайте собственные количественные свойства, которые можно использовать в качестве приведения к одним единицам измерения, например, м в км или кг в т. Для этого нажмите “Добавить” в правом верхнем углу.

![image-1683702212795.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfs1eZNR8-ibEVCL7SrSA0YCevGd5Z0vXsie3CGlsss15FBT1GKOZLCaRC3YymLxUmJCvTN0T00jb-pfhctcH1bVLJaJjYLfbjW2CM-uNrAkbz5L0ipO-271I733E-ONcu5Fk1CalxADb00cePsNA?key=k6iRdsF6jiaLjR-r1Qvtng)

-   Введите название количественного свойства и нажмите “ОК”

3\. Введите единицы измерения, пару “Категория-Свойство” и коэффициент для перевода из одной единицы измерения в другую.

![image-1683702236310.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdOOR0dFHBY9mrzglrRl8G1regai1BpBDL7AWLzCSkuhRMJ2ahsilu5pyMiUA17CSQZI4CPgpYFluyvgzOzg3EA3bxa9Vt0M0Bwj8h-9iMX03TAUnVwEOlBBEoVXxyz155ksEozUPMWOGSHa008Lw?key=k6iRdsF6jiaLjR-r1Qvtng)

4\. Закройте настройки, сохранив их в нижней части окна. Затем выделите необходимые элементы и с помощью команды [_"ПОЛЬЗ"_](https://wiki.sgnl.pro/ru/tools/tools-work/calculation-usage) на вкладке Расчеты посмотрите указанную числовую характеристику

![image-1683702248089.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd11gFZB8_eguhu1k-hhebk3ET_ViaUR_1yJ7vy7eNyK0Muc9A0MwA24RPEj-X5aR__Fhi_n9K5WT8tkj6-A2qASk1OfJja4hQJ9ZyU25Gd6lssodhtMMTwzZ4gk_SS5bQssmFsV9qxQmJVGdtS?key=k6iRdsF6jiaLjR-r1Qvtng)

![image-1683295832387.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcr4hxgYfej1BD1U88UBEvBJcOvbMmV1eD_Wwbs0hTZhE0Y4A8QHmHoncGNCrWg4hcX94_vtuxUxR2G08oWLTHd8g6QE_3fSZXWHNHKo40T8IL_Y-wj3x0qNDQ_zl2pyPR8HVaCiMbUAf10tQ5lcw?key=k6iRdsF6jiaLjR-r1Qvtng)

![image-1683296015309.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfo1VsHF1TeezDpO39E6SpDXiNfBxhKgI630M7K3sQDk-SwlPWruWnrz7YscJ-ptuX8hsg8fBjoPsVCIUNHGUiXG1eFQ0pF64gfhPfX3TP24fx57-_ASrtJMDIr0rnRpl7tOv8c5oEwAMPXOKzR?key=k6iRdsF6jiaLjR-r1Qvtng)

## Стандартные ПН

В настройке "Стандартные ПН" указываются определенные правила для создания поисковых наборов. Например, по созданным правилам Вы можете разбить информационную модель с помощью инструмента [_“Стандартные”_](https://wiki.sgnl.pro/ru/tools/tools-work/search-sets-basic) по любым сценариям: типы систем, виды оборудования, диаметры труб, материалы и т.д.

 1. Нажмите на панели Настройки ➤ Настройки ➤ Стандартные ПН

![image-1683296118134.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXef_Rncj4t-DDsszmdhZAO9_5Npr6we22mFWmrMUG5WsJA6kOeT2rQRM6DyCD95aTKFXC_r8EKBb6fnew5f8IN9XmehwSXoUiymEFf2tdj-PBfQCi1b5ZFHHkKuEAY23eWGBBQSN5JRFx2mLtEd?key=3YqF-xp4RZHSwh8tV_v6MQ)

-   Для того чтобы дублировать правило с значениями выделите его и нажмите  .

2\. Для того чтобы добавить правило создания ПН нажмите 

![image-1683296015309.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfV3fWlmD6-C_yeze4bbe7AWdib__ixSZ-loTn6rtLEXUAixX9hiXjBEwBE0NiWi0qYkXYNqmqrCOAy4UHKOwlsQuQrY1PWRQw32Eo2vkBAmeMcVpUp1KbMfnfr6b6hG-ztT_hGcNTMi2VMlC044g?key=3YqF-xp4RZHSwh8tV_v6MQ)

 и выберите одно из правил

![image-1683296198382.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcuoa7Zlp6452EtxS6DmuWdszT-MOy3pOkvheSCN1il1F3n40XohFqC-K20CjWLy-sSjIOxG65F2pnWKHD0TXdInrIeyWYUFd2CJHNadrSOJAErzZXDjLRaHz9oqfbGoO84beyZqXezBhuprZ9Z?key=3YqF-xp4RZHSwh8tV_v6MQ)

**_2.1. Простое правило_**

Данное правило  позволяет разбить модель по какому-нибудь одному из свойств, например, по категории, коду классификатора, этажу, корпусу и т.д.

![image-1683296264595.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdWrdrVA0nevyPni7dzGVDkGUii1iyqC8H4Ma8G8LYiFHXuzyaYQg8UEB2WueWT4kMZTyuNy2BtMZ1E4DdVua4VBfUbSnFcAdNk8no51vGsDYrTuP1oRqg25TYTgZKZImZuK7CGvMS18B0Pff5fTQ?key=3YqF-xp4RZHSwh8tV_v6MQ)

-   ***В строке “Название”*** впишите название правила, которое будет отображаться в окне создания [_“Стандартные”_](https://wiki.sgnl.pro/ru/tools/tools-work/search-sets-basic)
-   ***В строке “Имя папки”*** введите имя папки, в которой будут созданы поисковые наборы
-   ***В строке “Категория - Свойство”*** введите категорию и свойство, по которым будут созданы ПН.

![image-1683296286292.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeGOvkwFOh8ifUES1R3tiKRP0GqFcOg3TZnTRL8gvq48PSaRwLu_BsoqCniKbhuazHkLG4yujmC7K9hk9pc8DJWv2GrB5atKS0KXbNyYsMPaw4MaJbauRyw8brcQGRN9rwsclxojqIbOkhr3wcxEw?key=3YqF-xp4RZHSwh8tV_v6MQ)

-   ***В строке “Префикс”*** можете ввести префикс к поисковому набору, например, “Категория-”.

Например, разобьем модель по категории:

![image-1683296343208.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe5CIyhKGC1L9zxbF7QvljhXVDi_BIiqCY5D4gxRCQy4ZuQNwSo9pD5z4ZP8bekEKpNNlNMvkPTYpRO0G-llBw3ylDFk2olhm45Tavoovuw-Y9MSMG_agjxZTwF1jLHVtfJI43WL7WQK1es5kEf?key=3YqF-xp4RZHSwh8tV_v6MQ)

По данному правилу с помощью инструмента [*_“Стандартные”_*](https://wiki.sgnl.pro/ru/tools/tools-work/search-sets-basic) создаются поисковые наборы в панели Наборы.

![image-1683296355014.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdl_VT4q59xmuPegqTT6Njy50OvxZL9bYzGgjQ_ucSCWge-rqs7Fcg0qrCLprWgY2SWfsm46hONO8SMcrZwQnVJWairxuIjXEQ6VFkAfuV3qdAUGn1G1X431SW0XtPjRVGfuOwfvS0SUjjIlx9k8g?key=3YqF-xp4RZHSwh8tV_v6MQ)

**_2.2. Комплексное правило с условиями_**

Данное правило позволяет разбить элементы с определенным значением по различным свойствам. Например, элементы с значением категории “Стена” можно разбить по “Типу” или “Этажу”.

![image-1683296383625.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcC-qZDe3OUUIKo0cjLJUvF4qpd-kOQngb9WWHPRln2yD0uFRwqY_Wk5CThCYh96i296zATQPuvcPZFSVZC93Mz0NjxlDNIZn15k4NLdlZ8nujudeesyqAy_aTrs3mYAPNP3VTrEbfMcMeyTZcqTw?key=3YqF-xp4RZHSwh8tV_v6MQ)

-   ***В строке “Название”*** впишите название правила, которое будет отображаться в окне создания [_“Стандартные”_](https://wiki.sgnl.pro/ru/tools/tools-work/search-sets-basic)
-   Далее алгоритм следующий: Если в элементе имеется *_свойство_*, например, “Категория”, и значение этого свойства равно, например, “Стены”, то в папке создаются поисковые наборы, которые разбивают данные элементы по *_свойству_*, например, “Тип”.

*_Свойства_* указываются как пары “Категория-Свойство”

![image-1683296398833.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfb9L0XZIDWGq8I0ApxTz9OM5PW10dvlJxTmhAW4j5iZguutz6OavNVVhyK-PZJDAur5O8Hg6ArFkcwsQ6CCkDj7pB9JQjrQ1QqN-fcNydrD4LMfkpa6px9hlEhlo8l0ngO-NnlhCSm2x_lNhNQcA?key=3YqF-xp4RZHSwh8tV_v6MQ)

-   ***В строке “Имя папки”*** введите имя папки, в которой будут созданы поисковые наборы
-   ***В строке “Префикс”*** можете ввести префикс к поисковому набору, например, “Тип -”

Например, разобьем по “Типу” элементы категории “Стена” и “Перекрытие”:

![image-1683296424338.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcWYXDnd9qticXD4rjov_oiDfDw0dOPj50Q_HiVEzZ1-qNvYG40EyHaaAlmSH21Btsje28fZXjIh1Zsu2posi2GuvnD6_1tKcsltQjfTiHEC0v3W65XNjju3SXtquBxtUFzqrJ_oiOGJa6m2Fw6Xg?key=3YqF-xp4RZHSwh8tV_v6MQ)

По данному правилу с помощью инструмента [_“Стандартные”_](https://wiki.sgnl.pro/ru/tools/tools-work/search-sets-basic) создаются поисковые наборы в панели Наборы.

![image-1683296436007.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeoa3RDk2En2951-2vaSq4SmMpkPi3PFIO5qbaLHaco54HspkFWEWPg-y2houmye4fGzlps0UyIY9x7ou7aA5_I-zaAWGj8nELd3eVuPZ-Dor1cmr9aWIB-B4jKxOsB6rOdRTlq2sBOqQHmGKW8?key=3YqF-xp4RZHSwh8tV_v6MQ)

**_2.3. Правило с условным свойством_**

Данное правило позволяет разбить модель по [_“Условному свойству”_](https://wiki.sgnl.pro/ru/tools/tools-work/settings-conditional-properties).

![image-1683296453184.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf6_gWcQxWV9Vk7jPPbB1UbqqVEcjqysnHIwtrg-PGR1qqZaVyJXRPW-cnbjKiKNZbDRtmWHeMzFkrTs6UkVf8XHtHuHh0Rii9Xo4MBLXSRxoIzFVIOGLi42lpJmPluuq36Lu9AJ4dI8ea7IUoJDg?key=3YqF-xp4RZHSwh8tV_v6MQ)

-   ***Нажмите “+”*** и выберите из списка “Условное свойство”, по которому требуется разбить модель, например, “Код по классификатору”.
-   ***В строке “Имя папки”*** введите имя папки, в которой будут созданы поисковые наборы
-   ***В строке “Префикс”*** можете ввести префикс к поисковому набору, например, “Код - ”.

Например, разобьем модель по классификатору:

![image-1683296478032.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf5BoI0glhgWvEq3ZZmIc23jTNKe7CJcTgDOiAqvc9k0yV444M77ev316Mm9NDtwYFhwp23dclR1gF1k5bx9pfsAovaYSIQije_5VJZgcZIvk0MYI7Jqs9VScJ5MGgAZj1tDABTFPJ1bPkssONnXA?key=3YqF-xp4RZHSwh8tV_v6MQ)

По данному правилу с помощью инструмента [_“Стандартные”_](https://wiki.sgnl.pro/ru/tools/tools-work/search-sets-basic) создаются поисковые наборы в панели Наборы.

![image-1683296489395.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfZvTCEq2xBWPBWnJGtgaMUwqBuorZm36drxPmby0DeePdfF9pHb-8Kv6P6O-GyzLI37qesX9TbNpNhcIjijgp0fvsoSufdoZFHJBsPeumd9okUQBRFL3yG5ut4BRqDB95QvrTOtJiATmV928cr?key=3YqF-xp4RZHSwh8tV_v6MQ)

**_2.4. Правило древовидного построения_**

Данное правило включает в себя три предыдущих правила, и позволяет разбить всю модель по иерархической структуре.

Например, можно разбить модель сначала по “Категории”, потом по “Коду классификатора”, потом по “Этажу” и в конце по простому правилу разбить по “Типу”. При этом каждое последующее разбиение по иерархии будет входить в предыдущее разбиение.

![image-1683296518937.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdiRzEbZr4FGpCI2MqPFHvtLsJKGY2fylZ3m9VlldOuQvj0QQXOs6ZrkHCWdAnnRxJfX7ITCeEh2u9h_XoQX3TfoguX0WfoVUzTgioYmLML-XXgF5WvMHU_UbtuDLkl49GFixXeuXIMyLNqu8Rp6Q?key=3YqF-xp4RZHSwh8tV_v6MQ)

-   Свойства для папки указываются как пары “Категория-Свойство”

![image-1683296531272.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc6t1P5BNM953o5-PX_jPfKChWpc8_b1RmzbLvYoA77kXFdBNrTqtfiA0N9rKNv-yQq5jhhSz2uSTldzHnEok_oc5Xok9TtKGLqtMSmp50q5Vul6uZanyN3sh3RLP70y3Xr3zkXLEu3KNNDH4Ml7g?key=3YqF-xp4RZHSwh8tV_v6MQ)

Таким образом, мы получим древовидное построение поисковых наборов

![image-1683296544043.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcvWhMk6YE4PUsp-yxx-F_PnbiOvsGmlBmSuMxWgcVPpVebIThFKRzFGbphVXZ-C0wVSuLEq1LbFAFCuiJOyJusB_EZ3Nz_6MDHeH_3pu_VcpM3czg0NtqnCWAyldoJjnzDvhhdsfE4rWmYKzCa?key=3YqF-xp4RZHSwh8tV_v6MQ)

![image-1683296153487.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdNYu012k71B4G2BiR9R4u4PFgwN6aOrkp3JUzd-2a-AX_KaOuHMA0rvQvRMgRd0xx8_v_8a3ww_iAu_zWH0VBD68n1Ug-yh3WzFU6-Ee5vq_Hr8C3erYVb4NUBBBHO1bBZ3IfbaEGqBcAT_mhaZQ?key=3YqF-xp4RZHSwh8tV_v6MQ)

## Условные свойства

Это набор свойств элементов, которые в разных моделях или в разных элементах обозначают одно и тоже условное свойство. Например, свойство “Уровень” в разных элементах может быть в “Объект-Базовый уровень” или в “Объект-Уровень”. Данная настройка используется в [_“Стандартные ПН”_](https://wiki.sgnl.pro/ru/tools/tools-work/settings-search-sets) при создании поисковых наборов, а также при [_экспорте_](https://wiki.sgnl.pro/ru/tools/tools-work/import-export) свойств.

Нажмите на панели Настройки ➤ Настройки ➤ Условные свойства

![image-1683702376618.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe0vVgmNWBtRT1KWT70xqdKhs9e54VBBinMmi0pnJIRyZKx425lI_9zd9elMyaJK8L_6aGY1_4qjmiGU5DA5oR9qYOXIphF1o59qI-hEGhJFzQKNfl6NpWIFAA52oHOrhOZa1Y-OhTIzUc7EJx0Xw?key=neeEN69Vv4oopi_lMvU1TQ)

-   Набор свойств элементов задается парами “Категория-Свойство”

![image-1683702408365.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeXVLZDLSw2_GQLUJ2s1XRdQfVNsgM1pVlq4vrQLWuCWOUf6LoOF81vlcQEGtx5iq8oDYNr77iuN5CGxy0zfVgJEt9xvIxJLOgEFFdblKY-FS46wXgFeS1ilKLSJnwU0UejWk7xxdJ7ie0kYYSX?key=neeEN69Vv4oopi_lMvU1TQ)

-   Есть возможность скопировать данные из Excel. Для этого выделите ячейки в Excel, нажмите Ctrl+C, перейдите в плагин и нажмите кнопку “Вставить данные из Excel”. Данные скопируются в Условные свойства

![image-1683702433188.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeB4sl41m5Q24VcjjFAdIQabSIi4v2GFD7e389zXS0785FALRhtNSqBEImpZgmh87CtfZNmmgf9LmBwKVPti83klrcqkLpofFwCxdMhWQlgWTMW0da_AuU4tA_XyLzSkzbHrFVjwwgWH_yhNY_AJQ?key=neeEN69Vv4oopi_lMvU1TQ)

## Группы наборов

Настройка позволяет добавить группы наборов с элементами, которые требуется проверить на пересечения с помощью команды [_Checker_](https://wiki.sgnl.pro/app/page/1aFruelKZ3uZ_se-FEomcoyXEbmm8cPH9JzYlL0LqlLQ).

Нажмите на панели Настройки ➤ Настройки ➤ Группы наборов

C помощью команды [_“Стандартные”_](https://wiki.sgnl.pro/app/page/1TeixpZM_MDT9NRCwhePfMF83tnNJ5UYsHEFLyEFy19Y) предварительно создайте поисковые наборы с элементами , которые требуется проверить на пересечения.

![image-1684131749491.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdsHaYzrhb3rZAho-deCs-3kpzWi6xczz_gSqZERF2bqRtnymvVRmFaR-n1swmPLVpO3F1GqFUyrSbINUcCEDmACb_xFT6K1u_Aca_aNRVacTElbrphr8crbCWHmQJnRtC3SbwFGBd4qWA0u3WAuA?key=jOUloeX4PaB4ZiVYildZ8Q)

-   Создайте группу, нажав , напишите название группы, поставьте допуск на пересечения элементов, и добавьте в группу необходимые поисковые наборы.
-     
      
     [](https://wiki.sgnl.pro/uploads/images/gallery/2023-05/image-1684131763925.png)позволяет добавить в группу созданные поисковые наборы. Выберите набор и нажмите “ОК”

![image-1684131786740.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc-1ZVBXaD6EG7075WbkSLTRGCIhf94DTDuK1go3TdopyG2otGanq1YbFAKQ5T5gAhGOQL7cPem4NHMFbsd3_o3IQrX_HB7Fi4Xybyn_2Ax0AWaQGk7HDU5KynsBlVt_d5BxESHhPXfhFakRJt0?key=jOUloeX4PaB4ZiVYildZ8Q)

![image-1684131763925.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf5rgxnqE_5j2O1fKfHXQBqUsDUc0wZOdhtHTRi2GeahCPB6ljxWjvxMGj6uqHrzeeRPHmFwuq_ZcyEigw138WuKEMHDQQn7BjDVJ49bYR2gd06gQXngJu3DVdvNqjPynXm4fTMnJou7UTRopVLrQ?key=jOUloeX4PaB4ZiVYildZ8Q)

![image-1683296015309.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd1t-JUPIZrcJFle35o6HbdEo2KxUVzlaQTBNLuSG-0wDsagmSpbV-0PVcYF5w3outQ5EeMFHM2vkbrGKpGQf5F4BbTk0SsI7zxMUc_GW37YAzeYBy4aLX4By8By9NaR4Spb8D_4C3YQEg8rEtT?key=jOUloeX4PaB4ZiVYildZ8Q)

## Компании

Настройка позволяет добавить Компании, осуществляющие отдельные виды работ на объекте, и указать их при использовании инструментов [_Завершить/Принять/Запланировать_](https://wiki.sgnl.pro/app/page/1zKM2m_O8NPfp5ETOf5NXd1MkKZfEhWvHyyJyEXGYUaM).

1\. Нажмите на панели Настройки ➤ Настройки ➤ Компании

Добавить компанию можно вручную, заполнив поля самостоятельно, или найти ее по ИНН/ОГРН с помощью поиска.

![image-1684131651183.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfCEW7TZ14mlTEZhr9odmszHzUreDBFiv1KnNbhDnOLvM-QhpJzA6FrYEQKXRHkoWKvfi72mtq7vdTx0TnG428bCaZ-xU86m4SQ6wxETtwpdQixVgkeQC2zsoHpeBRp5CM75OS9VNYPAxnLkLG1Ig?key=umRQDo5b3Kb2-QphTMtzbQ)

2\. Нажмите “Добавить компанию по ИНН/ОГРН”, укажите ОГРН или ИНН компании и нажмите Поиск. Выберите компанию и нажмите “ОК”.

![image-1684131676778.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXes8SEG-cB9f800MhM0X1S8gmSQxBxZYEDQIMKcD-AB3rZyVz4zNKtfneZXbjjRuA4D_gy6LEmk7A-QWPKmpDkuVd7Bj7I3U09kNa-lczzOjoHfjxEIOXwN-kKhsDUekhoxmEhQSu05MMfG9YGS?key=umRQDo5b3Kb2-QphTMtzbQ)

#
<sub>**[<   TOOLS. Методология работы](/ru/tools/general/methodology)     **|**     [TOOLS FOR NAVIS. Панель    >](/ru/tools/navis/panel)**</sub>