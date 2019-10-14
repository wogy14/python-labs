# Messages

<div class="app-desc">Створити сервіс коротких (404 символи) заміток (із тегами) для кожного користувача із можливістю перегляду, редагування і видалення, а також надавати доступ редагувати замітку іншими користувачами (до 5 користувачів). Також надати можливість бачити статистику користувача, скільки повідомлень, коли редаговані і ким. .</div>

<div class="app-desc">More information: [https://helloreverb.com](https://helloreverb.com)</div>

<div class="app-desc">Contact Info: [wogy.wogy14@gmail.com](wogy.wogy14@gmail.com)</div>

<div class="app-desc">Version: 1.0</div>

<div class="app-desc">BasePath:/api/v1.0/</div>

<div class="license-info">All rights reserved</div>

<div class="license-url">http://apache.org/licenses/LICENSE-2.0.html</div>

## Access ## <a name="__Methods">Methods</a> [ Jump to [Models](#__Models) ] ### Table of Contents #### [Messages](#Messages) * [`<span class="http-method">get</span> /messages`](#messagesGet) * [`<span class="http-method">delete</span> /messages/{id}`](#messagesIdDelete) * [`<span class="http-method">get</span> /messages/{id}`](#messagesIdGet) * [`<span class="http-method">put</span> /messages/{id}`](#messagesIdPut) * [`<span class="http-method">post</span> /messages`](#messagesPost) #### [Users](#Users) * [`<span class="http-method">get</span> /users`](#usersGet) * [`<span class="http-method">delete</span> /users/{id}`](#usersIdDelete) * [`<span class="http-method">get</span> /users/{id}`](#usersIdGet) * [`<span class="http-method">put</span> /users/{id}`](#usersIdPut) * [`<span class="http-method">post</span> /users`](#usersPost) # <a name="Messages">Messages</a>

<div class="method"><a name="messagesGet"></a>

<div class="method-path">[Up](#__Methods) get /messages</div>

<div class="method-summary">Отримання повідомлень (<span class="nickname">messagesGet</span>)</div>

### Return type

<div class="return-type">[Message](#Message)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

{ "date" : "2000-01-23T04:56:07.000+00:00", "creator_id" : 6, "id" : 0, "text" : "text", "tags" : "tags" } ### Produces This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header. * `application/json` ### Responses #### 200 Об'єкт повідомлення [Message](#Message)</div>

* * *

<div class="method"><a name="messagesIdDelete"></a>

<div class="method-path">[Up](#__Methods) delete /messages/{id}</div>

<div class="method-summary">Видалення повідомлення (<span class="nickname">messagesIdDelete</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">id (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — унікальний ідентифікатор</div>

</div>

### Request headers ### Responses #### 200 Успішне видалення[](#) #### 401 Unauthorized[](#) #### 404 Not Found[](#) #### 406 Not Acceptable[](#)</div>

* * *

<div class="method"><a name="messagesIdGet"></a>

<div class="method-path">[Up](#__Methods) get /messages/{id}</div>

<div class="method-summary">Отримання даних про повідомлення (<span class="nickname">messagesIdGet</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">id (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — унікальний ідентифікатор</div>

</div>

### Return type

<div class="return-type">[Message](#Message)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

{ "date" : "2000-01-23T04:56:07.000+00:00", "creator_id" : 6, "id" : 0, "text" : "text", "tags" : "tags" } ### Produces This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header. * `application/json` ### Responses #### 200 Об'єкт повідомлення [Message](#Message) #### 404 Not Found[](#)</div>

* * *

<div class="method"><a name="messagesIdPut"></a>

<div class="method-path">[Up](#__Methods) put /messages/{id}</div>

<div class="method-summary">Оновлення даних (<span class="nickname">messagesIdPut</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">id (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — унікальний ідентифікатор</div>

</div>

### Consumes This API call consumes the following media types via the <span class="header">Content-Type</span> request header: * `application/json` ### Request body

<div class="field-items">

<div class="param">body [Message](#Message) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Об'єкт повідомлення</div>

</div>

### Request headers ### Return type

<div class="return-type">[Message](#Message)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

{ "date" : "2000-01-23T04:56:07.000+00:00", "creator_id" : 6, "id" : 0, "text" : "text", "tags" : "tags" } ### Produces This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header. * `application/json` ### Responses #### 200 Об'єкт повідомлення [Message](#Message) #### 400 Bad data[](#) #### 401 Unauthorized[](#) #### 404 Not Found[](#) #### 406 Not Acceptable[](#)</div>

* * *

<div class="method"><a name="messagesPost"></a>

<div class="method-path">[Up](#__Methods) post /messages</div>

<div class="method-summary">Створення нового повідомлення (<span class="nickname">messagesPost</span>)</div>

### Consumes This API call consumes the following media types via the <span class="header">Content-Type</span> request header: * `application/json` ### Request body

<div class="field-items">

<div class="param">body [Message](#Message) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Об'єкт повідомлення</div>

</div>

### Request headers ### Return type

<div class="return-type">[Message](#Message)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

{ "date" : "2000-01-23T04:56:07.000+00:00", "creator_id" : 6, "id" : 0, "text" : "text", "tags" : "tags" } ### Produces This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header. * `application/json` ### Responses #### 200 Об'єкт повідомлення [Message](#Message) #### 400 Bad data[](#) #### 401 Unauthorized[](#) #### 406 Not Acceptable[](#)</div>

* * * # <a name="Users">Users</a>

<div class="method"><a name="usersGet"></a>

<div class="method-path">[Up](#__Methods) get /users</div>

<div class="method-summary">Отримання даних про користувачів (<span class="nickname">usersGet</span>)</div>

### Return type

<div class="return-type">[User](#User)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

{ "count_messages" : 6, "name" : "name", "id" : 0 } ### Produces This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header. * `application/json` ### Responses #### 200 Об'єкт користувача [User](#User)</div>

* * *

<div class="method"><a name="usersIdDelete"></a>

<div class="method-path">[Up](#__Methods) delete /users/{id}</div>

<div class="method-summary">Видалення користувача (<span class="nickname">usersIdDelete</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">id (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — унікальний ідентифікатор</div>

</div>

### Request headers ### Responses #### 200 Успішне видалення[](#) #### 401 Unauthorized[](#) #### 404 Not Found[](#) #### 406 Not Acceptable[](#)</div>

* * *

<div class="method"><a name="usersIdGet"></a>

<div class="method-path">[Up](#__Methods) get /users/{id}</div>

<div class="method-summary">Отримання даних про користувача (<span class="nickname">usersIdGet</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">id (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — унікальний ідентифікатор</div>

</div>

### Return type

<div class="return-type">[User](#User)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

{ "count_messages" : 6, "name" : "name", "id" : 0 } ### Produces This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header. * `application/json` ### Responses #### 200 Об'єкт користувача [User](#User) #### 404 Not Found[](#)</div>

* * *

<div class="method"><a name="usersIdPut"></a>

<div class="method-path">[Up](#__Methods) put /users/{id}</div>

<div class="method-summary">Оновлення даних (<span class="nickname">usersIdPut</span>)</div>

### Path parameters

<div class="field-items">

<div class="param">id (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> — унікальний ідентифікатор</div>

</div>

### Consumes This API call consumes the following media types via the <span class="header">Content-Type</span> request header: * `application/json` ### Request body

<div class="field-items">

<div class="param">body [User](#User) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Об'єкт користувача</div>

</div>

### Request headers ### Return type

<div class="return-type">[User](#User)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

{ "count_messages" : 6, "name" : "name", "id" : 0 } ### Produces This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header. * `application/json` ### Responses #### 200 Об'єкт користувача [User](#User) #### 400 Bad data[](#) #### 401 Unauthorized[](#) #### 404 Not Found[](#) #### 406 Not Acceptable[](#)</div>

* * *

<div class="method"><a name="usersPost"></a>

<div class="method-path">[Up](#__Methods) post /users</div>

<div class="method-summary">Створення нового користувача (<span class="nickname">usersPost</span>)</div>

### Consumes This API call consumes the following media types via the <span class="header">Content-Type</span> request header: * `application/json` ### Request body

<div class="field-items">

<div class="param">body [User](#User) (required)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> — Об'єкт користувача</div>

</div>

### Request headers ### Return type

<div class="return-type">[User](#User)</div>

### Example data

<div class="example-data-content-type">Content-Type: application/json</div>

{ "count_messages" : 6, "name" : "name", "id" : 0 } ### Produces This API call produces the following media types according to the <span class="header">Accept</span> request header; the media type will be conveyed by the <span class="header">Content-Type</span> response header. * `application/json` ### Responses #### 200 Об'єкт користувача [User](#User) #### 400 Bad data[](#) #### 401 Unauthorized[](#) #### 406 Not Acceptable[](#)</div>

* * * ## <a name="__Models">Models</a> [ Jump to [Methods](#__Methods) ] ### Table of Contents 1\. [`Message`](#Message) 2\. [`User`](#User)

<div class="model">### <a name="Message">`Message`</a> [Up](#__Models)

<div class="field-items">

<div class="param">id (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">creator_id (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">date (optional)</div>

<div class="param-desc"><span class="param-type">[Date](#DateTime)</span> format: date-time</div>

<div class="param">text (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">tags (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

</div>

</div>

<div class="model">### <a name="User">`User`</a> [Up](#__Models)

<div class="field-items">

<div class="param">id (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

<div class="param">name (optional)</div>

<div class="param-desc"><span class="param-type">[String](#string)</span></div>

<div class="param">count_messages (optional)</div>

<div class="param-desc"><span class="param-type">[Long](#long)</span> format: int64</div>

</div>

</div>
