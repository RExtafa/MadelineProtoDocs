---
title: updates.channelDifferenceEmpty
description: There are no new updates
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/constructors/updates_channelDifferenceEmpty.html
---
# Constructor: updates.channelDifferenceEmpty  
[Back to constructors index](index.md)



There are no new updates

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|pts|[int](../types/int.md) | Yes|The latest [PTS](https://core.telegram.org/api/updates)|
|timeout|[int](../types/int.md) | Optional|Clients are supposed to refetch the channel difference after timeout seconds have elapsed|



### Type: [updates.ChannelDifference](../types/updates.ChannelDifference.md)


### Example:

```php
$updates.channelDifferenceEmpty = ['_' => 'updates.channelDifferenceEmpty', 'pts' => int, 'timeout' => int];
```  


Or, if you're into Lua:

```lua
updates.channelDifferenceEmpty={_='updates.channelDifferenceEmpty', pts=int, timeout=int}

```


