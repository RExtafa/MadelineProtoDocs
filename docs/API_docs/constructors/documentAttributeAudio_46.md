---
title: documentAttributeAudio
description: documentAttributeAudio attributes, type and example
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: documentAttributeAudio\_46  
[Back to constructors index](index.md)



### Attributes:

| Name     |    Type       | Required |
|----------|---------------|----------|
|duration|[int](../types/int.md) | Optional|
|title|[string](../types/string.md) | Yes|
|performer|[string](../types/string.md) | Yes|



### Type: [DocumentAttribute](../types/DocumentAttribute.md)


### Example:

```
$documentAttributeAudio_46 = ['_' => 'documentAttributeAudio', 'duration' => int, 'title' => 'string', 'performer' => 'string'];
```  

[PWRTelegram](https://pwrtelegram.xyz) json-encoded version:

```
{"_": "documentAttributeAudio", "duration": int, "title": "string", "performer": "string"}
```


Or, if you're into Lua:  


```
documentAttributeAudio_46={_='documentAttributeAudio', duration=int, title='string', performer='string'}

```

