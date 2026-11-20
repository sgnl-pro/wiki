---
title: Api New
description: 
published: true
date: 2026-11-20T14:36:28.524Z
tags: 
editor: markdown
dateCreated: 2026-11-17T13:04:57.412Z
---

<sub>**[<   SIGNAL. Что нового](/ru/general/updates)     **|**     [HUB. Введение   >](/ru/hub/intro)**</sub>

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
## 1. Начало работы
###### 1. Начало работы {#doc}

### Подразделы {.tabset}

#### 1.1. Адрес и документация
###### 1.1. Адрес и документация {#api-docs}

Адрес API — `https://api.sgnl.pro`. Версия входит в путь запроса, например `/public/v1/projects`.

- [Swagger](https://api.sgnl.pro/openapi/swagger/index.html) — описание методов и запуск запросов.
- Схемы OpenAPI для генерации клиентов — [v1](https://api.sgnl.pro/openapi/v1/schema.yml) и [v2](https://api.sgnl.pro/openapi/v2/schema.yml).

#### 1.2. Подключение и авторизация в Swagger
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

#### 1.3. Запросы, ответы и ограничения
###### 1.3. Запросы, ответы и ограничения {#api-rules}

В запросах к API передавайте токен в заголовке `Authorization: Bearer <token>`. Для тела в формате JSON используйте `Content-Type: application/json`.

- В методах с `Take` и `Skip` увеличивайте `Skip` на число полученных записей. Для списка согласований `Take` — до 50, для списка замечаний — до 200.
- Для передачи файлов используйте `signedUrl` из билета. Ссылка действует `ttlSec` секунд. Заголовок `Authorization` нужен в запросе к API за билетом. В хранилище передавайте только подписанную ссылку.
- При `429` повторите запрос после паузы, указанной в `Retry-After`. Если сервер не ответил на запрос записи, проверьте результат перед повтором.

## 2. Примеры
###### 2. Примеры {#examples}

### Подразделы {.tabset}

#### 2.1. Подготовка
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
| Проект | `GET /public/v1/projects` |
| Папка | `GET /public/v1/projects/{projectId}/folders/tree` |
| Файл | `GET /public/v1/items` |
| Версия файла | `GET /public/v1/versions` |
| Согласование | `POST /public/v1/reviews` |

Разрешения для этих запросов указаны в [справочнике](#reference). Файлы с результатами сохраняются в папке запуска, если Вы не указали другой путь. При совпадении имён скрипт перезапишет выходные файлы.

#### 2.2. Авторизация
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

#### 2.3. Загрузка файла
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

#### 2.4. Скачивание файла
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

#### 2.5. Данные согласования
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

#### 2.6. Реестр замечаний
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

#### 2.7. Видео и интеграции
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

## 3. Справочник API
###### 3. Справочник API {#reference}

При запросе токена передайте разрешение из колонки **Scope** в массиве `scopes`. В колонке **Что передать** указано, где передавать данные. Точка в имени поля обозначает вложенность. Например, `find.projectId` — поле `projectId` внутри объекта `find`. Полную схему полей и примеры запросов и ответов смотрите в Swagger. Если Swagger открыл общий список, найдите метод по пути из первой колонки. Для методов v2 сначала выберите схему **v2** в верхнем списке Swagger.
При запросе токена передайте разрешение из колонки **Scope** в массиве `scopes`. Раскройте **Контракт** в строке метода, чтобы посмотреть, что передать и какой ответ вернёт API. Точка в имени поля обозначает вложенность. Например, `find.projectId` — поле `projectId` внутри объекта `find`. Полную схему полей и примеры запросов и ответов смотрите в Swagger. Если Swagger открыл общий список, найдите метод по пути из первой колонки. Для методов v2 сначала выберите схему **v2** в верхнем списке Swagger.

### Разделы справочника {.tabset}
#### 3.1. Файлы и версии
###### 3.1. Файлы и версии {#reference-v1}

| Метод и путь | Назначение | Scope | Что передать | Что вернёт API |
| --- | --- | --- | --- | --- |
| <span id="ref-v1-item"></span>`PUT /public/v1/items/file`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemCreateV1) | Создаёт файл в папке и прикрепляет к нему существующую версию. | `docs:item:create` | JSON-объект, обязательные поля `folderId`, `name`, `versionId` | `200` — объект с идентификатором в `data` |
| `PUT /public/v1/items/link`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemCreateV1) | Создаёт элемент типа «ссылка» и возвращает его идентификатор. | `docs:item:create` | JSON-объект, обязательные поля `folderId`, `link`, `name` | `200` — объект с идентификатором в `data` |
| `GET /public/v1/items`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemListV1) | Возвращает файлы и ссылки в папке. | `docs:item:list` | В строке запроса — `folderId`<br>Необязательно — `deleted`, `Take`, `Skip` | `200` — массив записей |
| `GET /public/v1/items/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemListCountV1) | Возвращает число файлов и ссылок в папке. | `docs:item:list` | В строке запроса — `folderId`<br>Необязательно — `deleted` | `200` — объект с числом в `data` |
| `POST /public/v1/items/search`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemSearchV1) | Ищет элементы внутри папки, включая вложенные. | `docs:item:list` | Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `folderId` | `200` — массив записей |
| `GET /public/v1/items/item-version`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemGetItemVersionV1) | Возвращает версию элемента по её идентификатору. | `docs:item:read` | В строке запроса — `id` | `200` — JSON-объект |
| `GET /public/v1/items/download`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemDownloadV1) | Выдаёт ссылку для скачивания выбранной версии файла. | `docs:item:read` | В строке запроса — `itemId`, `versionId`<br>Необязательно — `fileName`, `urlTtlSecOverride` | `200` — объект с подписанной ссылкой `signedUrl` и сроком её действия `ttlSec` в секундах |
| `PUT /public/v1/items/versions`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemAttachVersionV1) | Прикрепляет новую версию к существующему элементу. | `docs:version:create` | JSON-объект, обязательные поля `itemId`, `versionId` | `204` — без тела ответа |
| `PATCH /public/v1/items/update`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemUpdateV1) | Обновляет существующий элемент. | `docs:item:update` | JSON-объект, обязательные поля `id` | `204` — без тела ответа |
| `PATCH /public/v1/items/move`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemMoveV1) | Перемещает элемент в другую папку. | `docs:item:update` | JSON-объект, обязательные поля `id`, `newFolderId` | `200` — без тела ответа |
| `PATCH /public/v1/items/versions/update`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemUpdateVersionV1) | Обновляет существующую версию элемента. | `docs:version:update` | JSON-объект, обязательные поля `id` | `204` — без тела ответа |
| `DELETE /public/v1/items/{itemId}`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemDeleteV1) | Перемещает элемент в корзину. | `docs:item:delete` | В пути — `itemId` | `204` — без тела ответа |
| <span id="ref-v1-version"></span>`POST /public/v1/versions`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Version/VersionCreateV1) | Создаёт новую версию объекта и возвращает её идентификатор. | `docs:version:create` | JSON-объект, обязательные поля `name`, `objectId`, `projectId` | `200` — объект с идентификатором в `data` |
| `GET /public/v1/versions`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Version/VersionListV1) | Возвращает версии элемента. | `docs:version:list` | В строке запроса — `itemId`<br>Необязательно — `Take`, `Skip` | `200` — массив версий. Поле `id` используется как `versionId` при скачивании |
| `POST /public/v1/versions/find-batch`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Version/VersionListBatchV1) | Возвращает версии для набора элементов. | `docs:version:list` | JSON-объект, обязательные поля `itemIds`, `projectId` | `200` — массив записей |
| `GET /public/v1/versions/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Version/VersionCountV1) | Подсчитывает версии элемента. | `docs:version:list` | В строке запроса — `itemId`<br>Необязательно — `Take`, `Skip` | `200` — объект с числом в `data` |
| <span id="ref-v1-object"></span>`PUT /public/v1/objects`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Object/ObjectCreateV1) | Выдаёт билет для загрузки объекта; после загрузки объект требуется подтвердить отдельным запросом. | `docs:object:create` | JSON-объект, обязательные поля `mimeType`, `projectId`, `size` | `200` — объект с `objectId`, ссылкой для загрузки `signedUrl` и сроком её действия `ttlSec` в секундах |
| `POST /public/v1/objects/{objectId}/uploading/commit`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Object/ObjectCommitUploadingV1) | Подтверждает завершение загрузки объекта в S3. | `docs:object:create` | В пути — `objectId` | `200` — без тела ответа |
| <span id="ref-v1-share"></span>`POST /public/v1/shares`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Share/ShareListV1) | Ищет публикации файлов по фильтру. | `docs:share:list` | Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `projectId` | `200` — массив записей |
| `PUT /public/v1/shares`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Share/ShareCreateV1) | Создаёт публикацию элемента. | `docs:share:create` | JSON-объект, обязательные поля `sharedItemId`, `sharedItemType`, `shareType` | `200` — объект с идентификатором в `data` |
| `PATCH /public/v1/shares`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Share/ShareUpdateV1) | Обновляет существующую публикацию. | `docs:share:update` | JSON-объект, обязательные поля `id` | `200` — без тела ответа |
| `DELETE /public/v1/shares`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Share/ShareDeleteV1) | Изменяет состояние удаления существующей публикации. | `docs:share:delete` | JSON-объект, обязательные поля `deleted`, `id` | `200` — без тела ответа |
| `POST /public/v1/shares/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Share/ShareListCountV1) | Подсчитывает публикации по фильтру. | `docs:share:list` | JSON-объект, обязательные поля `projectId` | `200` — объект с числом в `data` |
| Метод и путь | Назначение | Scope | Контракт |
| --- | --- | --- | --- |
| <span id="ref-v1-item"></span>`PUT /public/v1/items/file`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemCreateV1) | Создаёт файл в папке и прикрепляет к нему существующую версию. | `docs:item:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `folderId`, `name`, `versionId`<br><br>**Что вернёт API**<br>`200` — объект с идентификатором в `data`</details> |
| `PUT /public/v1/items/link`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemCreateV1) | Создаёт элемент типа «ссылка» и возвращает его идентификатор. | `docs:item:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `folderId`, `link`, `name`<br><br>**Что вернёт API**<br>`200` — объект с идентификатором в `data`</details> |
| `GET /public/v1/items`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemListV1) | Возвращает файлы и ссылки в папке. | `docs:item:list` | <details><summary>Контракт</summary><br>**Что передать**<br>В строке запроса — `folderId`<br>Необязательно — `deleted`, `Take`, `Skip`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `GET /public/v1/items/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemListCountV1) | Возвращает число файлов и ссылок в папке. | `docs:item:list` | <details><summary>Контракт</summary><br>**Что передать**<br>В строке запроса — `folderId`<br>Необязательно — `deleted`<br><br>**Что вернёт API**<br>`200` — объект с числом в `data`</details> |
| `POST /public/v1/items/search`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemSearchV1) | Ищет элементы внутри папки, включая вложенные. | `docs:item:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `folderId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `GET /public/v1/items/item-version`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemGetItemVersionV1) | Возвращает версию элемента по её идентификатору. | `docs:item:read` | <details><summary>Контракт</summary><br>**Что передать**<br>В строке запроса — `id`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| `GET /public/v1/items/download`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemDownloadV1) | Выдаёт ссылку для скачивания выбранной версии файла. | `docs:item:read` | <details><summary>Контракт</summary><br>**Что передать**<br>В строке запроса — `itemId`, `versionId`<br>Необязательно — `fileName`, `urlTtlSecOverride`<br><br>**Что вернёт API**<br>`200` — объект с подписанной ссылкой `signedUrl` и сроком её действия `ttlSec` в секундах</details> |
| `PUT /public/v1/items/versions`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemAttachVersionV1) | Прикрепляет новую версию к существующему элементу. | `docs:version:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `itemId`, `versionId`<br><br>**Что вернёт API**<br>`204` — без тела ответа</details> |
| `PATCH /public/v1/items/update`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemUpdateV1) | Обновляет существующий элемент. | `docs:item:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `id`<br><br>**Что вернёт API**<br>`204` — без тела ответа</details> |
| `PATCH /public/v1/items/move`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemMoveV1) | Перемещает элемент в другую папку. | `docs:item:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `id`, `newFolderId`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| `PATCH /public/v1/items/versions/update`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemUpdateVersionV1) | Обновляет существующую версию элемента. | `docs:version:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `id`<br><br>**Что вернёт API**<br>`204` — без тела ответа</details> |
| `DELETE /public/v1/items/{itemId}`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Item/ItemDeleteV1) | Перемещает элемент в корзину. | `docs:item:delete` | <details><summary>Контракт</summary><br>**Что передать**<br>В пути — `itemId`<br><br>**Что вернёт API**<br>`204` — без тела ответа</details> |
| <span id="ref-v1-version"></span>`POST /public/v1/versions`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Version/VersionCreateV1) | Создаёт новую версию объекта и возвращает её идентификатор. | `docs:version:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `name`, `objectId`, `projectId`<br><br>**Что вернёт API**<br>`200` — объект с идентификатором в `data`</details> |
| `GET /public/v1/versions`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Version/VersionListV1) | Возвращает версии элемента. | `docs:version:list` | <details><summary>Контракт</summary><br>**Что передать**<br>В строке запроса — `itemId`<br>Необязательно — `Take`, `Skip`<br><br>**Что вернёт API**<br>`200` — массив версий. Поле `id` используется как `versionId` при скачивании</details> |
| `POST /public/v1/versions/find-batch`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Version/VersionListBatchV1) | Возвращает версии для набора элементов. | `docs:version:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `itemIds`, `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `GET /public/v1/versions/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Version/VersionCountV1) | Подсчитывает версии элемента. | `docs:version:list` | <details><summary>Контракт</summary><br>**Что передать**<br>В строке запроса — `itemId`<br>Необязательно — `Take`, `Skip`<br><br>**Что вернёт API**<br>`200` — объект с числом в `data`</details> |
| <span id="ref-v1-object"></span>`PUT /public/v1/objects`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Object/ObjectCreateV1) | Выдаёт билет для загрузки объекта; после загрузки объект требуется подтвердить отдельным запросом. | `docs:object:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `mimeType`, `projectId`, `size`<br><br>**Что вернёт API**<br>`200` — объект с `objectId`, ссылкой для загрузки `signedUrl` и сроком её действия `ttlSec` в секундах</details> |
| `POST /public/v1/objects/{objectId}/uploading/commit`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Object/ObjectCommitUploadingV1) | Подтверждает завершение загрузки объекта в S3. | `docs:object:create` | <details><summary>Контракт</summary><br>**Что передать**<br>В пути — `objectId`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| <span id="ref-v1-share"></span>`POST /public/v1/shares`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Share/ShareListV1) | Ищет публикации файлов по фильтру. | `docs:share:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `PUT /public/v1/shares`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Share/ShareCreateV1) | Создаёт публикацию элемента. | `docs:share:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `sharedItemId`, `sharedItemType`, `shareType`<br><br>**Что вернёт API**<br>`200` — объект с идентификатором в `data`</details> |
| `PATCH /public/v1/shares`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Share/ShareUpdateV1) | Обновляет существующую публикацию. | `docs:share:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `id`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| `DELETE /public/v1/shares`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Share/ShareDeleteV1) | Изменяет состояние удаления существующей публикации. | `docs:share:delete` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `deleted`, `id`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| `POST /public/v1/shares/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Share/ShareListCountV1) | Подсчитывает публикации по фильтру. | `docs:share:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — объект с числом в `data`</details> |

#### 3.2. Папки и доступ
###### 3.2. Папки и доступ {#reference-folders}

| Метод и путь | Назначение | Scope | Что передать | Что вернёт API |
| --- | --- | --- | --- | --- |
| <span id="ref-v1-folder"></span>`GET /public/v1/folders/{folderId}/children`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Folder/FolderListChildrenV1) | Возвращает непосредственных потомков папки. | `docs:folder:list` | В пути — `folderId`<br>Необязательно в строке запроса — `deleted` | `200` — массив записей |
| `PUT /public/v1/folders`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Folder/FolderCreateV1) | Создаёт папку и возвращает её идентификатор. | `docs:folder:create` | JSON-объект, обязательные поля `name`, `parentId` | `200` — объект с идентификатором в `data` |
| `PATCH /public/v1/folders`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Folder/FolderUpdateV1) | Обновляет папку. | `docs:folder:update` | JSON-объект, обязательные поля `id` | `204` — без тела ответа |
| `DELETE /public/v1/folders/{folderId}`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Folder/FolderDeleteV1) | Перемещает папку в корзину. | `docs:folder:delete` | В пути — `folderId` | `204` — без тела ответа |
| `GET /public/v1/projects/{projectId}/folders/tree`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Folder/FolderGetProjectTreeV1) | Возвращает полное дерево папок проекта с правами пользователя. | `docs:folder:read` | В пути — `projectId` | `200` — JSON-объект |
| <span id="ref-v1-folderitemsnamingpattern"></span>`GET /public/v1/naming-patterns/folder-items/find`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/FolderItemsNamingPattern/FolderItemsNamingPatternFindV1) | Возвращает правила именования файлов в папке. | `docs:item:create` | В строке запроса — `folderId` | `200` — JSON-объект |
| <span id="ref-v1-storage"></span>`POST /public/v1/storages`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Storage/StorageListV1) | Ищет хранилища документов по фильтру. | `docs:storage:list` | JSON-объект с параметрами запроса | `200` — массив записей |
| <span id="ref-v1-permissions"></span>`POST /public/v1/permissions/folders/upsert`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Permissions/PermissionsUpsertBatchV1) | Создаёт или обновляет права пользователей и ролей на конкретную папку. | `docs:permissions:update` | JSON-объект, обязательные поля `folderId`, `items` | `200` — без тела ответа<br>`204` — без тела ответа |
| `GET /public/v1/permissions/tree`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Permissions/PermissionsGetProjectPermissionsTreeV1) | Возвращает дерево папок проекта с назначенными правами. | `docs:permissions:read` | В строке запроса — `projectId` | `200` — JSON-объект |
| `DELETE /public/v1/permissions/{permissionId}`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Permissions/PermissionsDeleteV1) | Удаляет конкретное разрешение. | `docs:permissions:update` | В пути — `permissionId` | `200` — без тела ответа |
| Метод и путь | Назначение | Scope | Контракт |
| --- | --- | --- | --- |
| <span id="ref-v1-folder"></span>`GET /public/v1/folders/{folderId}/children`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Folder/FolderListChildrenV1) | Возвращает непосредственных потомков папки. | `docs:folder:list` | <details><summary>Контракт</summary><br>**Что передать**<br>В пути — `folderId`<br>Необязательно в строке запроса — `deleted`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `PUT /public/v1/folders`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Folder/FolderCreateV1) | Создаёт папку и возвращает её идентификатор. | `docs:folder:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `name`, `parentId`<br><br>**Что вернёт API**<br>`200` — объект с идентификатором в `data`</details> |
| `PATCH /public/v1/folders`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Folder/FolderUpdateV1) | Обновляет папку. | `docs:folder:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `id`<br><br>**Что вернёт API**<br>`204` — без тела ответа</details> |
| `DELETE /public/v1/folders/{folderId}`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Folder/FolderDeleteV1) | Перемещает папку в корзину. | `docs:folder:delete` | <details><summary>Контракт</summary><br>**Что передать**<br>В пути — `folderId`<br><br>**Что вернёт API**<br>`204` — без тела ответа</details> |
| `GET /public/v1/projects/{projectId}/folders/tree`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Folder/FolderGetProjectTreeV1) | Возвращает полное дерево папок проекта с правами пользователя. | `docs:folder:read` | <details><summary>Контракт</summary><br>**Что передать**<br>В пути — `projectId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| <span id="ref-v1-folderitemsnamingpattern"></span>`GET /public/v1/naming-patterns/folder-items/find`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/FolderItemsNamingPattern/FolderItemsNamingPatternFindV1) | Возвращает правила именования файлов в папке. | `docs:item:create` | <details><summary>Контракт</summary><br>**Что передать**<br>В строке запроса — `folderId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| <span id="ref-v1-storage"></span>`POST /public/v1/storages`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Storage/StorageListV1) | Ищет хранилища документов по фильтру. | `docs:storage:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект с параметрами запроса<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| <span id="ref-v1-permissions"></span>`POST /public/v1/permissions/folders/upsert`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Permissions/PermissionsUpsertBatchV1) | Создаёт или обновляет права пользователей и ролей на конкретную папку. | `docs:permissions:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `folderId`, `items`<br><br>**Что вернёт API**<br>`200` — без тела ответа<br>`204` — без тела ответа</details> |
| `GET /public/v1/permissions/tree`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Permissions/PermissionsGetProjectPermissionsTreeV1) | Возвращает дерево папок проекта с назначенными правами. | `docs:permissions:read` | <details><summary>Контракт</summary><br>**Что передать**<br>В строке запроса — `projectId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| `DELETE /public/v1/permissions/{permissionId}`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Permissions/PermissionsDeleteV1) | Удаляет конкретное разрешение. | `docs:permissions:update` | <details><summary>Контракт</summary><br>**Что передать**<br>В пути — `permissionId`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |

#### 3.3. Замечания
###### 3.3. Замечания {#reference-issues}

| Метод и путь | Назначение | Scope | Что передать | Что вернёт API |
| --- | --- | --- | --- | --- |
| <span id="ref-v1-issue"></span>`POST /public/v1/issues`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Issue/IssueListV1) | Ищет замечания по фильтру с пагинацией. | `docs:issue:list` | Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `projectId` | `200` — массив записей |
| `PATCH /public/v1/issues`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Issue/IssueUpdateV1) | Пакетно обновляет несколько замечаний. | `docs:issue:update` | JSON-массив, в каждой записи нужны `id` | `200` — без тела ответа |
| `POST /public/v1/issues/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Issue/IssueListCountV1) | Подсчитывает замечания по фильтру. | `docs:issue:list` | JSON-объект, обязательные поля `projectId` | `200` — объект с числом в `data` |
| `POST /public/v1/issues/items/counts`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Issue/IssueListItemIssuesCountV1) | Возвращает число замечаний, связанных с каждым из указанных элементов. | `docs:issue:list` | JSON-объект, обязательные поля `itemIds`, `projectId` | `200` — массив записей |
| `POST /public/v1/issues/create`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Issue/IssueCreateV1) | Создаёт замечание. | `docs:issue:create` | JSON-объект, обязательные поля `authorId`, `issueTypeId`, `name`, `projectId`, `responsible`, `status` | `200` — идентификатор (UUID) |
| <span id="ref-v1-issueaccesses"></span>`POST /public/v1/issues/accesses`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueAccesses/IssueAccessesListV1) | Возвращает правила доступа к замечаниям. | `docs:issue:list` | JSON-объект, обязательные поля `issueTypeIds` | `200` — массив записей |
| <span id="ref-v1-issueattachment"></span>`POST /public/v1/issues/attachments`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueAttachment/IssueAttachmentListV1) | Возвращает вложения указанного замечания. | `docs:issue:list` | JSON-объект, обязательные поля `issueId` | `200` — массив записей |
| `POST /public/v1/issues/attachments/object/download`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueAttachment/IssueAttachmentDownloadObjectV1) | Создаёт билет для скачивания объекта вложения. | `docs:issue:read` | JSON-объект, обязательные поля `issueAttachmentId` | `200` — JSON-объект |
| <span id="ref-v1-issuecomment"></span>`POST /public/v1/issues/comments`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueComment/IssueCommentListV1) | Возвращает комментарии к замечаниям проекта. | `docs:issue:list` | Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `issueIds`, `projectId` | `200` — массив записей |
| `PUT /public/v1/issues/comments`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueComment/IssueCommentCreateV1) | Создаёт комментарий к указанному замечанию. | `docs:issue:create` | JSON-объект, обязательные поля `issueId`, `text` | `200` — объект с идентификатором в `data` |
| `POST /public/v1/issues/comments/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueComment/IssueCommentListCountV1) | Подсчитывает комментарии по фильтру. | `docs:issue:list` | JSON-объект, обязательные поля `issueIds`, `projectId` | `200` — объект с числом в `data` |
| <span id="ref-v1-issueevents"></span>`POST /public/v1/issues/events`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueEvents/IssueEventsListV1) | Возвращает события замечаний по фильтру с пагинацией. | `docs:issue:list` | Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `issueId` | `200` — массив записей |
| `POST /public/v1/issues/events/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueEvents/IssueEventsListCountV1) | Подсчитывает события замечаний по фильтру. | `docs:issue:list` | JSON-объект, обязательные поля `issueId` | `200` — объект с числом в `data` |
| <span id="ref-v1-issueprojectsettings"></span>`GET /public/v1/issues/settings/project`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueProjectSettings/IssueProjectSettingsGetV1) | Возвращает настройки замечаний для проекта. | `docs:issue:read` | В строке запроса — `projectId` | `200` — JSON-объект |
| <span id="ref-v1-issuetype"></span>`POST /public/v1/issues/types`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueType/IssueTypeListV1) | Ищет типы замечаний по фильтру. | `docs:issue:list` | JSON-объект, обязательные поля `projectId` | `200` — массив записей |
| Метод и путь | Назначение | Scope | Контракт |
| --- | --- | --- | --- |
| <span id="ref-v1-issue"></span>`POST /public/v1/issues`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Issue/IssueListV1) | Ищет замечания по фильтру с пагинацией. | `docs:issue:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `PATCH /public/v1/issues`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Issue/IssueUpdateV1) | Пакетно обновляет несколько замечаний. | `docs:issue:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-массив, в каждой записи нужны `id`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| `POST /public/v1/issues/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Issue/IssueListCountV1) | Подсчитывает замечания по фильтру. | `docs:issue:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — объект с числом в `data`</details> |
| `POST /public/v1/issues/items/counts`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Issue/IssueListItemIssuesCountV1) | Возвращает число замечаний, связанных с каждым из указанных элементов. | `docs:issue:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `itemIds`, `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `POST /public/v1/issues/create`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Issue/IssueCreateV1) | Создаёт замечание. | `docs:issue:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `authorId`, `issueTypeId`, `name`, `projectId`, `responsible`, `status`<br><br>**Что вернёт API**<br>`200` — идентификатор (UUID)</details> |
| <span id="ref-v1-issueaccesses"></span>`POST /public/v1/issues/accesses`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueAccesses/IssueAccessesListV1) | Возвращает правила доступа к замечаниям. | `docs:issue:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `issueTypeIds`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| <span id="ref-v1-issueattachment"></span>`POST /public/v1/issues/attachments`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueAttachment/IssueAttachmentListV1) | Возвращает вложения указанного замечания. | `docs:issue:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `issueId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `POST /public/v1/issues/attachments/object/download`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueAttachment/IssueAttachmentDownloadObjectV1) | Создаёт билет для скачивания объекта вложения. | `docs:issue:read` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `issueAttachmentId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| <span id="ref-v1-issuecomment"></span>`POST /public/v1/issues/comments`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueComment/IssueCommentListV1) | Возвращает комментарии к замечаниям проекта. | `docs:issue:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `issueIds`, `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `PUT /public/v1/issues/comments`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueComment/IssueCommentCreateV1) | Создаёт комментарий к указанному замечанию. | `docs:issue:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `issueId`, `text`<br><br>**Что вернёт API**<br>`200` — объект с идентификатором в `data`</details> |
| `POST /public/v1/issues/comments/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueComment/IssueCommentListCountV1) | Подсчитывает комментарии по фильтру. | `docs:issue:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `issueIds`, `projectId`<br><br>**Что вернёт API**<br>`200` — объект с числом в `data`</details> |
| <span id="ref-v1-issueevents"></span>`POST /public/v1/issues/events`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueEvents/IssueEventsListV1) | Возвращает события замечаний по фильтру с пагинацией. | `docs:issue:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `issueId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `POST /public/v1/issues/events/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueEvents/IssueEventsListCountV1) | Подсчитывает события замечаний по фильтру. | `docs:issue:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `issueId`<br><br>**Что вернёт API**<br>`200` — объект с числом в `data`</details> |
| <span id="ref-v1-issueprojectsettings"></span>`GET /public/v1/issues/settings/project`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueProjectSettings/IssueProjectSettingsGetV1) | Возвращает настройки замечаний для проекта. | `docs:issue:read` | <details><summary>Контракт</summary><br>**Что передать**<br>В строке запроса — `projectId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| <span id="ref-v1-issuetype"></span>`POST /public/v1/issues/types`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/IssueType/IssueTypeListV1) | Ищет типы замечаний по фильтру. | `docs:issue:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |

#### 3.4. Согласования
###### 3.4. Согласования {#reference-reviews}

| Метод и путь | Назначение | Scope | Что передать | Что вернёт API |
| --- | --- | --- | --- | --- |
| <span id="ref-v1-review"></span>`POST /public/v1/reviews`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Review/ReviewListV1) | Возвращает согласования проекта. | `docs:review:list` | Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `find.projectId` | `200` — массив согласований. В `topVersion` — данные последней версии |
| `PATCH /public/v1/reviews`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Review/ReviewUpdateV1) | Изменяет основные сведения согласования. | `docs:review:update` | JSON-объект, обязательные поля `id` | `200` — без тела ответа |
| `POST /public/v1/reviews/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Review/ReviewListCountV1) | Подсчитывает согласования по фильтру. | `docs:review:list` | JSON-объект, обязательные поля `projectId` | `200` — объект с числом в `data` |
| `POST /public/v1/reviews/versions`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Review/ReviewGetVersionsV1) | Возвращает версии согласований по указанным идентификаторам. | `docs:review:list` | JSON-объект, обязательные поля `reviewVersionIds` | `200` — массив записей |
| `POST /public/v1/reviews/versions/item-versions`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Review/ReviewFindItemVersionIdsByReviewVersionIdsV1) | Возвращает идентификаторы версий элементов, сгруппированные по версиям согласований. | `docs:review:list` | JSON-объект, обязательные поля `reviewVersionIds` | `200` — объект, где ключ — ID версии согласования, значение — массив ID версий элементов |
| `POST /public/v1/reviews/create`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Review/ReviewCreateV1) | Создаёт согласование. | `docs:review:create` | JSON-объект, обязательные поля `behalfUserId`, `cipher`, `name`, `projectId`, `reviewTypeId` | `200` — идентификатор (UUID) |
| `PATCH /public/v1/reviews/type`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Review/ReviewSetTypeV1) | Устанавливает или изменяет тип согласования. | `docs:review:update` | JSON-объект, обязательные поля `id`, `reviewTypeId` | `200` — без тела ответа |
| `PATCH /public/v1/reviews/comment`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Review/ReviewSetCommentV1) | Устанавливает или очищает комментарий последней версии согласования, кроме удалённого согласования. | `docs:review:update` | JSON-объект, обязательные поля `authorId`, `comment`, `id` | `200` — без тела ответа |
| <span id="ref-v1-reviewgroup"></span>`POST /public/v1/reviews/groups`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ReviewGroup/ReviewGroupListV1) | Возвращает группы согласований проекта. | `docs:review:list` | Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `projectId` | `200` — массив записей |
| <span id="ref-v1-reviewitem"></span>`POST /public/v1/reviews/items`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ReviewItem/ReviewItemGetReviewItemsStatusesV1) | Возвращает статусы согласования указанных версий элементов. | `docs:review:list` | JSON-объект, обязательные поля `itemVersionIds`, `projectId` | `200` — массив записей |
| `POST /public/v1/reviews/items/add`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ReviewItem/ReviewItemAddItemV1) | Добавляет версию элемента в существующее согласование. | `docs:review:update` | JSON-объект, обязательные поля `itemVersionId`, `reviewId` | `200` — без тела ответа |
| `POST /public/v1/reviews/items/remove`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ReviewItem/ReviewItemRemoveItemV1) | Удаляет версию элемента из согласования. | `docs:review:update` | JSON-объект, обязательные поля `itemVersionId`, `reviewId` | `200` — без тела ответа |
| <span id="ref-v1-reviewprocess"></span>`POST /public/v1/reviews/process/start`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ReviewProcess/ReviewProcessStartV1) | Запускает процесс указанного согласования. | `docs:review:update` | JSON-объект, обязательные поля `behalfUserId`, `reviewId` | `200` — без тела ответа |
| <span id="ref-v1-reviewtype"></span>`GET /public/v1/reviews/types/names`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ReviewType/ReviewTypeFindNamesV1) | Возвращает названия типов согласований проекта. | `docs:review:list` | В строке запроса — `projectId` | `200` — массив записей |
| `POST /public/v1/reviews/types/create`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ReviewType/ReviewTypeCreateV1) | Создаёт тип согласования проекта. | `docs:review:create` | JSON-объект, обязательные поля `name`, `projectId`, `version` | `200` — идентификатор (UUID) |
| `PATCH /public/v1/reviews/types`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ReviewType/ReviewTypeUpdateV1) | Обновляет существующий тип согласования. | `docs:review:update` | JSON-объект, обязательные поля `id`, `projectId` | `200` — без тела ответа |
| Метод и путь | Назначение | Scope | Контракт |
| --- | --- | --- | --- |
| <span id="ref-v1-review"></span>`POST /public/v1/reviews`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Review/ReviewListV1) | Возвращает согласования проекта. | `docs:review:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `find.projectId`<br><br>**Что вернёт API**<br>`200` — массив согласований. В `topVersion` — данные последней версии</details> |
| `PATCH /public/v1/reviews`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Review/ReviewUpdateV1) | Изменяет основные сведения согласования. | `docs:review:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `id`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| `POST /public/v1/reviews/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Review/ReviewListCountV1) | Подсчитывает согласования по фильтру. | `docs:review:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — объект с числом в `data`</details> |
| `POST /public/v1/reviews/versions`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Review/ReviewGetVersionsV1) | Возвращает версии согласований по указанным идентификаторам. | `docs:review:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `reviewVersionIds`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `POST /public/v1/reviews/versions/item-versions`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Review/ReviewFindItemVersionIdsByReviewVersionIdsV1) | Возвращает идентификаторы версий элементов, сгруппированные по версиям согласований. | `docs:review:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `reviewVersionIds`<br><br>**Что вернёт API**<br>`200` — объект, где ключ — ID версии согласования, значение — массив ID версий элементов</details> |
| `POST /public/v1/reviews/create`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Review/ReviewCreateV1) | Создаёт согласование. | `docs:review:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `behalfUserId`, `cipher`, `name`, `projectId`, `reviewTypeId`<br><br>**Что вернёт API**<br>`200` — идентификатор (UUID)</details> |
| `PATCH /public/v1/reviews/type`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Review/ReviewSetTypeV1) | Устанавливает или изменяет тип согласования. | `docs:review:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `id`, `reviewTypeId`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| `PATCH /public/v1/reviews/comment`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Review/ReviewSetCommentV1) | Устанавливает или очищает комментарий последней версии согласования, кроме удалённого согласования. | `docs:review:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `authorId`, `comment`, `id`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| <span id="ref-v1-reviewgroup"></span>`POST /public/v1/reviews/groups`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ReviewGroup/ReviewGroupListV1) | Возвращает группы согласований проекта. | `docs:review:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| <span id="ref-v1-reviewitem"></span>`POST /public/v1/reviews/items`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ReviewItem/ReviewItemGetReviewItemsStatusesV1) | Возвращает статусы согласования указанных версий элементов. | `docs:review:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `itemVersionIds`, `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `POST /public/v1/reviews/items/add`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ReviewItem/ReviewItemAddItemV1) | Добавляет версию элемента в существующее согласование. | `docs:review:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `itemVersionId`, `reviewId`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| `POST /public/v1/reviews/items/remove`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ReviewItem/ReviewItemRemoveItemV1) | Удаляет версию элемента из согласования. | `docs:review:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `itemVersionId`, `reviewId`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| <span id="ref-v1-reviewprocess"></span>`POST /public/v1/reviews/process/start`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ReviewProcess/ReviewProcessStartV1) | Запускает процесс указанного согласования. | `docs:review:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `behalfUserId`, `reviewId`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| <span id="ref-v1-reviewtype"></span>`GET /public/v1/reviews/types/names`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ReviewType/ReviewTypeFindNamesV1) | Возвращает названия типов согласований проекта. | `docs:review:list` | <details><summary>Контракт</summary><br>**Что передать**<br>В строке запроса — `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `POST /public/v1/reviews/types/create`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ReviewType/ReviewTypeCreateV1) | Создаёт тип согласования проекта. | `docs:review:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `name`, `projectId`, `version`<br><br>**Что вернёт API**<br>`200` — идентификатор (UUID)</details> |
| `PATCH /public/v1/reviews/types`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ReviewType/ReviewTypeUpdateV1) | Обновляет существующий тип согласования. | `docs:review:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `id`, `projectId`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |

#### 3.5. Передачи
###### 3.5. Передачи {#reference-transfers}

| Метод и путь | Назначение | Scope | Что передать | Что вернёт API |
| --- | --- | --- | --- | --- |
| <span id="ref-v1-documentstransfer"></span>`POST /public/v1/documents-transfers`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransfer/DocumentsTransferListV1) | Ищет передачи документов по фильтру с пагинацией. | `docs:docs_transfer:list` | Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `projectId` | `200` — массив записей |
| `GET /public/v1/documents-transfers`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransfer/DocumentsTransferGetAllDataV1) | Возвращает подробные сведения об одной передаче документов по её идентификатору. | `docs:docs_transfer:read` | В строке запроса — `id` | `200` — JSON-объект |
| `POST /public/v1/documents-transfers/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransfer/DocumentsTransferListCountV1) | Подсчитывает передачи документов по фильтру. | `docs:docs_transfer:list` | JSON-объект, обязательные поля `projectId` | `200` — объект с числом в `data` |
| `POST /public/v1/documents-transfers/create`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransfer/DocumentsTransferCreateV1) | Создаёт передачу документов. | `docs:docs_transfer:create` | JSON-объект, обязательные поля `authorId`, `cipher`, `documentsTransferTypeId`, `name` | `200` — идентификатор (UUID) |
| <span id="ref-v1-documentstransferacceptance"></span>`POST /public/v1/documents-transfer-acceptances/send`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransferAcceptance/DocumentsTransferAcceptanceSendV1) | Отправляет подготовленную передачу документов получателю. | `docs:docs_transfer:update` | JSON-объект, обязательные поля `authorId`, `documentsTransferId`, `recipient` | `200` — без тела ответа |
| <span id="ref-v1-documentstransferaccesses"></span>`POST /public/v1/documents-transfers/accesses`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransferAccesses/DocumentsTransferAccessesListV1) | Возвращает правила доступа для указанных типов передачи документов. | `docs:docs_transfer:list` | Необязательное тело — JSON-объект, обязательные поля `documentsTransferTypeIds` | `200` — массив записей |
| <span id="ref-v1-documentstransferitem"></span>`POST /public/v1/documents-transfer-items`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransferItem/DocumentsTransferItemListV1) | Возвращает элементы указанной передачи документов с пагинацией. | `docs:docs_transfer:list` | Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `documentsTransferId` | `200` — массив записей |
| `POST /public/v1/documents-transfer-items/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransferItem/DocumentsTransferItemListCountV1) | Подсчитывает элементы указанной передачи документов. | `docs:docs_transfer:list` | JSON-объект, обязательные поля `documentsTransferId` | `200` — объект с числом в `data` |
| `GET /public/v1/documents-transfer-items/download`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransferItem/DocumentsTransferItemDownloadV1) | Выдаёт временный билет для скачивания элемента передачи документов. | `docs:docs_transfer:read` | В строке запроса — `documentsTransferItemId`<br>Необязательно — `fileName` | `200` — JSON-объект |
| `POST /public/v1/documents-transfer-items/add`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransferItem/DocumentsTransferItemAddItemsV1) | Добавляет версии элементов в передачу документов. | `docs:docs_transfer:update` | JSON-объект, обязательные поля `documentsTransferId`, `itemVersionIds` | `200` — без тела ответа |
| <span id="ref-v1-documentstransfertype"></span>`POST /public/v1/documents-transfers/types`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransferType/DocumentsTransferTypeListV1) | Ищет типы передачи документов по фильтру. | `docs:docs_transfer:list` | JSON-объект, обязательные поля `projectId` | `200` — массив записей |
| <span id="ref-v1-acceptancecertificate"></span>`GET /public/v1/acceptance-certificates/download`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AcceptanceCertificate/AcceptanceCertificateDownloadV1) | Выдаёт временный билет для скачивания файла акта приёмки. | `docs:docs_transfer:read` | В строке запроса — `acceptanceCertificateId`<br>Необязательно — `fileName` | `200` — JSON-объект |
| `POST /public/v1/acceptance-certificates/attach`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AcceptanceCertificate/AcceptanceCertificateAttachV1) | Прикрепляет акт приёмки к передаче документов. | `docs:docs_transfer:update` | JSON-объект, обязательные поля `authorId`, `companyRecipient`, `companySender`, `documentsTransferId`, `projectName` | `200` — идентификатор (UUID) |
| Метод и путь | Назначение | Scope | Контракт |
| --- | --- | --- | --- |
| <span id="ref-v1-documentstransfer"></span>`POST /public/v1/documents-transfers`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransfer/DocumentsTransferListV1) | Ищет передачи документов по фильтру с пагинацией. | `docs:docs_transfer:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `GET /public/v1/documents-transfers`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransfer/DocumentsTransferGetAllDataV1) | Возвращает подробные сведения об одной передаче документов по её идентификатору. | `docs:docs_transfer:read` | <details><summary>Контракт</summary><br>**Что передать**<br>В строке запроса — `id`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| `POST /public/v1/documents-transfers/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransfer/DocumentsTransferListCountV1) | Подсчитывает передачи документов по фильтру. | `docs:docs_transfer:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — объект с числом в `data`</details> |
| `POST /public/v1/documents-transfers/create`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransfer/DocumentsTransferCreateV1) | Создаёт передачу документов. | `docs:docs_transfer:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `authorId`, `cipher`, `documentsTransferTypeId`, `name`<br><br>**Что вернёт API**<br>`200` — идентификатор (UUID)</details> |
| <span id="ref-v1-documentstransferacceptance"></span>`POST /public/v1/documents-transfer-acceptances/send`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransferAcceptance/DocumentsTransferAcceptanceSendV1) | Отправляет подготовленную передачу документов получателю. | `docs:docs_transfer:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `authorId`, `documentsTransferId`, `recipient`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| <span id="ref-v1-documentstransferaccesses"></span>`POST /public/v1/documents-transfers/accesses`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransferAccesses/DocumentsTransferAccessesListV1) | Возвращает правила доступа для указанных типов передачи документов. | `docs:docs_transfer:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательное тело — JSON-объект, обязательные поля `documentsTransferTypeIds`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| <span id="ref-v1-documentstransferitem"></span>`POST /public/v1/documents-transfer-items`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransferItem/DocumentsTransferItemListV1) | Возвращает элементы указанной передачи документов с пагинацией. | `docs:docs_transfer:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `documentsTransferId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `POST /public/v1/documents-transfer-items/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransferItem/DocumentsTransferItemListCountV1) | Подсчитывает элементы указанной передачи документов. | `docs:docs_transfer:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `documentsTransferId`<br><br>**Что вернёт API**<br>`200` — объект с числом в `data`</details> |
| `GET /public/v1/documents-transfer-items/download`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransferItem/DocumentsTransferItemDownloadV1) | Выдаёт временный билет для скачивания элемента передачи документов. | `docs:docs_transfer:read` | <details><summary>Контракт</summary><br>**Что передать**<br>В строке запроса — `documentsTransferItemId`<br>Необязательно — `fileName`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| `POST /public/v1/documents-transfer-items/add`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransferItem/DocumentsTransferItemAddItemsV1) | Добавляет версии элементов в передачу документов. | `docs:docs_transfer:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `documentsTransferId`, `itemVersionIds`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| <span id="ref-v1-documentstransfertype"></span>`POST /public/v1/documents-transfers/types`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocumentsTransferType/DocumentsTransferTypeListV1) | Ищет типы передачи документов по фильтру. | `docs:docs_transfer:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| <span id="ref-v1-acceptancecertificate"></span>`GET /public/v1/acceptance-certificates/download`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AcceptanceCertificate/AcceptanceCertificateDownloadV1) | Выдаёт временный билет для скачивания файла акта приёмки. | `docs:docs_transfer:read` | <details><summary>Контракт</summary><br>**Что передать**<br>В строке запроса — `acceptanceCertificateId`<br>Необязательно — `fileName`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| `POST /public/v1/acceptance-certificates/attach`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AcceptanceCertificate/AcceptanceCertificateAttachV1) | Прикрепляет акт приёмки к передаче документов. | `docs:docs_transfer:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `authorId`, `companyRecipient`, `companySender`, `documentsTransferId`, `projectName`<br><br>**Что вернёт API**<br>`200` — идентификатор (UUID)</details> |

#### 3.6. Формы
###### 3.6. Формы {#reference-forms}

| Метод и путь | Назначение | Scope | Что передать | Что вернёт API |
| --- | --- | --- | --- | --- |
| <span id="ref-v1-projectform"></span>`POST /public/v1/projects/forms`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormListV1) | Ищет формы проекта по фильтру и сортировке с пагинацией. | `forms:project_form:list` | Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `find.formTypeId`, `find.projectId` | `200` — JSON-объект |
| `POST /public/v1/projects/forms/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormListCountV1) | Подсчитывает формы проекта по фильтру. | `forms:project_form:list` | JSON-объект, обязательные поля `formTypeId`, `projectId` | `200` — число |
| `POST /public/v1/projects/forms/get`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormGetV1) | Возвращает форму проекта по идентификатору. | `forms:project_form:read` | JSON-объект, обязательные поля `projectFormId` | `200` — JSON-объект |
| `POST /public/v1/projects/forms/get-summary`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormGetSummaryV1) | Возвращает сводные данные указанных форм проекта. | `forms:project_form:read` | JSON-объект, обязательные поля `projectFormIds`, `projectIds` | `200` — массив записей |
| `POST /public/v1/projects/forms/find-form-source`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormFindFormSourceV1) | Ищет формы проекта, которые могут быть источниками данных для указанного типа поля, по заданным критериям. | `forms:project_form:list` | JSON-объект, обязательные поля `formFieldTypeId`, `projectId` | `200` — JSON-объект |
| `POST /public/v1/projects/forms/get-values-for-template-item`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormGetValuesForTemplateItemV1) | Возвращает значения элемента шаблона формы проекта. | `forms:project_form:read` | JSON-объект, обязательные поля `projectFormId` | `200` — JSON-объект |
| `POST /public/v1/projects/forms/get-download-url-by-template-item`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormGetDownloadUrlByTemplateItemV1) | Выдаёт временную ссылку для скачивания элемента шаблона формы проекта. | `forms:project_form:read` | JSON-объект, обязательные поля `projectFormId`, `templateItemId` | `200` — JSON-объект |
| `POST /public/v1/projects/forms/create-batch`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormCreateBatchV1) | Создаёт несколько форм проекта одним запросом. | `forms:project_form:create` | JSON-объект, обязательные поля `forms`, `projectFormTypeId` | `200` — массив записей |
| `PATCH /public/v1/projects/forms/update`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormUpdateV1) | Обновляет существующую форму проекта. | `forms:project_form:update` | JSON-объект, обязательные поля `projectFormFields`, `projectFormId` | `200` — без тела ответа |
| `PATCH /public/v1/projects/forms/complete`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormCompleteV1) | Переводит существующую форму проекта в завершённое состояние. | `forms:project_form:update` | JSON-объект, обязательные поля `projectFormId` | `200` — без тела ответа |
| <span id="ref-v1-projectformfieldtype"></span>`POST /public/v1/projects/forms/fields/types`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectFormFieldType/ProjectFormFieldTypeListV1) | Ищет типы полей форм проекта и связанные источники отображения по фильтру. | `forms:project_form_field_type:list` | JSON-объект, обязательные поля `projectFormTypeId` | `200` — JSON-объект |
| <span id="ref-v1-projectformtype"></span>`POST /public/v1/projects/forms/types`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectFormType/ProjectFormTypeListV1) | Ищет типы форм проекта по фильтру. | `forms:project_form_type:list` | JSON-объект, обязательные поля `projectId` | `200` — массив записей |
| <span id="ref-v1-formfieldtype"></span>`POST /public/v1/forms/fields/types`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/FormFieldType/FormFieldTypeListV1) | Ищет типы полей форм по фильтру. | `forms:form_field_type:list` | JSON-объект с параметрами запроса | `200` — массив записей |
| <span id="ref-v1-formtype"></span>`POST /public/v1/forms/types`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/FormType/FormTypeListV1) | Ищет типы форм по фильтру. | `forms:form_type:list` | JSON-объект с параметрами запроса | `200` — массив записей |
| <span id="ref-v1-formtypegroup"></span>`POST /public/v1/forms/types/groups`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/FormTypeGroup/FormTypeGroupListV1) | Ищет группы типов форм по фильтру. | `forms:form_type_group:list` | JSON-объект с параметрами запроса | `200` — массив записей |
| Метод и путь | Назначение | Scope | Контракт |
| --- | --- | --- | --- |
| <span id="ref-v1-projectform"></span>`POST /public/v1/projects/forms`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormListV1) | Ищет формы проекта по фильтру и сортировке с пагинацией. | `forms:project_form:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `find.formTypeId`, `find.projectId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| `POST /public/v1/projects/forms/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormListCountV1) | Подсчитывает формы проекта по фильтру. | `forms:project_form:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `formTypeId`, `projectId`<br><br>**Что вернёт API**<br>`200` — число</details> |
| `POST /public/v1/projects/forms/get`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormGetV1) | Возвращает форму проекта по идентификатору. | `forms:project_form:read` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectFormId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| `POST /public/v1/projects/forms/get-summary`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormGetSummaryV1) | Возвращает сводные данные указанных форм проекта. | `forms:project_form:read` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectFormIds`, `projectIds`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `POST /public/v1/projects/forms/find-form-source`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormFindFormSourceV1) | Ищет формы проекта, которые могут быть источниками данных для указанного типа поля, по заданным критериям. | `forms:project_form:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `formFieldTypeId`, `projectId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| `POST /public/v1/projects/forms/get-values-for-template-item`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormGetValuesForTemplateItemV1) | Возвращает значения элемента шаблона формы проекта. | `forms:project_form:read` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectFormId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| `POST /public/v1/projects/forms/get-download-url-by-template-item`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormGetDownloadUrlByTemplateItemV1) | Выдаёт временную ссылку для скачивания элемента шаблона формы проекта. | `forms:project_form:read` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectFormId`, `templateItemId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| `POST /public/v1/projects/forms/create-batch`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormCreateBatchV1) | Создаёт несколько форм проекта одним запросом. | `forms:project_form:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `forms`, `projectFormTypeId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `PATCH /public/v1/projects/forms/update`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormUpdateV1) | Обновляет существующую форму проекта. | `forms:project_form:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectFormFields`, `projectFormId`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| `PATCH /public/v1/projects/forms/complete`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectForm/ProjectFormCompleteV1) | Переводит существующую форму проекта в завершённое состояние. | `forms:project_form:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectFormId`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| <span id="ref-v1-projectformfieldtype"></span>`POST /public/v1/projects/forms/fields/types`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectFormFieldType/ProjectFormFieldTypeListV1) | Ищет типы полей форм проекта и связанные источники отображения по фильтру. | `forms:project_form_field_type:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectFormTypeId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| <span id="ref-v1-projectformtype"></span>`POST /public/v1/projects/forms/types`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectFormType/ProjectFormTypeListV1) | Ищет типы форм проекта по фильтру. | `forms:project_form_type:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| <span id="ref-v1-formfieldtype"></span>`POST /public/v1/forms/fields/types`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/FormFieldType/FormFieldTypeListV1) | Ищет типы полей форм по фильтру. | `forms:form_field_type:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект с параметрами запроса<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| <span id="ref-v1-formtype"></span>`POST /public/v1/forms/types`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/FormType/FormTypeListV1) | Ищет типы форм по фильтру. | `forms:form_type:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект с параметрами запроса<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| <span id="ref-v1-formtypegroup"></span>`POST /public/v1/forms/types/groups`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/FormTypeGroup/FormTypeGroupListV1) | Ищет группы типов форм по фильтру. | `forms:form_type_group:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект с параметрами запроса<br><br>**Что вернёт API**<br>`200` — массив записей</details> |

#### 3.7. Атрибуты
###### 3.7. Атрибуты {#reference-attributes}

| Метод и путь | Назначение | Scope | Что передать | Что вернёт API |
| --- | --- | --- | --- | --- |
| <span id="ref-v1-attribute"></span>`POST /public/v1/attributes`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Attribute/AttributeListV1) | Возвращает атрибуты по заданному фильтру. | `docs:attribute:list` | JSON-объект, обязательные поля `projectId`, `type` | `200` — массив записей |
| <span id="ref-v1-attributetype"></span>`POST /public/v1/attributes/types`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AttributeType/AttributeTypeListV1) | Ищет типы атрибутов по фильтру. | `docs:attribute:list` | JSON-объект, обязательные поля `projectId` | `200` — массив записей |
| `PATCH /public/v1/attributes/types`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AttributeType/AttributeTypeUpdateV1) | Обновляет существующие типы атрибутов. | `docs:attribute:update` | JSON-объект, обязательные поля `data`, `projectId` | `200` — без тела ответа |
| `POST /public/v1/attributes/types/create`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AttributeType/AttributeTypeCreateV1) | Создаёт новый тип атрибута. | `docs:attribute:create` | JSON-объект, обязательные поля `isRequired`, `name`, `order`, `projectId`, `type` | `200` — идентификатор (UUID) |
| <span id="ref-v1-attributetypelistitems"></span>`POST /public/v1/attributes/types/list/items/create`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AttributeTypeListItems/AttributeTypeListItemsCreateV1) | Добавляет варианты значений в атрибут типа «список». | `docs:attribute:create` | JSON-объект, обязательные поля `attributeTypeId`, `items` | `200` — без тела ответа |
| `PATCH /public/v1/attributes/types/list/items`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AttributeTypeListItems/AttributeTypeListItemsUpdateV1) | Изменяет варианты значений атрибута типа «список». | `docs:attribute:update` | JSON-объект, обязательные поля `attributeTypeId`, `items` | `200` — без тела ответа |
| <span id="ref-v1-attributevalue"></span>`POST /public/v1/attributes/values/issues`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AttributeValue/AttributeValueListIssuesV1) | Возвращает значения атрибутов замечаний по фильтру. | `docs:attribute:list` | JSON-объект, обязательные поля `issueIds`, `projectId` | `200` — массив записей |
| `POST /public/v1/attributes/values/items`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AttributeValue/AttributeValueListItemsV1) | Возвращает значения атрибутов элементов по фильтру. | `docs:attribute:list` | JSON-объект, обязательные поля `itemIds`, `projectId` | `200` — массив записей |
| `POST /public/v1/attributes/values/folders`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AttributeValue/AttributeValueListFoldersV1) | Возвращает значения атрибутов папок по фильтру. | `docs:attribute:list` | JSON-объект, обязательные поля `folderIds`, `projectId` | `200` — массив записей |
| `POST /public/v1/attributes/values/set`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AttributeValue/AttributeValueSetV1) | Устанавливает значения атрибутов для указанной сущности. | `docs:attribute:update` | JSON-объект, обязательные поля `type`, `values` | `200` — без тела ответа<br>`204` — без тела ответа |
| Метод и путь | Назначение | Scope | Контракт |
| --- | --- | --- | --- |
| <span id="ref-v1-attribute"></span>`POST /public/v1/attributes`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Attribute/AttributeListV1) | Возвращает атрибуты по заданному фильтру. | `docs:attribute:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectId`, `type`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| <span id="ref-v1-attributetype"></span>`POST /public/v1/attributes/types`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AttributeType/AttributeTypeListV1) | Ищет типы атрибутов по фильтру. | `docs:attribute:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `PATCH /public/v1/attributes/types`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AttributeType/AttributeTypeUpdateV1) | Обновляет существующие типы атрибутов. | `docs:attribute:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `data`, `projectId`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| `POST /public/v1/attributes/types/create`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AttributeType/AttributeTypeCreateV1) | Создаёт новый тип атрибута. | `docs:attribute:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `isRequired`, `name`, `order`, `projectId`, `type`<br><br>**Что вернёт API**<br>`200` — идентификатор (UUID)</details> |
| <span id="ref-v1-attributetypelistitems"></span>`POST /public/v1/attributes/types/list/items/create`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AttributeTypeListItems/AttributeTypeListItemsCreateV1) | Добавляет варианты значений в атрибут типа «список». | `docs:attribute:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `attributeTypeId`, `items`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| `PATCH /public/v1/attributes/types/list/items`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AttributeTypeListItems/AttributeTypeListItemsUpdateV1) | Изменяет варианты значений атрибута типа «список». | `docs:attribute:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `attributeTypeId`, `items`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| <span id="ref-v1-attributevalue"></span>`POST /public/v1/attributes/values/issues`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AttributeValue/AttributeValueListIssuesV1) | Возвращает значения атрибутов замечаний по фильтру. | `docs:attribute:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `issueIds`, `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `POST /public/v1/attributes/values/items`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AttributeValue/AttributeValueListItemsV1) | Возвращает значения атрибутов элементов по фильтру. | `docs:attribute:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `itemIds`, `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `POST /public/v1/attributes/values/folders`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AttributeValue/AttributeValueListFoldersV1) | Возвращает значения атрибутов папок по фильтру. | `docs:attribute:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `folderIds`, `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `POST /public/v1/attributes/values/set`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/AttributeValue/AttributeValueSetV1) | Устанавливает значения атрибутов для указанной сущности. | `docs:attribute:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `type`, `values`<br><br>**Что вернёт API**<br>`200` — без тела ответа<br>`204` — без тела ответа</details> |

#### 3.8. Компания и проекты
###### 3.8. Компания и проекты {#reference-access}

| Метод и путь | Назначение | Scope | Что передать | Что вернёт API |
| --- | --- | --- | --- | --- |
| <span id="ref-v1-auth"></span>`POST /public/v1/auth/token`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Auth/AuthGetTokenV1) | Выдаёт токен интеграции с запрошенными разрешениями. | Bearer-токен не нужен | JSON-объект, обязательные поля `clientId`, `clientSecret`, `scopes` | `200` — объект с токеном `token` и сроком действия `expiresIn` в секундах |
| <span id="ref-v1-company"></span>`GET /public/v1/company/users`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Company/CompanyListUsersV1) | Возвращает пользователей компании. | `company:user:list` | Необязательно в строке запроса — `Take`, `Skip` | `200` — массив записей |
| `GET /public/v1/company/roles`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Company/CompanyListRolesV1) | Возвращает роли компании. | `company:role:list` | Необязательно в строке запроса — `Take`, `Skip` | `200` — массив записей |
| <span id="ref-v1-companyuser"></span>`GET /public/v1/company-users/by-telegram-id`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/CompanyUser/CompanyUserGetUserIdByTelegramIdV1) | Возвращает идентификатор пользователя компании по Telegram ID. | `company:user:read` | В строке запроса — `telegramId` | `200` — идентификатор (UUID) |
| `PUT /public/v1/company-users`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/CompanyUser/CompanyUserAddCompanyUsersV1) | Пакетно приглашает или добавляет пользователей в компанию. | `company:user:create` | JSON-объект, обязательные поля `users` | `200` — массив записей |
| `DELETE /public/v1/company-users`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/CompanyUser/CompanyUserDeleteCompanyUsersV1) | Пакетно удаляет пользователей из компании. | `company:user:delete` | JSON-объект, обязательные поля `userIds` | `200` — без тела ответа |
| <span id="ref-v1-companyusercustomrole"></span>`PUT /public/v1/company-user-custom-roles`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/CompanyUserCustomRole/CompanyUserCustomRoleSetCompanyUserCustomRolesV1) | Заменяет дополнительные роли пользователя на уровне компании переданным списком. | `company:role:update` | JSON-объект, обязательные поля `customRoleIds`, `userId` | `200` — без тела ответа |
| <span id="ref-v1-applicationuser"></span>`PUT /public/v1/application-users`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ApplicationUser/ApplicationUserUpsertApplicationUsersV1) | Пакетно назначает пользователям роли в нескольких приложениях. | `application:user:update` | JSON-объект, обязательные поля `applicationIds`, `role`, `userIds` | `200` — без тела ответа |
| `DELETE /public/v1/application-users`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ApplicationUser/ApplicationUserDeleteApplicationUsersV1) | Пакетно отзывает доступ пользователей к приложениям. | `application:user:delete` | JSON-объект, обязательные поля `applicationIds`, `userIds` | `200` — без тела ответа |
| <span id="ref-v1-project"></span>`GET /public/v1/projects/{projectId}`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Project/ProjectGetV1) | Возвращает сведения об указанном проекте. | `project:read` | В пути — `projectId` | `200` — JSON-объект |
| `GET /public/v1/projects`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Project/ProjectListV1) | Возвращает список проектов компании. | `project:list` | Необязательно в строке запроса — `Take`, `Skip` | `200` — массив записей |
| `PATCH /public/v1/projects`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Project/ProjectUpdateV1) | Изменяет основные сведения существующего проекта. | `project:update` | JSON-объект, обязательные поля `id`, `name`, `timeZoneOffset` | `200` — без тела ответа |
| `GET /public/v1/projects/{projectId}/users`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Project/ProjectListUsersV1) | Возвращает пользователей проекта. | `project:user:list` | В пути — `projectId`<br>Необязательно в строке запроса — `Take`, `Skip` | `200` — массив записей |
| `GET /public/v1/projects/{projectId}/users/{userId}/permissions`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Project/ProjectGetUserPermissionsV1) | Возвращает права пользователя в проекте; при отсутствии прав схема предусматривает ответ 404. | `project:user:read` | В пути — `projectId`, `userId` | `200` — JSON-объект |
| `GET /public/v1/projects/{projectId}/roles`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Project/ProjectListRolesV1) | Возвращает роли проекта. | `project:role:list` | В пути — `projectId`<br>Необязательно в строке запроса — `Take`, `Skip` | `200` — массив записей |
| <span id="ref-v1-docsproject"></span>`GET /public/v1/docs/projects/{projectId}`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocsProject/DocsProjectGetInfoV1) | Возвращает сведения о проекте в SIGNAL DOCS. | `project:read` | В пути — `projectId` | `200` — JSON-объект |
| `GET /public/v1/docs/projects/storage-id`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocsProject/DocsProjectGetStorageIdV1) | Возвращает идентификатор хранилища, назначенного проекту. | `project:read` | В строке запроса — `projectId` | `200` — объект с идентификатором или `null` в `data` |
| <span id="ref-v1-projectuser"></span>`PUT /public/v1/project-users`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectUser/ProjectUserAddProjectsUsersV1) | Пакетно добавляет пользователей в несколько проектов. | `project:user:create` | JSON-объект, обязательные поля `projectIds`, `userIds` | `200` — без тела ответа |
| `DELETE /public/v1/project-users`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectUser/ProjectUserDeleteProjectsUsersV1) | Пакетно удаляет пользователей из нескольких проектов. | `project:user:delete` | JSON-объект, обязательные поля `projectIds`, `userIds` | `200` — без тела ответа |
| <span id="ref-v1-projectusercustomrole"></span>`PUT /public/v1/project-user-custom-roles`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectUserCustomRole/ProjectUserCustomRoleSetProjectUserCustomRolesV1) | Заменяет дополнительные роли пользователя в проекте переданным списком. | `project:role:update` | JSON-объект, обязательные поля `customRoleIds`, `projectId`, `userId` | `200` — без тела ответа |
| <span id="ref-v1-userlog"></span>`POST /public/v1/user-logs`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/UserLog/UserLogListV1) | Возвращает записи журнала действий пользователей по фильтру. | `logs:user:list` | JSON-объект с параметрами запроса | `200` — массив записей |
| Метод и путь | Назначение | Scope | Контракт |
| --- | --- | --- | --- |
| <span id="ref-v1-auth"></span>`POST /public/v1/auth/token`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Auth/AuthGetTokenV1) | Выдаёт токен интеграции с запрошенными разрешениями. | Bearer-токен не нужен | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `clientId`, `clientSecret`, `scopes`<br><br>**Что вернёт API**<br>`200` — объект с токеном `token` и сроком действия `expiresIn` в секундах</details> |
| <span id="ref-v1-company"></span>`GET /public/v1/company/users`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Company/CompanyListUsersV1) | Возвращает пользователей компании. | `company:user:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `GET /public/v1/company/roles`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Company/CompanyListRolesV1) | Возвращает роли компании. | `company:role:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| <span id="ref-v1-companyuser"></span>`GET /public/v1/company-users/by-telegram-id`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/CompanyUser/CompanyUserGetUserIdByTelegramIdV1) | Возвращает идентификатор пользователя компании по Telegram ID. | `company:user:read` | <details><summary>Контракт</summary><br>**Что передать**<br>В строке запроса — `telegramId`<br><br>**Что вернёт API**<br>`200` — идентификатор (UUID)</details> |
| `PUT /public/v1/company-users`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/CompanyUser/CompanyUserAddCompanyUsersV1) | Пакетно приглашает или добавляет пользователей в компанию. | `company:user:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `users`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `DELETE /public/v1/company-users`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/CompanyUser/CompanyUserDeleteCompanyUsersV1) | Пакетно удаляет пользователей из компании. | `company:user:delete` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `userIds`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| <span id="ref-v1-companyusercustomrole"></span>`PUT /public/v1/company-user-custom-roles`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/CompanyUserCustomRole/CompanyUserCustomRoleSetCompanyUserCustomRolesV1) | Заменяет дополнительные роли пользователя на уровне компании переданным списком. | `company:role:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `customRoleIds`, `userId`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| <span id="ref-v1-applicationuser"></span>`PUT /public/v1/application-users`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ApplicationUser/ApplicationUserUpsertApplicationUsersV1) | Пакетно назначает пользователям роли в нескольких приложениях. | `application:user:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `applicationIds`, `role`, `userIds`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| `DELETE /public/v1/application-users`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ApplicationUser/ApplicationUserDeleteApplicationUsersV1) | Пакетно отзывает доступ пользователей к приложениям. | `application:user:delete` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `applicationIds`, `userIds`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| <span id="ref-v1-project"></span>`GET /public/v1/projects/{projectId}`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Project/ProjectGetV1) | Возвращает сведения об указанном проекте. | `project:read` | <details><summary>Контракт</summary><br>**Что передать**<br>В пути — `projectId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| `GET /public/v1/projects`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Project/ProjectListV1) | Возвращает список проектов компании. | `project:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `PATCH /public/v1/projects`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Project/ProjectUpdateV1) | Изменяет основные сведения существующего проекта. | `project:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `id`, `name`, `timeZoneOffset`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| `GET /public/v1/projects/{projectId}/users`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Project/ProjectListUsersV1) | Возвращает пользователей проекта. | `project:user:list` | <details><summary>Контракт</summary><br>**Что передать**<br>В пути — `projectId`<br>Необязательно в строке запроса — `Take`, `Skip`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `GET /public/v1/projects/{projectId}/users/{userId}/permissions`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Project/ProjectGetUserPermissionsV1) | Возвращает права пользователя в проекте; при отсутствии прав схема предусматривает ответ 404. | `project:user:read` | <details><summary>Контракт</summary><br>**Что передать**<br>В пути — `projectId`, `userId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| `GET /public/v1/projects/{projectId}/roles`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Project/ProjectListRolesV1) | Возвращает роли проекта. | `project:role:list` | <details><summary>Контракт</summary><br>**Что передать**<br>В пути — `projectId`<br>Необязательно в строке запроса — `Take`, `Skip`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| <span id="ref-v1-docsproject"></span>`GET /public/v1/docs/projects/{projectId}`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocsProject/DocsProjectGetInfoV1) | Возвращает сведения о проекте в SIGNAL DOCS. | `project:read` | <details><summary>Контракт</summary><br>**Что передать**<br>В пути — `projectId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| `GET /public/v1/docs/projects/storage-id`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/DocsProject/DocsProjectGetStorageIdV1) | Возвращает идентификатор хранилища, назначенного проекту. | `project:read` | <details><summary>Контракт</summary><br>**Что передать**<br>В строке запроса — `projectId`<br><br>**Что вернёт API**<br>`200` — объект с идентификатором или `null` в `data`</details> |
| <span id="ref-v1-projectuser"></span>`PUT /public/v1/project-users`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectUser/ProjectUserAddProjectsUsersV1) | Пакетно добавляет пользователей в несколько проектов. | `project:user:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectIds`, `userIds`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| `DELETE /public/v1/project-users`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectUser/ProjectUserDeleteProjectsUsersV1) | Пакетно удаляет пользователей из нескольких проектов. | `project:user:delete` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectIds`, `userIds`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| <span id="ref-v1-projectusercustomrole"></span>`PUT /public/v1/project-user-custom-roles`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/ProjectUserCustomRole/ProjectUserCustomRoleSetProjectUserCustomRolesV1) | Заменяет дополнительные роли пользователя в проекте переданным списком. | `project:role:update` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `customRoleIds`, `projectId`, `userId`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| <span id="ref-v1-userlog"></span>`POST /public/v1/user-logs`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/UserLog/UserLogListV1) | Возвращает записи журнала действий пользователей по фильтру. | `logs:user:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект с параметрами запроса<br><br>**Что вернёт API**<br>`200` — массив записей</details> |

#### 3.9. Модели и подписи
###### 3.9. Модели и подписи {#reference-models}

| Метод и путь | Назначение | Scope | Что передать | Что вернёт API |
| --- | --- | --- | --- | --- |
| <span id="ref-v1-forge"></span>`POST /public/v1/forge/convert`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Forge/ForgeConvertV1) | Запускает преобразование модели через Forge для просмотра; поддерживаемые форматы перечислены в Swagger. | `docs:viewer:execute` | JSON-объект, обязательные поля `versionId` | `204` — без тела ответа |
| `POST /public/v1/forge/item-versions/viewer`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Forge/ForgeGetViewersDataV1) | Возвращает токен доступа и URN моделей для отображения версий файлов в Forge Viewer. | `docs:viewer:read` | JSON-объект, обязательные поля `itemVersionIds`, `projectId` | `200` — JSON-объект |
| <span id="ref-v1-tangl"></span>`POST /public/v1/tangl/convert`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Tangl/TanglConvertV1) | Запускает преобразование модели через Tangl для просмотра; схема указывает форматы .rvt и .ifc. | `docs:viewer:execute` | JSON-объект, обязательные поля `versionId` | `204` — без тела ответа |
| <span id="ref-v1-cadessignature"></span>`GET /public/v1/cades/signatures`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/CadesSignature/CadesSignatureListV1) | Возвращает CAdES-подписи версии файла. | `docs:signing:list` | В строке запроса — `versionId`<br>Необязательно — `searchMchdIds` | `200` — массив записей |
| `PUT /public/v1/cades/signatures`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/CadesSignature/CadesSignatureCreateV1) | Создаёт новую CAdES-подпись. | `docs:signing:create` | JSON-объект, обязательные поля `certificateId`, `signature`, `versionId` | `204` — без тела ответа |
| <span id="ref-v1-embeddedsignature"></span>`GET /public/v1/embedded/signatures`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/EmbeddedSignature/EmbeddedSignatureListV1) | Возвращает встроенные подписи элемента. | `docs:signing:list` | В строке запроса — `itemId` | `200` — массив записей |
| `PUT /public/v1/embedded/signatures`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/EmbeddedSignature/EmbeddedSignatureCreateV1) | Создаёт встроенную подпись. | `docs:signing:create` | JSON-объект, обязательные поля `certificateId`, `itemId`, `signature`, `versionId` | `204` — без тела ответа |
| <span id="ref-v1-mchd"></span>`GET /public/v1/mchd/company`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Mchd/MchdGetCompanyMchdDocumentsV1) | Возвращает UUID машиночитаемых доверенностей (МЧД) компании. | `docs:signing:list` | Необязательно в строке запроса — `Take`, `Skip` | `200` — объект с массивом идентификаторов в `data` |
| `GET /public/v1/mchd/cades/signatures/{cadesSignatureId}`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Mchd/MchdGetAttachedMchdDocumentsV1) | Возвращает идентификаторы МЧД, связанных с CAdES-подписью. | `docs:signing:list` | В пути — `cadesSignatureId` | `200` — массив записей |
| `GET /public/v1/mchd/{mchdId}/object/download`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Mchd/MchdDownloadV1) | Выдаёт билет для скачивания МЧД. | `docs:signing:read` | В пути — `mchdId` | `200` — JSON-объект |
| Метод и путь | Назначение | Scope | Контракт |
| --- | --- | --- | --- |
| <span id="ref-v1-forge"></span>`POST /public/v1/forge/convert`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Forge/ForgeConvertV1) | Запускает преобразование модели через Forge для просмотра; поддерживаемые форматы перечислены в Swagger. | `docs:viewer:execute` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `versionId`<br><br>**Что вернёт API**<br>`204` — без тела ответа</details> |
| `POST /public/v1/forge/item-versions/viewer`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Forge/ForgeGetViewersDataV1) | Возвращает токен доступа и URN моделей для отображения версий файлов в Forge Viewer. | `docs:viewer:read` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `itemVersionIds`, `projectId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| <span id="ref-v1-tangl"></span>`POST /public/v1/tangl/convert`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Tangl/TanglConvertV1) | Запускает преобразование модели через Tangl для просмотра; схема указывает форматы .rvt и .ifc. | `docs:viewer:execute` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `versionId`<br><br>**Что вернёт API**<br>`204` — без тела ответа</details> |
| <span id="ref-v1-cadessignature"></span>`GET /public/v1/cades/signatures`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/CadesSignature/CadesSignatureListV1) | Возвращает CAdES-подписи версии файла. | `docs:signing:list` | <details><summary>Контракт</summary><br>**Что передать**<br>В строке запроса — `versionId`<br>Необязательно — `searchMchdIds`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `PUT /public/v1/cades/signatures`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/CadesSignature/CadesSignatureCreateV1) | Создаёт новую CAdES-подпись. | `docs:signing:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `certificateId`, `signature`, `versionId`<br><br>**Что вернёт API**<br>`204` — без тела ответа</details> |
| <span id="ref-v1-embeddedsignature"></span>`GET /public/v1/embedded/signatures`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/EmbeddedSignature/EmbeddedSignatureListV1) | Возвращает встроенные подписи элемента. | `docs:signing:list` | <details><summary>Контракт</summary><br>**Что передать**<br>В строке запроса — `itemId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `PUT /public/v1/embedded/signatures`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/EmbeddedSignature/EmbeddedSignatureCreateV1) | Создаёт встроенную подпись. | `docs:signing:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `certificateId`, `itemId`, `signature`, `versionId`<br><br>**Что вернёт API**<br>`204` — без тела ответа</details> |
| <span id="ref-v1-mchd"></span>`GET /public/v1/mchd/company`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Mchd/MchdGetCompanyMchdDocumentsV1) | Возвращает UUID машиночитаемых доверенностей (МЧД) компании. | `docs:signing:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br><br>**Что вернёт API**<br>`200` — объект с массивом идентификаторов в `data`</details> |
| `GET /public/v1/mchd/cades/signatures/{cadesSignatureId}`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Mchd/MchdGetAttachedMchdDocumentsV1) | Возвращает идентификаторы МЧД, связанных с CAdES-подписью. | `docs:signing:list` | <details><summary>Контракт</summary><br>**Что передать**<br>В пути — `cadesSignatureId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `GET /public/v1/mchd/{mchdId}/object/download`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Mchd/MchdDownloadV1) | Выдаёт билет для скачивания МЧД. | `docs:signing:read` | <details><summary>Контракт</summary><br>**Что передать**<br>В пути — `mchdId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |

#### 3.10. Другие модули
###### 3.10. Другие модули {#reference-modules}

| Метод и путь | Назначение | Scope | Что передать | Что вернёт API |
| --- | --- | --- | --- | --- |
| <span id="ref-v1-board"></span>`POST /public/v1/boards`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Board/BoardListV1) | Возвращает дашборды проекта по фильтру; удалённые дашборды исключены. | `dash:board:list` | Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `projectId` | `200` — массив записей |
| <span id="ref-v1-card"></span>`POST /public/v1/boards/cards`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Card/CardListV1) | Возвращает карточки дашборда с возможностью отбора по группам; удалённые карточки и карточки удалённых групп или дашбордов исключены. | `dash:card:list` | Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `boardId` | `200` — массив записей |
| `GET /public/v1/boards/cards/{cardId}`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Card/CardGetV1) | Возвращает карточку с содержимым по её идентификатору. | `dash:card:read` | В пути — `cardId` | `200` — JSON-объект |
| <span id="ref-v1-cardpubliclink"></span>`PATCH /public/v1/card-public-links/regenerate`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/CardPublicLink/CardPublicLinkRegenerateCardPubLinkV1) | Перегенерирует публичную ссылку на карточку дашборда. | `dash:card_public_link:update` | В строке запроса — `pubLink` | `200` — JSON-объект |
| <span id="ref-v1-group"></span>`POST /public/v1/boards/groups`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Group/GroupListV1) | Возвращает группы карточек дашборда; удалённые группы и группы удалённого дашборда исключены. | `dash:group:list` | Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `boardId` | `200` — массив записей |
| <span id="ref-v1-inspectionfolder"></span>`POST /public/v1/inspection/folders`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/InspectionFolder/InspectionFolderListV1) | Возвращает папки фотомониторинга проекта по фильтру с пагинацией. | `inspection:folder:list` | Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `projectId` | `200` — массив записей |
| `POST /public/v1/inspection/folders/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/InspectionFolder/InspectionFolderListCountV1) | Подсчитывает папки фотомониторинга по фильтру. | `inspection:folder:list` | JSON-объект, обязательные поля `projectId` | `200` — число |
| <span id="ref-v1-plan"></span>`POST /public/v1/inspection/plans`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Plan/PlanListV1) | Возвращает планы фотомониторинга проекта по фильтру с пагинацией. | `inspection:plan:list` | Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `projectId` | `200` — массив записей |
| `POST /public/v1/inspection/plans/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Plan/PlanListCountV1) | Подсчитывает планы фотомониторинга по фильтру. | `inspection:plan:list` | JSON-объект, обязательные поля `projectId` | `200` — число |
| <span id="ref-v1-point"></span>`POST /public/v1/inspection/points`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Point/PointListV1) | Возвращает точки фотомониторинга проекта по фильтру с пагинацией. | `inspection:point:list` | Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `projectId` | `200` — массив записей |
| `POST /public/v1/inspection/points/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Point/PointListCountV1) | Подсчитывает точки фотомониторинга по фильтру. | `inspection:point:list` | JSON-объект, обязательные поля `projectId` | `200` — число |
| `GET /public/v1/inspection/points/{pointId}`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Point/PointGetV1) | Возвращает точку фотомониторинга по идентификатору. | `inspection:point:read` | В пути — `pointId` | `200` — JSON-объект |
| <span id="ref-v1-booking"></span>`POST /public/v1/bookings`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Booking/BookingListV1) | Возвращает бронирования компании интеграции, упорядоченные по времени изменения и идентификатору. | `settings:booking:list` | JSON-объект, обязательные поля `paging.take` | `200` — массив записей |
| `DELETE /public/v1/bookings`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Booking/BookingDeleteBatchV1) | Удаляет указанные бронирования компании интеграции. | `settings:booking:delete` | JSON-объект, обязательные поля `bookingIds` | `200` — без тела ответа |
| <span id="ref-v1-slot"></span>`POST /public/v1/slots`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Slot/SlotListV1) | Возвращает слоты компании интеграции, упорядоченные по началу и идентификатору. | `settings:slot:list` | JSON-объект, обязательные поля `paging.take` | `200` — массив записей |
| `DELETE /public/v1/slots`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Slot/SlotDeleteBatchV1) | Удаляет указанные слоты компании интеграции. | `settings:slot:delete` | JSON-объект, обязательные поля `slotIds` | `200` — без тела ответа |
| `POST /public/v1/slots/create-batch`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Slot/SlotCreateBatchV1) | Создаёт несколько слотов компании интеграции. | `settings:slot:create` | JSON-объект, обязательные поля `slots` | `200` — массив записей |
| Метод и путь | Назначение | Scope | Контракт |
| --- | --- | --- | --- |
| <span id="ref-v1-board"></span>`POST /public/v1/boards`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Board/BoardListV1) | Возвращает дашборды проекта по фильтру; удалённые дашборды исключены. | `dash:board:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| <span id="ref-v1-card"></span>`POST /public/v1/boards/cards`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Card/CardListV1) | Возвращает карточки дашборда с возможностью отбора по группам; удалённые карточки и карточки удалённых групп или дашбордов исключены. | `dash:card:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `boardId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `GET /public/v1/boards/cards/{cardId}`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Card/CardGetV1) | Возвращает карточку с содержимым по её идентификатору. | `dash:card:read` | <details><summary>Контракт</summary><br>**Что передать**<br>В пути — `cardId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| <span id="ref-v1-cardpubliclink"></span>`PATCH /public/v1/card-public-links/regenerate`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/CardPublicLink/CardPublicLinkRegenerateCardPubLinkV1) | Перегенерирует публичную ссылку на карточку дашборда. | `dash:card_public_link:update` | <details><summary>Контракт</summary><br>**Что передать**<br>В строке запроса — `pubLink`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| <span id="ref-v1-group"></span>`POST /public/v1/boards/groups`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Group/GroupListV1) | Возвращает группы карточек дашборда; удалённые группы и группы удалённого дашборда исключены. | `dash:group:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `boardId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| <span id="ref-v1-inspectionfolder"></span>`POST /public/v1/inspection/folders`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/InspectionFolder/InspectionFolderListV1) | Возвращает папки фотомониторинга проекта по фильтру с пагинацией. | `inspection:folder:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `POST /public/v1/inspection/folders/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/InspectionFolder/InspectionFolderListCountV1) | Подсчитывает папки фотомониторинга по фильтру. | `inspection:folder:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — число</details> |
| <span id="ref-v1-plan"></span>`POST /public/v1/inspection/plans`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Plan/PlanListV1) | Возвращает планы фотомониторинга проекта по фильтру с пагинацией. | `inspection:plan:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `POST /public/v1/inspection/plans/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Plan/PlanListCountV1) | Подсчитывает планы фотомониторинга по фильтру. | `inspection:plan:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — число</details> |
| <span id="ref-v1-point"></span>`POST /public/v1/inspection/points`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Point/PointListV1) | Возвращает точки фотомониторинга проекта по фильтру с пагинацией. | `inspection:point:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `POST /public/v1/inspection/points/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Point/PointListCountV1) | Подсчитывает точки фотомониторинга по фильтру. | `inspection:point:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — число</details> |
| `GET /public/v1/inspection/points/{pointId}`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Point/PointGetV1) | Возвращает точку фотомониторинга по идентификатору. | `inspection:point:read` | <details><summary>Контракт</summary><br>**Что передать**<br>В пути — `pointId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| <span id="ref-v1-booking"></span>`POST /public/v1/bookings`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Booking/BookingListV1) | Возвращает бронирования компании интеграции, упорядоченные по времени изменения и идентификатору. | `settings:booking:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `paging.take`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `DELETE /public/v1/bookings`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Booking/BookingDeleteBatchV1) | Удаляет указанные бронирования компании интеграции. | `settings:booking:delete` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `bookingIds`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| <span id="ref-v1-slot"></span>`POST /public/v1/slots`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Slot/SlotListV1) | Возвращает слоты компании интеграции, упорядоченные по началу и идентификатору. | `settings:slot:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `paging.take`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `DELETE /public/v1/slots`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Slot/SlotDeleteBatchV1) | Удаляет указанные слоты компании интеграции. | `settings:slot:delete` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `slotIds`<br><br>**Что вернёт API**<br>`200` — без тела ответа</details> |
| `POST /public/v1/slots/create-batch`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v1#/Slot/SlotCreateBatchV1) | Создаёт несколько слотов компании интеграции. | `settings:slot:create` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `slots`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |

#### 3.11. Методы v2
###### 3.11. Методы v2 {#reference-v2}

| Метод и путь | Назначение | Scope | Что передать | Что вернёт API |
| --- | --- | --- | --- | --- |
| `GET /public/v2/dummy/{someId}`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v2#/Dummy/DummyGetV2) | Возвращает переданный идентификатор и версию API. | Достаточно токена интеграции | В пути — `someId` | `200` — JSON-объект |
| `POST /public/v2/issues/events`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v2#/IssueEvents/IssueEventsListV2) | Возвращает события замечаний по фильтру с пагинацией. | `docs:issue:list` | Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `projectId` | `200` — массив записей |
| `POST /public/v2/issues/events/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v2#/IssueEvents/IssueEventsListCountV2) | Подсчитывает события замечаний по фильтру. | `docs:issue:list` | JSON-объект, обязательные поля `projectId` | `200` — объект с числом в `data` |
| Метод и путь | Назначение | Scope | Контракт |
| --- | --- | --- | --- |
| `GET /public/v2/dummy/{someId}`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v2#/Dummy/DummyGetV2) | Возвращает переданный идентификатор и версию API. | Достаточно токена интеграции | <details><summary>Контракт</summary><br>**Что передать**<br>В пути — `someId`<br><br>**Что вернёт API**<br>`200` — JSON-объект</details> |
| `POST /public/v2/issues/events`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v2#/IssueEvents/IssueEventsListV2) | Возвращает события замечаний по фильтру с пагинацией. | `docs:issue:list` | <details><summary>Контракт</summary><br>**Что передать**<br>Необязательно в строке запроса — `Take`, `Skip`<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — массив записей</details> |
| `POST /public/v2/issues/events/count`<br>[Swagger](https://api.sgnl.pro/openapi/swagger/index.html?urls.primaryName=v2#/IssueEvents/IssueEventsListCountV2) | Подсчитывает события замечаний по фильтру. | `docs:issue:list` | <details><summary>Контракт</summary><br>**Что передать**<br>JSON-объект, обязательные поля `projectId`<br><br>**Что вернёт API**<br>`200` — объект с числом в `data`</details> |

#### 3.12. Коды ответов
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

<sub>**[<   SIGNAL. Что нового](/ru/general/updates)     **|**     [HUB. Введение   >](/ru/hub/intro)**</sub>