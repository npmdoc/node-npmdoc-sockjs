# api documentation for  [sockjs (v0.3.18)](https://github.com/sockjs/sockjs-node)  [![npm package](https://img.shields.io/npm/v/npmdoc-sockjs.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-sockjs) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-sockjs.svg)](https://travis-ci.org/npmdoc/node-npmdoc-sockjs)
#### SockJS-node is a server counterpart of SockJS-client a JavaScript library that provides a WebSocket-like object in the browser. SockJS gives you a coherent, cross-browser, Javascript API which creates a low latency, full duplex, cross-domain communication

[![NPM](https://nodei.co/npm/sockjs.png?downloads=true)](https://www.npmjs.com/package/sockjs)

[![apidoc](https://npmdoc.github.io/node-npmdoc-sockjs/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-sockjs_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-sockjs/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-sockjs/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-sockjs/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Marek Majkowski"
    },
    "bugs": {
        "url": "https://github.com/sockjs/sockjs-node/issues"
    },
    "contributors": [
        {
            "name": "Bryce Kahle",
            "email": "bkahle@gmail.com"
        },
        {
            "name": "Marek Majkowski",
            "email": "deadbeef@popcount.org"
        }
    ],
    "dependencies": {
        "faye-websocket": "^0.10.0",
        "uuid": "^2.0.2"
    },
    "description": "SockJS-node is a server counterpart of SockJS-client a JavaScript library that provides a WebSocket-like object in the browser. SockJS gives you a coherent, cross-browser, Javascript API which creates a low latency, full duplex, cross-domain communication",
    "devDependencies": {
        "coffee-script": "^1.8.0"
    },
    "directories": {},
    "dist": {
        "shasum": "d9b289316ca7df77595ef299e075f0f937eb4207",
        "tarball": "https://registry.npmjs.org/sockjs/-/sockjs-0.3.18.tgz"
    },
    "gitHead": "a0178fae57d1f70b7d375369e70ce15bd592442e",
    "homepage": "https://github.com/sockjs/sockjs-node",
    "keywords": [
        "websockets",
        "websocket"
    ],
    "license": "MIT",
    "main": "index",
    "maintainers": [
        {
            "name": "majek",
            "email": "majek04@gmail.com"
        },
        {
            "name": "msackman",
            "email": "matthew@rabbitmq.com"
        },
        {
            "name": "squaremo",
            "email": "mikeb@squaremobius.net"
        },
        {
            "name": "glasser",
            "email": "glasser@meteor.com"
        },
        {
            "name": "brycekahle",
            "email": "bkahle@gmail.com"
        }
    ],
    "name": "sockjs",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/sockjs/sockjs-node.git"
    },
    "scripts": {},
    "version": "0.3.18"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module sockjs](#apidoc.module.sockjs)
1.  [function <span class="apidocSignatureSpan">sockjs.</span>createServer (options)](#apidoc.element.sockjs.createServer)
1.  [function <span class="apidocSignatureSpan">sockjs.</span>listen (http_server, options)](#apidoc.element.sockjs.listen)
1.  object <span class="apidocSignatureSpan">sockjs.</span>transport
1.  object <span class="apidocSignatureSpan">sockjs.</span>utils
1.  object <span class="apidocSignatureSpan">sockjs.</span>webjs

#### [module sockjs.transport](#apidoc.module.sockjs.transport)
1.  [function <span class="apidocSignatureSpan">sockjs.transport.</span>GenericReceiver (thingy)](#apidoc.element.sockjs.transport.GenericReceiver)
1.  [function <span class="apidocSignatureSpan">sockjs.transport.</span>ResponseReceiver (request, response, options)](#apidoc.element.sockjs.transport.ResponseReceiver)
1.  [function <span class="apidocSignatureSpan">sockjs.transport.</span>Session (session_id1, server)](#apidoc.element.sockjs.transport.Session)
1.  [function <span class="apidocSignatureSpan">sockjs.transport.</span>SockJSConnection (_session)](#apidoc.element.sockjs.transport.SockJSConnection)
1.  [function <span class="apidocSignatureSpan">sockjs.transport.</span>Transport ()](#apidoc.element.sockjs.transport.Transport)
1.  [function <span class="apidocSignatureSpan">sockjs.transport.</span>register (req, server, receiver)](#apidoc.element.sockjs.transport.register)
1.  [function <span class="apidocSignatureSpan">sockjs.transport.</span>registerNoSession (req, server, receiver)](#apidoc.element.sockjs.transport.registerNoSession)

#### [module sockjs.utils](#apidoc.module.sockjs.utils)
1.  [function <span class="apidocSignatureSpan">sockjs.utils.</span>array_intersection (arr_a, arr_b)](#apidoc.element.sockjs.utils.array_intersection)
1.  [function <span class="apidocSignatureSpan">sockjs.utils.</span>buffer_concat (buf_a, buf_b)](#apidoc.element.sockjs.utils.buffer_concat)
1.  [function <span class="apidocSignatureSpan">sockjs.utils.</span>escape_selected (str, chars)](#apidoc.element.sockjs.utils.escape_selected)
1.  [function <span class="apidocSignatureSpan">sockjs.utils.</span>md5_hex (data)](#apidoc.element.sockjs.utils.md5_hex)
1.  [function <span class="apidocSignatureSpan">sockjs.utils.</span>objectExtend (dst, src)](#apidoc.element.sockjs.utils.objectExtend)
1.  [function <span class="apidocSignatureSpan">sockjs.utils.</span>overshadowListeners (ee, event, handler)](#apidoc.element.sockjs.utils.overshadowListeners)
1.  [function <span class="apidocSignatureSpan">sockjs.utils.</span>parseCookie (cookie_header)](#apidoc.element.sockjs.utils.parseCookie)
1.  [function <span class="apidocSignatureSpan">sockjs.utils.</span>quote (string)](#apidoc.element.sockjs.utils.quote)
1.  [function <span class="apidocSignatureSpan">sockjs.utils.</span>random32 ()](#apidoc.element.sockjs.utils.random32)
1.  [function <span class="apidocSignatureSpan">sockjs.utils.</span>sha1_base64 (data)](#apidoc.element.sockjs.utils.sha1_base64)
1.  [function <span class="apidocSignatureSpan">sockjs.utils.</span>timeout_chain (arr)](#apidoc.element.sockjs.utils.timeout_chain)

#### [module sockjs.webjs](#apidoc.module.sockjs.webjs)
1.  [function <span class="apidocSignatureSpan">sockjs.webjs.</span>GenericApp ()](#apidoc.element.sockjs.webjs.GenericApp)
1.  [function <span class="apidocSignatureSpan">sockjs.webjs.</span>generateHandler (app, dispatcher)](#apidoc.element.sockjs.webjs.generateHandler)



# <a name="apidoc.module.sockjs"></a>[module sockjs](#apidoc.module.sockjs)

#### <a name="apidoc.element.sockjs.createServer"></a>[function <span class="apidocSignatureSpan">sockjs.</span>createServer (options)](#apidoc.element.sockjs.createServer)
- description and source-code
```javascript
createServer = function (options) {
  return new Server(options);
}
```
- example usage
```shell
...

A simplified echo SockJS server could look more or less like:

'''javascript
var http = require('http');
var sockjs = require('sockjs');

var echo = sockjs.createServer({ sockjs_url: 'http://cdn.jsdelivr.net/sockjs/1.0.1/sockjs.min.js' });
echo.on('connection', function(conn) {
    conn.on('data', function(message) {
        conn.write(message);
    });
    conn.on('close', function() {});
});
...
```

#### <a name="apidoc.element.sockjs.listen"></a>[function <span class="apidocSignatureSpan">sockjs.</span>listen (http_server, options)](#apidoc.element.sockjs.listen)
- description and source-code
```javascript
listen = function (http_server, options) {
  var srv;
  srv = exports.createServer(options);
  if (http_server) {
    srv.installHandlers(http_server);
  }
  return srv;
}
```
- example usage
```shell
...
        conn.write(message);
    });
    conn.on('close', function() {});
});

var server = http.createServer();
echo.installHandlers(server, {prefix:'/echo'});
server.listen(9999, '0.0.0.0');
'''

(Take look at
[examples](https://github.com/sockjs/sockjs-node/tree/master/examples/echo)
directory for a complete version.)

Subscribe to
...
```



# <a name="apidoc.module.sockjs.transport"></a>[module sockjs.transport](#apidoc.module.sockjs.transport)

#### <a name="apidoc.element.sockjs.transport.GenericReceiver"></a>[function <span class="apidocSignatureSpan">sockjs.transport.</span>GenericReceiver (thingy)](#apidoc.element.sockjs.transport.GenericReceiver)
- description and source-code
```javascript
function GenericReceiver(thingy) {
  this.thingy = thingy;
  this.setUp(this.thingy);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sockjs.transport.ResponseReceiver"></a>[function <span class="apidocSignatureSpan">sockjs.transport.</span>ResponseReceiver (request, response, options)](#apidoc.element.sockjs.transport.ResponseReceiver)
- description and source-code
```javascript
function ResponseReceiver(request, response, options) {
  var x;
  this.request = request;
  this.response = response;
  this.options = options;
  this.curr_response_size = 0;
  try {
    this.request.connection.setKeepAlive(true, 5000);
  } catch (error) {
    x = error;
  }
  ResponseReceiver.__super__.constructor.call(this, this.request.connection);
  if (this.max_response_size === void 0) {
    this.max_response_size = this.options.response_limit;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sockjs.transport.Session"></a>[function <span class="apidocSignatureSpan">sockjs.transport.</span>Session (session_id1, server)](#apidoc.element.sockjs.transport.Session)
- description and source-code
```javascript
function Session(session_id1, server) {
  this.session_id = session_id1;
  this.heartbeat_delay = server.options.heartbeat_delay;
  this.disconnect_delay = server.options.disconnect_delay;
  this.prefix = server.options.prefix;
  this.send_buffer = [];
  this.is_closing = false;
  this.readyState = Transport.CONNECTING;
  if (this.session_id) {
    MAP[this.session_id] = this;
  }
  this.timeout_cb = (function(_this) {
    return function() {
      return _this.didTimeout();
    };
  })(this);
  this.to_tref = setTimeout(this.timeout_cb, this.disconnect_delay);
  this.connection = new SockJSConnection(this);
  this.emit_open = (function(_this) {
    return function() {
      _this.emit_open = null;
      return server.emit('connection', _this.connection);
    };
  })(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sockjs.transport.SockJSConnection"></a>[function <span class="apidocSignatureSpan">sockjs.transport.</span>SockJSConnection (_session)](#apidoc.element.sockjs.transport.SockJSConnection)
- description and source-code
```javascript
function SockJSConnection(_session) {
  this._session = _session;
  this.id = uuid.v4();
  this.headers = {};
  this.prefix = this._session.prefix;
}
```
- example usage
```shell
...
this.ws = ws1;
this.prefix = server.options.prefix;
this.readyState = Transport.OPEN;
this.recv = {
  connection: conn,
  protocol: "websocket-raw"
};
this.connection = new transport.SockJSConnection(this);
this.decorateConnection(req);
server.emit('connection', this.connection);
this._end_cb = (function(_this) {
  return function() {
    return _this.didClose();
  };
})(this);
...
```

#### <a name="apidoc.element.sockjs.transport.Transport"></a>[function <span class="apidocSignatureSpan">sockjs.transport.</span>Transport ()](#apidoc.element.sockjs.transport.Transport)
- description and source-code
```javascript
function Transport() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sockjs.transport.register"></a>[function <span class="apidocSignatureSpan">sockjs.transport.</span>register (req, server, receiver)](#apidoc.element.sockjs.transport.register)
- description and source-code
```javascript
register = function (req, server, receiver) {
  return register(req, server, req.session, receiver);
}
```
- example usage
```shell
...
      res.setHeader('Vary', 'Origin');
      headers = req.headers['access-control-request-headers'];
      if (headers) {
        res.setHeader('Access-Control-Allow-Headers', headers);
      }
      res.writeHead(200);
      res.write('\r\n');
      transport.register(req, this, new EventSourceReceiver(req, res, this.options));
      return true;
    }
  };

}).call(this);
...
```

#### <a name="apidoc.element.sockjs.transport.registerNoSession"></a>[function <span class="apidocSignatureSpan">sockjs.transport.</span>registerNoSession (req, server, receiver)](#apidoc.element.sockjs.transport.registerNoSession)
- description and source-code
```javascript
registerNoSession = function (req, server, receiver) {
  return register(req, server, void 0, receiver);
}
```
- example usage
```shell
...
},
sockjs_websocket: function(req, connection, head) {
  var ws;
  this._websocket_check(req, connection, head);
  ws = new FayeWebsocket(req, connection, head, null, this.options.faye_server_options);
  ws.onopen = (function(_this) {
    return function() {
      return transport.registerNoSession(req, _this, new WebSocketReceiver(ws, connection));
    };
  })(this);
  return true;
},
raw_websocket: function(req, connection, head) {
  var ver, ws;
  this._websocket_check(req, connection, head);
...
```



# <a name="apidoc.module.sockjs.utils"></a>[module sockjs.utils](#apidoc.module.sockjs.utils)

#### <a name="apidoc.element.sockjs.utils.array_intersection"></a>[function <span class="apidocSignatureSpan">sockjs.utils.</span>array_intersection (arr_a, arr_b)](#apidoc.element.sockjs.utils.array_intersection)
- description and source-code
```javascript
array_intersection = function (arr_a, arr_b) {
  var a, j, len, r;
  r = [];
  for (j = 0, len = arr_a.length; j < len; j++) {
    a = arr_a[j];
    if (arr_b.indexOf(a) !== -1) {
      r.push(a);
    }
  }
  return r;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sockjs.utils.buffer_concat"></a>[function <span class="apidocSignatureSpan">sockjs.utils.</span>buffer_concat (buf_a, buf_b)](#apidoc.element.sockjs.utils.buffer_concat)
- description and source-code
```javascript
buffer_concat = function (buf_a, buf_b) {
  var dst;
  dst = new Buffer(buf_a.length + buf_b.length);
  buf_a.copy(dst);
  buf_b.copy(dst, buf_a.length);
  return dst;
}
```
- example usage
```shell
...
};

GenericApp.prototype.expect_form = function(req, res, _data, next_filter) {
  var data;
  data = new Buffer(0);
  req.on('data', (function(_this) {
    return function(d) {
      return data = utils.buffer_concat(data, new Buffer(d, 'binary'));
    };
  })(this));
  req.on('end', (function(_this) {
    return function() {
      var q;
      data = data.toString('utf-8');
      switch ((req.headers['content-type'] || '').split(';')[0]) {
...
```

#### <a name="apidoc.element.sockjs.utils.escape_selected"></a>[function <span class="apidocSignatureSpan">sockjs.utils.</span>escape_selected (str, chars)](#apidoc.element.sockjs.utils.escape_selected)
- description and source-code
```javascript
escape_selected = function (str, chars) {
  var c, i, j, l, len, map, parts, r, ref, v;
  map = {};
  chars = '%' + chars;
  for (j = 0, len = chars.length; j < len; j++) {
    c = chars[j];
    map[c] = escape(c);
  }
  r = new RegExp('([' + chars + '])');
  parts = str.split(r);
  for (i = l = 0, ref = parts.length; 0 <= ref ? l < ref : l > ref; i = 0 <= ref ? ++l : --l) {
    v = parts[i];
    if (v.length === 1 && v in map) {
      parts[i] = map[v];
    }
  }
  return parts.join('');
}
```
- example usage
```shell
...
    return EventSourceReceiver.__super__.constructor.apply(this, arguments);
  }

  EventSourceReceiver.prototype.protocol = "eventsource";

  EventSourceReceiver.prototype.doSendFrame = function(payload) {
    var data;
    data = ['data: ', utils.escape_selected(payload, '\r\n\x00'), '\r\n\r\n'];
    return EventSourceReceiver.__super__.doSendFrame.call(this, data.join(''));
  };

  return EventSourceReceiver;

})(transport.ResponseReceiver);
...
```

#### <a name="apidoc.element.sockjs.utils.md5_hex"></a>[function <span class="apidocSignatureSpan">sockjs.utils.</span>md5_hex (data)](#apidoc.element.sockjs.utils.md5_hex)
- description and source-code
```javascript
md5_hex = function (data) {
  return crypto.createHash('md5').update(data).digest('hex');
}
```
- example usage
```shell
...
context = {
  '{{ sockjs_url }}': this.options.sockjs_url
};
content = iframe_template;
for (k in context) {
  content = content.replace(k, context[k]);
}
quoted_md5 = '"' + utils.md5_hex(content) + '"';
if ('if-none-match' in req.headers && req.headers['if-none-match'] === quoted_md5) {
  res.statusCode = 304;
  return '';
}
res.setHeader('Content-Type', 'text/html; charset=UTF-8');
res.setHeader('ETag', quoted_md5);
return content;
...
```

#### <a name="apidoc.element.sockjs.utils.objectExtend"></a>[function <span class="apidocSignatureSpan">sockjs.utils.</span>objectExtend (dst, src)](#apidoc.element.sockjs.utils.objectExtend)
- description and source-code
```javascript
objectExtend = function (dst, src) {
  var k;
  for (k in src) {
    if (src.hasOwnProperty(k)) {
      dst[k] = src[k];
    }
  }
  return dst;
}
```
- example usage
```shell
...
    res.writeHead = function(status, user_headers) {
var k, r, x;
if (user_headers == null) {
  user_headers = {};
}
r = [];
r.push('HTTP/' + req.httpVersion + ' ' + status + ' ' + http.STATUS_CODES[status]);
utils.objectExtend(headers, user_headers);
for (k in headers) {
  r.push(k + ': ' + headers[k]);
}
r = r.concat(['', '']);
try {
  res.write(r.join('\r\n'));
} catch (error1) {
...
```

#### <a name="apidoc.element.sockjs.utils.overshadowListeners"></a>[function <span class="apidocSignatureSpan">sockjs.utils.</span>overshadowListeners (ee, event, handler)](#apidoc.element.sockjs.utils.overshadowListeners)
- description and source-code
```javascript
overshadowListeners = function (ee, event, handler) {
  var new_handler, old_listeners;
  old_listeners = ee.listeners(event).slice(0);
  ee.removeAllListeners(event);
  new_handler = function() {
    var j, len, listener;
    if (handler.apply(this, arguments) !== true) {
      for (j = 0, len = old_listeners.length; j < len; j++) {
        listener = old_listeners[j];
        listener.apply(this, arguments);
      }
      return false;
    }
    return true;
  };
  return ee.addListener(event, new_handler);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sockjs.utils.parseCookie"></a>[function <span class="apidocSignatureSpan">sockjs.utils.</span>parseCookie (cookie_header)](#apidoc.element.sockjs.utils.parseCookie)
- description and source-code
```javascript
parseCookie = function (cookie_header) {
  var cookie, cookies, j, len, parts, ref;
  cookies = {};
  if (cookie_header) {
    ref = cookie_header.split(';');
    for (j = 0, len = ref.length; j < len; j++) {
      cookie = ref[j];
      parts = cookie.split('=');
      cookies[parts[0].trim()] = (parts[1] || '').trim();
    }
  }
  return cookies;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sockjs.utils.quote"></a>[function <span class="apidocSignatureSpan">sockjs.utils.</span>quote (string)](#apidoc.element.sockjs.utils.quote)
- description and source-code
```javascript
quote = function (string) {
  var quoted;
  quoted = JSON.stringify(string);
  escapable.lastIndex = 0;
  if (!escapable.test(quoted)) {
    return quoted;
  }
  return quoted.replace(escapable, function(a) {
    return lookup[a];
  });
}
```
- example usage
```shell
...
GenericReceiver.prototype.doSendBulk = function(messages) {
  var m, q_msgs;
  q_msgs = (function() {
    var i, len, results;
    results = [];
    for (i = 0, len = messages.length; i < len; i++) {
      m = messages[i];
      results.push(utils.quote(m));
    }
    return results;
  })();
  return this.doSendFrame('a' + '[' + q_msgs.join(',') + ']');
};

GenericReceiver.prototype.heartbeat = function() {
...
```

#### <a name="apidoc.element.sockjs.utils.random32"></a>[function <span class="apidocSignatureSpan">sockjs.utils.</span>random32 ()](#apidoc.element.sockjs.utils.random32)
- description and source-code
```javascript
random32 = function () {
  var foo, v;
  foo = crypto.randomBytes(4);
  v = [foo[0], foo[1], foo[2], foo[3]];
  return v[0] + (v[1] * 256) + (v[2] * 256 * 256) + (v[3] * 256 * 256 * 256);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sockjs.utils.sha1_base64"></a>[function <span class="apidocSignatureSpan">sockjs.utils.</span>sha1_base64 (data)](#apidoc.element.sockjs.utils.sha1_base64)
- description and source-code
```javascript
sha1_base64 = function (data) {
  return crypto.createHash('sha1').update(data).digest('base64');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sockjs.utils.timeout_chain"></a>[function <span class="apidocSignatureSpan">sockjs.utils.</span>timeout_chain (arr)](#apidoc.element.sockjs.utils.timeout_chain)
- description and source-code
```javascript
timeout_chain = function (arr) {
  var fun, ref, timeout, user_fun;
  arr = arr.slice(0);
  if (!arr.length) {
    return;
  }
  ref = arr.shift(), timeout = ref[0], user_fun = ref[1];
  fun = (function(_this) {
    return function() {
      user_fun();
      return exports.timeout_chain(arr);
    };
  })(this);
  return setTimeout(fun, timeout);
}
```
- example usage
```shell
...
  if (!arr.length) {
    return;
  }
  ref = arr.shift(), timeout = ref[0], user_fun = ref[1];
  fun = (function(_this) {
    return function() {
      user_fun();
      return exports.timeout_chain(arr);
    };
  })(this);
  return setTimeout(fun, timeout);
};

exports.objectExtend = function(dst, src) {
  var k;
...
```



# <a name="apidoc.module.sockjs.webjs"></a>[module sockjs.webjs](#apidoc.module.sockjs.webjs)

#### <a name="apidoc.element.sockjs.webjs.GenericApp"></a>[function <span class="apidocSignatureSpan">sockjs.webjs.</span>GenericApp ()](#apidoc.element.sockjs.webjs.GenericApp)
- description and source-code
```javascript
function GenericApp() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sockjs.webjs.generateHandler"></a>[function <span class="apidocSignatureSpan">sockjs.webjs.</span>generateHandler (app, dispatcher)](#apidoc.element.sockjs.webjs.generateHandler)
- description and source-code
```javascript
generateHandler = function (app, dispatcher) {
  return function(req, res, head) {
    var allowed_methods, found, funs, i, j, l, len, m, method, path, ref, row;
    if (typeof res.writeHead === "undefined") {
      fake_response(req, res);
    }
    utils.objectExtend(req, url.parse(req.url, true));
    req.start_date = new Date();
    found = false;
    allowed_methods = [];
    for (j = 0, len = dispatcher.length; j < len; j++) {
      row = dispatcher[j];
      method = row[0], path = row[1], funs = row[2];
      if (path.constructor !== Array) {
        path = [path];
      }
      m = req.pathname.match(path[0]);
      if (!m) {
        continue;
      }
      if (!req.method.match(new RegExp(method))) {
        allowed_methods.push(method);
        continue;
      }
      for (i = l = 1, ref = path.length; 1 <= ref ? l < ref : l > ref; i = 1 <= ref ? ++l : --l) {
        req[path[i]] = m[i];
      }
      funs = funs.slice(0);
      funs.push('log_request');
      req.next_filter = function(data) {
        return execute_request(app, funs, req, res, data);
      };
      req.next_filter(head);
      found = true;
      break;
    }
    if (!found) {
      if (allowed_methods.length !== 0) {
        app['handle_405'](req, res, allowed_methods);
      } else {
        app['handle_404'](req, res);
      }
      app['log_request'](req, res, true);
    }
  };
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
