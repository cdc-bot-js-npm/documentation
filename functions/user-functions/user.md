---
description: >-
  A compact function with multiple options to return data about the given Discord User.
---

# $user

## Description

A compact function with multiple options to return data about the given Discord User.

## Usage

### Raw usage

`$user[option (optional);userID (optional)]`

This function has two optionalfields:

1. `option` =&gt; The option e.g.: id, discriminator.
2. `userID` =&gt; The id of the user.

### **Options**

Information about options that may exist, maybe a table here

## Example Commands

Example command to get the discriminator of a user;

```javascript
client.command({
name: "discriminator",
code: `
$user[discriminator;$message[1]]
`
});
```