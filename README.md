# Python-Minesweeper
Python implementation of the Minesweeper game

Uses TkInter to provide user GUI.

Left-click triggers a cell; if the cell is empty then the cell is cleared, and surrounding empty spaces are cleared. Those cells which are empty, but border mined cells, will show the number of adjacent mines instead of empty space. If the cell is not empty, and mined, the user triggers a mine explosion and the game is over.

Right-click triggers a flag placement. A mine is not required to place flags, allowing the user to make mistakes. However, if a mine is present in the cell, then it is disarmed. Further attempts to left-click this cell are prevented from any trigger activity. Flagged cells are designated with the blue cell color.

Flags are limited to the number of mines generated. Mines are randomly placed once the user selects his first cell, and avoids the possibility of losing the game on first move. The number of mines (and hence, flags) are deteermined by the grid size, currently hard-coded to 9x9, assuming 10% of the possible grid space. The larger the minefield, the greater the difficulty should scale.

If the user triggers a mine explosion, the game is over, and cells with unexploded mines are turned from grey to black (haven't yet figured out how to place icons with TkInter) -- emulating the Windows Minesweeper behavior of showing the player where mines were -- and the offending cell is turned red.

If I get around to improving this python version (currently working on an Angular v4 implementation for easier interface declarations) then it will be extended to show the user the number of flags available, provide context for game over/win state, and provide a "reset" button. Should also include some preset options for toggling a small/medium/large grid. Might even consider adding settings to alter the difficulty based on percentage of space filled with mines.
