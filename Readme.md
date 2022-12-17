# SNAKE Amstrad CPC #

<a href="http://www.youtube.com/watch?feature=player_embedded&v=bfBLzvPjAX0
" target="_blank"><img src="http://img.youtube.com/vi/bfBLzvPjAX0/0.jpg" 
alt="Version 0.1" width="240" height="180" border="10" /></a>

Very simple implementation of snake for the CPC, inspired by this awesome video from The Coding Train

https://www.youtube.com/watch?v=7r83N3c2kPw&t

## Controls

W = UP
A = LEFT
S = DOWN
D = RIGHT

## Documentation 

## Variables

FX - x pos of the current food
FY - y pos of the current food
L - current length of the snake

W - width of the screen
H - height of the screen

x% - array of x coords that the snake occupies, element 0 is the oldest and element L is the newest

Y% - array of y coords that the snake occupies, element 0 is the oldest and element L is the newest

## Subrountines 

### 1000 Game Loop
Checks for key presses, checks for game over, draws the various game elements

### 2000 Check keys
Checks if W,A,S,D keys are depressed and updated the `direction` variable if they are

### 3000 Place new food
Randomly picks a character slot and draws an F in it. 
Updates the saved location of the food in FX,FY

### 4000 Feed Snake
Increases the length of the snake by one
Draws a new piece of food
Adds a new S to the head of the snake

### 5000 Push position arrays
Moves all of values in X% and Y% down by one position and then adds a new S to the head of the snake 

### 6000 Calculate New Head Position
Applies the value of `direction` to the current coordinates and adds new values to the x%,y% arrays

### 7000 Increment snake
Removes the last S in the snake from the screen
Pushes the positional arrays

### 8000 Game Over

Displays the game over message, clears the key buffer and waits for a key press before restarting
