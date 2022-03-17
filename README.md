How to install nodejs app in heroku

Prerequiriments:
 - node installed
 - code in githug
 - account in heroku

cd nodejs-helloworld
npm init

# package.json is generated

# Your package.json file will look something like this:

"engines": {
    "node": "14.x"
  },
  
Build your app and run it locally

npm install
heroku local web

How to keep build artifacts out of git

Prevent build artifacts from going into revision control by creating a .gitignore file that looks something like this:

/node_modules
npm-debug.log
.DS_Store
/*.env

Deploy your application to Heroku

git add .
git commit -m "Added a Procfile."
heroku login
Enter your Heroku credentials.
...
heroku create
Creating arcane-lowlands-8408... done, stack is cedar
http://arcane-lowlands-8408.herokuapp.com/ | git@heroku.com:arcane-lowlands-8408.git
Git remote heroku added
git push heroku main
...
-----> Node.js app detected
...
-----> Launching... done
       http://arcane-lowlands-8408.herokuapp.com deployed to Heroku
