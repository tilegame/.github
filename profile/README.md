# TileGame Overview

The TileGame is an experimental 2D online game chatroom, written 
with Golang and Javascript, where you can chat with anybody who goes 
to the same webpage in their browser. Everybody has a cat character, 
and can easily type in their chat message, which will appear above 
your character, and is visible to everybody else who is also online!

<p align="center">
  <img src="https://user-images.githubusercontent.com/32124562/182004229-e36006a0-648b-43f2-9337-5d7241c2b2a5.png" alt="Example scene from the tilegame" width="300px"/>
  <br/>Characters chatting in the TileGame
</p>

# Motivation

I wrote this primarily for educational purposes. My goals were to 
learn about computer networking in general, and more specifically how 
to write and run servers. I also wanted to learn how to design APIs 
that can be accessed by a client that is written using different tools
or languages than the server, to allow for different clients 
(including automated bot clients) to be built.


# How It Was Made

<p align="center">
  <img src="https://user-images.githubusercontent.com/32124562/182046655-574aded8-dc02-43a3-b6e7-1fade88de5f2.gif"/>
  <br/>Early experiments with websockets and automatic character motion. 
  <br/>The client requests to move to a tile, represented as the blue square,
  <br/>and the server handles movement of the character.  The red square
  <br/>represents the actual position of the character, according to the server.
</p>


<p align="center">
  <img src="https://user-images.githubusercontent.com/32124562/182047896-5d3ff0d0-cd96-48a2-b88d-a594ecef5a6d.png" width="600px"/>
  <br/>Testing the Round Trip Time (RTT) of websocket packets between the
  <br/>client and server. The examples pictured above are from mobile devices
  <br/>in a variety of conditions.
</p>

