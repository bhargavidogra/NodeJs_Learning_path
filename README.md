# NodeJs_Learning_path
Refrence : https://www.linkedin.com/learning/node-js-essential-training-3/


What is NodeJs?
An Asynchronous event driven JavaScript runtime,Node is designed to build scalable network applications.


Basic Theory :

Node's Async Nature

  Node is event loop based i.e it is 'single threaded' environment and is made use of based on callback functions.

  Promises and replacment of promise with Async/Await
  
  EventEmitter :  emitter.emit()   emitter.on() 
     
     Example : emitter.emit('data','Hello World!')
               emitter.on('data',(msg)=>{
                   console.log(msg);   //prints the data Hello World
               })    


Streams:
  
  Readable Streams :
   Events: readable,data,end,error
   Methods:read,pause,resume,destroy
   Properties:readable,readableLength
 
  Writable Streams :
   Events:drain,close,finish,error
   Methods:write,destroy,end
   Properties:writable,writableLength
  Piping Streams and chaning then with file stream(fs) to import export file data could be useful.



NPM (Node Package Manager)
A package Repository to install third party modules and a command line Application

npm init -initializing project 

npm install - Adding Dependencies




Express - A very powerful middleware,routing and templating Engine.



Testing frame works mocha, chai testing assertion liberary,sinon for spies,stubs and mocks in sinonjs.org and istanbul for code coverage.

  



Basic Learning Topics:

Refrence - https://www.linkedin.com/learning/node-js-essential-training-3/

 1 Global object
 2 Require Function to get any file module into your code.eg getting the path from node module and using it to get the directory or filename. eg global.js
 3 Process object -process.argv eg globalProcess.js

 4 Standard Input and output - process.stdout  ,process.stdin  .Both are streams for reading and writing. Time out in intervals.



 NodeJs Core Module Topics:(Example Code : Core.js)

  1 path module: used to join path by - path.join(__dirname,'filename_to_concat');

  2 util module: log in this is more powerful than consolelog as it logs the date as well but we need to require this module.

  3 v8 module : to get the memory usage statstics. 

  4 ReadLine module :helps to read data form console .eg ask.js

  5 File System Basics 
    readFileSync -For reading files Syncronously
    readFile - For reading file Async by using a call back 
    ex code -readFile.js reads ReadMe.md
     
     if we want to read binary file we do not give UTF-8 as argument value
      
      writefile module used for writing data into file Asyncronously.eg writeFile.js

      creating directory using fs use of mkdir  for creation of directory.eg directory.js

      fs.appendFile() - to append file 

      fs.renameSync() or fs.rename()

  Streams 

  Readable File Streams:




Creation of your own modules and exporting them in other file for usage in code .eg myModule is  imported in app.js


Event Emitter 
   These are imported by importing the events into the code and they are async in nature and are emitted on call mainly. 





NPM
  NODE PACKAGE MANAGER

          node -v  =for getting node version

          package.json file for installing dependecies.

          npm init - for initailzing the node command package.json declaration important if you are going to publish the npm package.

          Syntax for installing any package:
            npm install package_name.
             eg -npm install express babel --save (to install as dev tools not to be included in production environment but used thoughout the production environment)
        At times installing thing globaly from inside some module may cause error so in that case you need to use :  sudo npm install -g package_name 
        Here it may promt to enter the machine pwd.

        npm outdated -g // checking the package vaersion
        update the package(to newest version) by simply typing 
                    npm install package_name
        in case it has to be globally installed : 
                   sudo npm install package_name


        Removing the package:
            npm uninstall package_name --save-dev

        Semantic versions:
           ^1.4.2   OR `1.4.2
            1->Major releases
            4->Minor releases
            2-> Patch releases
            ^ -> Caret All minor and patches OK ^1.X.X
            ` ->All patches only `1.4.X
          Control versions by removing ^ or `


         Package-lock.json
            when you share your project with some one make share to include it . This file will garantee to install same packages as per your project to run in any environment.
        
        NPM Cache 
          npm keeps a cache for installing any kind of packages or something.

          use cmd : npm cache verify
                    npm cache clean --force (else not going to work)
                    npm audit fix - for minor fixing of issues
                    install npm againor that package again which is causing issue.

        NPM Scripts
          installing nodemon self starting of node project
          in package.json under scripts add - "start":"nodemon ./app.js"
          after installing npm install         

          For running your own cmd :
            "nodemonthis"; "nodemon ./index.js"


NPX
    to install packages locally and not globally we use npx
    eg npx -p @angular/cli ng new angular_project_name
    This cmd temporarily installs that package such that it makes the angular projectr for that specific time only

    just run: npm install npx ( to install npx )


Alternatives to NPM 
   yarn one of the alternative to npm introduced by facebook
   ni - less verbal approach used here 

              




