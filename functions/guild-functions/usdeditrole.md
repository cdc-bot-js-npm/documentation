---
description: Edits a guild's role
---

# $editRole

## Description

This function is used to modify/edit a guild role using its id.

## Usage

### Raw usage

`$editRole[roleID;name(optional);color(optional);hoisted(optional);mentionable;guildID;permissions]`

This function has one required field and six optional.

1. `roleID` =&gt; the role to edit.
2. `name` =&gt; the new for the role.
3. `color` =&gt; the hex color for the role.
4. `hosited` =&gt; if the role will be hoisted.
5. `mentionable` =&gt; if the role will be mentionable.
6. `guildID` =&gt; the guild if of the role to manage it
7. `permissions` =&gt; the permissions for the role 

## Example Commands

Modify role color:

```javascript
client.command({
name: "role-color",
code. `$editRole[747882318554988687;;O4OE20]`
})
```

