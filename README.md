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