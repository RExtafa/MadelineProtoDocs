---
title: pageBlockPullquote
description: Pullquote
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: pageBlockPullquote  
[Back to constructors index](index.md)



Pullquote

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|text|[RichText](../types/RichText.md) | Yes|Text|
|caption|[RichText](../types/RichText.md) | Yes|Caption|



### Type: [PageBlock](../types/PageBlock.md)


### Example:

```php
$pageBlockPullquote = ['_' => 'pageBlockPullquote', 'text' => RichText, 'caption' => RichText];
```  


Or, if you're into Lua:

```lua
pageBlockPullquote={_='pageBlockPullquote', text=RichText, caption=RichText}

```


