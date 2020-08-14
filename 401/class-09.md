# Class Nine

## Express Server Routing

- express()
  - Creates an Express application. The express() function is a top-level function exported by the express module.

- express.json([options])
  - This is a built-in middleware function in Express. It parses incoming requests with JSON payloads and is based on body-parser.
  - Returns middleware that only parses JSON and only looks at requests where the Content-Type header matches the type option. This parser accepts any Unicode encoding of the body and supports automatic inflation of gzip and deflate encodings.

  - The following table describes the properties of the optional options object.

Property |	Description	| Type |	Default

inflate	| Enables or disables handling deflated (compressed) bodies; when disabled, deflated bodies are rejected.	| Boolean |	true

limit	| Controls the maximum request body size. If this is a number, then the value specifies the number of bytes; if it is a string, the value is passed to the bytes library for parsing. |	Mixed |	"100kb"

reviver	| The reviver option is passed directly to JSON.parse as the second argument. You can find more information on this argument in the MDN documentation about JSON.parse. |	Function |	null

strict |	Enables or disables only accepting arrays and objects; when disabled will accept anything JSON.parse accepts.	Boolean	true

type |	This is used to determine what media type the middleware will parse. This option can be a string, array of strings, or a function. If not a function, type option is passed directly to the type-is library and this can be an extension name (like json), a mime type (like application/json), or a mime type with a wildcard (like */* or */json). If a function, thetype option is called as fn(req) and the request is parsed if it returns a truthy value.	| Mixed	| "application/json"

verify |	This option, if supplied, is called as verify(req, res, buf, encoding), where buf is a Buffer of the raw request body and encoding is the encoding of the request. The parsing can be aborted by throwing an error.	| Function |	undefined

- express.raw([options])
  - This is a built-in middleware function in Express. It parses incoming request payloads into a Buffer and is based on body-parser.
  - Returns middleware that parses all bodies as a Buffer and only looks at requests where the Content-Type header matches the type option. This parser accepts any Unicode encoding of the body and supports automatic inflation of gzip and deflate encodings.

Property |	Description |	Type |	Default
inflate	| Enables or disables handling deflated (compressed) bodies; when disabled, deflated bodies are rejected.	| Boolean	 | true

limit	| Controls the maximum request body size. If this is a number, then the value specifies the number of bytes; if it is a string, the value is passed to the bytes library for parsing. |	Mixed	| "100kb"

type	| This is used to determine what media type the middleware will parse. This option can be a string, array of strings, or a function. If not a function, type option is passed directly to the type-is library and this can be an extension name (like bin), a mime type (like application/octet-stream), or a mime type with a wildcard (like */* or application/*). If a function, the type option is called as fn(req) and the request is parsed if it returns a truthy value.	| Mixed	| "application/octet-stream"

verify	| This option, if supplied, is called as verify(req, res, buf, encoding), where buf is a Buffer of the raw request body and encoding is the encoding of the request. The parsing can be aborted by throwing an error.	| Function	| undefined

express.static(root, [options])
  - This is a built-in middleware function in Express. It serves static files and is based on serve-static.

Property	| Description	| Type	| Default
dotfiles	| Determines how dotfiles (files or directories that begin with a dot “.”) are treated. |	String |	“ignore”
etag	| Enable or disable etag generation
NOTE: express.static always sends weak ETags.	| Boolean	| true
extensions |	Sets file extension fallbacks: If a file is not found, search for files with the specified extensions and serve the first one found. Example: ['html', 'htm'].	| Mixed	| false
fallthrough	| Let client errors fall-through as unhandled requests, otherwise forward a client error.	| Boolean	| true
immutable	| Enable or disable the immutable directive in the Cache-Control response header. If enabled, the maxAge option should also be specified to enable caching. The immutable directive will prevent supported clients from making conditional requests during the life of the maxAge option to check if the file has changed.	| Boolean	| false
index	| Sends the specified directory index file. Set to false to disable directory indexing.	| Mixed	| “index.html”
lastModified	| Set the Last-Modified header to the last modified date of the file on the OS.	| Boolean	| true
maxAge	| Set the max-age property of the Cache-Control header in milliseconds or a string in ms format. |	Number |	0
redirect	| Redirect to trailing “/” when the pathname is a directory. |	Boolean |	true
setHeaders |	Function for setting HTTP headers to serve with the file.
| Function	 

express.text([options])
  - This is a built-in middleware function in Express. It parses incoming request payloads into a string and is based on body-parser.

Returns middleware that parses all bodies as a string and only looks at requests where the Content-Type header matches the type option. This parser accepts any Unicode encoding of the body and supports automatic inflation of gzip and deflate encodings.

Property | 	Description	| Type	| Default
defaultCharset	| Specify the default character set for the text content if the charset is not specified in the Content-Type header of the request.	String | 	"utf-8" | 
inflate	| Enables or disables handling deflated (compressed) bodies; when disabled, deflated bodies are rejected.	| Boolean	| true

limit	| Controls the maximum request body size. If this is a number, then the value specifies the number of bytes; if it is a string, the value is passed to the bytes library for parsing.	| Mixed	| "100kb"

type	| This is used to determine what media type the middleware will parse. This option can be a string, array of strings, or a function. If not a function, type option is passed directly to the type-is library and this can be an extension name (like txt), a mime type (like text/plain), or a mime type with a wildcard (like */* or text/*). If a function, the type option is called as fn(req) and the request is parsed if it returns a truthy value.	| Mixed	| "text/plain"

verify | This option, if supplied, is called as verify(req, res, buf, encoding), where buf is a Buffer of the raw request body and encoding is the encoding of the request. The parsing can be aborted by throwing an error.	| Function |	undefined

express.urlencoded([options])
  - This is a built-in middleware function in Express. It parses incoming requests with urlencoded payloads and is based on body-parser.

  - Returns middleware that only parses urlencoded bodies and only looks at requests where the Content-Type header matches the type option. This parser accepts only UTF-8 encoding of the body and supports automatic inflation of gzip and deflate encodings.

- app.locals
  - The app.locals object has properties that are local variables within the application.

- app.mountpath
  - The app.mountpath property contains one or more path patterns on which a sub-app was mounted.

- app.on('mount', callback(parent))
  - The mount event is fired on a sub-app, when it is mounted on a parent app. The parent app is passed to the callback function.

- app.all(path, callback [, callback ...])
  - This method is like the standard app.METHOD() methods, except it matches all HTTP verbs.

- app.delete(path, callback [, callback ...])
  - Routes HTTP DELETE requests to the specified path with the specified callback functions. 










