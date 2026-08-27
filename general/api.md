---
title: SIGNAL. Публичный API
description: 
published: true
date: 2026-08-26T12:31:23.384Z
tags: general
editor: markdown
dateCreated: 2025-11-06T14:53:09.140Z
---

<sub>**[<   SIGNAL. Что нового](/ru/general/updates)     **|**     [HUB. Введение   >](/ru/hub/intro)**</sub>

<summary style="font-size: 16px; color: #0D47A1; background: #E3F2FD; border-radius: 7px; border: 1px solid #64B5F6; display: flex; gap: 10px; padding: 5px 16px; display: block; margin-top: 10px;">
<span style="flex-grow: 1;"> <a href="/general/api/updates" onclick="event.stopPropagation();" style="color: inherit; text-decoration: none;">🔄 Что нового (история изменений этого функционала)</a></span>
</summary>
  
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

- Кейсы с применением n8n:
[Интеграция SIGNAL DOCS с n8n](https://vkvideo.ru/video-230401166_456239022)
[Сбор аналитики в SIGNAL DOCS](https://vkvideo.ru/video-230401166_456239023)
[Ежедневный отчет в Telegram по событиям в SIGNAL DOCS](https://vkvideo.ru/video-230401166_456239026)

## Авторизация в Swagger
###### Авторизация в Swagger {#swagger}

1. Добавьте интеграцию в [настройках компании в HUB](/hub/admin#settings). Выберите **scopes**, к которым хотите предоставить доступ через API в рамках этой интеграции. При необходимости ограничьте срок действия интеграции. Нажмите **Сохранить**:
![auth_swagger_1.png](/api/auth_swagger_1.png)
  
2. Скопируйте **Secret key**. При утрате его можно сбросить:
![auth_swagger_2.png](/api/auth_swagger_2.png)

3. Нажмите на значок :eye: у добавленной интеграции и скопируйте **clientId** и названия выбранных **scopes**:
![auth_swagger_4.png](/api/auth_swagger_4.png)
  
4. Откройте [Swagger](https://api.sgnl.pro/openapi/swagger/index.html). Если вы уже авторизованы — отображается закрытый замок — выполните **Logout**:
![auth_swagger_3.png](/api/auth_swagger_3.png)

5. Раскройте метод **`/public/v1/auth/token`**, нажмите **Try it out** и вставьте в поле **Edit Value** скопированные **clientId**, **clientSecret** и список **scopes**. Каждый scope в списке нужно заключить в кавычки. Нажмите **Execute**:
![auth_swagger_5.png](/api/auth_swagger_5.png)

6. При успешном выполнении запроса — код `200` — скопируйте значение поля **token** из ответа. Токен действует один час; затем снова выполните запрос и получите новый токен:
![auth_swagger_6.png](/api/auth_swagger_6.png)

7. Нажмите **Authorize**, вставьте скопированный токен и ещё раз нажмите **Authorize**:
![auth_swagger_7.png](/api/auth_swagger_7.png)
  
Поздравляем, вы авторизованы. Теперь можно использовать методы, соответствующие выбранным для интеграции scopes.

<sub>**[<   SIGNAL. Что нового](/ru/general/updates)     **|**     [HUB. Введение   >](/ru/hub/intro)**</sub>