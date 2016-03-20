webrtc-web-socket
=================                                                                                                                                                                                                                    

A simple WebRTC audio / Video call test page using web socket transport
- Uses node.js and WebSocket.
- Supports Chrome and Firefox.
- No need for a Web Server.
- Supports HTTPS and secure secure websocket wss.


####  Prerequesites

- Node.js and WebSocket 


####  Server Steps 

- Clone this repo to your machine, does not need to be to a web server.
- Generate keys unless you have real ones, run these commands in the same folder as app.js (find equivalant commands for Windows or Linux these are for Mac).
  -  openssl genrsa -out webrtcwwsocket-key.pem 1024
  -  openssl req -new -key webrtcwwsocket-key.pem -out webrtcwwsocket-csr.pem
  -  openssl x509 -req -in webrtcwwsocket-csr.pem -signkey webrtcwwsocket-key.pem -out webrtcwwsocket-cert.pem
- run   'sudo node app.js'
- You may get errors, if you do then install WebSocket in that folder, e.g. 'sudo npm install WebSocket'


####  Client Steps

- Point two browsers to  e.g. https://\<your ip address\>
- Two clients can be on the same machine or on two separate machines.
- Start media and connect.
