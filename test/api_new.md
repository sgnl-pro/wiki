---
title: Api New
description: 
published: true
date: 2026-11-17T13:18:15.356Z
tags: 
editor: markdown
dateCreated: 2026-11-17T13:04:57.412Z
---

<sub>**[<   SIGNAL. Что нового](/ru/general/updates)     **|**     [HUB. Введение   >](/ru/hub/intro)**</sub>

<summary style="font-size: 16px; color: #0D47A1; background: #E3F2FD; border-radius: 7px; border: 1px solid #64B5F6; display: flex; gap: 10px; padding: 5px 16px; display: block; margin-top: 10px;">
<span style="flex-grow: 1;"> <a href="/general/api/updates" onclick="event.stopPropagation();" style="color: inherit; text-decoration: none;">🔄 Что нового (история изменений этого функционала)</a></span>
</summary>

> Публичный API SIGNAL позволяет подключать внешние системы к данным компании: работать с файлами, замечаниями, согласованиями и другими объектами, доступными интеграции.
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
    <h4 class="toc-card-title"><a href="#reference">3. Справочник функций</a></h4>
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

Базовый адрес: **https://api.sgnl.pro**. Версия указывается в пути запроса: `/public/v1/...` или `/public/v2/...`.

- [Swagger — методы, модели и выполнение запросов](https://api.sgnl.pro/openapi/swagger/index.html).
- [ReDoc — документация v1](https://api.sgnl.pro/openapi/redoc-v1/index.html).
- [Машинная схема OpenAPI v1](https://api.sgnl.pro/openapi/v1/schema.yml).
- [Машинная схема OpenAPI v2](https://api.sgnl.pro/openapi/v2/schema.yml).

Сначала создайте интеграцию и выберите разрешения, затем получите токен. После этого используйте готовый [пример](#examples) или найдите нужный метод в [справочнике функций](#reference).

#### 1.2. Подключение и авторизация в Swagger
###### 1.2. Подключение и авторизация в Swagger {#swagger}

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

6. При успешном выполнении запроса — код `200` — скопируйте значение поля **token** из ответа. Срок действия токена возвращается в поле **expiresIn** (секунды). После истечения срока снова выполните запрос:
![auth_swagger_6.png](/api/auth_swagger_6.png)

7. Нажмите **Authorize**, вставьте скопированный токен и ещё раз нажмите **Authorize**:
![auth_swagger_7.png](/api/auth_swagger_7.png)
  
Авторизация выполнена. Используйте методы, соответствующие выбранным для интеграции scopes.

> Secret key и токен дают доступ к данным интеграции. Храните их на стороне сервера или в защищённых переменных окружения. Не добавляйте их в клиентский JavaScript, публичный репозиторий и тексты обращений.
{.is-warning}

#### 1.3. Запросы, ответы и ограничения
###### 1.3. Запросы, ответы и ограничения {#api-rules}

Для получения токена передайте `clientId`, `clientSecret` и массив `scopes` в `POST /public/v1/auth/token`. В остальных запросах примеров используется заголовок:

```http
Authorization: Bearer <token>
```

Если запрос содержит JSON, добавьте `Content-Type: application/json`. Поля и обязательность параметров зависят от метода. Запрошенные scopes должны быть разрешены у интеграции; нужные значения указаны в справочнике.

- **Постраничная выдача.** В методах с параметрами `Take` и `Skip` запрашивайте очередную страницу, увеличивая `Skip` на число полученных записей. Для примеров ниже максимум `Take` — 200. Одна страница не является полным реестром.
- **Ответы.** Метод может вернуть массив, объект, значение в поле `data` или пустое тело. Не применяйте один формат разбора ко всем операциям.
- **Подписанные ссылки.** Билет загрузки или скачивания содержит `signedUrl` и `ttlSec`. Используйте ссылку до истечения указанного срока. JWT предназначен для API SIGNAL; в запрос к хранилищу по подписанной ссылке его передавать не нужно.
- **Частота запросов.** При `429` выдержите паузу из заголовка `Retry-After`. В текущей схеме для компании задан запас до 50 запросов с пополнением 4 запроса в секунду, для клиента — до 10 запросов в секунду. Для неавторизованных запросов — запас до 10 с пополнением 2 запроса каждые 2 секунды.
- **Повторы.** После сетевого обрыва при создании или изменении объекта сначала проверьте результат. Автоматический повтор всей последовательности может создать дубликат.

Назначение операции определяется её описанием: `POST` используется и для поиска, и для создания. В примерах «Данные согласования» и «Реестр замечаний» запросы только читают данные.

## 2. Примеры
###### 2. Примеры {#examples}

### Подразделы {.tabset}

#### 2.1. Подготовка
###### 2.1. Подготовка {#example-setup}

Выберите Python или JavaScript. Для Python используйте Python 3.10+ и установите пакет:

```bash
python -m pip install requests
```

Примеры JavaScript предназначены для Node.js 22+ и сохраняются с расширением `.mjs`; дополнительные пакеты не нужны. Это серверные скрипты, а не код для вставки в браузер.

Сохраните общий модуль из [примера авторизации](#example-auth) и выбранный сценарий в одну папку. Каждый сценарий сам получает токен через общий модуль. Задайте переменные окружения в настройках запуска своего терминала, IDE или сервера:

| Переменная | Значение |
| --- | --- |
| `SIGNAL_CLIENT_ID` | clientId интеграции. |
| `SIGNAL_CLIENT_SECRET` | Secret key интеграции. |
| `SIGNAL_SCOPES` | Нужные scopes одной строкой через пробел; см. таблицу ниже. |
| `SIGNAL_PROJECT_ID` | UUID проекта для загрузки, согласований и замечаний. |
| `SIGNAL_FOLDER_ID` | UUID папки назначения для загрузки. Папка должна принадлежать указанному проекту. |
| `SIGNAL_FILE` | Путь к локальному файлу для загрузки. |
| `SIGNAL_MIME_TYPE` | MIME-тип файла для JavaScript, например application/pdf. По умолчанию application/octet-stream. |
| `SIGNAL_ITEM_ID` и `SIGNAL_VERSION_ID` | UUID элемента и версии файла для скачивания. |
| `SIGNAL_REVIEW_ID` | UUID согласования. |
| `SIGNAL_OUTPUT` | Необязательное имя выходного файла для скачивания или JSON согласования. |
| `SIGNAL_OUTPUT_PREFIX` | Необязательное имя без расширения для CSV и JSON замечаний; по умолчанию issues. |

| Сценарий | Значение SIGNAL_SCOPES |
| --- | --- |
| Загрузка нового файла | `docs:object:create docs:version:create docs:item:create` |
| Скачивание файла | `docs:item:read` |
| Данные согласования | `docs:review:list` |
| Реестр замечаний | `docs:issue:list` |

Для отдельной проверки авторизации используйте scopes выбранного сценария. Дополнительные запросы для поиска идентификаторов требуют своих scopes из [справочника](#reference).

Идентификаторы можно получить через API: проекты — `GET /public/v1/projects`, папки — `GET /public/v1/projects/{projectId}/folders/tree`, файлы папки — `GET /public/v1/items`, версии — `GET /public/v1/versions`, согласования — `POST /public/v1/reviews`. Для скачивания нужен именно `versionId`; не подменяйте его идентификатором версии элемента `itemVersionId`.

Выходные файлы создаются в рабочей папке запуска. Если файл с выбранным именем уже существует, он будет заменён. Примеры рассчитаны на последовательный запуск; при долгой передаче увеличьте тайм-ауты под размер файла и скорость соединения.

#### 2.2. Авторизация
###### 2.2. Авторизация {#example-auth}

**Задача:** получить JWT и использовать его в последующих запросах. **Результат:** токен хранится в памяти; на экран выводится только срок действия. Общий модуль получает новый токен перед истечением срока и ограниченно повторяет запросы при HTTP 429. Ошибки авторизации, остальные HTTP-ошибки и сетевые ошибки останавливают сценарий.

**Python — `signal_api.py`.** Сохраните модуль; для проверки выполните `python signal_api.py`.

```python
import os
import time
from pathlib import Path
import requests

BASE_URL = "https://api.sgnl.pro"

class SignalAPI:
    def __init__(self):
        scopes = os.environ["SIGNAL_SCOPES"].split()
        if not scopes:
            raise ValueError("Укажите хотя бы один scope")
        self.credentials = {
            "clientId": os.environ["SIGNAL_CLIENT_ID"],
            "clientSecret": os.environ["SIGNAL_CLIENT_SECRET"],
            "scopes": scopes,
        }
        self.token = None
        self.expires_at = 0

    def authorize(self):
        started = time.monotonic()
        response = requests.post(
            BASE_URL + "/public/v1/auth/token",
            json=self.credentials, timeout=60,
        )
        if not response.ok:
            raise RuntimeError(f"Авторизация: HTTP {response.status_code}")
        result = response.json()
        self.token = result["token"]
        self.expires_at = started + result["expiresIn"]
        return result["expiresIn"]

    def request(self, method, route, *, body=None, params=None):
        if self.token is None or time.monotonic() >= self.expires_at - 30:
            self.authorize()
        for attempt in range(4):
            response = requests.request(
                method, BASE_URL + route, json=body, params=params,
                headers={"Authorization": f"Bearer {self.token}"}, timeout=60,
            )
            if response.status_code == 429 and attempt < 3:
                delay = response.headers.get("Retry-After", "2")
                time.sleep(float(delay) if delay.isdigit() else 2)
                continue
            if not response.ok:
                raise RuntimeError(f"{method} {route}: HTTP {response.status_code}")
            return response.json() if response.content else None
        raise RuntimeError("Превышено число повторов")

def download_file(url, destination):
    target = Path(destination)
    temporary = target.with_name(target.name + ".part")
    try:
        # Подписанная ссылка уже разрешает скачивание. JWT сюда не передаём.
        with requests.get(url, stream=True, timeout=300) as response:
            if not response.ok:
                raise RuntimeError(f"Скачивание: HTTP {response.status_code}")
            with temporary.open("wb") as output:
                for chunk in response.iter_content(chunk_size=1024 * 1024):
                    output.write(chunk)
        temporary.replace(target)
    finally:
        temporary.unlink(missing_ok=True)

if __name__ == "__main__":
    api = SignalAPI()
    seconds = api.authorize()
    print(f"Авторизация выполнена. Срок действия токена: {seconds} с.")
```

**JavaScript — `signal_api.mjs`.** Сохраните модуль; для проверки выполните `node signal_api.mjs`.

```javascript
import { createWriteStream } from "node:fs";
import { rename, rm } from "node:fs/promises";
import { Readable } from "node:stream";
import { pipeline } from "node:stream/promises";
import { pathToFileURL } from "node:url";

const BASE_URL = "https://api.sgnl.pro";
export function env(name) {
  const value = process.env[name];
  if (!value) throw new Error("Не задана переменная " + name);
  return value;
}
export class SignalAPI {
  constructor() {
    this.credentials = {
      clientId: env("SIGNAL_CLIENT_ID"),
      clientSecret: env("SIGNAL_CLIENT_SECRET"),
      scopes: env("SIGNAL_SCOPES").trim().split(/\s+/),
    };
    this.token = null;
    this.expiresAt = 0;
  }
  async authorize() {
    const started = Date.now();
    const response = await fetch(BASE_URL + "/public/v1/auth/token", {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify(this.credentials),
      signal: AbortSignal.timeout(60000),
    });
    if (!response.ok) throw new Error("Авторизация: HTTP " + response.status);
    const result = await response.json();
    this.token = result.token;
    this.expiresAt = started + result.expiresIn * 1000;
    return result.expiresIn;
  }
  async request(method, route, { body, params } = {}) {
    if (!this.token || Date.now() >= this.expiresAt - 30000) {
      await this.authorize();
    }
    const url = new URL(BASE_URL + route);
    if (params) url.search = new URLSearchParams(params).toString();
    for (let attempt = 0; attempt < 4; attempt++) {
      const response = await fetch(url, {
        method,
        headers: {
          Authorization: "Bearer " + this.token,
          ...(body === undefined ? {} : { "Content-Type": "application/json" }),
        },
        body: body === undefined ? undefined : JSON.stringify(body),
        signal: AbortSignal.timeout(60000),
      });
      if (response.status === 429 && attempt < 3) {
        const value = response.headers.get("Retry-After") ?? "2";
        const seconds = /^\d+$/.test(value) ? Number(value) : 2;
        await response.arrayBuffer();
        await new Promise(resolve => setTimeout(resolve, seconds * 1000));
        continue;
      }
      if (!response.ok) throw new Error(method + " " + route + ": HTTP " + response.status);
      const text = await response.text();
      return text ? JSON.parse(text) : null;
    }
    throw new Error("Превышено число повторов");
  }
}
export async function downloadFile(url, destination) {
  const temporary = destination + ".part";
  try {
    // JWT не передаётся по подписанной ссылке.
    const response = await fetch(url, { signal: AbortSignal.timeout(300000) });
    if (!response.ok) throw new Error("Скачивание: HTTP " + response.status);
    await pipeline(Readable.fromWeb(response.body), createWriteStream(temporary));
    await rename(temporary, destination);
  } finally {
    await rm(temporary, { force: true });
  }
}
if (process.argv[1] && import.meta.url === pathToFileURL(process.argv[1]).href) {
  const seconds = await new SignalAPI().authorize();
  console.log("Авторизация выполнена. Срок действия токена: " + seconds + " с.");
}
```


#### 2.3. Загрузка файла
###### 2.3. Загрузка файла {#example-upload}

**Задача:** создать новый файл в папке DOCS. Укажите `SIGNAL_PROJECT_ID`, `SIGNAL_FOLDER_ID` и `SIGNAL_FILE`. Размер в текущей схеме — от 10 байт до 5 ГиБ.

Последовательность:

1. Получить билет через `PUT /public/v1/objects`.
2. Передать содержимое файла методом PUT по `signedUrl`.
3. Подтвердить загрузку через `POST /public/v1/objects/{objectId}/uploading/commit`.
4. Создать версию через `POST /public/v1/versions`.
5. Создать файл в папке через `PUT /public/v1/items/file`.

**Результат:** новый файл в папке, его `itemId` и `versionId` в выводе скрипта. Пример не обновляет существующий файл. Для прикрепления версии к существующему элементу используйте `PUT /public/v1/items/versions` из справочника. Если папка требует правило именования, передайте допустимое имя и нужный `namingPatternId` в запросе создания файла согласно настройкам папки.

> Запуск этого примера создаёт данные в DOCS. Выберите папку для проверки интеграции. Если последовательность остановилась после загрузки объекта или создания версии, не запускайте её целиком повторно без проверки уже выполненных шагов.
{.is-warning}

**Python — `upload.py`; запуск: `python upload.py`.

```python
import mimetypes
import os
from pathlib import Path
import requests
from signal_api import SignalAPI

api = SignalAPI()
source = Path(os.environ["SIGNAL_FILE"])
project_id = os.environ["SIGNAL_PROJECT_ID"]
folder_id = os.environ["SIGNAL_FOLDER_ID"]
size = source.stat().st_size
if not 10 <= size <= 5368709120:
    raise ValueError("Размер файла должен быть от 10 байт до 5 ГиБ")
mime_type = mimetypes.guess_type(source.name)[0] or "application/octet-stream"

ticket = api.request("PUT", "/public/v1/objects", body={
    "projectId": project_id, "mimeType": mime_type, "size": size,
})
with source.open("rb") as content:
    response = requests.put(ticket["signedUrl"], data=content,
                            headers={"Content-Type": mime_type}, timeout=300)
if not response.ok:
    raise RuntimeError(f"Загрузка в хранилище: HTTP {response.status_code}")
api.request("POST", f"/public/v1/objects/{ticket['objectId']}/uploading/commit")
version = api.request("POST", "/public/v1/versions", body={
    "objectId": ticket["objectId"], "projectId": project_id, "name": source.name,
})
item = api.request("PUT", "/public/v1/items/file", body={
    "folderId": folder_id, "versionId": version["data"], "name": source.name,
})
print("itemId:", item["data"])
print("versionId:", version["data"])
```

**JavaScript — `upload.mjs`; запуск: `node upload.mjs`.

```javascript
import { createReadStream } from "node:fs";
import { stat } from "node:fs/promises";
import { basename } from "node:path";
import { SignalAPI, env } from "./signal_api.mjs";

const api = new SignalAPI();
const source = env("SIGNAL_FILE");
const projectId = env("SIGNAL_PROJECT_ID");
const folderId = env("SIGNAL_FOLDER_ID");
const name = basename(source);
const { size } = await stat(source);
if (size < 10 || size > 5368709120) throw new Error("Размер файла: от 10 байт до 5 ГиБ");
const mimeType = process.env.SIGNAL_MIME_TYPE || "application/octet-stream";
const ticket = await api.request("PUT", "/public/v1/objects", {
  body: { projectId, mimeType, size },
});
const stream = createReadStream(source);
try {
  const response = await fetch(ticket.signedUrl, {
    method: "PUT", body: stream, duplex: "half",
    headers: { "Content-Type": mimeType, "Content-Length": String(size) },
    signal: AbortSignal.timeout(300000),
  });
  if (!response.ok) throw new Error("Загрузка в хранилище: HTTP " + response.status);
} finally {
  stream.destroy();
}
await api.request("POST", "/public/v1/objects/" + ticket.objectId + "/uploading/commit");
const version = await api.request("POST", "/public/v1/versions", {
  body: { objectId: ticket.objectId, projectId, name },
});
const item = await api.request("PUT", "/public/v1/items/file", {
  body: { folderId, versionId: version.data, name },
});
console.log("itemId:", item.data);
console.log("versionId:", version.data);
```


#### 2.4. Скачивание файла
###### 2.4. Скачивание файла {#example-download}

**Задача:** скачать выбранную версию файла DOCS. Укажите `SIGNAL_ITEM_ID` и `SIGNAL_VERSION_ID`. Для сохранения с нужным именем и расширением задайте `SIGNAL_OUTPUT`, например `document.pdf`.

Сначала запросите билет через `GET /public/v1/items/download`, затем скачайте содержимое по `signedUrl`. Ответ API с билетом не является содержимым файла.

**Результат:** локальный файл. Запись идёт во временный файл с окончанием .part; итоговое имя присваивается после успешного скачивания.

**Python — `download.py`; запуск: `python download.py`.

```python
import os
from signal_api import SignalAPI, download_file

api = SignalAPI()
ticket = api.request("GET", "/public/v1/items/download", params={
    "itemId": os.environ["SIGNAL_ITEM_ID"],
    "versionId": os.environ["SIGNAL_VERSION_ID"],
})
destination = os.environ.get("SIGNAL_OUTPUT", "download.bin")
download_file(ticket["signedUrl"], destination)
print("Файл сохранён:", destination)
```

**JavaScript — `download.mjs`; запуск: `node download.mjs`.

```javascript
import { SignalAPI, env, downloadFile } from "./signal_api.mjs";

const api = new SignalAPI();
const ticket = await api.request("GET", "/public/v1/items/download", {
  params: { itemId: env("SIGNAL_ITEM_ID"), versionId: env("SIGNAL_VERSION_ID") },
});
const destination = process.env.SIGNAL_OUTPUT || "download.bin";
await downloadFile(ticket.signedUrl, destination);
console.log("Файл сохранён:", destination);
```


#### 2.5. Данные согласования
###### 2.5. Данные согласования {#example-review}

**Задача:** получить данные для собственного листа согласования. Укажите `SIGNAL_PROJECT_ID` и `SIGNAL_REVIEW_ID`.

`POST /public/v1/reviews` возвращает согласование с последней версией `topVersion`, этапами, статусом и данными подписаний. Второй запрос, `POST /public/v1/reviews/versions/item-versions`, возвращает идентификаторы входящих версий элементов.

**Результат:** `review.json` с двумя полями: `review` и `itemVersionIdsByReviewVersion`. В `review.topVersion.stages` находятся этапы, в `review.topVersion.signings` — данные подписаний. Для деталей конкретной версии элемента используйте `GET /public/v1/items/item-version` из справочника.

Это исходные данные для собственной формы отчёта, а не штатный PDF/XLSX из интерфейса. В проверенных схемах OpenAPI v1/v2 отдельный метод скачивания штатного листа согласования не описан. Пример получает последнюю версию; для известного идентификатора другой версии предусмотрен `POST /public/v1/reviews/versions`.

**Python — `review.py`; запуск: `python review.py`.

```python
import json
import os
from pathlib import Path
from signal_api import SignalAPI

api = SignalAPI()
review_id = os.environ["SIGNAL_REVIEW_ID"]
reviews = api.request("POST", "/public/v1/reviews", body={
    "projectId": os.environ["SIGNAL_PROJECT_ID"], "ids": [review_id],
}, params={"Take": 1, "Skip": 0})
if len(reviews) != 1 or reviews[0]["id"].lower() != review_id.lower():
    raise RuntimeError("Указанное согласование не найдено")
review = reviews[0]
version_id = review["topVersion"]["id"]
item_versions = api.request("POST", "/public/v1/reviews/versions/item-versions", body={
    "reviewVersionIds": [version_id],
})
result = {"review": review, "itemVersionIdsByReviewVersion": item_versions}
destination = Path(os.environ.get("SIGNAL_OUTPUT", "review.json"))
destination.write_text(json.dumps(result, ensure_ascii=False, indent=2), encoding="utf-8")
print("Данные согласования сохранены:", destination)
```

**JavaScript — `review.mjs`; запуск: `node review.mjs`.

```javascript
import { writeFile } from "node:fs/promises";
import { SignalAPI, env } from "./signal_api.mjs";

const api = new SignalAPI();
const reviewId = env("SIGNAL_REVIEW_ID");
const reviews = await api.request("POST", "/public/v1/reviews", {
  body: { projectId: env("SIGNAL_PROJECT_ID"), ids: [reviewId] },
  params: { Take: 1, Skip: 0 },
});
if (reviews.length !== 1 || reviews[0].id.toLowerCase() !== reviewId.toLowerCase()) {
  throw new Error("Указанное согласование не найдено");
}
const review = reviews[0];
const itemVersions = await api.request("POST", "/public/v1/reviews/versions/item-versions", {
  body: { reviewVersionIds: [review.topVersion.id] },
});
const destination = process.env.SIGNAL_OUTPUT || "review.json";
await writeFile(destination, JSON.stringify({
  review, itemVersionIdsByReviewVersion: itemVersions,
}, null, 2), "utf8");
console.log("Данные согласования сохранены:", destination);
```


#### 2.6. Реестр замечаний
###### 2.6. Реестр замечаний {#example-issues}

**Задача:** собрать неудалённые замечания проекта. Укажите `SIGNAL_PROJECT_ID`. При необходимости дополните фильтр полями из модели `IssueFind`: например, типом замечания, статусами или ответственными.

Скрипт получает число записей через `POST /public/v1/issues/count`, читает страницы через `POST /public/v1/issues` с сортировкой по номеру, проверяет дубликаты и повторно сверяет количество.

**Результат:**

- `issues.csv` — таблица с идентификатором, номером, названием, статусом, описанием, местоположением, сроком устранения, датами создания и изменения и ответственным. Разделитель — точка с запятой; кодировка — UTF-8 с BOM. Составное поле ответственного сохраняется как JSON, статусы — в значениях API.
- `issues.json` — полные полученные записи для дальнейшей обработки, включая поля, не вошедшие в CSV. Дополнительные атрибуты, комментарии и вложения запрашиваются отдельными методами из справочника.

CSV формируется скриптом из данных API; это не выгрузка штатного шаблона реестра из интерфейса. При отсутствии замечаний CSV содержит заголовки, JSON — пустой массив.

Проверка количества и дубликатов обнаруживает часть изменений во время выгрузки, но не создаёт снимок данных на один момент. Чтобы получить согласованный реестр, запускайте сбор в период без изменений замечаний. При ошибке проверки новые файлы не записываются; ранее созданные файлы могут остаться в папке.

**Python — `issues.py`; запуск: `python issues.py`.

```python
import csv
import json
import os
from pathlib import Path
from signal_api import SignalAPI

api = SignalAPI()
filters = {
    "projectId": os.environ["SIGNAL_PROJECT_ID"], "deleted": False,
    "order": "Number", "isOrderAsc": True,
}
def count():
    return api.request("POST", "/public/v1/issues/count", body=filters)["data"]

expected = count()
issues = []
seen = set()
skip = 0
while True:
    page = api.request("POST", "/public/v1/issues", body=filters,
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

**JavaScript — `issues.mjs`; запуск: `node issues.mjs`.

```javascript
import { writeFile } from "node:fs/promises";
import { SignalAPI, env } from "./signal_api.mjs";

const api = new SignalAPI();
const filters = {
  projectId: env("SIGNAL_PROJECT_ID"), deleted: false,
  order: "Number", isOrderAsc: true,
};
async function count() {
  return (await api.request("POST", "/public/v1/issues/count", { body: filters })).data;
}
const expected = await count();
const issues = [];
const seen = new Set();
let skip = 0;
while (true) {
  const page = await api.request("POST", "/public/v1/issues", {
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
const actual = await count();
if (issues.length !== expected || actual !== expected) {
  throw new Error("Число замечаний изменилось или выгрузка неполная; повторите её");
}
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

## 3. Справочник функций
###### 3. Справочник функций {#reference}

В справочнике 153 операции по состоянию на 17 ноября 2026 года. Методы v1 сгруппированы по задачам. В отдельной вкладке собраны методы v2.

Пути указаны относительно `https://api.sgnl.pro`. Нажмите **Контракт** в строке метода, чтобы увидеть параметры, модель тела и формат успешного ответа. Звёздочка обозначает обязательный параметр. Ссылка **Схема** ведёт к полному описанию метода в Swagger.

### Разделы справочника {.tabset}
#### 3.1. Файлы и версии
###### 3.1. Файлы и версии {#reference-v1}

| Метод и путь | Назначение | Параметры и ответ |
| --- | --- | --- |
| <span id="ref-v1-item"></span>`PUT /public/v1/items/file`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Item/ItemCreateV1) | <small>Файлы и элементы</small><br>Создаёт элемент типа «файл» вместе с версией и возвращает идентификатор элемента. | <details><summary>Контракт</summary><br>**Scope:** `docs:item:create`<br>JSON обязателен: `FileItemCreate`; поля: `folderId`, `name`, `versionId`<br>**Ответ:** `200` → `GuidSimpleDto`</details> |
| `PUT /public/v1/items/link`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Item/ItemCreateV1) | <small>Файлы и элементы</small><br>Создаёт элемент типа «ссылка» и возвращает его идентификатор. | <details><summary>Контракт</summary><br>**Scope:** `docs:item:create`<br>JSON обязателен: `LinkItemCreate`; поля: `folderId`, `link`, `name`<br>**Ответ:** `200` → `GuidSimpleDto`</details> |
| `GET /public/v1/items`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Item/ItemListV1) | <small>Файлы и элементы</small><br>Возвращает непосредственные элементы папки без вложенных элементов. | <details><summary>Контракт</summary><br>**Scope:** `docs:item:list`<br>`folderId`* (query), `deleted` (query), `Take` (query), `Skip` (query)<br>**Ответ:** `200` → `массив ItemsListItem`</details> |
| `GET /public/v1/items/count`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Item/ItemListCountV1) | <small>Файлы и элементы</small><br>Подсчитывает непосредственные элементы папки без вложенных элементов. | <details><summary>Контракт</summary><br>**Scope:** `docs:item:list`<br>`folderId`* (query), `deleted` (query)<br>**Ответ:** `200` → `Int32SimpleDto`</details> |
| `POST /public/v1/items/search`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Item/ItemSearchV1) | <small>Файлы и элементы</small><br>Ищет элементы внутри папки, включая вложенные. | <details><summary>Контракт</summary><br>**Scope:** `docs:item:list`<br>`Take` (query), `Skip` (query)<br>JSON обязателен: `ItemSearch`; поля: `folderId`<br>**Ответ:** `200` → `массив ItemsListItem`</details> |
| `GET /public/v1/items/item-version`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Item/ItemGetItemVersionV1) | <small>Файлы и элементы</small><br>Возвращает версию элемента по её идентификатору. | <details><summary>Контракт</summary><br>**Scope:** `docs:item:read`<br>`id`* (query)<br>**Ответ:** `200` → `ItemVersion`</details> |
| `GET /public/v1/items/download`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Item/ItemDownloadV1) | <small>Файлы и элементы</small><br>Выдаёт билет для скачивания файла из S3. | <details><summary>Контракт</summary><br>**Scope:** `docs:item:read`<br>`itemId`* (query), `versionId`* (query), `fileName` (query), `urlTtlSecOverride` (query)<br>**Ответ:** `200` → `ItemDownloadTicket`</details> |
| `PUT /public/v1/items/versions`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Item/ItemAttachVersionV1) | <small>Файлы и элементы</small><br>Прикрепляет новую версию к существующему элементу. | <details><summary>Контракт</summary><br>**Scope:** `docs:version:create`<br>JSON обязателен: `ItemAttachVersion`; поля: `itemId`, `versionId`<br>**Ответ:** `204` → тело не описано</details> |
| `PATCH /public/v1/items/update`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Item/ItemUpdateV1) | <small>Файлы и элементы</small><br>Обновляет существующий элемент. | <details><summary>Контракт</summary><br>**Scope:** `docs:item:update`<br>JSON обязателен: `ItemUpdate`; поля: `id`<br>**Ответ:** `204` → тело не описано</details> |
| `PATCH /public/v1/items/move`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Item/ItemMoveV1) | <small>Файлы и элементы</small><br>Перемещает элемент в другую папку. | <details><summary>Контракт</summary><br>**Scope:** `docs:item:update`<br>JSON обязателен: `ItemMove`; поля: `id`, `newFolderId`<br>**Ответ:** `200` → тело не описано</details> |
| `PATCH /public/v1/items/versions/update`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Item/ItemUpdateVersionV1) | <small>Файлы и элементы</small><br>Обновляет существующую версию элемента. | <details><summary>Контракт</summary><br>**Scope:** `docs:version:update`<br>JSON обязателен: `ItemVersionUpdate`; поля: `id`<br>**Ответ:** `204` → тело не описано</details> |
| `DELETE /public/v1/items/{itemId}`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Item/ItemDeleteV1) | <small>Файлы и элементы</small><br>Перемещает элемент в корзину. | <details><summary>Контракт</summary><br>**Scope:** `docs:item:delete`<br>`itemId`* (путь)<br>**Ответ:** `204` → тело не описано</details> |
| <span id="ref-v1-version"></span>`POST /public/v1/versions`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Version/VersionCreateV1) | <small>Версии файлов</small><br>Создаёт новую версию объекта и возвращает её идентификатор. | <details><summary>Контракт</summary><br>**Scope:** `docs:version:create`<br>JSON обязателен: `VersionCreate`; поля: `name`, `objectId`, `projectId`<br>**Ответ:** `200` → `GuidSimpleDto`</details> |
| `GET /public/v1/versions`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Version/VersionListV1) | <small>Версии файлов</small><br>Возвращает версии элемента. | <details><summary>Контракт</summary><br>**Scope:** `docs:version:list`<br>`itemId`* (query), `Take` (query), `Skip` (query)<br>**Ответ:** `200` → `массив VersionListItem`</details> |
| `POST /public/v1/versions/find-batch`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Version/VersionListBatchV1) | <small>Версии файлов</small><br>Возвращает версии для набора элементов. | <details><summary>Контракт</summary><br>**Scope:** `docs:version:list`<br>JSON обязателен: `VersionsByItemsFind`; поля: `itemIds`, `projectId`<br>**Ответ:** `200` → `массив VersionListItemsBatch`</details> |
| `GET /public/v1/versions/count`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Version/VersionCountV1) | <small>Версии файлов</small><br>Подсчитывает версии элемента. | <details><summary>Контракт</summary><br>**Scope:** `docs:version:list`<br>`itemId`* (query), `Take` (query), `Skip` (query)<br>**Ответ:** `200` → `Int32SimpleDto`</details> |
| <span id="ref-v1-object"></span>`PUT /public/v1/objects`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Object/ObjectCreateV1) | <small>Объекты хранилища</small><br>Выдаёт билет для загрузки объекта; после загрузки объект требуется подтвердить отдельным запросом. | <details><summary>Контракт</summary><br>**Scope:** `docs:object:create`<br>JSON обязателен: `ObjectCreate`; поля: `mimeType`, `projectId`, `size`<br>**Ответ:** `200` → `ObjectUploadTicket`</details> |
| `POST /public/v1/objects/{objectId}/uploading/commit`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Object/ObjectCommitUploadingV1) | <small>Объекты хранилища</small><br>Подтверждает завершение загрузки объекта в S3. | <details><summary>Контракт</summary><br>**Scope:** `docs:object:create`<br>`objectId`* (путь)<br>**Ответ:** `200` → тело не описано</details> |
| <span id="ref-v1-share"></span>`POST /public/v1/shares`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Share/ShareListV1) | <small>Публикации файлов</small><br>Ищет публикации файлов по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `docs:share:list`<br>`Take` (query), `Skip` (query)<br>JSON обязателен: `ShareFind`; поля: `projectId`<br>**Ответ:** `200` → `массив ShareListItem`</details> |
| `PUT /public/v1/shares`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Share/ShareCreateV1) | <small>Публикации файлов</small><br>Создаёт публикацию указанного элемента. | <details><summary>Контракт</summary><br>**Scope:** `docs:share:create`<br>JSON обязателен: `ShareCreate`; поля: `sharedItemId`, `sharedItemType`, `shareType`<br>**Ответ:** `200` → `GuidSimpleDto`</details> |
| `PATCH /public/v1/shares`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Share/ShareUpdateV1) | <small>Публикации файлов</small><br>Обновляет существующую публикацию. | <details><summary>Контракт</summary><br>**Scope:** `docs:share:update`<br>JSON обязателен: `ShareUpdate`; поля: `id`<br>**Ответ:** `200` → тело не описано</details> |
| `DELETE /public/v1/shares`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Share/ShareDeleteV1) | <small>Публикации файлов</small><br>Изменяет состояние удаления существующей публикации. | <details><summary>Контракт</summary><br>**Scope:** `docs:share:delete`<br>JSON обязателен: `ShareDelete`; поля: `deleted`, `id`<br>**Ответ:** `200` → тело не описано</details> |
| `POST /public/v1/shares/count`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Share/ShareListCountV1) | <small>Публикации файлов</small><br>Подсчитывает публикации по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `docs:share:list`<br>JSON обязателен: `ShareFind`; поля: `projectId`<br>**Ответ:** `200` → `Int32SimpleDto`</details> |

#### 3.2. Папки и доступ
###### 3.2. Папки и доступ {#reference-folders}

| Метод и путь | Назначение | Параметры и ответ |
| --- | --- | --- |
| <span id="ref-v1-folder"></span>`GET /public/v1/folders/{folderId}/children`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Folder/FolderListChildrenV1) | <small>Папки</small><br>Возвращает непосредственных потомков папки. | <details><summary>Контракт</summary><br>**Scope:** `docs:folder:list`<br>`folderId`* (путь), `deleted` (query)<br>**Ответ:** `200` → `массив FolderListItem`</details> |
| `PUT /public/v1/folders`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Folder/FolderCreateV1) | <small>Папки</small><br>Создаёт папку и возвращает её идентификатор. | <details><summary>Контракт</summary><br>**Scope:** `docs:folder:create`<br>JSON обязателен: `FolderCreate`; поля: `name`, `parentId`<br>**Ответ:** `200` → `GuidSimpleDto`</details> |
| `PATCH /public/v1/folders`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Folder/FolderUpdateV1) | <small>Папки</small><br>Обновляет папку. | <details><summary>Контракт</summary><br>**Scope:** `docs:folder:update`<br>JSON обязателен: `FolderUpdate`; поля: `id`<br>**Ответ:** `204` → тело не описано</details> |
| `DELETE /public/v1/folders/{folderId}`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Folder/FolderDeleteV1) | <small>Папки</small><br>Перемещает папку в корзину. | <details><summary>Контракт</summary><br>**Scope:** `docs:folder:delete`<br>`folderId`* (путь)<br>**Ответ:** `204` → тело не описано</details> |
| `GET /public/v1/projects/{projectId}/folders/tree`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Folder/FolderGetProjectTreeV1) | <small>Папки</small><br>Возвращает полное дерево папок проекта с правами пользователя. | <details><summary>Контракт</summary><br>**Scope:** `docs:folder:read`<br>`projectId`* (путь)<br>**Ответ:** `200` → `FolderNodeUserPermissions`</details> |
| <span id="ref-v1-folderitemsnamingpattern"></span>`GET /public/v1/naming-patterns/folder-items/find`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/FolderItemsNamingPattern/FolderItemsNamingPatternFindV1) | <small>Правила именования</small><br>Возвращает правила именования файлов в папке. | <details><summary>Контракт</summary><br>**Scope:** `docs:item:create`<br>`folderId`* (query)<br>**Ответ:** `200` → `FolderItemsNamingPatternsValueDto`</details> |
| <span id="ref-v1-storage"></span>`POST /public/v1/storages`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Storage/StorageListV1) | <small>Хранилища</small><br>Ищет хранилища документов по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `docs:storage:list`<br>JSON обязателен: `StorageFind`<br>**Ответ:** `200` → `массив StorageListItem`</details> |
| <span id="ref-v1-permissions"></span>`POST /public/v1/permissions/folders/upsert`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Permissions/PermissionsUpsertBatchV1) | <small>Права на папки</small><br>Создаёт или обновляет права пользователей и ролей на конкретную папку. | <details><summary>Контракт</summary><br>**Scope:** `docs:permissions:update`<br>JSON обязателен: `PermissionUpsertBatch`; поля: `folderId`, `items`<br>**Ответ:** `200` → тело не описано; `204` → тело не описано</details> |
| `GET /public/v1/permissions/tree`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Permissions/PermissionsGetProjectPermissionsTreeV1) | <small>Права на папки</small><br>Возвращает дерево папок проекта с назначенными правами. | <details><summary>Контракт</summary><br>**Scope:** `docs:permissions:read`<br>`projectId`* (query)<br>**Ответ:** `200` → `FolderNodePermissions`</details> |
| `DELETE /public/v1/permissions/{permissionId}`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Permissions/PermissionsDeleteV1) | <small>Права на папки</small><br>Удаляет конкретное разрешение. | <details><summary>Контракт</summary><br>**Scope:** `docs:permissions:delete`<br>`permissionId`* (путь)<br>**Ответ:** `200` → тело не описано</details> |

#### 3.3. Замечания
###### 3.3. Замечания {#reference-issues}

| Метод и путь | Назначение | Параметры и ответ |
| --- | --- | --- |
| <span id="ref-v1-issue"></span>`POST /public/v1/issues`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Issue/IssueListV1) | <small>Замечания</small><br>Ищет замечания по фильтру с постраничным выводом. | <details><summary>Контракт</summary><br>**Scope:** `docs:issue:list`<br>`Take` (query), `Skip` (query)<br>JSON обязателен: `IssueFind`; поля: `projectId`<br>**Ответ:** `200` → `массив IssueListItem`</details> |
| `PATCH /public/v1/issues`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Issue/IssueUpdateV1) | <small>Замечания</small><br>Пакетно обновляет несколько замечаний. | <details><summary>Контракт</summary><br>**Scope:** `docs:issue:update`<br>JSON обязателен: `массив IssueUpdate`<br>**Ответ:** `200` → тело не описано</details> |
| `POST /public/v1/issues/count`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Issue/IssueListCountV1) | <small>Замечания</small><br>Подсчитывает замечания по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `docs:issue:list`<br>JSON обязателен: `IssueFind`; поля: `projectId`<br>**Ответ:** `200` → `Int32SimpleDto`</details> |
| `POST /public/v1/issues/items/counts`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Issue/IssueListItemIssuesCountV1) | <small>Замечания</small><br>Возвращает число замечаний, связанных с каждым из указанных элементов. | <details><summary>Контракт</summary><br>**Scope:** `docs:issue:list`<br>JSON обязателен: `ItemsIssuesCountGet`; поля: `itemIds`, `projectId`<br>**Ответ:** `200` → `массив IssueCountListItem`</details> |
| `POST /public/v1/issues/create`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Issue/IssueCreateV1) | <small>Замечания</small><br>Создаёт замечание. | <details><summary>Контракт</summary><br>**Scope:** `docs:issue:create`<br>JSON обязателен: `IssueCreate`; поля: `authorId`, `issueTypeId`, `name`, `projectId`, `responsible`, `status`<br>**Ответ:** `200` → `uuid`</details> |
| <span id="ref-v1-issueaccesses"></span>`POST /public/v1/issues/accesses`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/IssueAccesses/IssueAccessesListV1) | <small>Доступ к замечаниям</small><br>Возвращает правила доступа к замечаниям. | <details><summary>Контракт</summary><br>**Scope:** `docs:issue:list`<br>JSON обязателен: `IssueAccessesFind`; поля: `issueTypeIds`<br>**Ответ:** `200` → `массив IssueAccessListItem`</details> |
| <span id="ref-v1-issueattachment"></span>`POST /public/v1/issues/attachments`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/IssueAttachment/IssueAttachmentListV1) | <small>Вложения замечаний</small><br>Возвращает вложения указанного замечания. | <details><summary>Контракт</summary><br>**Scope:** `docs:issue:list`<br>JSON обязателен: `IssueAttachmentFind`; поля: `issueId`<br>**Ответ:** `200` → `массив IssueAttachmentListItem`</details> |
| `POST /public/v1/issues/attachments/object/download`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/IssueAttachment/IssueAttachmentDownloadObjectV1) | <small>Вложения замечаний</small><br>Создаёт билет для скачивания объекта вложения. | <details><summary>Контракт</summary><br>**Scope:** `docs:issue:read`<br>JSON обязателен: `IssueAttachmentDownloadObject`; поля: `issueAttachmentId`<br>**Ответ:** `200` → `IssueAttachmentDownloadTicket`</details> |
| <span id="ref-v1-issuecomment"></span>`POST /public/v1/issues/comments`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/IssueComment/IssueCommentListV1) | <small>Комментарии замечаний</small><br>Возвращает комментарии к замечаниям указанного проекта. | <details><summary>Контракт</summary><br>**Scope:** `docs:issue:list`<br>`Take` (query), `Skip` (query)<br>JSON обязателен: `IssueCommentFind`; поля: `issueIds`, `projectId`<br>**Ответ:** `200` → `массив IssueCommentListItem`</details> |
| `PUT /public/v1/issues/comments`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/IssueComment/IssueCommentCreateV1) | <small>Комментарии замечаний</small><br>Создаёт комментарий к указанному замечанию. | <details><summary>Контракт</summary><br>**Scope:** `docs:issue:create`<br>JSON обязателен: `IssueCommentCreate`; поля: `issueId`, `text`<br>**Ответ:** `200` → `GuidSimpleDto`</details> |
| `POST /public/v1/issues/comments/count`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/IssueComment/IssueCommentListCountV1) | <small>Комментарии замечаний</small><br>Подсчитывает комментарии по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `docs:issue:list`<br>JSON обязателен: `IssueCommentFind`; поля: `issueIds`, `projectId`<br>**Ответ:** `200` → `Int32SimpleDto`</details> |
| <span id="ref-v1-issueevents"></span>`POST /public/v1/issues/events`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/IssueEvents/IssueEventsListV1) | <small>События замечаний</small><br>Возвращает события замечаний по фильтру с постраничным выводом. | <details><summary>Контракт</summary><br>**Scope:** `docs:issue:list`<br>`Take` (query), `Skip` (query)<br>JSON обязателен: `IssueEventFind`; поля: `issueId`<br>**Ответ:** `200` → `массив IssueEventListItem`</details> |
| `POST /public/v1/issues/events/count`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/IssueEvents/IssueEventsListCountV1) | <small>События замечаний</small><br>Подсчитывает события замечаний по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `docs:issue:list`<br>JSON обязателен: `IssueEventFind`; поля: `issueId`<br>**Ответ:** `200` → `Int32SimpleDto`</details> |
| <span id="ref-v1-issueprojectsettings"></span>`GET /public/v1/issues/settings/project`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/IssueProjectSettings/IssueProjectSettingsGetV1) | <small>Настройки замечаний проекта</small><br>Возвращает настройки замечаний для указанного проекта. | <details><summary>Контракт</summary><br>**Scope:** `docs:issue:read`<br>`projectId`* (query)<br>**Ответ:** `200` → `IssueProjectSettings`</details> |
| <span id="ref-v1-issuetype"></span>`POST /public/v1/issues/types`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/IssueType/IssueTypeListV1) | <small>Типы замечаний</small><br>Ищет типы замечаний по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `docs:issue:list`<br>JSON обязателен: `IssueTypeFind`; поля: `projectId`<br>**Ответ:** `200` → `массив IssueTypeListItem`</details> |

#### 3.4. Согласования
###### 3.4. Согласования {#reference-reviews}

| Метод и путь | Назначение | Параметры и ответ |
| --- | --- | --- |
| <span id="ref-v1-review"></span>`POST /public/v1/reviews`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Review/ReviewListV1) | <small>Согласования</small><br>Возвращает согласования указанного проекта. | <details><summary>Контракт</summary><br>**Scope:** `docs:review:list`<br>`Take` (query), `Skip` (query)<br>JSON обязателен: `ReviewFindOrdered`; поля: `find`<br>**Ответ:** `200` → `массив ReviewListItem`</details> |
| `PATCH /public/v1/reviews`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Review/ReviewUpdateV1) | <small>Согласования</small><br>Изменяет основные сведения согласования. | <details><summary>Контракт</summary><br>**Scope:** `docs:review:update`<br>JSON обязателен: `ReviewUpdate`; поля: `id`<br>**Ответ:** `200` → тело не описано</details> |
| `POST /public/v1/reviews/count`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Review/ReviewListCountV1) | <small>Согласования</small><br>Подсчитывает согласования по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `docs:review:list`<br>JSON обязателен: `ReviewFind`; поля: `projectId`<br>**Ответ:** `200` → `Int32SimpleDto`</details> |
| `POST /public/v1/reviews/versions`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Review/ReviewGetVersionsV1) | <small>Согласования</small><br>Возвращает версии согласований по указанным идентификаторам. | <details><summary>Контракт</summary><br>**Scope:** `docs:review:list`<br>JSON обязателен: `ReviewVersionsGet`; поля: `reviewVersionIds`<br>**Ответ:** `200` → `массив ReviewVersion`</details> |
| `POST /public/v1/reviews/versions/item-versions`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Review/ReviewFindItemVersionIdsByReviewVersionIdsV1) | <small>Согласования</small><br>Возвращает идентификаторы версий элементов, сгруппированные по версиям согласований. | <details><summary>Контракт</summary><br>**Scope:** `docs:review:list`<br>JSON обязателен: `ReviewVersionItemVersionIdsFind`; поля: `reviewVersionIds`<br>**Ответ:** `200` → `object`</details> |
| `POST /public/v1/reviews/create`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Review/ReviewCreateV1) | <small>Согласования</small><br>Создаёт согласование. | <details><summary>Контракт</summary><br>**Scope:** `docs:review:create`<br>JSON обязателен: `ReviewCreate`; поля: `behalfUserId`, `cipher`, `name`, `projectId`, `reviewTypeId`<br>**Ответ:** `200` → `uuid`</details> |
| `PATCH /public/v1/reviews/type`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Review/ReviewSetTypeV1) | <small>Согласования</small><br>Устанавливает или изменяет тип согласования. | <details><summary>Контракт</summary><br>**Scope:** `docs:review:update`<br>JSON обязателен: `ReviewSetType`; поля: `id`, `reviewTypeId`<br>**Ответ:** `200` → тело не описано</details> |
| `PATCH /public/v1/reviews/comment`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Review/ReviewSetCommentV1) | <small>Согласования</small><br>Устанавливает или очищает комментарий последней версии согласования, кроме удалённого согласования. | <details><summary>Контракт</summary><br>**Scope:** `docs:review:update`<br>JSON обязателен: `ReviewSetComment`; поля: `authorId`, `comment`, `id`<br>**Ответ:** `200` → тело не описано</details> |
| <span id="ref-v1-reviewgroup"></span>`POST /public/v1/reviews/groups`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ReviewGroup/ReviewGroupListV1) | <small>Группы согласований</small><br>Возвращает группы согласований указанного проекта. | <details><summary>Контракт</summary><br>**Scope:** `docs:review:list`<br>`Take` (query), `Skip` (query)<br>JSON обязателен: `ReviewGroupFind`; поля: `projectId`<br>**Ответ:** `200` → `массив ReviewGroupListItem`</details> |
| <span id="ref-v1-reviewitem"></span>`POST /public/v1/reviews/items`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ReviewItem/ReviewItemGetReviewItemsStatusesV1) | <small>Документы согласований</small><br>Возвращает статусы согласования указанных версий элементов. | <details><summary>Контракт</summary><br>**Scope:** `docs:review:list`<br>JSON обязателен: `ReviewItemsStatusesGet`; поля: `itemVersionIds`, `projectId`<br>**Ответ:** `200` → `массив ReviewItemStatusListItem`</details> |
| `POST /public/v1/reviews/items/add`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ReviewItem/ReviewItemAddItemV1) | <small>Документы согласований</small><br>Добавляет версию элемента в существующее согласование. | <details><summary>Контракт</summary><br>**Scope:** `docs:review:update`<br>JSON обязателен: `ReviewItemAdd`; поля: `itemVersionId`, `reviewId`<br>**Ответ:** `200` → тело не описано</details> |
| `POST /public/v1/reviews/items/remove`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ReviewItem/ReviewItemRemoveItemV1) | <small>Документы согласований</small><br>Удаляет версию элемента из согласования. | <details><summary>Контракт</summary><br>**Scope:** `docs:review:update`<br>JSON обязателен: `ReviewItemRemove`; поля: `itemVersionId`, `reviewId`<br>**Ответ:** `200` → тело не описано</details> |
| <span id="ref-v1-reviewprocess"></span>`POST /public/v1/reviews/process/start`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ReviewProcess/ReviewProcessStartV1) | <small>Запуск согласований</small><br>Запускает процесс указанного согласования. | <details><summary>Контракт</summary><br>**Scope:** `docs:review:update`<br>JSON обязателен: `ReviewStart`; поля: `behalfUserId`, `reviewId`<br>**Ответ:** `200` → тело не описано</details> |
| <span id="ref-v1-reviewtype"></span>`GET /public/v1/reviews/types/names`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ReviewType/ReviewTypeFindNamesV1) | <small>Типы согласований</small><br>Возвращает названия типов согласований указанного проекта. | <details><summary>Контракт</summary><br>**Scope:** `docs:review:list`<br>`projectId`* (query)<br>**Ответ:** `200` → `массив ReviewTypeName`</details> |
| `POST /public/v1/reviews/types/create`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ReviewType/ReviewTypeCreateV1) | <small>Типы согласований</small><br>Создаёт тип согласования проекта. | <details><summary>Контракт</summary><br>**Scope:** `docs:review:create`<br>JSON обязателен: `ReviewTypeCreate`; поля: `name`, `projectId`, `version`<br>**Ответ:** `200` → `uuid`</details> |
| `PATCH /public/v1/reviews/types`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ReviewType/ReviewTypeUpdateV1) | <small>Типы согласований</small><br>Обновляет существующий тип согласования. | <details><summary>Контракт</summary><br>**Scope:** `docs:review:update`<br>JSON обязателен: `ReviewTypeUpdate`; поля: `id`, `projectId`<br>**Ответ:** `200` → тело не описано</details> |

#### 3.5. Передачи
###### 3.5. Передачи {#reference-transfers}

| Метод и путь | Назначение | Параметры и ответ |
| --- | --- | --- |
| <span id="ref-v1-documentstransfer"></span>`POST /public/v1/documents-transfers`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/DocumentsTransfer/DocumentsTransferListV1) | <small>Передачи документов</small><br>Ищет передачи документов по фильтру с постраничным выводом. | <details><summary>Контракт</summary><br>**Scope:** `docs:docs_transfer:list`<br>`Take` (query), `Skip` (query)<br>JSON обязателен: `DocumentsTransfersFind`; поля: `projectId`<br>**Ответ:** `200` → `массив DocumentsTransferListItem`</details> |
| `GET /public/v1/documents-transfers`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/DocumentsTransfer/DocumentsTransferGetAllDataV1) | <small>Передачи документов</small><br>Возвращает подробные сведения об одной передаче документов по её идентификатору. | <details><summary>Контракт</summary><br>**Scope:** `docs:docs_transfer:read`<br>`id`* (query)<br>**Ответ:** `200` → `DocumentsTransferAllData`</details> |
| `POST /public/v1/documents-transfers/count`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/DocumentsTransfer/DocumentsTransferListCountV1) | <small>Передачи документов</small><br>Подсчитывает передачи документов по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `docs:docs_transfer:list`<br>JSON обязателен: `DocumentsTransfersFind`; поля: `projectId`<br>**Ответ:** `200` → `Int32SimpleDto`</details> |
| `POST /public/v1/documents-transfers/create`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/DocumentsTransfer/DocumentsTransferCreateV1) | <small>Передачи документов</small><br>Создаёт передачу документов. | <details><summary>Контракт</summary><br>**Scope:** `docs:docs_transfer:create`<br>JSON обязателен: `DocumentsTransferCreate`; поля: `authorId`, `cipher`, `documentsTransferTypeId`, `name`<br>**Ответ:** `200` → `uuid`</details> |
| <span id="ref-v1-documentstransferacceptance"></span>`POST /public/v1/documents-transfer-acceptances/send`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/DocumentsTransferAcceptance/DocumentsTransferAcceptanceSendV1) | <small>Отправка передач</small><br>Отправляет подготовленную передачу документов получателю. | <details><summary>Контракт</summary><br>**Scope:** `docs:docs_transfer:update`<br>JSON обязателен: `DocumentsTransferSend`; поля: `authorId`, `documentsTransferId`, `recipient`<br>**Ответ:** `200` → тело не описано</details> |
| <span id="ref-v1-documentstransferaccesses"></span>`POST /public/v1/documents-transfers/accesses`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/DocumentsTransferAccesses/DocumentsTransferAccessesListV1) | <small>Доступ к передачам</small><br>Возвращает правила доступа для указанных типов передачи документов. | <details><summary>Контракт</summary><br>**Scope:** `docs:docs_transfer:list`<br>JSON: `DocumentsTransferAccessesFind`; поля: `documentsTransferTypeIds`<br>**Ответ:** `200` → `массив DocumentsTransferAccessListItem`</details> |
| <span id="ref-v1-documentstransferitem"></span>`POST /public/v1/documents-transfer-items`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/DocumentsTransferItem/DocumentsTransferItemListV1) | <small>Состав передач</small><br>Возвращает элементы указанной передачи документов с постраничным выводом. | <details><summary>Контракт</summary><br>**Scope:** `docs:docs_transfer:list`<br>`Take` (query), `Skip` (query)<br>JSON обязателен: `DocumentsTransferItemFind`; поля: `documentsTransferId`<br>**Ответ:** `200` → `массив DocumentsTransferItemListItem`</details> |
| `POST /public/v1/documents-transfer-items/count`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/DocumentsTransferItem/DocumentsTransferItemListCountV1) | <small>Состав передач</small><br>Подсчитывает элементы указанной передачи документов. | <details><summary>Контракт</summary><br>**Scope:** `docs:docs_transfer:list`<br>JSON обязателен: `DocumentsTransferItemFind`; поля: `documentsTransferId`<br>**Ответ:** `200` → `Int32SimpleDto`</details> |
| `GET /public/v1/documents-transfer-items/download`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/DocumentsTransferItem/DocumentsTransferItemDownloadV1) | <small>Состав передач</small><br>Выдаёт временный билет для скачивания элемента передачи документов. | <details><summary>Контракт</summary><br>**Scope:** `docs:docs_transfer:read`<br>`documentsTransferItemId`* (query), `fileName` (query)<br>**Ответ:** `200` → `DocumentsTransferItemDownloadTicket`</details> |
| `POST /public/v1/documents-transfer-items/add`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/DocumentsTransferItem/DocumentsTransferItemAddItemsV1) | <small>Состав передач</small><br>Добавляет версии элементов в передачу документов. | <details><summary>Контракт</summary><br>**Scope:** `docs:docs_transfer:update`<br>JSON обязателен: `DocumentsTransferItemsAdd`; поля: `documentsTransferId`, `itemVersionIds`<br>**Ответ:** `200` → тело не описано</details> |
| <span id="ref-v1-documentstransfertype"></span>`POST /public/v1/documents-transfers/types`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/DocumentsTransferType/DocumentsTransferTypeListV1) | <small>Типы передач</small><br>Ищет типы передачи документов по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `docs:docs_transfer:list`<br>JSON обязателен: `DocumentsTransferTypeFind`; поля: `projectId`<br>**Ответ:** `200` → `массив DocumentsTransferTypeListItem`</details> |
| <span id="ref-v1-acceptancecertificate"></span>`GET /public/v1/acceptance-certificates/download`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/AcceptanceCertificate/AcceptanceCertificateDownloadV1) | <small>Акты приёмки</small><br>Выдаёт временный билет для скачивания файла акта приёмки. | <details><summary>Контракт</summary><br>**Scope:** `docs:docs_transfer:read`<br>`acceptanceCertificateId`* (query), `fileName` (query)<br>**Ответ:** `200` → `AcceptanceCertificateDownloadTicket`</details> |
| `POST /public/v1/acceptance-certificates/attach`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/AcceptanceCertificate/AcceptanceCertificateAttachV1) | <small>Акты приёмки</small><br>Прикрепляет акт приёмки к передаче документов. | <details><summary>Контракт</summary><br>**Scope:** `docs:docs_transfer:update`<br>JSON обязателен: `AcceptanceCertificateAttach`; поля: `authorId`, `companyRecipient`, `companySender`, `documentsTransferId`, `projectName`<br>**Ответ:** `200` → `uuid`</details> |

#### 3.6. Формы
###### 3.6. Формы {#reference-forms}

| Метод и путь | Назначение | Параметры и ответ |
| --- | --- | --- |
| <span id="ref-v1-projectform"></span>`POST /public/v1/projects/forms`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ProjectForm/ProjectFormListV1) | <small>Формы проекта</small><br>Ищет формы проекта по фильтру и сортировке с постраничным выводом. | <details><summary>Контракт</summary><br>**Scope:** `forms:project_form:list`<br>`Take` (query), `Skip` (query)<br>JSON обязателен: `ProjectFormFindOrdered`; поля: `find`<br>**Ответ:** `200` → `ProjectFormRegistryResult`</details> |
| `POST /public/v1/projects/forms/count`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ProjectForm/ProjectFormListCountV1) | <small>Формы проекта</small><br>Подсчитывает формы проекта по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `forms:project_form:list`<br>JSON обязателен: `ProjectFormFind`; поля: `formTypeId`, `projectId`<br>**Ответ:** `200` → `int32`</details> |
| `POST /public/v1/projects/forms/get`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ProjectForm/ProjectFormGetV1) | <small>Формы проекта</small><br>Возвращает форму проекта по идентификатору. | <details><summary>Контракт</summary><br>**Scope:** `forms:project_form:read`<br>JSON обязателен: `ProjectFormGet`; поля: `projectFormId`<br>**Ответ:** `200` → `ProjectForm`</details> |
| `POST /public/v1/projects/forms/get-summary`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ProjectForm/ProjectFormGetSummaryV1) | <small>Формы проекта</small><br>Возвращает сводные данные указанных форм проекта. | <details><summary>Контракт</summary><br>**Scope:** `forms:project_form:read`<br>JSON обязателен: `ProjectFormsSummaryGet`; поля: `projectFormIds`, `projectIds`<br>**Ответ:** `200` → `массив ProjectFormSummary`</details> |
| `POST /public/v1/projects/forms/find-form-source`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ProjectForm/ProjectFormFindFormSourceV1) | <small>Формы проекта</small><br>Ищет формы проекта, которые могут быть источниками данных для указанного типа поля, по заданным критериям. | <details><summary>Контракт</summary><br>**Scope:** `forms:project_form:list`<br>JSON обязателен: `FormSourceProjectFormFind`; поля: `formFieldTypeId`, `projectId`<br>**Ответ:** `200` → `FormSourceProjectFormResult`</details> |
| `POST /public/v1/projects/forms/get-values-for-template-item`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ProjectForm/ProjectFormGetValuesForTemplateItemV1) | <small>Формы проекта</small><br>Возвращает значения элемента шаблона формы проекта. | <details><summary>Контракт</summary><br>**Scope:** `forms:project_form:read`<br>JSON обязателен: `ProjectFormValuesForTemplateItemGet`; поля: `projectFormId`<br>**Ответ:** `200` → `ProjectFormValuesForTemplateItem`</details> |
| `POST /public/v1/projects/forms/get-download-url-by-template-item`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ProjectForm/ProjectFormGetDownloadUrlByTemplateItemV1) | <small>Формы проекта</small><br>Выдаёт временную ссылку для скачивания элемента шаблона формы проекта. | <details><summary>Контракт</summary><br>**Scope:** `forms:project_form:read`<br>JSON обязателен: `ProjectFormTemplateItemDownloadUrlGet`; поля: `projectFormId`, `templateItemId`<br>**Ответ:** `200` → `ProjectFormItemDownloadTicket`</details> |
| `POST /public/v1/projects/forms/create-batch`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ProjectForm/ProjectFormCreateBatchV1) | <small>Формы проекта</small><br>Создаёт несколько форм проекта одним запросом. | <details><summary>Контракт</summary><br>**Scope:** `forms:project_form:create`<br>JSON обязателен: `ProjectFormBatchCreate`; поля: `forms`, `projectFormTypeId`<br>**Ответ:** `200` → `массив uuid`</details> |
| `PATCH /public/v1/projects/forms/update`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ProjectForm/ProjectFormUpdateV1) | <small>Формы проекта</small><br>Обновляет существующую форму проекта. | <details><summary>Контракт</summary><br>**Scope:** `forms:project_form:update`<br>JSON обязателен: `ProjectFormUpdate`; поля: `projectFormFields`, `projectFormId`<br>**Ответ:** `200` → тело не описано</details> |
| `PATCH /public/v1/projects/forms/complete`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ProjectForm/ProjectFormCompleteV1) | <small>Формы проекта</small><br>Переводит существующую форму проекта в завершённое состояние. | <details><summary>Контракт</summary><br>**Scope:** `forms:project_form:update`<br>JSON обязателен: `ProjectFormComplete`; поля: `projectFormId`<br>**Ответ:** `200` → тело не описано</details> |
| <span id="ref-v1-projectformfieldtype"></span>`POST /public/v1/projects/forms/fields/types`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ProjectFormFieldType/ProjectFormFieldTypeListV1) | <small>Типы полей форм проекта</small><br>Ищет типы полей форм проекта и связанные источники отображения по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `forms:project_form_field_type:list`<br>JSON обязателен: `ProjectFormFieldTypeFind`; поля: `projectFormTypeId`<br>**Ответ:** `200` → `ProjectFormFieldTypeFindResult`</details> |
| <span id="ref-v1-projectformtype"></span>`POST /public/v1/projects/forms/types`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ProjectFormType/ProjectFormTypeListV1) | <small>Типы форм проекта</small><br>Ищет типы форм проекта по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `forms:project_form_type:list`<br>JSON обязателен: `ProjectFormTypeFind`; поля: `projectId`<br>**Ответ:** `200` → `массив ProjectFormType`</details> |
| <span id="ref-v1-formfieldtype"></span>`POST /public/v1/forms/fields/types`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/FormFieldType/FormFieldTypeListV1) | <small>Типы полей форм</small><br>Ищет типы полей форм по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `forms:form_field_type:list`<br>JSON обязателен: `FormFieldTypeFind`<br>**Ответ:** `200` → `массив FormFieldType`</details> |
| <span id="ref-v1-formtype"></span>`POST /public/v1/forms/types`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/FormType/FormTypeListV1) | <small>Типы форм</small><br>Ищет типы форм по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `forms:form_type:list`<br>JSON обязателен: `FormTypeFind`<br>**Ответ:** `200` → `массив FormType`</details> |
| <span id="ref-v1-formtypegroup"></span>`POST /public/v1/forms/types/groups`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/FormTypeGroup/FormTypeGroupListV1) | <small>Группы типов форм</small><br>Ищет группы типов форм по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `forms:form_type_group:list`<br>JSON обязателен: `FormTypeGroupFind`<br>**Ответ:** `200` → `массив FormTypeGroup`</details> |

#### 3.7. Атрибуты
###### 3.7. Атрибуты {#reference-attributes}

| Метод и путь | Назначение | Параметры и ответ |
| --- | --- | --- |
| <span id="ref-v1-attribute"></span>`POST /public/v1/attributes`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Attribute/AttributeListV1) | <small>Атрибуты</small><br>Возвращает атрибуты по заданному фильтру. | <details><summary>Контракт</summary><br>**Scope:** `docs:attribute:list`<br>JSON обязателен: `AttributeFind`; поля: `projectId`, `type`<br>**Ответ:** `200` → `массив AttributeListItem`</details> |
| <span id="ref-v1-attributetype"></span>`POST /public/v1/attributes/types`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/AttributeType/AttributeTypeListV1) | <small>Типы атрибутов</small><br>Ищет типы атрибутов по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `docs:attribute:list`<br>JSON обязателен: `AttributeTypeFind`; поля: `projectId`<br>**Ответ:** `200` → `массив AttributeType`</details> |
| `PATCH /public/v1/attributes/types`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/AttributeType/AttributeTypeUpdateV1) | <small>Типы атрибутов</small><br>Обновляет существующие типы атрибутов. | <details><summary>Контракт</summary><br>**Scope:** `docs:attribute:update`<br>JSON обязателен: `AttributeTypesUpdate`; поля: `data`, `projectId`<br>**Ответ:** `200` → тело не описано</details> |
| `POST /public/v1/attributes/types/create`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/AttributeType/AttributeTypeCreateV1) | <small>Типы атрибутов</small><br>Создаёт новый тип атрибута. | <details><summary>Контракт</summary><br>**Scope:** `docs:attribute:create`<br>JSON обязателен: `AttributeTypeCreate`; поля: `isRequired`, `name`, `order`, `projectId`, `type`<br>**Ответ:** `200` → `uuid`</details> |
| <span id="ref-v1-attributetypelistitems"></span>`POST /public/v1/attributes/types/list/items/create`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/AttributeTypeListItems/AttributeTypeListItemsCreateV1) | <small>Значения списочных типов</small><br>Добавляет варианты значений в атрибут типа «список». | <details><summary>Контракт</summary><br>**Scope:** `docs:attribute:create`<br>JSON обязателен: `AttributeTypeListItemsCreate`; поля: `attributeTypeId`, `items`<br>**Ответ:** `200` → тело не описано</details> |
| `PATCH /public/v1/attributes/types/list/items`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/AttributeTypeListItems/AttributeTypeListItemsUpdateV1) | <small>Значения списочных типов</small><br>Изменяет варианты значений атрибута типа «список». | <details><summary>Контракт</summary><br>**Scope:** `docs:attribute:update`<br>JSON обязателен: `AttributeTypeListItemsUpdate`; поля: `attributeTypeId`, `items`<br>**Ответ:** `200` → тело не описано</details> |
| <span id="ref-v1-attributevalue"></span>`POST /public/v1/attributes/values/issues`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/AttributeValue/AttributeValueListIssuesV1) | <small>Значения атрибутов</small><br>Возвращает значения атрибутов замечаний по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `docs:attribute:list`<br>JSON обязателен: `IssueAttributeValueFind`; поля: `issueIds`, `projectId`<br>**Ответ:** `200` → `массив IssueAttributeValueListItem`</details> |
| `POST /public/v1/attributes/values/items`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/AttributeValue/AttributeValueListItemsV1) | <small>Значения атрибутов</small><br>Возвращает значения атрибутов элементов по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `docs:attribute:list`<br>JSON обязателен: `ItemAttributeValueFind`; поля: `itemIds`, `projectId`<br>**Ответ:** `200` → `массив ItemAttributeValueListItem`</details> |
| `POST /public/v1/attributes/values/folders`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/AttributeValue/AttributeValueListFoldersV1) | <small>Значения атрибутов</small><br>Возвращает значения атрибутов папок по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `docs:attribute:list`<br>JSON обязателен: `FolderAttributeValueFind`; поля: `folderIds`, `projectId`<br>**Ответ:** `200` → `массив FolderAttributeValueListItem`</details> |
| `POST /public/v1/attributes/values/set`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/AttributeValue/AttributeValueSetV1) | <small>Значения атрибутов</small><br>Устанавливает значения атрибутов для указанной сущности. | <details><summary>Контракт</summary><br>**Scope:** `docs:attribute:update`<br>JSON обязателен: `AttributeValuesSet`; поля: `type`, `values`<br>**Ответ:** `200` → тело не описано; `204` → тело не описано</details> |

#### 3.8. Компания и проекты
###### 3.8. Компания и проекты {#reference-access}

| Метод и путь | Назначение | Параметры и ответ |
| --- | --- | --- |
| <span id="ref-v1-auth"></span>`POST /public/v1/auth/token`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Auth/AuthGetTokenV1) | <small>Авторизация</small><br>Выдаёт JWT указанному клиенту; запрошенные scope определяют права токена. | <details><summary>Контракт</summary><br>**Scope:** clientId, clientSecret и запрошенные scopes<br>JSON обязателен: `AuthCredentials`; поля: `clientId`, `clientSecret`, `scopes`<br>**Ответ:** `200` → `AuthToken`</details> |
| <span id="ref-v1-company"></span>`GET /public/v1/company/users`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Company/CompanyListUsersV1) | <small>Компания</small><br>Возвращает пользователей компании. | <details><summary>Контракт</summary><br>**Scope:** `company:user:list`<br>`Take` (query), `Skip` (query)<br>**Ответ:** `200` → `массив CompanyUserInfo`</details> |
| `GET /public/v1/company/roles`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Company/CompanyListRolesV1) | <small>Компания</small><br>Возвращает роли компании. | <details><summary>Контракт</summary><br>**Scope:** `company:role:list`<br>`Take` (query), `Skip` (query)<br>**Ответ:** `200` → `массив RoleInfo`</details> |
| <span id="ref-v1-companyuser"></span>`GET /public/v1/company-users/by-telegram-id`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/CompanyUser/CompanyUserGetUserIdByTelegramIdV1) | <small>Пользователи компании</small><br>Возвращает идентификатор пользователя компании по Telegram ID. | <details><summary>Контракт</summary><br>**Scope:** В схеме не указан<br>`telegramId`* (query)<br>**Ответ:** `200` → `uuid`</details> |
| `PUT /public/v1/company-users`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/CompanyUser/CompanyUserAddCompanyUsersV1) | <small>Пользователи компании</small><br>Пакетно приглашает или добавляет пользователей в компанию. | <details><summary>Контракт</summary><br>**Scope:** `hub:company:user:create`<br>JSON обязателен: `CompanyUsersAdd`; поля: `users`<br>**Ответ:** `200` → `массив CompanyUserAddResult`</details> |
| `DELETE /public/v1/company-users`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/CompanyUser/CompanyUserDeleteCompanyUsersV1) | <small>Пользователи компании</small><br>Пакетно удаляет пользователей из компании. | <details><summary>Контракт</summary><br>**Scope:** `hub:company:user:delete`<br>JSON обязателен: `CompanyUsersDelete`; поля: `userIds`<br>**Ответ:** `200` → тело не описано</details> |
| <span id="ref-v1-companyusercustomrole"></span>`PUT /public/v1/company-user-custom-roles`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/CompanyUserCustomRole/CompanyUserCustomRoleSetCompanyUserCustomRolesV1) | <small>Дополнительные роли компании</small><br>Заменяет дополнительные роли пользователя на уровне компании переданным списком. | <details><summary>Контракт</summary><br>**Scope:** `company:role:update`<br>JSON обязателен: `CompanyUserCustomRolesSet`; поля: `customRoleIds`, `userId`<br>**Ответ:** `200` → тело не описано</details> |
| <span id="ref-v1-applicationuser"></span>`PUT /public/v1/application-users`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ApplicationUser/ApplicationUserUpsertApplicationUsersV1) | <small>Доступ пользователей к приложениям</small><br>Пакетно назначает пользователям роли в нескольких приложениях. | <details><summary>Контракт</summary><br>**Scope:** `hub:application:user:update`<br>JSON обязателен: `ApplicationUsersUpsert`; поля: `applicationIds`, `role`, `userIds`<br>**Ответ:** `200` → тело не описано</details> |
| `DELETE /public/v1/application-users`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ApplicationUser/ApplicationUserDeleteApplicationUsersV1) | <small>Доступ пользователей к приложениям</small><br>Пакетно отзывает доступ пользователей к приложениям. | <details><summary>Контракт</summary><br>**Scope:** `hub:application:user:delete`<br>JSON обязателен: `ApplicationUsersDelete`; поля: `applicationIds`, `userIds`<br>**Ответ:** `200` → тело не описано</details> |
| <span id="ref-v1-project"></span>`GET /public/v1/projects/{projectId}`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Project/ProjectGetV1) | <small>Проекты</small><br>Возвращает сведения об указанном проекте. | <details><summary>Контракт</summary><br>**Scope:** `project:read`<br>`projectId`* (путь)<br>**Ответ:** `200` → `HubProjectInfo`</details> |
| `GET /public/v1/projects`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Project/ProjectListV1) | <small>Проекты</small><br>Возвращает список проектов компании. | <details><summary>Контракт</summary><br>**Scope:** `project:list`<br>`Take` (query), `Skip` (query)<br>**Ответ:** `200` → `массив ProjectListItem`</details> |
| `PATCH /public/v1/projects`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Project/ProjectUpdateV1) | <small>Проекты</small><br>Изменяет основные сведения существующего проекта. | <details><summary>Контракт</summary><br>**Scope:** `project:update`<br>JSON обязателен: `ProjectUpdate`; поля: `id`, `name`, `timeZoneOffset`<br>**Ответ:** `200` → тело не описано</details> |
| `GET /public/v1/projects/{projectId}/users`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Project/ProjectListUsersV1) | <small>Проекты</small><br>Возвращает пользователей проекта. | <details><summary>Контракт</summary><br>**Scope:** `project:user:list`<br>`projectId`* (путь), `Take` (query), `Skip` (query)<br>**Ответ:** `200` → `массив ProjectUserInfo`</details> |
| `GET /public/v1/projects/{projectId}/users/{userId}/permissions`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Project/ProjectGetUserPermissionsV1) | <small>Проекты</small><br>Возвращает права пользователя в проекте; при отсутствии прав схема предусматривает ответ 404. | <details><summary>Контракт</summary><br>**Scope:** `project:user:read`<br>`projectId`* (путь), `userId`* (путь)<br>**Ответ:** `200` → `ProjectUserPermissions`</details> |
| `GET /public/v1/projects/{projectId}/roles`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Project/ProjectListRolesV1) | <small>Проекты</small><br>Возвращает роли проекта. | <details><summary>Контракт</summary><br>**Scope:** `project:role:list`<br>`projectId`* (путь), `Take` (query), `Skip` (query)<br>**Ответ:** `200` → `массив RoleInfo`</details> |
| <span id="ref-v1-docsproject"></span>`GET /public/v1/docs/projects/{projectId}`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/DocsProject/DocsProjectGetInfoV1) | <small>Проекты DOCS</small><br>Возвращает сведения о проекте в SIGNAL DOCS. | <details><summary>Контракт</summary><br>**Scope:** `project:read`<br>`projectId`* (путь)<br>**Ответ:** `200` → `DocsProjectInfo`</details> |
| `GET /public/v1/docs/projects/storage-id`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/DocsProject/DocsProjectGetStorageIdV1) | <small>Проекты DOCS</small><br>Возвращает идентификатор хранилища, назначенного проекту. | <details><summary>Контракт</summary><br>**Scope:** `project:read`<br>`projectId`* (query)<br>**Ответ:** `200` → `GuidNullableSimpleDto`</details> |
| <span id="ref-v1-projectuser"></span>`PUT /public/v1/project-users`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ProjectUser/ProjectUserAddProjectsUsersV1) | <small>Пользователи проектов</small><br>Пакетно добавляет пользователей в несколько проектов. | <details><summary>Контракт</summary><br>**Scope:** `hub:project:user:create`<br>JSON обязателен: `ProjectsUsersAdd`; поля: `projectIds`, `userIds`<br>**Ответ:** `200` → тело не описано</details> |
| `DELETE /public/v1/project-users`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ProjectUser/ProjectUserDeleteProjectsUsersV1) | <small>Пользователи проектов</small><br>Пакетно удаляет пользователей из нескольких проектов. | <details><summary>Контракт</summary><br>**Scope:** `hub:project:user:delete`<br>JSON обязателен: `ProjectsUsersDelete`; поля: `projectIds`, `userIds`<br>**Ответ:** `200` → тело не описано</details> |
| <span id="ref-v1-projectusercustomrole"></span>`PUT /public/v1/project-user-custom-roles`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/ProjectUserCustomRole/ProjectUserCustomRoleSetProjectUserCustomRolesV1) | <small>Дополнительные роли проектов</small><br>Заменяет дополнительные роли пользователя в проекте переданным списком. | <details><summary>Контракт</summary><br>**Scope:** `project:role:update`<br>JSON обязателен: `ProjectUserCustomRolesSet`; поля: `customRoleIds`, `projectId`, `userId`<br>**Ответ:** `200` → тело не описано</details> |
| <span id="ref-v1-userlog"></span>`POST /public/v1/user-logs`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/UserLog/UserLogListV1) | <small>Журнал действий</small><br>Возвращает записи журнала действий пользователей по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `logs:user:list`<br>JSON обязателен: `UserLogFind`<br>**Ответ:** `200` → `массив UserLogListItem`</details> |

#### 3.9. Модели и подписи
###### 3.9. Модели и подписи {#reference-models}

| Метод и путь | Назначение | Параметры и ответ |
| --- | --- | --- |
| <span id="ref-v1-forge"></span>`POST /public/v1/forge/convert`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Forge/ForgeConvertV1) | <small>Просмотр моделей через Forge</small><br>Запускает преобразование модели через Forge для просмотра; поддерживаемые форматы перечислены в Swagger. | <details><summary>Контракт</summary><br>**Scope:** `docs:viewer:execute`<br>JSON обязателен: `ForgeConvert`; поля: `versionId`<br>**Ответ:** `204` → тело не описано</details> |
| `POST /public/v1/forge/item-versions/viewer`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Forge/ForgeGetViewersDataV1) | <small>Просмотр моделей через Forge</small><br>Возвращает токен доступа и URN моделей для отображения версий файлов в Forge Viewer. | <details><summary>Контракт</summary><br>**Scope:** `docs:viewer:read`<br>JSON обязателен: `ForgeModelsToViewRequest`; поля: `itemVersionIds`, `projectId`<br>**Ответ:** `200` → `ForgeModelsToView`</details> |
| <span id="ref-v1-tangl"></span>`POST /public/v1/tangl/convert`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Tangl/TanglConvertV1) | <small>Просмотр моделей через Tangl</small><br>Запускает преобразование модели через Tangl для просмотра; схема указывает форматы .rvt и .ifc. | <details><summary>Контракт</summary><br>**Scope:** `docs:viewer:execute`<br>JSON обязателен: `TanglConvert`; поля: `versionId`<br>**Ответ:** `204` → тело не описано</details> |
| <span id="ref-v1-cadessignature"></span>`GET /public/v1/cades/signatures`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/CadesSignature/CadesSignatureListV1) | <small>CAdES-подписи</small><br>Возвращает CAdES-подписи версии файла. | <details><summary>Контракт</summary><br>**Scope:** `docs:signing:list`<br>`versionId`* (query), `searchMchdIds` (query)<br>**Ответ:** `200` → `массив CadesVersionSignatureListItem`</details> |
| `PUT /public/v1/cades/signatures`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/CadesSignature/CadesSignatureCreateV1) | <small>CAdES-подписи</small><br>Создаёт новую CAdES-подпись. | <details><summary>Контракт</summary><br>**Scope:** `docs:signing:create`<br>JSON обязателен: `CadesSignatureCreate`; поля: `certificateId`, `signature`, `versionId`<br>**Ответ:** `204` → тело не описано</details> |
| <span id="ref-v1-embeddedsignature"></span>`GET /public/v1/embedded/signatures`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/EmbeddedSignature/EmbeddedSignatureListV1) | <small>Встроенные подписи</small><br>Возвращает встроенные подписи элемента. | <details><summary>Контракт</summary><br>**Scope:** `docs:signing:list`<br>`itemId`* (query)<br>**Ответ:** `200` → `массив EmbeddedVersionSignatureListItem`</details> |
| `PUT /public/v1/embedded/signatures`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/EmbeddedSignature/EmbeddedSignatureCreateV1) | <small>Встроенные подписи</small><br>Создаёт встроенную подпись. | <details><summary>Контракт</summary><br>**Scope:** `docs:signing:create`<br>JSON обязателен: `EmbeddedSignatureCreate`; поля: `certificateId`, `itemId`, `signature`, `versionId`<br>**Ответ:** `204` → тело не описано</details> |
| <span id="ref-v1-mchd"></span>`GET /public/v1/mchd/company`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Mchd/MchdGetCompanyMchdDocumentsV1) | <small>Машиночитаемые доверенности</small><br>Возвращает UUID машиночитаемых доверенностей (МЧД) компании. | <details><summary>Контракт</summary><br>**Scope:** `docs:signing:list`<br>`Take` (query), `Skip` (query)<br>**Ответ:** `200` → `GuidIReadOnlyCollectionSimpleDto`</details> |
| `GET /public/v1/mchd/cades/signatures/{cadesSignatureId}`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Mchd/MchdGetAttachedMchdDocumentsV1) | <small>Машиночитаемые доверенности</small><br>Возвращает идентификаторы МЧД, связанных с CAdES-подписью. | <details><summary>Контракт</summary><br>**Scope:** `docs:signing:list`<br>`cadesSignatureId`* (путь)<br>**Ответ:** `200` → `массив AttachedMchdDocumentListItem`</details> |
| `GET /public/v1/mchd/{mchdId}/object/download`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Mchd/MchdDownloadV1) | <small>Машиночитаемые доверенности</small><br>Выдаёт билет для скачивания МЧД. | <details><summary>Контракт</summary><br>**Scope:** `docs:signing:read`<br>`mchdId`* (путь)<br>**Ответ:** `200` → `MchdObjectDownloadTicket`</details> |

#### 3.10. Другие модули
###### 3.10. Другие модули {#reference-modules}

| Метод и путь | Назначение | Параметры и ответ |
| --- | --- | --- |
| <span id="ref-v1-board"></span>`POST /public/v1/boards`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Board/BoardListV1) | <small>Дашборды</small><br>Возвращает дашборды проекта по фильтру; удалённые дашборды исключены. | <details><summary>Контракт</summary><br>**Scope:** `dash:board:list`<br>`Take` (query), `Skip` (query)<br>JSON обязателен: `BoardFind`; поля: `projectId`<br>**Ответ:** `200` → `массив Board`</details> |
| <span id="ref-v1-card"></span>`POST /public/v1/boards/cards`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Card/CardListV1) | <small>Карточки дашбордов</small><br>Возвращает карточки дашборда с возможностью отбора по группам; удалённые карточки и карточки удалённых групп или дашбордов исключены. | <details><summary>Контракт</summary><br>**Scope:** `dash:card:list`<br>`Take` (query), `Skip` (query)<br>JSON обязателен: `CardFind`; поля: `boardId`<br>**Ответ:** `200` → `массив Card`</details> |
| `GET /public/v1/boards/cards/{cardId}`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Card/CardGetV1) | <small>Карточки дашбордов</small><br>Возвращает карточку с содержимым по её идентификатору. | <details><summary>Контракт</summary><br>**Scope:** `dash:card:read`<br>`cardId`* (путь)<br>**Ответ:** `200` → `Card`</details> |
| <span id="ref-v1-cardpubliclink"></span>`PATCH /public/v1/card-public-links/regenerate`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/CardPublicLink/CardPublicLinkRegenerateCardPubLinkV1) | <small>Публичные ссылки карточек</small><br>Перегенерирует публичную ссылку на карточку дашборда. | <details><summary>Контракт</summary><br>**Scope:** `dash:card_public_link:update`<br>`pubLink`* (query)<br>**Ответ:** `200` → `CardPubLink`</details> |
| <span id="ref-v1-group"></span>`POST /public/v1/boards/groups`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Group/GroupListV1) | <small>Группы карточек</small><br>Возвращает группы карточек дашборда; удалённые группы и группы удалённого дашборда исключены. | <details><summary>Контракт</summary><br>**Scope:** `dash:group:list`<br>`Take` (query), `Skip` (query)<br>JSON обязателен: `GroupFind`; поля: `boardId`<br>**Ответ:** `200` → `массив Group`</details> |
| <span id="ref-v1-inspectionfolder"></span>`POST /public/v1/inspection/folders`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/InspectionFolder/InspectionFolderListV1) | <small>Папки фотомониторинга</small><br>Возвращает папки фотомониторинга проекта по фильтру с постраничным выводом. | <details><summary>Контракт</summary><br>**Scope:** `inspection:folder:list`<br>`Take` (query), `Skip` (query)<br>JSON обязателен: `FolderFind`; поля: `projectId`<br>**Ответ:** `200` → `массив Folder`</details> |
| `POST /public/v1/inspection/folders/count`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/InspectionFolder/InspectionFolderListCountV1) | <small>Папки фотомониторинга</small><br>Подсчитывает папки фотомониторинга по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `inspection:folder:list`<br>JSON обязателен: `FolderFind`; поля: `projectId`<br>**Ответ:** `200` → `int32`</details> |
| <span id="ref-v1-plan"></span>`POST /public/v1/inspection/plans`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Plan/PlanListV1) | <small>Планы фотомониторинга</small><br>Возвращает планы фотомониторинга проекта по фильтру с постраничным выводом. | <details><summary>Контракт</summary><br>**Scope:** `inspection:plan:list`<br>`Take` (query), `Skip` (query)<br>JSON обязателен: `PlanFind`; поля: `projectId`<br>**Ответ:** `200` → `массив Plan`</details> |
| `POST /public/v1/inspection/plans/count`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Plan/PlanListCountV1) | <small>Планы фотомониторинга</small><br>Подсчитывает планы фотомониторинга по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `inspection:plan:list`<br>JSON обязателен: `PlanFind`; поля: `projectId`<br>**Ответ:** `200` → `int32`</details> |
| <span id="ref-v1-point"></span>`POST /public/v1/inspection/points`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Point/PointListV1) | <small>Точки фотомониторинга</small><br>Возвращает точки фотомониторинга проекта по фильтру с постраничным выводом. | <details><summary>Контракт</summary><br>**Scope:** `inspection:point:list`<br>`Take` (query), `Skip` (query)<br>JSON обязателен: `PointFind`; поля: `projectId`<br>**Ответ:** `200` → `массив Point`</details> |
| `POST /public/v1/inspection/points/count`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Point/PointListCountV1) | <small>Точки фотомониторинга</small><br>Подсчитывает точки фотомониторинга по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `inspection:point:list`<br>JSON обязателен: `PointFind`; поля: `projectId`<br>**Ответ:** `200` → `int32`</details> |
| `GET /public/v1/inspection/points/{pointId}`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Point/PointGetV1) | <small>Точки фотомониторинга</small><br>Возвращает точку фотомониторинга по идентификатору. | <details><summary>Контракт</summary><br>**Scope:** `inspection:point:read`<br>`pointId`* (путь)<br>**Ответ:** `200` → `Point`</details> |
| <span id="ref-v1-booking"></span>`POST /public/v1/bookings`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Booking/BookingListV1) | <small>Бронирования</small><br>Возвращает бронирования компании интеграции, упорядоченные по времени изменения и идентификатору. | <details><summary>Контракт</summary><br>**Scope:** `settings:booking:list`<br>JSON обязателен: `BookingFind`; поля: `paging`<br>**Ответ:** `200` → `массив Booking`</details> |
| `DELETE /public/v1/bookings`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Booking/BookingDeleteBatchV1) | <small>Бронирования</small><br>Удаляет указанные бронирования компании интеграции. | <details><summary>Контракт</summary><br>**Scope:** `settings:booking:delete`<br>JSON обязателен: `BookingBatchDelete`; поля: `bookingIds`<br>**Ответ:** `200` → тело не описано</details> |
| <span id="ref-v1-slot"></span>`POST /public/v1/slots`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Slot/SlotListV1) | <small>Слоты</small><br>Возвращает слоты компании интеграции, упорядоченные по началу и идентификатору. | <details><summary>Контракт</summary><br>**Scope:** `settings:slot:list`<br>JSON обязателен: `SlotFind`; поля: `paging`<br>**Ответ:** `200` → `массив Slot`</details> |
| `DELETE /public/v1/slots`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Slot/SlotDeleteBatchV1) | <small>Слоты</small><br>Удаляет указанные слоты компании интеграции. | <details><summary>Контракт</summary><br>**Scope:** `settings:slot:delete`<br>JSON обязателен: `SlotBatchDelete`; поля: `slotIds`<br>**Ответ:** `200` → тело не описано</details> |
| `POST /public/v1/slots/create-batch`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Slot/SlotCreateBatchV1) | <small>Слоты</small><br>Создаёт несколько слотов компании интеграции. | <details><summary>Контракт</summary><br>**Scope:** `settings:slot:create`<br>JSON обязателен: `SlotBatchCreate`; поля: `slots`<br>**Ответ:** `200` → `массив SlotCreateResult`</details> |

#### 3.11. Методы v2
###### 3.11. Методы v2 {#reference-v2}

В Swagger выберите схему v2. Если вы переходите с v1 на v2, сравните модели запроса и ответа для событий замечаний.

| Метод и путь | Назначение | Параметры и ответ |
| --- | --- | --- |
| `GET /public/v2/dummy/{someId}`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/Dummy/DummyGetV2) | <small>DummyItem</small><br>Возвращает объект `DummyItem` по параметру `someId`. В схеме нет текстового описания назначения запроса. | <details><summary>Контракт</summary><br>**Scope:** В схеме не указан<br>`someId`* (путь)<br>**Ответ:** `200` → `DummyItem`</details> |
| `POST /public/v2/issues/events`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/IssueEvents/IssueEventsListV2) | <small>События замечаний</small><br>Возвращает события замечаний по фильтру с постраничным выводом. | <details><summary>Контракт</summary><br>**Scope:** `docs:issue:list`<br>`Take` (query), `Skip` (query)<br>JSON обязателен: `IssueEventFind`; поля: `projectId`<br>**Ответ:** `200` → `массив IssueEventListItem`</details> |
| `POST /public/v2/issues/events/count`<br>[Схема](https://api.sgnl.pro/openapi/swagger/index.html#/IssueEvents/IssueEventsListCountV2) | <small>События замечаний</small><br>Подсчитывает события замечаний по фильтру. | <details><summary>Контракт</summary><br>**Scope:** `docs:issue:list`<br>JSON обязателен: `IssueEventFind`; поля: `projectId`<br>**Ответ:** `200` → `Int32SimpleDto`</details> |

Назначение операции с DummyItem и её scope в OpenAPI не описаны.

#### 3.12. Коды ответов
###### 3.12. Коды ответов {#reference-errors}

| Код | Значение и следующий шаг |
| --- | --- |
| 200 / 204 | Успешное выполнение. Наличие и формат тела зависят от метода. |
| 400 | Ошибка запроса. Проверьте обязательные поля, типы, UUID, ограничения массивов и ответ ValidationProblemDetails. |
| 401 | Ошибка авторизации. Проверьте заголовок Bearer и срок действия токена; получите новый токен при необходимости. |
| 403 | Доступ запрещён. Проверьте scopes токена и доступ интеграции к запрошенной операции/данным. |
| 404 | Запрошенный ресурс не найден. Проверьте идентификаторы и контекст запроса. |
| 429 | Превышена частота запросов. Дождитесь Retry-After и повторите запрос с ограничением числа попыток. |
| 450 | Достигнута квота ресурса. Для увеличения квоты обратитесь в поддержку. |
| 500 | Ошибка сервера. Сохраните время, метод, путь и код ответа для обращения в поддержку, не передавая секреты. |
| 550 | Сервис временно недоступен. Повторите чтение позднее; перед повтором записи проверьте результат предыдущей попытки. |

Точный набор кодов зависит от операции и приведён в её схеме. Для ошибок хранилища по signedUrl отдельно проверьте срок действия билета и успешность передачи файла.

Справочник и параметры примеров сверены с [OpenAPI v1](https://api.sgnl.pro/openapi/v1/schema.yml) и [OpenAPI v2](https://api.sgnl.pro/openapi/v2/schema.yml) 17 ноября 2026 года. Примеры показывают работу по опубликованному контракту; перед использованием в рабочей интеграции проверьте их со своими правами и данными.

#

<sub>**[<   SIGNAL. Что нового](/ru/general/updates)     **|**     [HUB. Введение   >](/ru/hub/intro)**</sub>
