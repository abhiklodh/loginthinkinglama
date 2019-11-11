# loginthinkinglama

### The Files

- app
>
>- models
>   - user.js - the user model 
>
>- routes.js - all the urls for the application
- config
>- database.js - database connection settings
>- passport.js - initialising funtions from passport
- package.json - list of dependencies
- server.js - setup the application

### Dependencies

- Express is the framework.
- Ejs is the templating engine.
- Mongoose is object modeling for our MongoDB database.
- Passport stuff will help us authenticating with different methods.
- Connect-flash allows for passing session flashdata messages.
- Bcrypt-nodejs gives us the ability to hash the password automatically.

### Methods

- Home Page (/)
- Login Page (/login)
- Signup Page (/signup)
- Handle the POST for both login
- Handle the POST for both signup
- Home Page (after logged in)
- isLoggedIn: Using route middleware, we can protect the profile section route. A user has to be logged in to access that route. Using the isLoggedIn function, we will kick a user back to the home page if they try to access http://localhost:8080/profile and they are not logged in.
- Logout: We will handle logout by using req.logout() provided by passport. After logging out, redirect the user to the home page.

### Instructions

- Install Homebrew (A package manager) by pasting the following command in the first terminal window
> `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
- Install Node.js by pasting the following command in the terminal
> `brew install node`
- Install Mongo.db by pasting the following command in the terminal
> `brew install mongodb`
- After downloading Mongo, create the “db” directory. This is where the Mongo data files will live. You can create the directory in the default location by running the following command in the terminal 
> `mkdir -p /data/db`
- Run the following command in the terminal to ensure proper permissions are provided to mongodb
> ``sudo chown -R `id -un` /data/db``
- Go to the base directory of this app from the terminal by running the following command in the terminal
> `cd UserName/downloads/loginthinkinglama-master`
- Run the following command in the terminal to install the dependencies
> `npm install`
- Run the following command in the terminal to install node daemon to allow the node server to restart itself if it detects file changes
> `npm install -g nodemon`
- Run the following command in a new (second) terminal window to start Mongo.db process
> `mongod`
- Run the following command in the first terminal window to start the Node.js app
> `nodemon server.js`
- Press the following in both the terminal windows to quit the Node server and Mongo.db server
> `control+c`
- Go to `localhost:8080`
