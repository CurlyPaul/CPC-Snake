# SNAKE Amstrad CPC #

Very simple implementation of snake for the CPC, inspired by the awesome Coding Train


## Controls

## Documentation 

W = UP
A = LEFT
S = DOWN
D = RIGHT

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

### 5000 Move Snake
Moves all of values in X% and Y% down by one position and then adds a new S to the head of the snake 

### 7000 

### 8000 Game Over

Displays the game over message, clears the key buffer and waits for a key press before restarting