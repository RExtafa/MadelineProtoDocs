---
title: auth.authorization
description: Contains user authorization info.
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/constructors/auth_authorization.html
---
# Constructor: auth.authorization  
[Back to constructors index](index.md)



Contains user authorization info.

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|tmp\_sessions|[int](../types/int.md) | Optional|Temporary [passport](https://core.telegram.org/passport) sessions|
|user|[User](../types/User.md) | Optional|Info on authorized user|



### Type: [auth.Authorization](../types/auth.Authorization.md)


### Example:

```php
$auth.authorization = ['_' => 'auth.authorization', 'tmp_sessions' => int, 'user' => User];
```  


Or, if you're into Lua:

```lua
auth.authorization={_='auth.authorization', tmp_sessions=int, user=User}

```


