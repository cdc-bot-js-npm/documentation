---
description: >-
  The client events are part of the main structure of your bot. Without enabling
  them you bot can't access specific Discord actions like tracking special
  Discord events etc.
---

# Client Events

## Introduction

cdc-bot.js covers most of the gateaway events of the Discord API.  
You can decide yourself what events you need for your bot or not. The more events you have enabled the more actions can be done and the more command types you can use  
If you do not enable a certain event, you will not receive any of the Discord gateway events that are batched into that group. The valid events are listed below:

## Available events

| Event Name | Default Setting | Note | Command Types: |
| :---: | :--- | :---: | :---: |
| `onMessageCreate` | true | If disabled, client won't see to any messages. | \`\`[`prefixedCommand`](../command-types/prefixedcommand.md), [`nonPrefixedCommand`](../command-types/nonprefixedcommand.md), [`messageCommand`](../command-types/messagecommand.md) |
| `onReady` | true | This event can't be disabled. | \`\`[`readyCommand`](../command-types/readycommand.md)\`\` |
| `onChannelCreate` | false | - | \`\`[`chnanelCreateCommand`](../command-types/channelcreatecommand.md)\`\` |
| `onChannelDelete` | false | - | \`\`[`channeldeleteCommand`](../command-types/channeldeletecommand.md)\`\` |
| `onChannelPinsUpdate` | false | Discord doesn't provide data about the pin status and not about the pinned/ unpinned message, just about the channel it belongs to. | \`\`[`channelPinsUpdateCommand`](../command-types/channelpinsupdatecommand.md)\`\` |
| `onChannelUpdate` | false | - | \`\`[`channelUpdateCommand`](../command-types/channelupdatecommand.md)\`\` |
| `onEmojiCreate` | false | - | \`\`[`emojiCreateCommand`](../command-types/emojicreatecommand.md)\`\` |
| `onEmojiDelete` | false | - | \`\`[`emojiDeleteComamnd`](../command-types/emojideletecommand.md)\`\` |
| `onEmojiUpdate` | false | - | \`\`[`emojiUpdateCommand`](../command-types/emojiupdatecommand.md)\`\` |
| `onGuildBanAdd` | false | - | \`\`[`guildBnAddCommand`](../command-types/guildbanaddcommand.md)\`\` |
| `onGuildBanRemove` | false | - | \`\`[`guildBanRemoveCommand`](../command-types/guildbanremovecommand.md)\`\` |
| `onGuildCreate` | false | - | \`\`[`guildCreateCommand`](../command-types/guildcreatecommand.md)\`\` |
| `onGuildDelete` | false | - | \`\`[`guildDeleteCommand`](../command-types/guilddeletecommand.md)\`\` |
| `onGuildMemberAdd` | false | - | \`\`[`guildMemberAddCommand`](../command-types/guildmemberaddcommand.md)\`\` |
| `onGuildMemberRemove` | false | - | \`\`[`guildMemberRemoveCommand`](../command-types/guildmemberremovecommand.md)\`\` |
| `onGuildMemberUpdate` | false | - | \`\`[`guildMemberUpdateCommand`](../command-types/guildmemberupdatecommand.md)\`\` |
| `onGuildUpdate` | false | - | \`\`[`guildUpdateCommand`](../command-types/guildupdatecommand.md)\`\` |
| `onInteractionCreate` | false | - | \`\`[`interactionCreateCommand`](../command-types/interactioncreatecommand.md)\`\` |
| `onInviteCreate` | false | - | \`\`[`inviteCreateCommand`](../command-types/invitecreatecommand.md)\`\` |
| `onInviteDelete` | false | - | \`\`[`inviteDeleteCommand`](../command-types/invitedeletecommand.md)\`\` |
| `onMessageDelete` | false |  | \`\`[`messageDeleteCommand`](../command-types/messagedeletecommand.md)\`\` |
| `onMessageDeleteBulk` | false |  | \`\`[`messageDeleteBulkCommand`](../command-types/messagedeletebulkcommand.md)\`\` |
| `onMessageReactionAdd` | false |  | \`\`[`messageReactionAddCommand`](../command-types/messagereactionaddcommand.md)\`\` |
| `onMessageReactionRemove` | false |  | \`\`[`messageReactionRemoveCommand`](../command-types/messagereactionremovecommand.md)\`\` |
| `onMessageUpdate` | false |  | \`\`[`messageUpdateCommand`](../command-types/messageupdatecommand.md)\`\` |
| `onPresenceUpdate` | false | - | \`\`[`presenceUpdateCommand`](../command-types/presenceupdatecommand.md)\`\` |
| `onRateLimit` | false | - | \`\`[`rateLimitCommand`](../command-types/ratelimitcommand.md)\`\` |
| `onRoleCreate` | false | - | \`\`[`roleCreateCommand`](../command-types/rolecreatecommand.md)\`\` |
| `onRoleDelete` | false | - | \`\`[`roleDeleteComamnd`](../command-types/roledeletecommand.md)\`\` |
| `onRoleUpdate` | false | - | \`\`[`roleUpdateCommand`](../command-types/roleupdatecommand.md)\`\` |
| `onTypingStart` | false | - | \`\`[`typingStartCommand`](../command-types/typingstartcommand.md)\`\` |
| `onUserUpdate` | false | - | \`\`[`userUpdateCommand`](../command-types/userupdatecommand.md)\`\` |
| `onVoiceStateUpdate` | false | - | \`\`[`voiceStateUpdateCommand`](../command-types/voicestateupdatecommand.md)\`\` |
| `onWebhookUpdate` | false | Discord doen't provide data about the updated webhook, just about the channel it belongs to. | \`\`[`webhookUpdateCommand`](../command-types/webhookupdatecommand.md)\`\` |

## Enable an event

To enable an event add it to the events option inside your client setup like in the example below:

{% code title="index.js" %}
```javascript
const cdc = require('cdc-bot.js')

const client = new cdc.Bot({
    token: "TOKEN_HERE",
    prefix: "PREFIX_HERE",
    events: {
    onChannelCreate: true,
    onChannelDelete: true,
    onChannelUpdate: true,
    // and so on...
    }
})
```
{% endcode %}

## Disable an event

Just add the event with the option set to `false`.  
In most cases this isn't needed if default option is set to `false`. In that cases you can just remove the event from the events option to disable it.

{% code title="index.js" %}
```javascript
const cdc = require('cdc-bot.js')

const client = new cdc.Bot({
    token: "TOKEN_HERE",
    prefix: "PREFIX_HERE",
    events: {
    onChannelCreate: false,
    onChannelDelete: false
    }
})
```
{% endcode %}

