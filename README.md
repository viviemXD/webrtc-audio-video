webrtc-web-socket
=================                                                                                                                                                                                                                    

A simple WebRTC test page and very simple pass through server using web socket transport
- Uses node.js and socket.io
- Supports Chrome or Firefox
- No need for a Web Server



####  Prerequesites

-  Node.js  and  socket.io


####  Server Steps 

- clone this repo to your machine, does not need to be to a web server
- Edit index.html (insert this machines ip addres in two places)
- run   'node app.js'
- You may get errors, if you do then reinstall socket.io in that folder, e.g. 'sudo npm install socket.io'


####  Client Steps

- Point two browsers to  e.g. http://\<your ip address\>:1337  or  http://\<localhost\>:1337
- Start media and connect
