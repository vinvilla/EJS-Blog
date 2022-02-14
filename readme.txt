TERMINAL
* When you first open Terminal Type : bash
* Go to ~/
* Run every time you make change to  bash_profile file……     ==> source ~/.bash_profile


1. Run "npm init"
2. Run "npm i express body-parser"
3. Run - "npm i ejs"
4. Run "npm i"
5.  Copy and paste this into the app.js
          //jshint esversion:6

          const express = require("express");
          const bodyParser = require("body-parser");

          const app = express();

          app.get("/", function(req, res){
            res.send("Hello");
          });

          app.listen(3000, function(){
            console.log("Server started on port 3000.");
          });
6. To run code: "nodemon app.js"


TERMINAL
brew services restart <mongodb-community@4.4>
brew services start mongodb-community@5.0
brew services restart mongodb-community@5.0

launchctl unload -w ~/Library/LaunchAgents/homebrew.mxcl.mongodb-community.plist
launchctl load -w ~/Library/LaunchAgents/homebrew.mxcl.mongodb-community.plist

sudo chown -R $(whoami) $(brew --prefix)/*
brew services restart mongodb-community
mongod
mongod-status


node app.js


1. Run the following to run MongoDB as a background service.
    brew services run mongodb-community

2. Open another terminal Cntrl + T and from Fruits DB directory,
  node app.js
  you should see this: Connnected successfully to server

3. to check if mongoDb is running
  brew services list

4. to stop running mongoDB
brew services stop mongodb-community

alias mongod='brew services run mongodb-community'
alias mongod-status='brew services list'
alias mongod-stop='brew services stop mongodb-community'

alias mongod-cli='mongod --dbpath /usr/local/var/mongodb --logpath /usr/local/var/log/mongodb/mongo.log --fork'
alias mongod-kill='sudo pkill -f mongod'
