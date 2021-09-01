---
description: >-
  This is our beginner guide you should read to learn how to work with the
  package.
---

# Beginner Guide

## How to install cdc-bot.js?

#### Terminal:

```javascript
const CDC = require('cdc-bot.js')

const client = new CDC.Client({
token: "TOKEN_HERE", //Discord Bot Token
prefix: "PREFIX_HERE" //Discord Bot Prefix
events: {
onMessageCreate: true, // enabled by default, all other events disabled by default
onMessageUpdate: false, // example... true/false = enabled/disabled
})

example default command:
bot.prefixedCommand({
name: "ping", //Trigger name (command name)
code: `Pong! $clientPing` //Code
})

// example readyCommand:
bot.readyCommand({
    channel: "", //You can use this or not
    code: `$log[Ready on $userTag[$clientID]]` //Example Ready on Client
})
```

#### package.json file:

### How to setup my bot client's code?

### 

### How to update the package?

