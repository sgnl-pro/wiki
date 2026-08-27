---
title: SIGNAL. Публичный API — История изменений
description: 
published: true
date: 2026-08-31T00:00:00.000Z
tags: general
editor: markdown
dateCreated: 2026-08-31T00:00:00.000Z
---

<summary style="font-size: 16px; color: #0D47A1; background: #E3F2FD; border-radius: 7px; border: 1px solid #64B5F6; display: flex; gap: 10px; padding: 5px 16px; display: block; margin-top: 10px;">
<span style="flex-grow: 1;"> <a href="/general/api" onclick="event.stopPropagation();" style="color: inherit; text-decoration: none;">См. также основную статью <b>SIGNAL. Публичный API</b></a></span>
</summary>

> Здесь перечислены основные изменения. Для получения подробностей нажмите на номер версии.
{.is-info}

**Обозначения**
:fire: — новые возможности
:sparkles: — доработки функционала
:hammer_and_wrench: — исправление ошибок

----
**[2026.16](/general/updates/2026-16)** ^31.08.2026^

:fire: Добавили методы API FORMS для чтения типов форм, групп, полей и этапов, поиска и получения заполненных форм, а также создания, изменения и завершения форм.

:sparkles: В ответах DOCS добавили идентификатор версии элемента `ItemVersionId`, а также номер и даты последней итерации согласования.

----
**[2026.15](/general/updates/2026-15)** ^17.08.2026^

:sparkles: В API DOCS добавили методы изменения проектов и атрибутов, управления правами на папки, работы с комплектами согласования и запуска согласования.

----
**[2026.12](/general/updates/2026-12)** ^02.07.2026^

:sparkles: Добавили метод переименования файлов.

----
**[2026.11](/general/updates/2026-11)** ^18.06.2026^

:sparkles: Добавили метод получения значений атрибутов папок.

----
**[2026.10](/general/updates/2026-10)** ^04.06.2026^

:sparkles: Добавили методы для добавления и редактирования пользователей и их ролей в компании и проектах (контроллеры `ApplicationUser`, `CompanyUser`, `CompanyUserCustomRole`, `ProjectUser`, `ProjectUserCustomRole`), метод `/public/v1/attributes/values/items` для получения значений атрибутов файлов и метод `/public/v1/naming-patterns/folder-items/find` для получения масок у папки.

----
**[2026.7](/general/updates/2026-7)** ^23.04.2026^

:sparkles: Добавили параметр `urlTtlSecOverride` в `GET /v1/items/download`, поле `urn` в `POST /public/v1/forge/item-versions/viewer`, методы для редактирования замечаний и поля `added`, `addedBy` в `POST /public/v1/documents-transfers`.

----
**[2026.6](/general/updates/2026-6)** ^09.04.2026^

:sparkles: Добавили поля `stage.completedPlanDate` и `scenario` в `ReviewVersion`, а также `customRoleIds` в `/public/v1/projects/{projectId}/users`.

:hammer_and_wrench: Исправили вызов `Review.List` и кэширование добавленных в интеграцию проектов.

----
**[2026.5](/general/updates/2026-5)** ^26.03.2026^

:sparkles: Добавили методы `/public/v1/items/versions/update`, `/public/v1/items/item-version`, `/public/v1/issues/comments` и поле `ItemVersion` в замечаниях.

----
**[2026.4](/general/updates/2026-4)** ^12.03.2026^

:sparkles: Добавили методы `/public/v1/attributes`, `/public/v1/attributes/values/set` и `/public/v1/reviews/items`.

----
**[2026.3](/general/updates/2026-3)** ^02.03.2026^

:sparkles: Добавили контроллер `Share` и метод `/public/v1/permissions/tree` для публикации папок и файлов.

----
**[2026.2](/general/updates/2026-2)** ^12.02.2026^

:sparkles: Добавили фильтр `ItemVersionId` в `POST /public/v1/issues`, поля завершившего этап пользователя, методы получения версий согласования и групп согласований, а также поля договорной даты и даты начала итерации.

----
**[2026.1](/general/updates/2026-1)** ^22.01.2026^

:sparkles: Добавили методы журнала событий HUB, поле `code` проекта, обновление комплектов согласования, получение итераций, сведения о завершившем этап пользователе и методы для работы с пакетами передачи.

----
**[2025.41](/general/updates/2025-41)** ^25.12.2025^

:sparkles: Добавили метод получения событий по всем замечаниям проекта.

----
**[2025.39](/general/updates/2025-39)** ^11.12.2025^

:hammer_and_wrench: Исправили метод `public/v1/projects/{projectId}/users`.

----
**[2025.37](/general/updates/2025-37)** ^27.11.2025^

:sparkles: Добавили методы назначения доступов на папки.

----
**[2025.36](/general/updates/2025-36)** ^20.11.2025^

:sparkles: Добавили методы получения дерева папок, раскраски папок и обработки моделей Forge.

----
**[2025.35](/general/updates/2025-35)** ^13.11.2025^

:sparkles: Добавили методы получения атрибутов и их значений у замечаний.

----
**[2025.34](/general/updates/2025-34)** ^06.11.2025^

:sparkles: Добавили методы получения согласований проекта.

----
**[2025.33](/general/updates/2025-33)** ^30.10.2025^

:sparkles: Добавили методы для работы с замечаниями, деревом папок, доступами и получения списка сотрудников и ролей.

> Информация о более ранних обновлениях доступна в закрытом Telegram-канале для пользователей SIGNAL. Для добавления [обращайтесь в поддержку](/general/support).
{.is-info}