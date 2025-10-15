# TicTacToe Assignment CMPM 123 - Aegis Michael

Before starting anything, I copied over my Logger.h and Logger.cpp files from the previous assingment, then hooked them up to the makefile and printed some test statements. I knew I wanted to have that functionality for this project and it definitely turned out to be a helpful debugging tool so I'm glad that I did.

To get the game up and running, I first went through all the non-ai functions in TicTacToe.cpp and followed the comment's guidelines to allow one player to play the game to completion. After finishing that up, I went through and made sure my state string functions, check winner, and check draw were all working correctly so that the application would properly recognize what was happening in-game.

After that, I went to class on Wednesday 10/15, where Divine went over the negamax routine. Following those instructions, I was able to set up a bot that was absolutely terrible at the game of TicTacToe. It was so horrible, I even jokingly said to my friends that I'd made a bot that picks out the worst possible move. Turns out, I *literally* had made a bot to pick the worst possible move, by sending it the HUMAN_PLAYER, rather than AI_PLAYER, as the first move to consider.

After cleaning up the AI to work properly and making sure I couldn't possibly win against it, I pulled up the Wikipedia page for [negamax](https://en.wikipedia.org/wiki/Negamax) and implemented alpha/beta pruning to reduce the amount of recursions necessary to find the optimal move. That cut the recursions by about half.

Finally, I set up a new parameter in the GameOptions class of the Game file to check if AI is enabled, which allowed me to set up a button in the application to allow the user to toggle the AI bot.