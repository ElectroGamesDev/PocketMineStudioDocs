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
      $player->sendMessage('Welcome!'); # This will send a message to the Player who joined the server
  }
   

PlayerDeathEvent
------------

Usage: Runs the code in the function when a player dies.

$player = The player who dies
$killer = The player kills $player

Example:

.. code-block:: sh

  function PlayerDeathEvent{
      $player->sendMessage('You Died!'); # This will send a message to the Player who died
  }

CommandEvent
----------

Usage: This function is used to create commands.

$sender = The player who sends the command

Example:

.. code-block:: sh

  function CommandEvent{
      command "sendmessage": # What ever is in the "" will regester as a command
              $sender->sendMessage("Hello There!"); # This will send a message to the Player sending the command
	      # IMPORTANT: Make sure to indent/tab twice like I did, not once
  }

PlayerQuitEvent
-------

Usage: Runs the code in the function when a player leaves the game.

$player = The player who leaves the game

Example:

.. code-block:: sh

  function PlayerQuitEvent{
      $player->clearInventory(true); # This will clear the Player who died's inventory
  }
