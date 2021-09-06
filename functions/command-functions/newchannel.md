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
  </tbody>
</table>
