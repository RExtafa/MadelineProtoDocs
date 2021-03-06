---
title: messages.getSearchCounters
description: Get the number of results that would be found by a [messages.search](../methods/messages.search.md) call with the same parameters
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_getSearchCounters.html
---
# Method: messages.getSearchCounters  
[Back to methods index](index.md)


Get the number of results that would be found by a [messages.search](../methods/messages.search.md) call with the same parameters

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](../types/InputPeer.md) | Peer where to search | Optional|
|filters|Array of [MessagesFilter](../types/MessagesFilter.md) | Filters | Yes|


### Return type: [Vector\_of\_messages.SearchCounter](../types/messages.SearchCounter.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Vector_of_messages.SearchCounter = $MadelineProto->messages->getSearchCounters(['peer' => InputPeer, 'filters' => [MessagesFilter, MessagesFilter], ]);
```

Or, if you're into Lua:

```lua
Vector_of_messages.SearchCounter = messages.getSearchCounters({peer=InputPeer, filters={MessagesFilter}, })
```

