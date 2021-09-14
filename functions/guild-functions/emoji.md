---
description: >-
  A compact function with multiple options to return data about the given custom
  emoji.
---

# $emoji

## Description

This function is used to get several information about the given custom emoji ID.

## Usage

### Raw usage

`$emoji[option;emojiID]`

This function has two required fields:

1. `option` =&gt; the option you want to get the data of the custom emoji.
2. `channelID` =&gt; the ID of the custom emoji you want to get the data of.

### **Options**

## Example Commands

Get the emoji created stamp:

```javascript
client.command({
name: "emojicreated",
code: `
That emoji was created in: $emoji[created_at;848531523334569994]
` //It will return the date when it was created
})
```

