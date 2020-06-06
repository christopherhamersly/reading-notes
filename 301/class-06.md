# Node, Express, and API's
  > What is node and when should I use it?
  > Node.js is a javascriript runtime built on Chrome's V8 Javascript engine. It is also an event based, non-blocking, asynchronous I/O runtime that uses Google's V8 javascript engine and libuv library. 
  > The V8 engine is the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers, including Brave, Opera, and Vivaldi. It was designed with performance in mind and is responsible for compiling JavaScript directly to native machine code that your computer can execute.
  > Node.js is a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.
  > You can check that Node is installed on your system by opening a terminal and typing node -v. If all has gone well, you should see something like v12.14.1 displayed. This is the current LTS version at the time of writing.
  > Next, create a new file hello.js and copy in the following code:
    >console.log("Hello, World!");
  >This uses Node’s built-in console module to display a message in a terminal window. To run the example, enter the following command:
    >node hello.js
  > If Node.js is configured properly, “Hello, World!” will be displayed.
  > Introducing npm, the JavaScript Package Manager
    > In addition to being the package manager for JavaScript, npm is also the world’s largest software registry. There are over 1,000,000 packages of JavaScript code available to download, with billions of downloads per week. Let’s take a quick look at how we would use npm to install a package.
  >Installing a Package Globally
    >Open your terminal and type the following:
      > npm install -g jshint
    >This will install the jshint package globally on your system. We can use it to lint the index.js file from the previous example:
      >jshint index.js
    >You should now see a number of ES6-related errors. If you want to fix them up, add /* jshint esversion: 6 */ to the top of the index.js file, re-run the command and linting should pass.
    nstalling a Package Locally
  > We can also install packages locally to a project, as opposed to globally, on our system. Create a test folder and open a terminal in that directory. Next type this:
    >npm init -y
  >This will create and auto-populate a package.json file in the same folder. Next, use npm to install the lodash package and save it as a project dependency:
    >npm install lodash --save
  >Create a file named test.js and add the following:
    >const _ = require('lodash');
    const arr = [0, 1, false, 2, '', 3];
    console.log(_.compact(arr));
  >Finally, run the script using node test.js. You should see [ 1, 2, 3 ] output to the terminal.
  1. If you look at the contents of the test directory, you’ll notice a folder entitled node_modules. This is where npm has saved lodash and any libraries that lodash depends on. The node_modules folder shouldn’t be checked in to version control, and can, in fact, be re-created at any time by running npm install from within the project’s root.
  1. If you open the package.json file, you’ll see lodash listed under the dependencies field. By specifying your project’s dependencies in this way, you allow any developer anywhere to clone your project and use npm to install whatever packages it needs to run.
  > If you want to start developing apps with any modern JavaScript framework (for example, React or Angular), you’ll be expected to have a working knowledge of Node and npm (or maybe Yarn).
  > Node.js Lets Us Run JavaScript on the Server.
  > The Node.js Execution Model
  1. In very simplistic terms, when you connect to a traditional server, such as Apache, it will spawn a new thread to handle the request. In a language such as PHP or Ruby, any subsequent I/O operations (for example, interacting with a database) block the execution of your code until the operation has completed. That is, the server has to wait for the database lookup to complete before it can move on to processing the result.
  > The fact that Node runs in a single thread does impose some limitations. For example, blocking I/O calls should be avoided, CPU-intensive operations should be handed off to a worker thread, and errors should always be handled correctly for fear of crashing the entire process.
  > Node is particularly suited to building applications that require some form of real-time interaction or collaboration — for example, chat sites, or apps such as CodeShare, where you can watch a document being edited live by someone else
  > Aside from speed and scalability, an often-touted advantage of using JavaScript on a web server — as well as in the browser — is that your brain no longer needs to switch modes. You can do everything in the same language, which, as a developer, makes you more productive (and hopefully, happier). For example, you can easily share code between the server and the client.
  > Another of Node’s big pluses is that it speaks JSON. JSON is probably the most important data exchange format on the Web, and the lingua franca for interacting with object databases (such as MongoDB). JSON is ideally suited for consumption by a JavaScript program, meaning that when you’re working with Node, data can flow neatly between layers without the need for reformatting. You can have one syntax from browser to server to database.
  