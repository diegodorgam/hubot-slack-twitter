# Hubot Slack Twitter

**Hubot Slack Twitter** allows to post twitt directly from slack. 

By adding the **Hubot Slack Twitter**, you can configure many twitter accounts and bind them to one or more Slack rooms. Then, anybody in the room (even private) can ask the robot to tweet on the dedicated room twitter account.

## Installation

In hubot project repository, run:

`npm install --save hubot-slack-twitter`

Then add **hubot-slack-twitter** to your `external-scripts.json`:

```json
["hubot-slack-twitter"]
```

## Configure

Create a `twitter-config.js` at the root of your hubot directory and fill it with that text and your own config:

```
{
  "accounts": {
    "custom-twitter-account-1": {
      "consumer_key": "xxxxxxxxxxxxxxx",
      "consumer_secret":"xxxxxxxxxxxxxxx",
      "access_token": "xxxxxxxxxxxxxxx",
      "access_token_secret": "xxxxxxxxxxxxxxx"
    },
    "custom-twitter-account-1": {
      "consumer_key": "xxxxxxxxxxxxxxx",
      "consumer_secret": "xxxxxxxxxxxxxxx",
      "access_token": "xxxxxxxxxxxxxxx",
      "access_token_secret": "xxxxxxxxxxxxxxx"
    }
  },
  "rooms": {
    "roomnameA": "custom-twitter-account-1",
    "roomnameB": "custom-twitter-account-1",
    "roomnameC": "custom-twitter-account-1",
    "username": "custom-twitter-account-2"
  }
}

```

Now, you can invite your bot in one of the rooms you mentionned in the config, and send a twitt (see example below).

## Sample Interaction

Twitt a link
```
user>> hubot tweet http://tilap.net/
```

Twitter a link with some description
```
user>> hubot tweet http://tilap.net/ a smart french blog about various dev tips
```

Show the current room twitter account the bot will post on
```
user>> hubot tweet infos
```
