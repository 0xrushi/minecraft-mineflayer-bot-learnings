# minecraft-mineflayer-bot-learnings

Now Microsoft moved all mojang accounts to Microsofts

```javascript
const bot = mineflayer.createBot({
  host: 'localhost', // server host
  port: 25565,
  version: "1.17.1",
  username: "noob@gmail.com", // microsoft email, fake name works for offline servers
  auth: "microsoft" // microsoft for microsoft account
  // password: "yourpasswored" // keep this commented for microsoft
})
```

### See what your bot is doing

Thanks to the [prismarine-viewer](https://github.com/PrismarineJS/prismarine-viewer) project, it's possible to display in a browser window what your bot is doing.
Just run `npm install prismarine-viewer` and add this to your bot:
```js
const { mineflayer: mineflayerViewer } = require('prismarine-viewer')
bot.once('spawn', () => {
  mineflayerViewer(bot, { port: 3007, firstPerson: true }) // port is the minecraft server port, if first person is false, you get a bird's-eye view
})
```
And you'll get a *live* view looking like this:

[<img src="https://prismarine.js.org/prismarine-viewer/test_1.16.1.png" alt="viewer" width="500">](https://prismarine.js.org/prismarine-viewer/)


# LIBS 
- Provides minecraft block names depending on the minecraft version https://github.com/PrismarineJS/minecraft-data   
- A simple utility plugin for Mineflayer that add a higher level API for collecting blocks. https://github.com/PrismarineJS/mineflayer-collectblock
- A tool/weapon selection Mineflayer plugin for automatically selecting the best tool to use for a specific task. https://github.com/PrismarineJS/mineflayer-tool