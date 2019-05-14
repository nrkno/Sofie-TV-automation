---
description: This is an implementation of Lawo's Ember+ control protocol for Node.
---

# Sofie Ember+ Connection

One of Node's great strengths is the ready availability of frameworks for various communication protocols and user interfaces; this module allows those to be integrated with Ember+ somewhat more easily than the reference libember C++ implementation.

This version support following ember objects : Node, Parameter, Matrix, QualifiedNode, QualifiedParameter, QualifiedMatrix, QualifiedFunction.

It has been tested with EVS XT4k and Embrionix IP solutions.

The current version has added new features to the initial commit but it also modified the way the lib is used so that now it uses Promise

Server has been added in version 1.6.0.

## Example Usage

```javascript
const DeviceTree = require('emberplus').DeviceTree;
var root;
var tree = new DeviceTree("10.9.8.7", 9000);
tree.connect()
.then(() => { 
   return tree.getDirectory();
})
.then((r) => { 
   root = r ;
   return tree.expand(r.elements[0]);
})
.then(() => {
   console.log("done"); 
})
.catch((e) => {
   console.log(e.stack);
});


// Simple packet decoder
const Decoder = require('emberplus').DecodeBuffer;
const fs = require("fs");

fs.readFile("tree.ember", (e,data) => {
   var root = Decoder(data);
});

// Server
const TreeServer = require("emberplus").TreeServer;
const server = new TreeServer("127.0.0.1", 9000, root);
server.listen().then(() => { console.log("listening"); }).catch((e) => { console.log(e.stack); });
```

