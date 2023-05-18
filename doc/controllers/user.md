# User

Operations about user

Find out more about our store: [http://swagger.io](http://swagger.io)

```ruby
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

```ruby
def create_users_with_array_input(body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`Array<User>`](../../doc/models/user.md) | Body, Required | List of user object |

## Response Type

`void`

## Example Usage

```ruby
body = [
  User.new(
    nil,
    nil,
    nil,
    nil,
    nil,
    nil,
    nil,
    nil
  )
]

user_controller.create_users_with_array_input(body)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | successful operation | `APIException` |


# Create Users With List Input

Creates list of users with given input array

```ruby
def create_users_with_list_input(body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`Array<User>`](../../doc/models/user.md) | Body, Required | List of user object |

## Response Type

`void`

## Example Usage

```ruby
body = [
  User.new(
    nil,
    nil,
    nil,
    nil,
    nil,
    nil,
    nil,
    nil
  )
]

user_controller.create_users_with_list_input(body)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | successful operation | `APIException` |


# Get User by Name

Get user by user name

```ruby
def get_user_by_name(username)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `String` | Template, Required | The name that needs to be fetched. Use user1 for testing. |

## Response Type

[`User`](../../doc/models/user.md)

## Example Usage

```ruby
username = 'username0'

result = user_controller.get_user_by_name(username)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid username supplied | `APIException` |
| 404 | User not found | `APIException` |


# Update User

This can only be done by the logged in user.

```ruby
def update_user(username,
                body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `String` | Template, Required | name that need to be updated |
| `body` | [`User`](../../doc/models/user.md) | Body, Required | Updated user object |

## Response Type

`void`

## Example Usage

```ruby
username = 'username0'

body = User.new(
  nil,
  nil,
  nil,
  nil,
  nil,
  nil,
  nil,
  nil
)

user_controller.update_user(
  username,
  body
)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid user supplied | `APIException` |
| 404 | User not found | `APIException` |


# Delete User

This can only be done by the logged in user.

```ruby
def delete_user(username)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `String` | Template, Required | The name that needs to be deleted |

## Response Type

`void`

## Example Usage

```ruby
username = 'username0'

user_controller.delete_user(username)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid username supplied | `APIException` |
| 404 | User not found | `APIException` |


# Login User

Logs user into the system

```ruby
def login_user(username,
               password)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `String` | Query, Required | The user name for login |
| `password` | `String` | Query, Required | The password for login in clear text |

## Response Type

`String`

## Example Usage

```ruby
username = 'username0'

password = 'password4'

result = user_controller.login_user(
  username,
  password
)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid username/password supplied | `APIException` |


# Logout User

Logs out current logged in user session

```ruby
def logout_user
```

## Response Type

`void`

## Example Usage

```ruby
user_controller.logout_user
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | successful operation | `APIException` |


# Create User

This can only be done by the logged in user.

```ruby
def create_user(body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`User`](../../doc/models/user.md) | Body, Required | Created user object |

## Response Type

`void`

## Example Usage

```ruby
body = User.new(
  nil,
  nil,
  nil,
  nil,
  nil,
  nil,
  nil,
  nil
)

user_controller.create_user(body)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | successful operation | `APIException` |

