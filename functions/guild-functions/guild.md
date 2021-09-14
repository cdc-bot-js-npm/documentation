---
description: >-
  A compact function with multiple options to return data about the given
  Discord server.
---

# $guild

## Description

This function is used to get several information about the given guild.

## Usage

### Raw usage

`$guild[option (optional);guildID (optional)]`

This function has two optional fields:

1. `option` =&gt; the option you want to get of the guild.
2. `guildID` =&gt; the ID of the guild you want to get the date of, default is the current guild's ID.

### **Options**

| Option | Description |
| :--- | :--- |


## Example Commands

Getting the id of a guild \(using function without brackets\):

```javascript
client.command({
name: "guildid",
code: `
This guild's ID is: $guild
`
})
```

Getting the current guild's name with using just the first field:

```javascript
client.command({
name: "guildid",
code: `
This guild's name is: $guild[name]
`
})
```

Getting the name of another guild with given ID by using both fields:

```javascript
client.command({
name: "guildid",
code: `
The given guild's name is: $guild[name;851026126524645416] and it'S ID is $guild[id;851026126524645416]
`
})
```

