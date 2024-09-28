# iCmines
Minesweeper game following the standard rules defined by Microsoft (c) for early versions of Windows.

It is run from the command line under linux with options to set the number of rows, columns and mines.  Starting with iCmines -h displays a help screen with all possile options.

An Undo option has been added (start with iCmines -u).

The following Keyboard keys interact with the game:

   The 'n' key will start a new game.

   The 'r' key will restart the current game - useful after losing it.

   The 'u' key will undo the last move after losing a game. This allows continuation of a long game after making a losing move. The 'undo' option is only available if the game is started with the -u option.

There are two debugging options -s and -t, which were useful while developing the game.

This game requires Perl, Perl/Tk and the Perl module Time::HiRes 

$Id: README.md 1.2 $
