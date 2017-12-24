# SwtorDiscordBot
The source of the bot used in the SWTOR Discord (https://discord.gg/swtor). __Note__: This does not include newer features, this is only core and essential features of the bot. With help of a programmer you can easily expand features and add commands as needed.

You will need:
- [Node.js](https://nodejs.org/en/)
- A _(novice)_ JavaScript Developer _(you probably have one if you run a gaming related Discord)_
- A Discord Bot Token [see apps](https://discordapp.com/developers/applications/me#top)

### Setting up
1) In the file `/config/config.json` replace the bot token and root id (_which is your user id_) with your own.  
2) Change the `"roles":[...]` array to be roles users are allowed to obtain via !roles (NOTE: IN LOWERCASE).
3) Change "channels" **VALUES** to match that of your server.
4) In the root folder run:  
```
npm install
```
5) You can start the bot by using:  
```
node app
```

The code is designed to work with a status monitor, specifically [PM2](http://pm2.keymetrics.io/). 

### How do I get my user id?
[Read here](https://support.discordapp.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-)

### How can I host this for free?
[Heroku](https://www.heroku.com/)
Use `Procfile`
```
worker: node app.js
```
and add
```
"engines": {
    "node": "6.11.1"
  },
"scripts": {
    "start": "node app.js"
  },
  "main": "app.js",
  ....
```
to `package.json`
