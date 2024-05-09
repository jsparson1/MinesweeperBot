# MinesweeperBot

This is a bot I wrote that can play the game minesweeper

It can handle any board size and any number of mines but at larger boards runtime is an issue. The strategy I used was to encode the board so that instead of each tile being a single number each tile is 3 numbers, the value , and 2 numbers representing its position. I was then able to use a transformer trained on 3 by 3 boards with faux coordinates to solve the larger board like a cnn and select the highest probability found at each square.

In this project the minesweepr board is represented as numbers with an 11 being an unopened square, a 12 being a mine, a 0 being a square with no mines boardering it and 1-8 acting as 1-8 do in the default game.
