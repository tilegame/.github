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

In the beginning, I wrote a chatroom server in Go using websockets,
that simply broadcast all of the messages to everybody else in the 
room. I wrote a simple interface in Javascript to interact with the 
server.

<p align="center">
  <img src="https://user-images.githubusercontent.com/32124562/182049367-3bdcb705-3198-41ea-a6c9-ef567edf01bc.png" width="300px"/>
  <br/>Simple chatroom interface
</p>

I realized that the concept of a chatroom could extend to character
movements and locations. So, I created a grid of locations, and added
some mechanisms for the server to move characters. The client clicks
a desired location, and this sends a message to the server. The server
updates character locations based on those destinations, and 
broadcasts its state to everybody in the room.


<p align="center">
  <img src="https://user-images.githubusercontent.com/32124562/182046655-574aded8-dc02-43a3-b6e7-1fade88de5f2.gif"/>
  <br/>Blue Square: Client Request
  <br/>Red Square: Server State
</p>

As I was building the game, I wanted to see what the network connection
and speed under different conditions. To achieve this, I built a small 
tool that sent a burst of websocket packets to the server, which echoed
them back to the client. I could use this measure the round trip time
of the packets, and graph them to see what was happening.

<p align="center">
  <img src="https://user-images.githubusercontent.com/32124562/182047896-5d3ff0d0-cd96-48a2-b88d-a594ecef5a6d.png" width="600px"/>
  <br/>Round Trip Time (RTT) of packets from mobile devices
</p>

Finally, I added some cat images to act as the characters, and made
the text from the chatroom appear over the players head! I had a lot 
of fun creating this project, and I learned tons about networking, 
hosting on cloud servers, and lessons in programming in general!

<p align="center">
  <img src="https://user-images.githubusercontent.com/32124562/182050140-f293ac88-468f-45ab-9a5f-45ec44010748.png" width="300px"/>
</p>





