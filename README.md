An asynchronous, realtime network logger for the browser (and Node.js).

# Server

Start the server. It will be available locally on port 3000.
Logs coming from the client will output on the console.

```
node dist/server.js
```

Note: there is no need to `npm install`, you only need a working, recent Node.js.

# Client

Add to the top of your HTML page's `head` section

```
<script src="https://unpkg.com/@shimaore/iolog/client-dist/client.js"></script>
```

It will automatically capture `console` and send it over the network to the
server-side.

# Advanced usage

`dist/client-lib.js` offers the functionality of the project for integration in
a custom scenario, for example if you need to override the server's location.

```
import { overrideConsole, start } from '@shimaore/iolog/dist/client-lib.js';
overrideConsole(start("https://logger.example.com"))
```
