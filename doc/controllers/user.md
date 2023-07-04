# User

Operations about user

Find out more about our store: [http://swagger.io](http://swagger.io)

```python
user_controller = client.user
```

## Class Name

`UserController`

## Methods

* [Create Users With Array Input](../../doc/controllers/user.md#create-users-with-array-input)
* [Create Users With List Input](../../doc/controllers/user.md#create-users-with-list-input)
* [Get User by Name](../../doc/controllers/user.md#get-user-by-name)
* [Update User](../../doc/controllers/user.md#update-user)
* [Delete User](../../doc/controllers/user.md#delete-user)
* [Login User](../../doc/controllers/user.md#login-user)
* [Logout User](../../doc/controllers/user.md#logout-user)
* [Create User](../../doc/controllers/user.md#create-user)


# Create Users With Array Input

Creates list of users with given input array

```python
def create_users_with_array_input(self,
                                 body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`List of User`](../../doc/models/user.md) | Body, Required | List of user object |

## Response Type

`void`

## Example Usage

```python
body = [
    User()
]

result = user_controller.create_users_with_array_input(body)
print(result)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | successful operation | `APIException` |


# Create Users With List Input

Creates list of users with given input array

```python
def create_users_with_list_input(self,
                                body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`List of User`](../../doc/models/user.md) | Body, Required | List of user object |

## Response Type

`void`

## Example Usage

```python
body = [
    User()
]

result = user_controller.create_users_with_list_input(body)
print(result)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | successful operation | `APIException` |


# Get User by Name

Get user by user name

```python
def get_user_by_name(self,
                    username)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `string` | Template, Required | The name that needs to be fetched. Use user1 for testing. |

## Response Type

[`User`](../../doc/models/user.md)

## Example Usage

```python
username = 'username0'

result = user_controller.get_user_by_name(username)
print(result)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid username supplied | `APIException` |
| 404 | User not found | `APIException` |


# Update User

This can only be done by the logged in user.

```python
def update_user(self,
               username,
               body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `string` | Template, Required | name that need to be updated |
| `body` | [`User`](../../doc/models/user.md) | Body, Required | Updated user object |

## Response Type

`void`

## Example Usage

```python
username = 'username0'

body = User()

result = user_controller.update_user(
    username,
    body
)
print(result)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid user supplied | `APIException` |
| 404 | User not found | `APIException` |


# Delete User

This can only be done by the logged in user.

```python
def delete_user(self,
               username)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `string` | Template, Required | The name that needs to be deleted |

## Response Type

`void`

## Example Usage

```python
username = 'username0'

result = user_controller.delete_user(username)
print(result)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid username supplied | `APIException` |
| 404 | User not found | `APIException` |


# Login User

Logs user into the system

```python
def login_user(self,
              username,
              password)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `string` | Query, Required | The user name for login |
| `password` | `string` | Query, Required | The password for login in clear text |

## Response Type

`string`

## Example Usage

```python
username = 'username0'

password = 'password4'

result = user_controller.login_user(
    username,
    password
)
print(result)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid username/password supplied | `APIException` |


# Logout User

Logs out current logged in user session

```python
def logout_user(self)
```

## Response Type

`void`

## Example Usage

```python
result = user_controller.logout_user()
print(result)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | successful operation | `APIException` |


# Create User

This can only be done by the logged in user.

```python
def create_user(self,
               body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`User`](../../doc/models/user.md) | Body, Required | Created user object |

## Response Type

`void`

## Example Usage

```python
body = User()

result = user_controller.create_user(body)
print(result)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | successful operation | `APIException` |

