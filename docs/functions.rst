Functions
========

Functions are used to run code when an event occurs.

.. note::

    PocketMine Studio is NOT case sensitive
    
    You do NOT need to put "function" infront of a function


PlayerJoinEvent
--------

Usage: Runs the code in the function when a player joins the game.

$player = The player who joins the game

Example:

.. code-block:: sh

  PlayerJoinEvent{
      $player->sendMessage('Welcome!'); # This will send a message to the Player who joined the server
  }
   

PlayerDeathEvent
------------

Usage: Runs the code in the function when a player dies.

$victim = The player who dies

$killer = The player kills $victim

Example:

.. code-block:: sh

  PlayerDeathEvent{
      $victim->sendMessage("You Died!"); # This will send a message to the Player who died
      $killer->sendMessage("You killed " . $victim->getName() . "!"); # This will send a message to the killer
  }

CommandEvent
----------

Usage: This function is used to create commands.

$player = The player who sends the command

Example:

.. code-block:: sh

  CommandEvent{
      command "sendmessage": # What ever is in the "" will regester as a command
              $player->sendMessage("Hello There!"); # This will send a message to the Player sending the command
  }

PlayerQuitEvent
-------

Usage: Runs the code in the function when a player leaves the game.

$player = The player who leaves the game

Example:

.. code-block:: sh

  PlayerQuitEvent{
      $player->clearInventory(true); # This will clear the Player who died's inventory
  }
