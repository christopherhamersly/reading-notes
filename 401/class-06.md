# Class Six

## HTTP & REST

- HTTP (hyper text transfer protocol) is a stateless request-response application layer protocol.  HTTP is used to build distributed, collaborative, hypermedia information systems.

- HTTP is often associated with serving .html files, but is also used to transfer images, videos, .json, and .xml files. 

- A HTTP request is formatted in text and transferred using TCP.  The first line of the request contains the method, url and HTTP version.  The following lines are the request HEADERS. 

- HTTP Method	| Request Has Body	| Response Has Body |	Safe |	Idempotent |	Cacheable |	Function
GET	| No |	Yes |	Yes |	Yes |	Yes |	Retrieve a resource
HEAD | No |	No | Yes |	Yes |	Yes |	Like GET but headers only
POST |	Yes |	Yes |	No |	No |	Yes |	Create a resource
PUT	 | Yes | 	Yes |	No |	Yes |	No |	Update a resource
DELETE |	No |	Yes |	No |	Yes |	No |	Delete a resource
CONNECT |	Yes |	Yes |	No	| No |	No |	Create TCP/IP tunnel
OPTIONS |	Optional |	Yes |	Yes |	Yes |	No | Returns supported methods for a URL
TRACE	 | No |	Yes |	Yes |	Yes |	No |	Echos retrieved request
PATCH	| Yes |	Yes |	No |	No	| No |	Partial modification of resource

- HTTP Response 
  - A HTTP/1.1 response is also formatted in text and transferred using TCP. The first line of the response contains the HTTP VERSION, STATUS CODE, and STATUS MESSAGE. The following lines are the request headers and are formatted exactly the same way as the request headers. The header section of the request is terminated with an empty line. An optional body follows the header section.

- REST 
  - is acronym for REpresentational State Transfer. In layman’s terms, is a means by which we can reference, manipulate, and transfer state. Rest uses a common set of methods (called “verbs”) to operate on the state of a resource (“noun”), generally using HTTP as the transfer protocol.

- Guiding Principles of REST
  - Client–server – By separating the user interface concerns from the data storage concerns, we improve the portability of the user interface across multiple platforms and improve scalability by simplifying the server components.

  - Stateless – Each request from client to server must contain all of the information necessary to understand the request, and cannot take advantage of any stored context on the server. Session state is therefore kept entirely on the client.

  - Cacheable – Cache constraints require that the data within a response to a request be implicitly or explicitly labeled as cacheable or non-cacheable. If a response is cacheable, then a client cache is given the right to reuse that response data for later, equivalent requests.

  - Uniform interface – By applying the software engineering principle of generality to the component interface, the overall system architecture is simplified and the visibility of interactions is improved. In order to obtain a uniform interface, multiple architectural constraints are needed to guide the behavior of components. REST is defined by four interface constraints: identification of resources; manipulation of resources through representations; self-descriptive messages; and, hypermedia as the engine of application state.

  - Layered system – The layered system style allows an architecture to be composed of hierarchical layers by constraining component behavior such that each component cannot “see” beyond the immediate layer with which they are interacting.

  - Code on demand (optional) – REST allows client functionality to be extended by downloading and executing code in the form of applets or scripts. This simplifies clients by reducing the number of features required to be pre-implemented.

- REST Documentation (Swagger)
  - The standard for documenting REST APIs is with a “live” documentation system: Open API (formerly “Swagger”)

  - Once generated, Swagger Docs present developers a way not only see how to use an API, but to actually use it. Yes, this is documentation that allows for live requests from with it.

