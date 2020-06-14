# EJS 
1. First step - npm init 
1. then npm install express, body parser, cors, ejs
1. var express = require ('express);
1. var body parser = require('body parser');
1. var cors = require ('cors');
1. var path = require('path');
1. var expressLayouts = require('express-ejs-layouts');
1. var app = express();
1. app.use(bodyParser());
1. app.use(cors());
1. app.use(expressLayouts);
1. app.set('views', path.join__dirname, 'views'));
1. app.set('view engine', 'ejs');
1. app.get('/, function(request, response){
  response.render('index', {
    foo: 'bar'
  }); -- takes the name of the file, not the filepath. -- get route for the root directory. This is now making a variable call foo, that makes it available to use. 
})
1. then set up a new folder called views, set up a file called index.ejs.
1. app.listen(8000, function() {
  console.log('heard on 8000);
})
1. response. render takes in three parameters. 
1. this is helpful if you either have an API call or a delete call.  
1. you can also use this to manipulate arrays as well. 
1. this is super helpful if you have an < ul > that you need to manipulate. 
1. this gives us the ability to write an if/else statement as well, to make evaluations on the front end.  
1. layouts are not native to EJS.  it is useful to have layout file and have everything wrapped in it. 
1. npm install --S express.ejs.layouts is the way to install it into your file. 
1. 
