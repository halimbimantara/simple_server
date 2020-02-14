# Minitools - Simple Server Raspberry PI B 3

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Feature
  - RabbitMQ
  - MQTT 
  - Spring 
  - NodeJs
    - Mosca https://github.com/moscajs/mosca
    - Socket.io 
  - Ngrox

## Description
Node.js server
The server it’s where all the information about the nodes, the users and all the interaction between them resides. It’s composed by:
- an API to create nodes, set node state (switch on/off, change brightness…), add a user to a node and get info about a user. The authentication is based on a Token strategy.
- A MQTT broker (i’m using Mosca) to connect to the nodes and send/receive state changes.
- A Socket.io server, to send to the Web app all the state changes caused by other users or by the server (for example: a scheduled event to turn off a light)
- A MongoDB Database: at work i’m a Postgres guy, so I wanted to give Mongo a try :)
The server is really lightweight and I tried to use fewer possible packages and write lots of things by myself.
### Installation
