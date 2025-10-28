---
title: Утилиты - Нарезка квартир
description: 
published: true
date: 2025-09-21T13:21:22.037Z
tags: 
editor: markdown
dateCreated: 2025-07-31T14:39:17.721Z
---

**Нарезка квартир**

*Инструмент помогает создавать 3D -модели квартир для их дальнейшей передачи клиенту.* 

*Подготовьте формообразующие фигуры в отдельном файле, установите параметры для квартир, загрузите их как связь в основные файлы и нарежьте квартиры с помощью данного плагина.*

### **Подготовка**

#### **Создание формообразующих**

Для того чтобы использовать утилиту “Нарезка квартир” заранее создайте файл где будут расположены формообразующие(системное семейство: формы), использующиеся для разметки квартир.

В подготовительном файле формообразующих  используйте связь файла архитектуры (или другого раздела) как подложку, чтобы с помощью неё разметить формы квартир. Сами формообразующие создаются через вкладку Формы и генплан, нажав на кнопку Форма в контексте.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdhx1Xn-cOdFiTlBq5ujHH28bQXKi6LvJ3tIIT0Dy6W3pZ1iyGACSJBXwUEm786_5ot_ZekRZVXnWTr0JFgIOWAQgfscLxicA57Wlq4A7L5fgYgOC0nOrwrPgQqPfCvMhowjo-N?key=YKT5IiDW3PatwqeGKkX1_w)

#### **Создание параметра**

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

### **Нарезка квартир**

Для вызова утилиты, нажмите во вкладке SIGNAL PRO в категории Утилиты -  “Нарезка квартир” (ВАЖНО: Утилита открывается только в 3D-виде). Эту утилиту нужно вызывать только в файле который вы хотите нарезать на квартиры (например: файл АР, ОВиК и ВК)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfEH2d9l_Z10DNlrlboLPtyBYbsdrwd0fChwfwKSrBv2Au6W29HUFIE_6Q06D170ryqD7b9yhrArUrBZ8tlEr1-4yUe8i0EEzPNBNCjcBUym1kPLnYGqb_Bv3pEAigsGGbJfuxycg?key=YKT5IiDW3PatwqeGKkX1_w)

После чего, вам откроется окно утилиты.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdgdOuKdSNhz1pTksgfclViwO7g6UCNAEtSqdhZtDUmQD2X5WOr1ip4v8cI-8A60VBmX1GkMM7plDjHLb9HsvzwVj1Cm5k5o-P-TAtoQJRFY752hKIa3looEo9wE1dfjSrAT8fy3Q?key=YKT5IiDW3PatwqeGKkX1_w)

 В графу “Параметр с кодами квартир”, как упоминалось ранее, мы вписываем подготовленный параметр (в примере это “Параметр\_квартир”). Это укажет плагину на нужные формообразующие с указанным атрибутом.

 В графу “Коды квартир” мы указываем все нужные нам квартиры, которые мы определили в атрибуте “Параметр\_квартир”. (Например: 1-1, 1-2 и т.д.).

 В графу “Префикс файлов” записываем любой удобный вам текст для наименования созданного файла квартир. По умолчанию, программа выбирает наименование открытого файла.

 Путь сохранения файлов - это путь куда будут сохранены будущие файлы квартир.

 Экспортировать в NWC - эта функция позволяет экспортировать файлы в формат Navisworks. Удобно для сборки разных связей, по типу АР и ВК в единое целое. (ВАЖНО: при экспорте в формат NWC, файлы в формате RVT не будут созданы).

### **Сборка квартир в Navisworks**

Экспорт в Navisworks представляет из себя множество файлов квартир, разных разделов. Открывать каждую будет трудоемко и не имеет смысла.

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

### **Простой просмотр в DOCS**

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