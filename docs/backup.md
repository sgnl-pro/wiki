---
title: DOCS Backup
description: 
published: true
date: 2025-09-09T13:31:17.343Z
tags: 
editor: markdown
dateCreated: 2025-09-09T12:36:10.875Z
---

<sub>**[← DOCS Disk](/ru/docs/disk) | [DOCS Android →](/ru/docs/android)**</sub>

----

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

#
<sub>**[← DOCS Disk](/ru/docs/disk) | [DOCS Android →](/ru/docs/android)**</sub>