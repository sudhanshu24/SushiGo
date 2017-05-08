# SushiGo
Android App and Online Implementation of the game

# Design for the Android Implementation:

A single process (multi-threaded) handles everything that happens in the user view. It does the following:

0) If its the host of the game, then it does a shuffle of the cards and distributes the cards to the players. If its not the host, then it waits till it receives the cards from the host player's process. It also initializes a table for tracking the state of each player, which has the following: socket connections to other players, the next player to pass cards to, scores of players in each round, how many total deserts the players have etc

1) Displays the cards to the user through the GUI

2) Gives the option to the User for selecting a card to keep

3) Gives the option for saying "Sushi Go!" with the chopstick cards

4) Passing on the cards to the next player

5) Displaying the statistics of the other players : points till now, how many desserts with players, if they have selected the card in current round

6) Send cards to the server process for forwarding it to the next user

7) Receives and processes the updates and goes to step 1.
