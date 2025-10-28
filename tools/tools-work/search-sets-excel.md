---
title: Создание ПН - Наборы из Excel
description: 
published: true
date: 2025-09-21T12:24:26.517Z
tags: 
editor: markdown
dateCreated: 2025-06-27T11:33:53.411Z
---

### **Наборы из Excel**

Инструмент позволяет создавать поисковые наборы (ПН) по определенным правилам, указанным в Excel файле.

1\. Нажмите на вкладке SIGNAL PRO на панели Создание ПН ➤ Наборы из Excel

![image-1683710542440.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcpPnJ0HtrnrvUo8WZcl_9lQg1lJJkyrFSteGoGlX3l7FFsHfUdHEUkXOERxU4ALvkLm6R_OhjctqCBdhgXsPWW5VcSB1pJdnrVnOjLDzbw1BBvbf9IOTm6DKw2mJycvwWhj_BDZY5Uj0jQuxcPgg?key=QmJxTI8etnagPturaVkHuw)

2\. Откроется окно создания ПН в котором нужно указать вариант загрузки Excel.

![image-1701154479099.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfcwynuoAK__9UnX8rtKcwhWSqPDZYyY4uiH8N7YcRbXaqGCLpxtT_mGUeNmJ0AZAlXCT8fhGzLW7L6Mbe_aKfWrzlQ7rUYRyxKBGNjW_qXwpdvHhO5MTDYLgkmo-SHz1PirJEUBCX-4qO7CNeD?key=QmJxTI8etnagPturaVkHuw)

3\. Варианты создания поисковых наборов:

Данный вариант используется для создания структуры по видам работ или реализации структуры классификатора элементов компании.

Скачать файл шаблона можно [по ссылке](https://docs.sgnl.pro/s/f/4d8f615a-27fd-4b1a-a631-c7529eb99f03/i/7897696f-6bfd-4175-9877-74b737ddf563?f=663dec15-0db0-4e70-b152-ceb803fe6ea6)

Принцип заполнения таблицы Excel следующий:

![image-1683710625627.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe5wApcLj-9Bozn-ZT5qo4H91g4Rl3_7k6UtVjARNjOrS4_Gj3s9lGxLE5RReVDSu8k3xwvP4yAHoZoHybZrk8VbWpptp-PI6_UbQVNs7coSQ7WT8XG8sDkxcm-MPYwUKv37IvyQgs-hcOpHT4-?key=QmJxTI8etnagPturaVkHuw)

-   ***В столбце “Поз.”*** содержится значение в формате F1, F1.1, F2, F2.1, F2.1.1 или W1, W1.1, W1.2, W2.1.1, где F означает, что данная строка задает папку, а W создает поисковый набор (Далее ПН).

1.1, 2.1, 2.1.1 - задает вложенность папок, т.е. F2.1.1 будет вложена в F2.1, а та в свою очередь в F2.

W2.1.1 - означает, что ПН должен быть создан внутри папки F2.1.1

***Внимание!*** W2.1.1 может и должен повторяться для всех ПН, которые размещаются в одной папке, т.е. он не увеличивается на последнюю цифру - это не номер по порядку, а указатель на размещение ПН.

-   ***В столбце “Код”*** указывается код ПН (например, код вида работ). Данный столбец может быть пустым.
-   ***В столбце “Описание”*** указывается название папки или ПН.
-   ***В столбце “Ед. изм.”*** указывается единица измерения, которая учитывается при выгрузке с помощью инструмента “Объемы по ПН”. Ед. изм. могут быть м, м2, м3, шт, кг или пустые. Для папки единицы измерения не указываются.

Условия создания ПН: Столбцы “Условие”, “Категория”, “Свойство”, “Значение” и “Оператор” задают одно условие, по которому будут создаваться поисковые наборы. Укажите данные столбцы столько раз, сколько условий требуется добавить.

-   ***В столбце “Условие”*** указывается условие И / ИЛИ.
-   ***В столбце “Категория”*** указывается название вкладки, в которой находится свойство для условия.
-   ***В столбце “Свойство”*** указывается свойство, которое необходимо для условия.

![image-1683710691765.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXddJp92XzA68S7-AQcgXapGoNgqD2Llid1m7Hh72MIyDF3Uca-hmKSDo4kXki6sc6GFcSAonEenc3eHxGzHmViG9CkP6o1otg0zffTW_RPi-uXGIuD5xUwJqxFT5n7CtaETHmSBvBRjFJxzJsxJ?key=QmJxTI8etnagPturaVkHuw)

-   ***В столбце “Значение”*** указывается значение свойства.
-   ***В столбце “Оператор”*** указывается оператор (Равно: **\=**), (Не равно: **!=**), (Содержит: **?**), (Не содержит: **!?**), (Определенный: **d**), (Неопределенный: **!d**), (Больше: **\>**), (Больше или равно: **\>=**), (Меньше: **<**), (Меньше или равно: **<=**).

***Примечание:*** Столбцы “Условие”, “Категория”, “Свойство”, “Значение” задают одно дополнительное условие, по которому будут создаваться поисковые наборы. Укажите данные столбцы столько раз, сколько дополнительных условий требуется добавить.

После импорта данного файла будут созданы ПН в папке Работы

![image-1683710700448.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfrFcCSRb0eOydoiX1HGDVC3pmKt7PhmunLiimBisTD-8P8QL6ZnkZPhaJBg8F4UZo0c8XAwtCl-fhVEpubgZh_R6J5lPKbtZdCIzbCBLm1dNMvsnUVVqXN1_gVQaJnYgBtl_FbYWBFgaP9iyfZig?key=QmJxTI8etnagPturaVkHuw)

**Вариант 2**

Данный вариант отличается от первого варианта тем, что Код и Описание записаны в одном столбце через дефис.

Скачать файл шаблона можно [по ссылке](https://docs.sgnl.pro/s/f/4d8f615a-27fd-4b1a-a631-c7529eb99f03/i/76a98b07-9783-4cef-885a-294b0b7a1053?f=663dec15-0db0-4e70-b152-ceb803fe6ea6)

Принцип заполнения таблицы Excel следующий:

![image-1683710775959.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXftsFLaIurfVc3loB-wULf9f6d4mLv0q0grai2nP8dnKNg_Xq8xV1teMovGJQ9c-7KXm_aOq_a65XwFN3orqJNAeUiTmynXQkvM8cnTyFO12MSK8XimcgnZYK5w3XptPsnYvsidTAnsaxIUSpdqmg?key=QmJxTI8etnagPturaVkHuw)

-   Столбцы Код и Описание записываются в одном столбце через дефис.

После импорта данного файла будут созданы ПН в папке Работы

![image-1683710792431.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf-1y2BuQVkJuA72Uy_xAWvzFccywZR6LKMxfQQYrEzwpzajEkNNfTbNsTGeebpc3bB3lDgJsGee_SyuT9sH8O3EGnRQiDZ2RWoRHc4Zs8nVSnv4V3D-QUCSHCd4c7ShMd3few9RnPQ6TZ5Egwo-Q?key=QmJxTI8etnagPturaVkHuw)

**Вариант 3**

Данный вариант используется для группировки известных имен типоразмеров в группы или для других группировок значений в один ПН.

Скачать файл шаблона можно [по ссылке](https://docs.sgnl.pro/s/f/4d8f615a-27fd-4b1a-a631-c7529eb99f03/i/755b1d05-640a-4079-a1f6-9a4cfcae69df?f=663dec15-0db0-4e70-b152-ceb803fe6ea6) 

Например, перечислим известные конвекторы в модели ИОС и объединим их в поисковые наборы:

![image-1683710833284.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcC6UTSy8Ils-MwRXMK1hb1MPljSVjxyfMREZwOGT830F3NeXseWTh3-HSU7TV1EzEgahTVIc3CAML8VWiPAzfAkeTISuASULyc7qA-cpjFVXe7Iq3bWXotz6wnW9a6IJb0ZbnQShW8r07fO0mXUA?key=QmJxTI8etnagPturaVkHuw)

-   ***В столбце “Поз.”*** содержится значение в формате F1, F1.1, F2, F2.1, F2.1.1 или W1, W1.1, W1.2, W2.1.1, где F означает, что данная строка задает папку, а W создает поисковый набор (Далее ПН).

1.1, 2.1, 2.1.1 - задает вложенность папок, т.е. F2.1.1 будет вложена в F2.1, а та в свою очередь в F2.

W2.1.1 - означает, что ПН должен быть создан внутри папки F2.1.1

***Внимание!*** W2.1.1 может и должен повторяться для всех ПН, которые размещаются в одной папке, т.е. он не увеличивается на последнюю цифру - это не номер по порядку, а указатель на размещение ПН.

-   ***В столбце “Описание”*** указывается название поискового набора.
-   ***В столбце “Ед. изм.”*** указывается единица измерения, которая учитывается при выгрузке с помощью инструмента “Объемы по ПН”. Ед. изм. могут быть м, м2, м3, шт, кг или пустые. Для папки единицы измерения не указываются.
-   ***В столбце “Категория”*** указывается название вкладки, в которой находится свойство.
-   ***В столбце “Свойство”*** указывается название свойства.

![image-1683710865407.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcsk_Ew9cZAHt8l1ttqlpRP_RGPp7VQbGY6y81nEu6gfPb6OhU973MrV165aUhLKtG1ndbvusYz2erG7RiyHRBAt1YLJkP6L_L0IPhbGlgtQyx9aH3UMqmBC02LzSkBuUGHMvW9-AFYMetX6XskTA?key=QmJxTI8etnagPturaVkHuw)

-   ***В столбце “Значение”*** указывается значение свойства.

После импорта данного файла будут созданы ПН в папке Оборудование:

![image-1683710877659.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeJ00TIPyPGem7nq9jeTv08HgWfJW3NodkTr2qc6vdZiZwDzX8UT8jjHhCivAx7xGg0HO1rU1V5oZEFyH6P9Ey9wj1SVRQBNSTF6eF0Y6nLzb3CeI59ZrCEspnqyx-KDKxGF4MLjE3rIVRK5Z560g?key=QmJxTI8etnagPturaVkHuw)

4\. "Создавать только не пустые наборы" - Пустые поисковые наборы не будут созданы

5\. "Выполнить разбивку ПН по структуре объекта" - позволяет дополнительно сделать разбивку ПН с помощью условных свойств.

Поставьте галочку напротив данного поля и затем ниже нажмите "Редактировать правила" для настройки правил. Откроется окно с настройками

![image-1701158168152.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfonQMF9OBFNF4XLURAX_IVj4zHUh5sjh-M8zMVXgu2bbOTNIv908M7bJgefQ-Jg2MHuPC7YBX0FU5N0cSZHmpglOJseDJTj73_6OFnkOOSRkyFTXOnwxKZ8EYHkFdVvD2ni0IDyGhUhvn38O2NIA?key=QmJxTI8etnagPturaVkHuw)

5.1. Нажмите + для добавления правила.

5.2. Укажите наименование правила.

5.3. В поле "Условное свойство" нажмите + и выберите условной свойство, по которому должна происходить разбивка ПН. Условные свойства задаются в [_настройках SIGNAL_](https://wiki.sgnl.pro/app/page/1dGtbOpYGviEU75IoqM3rgmuKhx30Z7S5wyhGoTXeLX0).

Внимание: Указанное условное свойство должно быть прописано в файле в конце всех условий

![image-1701155297907.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdax63rJnYAvhp4ZaGfC6BIqQbLZQ_m6yEHoLyJG3HnEvFj4AdFVTJK6Qs_fTvc6GRQshHovvIfs0jpr0KCzbAShOFMXx_X5_8l6AFz4MmtcUgBWQzgOGWWGfln3nbQWcQGTKj4Khjfa6Zpb7os3Q?key=QmJxTI8etnagPturaVkHuw)

5.4. "Добавить как префикс папки" добавляет к названию папки наименование условного свойства и его значение, например, Этаж Фундамент, где Этаж - название свойства, а Фундамент - значения данного свойства

5.5. "Менять код работы" добавляет к названию кода значение условного свойства, например, 4.1.1.1.Фундамент, где 4.1.1.1 - код работы, а Фундамент - значение условного свойства

5.6. "Менять название работы" добавляет к названию работы значение условного свойства, например, (Этаж Фундамент), где Этаж - название свойства, а Фундамент - значения данного свойства

![image-1701154699131.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXca0c_9l_a0KDp_Fw6fMM5DqDyHPKsYMu6_GD7XTEBFjQDoqyd7Xx-GIaA-7amh5NOuiu9JiZiaDeCYlw1s0W6mvWyGTNkMPX3cPn9YG_4KJrlPUaJADffJM-ZbY_WUSXHRungA32nuVOoDsZT8fw?key=QmJxTI8etnagPturaVkHuw)

5.7. При необходимости добавьте дополнительную вложенность по правилам по такому же принципу. Для вложенных правил не обязательно вписывать последующие условные свойства в файл.

6\. "Создавать папки снаружи от папки работы" - создает папки с разбивкой по ПН на уровень выше от папок Работы. Например, папка работы "Надземная часть" окажется внутри папки с условным свойством "Этаж"

![image-1701156432824.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfOSxy0pzO4XoTH7ePVdaO1sdLMXx0cu10JttsCaOlg8w1-tqXETTml8_xMxjJ59rnTMXjIik853eiVxeUzbPbhW2u-lBd4aqFNlrn203aVgl4M5HfFczDi5wFH_YEbqBB0jLE-fvGpibybUGe3Ww?key=QmJxTI8etnagPturaVkHuw)