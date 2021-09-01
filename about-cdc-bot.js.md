---
description: >-
  cdc-bot.js is an easy to learn npm package that makes it possible for you to
  code your own advanced Discord bots fast and uncomplicated. We use functions
  that make all imaginable uses for your bots!
---

# About cdc-bot.js

[![Discord](https://img.shields.io/discord/845696357406998588?color=blue&label=Discord&logo=discord&logoColor=white)](https://discord.gg/djcSRFPPaN)

### Table Of Contents:

* About cdc-bot.js
* How to install
* Examples
  * Setup your Bot
  * Bot Presence
  * Bot Variables
  * Client Events
* More features 
  * Discord Interactions & Slash Commands
* Links
* Contributing

### About our package:

cdc-bot.js is an easy to learn package that makes it possible for you to code your own advanced Discord bots fast and uncomplicated.

We use functions that make all imaginable uses for your Discord\* bots possible. &lt;/br&gt;

The package is open source that allows anyone to contribute to the package development. Together we can!   
  


### Installation:

**Node.JS version 12.0.0 or higher is required!**

```text
npm install cdc-bot.js
```

### Examples:

#### Bot Setup:

```javascript
const cdc = require('cdc-bot.js')

const client = new cdc.Bot({
    token: "TOKEN HERE", // paste your secret bot user's Discord Token
    prefix: "!", // prefix or array ( prefix: ['!', '?', 'xyz', '...'] ) of prefixes, optional, default is "!"
    executeCmdOnUpdate: true, // Whether to run commands with updated messages if they're a command trigger, optional, default false
    fetchInvites: true, // Whether to cache invites data for invite tracking system or not
    respondToDMs: false, // Whether to respond to messages in bot's DMS or not, optional, default true
    respondToBots: false, // Whether to respond to messages sent by bots or not, optional, default true
})
```

#### Bot Presence:

This is the activity presence the bot's user profile will show in it's profile and in the members list. You can set up as many presences as you like but timeout \(until bot reloads the presence/ changes to next presence\) must be higher than 12 seconds \(Discord Rate Limit\)

**Setting up bot's presence:**

```javascript
client.presence({
    status: "online", // online, idle, dnd, invisible
    name: "w?help on $client[guild_count] servers with $client[users_count] users", // Text to be shown
    type: "PLAYING", // PLAYING, COMPETING, WATCHING, LISTENING, STREAMING
    timeout: 12, // length in seconds before changing the presence again (must be 12 or higher)
    url: "https://twitch.tv/discord_dutchman" // Twitch-Channel-URL or YouTube-Video-URL if type is STREAMING
})
client.presence({
    status: "online", // online, idle, dnd, invisible
    name: "with $client[guild_count] servers", // Text to be shown
    type: "PLAYING", // PLAYING, COMPETING, WATCHING, LISTENING, STREAMING
    timeout: 12, // timeout in seconds
})
```

#### Bot Variables:

**What are variables?**

In our package we use variables to store data in the bot's database. The data is based on IDs \(e.g. based on a specific userID/channelID/messageID/guildID\). These variables are Key-Value based. This can be used as example to store channelIDs that are depending on the server the command was used in. It's also usable to store a user's economy balance based on the userID.

**Setup the variable keys:**

```javascript
bot.variables({
  VariableName1: "true", //This is the default value that can be changed via functions for each user/channel/server/message differently.
  VariableName2: "false" //Second variable's default value is "false".
})
```

#### Discord API Events

**What are these events?**

It's simple and easy process, it essentially allows you to trigger commands on special events of the Discord API, such as user joining a Guild. This will trigger an event, causing commands with supported type for each event to be executed then.

**The available events our package covers:**

```text
onChannelCreate, onChannelDelete, onChannelPinsUpdate, onChannelUpdate, onEmojiCreate, onEmojiUpdate, onEmojiDelete, onGuildBanAdd, onGuildBanRemove, onGuildCreate, onGuildDelete, onGuildMemberAdd, onGuildMemberRemove, onGuildMemberUpdate, onGuildUnavailable, onGuildUpdate, onInviteCreate, onInviteDelete, onInteractionCreate, onMessageCreate, onMessageDelete, onMessageDeleteBulk, onMessageUpdate, onMessageReactionAdd, onMessageReactionRemove, onMessageReactionRemoveAll, onMessageReactionRemoveEmoji, onPresenceUpdate, onRateLimit, onRoleCreate, onRoleDelete, onRoleUpdate, onTypingStart, onUserUpdate, onVoiceStateUpdate, onWebhookUpdate
```

**Example Event-Command:**

```javascript
bot.guildMemberCreateCommand({
        channel: "Channel ID", //Enter the welcome-channel-ID
        code: `<@$user> welcome to our server!` //Type in whatever message you would like to be send.
})
```

### More Features:

#### Discord Interactions & Application Commands:

With easy and simple functions, you can make Slash Commands \(application command type 1\) and Message Context Commands \(application command types 2 & 3\) and let your bot respond to the interactions quick!

```javascript
// Example of creating a slash command
client.prefixedCommand({
    name: "slash",
    code: `$createApplicationCommand[$guild;1;support;Returns invite-link of our support-server.]`
})
// responding to a slash command interaction:
client.interactionCreateCommand({
    name: "support", 
    code: `$interactionReply[Join our server by clicking [here](https://discord.gg/djcSRFPPaN)]`
})
// responding to a button click:
client.interactionCreateCommand({
interaction: 'component',
name: 'click_me' // custom_id of the button
code: `
$interactionReply[You clicked the button successfully!]
`
})
// responding to a select menu click:
client.interactionCreateCommand({
interaction: 'component',
name: 'click_me' // custom_id of the select menu
code: `
$interactionReply[You clicked the on the menu and selected the option $interactionData[select_values]!]
`
})
```

More Information in our [Documentation](https://cdc-bot.dutchman-dev.com/guide/application-commands)

### Links

cdc-bot.js was made by [The Dutchman\#0001](https://discordapp.com/users/704677071929999390).

* [Website](https://cdc-bot.dutchman-dev.com)
* [Documentation](https://cdc-bot.dutchman-dev.com)
* [Discord Server](https://discord.gg/HmtpbraCnk)
* [GitHub Repository](https://github.com/cdc-bot-js-npm/cdc-bot.js)
* [Documentation GitHub Repository](https://github.com/cdc-bot-js-npm/documentation)

### Contributing

You want to help us with developing the package? You can contibute to the package's development. Read [Contributing](https://github.com/cdc-bot-js-npm/cdc-bot.js/blob/main/.github/CONTRIBUTING.md) for more information.

* We're not affiliated with Discord.

