---
title: messageActionGeoChatCreate
description: messageActionGeoChatCreate attributes, type and example
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: messageActionGeoChatCreate  
[Back to constructors index](index.md)



### Attributes:

| Name     |    Type       | Required |
|----------|---------------|----------|
|title|[string](../types/string.md) | Yes|
|address|[string](../types/string.md) | Yes|



### Type: [MessageAction](../types/MessageAction.md)


### Example:

```php
$messageActionGeoChatCreate = ['_' => 'messageActionGeoChatCreate', 'title' => 'string', 'address' => 'string'];
```  


Or, if you're into Lua:

```lua
messageActionGeoChatCreate={_='messageActionGeoChatCreate', title='string', address='string'}

```


