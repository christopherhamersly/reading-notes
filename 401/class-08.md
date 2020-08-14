# Class Eight

## Express Server Routing

- Routing 
  - refers to how an application’s endpoints (URIs) respond to client requests
    - These routing methods specify a callback function (sometimes called “handler functions”) called when the application receives a request to the specified route (endpoint) and HTTP method.

- Route methods
  - A route method is derived from one of the HTTP methods, and is attached to an instance of the express class.  
  - Express supports methods that correspond to all HTTP request methods: get, post, and so on.
  
- Route paths
  - Route paths, in combination with a request method, define the endpoints at which requests can be made. Route paths can be strings, string patterns, or regular expressions.

- Route parameters
  - Route parameters are named URL segments that are used to capture the values specified at their position in the URL. The captured values are populated in the req.params object, with the name of the route parameter specified in the path as their respective keys.

- Route handlers
  - You can provide multiple callback functions that behave like middleware to handle a request. The only exception is that these callbacks might invoke next('route') to bypass the remaining route callbacks

- Some Examples of code to get you started

    var express = require('exppress);
    var app = express()

    //respond with "hello world" when a GET request is made to the homepage

    app.get('/', function(req, res){
    res.send('hello world)
    })

  ***
    This will match requests to the root route
      app.get('/', function (request, response) {
      respond.send('root')
    })

  ***
  This will match requests to /about
      app.get('/about', function (request, response) {
      respond.send('about')
    })



