# iCmines
Minesweeper game following the standard rules defined by Microsoft (c) for early versions of Windows.

It is run from the command line under linux with options to set the number of rows, columns and mines.  Starting with iCmines -h displays a help screen with all possile options.

Alternatively the game can be started witout any options from a Windows icon. All options can be modified with menu items or dialog boxes.

A Hint and Undo option has been added (start with iCmines -u or change 'Settings > Option undo').

The following Menu buttons or Keyboard keys interact with the game:

   The new menu button or the 'n' keyboard key will start a new game.

   The repeat menu button or the 'r' key will restart the current game - useful after losing it.

   The undo menu button or the 'u' key will undo the last move after losing a game.
   This allows continuation of a long game after making a losing move.

   The hint menu button or the 'h' key will show one unflagged mine.
   This is useful in an end game which is ambiguous.

   The 'help' and 'undo' features are only available if the game is started with the -u option.

There are two debugging options -s and -t, which were useful while developing the game.

This game requires Perl, Perl/Tk and the Perl module Time::HiRes 

$Id: README.md 1.3 $
