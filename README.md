# Messages
Створити сервіс коротких (404 символи) заміток (із тегами) для кожного користувача із можливістю перегляду, редагування і видалення, а також надавати доступ редагувати замітку іншими користувачами (до 5 користувачів). Також надати можливість бачити статистику користувача, скільки повідомлень, коли редаговані і ким. .

## Version: 1.0

**Contact information:**  
Oleksii Havryshkiv  
wogy.wogy14@gmail.com  

### /users

#### GET
##### Summary:

Отримання даних про користувачів

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Об'єкт користувача | [User](#user) |

#### POST
##### Summary:

Створення нового користувача

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body | Об'єкт користувача | Yes | [User](#user) |
| api_key | header | індивідуальний ключ користувача | Yes | string |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Об'єкт користувача | [User](#user) |
| 400 | Bad data |  |
| 401 | Unauthorized |  |
| 406 | Not Acceptable |  |

### /users/{id}

#### GET
##### Summary:

Отримання даних про користувача

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | унікальний ідентифікатор | Yes | integer |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Об'єкт користувача | [User](#user) |
| 404 | Not Found |  |

#### PUT
##### Summary:

Оновлення даних

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | унікальний ідентифікатор | Yes | integer |
| body | body | Об'єкт користувача | Yes | [User](#user) |
| api_key | header | індивідуальний ключ користувача | Yes | string |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Об'єкт користувача | [User](#user) |
| 400 | Bad data |  |
| 401 | Unauthorized |  |
| 404 | Not Found |  |
| 406 | Not Acceptable |  |

#### DELETE
##### Summary:

Видалення користувача

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | унікальний ідентифікатор | Yes | integer |
| api_key | header | індивідуальний ключ користувача | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Успішне видалення |
| 401 | Unauthorized |
| 404 | Not Found |
| 406 | Not Acceptable |

### /messages

#### GET
##### Summary:

Отримання повідомлень

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Об'єкт повідомлення | [Message](#message) |

#### POST
##### Summary:

Створення нового повідомлення

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body | Об'єкт повідомлення | Yes | [Message](#message) |
| api_key | header | індивідуальний ключ користувача | Yes | string |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Об'єкт повідомлення | [Message](#message) |
| 400 | Bad data |  |
| 401 | Unauthorized |  |
| 406 | Not Acceptable |  |

### /messages/{id}

#### GET
##### Summary:

Отримання даних про повідомлення

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | унікальний ідентифікатор | Yes | integer |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Об'єкт повідомлення | [Message](#message) |
| 404 | Not Found |  |

#### PUT
##### Summary:

Оновлення даних

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | унікальний ідентифікатор | Yes | integer |
| body | body | Об'єкт повідомлення | Yes | [Message](#message) |
| api_key | header | індивідуальний ключ користувача | Yes | string |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Об'єкт повідомлення | [Message](#message) |
| 400 | Bad data |  |
| 401 | Unauthorized |  |
| 404 | Not Found |  |
| 406 | Not Acceptable |  |

#### DELETE
##### Summary:

Видалення повідомлення

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | унікальний ідентифікатор | Yes | integer |
| api_key | header | індивідуальний ключ користувача | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Успішне видалення |
| 401 | Unauthorized |
| 404 | Not Found |
| 406 | Not Acceptable |

### Models


#### User

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | long |  | No |
| name | string |  | No |
| count_messages | long |  | No |

#### Message

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | long |  | No |
| creator_id | long |  | No |
| date | dateTime |  | No |
| text | string |  | No |
| tags | string |  | No |
