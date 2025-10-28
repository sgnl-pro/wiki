---
title: Проверка - Checker
description: 
published: true
date: 2025-09-22T08:57:51.868Z
tags: 
editor: markdown
dateCreated: 2025-06-27T11:48:15.737Z
---

<h3><strong>Checker</strong></h3>
<p>Комплексный инструмент, позволяющий проверять модель на наличие параметров в элементах и заполненность значений этих параметров. Например, перед выгрузкой модели в Navisworks проектировщик может проверить модель на заполненность важных параметров</p>
<p>1. Нажмите на на панели Проверка ➤ Checker</p>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc1B-kCvo1x7bBGWzeDG8Qp7c_oontdWyL0lUBPSa9yCPOEfM7bWYPEpVuHQOt8m6_JU8eR2PqETrcrcu1oE7CrMbQ1YWtxZlUdyQ8jEn-rR3aOVcxpHI_YrUqIxKy0bkgZ6BvY0JO6hijafzZV?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1684154725931.png"></figure>
<p>Окно Checker разделено на 3 зоны: проверки, правила и результаты</p>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXf-ULh2vEzk1rHIyFJue8urWQT2SEo5aNYxjndo9i--Uucvp7Bx49-P5TP3G0cFq3VelYxC1DgO003TdfFjePlC7glulhMn2QrkgZDxyJcoPDj-9rjMJXMJXrj6wG1ZK6JtYLaFJPqPU85o_XX0?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1684154736078.png"></figure>
<p>2. Добавьте одну из трех проверок, нажав&nbsp;</p>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcrQn537mklRRsC8mFzAZphAC-LuQvEj85lRfD-SE0WWxV6UCO5a3WeyKRUBspTxAGQQSXRfzVRJ1Jk9L1WjYtDiFfJEUWRzOqveMlKLu_KLV2upPe39U6RhHK1d-AkXrJoxJUpFKnFnMkdYNXBSg?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1684154757280.png"></figure>
<p>.</p>
<p>3. Добавьте правила и запустите проверку, нажав “ЗАПУСТИТЬ ВЫБРАННЫЕ ПРОВЕРКИ”.</p>
<p>4. Просматривайте в модели элементы с ошибками, чтобы составить замечания и исправить ошибки. Выгружайте результаты проверок в Excel или XML. Сравнивайте результаты с результатами предыдущей проверки, чтобы увидеть, какие замечания были исправлены.</p>
<p><strong><u>Зона проверок:</u></strong>&nbsp;в этой зоне отображается процент выполненных проверок, количество элементов прошедших и не прошедших проверку</p>
<ul>
  <li><i><strong>Нажмите “Добавить проверку” </strong></i>, чтобы добавить одну из трех проверок.</li>
  <li><i><strong>“ЭКСПОРТ”</strong></i>&nbsp;позволяет выгрузить в XML все проверки с их правилами. Вы можете отправить данный файл с проверками своим коллегам.</li>
  <li><i><strong>“ИМПОРТ”</strong></i>&nbsp;позволяет загрузить XML файл с проверками.</li>
  <li><i><strong>“ЗАПУСТИТЬ ВЫБРАННЫЕ ПРОВЕРКИ”</strong></i>&nbsp;запускает проверку напротив которой стоит галочка.</li>
  <li><i><strong>Переключатель “Проверить только выделенные элементы”</strong></i>&nbsp;позволяет проверить только выделенные в модели элементы</li>
  <li><i><strong>“ЭКСПОРТ ВСЕХ РЕЗУЛЬТАТОВ”</strong></i>&nbsp;позволяет выгрузить результаты всех проверок в один Excel файл, который можно передать коллегам для исправления элементов, которые не прошли проверку</li>
</ul>
<p><strong><u>Зона правил:</u></strong>&nbsp;в этой зоне создаются правила, по которым будет происходить проверка. Правила созданные в Navisworks совместимы с правилами в Revit.</p>
<ul>
  <li>При создании правил необходимо выбирать их вид из выпадающего списка - Параметр Типа или Экземпляра</li>
  <li>Кнопка &nbsp;позволяет выбрать параметр из списка</li>
  <li><i><strong>“ЭКСПОРТ”</strong></i>&nbsp;позволяет выгрузить правила проверки в Excel файл. Данный файл можно дополнить правилами и загрузить обратно в Checker или отправить его коллегам.</li>
  <li><i><strong>“ИМПОРТ”</strong></i>&nbsp;позволяет загрузить Excel файл с правилами проверки. Если у Вас уже есть созданные правила в Navisworks, то вы можете импортировать их в Checker в Revit</li>
</ul>
<p><strong><u>Зона результатов:</u></strong>&nbsp;в этой зоне отображаются результаты проверки в виде названия элементов и описания причины, почему элементы не прошли проверку</p>
<ul>
  <li><i><strong>Нажмите “Выбрать все”</strong></i>&nbsp;, чтобы выделить в модели все элементы не прошедшие проверку</li>
  <li><i><strong>Нажмите &nbsp;</strong></i>рядом с результатом, чтобы выделить в модели один или группу элементов не прошедших проверку.</li>
  <li><i><strong>Нажмите “Сгруппировать результаты”</strong></i>&nbsp;, чтобы сгруппировать результаты проверок по повторяющимся названиям элементов и описаниям результатов. Таким образом, количество позиций в списке уменьшится и будет проще посмотреть в модели элементы не прошедшие проверку.</li>
  <li><i><strong>Нажмите “Экспорт результатов</strong></i><strong>” </strong>, чтобы выгрузить результаты проверки в формате Excel или XML. После исправления замечаний данный XML можно сравнить с новыми результатами через команду “Сравнить”</li>
  <li><i><strong>Нажмите “Сравнить” &nbsp;</strong></i>и загрузите XML файл с результатами предыдущей проверки, чтобы посмотреть какие замечания были устранены</li>
</ul>
<p><i><strong><u>Проверки Checker</u></strong></i></p>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcNNb3hP2ZqmKlNAxY03aoAJa2bGxmGCl78UbXGoA2W0pNfHcmCD2KLPl6IlNvBCEj4CViFQDzykneBCM7NWXkVtmVaQk7-dS9HGWF60rXmjovEGcWeBYCtz-etBu4HLjyq8IgCLtpn5pSDxhxsbA?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1684154905217.png"></figure>
<p><strong><u>1.Наличие свойств</u></strong></p>
<p>Проверяет заполненность значения проверочного параметра. Подходит для проверки параметров, которые должны быть заполнены у всех элементов модели.</p>
<p>Например, проверим, что параметр “Код по классификатору” заполнен у всех элементов модели</p>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcDRRMTGBT4nzklSJe-BvVTJmFeakyXPfhLcsH9PZiX-rvwe7Y4fW35yuvqt1w_LyX6Dg1afmJTn7PzqKxmjGGng10APMzGDFbq3SPgrl2UvOlXL0iqsXLJQmy7kbVCd4xeDnrdSPrjJdOvbUh8?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1684154929435.png"></figure>
<ul>
  <li>Добавьте параметр, нажав +.</li>
  <li>Выберите вид параметра (Тип или Экземпляр)</li>
  <li>Введите название параметра, например, Код по классификатору, или выберите параметр из списка, нажав .</li>
  <li>Запустите проверку ➤ в зоне результатов будут показаны элементы, которые не прошли проверку.</li>
</ul>
<p><strong><u>2.Наличие свойств для групп элементов</u></strong></p>
<p>Проверяет, что у всех элементов модели, содержащих условный параметр с определенным значением, заполнены проверочные параметры. (В данном контексте условный параметр - это параметр, который задает начальное условие: Если свойство “Категория” имеет значение “Стены”. Проверочные параметры - это параметры, которые проверяются на наличие заполненного значения)</p>
<p>Например, проверим, что у элементов с условным параметром “Код по классификатору” &nbsp;“Е2.2.2.1” и “Е2.3.1.1” заполнены проверочные параметры ”Этаж” и “Корпус”.</p>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc9Rt_t6HmXNySfa5QMVMidO9k4MUWj1Tnam9KXkc_UGFBhwSnKd_ZrfwWfoF-426zq-hFuuJsJikPfYSRbKyOulDYbEtyk0NOCzNWTREtyk5qu10givZkFtk3hATwIdLaEKqFGwe-dFFSeH5l_?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1684154954487.png"></figure>
<ul>
  <li>Добавьте условный параметр, выбрав его вид (Тип или Экземпляр) и значение данного параметра.</li>
  <li>Добавьте проверочные параметры и запустите проверку ➤ в зоне результатов будут показаны элементы, которые не прошли проверку</li>
</ul>
<p>Правила к данной проверке удобнее создавать в таблице Excel: все правила в Excel из Checker в Navisworks совместимы с Checker в Revit. Если у Вас уже есть созданные правила в Navisworks, то вы можете импортировать их в Checker в Revit или создать новые:</p>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdCTUnGS2S_FkzJiBglm-_HrOQH4pSqmBQhzdaTZhNSsiEJdnuBZOh8moxQgOvKQxrzS16oEFbu_pZ4F3jVZZcjpudQz9fmRw4eciUmZ8-eVVDQTu4CDBcN4Tsb4PtUX7kJFLLXD2R7f7lm64-epg?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1684154967224.png"></figure>
<ul>
  <li>В столбце A (Правило) перечислите условные параметры в виде пары “Вид параметра-Параметр” через дефис без пробелов, а в столбце B (Значение) укажите значения для данных условных параметров.</li>
  <li>Далее в строке 1 начиная со столбца C перечислите проверочные параметры в виде пары “Вид параметра-Параметр” через дефис без пробелов.</li>
  <li>Затем заполните ячейки в матрице любыми значениями, например, “1”, чтобы привязать проверочный параметр к условному параметру.</li>
  <li>Таким образом, получится: “Если параметр “Категория” имеет значение “Стены”, то проверить на заполненность параметры “Имя”, “MP_Корпус” и т.д.”</li>
</ul>
<p>Также можно проверять по другим условиям, например по Коду классификатора</p>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXds356qSwr-cF1jxMYsfN-659rK2LoraFqI66R6x5n5zt6SdRsZk3G7CBQWfk5aKN83b70YOFEjx9a459uXX4qv-m59h_CxKPwwYGM56TOHYaMe5YiraxokhkPZZXKOkHtXd6zVpHgVNXv75o7O?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1684154979157.png"></figure>
<p>Шаблоны можно скачать по следующим ссылкам:</p>
<p><a href="https://wiki.sgnl.pro/app/page/18CaGLQx_pwteleJBblnEP4OxQD4592Cd/view"><u>Checker_Template1.xlsx</u></a></p>
<p><a href="https://wiki.sgnl.pro/app/page/1YO38qsLTx3pybIGwhqkzlFwEkDIUKHQL/view"><u>Checker_Template2.xlsx</u></a></p>
<p><strong><u>4.Заполненность значений свойств для групп элементов</u></strong></p>
<p>Проверяет, что у всех элементов модели, содержащих условный параметр с определенным значением, проверочные параметры имеют заданное значение.</p>
<p>Например, проверим, что у элементов с условным параметром “Категория”, имеющим значение “Стены”, проверочный параметр “Толщина” равен “0,200”.</p>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdy_l3UbflCVBNhh4yhpsgFGqnfMnQwxBKXyWTVoO9oekHQpvsyVhmWzjGlXJJW9z1UgXL-FkX3KGbyNlYF_EUUpiDQZ-93SYCOBedW7M6w2sof0_iL3Bkzb1HViQQrH4RqbXSeFXvbITSt3qIq?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1702554099521.png"></figure>
<ul>
  <li>Добавьте условный параметр, выбрав его вид (Тип или Экземпляр) и значение данного параметра.</li>
  <li>Добавьте проверочный параметр и значение, которое должно быть у данного параметра.</li>
  <li>Запустите проверку ➤ в зоне результатов будут показаны элементы, которые не прошли проверку.</li>
</ul>
<p>&nbsp;</p>
<ul>
  <li><strong>"Равно" (=) и "Не равно" (!=)</strong>- Проверка считается пройденной, если значение проверяемого свойства полностью совпадает или не совпадает с указанным значением. Можно указывать как числовое, так и строковое значение.<br>&nbsp;</li>
  <li><strong>"Содержит" (?) и "Не содержит" (!?)</strong>&nbsp;- Проверка считается пройденной, если в значении проверяемого свойства содержится или не содержится указанное строковое значение.<br>&nbsp;</li>
  <li><strong>"Больше" (&gt;) и "Меньше" (&lt;)</strong>&nbsp;- Проверка считается пройденной, если значение проверяемого свойства больше или меньше указанного числового значения.<br>&nbsp;</li>
  <li><strong>"Больше или равно" (&gt;=) и "Меньше или равно" (&lt;=)</strong>&nbsp;-Проверка считается пройденной, если значение проверяемого свойства "больше или равно" или "меньше или равно" указанному числовому значению.<br>&nbsp;</li>
  <li><strong>"В диапазоне"</strong>&nbsp;- Проверка считается пройденной, если значение проверяемого свойства находится в указанном диапазоне. Диапазон задается двумя числами (минимум и максимум), разделенные двумя точками. В Excel значение записывается следующим образом: <strong>[значение1..значение2]</strong><br>&nbsp;</li>
  <li><strong>"Равно из списка" и "Не равно из списка"</strong>&nbsp;- Проверка считается пройденной, если значение проверяемого свойства полностью совпадает с одним из указанных значений. Можно указать как числовые, так и строковые значения. Перечислите несколько значений, разделив их запятыми без пробела. Если указанные значения можно преобразовать в числа, то они будут проверены как числа. В Excel значение записывается следующим образом: <strong>[значение1,значение2]</strong>&nbsp;или <strong>![значение1,значение2]</strong><br>&nbsp;</li>
  <li><strong>"Содержит из списка" и "Не содержит из списка"</strong>&nbsp;- Проверка считается пройденной, если в значении проверяемого свойства содержится или не содержится хотя бы одно из указанных строковых значений. Перечислите несколько значений, разделив их запятыми без пробела. В Excel значение записывается следующим образом: <strong>?[значение1,значение2]</strong>&nbsp;или <strong>!?[значение1,значение2]</strong><br>&nbsp;</li>
</ul>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfMpnwbjx69tkniUnsXTJ3skmV6bivyrkwJirNEKebqZWbsj0dhmDqQdocLEbLfwg47CVCMEIegc2m7zZKW5Ypg3_8JgfnehEVgEVun_Y96h_gJ53NmXJ912e5dmRPjEaO1o7UJYlf0Wr3ZIp6Q?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1702559387405.png"></figure>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdd1BjKVi1umE9xJtZC8wkXqhN-hMH2TLU_8eiSDwAJ3oXVYG-6_V9ojM-7ADZGfT0Z-56IPtAqgDdm0n5bYhQQHnR_ynLSz1R1OmMtkbQ-0fUUfHtKqE-bljiU5cHau-9cEBKERo5Vv1qv9f-Syw?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1702559383639.png"></figure>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfDurZ97G8yNm5MKIXIdUdGCS2G3f_QWXmPG0jt3QR2oVxP4LCkQQ1EMKw01xaiD6g_DS_EaMB072DClfHRhSD4ChL45cedpIOobpyPEG31933eiINV26rTE_asJ1xDNTZUXseMq493Nz46_wFMxw?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1702559377352.png"></figure>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeiiqiNc_bfQjwxS-arlL7rrtoEWx2iAdgYd1rawjFn-1J-UhfZoW2NY4Nh8YFlxeNkhehUn3_bLyoQqx_n3ksOrvu07xbGfQx4yInaQJRca5J6_PRT2EaQYL7SW_lZZhymKpAKsiNFhuzTmoVOPQ?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1702559365714.png"></figure>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXe_XkPh-hhzArWKXKnTDVUp4m7-nTwAAsPjK5uznf1t8TGVMZQeNWdOaH_89eKNJJ7B4GUu50pczmDXcAYk-salqKMhv9RyiJObZODMayNGdHAYES7dFbKrnjesITKFWOclIJrWlfvwrA1HpaFx4A?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1702559351056.png"></figure>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXd_kO8asHXKMSiH4rpDjeMZmqIvi4O1NuGtL-MXDTXHdhEdhelG4yGiJvlONWcYIuB1bKlzroCZZ_E6reChBGzA7CHpffuach2FGjD-kC_hQV-nLII19AxwQL9nkkDy8RMEkuO-Jjw3R7uYTvgdjw?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1702559336188.png"></figure>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeNT6b_iLgMdZYD78ukC1GSwduWVXqk-uMKNETmMcwZet15xtjupFnmJX0iwnPhuSNPFt9knJZd_8H6rXuUMTZ8x9ZERMmxaRLhykQyGxHjhDnplN12V7ZRWLH3GF2_2-SmowbQ-xazpqDJzJxmyg?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1702559324937.png"></figure>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXddt4CbQ2HsabA2f7CPHyZMhfBcTl4qfJQ6I9sn3DoJ2FY3LsqvIYby6-KjiGy4Xjbf2N-DMwenM8om5vvbjJK1rUZB52atpf-2ren8sI_mH_WVi43jHEt3z6QJUoUJgH1FFv3ncGbq-8pmyOaSvw?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1684154822788.png"></figure>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcEh-kgnFW8oU7qwu-N9NfjzDV7DohRutO6D_od2BdRR3m5SJUSqXqdLpaW-_ZUOkjGAvByfEd06TneJcq0X2crm5wSPsXaJaSnr7B2jf_cHH0ETLXT1Wyc-dK9Q4OedNi75K0X0PBjFDlOxK3v?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1684154876665.png"></figure>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdXILEOdi0wzgMovMkXDYixb-8_RMAgIw4Dt3RuXYJ_iXzLAfEPodZ8r4pXFInHR1wBjh2fGJUSfnhGPrFuwbbqkuxjnOz3JZYeBCtPzRtp2u40_0c6raWSsw9oTpl7dzisrp5Aikxm7xHAILFWfw?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1684154867867.png"></figure>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXempT1NgTJMMPOKy2l6j4G9omtbGGXsmRj2R4G8sB7E1nULQ7vr0JbS_xHwkOGIrDVppdmziwiIjvHomK7BTexKpXQwTo0DNL9drqjANXToV5KjkWs-8141Du6NZegUAvERS9Ea-rj517M-647w?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1684154860341.png"></figure>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXclurTLyNuAOK0NaHr4H2T99E44ov-1hpaT3ZpXOZofN25ZQHoPp97rtKgoRmNGupcXaB1rdUAPATdTYe2L64Jl9F9Pc_cYT2Yf4Eh7-fgxdCGbAIWyQMGPk6Ni8pYc8LVPvCFvcsUw1jrnODEuJg?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1684154849028.png"></figure>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeYfTt95gz9NOf-ZExvxseNjTiDceBlOAVrgUbis1FP2y1i6FVc_PUkTw4TQzySBp_BRNRTIgz--f6yMSZ5Zb13I0P5Df_vHZLUNHaIQVdqgqb2mHzHuTHXzuacncxAaSncLVIiOZFpGhY2OpQMjA?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1684154841748.png"></figure>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXea8jFQqaZ6MNT46-ClKKLBCyA0XALIqLErUGMTNHuFfTFUbmTkgiRcqgRzCJsS3VtUdKPUEZOb9QlVRWwOlgrq-FVDm8dVAd4B3DU40i9O9_x4bq1GJGNhACikdDUQLqiX0HaPFp1L_aeCRx8a?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1684154822788.png"></figure>
<figure class="image"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXedTihpmwF9ZEzi8OFhmpAvhPVH3OzO4IqiLvKYiT2W6Phrgnp4Z7I-pHoRVQ58lF5ETEWZZ4cNWw6XeuSEY1LM6wn5PQ8-8zeg-z8uCGa0rwz2PvjSM9FMt6ESEIyrHAJOdpP958Y0yrTU2sLKLg?key=C5uBO1kflcqHmUaUGJoOYw" alt="image-1684154800280.png"></figure>
