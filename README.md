# Twitch Bot
This is a Twitch Bot created with NodeJS using the tmi.js module.

------

# What do I need?
You will need:
* [NodeJS](https://nodejs.org/en/)
* [TMI.JS](https://tmijs.org/)
* A text/script editor of choice (I strongly recommend [Atom](https://atom.io/), Notepad will work just fine though.)

------

# Where do I begin?
Well the first thing you need once you have installed Node, is you must install the tmi.js library wherever you will be keeping the rest of the files.

So for example if you are keeping these files in C:/Users/"Your_Username"/Desktop, you would cd (change directory) into your desktop and then run this command.
> `npm install --save tmi.js`

After running this command you will notice a `node_modules` folder which will have another folder inside named `tmi.js`.
This is good, if you have this, that means you are setup and ready to continue.

------

# Do I need a seperate Twitch account for my bot?
Yes.

You will need to create a new Twitch account for the bot, preferably with the word "bot" at the end or something so people can distinguish. Then you will need to go to this site:
* [Twitch Chat OAuth Password Generator](http://www.twitchapps.com/tmi/)
On this website you will be able to create an OAuth key that you will need to add into the script.

---

Okay now that you have a bot account with an OAuth key. You will want to go into the `index.js` file and replace the:
* username
* password
* channels

With your bots username, password (The OAuth key.) and then enter the channel that you want your bot to enter. Here is an example below:

>```javascript
var options = {
  options: {
    debug: true
  },
  connection: {
    cluster: "aws",
    reconnect: true
  },
  identity: {
    username: "tsuklebot",
    password: "oauth:..."
  },
  channels: ["tsukle"]
}
```

Now when you run the bot in Node it will login with your bot account and enter the channel or channels you have given it.

*REMEMBER!*: The bot can join multiple channels and you can do this by adding extra channels into the channels field and separating them by commas. e.g:
> `channels: ["tsukle", "other", "channels"]`


------

# What now?
From here on you can use the `index.js` file that is included here to run a simple bot with a single command.

`tmi.js` also has documentation, using this you can find all of the necessary event functions and so on to create a fully functional bot.
I will also be updating the bot regularly with more functions and commands added with some extra features so eventually you are left with a fully built bot.

---

As it stands the bot works and you have a few functions in there to get you started, you can run it and it will work with the commands currently given. You can add more and change the commands by copying the IF command shown here:
> ```javascript
if(message === "Hello"){
  client.say("channel", " Hi! " + user["display-name"])
}
```

And pasting it below the current one to create a new command, all you need to do is change the trigger word "Hello" to anything you want and then change the response which is inside the second set of speech marks on the `client.say` line. The initial command uses the username of the person that sent the trigger message, you can keep this in the command or you can remove it by deleting ` + user["display-name"]`. You must make sure that you change the "channel" string to have the name of your channel in it, or use the channel array from the options variable if you are using multiple channels.

------

# How do I run it?
This entire twitch bot runs of Node alone, so all you need to do is open your Node command prompt or use your normal command prompt depending on which you chose at setup. You then need to navigate to the folder that your bot files are located and run it using:
> `node index.js`

If your bot uses a different file for example `bot.js` or another name, then you must use that filename in the node command instead. If there are no errors you will see a twitch connection message come up. And then you will see your chat start showing up (test this by typing a message in chat.).

------

# Overview
* You must have Node installed.
* You must install the tmi.js module.
* You must create a seperate account for your bot and create an OAuth key for it.

---
---
---
---


# Changelog
* 27/06/2016 - Initial Files.
