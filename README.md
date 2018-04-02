# socketio-scale-demo
Simple demo of using socket io redis adapter for scaling sockets

# How to use it
1. `npm install` 
2. Run `PORT=3000 node index.js` from one terminal
3. Run `PORT=3001 node index.js` from another terminal
4. Open both urls in browser and try typing some message on both. 
5. You can see that messages are sent between those server processes and displayed on web page.
6. Try to Remove 
```js
var redis = require('socket.io-redis');
io.adapter(redis({ host: 'localhost', port: 6379 }));
```
To see that in this case, the messages won't be sent to both server instances.
