---
title: phone.requestCall
description: Start a telegram phone call
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/phone_requestCall.html
---
# Method: phone.requestCall
[Back to methods index](index.md)



Start a telegram phone call

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|user\_id|[Username, chat ID, Update, Message or InputUser](../types/InputUser.md) | Destination of the phone call | Optional|
|g\_a\_hash|[bytes](../types/bytes.md) | [Parameter for E2E encryption key exchange »](https://core.telegram.org/api/end-to-end/voice-calls) | Yes|
|protocol|[PhoneCallProtocol](../types/PhoneCallProtocol.md) | Phone call settings | Yes|


### Return type: [phone.PhoneCall](../types/phone.PhoneCall.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$phone.PhoneCall = $MadelineProto->phone->requestCall(['user_id' => InputUser, 'g_a_hash' => 'bytes', 'protocol' => PhoneCallProtocol, ]);
```

Or, if you're into Lua:

```lua
phone.PhoneCall = phone.requestCall({user_id=InputUser, g_a_hash='bytes', protocol=PhoneCallProtocol, })
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|CALL_PROTOCOL_FLAGS_INVALID|Call protocol flags invalid|
|400|PARTICIPANT_VERSION_OUTDATED|The other participant does not use an up to date telegram client with support for calls|
|400|USER_ID_INVALID|The provided user ID is invalid|
|403|USER_IS_BLOCKED|You were blocked by this user|
|403|USER_PRIVACY_RESTRICTED|The user's privacy settings do not allow you to do this|


