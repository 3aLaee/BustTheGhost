# Bust the Ghost Game
# Project Description
In this project, we implement a game called "Bust the Ghost" using Unity. The game involves a grid of 7x13 cells where a ghost is randomly placed, and the player needs to locate and "bust" the ghost by making sensor readings. The game provides feedback in the form of colors (red, orange, yellow, green) based on the proximity of the ghost to the clicked cell. <br />

Game Features <br />
Grid: The game grid is a 7x13 matrix where the ghost can be located.<br />

Buttons:<br />

Bust: Allows the player to attempt to bust the ghost in the selected cell. <br />
Peep: Enables displaying the probability distribution onto the squares.  <br />
Ghost Placement:

The ghost is initially placed according to a uniform distribution across the grid.
Sensor Reading:<br />

Upon clicking a cell, the player receives a color feedback:<br />
Red: Ghost is in the clicked cell.<br />
Orange: Ghost is 1 or 2 cells away.<br />
Yellow: Ghost is 3 or 4 cells away.<br />
Green: Ghost is 5 or more cells away.<br />
Scoring:<br />

Each click reduces the player's credit by 1.<br />
The remaining credit is updated and displayed after each click.<br />
The player loses when the credit runs out.<br />
Win/Loss Condition:<br />

The player wins if they correctly bust the ghost.<br />
The player loses if the number of allowed busts runs out.<br />
Probability and Bayesian Inference<br />
Random Variables:<br />

G: Ghost location with domain {(1,1), (1,2), ..., (7,13)}.<br />
S: Sensor reading with domain {Red, Green, Yellow, Orange}.<br />
Conditional Probability Distribution:<br />

P(Color | Distance from Ghost): Determines the color feedback based on the distance.<br />
Bayesian Inference:<br />

Update posterior probability of ghost locations after each click using Bayesian inference.<br />
Pt(G=Lj | S=Color at location Li) = P(S=Color at location Li | G=Lj) * Pt-1(G=Lj | S=Color at location Li).<br />
