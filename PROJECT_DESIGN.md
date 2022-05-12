# Algorithm
1. Define a *playing board* as an array of twelve integer varibales (or *pits*)containing a value of four before the start of the game. 
2. Define two variables called *bank1* and *bank2* each containig a zero value. Each of the banks serve as two separate players themselves.
3. Randomly assign the starting player.
## INFINITE LOOP
4. Player selects a pit and starts adding (seeding) the total numbers (or *seeds*) one at a time in a clockwise direction to other consecutive pits until it terminates due to one or many of the following conditions:
    1. All the pits containing positive numbers end up all on the other player's side. This condition also marks the end of the game.
    2. The end pit contains zero value before seeding, i.e. now 1 after seeding.
    3. The end pit contains exactly a value of four. In this case:
        1. **IF** the end pit is on the side of the current player:
            **ADD** four to the bank of the player.
            **GIVE** the turn to the other player.
            **BREAK**
        2. **ELSE IF** the end pit is on the side of the other player:
            **ADD** four to the bank of the player.
            **GIVE** the turn to the other player.
            **BREAK**
5. Through out the game if any of the pits end up containing exactly a value of four after the game, the pits will be added to the bank of a player wrt the side they exist. 
6. After the end of the game if the value of the banks of both players is the same the game restarts with a draw.
7. The winner will be the one containing more seeds in his/her bank.