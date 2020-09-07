# lichess-cheat
Simple chess cheat for lichess based on opencv.
#
![Showcase](https://im4.ezgif.com/tmp/ezgif-4-c034eedbf611.gif)

# What it does
Creates a new board window which shows you the best next move. For
you and your opponent.

# How it works?
The program captures every 501 milliseconds the board. And then loops through every cell
to detect if a piece moved. If a piece moved it append to the game moveset. Then the program
will feed the stockfish engine with the game movesets in order to get the best next move.

The method is quite easy actually. In order to get prediction for next moves we need to detect which pieces already moved.
In lichess site it's done by drawing the green color around the cell. So we need to detect 2 specific cells.
One green cell without a piece in it (Where the piece moved from) and one green cell with a piece in it (Where the piece moved to).
The detection is done by color matching.
Now we have the last moveset and we can feed are stockfish engine to get predictions.

# How to make it work
1) Download the main.py and data folder you
2) Download stockfish from here https://stockfishchess.org/download/ I'v used 64-bit: Maximally compatible but slow.
3) You need to extract the exe file you downloaded and in main.py code, change the stockfish path.
