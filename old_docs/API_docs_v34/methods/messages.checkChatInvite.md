---
title: messages.checkChatInvite
description: Check the validity of a chat invite link and get basic info about it
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_checkChatInvite.html
---
# Method: messages.checkChatInvite
[Back to methods index](index.md)



Check the validity of a chat invite link and get basic info about it

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|hash|[string](../types/string.md) | Invite hash in `t.me/joinchat/hash` | Yes|


### Return type: [ChatInvite](../types/ChatInvite.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$ChatInvite = $MadelineProto->messages->checkChatInvite(['hash' => 'string', ]);
```

Or, if you're into Lua:

```lua
ChatInvite = messages.checkChatInvite({hash='string', })
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|INVITE_HASH_EMPTY|The invite hash is empty|
|400|INVITE_HASH_EXPIRED|The invite link has expired|
|400|INVITE_HASH_INVALID|The invite hash is invalid|
|406|AUTH_KEY_DUPLICATED|An auth key with the same ID was already generated|
|401|SESSION_PASSWORD_NEEDED|2FA is enabled, use a password to login|


