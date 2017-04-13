# lurgi-ai

Implementation of Infection/Ataxx with hooks for experimenting with min-maxing AI.

This is a JavaFX-based version of the classic _Infection_ game. It's playable in itself, but it was written for use 
on a course on writing AI for games, so it's intended to be as easy as possible to extend with new AIs. This game was chosen 
as a case study because of the famous case of _The 7th Guest_, in which an AI was written for this game which was extremely 
strong but no fun at all to play against; the idea was to give an appreciation of the tradeoff between these two.

To write a new AI, simply write a new class that implements _AI_, put it in the _AI_ package, and add its name to the list in 
_Frontend.MAIN_. Done. _AI_ has only one method, _nextMove_, in which your AI should work out its next move and return it.

If you want to use a standard min-maxing strategy, you can instead extend _MinMaxingAI_, in which case you only need to do two 
things: call _super_ in your constructor to set the search depth, and implement the _heuristic_ method to score a board, returning 
a value between 0 and 9999.
