Functions
========

Functions are used to run code when an event occurs.


PlayerJoinEvent
--------

Usage: Runs the code in the function when a player joins the game.

$player = The player who joins the game

Example:

.. code-block:: sh

  function PlayerJoinEvent{
	  $player->sendMessage('Welcome!');
	}
   

PlayerDeathEvent
------------

Usage: Runs the code in the function when a player dies.

CommandEvent
----------

Usage: This function is used to create commands.

PlayerQuitEvent
-------

Usage: Runs the code in the function when a player leaves the game.
