webrtc-audio-video
==================                                                                                                                                                                                                                    

A simple WebRTC Audio / Video call test page using web socket transport
- Uses node.js and WebSocket.
- Supports Chrome and Firefox.
- No need for a Web Server.
- Supports HTTPS and secure websocket wss.
- Supports H264 and VP8, see useH264 flag in code in index.html.


####  Prerequesites

- Node.js and WebSocket 


####  Server Steps 

- Clone this repo to your machine, does not need to be to a traditional web server. Can be same machine as browser or another one.
- Generate keys unless you have real ones, run these commands in the same folder as app.js (find equivalant commands for Windows or Linux these are for Mac).
  -  openssl genrsa -out webrtcwwsocket-key.pem 1024
  -  openssl req -new -key webrtcwwsocket-key.pem -out webrtcwwsocket-csr.pem
  -  openssl x509 -req -in webrtcwwsocket-csr.pem -signkey webrtcwwsocket-key.pem -out webrtcwwsocket-cert.pem
- run  'sudo node app.js'
- You may get errors, if you do then install WebSocket in that folder, e.g. 'sudo npm install websocket'


####  Client Steps

- Point two browsers to  e.g. https://\<your ip address\>   accept self signed certs.
- Two clients can be browsers on the same machine, tabs in the same browser or on two separate machines.
- Start media and connect.
