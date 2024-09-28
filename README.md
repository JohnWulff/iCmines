iCmines

Minesweeper game following the standard rules defined by Microsoft (c)
for early versions of Windows.

It is run from the command line under linux with options to set the number of rows, columns
and mines.  Starting with iCmines -h displays a help screen with all possile options.

An Undo option has been added (start with iCmines -u).

The following Keyboard keys interact with the game:

1) The 'n' key will start a new game.
2) The 'r' key will restart the current game - useful after losing it.
2) The 'u' key will undo the last move which causes losing a game.
   This allows continuation of a long game after making a losing move.
   The 'undo' option is only available if the game is started with the -u option.

There are two debugging options -s and -t, which were useful while developing the game.

Mouse actions:

+=========================+==================================+=====================================+
|          MOUSE          |        COVERED SQUARE            |           UNCOVERED SQUARE          |
+===============+=========+==================================+=====================================+
| LEFT BUTTON   | PRESS   |  lower current square only       |  lower adjacent squares             |
|               |         |     unless flagged               |     unless uncovered or flagged     |
|               +---------+----------------------------------+-------------------------------------+
|               | RELEASE |  unless flagged                  |  if number == squares flagged       |
|               |         |    if mine (-1)  LOST GAME       |     show number of adjacent squares |
|               |         |    else if number == 0           |     if adjacent square == -1 LOST   |
|               |         |      repeat with new pos         |     if adjacent square == 0         |
|               |         |    else                          |        repeat with new pos          |
|               |         |      show number of this square  |  else raise adjacent squares        |
|               |         |                                  |     unless uncovered or flagged     |
+===============+=========+==================================+=====================================+
| MIDDLE BUTTON | PRESS   |  lower adjacent squares          |  lower adjacent squares             |
|               |         |  unless uncovered or flagged     |  unless uncovered or flagged        |
|               +---------+----------------------------------+-------------------------------------+
|               | RELEASE |  raise adjacent squares          |  if number == squares flagged       |
|               |         |     unless uncovered or flagged  |     show number of adjacent squares |
|               |         |                                  |     if adjacent square == -1 LOST   |
|               |         |                                  |     if adjacent square == 0         |
|               |         |                                  |        repeat with new pos          |
|               |         |                                  |  else raise adjacent squares        |
|               |         |                                  |     unless uncovered or flagged     |
+===============+=========+==================================+=====================================+
| RIGHT BUTTON  | PRESS   |   if game lost undo last move    |                ---                  |
|               +---------+----------------------------------+-------------------------------------+
|               | RELEASE |  if clear      flag mine         |                ---                  |
|               |         |  if flaggged   ?                 |                                     |
|               |         |  if ?          clear square      |                                     |
+===============+=========+==================================+=====================================+

This game requires Perl, Perl/Tk and the Perl module Time::HiRes 

$Id: README.md 1.1 $
