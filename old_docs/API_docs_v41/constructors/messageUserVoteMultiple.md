---
title: messageUserVoteMultiple
description: How a user voted in a multiple-choice poll
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: messageUserVoteMultiple  
[Back to constructors index](index.md)



How a user voted in a multiple-choice poll

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|user\_id|[int](../types/int.md) | Yes|User ID|
|options|Array of [bytes](../types/bytes.md) | Yes|Options chosen by the user|
|date|[int](../types/int.md) | Yes|When did the user cast their votes|



### Type: [MessageUserVote](../types/MessageUserVote.md)


### Example:

```php
$messageUserVoteMultiple = ['_' => 'messageUserVoteMultiple', 'user_id' => int, 'options' => ['bytes', 'bytes'], 'date' => int];
```  


Or, if you're into Lua:

```lua
messageUserVoteMultiple={_='messageUserVoteMultiple', user_id=int, options={'bytes'}, date=int}

```


