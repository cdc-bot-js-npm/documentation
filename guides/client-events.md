# Client Events

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
    onChannelDelete: true
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

## Available events

| name | default setting | note |
| :--- | :--- | :--- |
| `onMessageCreate` | true | If disabled, client won't see to any messages. |
| `onReady` | true | This event can't be disabled. |
| `onChannelCreate` | false | - |
| `onChannelDelete` | false | - |
| `onChannelPinsUpdate` | false | Discord doen't provide data about the pin status and not about the pinned/ unpinned message, just about the channel it belongs to. |
| `onChannelUpdate` | false | - |
| `onEmojiCreate` | false | - |
| `onEmojiDelete` | false | - |
| `onEmojiUpdate` | false | - |
| `onGuildBanAdd` | false | - |
| `onGuildBanRemove` | false | - |
| `onGuildCreate` | false | - |
| `onGuildDelete` | false | - |
| `onGuildMemberAdd` | false | - |
| `onGuildMemberRemove` | false | - |
| `onGuildMemberUpdate` | false | - |
| `onGuildUpdate` | false | - |
| `onInteractionCreate` | false | - |
| `onInviteCreate` | false | - |
| `onInviteDelete` | false | - |
| `onPresenceUpdate` | false | - |
| `onRateLimit` | false | - |
| `onRoleCreate` | false | - |
| `onRoleDelete` | false | - |
| `onRoleUpdate` | false | - |
| `onTypingStart` | false | - |
| `onUserUpdate` | false | - |
| `onVoiceStateUpdate` | false | - |
| `onWebhookUpdate` | false | Discord doen't provide data about the updated webhook, just about the channel it belongs to. |

