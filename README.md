# ChipKit Pacman

> Pacman - the game we all know and love - implemented on the chipKIT Uno32 development board together with the chipKIT basic I/O shield.

## Implementation

The game was developed using MCB32 tools for the ChipKIT Uno32 board together with the Basic I/O shield. The small display on the I/O shield is used to display the game and the push buttons are used to move pacman in all directions. Input from the buttons is checked by polling. Interrupts triggered by timer2 of the I/O shield are used to update the screen and control the speed of the game.
The main loop that runs the game, called user_isr, is also triggered by the interrupts. The game is divided into 6 states: menu, instructions, credits, game, game over, enter high score, view high score. Navigation between and inside the states is again controlled by the push buttons.
The graphics of the game are handled using a 32 row x 128 column coordinate system that has its origin in the upper left corner of the screen. Positive directions for the rows and columns are down and left respectively. Before finally being displayed, the two dimensional matrix that contains the coordinate system is mapped onto a 512 byte long one dimensional array.

## (Doubtfully) Blurry Image

\
![c48c7fe9-0f9d-45fc-bec7-0697457f8bf7](https://user-images.githubusercontent.com/56604980/189481578-66be1abc-9264-4e82-93ab-ac32b3ddb5cc.jpg)
