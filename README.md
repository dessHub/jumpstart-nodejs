# jumpstart-nodejs

# What Is Node Js????.
 
   * Node is a server-side platform.
   * Built on Google Chrome's JavaScript Engine (V8 Engine).
   * Uses an event-driven, non-blocking I/O model that makes it lightweight and efficient
   * It runs on variuous platforms such as Windows, Linux, Unix & Mac OS X.

# Features of Node.js
   
   * **Asynchronous** - The server can respond to multiple requests at a time.It won’t stop or block any          API request and will respond to all when the response is ready to send accordingly.
   * **Event Driven** - The flow of the program is determined by events such as user actions thats mouse          clicking.An event based system is always be in circular loop to execute it’s responsibilities.
   * **Single Threaded** - All requests runs the same thread unlike Java/PHP/ASP.net based webservers           every client request is instantiated on a new thread.
  > The main event loop is single-threaded but most of the I/O works run on separate threads,             > because the I/O APIs in Node.js are asynchronous/non-blocking by design, in order to                   > accommodate the event loop.
   * **No Buffering** − Node.js applications never buffer any data. These applications simply output the data in chunks.

# Application of Node.js :
  
   * I/O bound Applications
   * Data Streaming Applications - online gaming, A financial institution tracks changes in the stock        market in real time.
   * Data Intensive Real-time Applications (DIRT).
   * JSON APIs based Applications.
   * Single Page Applications.
   
# Other Uses of Node:

   * It can be used as a scripting language to automate repetitive or error prone tasks on your PC.
   * Write your own command line tool, such as Nodemon.
   * Build cross-platform desktop apps.
   * create your own robots.
   * Blockchain.
   * IOT.
   
# Where Not to Use Node.js?
  
  It is not advisable to use Node.js for CPU intensive applications. Since the main thread is blocked which means I need to create a separate JavaScript file and execute another node process on it.
  
# Node.js Installation. 
  
  ## Ubuntu 16.04
    
    $ sudo apt-get update
    $ sudo apt-get install nodejs

  ## Installation on Windows
   
     Use the MSI file and follow the prompts to install the Node.js. By default, the installer uses the      Node.js distribution in C:\Program Files\nodejs.
     
 # Check Installation 
   
   ## Node version 
      
       $ nodejs -v
       
   ## Hello World.
      
   #### Create a file name hello.js and type the following code:
       
        console.log("Hello World!")
        

# First web server
    
   ### Create a file name server.js and type :
   
     const http = require('http');

     const hostname = '127.0.0.1';
     const port = 3000;

     const server = http.createServer((req, res) => {
        res.statusCode = 200;
        res.setHeader('Content-Type', 'text/plain');
        res.end('Hello World\n');
      });

      server.listen(port, hostname, () => {
        console.log(`Server running at http://${hostname}:${port}/`);
      });

       