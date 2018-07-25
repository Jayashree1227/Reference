# Introduction

Ryan Dahl first introduction of Node.js

https://www.youtube.com/watch?v=jo_B4LTHi3I

---

## what is javascript inside nodejs?

functions, addition, numbers, strings, arrays, objects

---

## What is not javascript inside nodejs?

Networking, HTTP server, TCP server, stdout(printing the information from the server) - all these are not part of javascript

---

## What is node.js?

Node.js is a c++ application that embeds the v8 js engine

```Javascript
eg: #include <v8.h>
```

## To execute node:

```Javascript
node index.js
```

---

## Starting a http server

```Javascript

/* ----http server allows you to listen on ports and respond with data--- */

// Dependencies

var http = require('http');

/* ---- The server should respond to all request with a string --- */

var server = http.createServer(function(req,res){
	res.end('Hello World\n');
})

/* ----start the server, and have it listen on port 3000 ---- */

server.listen(3000,function(){
	console.log("The server is listening on port 3000");
})

```

/* ---- To run the program on command line ----*/

```Javascript
curl localhost:3000
```

---

## Parsing Request Paths - Using the URL library

```diff
/* ----------

+ The below code gets what URL has the user requested for. If the user has requested for http://xyz.com/admin/planet.html, the below code will identify that the user has requested for planet.html

---------*/
```


```Javascript

var http = require('http');
var url = require('url');


/* ---- The server should respond to all request with a string ----- */

var server = http.createServer(function(req,res){

/* -----when someone hit localhost:3000, the below function gets called and when each time this function gets called req and res is brand new every time. req object contains a whole bunch of information on what that user is asking for ------ */
	
/* ----- Get the URL and parse it ----*/

var parsedURL = url.parse(req.url, true); 
/* -------req.url will have the full URL what the user is asking for.
when you pass true it will call querystring.parse function which returns the query string 'foo=bar&abc=xyz&abc=123' returns as

{
   foo: 'bar',
   abc['xyz','123']
}  --------*/


/* -----Get the path from the URL -------*/

var path = parsedURL.pathname; /* ------- returns /admin/planet.html -> this is an untrimmed path ------ */

/* ----------To get the trimmed path -> this will trim unnecessary slashes(/) from the URL -------- */

var trimmedPath = path.replace(/^\/+|\/+$/g,'');

/* ------ Send the response ------- */
res.end('Hellow World\n');

/* -----Get print the path what the user has asked for ie. admin/planet.html -------*/
console.log('Request recieved on path: '+trimmedPath);

})

/* ---------- Start the server, and have it listen on port 3000 -------- */

server.listen(3000,function(){
	console.log("The server is listening on port 3000");
})

``` 

---

## Parsing HTTP Methods

