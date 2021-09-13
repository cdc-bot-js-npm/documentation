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

```javascript
client.command({
name: "perms",
code: `
$modifyChannelPerms[$authorID;-addreactons;-sendmessages;$channelID]
ok
`
})
```