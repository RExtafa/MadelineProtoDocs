---
title: langpack.getLangPack
description: Get localization pack strings
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/langpack_getLangPack.html
---
# Method: langpack.getLangPack
[Back to methods index](index.md)



Get localization pack strings

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|lang\_code|[string](../types/string.md) | Language code | Yes|


### Return type: [LangPackDifference](../types/LangPackDifference.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$LangPackDifference = $MadelineProto->langpack->getLangPack(['lang_code' => 'string', ]);
```

Or, if you're into Lua:

```lua
LangPackDifference = langpack.getLangPack({lang_code='string', })
```

### Errors

| Code | Type     | Description   |
|------|----------|---------------|
|400|LANG_PACK_INVALID|The provided language pack is invalid|


