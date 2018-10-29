# ownserver

Unicon Study 2018 da berilgan uy vazifaga qilingan micro framework.

```javascript
const http = require('http');
const finalhandler = require('finalhandler');
const Server = require('../');
const server = new Server();

server.get('/', (req, res) => {
    res.end('This is main page')
  })

server.get('/:1/:2', (args, req, res, err) => {
    res.end('This is main page', args[1], args[2]);
  });

server.post('/:1/:2', (args, req, res, err) => {
    res.end("this is sparta!!");
  });

http.createServer(function(req, res) {
  server(req, res, finalhandler(req, res))
}).listen(3000);

```

example papkasida ham bor..
