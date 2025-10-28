---
title: DOCS. Дополнительно
description: 
published: true
date: 2025-10-13T09:50:21.686Z
tags: 
editor: markdown
dateCreated: 2025-09-09T15:46:40.736Z
---

<sub>**[<   DOCS Disk](/ru/docs/disk)     **|**     [DASHBOARD. Введение   >](/ru/dash/intro)**</sub>

----

# Вкладки{.tabset}
## 1. DOCS Backup
###### 1. DOCS Backup {#Backup}
  
В SIGNAL DOCS возможно настроить резервное копирование файлов проекта на сервер компании. Для этого необходимо скачать [_клиент резервного копирования_](https://docs.sgnl.pro/s/i/e2f95796-0278-462c-930d-614f2d472c2f) и заполнить файл настроек.

1.  Скачать [_клиент резервного копирования_](https://docs.sgnl.pro/s/i/e2f95796-0278-462c-930d-614f2d472c2f) и распаковать его в папку резервной копии.

**Внимание!** Папка резервной копии должна располагаться на диске с достаточным объемом свободной памяти

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdk8RvSgX6nPVlkO0urcIGP9B1EW-jCPj5thvyL4JrwH3juZZ9VO97imLTiXLAhZNgl-vBWAuXom3bmwZBa0W54N6-y21iDAiPGscdh6aS8u_a2u6bg7_guPl8EaT7CBhE?key=VGXN1rdtEeDWgfm-RwOoQ0kd)

1.  Заполнить файл настроек **appsettings.json.** Открыть его можно с помощью стандартного блокнота

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfSWxP3gH_3i7gq434Znqkhk5WLMVBP_09P5dgISiE0EwX4lMH8A3tZp4qtavLDaKFq8lcCxwuEEj0WFwBFKo4jvwrgEphH4OhVnhqFQocEaTnjCSITFccfUY-H_JuEWuc?key=VGXN1rdtEeDWgfm-RwOoQ0kd)

1.  “YOUR\_PROJECT\_ID” необходимо заменить на ID проекта из DOCS. Для этого перейдите в нужный проект в DOCS и скопируйте его ID из адресной строки.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfQRvb0nspH5mU4_2Oa12KVm6vu7q0A8flwiT_Hr2VM6AaA8IB2i7_VHsUEqqIEVk8UQNRQFjMBon5f3jSEyi4QE1IlVwczM_Koirt6aVh8t-thE7CCg33zjHvN48va_uM?key=VGXN1rdtEeDWgfm-RwOoQ0kd)

1.  Данные для полей “YOUR\_CLIENT\_ID” и “YOUR\_CLIENT\_SECRET” нужно получить  на [_SIGNAL HUB_](https://hub.sgnl.pro/) в разеделе “Интеграции”

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe3At_LFUt-KTSqA-dsNtEerlxulmTuXNpTzCcVZhii2lhSeFYhoE674DP650HsAnhaDYZ2YNHak-TI05mbgBc5f2qSZvf0JwyAtg1ma0v0rxWMZpDak_rwqIpzneEeaNo?key=VGXN1rdtEeDWgfm-RwOoQ0kd)

1.  Нажмите “Добавить”, напишите название и выберите все методы в строке “Scopes”.
2.  После создания интеграции появится “YOUR\_CLIENT\_SECRET”, скопируйте его в файл настроек

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcGE4Av_06-6XM2DaBLTpcz29kC7DCp4oipEUoqSaIocVK8r3lbVzp-H3I0kH8ltted-XJPflgduV4BIVIu2SiHRJZO1VZqJ0An-06rvWM9aJgi509M6pG75C-rUG-NOcY?key=VGXN1rdtEeDWgfm-RwOoQ0kd)

1.  Выберите созданную интеграцию и нажмите   В открывшемся окне будет “YOUR\_CLIENT\_ID”, скопируйте его в файл настроек.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdSjTTfUvIIoWFlO8mIxqm9Xz-h5pjVpytJB_pYx9ESOE3TO2tEYCWrS02wDxudVvhewurTUKgWU52gjN4o6tMVBPkKn6Bf1rM07mTnWI8rRFFWnhRu44tUAk97xZZ1ahM?key=VGXN1rdtEeDWgfm-RwOoQ0kd)

1.  Сохраните заполненный файл настроек и запустите клиент резервного копирования, файлы начнут скачиваться в созданную ранее папку.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdbktgfHZBtBb2FBpwLCBDeHB7xN2Ht9H2z12ZhvAyzHCtV9F8VdydYQODBM5yWp3DSV4f4mngmo9TVsKz1WaQv2DCZKgG0GySu_Kx9OO8HHEJT3BtqN1ZFrhytkrOHw4Q?key=VGXN1rdtEeDWgfm-RwOoQ0kd)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeLXbyg01GyeNzGrFUFzKy_P9ex7lgpw8vIUMKWPtgwHuqdZfQjbA2WbdQgrMAyI_tmOVEy8jRFlq8Za_lOHhi-WpNw2gAjKxIZVDvIdma4mXaBHDNCEjHgJS8O7L0pbQ?key=VGXN1rdtEeDWgfm-RwOoQ0kd)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfv_nv60poflUXj1yYDkgT4GUiEFWCtBAn9IMxc3plTejybJxuirpj6RRHRq4k22_KBC0XfRKkmKFqP5kxGV3vCPRUg5GTD8Jor95M4LY31-gB8fl6sof2B7wIAlGC99w?key=VGXN1rdtEeDWgfm-RwOoQ0kd)

## 2. DOCS Android
###### 2. DOCS Android {#Android}
  
Мобильное приложение DOCS для Android можно скачать на странице приложений: https://hub.sgnl.pro/hub/apps.

Основная задача приложения — обеспечить стабильный доступ к файлам проекта в отсутствие стабильного Интернета (например на строительной площадке). Для этого необходимые файлы или весь проект нужно заранее скачать.
  
Также в приложении можно просматривать изображения и файлы PDF и загружать в проект изображения с мобильного устройства.
  
## 3. Интеграция с Tangl
###### 3. Интеграция с Tangl {#Tangl}
  
В SIGNAL есть модули DOCS, TOOLS, DASHBOARD, INSPECTION. Решения Tangl содержат BIM-вьювер аналогичный Forge вьюверу Autodesk, а также модули Value и Control для работы с объемами из модели и проверке моделей соответственно. Модуль SIGNAL DOCS - это среда общих данных, в которую можно загружать документацию и отправлять на согласование, в том числе и BIM-модели. При работе с BIM-моделями можно использовать Forge-вьювер и Tangl-вьювер. Forge-вьювер - это решение от Autodesk, которое конвертирует и хранит сконвертированные версии моделей на иностранных серверах (AWS в Америке и Европе). Tangl-вьювер имеет преимущество перед Forge в том, что он размещен на Российских серверах в Москве на Yandex-cloud. Некоторым компаниям в РФ запрещено использовать иностранные сервера, в связи с чем, если они хотят применять BIM-технологии в проектировании и строительстве, то Tangl - лучший выбор. В настоящий момент Tangle-вьювер работает с IFC и RVT форматами. Для конвертации IFC формата имеется серверная конвертация, для которой не требуется запущенного приложения Revit. Для работы с RVT моделями требуется либо плагин Tangl, либо SIGNAL TOOLS, чтобы из запущенного приложения Revit сконвертировать в тэнгловский формат модель и опубликовать в SIGNAL DOCS.

### Вкладки{.tabset}
#### 3.1. Настройка Tangl вьювера в DOCS

На каждом проекте отдельно администратор может включать или выключать вьюверы для просмотра BIM-моделей. Это делается в Настройках на вкладке Сервисы > BIM-вьювер

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXctVAQIVYbXdeC_C7ucKZ2EZC2hMFkF2oDV9OK5zRU6IKBbrsDZUA4xkudvucgkHnLKEfIL0fBNUdGfAl1Nce19kVc1G0GPoC9zL4Tq0p-c3rdXqiunii5PyRN0LgamHZg?key=XUWJ4SKiaeLKMYM5NHZ2KA)

Там же раскрыв Клиенты Tangl API можно добавить свой клиент Tangl, чтобы сконвертированные модели в Tangl хранились не на аккаунте SIGNAL, а на своем. Это также позволит пользоваться интеграцией SIGNAL DOCS с Tangl Value и Tangl Control.

#### 3.2. Работа с IFC

Если вы загрузили файл с расширением ifc в DOCS, то по умолчанию перед файлом иконка серого кубика. Вы можете нажать ПКМ по имени файла и нажать Обработать в Tangl

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdrTwd-SteW80KUxtn3j47AuT__dwtWSqD4P1kGBpsW_jakFieVe69fC2f04Vd35BwoNM70U5P6qHVn3nq1IHvc2Rpp-ciNQRaaa9Xp_T6kk0rkSo4UATLGia8XFTtLmQ0?key=XUWJ4SKiaeLKMYM5NHZ2KA)

Иконка станет желтой, что означает что происходит процесс конвертации

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfE6yHsqueBvRFi_GC4U3Orw-lCxyO-dL4FzLygnkw4JnYIuaSCn2E5AX1lT-I3NlkdPIjmAJCrw0yyd4QIpsFVSzKsrOy_D0lri6fxKREOg9AQFK7JjkKbS3WZXoA5mI8?key=XUWJ4SKiaeLKMYM5NHZ2KA)

При наведении на файл курсора мыши будет писаться лог событий по конвертации. Она может занимать от 3 до 10 минут в зависимости от размера файла.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdExa_DQh8piFADbyH0ujhX-PkVCiQB_XFY0DKdeoBSYihOLR52YqpbyQUaj8zuj6hlf3WZTCtZaGMR3gKESxHHNeJe_4tOkKLm-zETGccfFQhmjmKFRoDioenNVBrYzQ?key=XUWJ4SKiaeLKMYM5NHZ2KA)

Когда конвертация будет окончена, то иконка кубика станет зеленой.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcIePsCJa1xyxVf-vvsFT1TExMCwhU86s22xSPoFFw5oNh2pd-fY2g8eT1NwXPUFSTsWlZctQ7hfPsXBBLEizOJVZoprDrUOyEf6a0bUPm5o8Ca_uZuBLHpvtZ1s9_YWnc?key=XUWJ4SKiaeLKMYM5NHZ2KA)

Это означает, что файл можно открывать.

При нажатии по нему появится окно выбора вьювера, в котором требуется выбрать Tangl и откроется модель.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfirlrno11hmsBoycbf5f340hzgLqhTaDJgRs39I-xSRSB7MB0FBF6CWKjqSyoLGLdZDmLCB_sTgClk8QBmi07jX4ScWhRecEW3Im4PsP5HsnneUmzRGZ4e3vCknVnTXKw?key=XUWJ4SKiaeLKMYM5NHZ2KA)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdD_nuB7ruIvmT0IiOZ4-wztQ7Hjk6NoxW5zDMG-fuIWMoSZLD_1Ob0Ym9SK11qTD8LWLZQbdkaNu-KXkGK9xsAXRs-QyPxsOHAupNevSSbTNmMzg9PznZs5QSrIkiPVio?key=XUWJ4SKiaeLKMYM5NHZ2KA)

В случае, если у вас установлен в Настройках свой клиент Tangle API, то у вас будут отображаться еще 2 дополнительных кнопки для открытия Tangl Value и Tangl Control

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdNqQjj8GeMDoaRoP_CRxk7CKXo3fEuk2woJlwB8ZDJ27tDpj0Ny4vmxTxLV7MoZ8xiBoIWkWfIc9mK-VKaMARQxg5BGlFS8AgljkshZmBTPHrZ8JTOXB23ETy8qogVIQ?key=XUWJ4SKiaeLKMYM5NHZ2KA)

Если выбрать один из модулей, то откроется встроенный в DOCS интерфейс Tangl где потребуется ввести учетные данные от данного сервиса для проверки наличия лицензии и если она есть, то будет доступен интерфейс Tangl для работы с моделями напрямую из SIGNAL DOCS.

#### 3.3. Работа с RVT

Для открытия модели в RVT формате из SIGNAL DOCS, надо её загружать из Revit с автоматической конвертацией с помощью серверной обработки в SIGNAL TOOLS.

Для этого запустите на сервере компании Revit с установленным плагином Signal For Revit из модуля TOOLS. На вкладке SIGNAL PRO выберите команду Настройки и Войдите в учетную запись с лицензией TOOLS.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcES572J-lmBvH_7q_ZFYWuWWyq8BmzwbmGVvttTvx5iRCL-7q-joo28rLB_mYYTewLNnsamt9Tb9Ncogz0XUtjRcCDzgmbCpqsK4FFk_YfI2p8iXBdHQIwCKlEgANasv0?key=XUWJ4SKiaeLKMYM5NHZ2KA)

Далее выберите Серверная обработка > вкладку Задания и Создайте или выберите имеющееся задание на серверную обработку.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdGjdnwoMzEc0oU7gm_sxt36yHqoC_cJJanyjgwNT7Wx41oKJRq7dcrqRe-09quRL_H0jto9B6VN7Gd53CYTzmpmxmI2oSv7Ei1mVhIFLAhfezsHB__E_YPWC8ZYCg1tw?key=XUWJ4SKiaeLKMYM5NHZ2KA)

В правой части можно будет добавлять файлы с файлового сервера или со своего компьютера через + или с Revit-сервера через иконку сервера.

Напротив каждого файла можно выбирать сценарий его обработки. Изначально сценариев нет - их нужно создать на вкладке Сценарии

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfA-jlQlniAW5fsdycAdj7244FidT5eI-xFV9EFKDGavP4l2jdGa7qFcI1SkrNpC-E_1anK54eYpWMt5kHjnxvoaUGPBUAMVswrf-2PspKfGA7SGjEk72coj1_AI3vo8g?key=XUWJ4SKiaeLKMYM5NHZ2KA)

Затем можно перейти на 3й шаг настройки сценария Открытие и сохранение. Далее выбрать в поле Закрытие файла “Закрыть с сохранением как” и настроить публикацию либо в DOCS вместе с конвертацией Tangl, либо напрямую в Tangl (если не требуется публикация в DOCS)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfF4lXcpNOU6YD-lRvXV9dsXG8wamVKPTnF4iddOjIpafnwHt0_CBiXvtps34mJ2u2JmLiR7okknRyWjCGB8h6oTgQmuqKDnxfD6en7eQLK6HY7eMvmk0ddRD1l0hRYeGc?key=XUWJ4SKiaeLKMYM5NHZ2KA)

При публикации в DOCS будут браться данные об аккаунте Tangl из настроек DOCS для выбранного проекта в TOOLS.

Затем вернитесь на вкладку Задания, установите сценарии для выбранных моделей и заполните дни недели и время в которое должна запускаться серверная обработка. Но изначально мы рекомендуем протестировать настройки вручную, нажав “Запустить задание”.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdxp7iF-b60TojjGdFllT_a6A1MeyNrmWVlvY9vu6ydCEbun5SMD2tN-RubjqutdyKXp-LsbCoZ-aRKVUPIA8T_5cHmNDri8OrxvzqJTEvJvNAn7azXuZLByxi1GJScJcU?key=XUWJ4SKiaeLKMYM5NHZ2KA)

Затем после публикации

#### 3.4. Публикация только в Tangl через серверную обработку

При публикации только в Tangl требуется заполнить поля доступов для Tangl клиента. Их можно взять со страницы [_https://auth.tangl.cloud/client\_api_](https://auth.tangl.cloud/client_api) или перейдя в шестеренке вверху в API.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfb4Lgf7EicLemR-tyXyjPWDc9wPCG2G6FMxSmc9bspVrsp4HQdTCK39eA172Y75t_L6o22-tUofyDowevnUKNWvsTJdhnK0PYZWSNU3XP5hZ2saVMk5qjHQLml_Qd0ng?key=XUWJ4SKiaeLKMYM5NHZ2KA)

Затем справа вверху нажать Новый API+ и скопировать ID компании (в SIGNAL поле Идентификатор компании), Идентификатор клиента и Секрет клиента (в SIGNAL поле Клиентский ключ)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcB9LJfMBaql3OLN0p15Kai-ndOjT4zbUlpDtqK-scDJUKQnH-qK-KhvdL34fdNplm0YsFf1CWbadyntPvI00beraJZj5XJM_qHbbt99rOjOmoWcNVdjCxSQ92TPCvZxg?key=XUWJ4SKiaeLKMYM5NHZ2KA)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdpUY6-0AV8cQSehOK_tPZ5O0sqUAPHO1YFyWISPlN0Su7zCJ2L8S9F1xRkkBDhQ36YSpRR3TWULabH09DLpOGzvrt3HcAwsygEfMPqTp1bxua-EboAss8GHC4TNRPPw5k?key=XUWJ4SKiaeLKMYM5NHZ2KA)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXco7L4-Jslgum_x5q99g0uhhFiKcyIVPuq7rD3HSGb8RTuLVq890Q5cF4btAPjFimEAhZkT9dl2WB5Ofa4WCM_JTa549eeGSP01KZSj2YaoI3FUQv1wERydqI__--Lczk8?key=XUWJ4SKiaeLKMYM5NHZ2KA)

Далее введите логин и пароль от учетной записи от имени которой приложение будет работать с Tangl. Результат должен выглядеть примерно так:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd4fHg_EFy0d0gcheE46pMepJ2AWQ8eQFXY-vFKEd_X7tTnLf7o13s-khpyBQ7gjRM7bII0NKGoV3gc5j9V6sO15QRBabCHBk8FwSAiQFeJ1EE3hWeLw53ydoOYyyTU0Uc?key=XUWJ4SKiaeLKMYM5NHZ2KA)

Тут же можно проверить что все корректно введено нажав “Тест соединения”.

Если все настроено корректно, вы увидите следующее сообщение:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXewGS5PIbhARO7coaag5bZRbeMaimhpy6kZGyAS2X3bqSugv6IXMgLC_6g45qE30Y7mQuhhzN7Y5Cnt9GTUGoHM2C-A1q3xjUfoJMfGFO4Pk-iwz7y1K8BB5b7cY2fsFnM?key=XUWJ4SKiaeLKMYM5NHZ2KA)

Если нет, то:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfqTrgWU55qcOncI-81hS7RSs0tCtMKsysWjgEY0lkt7tr77IuTJgzYj4d7xji2zb8yAhNluTCSuD1aXWqqQ7lpY7I7KBbpGJDfctlOxJ93yxMpNu4x960MJg_KFp4-zqA?key=XUWJ4SKiaeLKMYM5NHZ2KA)

## 4. Установка MinIO на Linux
###### 4. Установка MinIO на Linux {#MinIOLinux}
  
### Вкладки{.tabset}
#### 4.1. Загрузка и установка Minio

Первым шагом является загрузка Minio. Мы будем использовать Ubuntu Server 22.04.

1.1. Скачайте и установите пакет MinIO с сайта **https://min.io/docs/minio/linux/index.html**

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdUeVOm7e1YJItqH3Q3KiAYMYU0DflJ7fclJMyHwqwqT9GIbuDKPflfO2xJq_WN0PHr-ODS-0qr65zMeVcZ_Oc6DnPeRD4tNpqtfaKBB9iUF_lwfpLBtzxqQgbZJ0Z6HlgRGUdrJm6JLRp3f2Dkmg?key=tGiWAnAfYwulDbckjXpJUQ)

#### 4.2. Создание службы и запуск MinIO

2.1. Создадим пользователя, от имени которого будет запускать службу приложения:

**sudo groupadd -r minio-user**

**sudo useradd -M -r -g minio-user minio-user**

2.2. Добавим этому пользователю полные права на каталог, в котором будут Ваши данные:

**sudo chown -R minio-user:minio-user /mnt/data/**

2.3. Скачаем файл службы для приложения, чтобы MinIO работало в фоновом режиме:

**wget** [**https://raw.githubusercontent.com/minio/minio-service/master/linux-systemd/minio.service**](https://raw.githubusercontent.com/minio/minio-service/master/linux-systemd/minio.service)

2.4. Переместим скачанный файл в каталог служб:

**sudo mv minio.service /lib/systemd/system/**

2.5. Включим автозагрузку службы:

**sudo systemctl enable minio.service**

2.6. Отредактируем файл конфигурации службы:

**sudo nano /etc/default/minio**

Вставим в файл следующий текст:

**\# Volume to be used for MinIO server.**

**MINIO\_VOLUMES="/mnt/data"**

**\# Use if you want to run MinIO on a custom port.**

**MINIO\_OPTS="--address :9000 --console-address :9090 --certs-dir /home/administrator/.minio/certs/"**

**\# Root user for the server.**

**MINIO\_ROOT\_USER=minioadmin**

**\# Root secret for the server.**

**MINIO\_ROOT\_PASSWORD=miniopassword**

**\# set this for MinIO to reload entries with 'mc admin service restart'**

**MINIO\_CONFIG\_ENV\_FILE=/etc/default/minio**

2.7. **ВАЖНО!** Требуется установить сертификат. См. подробнее ниже раздел **“ 2. Подключение SSL сертификата”**. После этого переходите к шагу 2.8.

2.8. Запустим службу:

**sudo systemctl start minio.service**

2.9. Проверим статус запуска:

**systemctl status minio.service**

2.10. Зададим имя суперпользователя и его пароль:

Откроем в редакторе файл:

**sudo nano /etc/environment**

Добавим две строки:

**MINIO\_ROOT\_USER=minioadmin**

**MINIO\_ROOT\_PASSWORD=miniopassword**

**ВНИМАНИЕ!** Рекомендуется указать более сложный пароль.

2.11. Запустим приложение в консоли:

**sudo minio server --console-address :9090 --certs-dir /home/administrator/.minio/certs /mnt/data/**

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcYJNXYp-5b-s-HFdzsOR-2uYKKil4zNdVV8T0Gn48K8B2G0SSwg1ChXTxIAsIwtlCTm5lPLmloG4O6R2MUwMGTCXFBYfnrJcOWgh22XWHJ3VxW3zubejE6O-s3g6OIbCe2XVjAkRGhcYUb009V?key=tGiWAnAfYwulDbckjXpJUQ)

2.12. Приложение запущено, можно переходить к настройке MinIO

#### 4.3. Подключение SSL сертификата

Вам необходимо заранее приобрести в специализированных центрах (например, [_https://www.reg.ru/_](https://www.reg.ru/))  коммерческий сертификат для доменного имени Вашего хранилища. Например, если адрес хранилища будет s3.YOURDOMAIN.RU, тогда сертификат необходим или непосредственно для адреса s3.YOURDOMAIN.RU, или сертификат домена типа WIldcard (\*.YOURDOMAIN.RU).

Полученные данные необходимо сохранить в двух файлах:

-   сертификат в файле **public.crt**
-   закрытый ключ в файле **private.key**

Оба файла необходимо поместить в папку certs в профиле пользователя на сервере, где будет работать приложение MinIO. Например, /home/administrator/.minio/certs/

#### 4.4. Настройка MinIO

После запуска Minio вы можете перейти в веб-интерфейс хранилища. Для этого откройте браузер и перейдите по адресу: [_https://localhost:9090_](https://localhost:9090/)

Введите логин и пароль суперпользователя. В предыдущих шагах (шаг 2.3.) инструкции мы указали их как minioadmin и miniopassword.  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdhMTVMbpW-9MDdp9DsYtToP-_-ULQ55rSqf7PHkrAuPycJiT_MhPuTRm5npWaYT-yfd4HPfeqEHYCFbxDZRpCgaqtPee-GUawuuxLjnNUeu01Cx6wai4_RjOj8BIBWsqzfmMs3h9N5xJuTJ2octw?key=tGiWAnAfYwulDbckjXpJUQ)

##### Создание ключа доступа

Ключ доступа в Minio используется для авторизации доступа к объектному хранилищу из сервиса DOCS. Ключ доступа включает в себя идентификатор пользователя (Access Key) и секретный ключ (Secret Key), который используется для аутентификации пользователя и обеспечения безопасности данных. Без ключа доступа невозможно получить доступ к объектам в хранилище Minio.

1.  Для создания ключа доступа перейдите во вкладку Access Keys ➤ Create access key

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeoocy1t3UC0xU4WbFU07kVXg0DK5Mg02ESJ2Z46jRVBIK-SSdAUaZTCBHtFiTWx-nDpVaiP7QR4kBXMlFIbSlmiKZdrk_8IYTerlSzENk9vLECYbeVAQfDK_5LLCOMbyqbJhI5EV7y9xdvpO8-wA?key=tGiWAnAfYwulDbckjXpJUQ)

1.  Заполните поля **Access Key** и **Secret Key** самостоятельно или оставьте их как есть. Запомните данные поля, т.к. они понадобятся для подключения к DOCS. Нажмите Create.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdmxIcwFtAUNB1ifVXsjiT3G5VUXRqg9E3N8cS-m58qVA4zMgA_TckRWpIyW5WXkHVSxLzUhubZKkaFXJZNUyMOh2zWT8YvFM5yegB3TWI54LJ89E0z1bPvYro7SMucDTVn-Ae8SkP2hymkOQR0?key=tGiWAnAfYwulDbckjXpJUQ)

1.  Ключ доступа создан

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXehfx3T4INSNvFWGhMbfkn8xX_x9t10-pJiRma5ZU-AjNU5OMHkwZR9R0Xq2bkLqKyOX-ytRkps9l_HPPhQEhMHJFK5k2xrzfpl5k22wcK3Xygwi0C-cgzAyZDkFBvwLrVkbFsna6NkttoYZ3FK?key=tGiWAnAfYwulDbckjXpJUQ)

##### Создание бакета

Для хранения файлов в Minio необходимо создать бакеты. Бакеты - это контейнеры, которые содержат файлы и папки.

1.  Чтобы создать новый бакет перейдите во вкладку Buckets ➤ Create bucket

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXewlmCQegGkqjp6c6sjjCvuEJ6cp26CJhP24DSJ4mle8pSyudMxpnaSWdyamk_OUUmmfOHb5JVCRwq32YsjAb4dh8mUZP4fsE1Wmfw1F8dNcuzDoGckSYg3ApQqPCY_7ZWl_sJGWXpLQjcXaLyheQ?key=tGiWAnAfYwulDbckjXpJUQ)

1.  Введите имя бакета, включите переключатель Versioning и нажмите Create Bucket

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeyMU5SjIi-NcXGNaOU8daZu42hWCZ_qdg6W9duF2R5THg4ePP1ABmNl6N_aaCh1d0vFPG60HAnX_pR5G-A9ygbKZlzjtsLy5tzgqAXpRq7cTGV0cGHQ9aiU7fxwCTj7WbDMuITIHFBtDyiPU6m2A?key=tGiWAnAfYwulDbckjXpJUQ)

1.  Бакет создан.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeNx_Fgjcjwu6OvMvbrDq1dOLFcS1Cb1q3p3EVtQVPsNmHkSojBKlqhBStTbGhPUmfHqBnpBv4Qe63CXlAscsF5GUIcQPMgDTGQKQei5vLBw2v8UWOettDFe1_zqHBkfshAtzwdt5JkD5NTDJfdqA?key=tGiWAnAfYwulDbckjXpJUQ)

#### 4.5. Подключение хранилища к сервису DOCS

> Для подключения к сервису DOCS данный сервер должен быть опубликован в сеть Интернет по портам 9000 и 9090. И во внешней DNS-зоне Вашего домена необходимо создать A-запись с указанием IP-адреса, на котором опубликован сервер с приложением MinIO.
{.is-warning}

Откройте сервис docs.sgnl.pro. Перейдите в настройки сервиса: для этого нажмите на профиль ➤ Настройки

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcaqOuZiGQx_ReaCBFormpAzGNv9yhNnIs0_c6flqSDi7R_TpNpWzVzUwQPitGGpYJG3VwWJzIGmKIEtEamshiDSH0-MPerw9L1NC1efzrZMB1gXKL1rTFfWOexxoGj2hrf4TRzD0lOUFFkdUn2Ng?key=tGiWAnAfYwulDbckjXpJUQ)

1.  Нажмите Добавить новое хранилище

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXePdy4AZ8DeDq5r2PeOagBUSZsfjAY-1Phzm7blqBOHr_oKJakP8KAQg4gE5RfAamepIbIEq3V6dXMcy3ILS72-UjWU9NOAyP1ofYBLzDwtRW9kyEkbev7p4N--drb2gZFVq8F3_0kM8NW3a5scGQ?key=tGiWAnAfYwulDbckjXpJUQ)

1.  Заполните данные в появившемся окне и нажмите Сохранить:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdu46sxReIUjmjFhEC8dc-zx6xoY4OiI7wru-Yy4uAQptOmcD2ozfEWyuKXHfG3p-znrrrqbIVBudr41omaFHp_HN9cs08LW0B0zSDb3SPMA2ItXJ-NoX7alW5CJazzOWrub1Qwdk9Z7F3HR9KAaw?key=tGiWAnAfYwulDbckjXpJUQ)

Обязательные поля:

-   **В строке “Название”** впишите название хранилища для сервиса DOCS
-   **В строку “EndPoint”** вставьте ссылку на сервер с портом 9000, например https://s3.YOURDOMAIN.RU:9090
-   **В строку “Access Key”** вставьте ключ доступа
-   **В строку “Secret Key”** вставьте секретный ключ

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdmxIcwFtAUNB1ifVXsjiT3G5VUXRqg9E3N8cS-m58qVA4zMgA_TckRWpIyW5WXkHVSxLzUhubZKkaFXJZNUyMOh2zWT8YvFM5yegB3TWI54LJ89E0z1bPvYro7SMucDTVn-Ae8SkP2hymkOQR0?key=tGiWAnAfYwulDbckjXpJUQ)

-   **В строку “Bucket Name”** впишите название бакета

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeNx_Fgjcjwu6OvMvbrDq1dOLFcS1Cb1q3p3EVtQVPsNmHkSojBKlqhBStTbGhPUmfHqBnpBv4Qe63CXlAscsF5GUIcQPMgDTGQKQei5vLBw2v8UWOettDFe1_zqHBkfshAtzwdt5JkD5NTDJfdqA?key=tGiWAnAfYwulDbckjXpJUQ)

Не обязательные поля

-   **В строку “Region”**  впишите регион сервера

1.  Готово. Теперь можно пользоваться сервисом

## 5. Установка MinIO на Windows
###### 5. Установка MinIO на Windows {#MinIOWindows}

Для разворачивания своего S3 хранилища можно использовать разные сервера. Мы рекомендуем MinIO - это открытое программное обеспечение, которое позволяет создавать собственное S3 хранилище на своем сервере или в облаке. С MinIO вы получите безопасное и надежное решение, а также быструю установку и простоту использования.

Если Вы планируете использовать другой сервер, обратитесь на почту info.sgnl.pro, и наши специалисты помогут Вам настроить сервер и подключится к сервису DOCS.

В этой инструкции мы рассмотрим, как установить MinIO на Windows и Linux, и подключить его к сервису DOCS

### Вкладки{.tabset}
#### 5.1. Скачивание Minio

Создайте пользователя Windows (или Active Directory) от имени которого будете запускать приложение MinIO. Например, CONTOSO\\minio.

Добавьте созданную учетную запись (пользователя) в локальную группу “Администраторы” на сервере, где будет работать приложение MinIO.

Подключитесь к удаленному рабочему столу пользователя CONTOSO\\minio на этом сервере.

Перейдите на официальный сайт Minio ([_https://min.io/download_](https://min.io/download)), выберите версию для Windows и скачайте файл minio.exe.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfBaSAtl26r-6-_CMf__rZFT_1hV3zIHGvdnhMjKgXvGEjui7mOMpPrrSrVzbuHlBT7gnhlEoovUc-MjFHePvma6dg1leU6petFzEUl8d4ME5Z1WG7AWSZUyRHkX5-DHvgZDmUsOlgNrADxyvh0KA?key=EY_Ajf-Vc1Arr0LG5cmV9g)

Рекомендуется поместить файл minio.exe на диск C:. Поэтому создайте на диске C:\\ папку MinIO.

#### 5.2. Запуск MinIO

2.1. Запустите командную строку Windows (cmd).

Чтобы перейти в директорию, где находится файл minio.exe, введите команду cd ПРОБЕЛ ПУТЬ К ПАПКЕ. Например, cd C:\\MinIO  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdauvMememOq_jTXaLOY5bu7xBXnue101QNk5hBMU_c_n6EuPuPltIT7XaG4Vm2DKnyOVKch19dADOovjiXbYJTGzdX2XP_pgdGwl6ulKlZ--PFVpEZbz0Js1SxxRGTEikkAUXU32qQ8R2aMhSTew?key=EY_Ajf-Vc1Arr0LG5cmV9g)

2.2. Создайте папку для хранения данных приложения следующей командой:  
mkdir data  
  
**ВНИМАНИЕ!**  
В этой папке будут храниться все Ваши файлы в будущем. Поэтому важно, чтобы сервер, на котором будет работать приложение MinIO был расположен (установлен) на отказоустойчивом дисковом RAID-массиве и на регулярной основе необходимо создавать резервные копии сервера (или хотя бы данной папки).  
 

2.3. Далее создайте в системе учетную запись и пароль суперпользователя для администрирования приложения. Это можно сделать следующими командами:  
setx MINIO\_ROOT\_USER minioadmin  
setx MINIO\_ROOT\_PASSWORD miniopassword  
  
**ВНИМАНИЕ!**  
Рекомендуется указать более сложный пароль.  
 
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfLdZpGN1OrHcKCDjN4IW8eVnMG1yk_0_W1z69lm94rvQNg9JHiwEoCv2Xr1U5fm3Z65eMDhxp3qyobIM20V-bu_2OTBmgE5ECzEsat_pmX-OMGk8S4_OlCIiebl8IwVaB4Fw2kIR8t1oApAklh1Q?key=EY_Ajf-Vc1Arr0LG5cmV9g)

2.4. Важным аспектом в подключении сервера к сервису DOCS является протокол HTTPS. Он обеспечивает безопасность передачи данных между клиентом и сервером, защищая их от перехвата и изменения. Поэтому необходимо установить SSL сертификат на сервере, где размещено приложение. Посмотрите как это сделать в разделе **3\. Подключение SSL сертификата**, а затем переходите к шагу 2.5.  

2.5. Запустите приложение MinIO, используя команду:

minio.exe server C:\\MinIO\\data --console-address :9090

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXemiO87edXG9iqly0CAtYd43q4ocqiY4fvhy10wgvq9Bd4-hHj3joqti2Mg0wuttu2tsgcz2aydoK_cZYVKNkbUwbUwqV0hIBt5RmpA2wVVVdr89Ek6E2clDsbeI8YpAcAotFRZo4vQq6U-2EOQ?key=EY_Ajf-Vc1Arr0LG5cmV9g)

2.6. Приложение запущено, можно приступить к его настройке.

#### 5.3. Подключение SSL сертификата

Вам необходимо заранее приобрести в специализированных центрах (например, [_https://www.reg.ru/_](https://www.reg.ru/))  коммерческий сертификат для доменного имени Вашего хранилища. Например, если адрес хранилища будет s3.YOURDOMAIN.RU, тогда сертификат необходим или непосредственно для адреса s3.YOURDOMAIN.RU, или сертификат домена типа WIldcard (\*.YOURDOMAIN.RU).

Полученные данные необходимо сохранить в двух файлах:

-   сертификат в файле **public.crt**
-   закрытый ключ в файле **private.key**

Оба файла необходимо поместить в папку certs в профиле пользователя на сервере, где Вы будет работать приложение MinIO.

Для этого создайте в папке профиля пользователя CONTOSO\\minio (обычно это C:\\Users\\minio) папку .minio с помощью следующей команды в командной строке:  
mkdir C:\\Users\\minio\\.minio   

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdSudbPp60mLLWjWnPdSaSvfdloyNvz3J24GMXCJRShJYCgqXwZK5R82uyI7DtWgqAdUXhF7btb7ls3WhNeJHT7Jl6nUjl7nOetTOQ5dxDkNM4dtWgcYxwahkn4ZoNnuzUcFOVDoew2aKXiEtE7?key=EY_Ajf-Vc1Arr0LG5cmV9g)

А внутри нее создайте папку certs, с помощью следующей команды в командной строке:  
mkdir C:\\Users\\minio\\.minio\\certs  
И переместите в нее файлы  **public.crt** и **private.key.**

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd3zelKnRp6F8pS7GviosM20bwsNw-SdIVgZaSGXEBQYhTztqdFFBZtzXaZa70o_Yp9naXMYQTak1K1215ToHST7cpvb7EP9Zmcjh7SBtiPu4W1b43FNsA9PyXCc4bkTLPcgZO9TKoh3RZQ3eofMw?key=EY_Ajf-Vc1Arr0LG5cmV9g)

#### 5.4. Настройка MinIO

После запуска Minio вы можете перейти в веб-интерфейс хранилища. Для этого откройте браузер и перейдите по адресу: [_https://localhost:9090_](https://localhost:9090/)

Введите логин и пароль суперпользователя. В предыдущих шагах (шаг 2.3.) инструкции мы указали их как minioadmin и miniopassword.  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcmOGEG6Ut3awlRp9dpMa1nUHTWRkffdflhsbeWZAx0wS5G5FhMbf9psSSWNAFpZrPJ4U0QU5easAslWYuksgSkpf-WomBYlGXex87L2veJYkZT75iW9PJ1rvFVyxyahQRW1VVK4gQxoDvsLpwR_A?key=EY_Ajf-Vc1Arr0LG5cmV9g)

##### Создание ключа доступа

Ключ доступа в Minio используется для авторизации доступа к объектному хранилищу из сервиса DOCS. Ключ доступа включает в себя идентификатор пользователя (Access Key) и секретный ключ (Secret Key), который используется для аутентификации пользователя и обеспечения безопасности данных. Без ключа доступа невозможно получить доступ к объектам в хранилище Minio.

1.  Для создания ключа доступа перейдите во вкладку Access Keys ➤ Create access key

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdR0H-BlKK9yIcst8na5HUn3M4CQ0oWzcjoHCrtdK85un4Oq-IK7WTpHVdkijlCuWmkZw2zjoM_b1-YPSzzvwE2l9dLFCFz5IHg_hxLnrBHndlTJhh9OBPnZH-iJnHZnL-9D-6rnCThEqaHcsNcSg?key=EY_Ajf-Vc1Arr0LG5cmV9g)

1.  Заполните поля **Access Key** и **Secret Key** самостоятельно или оставьте их как есть. Запомните данные поля, т.к. они понадобятся для подключения к DOCS. Нажмите Create.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcr4qfJrRg7exERBYKQqa7pSgOAn_zZoIxD99fQ3jLtjGkUOch3rVuEgOjwP5eVY7iaBLgSeKZLvlUrMADwj_fgqqHK3kYosMT4_R83DoWeMY6v1CKsNzjXb3fT-9XlAq2-YEJbDJp0VdKQK7qhGw?key=EY_Ajf-Vc1Arr0LG5cmV9g)

1.  Ключ доступа создан

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXff9Pji_V9KgyZVp2NsQVmL91TujIu0gcH5zI7uI1X7gFtM4aTkTT3rGnOIkmdZrDQmXuniwbVTf5KB10uZSkTq1VuKOgp5g8YFXfUXUMYPY3lrQ1LE2c91L_th6rcu4KwzY7fwVDwlUiR-QnGsew?key=EY_Ajf-Vc1Arr0LG5cmV9g)

##### Создание бакета

Для хранения файлов в Minio необходимо создать бакеты. Бакеты - это контейнеры, которые содержат файлы и папки.

1.  Чтобы создать новый бакет перейдите во вкладку Buckets ➤ Create bucket

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcgpg-g_pVY_99qdanaS1iI9_5aKifu1U26jizkJ4lzsmBSZzgq4fsldMklqACEh6xZ9QMDfj48IJzL-47_DWDfyVw7sw6qhfIa3kHg1ypnfPCuacZorSdDtPPLts-s1ns1CukLaWjMXo06sCeNRQ?key=EY_Ajf-Vc1Arr0LG5cmV9g)

1.  Введите имя бакета, включите переключатель Versioning и нажмите Create Bucket

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfiwrPJgBJyrQsDiU2EK6L0TYBoh5cX1rdBAvpCb7EibtRK_I0MVo0qsT9rDiCGCzZmU1LC4hQ_N4UAEOmyls56eCcZXddB_cq8HJAgRF2T7SkFsybrmLpVeATEhi9SAtD1ZVeH85yaNJ4ee4L5?key=EY_Ajf-Vc1Arr0LG5cmV9g)

1.  Бакет создан.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfmmOikuCdVx_3xMafj2SYwoyNxpNAVznDzwDcNobGDmb0vlNKuDrsKdkpSDmTho-6Ih_-CK5XF1vWZf6brqHXYh_aTAVgvttGdqpXOXoMzu_FMJyVi0Iy6EuCWgJbkV-kWcICTSkQzirC4yoJZQw?key=EY_Ajf-Vc1Arr0LG5cmV9g)

#### 5.5. Подключение хранилища к сервису DOCS

> Для подключения к сервису DOCS данный сервер должен быть опубликован в сеть Интернет по портам 9000 и 9090. И во внешней DNS-зоне Вашего домена необходимо создать A-запись с указанием IP-адреса, на котором опубликован сервер с приложением MinIO.
{.is-warning}


1.  Откройте сервис docs.sgnl.pro. Перейдите в настройки сервиса: для этого нажмите на профиль ➤ Настройки

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfr51WyWLppnax6jSe0IUGgy6rGAdnFva7iMoUPX87FksTb2F-qMz3EqJBPyHkbT5pTiFs1dj11Toz7qxHGULhwhtW1-BItkZUeSwltNcZiu1CihSiqkLBGq2EsgTZkM9ZJHR2t0zX4zHrJjMqcWQ?key=EY_Ajf-Vc1Arr0LG5cmV9g)

1.  Нажмите Добавить новое хранилище

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdIF1pQMG2lsnzdPSWyjtMSeEB6KmcDN-kAuw1T63IH_JDqgT73fbe7OhajcmB5AxJPZCqaulk4ZgHKycGy4lg_Ez7IXmfyth2Hj_FkR8KvraBpQkcyC2Nhp3Qbh16F_TmS9XP5Eo9fTaNKzDgD1g?key=EY_Ajf-Vc1Arr0LG5cmV9g)

1.  Заполните данные в появившемся окне и нажмите Сохранить:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdTG_ghAfhx9vG_1Mg-UjTk4WX3Shglc_jkE3e9HZ5dqjU0P1gL8QmFZScRPkeUYsiJVogslzZ4PkFcMOazEBhTbqOZH5ImrakqIhhBGyYbhW8FYjdr_-4jFntLGkxRiRkmbdg_DFERe0fcruVQ5g?key=EY_Ajf-Vc1Arr0LG5cmV9g)

Обязательные поля:

-   **В строке “Название”** впишите название хранилища для сервиса DOCS
-   **В строку “EndPoint”** вставьте ссылку на сервер с портом 9000, например https://s3.YOURDOMAIN.RU:9090
-   **В строку “Access Key”** вставьте ключ доступа
-   **В строку “Secret Key”** вставьте секретный ключ

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcr4qfJrRg7exERBYKQqa7pSgOAn_zZoIxD99fQ3jLtjGkUOch3rVuEgOjwP5eVY7iaBLgSeKZLvlUrMADwj_fgqqHK3kYosMT4_R83DoWeMY6v1CKsNzjXb3fT-9XlAq2-YEJbDJp0VdKQK7qhGw?key=EY_Ajf-Vc1Arr0LG5cmV9g)

-   **В строку “Bucket Name”** впишите название бакета

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfmmOikuCdVx_3xMafj2SYwoyNxpNAVznDzwDcNobGDmb0vlNKuDrsKdkpSDmTho-6Ih_-CK5XF1vWZf6brqHXYh_aTAVgvttGdqpXOXoMzu_FMJyVi0Iy6EuCWgJbkV-kWcICTSkQzirC4yoJZQw?key=EY_Ajf-Vc1Arr0LG5cmV9g)

Не обязательные поля

-   **В строку “Region”**  впишите регион сервера

1.  Готово. Теперь можно пользоваться сервисом

#
<sub>**[<   DOCS Disk](/ru/docs/disk)     **|**     [DASHBOARD. Введение   >](/ru/dash/intro)**</sub>