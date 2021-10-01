---
description: >-
  A response that gets executed if the given command was used in a text channel.
  This will be a message starting with the bot's prefix and the given name.
---

# prefixedCommand

## Description

This command type is the default command type. It is used to let your bot respond to messages starting with your bot's prefix and the command name like if you want to let your bot respond to a message starting with `?prefix` you use this command type.

{% hint style="info" %}
These commands need the [`onMessageCreate`](../guides/client-events.md) event to be anabled to work. But that event is enabled by default.
{% endhint %}

## Example commands

Return bot's ping:

```text
client.prefixedCommand({
name: "ping",
code: `
Ping! $client[ping]ms
`
})
```

This command will return `My prefix is ?` if a user types the word `prefix` behind the bot's prefix:

```text
client.prefixedCommand({
name: "prefix",
code: `
My prefix is ?
`
})
```



