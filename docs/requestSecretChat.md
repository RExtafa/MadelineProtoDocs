---
title: requestSecretChat
description: requestSecretChat parameters, return type and example
redirect_from: /request_secret_chat.html
---
## Method: requestSecretChat  


### Parameters:

| Name     |    Type       |
|----------|---------------|
|id| A username, a bot API chat id, a tg-cli chat id, a [User](API_docs/types/User.md), an [InputPeer](API_docs/types/InputPeer.md), an [InputUser](API_docs/types/InputUser.md), a [Peer](API_docs/types/Peer.md)|

### Return type: Number

Returns the secret chat ID

### Example ([now fully async!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
$secret_chat_id = yield $MadelineProto->requestSecretChat('@danogentili');
```

