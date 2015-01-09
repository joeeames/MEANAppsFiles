MEANAppsFiles
=============
This course is out of date. 

## Express Changes
The latest version of express has deprecated the body parser middleware.

That means that when you see the following line of code:
```
app.use(bodyParser.json());
```
you should instead use the following two lines of code:
```
app.use(bodyParser.urlencoded({extended: true}));
app.use(bodyParser.json());
```

The latest version of express has also changed the session middleware a little bit and now requires that you explicitly specify a value for the resave parameter and the saveUninitialized parameter. So in the module on authentication when you see the following code:
```
app.use(session({secret: 'multi vision unicorns'}))
```
you should instead use the following code:
```
app.use(session({secret: 'multi vision unicorns',resave:false,saveUninitialized:false}));
```

## Angular Changes
In addition to that, Angular 1.3 now requires a base tag when using html5Mode routing. In your layout.jade file (and maybe earlier in your index.jade), in the head you should place the following line of code:
```
base(href="/")
```

## MongoDB Changes
Current versions of MongoDB require a "query" when calling the remove function. So periodically in the course we will delete all the users from the db with the following command:
```
db.users.remove()
```
But instead, you need to pass an empty "query object" into the remove function like this:
```
db.users.remove({})
```

Notes:
To run the node server, type "node web-server.js" or "nodemon web-server.js" from the directory that contains the web-server.js file
