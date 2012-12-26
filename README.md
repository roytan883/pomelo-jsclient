#Pomelo javascript client

The javascript client libary for [Pomelo](https://github.com/NetEase/pomelo)


##Usage

### connect to the server
``` javascript
  pomelo.init(params, callback);
```
example:
``` javascript
  pomelo.init({
    host: host,
    port: port,
    log: true
  }, function() {
    console.log('success');
  });
```

### send request to server with callback
``` javascript
  pomelo.request(route, params, callback);
```

example:
``` javascript
	pomelo.request(route, {
		rid: rid
	}, function(data) {
    console.log(dta);	
	});
```

### send request to server without callback
``` javascript
  pomelo.notify(route, params);
```

### receive message from server 
``` javascript
  pomelo.on(route, callback); 
```

example: 
``` javascript
	pomelo.on('onChat', function(data) {
		addMessage(data.from, data.target, data.msg);
		$("#chatHistory").show();
	});
```


##License
(The MIT License)

Copyright (c) 2012 Netease, Inc. and other contributors

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the 'Software'), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
