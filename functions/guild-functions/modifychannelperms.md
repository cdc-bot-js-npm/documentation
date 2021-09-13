---
description: >-
  A function that changes the channel permissions.
---

# $modifyChannelPerms

## Description

Modifies the permissions of a user or a role in a guild channel the bot has access to...

## Usage

### Raw usage

`$modifyChannelPerms[userID/roleID;permission;permission2 (optional);...;channelID]`

## Example Commands

Description of the example command here with colons at the end

```javascript
client.command({
name: "perms",
code: `
$modifyChannelPerms[$authorID;-addreactons;-sendmessages;$channelID]
ok
`
})
```