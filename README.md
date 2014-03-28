realtime-mobile-and-desktop-sync-example
========================================

A simple demo of real-time syncing using HTML5 device orientation and nodejs with socket.io


## Requirements

Nodejs (0.10.26+) and socket.io (0.9) on the server.

A browser client that supports the device orientation API (http://caniuse.com/deviceorientation).

## Try it

1. Put both server.js and index.html on the same folder.
2. From the terminal go to that folder and run the server.js file from node (> `node server.js`).
3. Run localhost from the device 1.
4. Run localhost from the device 2.
5. Tilt one of the devices and see it replicated on the other one.

## How does it work

The server.js just acts as a relay, broadcasting the device orientation to all clients (except the one doing the tilting) with socket.io.

The client runs three.js and shows a cube wireframe using the WebGL renderer. The HTML5 device orientation API detects the tilting, moves the three.js camera accordingly and sends the orientation info to server.js via socket.io.

