---
title: SIGNAL. Дорожная карта
description: Планы развития и выпущенные возможности SIGNAL
published: true
date: 2026-09-21T14:58:02.000Z
tags: general
editor: markdown
dateCreated: 2026-09-21T07:32:13.388Z
---

<sub>**[<   SIGNAL. Что нового](/ru/general/updates)     **|**     [SIGNAL. Публичный API   >](/ru/general/api)**</sub>

---

Показываем, над чем работаем сейчас и что планируем дальше. Направления и сроки могут меняться по мере развития продукта.

> Раздел «Выпущено» собран по опубликованной истории обновлений SIGNAL за 2026 год. Планы подготовлены по публичным story в Tracker; состав и сроки могут меняться.
{.is-warning}

<style>
.roadmap-grid{display:grid;grid-template-columns:repeat(3,minmax(0,1fr))!important;gap:14px;margin:14px 0 24px}
.roadmap-status-grid .roadmap-status-planned{grid-column:1}.roadmap-status-grid .roadmap-status-progress{grid-column:2}.roadmap-status-grid .roadmap-status-ready{grid-column:3}
.roadmap-card.roadmap-status-planned{border:1px solid #dce4ef;border-left:4px solid #9aa6b2;border-radius:14px;padding:18px;background:#fff}
.roadmap-card.roadmap-status-progress{border:1px solid #dce4ef;border-left:4px solid #2f6fed;border-radius:14px;padding:18px;background:#fff}
.roadmap-card.roadmap-status-ready{border:1px solid #dce4ef;border-left:4px solid #17a673;border-radius:14px;padding:18px;background:#fff}
.roadmap-card-release{border:1px solid #dce4ef;border-left:4px solid #17a673;border-radius:14px;padding:18px;background:#fff}
.roadmap-card-status{display:flex;justify-content:flex-start;align-items:flex-start;margin-bottom:12px}
.roadmap-badge-planned{background:#eef2f6;color:#5d6878;padding:4px 8px;border-radius:999px;font-size:12px;font-weight:700}
.roadmap-badge-progress{background:#eaf0ff;color:#2156d9;padding:4px 8px;border-radius:999px;font-size:12px;font-weight:700}
.roadmap-badge-ready{background:#e8f7f2;color:#0d8b72;padding:4px 8px;border-radius:999px;font-size:12px;font-weight:700}
.roadmap-card-copy{color:#64748b;margin:8px 0 0}.roadmap-release-links{margin:14px 0 0}
@media(max-width:900px){.roadmap-grid{grid-template-columns:repeat(2,minmax(0,1fr))!important}.roadmap-card{grid-column:auto!important}}
@media(max-width:600px){.roadmap-grid{grid-template-columns:1fr!important}}
.roadmap-state-tabs{position:relative;margin-top:24px}
.roadmap-state-anchor{position:absolute;top:-90px}
.roadmap-state-nav{display:flex;gap:8px;margin:0 0 18px;flex-wrap:wrap}
.roadmap-state-tab{display:inline-block;padding:7px 12px;border-radius:8px;background:#eef2f6;color:#5d6878!important;font-weight:700;text-decoration:none!important}
.roadmap-state-tab-plan{background:linear-gradient(45deg,#5b8cff,#2f6fed);color:#fff!important}
.roadmap-state-release-panel{display:none}
.roadmap-state-release-anchor:target~.roadmap-state-nav .roadmap-state-tab-plan{background:#eef2f6;color:#5d6878!important}
.roadmap-state-release-anchor:target~.roadmap-state-nav .roadmap-state-tab-release{background:linear-gradient(45deg,#42cfa2,#17865f);color:#fff!important}
.roadmap-state-release-anchor:target~.roadmap-state-panels>.roadmap-state-plan-panel{display:none}
.roadmap-state-release-anchor:target~.roadmap-state-panels>.roadmap-state-release-panel{display:block}

</style>


# Модули{.tabset}

## <span style="background:linear-gradient(45deg,#2d4e67,#112538);color:#fff;padding:3px 7px;border-radius:5px;font-weight:700;pointer-events:none;">HUB</span>

<div class="roadmap-state-tabs">
<span id="roadmap-state-hub-plan" class="roadmap-state-anchor roadmap-state-plan-anchor"></span>
<span id="roadmap-state-hub-release" class="roadmap-state-anchor roadmap-state-release-anchor"></span>
<nav class="roadmap-state-nav" aria-label="Состояние дорожной карты">
<a class="roadmap-state-tab roadmap-state-tab-plan" href="#roadmap-state-hub-plan">Планы</a>
<a class="roadmap-state-tab roadmap-state-tab-release" href="#roadmap-state-hub-release">Выпущено</a>
</nav>
<div class="roadmap-state-panels">
<section class="roadmap-state-panel roadmap-state-plan-panel">
<div style="margin:18px 0 12px;"><span style="background:#eaf0ff;color:#2156d9;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">III квартал 2026</span></div>

<div class="roadmap-grid roadmap-status-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
<!-- Tracker: HUB-159 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Управление сотрудниками</strong>
    <p class="roadmap-card-copy">Мягкое удаление сотрудников организации без потери связанной истории и данных.</p>
  </div>
<!-- Tracker: HUB-12, HUB-45, HUB-52, HUB-54, HUB-121, HUB-163 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Управление проектами и пользователями</strong>
    <p class="roadmap-card-copy">Проект по умолчанию, редактирование пользователей, восстановление лицензий, удобный выбор ролей и пагинация.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-12">2026.12</a> · <a href="/ru/general/updates/2026-13">2026.13</a></p>
  </div>
<!-- Tracker: HUB-58 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Контрагенты компании</strong>
    <p class="roadmap-card-copy">Добавили компании-контрагенты и возможность назначать контрагента пользователю.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2026-15">2026.15</a></p>
  </div>
<!-- Tracker: HUB-178 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Уведомления в MAX</strong>
    <p class="roadmap-card-copy">Подключили уведомления SIGNAL в мессенджере MAX через профиль пользователя.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2026-16">2026.16</a></p>
  </div>
<!-- Tracker: HUB-88 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Новые поля и таблица проектов</strong>
    <p class="roadmap-card-copy">Добавили статус, сроки, стоимость и описание проекта и переработали таблицу проектов.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2026-17">2026.17</a></p>
  </div>
</div>

<div style="margin:18px 0 12px;"><span style="background:#eef2f6;color:#5d6878;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">IV квартал 2026</span></div>

<div class="roadmap-grid roadmap-status-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
<!-- Tracker: HUB-51, HUB-244 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Оргструктура и роли</strong>
    <p class="roadmap-card-copy">Структура подразделений компании и группировка ролей для более удобного управления доступом.</p>
  </div>
<!-- Tracker: HUB-382 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Настройки уведомлений организации</strong>
    <p class="roadmap-card-copy">Администратор сможет задавать настройки уведомлений по умолчанию для сотрудников.</p>
  </div>
<!-- Tracker: HUB-60 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Группы проектов</strong>
    <p class="roadmap-card-copy">Объединение проектов в группы и портфели для навигации и управления.</p>
  </div>
</div>
</section>
<section class="roadmap-state-panel roadmap-state-release-panel">
<div style="margin:18px 0 12px;"><span style="background:#e8f7f2;color:#0d8b72;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">II квартал 2026</span></div>

<div class="roadmap-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Пользователи и роли в проектах</strong>
    <p class="roadmap-card-copy">Добавили дату последнего входа, проекты в экспорт пользователей и синхронизацию ролей проекта с ролями организации.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-8">2026.8</a> · <a href="/ru/general/updates/2026-10">2026.10</a> · <a href="/ru/general/updates/2026-11">2026.11</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Настройки уведомлений</strong>
    <p class="roadmap-card-copy">Пользователь может управлять уведомлениями в своём профиле.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-9">2026.9</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Журнал событий компании</strong>
    <p class="roadmap-card-copy">Ускорили просмотр истории действий и добавили экспорт любого количества событий в Excel.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-7">2026.7</a></p>
  </div>
</div>

<div style="margin:18px 0 12px;"><span style="background:#e8f7f2;color:#0d8b72;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">I квартал 2026</span></div>

<div class="roadmap-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Управление пользователями и ролями</strong>
    <p class="roadmap-card-copy">Добавили групповое выделение пользователей, предупреждения при удалении используемой роли и отдельные приглашения для SSO.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-1">2026.1</a> · <a href="/ru/general/updates/2026-5">2026.5</a></p>
  </div>
</div>

<div style="margin:18px 0 12px;"><span style="background:#e8f7f2;color:#0d8b72;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">IV квартал 2025</span></div>

<div class="roadmap-grid">
<!-- Источник: Что нового 2025.41 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Добавление пользователей в проект</strong>
    <p class="roadmap-card-copy">Добавили выбор всех пользователей при назначении участников проекта.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-41">2025.41</a></p>
  </div>
<!-- Источник: Что нового 2025.40 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Пакетное редактирование пользователей</strong>
    <p class="roadmap-card-copy">Администраторы могут массово изменять данные и параметры пользователей.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-40">2025.40</a></p>
  </div>
<!-- Источник: Что нового 2025.28 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Массовый импорт пользователей</strong>
    <p class="roadmap-card-copy">Добавили понятный результат импорта и исправили обработку адресов с лишними пробелами.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-28">2025.28</a></p>
  </div>
</div>

<div style="margin:18px 0 12px;"><span style="background:#e8f7f2;color:#0d8b72;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">III квартал 2025</span></div>

<div class="roadmap-grid">
<!-- Источник: Что нового 2025.27 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Новый HUB, контрагенты и справочники</strong>
    <p class="roadmap-card-copy">Обновили интерфейс и добавили управление контрагентами и справочниками организации.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-27">2025.27</a></p>
  </div>
<!-- Источник: Что нового 2025.26 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Таблица пользователей</strong>
    <p class="roadmap-card-copy">Добавили сортировку, изменение ширины столбцов и улучшили поиск в проектах.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-26">2025.26</a></p>
  </div>
</div>
</section>
</div>
</div>

## <span style="background:linear-gradient(45deg,#00d1ff,#0695d7);color:#fff;padding:3px 7px;border-radius:5px;font-weight:700;pointer-events:none;">DOCS</span>

<div class="roadmap-state-tabs">
<span id="roadmap-state-docs-plan" class="roadmap-state-anchor roadmap-state-plan-anchor"></span>
<span id="roadmap-state-docs-release" class="roadmap-state-anchor roadmap-state-release-anchor"></span>
<nav class="roadmap-state-nav" aria-label="Состояние дорожной карты">
<a class="roadmap-state-tab roadmap-state-tab-plan" href="#roadmap-state-docs-plan">Планы</a>
<a class="roadmap-state-tab roadmap-state-tab-release" href="#roadmap-state-docs-release">Выпущено</a>
</nav>
<div class="roadmap-state-panels">
<section class="roadmap-state-panel roadmap-state-plan-panel">
<div style="margin:18px 0 12px;"><span style="background:#eaf0ff;color:#2156d9;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">III квартал 2026</span></div>

<div class="roadmap-grid roadmap-status-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
<!-- Tracker: DOCS-278 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Ручная блокировка файлов</strong>
    <p class="roadmap-card-copy">Редакторы смогут блокировать файл от изменения, перемещения и удаления и видеть автора блокировки.</p>
  </div>
<!-- Tracker: DOCS-522, DOCS-523 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Публичные ссылки: права и защита</strong>
    <p class="roadmap-card-copy">Настройка круга пользователей, которым разрешено создавать публичные ссылки, и защита ссылок паролем.</p>
  </div>
<!-- Tracker: DOCS-389, DOCS-520, DOCS-2034 -->
  <div class="roadmap-card roadmap-status-progress">
    <div class="roadmap-card-status"><span class="roadmap-badge-progress">● В работе</span></div>
    <strong>Массовая работа с файлами и моделями</strong>
    <p class="roadmap-card-copy">Пакетные команды в контекстном меню и обработка нескольких моделей за один запуск.</p>
  </div>
<!-- Tracker: DOCS-434, DOCS-1288, DOCS-1292, DOCS-1915, DOCS-1916, DOCS-1917 -->
  <div class="roadmap-card roadmap-status-progress">
    <div class="roadmap-card-status"><span class="roadmap-badge-progress">● В работе</span></div>
    <strong>Развитие согласований</strong>
    <p class="roadmap-card-copy">Плановые даты, гибкое назначение ответственных, фильтрация и новые параметры запуска согласований.</p>
  </div>
<!-- Tracker: DOCS-1978, DOCS-2277, DOCS-2391 -->
  <div class="roadmap-card roadmap-status-progress">
    <div class="roadmap-card-status"><span class="roadmap-badge-progress">● В работе</span></div>
    <strong>ИИ-проверка файлов и моделей</strong>
    <p class="roadmap-card-copy">Проверка документов с помощью ИИ и получение агрегированных свойств BIM-моделей.</p>
  </div>
<!-- Tracker: DOCS-2078, DOCS-2245 -->
  <div class="roadmap-card roadmap-status-progress">
    <div class="roadmap-card-status"><span class="roadmap-badge-progress">● В работе</span></div>
    <strong>Маски именования и атрибуты папок</strong>
    <p class="roadmap-card-copy">Применение масок к нескольким расширениям и использование атрибутов папки в имени файла.</p>
  </div>
<!-- Tracker: DOCS-369, DOCS-2031 -->
  <div class="roadmap-card roadmap-status-progress">
    <div class="roadmap-card-status"><span class="roadmap-badge-progress">● В работе</span></div>
    <strong>Мобильный DOCS и реестры</strong>
    <p class="roadmap-card-copy">Кеширование замечаний и более удобная работа с элементами реестров на мобильных устройствах.</p>
  </div>
<!-- Tracker: DOCS-2003 -->
  <div class="roadmap-card roadmap-status-progress">
    <div class="roadmap-card-status"><span class="roadmap-badge-progress">● В работе</span></div>
    <strong>Автозаполнение замечаний</strong>
    <p class="roadmap-card-copy">Подсказки и предложения значений при заполнении полей замечания.</p>
  </div>
<!-- Tracker: DOCS-1134, DOCS-1178, DOCS-1449, DOCS-1529, DOCS-1878, DOCS-1879, DOCS-1897, DOCS-1929, DOCS-1973, DOCS-2076 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Развитие SIGNAL Viewer</strong>
    <p class="roadmap-card-copy">Новый BIM-вьювер, публичные ссылки, замечания к элементам, облака точек PLY, сечения и улучшенная обработка моделей.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-12">2026.12</a> · <a href="/ru/general/updates/2026-14">2026.14</a> · <a href="/ru/general/updates/2026-15">2026.15</a> · <a href="/ru/general/updates/2026-16">2026.16</a> · <a href="/ru/general/updates/2026-17">2026.17</a></p>
  </div>
<!-- Tracker: DOCS-195, DOCS-984, DOCS-1277, DOCS-1389, DOCS-1392 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>ИИ-ассистент: чат, инструкции и скиллы</strong>
    <p class="roadmap-card-copy">Добавили чат и генерацию документов, инструкции проекта, скиллы и расширенный ввод текста.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-12">2026.12</a> · <a href="/ru/general/updates/2026-15">2026.15</a> · <a href="/ru/general/updates/2026-17">2026.17</a></p>
  </div>
<!-- Tracker: DOCS-1238, DOCS-1683, DOCS-648 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Загрузка и обновление файлов</strong>
    <p class="roadmap-card-copy">Получатели и комментарии при загрузке, обновление неактуальных файлов в комплекте и пакетное обновление версий.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-13">2026.13</a> · <a href="/ru/general/updates/2026-17">2026.17</a></p>
  </div>
<!-- Tracker: DOCS-385, DOCS-738, DOCS-647, DOCS-1315, DOCS-1531, DOCS-1993 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Согласования и передачи</strong>
    <p class="roadmap-card-copy">Гибкое управление типом и отменой согласования, значения по умолчанию, перезапуск и копирование передач.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-12">2026.12</a> · <a href="/ru/general/updates/2026-14">2026.14</a> · <a href="/ru/general/updates/2026-15">2026.15</a></p>
  </div>
<!-- Tracker: DOCS-1691 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Атрибуты в масках наименований</strong>
    <p class="roadmap-card-copy">В масках наименований файлов можно использовать значения атрибутов.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2026-15">2026.15</a></p>
  </div>
<!-- Tracker: DOCS-1247, DOCS-1742, DOCS-1818 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Копирование и обмен структурами папок</strong>
    <p class="roadmap-card-copy">Копирование папок вместе с файлами и версиями, импорт и экспорт пустых папок.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2026-16">2026.16</a></p>
  </div>
<!-- Tracker: DOCS-910, DOCS-937, DOCS-1873 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>График Ганта и прямые ссылки</strong>
    <p class="roadmap-card-copy">Доработали редактор графика и добавили ссылки на файлы, которые сохраняются после перемещения.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2026-17">2026.17</a></p>
  </div>
</div>

<div style="margin:18px 0 12px;"><span style="background:#eef2f6;color:#5d6878;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">IV квартал 2026</span></div>

<div class="roadmap-grid roadmap-status-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
<!-- Tracker: DOCS-415, DOCS-996 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>ИИ-поиск и саммари документов</strong>
    <p class="roadmap-card-copy">Умный поиск по именам и содержимому файлов и краткое содержание документов.</p>
  </div>
<!-- Tracker: DOCS-407, DOCS-396, DOCS-397, DOCS-398, DOCS-554, DOCS-966, DOCS-1290 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Развитие сравнения PDF</strong>
    <p class="roadmap-card-copy">Новые режимы сравнения, синхронизация положения и более точное совмещение версий.</p>
  </div>
<!-- Tracker: DOCS-538, DOCS-1189, DOCS-957 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Пакетная работа с замечаниями</strong>
    <p class="roadmap-card-copy">Создание и изменение сразу нескольких замечаний, включая тип и дату устранения.</p>
  </div>
<!-- Tracker: DOCS-423, DOCS-587, DOCS-737, DOCS-1858, DOCS-1944, DOCS-2159 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Гибкая настройка согласований</strong>
    <p class="roadmap-card-copy">Дополнительные параметры комплектов, этапов, штампов, фильтров и отчётов согласования.</p>
  </div>
<!-- Tracker: DOCS-742, DOCS-2162, DOCS-744, DOCS-1313 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Развитие пакетов передачи</strong>
    <p class="roadmap-card-copy">Несколько внешних получателей, комментарии, копирование настроек и переходы между передачей и согласованием.</p>
  </div>
<!-- Tracker: DOCS-2289, DOCS-1246, DOCS-371 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Мобильная работа с документами</strong>
    <p class="roadmap-card-copy">Открытие офисных файлов, публичные ссылки и кеширование согласований в мобильном DOCS.</p>
  </div>
<!-- Tracker: DOCS-2164, DOCS-337, DOCS-400, DOCS-395 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Просмотр моделей и коллизий</strong>
    <p class="roadmap-card-copy">Просмотр коллизий Navisworks, сборок, документов элементов модели и дополнительных форматов.</p>
  </div>
<!-- Tracker: DOCS-409, DOCS-410 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Обсуждения в замечаниях</strong>
    <p class="roadmap-card-copy">Отдельные пользовательские комментарии и ответы в журнале событий замечания.</p>
  </div>
</div>
</section>
<section class="roadmap-state-panel roadmap-state-release-panel">
<div style="margin:18px 0 12px;"><span style="background:#e8f7f2;color:#0d8b72;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">II квартал 2026</span></div>

<div class="roadmap-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Стандартизация наименований файлов</strong>
    <p class="roadmap-card-copy">В папках можно задавать маски имён и проверять файлы при загрузке, переименовании, копировании и перемещении.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-10">2026.10</a> · <a href="/ru/general/updates/2026-11">2026.11</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Массовое управление типами согласования</strong>
    <p class="roadmap-card-copy">Типы согласования можно массово редактировать и удалять в настройках проекта.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-11">2026.11</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Электронные и ручные подписи</strong>
    <p class="roadmap-card-copy">Добавили скачивание присоединённой ЭЦП и механизм факсимиле для ручной подписи PDF.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-7">2026.7</a> · <a href="/ru/general/updates/2026-10">2026.10</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Документы согласований и передач</strong>
    <p class="roadmap-card-copy">Добавили протокол согласования, настраиваемый текст акта и создание передачи из комплекта согласования.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-9">2026.9</a> · <a href="/ru/general/updates/2026-10">2026.10</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Лента предпросмотра файлов</strong>
    <p class="roadmap-card-copy">Все файлы папки можно последовательно просматривать в удобной ленте.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-8">2026.8</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Новые способы совмещения моделей</strong>
    <p class="roadmap-card-copy">Сборки можно формировать по общим координатам или внутренним началам моделей.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-8">2026.8</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Обновление файлов в согласовании</strong>
    <p class="roadmap-card-copy">Версии файлов можно обновлять, не прерывая запущенный процесс согласования.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-7">2026.7</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Больше данных в публичных ссылках</strong>
    <p class="roadmap-card-copy">В реестре и при публичном просмотре появились тип публикации, версия, срок действия и статусы согласований.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-7">2026.7</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Измерения и работа с большими PDF</strong>
    <p class="roadmap-card-copy">Добавили линейку для измерений и ускорили открытие больших PDF-документов.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-6">2026.6</a></p>
  </div>
</div>

<div style="margin:18px 0 12px;"><span style="background:#e8f7f2;color:#0d8b72;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">I квартал 2026</span></div>

<div class="roadmap-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Развитие сборок</strong>
    <p class="roadmap-card-copy">Добавили просмотр опубликованных листов, версии файлов и работу со сборками в мобильном приложении.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-4">2026.4</a> · <a href="/ru/general/updates/2026-5">2026.5</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Онлайн-редактор офисных документов</strong>
    <p class="roadmap-card-copy">Документы офисных форматов можно редактировать непосредственно в SIGNAL.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-5">2026.5</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Просмотрщик облаков точек</strong>
    <p class="roadmap-card-copy">Добавили встроенный просмотр данных лазерного сканирования.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-5">2026.5</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Копирование между проектами и компаниями</strong>
    <p class="roadmap-card-copy">Папки и файлы можно переносить в проекты другой компании.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-3">2026.3</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Гибкий перезапуск согласований</strong>
    <p class="roadmap-card-copy">Добавили три сценария повторного запуска процесса согласования.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-3">2026.3</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Настраиваемые таблицы</strong>
    <p class="roadmap-card-copy">Пользователи могут управлять видимостью и порядком системных столбцов и атрибутов.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-1">2026.1</a> · <a href="/ru/general/updates/2026-2">2026.2</a></p>
  </div>
</div>

<div style="margin:18px 0 12px;"><span style="background:#e8f7f2;color:#0d8b72;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">IV квартал 2025</span></div>

<div class="roadmap-grid">
<!-- Источник: Что нового 2025.41 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Согласования и передачи</strong>
    <p class="roadmap-card-copy">Добавили оповещение участников при завершении согласования и просмотр PDF в пакетах передачи.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-41">2025.41</a></p>
  </div>
<!-- Источник: Что нового 2025.40 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Работа с тяжёлыми документами</strong>
    <p class="roadmap-card-copy">Ускорили повторное открытие больших документов без повторной обработки.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-40">2025.40</a></p>
  </div>
<!-- Источник: Что нового 2025.39 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Управление согласованиями и публичным просмотром</strong>
    <p class="roadmap-card-copy">Просмотр удалённых комплектов, дополнительные ограничения отмены и улучшения простого просмотра.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-39">2025.39</a></p>
  </div>
<!-- Источник: Что нового 2025.38 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Согласования, передачи и графики Ганта</strong>
    <p class="roadmap-card-copy">Работа с согласованием из файла, группы согласований, публичная ссылка на передачу и редактор графиков Ганта.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-38">2025.38</a></p>
  </div>
<!-- Источник: Что нового 2025.37 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Уведомления по замечаниям и согласованиям</strong>
    <p class="roadmap-card-copy">В уведомления добавили информацию об ответственном.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-37">2025.37</a></p>
  </div>
<!-- Источник: Что нового 2025.36 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>DOCS Disk и большие файлы</strong>
    <p class="roadmap-card-copy">Улучшили скачивание больших файлов и синхронизацию файлов и папок в DOCS Disk.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-36">2025.36</a></p>
  </div>
<!-- Источник: Что нового 2025.35 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Плиточный режим и печать PDF</strong>
    <p class="roadmap-card-copy">Добавили плиточное представление документов, печать PDF и улучшили работу с пометками.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-35">2025.35</a></p>
  </div>
<!-- Источник: Что нового 2025.34 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Tangl, согласования и передачи</strong>
    <p class="roadmap-card-copy">Расширили настройки Tangl, добавление ссылок в комплект и данные компаний в передачах.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-34">2025.34</a></p>
  </div>
<!-- Источник: Что нового 2025.33 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Проверка типов и простой просмотр</strong>
    <p class="roadmap-card-copy">Добавили проверку настроек типов согласований и конфигуратор простого просмотра.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-33">2025.33</a></p>
  </div>
<!-- Источник: Что нового 2025.32 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>XML и перенос настроек</strong>
    <p class="roadmap-card-copy">Добавили создание XML-документов, экспорт типов согласований и подтверждение получения замечания.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-32">2025.32</a></p>
  </div>
<!-- Источник: Что нового 2025.31 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Конвертация Tangl и простой просмотр</strong>
    <p class="roadmap-card-copy">Добавили конвертацию Revit для Tangl и сообщения в режиме простого просмотра.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-31">2025.31</a></p>
  </div>
<!-- Источник: Что нового 2025.30 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Текстовые файлы в DOCS</strong>
    <p class="roadmap-card-copy">Добавили создание и редактирование текстовых файлов непосредственно в DOCS.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-30">2025.30</a></p>
  </div>
<!-- Источник: Что нового 2025.29 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Поиск и массовая работа с замечаниями</strong>
    <p class="roadmap-card-copy">Поиск по атрибутам, повторные оповещения и массовое редактирование замечаний.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-29">2025.29</a></p>
  </div>
<!-- Источник: Что нового 2025.28 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Путь к папке</strong>
    <p class="roadmap-card-copy">Добавили отображение и копирование пути к текущей папке.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-28">2025.28</a></p>
  </div>
</div>

<div style="margin:18px 0 12px;"><span style="background:#e8f7f2;color:#0d8b72;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">III квартал 2025</span></div>

<div class="roadmap-grid">
<!-- Источник: Что нового 2025.27 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Альтернативный просмотр офисных документов</strong>
    <p class="roadmap-card-copy">Добавили дополнительный вьювер для офисных форматов.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-27">2025.27</a></p>
  </div>
<!-- Источник: Что нового 2025.26 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Таблицы, согласования и публичные ссылки</strong>
    <p class="roadmap-card-copy">Улучшили таблицы, выбор доступных типов согласований и скачивание папок по публичной ссылке.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-26">2025.26</a></p>
  </div>
<!-- Источник: Что нового 2025.25 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Импорт настроек и штампование</strong>
    <p class="roadmap-card-copy">Добавили обновление типов замечаний и согласований из другого проекта и вывод сведений о файле в штампе.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-25">2025.25</a></p>
  </div>
</div>
</section>
</div>
</div>

## <span style="background:linear-gradient(45deg,#ff5867,#88383f);color:#fff;padding:3px 7px;border-radius:5px;font-weight:700;pointer-events:none;">FORMS</span>

<div class="roadmap-state-tabs">
<span id="roadmap-state-forms-plan" class="roadmap-state-anchor roadmap-state-plan-anchor"></span>
<span id="roadmap-state-forms-release" class="roadmap-state-anchor roadmap-state-release-anchor"></span>
<nav class="roadmap-state-nav" aria-label="Состояние дорожной карты">
<a class="roadmap-state-tab roadmap-state-tab-plan" href="#roadmap-state-forms-plan">Планы</a>
<a class="roadmap-state-tab roadmap-state-tab-release" href="#roadmap-state-forms-release">Выпущено</a>
</nav>
<div class="roadmap-state-panels">
<section class="roadmap-state-panel roadmap-state-plan-panel">
<div style="margin:18px 0 12px;"><span style="background:#eaf0ff;color:#2156d9;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">III квартал 2026</span></div>

<div class="roadmap-grid roadmap-status-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
<!-- Tracker: ID-156, ID-182, ID-349, ID-387 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Улучшения конструктора и реестра</strong>
    <p class="roadmap-card-copy">Описания полей, единое отображение заголовков, поиск типов форм и настройка видимости.</p>
  </div>
<!-- Tracker: ID-66 -->
  <div class="roadmap-card roadmap-status-progress">
    <div class="roadmap-card-status"><span class="roadmap-badge-progress">● В работе</span></div>
    <strong>Журнал событий и обсуждения</strong>
    <p class="roadmap-card-copy">История изменений и общение участников внутри формы.</p>
  </div>
<!-- Tracker: ID-107, ID-200, ID-265, ID-328 -->
  <div class="roadmap-card roadmap-status-progress">
    <div class="roadmap-card-status"><span class="roadmap-badge-progress">● В работе</span></div>
    <strong>Генерация и подписание документов</strong>
    <p class="roadmap-card-copy">Создание PDF и DOCX по данным формы, поддержка связанных полей и подписание результата.</p>
  </div>
<!-- Tracker: ID-192 -->
  <div class="roadmap-card roadmap-status-progress">
    <div class="roadmap-card-status"><span class="roadmap-badge-progress">● В работе</span></div>
    <strong>Бронирование времени</strong>
    <p class="roadmap-card-copy">Выбор и резервирование свободного времени в календаре из формы.</p>
  </div>
<!-- Tracker: ID-16, ID-150, ID-319 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Генерация DOCX по данным форм</strong>
    <p class="roadmap-card-copy">Шаблоны, условия, циклы, изображения, системные поля и работа со связанными формами.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-12">2026.12</a> · <a href="/ru/general/updates/2026-15">2026.15</a> · <a href="/ru/general/updates/2026-17">2026.17</a></p>
  </div>
<!-- Tracker: ID-115, ID-129, ID-146, ID-153 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Реестр и конструктор форм</strong>
    <p class="roadmap-card-copy">Логи изменений, редактирование завершённых форм, уникальные значения и корзина типов форм.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-13">2026.13</a> · <a href="/ru/general/updates/2026-15">2026.15</a></p>
  </div>
<!-- Tracker: ID-64, ID-159 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Связь полей с HUB и DOCS</strong>
    <p class="roadmap-card-copy">Поля форм можно связывать с пользователями, контрагентами, справочниками, замечаниями, согласованиями и передачами.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2026-15">2026.15</a></p>
  </div>
<!-- Tracker: ID-65, ID-140 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Импорт и экспорт форм в XLSX</strong>
    <p class="roadmap-card-copy">Добавили массовую выгрузку форм и импорт простых форм из таблиц XLSX.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2026-15">2026.15</a></p>
  </div>
<!-- Tracker: ID-176, ID-207 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Связанные формы и видимость полей</strong>
    <p class="roadmap-card-copy">Создание связанной формы из поля-источника и автоматическое скрытие недоступных столбцов реестра.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2026-16">2026.16</a></p>
  </div>
<!-- Tracker: ID-175, ID-178, ID-185, ID-293, ID-324, ID-325, ID-350, ID-355 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Настройки полей, этапов и замечаний</strong>
    <p class="roadmap-card-copy">Значения по умолчанию, выпадающие списки, уникальность, названия этапов и работа с замечаниями без выхода из формы.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2026-17">2026.17</a></p>
  </div>
</div>

<div style="margin:18px 0 12px;"><span style="background:#eef2f6;color:#5d6878;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">IV квартал 2026</span></div>

<div class="roadmap-grid roadmap-status-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
<!-- Tracker: ID-152, ID-186, ID-344, ID-386 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Связи и навигация между формами</strong>
    <p class="roadmap-card-copy">Просмотр взаимосвязей, переходы к связанным формам и перенос значений между ними.</p>
  </div>
<!-- Tracker: ID-296, ID-298, ID-299, ID-360, ID-361, ID-364, ID-365 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Гибкие этапы и ответственные</strong>
    <p class="roadmap-card-copy">Условия назначения, ограниченные списки ролей, наблюдатели, уведомления и отклонение формы.</p>
  </div>
<!-- Tracker: ID-180, ID-351, ID-391, ID-123, ID-177, ID-395 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Развитие конструктора форм</strong>
    <p class="roadmap-card-copy">Группы полей, новый интерфейс и дополнительные правила редактирования и обязательности.</p>
  </div>
<!-- Tracker: ID-84, ID-194, ID-198, ID-329, ID-332 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Новые сценарии генерации документов</strong>
    <p class="roadmap-card-copy">XML, дополнительные правила DOCX и формирование актов по выбранным формам.</p>
  </div>
<!-- Tracker: ID-187, ID-275 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Импорт и внешние интеграции</strong>
    <p class="roadmap-card-copy">Импорт форм с редактированием и интеграция с государственными информационными системами.</p>
  </div>
<!-- Tracker: ID-188 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>FORMS Mobile</strong>
    <p class="roadmap-card-copy">Мобильный сценарий работы с формами.</p>
  </div>
<!-- Tracker: ID-362, ID-366, ID-367 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Формы, объект и документы</strong>
    <p class="roadmap-card-copy">Связь полей, привязка форм к структуре объекта и контроль сроков документов.</p>
  </div>
<!-- Tracker: ID-63, ID-190 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Заполнение форм с помощью ИИ</strong>
    <p class="roadmap-card-copy">Заполнение по документу или изображению и голосовой ввод данных.</p>
  </div>
</div>
</section>
<section class="roadmap-state-panel roadmap-state-release-panel">
<p><em>В I–II кварталах 2026 крупных публичных обновлений модуля не было.</em></p>
</section>
</div>
</div>

## <span style="background:linear-gradient(45deg,#a09eff,#4b47ff);color:#fff;padding:3px 7px;border-radius:5px;font-weight:700;pointer-events:none;">DASHBOARD</span>

<div class="roadmap-state-tabs">
<span id="roadmap-state-dashboard-plan" class="roadmap-state-anchor roadmap-state-plan-anchor"></span>
<span id="roadmap-state-dashboard-release" class="roadmap-state-anchor roadmap-state-release-anchor"></span>
<nav class="roadmap-state-nav" aria-label="Состояние дорожной карты">
<a class="roadmap-state-tab roadmap-state-tab-plan" href="#roadmap-state-dashboard-plan">Планы</a>
<a class="roadmap-state-tab roadmap-state-tab-release" href="#roadmap-state-dashboard-release">Выпущено</a>
</nav>
<div class="roadmap-state-panels">
<section class="roadmap-state-panel roadmap-state-plan-panel">
<div style="margin:18px 0 12px;"><span style="background:#eaf0ff;color:#2156d9;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">III квартал 2026</span></div>

<div class="roadmap-grid roadmap-status-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
<!-- Tracker: DASH-74 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Состояние 3D-карточек</strong>
    <p class="roadmap-card-copy">Сохранение выбранного состояния карточек при изменениях модели на вкладке управления.</p>
  </div>
<!-- Tracker: DASH-29, DASH-99, DASH-101 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Экспорт и навигация по карточкам</strong>
    <p class="roadmap-card-copy">Экспорт отчёта в PPTX, переключение карточек в группе и предупреждения о разных единицах измерения.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2026-13">2026.13</a></p>
  </div>
<!-- Tracker: DASH-103, DASH-69 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Новые карточки и фильтры</strong>
    <p class="roadmap-card-copy">Интеграции со СКУД и Техзор, фильтрация 3D-карточек по подрядчику и общий SLA по ролям.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-14">2026.14</a> · <a href="/ru/general/updates/2026-15">2026.15</a></p>
  </div>
</div>

<div style="margin:18px 0 12px;"><span style="background:#eef2f6;color:#5d6878;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">IV квартал 2026</span></div>

<div class="roadmap-grid roadmap-status-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
<!-- Tracker: DASH-91 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Аналитика замечаний</strong>
    <p class="roadmap-card-copy">Карточка с распределением замечаний по статусам за выбранный период.</p>
  </div>
<!-- Tracker: DASH-100 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Иерархия работ в 3D-карточках</strong>
    <p class="roadmap-card-copy">Сворачивание работ в древовидную структуру для более компактного анализа модели.</p>
  </div>
<!-- Tracker: DASH-81, DASH-194, DASH-195 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Новые данные и экспорт карточек</strong>
    <p class="roadmap-card-copy">Карточки по типам согласований, дополнительные поля рисков и экспорт отдельной карточки в XLSX.</p>
  </div>
</div>
</section>
<section class="roadmap-state-panel roadmap-state-release-panel">
<div style="margin:18px 0 12px;"><span style="background:#e8f7f2;color:#0d8b72;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">II квартал 2026</span></div>

<div class="roadmap-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Интерактивная легенда 3D-карточек</strong>
    <p class="roadmap-card-copy">Цвета из TOOLS можно использовать в легенде и выбирать ими элементы модели.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-11">2026.11</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Накопительный график по финансам</strong>
    <p class="roadmap-card-copy">Обновили карточку накопительных финансовых показателей и управление размерностью данных.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-10">2026.10</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Новые источники данных</strong>
    <p class="roadmap-card-copy">Карточки получили импорт из JSON 1С и привязку XLSX-файлов из DOCS.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-8">2026.8</a> · <a href="/ru/general/updates/2026-9">2026.9</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Аналитика SLA и замечаний DOCS</strong>
    <p class="roadmap-card-copy">Добавили отчёт по SLA сотрудников и персональную карточку со всеми замечаниями пользователя.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-9">2026.9</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Обновление данных и план-факт финансирования</strong>
    <p class="roadmap-card-copy">Добавили ручное обновление отчётов и новую карточку для анализа финансирования.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-7">2026.7</a></p>
  </div>
</div>

<div style="margin:18px 0 12px;"><span style="background:#e8f7f2;color:#0d8b72;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">I квартал 2026</span></div>

<div class="roadmap-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Доступы и жизненный цикл отчётов</strong>
    <p class="roadmap-card-copy">Расширили управление доступами к показателям, группам и публикации, а карточки можно деактивировать без удаления.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-2">2026.2</a> · <a href="/ru/general/updates/2026-3">2026.3</a> · <a href="/ru/general/updates/2026-5">2026.5</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Публикация моделей для внешних систем</strong>
    <p class="roadmap-card-copy">Строительные модели можно передавать внешним системам по публичной ссылке.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-5">2026.5</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>3D-карточка с цветами модели</strong>
    <p class="roadmap-card-copy">Добавили представление модели с цветами элементов и расширенными настройками отображения.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-2">2026.2</a></p>
  </div>
</div>

<div style="margin:18px 0 12px;"><span style="background:#e8f7f2;color:#0d8b72;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">IV квартал 2025</span></div>

<div class="roadmap-grid">
<!-- Источник: Что нового 2025.37 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Карточки MPP и согласований</strong>
    <p class="roadmap-card-copy">Добавили обновление данных для MPP-карточек и вывели количество замечаний в карточках согласований.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-37">2025.37</a></p>
  </div>
<!-- Источник: Что нового 2025.36 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Доступы по ролям</strong>
    <p class="roadmap-card-copy">Добавили управление доступом к DASHBOARD на основе ролей проекта.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-36">2025.36</a></p>
  </div>
<!-- Источник: Что нового 2025.35 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Развитие карточек 41, 50 и 67</strong>
    <p class="roadmap-card-copy">Расширили настройки, выбор диапазона дат и работу с данными в аналитических карточках.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-35">2025.35</a></p>
  </div>
<!-- Источник: Что нового 2025.34 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>План-факт по объёмам MPP</strong>
    <p class="roadmap-card-copy">Добавили карточку 41 для сравнения плановых и фактических объёмов из MPP.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-34">2025.34</a></p>
  </div>
<!-- Источник: Что нового 2025.30 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Шаблоны карточек Онлайн</strong>
    <p class="roadmap-card-copy">Добавили копирование карточек Онлайн из шаблона проекта.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-30">2025.30</a></p>
  </div>
</div>

<div style="margin:18px 0 12px;"><span style="background:#e8f7f2;color:#0d8b72;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">III квартал 2025</span></div>

<div class="roadmap-grid">
<!-- Источник: Что нового 2025.26 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Карточка 67 и экспорт</strong>
    <p class="roadmap-card-copy">Добавили процент выполнения и экспорт данных карточки в Excel.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-26">2025.26</a></p>
  </div>
</div>
</section>
</div>
</div>

## <span style="background:linear-gradient(45deg,#83e6c7,#00cd8d);color:#fff;padding:3px 7px;border-radius:5px;font-weight:700;pointer-events:none;">INSPECTION</span>

<div class="roadmap-state-tabs">
<span id="roadmap-state-inspection-plan" class="roadmap-state-anchor roadmap-state-plan-anchor"></span>
<span id="roadmap-state-inspection-release" class="roadmap-state-anchor roadmap-state-release-anchor"></span>
<nav class="roadmap-state-nav" aria-label="Состояние дорожной карты">
<a class="roadmap-state-tab roadmap-state-tab-plan" href="#roadmap-state-inspection-plan">Планы</a>
<a class="roadmap-state-tab roadmap-state-tab-release" href="#roadmap-state-inspection-release">Выпущено</a>
</nav>
<div class="roadmap-state-panels">
<section class="roadmap-state-panel roadmap-state-plan-panel">
<p><em>Публичные планы модуля пока не подтверждены в Tracker.</em></p>
</section>
<section class="roadmap-state-panel roadmap-state-release-panel">
<div style="margin:18px 0 12px;"><span style="background:#e8f7f2;color:#0d8b72;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">I квартал 2026</span></div>

<div class="roadmap-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Реестр комментариев</strong>
    <p class="roadmap-card-copy">Добавили отдельный реестр для работы с комментариями к результатам проверок.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-4">2026.4</a></p>
  </div>
</div>
</section>
</div>
</div>

## <span style="background:linear-gradient(45deg,#7aa6cf,#7d96ad);color:#fff;padding:3px 7px;border-radius:5px;font-weight:700;pointer-events:none;">TOOLS</span>

<div class="roadmap-state-tabs">
<span id="roadmap-state-tools-plan" class="roadmap-state-anchor roadmap-state-plan-anchor"></span>
<span id="roadmap-state-tools-release" class="roadmap-state-anchor roadmap-state-release-anchor"></span>
<nav class="roadmap-state-nav" aria-label="Состояние дорожной карты">
<a class="roadmap-state-tab roadmap-state-tab-plan" href="#roadmap-state-tools-plan">Планы</a>
<a class="roadmap-state-tab roadmap-state-tab-release" href="#roadmap-state-tools-release">Выпущено</a>
</nav>
<div class="roadmap-state-panels">
<section class="roadmap-state-panel roadmap-state-plan-panel">
<div style="margin:18px 0 12px;"><span style="background:#eaf0ff;color:#2156d9;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">III квартал 2026</span></div>

<div class="roadmap-grid roadmap-status-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
<!-- Источник: Что нового 2026.16 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>SIGNAL Basic для Revit и Navisworks</strong>
    <p class="roadmap-card-copy">Бесплатные плагины для просмотра свойств, поиска элементов и базовой работы с моделями.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2026-16">2026.16</a></p>
  </div>
</div>
</section>
<section class="roadmap-state-panel roadmap-state-release-panel">
<div style="margin:18px 0 12px;"><span style="background:#e8f7f2;color:#0d8b72;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">II квартал 2026</span></div>

<div class="roadmap-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Серверная обработка с сохранением в DOCS</strong>
    <p class="roadmap-card-copy">Модели можно выгружать из проводника или Revit Server напрямую в DOCS без открытия на рабочей машине.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-8">2026.8</a></p>
  </div>
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Расширенный экспорт в IFC</strong>
    <p class="roadmap-card-copy">Добавили экспорт всех видимых элементов, прогресс выполнения и передачу цветов TOOLS в IFC.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-8">2026.8</a></p>
  </div>
</div>

<div style="margin:18px 0 12px;"><span style="background:#e8f7f2;color:#0d8b72;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">IV квартал 2025</span></div>

<div class="roadmap-grid">
<!-- Источник: Что нового 2025.28 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Поддержка новых Revit и Navisworks</strong>
    <p class="roadmap-card-copy">Обновили совместимость плагинов и доработали серверную обработку, экспорт и команды работы с моделями.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-28">2025.28</a></p>
  </div>
</div>
</section>
</div>
</div>

## <span style="background:linear-gradient(45deg,#7aa6cf,#7d96ad);color:#fff;padding:3px 7px;border-radius:5px;font-weight:700;pointer-events:none;">API</span>

<div class="roadmap-state-tabs">
<span id="roadmap-state-api-plan" class="roadmap-state-anchor roadmap-state-plan-anchor"></span>
<span id="roadmap-state-api-release" class="roadmap-state-anchor roadmap-state-release-anchor"></span>
<nav class="roadmap-state-nav" aria-label="Состояние дорожной карты">
<a class="roadmap-state-tab roadmap-state-tab-plan" href="#roadmap-state-api-plan">Планы</a>
<a class="roadmap-state-tab roadmap-state-tab-release" href="#roadmap-state-api-release">Выпущено</a>
</nav>
<div class="roadmap-state-panels">
<section class="roadmap-state-panel roadmap-state-plan-panel">
<div style="margin:18px 0 12px;"><span style="background:#eaf0ff;color:#2156d9;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">III квартал 2026</span></div>

<div class="roadmap-grid roadmap-status-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
<!-- Tracker: HUB-468 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Свойства и атрибуты проектов</strong>
    <p class="roadmap-card-copy">Чтение и редактирование новых свойств и атрибутов проектов через публичный API.</p>
  </div>
<!-- Tracker: DOCS-1915 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Комментарий версии в согласованиях</strong>
    <p class="roadmap-card-copy">Работа с редактируемым комментарием версии согласования через реестр и публичный API.</p>
  </div>
<!-- Tracker: DOCS-1734, DOCS-566, DOCS-1822, DOCS-1908, DOCS-1914, HUB-249 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Новые методы HUB и DOCS</strong>
    <p class="roadmap-card-copy">Переименование файлов, изменение проектов и атрибутов, управление правами и создание согласований.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-12">2026.12</a> · <a href="/ru/general/updates/2026-14">2026.14</a> · <a href="/ru/general/updates/2026-15">2026.15</a> · <a href="/ru/general/updates/2026-16">2026.16</a></p>
  </div>
<!-- Tracker: ID-181 -->
  <div class="roadmap-card roadmap-status-ready">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Публичный API FORMS</strong>
    <p class="roadmap-card-copy">Чтение структуры форм, поиск, создание, изменение и завершение заполненных форм.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2026-16">2026.16</a></p>
  </div>
</div>

<div style="margin:18px 0 12px;"><span style="background:#eef2f6;color:#5d6878;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">IV квартал 2026</span></div>

<div class="roadmap-grid roadmap-status-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
<!-- Tracker: DOCS-1636, DOCS-2036 -->
  <div class="roadmap-card roadmap-status-planned">
    <div class="roadmap-card-status"><span class="roadmap-badge-planned">● В планах</span></div>
    <strong>Новые методы DOCS</strong>
    <p class="roadmap-card-copy">Копирование и перенос папок, а также создание замечаний через публичный API.</p>
  </div>
</div>
</section>
<section class="roadmap-state-panel roadmap-state-release-panel">
<div style="margin:18px 0 12px;"><span style="background:#e8f7f2;color:#0d8b72;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">II квартал 2026</span></div>

<div class="roadmap-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Расширение публичного API</strong>
    <p class="roadmap-card-copy">Добавили работу с замечаниями, передачами, пользователями и ролями, атрибутами файлов и папок, а также масками наименований.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-6">2026.6</a> · <a href="/ru/general/updates/2026-7">2026.7</a> · <a href="/ru/general/updates/2026-10">2026.10</a> · <a href="/ru/general/updates/2026-11">2026.11</a></p>
  </div>
</div>

<div style="margin:18px 0 12px;"><span style="background:#e8f7f2;color:#0d8b72;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">I квартал 2026</span></div>

<div class="roadmap-grid" style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin:14px 0 24px;">
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Новые методы публичного API</strong>
    <p class="roadmap-card-copy">Расширили интеграции с журналом HUB, согласованиями, передачами, публикациями, атрибутами, версиями файлов и замечаниями.</p>
    <p class="roadmap-release-links">В релизах: <a href="/ru/general/updates/2026-1">2026.1</a> · <a href="/ru/general/updates/2026-2">2026.2</a> · <a href="/ru/general/updates/2026-3">2026.3</a> · <a href="/ru/general/updates/2026-4">2026.4</a> · <a href="/ru/general/updates/2026-5">2026.5</a></p>
  </div>
</div>

<div style="margin:18px 0 12px;"><span style="background:#e8f7f2;color:#0d8b72;padding:4px 9px;border-radius:7px;font-weight:700;pointer-events:none;">IV квартал 2025</span></div>

<div class="roadmap-grid">
<!-- Источник: Что нового 2025.41 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>События замечаний</strong>
    <p class="roadmap-card-copy">Добавили метод получения событий по всем замечаниям проекта.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-41">2025.41</a></p>
  </div>
<!-- Источник: Что нового 2025.38 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Вложения замечаний</strong>
    <p class="roadmap-card-copy">Добавили загрузку и скачивание вложений замечаний через публичный API.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-38">2025.38</a></p>
  </div>
<!-- Источник: Что нового 2025.37 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Доступы к папкам</strong>
    <p class="roadmap-card-copy">Добавили методы назначения прав доступа к папкам.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-37">2025.37</a></p>
  </div>
<!-- Источник: Что нового 2025.36 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Дерево папок и обработка моделей</strong>
    <p class="roadmap-card-copy">Добавили методы дерева и раскраски папок и запуска обработки моделей Forge.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-36">2025.36</a></p>
  </div>
<!-- Источник: Что нового 2025.35 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Атрибуты замечаний</strong>
    <p class="roadmap-card-copy">Добавили получение атрибутов замечаний и их значений.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-35">2025.35</a></p>
  </div>
<!-- Источник: Что нового 2025.34 -->
  <div class="roadmap-card roadmap-card-release">
    <div class="roadmap-card-status"><span class="roadmap-badge-ready">● Готово</span></div>
    <strong>Согласования проекта</strong>
    <p class="roadmap-card-copy">Добавили получение согласований проекта.</p>
    <p class="roadmap-release-links">В релизе: <a href="/ru/general/updates/2025-34">2025.34</a></p>
  </div>
</div>
</section>
</div>
</div>

---

Кварталы в «Планах» отражают текущие ориентиры команды и не являются обязательством выпустить возможности в указанные сроки.

#
<sub>**[<   SIGNAL. Что нового](/ru/general/updates)     **|**     [SIGNAL. Публичный API   >](/ru/general/api)**</sub>
