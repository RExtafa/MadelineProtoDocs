---
title: messages.sendMessage
description: Sends a message to a chat
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_sendMessage.html
---
# Method: messages.sendMessage
[Back to methods index](index.md)



Sends a message to a chat

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](../types/InputPeer.md) | The destination where the message will be sent | Optional|
|message|[string](../types/string.md) | The message | Yes|


### Return type: [messages.SentMessage](../types/messages.SentMessage.md)

### Can bots use this method: **YES**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages.SentMessage = $MadelineProto->messages->sendMessage(['peer' => InputPeer, 'message' => 'string', ]);
```

Or, if you're into Lua:

```lua
messages.SentMessage = messages.sendMessage({peer=InputPeer, message='string', })
```


## Return value 

If the length of the provided message is bigger than 4096, the message will be split in chunks and the method will be called multiple times, with the same parameters (except for the message), and an array of [messages.SentMessage](../types/messages.SentMessage.md) will be returned instead.


### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|BOT_DOMAIN_INVALID|Bot domain invalid|
|400|BOT_INVALID|This is not a valid bot|
|400|BUTTON_DATA_INVALID|The data of one or more of the buttons you provided is invalid|
|400|BUTTON_TYPE_INVALID|The type of one or more of the buttons you provided is invalid|
|400|BUTTON_URL_INVALID|Button URL invalid|
|400|CHANNEL_INVALID|The provided channel is invalid|
|400|CHANNEL_PRIVATE|You haven't joined this channel/supergroup|
|400|CHAT_ADMIN_REQUIRED|You must be an admin in this chat to do this|
|400|CHAT_ID_INVALID|The provided chat id is invalid|
|400|CHAT_RESTRICTED|You can't send messages in this chat, you were restricted|
|400|ENCRYPTION_DECLINED|The secret chat was declined|
|400|ENTITY_MENTION_USER_INVALID|You mentioned an invalid user|
|400|FROM_MESSAGE_BOT_DISABLED|Bots can't use fromMessage min constructors|
|400|INPUT_USER_DEACTIVATED|The specified user was deleted|
|400|MESSAGE_EMPTY|The provided message is empty|
|400|MESSAGE_TOO_LONG|The provided message is too long|
|400|MSG_ID_INVALID|Invalid message ID provided|
|400|PEER_ID_INVALID|The provided peer id is invalid|
|400|PINNED_DIALOGS_TOO_MUCH|Too many pinned dialogs|
|400|REPLY_MARKUP_INVALID|The provided reply markup is invalid|
|400|SCHEDULE_BOT_NOT_ALLOWED|Bots cannot schedule messages|
|400|SCHEDULE_TOO_MUCH|There are too many scheduled messages|
|400|USER_BANNED_IN_CHANNEL|You're banned from sending messages in supergroups/channels|
|400|USER_IS_BLOCKED|You were blocked by this user|
|400|USER_IS_BOT|Bots can't send messages to other bots|
|400|YOU_BLOCKED_USER|You blocked this user|
|406|AUTH_KEY_DUPLICATED|An auth key with the same ID was already generated|
|401|AUTH_KEY_PERM_EMPTY|The temporary auth key must be binded to the permanent auth key to use these methods.|
|403|CHAT_WRITE_FORBIDDEN|You can't write in this chat|
|420|SLOWMODE_WAIT_X|Slowmode is enabled in this chat: you must wait for the specified number of seconds before sending another message to the chat.|
|-503|Timeout|Timeout while fetching data|


