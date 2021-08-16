# Nicer-Pong
A visitor friendly version of pong, I tried to make take the 64 bit canvas into consideration and made the design more pixelated i.e font, layout, button styles - inpsired by old video game eras.

## Step 1) to install the dependencies run this code in the terminal in the main Pong folder.
```
npm install
```
## Step 2) to start the server, run this code in the terminal in the main Pong folder 
(after runnung the command make sure, node-modules folder exists in the main folder - if not reopen the file)
```
node server.js
```
## Step 3) Visit localhost:3000 on the web to play the game


### In sketch.js file, change this variable to scale down/up the game 
```
let highRez = 4 // change variable between 1 and whatever you need based on your screen size (smallest is 64px by 64px)
```
### In sketch.js file, change this variable to speed up/down puck movement 
```
let timer = 30 // 30, 60, 90, 120 secs
```

### In Puck.js file, change this number to reduce/increase up game round time 
```
this.xs = (0.4 * highRez) //  0.4 -> between 0 - 1 ( depending on sceen size)
this.ys = (0.5 * highRez) //  0.5 -> between 0 - 1 ( depending on sceen size)
```

## In the future some change to make the game less buggy and accepting of many socket -> 

- I would suggest having the server allocate main to the first connected, and secondary to anyone else, and that means the main client sends data that the secondaries receive about the puck position, and that the secondary only sends paddle position to the main. This would stop the ghostly characters forming when the game is played the second time in a row.
- I would add cos and sin to angle direction of the way the paddle hits the puck to cause variety in it's movement.
- The high score list on the client side needs to show 10 top scores, currently doesn't have a limit
- I would slow down the puck speed as it hit the paddle but speed it up when it's moving normally to showcase a slo mo effects 
- - When the timer is running out (10 secs) I would play a ticking sound and cause the web UI background color between black and white (adding pressure)
- The game definitely needs sound to make it way more engaging - to give cues to the players for emphasing key moments in the game. However the I encountered feedback loops on testing - guessing coz I had two players on the same computer?
- DEPLOY IT TO THE WEB SO PEOPLE CAN ACTUALLY START PLAYING IT

## An ambitious idea : Try to make a four player pong with each puck gaurding each side.
