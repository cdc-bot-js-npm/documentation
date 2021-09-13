---
description: >-
  A function that modify a custom guild emoji.
---

# $modifyEmoji

## Description

Modifies a guild's custom emoji with given ID to edit emoji's name or roles.

## Usage

### Raw usage

`$modifyEmoji[emojiID;name;roleIDs (optional)]`

## Example Commands

```javascript
client.command({
name: "modify-emoji",
code: `
$modifyEmoji[853619633495736320;this_new_name]
ok
`
})
```