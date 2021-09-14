---
description: Edits the given option of a guild.
---

# $editGuild

## Description

This function is used to modify/edit a option of the guild given \(ID\)

## Usage

### Raw usage

`$editGuild[option;newValue;reason (optional);guildID (optional)]`

This function has two required fields and two optional.

1. `option` =&gt; the option you want to edit.
2. `newValue` =&gt; the new value for that option.
3. `reason` =&gt; the reason.
4. `guildID` =&gt; the if of the guild to edit.

## Example Commands

Modify guild name:

```javascript
client.command({
name: "modify-guild-name",
code: `Ok
$editGuild[name;New server name!]`
})
```

