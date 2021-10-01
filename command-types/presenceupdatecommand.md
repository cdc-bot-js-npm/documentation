---
description: >-
  A command that will be executed whenever a guild member's presence (e.g.
  status, activity) is changed if the onPresenceUpdate event is enabled.
---

# presenceUpdateCommand

## Description

This command type will be executed whenever a guild member's presence changed, like status or activities. This can be used to track changes of the custom status, the presence status \(offline, online, etc.\) or the user's presence activities like playing a game.

{% hint style="warning" %}
 These commands need the [`onPresenceUpdate`](../guides/client-events.md) event to be anabled to work.
{% endhint %}

## Example commands

This command will be executed if a user's presence activities changed.

```text
client.presenceUpdateCommand({
channel: "848540884438220800",
code: `
$if[$oldPresence[activities_names]!=$newPresence[activities_names]]
$newPresence[user_tag] changed their activities from $oldPresence[activities_names] to $newPresence[activities_names].
$endif
`
})
```

This command will be executed if a user changes their status:

```text
client.presenceUpdateCommand({
channel: "848540884438220800",
code: `
$if[$oldPresence[status]!=$newPresence[status]]
$newPresence[user_tag] changed status from $oldPresence[status] to $newPresence[status].
$endif
`
})
```

## Functions

### Options

These options can be used in the functions $oldPresence and $newPresence

| Option | Description |
| :--- | :--- |
| `activities_names` | The presence activities of the user that updated the presence, mapped by their name. |
| `activities_types` | The presence activities of the user that updated the presence, mapped by their type. |
| `guild_id` | The ID of the guild the user updated the presence on. |
| `id` | The ID of the user that updated the presence. |
| `status` | The status of the user. |
| `user_tag` | The user tag of the user that updated the presence. |
| `username` | The username of the user that updated the presence. |

