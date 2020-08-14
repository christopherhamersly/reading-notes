# Class Six

## Express Servers

- Express Routing
   -  Event driven system
      app.get('/thing', (req,res) => {})
      This is the same pattern we see in Vanilla JS, jQuery
      ‘When a get event happens in our server, on “/thing”, run this function…’
- The Request Object
  - (req,..)
  - /:parameters
      - app.get('/api/:thing',...) = req.params.thing
  - Query Strings
    - http://server/route?ball=round = req.query.ball
- The Response Object
  - (..., res)
  - Responsible for sending data back to the browser
  - Has methods like send() and status() that Express uses to format the output to the browser properly
  - Sends Headers
  - Cookies
  - Status Codes

- Express is a routing and middleware web framework that has minimal functionality of its own: An Express application is essentially a series of middleware function calls.

- Middleware functions can perform the following tasks:

  - Execute any code.
  - Make changes to the request and the response objects.
  - End the request-response cycle.
  - Call the next middleware function in the stack.

- An Express application can use the following types of middleware:

  - Application-level middleware
  - Router-level middleware
  - Error-handling middleware
  - Built-in middleware
  - Third-party middleware

- Routing refers to how an application’s endpoints (URIs) respond to client requests. For an introduction to routing, see Basic routing.

  - You define routing using methods of the Express app object that correspond to HTTP methods; for example, app.get() to handle GET requests and app.post to handle POST requests. For a full list, see app.METHOD. You can also use app.all() to handle all HTTP methods and app.use() to specify middleware as the callback function.

- A route method is derived from one of the HTTP methods, and is attached to an instance of the express class.

- Express supports methods that correspond to all HTTP request methods: get, post, and so on. For a full list, see app.METHOD.

HTTP Status Codes 
- 1xx Informational
- 100 Continue
- 101 Switching Protocols
- 102 Processing (WebDAV)
- 2xx Success
- 200 OK
- 201 Created
- 202 Accepted
- 203 Non-Authoritative Information
- 204 No Content
- 205 Reset Content
- 206 Partial Content
- 207 Multi-Status (WebDAV)
- 208 Already Reported (WebDAV)
- 226 IM Used
- 3xx Redirection
- 300 Multiple Choices
- 301 Moved Permanently
- 302 Found
- 303 See Other
- 304 Not Modified
- 305 Use Proxy
- 306 (Unused)
- 307 Temporary Redirect
- 308 Permanent Redirect (experimental)
- 4xx Client Error
- 400 Bad Request
- 401 Unauthorized
- 402 Payment Required
- 403 Forbidden
- 404 Not Found
- 405 Method Not Allowed
- 406 Not Acceptable
- 407 Proxy Authentication Required
- 408 Request Timeout
- 409 Conflict
- 410 Gone
- 411 Length Required
- 412 Precondition Failed
- 413 Request Entity Too Large
- 414 Request-URI Too Long
- 415 Unsupported Media Type
- 416 Requested Range Not Satisfiable
- 417 Expectation Failed
- 418 I'm a teapot (RFC 2324)
- 420 Enhance Your Calm (Twitter)
- 422 Unprocessable Entity (WebDAV)
- 423 Locked (WebDAV)
- 424 Failed Dependency (WebDAV)
- 425 Reserved for WebDAV
- 426 Upgrade Required
- 428 Precondition Required
- 429 Too Many Requests
- 431 Request Header Fields Too Large
- 444 No Response (Nginx)
- 449 Retry With (Microsoft)
- 450 Blocked by Windows Parental Controls (Microsoft)
- 451 Unavailable For Legal Reasons
- 499 Client Closed Request (Nginx)
- 5xx Server Error
- 500 Internal Server Error
- 501 Not Implemented
- 502 Bad Gateway
- 503 Service Unavailable
- 504 Gateway Timeout
- 505 HTTP Version Not Supported
- 506 Variant Also Negotiates (Experimental)
- 507 Insufficient Storage (WebDAV)
- 508 Loop Detected (WebDAV)
- 509 Bandwidth Limit Exceeded (Apache)
- 510 Not Extended
- 511 Network Authentication Required
- 598 Network read timeout error
- 599 Network connect timeout error


