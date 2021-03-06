---
title: updateNewAuthorization
description: updateNewAuthorization attributes, type and example
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: updateNewAuthorization  
[Back to constructors index](index.md)



### Attributes:

| Name     |    Type       | Required |
|----------|---------------|----------|
|auth\_key\_id|[long](../types/long.md) | Yes|
|date|[int](../types/int.md) | Yes|
|device|[string](../types/string.md) | Yes|
|location|[string](../types/string.md) | Yes|



### Type: [Update](../types/Update.md)


### Example:

```php
$updateNewAuthorization = ['_' => 'updateNewAuthorization', 'auth_key_id' => long, 'date' => int, 'device' => 'string', 'location' => 'string'];
```  


Or, if you're into Lua:

```lua
updateNewAuthorization={_='updateNewAuthorization', auth_key_id=long, date=int, device='string', location='string'}

```


