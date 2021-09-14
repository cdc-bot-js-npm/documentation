---
description: Edits a server channel using its id.
---

# $editChannel

## Description

This function is used to modify/edit a server channel

## Usage

### Raw usage

`$editChannel[name;position (optional);topic (optional);nsfw (yes/no, optional);bitrate (optional);userLimit (optional);categoryID (optional);sync (yes/no, optional);reason (optional);channelID (optional)]`

This function has minimum two required fields and the other optional:

## Example Commands

Modify channel name:

```javascript
client.command({
name: "change-name",
code: `$editChannel[new-name]`
})
```

