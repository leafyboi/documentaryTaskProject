# API v1.0.0

BASE_URL  http://host1819712.hostland.pro/api

## Registration

[<-- Back to Table Of Contents](#table-of-contents)

|attribute        |value         	      |
|----------------	|-------------------	|
| request method 	| POST              	|
| route          	| BASE_URL/register 	|
| error types    	| EmailError          |

#### REQUEST DATA

```json
{
    "email": "example@mail.com",
    "name": "Ivan",
    "password": "somepassword",
    "password_confirmation": "somepassword",
}
```
#### RESPONSE DATA [SUCCESS]

```json
{ 
    "message": "Регистрация прошла успешно. Вы были перенаправлены на страницу авторизации.",
}
```

#### RESPONSE DATA [FAIL]

>*Note*: 1) Возвращаются только найденные ошибки

```json
{
    "message": "Указанные данные введены неверно.",
    "errors": {
        "email": [
            "Пользователь с таким email уже зарегистрирован."
        ],
        "password": [
            "Поле пароль не совпадает с полем подтверждения."
        ]
    }
}
```

## Authorization

[<-- Back to Table Of Contents](#table-of-contents)

|attribute        |value         	      |
|----------------	|-------------------	|
| request method 	| POST              	|
| route          	| BASE_URL/login    	|
| error types    	| EmailError, PasswordError|

#### REQUEST DATA

```json
{
    "email": "example@mail.com",
    "password": "userpassword"
}
```
#### RESPONSE DATA [SUCCESS]


```json
{
    "token": "access_token_here",
    "user": {
        "id": 67,
        "email": "example@mail.com",
        "name": "Ivan",
        "surname": "Ivanov"
    }
}
```
#### RESPONSE DATA [FAIL]

>*Note*: 1) Возвращаются только найденные ошибки

```json
{
    "message": "Не удаётся войти. Неверный логин или пароль."
}
```

## Logout

[<-- Back to Table Of Contents](#table-of-contents)

|attribute          |value         	        |
|----------------	|-------------------	|
| request method 	| POST              	|
| route          	| BASE_URL/logout    	|
| required headers  | Authorization         |

>*Note*: Формально логаут это удаление токена, т.е. никакие дополнительные данные не нужны. Токен будет в приведенном хэдере запроса. 

#### RESPONSE DATA [SUCCESS]

```json
{ 
    "message": "Вы успешно вышли из системы.",
}
```

