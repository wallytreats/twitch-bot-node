## Twitch Bot
This is a Twitch Bot created with NodeJS using the tmi.js module.

------

## What do I need?
You will need:
* [NodeJS](https://nodejs.org/en/)
* [TMI.JS](https://tmijs.org/)
* A text/script editor of choice (I strongly recommend [Atom](https://atom.io/), Notepad will work just fine though.)

------

## Where do I begin?
Well the first thing you need once you have installed Node, is you must install the tmi.js library wherever you will be keeping the rest of the files.

So for example if you are keeping these files in C:/Users/"Your_Username"/Desktop, you would cd (change directory) into your desktop and then run this command.
> `npm install --save tmi.js`

After running this command you will notice a `node_modules` folder which will have another folder inside named `tmi.js`.
This is good, if you have this, that means you are setup and ready to continue.

------

## What now?
From here on you can use the `index.js` file that is included here to run a simple bot with a single command.

`tmi.js` also has documentation, using this you can find all of the necessary event functions and so on to create a fully functional bot.
I will also be updating the bot regularly with more functions and commands added with some extra features so eventually you are left with a fully built bot.

As it stands the bot works. You can copy the if command inside the chat function and paste it underneath the current one to create another command, you can do this to make as many as you wish.
