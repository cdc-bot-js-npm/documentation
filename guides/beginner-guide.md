---
description: >-
  This is our beginner guide you should read to learn how to work with the
  package.
---

# Beginner Guide

## How to install cdc-bot.js?

{% hint style="warning" %}
**Node.JS** version **12.0.0** or higher is required to use the package!
{% endhint %}

#### Terminal:

 Go to your terminal and run the following command:

{% tabs %}
{% tab title="Terminal" %}
```text
npm install cdc-bot.js
```
{% endtab %}
{% endtabs %}

#### package.json file:

If you use a hosting server like hosts with the Pterodactyl Panel offer, create a file called `package.json` in the main folder of your host server and paste the following text into it:

{% code title="package.json" %}
```javascript
{
  "name": "-asdf",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "start": "node index.js"
  },
  "engines": {
    "node": "12.x"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    "cdc-bot.js": "^1.0.0",
  }
}
```
{% endcode %}

## How to setup my bot client's code?

This JavaScript file called `index.js` or whatever you have chosen as main file name is the heart of your bot's code and responsible for setting up your bot client. Copy this part and place it at the top of your mainfile. Replace `TOKEN_HERE` with your bot's token from the [Developer Portal](https://discordapp.com/developers/applications) and replace the `PREFIX_HERE`with your bot's new prefix. You can also check our example main file attached below.

{% code title="index.js" %}
```javascript
const CDC = require('cdc-bot.js')

const client = new CDC.Client({
token: "TOKEN_HERE", //Paste Discord Bot Token in the quotes
prefix: "PREFIX_HERE" //Paste your Discord Bot Prefix in the quotes
events: {
onMessageCreate: true, // enabled by default, all other events disabled by default
onMessageUpdate: false, // example event | true/false = enabled/disabled
})

// example default command:
bot.prefixedCommand({
name: "ping", //Trigger name (command name)
code: `Pong! $clientPing` //Code
})

// example readyCommand:
bot.readyCommand({
channel: "851026126524645416",
code: `I am back online!
` // Sends the message in the given channel whenever bot is back online
})
```
{% endcode %}

{% hint style="info" %}
Now your bot is ready to use. Now you can add commands, a presence and more. 👍
{% endhint %}

## How to update the package?

If your package version is outdated and you want to use the latest version for your bots, you can easily use the following command in your terminal:

```text
npm i cdc-bot.js@latest
```

 You can also use this command in the eval command when using `$exec[nmp i cdc-bot.js@latest]`. Additionally you can just head over to your `package.json` file and change the version of cdc-bot.js to the current version and restart your server. **Example** updating package from version 0.0.1 to version 1.0.0:

```javascript
"cdc-bot.js": "^0.0.1" // Example before update to 1.0.0

"cdc-bot.js": "^1.0.0" // after updating
```

{% hint style="info" %}
You find the latest package version at the top of the changelog page and in our [Discord Server](https://discord.gg/HmtpbraCnk).
{% endhint %}

## Setup bot's presence

You can add as many presences as you want to. After the given `timeout` the client will switch to the next presence or will reload the presence if just one set. Presences must be set below the client setup from below inside your main file.

### Presence options

| Option | Description |
| :--- | :--- |
| `text` | Text to be shown. |
| `status` | The status of the client user \(see below\). |
| `timeout` | The time in seconds after the presence will be updated in it's circle. |
| `type` | The presence type \(see below\). |
| `url` | The url of a streaming activity. |

#### Status options

`online`, `dnd`, `idle`, `invisible` 

#### Activity types

`COMPETING`, `PLAYING`, `LISTENING`, `STRAMING`, `WATCHING`

{% hint style="warning" %}
Timeout must be `12` seconds or higher, otherwise your bot will be rate limited by Discord!
{% endhint %}

### Example presences

```javascript
client.presence({
    status: "online",
    name: "with $client[guild_count] servers", // Text to be shown
    type: "STREAMING", // PLAYING, COMPETING, WATCHING, LISTENING, STREAMING
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

## Client options

The package currently has the following options for the client setup:

| Option | Description | required | Default setting |
| :---: | :---: | :---: | :---: |
| `token` | The client's token to login in Discord. | true | none |
| `prefix` | String or array of prefixes. Used for `prefixedCommands`. | false | `!` |
| `mobileLogin` | Whether to login the bot via mobile presence or not. | false | `false` |
| `memberMinAge` | Amount of seconds a joined member must be older as to not count as a fake invite. Used for the invite tracking system. | false | `86400` |
| `events` | The object of events for the client, needed for special command types functionality. | false | `onMessageCreate: true` |
| `respondToBots` | Whether to respond to bot users or to ignore them. | false | `true` |
| `respondToWebhooks` | Whether to respond to bot webhook messages or to ignore them. | false | `false` |
| `respondToDMs` | Whether to respond to bot users or to ignore them. | false | `true` |
| `executeCmdOnUpdate` | Whether to execute commands with message updates if the new content matches a command name. | false | `false` |

{% code title="index.js" %}
```javascript
const cdc = require('cdc-bot.js')

const client = new cdc.Bot({
    token: "TOKEN_HERE",
    prefix: "PREFIX_HERE",
    cacheInvites: true,
    mobileLogin: true,
    memberMinAge: 86400,
    executeCmdOnUpdate: true,
    respondToDMs: true,
    respondToBots: true,
    respondToWebhooks: true,
    events: {
    onChannelCreate: false,
    onChannelDelete: false
    }
})
```
{% endcode %}

