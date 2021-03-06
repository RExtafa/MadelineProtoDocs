---
title: phone.setCallRating
description: Rate a call
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/phone_setCallRating.html
---
# Method: phone.setCallRating
[Back to methods index](index.md)



Rate a call

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[InputPhoneCall](../types/InputPhoneCall.md) | The call to rate | Yes|
|rating|[int](../types/int.md) | Rating in `1-5` stars | Yes|
|comment|[string](../types/string.md) | An additional comment | Yes|


### Return type: [Updates](../types/Updates.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Updates = $MadelineProto->phone->setCallRating(['peer' => InputPhoneCall, 'rating' => int, 'comment' => 'string', ]);
```

Or, if you're into Lua:

```lua
Updates = phone.setCallRating({peer=InputPhoneCall, rating=int, comment='string', })
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|CALL_PEER_INVALID|The provided call peer object is invalid|


