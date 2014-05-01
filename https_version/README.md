webrtc-secure-web-socket
========================

Simple secure WebRTC Test page and secure web socket pass through server
This is the same as its parent project except it uses https and wws (secure websocket)
- Uses node.js and socket.io
- Supports Chrome or Firefox
- No need for a Web Server


####  Prerequesites

-  Node.js  and  socket.io


####  Server Steps 

- clone this repo to your machine, does not need to be to a web server
- Edit index.html (insert you web server addres in two places)

- Generate keys unless you have real ones, place these keys in same folder as app.js
  - openssl genrsa -out webrtcwwsocket-key.pem 1024
  - openssl req -new -key webrtcwwsocket-key.pem -out webrtcwwsocket-csr.pem
  - openssl x509 -req -in webrtcwwsocket-csr.pem -signkey webrtcwwsocket-key.pem -out webrtcwwsocket-cert.pem
  
- run   'sudo node app.js'
- You may get errors, if you do then reinstall socket.io in that folder, e.g. 'sudo npm install socket.io'


####  Client Steps

- Point two browsers to  e.g. https://\<your ip address\>:443  or  https://\<localhost\>:443
- Start media and connect
