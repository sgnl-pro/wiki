---
title: SIGNAL. Публичный API
description: 
published: true
date: 2025-11-17T10:20:53.856Z
tags: 
editor: markdown
dateCreated: 2025-11-06T14:53:09.140Z
---

<sub>**[<   SIGNAL. Что нового](/ru/general/updates)     **|**     [HUB. Введение   >](/ru/hub/intro)**</sub>

<details>
<summary>Что нового</summary>

**[2025.35](/general/updates/2025-35)** ^13.11.2025^
- Добавили методы получения атрибутов и их значений у замечаний.
  
**[2025.34](/general/updates/2025-34)** ^06.11.2025^
- Добавили методы получения согласований проекта.
  
**[2025.33](/general/updates/2025-33)** ^30.10.2025^
- Добавили методы для работы с замечаниями, деревом папок (в том числе назначение доступов) и получения списка сотрудников и ролей.

> Информация о более ранних обновлениях доступна в закрытом Telegam канале для пользователей SIGNAL. Для добавления **[обращайтесь в поддержку](/general/support)**.
{.is-info}

</details>  
  
----

# Вкладки{.tabset}
## Документация
###### Документация {#doc}
  
- Swagger: https://api.sgnl.pro/openapi/swagger/index.html
- ReDoc: https://api.sgnl.pro/openapi/redoc-v1/index.html
  
## Примеры
###### Примеры {#examples}
  
- Авторизация:
[GoogleScript](https://vkvideo.ru/video890470724_456239019)
[IronPython](https://vkvideo.ru/video890470724_456239020)
[1С](https://vkvideo.ru/video890470724_456239021)
  
- Загрузка и скачивание файлов из DOCS:
[PowerShell](https://vkvideo.ru/video-230401166_456239017)
[VBA Excel](https://vkvideo.ru/video-230401166_456239018)
[Python](https://vkvideo.ru/video-230401166_456239019)

- [Сбор аналитики в SIGNAL DOCS с помощью n8n](https://vkvideo.ru/video-230401166_456239023)
  
## Авторизация в Swagger
###### Авторизация в Swagger {#swagger}

1. Добавьте интеграцию в [настройках компании в HUB](/hub/admin#settings). Выберите **scopes,** к которым хотите иметь доступ через API в рамках этой интеграции. При необходимости ограничьте срок действия интеграции. Нажмите **Сохранить:**
![auth_swagger_1.png](/api/auth_swagger_1.png)
  
2. Скопируйте **Secret key** (при утрате его можно будет сбросить):
![auth_swagger_2.png](/api/auth_swagger_2.png)

3. Нажмите на глазик :eye: у добавленной интеграции, скопируйте **clientId** и названия выбранных **scopes:**
![auth_swagger_4.png](/api/auth_swagger_4.png)
  
4. Зайдите в [Swagger](https://api.sgnl.dev/openapi/swagger/index.html) и при наличии авторизации (закрытого замочка) выполните **Logout:**
![auth_swagger_3.png](/api/auth_swagger_3.png)

5. Раскройте метод **/public/v1/auth/token** (самый первый), нажмите **Try it out** и вставьте в поле **Edit Value** скопированные ранее **clientId, clientSecret** и список **scopes** (обратите внимание, что каждый **scope** в списке нужно брать в кавычки). Нажмите **Execute:**
![auth_swagger_5.png](/api/auth_swagger_5.png)

6. При успешном выполнении запроса (Code 200) скопируйте значение поля **token** из ответа (обратите внимание, что токен сбрасывается через час, затем нужно будет повторно нажать **Execute** и получить новый токен):
![auth_swagger_6.png](/api/auth_swagger_6.png)

7. Нажмите **Authorize,** вставьте скопированный токен и затем снова **Authorize:**
![auth_swagger_7.png](/api/auth_swagger_7.png)
  
Поздравляем, вы авторизованы! Теперь можете использовать методы, соответствующие выбранным в рамках этой интеграции скоупам.

<sub>**[<   SIGNAL. Что нового](/ru/general/updates)     **|**     [HUB. Введение   >](/ru/hub/intro)**</sub>