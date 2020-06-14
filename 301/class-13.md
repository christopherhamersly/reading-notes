# Sending Form Data
  1. Once the form data has been validated on the client-side, it is okay to submit the form
  1. Client/server architecture - 
    > At it's most basic, the web uses a client/server architecture that can be summarized as follows. a client (usually a web browser) sends a request to a server (most of the time a web server like Apache, Nginx, IIS, Tomcat, etc.), using the HTTP protocol. The server answers the request using the same protocol.
  1. An HTML form on a web page is nothing more than a convenient user-friendly way to configure an HTTP request to send data to a server. This enables the user to provide information to be delivered in the HTTP request.
  1.  The < form > element defines how the data will be sent. All of its attributes are designed to let you configure the request to be sent when a user hits a submit button. The two most important attributes are action and method.
  1. The action attribute defines where the data gets sent. Its value must be a valid relative or absolute URL. If this attribute isn't provided, the data will be sent to the URL of the page containing the form — the current page.
  1. The names and values of the non-file form controls are sent to the server as name=value pairs joined with ampersands. The action value should be a file on the server that can handle the incoming data, including ensuring server-side validation. The server then responds, generally handling the data and loading the URL defined by the action attribute, causing a new page load (or a refresh of the existing page, if the action points to the same page).
  1. The method attribute defines how data is sent. The HTTP protocol provides several ways to perform a request; HTML form data can be transmitted via a number of different methods, the most common being the GET method and the POST method
  1. The GET method is the method used by the browser to ask the server to send back a given resource: "Hey server, I want to get this resource." In this case, the browser sends an empty body. Because the body is empty, if a form is sent using this method the data sent to the server is appended to the URL.
  1. The POST method is a little different. It's the method the browser uses to talk to the server when asking for a response that takes into account the data provided in the body of the HTTP request: "Hey server, take a look at this data and send me back an appropriate result." If a form is sent using this method, the data is appended to the body of the HTTP request.
  1. HTTP requests are never displayed to the user (if you want to see them, you need to use tools such as the Firefox Network Monitor or the Chrome Developer Tools). As an example, your form data will be shown as follows in the Chrome Network tab. After submitting the form:
  1. Whichever HTTP method you choose, the server receives a string that will be parsed in order to get the data as a list of key/value pairs. The way you access this list depends on the development platform you use and on any specific frameworks you may be using with it.
  1. PHP offers some global objects to access the data. Assuming you've used the POST method, the following example just takes the data and displays it to the user. Of course, what you do with the data is up to you. You might display it, store it into a database, send it by email, or process it in some other way.
  1. form.html: The same form as we saw above in the The POST method section but with the action set to {{ url_for('hello') }}. This is a Jinja2 template, which is basically HTML but can contain calls to the Python code that is running the web server contained in curly braces. url_for('hello') is basically saying "redirect to /hello when the form is submitted".
  1. greeting.html: This template just contains a line that renders the two bits of data passed to it when it is rendered. This is done via the hello() function seen above, which runs when the /hello URL is navigated to.
  1. Each time you send data to a server, you need to consider security. HTML forms are by far the most common server attack vectors (places where attacks can occur). The problems never come from the HTML forms themselves — they come from how the server handles data.


## HTML5 forms
  1. name - Defines the unique identifier for that button within the form. It allows the server to access each button's value when submitted.
  1. value - The value sent to the server when submitting the form
  1. type - Defines the button type.
  1. fieldset - Defines a group of controls within a form.
  1. form - Defines an interactive form with controls.
  1. input - Defines an interactive control within a web form.
  1. legend - Defines a caption for a parent's content.
  1. textarea - Defines a multi-line text control within a web form.
  1. 