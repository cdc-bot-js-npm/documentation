---
description: >-
  A compact function with multiple options to return data about the given
  Discord channel.
---

# $channel

## Description

This function is used to get several information about the given channel.  
If you don't provide any data in the function, it will return the current channel's ID.

## Usage

### Raw usage

`$channel[option (optional);channelID (optional)]`

This function has two optional fields:

1. `option` =&gt; the option you want to get of the channel.
2. `channelID` =&gt; the ID of the channel you want to get the data of, default is the current channel's ID.

### **Options**

<table>
  <thead>
    <tr>
      <th style="text-align:left">Option</th>
      <th style="text-align:left">Description</th>
      <th style="text-align:left">Channel types</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>bitrate</code>
      </td>
      <td style="text-align:left">The bitrate of the voice channel.</td>
      <td style="text-align:left">voice</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>children_names</code>
      </td>
      <td style="text-align:left">The names of channels in this category.</td>
      <td style="text-align:left">category</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>children_ids</code>
      </td>
      <td style="text-align:left">The IDs of channels in this category.</td>
      <td style="text-align:left">category</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>children_mentions</code>
      </td>
      <td style="text-align:left">The mentions of channels in this category.</td>
      <td style="text-align:left">category</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>created_at</code>
      </td>
      <td style="text-align:left">The time the channel was created at.</td>
      <td style="text-align:left">all</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>created_timestamp</code>
      </td>
      <td style="text-align:left">The timestamp the channel was created at.</td>
      <td style="text-align:left">all</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>deletable</code>
      </td>
      <td style="text-align:left">Whether the channel is deletable by the client user.</td>
      <td style="text-align:left">all</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>deleted</code>
      </td>
      <td style="text-align:left">Whether the channel has been deleted.</td>
      <td style="text-align:left">all</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>full</code>
      </td>
      <td style="text-align:left">Checks if the voice channel is full.</td>
      <td style="text-align:left">voice</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>guild_id</code>
      </td>
      <td style="text-align:left">The id of the guild the channel is in.</td>
      <td style="text-align:left">all</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>guild_name</code>
      </td>
      <td style="text-align:left">The guild the channel is in.</td>
      <td style="text-align:left">all</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>id</code>
      </td>
      <td style="text-align:left">The ID of the channel.</td>
      <td style="text-align:left">all</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>joinable</code>
      </td>
      <td style="text-align:left">Whether the channel is joinable by the client user.</td>
      <td style="text-align:left">voice</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>last_message_id</code>
      </td>
      <td style="text-align:left">The last message id sent in the channel, if one was sent.</td>
      <td style="text-align:left">text, news</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>last_pin_at</code>
      </td>
      <td style="text-align:left">The date when the last pinned message was pinned, if there was one.</td>
      <td
      style="text-align:left">text, news</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>last_pin_timestamp</code>
      </td>
      <td style="text-align:left">The timestamp when the last pinned message was pinned, if there was one.</td>
      <td
      style="text-align:left">text, news</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>manageable</code>
      </td>
      <td style="text-align:left">Whether the channel is manageable by the client user.</td>
      <td style="text-align:left">all</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>members_names</code>
      </td>
      <td style="text-align:left">A collection of cached members of this channel, mapped by their usernames.
        Members that can view this channel, if the channel is text based. Members
        in the channel, if the channel is voice based.</td>
      <td style="text-align:left">all</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>members_ids</code>
      </td>
      <td style="text-align:left">A collection of cached members of this channel, mapped by their ids. Members
        that can view this channel, if the channel is text based. Members in the
        channel, if the channel is voice based.</td>
      <td style="text-align:left">all</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>member_mentions</code> 
      </td>
      <td style="text-align:left">A collection of cached members of this channel, mapped by their mention.
        Members that can view this channel, if the channel is text based. Members
        in the channel, if the channel is voice based.</td>
      <td style="text-align:left">all</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>mention</code>
      </td>
      <td style="text-align:left">The mention of the channel.</td>
      <td style="text-align:left">all</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>name</code>
      </td>
      <td style="text-align:left">The name of the guild channel.</td>
      <td style="text-align:left">all</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>nsfw</code>
      </td>
      <td style="text-align:left">If the guild considers this channel NSFW.</td>
      <td style="text-align:left">text, nsfw</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>category_id</code>
      </td>
      <td style="text-align:left">The ID of the category parent of this channel.</td>
      <td style="text-align:left">text, voice, news</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>category_name</code>
      </td>
      <td style="text-align:left">The name of the category parent of this channel.</td>
      <td style="text-align:left">text, voice, news</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>partial</code>
      </td>
      <td style="text-align:left">
        <p>Whether this Channel is a partial.</p>
        <p>This is always false outside of DM channels.</p>
      </td>
      <td style="text-align:left">all</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>permissions_locked</code>
      </td>
      <td style="text-align:left">If the permissionOverwrites match the parent channel, null if no parent.</td>
      <td
      style="text-align:left">text, voice, news</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>position</code>
      </td>
      <td style="text-align:left">The position of the channel.</td>
      <td style="text-align:left">all</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>rate_limit_per_user</code>
      </td>
      <td style="text-align:left">The ratelimit (slowmode) per user for this channel in seconds.</td>
      <td
      style="text-align:left">text</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>raw_position</code>
      </td>
      <td style="text-align:left">The raw position of the channel from discord. Starting with <code>0</code> as
        highest channel in the guild. Each channel type has it&apos;s own row.</td>
      <td
      style="text-align:left">all</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>speakable</code>
      </td>
      <td style="text-align:left">Checks if the client has permission to send audio to the voice channel.</td>
      <td
      style="text-align:left">voice</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>topic</code>
      </td>
      <td style="text-align:left">The topic of the text channel.</td>
      <td style="text-align:left">text, news</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>type</code>
      </td>
      <td style="text-align:left">The type of the channel.</td>
      <td style="text-align:left">all</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>user_limit</code>
      </td>
      <td style="text-align:left">The maximum amount of users allowed in this channel - 0 means unlimited.</td>
      <td
      style="text-align:left">voice</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>viewable</code>
      </td>
      <td style="text-align:left">Whether the channel is viewable by the client user.</td>
      <td style="text-align:left">all</td>
    </tr>
  </tbody>
</table>

## Example Commands

Getting the id of a channel \(using function without brackets\):

```javascript
client.command({
name: "channelid",
code: `
This channel's ID is: $channel
`
})
```

Getting the current channel's name with using just the first field:

```javascript
client.command({
name: "channelid",
code: `
This channel's name is: $channel[name]
`
})
```

Getting the name of another channel with given ID by using both fields:

```javascript
client.command({
name: "channelid",
code: `
The given channel's name is: $channel[name;851026126524645416] and it'S ID is $channel[id;851026126524645416]
`
})
```

### Guild channel types:

* `text`
* `news`
* `voice`
* `store`
* `category`

