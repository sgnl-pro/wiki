---
title: Api New
description: 
published: true
date: 2026-11-20T15:18:44.956Z
tags: 
editor: markdown
dateCreated: 2026-11-17T13:04:57.412Z
---

<sub>**[<   SIGNAL. Что нового](/ru/general/updates)     **|**     [HUB. Введение   >](/ru/hub/intro)**</sub>

<summary style="font-size: 16px; color: #0D47A1; background: #E3F2FD; border-radius: 7px; border: 1px solid #64B5F6; display: flex; gap: 10px; padding: 5px 16px; display: block; margin-top: 10px;">
<span style="flex-grow: 1;"> <a href="/general/api/updates" onclick="event.stopPropagation();" style="color: inherit; text-decoration: none;">Что нового в API</a></span>
</summary>

> Через API можно работать с файлами, замечаниями, согласованиями и другими данными SIGNAL из своей системы.
{.is-info}

<div class="toc-grid">
  <div class="toc-card toc-green">
    <h4 class="toc-card-title"><a href="#doc">1. Начало работы</a></h4>
    <ul class="toc-list">
      <li><a href="#api-docs"><span class="toc-badge">1.1</span> Адрес и документация</a></li>
      <li><a href="#swagger"><span class="toc-badge">1.2</span> Подключение и авторизация в Swagger</a></li>
      <li><a href="#api-rules"><span class="toc-badge">1.3</span> Запросы, ответы и ограничения</a></li>
    </ul>
  </div>
  <div class="toc-card toc-green">
    <h4 class="toc-card-title"><a href="#examples">2. Примеры</a></h4>
    <ul class="toc-list">
      <li><a href="#example-setup"><span class="toc-badge">2.1</span> Подготовка</a></li>
      <li><a href="#example-auth"><span class="toc-badge">2.2</span> Авторизация</a></li>
      <li><a href="#example-upload"><span class="toc-badge">2.3</span> Загрузка файла</a></li>
      <li><a href="#example-download"><span class="toc-badge">2.4</span> Скачивание файла</a></li>
      <li><a href="#example-review"><span class="toc-badge">2.5</span> Данные согласования</a></li>
      <li><a href="#example-issues"><span class="toc-badge">2.6</span> Реестр замечаний</a></li>
      <li><a href="#example-videos"><span class="toc-badge">2.7</span> Видео и интеграции</a></li>
    </ul>
  </div>
  <div class="toc-card toc-green">
    <h4 class="toc-card-title"><a href="#reference">3. Справочник API</a></h4>
    <ul class="toc-list">
      <li><a href="#reference-v1"><span class="toc-badge">3.1</span> Файлы и версии</a></li>
      <li><a href="#reference-folders"><span class="toc-badge">3.2</span> Папки и доступ</a></li>
      <li><a href="#reference-issues"><span class="toc-badge">3.3</span> Замечания</a></li>
      <li><a href="#reference-reviews"><span class="toc-badge">3.4</span> Согласования</a></li>
      <li><a href="#reference-transfers"><span class="toc-badge">3.5</span> Передачи</a></li>
      <li><a href="#reference-forms"><span class="toc-badge">3.6</span> Формы</a></li>
      <li><a href="#reference-attributes"><span class="toc-badge">3.7</span> Атрибуты</a></li>
      <li><a href="#reference-access"><span class="toc-badge">3.8</span> Компания и проекты</a></li>
      <li><a href="#reference-models"><span class="toc-badge">3.9</span> Модели и подписи</a></li>
      <li><a href="#reference-modules"><span class="toc-badge">3.10</span> Другие модули</a></li>
      <li><a href="#reference-v2"><span class="toc-badge">3.11</span> Методы v2</a></li>
      <li><a href="#reference-errors"><span class="toc-badge">3.12</span> Коды ответов</a></li>
    </ul>
  </div>
</div>

----

# Вкладки {.tabset}
## Начало работы
###### 1. Начало работы {#doc}

### Подразделы {.tabset}

#### Документация
###### 1.1. Адрес и документация {#api-docs}

Адрес API — `https://api.sgnl.pro`. Версия входит в путь запроса, например `/public/v1/projects`.

- ReDoc — документация [v1](https://api.sgnl.pro/openapi/redoc-v1/index.html) и [v2](https://api.sgnl.pro/openapi/redoc-v2/index.html).
- [Swagger](https://api.sgnl.pro/openapi/swagger/index.html) — запуск запросов.

#### Вход в Swagger
###### 1.2. Подключение и авторизация в Swagger {#swagger}

1. Откройте [настройки компании в HUB](/hub/admin#settings) и добавьте интеграцию. Выберите разрешения (scopes) для нужных методов. При необходимости задайте срок действия интеграции. Нажмите **Сохранить**.

   ![Создание интеграции](/api/auth_swagger_1.png)

2. Скопируйте **Secret key**. Если ключ утерян, его можно сбросить в настройках интеграции.

   ![Ключ интеграции](/api/auth_swagger_2.png)

3. Нажмите :eye: у интеграции и скопируйте `clientId` и названия разрешений.

   ![Идентификатор и разрешения интеграции](/api/auth_swagger_4.png)

4. Откройте [Swagger](https://api.sgnl.pro/openapi/swagger/index.html). Если у кнопки **Authorize** закрытый замок, нажмите её и выберите **Logout**.

   ![Выход из текущей авторизации](/api/auth_swagger_3.png)

5. Откройте **POST /public/v1/auth/token** и нажмите **Try it out**. В **Edit Value** укажите `clientId`, `clientSecret` и массив `scopes`. Включите в массив разрешения из колонки **Scope** для методов, которые будете вызывать. Нажмите **Execute**.

   ![Запрос токена](/api/auth_swagger_5.png)

6. Если Swagger вернул `200`, скопируйте значение `token`. Поле `expiresIn` показывает срок действия токена в секундах. По истечении этого срока запросите токен снова.

   ![Ответ с токеном](/api/auth_swagger_6.png)

7. Нажмите **Authorize**, вставьте токен и нажмите **Authorize** ещё раз.

   ![Ввод токена в Swagger](/api/auth_swagger_7.png)

#### Запросы
###### 1.3. Запросы, ответы и ограничения {#api-rules}

В запросах к API передавайте токен в заголовке `Authorization: Bearer <token>`. Для тела в формате JSON используйте `Content-Type: application/json`.

- В методах с `Take` и `Skip` увеличивайте `Skip` на число полученных записей. Для списка согласований `Take` — до 50, для списка замечаний — до 200.
- Для передачи файлов используйте `signedUrl` из билета. Ссылка действует `ttlSec` секунд. Заголовок `Authorization` нужен в запросе к API за билетом. В хранилище передавайте только подписанную ссылку.
- При `429` повторите запрос после паузы, указанной в `Retry-After`. Если сервер не ответил на запрос записи, проверьте результат перед повтором.

## Примеры
###### 2. Примеры {#examples}

### Подразделы {.tabset}

#### Подготовка
###### 2.1. Подготовка {#example-setup}

Для Python 3.10 и новее установите `requests` командой `python -m pip install requests`. На macOS используйте `python3`, если команды `python` нет. Примеры JavaScript запускаются в Node.js 22 и новее.

Сохраните файл авторизации и нужный скрипт в одну папку. В переменных окружения укажите `SIGNAL_CLIENT_ID` и `SIGNAL_CLIENT_SECRET` из HUB.

| Сценарий | Необходимые разрешения интеграции |
| --- | --- |
| [Загрузка файла](#example-upload) | `docs:object:create`, `docs:version:create`, `docs:item:create` |
| [Скачивание файла](#example-download) | `docs:item:read`. Для поиска последней версии добавьте `docs:version:list`. |
| [Данные согласования](#example-review) | `docs:review:list` |
| [Реестр замечаний](#example-issues) | `docs:issue:list` |

Идентификаторы для примеров можно получить через API.

| Что нужно найти | Запрос |
| --- | --- |
| Проект | [`GET /public/v1/projects`](https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Project/operation/ProjectListV1) |
| Папка | [`GET /public/v1/projects/{projectId}/folders/tree`](https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Folder/operation/FolderGetProjectTreeV1) |
| Файл | [`GET /public/v1/items`](https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Item/operation/ItemListV1) |
| Версия файла | [`GET /public/v1/versions`](https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Version/operation/VersionListV1) |
| Согласование | [`POST /public/v1/reviews`](https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Review/operation/ReviewListV1) |

Разрешения для этих запросов указаны в [справочнике](#reference). Файлы с результатами сохраняются в папке запуска, если Вы не указали другой путь. При совпадении имён скрипт перезапишет выходные файлы.

#### Авторизация
###### 2.2. Авторизация {#example-auth}

Запустите этот пример, чтобы проверить ключ интеграции и выбранные разрешения. Сохраните файл `signal_api.py` или `signal_api.mjs` рядом со скриптами, которые будут пользоваться API.

Для отдельной проверки задайте `SIGNAL_SCOPES` — разрешения через пробел, например `docs:item:read`. При успешном запуске в терминале появится срок действия токена в секундах. Остальные скрипты запрашивают свои разрешения автоматически.

**Python** — `signal_api.py`. Запуск — `python signal_api.py`.

```python
import os

import requests

BASE_URL = os.environ.get("SIGNAL_API_URL", "https://api.sgnl.pro").rstrip("/")


# Запрашиваем токен только с разрешениями, нужными для этого сценария.
def get_token(scopes):
    response = requests.post(
        f"{BASE_URL}/public/v1/auth/token",
        json={
            "clientId": os.environ["SIGNAL_CLIENT_ID"],
            "clientSecret": os.environ["SIGNAL_CLIENT_SECRET"],
            "scopes": scopes,
        },
        timeout=30,
        allow_redirects=False,
    )
    if response.status_code != 200:
        raise RuntimeError(f"Получение токена: HTTP {response.status_code}")
    return response.json()


# Передаём токен в заголовке Authorization. Для ответа без тела возвращаем пустое значение.
def api_request(token, method, path, *, body=None, params=None):
    response = requests.request(
        method, BASE_URL + path,
        headers={"Authorization": f"Bearer {token}"},
        json=body, params=params, timeout=60, allow_redirects=False,
    )
    if not 200 <= response.status_code < 300:
        raise RuntimeError(f"{method} {path}: HTTP {response.status_code}")
    return response.json() if response.content else None


# При прямом запуске проверяем авторизацию и выводим только срок действия токена.
if __name__ == "__main__":
    auth = get_token(os.environ["SIGNAL_SCOPES"].split())
    print("Токен получен. Срок действия в секундах:", auth["expiresIn"])
```

**Node.js** — `signal_api.mjs`. Запуск — `node signal_api.mjs`.

```javascript
import { pathToFileURL } from "node:url";

const baseUrl = (process.env.SIGNAL_API_URL || "https://api.sgnl.pro").replace(/\/+$/, "");

export function env(name) {
  const value = process.env[name];
  if (!value) throw new Error("Задайте переменную " + name);
  return value;
}

// Запрашиваем токен только с разрешениями, нужными для этого сценария.
export async function getToken(scopes) {
  const response = await fetch(baseUrl + "/public/v1/auth/token", {
    method: "POST",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify({
      clientId: env("SIGNAL_CLIENT_ID"),
      clientSecret: env("SIGNAL_CLIENT_SECRET"),
      scopes,
    }),
    signal: AbortSignal.timeout(30000),
    redirect: "error",
  });
  if (response.status !== 200) throw new Error("Получение токена: HTTP " + response.status);
  return response.json();
}

// Передаём токен в заголовке Authorization. Для ответа без тела возвращаем пустое значение.
export async function apiRequest(token, method, path, { body, params } = {}) {
  const url = new URL(baseUrl + path);
  if (params) url.search = new URLSearchParams(params).toString();
  const headers = { Authorization: `Bearer ${token}` };
  if (body !== undefined) headers["Content-Type"] = "application/json";
  const response = await fetch(url, {
    method, headers, body: JSON.stringify(body), redirect: "error",
    signal: AbortSignal.timeout(60000),
  });
  if (!response.ok) throw new Error(`${method} ${path}: HTTP ${response.status}`);
  const text = await response.text();
  return text ? JSON.parse(text) : null;
}

// При прямом запуске проверяем авторизацию и выводим только срок действия токена.
if (process.argv[1] && import.meta.url === pathToFileURL(process.argv[1]).href) {
  const auth = await getToken(env("SIGNAL_SCOPES").trim().split(/\s+/));
  console.log("Токен получен. Срок действия в секундах:", auth.expiresIn);
}
```

#### Загрузка
###### 2.3. Загрузка файла {#example-upload}

Используйте пример, чтобы загрузить локальный файл в выбранную папку DOCS. В папке появится новый файл, а в терминале — идентификаторы объекта, версии и файла.

Укажите `SIGNAL_PROJECT_ID`, `SIGNAL_FOLDER_ID` и путь к файлу в `SIGNAL_FILE`. Папка должна находиться в указанном проекте. Допустимый размер файла — от 10 байт до 5 ГиБ. При необходимости задайте `SIGNAL_MIME_TYPE`, например `application/pdf`. Если папка использует правило именования, задайте `SIGNAL_NAMING_PATTERN_ID` и выберите имя файла по этому правилу.

Если загрузка прервалась, сверяйтесь с выведенными идентификаторами перед повторным запуском. Для добавления версии к существующему файлу найдите в справочнике `PUT /public/v1/items/versions`.

**Python** — `upload.py`. Запуск — `python upload.py`.

```python
import mimetypes
import os
from pathlib import Path
import requests
from signal_api import api_request, get_token

source = Path(os.environ["SIGNAL_FILE"])
project_id = os.environ["SIGNAL_PROJECT_ID"]
folder_id = os.environ["SIGNAL_FOLDER_ID"]
if not source.is_file():
    raise ValueError("Укажите локальный файл")
size = source.stat().st_size
if not 10 <= size <= 5368709120:
    raise ValueError("Размер файла должен быть от 10 байт до 5 ГиБ")
mime_type = (
    os.environ.get("SIGNAL_MIME_TYPE")
    or mimetypes.guess_type(source.name)[0]
    or "application/octet-stream"
)

token = get_token(["docs:object:create", "docs:version:create", "docs:item:create"])["token"]

# Получаем подписанную ссылку для загрузки содержимого в хранилище.
ticket = api_request(token, "PUT", "/public/v1/objects", body={
    "projectId": project_id, "mimeType": mime_type, "size": size,
})
object_id = ticket["objectId"]
print("objectId:", object_id, flush=True)
# Передаём файл потоком. Запрос идёт в хранилище по подписанной ссылке.
with source.open("rb") as content:
    try:
        response = requests.put(
            ticket["signedUrl"], data=content, headers={"Content-Type": mime_type},
            timeout=300, allow_redirects=False,
        )
    except requests.RequestException:
        raise RuntimeError("Передача файла в хранилище прервалась") from None
if not 200 <= response.status_code < 300:
    raise RuntimeError(f"Загрузка в хранилище: HTTP {response.status_code}")
# Подтверждаем загрузку объекта перед созданием версии.
api_request(token, "POST", f"/public/v1/objects/{object_id}/uploading/commit")
# Создаём версию, которая ссылается на загруженный объект.
version = api_request(token, "POST", "/public/v1/versions", body={
    "objectId": object_id, "projectId": project_id, "name": source.name,
})
print("versionId:", version["data"], flush=True)
# Добавляем файл в папку и прикрепляем к нему созданную версию.
file_item = {"folderId": folder_id, "versionId": version["data"], "name": source.name}
naming_pattern_id = os.environ.get("SIGNAL_NAMING_PATTERN_ID")
if naming_pattern_id:
    file_item["namingPatternId"] = naming_pattern_id
item = api_request(token, "PUT", "/public/v1/items/file", body=file_item)
print("itemId:", item["data"])
```

**Node.js** — `upload.mjs`. Запуск — `node upload.mjs`.

```javascript
import { createReadStream } from "node:fs";
import { stat } from "node:fs/promises";
import { basename } from "node:path";
import { apiRequest, env, getToken } from "./signal_api.mjs";

const source = env("SIGNAL_FILE");
const projectId = env("SIGNAL_PROJECT_ID");
const folderId = env("SIGNAL_FOLDER_ID");
const name = basename(source);
const file = await stat(source);
if (!file.isFile()) throw new Error("Укажите локальный файл");
const { size } = file;
if (size < 10 || size > 5368709120) throw new Error("Размер файла: от 10 байт до 5 ГиБ");
const mimeType = process.env.SIGNAL_MIME_TYPE || "application/octet-stream";
const { token } = await getToken(["docs:object:create", "docs:version:create", "docs:item:create"]);
// Получаем подписанную ссылку для загрузки содержимого в хранилище.
const ticket = await apiRequest(token, "PUT", "/public/v1/objects", {
  body: { projectId, mimeType, size },
});
console.log("objectId:", ticket.objectId);
// Передаём файл потоком. Запрос идёт в хранилище по подписанной ссылке.
const stream = createReadStream(source);
try {
  const response = await fetch(ticket.signedUrl, {
    method: "PUT", body: stream, duplex: "half",
    headers: { "Content-Type": mimeType, "Content-Length": String(size) },
    signal: AbortSignal.timeout(300000), redirect: "error",
  }).catch(() => { throw new Error("Передача файла в хранилище прервалась"); });
  if (!response.ok) throw new Error("Загрузка в хранилище: HTTP " + response.status);
} finally {
  stream.destroy();
}
// Подтверждаем загрузку объекта перед созданием версии.
await apiRequest(token, "POST", "/public/v1/objects/" + ticket.objectId + "/uploading/commit");
// Создаём версию, которая ссылается на загруженный объект.
const version = await apiRequest(token, "POST", "/public/v1/versions", {
  body: { objectId: ticket.objectId, projectId, name },
});
console.log("versionId:", version.data);
// Добавляем файл в папку и прикрепляем к нему созданную версию.
const body = { folderId, versionId: version.data, name };
if (process.env.SIGNAL_NAMING_PATTERN_ID) {
  body.namingPatternId = process.env.SIGNAL_NAMING_PATTERN_ID;
}
const item = await apiRequest(token, "PUT", "/public/v1/items/file", { body });
console.log("itemId:", item.data);
```

#### Скачивание
###### 2.4. Скачивание файла {#example-download}

Используйте пример, чтобы скачать файл из DOCS по ссылке на него. Укажите ссылку вида `https://docs.sgnl.pro/projects/…/folders/…/items/…` в `SIGNAL_DOCS_URL` или задайте ID файла в `SIGNAL_ITEM_ID`.

По умолчанию скрипт скачает последнюю версию. Для этого интеграции нужны `docs:version:list` и `docs:item:read`. Если нужна конкретная версия, укажите `SIGNAL_VERSION_ID` — поле `id` нужной записи из `GET /public/v1/versions`. Тогда достаточно `docs:item:read`.

Файл появится локально после завершения скачивания. В `SIGNAL_OUTPUT` задайте путь с нужным расширением, например `document.pdf`. По умолчанию файл сохранится как `download.bin`.

**Python** — `download.py`. Запуск — `python download.py`.

```python
import os
import re
from pathlib import Path
from tempfile import NamedTemporaryFile
from urllib.parse import urlsplit
from uuid import UUID

import requests
from signal_api import api_request, get_token

destination = Path(os.environ.get("SIGNAL_OUTPUT", "download.bin"))
item_id = os.environ.get("SIGNAL_ITEM_ID")

# Ссылка DOCS нужна только для извлечения ID файла.
if not item_id:
    path = urlsplit(os.environ["SIGNAL_DOCS_URL"]).path
    match = re.search(r"/items/([^/]+)", path)
    if not match:
        raise ValueError("В ссылке DOCS должен быть путь /items/<ID файла>")
    item_id = match.group(1)
item_id = str(UUID(item_id))

# Если версия не задана, запрашиваем только первую запись списка версий.
version_id = os.environ.get("SIGNAL_VERSION_ID")
scopes = ["docs:item:read"]
if version_id:
    version_id = str(UUID(version_id))
else:
    scopes.append("docs:version:list")

token = get_token(scopes)["token"]
if not version_id:
    versions = api_request(token, "GET", "/public/v1/versions", params={
        "itemId": item_id, "Take": 1,
    })
    if not versions:
        raise RuntimeError("У файла нет доступных версий")
    version_id = versions[0]["id"]

# API возвращает подписанную ссылку. Сам файл скачиваем из хранилища без токена.
ticket = api_request(token, "GET", "/public/v1/items/download", params={
    "itemId": item_id, "versionId": version_id,
})

# Пишем во временный файл. Меняем итоговый файл только по завершении скачивания.
temporary = None
try:
    with requests.get(ticket["signedUrl"], stream=True, timeout=(10, 120)) as response:
        if response.status_code != 200:
            raise RuntimeError(f"Скачивание из хранилища: HTTP {response.status_code}")
        with NamedTemporaryFile(dir=destination.parent, suffix=".part", delete=False) as output:
            temporary = Path(output.name)
            for chunk in response.iter_content(chunk_size=1024 * 1024):
                output.write(chunk)
    temporary.replace(destination)
except requests.RequestException:
    raise RuntimeError("Скачивание из хранилища прервалось") from None
finally:
    if temporary is not None:
        temporary.unlink(missing_ok=True)

print("Файл сохранён:", destination)
```

**Node.js** — `download.mjs`. Запуск — `node download.mjs`.

```javascript
import { createWriteStream } from "node:fs";
import { mkdtemp, rename, rm } from "node:fs/promises";
import { dirname, join } from "node:path";
import { Readable } from "node:stream";
import { pipeline } from "node:stream/promises";
import { apiRequest, env, getToken } from "./signal_api.mjs";

function uuid(value) {
  if (!/^[a-f\d]{8}-(?:[a-f\d]{4}-){3}[a-f\d]{12}$/i.test(value)) {
    throw new Error("Ожидается идентификатор в формате UUID");
  }
  return value.toLowerCase();
}

const destination = process.env.SIGNAL_OUTPUT || "download.bin";
let itemId = process.env.SIGNAL_ITEM_ID;

// Ссылка DOCS нужна только для извлечения ID файла.
if (!itemId) {
  const path = new URL(env("SIGNAL_DOCS_URL")).pathname;
  const match = path.match(/\/items\/([^/]+)/);
  if (!match) throw new Error("В ссылке DOCS должен быть путь /items/<ID файла>");
  itemId = match[1];
}
itemId = uuid(itemId);

// Если версия не задана, запрашиваем только первую запись списка версий.
let versionId = process.env.SIGNAL_VERSION_ID;
const scopes = ["docs:item:read"];
if (versionId) {
  versionId = uuid(versionId);
} else {
  scopes.push("docs:version:list");
}

const { token } = await getToken(scopes);
if (!versionId) {
  const versions = await apiRequest(token, "GET", "/public/v1/versions", {
    params: { itemId, Take: 1 },
  });
  if (!versions.length) throw new Error("У файла нет доступных версий");
  versionId = versions[0].id;
}

// API возвращает подписанную ссылку. Сам файл скачиваем из хранилища без токена.
const ticket = await apiRequest(token, "GET", "/public/v1/items/download", {
  params: { itemId, versionId },
});
const response = await fetch(ticket.signedUrl, {
  signal: AbortSignal.timeout(300000),
}).catch(() => { throw new Error("Запрос к хранилищу не выполнен"); });
if (response.status !== 200 || !response.body) {
  throw new Error("Скачивание из хранилища: HTTP " + response.status);
}

// Пишем во временный файл. Меняем итоговый файл только по завершении скачивания.
const directory = await mkdtemp(join(dirname(destination), ".signal-download-"));
const temporary = join(directory, "download.part");
try {
  await pipeline(Readable.fromWeb(response.body), createWriteStream(temporary));
  await rename(temporary, destination);
} finally {
  await rm(directory, { recursive: true, force: true });
}
console.log("Файл сохранён:", destination);
```

#### Согласования
###### 2.5. Данные согласования {#example-review}

Используйте пример, чтобы собрать данные для своего отчёта по согласованию. Задайте `SIGNAL_PROJECT_ID` и `SIGNAL_REVIEW_ID`. Результат сохранится в `review.json`. Для другого имени задайте `SIGNAL_OUTPUT`.

- `review` — данные согласования. Этапы и подписания последней версии находятся в `topVersion.stages` и `topVersion.signings`.
- `itemVersionIdsByReviewVersion` — список идентификаторов версий файлов для этой версии согласования. Ключ словаря — идентификатор версии согласования.

Для другой версии согласования используйте `POST /public/v1/reviews/versions`. Детали конкретной версии элемента возвращает `GET /public/v1/items/item-version`.

**Python** — `review.py`. Запуск — `python review.py`.

```python
import json
import os
from pathlib import Path
from signal_api import api_request, get_token

review_id = os.environ["SIGNAL_REVIEW_ID"]
project_id = os.environ["SIGNAL_PROJECT_ID"]
token = get_token(["docs:review:list"])["token"]

# Ищем одно согласование. Идентификаторы передаём внутри поля find.
reviews = api_request(token, "POST", "/public/v1/reviews", body={
    "find": {"projectId": project_id, "ids": [review_id]},
}, params={"Take": 1, "Skip": 0})
if len(reviews) != 1 or reviews[0]["id"].lower() != review_id.lower():
    raise RuntimeError("Указанное согласование не найдено")
review = reviews[0]
# По ID последней версии согласования запрашиваем ID версий вошедших в него файлов.
version_id = review["topVersion"]["id"]
item_versions = api_request(token, "POST", "/public/v1/reviews/versions/item-versions", body={
    "reviewVersionIds": [version_id],
})
# Записываем оба ответа в один JSON-файл.
result = {"review": review, "itemVersionIdsByReviewVersion": item_versions}
destination = Path(os.environ.get("SIGNAL_OUTPUT", "review.json"))
destination.write_text(json.dumps(result, ensure_ascii=False, indent=2), encoding="utf-8")
print("Данные согласования сохранены:", destination)
```

**Node.js** — `review.mjs`. Запуск — `node review.mjs`.

```javascript
import { writeFile } from "node:fs/promises";
import { apiRequest, env, getToken } from "./signal_api.mjs";

const reviewId = env("SIGNAL_REVIEW_ID");
const projectId = env("SIGNAL_PROJECT_ID");
const { token } = await getToken(["docs:review:list"]);
// Ищем одно согласование. Идентификаторы передаём внутри поля find.
const reviews = await apiRequest(token, "POST", "/public/v1/reviews", {
  body: { find: { projectId, ids: [reviewId] } },
  params: { Take: 1, Skip: 0 },
});
if (reviews.length !== 1 || reviews[0].id.toLowerCase() !== reviewId.toLowerCase()) {
  throw new Error("Указанное согласование не найдено");
}
const review = reviews[0];
// По ID последней версии согласования запрашиваем ID версий вошедших в него файлов.
const itemVersions = await apiRequest(token, "POST", "/public/v1/reviews/versions/item-versions", {
  body: { reviewVersionIds: [review.topVersion.id] },
});
// Записываем оба ответа в один JSON-файл.
const destination = process.env.SIGNAL_OUTPUT || "review.json";
await writeFile(destination, JSON.stringify({
  review, itemVersionIdsByReviewVersion: itemVersions,
}, null, 2), "utf8");
console.log("Данные согласования сохранены:", destination);
```

#### Замечания
###### 2.6. Реестр замечаний {#example-issues}

Используйте пример, чтобы выгрузить неудалённые замечания проекта для работы в Excel или дальнейшей обработки. Укажите `SIGNAL_PROJECT_ID`. Скрипт создаст два файла.

- `issues.csv` — таблица с номером, названием, статусом, ответственным и другими полями. Разделитель — точка с запятой, кодировка — UTF-8 с BOM.
- `issues.json` — полный список записей, возвращённых API. Комментарии, вложения и атрибуты можно получить отдельными запросами из справочника.

Для другого имени пары файлов задайте `SIGNAL_OUTPUT_PREFIX` без расширения. Чтобы отобрать замечания по типу или статусу, добавьте в фильтр `issueTypeId` или `statuses`. Запускайте выгрузку, когда реестр не редактируют. Скрипт прерывает выгрузку при дубликатах или расхождении с результатом запроса на подсчёт.

**Python** — `issues.py`. Запуск — `python issues.py`.

```python
import csv
import json
import os
from pathlib import Path
from signal_api import api_request, get_token

filters = {
    "projectId": os.environ["SIGNAL_PROJECT_ID"], "deleted": False,
    "order": "Number", "isOrderAsc": True,
}
token = get_token(["docs:issue:list"])["token"]

# Считаем замечания по тому же фильтру, по которому будем получать записи.
def count():
    return api_request(token, "POST", "/public/v1/issues/count", body=filters)["data"]

expected = count()
issues = []
seen = set()
skip = 0
# Берём следующую страницу, начиная после уже полученных записей.
while skip < expected:
    page = api_request(token, "POST", "/public/v1/issues", body=filters,
                       params={"Take": 200, "Skip": skip})
    if not page:
        break
    for issue in page:
        if issue["id"] in seen:
            raise RuntimeError("Повтор записи: повторите выгрузку после окончания изменений")
        seen.add(issue["id"])
        issues.append(issue)
    skip += len(page)
    if len(issues) > expected:
        raise RuntimeError("Состав замечаний изменился во время выгрузки; повторите её")
# Повторно сверяем количество перед записью файлов.
actual = count()
if len(issues) != expected or actual != expected:
    raise RuntimeError("Число замечаний изменилось или выгрузка неполная; повторите её")

fields = ["id", "number", "name", "status", "description", "placement",
          "eliminationDate", "added", "modified", "responsible"]


def cell(value):
    if isinstance(value, (dict, list)):
        value = json.dumps(value, ensure_ascii=False)
    text = "" if value is None else str(value)
    # Текст из API не должен становиться формулой при открытии CSV.
    return "'" + text if text.lstrip().startswith(("=", "+", "-", "@")) else text



# Сохраняем таблицу для Excel и полные ответы API в JSON.
stem = Path(os.environ.get("SIGNAL_OUTPUT_PREFIX", "issues"))
with Path(str(stem) + ".csv").open("w", encoding="utf-8-sig", newline="") as output:
    writer = csv.writer(output, delimiter=";")
    writer.writerow(fields)
    writer.writerows([cell(issue.get(key)) for key in fields] for issue in issues)
Path(str(stem) + ".json").write_text(
    json.dumps(issues, ensure_ascii=False, indent=2), encoding="utf-8",
)
print(f"Сохранено {len(issues)} замечаний: {stem}.csv и {stem}.json")
```

**Node.js** — `issues.mjs`. Запуск — `node issues.mjs`.

```javascript
import { writeFile } from "node:fs/promises";
import { apiRequest, env, getToken } from "./signal_api.mjs";

const filters = {
  projectId: env("SIGNAL_PROJECT_ID"), deleted: false,
  order: "Number", isOrderAsc: true,
};
const { token } = await getToken(["docs:issue:list"]);
// Считаем замечания по тому же фильтру, по которому будем получать записи.
async function count() {
  return (await apiRequest(token, "POST", "/public/v1/issues/count", { body: filters })).data;
}
const expected = await count();
const issues = [];
const seen = new Set();
let skip = 0;
// Берём следующую страницу, начиная после уже полученных записей.
while (skip < expected) {
  const page = await apiRequest(token, "POST", "/public/v1/issues", {
    body: filters, params: { Take: 200, Skip: skip },
  });
  if (!page.length) break;
  for (const issue of page) {
    if (seen.has(issue.id)) throw new Error("Повтор записи: повторите выгрузку после окончания изменений");
    seen.add(issue.id);
    issues.push(issue);
  }
  skip += page.length;
  if (issues.length > expected) throw new Error("Состав замечаний изменился; повторите выгрузку");
}
// Повторно сверяем количество перед записью файлов.
const actual = await count();
if (issues.length !== expected || actual !== expected) {
  throw new Error("Число замечаний изменилось или выгрузка неполная; повторите её");
}
// Сохраняем таблицу для Excel и полные ответы API в JSON.
const fields = ["id", "number", "name", "status", "description", "placement",
                "eliminationDate", "added", "modified", "responsible"];
function cell(value) {
  let text = value == null ? "" : typeof value === "object" ? JSON.stringify(value) : String(value);
  if (/^[=+\-@]/.test(text.trimStart())) text = "'" + text;
  return '"' + text.replaceAll('"', '""') + '"';
}
const rows = [fields.map(cell).join(";"),
  ...issues.map(issue => fields.map(key => cell(issue[key])).join(";"))];
const stem = process.env.SIGNAL_OUTPUT_PREFIX || "issues";
await writeFile(stem + ".csv", "\uFEFF" + rows.join("\r\n") + "\r\n", "utf8");
await writeFile(stem + ".json", JSON.stringify(issues, null, 2), "utf8");
console.log("Сохранено " + issues.length + " замечаний: " + stem + ".csv и " + stem + ".json");
```

#### Видео
###### 2.7. Видео и интеграции {#example-videos}

Авторизация

- [Google Apps Script](https://vkvideo.ru/video890470724_456239019)
- [IronPython](https://vkvideo.ru/video890470724_456239020)
- [1С](https://vkvideo.ru/video890470724_456239021)
  
Загрузка и скачивание файлов из DOCS

- [PowerShell](https://vkvideo.ru/video-230401166_456239017)
- [VBA Excel](https://vkvideo.ru/video-230401166_456239018)
- [Python](https://vkvideo.ru/video-230401166_456239019)

Примеры на n8n

- [Интеграция SIGNAL DOCS с n8n](https://vkvideo.ru/video-230401166_456239022)
- [Сбор аналитики в SIGNAL DOCS](https://vkvideo.ru/video-230401166_456239023)
- [Ежедневный отчет в Telegram по событиям в SIGNAL DOCS](https://vkvideo.ru/video-230401166_456239026)

## Справочник
###### 3. Справочник API {#reference}

При запросе токена передайте разрешение из колонки **Scope** в массиве `scopes`. Раскройте **Контракт** в строке метода, чтобы посмотреть, что передать и какой ответ вернёт API. Параметры строки запроса указываются после знака `?`. В постраничной выдаче `Take` задаёт размер страницы, а `Skip` — сколько записей пропустить. Под каждым методом есть ссылка на ReDoc с описанием полей, запросов и ответов.

### Разделы справочника {.tabset}
#### Файлы
###### 3.1. Файлы и версии {#reference-v1}

<div aria-label="Справочник API — Файлы" role="region" tabindex="0" style="width:100%;max-width:100%;box-sizing:border-box;overflow-x:auto;border:1px solid rgba(128,128,128,.32);border-radius:6px">
<table style="width:100%;min-width:48rem;table-layout:fixed;box-sizing:border-box;border:0;border-radius:0;margin:0">
<thead>
<tr>
<th style="width:30%;box-sizing:border-box">Метод и путь</th>
<th style="width:21%;box-sizing:border-box">Назначение</th>
<th style="width:15%;box-sizing:border-box">Scope</th>
<th style="width:34%;box-sizing:border-box">Контракт</th>
</tr>
</thead>
<tbody>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-item"></span><code style="white-space:normal;overflow-wrap:anywhere">PUT /public/v1/items/file</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Item">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Создаёт файл в папке и прикрепляет к нему существующую версию.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:item:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">folderId</code>, <code style="white-space:normal;overflow-wrap:anywhere">name</code> и <code style="white-space:normal;overflow-wrap:anywhere">versionId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — идентификатор в <code style="white-space:normal;overflow-wrap:anywhere">data</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PUT /public/v1/items/link</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Item">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Создаёт элемент типа «ссылка» и возвращает его идентификатор.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:item:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">folderId</code>, <code style="white-space:normal;overflow-wrap:anywhere">link</code> и <code style="white-space:normal;overflow-wrap:anywhere">name</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — идентификатор в <code style="white-space:normal;overflow-wrap:anywhere">data</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/items</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Item/operation/ItemListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает файлы и ссылки в папке.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:item:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В URL передайте <code style="white-space:normal;overflow-wrap:anywhere">folderId</code>.<br>В URL можно добавить <code style="white-space:normal;overflow-wrap:anywhere">deleted</code>, <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code>, <code style="white-space:normal;overflow-wrap:anywhere">name</code> и <code style="white-space:normal;overflow-wrap:anywhere">type</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/items/count</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Item/operation/ItemListCountV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает число файлов и ссылок в папке.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:item:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В URL передайте <code style="white-space:normal;overflow-wrap:anywhere">folderId</code>.<br>В URL можно добавить <code style="white-space:normal;overflow-wrap:anywhere">deleted</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — число в <code style="white-space:normal;overflow-wrap:anywhere">data</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/items/search</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Item/operation/ItemSearchV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Ищет элементы внутри папки, включая вложенные.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:item:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">folderId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code>, <code style="white-space:normal;overflow-wrap:anywhere">name</code> и <code style="white-space:normal;overflow-wrap:anywhere">type</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/items/item-version</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Item/operation/ItemGetItemVersionV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает версию элемента по её идентификатору.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:item:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В URL передайте <code style="white-space:normal;overflow-wrap:anywhere">id</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — идентификатор записи версии <code style="white-space:normal;overflow-wrap:anywhere">id</code>, идентификатор элемента <code style="white-space:normal;overflow-wrap:anywhere">itemId</code> и идентификатор версии <code style="white-space:normal;overflow-wrap:anywhere">versionId</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/items/download</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Item/operation/ItemDownloadV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Выдаёт ссылку для скачивания выбранной версии файла.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:item:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В URL передайте <code style="white-space:normal;overflow-wrap:anywhere">itemId</code> и <code style="white-space:normal;overflow-wrap:anywhere">versionId</code>.<br>В URL можно добавить <code style="white-space:normal;overflow-wrap:anywhere">fileName</code> и <code style="white-space:normal;overflow-wrap:anywhere">urlTtlSecOverride</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — подписанная ссылка в <code style="white-space:normal;overflow-wrap:anywhere">signedUrl</code> и срок её действия в секундах в <code style="white-space:normal;overflow-wrap:anywhere">ttlSec</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PUT /public/v1/items/versions</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Item/operation/ItemAttachVersionV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Прикрепляет новую версию к существующему элементу.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:version:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">itemId</code> и <code style="white-space:normal;overflow-wrap:anywhere">versionId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">204</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PATCH /public/v1/items/update</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Item/operation/ItemUpdateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Обновляет существующий элемент.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:item:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">id</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">204</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PATCH /public/v1/items/move</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Item/operation/ItemMoveV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Перемещает элемент в другую папку.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:item:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">newFolderId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PATCH /public/v1/items/versions/update</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Item/operation/ItemUpdateVersionV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Обновляет существующую версию элемента.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:version:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">id</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">204</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">DELETE /public/v1/items/{itemId}</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Item/operation/ItemDeleteV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Перемещает элемент в корзину.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:item:delete</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В пути замените <code style="white-space:normal;overflow-wrap:anywhere">{itemId}</code> на нужные значения.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">204</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-version"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/versions</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Version/operation/VersionCreateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Создаёт новую версию объекта и возвращает её идентификатор.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:version:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">name</code>, <code style="white-space:normal;overflow-wrap:anywhere">objectId</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — идентификатор в <code style="white-space:normal;overflow-wrap:anywhere">data</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/versions</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Version/operation/VersionListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает версии элемента.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:version:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В URL передайте <code style="white-space:normal;overflow-wrap:anywhere">itemId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — массив версий файла. Для скачивания используйте поле <code style="white-space:normal;overflow-wrap:anywhere">id</code> как <code style="white-space:normal;overflow-wrap:anywhere">versionId</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/versions/find-batch</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Version/operation/VersionListBatchV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает версии для набора элементов.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:version:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">itemIds</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">itemId</code> и <code style="white-space:normal;overflow-wrap:anywhere">attachedVersions</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/versions/count</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Version/operation/VersionCountV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Подсчитывает версии элемента.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:version:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В URL передайте <code style="white-space:normal;overflow-wrap:anywhere">itemId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — число в <code style="white-space:normal;overflow-wrap:anywhere">data</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-object"></span><code style="white-space:normal;overflow-wrap:anywhere">PUT /public/v1/objects</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Object/operation/ObjectCreateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Выдаёт билет для загрузки объекта; после загрузки объект требуется подтвердить отдельным запросом.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:object:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">mimeType</code>, <code style="white-space:normal;overflow-wrap:anywhere">projectId</code> и <code style="white-space:normal;overflow-wrap:anywhere">size</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — идентификатор загружаемого объекта <code style="white-space:normal;overflow-wrap:anywhere">objectId</code>, ссылка для загрузки <code style="white-space:normal;overflow-wrap:anywhere">signedUrl</code> и срок её действия в секундах в <code style="white-space:normal;overflow-wrap:anywhere">ttlSec</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/objects/{objectId}/uploading/commit</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Object/operation/ObjectCommitUploadingV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Подтверждает завершение загрузки объекта в S3.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:object:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В пути замените <code style="white-space:normal;overflow-wrap:anywhere">{objectId}</code> на нужные значения.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-share"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/shares</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Share/operation/ShareListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Ищет публикации файлов по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:share:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">type</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PUT /public/v1/shares</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Share/operation/ShareCreateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Создаёт публикацию элемента.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:share:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">sharedItemId</code>, <code style="white-space:normal;overflow-wrap:anywhere">sharedItemType</code> и <code style="white-space:normal;overflow-wrap:anywhere">shareType</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — идентификатор в <code style="white-space:normal;overflow-wrap:anywhere">data</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PATCH /public/v1/shares</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Share/operation/ShareUpdateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Обновляет существующую публикацию.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:share:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">id</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">DELETE /public/v1/shares</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Share/operation/ShareDeleteV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Изменяет состояние удаления существующей публикации.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:share:delete</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">deleted</code> и <code style="white-space:normal;overflow-wrap:anywhere">id</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/shares/count</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Share/operation/ShareListCountV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Подсчитывает публикации по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:share:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — число в <code style="white-space:normal;overflow-wrap:anywhere">data</code>.</div></details></td>
</tr>
</tbody>
</table>
</div>

#### Папки
###### 3.2. Папки и доступ {#reference-folders}

<div aria-label="Справочник API — Папки" role="region" tabindex="0" style="width:100%;max-width:100%;box-sizing:border-box;overflow-x:auto;border:1px solid rgba(128,128,128,.32);border-radius:6px">
<table style="width:100%;min-width:48rem;table-layout:fixed;box-sizing:border-box;border:0;border-radius:0;margin:0">
<thead>
<tr>
<th style="width:30%;box-sizing:border-box">Метод и путь</th>
<th style="width:21%;box-sizing:border-box">Назначение</th>
<th style="width:15%;box-sizing:border-box">Scope</th>
<th style="width:34%;box-sizing:border-box">Контракт</th>
</tr>
</thead>
<tbody>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-folder"></span><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/folders/{folderId}/children</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Folder/operation/FolderListChildrenV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает непосредственных потомков папки.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:folder:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В пути замените <code style="white-space:normal;overflow-wrap:anywhere">{folderId}</code> на нужные значения.<br>В URL можно добавить <code style="white-space:normal;overflow-wrap:anywhere">deleted</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code>, <code style="white-space:normal;overflow-wrap:anywhere">name</code> и <code style="white-space:normal;overflow-wrap:anywhere">type</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PUT /public/v1/folders</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Folder/operation/FolderCreateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Создаёт папку и возвращает её идентификатор.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:folder:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">name</code> и <code style="white-space:normal;overflow-wrap:anywhere">parentId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — идентификатор в <code style="white-space:normal;overflow-wrap:anywhere">data</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PATCH /public/v1/folders</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Folder/operation/FolderUpdateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Обновляет папку.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:folder:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">id</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">204</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">DELETE /public/v1/folders/{folderId}</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Folder/operation/FolderDeleteV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Перемещает папку в корзину.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:folder:delete</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В пути замените <code style="white-space:normal;overflow-wrap:anywhere">{folderId}</code> на нужные значения.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">204</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/projects/{projectId}/folders/tree</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Folder/operation/FolderGetProjectTreeV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает полное дерево папок проекта с правами пользователя.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:folder:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В пути замените <code style="white-space:normal;overflow-wrap:anywhere">{projectId}</code> на нужные значения.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — дерево папок. У каждого узла есть <code style="white-space:normal;overflow-wrap:anywhere">id</code>, <code style="white-space:normal;overflow-wrap:anywhere">name</code>, <code style="white-space:normal;overflow-wrap:anywhere">permissions</code> и <code style="white-space:normal;overflow-wrap:anywhere">children</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-folderitemsnamingpattern"></span><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/naming-patterns/folder-items/find</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/FolderItemsNamingPattern/operation/FolderItemsNamingPatternFindV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает правила именования файлов в папке.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:item:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В URL передайте <code style="white-space:normal;overflow-wrap:anywhere">folderId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — настройки именования в поле <code style="white-space:normal;overflow-wrap:anywhere">value</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-storage"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/storages</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Storage/operation/StorageListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Ищет хранилища документов по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:storage:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В теле запроса передайте JSON-объект. Все его поля необязательны. Для фильтрации можно указать <code style="white-space:normal;overflow-wrap:anywhere">isSystem</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">name</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-permissions"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/permissions/folders/upsert</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Permissions/operation/PermissionsUpsertBatchV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Создаёт или обновляет права пользователей и ролей на конкретную папку.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:permissions:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">folderId</code> и <code style="white-space:normal;overflow-wrap:anywhere">items</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.<br><code style="white-space:normal;overflow-wrap:anywhere">204</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/permissions/tree</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Permissions/operation/PermissionsGetProjectPermissionsTreeV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает дерево папок проекта с назначенными правами.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:permissions:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В URL передайте <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — дерево папок с назначенными правами. Права узла находятся в <code style="white-space:normal;overflow-wrap:anywhere">permissions</code>, вложенные папки — в <code style="white-space:normal;overflow-wrap:anywhere">children</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">DELETE /public/v1/permissions/{permissionId}</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Permissions/operation/PermissionsDeleteV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Удаляет конкретное разрешение.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:permissions:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В пути замените <code style="white-space:normal;overflow-wrap:anywhere">{permissionId}</code> на нужные значения.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
</tbody>
</table>
</div>

#### Замечания
###### 3.3. Замечания {#reference-issues}

<div aria-label="Справочник API — Замечания" role="region" tabindex="0" style="width:100%;max-width:100%;box-sizing:border-box;overflow-x:auto;border:1px solid rgba(128,128,128,.32);border-radius:6px">
<table style="width:100%;min-width:48rem;table-layout:fixed;box-sizing:border-box;border:0;border-radius:0;margin:0">
<thead>
<tr>
<th style="width:30%;box-sizing:border-box">Метод и путь</th>
<th style="width:21%;box-sizing:border-box">Назначение</th>
<th style="width:15%;box-sizing:border-box">Scope</th>
<th style="width:34%;box-sizing:border-box">Контракт</th>
</tr>
</thead>
<tbody>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-issue"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/issues</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Issue/operation/IssueListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Ищет замечания по фильтру с пагинацией.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:issue:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code>, <code style="white-space:normal;overflow-wrap:anywhere">name</code> и <code style="white-space:normal;overflow-wrap:anywhere">number</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PATCH /public/v1/issues</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Issue/operation/IssueUpdateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Пакетно обновляет несколько замечаний.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:issue:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В теле JSON-массив. В каждой записи укажите <code style="white-space:normal;overflow-wrap:anywhere">id</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/issues/count</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Issue/operation/IssueListCountV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Подсчитывает замечания по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:issue:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — число в <code style="white-space:normal;overflow-wrap:anywhere">data</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/issues/items/counts</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Issue/operation/IssueListItemIssuesCountV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает число замечаний, связанных с каждым из указанных элементов.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:issue:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">itemIds</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">itemId</code> и <code style="white-space:normal;overflow-wrap:anywhere">count</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/issues/create</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Issue/operation/IssueCreateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Создаёт замечание.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:issue:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">authorId</code>, <code style="white-space:normal;overflow-wrap:anywhere">issueTypeId</code>, <code style="white-space:normal;overflow-wrap:anywhere">name</code>, <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>, <code style="white-space:normal;overflow-wrap:anywhere">responsible</code> и <code style="white-space:normal;overflow-wrap:anywhere">status</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — идентификатор (UUID) в виде строки.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-issueaccesses"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/issues/accesses</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/IssueAccesses/operation/IssueAccessesListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает правила доступа к замечаниям.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:issue:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">issueTypeIds</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">roleId</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-issueattachment"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/issues/attachments</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/IssueAttachment/operation/IssueAttachmentListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает вложения указанного замечания.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:issue:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">issueId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code>, <code style="white-space:normal;overflow-wrap:anywhere">name</code> и <code style="white-space:normal;overflow-wrap:anywhere">itemId</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/issues/attachments/object/download</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/IssueAttachment/operation/IssueAttachmentDownloadObjectV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Создаёт билет для скачивания объекта вложения.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:issue:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">issueAttachmentId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — подписанная ссылка в <code style="white-space:normal;overflow-wrap:anywhere">signedUrl</code> и срок её действия в секундах в <code style="white-space:normal;overflow-wrap:anywhere">ttlSec</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-issuecomment"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/issues/comments</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/IssueComment/operation/IssueCommentListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает комментарии к замечаниям проекта.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:issue:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">issueIds</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">text</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PUT /public/v1/issues/comments</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/IssueComment/operation/IssueCommentCreateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Создаёт комментарий к указанному замечанию.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:issue:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">issueId</code> и <code style="white-space:normal;overflow-wrap:anywhere">text</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — идентификатор в <code style="white-space:normal;overflow-wrap:anywhere">data</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/issues/comments/count</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/IssueComment/operation/IssueCommentListCountV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Подсчитывает комментарии по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:issue:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">issueIds</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — число в <code style="white-space:normal;overflow-wrap:anywhere">data</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-issueevents"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/issues/events</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/IssueEvents/operation/IssueEventsListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает события замечаний по фильтру с пагинацией.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:issue:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">issueId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code>, <code style="white-space:normal;overflow-wrap:anywhere">itemId</code> и <code style="white-space:normal;overflow-wrap:anywhere">type</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/issues/events/count</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/IssueEvents/operation/IssueEventsListCountV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Подсчитывает события замечаний по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:issue:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">issueId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — число в <code style="white-space:normal;overflow-wrap:anywhere">data</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-issueprojectsettings"></span><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/issues/settings/project</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/IssueProjectSettings/operation/IssueProjectSettingsGetV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает настройки замечаний для проекта.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:issue:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В URL передайте <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-объект с полями <code style="white-space:normal;overflow-wrap:anywhere">projectId</code> и <code style="white-space:normal;overflow-wrap:anywhere">imageColorByIssueStatusIsEnabled</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-issuetype"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/issues/types</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/IssueType/operation/IssueTypeListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Ищет типы замечаний по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:issue:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">name</code>.</div></details></td>
</tr>
</tbody>
</table>
</div>

#### Согласования
###### 3.4. Согласования {#reference-reviews}

<div aria-label="Справочник API — Согласования" role="region" tabindex="0" style="width:100%;max-width:100%;box-sizing:border-box;overflow-x:auto;border:1px solid rgba(128,128,128,.32);border-radius:6px">
<table style="width:100%;min-width:48rem;table-layout:fixed;box-sizing:border-box;border:0;border-radius:0;margin:0">
<thead>
<tr>
<th style="width:30%;box-sizing:border-box">Метод и путь</th>
<th style="width:21%;box-sizing:border-box">Назначение</th>
<th style="width:15%;box-sizing:border-box">Scope</th>
<th style="width:34%;box-sizing:border-box">Контракт</th>
</tr>
</thead>
<tbody>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-review"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/reviews</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Review/operation/ReviewListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает согласования проекта.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:review:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В теле JSON. В объекте <code style="white-space:normal;overflow-wrap:anywhere">find</code> укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — массив согласований. В поле <code style="white-space:normal;overflow-wrap:anywhere">topVersion</code> содержатся данные последней версии.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PATCH /public/v1/reviews</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Review/operation/ReviewUpdateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Изменяет основные сведения согласования.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:review:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">id</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/reviews/count</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Review/operation/ReviewListCountV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Подсчитывает согласования по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:review:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — число в <code style="white-space:normal;overflow-wrap:anywhere">data</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/reviews/versions</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Review/operation/ReviewGetVersionsV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает версии согласований по указанным идентификаторам.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:review:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">reviewVersionIds</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">number</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/reviews/versions/item-versions</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Review/operation/ReviewFindItemVersionIdsByReviewVersionIdsV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает идентификаторы версий элементов, сгруппированные по версиям согласований.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:review:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">reviewVersionIds</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — объект, где ключ — ID версии согласования, а значение — массив ID версий файлов.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/reviews/create</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Review/operation/ReviewCreateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Создаёт согласование.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:review:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">behalfUserId</code>, <code style="white-space:normal;overflow-wrap:anywhere">cipher</code>, <code style="white-space:normal;overflow-wrap:anywhere">name</code>, <code style="white-space:normal;overflow-wrap:anywhere">projectId</code> и <code style="white-space:normal;overflow-wrap:anywhere">reviewTypeId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — идентификатор (UUID) в виде строки.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PATCH /public/v1/reviews/type</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Review/operation/ReviewSetTypeV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Устанавливает или изменяет тип согласования.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:review:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">reviewTypeId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PATCH /public/v1/reviews/comment</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Review/operation/ReviewSetCommentV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Устанавливает или очищает комментарий последней версии согласования, кроме удалённого согласования.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:review:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">authorId</code>, <code style="white-space:normal;overflow-wrap:anywhere">comment</code> и <code style="white-space:normal;overflow-wrap:anywhere">id</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-reviewgroup"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/reviews/groups</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ReviewGroup/operation/ReviewGroupListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает группы согласований проекта.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:review:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">name</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-reviewitem"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/reviews/items</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ReviewItem/operation/ReviewItemGetReviewItemsStatusesV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает статусы согласования указанных версий элементов.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:review:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">itemVersionIds</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">status</code> и <code style="white-space:normal;overflow-wrap:anywhere">itemVersionId</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/reviews/items/add</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ReviewItem/operation/ReviewItemAddItemV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Добавляет версию элемента в существующее согласование.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:review:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">itemVersionId</code> и <code style="white-space:normal;overflow-wrap:anywhere">reviewId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/reviews/items/remove</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ReviewItem/operation/ReviewItemRemoveItemV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Удаляет версию элемента из согласования.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:review:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">itemVersionId</code> и <code style="white-space:normal;overflow-wrap:anywhere">reviewId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-reviewprocess"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/reviews/process/start</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ReviewProcess/operation/ReviewProcessStartV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Запускает процесс указанного согласования.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:review:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">behalfUserId</code> и <code style="white-space:normal;overflow-wrap:anywhere">reviewId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-reviewtype"></span><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/reviews/types/names</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ReviewType/operation/ReviewTypeFindNamesV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает названия типов согласований проекта.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:review:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В URL передайте <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">name</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/reviews/types/create</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ReviewType/operation/ReviewTypeCreateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Создаёт тип согласования проекта.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:review:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">name</code>, <code style="white-space:normal;overflow-wrap:anywhere">projectId</code> и <code style="white-space:normal;overflow-wrap:anywhere">version</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — идентификатор (UUID) в виде строки.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PATCH /public/v1/reviews/types</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ReviewType/operation/ReviewTypeUpdateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Обновляет существующий тип согласования.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:review:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
</tbody>
</table>
</div>

#### Передачи
###### 3.5. Передачи {#reference-transfers}

<div aria-label="Справочник API — Передачи" role="region" tabindex="0" style="width:100%;max-width:100%;box-sizing:border-box;overflow-x:auto;border:1px solid rgba(128,128,128,.32);border-radius:6px">
<table style="width:100%;min-width:48rem;table-layout:fixed;box-sizing:border-box;border:0;border-radius:0;margin:0">
<thead>
<tr>
<th style="width:30%;box-sizing:border-box">Метод и путь</th>
<th style="width:21%;box-sizing:border-box">Назначение</th>
<th style="width:15%;box-sizing:border-box">Scope</th>
<th style="width:34%;box-sizing:border-box">Контракт</th>
</tr>
</thead>
<tbody>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-documentstransfer"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/documents-transfers</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/DocumentsTransfer/operation/DocumentsTransferListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Ищет передачи документов по фильтру с пагинацией.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:docs_transfer:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code>, <code style="white-space:normal;overflow-wrap:anywhere">name</code> и <code style="white-space:normal;overflow-wrap:anywhere">number</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/documents-transfers</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/DocumentsTransfer/operation/DocumentsTransferGetAllDataV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает подробные сведения об одной передаче документов по её идентификатору.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:docs_transfer:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В URL передайте <code style="white-space:normal;overflow-wrap:anywhere">id</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — данные передачи, включая номер <code style="white-space:normal;overflow-wrap:anywhere">number</code>, статус <code style="white-space:normal;overflow-wrap:anywhere">status</code> и сведения о текущей приёмке <code style="white-space:normal;overflow-wrap:anywhere">currentAcceptance</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/documents-transfers/count</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/DocumentsTransfer/operation/DocumentsTransferListCountV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Подсчитывает передачи документов по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:docs_transfer:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — число в <code style="white-space:normal;overflow-wrap:anywhere">data</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/documents-transfers/create</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/DocumentsTransfer/operation/DocumentsTransferCreateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Создаёт передачу документов.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:docs_transfer:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">authorId</code>, <code style="white-space:normal;overflow-wrap:anywhere">cipher</code>, <code style="white-space:normal;overflow-wrap:anywhere">documentsTransferTypeId</code> и <code style="white-space:normal;overflow-wrap:anywhere">name</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — идентификатор (UUID) в виде строки.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-documentstransferacceptance"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/documents-transfer-acceptances/send</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/DocumentsTransferAcceptance/operation/DocumentsTransferAcceptanceSendV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Отправляет подготовленную передачу документов получателю.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:docs_transfer:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">authorId</code>, <code style="white-space:normal;overflow-wrap:anywhere">documentsTransferId</code> и <code style="white-space:normal;overflow-wrap:anywhere">recipient</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-documentstransferaccesses"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/documents-transfers/accesses</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/DocumentsTransferAccesses/operation/DocumentsTransferAccessesListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает правила доступа для указанных типов передачи документов.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:docs_transfer:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>Тело запроса можно опустить. Если передаёте JSON-объект, укажите <code style="white-space:normal;overflow-wrap:anywhere">documentsTransferTypeIds</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">documentsTransferTypeId</code> и <code style="white-space:normal;overflow-wrap:anywhere">roleId</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-documentstransferitem"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/documents-transfer-items</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/DocumentsTransferItem/operation/DocumentsTransferItemListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает элементы указанной передачи документов с пагинацией.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:docs_transfer:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">documentsTransferId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">itemId</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/documents-transfer-items/count</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/DocumentsTransferItem/operation/DocumentsTransferItemListCountV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Подсчитывает элементы указанной передачи документов.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:docs_transfer:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">documentsTransferId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — число в <code style="white-space:normal;overflow-wrap:anywhere">data</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/documents-transfer-items/download</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/DocumentsTransferItem/operation/DocumentsTransferItemDownloadV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Выдаёт временный билет для скачивания элемента передачи документов.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:docs_transfer:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В URL передайте <code style="white-space:normal;overflow-wrap:anywhere">documentsTransferItemId</code>.<br>В URL можно добавить <code style="white-space:normal;overflow-wrap:anywhere">fileName</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — подписанная ссылка в <code style="white-space:normal;overflow-wrap:anywhere">signedUrl</code> и срок её действия в секундах в <code style="white-space:normal;overflow-wrap:anywhere">ttlSec</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/documents-transfer-items/add</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/DocumentsTransferItem/operation/DocumentsTransferItemAddItemsV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Добавляет версии элементов в передачу документов.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:docs_transfer:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">documentsTransferId</code> и <code style="white-space:normal;overflow-wrap:anywhere">itemVersionIds</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-documentstransfertype"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/documents-transfers/types</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/DocumentsTransferType/operation/DocumentsTransferTypeListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Ищет типы передачи документов по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:docs_transfer:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">name</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-acceptancecertificate"></span><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/acceptance-certificates/download</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/AcceptanceCertificate/operation/AcceptanceCertificateDownloadV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Выдаёт временный билет для скачивания файла акта приёмки.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:docs_transfer:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В URL передайте <code style="white-space:normal;overflow-wrap:anywhere">acceptanceCertificateId</code>.<br>В URL можно добавить <code style="white-space:normal;overflow-wrap:anywhere">fileName</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — подписанная ссылка в <code style="white-space:normal;overflow-wrap:anywhere">signedUrl</code> и срок её действия в секундах в <code style="white-space:normal;overflow-wrap:anywhere">ttlSec</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/acceptance-certificates/attach</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/AcceptanceCertificate/operation/AcceptanceCertificateAttachV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Прикрепляет акт приёмки к передаче документов.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:docs_transfer:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">authorId</code>, <code style="white-space:normal;overflow-wrap:anywhere">companyRecipient</code>, <code style="white-space:normal;overflow-wrap:anywhere">companySender</code>, <code style="white-space:normal;overflow-wrap:anywhere">documentsTransferId</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectName</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — идентификатор (UUID) в виде строки.</div></details></td>
</tr>
</tbody>
</table>
</div>

#### Формы
###### 3.6. Формы {#reference-forms}

<div aria-label="Справочник API — Формы" role="region" tabindex="0" style="width:100%;max-width:100%;box-sizing:border-box;overflow-x:auto;border:1px solid rgba(128,128,128,.32);border-radius:6px">
<table style="width:100%;min-width:48rem;table-layout:fixed;box-sizing:border-box;border:0;border-radius:0;margin:0">
<thead>
<tr>
<th style="width:30%;box-sizing:border-box">Метод и путь</th>
<th style="width:21%;box-sizing:border-box">Назначение</th>
<th style="width:15%;box-sizing:border-box">Scope</th>
<th style="width:34%;box-sizing:border-box">Контракт</th>
</tr>
</thead>
<tbody>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-projectform"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/projects/forms</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ProjectForm/operation/ProjectFormListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Ищет формы проекта по фильтру и сортировке с пагинацией.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">forms:project_form:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В теле JSON. В объекте <code style="white-space:normal;overflow-wrap:anywhere">find</code> укажите <code style="white-space:normal;overflow-wrap:anywhere">formTypeId</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — записи реестра в <code style="white-space:normal;overflow-wrap:anywhere">projectFormEntries</code> и типы полей форм в <code style="white-space:normal;overflow-wrap:anywhere">usedFormFieldTypes</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/projects/forms/count</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ProjectForm/operation/ProjectFormListCountV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Подсчитывает формы проекта по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">forms:project_form:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">formTypeId</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — число.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/projects/forms/get</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ProjectForm/operation/ProjectFormGetV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает форму проекта по идентификатору.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">forms:project_form:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectFormId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — карточка формы с номером <code style="white-space:normal;overflow-wrap:anywhere">number</code>, статусом <code style="white-space:normal;overflow-wrap:anywhere">status</code> и полями <code style="white-space:normal;overflow-wrap:anywhere">projectFormFields</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/projects/forms/get-summary</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ProjectForm/operation/ProjectFormGetSummaryV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает сводные данные указанных форм проекта.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">forms:project_form:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectFormIds</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectIds</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">number</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/projects/forms/find-form-source</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ProjectForm/operation/ProjectFormFindFormSourceV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Ищет формы проекта, которые могут быть источниками данных для указанного типа поля, по заданным критериям.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">forms:project_form:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">formFieldTypeId</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — формы источника в <code style="white-space:normal;overflow-wrap:anywhere">forms</code> и типы отображаемых полей в <code style="white-space:normal;overflow-wrap:anywhere">displayFieldTypes</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/projects/forms/get-values-for-template-item</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ProjectForm/operation/ProjectFormGetValuesForTemplateItemV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает значения элемента шаблона формы проекта.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">forms:project_form:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectFormId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — данные формы для шаблона в <code style="white-space:normal;overflow-wrap:anywhere">form</code> и сведения о внешних источниках в <code style="white-space:normal;overflow-wrap:anywhere">externalSources</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/projects/forms/get-download-url-by-template-item</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ProjectForm/operation/ProjectFormGetDownloadUrlByTemplateItemV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Выдаёт временную ссылку для скачивания элемента шаблона формы проекта.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">forms:project_form:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectFormId</code> и <code style="white-space:normal;overflow-wrap:anywhere">templateItemId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — подписанная ссылка в <code style="white-space:normal;overflow-wrap:anywhere">signedUrl</code> и срок её действия в секундах в <code style="white-space:normal;overflow-wrap:anywhere">ttlSec</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/projects/forms/create-batch</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ProjectForm/operation/ProjectFormCreateBatchV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Создаёт несколько форм проекта одним запросом.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">forms:project_form:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">forms</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectFormTypeId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — массив идентификаторов (UUID).</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PATCH /public/v1/projects/forms/update</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ProjectForm/operation/ProjectFormUpdateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Обновляет существующую форму проекта.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">forms:project_form:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectFormFields</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectFormId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PATCH /public/v1/projects/forms/complete</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ProjectForm/operation/ProjectFormCompleteV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Переводит существующую форму проекта в завершённое состояние.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">forms:project_form:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectFormId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-projectformfieldtype"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/projects/forms/fields/types</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ProjectFormFieldType/operation/ProjectFormFieldTypeListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Ищет типы полей форм проекта и связанные источники отображения по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">forms:project_form_field_type:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectFormTypeId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — типы полей в <code style="white-space:normal;overflow-wrap:anywhere">projectFormFieldTypes</code> и сведения о внешних источниках в <code style="white-space:normal;overflow-wrap:anywhere">externalSources</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-projectformtype"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/projects/forms/types</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ProjectFormType/operation/ProjectFormTypeListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Ищет типы форм проекта по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">forms:project_form_type:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">formTypeId</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-formfieldtype"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/forms/fields/types</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/FormFieldType/operation/FormFieldTypeListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Ищет типы полей форм по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">forms:form_field_type:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В теле запроса передайте JSON-объект. Все его поля необязательны. Для фильтрации можно указать <code style="white-space:normal;overflow-wrap:anywhere">name</code> и <code style="white-space:normal;overflow-wrap:anywhere">formTypeIds</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">name</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-formtype"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/forms/types</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/FormType/operation/FormTypeListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Ищет типы форм по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">forms:form_type:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В теле запроса передайте JSON-объект. Все его поля необязательны. Для фильтрации можно указать <code style="white-space:normal;overflow-wrap:anywhere">name</code> и <code style="white-space:normal;overflow-wrap:anywhere">formTypeGroupIds</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">name</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-formtypegroup"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/forms/types/groups</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/FormTypeGroup/operation/FormTypeGroupListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Ищет группы типов форм по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">forms:form_type_group:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В теле запроса передайте JSON-объект. Все его поля необязательны. Для фильтрации можно указать <code style="white-space:normal;overflow-wrap:anywhere">name</code> и <code style="white-space:normal;overflow-wrap:anywhere">deleted</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">name</code>.</div></details></td>
</tr>
</tbody>
</table>
</div>

#### Атрибуты
###### 3.7. Атрибуты {#reference-attributes}

<div aria-label="Справочник API — Атрибуты" role="region" tabindex="0" style="width:100%;max-width:100%;box-sizing:border-box;overflow-x:auto;border:1px solid rgba(128,128,128,.32);border-radius:6px">
<table style="width:100%;min-width:48rem;table-layout:fixed;box-sizing:border-box;border:0;border-radius:0;margin:0">
<thead>
<tr>
<th style="width:30%;box-sizing:border-box">Метод и путь</th>
<th style="width:21%;box-sizing:border-box">Назначение</th>
<th style="width:15%;box-sizing:border-box">Scope</th>
<th style="width:34%;box-sizing:border-box">Контракт</th>
</tr>
</thead>
<tbody>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-attribute"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/attributes</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Attribute/operation/AttributeListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает атрибуты по заданному фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:attribute:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code> и <code style="white-space:normal;overflow-wrap:anywhere">type</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">type</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-attributetype"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/attributes/types</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/AttributeType/operation/AttributeTypeListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Ищет типы атрибутов по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:attribute:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code>, <code style="white-space:normal;overflow-wrap:anywhere">name</code> и <code style="white-space:normal;overflow-wrap:anywhere">type</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PATCH /public/v1/attributes/types</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/AttributeType/operation/AttributeTypeUpdateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Обновляет существующие типы атрибутов.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:attribute:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">data</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/attributes/types/create</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/AttributeType/operation/AttributeTypeCreateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Создаёт новый тип атрибута.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:attribute:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">isRequired</code>, <code style="white-space:normal;overflow-wrap:anywhere">name</code>, <code style="white-space:normal;overflow-wrap:anywhere">order</code>, <code style="white-space:normal;overflow-wrap:anywhere">projectId</code> и <code style="white-space:normal;overflow-wrap:anywhere">type</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — идентификатор (UUID) в виде строки.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-attributetypelistitems"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/attributes/types/list/items/create</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/AttributeTypeListItems/operation/AttributeTypeListItemsCreateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Добавляет варианты значений в атрибут типа «список».</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:attribute:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">attributeTypeId</code> и <code style="white-space:normal;overflow-wrap:anywhere">items</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PATCH /public/v1/attributes/types/list/items</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/AttributeTypeListItems/operation/AttributeTypeListItemsUpdateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Изменяет варианты значений атрибута типа «список».</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:attribute:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">attributeTypeId</code> и <code style="white-space:normal;overflow-wrap:anywhere">items</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-attributevalue"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/attributes/values/issues</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/AttributeValue/operation/AttributeValueListIssuesV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает значения атрибутов замечаний по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:attribute:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">issueIds</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">attributeId</code> и <code style="white-space:normal;overflow-wrap:anywhere">attributeTypeId</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/attributes/values/items</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/AttributeValue/operation/AttributeValueListItemsV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает значения атрибутов элементов по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:attribute:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">itemIds</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">itemId</code> и <code style="white-space:normal;overflow-wrap:anywhere">attributeId</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/attributes/values/folders</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/AttributeValue/operation/AttributeValueListFoldersV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает значения атрибутов папок по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:attribute:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">folderIds</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">attributeId</code> и <code style="white-space:normal;overflow-wrap:anywhere">attributeTypeId</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/attributes/values/set</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/AttributeValue/operation/AttributeValueSetV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Устанавливает значения атрибутов для указанной сущности.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:attribute:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">type</code> и <code style="white-space:normal;overflow-wrap:anywhere">values</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.<br><code style="white-space:normal;overflow-wrap:anywhere">204</code> — без тела.</div></details></td>
</tr>
</tbody>
</table>
</div>

#### HUB
###### 3.8. Компания и проекты {#reference-access}

<div aria-label="Справочник API — HUB" role="region" tabindex="0" style="width:100%;max-width:100%;box-sizing:border-box;overflow-x:auto;border:1px solid rgba(128,128,128,.32);border-radius:6px">
<table style="width:100%;min-width:48rem;table-layout:fixed;box-sizing:border-box;border:0;border-radius:0;margin:0">
<thead>
<tr>
<th style="width:30%;box-sizing:border-box">Метод и путь</th>
<th style="width:21%;box-sizing:border-box">Назначение</th>
<th style="width:15%;box-sizing:border-box">Scope</th>
<th style="width:34%;box-sizing:border-box">Контракт</th>
</tr>
</thead>
<tbody>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-auth"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/auth/token</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Auth/operation/AuthGetTokenV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Выдаёт токен интеграции с запрошенными разрешениями.</td>
<td style="overflow-wrap:anywhere">Bearer-токен не нужен</td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">clientId</code>, <code style="white-space:normal;overflow-wrap:anywhere">clientSecret</code> и <code style="white-space:normal;overflow-wrap:anywhere">scopes</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — токен <code style="white-space:normal;overflow-wrap:anywhere">token</code> и срок его действия в секундах в <code style="white-space:normal;overflow-wrap:anywhere">expiresIn</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-company"></span><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/company/users</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Company/operation/CompanyListUsersV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает пользователей компании.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">company:user:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">email</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/company/roles</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Company/operation/CompanyListRolesV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает роли компании.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">company:role:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">name</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-companyuser"></span><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/company-users/by-telegram-id</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/CompanyUser/operation/CompanyUserGetUserIdByTelegramIdV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает идентификатор пользователя компании по Telegram ID.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">company:user:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В URL передайте <code style="white-space:normal;overflow-wrap:anywhere">telegramId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — идентификатор (UUID) в виде строки.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PUT /public/v1/company-users</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/CompanyUser/operation/CompanyUserAddCompanyUsersV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Пакетно приглашает или добавляет пользователей в компанию.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">company:user:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">users</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">status</code> и <code style="white-space:normal;overflow-wrap:anywhere">email</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">DELETE /public/v1/company-users</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/CompanyUser/operation/CompanyUserDeleteCompanyUsersV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Пакетно удаляет пользователей из компании.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">company:user:delete</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">userIds</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-companyusercustomrole"></span><code style="white-space:normal;overflow-wrap:anywhere">PUT /public/v1/company-user-custom-roles</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/CompanyUserCustomRole/operation/CompanyUserCustomRoleSetCompanyUserCustomRolesV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Заменяет дополнительные роли пользователя на уровне компании переданным списком.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">company:role:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">customRoleIds</code> и <code style="white-space:normal;overflow-wrap:anywhere">userId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-applicationuser"></span><code style="white-space:normal;overflow-wrap:anywhere">PUT /public/v1/application-users</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ApplicationUser/operation/ApplicationUserUpsertApplicationUsersV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Пакетно назначает пользователям роли в нескольких приложениях.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">application:user:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">applicationIds</code>, <code style="white-space:normal;overflow-wrap:anywhere">role</code> и <code style="white-space:normal;overflow-wrap:anywhere">userIds</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">DELETE /public/v1/application-users</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ApplicationUser/operation/ApplicationUserDeleteApplicationUsersV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Пакетно отзывает доступ пользователей к приложениям.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">application:user:delete</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">applicationIds</code> и <code style="white-space:normal;overflow-wrap:anywhere">userIds</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-project"></span><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/projects/{projectId}</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Project/operation/ProjectGetV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает сведения об указанном проекте.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">project:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В пути замените <code style="white-space:normal;overflow-wrap:anywhere">{projectId}</code> на нужные значения.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-объект с полями <code style="white-space:normal;overflow-wrap:anywhere">id</code>, <code style="white-space:normal;overflow-wrap:anywhere">name</code>, <code style="white-space:normal;overflow-wrap:anywhere">code</code> и <code style="white-space:normal;overflow-wrap:anywhere">email</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/projects</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Project/operation/ProjectListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает список проектов компании.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">project:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">name</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PATCH /public/v1/projects</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Project/operation/ProjectUpdateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Изменяет основные сведения существующего проекта.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">project:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">id</code>, <code style="white-space:normal;overflow-wrap:anywhere">name</code> и <code style="white-space:normal;overflow-wrap:anywhere">timeZoneOffset</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/projects/{projectId}/users</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Project/operation/ProjectListUsersV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает пользователей проекта.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">project:user:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В пути замените <code style="white-space:normal;overflow-wrap:anywhere">{projectId}</code> на нужные значения.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">email</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/projects/{projectId}/users/{userId}/permissions</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Project/operation/ProjectGetUserPermissionsV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает права пользователя в проекте; при отсутствии прав схема предусматривает ответ 404.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">project:user:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В пути замените <code style="white-space:normal;overflow-wrap:anywhere">{projectId}</code> и <code style="white-space:normal;overflow-wrap:anywhere">{userId}</code> на нужные значения.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — роли пользователя в проекте в поле <code style="white-space:normal;overflow-wrap:anywhere">roles</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/projects/{projectId}/roles</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Project/operation/ProjectListRolesV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает роли проекта.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">project:role:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В пути замените <code style="white-space:normal;overflow-wrap:anywhere">{projectId}</code> на нужные значения.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">name</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-docsproject"></span><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/docs/projects/{projectId}</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/DocsProject/operation/DocsProjectGetInfoV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает сведения о проекте в SIGNAL DOCS.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">project:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В пути замените <code style="white-space:normal;overflow-wrap:anywhere">{projectId}</code> на нужные значения.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — ID корневой папки в <code style="white-space:normal;overflow-wrap:anywhere">rootFolderId</code> и признак настроенного хранилища в <code style="white-space:normal;overflow-wrap:anywhere">isStorageConfigured</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/docs/projects/storage-id</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/DocsProject/operation/DocsProjectGetStorageIdV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает идентификатор хранилища, назначенного проекту.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">project:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В URL передайте <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — поле <code style="white-space:normal;overflow-wrap:anywhere">data</code> для идентификатора хранилища.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-projectuser"></span><code style="white-space:normal;overflow-wrap:anywhere">PUT /public/v1/project-users</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ProjectUser/operation/ProjectUserAddProjectsUsersV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Пакетно добавляет пользователей в несколько проектов.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">project:user:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectIds</code> и <code style="white-space:normal;overflow-wrap:anywhere">userIds</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">DELETE /public/v1/project-users</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ProjectUser/operation/ProjectUserDeleteProjectsUsersV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Пакетно удаляет пользователей из нескольких проектов.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">project:user:delete</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectIds</code> и <code style="white-space:normal;overflow-wrap:anywhere">userIds</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-projectusercustomrole"></span><code style="white-space:normal;overflow-wrap:anywhere">PUT /public/v1/project-user-custom-roles</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/ProjectUserCustomRole/operation/ProjectUserCustomRoleSetProjectUserCustomRolesV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Заменяет дополнительные роли пользователя в проекте переданным списком.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">project:role:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">customRoleIds</code>, <code style="white-space:normal;overflow-wrap:anywhere">projectId</code> и <code style="white-space:normal;overflow-wrap:anywhere">userId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-userlog"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/user-logs</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/UserLog/operation/UserLogListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает записи журнала действий пользователей по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">logs:user:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В теле запроса передайте JSON-объект. Все его поля необязательны. Для фильтрации можно указать <code style="white-space:normal;overflow-wrap:anywhere">projectIds</code>, <code style="white-space:normal;overflow-wrap:anywhere">userIds</code> и <code style="white-space:normal;overflow-wrap:anywhere">logTypes</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">type</code>.</div></details></td>
</tr>
</tbody>
</table>
</div>

#### Модели и ЭП
###### 3.9. Модели и подписи {#reference-models}

<div aria-label="Справочник API — Модели и ЭП" role="region" tabindex="0" style="width:100%;max-width:100%;box-sizing:border-box;overflow-x:auto;border:1px solid rgba(128,128,128,.32);border-radius:6px">
<table style="width:100%;min-width:48rem;table-layout:fixed;box-sizing:border-box;border:0;border-radius:0;margin:0">
<thead>
<tr>
<th style="width:30%;box-sizing:border-box">Метод и путь</th>
<th style="width:21%;box-sizing:border-box">Назначение</th>
<th style="width:15%;box-sizing:border-box">Scope</th>
<th style="width:34%;box-sizing:border-box">Контракт</th>
</tr>
</thead>
<tbody>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-forge"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/forge/convert</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Forge/operation/ForgeConvertV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Запускает преобразование модели через Forge для просмотра; поддерживаемые форматы перечислены в Swagger.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:viewer:execute</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">versionId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">204</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/forge/item-versions/viewer</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Forge/operation/ForgeGetViewersDataV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает токен доступа и URN моделей для отображения версий файлов в Forge Viewer.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:viewer:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">itemVersionIds</code> и <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — список моделей в <code style="white-space:normal;overflow-wrap:anywhere">models</code>, токен просмотра в <code style="white-space:normal;overflow-wrap:anywhere">token</code> и срок его действия в <code style="white-space:normal;overflow-wrap:anywhere">expiresIn</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-tangl"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/tangl/convert</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Tangl/operation/TanglConvertV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Запускает преобразование модели через Tangl для просмотра; схема указывает форматы .rvt и .ifc.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:viewer:execute</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">versionId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">204</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-cadessignature"></span><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/cades/signatures</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/CadesSignature/operation/CadesSignatureListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает CAdES-подписи версии файла.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:signing:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В URL передайте <code style="white-space:normal;overflow-wrap:anywhere">versionId</code>.<br>В URL можно добавить <code style="white-space:normal;overflow-wrap:anywhere">searchMchdIds</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">subject</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PUT /public/v1/cades/signatures</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/CadesSignature/operation/CadesSignatureCreateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Создаёт новую CAdES-подпись.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:signing:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">certificateId</code>, <code style="white-space:normal;overflow-wrap:anywhere">signature</code> и <code style="white-space:normal;overflow-wrap:anywhere">versionId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">204</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-embeddedsignature"></span><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/embedded/signatures</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/EmbeddedSignature/operation/EmbeddedSignatureListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает встроенные подписи элемента.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:signing:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В URL передайте <code style="white-space:normal;overflow-wrap:anywhere">itemId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">versionId</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">PUT /public/v1/embedded/signatures</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/EmbeddedSignature/operation/EmbeddedSignatureCreateV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Создаёт встроенную подпись.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:signing:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">certificateId</code>, <code style="white-space:normal;overflow-wrap:anywhere">itemId</code>, <code style="white-space:normal;overflow-wrap:anywhere">signature</code> и <code style="white-space:normal;overflow-wrap:anywhere">versionId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">204</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-mchd"></span><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/mchd/company</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Mchd/operation/MchdGetCompanyMchdDocumentsV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает UUID машиночитаемых доверенностей (МЧД) компании.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:signing:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — массив идентификаторов в поле <code style="white-space:normal;overflow-wrap:anywhere">data</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/mchd/cades/signatures/{cadesSignatureId}</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Mchd/operation/MchdGetAttachedMchdDocumentsV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает идентификаторы МЧД, связанных с CAdES-подписью.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:signing:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В пути замените <code style="white-space:normal;overflow-wrap:anywhere">{cadesSignatureId}</code> на нужные значения.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/mchd/{mchdId}/object/download</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Mchd/operation/MchdDownloadV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Выдаёт билет для скачивания МЧД.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:signing:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В пути замените <code style="white-space:normal;overflow-wrap:anywhere">{mchdId}</code> на нужные значения.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — подписанная ссылка в <code style="white-space:normal;overflow-wrap:anywhere">signedUrl</code> и срок её действия в секундах в <code style="white-space:normal;overflow-wrap:anywhere">ttlSec</code>.</div></details></td>
</tr>
</tbody>
</table>
</div>

#### Модули
###### 3.10. Другие модули {#reference-modules}

<div aria-label="Справочник API — Модули" role="region" tabindex="0" style="width:100%;max-width:100%;box-sizing:border-box;overflow-x:auto;border:1px solid rgba(128,128,128,.32);border-radius:6px">
<table style="width:100%;min-width:48rem;table-layout:fixed;box-sizing:border-box;border:0;border-radius:0;margin:0">
<thead>
<tr>
<th style="width:30%;box-sizing:border-box">Метод и путь</th>
<th style="width:21%;box-sizing:border-box">Назначение</th>
<th style="width:15%;box-sizing:border-box">Scope</th>
<th style="width:34%;box-sizing:border-box">Контракт</th>
</tr>
</thead>
<tbody>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-board"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/boards</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Board/operation/BoardListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает дашборды проекта по фильтру; удалённые дашборды исключены.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">dash:board:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">title</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-card"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/boards/cards</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Card/operation/CardListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает карточки дашборда с возможностью отбора по группам; удалённые карточки и карточки удалённых групп или дашбордов исключены.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">dash:card:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">boardId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code>, <code style="white-space:normal;overflow-wrap:anywhere">title</code> и <code style="white-space:normal;overflow-wrap:anywhere">type</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/boards/cards/{cardId}</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Card/operation/CardGetV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает карточку с содержимым по её идентификатору.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">dash:card:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В пути замените <code style="white-space:normal;overflow-wrap:anywhere">{cardId}</code> на нужные значения.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-объект с полями <code style="white-space:normal;overflow-wrap:anywhere">id</code>, <code style="white-space:normal;overflow-wrap:anywhere">modified</code>, <code style="white-space:normal;overflow-wrap:anywhere">modifiedBy</code> и <code style="white-space:normal;overflow-wrap:anywhere">added</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-cardpubliclink"></span><code style="white-space:normal;overflow-wrap:anywhere">PATCH /public/v1/card-public-links/regenerate</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/CardPublicLink/operation/CardPublicLinkRegenerateCardPubLinkV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Перегенерирует публичную ссылку на карточку дашборда.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">dash:card_public_link:update</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В URL передайте <code style="white-space:normal;overflow-wrap:anywhere">pubLink</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — новая публичная ссылка в поле <code style="white-space:normal;overflow-wrap:anywhere">publicLink</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-group"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/boards/groups</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Group/operation/GroupListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает группы карточек дашборда; удалённые группы и группы удалённого дашборда исключены.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">dash:group:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">boardId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">title</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-inspectionfolder"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/inspection/folders</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/InspectionFolder/operation/InspectionFolderListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает папки фотомониторинга проекта по фильтру с пагинацией.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">inspection:folder:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">name</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/inspection/folders/count</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/InspectionFolder/operation/InspectionFolderListCountV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Подсчитывает папки фотомониторинга по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">inspection:folder:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — число.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-plan"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/inspection/plans</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Plan/operation/PlanListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает планы фотомониторинга проекта по фильтру с пагинацией.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">inspection:plan:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">name</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/inspection/plans/count</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Plan/operation/PlanListCountV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Подсчитывает планы фотомониторинга по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">inspection:plan:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — число.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-point"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/inspection/points</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Point/operation/PointListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает точки фотомониторинга проекта по фильтру с пагинацией.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">inspection:point:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code>, <code style="white-space:normal;overflow-wrap:anywhere">name</code> и <code style="white-space:normal;overflow-wrap:anywhere">status</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/inspection/points/count</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Point/operation/PointListCountV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Подсчитывает точки фотомониторинга по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">inspection:point:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — число.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v1/inspection/points/{pointId}</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Point/operation/PointGetV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает точку фотомониторинга по идентификатору.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">inspection:point:read</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В пути замените <code style="white-space:normal;overflow-wrap:anywhere">{pointId}</code> на нужные значения.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-объект с полями <code style="white-space:normal;overflow-wrap:anywhere">id</code>, <code style="white-space:normal;overflow-wrap:anywhere">modified</code>, <code style="white-space:normal;overflow-wrap:anywhere">modifiedBy</code> и <code style="white-space:normal;overflow-wrap:anywhere">added</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-booking"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/bookings</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Booking/operation/BookingListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает бронирования компании интеграции, упорядоченные по времени изменения и идентификатору.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">settings:booking:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В теле JSON. В объекте <code style="white-space:normal;overflow-wrap:anywhere">paging</code> укажите <code style="white-space:normal;overflow-wrap:anywhere">take</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">status</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">DELETE /public/v1/bookings</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Booking/operation/BookingDeleteBatchV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Удаляет указанные бронирования компании интеграции.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">settings:booking:delete</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">bookingIds</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><span id="ref-v1-slot"></span><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/slots</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Slot/operation/SlotListV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает слоты компании интеграции, упорядоченные по началу и идентификатору.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">settings:slot:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В теле JSON. В объекте <code style="white-space:normal;overflow-wrap:anywhere">paging</code> укажите <code style="white-space:normal;overflow-wrap:anywhere">take</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code> и <code style="white-space:normal;overflow-wrap:anywhere">userId</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">DELETE /public/v1/slots</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Slot/operation/SlotDeleteBatchV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Удаляет указанные слоты компании интеграции.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">settings:slot:delete</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">slotIds</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — без тела.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v1/slots/create-batch</code><br><a href="https://api.sgnl.pro/openapi/redoc-v1/index.html#tag/Slot/operation/SlotCreateBatchV1">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Создаёт несколько слотов компании интеграции.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">settings:slot:create</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">slots</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">type</code> и <code style="white-space:normal;overflow-wrap:anywhere">index</code>.</div></details></td>
</tr>
</tbody>
</table>
</div>

#### API v2
###### 3.11. Методы v2 {#reference-v2}

<div aria-label="Справочник API — API v2" role="region" tabindex="0" style="width:100%;max-width:100%;box-sizing:border-box;overflow-x:auto;border:1px solid rgba(128,128,128,.32);border-radius:6px">
<table style="width:100%;min-width:48rem;table-layout:fixed;box-sizing:border-box;border:0;border-radius:0;margin:0">
<thead>
<tr>
<th style="width:30%;box-sizing:border-box">Метод и путь</th>
<th style="width:21%;box-sizing:border-box">Назначение</th>
<th style="width:15%;box-sizing:border-box">Scope</th>
<th style="width:34%;box-sizing:border-box">Контракт</th>
</tr>
</thead>
<tbody>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">GET /public/v2/dummy/{someId}</code><br><a href="https://api.sgnl.pro/openapi/redoc-v2/index.html#tag/Dummy/operation/DummyGetV2">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает переданный идентификатор и версию API.</td>
<td style="overflow-wrap:anywhere">Достаточно токена интеграции</td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В пути замените <code style="white-space:normal;overflow-wrap:anywhere">{someId}</code> на нужные значения.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-объект с полями <code style="white-space:normal;overflow-wrap:anywhere">controller</code>, <code style="white-space:normal;overflow-wrap:anywhere">accountId</code> и <code style="white-space:normal;overflow-wrap:anywhere">apiVersion</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v2/issues/events</code><br><a href="https://api.sgnl.pro/openapi/redoc-v2/index.html#tag/IssueEvents/operation/IssueEventsListV2">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Возвращает события замечаний по фильтру с пагинацией.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:issue:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br>Для пагинации в URL можно указать <code style="white-space:normal;overflow-wrap:anywhere">Take</code> и <code style="white-space:normal;overflow-wrap:anywhere">Skip</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — JSON-массив записей. Поля записи включают <code style="white-space:normal;overflow-wrap:anywhere">id</code>, <code style="white-space:normal;overflow-wrap:anywhere">itemId</code> и <code style="white-space:normal;overflow-wrap:anywhere">type</code>.</div></details></td>
</tr>
<tr>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">POST /public/v2/issues/events/count</code><br><a href="https://api.sgnl.pro/openapi/redoc-v2/index.html#tag/IssueEvents/operation/IssueEventsListCountV2">ReDoc</a></td>
<td style="overflow-wrap:anywhere">Подсчитывает события замечаний по фильтру.</td>
<td style="overflow-wrap:anywhere"><code style="white-space:normal;overflow-wrap:anywhere">docs:issue:list</code></td>
<td style="overflow-wrap:anywhere"><details style="box-sizing:border-box;max-width:100%"><summary>Контракт</summary><div><strong>Что передать</strong><br>В JSON-теле укажите <code style="white-space:normal;overflow-wrap:anywhere">projectId</code>.<br><br><strong>Ответ</strong><br><code style="white-space:normal;overflow-wrap:anywhere">200</code> — число в <code style="white-space:normal;overflow-wrap:anywhere">data</code>.</div></details></td>
</tr>
</tbody>
</table>
</div>

#### Ответы
###### 3.12. Коды ответов {#reference-errors}

| Код | Значение и следующий шаг |
| --- | --- |
| 200 / 204 | Успешное выполнение. Наличие и формат тела зависят от метода. |
| 400 | Ошибка запроса. Проверьте обязательные поля, типы, UUID, ограничения массивов и ответ ValidationProblemDetails. |
| 401 | Ошибка авторизации. Проверьте заголовок Bearer и срок действия токена. |
| 403 | Доступ запрещён. Проверьте scopes токена и доступ интеграции к нужным данным. |
| 404 | Запрошенный ресурс не найден. Проверьте идентификаторы и контекст запроса. |
| 422 | При получении токена, проверьте ключ, срок действия интеграции, разрешения и лицензию. |
| 429 | Превышена частота запросов. Повторите запрос после паузы из `Retry-After`. |
| 450 | Достигнута квота ресурса. Для увеличения квоты обратитесь в поддержку. |
| 500 | Ошибка сервера. Сохраните время, метод, путь и код ответа для обращения в поддержку, не передавая секреты. |
| 550 | Сервис временно недоступен. Повторите чтение позднее. Перед повтором записи проверьте её результат. |



#

<sub>**[<   SIGNAL. Что нового](/ru/general/updates)     **|**     [HUB. Введение   >](/ru/hub/intro)**</sub>
