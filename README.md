Messages
========

Створити сервіс коротких (404 символи) заміток (із тегами) для кожного
користувача із можливістю перегляду, редагування і видалення, а також
надавати доступ редагувати замітку іншими користувачами (до 5
користувачів). Також надати можливість бачити статистику користувача,
скільки повідомлень, коли редаговані і ким. .

More information: [https://helloreverb.com](https://helloreverb.com)

Contact Info: [wogy.wogy14@gmail.com](wogy.wogy14@gmail.com)

Version: 1.0

BasePath:/api/v1.0/

All rights reserved

http://apache.org/licenses/LICENSE-2.0.html

Access
------

Methods
-------

[ Jump to [Models](#__Models) ]

### Table of Contents

#### [Messages](#Messages)

-   [`get /messages`](#messagesGet)
-   [`delete /messages/{id}`](#messagesIdDelete)
-   [`get /messages/{id}`](#messagesIdGet)
-   [`put /messages/{id}`](#messagesIdPut)
-   [`post /messages`](#messagesPost)

#### [Users](#Users)

-   [`get /users`](#usersGet)
-   [`delete /users/{id}`](#usersIdDelete)
-   [`get /users/{id}`](#usersIdGet)
-   [`put /users/{id}`](#usersIdPut)
-   [`post /users`](#usersPost)

Messages
========

[Up](#__Methods)

``` {.get}
get /messages
```

Отримання повідомлень (messagesGet)

### Return type {.field-label}

[Message](#Message)

### Example data {.field-label}

Content-Type: application/json

``` {.example}
{
  "date" : "2000-01-23T04:56:07.000+00:00",
  "creator_id" : 6,
  "id" : 0,
  "text" : "text",
  "tags" : "tags"
}
```

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

Об'єкт повідомлення [Message](#Message)

* * * * *

[Up](#__Methods)

``` {.delete}
delete /messages/{id}
```

Видалення повідомлення (messagesIdDelete)

### Path parameters {.field-label}

id (required)

Path Parameter — унікальний ідентифікатор

### Request headers {.field-label}

### Responses {.field-label}

#### 200 {.field-label}

Успішне видалення [](#)

#### 401 {.field-label}

Unauthorized [](#)

#### 404 {.field-label}

Not Found [](#)

#### 406 {.field-label}

Not Acceptable [](#)

* * * * *

[Up](#__Methods)

``` {.get}
get /messages/{id}
```

Отримання даних про повідомлення (messagesIdGet)

### Path parameters {.field-label}

id (required)

Path Parameter — унікальний ідентифікатор

### Return type {.field-label}

[Message](#Message)

### Example data {.field-label}

Content-Type: application/json

``` {.example}
{
  "date" : "2000-01-23T04:56:07.000+00:00",
  "creator_id" : 6,
  "id" : 0,
  "text" : "text",
  "tags" : "tags"
}
```

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

Об'єкт повідомлення [Message](#Message)

#### 404 {.field-label}

Not Found [](#)

* * * * *

[Up](#__Methods)

``` {.put}
put /messages/{id}
```

Оновлення даних (messagesIdPut)

### Path parameters {.field-label}

id (required)

Path Parameter — унікальний ідентифікатор

### Consumes {.field-label}

This API call consumes the following media types via the Content-Type
request header:

-   `application/json`

### Request body {.field-label}

body [Message](#Message) (required)

Body Parameter — Об'єкт повідомлення

### Request headers {.field-label}

### Return type {.field-label}

[Message](#Message)

### Example data {.field-label}

Content-Type: application/json

``` {.example}
{
  "date" : "2000-01-23T04:56:07.000+00:00",
  "creator_id" : 6,
  "id" : 0,
  "text" : "text",
  "tags" : "tags"
}
```

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

Об'єкт повідомлення [Message](#Message)

#### 400 {.field-label}

Bad data [](#)

#### 401 {.field-label}

Unauthorized [](#)

#### 404 {.field-label}

Not Found [](#)

#### 406 {.field-label}

Not Acceptable [](#)

* * * * *

[Up](#__Methods)

``` {.post}
post /messages
```

Створення нового повідомлення (messagesPost)

### Consumes {.field-label}

This API call consumes the following media types via the Content-Type
request header:

-   `application/json`

### Request body {.field-label}

body [Message](#Message) (required)

Body Parameter — Об'єкт повідомлення

### Request headers {.field-label}

### Return type {.field-label}

[Message](#Message)

### Example data {.field-label}

Content-Type: application/json

``` {.example}
{
  "date" : "2000-01-23T04:56:07.000+00:00",
  "creator_id" : 6,
  "id" : 0,
  "text" : "text",
  "tags" : "tags"
}
```

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

Об'єкт повідомлення [Message](#Message)

#### 400 {.field-label}

Bad data [](#)

#### 401 {.field-label}

Unauthorized [](#)

#### 406 {.field-label}

Not Acceptable [](#)

* * * * *

Users
=====

[Up](#__Methods)

``` {.get}
get /users
```

Отримання даних про користувачів (usersGet)

### Return type {.field-label}

[User](#User)

### Example data {.field-label}

Content-Type: application/json

``` {.example}
{
  "count_messages" : 6,
  "name" : "name",
  "id" : 0
}
```

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

Об'єкт користувача [User](#User)

* * * * *

[Up](#__Methods)

``` {.delete}
delete /users/{id}
```

Видалення користувача (usersIdDelete)

### Path parameters {.field-label}

id (required)

Path Parameter — унікальний ідентифікатор

### Request headers {.field-label}

### Responses {.field-label}

#### 200 {.field-label}

Успішне видалення [](#)

#### 401 {.field-label}

Unauthorized [](#)

#### 404 {.field-label}

Not Found [](#)

#### 406 {.field-label}

Not Acceptable [](#)

* * * * *

[Up](#__Methods)

``` {.get}
get /users/{id}
```

Отримання даних про користувача (usersIdGet)

### Path parameters {.field-label}

id (required)

Path Parameter — унікальний ідентифікатор

### Return type {.field-label}

[User](#User)

### Example data {.field-label}

Content-Type: application/json

``` {.example}
{
  "count_messages" : 6,
  "name" : "name",
  "id" : 0
}
```

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

Об'єкт користувача [User](#User)

#### 404 {.field-label}

Not Found [](#)

* * * * *

[Up](#__Methods)

``` {.put}
put /users/{id}
```

Оновлення даних (usersIdPut)

### Path parameters {.field-label}

id (required)

Path Parameter — унікальний ідентифікатор

### Consumes {.field-label}

This API call consumes the following media types via the Content-Type
request header:

-   `application/json`

### Request body {.field-label}

body [User](#User) (required)

Body Parameter — Об'єкт користувача

### Request headers {.field-label}

### Return type {.field-label}

[User](#User)

### Example data {.field-label}

Content-Type: application/json

``` {.example}
{
  "count_messages" : 6,
  "name" : "name",
  "id" : 0
}
```

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

Об'єкт користувача [User](#User)

#### 400 {.field-label}

Bad data [](#)

#### 401 {.field-label}

Unauthorized [](#)

#### 404 {.field-label}

Not Found [](#)

#### 406 {.field-label}

Not Acceptable [](#)

* * * * *

[Up](#__Methods)

``` {.post}
post /users
```

Створення нового користувача (usersPost)

### Consumes {.field-label}

This API call consumes the following media types via the Content-Type
request header:

-   `application/json`

### Request body {.field-label}

body [User](#User) (required)

Body Parameter — Об'єкт користувача

### Request headers {.field-label}

### Return type {.field-label}

[User](#User)

### Example data {.field-label}

Content-Type: application/json

``` {.example}
{
  "count_messages" : 6,
  "name" : "name",
  "id" : 0
}
```

### Produces {.field-label}

This API call produces the following media types according to the Accept
request header; the media type will be conveyed by the Content-Type
response header.

-   `application/json`

### Responses {.field-label}

#### 200 {.field-label}

Об'єкт користувача [User](#User)

#### 400 {.field-label}

Bad data [](#)

#### 401 {.field-label}

Unauthorized [](#)

#### 406 {.field-label}

Not Acceptable [](#)

* * * * *

Models
------

[ Jump to [Methods](#__Methods) ]

### Table of Contents

1.  [`Message`](#Message)
2.  [`User`](#User)

### `Message` [Up](#__Models)

id (optional)

[Long](#long) format: int64

creator\_id (optional)

[Long](#long) format: int64

date (optional)

[Date](#DateTime) format: date-time

text (optional)

[String](#string)

tags (optional)

[String](#string)

### `User` [Up](#__Models)

id (optional)

[Long](#long) format: int64

name (optional)

[String](#string)

count\_messages (optional)

[Long](#long) format: int64
