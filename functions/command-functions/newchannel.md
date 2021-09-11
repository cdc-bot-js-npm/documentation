---
description: >-
  A function that returns the new Discord channel data.
---

# $newChannel

This function returns the new discord channel data registred, its used in the [`onChannelUpdate`](https://github.com/cdc-bot-js-npm/documentation/blob/main/guides/client-events.md) event.

## Usage

### Raw usage
`$newChannel[option]`

### **Options**

<table>
  <thead>
    <tr>
      <th style="text-align:left">Option</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>id</code>
      </td>
      <td style="text-align:left">The channel id.</td>
    </tr>
      <tr>
      <td style="text-align:left"><code>name</code>
      </td>
      <td style="text-align:left">The channel name.</td>
           <tr>
      <td style="text-align:left"><code>topic</code>
      </td>
      <td style="text-align:left">The topic for this channel, if channel is a text channel.</td>
    </tr>
    </tr>
       <tr>
      <td style="text-align:left"><code>position</code>
      </td>
      <td style="text-align:left">The channel position.</td>
    </tr>
       <tr>
      <td style="text-align:left"><code>category_id</code>
      </td>
      <td style="text-align:left">The ID of the category this channel belongs to.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>guild_id</code>
      </td>
      <td style="text-align:left">The ID of the guild this channel belongs to.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>last_message_id</code>
      </td>
      <td style="text-align:left">The ID of the last message sent here (if any).</td>
    </tr>
        <tr>
      <td style="text-align:left"><code>last_pin_timestamp</code>
      </td>
      <td style="text-align:left">The timestamp of the last channel pin in the text channel, if any.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>type</code>
      </td>
      <td style="text-align:left">The type of this channel.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>nsfw</code>
      </td>
      <td style="text-align:left">Whether the channel is nsfw or not.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>slowmode</code>
      </td>
      <td style="text-align:left">The slow mode duration of this channel.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>raw_position</code>
      </td>
      <td style="text-align:left">The raw position of this channel.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>deleted</code>
      </td>
      <td style="text-align:left">Wheter the channel was deleted or not.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>text</code>
      </td>
      <td style="text-align:left">Wheter this channel is text channel or not.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>viewable</code>
      </td>
      <td style="text-align:left">Wheter the channel was be seen by the bot or not.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>manageable</code>
      </td>
      <td style="text-align:left">Wheter the bot can or not manage the channel.</td>
    </tr>
     <tr>
      <td style="text-align:left"><code>deleteable</code>
      </td>
      <td style="text-align:left">Wheter the channel can be deleted by the bot or not.</td>
    </tr>
     <tr>
      <td style="text-align:left"><code>bitrate</code>
      </td>
      <td style="text-align:left">The bitrate of the voice channel, if channel is a voice channel.</td>
    </tr>
         <tr>
      <td style="text-align:left"><code>user_limit</code>
      </td>
      <td style="text-align:left">The user limit of the voice channel, if channel is a voice channel.</td>
    </tr>
        <tr>
      <td style="text-align:left"><code>full</code>
      </td>
      <td style="text-align:left">Whether the voice channel is full, if channel is a voice channel.</td>
    </tr>
         <tr>
      <td style="text-align:left"><code>created_timestamp</code>
      </td>
      <td style="text-align:left">The timestamp of the channel creation.</td>
    </tr>
  </tbody>
</table>
